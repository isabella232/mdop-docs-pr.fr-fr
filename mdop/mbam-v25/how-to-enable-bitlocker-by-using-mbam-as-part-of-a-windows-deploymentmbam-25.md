---
title: Comment activer BitLocker à l'aide de MBAM dans le cadre d'un déploiement Windows
description: Comment activer BitLocker à l'aide de MBAM dans le cadre d'un déploiement Windows
author: dansimp
ms.assetid: 7609ad7a-bb06-47be-b186-0a2db787c8a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 4b2cbf333c705088d0a068521fb65e99551bb1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811628"
---
# Comment activer BitLocker à l'aide de MBAM dans le cadre d'un déploiement Windows


Cet article explique comment activer BitLocker sur l’ordinateur d’un utilisateur final en utilisant MBAM dans le cadre de votre processus d’imagerie et de déploiement Windows. Si vous voyez un écran noir au démarrage (après la phase d’installation) indiquant que le lecteur ne peut pas être déverrouillé, voir les [versions antérieures de Windows ne démarrent pas après l’installation de la version préconfigurée de BitLocker et de la version 1511 de Windows 10](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo).

**Conditions préalables:**

-   Un processus de déploiement d’image Windows existant – Kit de ressources de déploiement Microsoft (MDT), Microsoft System Center Configuration Manager ou un autre outil ou processus d’imagerie doit être en place

-   Le module de plateforme sécurisée doit être activé dans le BIOS et visible par le système d’exploitation.

-   L’infrastructure de serveur MBAM doit être en place et accessible.

-   La partition système requise par BitLocker doit être créée.

-   L’ordinateur doit être joint au domaine lors de l’image avant que MBAM active entièrement BitLocker.

**Pour activer BitLocker en utilisant MBAM 2,5 SP1 dans le cadre d’un déploiement Windows**

1. Dans MBAM 2,5 SP1, l’approche recommandée d’activation de BitLocker lors d’un déploiement Windows consiste à utiliser le `Invoke-MbamClientDeployment.ps1` script PowerShell.

   -   Le script entrait à `Invoke-MbamClientDeployment.ps1` BitLocker lors du processus d’acquisition d’images. Lorsque la stratégie BitLocker l’exige, l’agent MBAM invite immédiatement l’utilisateur à entrer un code confidentiel ou un mot de passe lors de la première connexion de l’utilisateur du domaine après l’acquisition d’images.

   -   Facile à utiliser avec MDT, System Center Configuration Manager ou les processus d’imagerie autonomes

   -   Compatible avec PowerShell 2,0 ou version ultérieure

   -   Chiffrer le volume du système d’exploitation avec le protecteur de clé TPM

   -   Prise en charge complète de la configuration de la mise en service de BitLocker

   -   Vous pouvez également chiffrer FDDs

   -   Trusted GPC OwnerAuth pour Windows 7, MBAM doit être propriétaire du TPM pour le tiers de confiance.
   Pour Windows 8,1, Windows 10 RTM et Windows 10 version 1511, le fiduciaire de TRUSTed OwnerAuth est pris en charge.
   Pour Windows 10, version 1607 ou ultérieure, seules les fenêtres peuvent prendre possession du module de plateforme sécurisée. Dans addiiton, Windows ne conserve pas le mot de passe du propriétaire du TPM lors de la mise en service du module de plateforme sécurisée. Pour en savoir plus, voir [mot de passe du propriétaire du TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

   -   Clés de récupération de confiance et packages de clés de récupération

   -   Signaler l’état de cryptage immédiatement

   -   Nouveaux fournisseurs WMI

   -   Journalisation détaillée

   -   Gestion fiable des erreurs

   Vous pouvez télécharger le `Invoke-MbamClientDeployment.ps1` script à partir du [Centre de téléchargement Microsoft.com](https://www.microsoft.com/download/details.aspx?id=54439). Il s’agit du script principal qui sera appelé par votre système de déploiement pour configurer le chiffrement de lecteur BitLocker et enregistrer les clés de récupération auprès du serveur MBAM.

   **Méthodes de déploiement WMI pour MBAM:** Les méthodes WMI suivantes ont été ajoutées dans MBAM 2,5 SP1 pour prendre en charge l’activation de BitLocker à l’aide du `Invoke-MbamClientDeployment.ps1` script PowerShell.

   <a href="" id="mbam-machine-wmi-class"></a>**MBAM \ _Machine classe WMI** 
    **PrepareTpmAndEscrowOwnerAuth:** Lit le OwnerAuth TPM et l’envoie vers la base de données de récupération MBAM à l’aide du service de récupération de MBAM. Si le module de plateforme sécurisée n’est pas détenu et si la configuration automatique n’est pas activée, il génère une OwnerAuth TPM et prend la propriété. Si le problème persiste, le code d’erreur est retourné.

   **Remarques** Pour Windows 10, version 1607 ou ultérieure, seules les fenêtres peuvent prendre possession du module de plateforme sécurisée. Dans addiiton, Windows ne conserve pas le mot de passe du propriétaire du TPM lors de la mise en service du module de plateforme sécurisée. Pour en savoir plus, voir [mot de passe du propriétaire du TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

| Paramètre | Description |
| -------- | ----------- |
| RecoveryServiceEndPoint | Chaîne spécifiant le point de terminaison du service de récupération de MBAM. |

Voici une liste des messages d’erreur courants:

| Valeurs de retour courantes | Message d’erreur |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0x0) | La méthode a réussi. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | Le module de plateforme sécurisée n’est pas présent dans l’ordinateur ou est désactivé dans la configuration du BIOS. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | Le module de plateforme sécurisée n’est pas dans le bon état |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM ne peut pas prendre possession du TPM, car la configuration automatique est en attente. Réessayez une fois la configuration automatique terminée. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM ne peut pas lire la valeur d’autorisation du propriétaire du TPM. La valeur risque d’avoir été supprimée après un tiers de confiance. Sur Windows 7, MBAM ne peut pas lire la valeur si le TPM est possédé par d’autres utilisateurs. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | L’ordinateur doit être redémarré pour que le TPM soit correctement configuré. Vous devrez peut-être redémarrer l’ordinateur manuellement. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | L’ordinateur doit être arrêté et réactivé pour que le TPM soit correctement configuré. Vous devrez peut-être redémarrer l’ordinateur manuellement. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | L’accès a été refusé par le point de terminaison distant. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Le point de terminaison distant n’existe pas ou n’est pas disponible. |
| * * WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | Le point de terminaison distant n’a pas pu traiter la demande. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Le point de terminaison distant n’a pas été joignable. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Un message contenant une erreur a été reçu du point de terminaison distant. Vérifiez que vous êtes connecté au point de terminaison de service approprié. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | L’URL d’adresse de point de terminaison n’est pas valide. L’URL doit commencer par «http» ou «HTTPS». |

   **ReportStatus:** Lit l’état de conformité du volume et l’envoie vers la base de données d’état de conformité MBAM à l’aide du service de rapport d’État MBAM. L’état inclut le niveau de cryptage, le type de protecteur, l’état de protecteur et l’état de chiffrement. Si le problème persiste, le code d’erreur est retourné.

   | Paramètre | Description |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Chaîne spécifiant le point de terminaison du service de rapport d’État MBAM. |

   Voici une liste des messages d’erreur courants:

   | Valeurs de retour courantes | Message d’erreur |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0x0) | La méthode a réussi |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | L’accès a été refusé par le point de terminaison distant.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Le point de terminaison distant n’existe pas ou n’est pas disponible. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | Le point de terminaison distant n’a pas pu traiter la demande. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Le point de terminaison distant n’a pas été joignable. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Un message contenant une erreur a été reçu du point de terminaison distant. Vérifiez que vous êtes connecté au point de terminaison de service approprié. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | L’URL d’adresse de point de terminaison n’est pas valide. L’URL doit commencer par «http» ou «HTTPS». |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM \ _Volume classe WMI** **EscrowRecoveryKey:** lit le mot de passe numérique de récupération et le package de clé du volume et les envoie vers la base de données de récupération MBAM à l’aide du service de récupération de MBAM. Si le problème persiste, le code d’erreur est retourné.

   | Paramètre | Description |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Chaîne spécifiant le point de terminaison du service de récupération de MBAM. |

   Voici une liste des messages d’erreur courants:

   | Valeurs de retour courantes | Message d’erreur |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0x0) | La méthode a réussi |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | Le volume est verrouillé. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | Aucun protecteur de mot de passe numérique n’a été trouvé pour le volume. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | L’accès a été refusé par le point de terminaison distant. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Le point de terminaison distant n’existe pas ou n’est pas disponible. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | Le point de terminaison distant n’a pas pu traiter la demande. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Le point de terminaison distant n’a pas été joignable. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Un message contenant une erreur a été reçu du point de terminaison distant. Vérifiez que vous êtes connecté au point de terminaison de service approprié. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | L’URL d’adresse de point de terminaison n’est pas valide. L’URL doit commencer par «http» ou «HTTPS». |
     

2. **Déploiement d’MBAM à l’aide de Microsoft Deployment Toolkit (MDT) et PowerShell**

   1.  Dans MDT, créer un partage de déploiement ou ouvrir un partage de déploiement existant.

       **Remarque**  
       Le `Invoke-MbamClientDeployment.ps1` script PowerShell peut être utilisé avec tout processus ou outil d’imagerie. Cette section montre comment l’intégrer à l’aide de MDT, mais les étapes sont similaires à l’intégration à tout autre processus ou outil.

       **Vigilance**  
       Si vous utilisez la version préliminaire de BitLocker (WinPE) et souhaitez conserver la valeur d’autorisation du propriétaire du TPM, vous devez ajouter le `SaveWinPETpmOwnerAuth.wsf` script dans WinPE immédiatement avant le redémarrage de l’installation dans le système d’exploitation complet. **Si vous n’utilisez pas ce script, vous perdez la valeur d’autorisation du propriétaire du TPM au redémarrage.**

   2.  Copy `Invoke-MbamClientDeployment.ps1` to ** &lt; DeploymentShare &gt; \\Scripts**. Si vous utilisez la version préliminaire, copiez le `SaveWinPETpmOwnerAuth.wsf` fichier dans ** &lt; DeploymentShare &gt; \\Scripts**.

   3.  Ajoutez l’application cliente 2,5 MBAM SP1 au nœud applications du partage de déploiement.

       1.  Sous le nœud **applications** , cliquez sur **nouvelle application**.

       2.  Sélectionnez **application avec des fichiers sources**. Cliquez sur **Suivant**.

       3.  Dans **nom**de l’application, tapez «MBAM 2,5 SP1 client». Cliquez sur **Suivant**.

       4.  Accédez au répertoire contenant `MBAMClientSetup-<Version>.msi` . Cliquez sur **Suivant**.

       5.  Tapez «client 2,5 SP1 MBAM» en tant qu’annuaire à créer. Cliquez sur **Suivant**.

       6.  Entrez `msiexec /i MBAMClientSetup-<Version>.msi /quiet` sur la ligne de commande. Cliquez sur **Suivant**.

       7.  Acceptez les valeurs par défaut restantes pour terminer l’Assistant Nouvelle application.

   4.  Dans MDT, cliquez avec le bouton droit sur le nom du partage de déploiement, puis cliquez sur **Propriétés**. Cliquez sur l’onglet **règles** . Ajoutez les lignes suivantes:

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Cliquez sur OK pour fermer la fenêtre.

   5.  Sous le nœud séquences de tâches, modifiez une séquence de tâches existante utilisée pour le déploiement Windows. Si vous le souhaitez, vous pouvez créer une nouvelle séquence de tâches en cliquant avec le bouton droit sur le nœud **séquences de tâches** , en sélectionnant **nouvelle séquence de tâches**et en remplissant l’Assistant.

       Dans l’onglet **séquence de tâches** de la séquence de tâches sélectionnée, effectuez les étapes suivantes:

       1.  Dans le dossier **préinstallation** , activez l’option tâches facultatives **BitLocker (hors connexion)** si vous souhaitez que BitLocker soit activé dans WinPE, qui chiffre uniquement l’espace utilisé.

       2.  Pour persister sur le TPM OwnerAuth lors de l’utilisation de la préconditionnement, en autorisant MBAM à le faire par la suite, procédez comme suit:

           1.  Recherchez l’étape **installer le système d’exploitation** .

           2.  Étape ajouter une nouvelle **ligne de commande** après celle-ci

           3.  Nommez l’étape **Persist GPC OwnerAuth**

           4.  Définissez la ligne de commande sur `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **Remarque:** pour Windows 10, version 1607 ou ultérieure, seules les fenêtres peuvent prendre possession du module de plateforme sécurisée. Dans addiiton, Windows ne conserve pas le mot de passe du propriétaire du TPM lors de la mise en service du module de plateforme sécurisée. Pour en savoir plus, voir [mot de passe du propriétaire du TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

       3.  Dans le dossier restauration de l' **État** , supprimez la tâche **activer BitLocker** .

       4.  Dans le **dossier restauration d’État** sous **tâches personnalisées**, créez une nouvelle tâche d' **application** et nommez-la **MBAM agent**. Cliquez sur la case d’option **installer une application unique** et naviguez jusqu’à l’application cliente MBAM 2,5 SP1 précédemment créée.

       5.  Dans le dossier **restauration d’État** sous **tâches personnalisées**, créez une tâche de script d' **exécution PowerShell** (après l’étape de l’application cliente 2,5 SP1) avec les paramètres suivants (mettez à jour les paramètres en fonction de votre environnement):

           -   Nom: configurer BitLocker pour MBAM

           -   Script PowerShell: `Invoke-MbamClientDeployment.ps1`

           -   Paramètres

               <table>
               <colgroup>
               <col width="33%" />
               <col width="33%" />
               <col width="33%" />
               </colgroup>
               <tbody>
               <tr class="odd">
               <td align="left"><p>-RecoveryServiceEndpoint</p></td>
               <td align="left"><p>Requis</p></td>
               <td align="left"><p>Point de terminaison du service de récupération de MBAM</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>Facultatif</p></td>
               <td align="left"><p>Point de terminaison du service de rapport d’État MBAM</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Facultatif</p></td>
               <td align="left"><p>Méthode de chiffrement (par défaut: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifier pour chiffrer les volumes de données et les clés de récupération du volume de données (s) de confiance</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifier le délai d’exécution du chiffrement</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifier que le script de déploiement ne va pas reprendre le chiffrement suspendu</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifiez pour ignorer l’échec du tiers de confiance par le propriétaire du TPM. Il doit être utilisé dans les scénarios dans lesquels MBAM n’est pas en mesure de lire le propriétaire du TPM (par exemple, si la configuration automatique du TPM est activée).</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifiez d’ignorer l’échec du tiers de clés de récupération de volume</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifier pour ignorer l’échec du rapport d’État</p></td>
               </tr>
               </tbody>
               </table>

                 

**Pour activer BitLocker à l’aide de MBAM 2,5 ou version antérieure dans le cadre d’un déploiement Windows**

1.  Installez le client MBAM. Pour obtenir des instructions, reportez-vous à la rubrique [déploiement du client MBAM à l’aide d’une ligne de commande](how-to-deploy-the-mbam-client-by-using-a-command-line.md).

2.  Rejoignez l’ordinateur à un domaine (recommandé).

    -   Si l’ordinateur n’est pas joint à un domaine, le mot de passe de récupération n’est pas stocké dans le service de récupération de clé MBAM. Par défaut, MBAM ne permet pas d’effectuer le chiffrement, sauf si la clé de récupération peut être stockée.

    -   Si un ordinateur démarre en mode de récupération avant que la clé de récupération ne soit stockée sur le serveur MBAM, aucune méthode de récupération n’est disponible et l’ordinateur doit être reimageé.

3.  Ouvrez une invite de commandes en tant qu’administrateur, puis arrêtez le service MBAM.

4.  Définissez le service sur **Manuel** ou à **la demande** en entrant les commandes suivantes:

    **net stop mbamagent**

    **sc config mbamagent Start = Demand**

5.  Définissez les valeurs de registre de sorte que le client MBAM ignore les paramètres de stratégie de groupe et configure le chiffrement pour démarrer la durée de déploiement de Windows sur l’ordinateur client.

    **Attention**  Cette étape décrit la modification du Registre Windows. L’utilisation de l’éditeur du Registre peut être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows. Nous ne sommes pas en mesure de résoudre les problèmes résultant de l’utilisation incorrecte de l’éditeur du Registre. Utilisez l’éditeur du Registre à vos propres risques.

    1.  Définissez le module de plateforme sécurisée pour le **chiffrement du système d’exploitation**, exécutez Regedit.exe, puis importez le modèle de clé de Registre à partir de C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

    2.  Dans Regedit.exe, accédez à HKLM\\SOFTWARE\\Microsoft\\MBAM et configurez les paramètres indiqués dans le tableau suivant.

        **Remarques**  Vous pouvez définir les paramètres de stratégie de groupe ou les valeurs de Registre associées à MBAM ici. Ces paramètres remplaceront les valeurs précédemment définies.

        Paramètres de configuration des entrées de Registre

        DeploymentTime

        0 = désactivé

        1 = utiliser les paramètres de stratégie de temps de déploiement (par défaut): utilisez ce paramètre pour activer le chiffrement au moment où Windows est déployé sur l’ordinateur client.

        UseKeyRecoveryService

        0 = ne pas utiliser la clé de dépôt clé (les deux entrées de Registre suivantes ne sont pas requises dans le cas présent)

        1 = utiliser le tiers de confiance principal dans le système de récupération de clés (par défaut)

        Il s’agit du paramètre recommandé, qui permet à MBAM de stocker les clés de récupération. L’ordinateur doit pouvoir communiquer avec le service de récupération de clé MBAM. Vérifiez que l’ordinateur peut communiquer avec le service avant de continuer.

        KeyRecoveryOptions

        0 = Télécharger uniquement la clé de récupération

        1 = Télécharger la clé de récupération et le package de récupération de clé (par défaut)

        KeyRecoveryServiceEndPoint

        Définissez cette valeur sur l’URL du serveur exécutant le service de récupération de clés (par exemple, http://nom de l' &lt; ordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.


6.  Le client MBAM redémarre le système pendant le déploiement du client MBAM. Lorsque vous êtes prêt à effectuer ce redémarrage, exécutez la commande suivante à l’invite de commandes en tant qu’administrateur:

    **mbamagent de début net**

7.  Lorsque l’ordinateur redémarre, et le BIOS vous y invite, acceptez le changement de module de plateforme sécurisée.

8.  Pendant le processus d’imagerie du système d’exploitation du client Windows, lorsque vous êtes prêt à commencer le chiffrement, ouvrez une invite de commandes en tant qu’administrateur, puis tapez les commandes suivantes pour définir le démarrage sur **automatique** et redémarrer l’agent client MBAM:

    **sc config mbamagent start = auto**

    **mbamagent de début net**

9.  Pour supprimer les valeurs de registre de contournement, exécutez Regedit.exe, puis accédez à l’entrée de Registre HKLM\\SOFTWARE\\Microsoft. Cliquez avec le bouton droit sur le nœud **MBAM** , puis cliquez sur **supprimer**.

## Rubriques connexes

[Déploiement du client MBAM2.5](deploying-the-mbam-25-client.md)

[Planification du déploiement de clients MBAM2.5](planning-for-mbam-25-client-deployment.md)

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

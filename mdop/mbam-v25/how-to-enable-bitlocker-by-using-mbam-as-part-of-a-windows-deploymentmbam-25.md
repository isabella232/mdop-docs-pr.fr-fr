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
ms.openlocfilehash: cd4086ca6bb2ea8d253ea3b743f4efe7efbbb6c1
ms.sourcegitcommit: 325c4b77f9a9df0f3de268457fed06184623bb94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "11626181"
---
# <a name="how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deployment"></a>Comment activer BitLocker à l'aide de MBAM dans le cadre d'un déploiement Windows

> [!IMPORTANT]
> Ces instructions ne concernent pas Configuration Manager BitLocker Management. Le `Invoke-MbamClientDeployment.ps1` script PowerShell n’est pas pris en charge pour une utilisation avec La gestion BitLocker dans Configuration Manager. Cela inclut le dépôt de clés de récupération BitLocker au cours d’une séquence de tâches configuration Manager. En outre, à partir de Configuration Manager Current Branch 2103, Configuration Manager BitLocker Management n’utilise plus le site des services de récupération de clés MBAM pour récupérer des clés. Toute tentative d’utilisation du script PowerShell avec `Invoke-MbamClientDeployment.ps1` Configuration Manager Current Branch 2103 ou une version plus nouvelle peut entraîner de graves problèmes avec le site Configuration Manager. Les problèmes connus incluent la création d’une grande quantité de stratégies ciblées sur tous les appareils, ce qui peut provoquer des tempêtes de stratégies. Cela entraîne une dégradation grave des performances dans Configuration Manager principalement dans SQL et avec des points de gestion.

Cette rubrique explique comment activer BitLocker sur l’ordinateur d’un utilisateur final à l’aide de MBAM dans le cadre de votre processus d’Windows et de déploiement. Si un écran noir s’affiche au redémarrage (après la fin de la phase d’installation) indiquant que le lecteur ne peut pas être déverrouillé, consultez les versions antérieures de Windows ne démarrent pas après l’étape « Configuration Windows et Configuration Manager » si la pré-configuration de BitLocker est utilisée avec [Windows 10, version 1511.](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo)

**Conditions préalables:**

-   Un processus de déploiement d’image Windows existant (Microsoft Deployment Shared Computer Toolkit (MDT), Microsoft System Center Configuration Manager ou un autre outil ou processus d’imagerie doit être en place.

-   Le TPM doit être activé dans le BIOS et visible pour le système d’exploitation

-   L’infrastructure de serveur MBAM doit être en place et accessible

-   La partition système requise par BitLocker doit être créée

-   L’ordinateur doit être joint au domaine pendant l’imagerie pour que MBAM active entièrement BitLocker

**Pour activer BitLocker à l’aide de MBAM 2.5 SP1 dans le cadre d’Windows déploiement**

1. Dans MBAM 2.5 SP1, l’approche recommandée pour activer BitLocker pendant un déploiement Windows consiste à utiliser le `Invoke-MbamClientDeployment.ps1` script PowerShell.

   -   Le `Invoke-MbamClientDeployment.ps1` script édicte BitLocker pendant le processus d’imagerie. Lorsque la stratégie BitLocker l’exige, l’agent MBAM invite immédiatement l’utilisateur du domaine à créer un code confidentiel ou un mot de passe lorsque l’utilisateur du domaine se connecte pour la première fois après l’imagerie.

   -   Facile à utiliser avec les processus d’imagerie MDT, System Center Configuration Manager ou autonomes

   -   Compatible avec PowerShell 2.0 ou une édition supérieure

   -   Chiffrer le volume du système d’exploitation avec le protecteur de clé TPM

   -   Prise en charge complète de la pré-mise en service de BitLocker

   -   Chiffrer éventuellement les FDD

   -   Escrow TPM OwnerAuth For Windows 7, MBAM must own the TPM for escrow to occur.
   Pour Windows 8.1, Windows 10 RTM et Windows 10 version 1511, la dépôt de TPM OwnerAuth est prise en charge.
   Pour Windows 10 version 1607 ou ultérieure, seuls les Windows peuvent prendre possession du TPM. Dans l’ajout, Windows conservera pas le mot de passe du propriétaire du module TPM lors de la mise en service du module TPM. Pour plus [d’informations, voir](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) le mot de passe du propriétaire du TPM.

   -   Clés de récupération de dépôt de clé et packages de clés de récupération

   -   État du chiffrement de rapport immédiatement

   -   Nouveaux fournisseurs WMI

   -   Journalisation détaillée

   -   Gestion robuste des erreurs

   Vous pouvez télécharger le `Invoke-MbamClientDeployment.ps1` script à partir du centre Microsoft.com [téléchargement.](https://www.microsoft.com/download/details.aspx?id=54439) Il s’agit du script principal que votre système de déploiement appellera pour configurer le chiffrement de lecteur BitLocker et enregistrer les clés de récupération avec le serveur MBAM.

   **Méthodes de déploiement WMI pour MBAM :** Les méthodes WMI suivantes ont été ajoutées dans MBAM 2.5 SP1 pour prendre en charge l’activation de BitLocker à l’aide du `Invoke-MbamClientDeployment.ps1` script PowerShell.

   <a href="" id="mbam-machine-wmi-class"></a>**MBAM\_Machine classe WMI** 
    **PrepareTpmAndEscrowOwnerAuth :** Lit le TPM OwnerAuth et l’envoie à la base de données de récupération MBAM à l’aide du service de récupération MBAM. Si le TPM n’est pas propriétaire et que l’approvisionnement automatique n’est pas en cours, il génère un TPM OwnerAuth et en prend possession. En cas d’échec, un code d’erreur est renvoyé pour la résolution des problèmes.

   **Remarque** Pour Windows 10 version 1607 ou ultérieure, seuls les Windows peuvent prendre possession du TPM. Dans l’ajout, Windows conservera pas le mot de passe du propriétaire du module TPM lors de la mise en service du module TPM. Pour plus [d’informations, voir](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) le mot de passe du propriétaire du TPM.

| Paramètre | Description |
| -------- | ----------- |
| RecoveryServiceEndPoint | Chaîne spécifiant le point de terminaison du service de récupération MBAM. |

Voici une liste des messages d’erreur courants :

| Valeurs de retour courantes | Message d’erreur |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0x0) | La méthode a réussi. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | Le TPM n’est pas présent sur l’ordinateur ou est désactivé dans la configuration du BIOS. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | Le TPM n’est pas dans l’état correct (activé, activé et l’installation du propriétaire est autorisée). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM ne peut pas prendre possession du TPM car la mise en service automatique est en attente. Essayez à nouveau une fois la mise en service automatique terminée. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM ne peut pas lire la valeur d’autorisation du propriétaire du TPM. La valeur a peut-être été supprimée après un dépôt de dépôt réussi. Sur Windows 7, MBAM ne peut pas lire la valeur si le TPM appartient à d’autres personnes. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | L’ordinateur doit être redémarré pour que le TPM soit à l’état correct. Vous devrez peut-être redémarrer manuellement l’ordinateur. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | L’ordinateur doit être arrêté et de nouveau allumé pour que le TPM soit à l’état correct. Vous devrez peut-être redémarrer manuellement l’ordinateur. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | L’accès a été refusé par le point de terminaison distant. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Le point de terminaison distant n’existe pas ou n’a pas pu être localisé. |
| **WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | Le point de terminaison distant n’a pas pu traiter la demande. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Le point de terminaison distant n’était pas accessible. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Un message contenant une erreur a été reçu du point de terminaison distant. Assurez-vous que vous vous connectez au point de terminaison de service correct. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | URL d’adresse de point de terminaison non valide. L’URL doit commencer par « http » ou « https ». |

   **ReportStatus :** Lit l’état de conformité du volume et l’envoie à la base de données d’état de conformité MBAM à l’aide du service de rapports d’état MBAM. L’état inclut la puissance de chiffrement, le type de logiciel de protection, l’état du logiciel de protection et l’état de chiffrement. En cas d’échec, un code d’erreur est renvoyé pour la résolution des problèmes.

   | Paramètre | Description |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Chaîne spécifiant le point de terminaison du service de rapports d’état MBAM. |

   Voici une liste des messages d’erreur courants :

   | Valeurs de retour courantes | Message d’erreur |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0x0) | La méthode a réussi |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | L’accès a été refusé par le point de terminaison distant.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Le point de terminaison distant n’existe pas ou n’a pas pu être localisé. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | Le point de terminaison distant n’a pas pu traiter la demande. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Le point de terminaison distant n’était pas accessible. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Un message contenant une erreur a été reçu du point de terminaison distant. Assurez-vous que vous vous connectez au point de terminaison de service correct. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | URL d’adresse de point de terminaison non valide. L’URL doit commencer par « http » ou « https ». |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM\_Volume Classe WMI** **EscrowRecoveryKey** : lit le mot de passe numérique de récupération et le package de clé du volume et les envoie à la base de données de récupération MBAM à l’aide du service de récupération MBAM. En cas d’échec, un code d’erreur est renvoyé pour la résolution des problèmes.

   | Paramètre | Description |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Chaîne spécifiant le point de terminaison du service de récupération MBAM. |

   Voici une liste des messages d’erreur courants :

   | Valeurs de retour courantes | Message d’erreur |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0x0) | La méthode a réussi |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | Le volume est verrouillé. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | Un protecteur de mot de passe numérique n’a pas été trouvé pour le volume. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | L’accès a été refusé par le point de terminaison distant. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | Le point de terminaison distant n’existe pas ou n’a pas pu être localisé. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | Le point de terminaison distant n’a pas pu traiter la demande. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | Le point de terminaison distant n’était pas accessible. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Un message contenant une erreur a été reçu du point de terminaison distant. Assurez-vous que vous vous connectez au point de terminaison de service correct. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | URL d’adresse de point de terminaison non valide. L’URL doit commencer par « http » ou « https ». |
     

2. **Déployer MBAM à l’aide de Microsoft Deployment Shared Computer Toolkit (MDT) et PowerShell**

   1.  Dans MDT, créez un partage de déploiement ou ouvrez un partage de déploiement existant.

       **Remarque**  
       Le `Invoke-MbamClientDeployment.ps1` script PowerShell peut être utilisé avec n’importe quel processus ou outil d’imagerie. Cette section montre comment l’intégrer à l’aide de MDT, mais les étapes sont similaires à son intégration à tout autre processus ou outil.

       **Attention**  
       Si vous utilisez la pré-approvisionnement BitLocker (WinPE) et souhaitez conserver la valeur d’autorisation du propriétaire du module TPM, vous devez ajouter le script dans WinPE immédiatement avant le redémarrage de l’installation dans le système d’exploitation `SaveWinPETpmOwnerAuth.wsf` complet. **Si vous n’utilisez pas ce script, vous perdrez la valeur d’autorisation du propriétaire du TPM au redémarrage.**

   2.  Copiez `Invoke-MbamClientDeployment.ps1` ** &lt; dans DeploymentShare &gt; \\Scripts**. Si vous utilisez la pré-mise en service, copiez le fichier `SaveWinPETpmOwnerAuth.wsf` dans ** &lt; DeploymentShare &gt; \\Scripts**.

   3.  Ajoutez l’application cliente MBAM 2.5 SP1 au nœud Applications dans le partage de déploiement.

       1.  Sous le nœud **Applications,** cliquez sur **Nouvelle application.**

       2.  Sélectionnez **Application avec fichiers sources.** Cliquez sur **Suivant**.

       3.  Dans **le nom de l’application,** tapez « CLIENT MBAM 2.5 SP1 ». Cliquez sur **Suivant**.

       4.  Accédez au répertoire contenant `MBAMClientSetup-<Version>.msi` . Cliquez sur **Suivant**.

       5.  Tapez « MBAM 2.5 SP1 Client » comme répertoire à créer. Cliquez sur **Suivant**.

       6.  Entrez `msiexec /i MBAMClientSetup-<Version>.msi /quiet` à partir de la ligne de commande. Cliquez sur **Suivant**.

       7.  Acceptez les valeurs par défaut restantes pour terminer l’Assistant Nouvelle application.

   4.  Dans MDT, cliquez avec le bouton droit sur le nom du partage de déploiement, puis cliquez sur **Propriétés.** Cliquez sur **l’onglet Règles.** Ajoutez les lignes suivantes :

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Cliquez sur OK pour fermer la fenêtre.

   5.  Sous le nœud Séquences de tâches, modifiez une séquence de tâches existante utilisée pour Windows déploiement. Si vous le souhaitez, vous pouvez créer une séquence de tâches en **** cliquant avec le bouton droit sur le nœud **Séquences** de tâches, en sélectionnant Nouvelle séquence de tâches et en terminant l’Assistant.

       Sous **l’onglet Séquence de** tâches de la séquence de tâches sélectionnée, effectuez les étapes suivantes :

       1.  Sous le **dossier De préinstallation,** activez la tâche facultative Activer **BitLocker (hors connexion)** si vous souhaitez activer BitLocker dans WinPE, qui chiffre l’espace utilisé uniquement.

       2.  Pour rendre le TPM OwnerAuth persistant lors de l’utilisation de la pré-mise en service, en permettant à MBAM de le mettre en dépôt ultérieurement, utilisez les actions suivantes :

           1.  Rechercher **l’étape Installer le système d’exploitation**

           2.  Ajouter une nouvelle étape **de ligne de commande d’exécuter** après

           3.  Nommez l’étape **Persist TPM OwnerAuth**

           4.  Définissez la ligne de commande sur Remarque : pour `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **** Windows 10 version 1607 ou ultérieure, seuls les Windows peuvent prendre possession du TPM. Dans l’ajout, Windows conservera pas le mot de passe du propriétaire du module TPM lors de la mise en service du module TPM. Pour plus [d’informations, voir](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) le mot de passe du propriétaire du TPM.

       3.  Dans le **dossier Restauration d’état,** supprimez **la tâche Activer BitLocker.**

       4.  Dans le dossier **Restauration de l’état** sous **Tâches personnalisées,** créez une tâche Installer l’application et nommez-la Installer **l’agent MBAM.** **** Cliquez sur **la radio Installer une application** unique et accédez à l’application cliente MBAM 2.5 SP1 créée précédemment.

       5.  Dans **** le dossier Restauration de l’état sous Tâches personnalisées, **** créez une tâche Exécuter le script **PowerShell** (après l’étape de l’application cliente MBAM 2.5 SP1) avec les paramètres suivants (mettez à jour les paramètres selon les besoins de votre environnement) :

           -   Nom : configurer BitLocker pour MBAM

           -   Script PowerShell : `Invoke-MbamClientDeployment.ps1`

           -   Paramètres :

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
               <td align="left"><p>Point de terminaison du service de récupération MBAM</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>Facultatif</p></td>
               <td align="left"><p>Point de terminaison du service de rapports d’état MBAM</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Facultatif</p></td>
               <td align="left"><p>Méthode de chiffrement (par défaut : AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifier le chiffrement des volumes de données et des clés de récupération de volume de données en dépôt</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifier d’attendre la fin du chiffrement</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifier que le script de déploiement ne reprendra pas le chiffrement suspendu</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifiez d’ignorer l’échec de dépôt de dépôt d’th du propriétaire du TPM. Il doit être utilisé dans les scénarios où MBAM n’est pas en mesure de lire l’th de propriétaire du TPM, par exemple, si la mise en service automatique du TPM est activée</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifier d’ignorer l’échec de dépôt de clé de récupération de volume</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Commutateur</p></td>
               <td align="left"><p>Spécifier d’ignorer l’échec du rapport d’état</p></td>
               </tr>
               </tbody>
               </table>

                 

**Pour activer BitLocker à l’aide de MBAM 2.5 ou d’une Windows déploiement**

1.  Installez le client MBAM. Pour obtenir des instructions, [voir Comment déployer le client MBAM à l’aide d’une ligne de commande](how-to-deploy-the-mbam-client-by-using-a-command-line.md).

2.  Joindre l’ordinateur à un domaine (recommandé).

    -   Si l’ordinateur n’est pas joint à un domaine, le mot de passe de récupération n’est pas stocké dans le service de récupération de clé MBAM. Par défaut, MBAM n’autorise pas le chiffrement, sauf si la clé de récupération peut être stockée.

    -   Si un ordinateur démarre en mode de récupération avant que la clé de récupération ne soit stockée sur le serveur MBAM, aucune méthode de récupération n’est disponible et l’ordinateur doit être réinventé.

3.  Ouvrez une invite de commandes en tant qu’administrateur et arrêtez le service MBAM.

4.  Définissez le service sur **Manuel ou** à **la demande** en tapant les commandes suivantes :

    **net stop mbamagent**

    **sc config mbamagent start= demand**

5.  Définissez les valeurs de Registre de sorte que le client MBAM ignore les paramètres de stratégie de groupe et définit plutôt le chiffrement pour démarrer l’heure à Windows est déployée sur cet ordinateur client.

    **Attention**  
    Cette étape décrit comment modifier le Windows registre. L’utilisation incorrecte de l’Éditeur du Registre peut entraîner de graves problèmes qui peuvent nécessiter la réinstallation Windows. Nous ne pouvons pas garantir que les problèmes résultant de l’utilisation incorrecte de l’Éditeur du Registre peuvent être résolus. Utilisez l’Éditeur du Registre à vos risques et périls.

    1.  Définissez le TPM pour le chiffrement du système d’exploitation **uniquement,** exécutez Regedit.exe, puis importez le modèle de clé de Registre à partir de C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

    2.  Dans Regedit.exe, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.

        **Remarque**  
        Vous pouvez définir les paramètres de stratégie de groupe ou les valeurs de Registre relatives à MBAM ici. Ces paramètres remplacent les valeurs précédemment définies.

        Paramètres de configuration de l’entrée de Registre

        DeploymentTime

        0 = Éteint

        1 = Utiliser les paramètres de stratégie de temps de déploiement (par défaut) : utilisez ce paramètre pour activer le chiffrement au moment Windows est déployé sur l’ordinateur client.

        UseKeyRecoveryService

        0 = Ne pas utiliser la clé de dépôt (les deux entrées de Registre suivantes ne sont pas requises dans ce cas)

        1 = Utiliser un dépôt de clé dans le système de récupération de clé (par défaut)

        Il s’agit du paramètre recommandé, qui permet à MBAM de stocker les clés de récupération. L’ordinateur doit pouvoir communiquer avec le service de récupération de clés MBAM. Vérifiez que l’ordinateur peut communiquer avec le service avant de continuer.

        KeyRecoveryOptions

        0 = Charge la clé de récupération uniquement

        1 = charge la clé de récupération et le package de récupération de clé (par défaut)

        KeyRecoveryServiceEndPoint

        Définissez cette valeur sur l’URL du serveur exécutant le service de récupération de clé, par exemple, http:// nom de l’ordinateur &lt; &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.


6.  Le client MBAM redémarre le système pendant le déploiement du client MBAM. Lorsque vous êtes prêt pour ce redémarrage, exécutez la commande suivante à l’invite de commandes en tant qu’administrateur :

    **net start mbamagent**

7.  Lorsque les ordinateurs redémarrent et que le BIOS vous invite, acceptez la modification du TPM.

8.  Pendant le processus d’imagerie du système d’exploitation client Windows, lorsque vous êtes prêt à démarrer le chiffrement, ouvrez une invite de commandes en tant qu’administrateur et tapez les commandes suivantes pour définir le démarrage sur Automatique et redémarrer l’agent client MBAM : ****

    **sc config mbamagent start= auto**

    **net start mbamagent**

9.  Pour supprimer les valeurs de Registre de contournement, exécutez Regedit.exe et allez à l’entrée de Registre HKLM\\SOFTWARE\\Microsoft. Cliquez avec le bouton droit **sur le nœud MBAM,** puis cliquez sur **Supprimer.**

## <a name="related-topics"></a>Rubriques associées

[Déploiement du client MBAM 2.5](deploying-the-mbam-25-client.md)

[Planification du déploiement de clients MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## <a name="got-a-suggestion-for-mbam"></a>Vous avez une suggestion pour MBAM ?
- Ajoutez ou votez sur les suggestions [ici.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes de MBAM, utilisez le [forum TechNet MBAM.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)

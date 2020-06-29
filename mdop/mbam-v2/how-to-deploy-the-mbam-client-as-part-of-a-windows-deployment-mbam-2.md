---
title: Déploiement du client MBAM dans le cadre d'un déploiement de Windows
description: Déploiement du client MBAM dans le cadre d'un déploiement de Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810667"
---
# Déploiement du client MBAM dans le cadre d'un déploiement de Windows


Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Si les ordinateurs disposant d’une puce de module de plateforme sécurisée (TPM), le client BitLocker peut être intégré au sein d’une organisation en activant la gestion et le chiffrement de BitLocker sur les ordinateurs clients dans le cadre du processus de déploiement d’imagerie et Windows.

**Remarque**  
Pour vérifier la configuration système requise pour le client d’administration et de surveillance de BitLocker, voir [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



Le chiffrement d’ordinateurs clients avec BitLocker lors de la phase d’imagerie initiale d’un déploiement Windows peut réduire la surcharge administrative nécessaire pour implémenter MBAM au sein d’une organisation. Cela permet également de s’assurer que chaque ordinateur déployé possède déjà BitLocker et qu’il est configuré correctement.

**Remarque**  
La procédure décrite dans cette rubrique décrit la modification du Registre Windows. L’utilisation de l’éditeur du Registre peut être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows. Microsoft ne peut pas garantir que les problèmes résultant de l’utilisation incorrecte de l’éditeur du Registre peuvent être résolus. Utilisez l’éditeur du Registre à vos propres risques.



**Pour chiffrer un ordinateur dans le cadre du déploiement Windows**

1.  Si votre organisation envisagez d’utiliser le protecteur de module de plateforme sécurisée (TPM) ou les options de protecteur de TPM + PIN dans BitLocker, vous devez activer le processeur du TPM avant le déploiement initial de MBAM. Lorsque vous activez le processeur du TPM, vous évitez un redémarrage ultérieur dans le processus et vous vous assurez que les puces du TPM sont correctement configurées conformément aux exigences de votre organisation. Vous devez activer manuellement le processeur du TPM dans le BIOS de l’ordinateur.

    **Remarque**  
    Certains fournisseurs fournissent des outils permettant d’activer et d’activer le processeur du TPM dans le BIOS à partir du système d’exploitation. Pour plus d’informations sur la façon de configurer le processeur du TPM, consultez la documentation fournie par le fabricant.



2.  Installez l’agent client d’administration et de contrôle Microsoft BitLocker.

3.  Rejoignez l’ordinateur à un domaine (recommandé).

    -   Si l’ordinateur n’est pas joint au domaine, le mot de passe de récupération n’est pas stocké dans le service de récupération de clé MBAM. Par défaut, MBAM ne permet pas d’effectuer le chiffrement, sauf si la clé de récupération peut être stockée.

    -   Si un ordinateur démarre en mode de récupération avant que la clé de récupération ne soit stockée sur le serveur MBAM, l’ordinateur doit être rephoto. Aucune méthode de récupération n’est disponible.

4.  Exécutez l’invite de commandes en tant qu’administrateur, arrêtez le service MBAM, puis définissez le service sur **Manuel** ou à **la demande**, puis commencez par taper les commandes suivantes:

    **net stop mbamagent**

    **sc config mbamagent Start = Demand**

5.  Définissez les paramètres de registre de l’agent MBAM pour ignorer la stratégie de groupe et exécuter le TPM pour le **chiffrement du système d’exploitation uniquement** en exécutant **regedit**, puis en important le modèle de clé de Registre à partir de C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  Dans Regedit, accédez à HKLM\\SOFTWARE\\Microsoft\\MBAM et configurez les paramètres indiqués dans le tableau suivant.

    Entrée du Registre

    Paramètres de configuration

    DeploymentTime

    0 = DÉSACTIVÉ

    1 = utiliser les paramètres de stratégie de moment de déploiement (par défaut)

    UseKeyRecoveryService

    0 = ne pas utiliser la clé de dépôt clé (les deux entrées de Registre suivantes ne sont pas requises dans le cas présent)

    1 = utiliser le tiers de confiance principal dans le système de récupération de clés (par défaut)

    Recommandé: l’ordinateur doit pouvoir communiquer avec le service de récupération de clés. Vérifiez que l’ordinateur peut communiquer avec le service avant de continuer.

    KeyRecoveryOptions

    0 = Télécharger uniquement la clé de récupération

    1 = Télécharger la clé de récupération et le package de récupération de clé (par défaut)

    KeyRecoveryServiceEndPoint

    Définissez cette valeur sur l’URL du serveur Web de récupération de clé (par exemple, http://nom de l' &lt; ordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. L’agent MBAM redémarre le système lors du déploiement du client MBAM. Lorsque vous êtes prêt à redémarrer, exécutez la commande suivante à l’invite de commandes en tant qu’administrateur:

   **mbamagent de début net**

8. Au redémarrage de l’ordinateur, le BIOS vous demande d’accepter un changement de TPM en acceptant la modification.

9. Pendant le processus d’imagerie du système d’exploitation du client Windows, lorsque vous êtes prêt à commencer le chiffrement, redémarrez le service de l’agent MBAM et définissez démarrer sur **automatique** en exécutant une invite de commandes en tant qu’administrateur et en entrant les commandes suivantes:

   **sc config mbamagent start = auto**

   **mbamagent de début net**

10. Supprimez les valeurs de registre de contournement en exécutant regedit et en accédant à l’entrée de Registre HKLM\\SOFTWARE\\Microsoft. Pour supprimer le nœud **MBAM** , cliquez avec le bouton droit sur le nœud, puis cliquez sur **supprimer**.

## Rubriques connexes


[Déploiement du client MBAM2.0](deploying-the-mbam-20-client-mbam-2.md)










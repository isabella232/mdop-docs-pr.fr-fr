---
title: Déploiement du client MBAM dans le cadre d'un déploiement de Windows
description: Déploiement du client MBAM dans le cadre d'un déploiement de Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810841"
---
# Déploiement du client MBAM dans le cadre d'un déploiement de Windows


Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Le client BitLocker peut être intégré au sein d’une organisation en activant la gestion et le chiffrement de BitLocker sur les ordinateurs clients lors du processus de déploiement d’images et Windows.

**Remarque**  
Pour vérifier la configuration système requise pour le client MBAM, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).



Le chiffrement d’ordinateurs clients avec BitLocker lors de la phase d’imagerie initiale d’un déploiement de Windows peut réduire la surcharge d’administration de l’implémentation de MBAM. Cette approche permet également de s’assurer que chaque ordinateur déployé possède déjà BitLocker et qu’il est configuré correctement.

**Warning**  
Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre. Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows. Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre. Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus. Changez de Registre à vos propres risques.



**Pour chiffrer un ordinateur dans le cadre du déploiement Windows**

1.  Si votre organisation envisage d’utiliser le protecteur de module de plateforme sécurisée (TPM) ou les options de protecteur de TPM + PIN dans BitLocker, vous devez activer le processeur du TPM avant le déploiement initial d’MBAM. Lorsque vous activez le processeur du TPM, vous évitez un redémarrage ultérieur dans le processus et vous vous assurez que les puces du TPM sont correctement configurées conformément aux exigences de votre organisation. Vous devez activer manuellement le processeur du TPM dans le BIOS de votre ordinateur. Pour plus d’informations sur la façon de configurer le processeur du TPM, consultez la documentation fournie par le fabricant.

2.  Installez l’agent client MBAM.

3.  Nous vous recommandons de joindre l’ordinateur à un domaine...

    -   Si l’ordinateur n’est pas joint à un domaine, le mot de passe de récupération n’est pas stocké dans le service de récupération de clé MBAM. Par défaut, MBAM ne permet pas d’effectuer le chiffrement, sauf si la clé de récupération peut être stockée.

    -   Si un ordinateur démarre en mode de récupération avant que la clé de récupération ne soit stockée sur le serveur MBAM, l’ordinateur doit être rephoto. Aucune méthode de récupération n’est disponible.

4.  Ouvrez une invite de commandes en tant qu’administrateur, arrêtez le service MBAM, puis définissez le service sur **Manuel** ou à **la demande**. Exécutez ensuite les commandes suivantes:

    **net stop mbamagent**

    **sc config mbamagent Start = Demand**

5.  Définissez les paramètres de registre de l’agent MBAM pour qu’il ignore les stratégies de groupe et exécutez le module de plateforme sécurisée pour le **système d’exploitation uniquement le chiffrement** pour effectuer cette opération, exécutez **regedit**, puis importez le modèle de clé de Registre à partir de C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  Dans Regedit, accédez à HKLM\\SOFTWARE\\Microsoft\\MBAM et configurez les paramètres indiqués dans le tableau suivant.

    Entrée du Registre

    Paramètres de configuration

    DeploymentTime

    0 = DÉSACTIVÉ

    1 = utiliser les paramètres de stratégie de moment de déploiement (par défaut)

    UseKeyRecoveryService

    0 = ne pas utiliser le tiers de confiance principal (les deux entrées de Registre suivantes ne sont pas requises dans le cas présent).

    1 = utiliser le tiers de confiance principal dans le système de récupération de clés (par défaut)

    Recommandé: l’ordinateur doit pouvoir communiquer avec le service de récupération de clés. Vérifiez que l’ordinateur peut communiquer avec le service avant de continuer.

    KeyRecoveryOptions

    0 = Télécharger la clé de récupération uniquement

    1 = Télécharger la clé de récupération et le package de récupération de clé (par défaut)

    KeyRecoveryServiceEndPoint

    Définissez cette valeur sur l’URL du serveur Web de récupération de clés.

    Par exemple: http:// &lt; nom d’ordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. L’agent MBAM redémarre le système lors du déploiement du client MBAM. Lorsque vous êtes prêt à redémarrer, exécutez la commande suivante à l’invite de commandes en tant qu’administrateur:

   **mbamagent de début net**

8. Au redémarrage de l’ordinateur et le BIOS vous demande d’accepter un changement de TPM, acceptez la modification.

9. Pendant le processus d’imagerie du système d’exploitation du client Windows, lorsque vous êtes prêt à commencer le chiffrement, redémarrez le service de l’agent MBAM. Pour définir l’option de démarrage **automatique**, ouvrez une invite de commandes en tant qu’administrateur et exécutez les commandes suivantes:

   **sc config mbamagent start = auto**

   **mbamagent de début net**

10. Supprimez les valeurs de Registre Bypass. Pour cela, exécutez regedit, accédez à l’entrée de Registre HKLM\\SOFTWARE\\Microsoft, cliquez avec le bouton droit sur le nœud **MBAM** , puis cliquez sur **supprimer**.

## Rubriques connexes


[Déploiement du client MBAM1.0](deploying-the-mbam-10-client.md)










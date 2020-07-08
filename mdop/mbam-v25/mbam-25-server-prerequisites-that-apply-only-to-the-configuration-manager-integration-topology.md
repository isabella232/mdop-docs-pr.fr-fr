---
title: Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager
description: Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804321"
---
# Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager


Si vous installez la fonctionnalité d’administration et de surveillance de BitLocker (MBAM) 2,5 à l’aide de la fonctionnalité d’intégration de System Center Configuration Manager, vous devez remplir les conditions préalables décrites dans cette rubrique, en plus de celles dans [MBAM 2,5 Server Prerequisites pour les topologies d’intégration autonome et Configuration Manager](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md). Vous devez également créer ou modifier des fichiers. mof nécessaires pour la topologie d’intégration de Configuration Manager.

## Conditions préalables pour le composant Intégration Configuration Manager


Si vous configurez MBAM avec la topologie d’intégration System Center Configuration Manager, vous devez effectuer les conditions préalables supplémentaires requises pour Configuration Manager.

[Conditions préalables pour le composant Intégration Configuration Manager](prerequisites-for-the-configuration-manager-integration-feature.md)

## Modifier le fichier Configuration. mof


Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez modifier le fichier Configuration. mof pour SystemCenter2012 ConfigurationManager et Microsoft System Center Configuration Manager 2007.

[Modifier le fichier Configuration.mof](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Créer ou modifier le fichier SMS \ _def. mof


Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker dans les rapports du gestionnaire de configuration MBAM, vous devez créer ou modifier le fichier SMS \ _def. mof. Si vous utilisez SystemCenter2012 ConfigurationManager, vous devez créer le fichier. Dans Configuration Manager 2007, le fichier existe déjà, vous devez donc modifier le fichier existant, mais pas le remplacer.

[Créer ou modifier le fichier SMS \ _def. mof](create-or-edit-the-sms-defmof-file-mbam-25.md)


## Rubriques connexes


[Préparation de votre environnement pour MBAM2.5](preparing-your-environment-for-mbam-25.md)

[Configurations prises en charge par MBAM2.5](mbam-25-supported-configurations.md)

[Planification du déploiement de MBAM2.5](planning-to-deploy-mbam-25.md)

 

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).





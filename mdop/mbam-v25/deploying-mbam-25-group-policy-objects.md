---
title: Déploiement d'objets de stratégie de groupe MBAM2.5
description: Déploiement d'objets de stratégie de groupe MBAM2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810524"
---
# Déploiement d'objets de stratégie de groupe MBAM2.5


Pour déployer MBAM, vous devez définir les paramètres de stratégie de groupe définissant les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker. Pour effectuer cette tâche, vous devez copier les modèles de stratégie de groupe MBAM sur un serveur ou une station de travail capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou la gestion avancée des stratégies de groupe (AGPM), puis de modifier les paramètres.

**Important**  Ne modifiez pas les paramètres de stratégie de groupe du nœud **BitLocker Drive Encryption** , ou MBAM ne fonctionne pas correctement. Lorsque vous configurez les paramètres de stratégie de groupe dans le nœud **MDOP MBAM (gestion du BitLocker)** , MBAM configure automatiquement les paramètres de **chiffrement de lecteur BitLocker** pour vous.

 

## Copie des modèles de stratégie de groupe MBAM2.5


Avant d’installer le client MBAM, vous devez copier des objets de stratégie de groupe spécifiques MBAM (GPO) sur la station de travail de gestion. Ces objets de stratégie de groupe définissent des paramètres d’implémentation MBAM pour le chiffrement de lecteur BitLocker. Vous pouvez copier les modèles de stratégie de groupe sur n’importe quel serveur ou station de travail, qui est un ordinateur client ou un serveur Windows pris en charge, et qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).

[Copie des modèles de stratégie de groupe MBAM2.5](copying-the-mbam-25-group-policy-templates.md)

## Modification des paramètres de l’objet de stratégie de MBAM 2,0


Après avoir créé les objets de stratégie de groupe nécessaires, vous devez déployer les paramètres de stratégie de groupe MBAM sur les ordinateurs clients de votre organisation. Pour afficher et créer des objets de stratégie de groupe, vous devez avoir installé la console de gestion des stratégies de groupe (GPMC) ou la gestion de la stratégie de groupe avancée.

[Modification des paramètres de stratégie de groupe MBAM2.5](editing-the-mbam-25-group-policy-settings.md)

## Affichage ou masquage du panneau de configuration MBAM du panneau de configuration Windows


Dans la mesure où MBAM propose un panneau de configuration MBAM personnalisé qui peut remplacer le panneau de configuration Windows BitLocker par défaut, vous pouvez également choisir d’afficher ou de masquer le panneau de configuration BitLocker par défaut auprès des utilisateurs finaux à l’aide de paramètres de stratégie de groupe.

[Masquage de l'élément de chiffrement de lecteur BitLocker par défaut dans le Panneau de configuration](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## Autres ressources pour le déploiement d’objets de stratégie de groupe MBAM 2,0


[Déploiement de MBAM2.5](deploying-mbam-25.md)

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

 

 






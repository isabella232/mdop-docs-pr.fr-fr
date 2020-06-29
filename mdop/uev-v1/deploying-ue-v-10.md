---
title: Déploiement d'UE-V1.0
description: Déploiement d'UE-V1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812180"
---
# Déploiement d'UE-V1.0


Il existe diverses configurations de déploiement prises en charge par Microsoft User User Virtualization (UE-V). Cette section contient des informations générales et des procédures pas à pas pour vous aider à effectuer les tâches que vous devez effectuer à différentes étapes de votre déploiement.

## Informations de déploiement pour UE-V


Le déploiement d’UE-V nécessite un emplacement de stockage des paramètres sur un partage réseau et un agent UE-V installé sur chaque ordinateur qui synchronise les paramètres. Les modèles de stratégie de groupe UE-V peuvent être utilisés pour gérer les paramètres d’UE-V. Les rubriques suivantes décrivent le déploiement de ces fonctionnalités.

[Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

Toutes les solutions de déploiement d’UE-V requièrent un emplacement de stockage des paramètres dans lequel se trouvent les packages de paramètres qui contiennent les valeurs de paramètre synchronisées.

[Déploiement de l'agent UE-V](deploying-the-ue-v-agent.md)

Pour synchroniser les paramètres à l’aide d’UE-V, l’agent UE-V doit être installé et exécuté sur un ordinateur.

[Installation des modèles ADMX de stratégie de groupe UE-V](installing-the-ue-v-group-policy-admx-templates.md)

Vous pouvez utiliser une stratégie de groupe pour préconfigurer les paramètres d’UE-V avant de déployer l’agent UE-V ainsi que la configuration standard pour UE-V.

## Informations de déploiement pour le déploiement de modèles personnalisés


Si vous envisagez de créer des modèles d’emplacement des paramètres personnalisés pour des applications autres que les applications Microsoft incluses dans UE-V, telles que des applications métier, vous pouvez déployer un catalogue de modèles de paramètres et vous devez installer le générateur UE-V pour créer ces modèles. Pour plus d’informations, consultez [planification du déploiement de modèles personnalisés pour UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

[Installation du Générateur UE-V](installing-the-ue-v-generator.md)

Le générateur UE-V permet de créer, de modifier et de valider des modèles d’emplacements de paramètres personnalisés qui permettent de synchroniser les paramètres d’applications autres que les applications par défaut.

[Déploiement du catalogue de modèles de paramètres pour UE-V1.0](deploying-the-settings-template-catalog-for-ue-v-10.md)

Si vous devez déployer des modèles d’emplacement des paramètres personnalisés pour prendre en charge des applications autres que les applications par défaut de l’agent UE-V, vous devez configurer un catalogue de modèles de paramètres pour les stocker.

[Déploiement de modèles d'emplacement de paramètres UE-V pour UE-V1.0](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

Si vous avez besoin de synchroniser des applications qui ne sont pas les applications par défaut dans l’agent UE-V, les modèles d’emplacement des paramètres personnalisés créés avec le générateur UE-V peuvent être distribués dans le catalogue de modèles de paramètres d’UE-v.

**Remarques**  Le déploiement de modèles personnalisés nécessite un catalogue de modèles de paramètres. Les modèles d’application Microsoft par défaut sont déployés avec UE-V agent.

 

## Rubriques relatives à ce produit


[Microsoft User Experience Virtualization (UE-V)1.0](index.md)

[Prise en main de User Experience Virtualization1.0](getting-started-with-user-experience-virtualization-10.md)

[Planification pour UE-V1.0](planning-for-ue-v-10.md)

[Opérations d'UE-V1.0](operations-for-ue-v-10.md)

[Résolution des problèmes liés à UE-V1.0](troubleshooting-ue-v-10.md)

 

 






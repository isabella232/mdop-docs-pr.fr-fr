---
title: Planification du déploiement de modèle personnalisé d'UE-V1.0
description: Planification du déploiement de modèle personnalisé d'UE-V1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808609"
---
# Planification du déploiement de modèle personnalisé d'UE-V1.0


La virtualisation de l’utilisation de Microsoft User (UE-V) utilise des modèles d’emplacement des paramètres (fichiers XML) qui définissent les paramètres capturés et appliqués par UE-V. Vous pouvez utiliser le générateur UE-V pour créer des modèles d’emplacement des paramètres personnalisés qui permettent aux utilisateurs d’utiliser les paramètres des applications qui ne sont pas incluses dans les modèles UE-V par défaut. Après avoir testé le modèle personnalisé pour vous assurer que les paramètres de l’application s’immobilent correctement dans un environnement de test, vous pouvez déployer ces modèles d’emplacement des paramètres sur les ordinateurs de l’entreprise.

Vous pouvez déployer vos modèles d’emplacement des paramètres personnalisés avec une infrastructure de déploiement existante, telle que la distribution de logiciels d’entreprise, avec des préférences de stratégie de groupe, ou en configurant un catalogue de modèles de paramètres UE-V. Les modèles déployés à l’aide de ESD ou d’une stratégie de groupe doivent être enregistrés auprès d’UE-V WMI ou PowerShell.

## Catalogue de modèles de paramètres


Le catalogue de modèles de paramètres de virtualisation de l’utilisation de l’utilisateur est un chemin de dossier sur les ordinateurs UE-V ou un partage réseau SMB qui stocke tous les modèles d’emplacement des paramètres personnalisés. L’agent UE-V récupère les modèles nouveaux ou mis à jour à partir de cet emplacement. L’agent UE-V vérifie cet emplacement une fois par jour et met à jour son comportement de synchronisation en fonction des modèles figurant dans ce dossier. Les modèles ajoutés ou mis à jour dans ce dossier depuis la dernière fois où le dossier a été activé sont enregistrés par l’agent UE-V. UE-V agent annule les modèles supprimés de ce dossier. Par défaut, les modèles sont inscrits et annulés une fois par jour à 3:30 matin. heure locale par le planificateur de tâches. Pour plus d’informations sur les tâches UE-V, voir [modification de la fréquence des tâches planifiées UE-v](changing-the-frequency-of-ue-v-scheduled-tasks.md).

Vous pouvez configurer le chemin du catalogue de modèles de paramètres à l’aide des options de ligne de commande d’installation, de stratégie de groupe, de WMI ou d’PowerShell. Les modèles stockés dans le modèle de modèle paramètres sont automatiquement inscrits et désinscrits par une tâche planifiée. Vous pouvez personnaliser cette tâche planifiée selon vos besoins.

## Remplacer les modèles Microsoft par défaut


L’agent UE-V installe un groupe par défaut de modèles d’emplacements de paramètres pour les applications Microsoft courantes et les paramètres Windows. Si votre entreprise a besoin d’une version personnalisée de ces modèles, l’agent UE-V peut être configuré pour utiliser un catalogue de modèles de paramètres, puis remplacer les modèles Microsoft par défaut.

Lors de l’installation de l’agent UE-V, le paramètre de ligne de commande, `RegisterMSTemplates` qui peut être utilisé pour désactiver l’inscription des modèles Microsoft par défaut. Pour plus d’informations sur la définition des paramètres de UE-V, voir [planification pour les méthodes de configuration de UE-v](planning-for-ue-v-configuration-methods.md).

Lorsque vous utilisez une stratégie de groupe pour configurer le chemin du catalogue de modèles de paramètres, vous pouvez choisir de remplacer les modèles Microsoft par défaut. Si vous configurez les paramètres de stratégie pour remplacer les modèles Microsoft par défaut, tous les modèles Microsoft par défaut installés par l’agent UE-V seront supprimés de l’ordinateur et seuls les modèles figurant dans le catalogue de modèles de paramètres seront utilisés. Le paramètre de configuration de l’agent UE-V `RegisterMSTemplates` doit être défini sur true pour pouvoir remplacer le modèle Microsoft par défaut.

**Remarques**  Si vous désactivez ce paramètre de stratégie une fois qu’il est activé, l’agent UE-V ne restaure pas les modèles Microsoft par défaut.

 

S’il existe des modèles personnalisés dans le catalogue de modèles de paramètres qui utilisent le même IDENTIFIant que les modèles Microsoft par défaut, et que l’agent UE-V n’est pas configuré pour remplacer les modèles Microsoft par défaut, les modèles Microsoft dans le catalogue seront ignorés.

Vous pouvez également remplacer les modèles par défaut en utilisant les fonctionnalités PowerShell d’UE-V. Pour remplacer le modèle Microsoft par défaut par PowerShell, annulez l’enregistrement de tous les modèles Microsoft par défaut, puis enregistrez les modèles personnalisés.

**Remarques**  Les packages d’anciens paramètres restent dans l’emplacement de stockage des paramètres même si de nouveaux modèles de paramètres sont déployés pour une application. Ces packages ne sont pas lus par l’agent, mais aucun d’eux n’est automatiquement supprimé.

 

## Rubriques connexes


[Planification pour UE-V1.0](planning-for-ue-v-10.md)

[Planification des applications à synchroniser avec UE-V1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planification de méthodes de configuration d'UE-V](planning-for-ue-v-configuration-methods.md)

Planification du déploiement d’un modèle personnalisé
 

 






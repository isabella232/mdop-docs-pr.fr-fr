---
title: Déploiement de modèles d'emplacement de paramètres UE-V pour UE-V1.0
description: Déploiement de modèles d'emplacement de paramètres UE-V pour UE-V1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812167"
---
# Déploiement de modèles d'emplacement de paramètres UE-V pour UE-V1.0


La virtualisation de l’interface utilisateur de Microsoft (UE-V) utilise des modèles d’emplacement des paramètres (fichiers XML) qui définissent les paramètres qui sont capturés et appliqués par la virtualisation de l’utilisation de l’utilisateur. UE-V inclut un ensemble de modèles standard, ainsi qu’un outil, le générateur UE-V, qui vous permet de créer des modèles d’emplacement des paramètres personnalisés. Après avoir créé un modèle d’emplacement des paramètres, vous devez le tester pour vous assurer que les paramètres de l’application s’immobilessent correctement dans un environnement de test. Vous pouvez ensuite déployer en toute sécurité le modèle d’emplacement des paramètres sur les ordinateurs de l’entreprise.

Les modèles d’emplacement des paramètres peuvent être déployés à l’aide de la distribution de logiciels d’entreprise, des préférences de stratégie de groupe, ou en configurant un catalogue de modèles de paramètres UE-V. Les modèles déployés à l’aide d’une stratégie de groupe ou d’ESD doivent être inscrits via le WMI ou PowerShell d’UE-V. Les modèles stockés dans l’emplacement du catalogue de modèles de paramètres sont automatiquement inscrits par l’agent UE-V.

## Déployer les modèles d’emplacement des paramètres à l’aide d’un chemin d’accès au catalogue de modèles de paramètres


Le chemin du catalogue de modèles d’emplacement des paramètres d’UE-V peut être défini à l’aide des méthodes suivantes: stratégie de groupe, paramètres de ligne de commande d’installation de l’agent, WMI ou PowerShell. Après avoir défini le chemin du catalogue de modèles, UE-V agent récupère les modèles nouveaux ou mis à jour à partir de cet emplacement. L’agent UE-V vérifie cet emplacement une fois par jour et met à jour son comportement de synchronisation en fonction des modèles figurant dans ce dossier. Les modèles qui ont été ajoutés ou mis à jour dans ce dossier depuis la dernière vérification sont inscrits par l’agent UE-V. UE-V agent annule également les modèles qui ont été supprimés de ce dossier. Les modèles sont inscrits et annulés une fois par jour par le planificateur de tâches.

**Pour utiliser le modèle de modèle de paramètres pour déployer des modèles d’emplacement des paramètres UE-V**

1.  Naviguez jusqu’au dossier de partage réseau défini comme catalogue de modèles de paramètres.

2.  Ajoutez, supprimez ou mettez à jour les modèles d’emplacement des paramètres dans le catalogue de modèles de paramètres pour refléter la configuration de modèle d’agent UE-V requise pour les ordinateurs UE-V.

3.  Les modèles sur les ordinateurs sont mis à jour quotidiennement en fonction des modifications apportées au catalogue de modèles de paramètres.

4.  Ouvrez une invite de commandes avec élévation de privilèges et naviguez jusqu’à **% Program Files%\\Microsoft User performance Virtualization \ \ agent \ \ &lt; x86 ou x64 &gt; **, puis exécutez **ApplySettingsTemplateCatalog.exe** pour mettre à jour manuellement les modèles sur un ordinateur qui exécute l’agent UE-V.

## Rubriques connexes


[Microsoft User Experience Virtualization (UE-V)1.0](index.md)

[Déploiement d'UE-V1.0](deploying-ue-v-10.md)

[Planification des applications à synchroniser avec UE-V1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 






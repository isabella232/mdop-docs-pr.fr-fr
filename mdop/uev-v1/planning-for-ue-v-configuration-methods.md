---
title: Planification de méthodes de configuration d'UE-V
description: Planification de méthodes de configuration d'UE-V
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812149"
---
# Planification de méthodes de configuration d'UE-V


Les configurations Microsoft User Interface Virtualization (UE-V) déterminent la manière dont les paramètres sont synchronisés au sein de l’entreprise. Cette rubrique décrit comment créer des configurations UE-V pour vous aider à formuler un plan de configuration qui correspond le mieux à vos besoins professionnels.

## Méthodes de configuration pour UE-V


Vous pouvez configurer UE-V avant, pendant ou après l’installation de l’agent, en fonction de la méthode de configuration que vous utilisez.

**Stratégie de groupe:** une infrastructure de stratégie de groupe existante peut être utilisée pour configurer UE-v avant ou après le déploiement de l’agent UE-v. Le modèle ADMX-V pour la gestion centralisée des options de configuration de l’agent UE-V et il comprend des paramètres pour configurer la synchronisation d’UE-V. Les environnements réseau qui utilisent une stratégie de groupe peuvent préconfigurer UE-V en prévision du déploiement de l’agent.

[Configuration d’UE-V avec les objets de stratégie de groupe](configuring-ue-v-with-group-policy-objects.md)

[Installation des modèles ADMX de stratégie de groupe UE-V](installing-the-ue-v-group-policy-admx-templates.md)

**L’installation d’un script de ligne de commande ou de lot:** les paramètres qui sont utilisés avec le déploiement de l’agent UE-v permettent de configurer de nombreux paramètres d’UE-v. Dans les systèmes de distribution de logiciels électroniques tels que System Center Configuration Manager, utilisez ces paramètres pour configurer leurs clients lors du déploiement et de l’installation du logiciel d’agent UE-V. Pour obtenir la liste des paramètres d’installation et des exemples de script d’installation, voir [déploiement de l’agent UE-V](deploying-the-ue-v-agent.md).

**PowerShell et WMI:** les commandes créées à l’aide de PowerShell ou WMI peuvent être utilisées pour modifier des configurations après l’installation d’UE-V agent. Pour obtenir la liste des commandes PowerShell et WMI, voir [gestion de l’agent et des packages d’UE-V 1,0 avec PowerShell et WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

**Modifier les paramètres du Registre:** Les paramètres d’UE-V sont stockés dans le registre et peuvent être modifiés à l’aide de n’importe quel outil permettant de modifier les paramètres du Registre, comme RegEdit.

**Remarques**  La modification du Registre peut entraîner une perte de données ou l’ordinateur ne répond plus. Nous vous recommandons d’utiliser d’autres méthodes de configuration.

 

### Paramètres de configuration d’UE-V

Vous trouverez ci-dessous des exemples de paramètres de configuration UE-V:

-   **Définition du chemin d’accès de stockage:** spécifie l’emplacement du partage de fichiers qui stocke les paramètres UE-V.

-   **Modèle de modèle de paramètres:** spécifie le chemin d’accès UNC (Universal Naming Convention) qui définit l’emplacement dans lequel les nouveaux modèles d’emplacement des paramètres sont consultés.

-   **Enregistrer les modèles Microsoft:** indique si les modèles Microsoft par défaut doivent être inscrits lors de l’installation.

-   **Méthode de synchronisation:** indique si la fonctionnalité fichiers en mode hors connexion de Windows est utilisée pour la prise en charge hors connexion.

-   **Délai d’expiration de la synchronisation:** indique le nombre de millisecondes que l’ordinateur attend avant le délai d’expiration lors de la récupération des paramètres utilisateur à partir de l’emplacement de stockage des paramètres.

-   **Activation de la synchronisation:** indique si la synchronisation des paramètres d’UE-V est activée ou désactivée.

-   **Taille maximale du package:** spécifie une taille de seuil du fichier de package de paramètres en octets auxquelles l’agent UE-V signale une alerte.

## Rubriques connexes


[Planification pour UE-V1.0](planning-for-ue-v-10.md)

[Planification de la configuration d'UE-V](planning-for-ue-v-configuration.md)

 

 






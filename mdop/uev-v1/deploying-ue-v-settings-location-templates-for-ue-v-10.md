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
# <span data-ttu-id="5b115-103">Déploiement de modèles d'emplacement de paramètres UE-V pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="5b115-103">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>


<span data-ttu-id="5b115-104">La virtualisation de l’interface utilisateur de Microsoft (UE-V) utilise des modèles d’emplacement des paramètres (fichiers XML) qui définissent les paramètres qui sont capturés et appliqués par la virtualisation de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5b115-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="5b115-105">UE-V inclut un ensemble de modèles standard, ainsi qu’un outil, le générateur UE-V, qui vous permet de créer des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5b115-105">UE-V includes a set of standard templates, as well as a tool, the UE-V Generator, which allows you to create custom settings location templates.</span></span> <span data-ttu-id="5b115-106">Après avoir créé un modèle d’emplacement des paramètres, vous devez le tester pour vous assurer que les paramètres de l’application s’immobilessent correctement dans un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="5b115-106">After you create a settings location template, you should test it to ensure that the application settings roam correctly in a test environment.</span></span> <span data-ttu-id="5b115-107">Vous pouvez ensuite déployer en toute sécurité le modèle d’emplacement des paramètres sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="5b115-107">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="5b115-108">Les modèles d’emplacement des paramètres peuvent être déployés à l’aide de la distribution de logiciels d’entreprise, des préférences de stratégie de groupe, ou en configurant un catalogue de modèles de paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="5b115-108">Settings location templates can be deployed by using enterprise software distribution (ESD), Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="5b115-109">Les modèles déployés à l’aide d’une stratégie de groupe ou d’ESD doivent être inscrits via le WMI ou PowerShell d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="5b115-109">Templates that are deployed by using an ESD or Group Policy must be registered through UE-V WMI or PowerShell.</span></span> <span data-ttu-id="5b115-110">Les modèles stockés dans l’emplacement du catalogue de modèles de paramètres sont automatiquement inscrits par l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="5b115-110">Templates that are stored in the settings template catalog location are automatically registered by the UE-V agent.</span></span>

## <span data-ttu-id="5b115-111">Déployer les modèles d’emplacement des paramètres à l’aide d’un chemin d’accès au catalogue de modèles de paramètres</span><span class="sxs-lookup"><span data-stu-id="5b115-111">Deploy the settings location templates with a settings template catalog path</span></span>


<span data-ttu-id="5b115-112">Le chemin du catalogue de modèles d’emplacement des paramètres d’UE-V peut être défini à l’aide des méthodes suivantes: stratégie de groupe, paramètres de ligne de commande d’installation de l’agent, WMI ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5b115-112">The UE-V settings location template catalog path can be defined by using the following methods: Group Policy, the agent install command-line parameters, WMI, or PowerShell.</span></span> <span data-ttu-id="5b115-113">Après avoir défini le chemin du catalogue de modèles, UE-V agent récupère les modèles nouveaux ou mis à jour à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="5b115-113">After the template catalog path has been defined, the UE-V agent retrieves the new or updated templates from this location.</span></span> <span data-ttu-id="5b115-114">L’agent UE-V vérifie cet emplacement une fois par jour et met à jour son comportement de synchronisation en fonction des modèles figurant dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="5b115-114">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates found in this folder.</span></span> <span data-ttu-id="5b115-115">Les modèles qui ont été ajoutés ou mis à jour dans ce dossier depuis la dernière vérification sont inscrits par l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="5b115-115">Templates that have been added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="5b115-116">UE-V agent annule également les modèles qui ont été supprimés de ce dossier.</span><span class="sxs-lookup"><span data-stu-id="5b115-116">The UE-V agent also unregisters templates that have been removed from this folder.</span></span> <span data-ttu-id="5b115-117">Les modèles sont inscrits et annulés une fois par jour par le planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="5b115-117">Templates are registered and unregistered one time per day by the task scheduler.</span></span>

**<span data-ttu-id="5b115-118">Pour utiliser le modèle de modèle de paramètres pour déployer des modèles d’emplacement des paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="5b115-118">To use settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="5b115-119">Naviguez jusqu’au dossier de partage réseau défini comme catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5b115-119">Navigate to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="5b115-120">Ajoutez, supprimez ou mettez à jour les modèles d’emplacement des paramètres dans le catalogue de modèles de paramètres pour refléter la configuration de modèle d’agent UE-V requise pour les ordinateurs UE-V.</span><span class="sxs-lookup"><span data-stu-id="5b115-120">Add, remove, or update settings location templates in the settings template catalog to reflect the desired UE-V agent template configuration for UE-V computers.</span></span>

3.  <span data-ttu-id="5b115-121">Les modèles sur les ordinateurs sont mis à jour quotidiennement en fonction des modifications apportées au catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5b115-121">Templates on computers are updated daily based on changes to the settings template catalog.</span></span>

4.  <span data-ttu-id="5b115-122">Ouvrez une invite de commandes avec élévation de privilèges et naviguez jusqu’à \*\*% Program Files%\\Microsoft User performance Virtualization \ \ agent \ \ &lt; x86 ou x64 &gt; \*\*, puis exécutez **ApplySettingsTemplateCatalog.exe** pour mettre à jour manuellement les modèles sur un ordinateur qui exécute l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="5b115-122">Open an elevated command prompt and navigate to **%program files%\\Microsoft user Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe** to manually update templates on a computer that runs the UE-V agent.</span></span>

## <span data-ttu-id="5b115-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b115-123">Related topics</span></span>


[<span data-ttu-id="5b115-124">Microsoft User Experience Virtualization (UE-V)1.0</span><span class="sxs-lookup"><span data-stu-id="5b115-124">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="5b115-125">Déploiement d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="5b115-125">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="5b115-126">Planification des applications à synchroniser avec UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="5b115-126">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 






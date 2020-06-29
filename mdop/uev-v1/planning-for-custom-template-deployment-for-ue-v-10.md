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
# <span data-ttu-id="2d2ed-103">Planification du déploiement de modèle personnalisé d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="2d2ed-103">Planning for Custom Template Deployment for UE-V 1.0</span></span>


<span data-ttu-id="2d2ed-104">La virtualisation de l’utilisation de Microsoft User (UE-V) utilise des modèles d’emplacement des paramètres (fichiers XML) qui définissent les paramètres capturés et appliqués par UE-V.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="2d2ed-105">Vous pouvez utiliser le générateur UE-V pour créer des modèles d’emplacement des paramètres personnalisés qui permettent aux utilisateurs d’utiliser les paramètres des applications qui ne sont pas incluses dans les modèles UE-V par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-105">You can use the UE-V Generator to create custom settings location templates that let users roam the settings of applications other than those that are included in the default UE-V templates.</span></span> <span data-ttu-id="2d2ed-106">Après avoir testé le modèle personnalisé pour vous assurer que les paramètres de l’application s’immobilent correctement dans un environnement de test, vous pouvez déployer ces modèles d’emplacement des paramètres sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-106">After you test the custom template to ensure that the application settings roam correctly in a test environment, you can deploy these settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="2d2ed-107">Vous pouvez déployer vos modèles d’emplacement des paramètres personnalisés avec une infrastructure de déploiement existante, telle que la distribution de logiciels d’entreprise, avec des préférences de stratégie de groupe, ou en configurant un catalogue de modèles de paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-107">You can deploy your custom settings location templates with an existing deployment infrastructure, such as Enterprise Software Distribution (ESD), with Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="2d2ed-108">Les modèles déployés à l’aide de ESD ou d’une stratégie de groupe doivent être enregistrés auprès d’UE-V WMI ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-108">Templates that are deployed by using ESD or Group Policy must be registered with UE-V WMI or PowerShell.</span></span>

## <span data-ttu-id="2d2ed-109">Catalogue de modèles de paramètres</span><span class="sxs-lookup"><span data-stu-id="2d2ed-109">Settings template catalog</span></span>


<span data-ttu-id="2d2ed-110">Le catalogue de modèles de paramètres de virtualisation de l’utilisation de l’utilisateur est un chemin de dossier sur les ordinateurs UE-V ou un partage réseau SMB qui stocke tous les modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-110">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="2d2ed-111">L’agent UE-V récupère les modèles nouveaux ou mis à jour à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-111">The UE-V agent retrieves new or updated templates from this location.</span></span> <span data-ttu-id="2d2ed-112">L’agent UE-V vérifie cet emplacement une fois par jour et met à jour son comportement de synchronisation en fonction des modèles figurant dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-112">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="2d2ed-113">Les modèles ajoutés ou mis à jour dans ce dossier depuis la dernière fois où le dossier a été activé sont enregistrés par l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-113">Templates that were added or updated in this folder since the last time that the folder was checked are registered by the UE-V agent.</span></span> <span data-ttu-id="2d2ed-114">UE-V agent annule les modèles supprimés de ce dossier.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-114">The UE-V agent deregisters templates that are removed from this folder.</span></span> <span data-ttu-id="2d2ed-115">Par défaut, les modèles sont inscrits et annulés une fois par jour à 3:30 matin.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-115">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="2d2ed-116">heure locale par le planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-116">local time by the task scheduler.</span></span> <span data-ttu-id="2d2ed-117">Pour plus d’informations sur les tâches UE-V, voir [modification de la fréquence des tâches planifiées UE-v](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="2d2ed-117">For more information about the UE-V tasks, see [Changing the Frequency of UE-V Scheduled Tasks](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span></span>

<span data-ttu-id="2d2ed-118">Vous pouvez configurer le chemin du catalogue de modèles de paramètres à l’aide des options de ligne de commande d’installation, de stratégie de groupe, de WMI ou d’PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-118">You can configure the settings template catalog path by using the install command-line options, Group Policy, WMI, or PowerShell.</span></span> <span data-ttu-id="2d2ed-119">Les modèles stockés dans le modèle de modèle paramètres sont automatiquement inscrits et désinscrits par une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-119">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span> <span data-ttu-id="2d2ed-120">Vous pouvez personnaliser cette tâche planifiée selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-120">You can customize this scheduled task as needed.</span></span>

## <span data-ttu-id="2d2ed-121">Remplacer les modèles Microsoft par défaut</span><span class="sxs-lookup"><span data-stu-id="2d2ed-121">Replace the default Microsoft templates</span></span>


<span data-ttu-id="2d2ed-122">L’agent UE-V installe un groupe par défaut de modèles d’emplacements de paramètres pour les applications Microsoft courantes et les paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-122">The UE-V agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="2d2ed-123">Si votre entreprise a besoin d’une version personnalisée de ces modèles, l’agent UE-V peut être configuré pour utiliser un catalogue de modèles de paramètres, puis remplacer les modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-123">If your enterprise needs customized versions of these templates, the UE-V agent can be configured to use a settings template catalog and you should then replace the default Microsoft templates.</span></span>

<span data-ttu-id="2d2ed-124">Lors de l’installation de l’agent UE-V, le paramètre de ligne de commande, `RegisterMSTemplates` qui peut être utilisé pour désactiver l’inscription des modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-124">During the installation of the UE-V agent, the command-line parameter, `RegisterMSTemplates`, can be used to disable the registration of the default Microsoft templates.</span></span> <span data-ttu-id="2d2ed-125">Pour plus d’informations sur la définition des paramètres de UE-V, voir [planification pour les méthodes de configuration de UE-v](planning-for-ue-v-configuration-methods.md).</span><span class="sxs-lookup"><span data-stu-id="2d2ed-125">For more information about how to set the UE-V parameters, see [Planning for UE-V Configuration Methods](planning-for-ue-v-configuration-methods.md).</span></span>

<span data-ttu-id="2d2ed-126">Lorsque vous utilisez une stratégie de groupe pour configurer le chemin du catalogue de modèles de paramètres, vous pouvez choisir de remplacer les modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-126">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="2d2ed-127">Si vous configurez les paramètres de stratégie pour remplacer les modèles Microsoft par défaut, tous les modèles Microsoft par défaut installés par l’agent UE-V seront supprimés de l’ordinateur et seuls les modèles figurant dans le catalogue de modèles de paramètres seront utilisés.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-127">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V agent will be deleted from the computer, and only the templates that are located in the settings template catalog will be used.</span></span> <span data-ttu-id="2d2ed-128">Le paramètre de configuration de l’agent UE-V `RegisterMSTemplates` doit être défini sur true pour pouvoir remplacer le modèle Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-128">The UE-V Agent configuration setting `RegisterMSTemplates` must be set to true in order to override the default Microsoft template.</span></span>

<span data-ttu-id="2d2ed-129">**Remarques**  Si vous désactivez ce paramètre de stratégie une fois qu’il est activé, l’agent UE-V ne restaure pas les modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-129">**Note** If you disable this policy setting after it has been enabled, the UE-V agent will not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="2d2ed-130">S’il existe des modèles personnalisés dans le catalogue de modèles de paramètres qui utilisent le même IDENTIFIant que les modèles Microsoft par défaut, et que l’agent UE-V n’est pas configuré pour remplacer les modèles Microsoft par défaut, les modèles Microsoft dans le catalogue seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-130">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V agent is not configured to replace the default Microsoft templates, the Microsoft templates in the catalog will be ignored.</span></span>

<span data-ttu-id="2d2ed-131">Vous pouvez également remplacer les modèles par défaut en utilisant les fonctionnalités PowerShell d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-131">You can also replace the default templates by using the UE-V PowerShell features.</span></span> <span data-ttu-id="2d2ed-132">Pour remplacer le modèle Microsoft par défaut par PowerShell, annulez l’enregistrement de tous les modèles Microsoft par défaut, puis enregistrez les modèles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-132">To replace the default Microsoft Template with PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="2d2ed-133">**Remarques**  Les packages d’anciens paramètres restent dans l’emplacement de stockage des paramètres même si de nouveaux modèles de paramètres sont déployés pour une application.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-133">**Note** Old settings packages remain in the settings storage location even if new settings templates are deployed for an application.</span></span> <span data-ttu-id="2d2ed-134">Ces packages ne sont pas lus par l’agent, mais aucun d’eux n’est automatiquement supprimé.</span><span class="sxs-lookup"><span data-stu-id="2d2ed-134">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <span data-ttu-id="2d2ed-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d2ed-135">Related topics</span></span>


[<span data-ttu-id="2d2ed-136">Planification pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="2d2ed-136">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="2d2ed-137">Planification des applications à synchroniser avec UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="2d2ed-137">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

[<span data-ttu-id="2d2ed-138">Planification de méthodes de configuration d'UE-V</span><span class="sxs-lookup"><span data-stu-id="2d2ed-138">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

<span data-ttu-id="2d2ed-139">Planification du déploiement d’un modèle personnalisé</span><span class="sxs-lookup"><span data-stu-id="2d2ed-139">Planning for Custom Template Deployment</span></span>
 

 






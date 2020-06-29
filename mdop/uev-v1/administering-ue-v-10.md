---
title: Administration d'UE-V1.0
description: Administration d'UE-V1.0
author: dansimp
ms.assetid: c399ae8d-c839-4f84-9bfc-adacd8f89f34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4dcafd1949dcedd195569dabb7540ce55a2f1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809510"
---
# <span data-ttu-id="b2930-103">Administration d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2930-103">Administering UE-V 1.0</span></span>


<span data-ttu-id="b2930-104">Une fois que vous avez déployé la virtualisation de l’utilisation de Microsoft Users (UE-V), vous devez être en mesure d’effectuer diverses tâches d’administration courantes.</span><span class="sxs-lookup"><span data-stu-id="b2930-104">After you have deployed Microsoft User Experience Virtualization (UE-V), you must be able to perform various ongoing administrative tasks.</span></span> <span data-ttu-id="b2930-105">Ces tâches de post-installation sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2930-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="b2930-106">Gestion des ressources UE-V</span><span class="sxs-lookup"><span data-stu-id="b2930-106">Managing UE-V resources</span></span>


<span data-ttu-id="b2930-107">Dans le cadre du cycle de vie d’UE-V, vous devez gérer la configuration de l’agent UE-V et gérer les emplacements de stockage des ressources telles que les packages de paramètres.</span><span class="sxs-lookup"><span data-stu-id="b2930-107">In the course of the UE-V lifecycle, you will need to manage the configuration of the UE-V agent and also manage storage locations for resources such as settings packages.</span></span> <span data-ttu-id="b2930-108">Vous devrez peut-être effectuer d’autres tâches, par exemple pour rétablir l’état d’origine des paramètres d’un utilisateur antérieurs à l’installation de UE-V, afin de récupérer les paramètres perdus.</span><span class="sxs-lookup"><span data-stu-id="b2930-108">You might need to perform other tasks such as to restore a user’s settings to their original state from before UE-V was installed in order to recover lost settings.</span></span> <span data-ttu-id="b2930-109">Les rubriques suivantes fournissent des instructions pour la gestion des ressources d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="b2930-109">The following topics provide guidance for managing UE-V resources.</span></span>

### <span data-ttu-id="b2930-110">Modification de la fréquence des tâches planifiées UE-V</span><span class="sxs-lookup"><span data-stu-id="b2930-110">Changing the Frequency of UE-V Scheduled Tasks</span></span>

<span data-ttu-id="b2930-111">Vous pouvez configurer les tâches planifiées qui gèrent lorsque UE-V recherche les modèles d’emplacements personnalisés nouveaux, mis à jour ou supprimés supprimés dans le catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="b2930-111">You can configure the scheduled tasks that manage when UE-V checks for new, updated, or removed custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="b2930-112">Modification de la fréquence des tâches planifiées UE-V</span><span class="sxs-lookup"><span data-stu-id="b2930-112">Changing the Frequency of UE-V Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-scheduled-tasks.md)

### <a href="" id="sharing-settings-location-templates-with-the-ue-v-template-gallery-"></a><span data-ttu-id="b2930-113">Modèles d'emplacement des paramètres de partage avec la galerie des modèles UE-V</span><span class="sxs-lookup"><span data-stu-id="b2930-113">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>

<span data-ttu-id="b2930-114">La Galerie de modèles UE-V facilite le partage des modèles d’emplacement des paramètres de UE-V.</span><span class="sxs-lookup"><span data-stu-id="b2930-114">The UE-V template gallery facilitates the sharing of UE-V settings location templates.</span></span> <span data-ttu-id="b2930-115">La Galerie vous permet de télécharger vos modèles d’emplacements de paramètres pour les partager avec d’autres personnes et de télécharger des modèles que d’autres personnes ont créés.</span><span class="sxs-lookup"><span data-stu-id="b2930-115">The gallery enables you to upload your settings location templates to share with other people and to download templates that other people have created.</span></span>

[<span data-ttu-id="b2930-116">Modèles d'emplacement des paramètres de partage avec la galerie des modèles UE-V</span><span class="sxs-lookup"><span data-stu-id="b2930-116">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>](sharing-settings-location-templates-with-the-ue-v-template-gallery.md)

### <span data-ttu-id="b2930-117">Restauration des paramètres d’application et de fenêtre synchronisés avec UE-V 1,0</span><span class="sxs-lookup"><span data-stu-id="b2930-117">Restoring application and Windows settings synchronized with UE-V 1.0</span></span>

<span data-ttu-id="b2930-118">Les fonctionnalités WMI et PowerShell d’UE-V permettent de restaurer les packages de paramètres.</span><span class="sxs-lookup"><span data-stu-id="b2930-118">WMI and PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="b2930-119">Les commandes WMI et PowerShell vous permettent de restaurer les paramètres d’application et les paramètres Windows aux valeurs de paramètres qui se trouvaient sur l’ordinateur lors du premier démarrage de l’application après le lancement de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="b2930-119">WMI and PowerShell commands allow you to restore application settings and Windows settings to the settings values that were on the computer the first time the application was started after the UE-V agent was launched.</span></span>

[<span data-ttu-id="b2930-120">Restauration des applications et des paramètres Windows synchronisés avec UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2930-120">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)

### <span data-ttu-id="b2930-121">Configuration d'UE-V avec les objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b2930-121">Configuring UE-V with Group Policy Objects</span></span>

<span data-ttu-id="b2930-122">Vous pouvez utiliser une stratégie de groupe pour modifier les paramètres qui déterminent la façon dont UE-V synchronise les paramètres sur les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="b2930-122">You can use Group Policy to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="b2930-123">Configuration d’UE-V avec les objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b2930-123">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

### <span data-ttu-id="b2930-124">Administration d'UE-V avec PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="b2930-124">Administering UE-V with PowerShell and WMI</span></span>

<span data-ttu-id="b2930-125">Vous pouvez utiliser PowerShell et WMI pour modifier les paramètres définissant le mode de synchronisation des paramètres sur les ordinateurs par UE-V.</span><span class="sxs-lookup"><span data-stu-id="b2930-125">You can use PowerShell and WMI to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="b2930-126">Gestion de l'agent UE-V1.0 et des packages avec PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="b2930-126">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

### <span data-ttu-id="b2930-127">Migration des packages de paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="b2930-127">Migrating UE-V Settings Packages</span></span>

<span data-ttu-id="b2930-128">Vous pouvez déplacer les packages de paramètres utilisateur lors de la migration vers un nouveau serveur ou à des fins de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="b2930-128">You can relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span>

[<span data-ttu-id="b2930-129">Migration des packages de paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="b2930-129">Migrating UE-V Settings Packages</span></span>](migrating-ue-v-settings-packages.md)

## <span data-ttu-id="b2930-130">Autres ressources pour ce produit</span><span class="sxs-lookup"><span data-stu-id="b2930-130">Other resources for this product</span></span>


[<span data-ttu-id="b2930-131">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2930-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 






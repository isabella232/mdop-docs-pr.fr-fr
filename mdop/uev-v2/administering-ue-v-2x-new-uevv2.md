---
title: Administration d’UE-V 2. x
description: Administration d’UE-V 2. x
author: dansimp
ms.assetid: 996e4797-8383-4627-b714-24a84c907798
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2674f6ace80672c1e89bb4f9c765b56f260c3bc0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811297"
---
# <span data-ttu-id="c439b-103">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-103">Administering UE-V 2.x</span></span>


<span data-ttu-id="c439b-104">Une fois que vous avez déployé Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, vous devez être en mesure d’effectuer diverses tâches d’administration courantes, telles que la gestion de la configuration de l’agent UE-V et la récupération des paramètres perdus.</span><span class="sxs-lookup"><span data-stu-id="c439b-104">After you have deployed Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you must be able to perform various ongoing administrative tasks, such as managing the configuration of the UE-V Agent and recovering lost settings.</span></span> <span data-ttu-id="c439b-105">Ces tâches de post-installation sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c439b-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="c439b-106">Gestion des configurations UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-106">Managing UE-V 2.x configurations</span></span>


<span data-ttu-id="c439b-107">Dans le cadre du cycle de vie d’UE-V, vous devez gérer la configuration de l’agent UE-V et gérer les emplacements de stockage des ressources telles que les fichiers du package de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c439b-107">In the course of the UE-V lifecycle, you have to manage the configuration of the UE-V Agent and also manage storage locations for resources such as settings package files.</span></span>

[<span data-ttu-id="c439b-108">Gérer les configurations pour UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="c439b-108">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

## <span data-ttu-id="c439b-109">Utilisation de modèles UE-V personnalisés et du générateur UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-109">Working with custom UE-V templates and the UE-V 2.x Generator</span></span>


<span data-ttu-id="c439b-110">Cette rubrique fournit des instructions sur l’utilisation du générateur UE-V et sur la gestion des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c439b-110">This topic provides instructions for how to use the UE-V Generator and manage custom settings location templates.</span></span>

[<span data-ttu-id="c439b-111">Utilisation de modèles UE-V 2 ou x personnalisés et du générateur UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-111">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

## <span data-ttu-id="c439b-112">Sauvegarder et restaurer des paramètres d’application et de fenêtre qui sont synchronisés avec UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-112">Backup and restore application and Windows settings that are synchronized with UE-V 2.x</span></span>


<span data-ttu-id="c439b-113">Les fonctionnalités WMI (Windows Management Instrumentation) et Windows PowerShell d’UE-V permettent de restaurer les packages de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c439b-113">Windows Management Instrumentation (WMI) and Windows PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="c439b-114">Les commandes WMI et Windows PowerShell vous permettent de restaurer l’état d’origine des paramètres d’application et de fenêtre, et de restaurer des paramètres supplémentaires lorsqu’un utilisateur adopte un nouvel appareil.</span><span class="sxs-lookup"><span data-stu-id="c439b-114">By using WMI and Windows PowerShell commands, you can restore application and Windows settings to their original state and restore additional settings when a user adopts a new device.</span></span>

[<span data-ttu-id="c439b-115">Gérer la sauvegarde et la restauration d’administration dans UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-115">Manage Administrative Backup and Restore in UE-V 2.x</span></span>](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md)

## <span data-ttu-id="c439b-116">Modification de la fréquence des tâches planifiées UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-116">Changing the frequency of UE-V 2.x scheduled tasks</span></span>


<span data-ttu-id="c439b-117">Vous pouvez configurer les tâches planifiées qui gèrent lorsque UE-V recherche des paramètres nouveaux ou mis à jour ou des modèles d’emplacement des paramètres personnalisés mis à jour dans le catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c439b-117">You can configure the scheduled tasks that manage when UE-V checks for new or updated settings or for updated custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="c439b-118">Modification de la fréquence des tâches planifiées UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-118">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

## <span data-ttu-id="c439b-119">Migration des packages de paramètres UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-119">Migrating UE-V 2.x settings packages</span></span>


<span data-ttu-id="c439b-120">Vous pouvez déplacer les packages de paramètres d’utilisateur soit lors de leur migration vers un nouveau serveur, soit à des fins de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="c439b-120">You can relocate the user settings packages either when they migrate to a new server or for backup purposes.</span></span>

[<span data-ttu-id="c439b-121">Migration des packages de paramètres UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-121">Migrating UE-V 2.x Settings Packages</span></span>](migrating-ue-v-2x-settings-packages-both-uevv2.md)

## <span data-ttu-id="c439b-122">Utilisation d’UE-V 2. x avec les applications de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="c439b-122">Using UE-V 2.x with Application Virtualization applications</span></span>


<span data-ttu-id="c439b-123">Vous pouvez utiliser UE-V avec Microsoft Application Virtualization (App-v) pour partager les paramètres entre des applications virtuelles et des applications installées sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="c439b-123">You can use UE-V with Microsoft Application Virtualization (App-V) to share settings between virtual applications and installed applications across multiple computers.</span></span>

[<span data-ttu-id="c439b-124">Utilisation d’UE-V 2. x avec les applications de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="c439b-124">Using UE-V 2.x with Application Virtualization Applications</span></span>](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md)

## <span data-ttu-id="c439b-125">Autres ressources pour ce produit</span><span class="sxs-lookup"><span data-stu-id="c439b-125">Other resources for this product</span></span>


-   [<span data-ttu-id="c439b-126">Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-126">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="c439b-127">Prise en main d'UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="c439b-127">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="c439b-128">Préparer un déploiement UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-128">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="c439b-129">Résolution des problèmes de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c439b-129">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="c439b-130">Informations techniques de référence sur UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="c439b-130">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 






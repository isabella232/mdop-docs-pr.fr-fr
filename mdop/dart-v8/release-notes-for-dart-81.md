---
title: Notes de publication pour DaRT8.1
description: Notes de publication pour DaRT8.1
author: dansimp
ms.assetid: 44303107-60f4-485c-848a-7e0529f142d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d0ba817ddd5bbdefcf7fed833f4c47e7b9d9ce0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810751"
---
# <span data-ttu-id="a6752-103">Notes de publication pour DaRT8.1</span><span class="sxs-lookup"><span data-stu-id="a6752-103">Release Notes for DaRT 8.1</span></span>


**<span data-ttu-id="a6752-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="a6752-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="a6752-105">Lisez attentivement ces notes de publication avant de procéder à l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 8,1.</span><span class="sxs-lookup"><span data-stu-id="a6752-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1.</span></span>

<span data-ttu-id="a6752-106">Ces notes de publication contiennent des informations nécessaires à l’installation réussie des 8,1 outils de diagnostics et de récupération.</span><span class="sxs-lookup"><span data-stu-id="a6752-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.1.</span></span> <span data-ttu-id="a6752-107">Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="a6752-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="a6752-108">S’il existe une différence entre ces notes de publication et d’autres documents DaRT, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="a6752-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="a6752-109">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="a6752-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="a6752-110">Problèmes connus avec le 8,1 DaRT</span><span class="sxs-lookup"><span data-stu-id="a6752-110">Known issues with DaRT 8.1</span></span>


### <span data-ttu-id="a6752-111">Disk commander ne peut pas réparer un enregistrement de démarrage maître endommagé dans une partition physique dans Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="a6752-111">Disk Commander is unable to repair a corrupt master boot record in a physical partition in Windows 8.1</span></span>

<span data-ttu-id="a6752-112">Dans Windows 8,1, l’option «restaurer l’enregistrement de démarrage principal (MBR) ou l’en-tête de la table de partitions GUID (GPT) dans Disk commander ne peut pas réparer un enregistrement de démarrage maître endommagé dans une partition physique, et ne peut donc pas démarrer l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="a6752-112">In Windows 8.1, the “Restore the Master Boot Record (MBR) or the header of the GUID Partition Table (GPT)” option in Disk Commander is unable to repair a corrupt master boot record in a physical partition, and therefore is unable to boot the client computer.</span></span>

<span data-ttu-id="a6752-113">**Solution de contournement:** Cliquez sur **résolution des problèmes** **, sur** **Options avancées**, puis sur Démarrer la **réparation**.</span><span class="sxs-lookup"><span data-stu-id="a6752-113">**Workaround:** Start **Startup Repair**, click **Troubleshoot**, click **Advanced options**, and then click **Start repair**.</span></span>

### <span data-ttu-id="a6752-114">Plusieurs instances d’une réinitialisation de disque qui ciblent le même lecteur, à l’exception de la première, de signaler une panne.</span><span class="sxs-lookup"><span data-stu-id="a6752-114">Multiple instances of Disk Wipe that target the same drive cause all instances except the last one to report a failure</span></span>

<span data-ttu-id="a6752-115">Si vous démarrez plusieurs instances de Disk Wipe et que vous essayez de réinitialiser le même lecteur en utilisant deux instances de réinitialisation de disque distinctes, toutes les instances à l’exception du dernier indiquent un échec de réinitialisation du lecteur.</span><span class="sxs-lookup"><span data-stu-id="a6752-115">If you start multiple instances of Disk Wipe, and then try to wipe the same drive by using two separate Disk Wipe instances, all instances except the last one report a failure to wipe the drive.</span></span>

<span data-ttu-id="a6752-116">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="a6752-116">**Workaround:** None.</span></span>

### <span data-ttu-id="a6752-117">La réinitialisation du disque risque de ne pas effacer toutes les données sur les lecteurs à état solide disposant d’une mémoire flash</span><span class="sxs-lookup"><span data-stu-id="a6752-117">Disk Wipe may not clear all data on solid-state drives that have flash memory</span></span>

<span data-ttu-id="a6752-118">Si vous utilisez la fonction de réinitialisation du disque pour effacer les données sur un disque SSD qui est doté de mémoire flash, il est possible que l’ensemble des données ne soient pas effacées.</span><span class="sxs-lookup"><span data-stu-id="a6752-118">If you use Disk Wipe to clear data on a solid-state drive (SSD) that has flash memory, all of the data may not be erased.</span></span> <span data-ttu-id="a6752-119">Ce problème se produit car le microprogramme SSD contrôle l’emplacement physique des écritures lorsque le disque est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a6752-119">This issue occurs because the SSD firmware controls the physical location of writes while Disk Wipe is running.</span></span>

<span data-ttu-id="a6752-120">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="a6752-120">**Workaround:** None.</span></span>

### <span data-ttu-id="a6752-121">La restauration du système échoue lorsque vous exécutez l’Assistant Locksmith ou l’éditeur du Registre</span><span class="sxs-lookup"><span data-stu-id="a6752-121">System restore fails when you run Locksmith Wizard or Registry Editor</span></span>

<span data-ttu-id="a6752-122">Si vous exécutez l’Assistant Locksmith, l’éditeur du Registre et éventuellement d’autres outils, la restauration du système échoue.</span><span class="sxs-lookup"><span data-stu-id="a6752-122">If you run Locksmith Wizard, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="a6752-123">**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez la restauration du système.</span><span class="sxs-lookup"><span data-stu-id="a6752-123">**Workaround:** Close and restart DaRT, and then start System Restore.</span></span>

### <span data-ttu-id="a6752-124">Le vérificateur des fichiers système ne peut pas être exécuté après que vous avez démarré et fermé Locksmith Assistant ou la gestion de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="a6752-124">System File Checker (SFC) Scan fails to run after you start and close Locksmith Wizard or Computer Management</span></span>

<span data-ttu-id="a6752-125">Si vous démarrez, puis fermez Locksmith Assistant ou outils dans gestion de l’ordinateur, le vérificateur de fichiers système ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="a6752-125">If you start and then close Locksmith Wizard or tools in Computer Management, System File Checker fails to run.</span></span>

<span data-ttu-id="a6752-126">**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez le vérificateur des fichiers système.</span><span class="sxs-lookup"><span data-stu-id="a6752-126">**Workaround:** Close and restart DaRT, and then start System File Checker.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> <span data-ttu-id="a6752-127">Le programme d’installation de DaRT ne fonctionne pas lorsque le kit d’évaluation et de déploiement Windows n’est pas installé</span><span class="sxs-lookup"><span data-stu-id="a6752-127">DaRT installer does not fail when the Windows Assessment and Deployment Kit is not installed</span></span>

<span data-ttu-id="a6752-128">Si vous installez DaRT 8,1 à l’aide de la ligne de commande pour exécuter Windows Installer (. msi) et que le kit d’évaluation et de déploiement Windows (WindowsADK) n’a pas été installé, l’installation DaRT doit échouer.</span><span class="sxs-lookup"><span data-stu-id="a6752-128">If you install DaRT 8.1 by using the command line to run the Windows Installer (.msi), and the Windows Assessment and Deployment Kit (WindowsADK) has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="a6752-129">Pour le moment, le programme d’installation 8,1 de DaRT installe tous les composants, à l’exception de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="a6752-129">Currently, the DaRT 8.1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="a6752-130">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="a6752-130">**Workaround:** None.</span></span>

### <span data-ttu-id="a6752-131">Windows Defender ne peut pas démarrer après le démarrage de l’Assistant Locksmith, de l’éditeur du Registre, de l’analyse crash et de la gestion de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="a6752-131">Windows Defender cannot start after Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management are started</span></span>

<span data-ttu-id="a6752-132">Windows Defender ne démarre pas si vous avez déjà démarré l’Assistant Locksmith, l’éditeur du Registre, l’analyse crash et la gestion de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a6752-132">Windows Defender does not start if you have already started Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="a6752-133">**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="a6752-133">**Workaround:** Close and restart DaRT, and then start Windows Defender.</span></span>

### <span data-ttu-id="a6752-134">Windows Defender risque de ne pas être démarré</span><span class="sxs-lookup"><span data-stu-id="a6752-134">Windows Defender may be slow to start</span></span>

<span data-ttu-id="a6752-135">Le démarrage de Windows Defender peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="a6752-135">Windows Defender sometimes takes a few minutes to start.</span></span> <span data-ttu-id="a6752-136">La barre de progression indique l’état de chargement actuel.</span><span class="sxs-lookup"><span data-stu-id="a6752-136">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="a6752-137">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="a6752-137">**Workaround:** None.</span></span>

## <span data-ttu-id="a6752-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6752-138">Related topics</span></span>


[<span data-ttu-id="a6752-139">À propos de DaRT8.1</span><span class="sxs-lookup"><span data-stu-id="a6752-139">About DaRT 8.1</span></span>](about-dart-81.md)

 

 






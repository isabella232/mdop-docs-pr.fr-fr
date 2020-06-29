---
title: Options de ligne de commande pour les fichiers d'installation de MED-V
description: Options de ligne de commande pour les fichiers d'installation de MED-V
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811772"
---
# <span data-ttu-id="63873-103">Options de ligne de commande pour les fichiers d'installation de MED-V</span><span class="sxs-lookup"><span data-stu-id="63873-103">Command-Line Options for MED-V Installation Files</span></span>


<span data-ttu-id="63873-104">Lors de l’installation ou de la désinstallation de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, vous avez la possibilité d’exécuter les fichiers d’installation à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="63873-104">When you install or uninstall Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="63873-105">Cette section décrit les différentes options que vous pouvez spécifier lorsque vous installez ou désinstallez MED-V à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="63873-105">This section describes different options that you can specify when you install or uninstall MED-V at the command prompt.</span></span>

### <span data-ttu-id="63873-106">Arguments de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="63873-106">Command-Line Arguments</span></span>

<span data-ttu-id="63873-107">Vous pouvez utiliser les arguments de ligne de commande suivants avec leurs fichiers d’installation MED-V correspondants.</span><span class="sxs-lookup"><span data-stu-id="63873-107">You can use the following command-line arguments together with their respective MED-V installation files.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63873-108">Fichier d’installation</span><span class="sxs-lookup"><span data-stu-id="63873-108">Installation File</span></span></th>
<th align="left"><span data-ttu-id="63873-109">Argument</span><span class="sxs-lookup"><span data-stu-id="63873-109">Argument</span></span></th>
<th align="left"><span data-ttu-id="63873-110">Valeurs acceptées</span><span class="sxs-lookup"><span data-stu-id="63873-110">Accepted Values</span></span></th>
<th align="left"><span data-ttu-id="63873-111">Type</span><span class="sxs-lookup"><span data-stu-id="63873-111">Type</span></span></th>
<th align="left"><span data-ttu-id="63873-112">Description</span><span class="sxs-lookup"><span data-stu-id="63873-112">Description</span></span></th>
<th align="left"><span data-ttu-id="63873-113">Par défaut</span><span class="sxs-lookup"><span data-stu-id="63873-113">Default</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63873-114">Agent hôte</span><span class="sxs-lookup"><span data-stu-id="63873-114">Host Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-115">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="63873-115">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-116">&lt;chemin d’installation&gt;</span><span class="sxs-lookup"><span data-stu-id="63873-116">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-117">Installation</span><span class="sxs-lookup"><span data-stu-id="63873-117">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-118">Changer le répertoire installé</span><span class="sxs-lookup"><span data-stu-id="63873-118">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-119">L’installation accède à Program Files\Microsoft Enterprise Desktop Virtualization.</span><span class="sxs-lookup"><span data-stu-id="63873-119">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63873-120">Module de création de package de l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="63873-120">MED-V Workspace Packager</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-121">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="63873-121">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-122">&lt;chemin d’installation&gt;</span><span class="sxs-lookup"><span data-stu-id="63873-122">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-123">Installation</span><span class="sxs-lookup"><span data-stu-id="63873-123">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-124">Changer le répertoire installé</span><span class="sxs-lookup"><span data-stu-id="63873-124">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-125">L’installation accède à Program Files\Microsoft Enterprise Desktop Virtualization.</span><span class="sxs-lookup"><span data-stu-id="63873-125">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63873-126">Espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="63873-126">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-127">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="63873-127">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-128">&lt;chemin d’installation&gt;</span><span class="sxs-lookup"><span data-stu-id="63873-128">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-129">Installation</span><span class="sxs-lookup"><span data-stu-id="63873-129">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-130">Changer le répertoire installé</span><span class="sxs-lookup"><span data-stu-id="63873-130">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-131">Installation de ProgramData\Microsoft\Medv\Workspace.</span><span class="sxs-lookup"><span data-stu-id="63873-131">Installation goes to ProgramData\Microsoft\Medv\Workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63873-132">Espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="63873-132">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-133">REMPLACEMENT DU VHD</span><span class="sxs-lookup"><span data-stu-id="63873-133">OVERWRITE VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-134">0 ou 1</span><span class="sxs-lookup"><span data-stu-id="63873-134">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-135">Installation</span><span class="sxs-lookup"><span data-stu-id="63873-135">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-136">Échec de l’installation si le disque dur virtuel existe (0) ou écrasez le disque dur virtuel existant (1).</span><span class="sxs-lookup"><span data-stu-id="63873-136">Fail installation if VHD exists(0) or overwrite existing VHD(1).</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-137">Le remplacement ne se produit pas et l’installation échoue s’il existe déjà un disque dur virtuel (VHD).</span><span class="sxs-lookup"><span data-stu-id="63873-137">Overwrite does not occur and installation fails if a virtual hard disk (VHD) already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63873-138">Espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="63873-138">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-139">SUPPRESSMEDVLAUNCH</span><span class="sxs-lookup"><span data-stu-id="63873-139">SUPPRESSMEDVLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-140">0 ou 1</span><span class="sxs-lookup"><span data-stu-id="63873-140">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-141">Installation</span><span class="sxs-lookup"><span data-stu-id="63873-141">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-142">Démarrez (0) ou ne démarrez pas (1) MED-V après l’installation d’un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="63873-142">Start(0) or do not start(1) MED-V after MED-V workspace is installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-143">Si l’espace de travail MED-V a été installé à l’aide de l’interface utilisateur (UI), une case à cocher sur la <strong> </strong> page terminer détermine s’il convient de démarrer la technologie med-v.</span><span class="sxs-lookup"><span data-stu-id="63873-143">If the MED-V workspace was installed with the user interface (UI), a check box on the <strong>Finish</strong> page controls whether to start MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63873-144">Espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="63873-144">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-145">DELETEDIFFDISKS</span><span class="sxs-lookup"><span data-stu-id="63873-145">DELETEDIFFDISKS</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-146">0 ou 1</span><span class="sxs-lookup"><span data-stu-id="63873-146">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-147">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="63873-147">Uninstallation</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-148">Conserver (0) ou supprimer (1) des VHD créés par MED-V</span><span class="sxs-lookup"><span data-stu-id="63873-148">Keep(0) or delete(1) VHDs created by MED-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="63873-149">Aucun VHD n’est supprimé.</span><span class="sxs-lookup"><span data-stu-id="63873-149">No VHDs are deleted.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="63873-150">Exemples d’arguments de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="63873-150">Examples of Command-Line Arguments</span></span>

<span data-ttu-id="63873-151">L’exemple suivant installe l’espace de travail MED-V créé par le gestionnaire de package de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="63873-151">The following example installs the MED-V workspace created by the MED-V workspace Packager.</span></span> <span data-ttu-id="63873-152">Le fichier d’installation crée un fichier journal dans le répertoire temporaire et exécute le fichier d’installation en mode quiet, mais ne démarre pas l’agent hôte MED-V à l’achèvement.</span><span class="sxs-lookup"><span data-stu-id="63873-152">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode, but does not start the MED-V Host Agent on completion.</span></span> <span data-ttu-id="63873-153">Le fichier d’installation remplace tout VHD laissé par une installation précédente portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="63873-153">The installation file overwrites any VHD left behind by a previous installation that has the same name.</span></span>

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

<span data-ttu-id="63873-154">Dans l’exemple suivant, l’espace de travail MED-V est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="63873-154">The following example uninstalls the MED-V workspace that was previously installed.</span></span> <span data-ttu-id="63873-155">Le fichier d’installation crée un fichier journal dans le répertoire temporaire et exécute le fichier d’installation en mode quiet.</span><span class="sxs-lookup"><span data-stu-id="63873-155">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode.</span></span> <span data-ttu-id="63873-156">Le fichier d’installation supprime les fichiers de disque dur virtuel restants du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="63873-156">The installation file deletes any remaining virtual hard disk files from the file system.</span></span>

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## <span data-ttu-id="63873-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63873-157">Related topics</span></span>


[<span data-ttu-id="63873-158">Déployer les composants MED-V</span><span class="sxs-lookup"><span data-stu-id="63873-158">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

[<span data-ttu-id="63873-159">Informations techniques de référence pour MED-V</span><span class="sxs-lookup"><span data-stu-id="63873-159">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 






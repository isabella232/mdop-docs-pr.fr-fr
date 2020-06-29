---
title: Migration vers App-V5.1 à partir d'une version antérieure
description: Migration vers App-V5.1 à partir d'une version antérieure
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805064"
---
# <span data-ttu-id="eb487-103">Migration vers App-V5.1 à partir d'une version antérieure</span><span class="sxs-lookup"><span data-stu-id="eb487-103">Migrating to App-V 5.1 from a Previous Version</span></span>


<span data-ttu-id="eb487-104">La version 5,1 de Microsoft Application Virtualization (App-V) vous permet de migrer votre infrastructure App-v 4,6 ou App-V 5,0 vers une infrastructure plus flexible, intégrée et plus facile à 5,1 gérer.</span><span class="sxs-lookup"><span data-stu-id="eb487-104">With Microsoft Application Virtualization (App-V) 5.1, you can migrate your existing App-V 4.6 or App-V 5.0 infrastructure to the more flexible, integrated, and easier to manage App-V 5.1 infrastructure.</span></span>
<span data-ttu-id="eb487-105">Toutefois, vous ne pouvez pas effectuer de migration directe de App-V 4. x vers App-V 5,1, vous devez d’abord migrer vers App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="eb487-105">However, you cannot migrate directly from App-V 4.x to App-V 5.1, you must migrate to App-V 5.0 first.</span></span> <span data-ttu-id="eb487-106">Pour plus d’informations sur la migration de App-V 4. x vers App-V 5,0, voir [migration à partir d’une version précédente](migrating-from-a-previous-version-app-v-50.md)</span><span class="sxs-lookup"><span data-stu-id="eb487-106">For more information on migrating from App-V 4.x to App-V 5.0, see [Migrating from a Previous Version](migrating-from-a-previous-version-app-v-50.md)</span></span>  

<span data-ttu-id="eb487-107">**Remarques**  Les packages App-V 5,1 sont exactement les mêmes que les packages App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="eb487-107">**Note** App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="eb487-108">Il n’y a aucune modification du format de package entre les versions et par conséquent, il est inutile de convertir les packages App-V 5,0 en packages App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="eb487-108">There has been no change in the package format between the versions and therefore, there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>

<span data-ttu-id="eb487-109">Pour plus d’informations sur les différences entre App-V 4,6 et App-V 5,1, voir **différences entre les sections App-v 4,6 et App-v 5,0** de l' [application-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="eb487-109">For more information about the differences between App-V 4.6 and App-V 5.1, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="eb487-110">Améliorations apportées au convertisseur App-V 5,1 package</span><span class="sxs-lookup"><span data-stu-id="eb487-110">Improvements to the App-V 5.1 Package Converter</span></span>


<span data-ttu-id="eb487-111">Vous pouvez désormais utiliser le convertisseur de package pour convertir les packages App-V 4,6 qui contiennent des scripts, et les informations de Registre et les scripts des fichiers source. OSD sont désormais inclus dans la sortie du convertisseur de package.</span><span class="sxs-lookup"><span data-stu-id="eb487-111">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="eb487-112">Vous pouvez également utiliser le `–OSDsToIncludeInPackage` paramètre avec l' `ConvertFrom-AppvLegacyPackage` applet de cmdlet pour spécifier les informations de fichiers. OSD qui sont converties et placées dans le nouveau package.</span><span class="sxs-lookup"><span data-stu-id="eb487-112">You can also use the `–OSDsToIncludeInPackage` parameter with the `ConvertFrom-AppvLegacyPackage` cmdlet to specify which .osd files’ information is converted and placed within the new package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="eb487-113">Nouveauté de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="eb487-113">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="eb487-114">Avant l’application-V 5,1</span><span class="sxs-lookup"><span data-stu-id="eb487-114">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb487-115">Les nouveaux fichiers. XML sont créés correspondant aux fichiers. OSD associés à un package. ces fichiers incluent les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="eb487-115">New .xml files are created corresponding to the .osd files associated with a package; these files include the following information:</span></span></p>
<ul>
<li><p><span data-ttu-id="eb487-116">variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="eb487-116">environment variables</span></span></p></li>
<li><p><span data-ttu-id="eb487-117">associés</span><span class="sxs-lookup"><span data-stu-id="eb487-117">shortcuts</span></span></p></li>
<li><p><span data-ttu-id="eb487-118">associations de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="eb487-118">file type associations</span></span></p></li>
<li><p><span data-ttu-id="eb487-119">informations de Registre</span><span class="sxs-lookup"><span data-stu-id="eb487-119">registry information</span></span></p></li>
<li><p><span data-ttu-id="eb487-120">scripts</span><span class="sxs-lookup"><span data-stu-id="eb487-120">scripts</span></span></p></li>
</ul>
<p><span data-ttu-id="eb487-121">Vous pouvez désormais choisir d’ajouter des informations à partir d’un sous-ensemble de fichiers. OSD du répertoire source au package à l’aide du <code>-OSDsToIncludeInPackage</code> paramètre.</span><span class="sxs-lookup"><span data-stu-id="eb487-121">You can now choose to add information from a subset of the .osd files in the source directory to the package using the <code>-OSDsToIncludeInPackage</code> parameter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb487-122">Les informations et scripts du Registre inclus dans les fichiers. OSD associés à un package n’ont pas été inclus dans la sortie du convertisseur de package.</span><span class="sxs-lookup"><span data-stu-id="eb487-122">Registry information and scripts included in .osd files associated with a package were not included in package converter output.</span></span></p>
<p><span data-ttu-id="eb487-123">Le convertisseur de package remplit le nouveau package avec les informations de tous les fichiers. OSD dans le répertoire source.</span><span class="sxs-lookup"><span data-stu-id="eb487-123">The package converter would populate the new package with information from all of the .osd files in the source directory.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="eb487-124">Exemple d’instruction de conversion</span><span class="sxs-lookup"><span data-stu-id="eb487-124">Example conversion statement</span></span>

<span data-ttu-id="eb487-125">Pour mieux comprendre le nouveau processus, consultez l’exemple d' `ConvertFrom-AppvLegacyPackage` instruction de convertisseur de package suivant.</span><span class="sxs-lookup"><span data-stu-id="eb487-125">To understand the new process, review the following example `ConvertFrom-AppvLegacyPackage` package converter statement.</span></span>

**<span data-ttu-id="eb487-126">Si le répertoire source (\\\\OldPkgStore\\ContosoApp) inclut les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="eb487-126">If the source directory (\\\\OldPkgStore\\ContosoApp) includes the following:</span></span>**

-   <span data-ttu-id="eb487-127">ContosoApp. sft</span><span class="sxs-lookup"><span data-stu-id="eb487-127">ContosoApp.sft</span></span>

-   <span data-ttu-id="eb487-128">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="eb487-128">ContosoApp.msi</span></span>

-   <span data-ttu-id="eb487-129">ContosoApp. sprj</span><span class="sxs-lookup"><span data-stu-id="eb487-129">ContosoApp.sprj</span></span>

-   <span data-ttu-id="eb487-130">ContosoApp\_manifest.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-130">ContosoApp\_manifest.xml</span></span>

-   <span data-ttu-id="eb487-131">X. OSD</span><span class="sxs-lookup"><span data-stu-id="eb487-131">X.osd</span></span>

-   <span data-ttu-id="eb487-132">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="eb487-132">Y.osd</span></span>

-   <span data-ttu-id="eb487-133">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="eb487-133">Z.osd</span></span>

**<span data-ttu-id="eb487-134">Et si vous exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="eb487-134">And you run this command:</span></span>**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**<span data-ttu-id="eb487-135">Les informations suivantes sont créées dans le répertoire de destination (\\\\NewPkgStore\\ContosoApp):</span><span class="sxs-lookup"><span data-stu-id="eb487-135">The following is created in the destination directory (\\\\NewPkgStore\\ContosoApp):</span></span>**

-   <span data-ttu-id="eb487-136">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="eb487-136">ContosoApp.appv</span></span>

-   <span data-ttu-id="eb487-137">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="eb487-137">ContosoApp.msi</span></span>

-   <span data-ttu-id="eb487-138">ContosoApp\_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-138">ContosoApp\_DeploymentConfig.xml</span></span>

-   <span data-ttu-id="eb487-139">ContosoApp\_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-139">ContosoApp\_UserConfig.xml</span></span>

-   <span data-ttu-id="eb487-140">X\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-140">X\_Config.xml</span></span>

-   <span data-ttu-id="eb487-141">Y\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-141">Y\_Config.xml</span></span>

-   <span data-ttu-id="eb487-142">Z\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-142">Z\_Config.xml</span></span>

**<span data-ttu-id="eb487-143">Dans l’exemple ci-dessus:</span><span class="sxs-lookup"><span data-stu-id="eb487-143">In the above example:</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="eb487-144">Fichiers de répertoire sources suivants...</span><span class="sxs-lookup"><span data-stu-id="eb487-144">These Source directory files…</span></span></th>
<th align="left"><span data-ttu-id="eb487-145">... sont convertis en fichiers de répertoire de destination...</span><span class="sxs-lookup"><span data-stu-id="eb487-145">…are converted to these Destination directory files…</span></span></th>
<th align="left"><span data-ttu-id="eb487-146">... et contiennent ces éléments.</span><span class="sxs-lookup"><span data-stu-id="eb487-146">…and will contain these items</span></span></th>
<th align="left"><span data-ttu-id="eb487-147">Description</span><span class="sxs-lookup"><span data-stu-id="eb487-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="eb487-148">X. OSD</span><span class="sxs-lookup"><span data-stu-id="eb487-148">X.osd</span></span></p></li>
<li><p><span data-ttu-id="eb487-149">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="eb487-149">Y.osd</span></span></p></li>
<li><p><span data-ttu-id="eb487-150">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="eb487-150">Z.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb487-151">X_Config.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-151">X_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="eb487-152">Y_Config.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-152">Y_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="eb487-153">Z_Config.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-153">Z_Config.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb487-154">Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="eb487-154">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="eb487-155">Associés</span><span class="sxs-lookup"><span data-stu-id="eb487-155">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="eb487-156">Associations de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="eb487-156">File type associations</span></span></p></li>
<li><p><span data-ttu-id="eb487-157">Informations de Registre</span><span class="sxs-lookup"><span data-stu-id="eb487-157">Registry information</span></span></p></li>
<li><p><span data-ttu-id="eb487-158">Scripts</span><span class="sxs-lookup"><span data-stu-id="eb487-158">Scripts</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="eb487-159">Chaque fichier. OSD est converti en un fichier XML distinct correspondant qui contient les éléments répertoriés ici dans le format de configuration de déploiement App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="eb487-159">Each .osd file is converted to a separate, corresponding .xml file that contains the items listed here in App-V 5.1 deployment configuration format.</span></span> <span data-ttu-id="eb487-160">Ces éléments peuvent ensuite être copiés à partir de ces fichiers. xml et placés dans les fichiers de configuration de déploiement ou de configuration utilisateur comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="eb487-160">These items can then be copied from these .xml files and placed in the deployment configuration or user configuration files as desired.</span></span></p>
<p><span data-ttu-id="eb487-161">Dans cet exemple, il existe trois fichiers. xml correspondant aux trois fichiers. OSD dans le répertoire source.</span><span class="sxs-lookup"><span data-stu-id="eb487-161">In this example, there are three .xml files, corresponding with the three .osd files in the source directory.</span></span> <span data-ttu-id="eb487-162">Chaque fichier. xml contient les variables d’environnement, les raccourcis, les associations de types de fichier, les informations de Registre et les scripts dans le fichier. OSD correspondant.</span><span class="sxs-lookup"><span data-stu-id="eb487-162">Each .xml file contains the environment variables, shortcuts, file type associations, registry information, and scripts in its corresponding .osd file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="eb487-163">X. OSD</span><span class="sxs-lookup"><span data-stu-id="eb487-163">X.osd</span></span></p></li>
<li><p><span data-ttu-id="eb487-164">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="eb487-164">Y.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb487-165">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="eb487-165">ContosoApp.appv</span></span></p></li>
<li><p><span data-ttu-id="eb487-166">ContosoApp_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-166">ContosoApp_DeploymentConfig.xml</span></span></p></li>
<li><p><span data-ttu-id="eb487-167">ContosoApp_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="eb487-167">ContosoApp_UserConfig.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="eb487-168">Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="eb487-168">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="eb487-169">Associés</span><span class="sxs-lookup"><span data-stu-id="eb487-169">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="eb487-170">Associations de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="eb487-170">File type associations</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="eb487-171">Les informations des fichiers. OSD spécifiés dans le <code>-OSDsToIncludeInPackage</code> paramètre sont converties et placées à l’intérieur du package.</span><span class="sxs-lookup"><span data-stu-id="eb487-171">The information from the .osd files specified in the <code>-OSDsToIncludeInPackage</code> parameter are converted and placed inside the package.</span></span> <span data-ttu-id="eb487-172">Le convertisseur remplit alors le fichier de configuration du déploiement et le fichier de configuration de l’utilisateur avec le contenu du package, tout comme le Sequencer App-V lors du séquençage d’un nouveau package.</span><span class="sxs-lookup"><span data-stu-id="eb487-172">The converter then populates the deployment configuration file and the user configuration file with the contents of the package, just as App-V Sequencer does when sequencing a new package.</span></span></p>
<p><span data-ttu-id="eb487-173">Dans cet exemple, des variables d’environnement, des raccourcis et des associations de types de fichiers incluses dans X. OSD et Y. OSD ont été converties et placées dans le package App-V et certaines de ces informations sont également incluses dans les fichiers de configuration de déploiement et de configuration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb487-173">In this example, environment variables, shortcuts, and file type associations included in X.osd and Y.osd were converted and placed in the App-V package, and some of this information was also included in the deployment configuration and user configuration files.</span></span> <span data-ttu-id="eb487-174">X. OSD et Y. OSD étaient utilisés, car ils ont été inclus comme arguments pour le <code>-OSDsToIncludeInPackage</code> paramètre.</span><span class="sxs-lookup"><span data-stu-id="eb487-174">X.osd and Y.osd were used because they were included as arguments to the <code>-OSDsToIncludeInPackage</code> parameter.</span></span> <span data-ttu-id="eb487-175">Aucune information de Z. OSD n’est incluse dans le package, car elle n’a pas été incluse dans l’un des arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="eb487-175">No information from Z.osd was included in the package, because it was not included as one of these arguments.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="eb487-176">Conversion de packages créés à l’aide d’une version antérieure d’App-V</span><span class="sxs-lookup"><span data-stu-id="eb487-176">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="eb487-177">Utilisez l’utilitaire convertisseur de package pour mettre à niveau des packages d’application virtuels créés à l’aide de versions de App-V antérieures à App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="eb487-177">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="eb487-178">Le convertisseur de package utilise PowerShell pour convertir des packages et peut faciliter l’automatisation du processus si vous avez de nombreux packages qui nécessitent une conversion.</span><span class="sxs-lookup"><span data-stu-id="eb487-178">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="eb487-179">**Important**  Après avoir converti un package existant, vous devez tester le package avant de déployer le package pour vérifier que le processus de conversion a abouti.</span><span class="sxs-lookup"><span data-stu-id="eb487-179">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="eb487-180">Ce que vous devez savoir avant de convertir des packages existants</span><span class="sxs-lookup"><span data-stu-id="eb487-180">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="eb487-181">Problème</span><span class="sxs-lookup"><span data-stu-id="eb487-181">Issue</span></span></th>
<th align="left"><span data-ttu-id="eb487-182">Solution de contournement</span><span class="sxs-lookup"><span data-stu-id="eb487-182">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb487-183">Les packages virtuels utilisant DSC ne sont pas liés après la conversion.</span><span class="sxs-lookup"><span data-stu-id="eb487-183">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb487-184">Liez les packages à l’aide de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="eb487-184">Link the packages using connection groups.</span></span> <span data-ttu-id="eb487-185">Voir <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> gestion des groupes de connexion </a> .</span><span class="sxs-lookup"><span data-stu-id="eb487-185">See <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb487-186">Des conflits de variables d’environnement sont détectés lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="eb487-186">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb487-187">Résoudre les conflits dans le <strong> fichier. OSD associé </strong> .</span><span class="sxs-lookup"><span data-stu-id="eb487-187">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb487-188">Les chemins d’accès codés en dur sont détectés lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="eb487-188">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb487-189">Les chemins d’accès codés en dur sont difficiles à convertir correctement.</span><span class="sxs-lookup"><span data-stu-id="eb487-189">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="eb487-190">Le convertisseur de package détectera et renverra des packages avec des fichiers contenant des chemins d’accès codés en dur.</span><span class="sxs-lookup"><span data-stu-id="eb487-190">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="eb487-191">Affichez le fichier avec le chemin codé en dur et déterminez s’il nécessite le fichier.</span><span class="sxs-lookup"><span data-stu-id="eb487-191">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="eb487-192">Si tel est le cas, nous vous recommandons de réorganiser le package.</span><span class="sxs-lookup"><span data-stu-id="eb487-192">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="eb487-193">Lors de la conversion d’un package Vérifiez l’absence de raccourcis vers les fichiers ou les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="eb487-193">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="eb487-194">Recherchez l’élément dans le package App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="eb487-194">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="eb487-195">Il peut s’agir d’un chemin d’accès codé en dur.</span><span class="sxs-lookup"><span data-stu-id="eb487-195">It could possibly be a hard-coded path.</span></span> <span data-ttu-id="eb487-196">Convertissez le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="eb487-196">Convert the path.</span></span>

<span data-ttu-id="eb487-197">**Remarques**  Nous vous recommandons d’utiliser le Sequencer App-V 5,1 pour convertir des applications ou applications critiques qui doivent tirer parti de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="eb487-197">**Note** It is recommended that you use the App-V 5.1 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="eb487-198">Pour plus d' [informations sur la façon de séquencer une nouvelle application avec App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md), voir.</span><span class="sxs-lookup"><span data-stu-id="eb487-198">See, [How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span></span>

<span data-ttu-id="eb487-199">Si un package converti ne s’ouvre pas après l’avoir converti, il est également recommandé de réorganiser l’application à l’aide du séquenceur App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="eb487-199">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.1 sequencer.</span></span>

 

[<span data-ttu-id="eb487-200">Comment convertir un package créé dans une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="eb487-200">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## <span data-ttu-id="eb487-201">Migration des clients</span><span class="sxs-lookup"><span data-stu-id="eb487-201">Migrating Clients</span></span>


<span data-ttu-id="eb487-202">Le tableau suivant présente la méthode recommandée pour la mise à niveau des clients.</span><span class="sxs-lookup"><span data-stu-id="eb487-202">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="eb487-203">Tâche</span><span class="sxs-lookup"><span data-stu-id="eb487-203">Task</span></span></th>
<th align="left"><span data-ttu-id="eb487-204">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="eb487-204">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb487-205">Mettez à niveau votre environnement vers la dernière version de l’application-V 4.6</span><span class="sxs-lookup"><span data-stu-id="eb487-205">Upgrade your environment to the latest version of App-V4.6</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="eb487-206">Considérations en matière de déploiement et de mise à niveau de la virtualisation des applications </a> .</span><span class="sxs-lookup"><span data-stu-id="eb487-206">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb487-207">Installez le client App-V 5,1 avec la coexistence activée.</span><span class="sxs-lookup"><span data-stu-id="eb487-207">Install the App-V 5.1 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)"><span data-ttu-id="eb487-208">Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur </a> .</span><span class="sxs-lookup"><span data-stu-id="eb487-208">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb487-209">Séquence et déploiement des packages App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="eb487-209">Sequence and roll out App-V 5.1 packages.</span></span> <span data-ttu-id="eb487-210">Le cas échéant, annulez la publication des packages App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="eb487-210">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)"><span data-ttu-id="eb487-211">Comment séquencer une nouvelle application avec App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="eb487-211">How to Sequence a New Application with App-V 5.1</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="eb487-212">**Important**  Vous devez utiliser la dernière version de App-V 4.6 pour utiliser le mode de coexistence.</span><span class="sxs-lookup"><span data-stu-id="eb487-212">**Important** You must be running the latest version of App-V4.6 to use coexistence mode.</span></span> <span data-ttu-id="eb487-213">Par ailleurs, lorsque vous séquencez un package, vous devez configurer le paramètre administration de l’autorité, qui se trouve dans la **Configuration utilisateur** , dans la section Configuration de l' **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="eb487-213">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="eb487-214">Migration de l’infrastructure complète de l’application-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="eb487-214">Migrating the App-V 5.1 Server Full Infrastructure</span></span>


<span data-ttu-id="eb487-215">Il n’existe aucune méthode directe pour effectuer une mise à niveau vers une infrastructure App-V 5,1 complète.</span><span class="sxs-lookup"><span data-stu-id="eb487-215">There is no direct method to upgrade to a full App-V 5.1 infrastructure.</span></span> <span data-ttu-id="eb487-216">Pour plus d’informations sur la mise à niveau de l’application-V Server, utilisez les informations de la section suivante.</span><span class="sxs-lookup"><span data-stu-id="eb487-216">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="eb487-217">Tâche</span><span class="sxs-lookup"><span data-stu-id="eb487-217">Task</span></span></th>
<th align="left"><span data-ttu-id="eb487-218">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="eb487-218">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb487-219">Mettez à niveau votre environnement vers la dernière version de App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="eb487-219">Upgrade your environment to the latest version of App-V4.6.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="eb487-220">Considérations en matière de déploiement et de mise à niveau de la virtualisation des applications </a> .</span><span class="sxs-lookup"><span data-stu-id="eb487-220">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb487-221">Déploiement de la version 5,1 App-V du client.</span><span class="sxs-lookup"><span data-stu-id="eb487-221">Deploy App-V 5.1 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="eb487-222">Déploiement du client App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="eb487-222">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb487-223">Installez App-V 5,1 Server.</span><span class="sxs-lookup"><span data-stu-id="eb487-223">Install App-V 5.1 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="eb487-224">Déploiement du serveur App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="eb487-224">How to Deploy the App-V 5.1 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb487-225">Migrer des packages existants.</span><span class="sxs-lookup"><span data-stu-id="eb487-225">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb487-226">Voir les <strong> packages de conversion créés à l’aide d’une version antérieure de la section App-V </strong> de cet article.</span><span class="sxs-lookup"><span data-stu-id="eb487-226">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="eb487-227">Tâches de migration supplémentaires</span><span class="sxs-lookup"><span data-stu-id="eb487-227">Additional Migration tasks</span></span>


<span data-ttu-id="eb487-228">Vous pouvez également effectuer d’autres tâches de migration telles que la reconfiguration des points de terminaison et l’ouverture d’un package créé à l’aide d’une version antérieure sur un ordinateur exécutant le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="eb487-228">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.1 client.</span></span> <span data-ttu-id="eb487-229">Les liens suivants fournissent des informations supplémentaires sur l’exécution de ces tâches.</span><span class="sxs-lookup"><span data-stu-id="eb487-229">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="eb487-230">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="eb487-230">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="eb487-231">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="eb487-231">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[<span data-ttu-id="eb487-232">Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="eb487-232">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="eb487-233">Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="eb487-233">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="eb487-234">Autres ressources pour effectuer des tâches de migration d’application-V</span><span class="sxs-lookup"><span data-stu-id="eb487-234">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="eb487-235">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="eb487-235">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="eb487-236">Procédure de mise à niveau du serveur de gestion Microsoft App-V 5,1 simplifiée</span><span class="sxs-lookup"><span data-stu-id="eb487-236">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 






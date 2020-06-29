---
title: Publication d'applications et interaction avec le Client
description: Publication d'applications et interaction avec le Client
author: dansimp
ms.assetid: 36a4bf6f-a917-41a6-9856-6248686df352
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 69fcf119faaf35e53ae36f386bcb3480e2ee3b0e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805947"
---
# <span data-ttu-id="a5a64-103">Publication d'applications et interaction avec le Client</span><span class="sxs-lookup"><span data-stu-id="a5a64-103">Application Publishing and Client Interaction</span></span>


<span data-ttu-id="a5a64-104">Cet article fournit des informations techniques sur les opérations courantes du client d’application V et son intégration au système d’exploitation local.</span><span class="sxs-lookup"><span data-stu-id="a5a64-104">This article provides technical information about common App-V client operations and their integration with the local operating system.</span></span>

-   [<span data-ttu-id="a5a64-105">Fichiers de package App-V créés par le Sequencer</span><span class="sxs-lookup"><span data-stu-id="a5a64-105">App-V package files created by the Sequencer</span></span>](#bkmk-appv-pkg-files-list)

-   [<span data-ttu-id="a5a64-106">Qu’est-ce que le fichier AppV?</span><span class="sxs-lookup"><span data-stu-id="a5a64-106">What’s in the appv file?</span></span>](#bkmk-appv-file-contents)

-   [<span data-ttu-id="a5a64-107">Emplacements de stockage des données du client App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-107">App-V client data storage locations</span></span>](#bkmk-files-data-storage)

-   [<span data-ttu-id="a5a64-108">Registre de package</span><span class="sxs-lookup"><span data-stu-id="a5a64-108">Package registry</span></span>](#bkmk-pkg-registry)

-   [<span data-ttu-id="a5a64-109">Comportement du magasin de packages App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-109">App-V package store behavior</span></span>](#bkmk-pkg-store-behavior)

-   [<span data-ttu-id="a5a64-110">Itinérance et Registre</span><span class="sxs-lookup"><span data-stu-id="a5a64-110">Roaming registry and data</span></span>](#bkmk-roaming-reg-data)

-   [<span data-ttu-id="a5a64-111">Gestion du cycle de vie des applications du client App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-111">App-V client application lifecycle management</span></span>](#bkmk-clt-app-lifecycle)

-   [<span data-ttu-id="a5a64-112">Intégration des packages App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-112">Integration of App-V packages</span></span>](#bkmk-integr-appv-pkgs)

-   [<span data-ttu-id="a5a64-113">Traitement dynamique des configurations</span><span class="sxs-lookup"><span data-stu-id="a5a64-113">Dynamic configuration processing</span></span>](#bkmk-dynamic-config)

-   [<span data-ttu-id="a5a64-114">Assemblys côte à côte</span><span class="sxs-lookup"><span data-stu-id="a5a64-114">Side-by-side assemblies</span></span>](#bkmk-sidebyside-assemblies)

-   [<span data-ttu-id="a5a64-115">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="a5a64-115">Client logging</span></span>](#bkmk-client-logging)

<span data-ttu-id="a5a64-116">Pour obtenir des informations de référence supplémentaires, voir [la page de téléchargement des ressources de documentation de Microsoft Application Virtualization (App-V)](https://www.microsoft.com/download/details.aspx?id=27760).</span><span class="sxs-lookup"><span data-stu-id="a5a64-116">For additional reference information, see [Microsoft Application Virtualization (App-V) Documentation Resources Download Page](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-pkg-files-list"></a><span data-ttu-id="a5a64-117">Fichiers de package App-V créés par le Sequencer</span><span class="sxs-lookup"><span data-stu-id="a5a64-117">App-V package files created by the Sequencer</span></span>


<span data-ttu-id="a5a64-118">Le Sequencer crée des packages App-V et génère une application virtualisée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-118">The Sequencer creates App-V packages and produces a virtualized application.</span></span> <span data-ttu-id="a5a64-119">Le processus de séquençage génère les fichiers suivants:</span><span class="sxs-lookup"><span data-stu-id="a5a64-119">The sequencing process creates the following files:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-120">Fichier</span><span class="sxs-lookup"><span data-stu-id="a5a64-120">File</span></span></th>
<th align="left"><span data-ttu-id="a5a64-121">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-122">. AppV</span><span class="sxs-lookup"><span data-stu-id="a5a64-122">.appv</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-123">Le fichier de package principal, qui contient les ressources capturées et les informations d’État du processus de séquençage.</span><span class="sxs-lookup"><span data-stu-id="a5a64-123">The primary package file, which contains the captured assets and state information from the sequencing process.</span></span></p></li>
<li><p><span data-ttu-id="a5a64-124">Architecture du fichier de package, des informations de publication et du Registre sous la forme d’un jeton qui peut être réappliqué à un ordinateur et à un utilisateur spécifique lors de la remise.</span><span class="sxs-lookup"><span data-stu-id="a5a64-124">Architecture of the package file, publishing information, and registry in a tokenized form that can be reapplied to a machine and to a specific user upon delivery.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-125">. PORTION</span><span class="sxs-lookup"><span data-stu-id="a5a64-125">.MSI</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-126">Wrapper de déploiement exécutable qui vous permet de déployer manuellement des fichiers. AppV ou en utilisant une plate-forme de déploiement tierce.</span><span class="sxs-lookup"><span data-stu-id="a5a64-126">Executable deployment wrapper that you can use to deploy .appv files manually or by using a third-party deployment platform.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-127">_DeploymentConfig.XML</span><span class="sxs-lookup"><span data-stu-id="a5a64-127">_DeploymentConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-128">Fichier utilisé pour personnaliser les paramètres de publication par défaut de toutes les applications d’un package déployé globalement pour tous les utilisateurs sur un ordinateur exécutant le client App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-128">File used to customize the default publishing parameters for all applications in a package that is deployed globally to all users on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-129">_UserConfig.XML</span><span class="sxs-lookup"><span data-stu-id="a5a64-129">_UserConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-130">Fichier utilisé pour personnaliser les paramètres de publication de toutes les applications d’un package déployés pour un utilisateur spécifique sur un ordinateur exécutant le client App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-130">File used to customize the publishing parameters for all applications in a package that is a deployed to a specific user on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-131">Report.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-131">Report.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-132">Résumé des messages issus du processus de séquençage, y compris les pilotes, fichiers et emplacements de Registre omis.</span><span class="sxs-lookup"><span data-stu-id="a5a64-132">Summary of messages resulting from the sequencing process, including omitted drivers, files, and registry locations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-133">. CAB</span><span class="sxs-lookup"><span data-stu-id="a5a64-133">.CAB</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="a5a64-134">Facultatif: </em> fichier d’accélérateur de package utilisé pour générer automatiquement un package d’application virtuelle précédemment séquencé.</span><span class="sxs-lookup"><span data-stu-id="a5a64-134">Optional:</em> Package accelerator file used to automatically rebuild a previously sequenced virtual application package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-135">.appvt</span><span class="sxs-lookup"><span data-stu-id="a5a64-135">.appvt</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="a5a64-136">Facultatif: </em> fichier de modèle de Sequencer permettant de conserver les paramètres de Sequencer fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-136">Optional:</em> Sequencer template file used to retain commonly reused Sequencer settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a5a64-137">Pour plus d’informations sur le séquençage, voir [Guide de séquençage de l’application virtualisation](https://go.microsoft.com/fwlink/?LinkID=269810).</span><span class="sxs-lookup"><span data-stu-id="a5a64-137">For information about sequencing, see [Application Virtualization Sequencing Guide](https://go.microsoft.com/fwlink/?LinkID=269810).</span></span>

## <a href="" id="bkmk-appv-file-contents"></a><span data-ttu-id="a5a64-138">Qu’est-ce que le fichier AppV?</span><span class="sxs-lookup"><span data-stu-id="a5a64-138">What’s in the appv file?</span></span>


<span data-ttu-id="a5a64-139">Le fichier AppV est un conteneur qui stocke les fichiers XML et non XML ensemble dans une seule entité.</span><span class="sxs-lookup"><span data-stu-id="a5a64-139">The appv file is a container that stores XML and non-XML files together in a single entity.</span></span> <span data-ttu-id="a5a64-140">Ce fichier est créé à partir du format AppX, qui est basé sur le standard Open Packaging Conventions (OPC).</span><span class="sxs-lookup"><span data-stu-id="a5a64-140">This file is built from the AppX format, which is based on the Open Packaging Conventions (OPC) standard.</span></span>

<span data-ttu-id="a5a64-141">Pour afficher le contenu du fichier AppV, effectuez une copie du package, puis renommez le fichier copié en extension ZIP.</span><span class="sxs-lookup"><span data-stu-id="a5a64-141">To view the appv file contents, make a copy of the package, and then rename the copied file to a ZIP extension.</span></span>

<span data-ttu-id="a5a64-142">Le fichier AppV contient les dossiers et fichiers suivants qui sont utilisés lors de la création et de la publication d’une application virtuelle:</span><span class="sxs-lookup"><span data-stu-id="a5a64-142">The appv file contains the following folder and files, which are used when creating and publishing a virtual application:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-143">Nom</span><span class="sxs-lookup"><span data-stu-id="a5a64-143">Name</span></span></th>
<th align="left"><span data-ttu-id="a5a64-144">Type</span><span class="sxs-lookup"><span data-stu-id="a5a64-144">Type</span></span></th>
<th align="left"><span data-ttu-id="a5a64-145">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-145">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-146">Racine</span><span class="sxs-lookup"><span data-stu-id="a5a64-146">Root</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-147">Dossier de fichiers</span><span class="sxs-lookup"><span data-stu-id="a5a64-147">File folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-148">Répertoire qui contient le système de fichiers de l’application virtualisée qui est capturée lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="a5a64-148">Directory that contains the file system for the virtualized application that is captured during sequencing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-149">[Content_Types]. Xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-149">[Content_Types].xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-150">Fichier XML</span><span class="sxs-lookup"><span data-stu-id="a5a64-150">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-151">Liste des types de contenu principaux dans le fichier AppV (par exemple, DLL, EXE, BIN).</span><span class="sxs-lookup"><span data-stu-id="a5a64-151">List of the core content types in the appv file (e.g. DLL, EXE, BIN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-152">AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-152">AppxBlockMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-153">Fichier XML</span><span class="sxs-lookup"><span data-stu-id="a5a64-153">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-154">Disposition du fichier AppV, qui utilise des éléments de fichier, de bloc et de BlockMap qui permettent d’organiser et de valider des fichiers dans le package App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-154">Layout of the appv file, which uses File, Block, and BlockMap elements that enable location and validation of files in the App-V package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-155">AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-155">AppxManifest.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-156">Fichier XML</span><span class="sxs-lookup"><span data-stu-id="a5a64-156">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-157">Métadonnées du package qui contient les informations requises pour l’ajout, la publication et le lancement du package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-157">Metadata for the package that contains the required information for adding, publishing, and launching the package.</span></span> <span data-ttu-id="a5a64-158">Inclut des points d’extension (associations et raccourcis de types de fichiers), ainsi que les noms et GUID associés au package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-158">Includes extension points (file type associations and shortcuts) and the names and GUIDs associated with the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-159">FilesystemMetadata.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-159">FilesystemMetadata.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-160">Fichier XML</span><span class="sxs-lookup"><span data-stu-id="a5a64-160">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-161">Liste des fichiers capturés lors du séquençage, y compris les attributs (par exemple, les répertoires, les fichiers, les répertoires opaques, les répertoires vides et les noms longs et courts).</span><span class="sxs-lookup"><span data-stu-id="a5a64-161">List of the files captured during sequencing, including attributes (e.g., directories, files, opaque directories, empty directories,and long and short names).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-162">PackageHistory.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-162">PackageHistory.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-163">Fichier XML</span><span class="sxs-lookup"><span data-stu-id="a5a64-163">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-164">Des informations sur le séquençage de l’ordinateur (version du système d’exploitation, version d’Internet Explorer, version du .NET Framework) et du processus (mise à niveau, version du package).</span><span class="sxs-lookup"><span data-stu-id="a5a64-164">Information about the sequencing computer (operating system version, Internet Explorer version, .Net Framework version) and process (upgrade, package version).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-165">Registry. dat</span><span class="sxs-lookup"><span data-stu-id="a5a64-165">Registry.dat</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-166">Fichier DAT</span><span class="sxs-lookup"><span data-stu-id="a5a64-166">DAT File</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-167">Valeurs et clés de Registre capturées lors du processus de séquençage pour le package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-167">Registry keys and values captured during the sequencing process for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-168">StreamMap.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-168">StreamMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-169">Fichier XML</span><span class="sxs-lookup"><span data-stu-id="a5a64-169">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-170">Liste des fichiers pour le bloc de fonctionnalités principal et de publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-170">List of files for the primary and publishing feature block.</span></span> <span data-ttu-id="a5a64-171">Le bloc de fonctionnalité de publication contient les fichiers ICO et les portions de fichiers requises (EXE et DLL) pour la publication du package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-171">The publishing feature block contains the ICO files and required portions of files (EXE and DLL) for publishing the package.</span></span> <span data-ttu-id="a5a64-172">Lorsqu’il est présent, le bloc de fonctionnalités principal inclut les fichiers qui ont été optimisés pour la diffusion en continu lors du processus de séquençage.</span><span class="sxs-lookup"><span data-stu-id="a5a64-172">When present, the primary feature block includes files that have been optimized for streaming during the sequencing process.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a><span data-ttu-id="a5a64-173">Emplacements de stockage des données du client App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-173">App-V client data storage locations</span></span>


<span data-ttu-id="a5a64-174">Le client App-V effectue des tâches pour s’assurer que les applications virtuelles s’exécutent correctement et fonctionnent comme des applications installées localement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-174">The App-V client performs tasks to ensure that virtual applications run properly and work like locally installed applications.</span></span> <span data-ttu-id="a5a64-175">Le processus d’ouverture et d’exécution des applications virtuelles nécessite le mappage à partir du système de fichiers virtuel et du Registre pour s’assurer que l’application possède les composants requis d’une application traditionnelle attendue par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-175">The process of opening and running virtual applications requires mapping from the virtual file system and registry to ensure the application has the required components of a traditional application expected by users.</span></span> <span data-ttu-id="a5a64-176">Cette section décrit les ressources nécessaires à l’exécution d’applications virtuelles et indique l’emplacement dans lequel App-V stocke les ressources.</span><span class="sxs-lookup"><span data-stu-id="a5a64-176">This section describes the assets that are required to run virtual applications and lists the location where App-V stores the assets.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-177">Nom</span><span class="sxs-lookup"><span data-stu-id="a5a64-177">Name</span></span></th>
<th align="left"><span data-ttu-id="a5a64-178">Emplacement</span><span class="sxs-lookup"><span data-stu-id="a5a64-178">Location</span></span></th>
<th align="left"><span data-ttu-id="a5a64-179">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-179">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-180">Magasin de packages</span><span class="sxs-lookup"><span data-stu-id="a5a64-180">Package Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-181">%ProgramData%\App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-181">%ProgramData%\App-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-182">Emplacement par défaut des fichiers de package en lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5a64-182">Default location for read only package files</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-183">Catalogue d’ordinateurs</span><span class="sxs-lookup"><span data-stu-id="a5a64-183">Machine Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="a5a64-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-185">Contient des documents de configuration par ordinateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-185">Contains per-machine configuration documents</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-186">Catalogue utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-186">User Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-187">%AppData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="a5a64-187">%AppData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-188">Contient des documents de configuration par utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-188">Contains per-user configuration documents</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-189">Sauvegardes de raccourci</span><span class="sxs-lookup"><span data-stu-id="a5a64-189">Shortcut Backups</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span><span class="sxs-lookup"><span data-stu-id="a5a64-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-191">Stocke les points d’intégration précédents qui permettent la restauration sur l’annulation de la publication d’un package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-191">Stores previous integration points that enable restore on package unpublish</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-192">Itinérance dans l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="a5a64-192">Copy on Write (COW) Roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-193">%AppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="a5a64-193">%AppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-194">Emplacement d’itinérance inscriptible pour la modification d’un package</span><span class="sxs-lookup"><span data-stu-id="a5a64-194">Writeable roaming location for package modification</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-195">Copie lors de l’écriture (vache) locale</span><span class="sxs-lookup"><span data-stu-id="a5a64-195">Copy on Write (COW) Local</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="a5a64-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-197">Emplacement sans itinérance pour la modification d’un package</span><span class="sxs-lookup"><span data-stu-id="a5a64-197">Writeable non-roaming location for package modification</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-198">Registre de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-198">Machine Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-199">HKLM\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="a5a64-199">HKLM\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-200">Contient des informations sur l’état du package, notamment les packages de VReg pour ordinateur ou les packages publiés globalement (ruche de l’ordinateur)</span><span class="sxs-lookup"><span data-stu-id="a5a64-200">Contains package state information, including VReg for machine or globally published packages (Machine hive)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-201">Registre de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-201">User Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-202">HKCU\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="a5a64-202">HKCU\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-203">Contient des informations sur l’état du package utilisateur, notamment VReg</span><span class="sxs-lookup"><span data-stu-id="a5a64-203">Contains user package state information including VReg</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-204">Classes Registry d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-204">User Registry Classes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-205">HKCU\Software\Classes\AppV</span><span class="sxs-lookup"><span data-stu-id="a5a64-205">HKCU\Software\Classes\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-206">Contient des informations supplémentaires sur l’état du package utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-206">Contains additional user package state information</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a5a64-207">Des informations supplémentaires sur le tableau sont fournies dans la section ci-dessous et dans l’ensemble du document.</span><span class="sxs-lookup"><span data-stu-id="a5a64-207">Additional details for the table are provided in the section below and throughout the document.</span></span>

### <span data-ttu-id="a5a64-208">Magasin de packages</span><span class="sxs-lookup"><span data-stu-id="a5a64-208">Package store</span></span>

<span data-ttu-id="a5a64-209">Le client App-V gère les ressources d’applications chargées dans le magasin de packages.</span><span class="sxs-lookup"><span data-stu-id="a5a64-209">The App-V Client manages the applications assets mounted in the package store.</span></span> <span data-ttu-id="a5a64-210">Cet emplacement de stockage par défaut est `%ProgramData%\App-V` , mais vous pouvez le configurer pendant ou après l’installation à l’aide de la `Set-AppVClientConfiguration` commande PowerShell qui modifie le registre local ( `PackageInstallationRoot` valeur située sous la `HKLM\Software\Microsoft\AppV\Client\Streaming` clé).</span><span class="sxs-lookup"><span data-stu-id="a5a64-210">This default storage location is `%ProgramData%\App-V`, but you can configure it during or after setup by using the `Set-AppVClientConfiguration` PowerShell command, which modifies the local registry (`PackageInstallationRoot` value under the `HKLM\Software\Microsoft\AppV\Client\Streaming` key).</span></span> <span data-ttu-id="a5a64-211">Le magasin de packages doit être localisé sur un chemin local du système d’exploitation du client.</span><span class="sxs-lookup"><span data-stu-id="a5a64-211">The package store must be located at a local path on the client operating system.</span></span> <span data-ttu-id="a5a64-212">Les packages individuels sont stockés dans le magasin de packages dans les sous-répertoires nommés pour le GUID et le GUID de la version du package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-212">The individual packages are stored in the package store in subdirectories named for the Package GUID and Version GUID.</span></span>

<span data-ttu-id="a5a64-213">Exemple de chemin d’accès à une application spécifique:</span><span class="sxs-lookup"><span data-stu-id="a5a64-213">Example of a path to a specific application:</span></span>

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

<span data-ttu-id="a5a64-214">Pour modifier l’emplacement par défaut du magasin de packages lors de l’installation, voir [comment déployer le client App-V](how-to-deploy-the-app-v-client-51gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="a5a64-214">To change the default location of the package store during setup, see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md).</span></span>

### <span data-ttu-id="a5a64-215">Magasin de contenus partagés</span><span class="sxs-lookup"><span data-stu-id="a5a64-215">Shared Content Store</span></span>

<span data-ttu-id="a5a64-216">Si le client App-V est configuré en mode de magasin de contenus partagés, il est impossible d’écrire des données sur le disque quand une erreur de flux se produit, ce qui signifie que les packages nécessitent au moins un espace libre sur le disque local (publications de données).</span><span class="sxs-lookup"><span data-stu-id="a5a64-216">If the App-V Client is configured in Shared Content Store mode, no data is written to disk when a stream fault occurs, which means that the packages require minimal local disk space (publishing data).</span></span> <span data-ttu-id="a5a64-217">L’utilisation de moins d’espace disque est particulièrement utile dans les environnements VDI, où le stockage local peut être limité et la diffusion en continu des applications à partir d’un emplacement réseau haute performance (par exemple, un SAN) est préférable.</span><span class="sxs-lookup"><span data-stu-id="a5a64-217">The use of less disk space is highly desirable in VDI environments, where local storage can be limited, and streaming the applications from a high performance network location (such as a SAN) is preferable.</span></span> <span data-ttu-id="a5a64-218">Pour plus d’informations sur le mode magasin de contenu partagé, voir <https://go.microsoft.com/fwlink/p/?LinkId=392750> .</span><span class="sxs-lookup"><span data-stu-id="a5a64-218">For more information on shared content store mode, see <https://go.microsoft.com/fwlink/p/?LinkId=392750>.</span></span>

<span data-ttu-id="a5a64-219">**Remarques**  Le magasin d’ordinateurs et de packages doit résider sur un disque local, même si vous utilisez des configurations de magasin de contenu partagé pour le client App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-219">**Note** The machine and package store must be located on a local drive, even when you’re using Shared Content Store configurations for the App-V Client.</span></span>

 

### <span data-ttu-id="a5a64-220">Catalogues de package</span><span class="sxs-lookup"><span data-stu-id="a5a64-220">Package catalogs</span></span>

<span data-ttu-id="a5a64-221">Le client App-V gère les deux emplacements suivants sur les fichiers:</span><span class="sxs-lookup"><span data-stu-id="a5a64-221">The App-V Client manages the following two file-based locations:</span></span>

-   **<span data-ttu-id="a5a64-222">Catalogues (utilisateur et ordinateur).</span><span class="sxs-lookup"><span data-stu-id="a5a64-222">Catalogs (user and machine).</span></span>**

-   <span data-ttu-id="a5a64-223">**Emplacements du Registre** : dépend de la manière dont le package est destiné à la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-223">**Registry locations** - depends on how the package is targeted for publishing.</span></span> <span data-ttu-id="a5a64-224">Il existe un catalogue (magasin de données) pour l’ordinateur ainsi qu’un catalogue pour chaque utilisateur individuel.</span><span class="sxs-lookup"><span data-stu-id="a5a64-224">There is a Catalog (data store) for the computer, and a catalog for each individual user.</span></span> <span data-ttu-id="a5a64-225">Le catalogue d’ordinateurs stocke les informations globales applicables à tous les utilisateurs ou à tout utilisateur, et le catalogue de l’utilisateur stocke les informations applicables à un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="a5a64-225">The Machine Catalog stores global information applicable to all users or any user, and the User Catalog stores information applicable to a specific user.</span></span> <span data-ttu-id="a5a64-226">Le catalogue est une collection de configurations dynamiques et de fichiers manifeste; Il existe des données discrètes pour le fichier et le registre par version de package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-226">The Catalog is a collection of Dynamic Configurations and manifest files; there is discrete data for both file and registry per package version.</span></span> 

### <span data-ttu-id="a5a64-227">Catalogue d’ordinateurs</span><span class="sxs-lookup"><span data-stu-id="a5a64-227">Machine catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-228">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-228">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-229">Stocke les documents de package disponibles pour les utilisateurs sur l’ordinateur, lors de l’ajout et de la publication de packages.</span><span class="sxs-lookup"><span data-stu-id="a5a64-229">Stores package documents that are available to users on the machine, when packages are added and published.</span></span> <span data-ttu-id="a5a64-230">Toutefois, si un package est «global» au moment de la publication, les intégrations sont disponibles pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-230">However, if a package is “global” at publishing time, the integrations are available to all users.</span></span></p>
<p><span data-ttu-id="a5a64-231">Si un package n’est pas global, les intégrations sont uniquement publiées pour des utilisateurs spécifiques, mais il existe toujours des ressources globales qui sont modifiées et visibles par tout le monde sur l’ordinateur client (par exemple, le répertoire du package se trouve dans un emplacement sur le disque partagé).</span><span class="sxs-lookup"><span data-stu-id="a5a64-231">If a package is non-global, the integrations are published only for specific users, but there are still global resources that are modified and visible to anyone on the client computer (e.g., the package directory is in a shared disk location).</span></span></p>
<p><span data-ttu-id="a5a64-232">Si un package est disponible pour un utilisateur de l’ordinateur (global ou non-global), le manifeste est stocké dans le catalogue d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-232">If a package is available to a user on the computer (global or non-global), the manifest is stored in the Machine Catalog.</span></span> <span data-ttu-id="a5a64-233">Lorsqu’un package est publié globalement, il existe un fichier de configuration dynamique, qui est stocké dans le catalogue de l’ordinateur; par conséquent, la détermination de la présence d’un package global est définie en fonction de la présence d’un fichier de stratégie (fichier UserDeploymentConfiguration) dans le catalogue d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-233">When a package is published globally, there is a Dynamic Configuration file, stored in the Machine Catalog; therefore, the determination of whether a package is global is defined according to whether there is a policy file (UserDeploymentConfiguration file) in the Machine Catalog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-234">Emplacement de stockage par défaut</span><span class="sxs-lookup"><span data-stu-id="a5a64-234">Default storage location</span></span></p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p><span data-ttu-id="a5a64-235">Cet emplacement n’est pas identique à l’emplacement de stockage du package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-235">This location is not the same as the Package Store location.</span></span> <span data-ttu-id="a5a64-236">Le Windows Store est la copie du fichier de package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-236">The Package Store is the golden or pristine copy of the package files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-237">Fichiers dans le catalogue d’ordinateurs</span><span class="sxs-lookup"><span data-stu-id="a5a64-237">Files in the machine catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-238">Manifest.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-238">Manifest.xml</span></span></p></li>
<li><p><span data-ttu-id="a5a64-239">DeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-239">DeploymentConfiguration.xml</span></span></p></li>
<li><p><span data-ttu-id="a5a64-240">UserManifest.xml (package publié globalement)</span><span class="sxs-lookup"><span data-stu-id="a5a64-240">UserManifest.xml (Globally Published Package)</span></span></p></li>
<li><p><span data-ttu-id="a5a64-241">UserDeploymentConfiguration.xml (package publié globalement)</span><span class="sxs-lookup"><span data-stu-id="a5a64-241">UserDeploymentConfiguration.xml (Globally Published Package)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-242">Emplacement supplémentaire du catalogue d’ordinateurs, utilisé lorsque le package fait partie d’un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="a5a64-242">Additional machine catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-243">L’emplacement suivant est en plus de l’emplacement de package spécifique mentionné ci-dessus:</span><span class="sxs-lookup"><span data-stu-id="a5a64-243">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-244">Fichiers supplémentaires dans le catalogue d’ordinateurs lorsque le package fait partie d’un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="a5a64-244">Additional files in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-245">PackageGroupDescriptor.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-245">PackageGroupDescriptor.xml</span></span></p></li>
<li><p><span data-ttu-id="a5a64-246">UserPackageGroupDescriptor.xml (groupe de connexions à publication globale)</span><span class="sxs-lookup"><span data-stu-id="a5a64-246">UserPackageGroupDescriptor.xml (globally published Connection Group)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a5a64-247">Catalogue utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-247">User catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-248">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-248">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-249">Créé lors du processus de publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-249">Created during the publishing process.</span></span> <span data-ttu-id="a5a64-250">Contient des informations permettant de publier le package, ainsi que de l’utiliser au démarrage pour vérifier qu’un package est configuré pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="a5a64-250">Contains information used for publishing the package, and also used at launch to ensure that a package is provisioned to a specific user.</span></span> <span data-ttu-id="a5a64-251">Créé à un emplacement itinérant et inclut des informations de publication spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-251">Created in a roaming location and includes user-specific publishing information.</span></span></p>
<p><span data-ttu-id="a5a64-252">Lors de la publication d’un package pour un utilisateur, celui-ci est stocké dans le catalogue utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-252">When a package is published for a user, the policy file is stored in the User Catalog.</span></span> <span data-ttu-id="a5a64-253">En même temps, une copie du manifeste est également stockée dans le catalogue utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-253">At the same time, a copy of the manifest is also stored in the User Catalog.</span></span> <span data-ttu-id="a5a64-254">Lorsqu’un utilisateur est supprimé, les fichiers de package pertinents sont supprimés du catalogue de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-254">When a package entitlement is removed for a user, the relevant package files are removed from the User Catalog.</span></span> <span data-ttu-id="a5a64-255">En examinant le catalogue de l’utilisateur, un administrateur peut voir la présence d’un fichier de configuration dynamique, qui indique que le package est habilité pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-255">Looking at the user catalog, an administrator can view the presence of a Dynamic Configuration file, which indicates that the package is entitled for that user.</span></span></p>
<p><span data-ttu-id="a5a64-256">Pour les utilisateurs itinérants, le catalogue utilisateur doit se trouver dans un emplacement itinérant ou partagé pour conserver par défaut le comportement d’application-V hérité du ciblage des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-256">For roaming users, the User Catalog needs to be in a roaming or shared location to preserve the legacy App-V behavior of targeting users by default.</span></span> <span data-ttu-id="a5a64-257">Le droit d’utilisation et la politique sont liés à un utilisateur, et non à un ordinateur, afin qu’il ne soit pas itinérant auprès de l’utilisateur une fois qu’il est approvisionné.</span><span class="sxs-lookup"><span data-stu-id="a5a64-257">Entitlement and policy are tied to a user, not a computer, so they should roam with the user once they are provisioned.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-258">Emplacement de stockage par défaut</span><span class="sxs-lookup"><span data-stu-id="a5a64-258">Default storage location</span></span></p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-259">Fichiers dans le catalogue utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-259">Files in the user catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-260">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-260">UserManifest.xml</span></span></p></li>
<li><p><span data-ttu-id="a5a64-261">DynamicConfiguration.xml ou UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-261">DynamicConfiguration.xml or UserDeploymentConfiguration.xml</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-262">Emplacement supplémentaire du catalogue utilisateur, utilisé lorsque le package fait partie d’un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="a5a64-262">Additional user catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-263">L’emplacement suivant est en plus de l’emplacement de package spécifique mentionné ci-dessus:</span><span class="sxs-lookup"><span data-stu-id="a5a64-263">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-264">Fichier supplémentaire dans le catalogue d’ordinateurs lorsque le package fait partie d’un groupe de connexions</span><span class="sxs-lookup"><span data-stu-id="a5a64-264">Additional file in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a5a64-265">Sauvegardes de raccourci</span><span class="sxs-lookup"><span data-stu-id="a5a64-265">Shortcut backups</span></span>

<span data-ttu-id="a5a64-266">Pendant le processus de publication, le client App-V restaure les raccourcis et les points d’intégration de `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` cette sauvegarde pour la restauration de ces points d’intégration aux versions précédentes lorsque le package n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="a5a64-266">During the publishing process, the App-V Client backs up any shortcuts and integration points to `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` This backup enables the restoration of these integration points to the previous versions when the package is unpublished.</span></span>

### <span data-ttu-id="a5a64-267">Copier sur un fichier d’écriture</span><span class="sxs-lookup"><span data-stu-id="a5a64-267">Copy on Write files</span></span>

<span data-ttu-id="a5a64-268">Le magasin de packages contient une copie de fichiers de package qui ont été diffusés en continu à partir du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-268">The Package Store contains a pristine copy of the package files that have been streamed from the publishing server.</span></span> <span data-ttu-id="a5a64-269">Pendant le fonctionnement normal d’une application application V, l’utilisateur ou le service doit éventuellement modifier les fichiers.</span><span class="sxs-lookup"><span data-stu-id="a5a64-269">During normal operation of an App-V application, the user or service may require changes to the files.</span></span> <span data-ttu-id="a5a64-270">Ces modifications ne sont pas apportées dans le magasin de packages afin de préserver la possibilité de réparer l’application, ce qui a pour but de supprimer ces modifications.</span><span class="sxs-lookup"><span data-stu-id="a5a64-270">These changes are not made in the package store in order to preserve your ability to repair the application, which removes these changes.</span></span> <span data-ttu-id="a5a64-271">Ces emplacements, appelés copies lors de l’écriture (vache), prennent en charge les emplacements itinérants et non itinérants.</span><span class="sxs-lookup"><span data-stu-id="a5a64-271">These locations, called Copy on Write (COW), support both roaming and non-roaming locations.</span></span> <span data-ttu-id="a5a64-272">L’emplacement où les modifications sont stockées dépend de l’application programmée pour écrire les modifications apportées à une expérimentation native.</span><span class="sxs-lookup"><span data-stu-id="a5a64-272">The location where the modifications are stored depends where the application has been programmed to write changes to in a native experience.</span></span>

### <span data-ttu-id="a5a64-273">Itinérance COW</span><span class="sxs-lookup"><span data-stu-id="a5a64-273">COW roaming</span></span>

<span data-ttu-id="a5a64-274">L’emplacement d’itinérance COW décrit ci-dessus enregistre les modifications apportées aux fichiers et répertoires ciblant l’emplacement par défaut de% AppData% ou l’emplacement \\Users\\{username}\\AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="a5a64-274">The COW Roaming location described above stores changes to files and directories that are targeted to the typical %AppData% location or \\Users\\{username}\\AppData\\Roaming location.</span></span> <span data-ttu-id="a5a64-275">Ces fichiers et répertoires sont alors en itinérance en fonction des paramètres du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-275">These directories and files are then roamed based on the operating system settings.</span></span>

### <span data-ttu-id="a5a64-276">VACHES locales</span><span class="sxs-lookup"><span data-stu-id="a5a64-276">COW local</span></span>

<span data-ttu-id="a5a64-277">L’emplacement local de vache est semblable à l’emplacement d’itinérance, mais les répertoires et fichiers ne sont pas itinérants vers d’autres ordinateurs, même si la prise en charge de l’itinérance a été configurée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-277">The COW Local location is similar to the roaming location, but the directories and files are not roamed to other computers, even if roaming support has been configured.</span></span> <span data-ttu-id="a5a64-278">Dans l’emplacement local de vache décrit ci-dessus, les modifications sont apportées aux fenêtres standard et non à l’emplacement% AppData%.</span><span class="sxs-lookup"><span data-stu-id="a5a64-278">The COW Local location described above stores changes applicable to typical windows and not the %AppData% location.</span></span> <span data-ttu-id="a5a64-279">Les répertoires indiqués varient en fonction du type d’emplacement Windows (par exemple, AppData et Common AppDataS).</span><span class="sxs-lookup"><span data-stu-id="a5a64-279">The directories listed will vary but there will be two locations for any typical Windows locations (e.g. Common AppData and Common AppDataS).</span></span> <span data-ttu-id="a5a64-280">Le **S** indique l’emplacement restreint lorsque le service virtuel demande la modification en tant qu’utilisateur à élévation de privilèges différent des utilisateurs connectés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-280">The **S** signifies the restricted location when the virtual service requests the change as a different elevated user from the logged on users.</span></span> <span data-ttu-id="a5a64-281">L’emplacement non-**S** enregistre les modifications apportées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-281">The non-**S** location stores user based changes.</span></span>

## <a href="" id="bkmk-pkg-registry"></a><span data-ttu-id="a5a64-282">Registre de package</span><span class="sxs-lookup"><span data-stu-id="a5a64-282">Package registry</span></span>


<span data-ttu-id="a5a64-283">Pour qu’une application puisse accéder aux données du Registre du package, le client App-V doit rendre les données du Registre du package accessibles aux applications.</span><span class="sxs-lookup"><span data-stu-id="a5a64-283">Before an application can access the package registry data, the App-V Client must make the package registry data available to the applications.</span></span> <span data-ttu-id="a5a64-284">Le client App-V utilise le registre réel comme magasin de stockage pour toutes les données du Registre.</span><span class="sxs-lookup"><span data-stu-id="a5a64-284">The App-V Client uses the real registry as a backing store for all registry data.</span></span>

<span data-ttu-id="a5a64-285">Lors de l’ajout d’un nouveau package au client App-V, une copie du Registre. Un fichier DAT du package est créé à `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` .</span><span class="sxs-lookup"><span data-stu-id="a5a64-285">When a new package is added to the App-V Client, a copy of the REGISTRY.DAT file from the package is created at `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat`.</span></span> <span data-ttu-id="a5a64-286">Le nom du fichier est le GUID de la version avec l’extension. Extension DAT.</span><span class="sxs-lookup"><span data-stu-id="a5a64-286">The name of the file is the version GUID with the .DAT extension.</span></span> <span data-ttu-id="a5a64-287">La raison pour laquelle il s’agit d’une copie est de s’assurer que le fichier de la ruche réel du package n’est jamais utilisé, ce qui empêche la suppression du package ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-287">The reason this copy is made is to ensure that the actual hive file in the package is never in use, which would prevent the removal of the package at a later time.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a5a64-288">Registry. dat du package Store</span><span class="sxs-lookup"><span data-stu-id="a5a64-288">Registry.dat from Package Store</span></span></strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a5a64-289">%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</span><span class="sxs-lookup"><span data-stu-id="a5a64-289">%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a5a64-290">Lorsque la première application du package est lancée sur le client, le client exécute ou copie le contenu du fichier ruche, en recréant les données du Registre du package à un autre emplacement `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` .</span><span class="sxs-lookup"><span data-stu-id="a5a64-290">When the first application from the package is launched on the client, the client stages or copies the contents out of the hive file, re-creating the package registry data in an alternate location `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY`.</span></span> <span data-ttu-id="a5a64-291">Les données de Registre intermédiaire sont dotées de deux types de données d’ordinateur et de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-291">The staged registry data has two distinct types of machine data and user data.</span></span> <span data-ttu-id="a5a64-292">Les données d’ordinateur sont partagées par tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-292">Machine data is shared across all users on the machine.</span></span> <span data-ttu-id="a5a64-293">Les données utilisateur sont transférées par utilisateur vers un emplacement userspecific `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` .</span><span class="sxs-lookup"><span data-stu-id="a5a64-293">User data is staged for each user to a userspecific location `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User`.</span></span> <span data-ttu-id="a5a64-294">Les données de l’ordinateur sont en définitive supprimées lors de la suppression du package, et les données utilisateur sont supprimées lors d’une opération de suppression de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-294">The machine data is ultimately removed at package removal time, and the user data is removed on a user unpublish operation.</span></span>

### <span data-ttu-id="a5a64-295">Échelonnement du Registre du package et de la mise en place du Registre du groupe de connexions</span><span class="sxs-lookup"><span data-stu-id="a5a64-295">Package registry staging vs. connection group registry staging</span></span>

<span data-ttu-id="a5a64-296">Lorsque des groupes de connexion sont présents, le processus précédent de staging du registre a la valeur true, mais au lieu d’avoir un fichier Hive à traiter, il en existe plusieurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-296">When connection groups are present, the previous process of staging the registry holds true, but instead of having one hive file to process, there are more than one.</span></span> <span data-ttu-id="a5a64-297">Les fichiers sont traités dans l’ordre dans lequel ils s’affichent dans le fichier XML du groupe de connexion, avec le premier scripteur qui gagne des conflits.</span><span class="sxs-lookup"><span data-stu-id="a5a64-297">The files are processed in the order in which they appear in the connection group XML, with the first writer winning any conflicts.</span></span>

<span data-ttu-id="a5a64-298">Le registre intermédiaire persiste de la même manière que dans le cas du package unique.</span><span class="sxs-lookup"><span data-stu-id="a5a64-298">The staged registry persists the same way as in the single package case.</span></span> <span data-ttu-id="a5a64-299">Les données de registre de l’utilisateur intermédiaire restent pour le groupe de connexion tant qu’il n’est pas désactivé; les données de registre de l’ordinateur intermédiaire sont supprimées lors de la suppression du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="a5a64-299">Staged user registry data remains for the connection group until it is disabled; staged machine registry data is removed on connection group removal.</span></span>

### <span data-ttu-id="a5a64-300">Registre virtuel</span><span class="sxs-lookup"><span data-stu-id="a5a64-300">Virtual registry</span></span>

<span data-ttu-id="a5a64-301">L’objectif du Registre virtuel (VREG) consiste à fournir une seule vue fusionnée du Registre du package et du Registre natif aux applications.</span><span class="sxs-lookup"><span data-stu-id="a5a64-301">The purpose of the virtual registry (VREG) is to provide a single merged view of the package registry and the native registry to applications.</span></span> <span data-ttu-id="a5a64-302">Il fournit également une fonctionnalité de copie à l’écriture (vache), qui est une modification apportée au registre à partir du contexte de processus virtuel.</span><span class="sxs-lookup"><span data-stu-id="a5a64-302">It also provides copy-on-write (COW) functionality – that is any changes made to the registry from the context of a virtual process are made to a separate COW location.</span></span> <span data-ttu-id="a5a64-303">Cela signifie que le VREG doit combiner trois emplacements du Registre distincts en une seule vue en fonction des emplacements remplis dans le registre COW- &gt; package- &gt; natif.</span><span class="sxs-lookup"><span data-stu-id="a5a64-303">This means that the VREG must combine up to three separate registry locations into a single view based on the populated locations in the registry COW -&gt; package -&gt; native.</span></span> <span data-ttu-id="a5a64-304">Lorsqu’une demande de données de Registre est formulée, elle se trouve dans l’ordre jusqu’à ce qu’elle trouve les données demandées.</span><span class="sxs-lookup"><span data-stu-id="a5a64-304">When a request is made for a registry data it will locate in order until it finds the data it was requesting.</span></span> <span data-ttu-id="a5a64-305">C’est la raison pour laquelle il n’y a pas de valeur stockée à d’autres emplacements; Toutefois, s’il n’y a pas de données dans l’emplacement de la vache, il passe au package, puis à l’emplacement natif jusqu’à ce qu’il trouve les données appropriées.</span><span class="sxs-lookup"><span data-stu-id="a5a64-305">Meaning if there is a value stored in a COW location it will not proceed to other locations, however, if there is no data in the COW location it will proceed to the Package and then Native location until it finds the appropriate data.</span></span>

### <span data-ttu-id="a5a64-306">Emplacements du Registre</span><span class="sxs-lookup"><span data-stu-id="a5a64-306">Registry locations</span></span>

<span data-ttu-id="a5a64-307">Il existe deux emplacements de registre de package et deux emplacements de groupe de connexion dans lesquels le client App-V stocke les informations de Registre, selon que le package est publié individuellement ou en tant que membre d’un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="a5a64-307">There are two package registry locations and two connection group locations where the App-V Client stores registry information, depending on whether the Package is published individually or as part of a connection group.</span></span> <span data-ttu-id="a5a64-308">Il existe trois emplacements de vache pour les packages et trois pour les groupes de connexion, qui sont créés et gérés par le VREG.</span><span class="sxs-lookup"><span data-stu-id="a5a64-308">There are three COW locations for packages and three for connection groups, which are created and managed by the VREG.</span></span> <span data-ttu-id="a5a64-309">Les paramètres des packages et des groupes de connexion ne sont pas partagés:</span><span class="sxs-lookup"><span data-stu-id="a5a64-309">Settings for packages and connection groups are not shared:</span></span>

**<span data-ttu-id="a5a64-310">Package VReg:</span><span class="sxs-lookup"><span data-stu-id="a5a64-310">Single Package VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a5a64-311">Emplacement</span><span class="sxs-lookup"><span data-stu-id="a5a64-311">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a5a64-312">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-312">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a5a64-313">VACHE</span><span class="sxs-lookup"><span data-stu-id="a5a64-313">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (seul le processus d’élévation peut écrire)</span><span class="sxs-lookup"><span data-stu-id="a5a64-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (Only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="a5a64-315">Utilisateur Registry\Client\Packages\PkgGUID\REGISTRY (utilisateur itinérance d’éléments écrits sous HKCU sauf Software\Classes</span><span class="sxs-lookup"><span data-stu-id="a5a64-315">User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="a5a64-316">Classes\Client\Packages\PkgGUID\REGISTRY du registre des utilisateurs (HKCU\Software\Classes écrit et HKLM pour les processus non élevés)</span><span class="sxs-lookup"><span data-stu-id="a5a64-316">User Registry Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a5a64-317">Package</span><span class="sxs-lookup"><span data-stu-id="a5a64-317">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span><span class="sxs-lookup"><span data-stu-id="a5a64-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span></span></p></li>
<li><p><span data-ttu-id="a5a64-319">Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry Registre des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a5a64-319">User Registry Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a5a64-320">En</span><span class="sxs-lookup"><span data-stu-id="a5a64-320">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-321">Emplacement du registre d’application natif</span><span class="sxs-lookup"><span data-stu-id="a5a64-321">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**<span data-ttu-id="a5a64-322">Groupe de connexion VReg:</span><span class="sxs-lookup"><span data-stu-id="a5a64-322">Connection Group VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a5a64-323">Emplacement</span><span class="sxs-lookup"><span data-stu-id="a5a64-323">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a5a64-324">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-324">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a5a64-325">VACHE</span><span class="sxs-lookup"><span data-stu-id="a5a64-325">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (seul le processus d’élévation peut écrire)</span><span class="sxs-lookup"><span data-stu-id="a5a64-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="a5a64-327">Registry\Client\PackageGroups\GrpGUID\REGISTRY utilisateur (ce que vous avez écrit dans HKCU sauf Software\Classes</span><span class="sxs-lookup"><span data-stu-id="a5a64-327">User Registry\Client\PackageGroups\GrpGUID\REGISTRY (Anything written to HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="a5a64-328">Classes\Client\PackageGroups\GrpGUID\REGISTRY Registre des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a5a64-328">User Registry Classes\Client\PackageGroups\GrpGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a5a64-329">Package</span><span class="sxs-lookup"><span data-stu-id="a5a64-329">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="a5a64-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
<li><p><span data-ttu-id="a5a64-331">Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY Registre des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a5a64-331">User Registry Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a5a64-332">En</span><span class="sxs-lookup"><span data-stu-id="a5a64-332">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a5a64-333">Emplacement du registre d’application natif</span><span class="sxs-lookup"><span data-stu-id="a5a64-333">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="a5a64-334">Il existe deux emplacements de vache pour HKLM. processus élevés et non élevés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-334">There are two COW locations for HKLM; elevated and non-elevated processes.</span></span> <span data-ttu-id="a5a64-335">Les processus élevés écrivent toujours les modifications HKLM de Secure COW dans HKLM.</span><span class="sxs-lookup"><span data-stu-id="a5a64-335">Elevated processes always write HKLM changes to the secure COW under HKLM.</span></span> <span data-ttu-id="a5a64-336">Les processus non contrôlés par élévation écrivent toujours des modifications HKLM de la vache non sécurisée sous HKCU\\Software\\Classes.</span><span class="sxs-lookup"><span data-stu-id="a5a64-336">Non-elevated processes always write HKLM changes to the non-secure COW under HKCU\\Software\\Classes.</span></span> <span data-ttu-id="a5a64-337">Lorsqu’une application lit les modifications apportées par HKLM, les processus élevés lisent les modifications de la COW sécurisée sous HKLM.</span><span class="sxs-lookup"><span data-stu-id="a5a64-337">When an application reads changes from HKLM, elevated processes will read changes from the secure COW under HKLM.</span></span> <span data-ttu-id="a5a64-338">Les lectures non élévations à la fois, en favorisant les changements apportés à la vache non sécurisée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-338">Non-elevated reads from both, favoring the changes made in the unsecure COW first.</span></span>

### <span data-ttu-id="a5a64-339">Touches directes</span><span class="sxs-lookup"><span data-stu-id="a5a64-339">Pass-through keys</span></span>

<span data-ttu-id="a5a64-340">Les clés directes permettent à un administrateur de configurer certaines touches afin qu’elles puissent être lues uniquement à partir du Registre natif, en ignorant les emplacements des packages et des vaches.</span><span class="sxs-lookup"><span data-stu-id="a5a64-340">Pass-through keys enable an administrator to configure certain keys so they can only be read from the native registry, bypassing the Package and COW locations.</span></span> <span data-ttu-id="a5a64-341">Les emplacements de transfert sont globaux pour l’ordinateur (et non spécifiques au package) et peuvent être configurés en ajoutant le chemin d’accès à la clé, qui doit être traité comme directe à la valeur **reg \ _MULTI \ _SZ** appelée **PassThroughPaths** de la clé `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` .</span><span class="sxs-lookup"><span data-stu-id="a5a64-341">Pass-through locations are global to the machine (not package specific) and can be configured by adding the path to the key, which should be treated as pass-through to the **REG\_MULTI\_SZ** value called **PassThroughPaths** of the key `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry`.</span></span> <span data-ttu-id="a5a64-342">Toute touche qui s’affiche sous cette valeur de chaîne multiple (et leurs enfants) sera traitée comme directe.</span><span class="sxs-lookup"><span data-stu-id="a5a64-342">Any key that appears under this multi-string value (and their children) will be treated as pass-through.</span></span>

<span data-ttu-id="a5a64-343">Les emplacements suivants sont configurés comme emplacements de transfert par défaut:</span><span class="sxs-lookup"><span data-stu-id="a5a64-343">The following locations are configured as pass-through locations by default:</span></span>

-   <span data-ttu-id="a5a64-344">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="a5a64-344">HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="a5a64-345">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="a5a64-345">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="a5a64-346">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span><span class="sxs-lookup"><span data-stu-id="a5a64-346">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span></span>

-   <span data-ttu-id="a5a64-347">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span><span class="sxs-lookup"><span data-stu-id="a5a64-347">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span></span>

-   <span data-ttu-id="a5a64-348">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span><span class="sxs-lookup"><span data-stu-id="a5a64-348">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span></span>

-   <span data-ttu-id="a5a64-349">HKEY \ _CURRENT \ _USER paramètres de \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet</span><span class="sxs-lookup"><span data-stu-id="a5a64-349">HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Settings</span></span>

-   <span data-ttu-id="a5a64-350">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span><span class="sxs-lookup"><span data-stu-id="a5a64-350">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span></span>

-   <span data-ttu-id="a5a64-351">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="a5a64-351">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies</span></span>

-   <span data-ttu-id="a5a64-352">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="a5a64-352">HKEY\_CURRENT\_USER\\SOFTWARE\\Policies</span></span>

<span data-ttu-id="a5a64-353">L’objectif des clés directes consiste à s’assurer qu’une application virtuelle n’écrit pas de données de Registre dans le VReg requis pour les applications non virtuelles pour une opération ou une intégration réussie.</span><span class="sxs-lookup"><span data-stu-id="a5a64-353">The purpose of Pass-through keys is to ensure that a virtual application does not write registry data in the VReg that is required for non-virtual applications for successful operation or integration.</span></span> <span data-ttu-id="a5a64-354">La clé stratégies vérifie que les paramètres basés sur les stratégies de groupe définis par l’administrateur sont utilisés et pas par rapport aux paramètres du package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-354">The Policies key ensures that Group Policy based settings set by the administrator are utilized and not per package settings.</span></span> <span data-ttu-id="a5a64-355">La touche AppModel est nécessaire pour l’intégration aux applications basées sur les interfaces utilisateur modernes Windows.</span><span class="sxs-lookup"><span data-stu-id="a5a64-355">The AppModel key is required for integration with Windows Modern UI based applications.</span></span> <span data-ttu-id="a5a64-356">Il est recommandé de ne pas modifier les clés directes par défaut, mais dans certains cas, en fonction du comportement de l’application, il peut être nécessaire d’ajouter d’autres touches directes.</span><span class="sxs-lookup"><span data-stu-id="a5a64-356">It is recommend that administers do not modify any of the default pass-through keys, but in some instances, based on application behavior may require adding additional pass-through keys.</span></span>

## <a href="" id="bkmk-pkg-store-behavior"></a><span data-ttu-id="a5a64-357">Comportement du magasin de packages App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-357">App-V package store behavior</span></span>


<span data-ttu-id="a5a64-358">App-V 5 gère le magasin de packages, qui est l’emplacement de stockage des fichiers de ressources développés à partir du fichier AppV.</span><span class="sxs-lookup"><span data-stu-id="a5a64-358">App-V 5 manages the Package Store, which is the location where the expanded asset files from the appv file are stored.</span></span> <span data-ttu-id="a5a64-359">Par défaut, cet emplacement est stocké sur%ProgramData%\\App-V et est limité en termes de capacités de stockage uniquement par un espace libre sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a5a64-359">By default, this location is stored at %ProgramData%\\App-V, and is limited in terms of storage capabilities only by free disk space.</span></span> <span data-ttu-id="a5a64-360">Le magasin de packages est organisé selon les GUID pour le package et la version, comme indiqué dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="a5a64-360">The package store is organized by the GUIDs for the package and version as mentioned in the previous section.</span></span>

### <span data-ttu-id="a5a64-361">Ajouter des packages</span><span class="sxs-lookup"><span data-stu-id="a5a64-361">Add packages</span></span>

<span data-ttu-id="a5a64-362">Les packages App-V sont intermédiaires en plus de l’ordinateur doté du client App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-362">App-V Packages are staged upon addition to the computer with the App-V Client.</span></span> <span data-ttu-id="a5a64-363">Le client App-V fournit le Staging à la demande.</span><span class="sxs-lookup"><span data-stu-id="a5a64-363">The App-V Client provides on-demand staging.</span></span> <span data-ttu-id="a5a64-364">Lors de la publication ou d’une AppVClientPackage manuelle, la structure de données est intégrée à la Banque de packages (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span><span class="sxs-lookup"><span data-stu-id="a5a64-364">During publishing or a manual Add-AppVClientPackage, the data structure is built in the package store (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span></span> <span data-ttu-id="a5a64-365">Les fichiers de package identifiés dans le bloc de publication définis dans le StreamMap.xml sont ajoutés au système et les dossiers de niveau supérieur et les fichiers enfants intermédiaires pour garantir l’existence de ressources d’application appropriées au lancement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-365">The package files identified in the publishing block defined in the StreamMap.xml are added to the system and the top level folders and child files staged to ensure proper application assets exist at launch.</span></span>

### <span data-ttu-id="a5a64-366">Packages de montage</span><span class="sxs-lookup"><span data-stu-id="a5a64-366">Mounting packages</span></span>

<span data-ttu-id="a5a64-367">Les packages peuvent être chargés explicitement via PowerShell `Mount-AppVClientPackage` ou en utilisant l' **interface utilisateur du client App-V** pour télécharger un package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-367">Packages can be explicitly loaded using the PowerShell `Mount-AppVClientPackage` or by using the **App-V Client UI** to download a package.</span></span> <span data-ttu-id="a5a64-368">Cette opération charge entièrement le package complet dans le magasin de packages.</span><span class="sxs-lookup"><span data-stu-id="a5a64-368">This operation completely loads the entire package into the package store.</span></span>

### <span data-ttu-id="a5a64-369">Packages de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="a5a64-369">Streaming packages</span></span>

<span data-ttu-id="a5a64-370">Le client App-V peut être configuré pour modifier le comportement par défaut de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="a5a64-370">The App-V Client can be configured to change the default behavior of streaming.</span></span> <span data-ttu-id="a5a64-371">Toutes les stratégies de streaming sont stockées sous la clé de Registre `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` suivante:</span><span class="sxs-lookup"><span data-stu-id="a5a64-371">All streaming policies are stored under the following registry key: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming`.</span></span> <span data-ttu-id="a5a64-372">Les stratégies sont définies à l’aide de l’applet de passe PowerShell `Set-AppvClientConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="a5a64-372">Policies are set using the PowerShell cmdlet `Set-AppvClientConfiguration`.</span></span> <span data-ttu-id="a5a64-373">Les stratégies suivantes s’appliquent à la diffusion en continu:</span><span class="sxs-lookup"><span data-stu-id="a5a64-373">The following policies apply to Streaming:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-374">Stratégie</span><span class="sxs-lookup"><span data-stu-id="a5a64-374">Policy</span></span></th>
<th align="left"><span data-ttu-id="a5a64-375">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-376">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="a5a64-376">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-377">Sur Windows 8 et versions ultérieures, il permet de diffuser en continu des réseaux 3G et cellulaires.</span><span class="sxs-lookup"><span data-stu-id="a5a64-377">On Windows 8 and later, it allows streaming over 3G and cellular networks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-378">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="a5a64-378">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-379">Spécifie le paramètre de chargement en arrière-plan:</span><span class="sxs-lookup"><span data-stu-id="a5a64-379">Specifies the Background Load setting:</span></span></p>
<p><strong><span data-ttu-id="a5a64-380">0 </strong> - désactivé</span><span class="sxs-lookup"><span data-stu-id="a5a64-380">0</strong> - Disabled</span></span></p>
<p><strong><span data-ttu-id="a5a64-381">1 </strong> -packages auparavant utilisés</span><span class="sxs-lookup"><span data-stu-id="a5a64-381">1</strong> – Previously Used Packages only</span></span></p>
<p><strong><span data-ttu-id="a5a64-382">2 </strong> – tous les packages</span><span class="sxs-lookup"><span data-stu-id="a5a64-382">2</strong> – All Packages</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-383">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="a5a64-383">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-384">Le dossier racine pour le magasin de packages de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="a5a64-384">The root folder for the package store in the local machine</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-385">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="a5a64-385">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-386">Remplacement de la racine où les packages doivent être diffusés en continu</span><span class="sxs-lookup"><span data-stu-id="a5a64-386">The root override where packages should be streamed from</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-387">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="a5a64-387">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-388">Active l’utilisation du magasin de contenu partagé pour les scénarios d’infrastructure VDI</span><span class="sxs-lookup"><span data-stu-id="a5a64-388">Enables the use of Shared Content Store for VDI scenarios</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="a5a64-389">Ces paramètres affectent le comportement de la diffusion de ressources de package App-V pour le client.</span><span class="sxs-lookup"><span data-stu-id="a5a64-389">These settings affect the behavior of streaming App-V package assets to the client.</span></span> <span data-ttu-id="a5a64-390">Par défaut, App-V télécharge uniquement les ressources nécessaires après le téléchargement de la publication initiale et des blocs de fonctionnalités principaux.</span><span class="sxs-lookup"><span data-stu-id="a5a64-390">By default, App-V only downloads the assets required after downloading the initial publishing and primary feature blocks.</span></span> <span data-ttu-id="a5a64-391">Il existe trois comportements spécifiques dans les packages de diffusion en continu qui doivent être décrits:</span><span class="sxs-lookup"><span data-stu-id="a5a64-391">There are three specific behaviors around streaming packages that must be explained:</span></span>

-   <span data-ttu-id="a5a64-392">Lecture en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="a5a64-392">Background Streaming</span></span>

-   <span data-ttu-id="a5a64-393">Streaming optimisée</span><span class="sxs-lookup"><span data-stu-id="a5a64-393">Optimized Streaming</span></span>

-   <span data-ttu-id="a5a64-394">Erreurs de flux</span><span class="sxs-lookup"><span data-stu-id="a5a64-394">Stream Faults</span></span>

### <span data-ttu-id="a5a64-395">Lecture en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="a5a64-395">Background streaming</span></span>

<span data-ttu-id="a5a64-396">L’applet de cmdlet PowerShell `Get-AppvClientConfiguration` peut être utilisée pour déterminer le mode actuel de diffusion en arrière-plan avec le paramètre autoload et modifié avec l’applet de cmdlet Set-AppvClientConfiguration ou à partir du Registre (clé HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming).</span><span class="sxs-lookup"><span data-stu-id="a5a64-396">The PowerShell cmdlet `Get-AppvClientConfiguration` can be used to determine the current mode for background streaming with the AutoLoad setting and modified with the cmdlet Set-AppvClientConfiguration or from the registry (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming key).</span></span> <span data-ttu-id="a5a64-397">L’arrière-plan en arrière-plan est un paramètre par défaut dans lequel le paramètre autoload est défini pour télécharger les packages déjà utilisés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-397">Background streaming is a default setting where the Autoload setting is set to download previously used packages.</span></span> <span data-ttu-id="a5a64-398">Le comportement en fonction du paramètre par défaut (valeur = 1) télécharge les blocs de données App-V en arrière-plan après le lancement de l’application.</span><span class="sxs-lookup"><span data-stu-id="a5a64-398">The behavior based on default setting (value=1) downloads App-V data blocks in the background after the application has been launched.</span></span> <span data-ttu-id="a5a64-399">Ce paramètre peut être désactivé (valeur = 0) ou activé pour tous les packages (valeur = 2), qu’il ait été lancé.</span><span class="sxs-lookup"><span data-stu-id="a5a64-399">This setting can be disabled all together (value=0) or enabled for all packages (value=2), whether they have been launched.</span></span>

### <span data-ttu-id="a5a64-400">Streaming optimisée</span><span class="sxs-lookup"><span data-stu-id="a5a64-400">Optimized streaming</span></span>

<span data-ttu-id="a5a64-401">Les packages App-V peuvent être configurés avec un bloc de fonctionnalités principal lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="a5a64-401">App-V packages can be configured with a primary feature block during sequencing.</span></span> <span data-ttu-id="a5a64-402">Ce paramètre permet à l’ingénieur de séquençage de surveiller les fichiers de démarrage pour une application spécifique, ou applications, et de marquer les blocs de données dans le package App-V pour la diffusion en continu lors du premier lancement de l’application dans le package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-402">This setting allows the sequencing engineer to monitor launch files for a specific application, or applications, and mark the blocks of data in the App-V package for streaming at first launch of any application in the package.</span></span>

### <span data-ttu-id="a5a64-403">Erreurs de flux</span><span class="sxs-lookup"><span data-stu-id="a5a64-403">Stream faults</span></span>

<span data-ttu-id="a5a64-404">Après le flux initial de toutes les données de publication et du bloc de fonctionnalités principal, les demandes de fichiers supplémentaires effectuent des erreurs de flux.</span><span class="sxs-lookup"><span data-stu-id="a5a64-404">After the initial stream of any publishing data and the primary feature block, requests for additional files perform stream faults.</span></span> <span data-ttu-id="a5a64-405">Ces blocs de données sont téléchargés vers le magasin de packages le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a5a64-405">These blocks of data are downloaded to the package store on an as-needed basis.</span></span> <span data-ttu-id="a5a64-406">Cela permet à un utilisateur de télécharger uniquement une petite partie du package, qui suffit en général pour lancer le package et exécuter des tâches normales.</span><span class="sxs-lookup"><span data-stu-id="a5a64-406">This allows a user to download only a small part of the package, typically enough to launch the package and run normal tasks.</span></span> <span data-ttu-id="a5a64-407">Tous les autres blocs sont téléchargés lorsqu’un utilisateur lance une opération qui nécessite des données qui ne figurent pas actuellement dans le magasin de packages.</span><span class="sxs-lookup"><span data-stu-id="a5a64-407">All other blocks are downloaded when a user initiates an operation that requires data not currently in the package store.</span></span>

<span data-ttu-id="a5a64-408">Pour plus d’informations sur la diffusion en continu de packages App-V, voir: <https://go.microsoft.com/fwlink/?LinkId=392770> .</span><span class="sxs-lookup"><span data-stu-id="a5a64-408">For more information on App-V Package streaming visit: <https://go.microsoft.com/fwlink/?LinkId=392770>.</span></span>

<span data-ttu-id="a5a64-409">Le séquençage pour l’optimisation de la diffusion en continu est disponible à l’adresse suivante: <https://go.microsoft.com/fwlink/?LinkId=392771> .</span><span class="sxs-lookup"><span data-stu-id="a5a64-409">Sequencing for streaming optimization is available at: <https://go.microsoft.com/fwlink/?LinkId=392771>.</span></span>

### <span data-ttu-id="a5a64-410">Mises à jour de package</span><span class="sxs-lookup"><span data-stu-id="a5a64-410">Package upgrades</span></span>

<span data-ttu-id="a5a64-411">Les packages App-V nécessitent une mise à jour tout au long du cycle de vie de l’application.</span><span class="sxs-lookup"><span data-stu-id="a5a64-411">App-V Packages require updating throughout the lifecycle of the application.</span></span> <span data-ttu-id="a5a64-412">Les mises à niveau des packages App-V sont similaires à l’opération de publication de package, car chaque version sera créée dans son propre emplacement racine: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` .</span><span class="sxs-lookup"><span data-stu-id="a5a64-412">App-V Package upgrades are similar to the package publish operation, as each version will be created in its own PackageRoot location: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}`.</span></span> <span data-ttu-id="a5a64-413">L’opération de mise à niveau est optimisée en créant des liens durs vers des fichiers identiques et en continu à partir d’autres versions du même package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-413">The upgrade operation is optimized by creating hard links to identical- and streamed-files from other versions of the same package.</span></span>

### <span data-ttu-id="a5a64-414">Suppression de package</span><span class="sxs-lookup"><span data-stu-id="a5a64-414">Package removal</span></span>

<span data-ttu-id="a5a64-415">Le comportement du client App-V lors de la suppression des packages dépend de la méthode de suppression utilisée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-415">The behavior of the App-V Client when packages are removed depends on the method used for removal.</span></span> <span data-ttu-id="a5a64-416">L’utilisation de l’infrastructure complète d’App-V pour annuler la publication de l’application, les fichiers de catalogue des utilisateurs (catalogue d’ordinateurs pour les applications publiées globalement) sont supprimés, mais conserve l’emplacement et les emplacements de la boutique du package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-416">Using an App-V full infrastructure to unpublish the application, the user catalog files (machine catalog for globally published applications) are removed, but retains the package store location and COW locations.</span></span> <span data-ttu-id="a5a64-417">Lorsque l’applet de cmdlet PowerShell `Remove-AppVClientPackge` est utilisée pour supprimer un package App-V, l’emplacement du magasin de packages est nettoyé.</span><span class="sxs-lookup"><span data-stu-id="a5a64-417">When the PowerShell cmdlet `Remove-AppVClientPackge` is used to remove an App-V Package, the package store location is cleaned.</span></span> <span data-ttu-id="a5a64-418">N’oubliez pas que l’annulation de la publication d’un package App-V à partir du serveur de gestion n’effectue aucune opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="a5a64-418">Remember that unpublishing an App-V Package from the Management Server does not perform a Remove operation.</span></span> <span data-ttu-id="a5a64-419">Aucune opération ne supprime les fichiers de package du magasin de packages.</span><span class="sxs-lookup"><span data-stu-id="a5a64-419">Neither operation will remove the Package Store package files.</span></span>

## <a href="" id="bkmk-roaming-reg-data"></a><span data-ttu-id="a5a64-420">Itinérance et Registre</span><span class="sxs-lookup"><span data-stu-id="a5a64-420">Roaming registry and data</span></span>


<span data-ttu-id="a5a64-421">App-V 5 est en mesure de fournir une version proche du natif lors de l’itinérance, en fonction du mode d’écriture de l’application utilisée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-421">App-V 5 is able to provide a near-native experience when roaming, depending on how the application being used is written.</span></span> <span data-ttu-id="a5a64-422">Par défaut, App-V est une itinérance qui est stockée dans l’emplacement d’itinérance en fonction de la configuration d’itinérance du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-422">By default, App-V roams AppData that is stored in the roaming location, based on the roaming configuration of the operating system.</span></span> <span data-ttu-id="a5a64-423">D’autres emplacements pour le stockage des données basées sur des fichiers ne peuvent pas être déplacés de l’ordinateur vers l’ordinateur, car ils se trouvent dans des emplacements qui ne sont pas en itinérance.</span><span class="sxs-lookup"><span data-stu-id="a5a64-423">Other locations for storage of file-based data do not roam from computer to computer, since they are in locations that are not roamed.</span></span>

### <a href="" id="bkmk-clt-inter-roam-reqs"></a><span data-ttu-id="a5a64-424">Configuration requise pour l’itinérance et stockage des données de catalogue utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-424">Roaming requirements and user catalog data storage</span></span>

<span data-ttu-id="a5a64-425">App-V stocke les données, qui représentent l’état du catalogue de l’utilisateur, sous la forme:</span><span class="sxs-lookup"><span data-stu-id="a5a64-425">App-V stores data, which represents the state of the user’s catalog, in the form of:</span></span>

-   <span data-ttu-id="a5a64-426">Fichiers sous%appdata%\\Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="a5a64-426">Files under %appdata%\\Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="a5a64-427">Paramètres du Registre sous</span><span class="sxs-lookup"><span data-stu-id="a5a64-427">Registry settings under</span></span> `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

<span data-ttu-id="a5a64-428">Ensemble, ces fichiers et paramètres de Registre représentent le catalogue de l’utilisateur, ce qui signifie que les deux doivent être itinérants ou qu’aucun autre utilisateur ne doit être itinérant pour un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="a5a64-428">Together, these files and registry settings represent the user’s catalog, so either both must be roamed, or neither must be roamed for a given user.</span></span> <span data-ttu-id="a5a64-429">App-V ne prend pas en charge l’itinérance% AppData%, mais pas l’itinérance du profil de l’utilisateur (registre), ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a5a64-429">App-V does not support roaming %AppData%, but not roaming the user’s profile (registry), or vice versa.</span></span>

<span data-ttu-id="a5a64-430">**Remarques**  L’applet de **AppvClientPackage de réparation** ne répare pas l’état de publication des packages dans lesquels l’État App-V de l’utilisateur `HKEY_CURRENT_USER` est manquant ou ne correspond pas aux données dans% AppData%.</span><span class="sxs-lookup"><span data-stu-id="a5a64-430">**Note** The **Repair-AppvClientPackage** cmdlet does not repair the publishing state of packages, where the user’s App-V state under `HKEY_CURRENT_USER` is missing or mismatched with the data in %appdata%.</span></span>

 

### <span data-ttu-id="a5a64-431">Données basées sur le registre</span><span class="sxs-lookup"><span data-stu-id="a5a64-431">Registry-based data</span></span>

<span data-ttu-id="a5a64-432">L’itinérance de Registre dans App-V est divisée en deux scénarios, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a5a64-432">App-V registry roaming falls into two scenarios, as shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-433">Scénario</span><span class="sxs-lookup"><span data-stu-id="a5a64-433">Scenario</span></span></th>
<th align="left"><span data-ttu-id="a5a64-434">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-434">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-435">Applications exécutées en tant qu’utilisateurs standard</span><span class="sxs-lookup"><span data-stu-id="a5a64-435">Applications that are run as standard users</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-436">Lorsqu’un utilisateur standard lance une application App-V, les applications HKLM et HKCU pour les applications App-V sont stockées dans la ruche HKCU de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-436">When a standard user launches an App-V application, both HKLM and HKCU for App-V applications are stored in the HKCU hive on the machine.</span></span> <span data-ttu-id="a5a64-437">Ce qui s’affiche sous la forme de deux trajectoires distinctes:</span><span class="sxs-lookup"><span data-stu-id="a5a64-437">This presents as two distinct paths:</span></span></p>
<ul>
<li><p><span data-ttu-id="a5a64-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="a5a64-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="a5a64-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {UserSID} \ logiciel</span><span class="sxs-lookup"><span data-stu-id="a5a64-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</span></span></p></li>
</ul>
<p><span data-ttu-id="a5a64-440">Les emplacements sont activés pour l’itinérance en fonction des paramètres du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-440">The locations are enabled for roaming based on the operating system settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-441">Applications qui sont exécutées avec l’élévation</span><span class="sxs-lookup"><span data-stu-id="a5a64-441">Applications that are run with elevation</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-442">Lorsqu’une application est lancée avec l’élévation:</span><span class="sxs-lookup"><span data-stu-id="a5a64-442">When an application is launched with elevation:</span></span></p>
<ul>
<li><p><span data-ttu-id="a5a64-443">Les données HKLM sont stockées dans la ruche HKLM de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a5a64-443">HKLM data is stored in the HKLM hive on the local computer</span></span></p></li>
<li><p><span data-ttu-id="a5a64-444">Les données HKCU sont stockées dans l’emplacement du registre de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-444">HKCU data is stored in the User Registry location</span></span></p></li>
</ul>
<p><span data-ttu-id="a5a64-445">Dans ce scénario, ces paramètres ne sont pas itinérants avec des configurations d’itinérance de système d’exploitation normales, et les valeurs et clés de Registre obtenues sont stockées à l’emplacement suivant:</span><span class="sxs-lookup"><span data-stu-id="a5a64-445">In this scenario, these settings are not roamed with normal operating system roaming configurations, and the resulting registry keys and values are stored in the following location:</span></span></p>
<ul>
<li><p><span data-ttu-id="a5a64-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {UserSID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="a5a64-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="a5a64-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {UserSID} \ logiciel</span><span class="sxs-lookup"><span data-stu-id="a5a64-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a5a64-448">Redirection d’App-V et de dossiers</span><span class="sxs-lookup"><span data-stu-id="a5a64-448">App-V and folder redirection</span></span>

<span data-ttu-id="a5a64-449">App-V 5,1 prend en charge la redirection de dossiers du dossier AppData Roaming (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="a5a64-449">App-V 5.1 supports folder redirection of the roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="a5a64-450">Lorsque l’environnement virtuel est démarré, l’État AppData d’itinérance du répertoire de l’itinérance de l’utilisateur est copié dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="a5a64-450">When the virtual environment is started, the roaming AppData state from the user’s roaming AppData directory is copied to the local cache.</span></span> <span data-ttu-id="a5a64-451">À l’inverse, lorsque l’environnement virtuel est arrêté, le cache local associé au AppData d’itinérance d’un utilisateur particulier est transféré vers l’emplacement réel du répertoire AppData errant de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-451">Conversely, when the virtual environment is shut down, the local cache that is associated with a specific user’s roaming AppData is transferred to the actual location of that user’s roaming AppData directory.</span></span>

<span data-ttu-id="a5a64-452">Un package standard comporte plusieurs emplacements mappés dans le magasin de stockage de l’utilisateur pour les paramètres à la fois dans AppData\\Local et AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="a5a64-452">A typical package has several locations mapped in the user’s backing store for settings in both AppData\\Local and AppData\\Roaming.</span></span> <span data-ttu-id="a5a64-453">Il s’agit de la copie de l’emplacement d’écriture qui est stockée par utilisateur dans le profil de l’utilisateur et qui est utilisée pour enregistrer les modifications apportées aux répertoires VFS du package et pour protéger le fichier VFS de package par défaut.</span><span class="sxs-lookup"><span data-stu-id="a5a64-453">These locations are the Copy on Write locations that are stored per user in the user’s profile, and that are used to store changes made to the package VFS directories and to protect the default package VFS.</span></span>

<span data-ttu-id="a5a64-454">Le tableau suivant indique les emplacements local et d’itinérance, lorsque la redirection de dossiers n’a pas été implémentée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-454">The following table shows local and roaming locations, when folder redirection has not been implemented.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-455">Répertoire VFS dans le package</span><span class="sxs-lookup"><span data-stu-id="a5a64-455">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="a5a64-456">Emplacement mappé du magasin de stockage</span><span class="sxs-lookup"><span data-stu-id="a5a64-456">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-457">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="a5a64-457">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-458">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="a5a64-458">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-459">SystemX86</span><span class="sxs-lookup"><span data-stu-id="a5a64-459">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-460">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="a5a64-460">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-461">Windows</span><span class="sxs-lookup"><span data-stu-id="a5a64-461">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-462">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</span><span class="sxs-lookup"><span data-stu-id="a5a64-462">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-463">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="a5a64-463">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-464">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="a5a64-464">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-465">AppData</span><span class="sxs-lookup"><span data-stu-id="a5a64-465">AppData</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-466">C:\users\jsmith\AppData &lt; &gt; </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="a5a64-466">C:\users\jsmith\AppData&lt;strong&gt;Roaming</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="a5a64-467">Le tableau suivant répertorie les emplacements local et d’itinérance, lorsque la redirection de dossiers a été implémentée pour% AppData% et que l’emplacement a été redirigé (généralement vers un emplacement réseau).</span><span class="sxs-lookup"><span data-stu-id="a5a64-467">The following table shows local and roaming locations, when folder redirection has been implemented for %AppData%, and the location has been redirected (typically to a network location).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-468">Répertoire VFS dans le package</span><span class="sxs-lookup"><span data-stu-id="a5a64-468">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="a5a64-469">Emplacement mappé du magasin de stockage</span><span class="sxs-lookup"><span data-stu-id="a5a64-469">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-470">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="a5a64-470">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-471">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="a5a64-471">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-472">SystemX86</span><span class="sxs-lookup"><span data-stu-id="a5a64-472">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-473">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="a5a64-473">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-474">Windows</span><span class="sxs-lookup"><span data-stu-id="a5a64-474">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-475">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</span><span class="sxs-lookup"><span data-stu-id="a5a64-475">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-476">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="a5a64-476">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-477">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="a5a64-477">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-478">AppData</span><span class="sxs-lookup"><span data-stu-id="a5a64-478">AppData</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a5a64-479">\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="a5a64-479">\Fileserver</strong>\users\jsmith\roaming\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="a5a64-480">Le pilote de client virtuel App-V ne peut pas écrire sur les emplacements réseau, de sorte que le client App-V détecte la présence d’une redirection de dossier et copie les données sur le disque local lors de la publication et au démarrage de l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="a5a64-480">The current App-V Client VFS driver cannot write to network locations, so the App-V Client detects the presence of folder redirection and copies the data on the local drive during publishing and when the virtual environment starts.</span></span> <span data-ttu-id="a5a64-481">Après que l’utilisateur a fermé l’application application-V et que le client App-V ferme l’environnement virtuel, le stockage local de VFS AppData est copié sur le réseau, ce qui permet d’utiliser l’itinérance sur des ordinateurs supplémentaires dans lesquels le processus est répété.</span><span class="sxs-lookup"><span data-stu-id="a5a64-481">After the user closes the App-V application and the App-V Client closes the virtual environment, the local storage of the VFS AppData is copied back to the network, enabling roaming to additional machines, where the process will be repeated.</span></span> <span data-ttu-id="a5a64-482">Les étapes détaillées des processus sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="a5a64-482">The detailed steps of the processes are:</span></span>

1.  <span data-ttu-id="a5a64-483">Lors du démarrage d’une publication ou d’un environnement virtuel, le client App-V détecte l’emplacement du répertoire AppData.</span><span class="sxs-lookup"><span data-stu-id="a5a64-483">During publishing or virtual environment startup, the App-V Client detects the location of the AppData directory.</span></span>

2.  <span data-ttu-id="a5a64-484">Si le chemin d’accès AppData d’itinérance est local ou INO AppData\\Roaming location est mappé, rien ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a5a64-484">If the roaming AppData path is local or ino AppData\\Roaming location is mapped, nothing happens.</span></span>

3.  <span data-ttu-id="a5a64-485">Si le chemin d’accès AppData d’itinérance n’est pas local, le répertoire de VFS AppData est mappé au répertoire AppData Local.</span><span class="sxs-lookup"><span data-stu-id="a5a64-485">If the roaming AppData path is not local, the VFS AppData directory is mapped to the local AppData directory.</span></span>

<span data-ttu-id="a5a64-486">Ce processus résout le problème de% AppData% non local qui n’est pas pris en charge par le pilote VFS du client App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-486">This process solves the problem of a non-local %AppData% that is not supported by the App-V Client VFS driver.</span></span> <span data-ttu-id="a5a64-487">Toutefois, les données stockées dans ce nouvel emplacement ne sont pas itinérantes lors de la redirection de dossiers.</span><span class="sxs-lookup"><span data-stu-id="a5a64-487">However, the data stored in this new location is not roamed with folder redirection.</span></span> <span data-ttu-id="a5a64-488">Les modifications apportées lors de l’exécution de l’application se produisent dans l’emplacement AppData Local et doivent être copiées à l’emplacement Redirigé.</span><span class="sxs-lookup"><span data-stu-id="a5a64-488">All changes during the running of the application happen to the local AppData location and must be copied to the redirected location.</span></span> <span data-ttu-id="a5a64-489">Les étapes détaillées du processus sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="a5a64-489">The detailed steps of this process are:</span></span>

1.  <span data-ttu-id="a5a64-490">L’application application-V s’arrête, ce qui arrête l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="a5a64-490">App-V application is shut down, which shuts down the virtual environment.</span></span>

2.  <span data-ttu-id="a5a64-491">Le cache local de l’emplacement AppData d’itinérance est compressé et est stocké dans un fichier ZIP.</span><span class="sxs-lookup"><span data-stu-id="a5a64-491">The local cache of the roaming AppData location is compressed and stored in a ZIP file.</span></span>

3.  <span data-ttu-id="a5a64-492">Un horodatage à la fin du processus d’empaquetage ZIP est utilisé pour nommer le fichier.</span><span class="sxs-lookup"><span data-stu-id="a5a64-492">A timestamp at the end of the ZIP packaging process is used to name the file.</span></span>

4.  <span data-ttu-id="a5a64-493">L’horodatage est enregistré dans le registre: HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime en tant que dernier horodatage connu de AppData.</span><span class="sxs-lookup"><span data-stu-id="a5a64-493">The timestamp is recorded in the registry: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\&lt;GUID&gt;\\AppDataTime as the last known AppData timestamp.</span></span>

5.  <span data-ttu-id="a5a64-494">Le processus de redirection de dossier est appelé pour évaluer et lancer le fichier ZIP chargé dans le répertoire AppData d’itinérance.</span><span class="sxs-lookup"><span data-stu-id="a5a64-494">The folder redirection process is called to evaluate and initiate the ZIP file uploaded to the roaming AppData directory.</span></span>

<span data-ttu-id="a5a64-495">La date d’horodatage est utilisée pour déterminer un scénario de dernier scripteur WINS s’il existe un conflit et est utilisé pour optimiser le téléchargement des données lors de la publication de l’application App-V ou de l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="a5a64-495">The timestamp is used to determine a “last writer wins” scenario if there is a conflict and is used to optimize the download of the data when the App-V application is published or the virtual environment is started.</span></span> <span data-ttu-id="a5a64-496">La redirection de dossiers rend les données accessibles à tous les autres clients couverts par la stratégie de prise en charge et démarre le processus de stockage des données AppData\\Roaming à l’emplacement AppData Local sur le client.</span><span class="sxs-lookup"><span data-stu-id="a5a64-496">Folder redirection will make the data available from any other clients covered by the supporting policy and will initiate the process of storing the AppData\\Roaming data to the local AppData location on the client.</span></span> <span data-ttu-id="a5a64-497">Les processus détaillés sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="a5a64-497">The detailed processes are:</span></span>

1.  <span data-ttu-id="a5a64-498">L’utilisateur démarre l’environnement virtuel en démarrant une application.</span><span class="sxs-lookup"><span data-stu-id="a5a64-498">The user starts the virtual environment by starting an application.</span></span>

2.  <span data-ttu-id="a5a64-499">L’environnement virtuel de l’application vérifie le fichier ZIP le plus récent, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a5a64-499">The application’s virtual environment checks for the most recent time stamped ZIP file, if present.</span></span>

3.  <span data-ttu-id="a5a64-500">Le Registre est consulté pour le dernier horodatage téléchargé connu, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a5a64-500">The registry is checked for the last known uploaded timestamp, if present.</span></span>

4.  <span data-ttu-id="a5a64-501">Le fichier ZIP le plus récent est téléchargé, sauf si le dernier horodatage de chargement connu est supérieur ou égal à la date d’horodatage du fichier ZIP.</span><span class="sxs-lookup"><span data-stu-id="a5a64-501">The most recent ZIP file is downloaded unless the local last known upload timestamp is greater than or equal to the timestamp from the ZIP file.</span></span>

5.  <span data-ttu-id="a5a64-502">Si le dernier horodatage connu connu est antérieur à celui du fichier ZIP le plus récent dans l’emplacement AppData d’itinérance, le fichier ZIP est extrait dans le répertoire temporaire local du profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-502">If the local last known upload timestamp is earlier than that of the most recent ZIP file in the roaming AppData location, the ZIP file is extracted to the local temp directory in the user’s profile.</span></span>

6.  <span data-ttu-id="a5a64-503">Après l’extraction réussie du fichier ZIP, le cache local de l’annuaire AppData d’itinérance est renommé et les nouvelles données sont déplacées vers l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-503">After the ZIP file is successfully extracted, the local cache of the roaming AppData directory is renamed and the new data is moved into place.</span></span>

7.  <span data-ttu-id="a5a64-504">L’annuaire renommé est supprimé et l’application s’ouvre avec le plus dernier enregistrement de données AppData.</span><span class="sxs-lookup"><span data-stu-id="a5a64-504">The renamed directory is deleted and the application opens with the most recently saved roaming AppData data.</span></span>

<span data-ttu-id="a5a64-505">Cette opération complète l’itinérance réussie des paramètres d’application présents dans les emplacements AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="a5a64-505">This completes the successful roaming of application settings that are present in AppData\\Roaming locations.</span></span> <span data-ttu-id="a5a64-506">La seule autre condition devant être adressée est une opération de réparation de package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-506">The only other condition that must be addressed is a package repair operation.</span></span> <span data-ttu-id="a5a64-507">Les détails du processus sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="a5a64-507">The details of the process are:</span></span>

1.  <span data-ttu-id="a5a64-508">Lors de la réparation, détecter si le chemin d’accès au répertoire de l’itinérance de l’utilisateur n’est pas local.</span><span class="sxs-lookup"><span data-stu-id="a5a64-508">During repair, detect if the path to the user’s roaming AppData directory is not local.</span></span>

2.  <span data-ttu-id="a5a64-509">Mapper les cibles de chemin d’accès AppData non locales sont recréées en tant qu’itinérance attendue et en local AppData.</span><span class="sxs-lookup"><span data-stu-id="a5a64-509">Map the non-local roaming AppData path targets are recreated the expected roaming and local AppData locations.</span></span>

3.  <span data-ttu-id="a5a64-510">Supprimez l’estampille qui est stockée dans le registre, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a5a64-510">Delete the timestamp stored in the registry, if present.</span></span>

<span data-ttu-id="a5a64-511">Ce processus permet de recréer les emplacements local et réseau pour AppData et de supprimer l’enregistrement de registre de l’estampille.</span><span class="sxs-lookup"><span data-stu-id="a5a64-511">This process will re-create both the local and network locations for AppData and remove the registry record of the timestamp.</span></span>

## <a href="" id="bkmk-clt-app-lifecycle"></a><span data-ttu-id="a5a64-512">Gestion du cycle de vie des applications du client App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-512">App-V client application lifecycle management</span></span>


<span data-ttu-id="a5a64-513">Dans une infrastructure complète App-V, une fois les applications séquencées, elles sont gérées et publiées sur des utilisateurs ou des ordinateurs via la gestion de l’application-V et des serveurs de publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-513">In an App-V Full Infrastructure, after applications are sequenced they are managed and published to users or computers via the App-V Management and Publishing servers.</span></span> <span data-ttu-id="a5a64-514">Cette section détaille les opérations effectuées pendant les opérations courantes du cycle de vie des applications (ajout, publication, lancement, mise à niveau et suppression), ainsi que les emplacements de fichiers et de Registre modifiés et modifiés du point de vue du client App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-514">This section details the operations that occur during the common App-V application lifecycle operations (Add, publishing, launch, upgrade, and removal) and the file and registry locations that are changed and modified from the App-V Client perspective.</span></span> <span data-ttu-id="a5a64-515">Les opérations clientes App-V sont exécutées sous la forme d’une série de commandes PowerShell démarrées sur l’ordinateur exécutant le client App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-515">The App-V Client operations are performed as a series of PowerShell commands initiated on the computer running the App-V Client.</span></span>

<span data-ttu-id="a5a64-516">Ce document porte sur les solutions d’infrastructure complète App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-516">This document focuses on App-V Full Infrastructure solutions.</span></span> <span data-ttu-id="a5a64-517">Pour obtenir des informations spécifiques sur l’intégration d’App-V à Configuration Manager 2012, consultez la page suivante: <https://go.microsoft.com/fwlink/?LinkId=392773></span><span class="sxs-lookup"><span data-stu-id="a5a64-517">For specific information on App-V Integration with Configuration Manager 2012 visit: <https://go.microsoft.com/fwlink/?LinkId=392773>.</span></span>

<span data-ttu-id="a5a64-518">Les tâches du cycle de vie de l’application-V sont déclenchées lors de la connexion utilisateur (par défaut), au démarrage de l’ordinateur ou en tant qu’opérations chronométrées en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a5a64-518">The App-V application lifecycle tasks are triggered at user login (default), machine startup, or as background timed operations.</span></span> <span data-ttu-id="a5a64-519">Les paramètres des opérations clientes App-V, y compris les serveurs de publication, les intervalles d’actualisation, l’activation du script de package, etc., sont configurés lors de l’installation du client ou après l’installation de commandes PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5a64-519">The settings for the App-V Client operations, including Publishing Servers, refresh intervals, package script enablement, and others, are configured during setup of the client or post-setup with PowerShell commands.</span></span> <span data-ttu-id="a5a64-520">Pour plus d’informations sur le déploiement du [client App-V](how-to-deploy-the-app-v-client-51gb18030.md) et sur l’utilisation de PowerShell, voir la section déploiement du client sur TechNet:</span><span class="sxs-lookup"><span data-stu-id="a5a64-520">See the How to Deploy the Client section on TechNet at: [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md) or utilize the PowerShell:</span></span>

```powershell
get-command *appv*
```

### <span data-ttu-id="a5a64-521">Actualisation de la publication</span><span class="sxs-lookup"><span data-stu-id="a5a64-521">Publishing refresh</span></span>

<span data-ttu-id="a5a64-522">Le processus d’actualisation de publication inclut plusieurs opérations plus petites effectuées sur le client App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-522">The publishing refresh process is comprised of several smaller operations that are performed on the App-V Client.</span></span> <span data-ttu-id="a5a64-523">Dans la mesure où App-V est une technologie de virtualisation des applications qui n’est pas une technologie de planification de tâches, le planificateur de tâches Windows est utilisé pour activer le processus lors de l’ouverture de session de l’utilisateur, au démarrage de l’ordinateur et aux intervalles prévus.</span><span class="sxs-lookup"><span data-stu-id="a5a64-523">Since App-V is an application virtualization technology and not a task scheduling technology, the Windows Task Scheduler is utilized to enable the process at user logon, machine startup, and at scheduled intervals.</span></span> <span data-ttu-id="a5a64-524">Dans le cadre de l’installation, la configuration du client est la méthode recommandée lors de la distribution du client à un grand groupe d’ordinateurs avec les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-524">The configuration of the client during setup listed above is the preferred method when distributing the client to a large group of computers with the correct settings.</span></span> <span data-ttu-id="a5a64-525">Ces paramètres client peuvent être configurés avec les applets de commande PowerShell suivantes:</span><span class="sxs-lookup"><span data-stu-id="a5a64-525">These client settings can be configured with the following PowerShell cmdlets:</span></span>

-   <span data-ttu-id="a5a64-526">**Add-AppVPublishingServer:** Configure le client avec un serveur de publication App-V qui fournit des packages App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-526">**Add-AppVPublishingServer:** Configures the client with an App-V Publishing Server that provides App-V packages.</span></span>

-   <span data-ttu-id="a5a64-527">**Set-AppVPublishingServer:** Modifie les paramètres actuels du serveur de publication App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-527">**Set-AppVPublishingServer:** Modifies the current settings for the App-V Publishing Server.</span></span>

-   <span data-ttu-id="a5a64-528">**Set-AppVClientConfiguration:** Modifie les paramètres actuels pour le client App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-528">**Set-AppVClientConfiguration:** Modifies the currents settings for the App-V Client.</span></span>

-   <span data-ttu-id="a5a64-529">**Synchronisation-AppVPublishingServer:** Démarre un processus d’actualisation de la publication de l’application V manuellement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-529">**Sync-AppVPublishingServer:** Initiates an App-V Publishing Refresh process manually.</span></span> <span data-ttu-id="a5a64-530">Il est également utilisé dans les tâches planifiées créées lors de la configuration du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-530">This is also utilized in the scheduled tasks created during configuration of the publishing server.</span></span>

<span data-ttu-id="a5a64-531">Les sections suivantes permettent de détailler les opérations qui se produisent pendant différentes phases d’actualisation de la publication d’une application.</span><span class="sxs-lookup"><span data-stu-id="a5a64-531">The focus of the following sections is to detail the operations that occur during different phases of an App-V Publishing Refresh.</span></span> <span data-ttu-id="a5a64-532">Les rubriques suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="a5a64-532">The topics include:</span></span>

-   <span data-ttu-id="a5a64-533">Ajout d’un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-533">Adding an App-V Package</span></span>

-   <span data-ttu-id="a5a64-534">Publication d’un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-534">Publishing an App-V Package</span></span>

### <span data-ttu-id="a5a64-535">Ajout d’un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-535">Adding an App-V package</span></span>

<span data-ttu-id="a5a64-536">L’ajout d’un package App-V au client est la première étape du processus d’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-536">Adding an App-V package to the client is the first step of the publishing refresh process.</span></span> <span data-ttu-id="a5a64-537">Le résultat final est le même que celui `Add-AppVClientPackage` de l’applet de commande dans PowerShell, sauf lors du processus d’actualisation de la publication, le serveur de publication configuré est contacté et transmet une liste d’applications de niveau supérieur au client pour extraire des informations plus détaillées et non une opération d’ajout de package unique.</span><span class="sxs-lookup"><span data-stu-id="a5a64-537">The end result is the same as the `Add-AppVClientPackage` cmdlet in PowerShell, except during the publishing refresh add process, the configured publishing server is contacted and passes a high-level list of applications back to the client to pull more detailed information and not a single package add operation.</span></span> <span data-ttu-id="a5a64-538">Le processus se poursuit en configurant le client pour les ajouts ou mises à jour d’un package ou d’un groupe de connexions, puis accède au fichier AppV.</span><span class="sxs-lookup"><span data-stu-id="a5a64-538">The process continues by configuring the client for package or connection group additions or updates, then accesses the appv file.</span></span> <span data-ttu-id="a5a64-539">Ensuite, le contenu du fichier AppV est développé et placé sur le système d’exploitation local aux emplacements appropriés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-539">Next, the contents of the appv file are expanded and placed on the local operating system in the appropriate locations.</span></span> <span data-ttu-id="a5a64-540">Vous trouverez ci-dessous un flux de travail détaillé du processus, en supposant que le package est configuré pour le streaming de panne.</span><span class="sxs-lookup"><span data-stu-id="a5a64-540">The following is a detailed workflow of the process, assuming the package is configured for Fault Streaming.</span></span>

**<span data-ttu-id="a5a64-541">Comment ajouter un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-541">How to add an App-V package</span></span>**

1.  <span data-ttu-id="a5a64-542">Initiation manuelle via PowerShell ou le lancement de séquence de tâches du processus d’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-542">Manual initiation via PowerShell or Task Sequence initiation of the Publishing Refresh process.</span></span>

    1.  <span data-ttu-id="a5a64-543">Le client App-V effectue une connexion HTTP et demande une liste d’applications basées sur la cible.</span><span class="sxs-lookup"><span data-stu-id="a5a64-543">The App-V Client makes an HTTP connection and requests a list of applications based on the target.</span></span> <span data-ttu-id="a5a64-544">Le processus d’actualisation de publication prend en charge le ciblage des ordinateurs ou des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-544">The Publishing refresh process supports targeting machines or users.</span></span>

    2.  <span data-ttu-id="a5a64-545">Le serveur de publication App-V utilise l’identité de la cible, de l’utilisateur ou de l’ordinateur de lancement et interroge la base de données pour obtenir la liste des applications autorisées.</span><span class="sxs-lookup"><span data-stu-id="a5a64-545">The App-V Publishing Server uses the identity of the initiating target, user or machine, and queries the database for a list of entitled applications.</span></span> <span data-ttu-id="a5a64-546">La liste des applications est fournie sous la forme d’une réponse XML, que le client utilise pour envoyer des demandes supplémentaires au serveur pour plus d’informations sur chaque package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-546">The list of applications is provided as an XML response, which the client uses to send additional requests to the server for more information on a per package basis.</span></span>

2.  <span data-ttu-id="a5a64-547">L’agent de publication sur le client App-V effectue toutes les actions ci-dessous sérialisées.</span><span class="sxs-lookup"><span data-stu-id="a5a64-547">The Publishing Agent on the App-V Client performs all actions below serialized.</span></span>

    <span data-ttu-id="a5a64-548">Évaluez les groupes de connexion qui sont non publiés ou désactivés, car les mises à jour de version de package qui font partie du groupe de connexion ne peuvent pas être traitées.</span><span class="sxs-lookup"><span data-stu-id="a5a64-548">Evaluate any connection groups that are unpublished or disabled, since package version updates that are part of the connection group cannot be processed.</span></span>

3.  <span data-ttu-id="a5a64-549">Configurez les packages en identifiant des opérations d’ajout ou de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a5a64-549">Configure the packages by identifying an Add or Update operations.</span></span>

    1.  <span data-ttu-id="a5a64-550">Le client App-V utilise l’API AppX de Windows et accède au fichier AppV à partir du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-550">The App-V Client utilizes the AppX API from Windows and accesses the appv file from the publishing server.</span></span>

    2.  <span data-ttu-id="a5a64-551">Le fichier de package est ouvert, et les AppXManifest.xml et les StreamMap.xml sont téléchargés vers le magasin de packages.</span><span class="sxs-lookup"><span data-stu-id="a5a64-551">The package file is opened and the AppXManifest.xml and StreamMap.xml are downloaded to the Package Store.</span></span>

    3.  <span data-ttu-id="a5a64-552">La publication de flux entièrement bloque les données définies dans le StreamMap.xml.</span><span class="sxs-lookup"><span data-stu-id="a5a64-552">Completely stream publishing block data defined in the StreamMap.xml.</span></span> <span data-ttu-id="a5a64-553">Stocke les données de bloc de publication dans le package Store\\PkgGUID\\VerGUID\\Root.</span><span class="sxs-lookup"><span data-stu-id="a5a64-553">Stores the publishing block data in the Package Store\\PkgGUID\\VerGUID\\Root.</span></span>

        -   <span data-ttu-id="a5a64-554">Icônes: cibles de points d’extension.</span><span class="sxs-lookup"><span data-stu-id="a5a64-554">Icons: Targets of extension points.</span></span>

        -   <span data-ttu-id="a5a64-555">En-têtes d’exécutable portables (en-têtes PE): cibles de points d’extension qui contiennent les informations de base relatives à l’image nécessaires sur le disque, accessibles directement ou via des types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a5a64-555">Portable Executable Headers (PE Headers): Targets of extension points that contain the base information about the image need on disk, directly accessed or via file types.</span></span>

        -   <span data-ttu-id="a5a64-556">Scripts: Télécharger le répertoire scripts à utiliser tout au long du processus de publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-556">Scripts: Download scripts directory for use throughout the publishing process.</span></span>

    4.  <span data-ttu-id="a5a64-557">Peuplez le magasin de packages:</span><span class="sxs-lookup"><span data-stu-id="a5a64-557">Populate the Package store:</span></span>

        1.  <span data-ttu-id="a5a64-558">Créez des fichiers épars sur le disque qui représentent le package extrait pour les répertoires répertoriés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-558">Create sparse files on disk that represent the extracted package for any directories listed.</span></span>

        2.  <span data-ttu-id="a5a64-559">Déphasez les fichiers et répertoires de niveau supérieur sous racine.</span><span class="sxs-lookup"><span data-stu-id="a5a64-559">Stage top level files and directories under root.</span></span>

        3.  <span data-ttu-id="a5a64-560">Tous les autres fichiers sont créés lorsque le répertoire est répertorié comme incomplet sur le disque et en flux à la demande.</span><span class="sxs-lookup"><span data-stu-id="a5a64-560">All other files are created when the directory is listed as sparse on disk and streamed on demand.</span></span>

    5.  <span data-ttu-id="a5a64-561">Créer des entrées de catalogue d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-561">Create the machine catalog entries.</span></span> <span data-ttu-id="a5a64-562">Créez le Manifest.xml et le DeploymentConfiguration.xml des fichiers du package (si aucun fichier DeploymentConfiguration.xml du package n’est créé).</span><span class="sxs-lookup"><span data-stu-id="a5a64-562">Create the Manifest.xml and DeploymentConfiguration.xml from the package files (if no DeploymentConfiguration.xml file in the package a placeholder is created).</span></span>

    6.  <span data-ttu-id="a5a64-563">Créer l’emplacement du magasin de packages dans le HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog Registre</span><span class="sxs-lookup"><span data-stu-id="a5a64-563">Create location of the package store in the registry HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span></span>

    7.  <span data-ttu-id="a5a64-564">Créer le fichier Registry. dat à partir du Windows Store vers%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat</span><span class="sxs-lookup"><span data-stu-id="a5a64-564">Create the Registry.dat file from the package store to %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat</span></span>

    8.  <span data-ttu-id="a5a64-565">Inscrire le package avec le pilote en mode noyau App-V HKLM\\Microsoft\\Software\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="a5a64-565">Register the package with the App-V Kernel Mode Driver HKLM\\Microsoft\\Software\\AppV\\MAV</span></span>

    9.  <span data-ttu-id="a5a64-566">Appelez le script à partir du fichier AppxManifest.xml ou DeploymentConfig.xml pour le minutage d’ajout du package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-566">Invoke scripting from the AppxManifest.xml or DeploymentConfig.xml file for Package Add timing.</span></span>

4.  <span data-ttu-id="a5a64-567">Configurez les groupes de connexions en ajoutant et en activant ou en désactivant.</span><span class="sxs-lookup"><span data-stu-id="a5a64-567">Configure Connection Groups by adding and enabling or disabling.</span></span>

5.  <span data-ttu-id="a5a64-568">Supprimez les objets qui ne sont pas publiés sur la cible (utilisateur ou ordinateur).</span><span class="sxs-lookup"><span data-stu-id="a5a64-568">Remove objects that are not published to the target (user or machine).</span></span>

    <span data-ttu-id="a5a64-569">**Remarques**  Cette opération n’entraîne pas la suppression d’un package, mais la suppression de points d’intégration pour la cible spécifique (utilisateur ou ordinateur) et la suppression des fichiers de catalogue d’utilisateurs (fichiers de catalogue d’ordinateur pour une publication internationale).</span><span class="sxs-lookup"><span data-stu-id="a5a64-569">**Note** This will not perform a package deletion but rather remove integration points for the specific target (user or machine) and remove user catalog files (machine catalog files for globally published).</span></span>

     

6.  <span data-ttu-id="a5a64-570">Invoquez le montage de chargement en arrière-plan en fonction de la configuration du client.</span><span class="sxs-lookup"><span data-stu-id="a5a64-570">Invoke background load mounting based on client configuration.</span></span>

7.  <span data-ttu-id="a5a64-571">Les packages qui ont déjà des informations de publication pour l’ordinateur ou l’utilisateur sont immédiatement restaurés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-571">Packages that already have publishing information for the machine or user are immediately restored.</span></span>

    <span data-ttu-id="a5a64-572">**Remarques**  Cette condition est en tant que produit de suppression sans annuler la publication avec l’ajout en arrière-plan du package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-572">**Note** This condition occurs as a product of removal without unpublishing with background addition of the package.</span></span>

     

<span data-ttu-id="a5a64-573">Cela a pour fin un ajout de package App-V à la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-573">This completes an App-V package add of the publishing refresh process.</span></span> <span data-ttu-id="a5a64-574">L’étape suivante consiste à publier le package sur la cible spécifique (ordinateur ou utilisateur).</span><span class="sxs-lookup"><span data-stu-id="a5a64-574">The next step is publishing the package to the specific target (machine or user).</span></span>

![créer un fichier et des données de registre de package](images/packageaddfileandregistrydata.png)

### <span data-ttu-id="a5a64-576">Publication d’un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-576">Publishing an App-V package</span></span>

<span data-ttu-id="a5a64-577">Pendant l’opération d’actualisation de la publication, l’opération de publication spécifique (publication-AppVClientPackage) ajoute des entrées au catalogue d’utilisateurs, des cartes de habilitation pour l’utilisateur, identifie le magasin local et se termine en effectuant les étapes d’intégration.</span><span class="sxs-lookup"><span data-stu-id="a5a64-577">During the Publishing Refresh operation, the specific publishing operation (Publish-AppVClientPackage) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span> <span data-ttu-id="a5a64-578">Les étapes suivantes sont détaillées.</span><span class="sxs-lookup"><span data-stu-id="a5a64-578">The following are the detailed steps.</span></span>

**<span data-ttu-id="a5a64-579">Publication d’un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-579">How to publish and App-V package</span></span>**

1.  <span data-ttu-id="a5a64-580">Des entrées de package sont ajoutées au catalogue utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-580">Package entries are added to the user catalog</span></span>

    1.  <span data-ttu-id="a5a64-581">Packages ciblés par l’utilisateur: le UserDeploymentConfiguration.xml et le UserManifest.xml sont placés sur l’ordinateur dans le catalogue de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-581">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the User Catalog</span></span>

    2.  <span data-ttu-id="a5a64-582">Packages d’ordinateur ciblé (Global): le UserDeploymentConfiguration.xml est placé dans le catalogue d’ordinateurs</span><span class="sxs-lookup"><span data-stu-id="a5a64-582">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the Machine Catalog</span></span>

2.  <span data-ttu-id="a5a64-583">Inscrire le package avec le pilote du mode noyau pour l’utilisateur sur HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="a5a64-583">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

3.  <span data-ttu-id="a5a64-584">Effectuer des tâches d’intégration.</span><span class="sxs-lookup"><span data-stu-id="a5a64-584">Perform integration tasks.</span></span>

    1.  <span data-ttu-id="a5a64-585">Créer des points d’extension.</span><span class="sxs-lookup"><span data-stu-id="a5a64-585">Create extension points.</span></span>

    2.  <span data-ttu-id="a5a64-586">Stocker les informations de sauvegarde dans le registre de l’utilisateur et le profil d’itinérance (sauvegardes de raccourci).</span><span class="sxs-lookup"><span data-stu-id="a5a64-586">Store backup information in the user’s registry and roaming profile (Shortcut Backups).</span></span>

        <span data-ttu-id="a5a64-587">**Remarques**  Cela permet de restaurer les points d’extension si le package n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="a5a64-587">**Note** This enables restore extension points if the package is unpublished.</span></span>

         

    3.  <span data-ttu-id="a5a64-588">Exécutez les scripts destinés au minutage de la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-588">Run scripts targeted for publishing timing.</span></span>

<span data-ttu-id="a5a64-589">La publication d’un package App-V qui fait partie d’un groupe de connexions est très similaire au processus ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a5a64-589">Publishing an App-V Package that is part of a Connection Group is very similar to the above process.</span></span> <span data-ttu-id="a5a64-590">Pour les groupes de connexion, le chemin d’accès qui stocke les informations de catalogue spécifiques inclut PackageGroups en tant qu’enfant du répertoire de catalogue.</span><span class="sxs-lookup"><span data-stu-id="a5a64-590">For connection groups, the path that stores the specific catalog information includes PackageGroups as a child of the Catalog Directory.</span></span> <span data-ttu-id="a5a64-591">Pour plus d’informations, consultez les informations du catalogue de l’ordinateur et des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-591">Review the machine and users catalog information above for details.</span></span>

![créer un fichier et des données de Registre globales du package](images/packageaddfileandregistrydata-global.png)

### <span data-ttu-id="a5a64-593">Lancement d’une application</span><span class="sxs-lookup"><span data-stu-id="a5a64-593">Application launch</span></span>

<span data-ttu-id="a5a64-594">Après le processus d’actualisation de publication, l’utilisateur lance, puis redémarre une application application-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-594">After the Publishing Refresh process, the user launches and subsequently re-launches an App-V application.</span></span> <span data-ttu-id="a5a64-595">Le processus est très simple et optimisé pour le lancement rapide avec un trafic réseau minimal.</span><span class="sxs-lookup"><span data-stu-id="a5a64-595">The process is very simple and optimized to launch quickly with a minimum of network traffic.</span></span> <span data-ttu-id="a5a64-596">Le client App-V vérifie le chemin d’accès au catalogue utilisateur pour les fichiers créés lors de la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-596">The App-V Client checks the path to the user catalog for files created during publishing.</span></span> <span data-ttu-id="a5a64-597">Une fois que les droits d’ouverture du package sont établis, le client App-V crée un environnement virtuel, commence à diffuser en continu les données nécessaires et applique les fichiers de configuration de manifeste et de déploiement appropriés lors de la création de l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="a5a64-597">After rights to launch the package are established, the App-V Client creates a virtual environment, begins streaming any necessary data, and applies the appropriate manifest and deployment configuration files during virtual environment creation.</span></span> <span data-ttu-id="a5a64-598">Après avoir créé et configuré l’environnement virtuel pour le package et l’application spécifiques, l’application démarre.</span><span class="sxs-lookup"><span data-stu-id="a5a64-598">With the virtual environment created and configured for the specific package and application, the application starts.</span></span>

**<span data-ttu-id="a5a64-599">Comment lancer des applications App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-599">How to launch App-V applications</span></span>**

1.  <span data-ttu-id="a5a64-600">Un utilisateur lance l’application en cliquant sur un raccourci ou un appel de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="a5a64-600">User launches the application by clicking on a shortcut or file type invocation.</span></span>

2.  <span data-ttu-id="a5a64-601">Le client App-V vérifie qu’il existe dans le catalogue utilisateur les fichiers suivants.</span><span class="sxs-lookup"><span data-stu-id="a5a64-601">The App-V Client verifies existence in the User Catalog for the following files</span></span>

    -   <span data-ttu-id="a5a64-602">UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-602">UserDeploymentConfiguration.xml</span></span>

    -   <span data-ttu-id="a5a64-603">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="a5a64-603">UserManifest.xml</span></span>

3.  <span data-ttu-id="a5a64-604">S’il s’agit d’un fichier, l’application est autorisée pour cet utilisateur et l’application démarre le processus pour le lancement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-604">If the files are present, the application is entitled for that specific user and the application will start the process for launch.</span></span> <span data-ttu-id="a5a64-605">Il n’y a pas de trafic réseau à ce stade.</span><span class="sxs-lookup"><span data-stu-id="a5a64-605">There is no network traffic at this point.</span></span>

4.  <span data-ttu-id="a5a64-606">Ensuite, le client App-V vérifie que le chemin d’accès du package enregistré pour le service client App-V est disponible dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a5a64-606">Next, the App-V Client checks that the path for the package registered for the App-V Client service is found in the registry.</span></span>

5.  <span data-ttu-id="a5a64-607">Lors de la recherche du chemin d’accès au magasin de packages, l’environnement virtuel est créé.</span><span class="sxs-lookup"><span data-stu-id="a5a64-607">Upon finding the path to the package store, the virtual environment is created.</span></span> <span data-ttu-id="a5a64-608">S’il s’agit du premier lancement, le bloc de fonctionnalité principal télécharge le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a5a64-608">If this is the first launch, the Primary Feature Block downloads if present.</span></span>

6.  <span data-ttu-id="a5a64-609">Après le téléchargement, le service client App-V utilise les fichiers de configuration de manifeste et de déploiement pour configurer l’environnement virtuel et tous les sous-systèmes App-V chargés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-609">After downloading, the App-V Client service consumes the manifest and deployment configuration files to configure the virtual environment and all App-V subsystems are loaded.</span></span>

7.  <span data-ttu-id="a5a64-610">L’application est lancée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-610">The Application launches.</span></span> <span data-ttu-id="a5a64-611">Dans le cas de tous les fichiers manquants du magasin de packages (fichiers fragmentés), l’application-V va provoquer une erreur de flux sur les fichiers selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="a5a64-611">For any missing files in the package store (sparse files), App-V will stream fault the files on an as needed basis.</span></span>

    ![fichier d’ajout de package et flux de données du Registre](images/packageaddfileandregistrydata-stream.png)

### <span data-ttu-id="a5a64-613">Mise à niveau d’un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-613">Upgrading an App-V package</span></span>

<span data-ttu-id="a5a64-614">Le processus de mise à niveau du package App-V 5 diffère de l’ancienne version de App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-614">The App-V 5 package upgrade process differs from the older versions of App-V.</span></span> <span data-ttu-id="a5a64-615">App-V prend en charge plusieurs versions du même package sur un ordinateur habilité à différents utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-615">App-V supports multiple versions of the same package on a machine entitled to different users.</span></span> <span data-ttu-id="a5a64-616">Les versions de package peuvent être ajoutées à tout moment, car le magasin de packages et les catalogues sont mis à jour avec les nouvelles ressources.</span><span class="sxs-lookup"><span data-stu-id="a5a64-616">Package versions can be added at any time as the package store and catalogs are updated with the new resources.</span></span> <span data-ttu-id="a5a64-617">Le seul processus spécifique à l’ajout de nouvelles ressources de version est l’optimisation du stockage.</span><span class="sxs-lookup"><span data-stu-id="a5a64-617">The only process specific to the addition of new version resources is storage optimization.</span></span> <span data-ttu-id="a5a64-618">Lors d’une mise à niveau, seuls les nouveaux fichiers sont ajoutés à la nouvelle position du magasin de versions et les liens durs sont créés pour les fichiers non modifiés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-618">During an upgrade, only the new files are added to the new version store location and hard links are created for unchanged files.</span></span> <span data-ttu-id="a5a64-619">Ainsi, le stockage global est réduit en ne présentant que le fichier à un emplacement sur le disque, puis en le projetant dans tous les dossiers avec une entrée d’emplacement du fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a5a64-619">This reduces the overall storage by only presenting the file on one disk location and then projecting it into all folders with a file location entry on the disk.</span></span> <span data-ttu-id="a5a64-620">Les détails spécifiques de la mise à niveau d’un package App-V sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="a5a64-620">The specific details of upgrading an App-V Package are as follows:</span></span>

**<span data-ttu-id="a5a64-621">Comment mettre à niveau un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-621">How to upgrade an App-V package</span></span>**

1.  <span data-ttu-id="a5a64-622">Le client App-V effectue une actualisation de publication et découvre une nouvelle version d’un package App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-622">The App-V Client performs a Publishing Refresh and discovers a newer version of an App-V Package.</span></span>

2.  <span data-ttu-id="a5a64-623">Des entrées de package sont ajoutées dans le catalogue approprié pour la nouvelle version</span><span class="sxs-lookup"><span data-stu-id="a5a64-623">Package entries are added to the appropriate catalog for the new version</span></span>

    1.  <span data-ttu-id="a5a64-624">Packages ciblés par l’utilisateur: le UserDeploymentConfiguration.xml et le UserManifest.xml sont placés sur l’ordinateur dans le catalogue utilisateur sur appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="a5a64-624">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the user catalog at appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

    2.  <span data-ttu-id="a5a64-625">Packages d’ordinateur ciblé (Global): le UserDeploymentConfiguration.xml est placé dans le catalogue d’ordinateurs sur%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="a5a64-625">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the machine catalog at %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

3.  <span data-ttu-id="a5a64-626">Inscrire le package avec le pilote du mode noyau pour l’utilisateur sur HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="a5a64-626">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

4.  <span data-ttu-id="a5a64-627">Effectuer des tâches d’intégration.</span><span class="sxs-lookup"><span data-stu-id="a5a64-627">Perform integration tasks.</span></span>

    -   <span data-ttu-id="a5a64-628">Intégrez les points d’extensions (EP) à partir du manifeste et des fichiers de configuration dynamiques.</span><span class="sxs-lookup"><span data-stu-id="a5a64-628">Integrate extensions points (EP) from the Manifest and Dynamic Configuration files.</span></span>

    1.  <span data-ttu-id="a5a64-629">Les données EP basées sur des fichiers sont stockées dans le dossier AppData à l’aide de points de jonction du magasin de packages.</span><span class="sxs-lookup"><span data-stu-id="a5a64-629">File based EP data is stored in the AppData folder utilizing Junction Points from the package store.</span></span>

    2.  <span data-ttu-id="a5a64-630">Le EPs version 1 existe déjà lorsqu’une nouvelle version est disponible.</span><span class="sxs-lookup"><span data-stu-id="a5a64-630">Version 1 EPs already exist when a new version becomes available.</span></span>

    3.  <span data-ttu-id="a5a64-631">Les points d’extension sont basculés vers l’emplacement version 2 dans les catalogues d’ordinateur ou d’utilisateur pour les points d’extension plus récents ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="a5a64-631">The extension points are switched to the Version 2 location in machine or user catalogs for any newer or updated extension points.</span></span>

5.  <span data-ttu-id="a5a64-632">Exécutez les scripts destinés au minutage de la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-632">Run scripts targeted for publishing timing.</span></span>

6.  <span data-ttu-id="a5a64-633">Installez les assemblys côte à côte selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="a5a64-633">Install Side by Side assemblies as required.</span></span>

### <span data-ttu-id="a5a64-634">Mise à niveau d’un package App-V d’application en cours d’utilisation</span><span class="sxs-lookup"><span data-stu-id="a5a64-634">Upgrading an in-use App-V package</span></span>

<span data-ttu-id="a5a64-635">À **partir de App-V 5 SP2**: Si vous tentez de mettre à niveau un package utilisé par un utilisateur final, la tâche de mise à niveau est placée dans un État en attente.</span><span class="sxs-lookup"><span data-stu-id="a5a64-635">**Starting in App-V 5 SP2**: If you try to upgrade a package that is in use by an end user, the upgrade task is placed in a pending state.</span></span> <span data-ttu-id="a5a64-636">La mise à niveau sera exécutée plus tard, conformément aux règles suivantes:</span><span class="sxs-lookup"><span data-stu-id="a5a64-636">The upgrade will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-637">Type de tâche</span><span class="sxs-lookup"><span data-stu-id="a5a64-637">Task type</span></span></th>
<th align="left"><span data-ttu-id="a5a64-638">Règle applicable</span><span class="sxs-lookup"><span data-stu-id="a5a64-638">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-639">Tâche basée sur l’utilisateur (par exemple, publication d’un package pour un utilisateur);</span><span class="sxs-lookup"><span data-stu-id="a5a64-639">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-640">La tâche en attente sera exécutée après que l’utilisateur se déconnecte, puis se reconnecte.</span><span class="sxs-lookup"><span data-stu-id="a5a64-640">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-641">Une tâche basée sur le monde (par exemple, l’activation globale d’un groupe de connexions);</span><span class="sxs-lookup"><span data-stu-id="a5a64-641">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-642">La tâche en attente sera effectuée lorsque l’ordinateur sera arrêté, puis redémarré.</span><span class="sxs-lookup"><span data-stu-id="a5a64-642">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a5a64-643">Lorsqu’une tâche est placée dans un état d’attente, le client App-V génère également une clé de Registre pour la tâche en attente, comme suit:</span><span class="sxs-lookup"><span data-stu-id="a5a64-643">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-644">Tâche basée sur le niveau utilisateur ou global</span><span class="sxs-lookup"><span data-stu-id="a5a64-644">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="a5a64-645">Emplacement de génération de la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="a5a64-645">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-646">Tâches basées sur l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-646">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-647">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="a5a64-647">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-648">Tâches globalement basées</span><span class="sxs-lookup"><span data-stu-id="a5a64-648">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-649">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="a5a64-649">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a5a64-650">Les opérations suivantes doivent être effectuées pour que les utilisateurs puissent utiliser la version la plus récente du package:</span><span class="sxs-lookup"><span data-stu-id="a5a64-650">The following operations must be completed before users can use the newer version of the package:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-651">Tâche</span><span class="sxs-lookup"><span data-stu-id="a5a64-651">Task</span></span></th>
<th align="left"><span data-ttu-id="a5a64-652">Détails</span><span class="sxs-lookup"><span data-stu-id="a5a64-652">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-653">Ajouter le package à l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-653">Add the package to the computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-654">Cette tâche est spécifique à un ordinateur et vous pouvez l’exécuter à tout moment en suivant les étapes décrites dans la section Ajouter un package ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a5a64-654">This task is computer specific and you can perform it at any time by completing the steps in the Package Add section above.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-655">Publier le package</span><span class="sxs-lookup"><span data-stu-id="a5a64-655">Publish the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-656">Pour connaître les étapes à suivre, voir la section publication de package ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a5a64-656">See the Package Publishing section above for steps.</span></span> <span data-ttu-id="a5a64-657">Ce processus nécessite la mise à jour des points d’extension sur le système.</span><span class="sxs-lookup"><span data-stu-id="a5a64-657">This process requires that you update extension points on the system.</span></span> <span data-ttu-id="a5a64-658">Les utilisateurs finaux ne peuvent pas utiliser l’application une fois cette tâche terminée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-658">End users cannot be using the application when you complete this task.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a5a64-659">Utilisez les scénarios d’exemples suivants comme guide pour la mise à jour des packages.</span><span class="sxs-lookup"><span data-stu-id="a5a64-659">Use the following example scenarios as a guide for updating packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-660">Scénario</span><span class="sxs-lookup"><span data-stu-id="a5a64-660">Scenario</span></span></th>
<th align="left"><span data-ttu-id="a5a64-661">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5a64-661">Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-662">Le package App-V n’est pas utilisé lorsque vous essayez de procéder à la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="a5a64-662">App-V package is not in use when you try to upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-663">Aucun des composants suivants du package ne peut être utilisé: application virtuelle, serveur COM ou extensions d’interpréteur de commande.</span><span class="sxs-lookup"><span data-stu-id="a5a64-663">None of the following components of the package can be in use: virtual application, COM server, or shell extensions.</span></span></p>
<p><span data-ttu-id="a5a64-664">L’administrateur publie une nouvelle version du package et la mise à niveau fonctionne lors du lancement suivant d’un composant ou d’une application dans le package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-664">The administrator publishes a newer version of the package and the upgrade works the next time a component or application inside the package is launched.</span></span> <span data-ttu-id="a5a64-665">La nouvelle version du package est diffusée et exécutée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-665">The new version of the package is streamed and run.</span></span> <span data-ttu-id="a5a64-666">Aucune modification n’a été apportée dans ce scénario dans App-V 5 SP2 à partir des versions précédentes de App-V 5.</span><span class="sxs-lookup"><span data-stu-id="a5a64-666">Nothing has changed in this scenario in App-V 5 SP2 from previous releases of App-V 5.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-667">Le package App-V est en cours d’utilisation lorsque l’administrateur publie une nouvelle version du package</span><span class="sxs-lookup"><span data-stu-id="a5a64-667">App-V package is in use when the administrator publishes a newer version of the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-668">L’opération de mise à niveau est définie sur en attente par le client App-V, ce qui signifie qu’elle est mise en file d’attente et exécutée ultérieurement lorsque le package n’est pas en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-668">The upgrade operation is set to pending by the App-V Client, which means that it is queued and carried out later when the package is not in use.</span></span></p>
<p><span data-ttu-id="a5a64-669">Si l’application de package est utilisée, l’utilisateur ferme l’application virtuelle à l’issue de laquelle la mise à niveau peut avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="a5a64-669">If the package application is in use, the user shuts down the virtual application, after which the upgrade can occur.</span></span></p>
<p><span data-ttu-id="a5a64-670">Si le package dispose d’extensions d’interpréteur de charge (Office 2013), qui sont chargées définitivement par l’Explorateur Windows, l’utilisateur ne peut pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="a5a64-670">If the package has shell extensions (Office 2013), which are permanently loaded by Windows Explorer, the user cannot be logged in.</span></span> <span data-ttu-id="a5a64-671">Les utilisateurs doivent se déconnecter, puis se reconnecter pour lancer la mise à niveau du package App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-671">Users must log off and the log back in to initiate the App-V package upgrade.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a5a64-672">Publication globale et par utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-672">Global vs user publishing</span></span>

<span data-ttu-id="a5a64-673">Les packages App-V peuvent être publiés de l’une des deux manières suivantes: Utilisateur qui s’applique à un package App-V à un utilisateur ou à un groupe d’utilisateurs spécifiques et au monde qui applique le package App-V à l’ensemble de l’ordinateur pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-673">App-V Packages can be published in one of two ways; User which entitles an App-V package to a specific user or group of users and Global which entitles the App-V package to the entire machine for all users of the machine.</span></span> <span data-ttu-id="a5a64-674">Dès qu’une mise à niveau de package est en attente et que le package App-V n’est pas en cours d’utilisation, considérez les deux types de publication:</span><span class="sxs-lookup"><span data-stu-id="a5a64-674">Once a package upgrade has been pended and the App-V package is not in use, consider the two types of publishing:</span></span>

-   <span data-ttu-id="a5a64-675">**Publiées globalement**: l’application est publiée sur un ordinateur; tous les utilisateurs de cet ordinateur peuvent l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="a5a64-675">**Globally published**: the application is published to a machine; all users on that machine can use it.</span></span> <span data-ttu-id="a5a64-676">La mise à niveau aura lieu lorsque le service client App-V démarre, ce qui signifie qu’un redémarrage de l’ordinateur est efficace.</span><span class="sxs-lookup"><span data-stu-id="a5a64-676">The upgrade will happen when the App-V Client Service starts, which effectively means a machine restart.</span></span>

-   <span data-ttu-id="a5a64-677">**Utilisateur publié**: l’application est publiée à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-677">**User published**: the application is published to a user.</span></span> <span data-ttu-id="a5a64-678">S’il existe plusieurs utilisateurs sur l’ordinateur, l’application peut être publiée dans un sous-ensemble d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-678">If there are multiple users on the machine, the application can be published to a subset of the users.</span></span> <span data-ttu-id="a5a64-679">La mise à niveau se produit lorsque l’utilisateur se connecte ou qu’il est à nouveau publié (périodiquement, l’actualisation de la stratégie ConfigMgr et son évaluation, ou une mise à jour ou une actualisation périodique de l’application).</span><span class="sxs-lookup"><span data-stu-id="a5a64-679">The upgrade will happen when the user logs in or when it is published again (periodically, ConfigMgr Policy refresh and evaluation, or an App-V periodic publishing/refresh, or explicitly via PowerShell commands).</span></span>

### <span data-ttu-id="a5a64-680">Suppression d’un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-680">Removing an App-V package</span></span>

<span data-ttu-id="a5a64-681">La suppression d’applications App-V dans une infrastructure complète est une opération de dépublication qui n’effectue pas de suppression de package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-681">Removing App-V applications in a Full Infrastructure is an unpublish operation, and does not perform a package removal.</span></span> <span data-ttu-id="a5a64-682">Le processus est le même que le processus de publication ci-dessus, mais au lieu d’ajouter le processus de suppression inverse les modifications apportées pour les packages App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-682">The process is the same as the publish process above, but instead of adding the removal process reverses the changes that have been made for App-V Packages.</span></span>

### <span data-ttu-id="a5a64-683">Réparation d’un package App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-683">Repairing an App-V package</span></span>

<span data-ttu-id="a5a64-684">L’opération de réparation est très simple, mais peut affecter de nombreux emplacements sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-684">The repair operation is very simple but may affect many locations on the machine.</span></span> <span data-ttu-id="a5a64-685">Le cliché mentionné précédemment lors de l’écriture (vache) est supprimé et les points d’extension sont désintégrés, puis intégrés à nouveau.</span><span class="sxs-lookup"><span data-stu-id="a5a64-685">The previously mentioned Copy on Write (COW) locations are removed, and extension points are de-integrated and then re-integrated.</span></span> <span data-ttu-id="a5a64-686">Veuillez consulter les emplacements de placement des données de COW en passant en revue les emplacements enregistrés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a5a64-686">Please review the COW data placement locations by reviewing where they are registered in the registry.</span></span> <span data-ttu-id="a5a64-687">Cette opération s’effectue automatiquement et il n’y a pas de contrôle d’administration à l’origine d’une opération de réparation à partir de la console cliente App-V ou via PowerShell (réparation-AppVClientPackage).</span><span class="sxs-lookup"><span data-stu-id="a5a64-687">This operation is done automatically and there is no administrative control other than initiating a Repair operation from the App-V Client Console or via PowerShell (Repair-AppVClientPackage).</span></span>

## <a href="" id="bkmk-integr-appv-pkgs"></a><span data-ttu-id="a5a64-688">Intégration des packages App-V</span><span class="sxs-lookup"><span data-stu-id="a5a64-688">Integration of App-V packages</span></span>


<span data-ttu-id="a5a64-689">Le client et l’architecture du package App-V fournissent une intégration spécifique au système d’exploitation local lors de l’ajout et de la publication de packages.</span><span class="sxs-lookup"><span data-stu-id="a5a64-689">The App-V Client and package architecture provides specific integration with the local operating system during the addition and publishing of packages.</span></span> <span data-ttu-id="a5a64-690">Trois fichiers définissent les points d’intégration ou d’extension d’un package App-V:</span><span class="sxs-lookup"><span data-stu-id="a5a64-690">Three files define the integration or extension points for an App-V Package:</span></span>

-   <span data-ttu-id="a5a64-691">AppXManifest.xml: stockées à l’intérieur du package avec des copies de secours stockées dans le magasin de packages et le profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-691">AppXManifest.xml: Stored inside of the package with fallback copies stored in the package store and the user profile.</span></span> <span data-ttu-id="a5a64-692">Contient les options créées lors du processus de séquençage.</span><span class="sxs-lookup"><span data-stu-id="a5a64-692">Contains the options created during the sequencing process.</span></span>

-   <span data-ttu-id="a5a64-693">DeploymentConfig.xml: fournit des informations de configuration pour les points d’extension d’intégration basés sur les ordinateurs et les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-693">DeploymentConfig.xml: Provides configuration information of computer and user based integration extension points.</span></span>

-   <span data-ttu-id="a5a64-694">UserConfig.xml: sous-ensemble de l' Deploymentconfig.xml qui fournit uniquement des configurations utilisateur et cibles uniquement aux points d’extension utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-694">UserConfig.xml: A subset of the Deploymentconfig.xml that only provides user- based configurations and only targets user-based extension points.</span></span>

### <span data-ttu-id="a5a64-695">Règles d’intégration</span><span class="sxs-lookup"><span data-stu-id="a5a64-695">Rules of integration</span></span>

<span data-ttu-id="a5a64-696">Lorsque les applications App-V sont publiées sur un ordinateur avec le client App-V, certaines actions spécifiques se produisent comme décrit dans la liste ci-dessous:</span><span class="sxs-lookup"><span data-stu-id="a5a64-696">When App-V applications are published to a computer with the App-V Client, some specific actions take place as described in the list below:</span></span>

-   <span data-ttu-id="a5a64-697">Publication globale: les raccourcis sont stockés dans l’emplacement du profil de tous les utilisateurs et d’autres points d’extension sont stockés dans le registre dans la ruche HKLM.</span><span class="sxs-lookup"><span data-stu-id="a5a64-697">Global Publishing: Shortcuts are stored in the All Users profile location and other extension points are stored in the registry in the HKLM hive.</span></span>

-   <span data-ttu-id="a5a64-698">Publication des utilisateurs: les raccourcis sont stockés dans le profil de compte d’utilisateur actuel et d’autres points d’extension sont stockés dans le registre dans la ruche HKCU.</span><span class="sxs-lookup"><span data-stu-id="a5a64-698">User Publishing: Shortcuts are stored in the current user account profile and other extension points are stored in the registry in the HKCU hive.</span></span>

-   <span data-ttu-id="a5a64-699">Sauvegarde et restauration: les données d’application natives existantes et le registre (par exemple, les inscriptions FTA) sont sauvegardés lors de la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-699">Backup and Restore: Existing native application data and registry (such as FTA registrations) are backed up during publishing.</span></span>

    1.  <span data-ttu-id="a5a64-700">La propriété des packages App-V est attribuée en fonction du dernier package intégré pour lequel la propriété est transmise à la dernière application publiée par l’application.</span><span class="sxs-lookup"><span data-stu-id="a5a64-700">App-V packages are given ownership based on the last integrated package where the ownership is passed to the newest published App-V application.</span></span>

    2.  <span data-ttu-id="a5a64-701">Le transfert de propriété d’un package App-V à un autre lorsque le package App-V propriétaire n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="a5a64-701">Ownership transfers from one App-V package to another when the owning App-V package is unpublished.</span></span> <span data-ttu-id="a5a64-702">Cette opération n’entraîne pas de restauration des données et du Registre.</span><span class="sxs-lookup"><span data-stu-id="a5a64-702">This will not initiate a restore of the data or registry.</span></span>

    3.  <span data-ttu-id="a5a64-703">Restaurez les données sauvegardées lorsque le dernier package n’est pas publié ou supprimé par point d’extension.</span><span class="sxs-lookup"><span data-stu-id="a5a64-703">Restore the backed up data when the last package is unpublished or removed on a per extension point basis.</span></span>

### <span data-ttu-id="a5a64-704">Points d’extension</span><span class="sxs-lookup"><span data-stu-id="a5a64-704">Extension points</span></span>

<span data-ttu-id="a5a64-705">Les fichiers de publication App-V (manifeste et configuration dynamique) fournissent plusieurs points d’extension permettant à l’application d’être intégré au système d’exploitation local.</span><span class="sxs-lookup"><span data-stu-id="a5a64-705">The App-V publishing files (manifest and dynamic configuration) provide several extension points that enable the application to integrate with the local operating system.</span></span> <span data-ttu-id="a5a64-706">Ces points d’extension effectuent des tâches standard d’installation des applications, telles que le placement de raccourcis, la création d’associations de types de fichiers et l’inscription des composants.</span><span class="sxs-lookup"><span data-stu-id="a5a64-706">These extension points perform typical application installation tasks, such as placing shortcuts, creating file type associations, and registering components.</span></span> <span data-ttu-id="a5a64-707">Étant donné qu’il s’agit d’applications virtualisées qui ne sont pas installées de la même manière qu’une application traditionnelle, il existe des différences.</span><span class="sxs-lookup"><span data-stu-id="a5a64-707">As these are virtualized applications that are not installed in the same manner a traditional application, there are some differences.</span></span> <span data-ttu-id="a5a64-708">La liste suivante répertorie les points d’extension abordés dans cette section:</span><span class="sxs-lookup"><span data-stu-id="a5a64-708">The following is a list of extension points covered in this section:</span></span>

-   <span data-ttu-id="a5a64-709">Associés</span><span class="sxs-lookup"><span data-stu-id="a5a64-709">Shortcuts</span></span>

-   <span data-ttu-id="a5a64-710">Associations de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="a5a64-710">File Type Associations</span></span>

-   <span data-ttu-id="a5a64-711">Extensions d’environnement</span><span class="sxs-lookup"><span data-stu-id="a5a64-711">Shell Extensions</span></span>

-   <span data-ttu-id="a5a64-712">MODÈLE</span><span class="sxs-lookup"><span data-stu-id="a5a64-712">COM</span></span>

-   <span data-ttu-id="a5a64-713">Clients logiciels</span><span class="sxs-lookup"><span data-stu-id="a5a64-713">Software Clients</span></span>

-   <span data-ttu-id="a5a64-714">Fonctionnalités des applications</span><span class="sxs-lookup"><span data-stu-id="a5a64-714">Application capabilities</span></span>

-   <span data-ttu-id="a5a64-715">Gestionnaire de protocole d’URL</span><span class="sxs-lookup"><span data-stu-id="a5a64-715">URL Protocol Handler</span></span>

-   <span data-ttu-id="a5a64-716">AppPath</span><span class="sxs-lookup"><span data-stu-id="a5a64-716">AppPath</span></span>

-   <span data-ttu-id="a5a64-717">Application virtuelle</span><span class="sxs-lookup"><span data-stu-id="a5a64-717">Virtual Application</span></span>

### <span data-ttu-id="a5a64-718">Associés</span><span class="sxs-lookup"><span data-stu-id="a5a64-718">Shortcuts</span></span>

<span data-ttu-id="a5a64-719">Le raccourci est l’un des éléments de base de l’intégration avec le système d’exploitation et est l’interface pour le lancement d’une application application V directe par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-719">The short cut is one of the basic elements of integration with the OS and is the interface for direct user launch of an App-V application.</span></span> <span data-ttu-id="a5a64-720">Lors de la publication et de la dépublication des applications App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-720">During the publishing and unpublishing of App-V applications.</span></span>

<span data-ttu-id="a5a64-721">À partir du manifeste du package et des fichiers XML de configuration dynamique, le chemin d’accès au fichier exécutable d’une application spécifique se trouve dans une section semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="a5a64-721">From the package manifest and dynamic configuration XML files, the path to a specific application executable can be found in a section similar to the following:</span></span>

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

<span data-ttu-id="a5a64-722">Comme indiqué précédemment, les raccourcis de l’application-V sont placés par défaut dans le profil de l’utilisateur en fonction de l’opération d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-722">As mentioned previously, the App-V shortcuts are placed by default in the user’s profile based on the refresh operation.</span></span> <span data-ttu-id="a5a64-723">Actualisation globale place les raccourcis dans le profil tous les utilisateurs et l’actualisation des utilisateurs dans le profil de l’utilisateur concerné.</span><span class="sxs-lookup"><span data-stu-id="a5a64-723">Global refresh places shortcuts in the All Users profile and user refresh stores them in the specific user’s profile.</span></span> <span data-ttu-id="a5a64-724">Le fichier exécutable réel est stocké dans le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a5a64-724">The actual executable is stored in the Package Store.</span></span> <span data-ttu-id="a5a64-725">L’emplacement du fichier ICO est un emplacement sous-jeton dans le package App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-725">The location of the ICO file is a tokenized location in the App-V package.</span></span>

### <span data-ttu-id="a5a64-726">Associations de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="a5a64-726">File type associations</span></span>

<span data-ttu-id="a5a64-727">Le client App-V gère les associations de types de fichiers du système d’exploitation local lors de la publication, ce qui permet aux utilisateurs d’utiliser des appels de type de fichier ou d’ouvrir un fichier à l’aide d’une extension spécifiquement inscrite (. docx) pour démarrer une application application-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-727">The App-V Client manages the local operating system File Type Associations during publishing, which enables users to use file type invocations or to open a file with a specifically registered extension (.docx) to start an App-V application.</span></span> <span data-ttu-id="a5a64-728">Des associations de types de fichiers sont disponibles dans les fichiers de configuration de manifeste et de configuration dynamique, comme illustré dans l’exemple ci-dessous:</span><span class="sxs-lookup"><span data-stu-id="a5a64-728">File type associations are present in the manifest and dynamic configuration files as represented in the example below:</span></span>

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

<span data-ttu-id="a5a64-729">**Remarques**  Dans cet exemple:</span><span class="sxs-lookup"><span data-stu-id="a5a64-729">**Note** In this example:</span></span>

-   `<Name>.xdp</Name>` <span data-ttu-id="a5a64-730">est l’extension</span><span class="sxs-lookup"><span data-stu-id="a5a64-730">is the extension</span></span>

-   `<Name>AcroExch.XDPDoc</Name>` <span data-ttu-id="a5a64-731">est la valeur ProgId (qui pointe vers l’ID de PROG adjacent)</span><span class="sxs-lookup"><span data-stu-id="a5a64-731">is the ProgId value (which points to the adjoining ProgId)</span></span>

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` <span data-ttu-id="a5a64-732">est la ligne de commande, qui pointe vers l’exécutable de l’application</span><span class="sxs-lookup"><span data-stu-id="a5a64-732">is the command line, which points to the application executable</span></span>

 

### <span data-ttu-id="a5a64-733">Extensions d'environnement</span><span class="sxs-lookup"><span data-stu-id="a5a64-733">Shell extensions</span></span>

<span data-ttu-id="a5a64-734">Les extensions d’interpréteur sont incorporées automatiquement dans le package lors du processus de séquençage.</span><span class="sxs-lookup"><span data-stu-id="a5a64-734">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="a5a64-735">Lorsque le package est publié globalement, l’extension de l’interpréteur de Shell donne aux utilisateurs les mêmes fonctionnalités que si l’application a été installée localement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-735">When the package is published globally, the shell extension gives users the same functionality as if the application were locally installed.</span></span> <span data-ttu-id="a5a64-736">L’application ne nécessite aucune installation ou configuration supplémentaire sur le client pour activer la fonctionnalité d’extension du shell.</span><span class="sxs-lookup"><span data-stu-id="a5a64-736">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

**<span data-ttu-id="a5a64-737">Configuration requise pour l’utilisation des extensions d’interpréteur de tâches:</span><span class="sxs-lookup"><span data-stu-id="a5a64-737">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="a5a64-738">Les packages contenant des extensions d’interpréteur de Troie doivent être publiés globalement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-738">Packages that contain embedded shell extensions must be published globally.</span></span>

-   <span data-ttu-id="a5a64-739">Le nombre de bits d’application, de Sequencer et de client App-V doit correspondre ou les extensions de Shell ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="a5a64-739">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="a5a64-740">Exemple:</span><span class="sxs-lookup"><span data-stu-id="a5a64-740">For example:</span></span>

    -   <span data-ttu-id="a5a64-741">La version de l’application est 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a5a64-741">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="a5a64-742">Le Sequencer s’exécute sur un ordinateur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a5a64-742">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="a5a64-743">Le package est remis à un ordinateur client d’application 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a5a64-743">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="a5a64-744">Le tableau suivant répertorie les extensions d’environnement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a5a64-744">The following table displays the supported shell extensions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-745">Gestionnaire d'</span><span class="sxs-lookup"><span data-stu-id="a5a64-745">Handler</span></span></th>
<th align="left"><span data-ttu-id="a5a64-746">Description</span><span class="sxs-lookup"><span data-stu-id="a5a64-746">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-747">Gestionnaire de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="a5a64-747">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-748">Ajoute des éléments de menu dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="a5a64-748">Adds menu items to the context menu.</span></span> <span data-ttu-id="a5a64-749">Il est appelé avant que le menu contextuel ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a5a64-749">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-750">Gestionnaire de glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="a5a64-750">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-751">Contrôle l’action dès que vous cliquez avec le bouton droit sur un glisser-déplacer, puis modifie le menu contextuel qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a5a64-751">Controls the action upon right-click drag-and-drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-752">Supprimer le gestionnaire de cibles</span><span class="sxs-lookup"><span data-stu-id="a5a64-752">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-753">Contrôle l’action après le glissement et la suppression d’un objet de données sur une cible de dépôt telle qu’un fichier.</span><span class="sxs-lookup"><span data-stu-id="a5a64-753">Controls the action after a data object is dragged-and-dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-754">Gestionnaire d’objets de données</span><span class="sxs-lookup"><span data-stu-id="a5a64-754">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-755">Contrôle l’action après la copie d’un fichier dans le presse-papiers ou le glisser-déplacer sur une cible de déplacement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-755">Controls the action after a file is copied to the clipboard or dragged-and-dropped over a drop target.</span></span> <span data-ttu-id="a5a64-756">Il peut fournir des formats de presse-papiers supplémentaires à la cible de dépôt.</span><span class="sxs-lookup"><span data-stu-id="a5a64-756">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-757">Gestionnaire de feuilles de propriétés</span><span class="sxs-lookup"><span data-stu-id="a5a64-757">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-758">Remplace ou ajoute des pages dans la boîte de dialogue feuille de propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="a5a64-758">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-759">Gestionnaire d’info-bulle</span><span class="sxs-lookup"><span data-stu-id="a5a64-759">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-760">Permet de récupérer les indicateurs et les informations de l’info-bulle d’un élément et de l’afficher dans une info-bulle contextuelle lors du survol de la souris.</span><span class="sxs-lookup"><span data-stu-id="a5a64-760">Allows retrieving flags and infotip information for an item and displaying it inside a popup tooltip upon mouse- hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-761">Gestionnaire de colonnes</span><span class="sxs-lookup"><span data-stu-id="a5a64-761">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-762">Autorise la création et l’affichage de colonnes personnalisées dans l’affichage détaillé de l’Explorateur Windows <em> </em> .</span><span class="sxs-lookup"><span data-stu-id="a5a64-762">Allows creating and displaying custom columns in Windows Explorer <em>Details view</em>.</span></span> <span data-ttu-id="a5a64-763">Elle peut être utilisée pour étendre le tri et le regroupement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-763">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-764">Gestionnaire d’aperçu</span><span class="sxs-lookup"><span data-stu-id="a5a64-764">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-765">Permet d’afficher un aperçu d’un fichier dans le volet de visualisation de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="a5a64-765">Enables a preview of a file to be displayed in the Windows Explorer Preview Pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a5a64-766">MODÈLE</span><span class="sxs-lookup"><span data-stu-id="a5a64-766">COM</span></span>

<span data-ttu-id="a5a64-767">Le client App-V prend en charge la publication d’applications grâce à la prise en charge de l’intégration COM et de la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-767">The App-V Client supports publishing applications with support for COM integration and virtualization.</span></span> <span data-ttu-id="a5a64-768">L’intégration COM permet au client App-V d’inscrire des objets COM sur le système d’exploitation local et la virtualisation des objets.</span><span class="sxs-lookup"><span data-stu-id="a5a64-768">COM integration allows the App-V Client to register COM objects on the local operating system and virtualization of the objects.</span></span> <span data-ttu-id="a5a64-769">Dans le cadre de ce document, l’intégration d’objets COM nécessite des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a5a64-769">For the purposes of this document, the integration of COM objects requires additional detail.</span></span>

<span data-ttu-id="a5a64-770">App-V prend en charge l’enregistrement d’objets COM du package sur le système d’exploitation local avec deux types de processus: hors processus et in-process.</span><span class="sxs-lookup"><span data-stu-id="a5a64-770">App-V supports registering COM objects from the package to the local operating system with two process types: Out-of-process and in-process.</span></span> <span data-ttu-id="a5a64-771">L’enregistrement d’objets COM s’effectue à l’aide d’un ou de plusieurs modes d’opération pour un package App-V spécifique incluant désactivé, isolé et intégré.</span><span class="sxs-lookup"><span data-stu-id="a5a64-771">Registering COM objects is accomplished with one or a combination of multiple modes of operation for a specific App-V package that includes off, Isolated, and Integrated.</span></span> <span data-ttu-id="a5a64-772">Le mode intégré est configuré pour le type hors processus ou in-process.</span><span class="sxs-lookup"><span data-stu-id="a5a64-772">The integrated mode is configured for either the out-of-process or in-process type.</span></span> <span data-ttu-id="a5a64-773">La configuration des types et modes COM s’effectue à l’aide des fichiers de configuration dynamiques (deploymentconfig.xml ou userconfig.xml).</span><span class="sxs-lookup"><span data-stu-id="a5a64-773">Configuration of COM modes and types is accomplished with dynamic configuration files (deploymentconfig.xml or userconfig.xml).</span></span>

<span data-ttu-id="a5a64-774">Des informations sur l’intégration d’App-V sont disponibles à l’adresse suivante: <https://go.microsoft.com/fwlink/?LinkId=392834> .</span><span class="sxs-lookup"><span data-stu-id="a5a64-774">Details on App-V integration are available at: <https://go.microsoft.com/fwlink/?LinkId=392834>.</span></span>

### <span data-ttu-id="a5a64-775">Clients logiciels et fonctionnalités d’application</span><span class="sxs-lookup"><span data-stu-id="a5a64-775">Software clients and application capabilities</span></span>

<span data-ttu-id="a5a64-776">App-V prend en charge des clients logiciels et des points d’extension de fonctionnalités d’application spécifiques qui permettent aux applications virtualisées d’être inscrites auprès du client logiciel du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-776">App-V supports specific software clients and application capabilities extension points that enable virtualized applications to be registered with the software client of the operating system.</span></span> <span data-ttu-id="a5a64-777">Cela permet aux utilisateurs de sélectionner des programmes par défaut pour les opérations telles que la messagerie, la messagerie instantanée et le lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="a5a64-777">This enables users to select default programs for operations like email, instant messaging, and media player.</span></span> <span data-ttu-id="a5a64-778">Cette opération est effectuée dans le panneau de configuration avec les valeurs par défaut de l’accès au programme et aux paramètres d’ordinateur, puis configurées lors du séquençage dans les fichiers de configuration de manifeste ou dynamiques.</span><span class="sxs-lookup"><span data-stu-id="a5a64-778">This operation is performed in the control panel with the Set Program Access and Computer Defaults, and configured during sequencing in the manifest or dynamic configuration files.</span></span> <span data-ttu-id="a5a64-779">Les fonctionnalités d’application sont uniquement prises en charge lorsque les applications App-V sont publiées globalement.</span><span class="sxs-lookup"><span data-stu-id="a5a64-779">Application capabilities are only supported when the App-V applications are published globally.</span></span>

<span data-ttu-id="a5a64-780">Exemple d’inscription d’un client de messagerie application par le logiciel</span><span class="sxs-lookup"><span data-stu-id="a5a64-780">Example of software client registration of an App-V based mail client.</span></span>

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

<span data-ttu-id="a5a64-781">**Remarques**  Dans cet exemple:</span><span class="sxs-lookup"><span data-stu-id="a5a64-781">**Note** In this example:</span></span>

-   `<ClientConfiguration EmailEnabled="true" />` <span data-ttu-id="a5a64-782">est le paramètre global des clients logiciels pour intégrer les clients de messagerie</span><span class="sxs-lookup"><span data-stu-id="a5a64-782">is the overall Software Clients setting to integrate Email clients</span></span>

-   `<EMail MakeDefault="true">` <span data-ttu-id="a5a64-783">est l’indicateur permettant de définir un client de messagerie particulier en tant que client de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="a5a64-783">is the flag to set a particular Email client as the default Email client</span></span>

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` <span data-ttu-id="a5a64-784">est l’inscription de la dll MAPI</span><span class="sxs-lookup"><span data-stu-id="a5a64-784">is the MAPI dll registration</span></span>

 

### <span data-ttu-id="a5a64-785">Gestionnaire de protocole d’URL</span><span class="sxs-lookup"><span data-stu-id="a5a64-785">URL Protocol handler</span></span>

<span data-ttu-id="a5a64-786">Les applications ne sont pas toujours appelées applications virtuelles à l’aide d’un appel de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="a5a64-786">Applications do not always specifically called virtualized applications utilizing file type invocation.</span></span> <span data-ttu-id="a5a64-787">Par exemple, dans une application qui prend en charge l’incorporation d’un lien mailto: à l’intérieur d’un document ou d’une page Web, l’utilisateur clique sur un lien mailto: et attend qu’il dispose d’un client de messagerie enregistré.</span><span class="sxs-lookup"><span data-stu-id="a5a64-787">For, example, in an application that supports embedding a mailto: link inside a document or web page, the user clicks on a mailto: link and expects to get their registered mail client.</span></span> <span data-ttu-id="a5a64-788">App-V prend en charge les gestionnaires de protocole d’URL qui peuvent être inscrits en fonction de chaque package avec le système d’exploitation local.</span><span class="sxs-lookup"><span data-stu-id="a5a64-788">App-V supports URL Protocol handlers that can be registered on a per-package basis with the local operating system.</span></span> <span data-ttu-id="a5a64-789">Lors du séquençage, les gestionnaires de protocole d’URL sont automatiquement ajoutés au package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-789">During sequencing, the URL protocol handlers are automatically added to the package.</span></span>

<span data-ttu-id="a5a64-790">Dans le cas où plusieurs applications peuvent inscrire le gestionnaire de protocole d’URL spécifique, les fichiers de configuration dynamique peuvent être utilisés pour modifier le comportement et supprimer ou désactiver cette fonctionnalité pour une application qui ne doit pas être lancée.</span><span class="sxs-lookup"><span data-stu-id="a5a64-790">For situations where there is more than one application that could register the specific URL Protocol handler, the dynamic configuration files can be utilized to modify the behavior and suppress or disable this feature for an application that should not be the primary application launched.</span></span>

### <span data-ttu-id="a5a64-791">AppPath</span><span class="sxs-lookup"><span data-stu-id="a5a64-791">AppPath</span></span>

<span data-ttu-id="a5a64-792">Le point d’extension AppPath prend en charge l’appel des applications App-V directement à partir du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-792">The AppPath extension point supports calling App-V applications directly from the operating system.</span></span> <span data-ttu-id="a5a64-793">Pour ce faire, vous devez généralement effectuer cette opération à partir de l’écran de démarrage ou d’ouverture, en fonction du système d’exploitation, qui permet aux administrateurs de fournir un accès aux applications App-V à partir de commandes ou de scripts du système d’exploitation sans appeler le chemin d’accès spécifique au fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="a5a64-793">This is typically accomplished from the Run or Start Screen, depending on the operating system, which enables administrators to provide access to App-V applications from operating system commands or scripts without calling the specific path to the executable.</span></span> <span data-ttu-id="a5a64-794">Par conséquent, il n’est pas nécessaire de modifier la variable d’environnement de chemin d’accès système sur tous les systèmes, car elle est effectuée lors de la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-794">It therefore avoids modifying the system path environment variable on all systems, as it is accomplished during publishing.</span></span>

<span data-ttu-id="a5a64-795">Le point d’extension AppPath est configuré dans le manifeste ou dans les fichiers de configuration dynamique et est stocké dans le registre de l’ordinateur local lors de la publication de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-795">The AppPath extension point is configured either in the manifest or in the dynamic configuration files and is stored in the registry on the local machine during publishing for the user.</span></span> <span data-ttu-id="a5a64-796">Pour plus d’informations sur la révision de AppPath: <https://go.microsoft.com/fwlink/?LinkId=392835> .</span><span class="sxs-lookup"><span data-stu-id="a5a64-796">For additional information on AppPath review: <https://go.microsoft.com/fwlink/?LinkId=392835>.</span></span>

### <span data-ttu-id="a5a64-797">Application virtuelle</span><span class="sxs-lookup"><span data-stu-id="a5a64-797">Virtual application</span></span>

<span data-ttu-id="a5a64-798">Ce sous-système fournit une liste des applications capturées lors du séquençage qui sont généralement consommées par d’autres composants App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-798">This subsystem provides a list of applications captured during sequencing which is usually consumed by other App-V components.</span></span> <span data-ttu-id="a5a64-799">L’intégration de points d’extension qui appartiennent à une application particulière peut être désactivée à l’aide de fichiers de configuration dynamiques.</span><span class="sxs-lookup"><span data-stu-id="a5a64-799">Integration of extension points belonging to a particular application can be disabled using dynamic configuration files.</span></span> <span data-ttu-id="a5a64-800">Par exemple, dans le cas d’un package contenant deux applications, il est possible de désactiver tous les points d’extension d’une application afin de permettre uniquement l’intégration de points d’extension d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="a5a64-800">For example, if a package contains two applications, it is possible to disable all extension points belonging to one application, in order to allow only integration of extension points of other application.</span></span>

### <span data-ttu-id="a5a64-801">Règles de point d’extension</span><span class="sxs-lookup"><span data-stu-id="a5a64-801">Extension point rules</span></span>

<span data-ttu-id="a5a64-802">Les points d’extension décrits ci-dessus sont intégrés au système d’exploitation en fonction de la façon dont les packages ont été publiés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-802">The extension points described above are integrated into the operating system based on how the packages has been published.</span></span> <span data-ttu-id="a5a64-803">La publication globale place les points d’extension dans les emplacements des machines publiques, où la publication des utilisateurs place des points d’extension dans les emplacements des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a5a64-803">Global publishing places extension points in public machine locations, where user publishing places extension points in user locations.</span></span> <span data-ttu-id="a5a64-804">Par exemple, un raccourci qui est créé sur le bureau et publié globalement aura pour effet de générer le raccourci (%Public%\\Desktop) et les données de Registre (HKLM\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="a5a64-804">For example a shortcut that is created on the desktop and published globally will result in the file data for the shortcut (%Public%\\Desktop) and the registry data (HKLM\\Software\\Classes).</span></span> <span data-ttu-id="a5a64-805">Le même raccourci aurait des données de fichier (%UserProfile%\\Desktop) et des données de Registre (HKCU\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="a5a64-805">The same shortcut would have file data (%UserProfile%\\Desktop) and registry data (HKCU\\Software\\Classes).</span></span>

<span data-ttu-id="a5a64-806">Les points d’extension ne sont pas tous publiés de la même façon, dans la mesure où certains points d’extension nécessitent une publication globale et d’autres le séquençage sur le système d’exploitation et l’architecture spécifiques où ils sont remis.</span><span class="sxs-lookup"><span data-stu-id="a5a64-806">Extension points are not all published the same way, where some extension points will require global publishing and others require sequencing on the specific operating system and architecture where they are delivered.</span></span> <span data-ttu-id="a5a64-807">Vous trouverez ci-dessous un tableau qui décrit ces deux règles clés.</span><span class="sxs-lookup"><span data-stu-id="a5a64-807">Below is a table that describes these two key rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5a64-808">Extension virtuelle</span><span class="sxs-lookup"><span data-stu-id="a5a64-808">Virtual Extension</span></span></th>
<th align="left"><span data-ttu-id="a5a64-809">Nécessite le séquençage du système d’exploitation cible</span><span class="sxs-lookup"><span data-stu-id="a5a64-809">Requires target OS Sequencing</span></span></th>
<th align="left"><span data-ttu-id="a5a64-810">Nécessite une publication globale</span><span class="sxs-lookup"><span data-stu-id="a5a64-810">Requires Global Publishing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-811">Raccourci</span><span class="sxs-lookup"><span data-stu-id="a5a64-811">Shortcut</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-812">Association de type de fichier</span><span class="sxs-lookup"><span data-stu-id="a5a64-812">File Type Association</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-813">Protocoles d’URL</span><span class="sxs-lookup"><span data-stu-id="a5a64-813">URL Protocols</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-814">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-814">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-815">AppPaths</span><span class="sxs-lookup"><span data-stu-id="a5a64-815">AppPaths</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-816">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-816">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-817">Mode COM</span><span class="sxs-lookup"><span data-stu-id="a5a64-817">COM Mode</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-818">Client logiciel</span><span class="sxs-lookup"><span data-stu-id="a5a64-818">Software Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-819">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-819">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-820">Fonctionnalités des applications</span><span class="sxs-lookup"><span data-stu-id="a5a64-820">Application Capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-821">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-821">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-822">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-822">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-823">Gestionnaire de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="a5a64-823">Context Menu Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-824">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-824">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-825">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-825">X</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-826">Gestionnaire de glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="a5a64-826">Drag-and-drop Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-827">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-827">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-828">Gestionnaire d’objets de données</span><span class="sxs-lookup"><span data-stu-id="a5a64-828">Data Object Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-829">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-829">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-830">Gestionnaire de feuilles de propriétés</span><span class="sxs-lookup"><span data-stu-id="a5a64-830">Property Sheet Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-831">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-831">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-832">Gestionnaire d’info-bulle</span><span class="sxs-lookup"><span data-stu-id="a5a64-832">Infotip Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-833">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-833">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-834">Gestionnaire de colonnes</span><span class="sxs-lookup"><span data-stu-id="a5a64-834">Column Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-835">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-835">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-836">Extensions d’environnement</span><span class="sxs-lookup"><span data-stu-id="a5a64-836">Shell Extensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-837">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-837">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5a64-838">Objet d’assistance du navigateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-838">Browser Helper Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-839">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-839">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-840">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-840">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5a64-841">Objet Active X</span><span class="sxs-lookup"><span data-stu-id="a5a64-841">Active X Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-842">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-842">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5a64-843">X</span><span class="sxs-lookup"><span data-stu-id="a5a64-843">X</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a><span data-ttu-id="a5a64-844">Traitement dynamique des configurations</span><span class="sxs-lookup"><span data-stu-id="a5a64-844">Dynamic configuration processing</span></span>


<span data-ttu-id="a5a64-845">Le déploiement de packages App-V sur un ordinateur ou un utilisateur est très simple.</span><span class="sxs-lookup"><span data-stu-id="a5a64-845">Deploying App-V packages to one machine or user is very simple.</span></span> <span data-ttu-id="a5a64-846">Toutefois, au fur et à mesure que des organisations déploient des applications AppV sur des lignes métiers et des frontières géographiques et politiques, la possibilité de séquencer une application une seule fois avec un ensemble de paramètres devient impossible.</span><span class="sxs-lookup"><span data-stu-id="a5a64-846">However, as organizations deploy AppV applications across business lines and geographic and political boundaries, the ability to sequence an application one time with one set of settings becomes impossible.</span></span> <span data-ttu-id="a5a64-847">App-V a été conçu pour ce scénario, au fur et à mesure de la capture de paramètres et configurations spécifiques lors du séquençage dans le fichier manifeste, mais également de la modification de fichiers de configuration dynamique.</span><span class="sxs-lookup"><span data-stu-id="a5a64-847">App-V was designed for this scenario, as it captures specific settings and configurations during sequencing in the Manifest file, but also supports modification with Dynamic Configuration files.</span></span>

<span data-ttu-id="a5a64-848">La configuration dynamique App-V permet de spécifier une stratégie pour un package au niveau de l’ordinateur ou au niveau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-848">App-V dynamic configuration allows for specifying a policy for a package either at the machine level or at the user level.</span></span> <span data-ttu-id="a5a64-849">Les fichiers de configuration dynamiques permettent aux ingénieurs de séquençage de modifier la configuration d’un package, après le séquençage, afin de répondre aux besoins des groupes d’utilisateurs ou de machines individuels.</span><span class="sxs-lookup"><span data-stu-id="a5a64-849">The Dynamic Configuration files enable sequencing engineers to modify the configuration of a package, post-sequencing, to address the needs of individual groups of users or machines.</span></span> <span data-ttu-id="a5a64-850">Dans certains cas, il est possible que les modifications apportées à l’application fournissent des fonctionnalités appropriées au sein de l’environnement App-V.</span><span class="sxs-lookup"><span data-stu-id="a5a64-850">In some instances it may be necessary to make modifications to the application to provide proper functionality within the App-V environment.</span></span> <span data-ttu-id="a5a64-851">Par exemple, il se peut qu’il soit nécessaire de modifier les fichiers \ _ \ \* config.xml pour permettre l’exécution de certaines actions à une heure spécifique au cours de l’exécution de l’application, par exemple, la désactivation d’une extension mailto pour empêcher une application virtualisée de remplacer cette extension par une autre application.</span><span class="sxs-lookup"><span data-stu-id="a5a64-851">For example, it may be necessary to make modifications to the \_\*config.xml files to allow certain actions to be performed at a specified time during the execution of the application, like disabling a mailto extension to prevent a virtualized application from overwriting that extension from another application.</span></span>

<span data-ttu-id="a5a64-852">Les packages App-V contiennent le fichier manifeste dans le fichier de package AppV, qui est représentatif des opérations de séquençage et est la stratégie de choix à moins que les fichiers de configuration dynamique ne soient assignés à un package spécifique.</span><span class="sxs-lookup"><span data-stu-id="a5a64-852">App-V Packages contain the Manifest file inside of the appv package file, which is representative of sequencing operations and is the policy of choice unless Dynamic Configuration files are assigned to a specific package.</span></span> <span data-ttu-id="a5a64-853">Après le séquençage, les fichiers de configuration dynamique peuvent être modifiés pour permettre la publication d’une application sur des ordinateurs de bureau ou des utilisateurs différents.</span><span class="sxs-lookup"><span data-stu-id="a5a64-853">Post-sequencing, the Dynamic Configuration files can be modified to allow the publishing of an application to different desktops or users with different extension points.</span></span> <span data-ttu-id="a5a64-854">Les deux fichiers de configuration dynamiques sont les fichiers de configuration de déploiement dynamique (DDC) et de configuration de l’utilisateur dynamique (DUC).</span><span class="sxs-lookup"><span data-stu-id="a5a64-854">The two Dynamic Configuration Files are the Dynamic Deployment Configuration (DDC) and Dynamic User Configuration (DUC) files.</span></span> <span data-ttu-id="a5a64-855">Cette section porte sur la combinaison des fichiers de configuration de manifeste et de configuration dynamique.</span><span class="sxs-lookup"><span data-stu-id="a5a64-855">This section focuses on the combination of the manifest and dynamic configuration files.</span></span>

### <span data-ttu-id="a5a64-856">Exemple pour les fichiers de configuration dynamiques</span><span class="sxs-lookup"><span data-stu-id="a5a64-856">Example for dynamic configuration files</span></span>

<span data-ttu-id="a5a64-857">L’exemple ci-dessous montre la combinaison du manifeste, de la configuration du déploiement et des fichiers de configuration utilisateur après la publication et l’opération normale.</span><span class="sxs-lookup"><span data-stu-id="a5a64-857">The example below shows the combination of the Manifest, Deployment Configuration and User Configuration files after publishing and during normal operation.</span></span> <span data-ttu-id="a5a64-858">Ces exemples sont des exemples abrégés de chacun des fichiers.</span><span class="sxs-lookup"><span data-stu-id="a5a64-858">These examples are abbreviated examples of each of the files.</span></span> <span data-ttu-id="a5a64-859">L’objectif est de montrer la combinaison des fichiers uniquement et de ne pas être une description complète des catégories spécifiques disponibles dans chacun des fichiers.</span><span class="sxs-lookup"><span data-stu-id="a5a64-859">The purpose is show the combination of the files only and not to be a complete description of the specific categories available in each of the files.</span></span> <span data-ttu-id="a5a64-860">Pour plus d’informations, reportez-vous au Guide de séquençage de l’App-V 5 à l’adresse suivante:</span><span class="sxs-lookup"><span data-stu-id="a5a64-860">For more information review the App-V 5 Sequencing Guide at:</span></span> <https://go.microsoft.com/fwlink/?LinkID=269810>

**<span data-ttu-id="a5a64-861">Manifeste</span><span class="sxs-lookup"><span data-stu-id="a5a64-861">Manifest</span></span>**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**<span data-ttu-id="a5a64-862">Configuration du déploiement</span><span class="sxs-lookup"><span data-stu-id="a5a64-862">Deployment Configuration</span></span>**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**<span data-ttu-id="a5a64-863">Configuration utilisateur</span><span class="sxs-lookup"><span data-stu-id="a5a64-863">User Configuration</span></span>**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a><span data-ttu-id="a5a64-864">Assemblys côte à côte</span><span class="sxs-lookup"><span data-stu-id="a5a64-864">Side-by-side assemblies</span></span>


<span data-ttu-id="a5a64-865">App-V prend en charge l’emballage automatique d’assemblys côte à côte (SxS) lors du séquençage et du déploiement sur le client lors de la publication d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="a5a64-865">App-V supports the automatic packaging of side-by-side (SxS) assemblies during sequencing and deployment on the client during virtual application publishing.</span></span> <span data-ttu-id="a5a64-866">App-V 5 SP2 prend en charge la capture d’assemblys SxS lors du séquençage pour les assemblys non présents sur l’ordinateur de séquençage.</span><span class="sxs-lookup"><span data-stu-id="a5a64-866">App-V 5 SP2 supports capturing SxS assemblies during sequencing for assemblies not present on the sequencing machine.</span></span> <span data-ttu-id="a5a64-867">Quant aux assemblys qui se composent de Visual C++ (version 8 et version ultérieure) et/ou du runtime MSXML, le Sequencer détectera et capturera automatiquement ces dépendances, même si celles-ci n’ont pas été installées lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a5a64-867">And for assemblies consisting of Visual C++ (Version 8 and newer) and/or MSXML run-time, the Sequencer will automatically detect and capture these dependencies even if they were not installed during monitoring.</span></span> <span data-ttu-id="a5a64-868">La fonctionnalité d’assemblys côte à côte supprime les limitations relatives aux versions précédentes d’App-V, car le Sequencer App-V n’a pas pu capturer les assemblys déjà présents sur la station de travail de séquençage et en privatisation les assemblys limités à une version de bit par package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-868">The Side by Side assemblies feature removes the limitations of previous versions of App-V, where the App-V Sequencer did not capture assemblies already present on the sequencing workstation, and privatizing the assemblies which limited to one bit version per package.</span></span> <span data-ttu-id="a5a64-869">Ce comportement entraînait le déploiement d’applications App-V pour les clients ayant manquant les assemblys SxS requis, provoquant des échecs de lancement d’applications.</span><span class="sxs-lookup"><span data-stu-id="a5a64-869">This behavior resulted in deployed App-V applications to clients missing the required SxS assemblies, causing application launch failures.</span></span> <span data-ttu-id="a5a64-870">Cela forcé le processus d’empaquetage de document, puis de s’assurer que tous les assemblys requis pour les packages étaient installés localement sur le système d’exploitation client de l’utilisateur pour garantir la prise en charge des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="a5a64-870">This forced the packaging process to document and then ensure that all assemblies required for packages were locally installed on the user’s client operating system to ensure support for the virtual applications.</span></span> <span data-ttu-id="a5a64-871">En fonction du nombre d’assemblys et de la documentation de l’application associée aux dépendances requises, cette tâche était une demande de gestion et d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-871">Based on the number of assemblies and the lack of application documentation for the required dependencies, this task was both a management and implementation challenge.</span></span>

<span data-ttu-id="a5a64-872">La prise en charge des assemblys côte à côte dans App-V comporte les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="a5a64-872">Side by Side Assembly support in App-V has the following features.</span></span>

-   <span data-ttu-id="a5a64-873">Capture automatique de l’assembly SxS lors du séquençage, qu’il s’agisse d’un assembly ou d’un assembly déjà installé sur la station de travail de séquençage.</span><span class="sxs-lookup"><span data-stu-id="a5a64-873">Automatic captures of SxS assembly during Sequencing, regardless of whether the assembly was already installed on the sequencing workstation.</span></span>

-   <span data-ttu-id="a5a64-874">Le client App-V installe automatiquement les assemblys SxS requis sur l’ordinateur client au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="a5a64-874">The App-V Client automatically installs required SxS assemblies to the client computer at publishing time when they are not present.</span></span>

-   <span data-ttu-id="a5a64-875">Le Sequencer signale la dépendance au moment de l’exécution VC dans le mécanisme de création de rapports de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a5a64-875">The Sequencer reports the VC run-time dependency in Sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="a5a64-876">Le Sequencer autorise ne pas empaqueter les assemblys déjà installés sur le Sequencer, qui prennent en charge les scénarios dans lesquels les assemblys ont déjà été installés sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="a5a64-876">The Sequencer allows opting to not package the assemblies that are already installed on the Sequencer, supporting scenarios where the assemblies have previously been installed on the target computers.</span></span>

### <span data-ttu-id="a5a64-877">Publication automatique d’assemblys SxS</span><span class="sxs-lookup"><span data-stu-id="a5a64-877">Automatic publishing of SxS assemblies</span></span>

<span data-ttu-id="a5a64-878">Lors de la publication d’un package App-V avec des assemblys SxS, le client App-V vérifie la présence de l’assembly sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-878">During publishing of an App-V package with SxS assemblies the App-V Client will check for the presence of the assembly on the machine.</span></span> <span data-ttu-id="a5a64-879">S’il n’existe pas, le client déploie l’assembly vers l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a5a64-879">If the assembly does not exist, the client will deploy the assembly to the machine.</span></span> <span data-ttu-id="a5a64-880">Les packages qui font partie des groupes de connexion dépendent des installations d’assemblys côte à côte qui font partie des packages de base, car le groupe de connexion ne contient aucune information sur l’installation de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a5a64-880">Packages that are part of connection groups will rely on the Side by Side assembly installations that are part of the base packages, as the connection group does not contain any information about assembly installation.</span></span>

<span data-ttu-id="a5a64-881">**Remarques**  L’annulation de la publication ou de la suppression d’un package avec un assembly ne supprime pas les assemblys pour ce package.</span><span class="sxs-lookup"><span data-stu-id="a5a64-881">**Note** UnPublishing or removing a package with an assembly does not remove the assemblies for that package.</span></span>

 

## <a href="" id="bkmk-client-logging"></a><span data-ttu-id="a5a64-882">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="a5a64-882">Client logging</span></span>


<span data-ttu-id="a5a64-883">Le client App-V enregistre les informations dans le journal des événements Windows au format ETW standard.</span><span class="sxs-lookup"><span data-stu-id="a5a64-883">The App-V client logs information to the Windows Event log in standard ETW format.</span></span> <span data-ttu-id="a5a64-884">Pour plus d’informations, reportez-vous à l’observateur d’événements, sous applications et services Logs\\Microsoft\\AppV\\Client.</span><span class="sxs-lookup"><span data-stu-id="a5a64-884">The specific App-V events can be found in the event viewer, under Applications and Services Logs\\Microsoft\\AppV\\Client.</span></span>

<span data-ttu-id="a5a64-885">**Remarques**  Dans App-V 5,0 SP3, certains journaux ont été consolidés et déplacés vers l’emplacement suivant:</span><span class="sxs-lookup"><span data-stu-id="a5a64-885">**Note** In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span>

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

<span data-ttu-id="a5a64-886">Pour obtenir la liste des journaux déplacés, voir [à propos de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="a5a64-886">For a list of the moved logs, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

 

<span data-ttu-id="a5a64-887">Il existe trois catégories spécifiques d’événements enregistrés décrits ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a5a64-887">There are three specific categories of events recorded described below.</span></span>

<span data-ttu-id="a5a64-888">**Administrateur**: consigne les événements relatifs aux configurations appliquées au client App-V, et contient les principales erreurs et les avertissements.</span><span class="sxs-lookup"><span data-stu-id="a5a64-888">**Admin**: Logs events for configurations being applied to the App-V Client, and contains the primary warnings and errors.</span></span>

<span data-ttu-id="a5a64-889">**Opérationnel**: consigne l’exécution générale de l’application et l’utilisation des composants individuels créant un journal d’audit des opérations App-v exécutées sur le client App-v.</span><span class="sxs-lookup"><span data-stu-id="a5a64-889">**Operational**: Logs the general App-V execution and usage of individual components creating an audit log of the App-V operations that have been completed on the App-V Client.</span></span>

<span data-ttu-id="a5a64-890">**Application virtuelle**: consigne le lancement d’applications virtuelles et l’utilisation de sous-systèmes de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="a5a64-890">**Virtual Application**: Logs virtual application launches and use of virtualization subsystems.</span></span>






 

 






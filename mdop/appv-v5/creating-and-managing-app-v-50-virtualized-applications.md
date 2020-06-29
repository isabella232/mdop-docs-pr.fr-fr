---
title: Création et gestion d'applications virtualisées App-V5.0
description: Création et gestion d'applications virtualisées App-V5.0
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805923"
---
# <span data-ttu-id="ec267-103">Création et gestion d'applications virtualisées App-V5.0</span><span class="sxs-lookup"><span data-stu-id="ec267-103">Creating and Managing App-V 5.0 Virtualized Applications</span></span>


<span data-ttu-id="ec267-104">Une fois que vous avez correctement déployé le Sequencer Microsoft Application Virtualization (App-V) 5,0, vous pouvez l’utiliser pour surveiller et enregistrer le processus d’installation et de configuration pour qu’une application s’exécute en tant qu’application virtualisée.</span><span class="sxs-lookup"><span data-stu-id="ec267-104">After you have properly deployed the Microsoft Application Virtualization (App-V) 5.0 sequencer, you can use it to monitor and record the installation and setup process for an application to be run as a virtualized application.</span></span>

<span data-ttu-id="ec267-105">**Remarques**  Pour plus d’informations sur la configuration du Sequencer Microsoft Application Virtualization (App-V) 5,0, le séquençage des meilleures pratiques et un exemple de création et de mise à jour d’une application virtuelle, voir le Guide de mise en route de [Microsoft application virtualization 5,0](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5,0 séquençage Guide.docx).</span><span class="sxs-lookup"><span data-stu-id="ec267-105">**Note** For more information about configuring the Microsoft Application Virtualization (App-V) 5.0 sequencer, sequencing best practices, and an example of creating and updating a virtual application, see the [Microsoft Application Virtualization 5.0 Sequencing Guide](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) (https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx).</span></span>

 

## <span data-ttu-id="ec267-106">Séquençage d’une application</span><span class="sxs-lookup"><span data-stu-id="ec267-106">Sequencing an application</span></span>


<span data-ttu-id="ec267-107">Vous pouvez utiliser le Sequencer App-V 5,0 pour effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="ec267-107">You can use the App-V 5.0 Sequencer to perform the following tasks:</span></span>

-   <span data-ttu-id="ec267-108">Créer des packages virtuels qui peuvent être déployés sur des ordinateurs exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ec267-108">Create virtual packages that can be deployed to computers running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="ec267-109">Mettre à niveau des packages existants.</span><span class="sxs-lookup"><span data-stu-id="ec267-109">Upgrade existing packages.</span></span> <span data-ttu-id="ec267-110">Vous pouvez développer un package existant sur l’ordinateur exécutant le Sequencer, puis mettre à niveau l’application pour créer une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="ec267-110">You can expand an existing package onto the computer running the sequencer and then upgrade the application to create a newer version.</span></span>

-   <span data-ttu-id="ec267-111">Modifier les informations de configuration associées à un package existant.</span><span class="sxs-lookup"><span data-stu-id="ec267-111">Edit configuration information associated with an existing package.</span></span> <span data-ttu-id="ec267-112">Par exemple, vous pouvez ajouter un raccourci ou modifier une association de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="ec267-112">For example, you can add a shortcut or modify a file type association.</span></span>

    <span data-ttu-id="ec267-113">**Remarques**  Vous devez créer des raccourcis et les enregistrer dans un emplacement réseau disponible pour autoriser l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="ec267-113">**Note** You must create shortcuts and save them to an available network location to allow roaming.</span></span> <span data-ttu-id="ec267-114">Si un raccourci est créé et enregistré dans un emplacement privé, le package doit être publié localement sur l’ordinateur exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ec267-114">If a shortcut is created and saved in a private location, the package must be published locally to the computer running the App-V 5.0 client.</span></span>

     

-   <span data-ttu-id="ec267-115">Convertir des packages virtuels existants.</span><span class="sxs-lookup"><span data-stu-id="ec267-115">Convert existing virtual packages.</span></span>

<span data-ttu-id="ec267-116">Le Sequencer utilise le répertoire **% tmp% \ \ Scratch** ou **% TEMP% \ \ Scratch** , ainsi que **le répertoire temporaire pour** le stockage des fichiers temporaires lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="ec267-116">The sequencer uses the **%TMP% \\ Scratch** or **%TEMP% \\ Scratch** directory and the **Temp** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="ec267-117">Sur l’ordinateur qui exécute le Sequencer, vous devez configurer ces annuaires avec l’espace disque disponible correspondant à la configuration estimée requise pour l’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="ec267-117">On the computer that runs the sequencer, you should configure these directories with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="ec267-118">La configuration des répertoires temporaires et du répertoire temporaire sur différentes partitions de disque dur peut contribuer à améliorer les performances lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="ec267-118">Configuring the temp directories and the Temp directory on different hard drive partitions can help improve performance during sequencing.</span></span>

<span data-ttu-id="ec267-119">Lorsque vous utilisez le Sequencer pour créer une nouvelle application virtuelle, les fichiers répertoriés suivants sont créés.</span><span class="sxs-lookup"><span data-stu-id="ec267-119">When you use the sequencer to create a new virtual application, the following listed files are created.</span></span> <span data-ttu-id="ec267-120">Ces fichiers comprennent le package App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ec267-120">These files comprise the App-V 5.0 package.</span></span>

-   <span data-ttu-id="ec267-121">fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="ec267-121">.msi file.</span></span> <span data-ttu-id="ec267-122">Ce fichier Windows Installer (. msi) est créé par le Sequencer et est utilisé pour installer le package virtuel sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="ec267-122">This Windows Installer (.msi) file is created by the sequencer and is used to install the virtual package on target computers.</span></span>

-   <span data-ttu-id="ec267-123">Report.xml un fichier.</span><span class="sxs-lookup"><span data-stu-id="ec267-123">Report.xml file.</span></span> <span data-ttu-id="ec267-124">Dans ce fichier, le Sequencer enregistre tous les problèmes, avertissements et erreurs identifiés lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="ec267-124">In this file, the sequencer saves all issues, warnings, and errors that were discovered during sequencing.</span></span> <span data-ttu-id="ec267-125">Il affiche les informations après la création du package.</span><span class="sxs-lookup"><span data-stu-id="ec267-125">It displays the information after the package has been created.</span></span> <span data-ttu-id="ec267-126">Vous pouvez nous faire parvenir ce rapport pour détecter et résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="ec267-126">You can us this report for diagnosing and troubleshooting.</span></span>

-   <span data-ttu-id="ec267-127">fichier. AppV.</span><span class="sxs-lookup"><span data-stu-id="ec267-127">.appv file.</span></span> <span data-ttu-id="ec267-128">Il s’agit du fichier d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="ec267-128">This is the virtual application file.</span></span>

-   <span data-ttu-id="ec267-129">Fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="ec267-129">Deployment configuration file.</span></span> <span data-ttu-id="ec267-130">Le fichier de configuration de déploiement détermine la façon dont l’application virtuelle sera déployée sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="ec267-130">The deployment configuration file determines how the virtual application will be deployed to target computers.</span></span>

-   <span data-ttu-id="ec267-131">Fichier de configuration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec267-131">User configuration file.</span></span> <span data-ttu-id="ec267-132">Le fichier de configuration utilisateur détermine la façon dont l’application virtuelle s’exécute sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="ec267-132">The user configuration file determines how the virtual application will run on target computers.</span></span>

<span data-ttu-id="ec267-133">**Important**  Vous devez configurer les dossiers% TMP% et% TEMP% que le convertisseur de package utilise pour être sécurisé et l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ec267-133">**Important** You must configure the %TMP% and %TEMP% folders that the package converter uses to be a secure location and directory.</span></span> <span data-ttu-id="ec267-134">Un emplacement sécurisé est accessible uniquement par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="ec267-134">A secure location is only accessible by an administrator.</span></span> <span data-ttu-id="ec267-135">Par ailleurs, lorsque vous séquencez le package, vous devez enregistrer le package à un emplacement sécurisé ou vérifier qu’aucun autre utilisateur n’est autorisé à se connecter pendant le processus de conversion et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="ec267-135">Additionally, when you sequence the package you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion and monitoring process.</span></span>

 

<span data-ttu-id="ec267-136">La boîte de dialogue **options** de la console Sequencer contient les onglets suivants:</span><span class="sxs-lookup"><span data-stu-id="ec267-136">The **Options** dialog box in the sequencer console contains the following tabs:</span></span>

-   <span data-ttu-id="ec267-137">Informations **générales**.</span><span class="sxs-lookup"><span data-stu-id="ec267-137">**General**.</span></span> <span data-ttu-id="ec267-138">Utilisez cet onglet pour autoriser l’exécution des mises à jour de Microsoft lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="ec267-138">Use this tab to enable Microsoft Updates to run during sequencing.</span></span> <span data-ttu-id="ec267-139">Sélectionnez **Ajouter la version du package au nom du fichier** pour configurer la séquence pour ajouter un numéro de version au package virtualisé en cours de séquence.</span><span class="sxs-lookup"><span data-stu-id="ec267-139">Select **Append Package Version to Filename** to configure the sequence to add a version number to the virtualized package that is being sequenced.</span></span> <span data-ttu-id="ec267-140">Sélectionnez **toujours faire confiance à la source des accélérateurs de package** pour créer des packages virtualisés à l’aide d’un accélérateur de package sans être invité à procéder à une autorisation.</span><span class="sxs-lookup"><span data-stu-id="ec267-140">Select **Always trust the source of Package Accelerators** to create virtualized packages using a package accelerator without being prompted for authorization.</span></span>

    <span data-ttu-id="ec267-141">**Important**  Les accélérateurs de package créés à l’aide de App-V 4.6 ne sont pas pris en charge par App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ec267-141">**Important** Package Accelerators created using App-V4.6 are not supported by App-V 5.0.</span></span>

     

-   <span data-ttu-id="ec267-142">**Analyser des éléments**.</span><span class="sxs-lookup"><span data-stu-id="ec267-142">**Parse Items**.</span></span> <span data-ttu-id="ec267-143">Cet onglet affiche les emplacements de chemin d’accès de fichier associés qui seront analysés ou qui sont considérés comme étant dans l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="ec267-143">This tab displays the associated file path locations that will be parsed or tokenized into in the virtual environment.</span></span> <span data-ttu-id="ec267-144">Les jetons sont utiles pour ajouter des fichiers à l’aide de l’onglet **fichiers du package** dans **modification avancée**.</span><span class="sxs-lookup"><span data-stu-id="ec267-144">Tokens are useful for adding files using the **Package Files** tab in **Advanced Editing**.</span></span>

-   <span data-ttu-id="ec267-145">**Éléments d’exclusion**.</span><span class="sxs-lookup"><span data-stu-id="ec267-145">**Exclusion Items**.</span></span> <span data-ttu-id="ec267-146">Utilisez cet onglet pour spécifier quels dossiers et répertoires ne doivent pas être analysés lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="ec267-146">Use this tab to specify which folders and directories should not be monitored during sequencing.</span></span> <span data-ttu-id="ec267-147">Pour ajouter des données d’application locales enregistrées dans le dossier Data App local du package, cliquez sur **nouveau** , puis spécifiez l’emplacement et le **type de mappage**associé.</span><span class="sxs-lookup"><span data-stu-id="ec267-147">To add local application data that is saved in the Local App Data folder in the package, click **New** and specify the location and the associated **Mapping Type**.</span></span> <span data-ttu-id="ec267-148">Cette option est obligatoire pour certains packages.</span><span class="sxs-lookup"><span data-stu-id="ec267-148">This option is required for some packages.</span></span>

<span data-ttu-id="ec267-149">App-V 5,0 prend en charge les applications incluant des services Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ec267-149">App-V 5.0 supports applications that include Microsoft Windows Services.</span></span> <span data-ttu-id="ec267-150">Si une application inclut un service Windows, le service sera inclus dans le package virtuel séquencé tant qu’il est installé lors de la surveillance par le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="ec267-150">If an application includes a Windows service, the Service will be included in the sequenced virtual package as long as it is installed while being monitored by the sequencer.</span></span> <span data-ttu-id="ec267-151">Si une application virtuelle crée un service Windows lors de son exécution initiale, puis ultérieurement, après l’installation, l’application doit être exécutée pendant que le Sequencer analyse le fonctionnement du service Windows.</span><span class="sxs-lookup"><span data-stu-id="ec267-151">If a virtual application creates a Windows service when it initially runs, then later, after installation, the application must be run while the sequencer is monitoring so that the Windows Service will be added to the package.</span></span> <span data-ttu-id="ec267-152">Seuls les services exécutés sous le compte système local sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ec267-152">Only Services that run under the Local System account are supported.</span></span> <span data-ttu-id="ec267-153">Les services qui sont configurés pour le démarrage automatique ou le démarrage automatique retardé sont démarrés avant que la première application virtuelle d’un package s’exécute à l’intérieur de l’environnement virtuel du package.</span><span class="sxs-lookup"><span data-stu-id="ec267-153">Services that are configured for AutoStart or Delayed AutoStart are started before the first virtual application in a package runs inside the package’s Virtual Environment.</span></span> <span data-ttu-id="ec267-154">Les services Windows configurés pour être démarrés à la demande par une application sont démarrés lorsque l’application virtuelle à l’intérieur du package démarre le service via l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="ec267-154">Windows Services that are configured to be started on demand by an application are started when the virtual application inside the package starts the Service via API call.</span></span>

[<span data-ttu-id="ec267-155">Comment séquencer une nouvelle application avec App-V5.0</span><span class="sxs-lookup"><span data-stu-id="ec267-155">How to Sequence a New Application with App-V 5.0</span></span>](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> <span data-ttu-id="ec267-156">Prise en charge de l’extension Shell App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="ec267-156">App-V 5.0SP2 shell extension support</span></span>


<span data-ttu-id="ec267-157">App-V 5.0 SP2 prend en charge les extensions d’environnement.</span><span class="sxs-lookup"><span data-stu-id="ec267-157">App-V 5.0SP2 supports shell extensions.</span></span> <span data-ttu-id="ec267-158">Les extensions d’environnement seront détectées et incorporées dans le package lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="ec267-158">Shell extensions will be detected and embedded in the package during sequencing.</span></span>

<span data-ttu-id="ec267-159">Les extensions d’interpréteur sont incorporées automatiquement dans le package lors du processus de séquençage.</span><span class="sxs-lookup"><span data-stu-id="ec267-159">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="ec267-160">Lorsque le package est publié, l’extension d’interpréteur de Shell donne aux utilisateurs les mêmes fonctionnalités que si l’application a été installée localement.</span><span class="sxs-lookup"><span data-stu-id="ec267-160">When the package is published, the shell extension gives users the same functionality as if the application were locally installed.</span></span>

**<span data-ttu-id="ec267-161">Configuration requise pour l’utilisation des extensions d’interpréteur de tâches:</span><span class="sxs-lookup"><span data-stu-id="ec267-161">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="ec267-162">Les packages contenant des extensions d’interpréteur de Troie doivent être publiés globalement.</span><span class="sxs-lookup"><span data-stu-id="ec267-162">Packages that contain embedded shell extensions must be published globally.</span></span> <span data-ttu-id="ec267-163">L’application ne nécessite aucune installation ou configuration supplémentaire sur le client pour activer la fonctionnalité d’extension du shell.</span><span class="sxs-lookup"><span data-stu-id="ec267-163">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

-   <span data-ttu-id="ec267-164">Le nombre de bits d’application, de Sequencer et de client App-V doit correspondre ou les extensions de Shell ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="ec267-164">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="ec267-165">Exemple:</span><span class="sxs-lookup"><span data-stu-id="ec267-165">For example:</span></span>

    -   <span data-ttu-id="ec267-166">La version de l’application est 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ec267-166">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="ec267-167">Le Sequencer s’exécute sur un ordinateur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ec267-167">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="ec267-168">Le package est remis à un ordinateur client d’application 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ec267-168">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="ec267-169">Le tableau suivant répertorie les extensions d’environnement prises en charge:</span><span class="sxs-lookup"><span data-stu-id="ec267-169">The following table lists the supported shell extensions:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ec267-170">Gestionnaire d'</span><span class="sxs-lookup"><span data-stu-id="ec267-170">Handler</span></span></th>
<th align="left"><span data-ttu-id="ec267-171">Description</span><span class="sxs-lookup"><span data-stu-id="ec267-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec267-172">Gestionnaire de menu contextuel</span><span class="sxs-lookup"><span data-stu-id="ec267-172">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec267-173">Ajoute des éléments de menu dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ec267-173">Adds menu items to the context menu.</span></span> <span data-ttu-id="ec267-174">Il est appelé avant que le menu contextuel ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ec267-174">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec267-175">Gestionnaire de glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="ec267-175">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec267-176">Contrôle l’action en cliquant avec le bouton droit, puis en faisant glisser et en modifiant le menu contextuel qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ec267-176">Controls the action where right-click, drag and drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec267-177">Supprimer le gestionnaire de cibles</span><span class="sxs-lookup"><span data-stu-id="ec267-177">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec267-178">Contrôle l’action après le glissement et la suppression d’un objet de données sur une cible de dépôt telle qu’un fichier.</span><span class="sxs-lookup"><span data-stu-id="ec267-178">Controls the action after a data object is dragged and dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec267-179">Gestionnaire d’objets de données</span><span class="sxs-lookup"><span data-stu-id="ec267-179">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec267-180">Contrôle l’action après qu’un fichier est copié dans le presse-papiers ou glissé et déposé sur une cible de déplacement.</span><span class="sxs-lookup"><span data-stu-id="ec267-180">Controls the action after a file is copied to the clipboard or dragged and dropped over a drop target.</span></span> <span data-ttu-id="ec267-181">Il peut fournir des formats de presse-papiers supplémentaires à la cible de dépôt.</span><span class="sxs-lookup"><span data-stu-id="ec267-181">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec267-182">Gestionnaire de feuilles de propriétés</span><span class="sxs-lookup"><span data-stu-id="ec267-182">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec267-183">Remplace ou ajoute des pages dans la boîte de dialogue feuille de propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="ec267-183">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec267-184">Gestionnaire d’info-bulle</span><span class="sxs-lookup"><span data-stu-id="ec267-184">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec267-185">Permet de récupérer les indicateurs et les informations de l’info-bulle d’un élément et de l’afficher dans une info-bulle contextuelle lors du survol de la souris.</span><span class="sxs-lookup"><span data-stu-id="ec267-185">Allows retrieving flags and infotip information for an item and displaying it inside a pop-up tooltip upon mouse hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec267-186">Gestionnaire de colonnes</span><span class="sxs-lookup"><span data-stu-id="ec267-186">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec267-187">Autorise la création et l’affichage de colonnes personnalisées dans l' <strong> affichage détaillé de l’Explorateur Windows </strong> .</span><span class="sxs-lookup"><span data-stu-id="ec267-187">Allows creating and displaying custom columns in <strong>Windows Explorer Details view</strong>.</span></span> <span data-ttu-id="ec267-188">Elle peut être utilisée pour étendre le tri et le regroupement.</span><span class="sxs-lookup"><span data-stu-id="ec267-188">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec267-189">Gestionnaire d’aperçu</span><span class="sxs-lookup"><span data-stu-id="ec267-189">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec267-190">Permet d’afficher un aperçu d’un fichier dans le volet de visualisation de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="ec267-190">Enables a preview of a file to be displayed in the Windows Explorer Preview pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ec267-191">Extension de la prise en charge de l’extension de fichier</span><span class="sxs-lookup"><span data-stu-id="ec267-191">Copy on Write (CoW) file extension support</span></span>


<span data-ttu-id="ec267-192">Les extensions de fichier copie sur écriture (vache) permettent à l’application-V 5,0 d’écrire de manière dynamique sur des emplacements spécifiques contenus dans le package virtuel lors de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="ec267-192">Copy on write (CoW) file extensions allow App-V 5.0 to dynamically write to specific locations contained in the virtual package while it is being used.</span></span>

<span data-ttu-id="ec267-193">Le tableau suivant répertorie les types de fichiers qui peuvent exister dans un package virtuel sous le répertoire VFS, mais qui ne peuvent pas être mis à jour sur l’ordinateur exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ec267-193">The following table displays the file types that can exist in a virtual package under the VFS directory, but cannot be updated on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="ec267-194">Tous les autres fichiers et répertoires peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="ec267-194">All other files and directories can be modified.</span></span>

<span data-ttu-id="ec267-195">. acm</span><span class="sxs-lookup"><span data-stu-id="ec267-195">.acm</span></span>

<span data-ttu-id="ec267-196">. ASA</span><span class="sxs-lookup"><span data-stu-id="ec267-196">.asa</span></span>

<span data-ttu-id="ec267-197">.asp</span><span class="sxs-lookup"><span data-stu-id="ec267-197">.asp</span></span>

<span data-ttu-id="ec267-198">. aspx</span><span class="sxs-lookup"><span data-stu-id="ec267-198">.aspx</span></span>

<span data-ttu-id="ec267-199">. ax</span><span class="sxs-lookup"><span data-stu-id="ec267-199">.ax</span></span>

<span data-ttu-id="ec267-200">.bat</span><span class="sxs-lookup"><span data-stu-id="ec267-200">.bat</span></span>

<span data-ttu-id="ec267-201">.cer</span><span class="sxs-lookup"><span data-stu-id="ec267-201">.cer</span></span>

<span data-ttu-id="ec267-202">.chm</span><span class="sxs-lookup"><span data-stu-id="ec267-202">.chm</span></span>

<span data-ttu-id="ec267-203">. CLB</span><span class="sxs-lookup"><span data-stu-id="ec267-203">.clb</span></span>

<span data-ttu-id="ec267-204">.cmd</span><span class="sxs-lookup"><span data-stu-id="ec267-204">.cmd</span></span>

<span data-ttu-id="ec267-205">.cnt</span><span class="sxs-lookup"><span data-stu-id="ec267-205">.cnt</span></span>

<span data-ttu-id="ec267-206">. cnv</span><span class="sxs-lookup"><span data-stu-id="ec267-206">.cnv</span></span>

<span data-ttu-id="ec267-207">.com</span><span class="sxs-lookup"><span data-stu-id="ec267-207">.com</span></span>

<span data-ttu-id="ec267-208">.cpl</span><span class="sxs-lookup"><span data-stu-id="ec267-208">.cpl</span></span>

<span data-ttu-id="ec267-209">. CPX</span><span class="sxs-lookup"><span data-stu-id="ec267-209">.cpx</span></span>

<span data-ttu-id="ec267-210">.crt</span><span class="sxs-lookup"><span data-stu-id="ec267-210">.crt</span></span>

<span data-ttu-id="ec267-211">.dll</span><span class="sxs-lookup"><span data-stu-id="ec267-211">.dll</span></span>

<span data-ttu-id="ec267-212">.drv</span><span class="sxs-lookup"><span data-stu-id="ec267-212">.drv</span></span>

<span data-ttu-id="ec267-213">.exe</span><span class="sxs-lookup"><span data-stu-id="ec267-213">.exe</span></span>

<span data-ttu-id="ec267-214">.fon</span><span class="sxs-lookup"><span data-stu-id="ec267-214">.fon</span></span>

<span data-ttu-id="ec267-215">.grp</span><span class="sxs-lookup"><span data-stu-id="ec267-215">.grp</span></span>

<span data-ttu-id="ec267-216">.hlp</span><span class="sxs-lookup"><span data-stu-id="ec267-216">.hlp</span></span>

<span data-ttu-id="ec267-217">.hta</span><span class="sxs-lookup"><span data-stu-id="ec267-217">.hta</span></span>

<span data-ttu-id="ec267-218">. IME</span><span class="sxs-lookup"><span data-stu-id="ec267-218">.ime</span></span>

<span data-ttu-id="ec267-219">.inf</span><span class="sxs-lookup"><span data-stu-id="ec267-219">.inf</span></span>

<span data-ttu-id="ec267-220">.ins</span><span class="sxs-lookup"><span data-stu-id="ec267-220">.ins</span></span>

<span data-ttu-id="ec267-221">.isp</span><span class="sxs-lookup"><span data-stu-id="ec267-221">.isp</span></span>

<span data-ttu-id="ec267-222">. ses</span><span class="sxs-lookup"><span data-stu-id="ec267-222">.its</span></span>

<span data-ttu-id="ec267-223">.js</span><span class="sxs-lookup"><span data-stu-id="ec267-223">.js</span></span>

<span data-ttu-id="ec267-224">.jse</span><span class="sxs-lookup"><span data-stu-id="ec267-224">.jse</span></span>

<span data-ttu-id="ec267-225">.lnk</span><span class="sxs-lookup"><span data-stu-id="ec267-225">.lnk</span></span>

<span data-ttu-id="ec267-226">.msc</span><span class="sxs-lookup"><span data-stu-id="ec267-226">.msc</span></span>

<span data-ttu-id="ec267-227">.msi</span><span class="sxs-lookup"><span data-stu-id="ec267-227">.msi</span></span>

<span data-ttu-id="ec267-228">.msp</span><span class="sxs-lookup"><span data-stu-id="ec267-228">.msp</span></span>

<span data-ttu-id="ec267-229">.mst</span><span class="sxs-lookup"><span data-stu-id="ec267-229">.mst</span></span>

<span data-ttu-id="ec267-230">. mui</span><span class="sxs-lookup"><span data-stu-id="ec267-230">.mui</span></span>

<span data-ttu-id="ec267-231">. nls</span><span class="sxs-lookup"><span data-stu-id="ec267-231">.nls</span></span>

<span data-ttu-id="ec267-232">.ocx</span><span class="sxs-lookup"><span data-stu-id="ec267-232">.ocx</span></span>

<span data-ttu-id="ec267-233">. PAL</span><span class="sxs-lookup"><span data-stu-id="ec267-233">.pal</span></span>

<span data-ttu-id="ec267-234">.pcd</span><span class="sxs-lookup"><span data-stu-id="ec267-234">.pcd</span></span>

<span data-ttu-id="ec267-235">.pif</span><span class="sxs-lookup"><span data-stu-id="ec267-235">.pif</span></span>

<span data-ttu-id="ec267-236">.reg</span><span class="sxs-lookup"><span data-stu-id="ec267-236">.reg</span></span>

<span data-ttu-id="ec267-237">.scf</span><span class="sxs-lookup"><span data-stu-id="ec267-237">.scf</span></span>

<span data-ttu-id="ec267-238">.scr</span><span class="sxs-lookup"><span data-stu-id="ec267-238">.scr</span></span>

<span data-ttu-id="ec267-239">. SCT</span><span class="sxs-lookup"><span data-stu-id="ec267-239">.sct</span></span>

<span data-ttu-id="ec267-240">.shb</span><span class="sxs-lookup"><span data-stu-id="ec267-240">.shb</span></span>

<span data-ttu-id="ec267-241">.shs</span><span class="sxs-lookup"><span data-stu-id="ec267-241">.shs</span></span>

<span data-ttu-id="ec267-242">.sys</span><span class="sxs-lookup"><span data-stu-id="ec267-242">.sys</span></span>

<span data-ttu-id="ec267-243">. tlb</span><span class="sxs-lookup"><span data-stu-id="ec267-243">.tlb</span></span>

<span data-ttu-id="ec267-244">. tsp</span><span class="sxs-lookup"><span data-stu-id="ec267-244">.tsp</span></span>

<span data-ttu-id="ec267-245">.url</span><span class="sxs-lookup"><span data-stu-id="ec267-245">.url</span></span>

<span data-ttu-id="ec267-246">.vb</span><span class="sxs-lookup"><span data-stu-id="ec267-246">.vb</span></span>

<span data-ttu-id="ec267-247">.vbe</span><span class="sxs-lookup"><span data-stu-id="ec267-247">.vbe</span></span>

<span data-ttu-id="ec267-248">.vbs</span><span class="sxs-lookup"><span data-stu-id="ec267-248">.vbs</span></span>

<span data-ttu-id="ec267-249">.vsmacros</span><span class="sxs-lookup"><span data-stu-id="ec267-249">.vsmacros</span></span>

<span data-ttu-id="ec267-250">.ws</span><span class="sxs-lookup"><span data-stu-id="ec267-250">.ws</span></span>

<span data-ttu-id="ec267-251">. Échap</span><span class="sxs-lookup"><span data-stu-id="ec267-251">.esc</span></span>

<span data-ttu-id="ec267-252">.wsf</span><span class="sxs-lookup"><span data-stu-id="ec267-252">.wsf</span></span>

<span data-ttu-id="ec267-253">.wsh</span><span class="sxs-lookup"><span data-stu-id="ec267-253">.wsh</span></span>

 

## <span data-ttu-id="ec267-254">Modification d’un package d’application virtuelle existant</span><span class="sxs-lookup"><span data-stu-id="ec267-254">Modifying an existing virtual application package</span></span>


<span data-ttu-id="ec267-255">Vous pouvez utiliser le Sequencer pour modifier un package existant.</span><span class="sxs-lookup"><span data-stu-id="ec267-255">You can use the sequencer to modify an existing package.</span></span> <span data-ttu-id="ec267-256">L’ordinateur sur lequel vous procédez ainsi doit correspondre à l’architecture de processeur de l’ordinateur que vous avez utilisé pour créer l’application.</span><span class="sxs-lookup"><span data-stu-id="ec267-256">The computer on which you do this should match the chip architecture of the computer you used to create the application.</span></span> <span data-ttu-id="ec267-257">Par exemple, si vous avez initialement séquencé un package à l’aide d’un ordinateur exécutant un système d’exploitation 64 bits, vous devez modifier le package à l’aide d’un ordinateur exécutant un système d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ec267-257">For example, if you initially sequenced a package using a computer running a 64-bit operating system, you should modify the package using a computer running a 64-bit operating system.</span></span>

[<span data-ttu-id="ec267-258">Comment modifier un package d'application virtuelle existant</span><span class="sxs-lookup"><span data-stu-id="ec267-258">How to Modify an Existing Virtual Application Package</span></span>](how-to-modify-an-existing-virtual-application-package-beta.md)

## <span data-ttu-id="ec267-259">Création d’un modèle de projet</span><span class="sxs-lookup"><span data-stu-id="ec267-259">Creating a project template</span></span>


<span data-ttu-id="ec267-260">Un fichier. appvt est un modèle de projet qui peut être utilisé pour enregistrer les paramètres personnalisés fréquemment appliqués.</span><span class="sxs-lookup"><span data-stu-id="ec267-260">A .appvt file is a project template that can be used to save commonly applied, customized settings.</span></span> <span data-ttu-id="ec267-261">Vous pouvez ensuite plus facilement utiliser ces paramètres pour de futurs séquençages.</span><span class="sxs-lookup"><span data-stu-id="ec267-261">You can then more easily use these settings for future sequencings.</span></span>

<span data-ttu-id="ec267-262">Les modèles de projet App-V 5,0 diffèrent des accélérateurs d’application à l’application-V 5,0, car les accélérateurs d’application-V 5,0 sont propres à l’application et les modèles de projets App-V 5,0 peuvent être appliqués à plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="ec267-262">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span> <span data-ttu-id="ec267-263">Par ailleurs, vous ne pouvez pas utiliser un modèle de projet lorsque vous utilisez un accélérateur de package pour créer un package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ec267-263">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span> <span data-ttu-id="ec267-264">Les paramètres généraux suivants sont enregistrés avec un modèle de projet App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="ec267-264">The following general settings are saved with an App-V 5.0 project template:</span></span>

<span data-ttu-id="ec267-265">Un modèle peut spécifier et stocker plusieurs paramètres comme suit:</span><span class="sxs-lookup"><span data-stu-id="ec267-265">A template can specify and store multiple settings as follows:</span></span>

-   <span data-ttu-id="ec267-266">**Options de surveillance avancée**.</span><span class="sxs-lookup"><span data-stu-id="ec267-266">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="ec267-267">Autorise l’exécution de Microsoft Update lors du suivi.</span><span class="sxs-lookup"><span data-stu-id="ec267-267">Enables Microsoft Update to run during monitoring.</span></span> <span data-ttu-id="ec267-268">Enregistre les paramètres autoriser les interactions locales</span><span class="sxs-lookup"><span data-stu-id="ec267-268">Saves allow local interaction option settings</span></span>

-   <span data-ttu-id="ec267-269">**Options générales**.</span><span class="sxs-lookup"><span data-stu-id="ec267-269">**General Options**.</span></span> <span data-ttu-id="ec267-270">Active l’utilisation du **programme d’installation Windows**, **Ajouter la version du package au nom de fichier**.</span><span class="sxs-lookup"><span data-stu-id="ec267-270">Enables the use of **Windows Installer**, **Append Package Version to Filename**.</span></span>

-   **<span data-ttu-id="ec267-271">Éléments d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="ec267-271">Exclusion Items.</span></span>** <span data-ttu-id="ec267-272">Contient la liste modèle d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="ec267-272">Contains the Exclusion pattern list.</span></span>

[<span data-ttu-id="ec267-273">Comment créer et utiliser un modèle de projet</span><span class="sxs-lookup"><span data-stu-id="ec267-273">How to Create and Use a Project Template</span></span>](how-to-create-and-use-a-project-template.md)

## <span data-ttu-id="ec267-274">Création d’un accélérateur de package</span><span class="sxs-lookup"><span data-stu-id="ec267-274">Creating a package accelerator</span></span>


<span data-ttu-id="ec267-275">**Remarques**  Les accélérateurs de package créés à l’aide d’une version antérieure de App-V doivent être recréés à l’aide de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ec267-275">**Note** Package accelerators created using a previous version of App-V must be recreated using App-V 5.0.</span></span>

 

<span data-ttu-id="ec267-276">Vous pouvez utiliser les accélérateurs de package App-V 5,0 pour générer automatiquement un nouveau package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="ec267-276">You can use App-V 5.0 package accelerators to automatically generate a new virtual application packages.</span></span> <span data-ttu-id="ec267-277">Une fois que vous avez correctement créé un accélérateur de package, vous pouvez réutiliser et partager l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="ec267-277">After you have successfully created a package accelerator, you can reuse and share the package accelerator.</span></span>

<span data-ttu-id="ec267-278">Dans certains cas, pour créer l’accélérateur de package, vous devrez peut-être installer l’application localement sur l’ordinateur qui exécute le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="ec267-278">In some situations, to create the package accelerator, you might have to install the application locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="ec267-279">Dans ces cas, vous devez commencer par créer l’accélérateur de package à l’aide du support d’installation.</span><span class="sxs-lookup"><span data-stu-id="ec267-279">In such cases, you should first try to create the package accelerator with the installation media.</span></span> <span data-ttu-id="ec267-280">Si plusieurs fichiers manquants sont requis, vous devez installer l’application localement sur l’ordinateur qui exécute le Sequencer, puis créer l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="ec267-280">If multiple missing files are required, you should install the application locally to the computer that runs the sequencer, and then create the package accelerator.</span></span>

<span data-ttu-id="ec267-281">Une fois que vous avez correctement créé un accélérateur de package, vous pouvez réutiliser et partager l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="ec267-281">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="ec267-282">Le fait de créer des accélérateurs de package App-V 5,0 est une tâche avancée.</span><span class="sxs-lookup"><span data-stu-id="ec267-282">Creating App-V 5.0 Package Accelerators is an advanced task.</span></span> <span data-ttu-id="ec267-283">Les accélérateurs de package peuvent contenir des informations relatives aux mots de passe et aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ec267-283">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="ec267-284">Par conséquent, vous devez enregistrer les accélérateurs de packages et le média d’installation associé dans un emplacement sécurisé, et vous devez signer numériquement l’accélérateur de package après l’avoir créé, afin que l’éditeur puisse être vérifié lorsque l’accélérateur de package App-V 5,0 est appliqué.</span><span class="sxs-lookup"><span data-stu-id="ec267-284">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>

[<span data-ttu-id="ec267-285">Comment créer un accélérateur de package</span><span class="sxs-lookup"><span data-stu-id="ec267-285">How to Create a Package Accelerator</span></span>](how-to-create-a-package-accelerator.md)

[<span data-ttu-id="ec267-286">Comment créer un package d'application virtuelle à l'aide d'un accélérateur de package App-V</span><span class="sxs-lookup"><span data-stu-id="ec267-286">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## <span data-ttu-id="ec267-287">Rapports d’erreur de Sequencer</span><span class="sxs-lookup"><span data-stu-id="ec267-287">Sequencer error reporting</span></span>


<span data-ttu-id="ec267-288">Le Sequencer App-V 5,0 peut détecter les problèmes courants de séquençage lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="ec267-288">The App-V 5.0 Sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="ec267-289">La page **rapport d’installation** à la fin de l’Assistant séquençage affiche les messages de diagnostic classés en **erreurs**, **avertissements**et **informations** en fonction de la gravité du problème.</span><span class="sxs-lookup"><span data-stu-id="ec267-289">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="ec267-290">Vous pouvez également accéder à des informations supplémentaires sur les erreurs de séquençage à l’aide de l’observateur d’événements Windows.</span><span class="sxs-lookup"><span data-stu-id="ec267-290">You can also find additional information about sequencing errors using the Windows Event Viewer.</span></span>






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a><span data-ttu-id="ec267-291">Autres ressources pour le Sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ec267-291">Other resources for the App-V 5.0 sequencer</span></span>


-   [<span data-ttu-id="ec267-292">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="ec267-292">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 






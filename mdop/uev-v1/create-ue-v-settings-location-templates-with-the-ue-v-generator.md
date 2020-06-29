---
title: Créer des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V
description: Créer des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811879"
---
# <span data-ttu-id="7d7a1-103">Créer des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="7d7a1-103">Create UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="7d7a1-104">La virtualisation de l’utilisation de l’utilisation de Microsoft (UE-V) utilise des *modèles d’emplacement des paramètres* pour itinérance des paramètres d’application entre les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-104">Microsoft User Experience Virtualization (UE-V) uses *settings location templates* to roam application settings between user computers.</span></span> <span data-ttu-id="7d7a1-105">Certains modèles d’emplacement des paramètres standard sont inclus avec la virtualisation de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-105">Some standard settings location templates are included with User Experience Virtualization.</span></span> <span data-ttu-id="7d7a1-106">Vous pouvez également créer, modifier ou valider des modèles d’emplacements de paramètres personnalisés avec le générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-106">You can also create, edit, or validate custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="7d7a1-107">Le générateur UE-V analyse une application afin de détecter et de capturer les emplacements où l’application stocke ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-107">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="7d7a1-108">L’application surveillée doit être une application classique.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-108">The application that is being monitored must be a traditional application.</span></span> <span data-ttu-id="7d7a1-109">Le générateur UE-V ne peut pas créer de modèle d’emplacement des paramètres à partir des types d’applications suivants:</span><span class="sxs-lookup"><span data-stu-id="7d7a1-109">The UE-V Generator cannot create a settings location template from the following application types:</span></span>

-   <span data-ttu-id="7d7a1-110">Applications virtualisées</span><span class="sxs-lookup"><span data-stu-id="7d7a1-110">Virtualized applications</span></span>

-   <span data-ttu-id="7d7a1-111">Application proposée via les services Terminal Server</span><span class="sxs-lookup"><span data-stu-id="7d7a1-111">Application offered through terminal services</span></span>

-   <span data-ttu-id="7d7a1-112">Applications Java</span><span class="sxs-lookup"><span data-stu-id="7d7a1-112">Java applications</span></span>

-   <span data-ttu-id="7d7a1-113">Applications Windows 8</span><span class="sxs-lookup"><span data-stu-id="7d7a1-113">Windows 8 applications</span></span>

<span data-ttu-id="7d7a1-114">**Remarques**  Les modèles UE-V ne peuvent pas être créés à partir d’applications virtuelles ou d’applications de services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-114">**Note** UE-V templates cannot be created from virtualized applications or terminal services applications.</span></span> <span data-ttu-id="7d7a1-115">Néanmoins, il est possible d’appliquer des paramètres synchronisés à l’aide des modèles à ces applications.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-115">However, settings synchronized using the templates can be applied to those applications.</span></span> <span data-ttu-id="7d7a1-116">Pour créer des modèles qui prennent en charge les applications VDI (Virtual Desktop Infrastructure) et Terminal Services, ouvrez une version du fichier Windows Installer (. msi) de l’application auprès d’UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-116">To create templates that support Virtual Desktop Infrastructure (VDI) and terminal services applications, open a Windows Installer File (.msi) version of the application with UE-V Generator.</span></span>

 

**<span data-ttu-id="7d7a1-117">Emplacements exclus</span><span class="sxs-lookup"><span data-stu-id="7d7a1-117">Excluded Locations</span></span>**

<span data-ttu-id="7d7a1-118">Le processus de découverte exclut les emplacements dans lesquels les fichiers de logiciels d’application stockés habituellement sur les ordinateurs des utilisateurs et les environnements.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-118">The discovery process excludes locations which commonly store application software files that do not roam well between user computers or environments.</span></span> <span data-ttu-id="7d7a1-119">Les éléments suivants sont exclus:</span><span class="sxs-lookup"><span data-stu-id="7d7a1-119">The following are excluded:</span></span>

-   <span data-ttu-id="7d7a1-120">HKEY \ _CURRENT \ _USER clés de Registre et les fichiers auxquels l’utilisateur connecté ne peut pas écrire de valeurs</span><span class="sxs-lookup"><span data-stu-id="7d7a1-120">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="7d7a1-121">HKEY \ _CURRENT \ _USER clés de Registre et fichiers associés aux fonctionnalités principales du système d’exploitation Windows</span><span class="sxs-lookup"><span data-stu-id="7d7a1-121">HKEY\_CURRENT\_USER registry keys and files associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="7d7a1-122">Toutes les clés de Registre se trouvant dans la ruche du _MACHINE HKEY \ _LOCAL</span><span class="sxs-lookup"><span data-stu-id="7d7a1-122">All registry keys located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="7d7a1-123">Fichiers situés dans les répertoires de fichiers du programme</span><span class="sxs-lookup"><span data-stu-id="7d7a1-123">Files located in Program Files directories</span></span>

-   <span data-ttu-id="7d7a1-124">Fichiers situés dans les utilisateurs \ \ \ [nom d’utilisateur \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="7d7a1-124">Files located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="7d7a1-125">Fichiers du système d’exploitation Windows situés dans% SystemRoot%</span><span class="sxs-lookup"><span data-stu-id="7d7a1-125">Windows operating system files located in %systemroot%</span></span>

<span data-ttu-id="7d7a1-126">Si les clés de Registre et les fichiers stockés dans ces emplacements exclus sont requis pour pouvoir itinérance des paramètres d’application, les administrateurs peuvent ajouter manuellement les emplacements au modèle d’emplacement des paramètres pendant le processus de création de modèle.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-126">If registry keys and files stored in these excluded locations are required in order to roam application settings, administrators can manually add the locations to the settings location template during the template creation process.</span></span>

## <span data-ttu-id="7d7a1-127">Créer des modèles UE-V</span><span class="sxs-lookup"><span data-stu-id="7d7a1-127">Create UE-V templates</span></span>


<span data-ttu-id="7d7a1-128">Utilisez le générateur UE-V pour créer des modèles d’emplacement des paramètres pour applications métier ou d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-128">Use the UE-V Generator to create settings location templates for line-of-business applications or other applications.</span></span> <span data-ttu-id="7d7a1-129">Une fois le modèle créé pour une application créée, vous pouvez déployer le modèle sur des ordinateurs pour permettre aux utilisateurs d’effectuer les réglages de l’application.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-129">After the template for an application is created, you can deploy the template to computers so users can roam the settings for that application.</span></span>

**<span data-ttu-id="7d7a1-130">Pour créer un modèle d’emplacement des paramètres UE-V avec le générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="7d7a1-130">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="7d7a1-131">Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **utilisation de Microsoft**, puis sur générateur de **virtualisation Microsoft User Interface**.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-131">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="7d7a1-132">Cliquez sur **créer un modèle d’emplacement des paramètres**.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-132">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="7d7a1-133">Spécifiez l’application.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-133">Specify the application.</span></span> <span data-ttu-id="7d7a1-134">Naviguez jusqu’au chemin d’accès de l’application (. exe) ou du raccourci de l’application (. lnk) pour lequel vous voulez créer un modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-134">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="7d7a1-135">Spécifiez les arguments de ligne de commande, le cas échéant, et le répertoire de travail, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-135">Specify the command line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="7d7a1-136">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-136">Click **Next** to continue.</span></span>

    <span data-ttu-id="7d7a1-137">**Remarques**  Avant le démarrage de l’application, le système affiche une invite de **contrôle de compte d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-137">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="7d7a1-138">Une autorisation est requise pour contrôler les emplacements du Registre et des fichiers utilisés par l’application pour le stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-138">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="7d7a1-139">Après le démarrage de l’application, fermez l’application.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-139">After the application starts, close the application.</span></span> <span data-ttu-id="7d7a1-140">Le générateur UE-V enregistre les emplacements où l’application stocke ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-140">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="7d7a1-141">Une fois le processus terminé, cliquez sur **suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-141">After the process is complete, click **Next** to continue.</span></span>

6.  <span data-ttu-id="7d7a1-142">Activez et désactivez les cases à cocher en regard des emplacements et paramètres de fichier de paramètres du registre appropriés à déplacer pour cette application.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-142">Review and select the check boxes next to the appropriate registry settings locations and settings file locations to roam for this application.</span></span> <span data-ttu-id="7d7a1-143">La liste inclut les deux catégories suivantes pour les emplacements de paramètres:</span><span class="sxs-lookup"><span data-stu-id="7d7a1-143">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="7d7a1-144">**Standard**: les paramètres de l’application qui sont stockés dans le Registre sous les clés HKEY \ _CURRENT \ _USER ou dans les dossiers de fichiers sous \ \ **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **itinérance**.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-144">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="7d7a1-145">UE-V Generator inclut ces paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-145">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="7d7a1-146">Non **standard**: paramètres d’application stockés en dehors des emplacements spécifiés dans les recommandations en matière de stockage des données de paramètres (facultatif).</span><span class="sxs-lookup"><span data-stu-id="7d7a1-146">**Nonstandard**: Application settings that are stored outside the locations specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="7d7a1-147">Il s’agit des fichiers et dossiers sous **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-147">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="7d7a1-148">Passez en revue ces emplacements pour déterminer s’ils doivent figurer dans le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-148">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="7d7a1-149">Activez les cases à cocher emplacements pour les inclure.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-149">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="7d7a1-150">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-150">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="7d7a1-151">Examinez et modifiez les **Propriétés**, emplacements **du Registre** et emplacements des **fichiers** pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-151">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="7d7a1-152">Modifiez les propriétés suivantes sous l’onglet **Propriétés** :</span><span class="sxs-lookup"><span data-stu-id="7d7a1-152">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="7d7a1-153">**Nom**de l’application: nom de l’application rédigée dans la description des propriétés du programme files.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-153">**Application Name**: The application name written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="7d7a1-154">**Nom du programme**: nom du programme que vous avez utilisé dans les propriétés du fichier programme.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-154">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="7d7a1-155">Ce nom est généralement l’extension. exe.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-155">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="7d7a1-156">**Version du produit**: numéro de version du fichier. exe de l’application.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-156">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="7d7a1-157">En conjonction avec la version du fichier, cette propriété permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-157">This property, in conjunction with the File version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="7d7a1-158">Cette propriété accepte un numéro de version principal.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-158">This property accepts a major version number.</span></span> <span data-ttu-id="7d7a1-159">Si cette propriété est vide, le modèle d’emplacement des paramètres s’applique à toutes les versions du produit.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-159">If this property is empty, the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="7d7a1-160">**Version du fichier**: numéro de version du fichier the.exe de l’application.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-160">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="7d7a1-161">Combinée à la version du produit, cette propriété permet d’identifier les applications ciblées par le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-161">This property, in conjunction with the Product version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="7d7a1-162">Cette propriété accepte un numéro de version principal.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-162">This property accepts a major version number.</span></span> <span data-ttu-id="7d7a1-163">Si cette propriété est vide, le modèle d’emplacement des paramètres s’appliquera à toutes les versions du programme.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-163">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="7d7a1-164">**Nom** de l’auteur du modèle (facultatif): nom de l’auteur du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-164">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="7d7a1-165">**Courrier de création de modèles** (facultatif): adresse de messagerie de l’auteur du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-165">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="7d7a1-166">L’onglet **Registre** recense la **clé** et l' **étendue** des emplacements du Registre inclus dans le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-166">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="7d7a1-167">Modifiez les emplacements du Registre à l’aide du menu déroulant **tâches** .</span><span class="sxs-lookup"><span data-stu-id="7d7a1-167">Edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="7d7a1-168">Il s’agit notamment de l’ajout de nouvelles clés, de la modification du nom ou de l’étendue des clés existantes, de la suppression de clés et de la consultation du registre où se trouvent les clés.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-168">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry where the keys are located.</span></span> <span data-ttu-id="7d7a1-169">Utilisez l’étendue **all settings** pour inclure tous les paramètres de Registre sous la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-169">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="7d7a1-170">Utilisez les **paramètres et** sous-clés pour inclure tous les paramètres de Registre sous les paramètres de clé, de sous-clé et de sous-clé spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-170">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="7d7a1-171">L’onglet **fichiers** recense le chemin d’accès au fichier et le masque des fichiers des emplacements de fichier inclus dans le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-171">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="7d7a1-172">Modifiez les emplacements des fichiers à l’aide du menu déroulant **tâches** .</span><span class="sxs-lookup"><span data-stu-id="7d7a1-172">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="7d7a1-173">Les tâches pour les emplacements de fichiers incluent l’ajout de nouveaux fichiers ou d’emplacements de dossiers, la modification de l’étendue de fichiers ou dossiers existants, la suppression de fichiers ou de dossiers et l’ouverture de l’emplacement sélectionné dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-173">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="7d7a1-174">Laissez le masque de fichiers vide pour inclure tous les fichiers dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-174">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="7d7a1-175">Cliquez sur **créer** , puis enregistrez le modèle d’emplacement des paramètres sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-175">Click **Create** and save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="7d7a1-176">Cliquez sur **Fermer** pour fermer l’Assistant modèle de paramètres.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-176">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="7d7a1-177">Quittez l’application de générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-177">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="7d7a1-178">Après avoir créé le modèle d’emplacement des paramètres pour une application, vous devez tester le modèle.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-178">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="7d7a1-179">Déployez le modèle dans un environnement de laboratoire avant de le mettre en production dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7d7a1-179">Deploy the template in a lab environment before putting it into production in the enterprise.</span></span>

## <span data-ttu-id="7d7a1-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d7a1-180">Related topics</span></span>


[<span data-ttu-id="7d7a1-181">Utilisation de modèles UE-V personnalisés et du Générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="7d7a1-181">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="7d7a1-182">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="7d7a1-182">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 






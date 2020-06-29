---
title: Modifier des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V
description: Modifier des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812161"
---
# <span data-ttu-id="00997-103">Modifier des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="00997-103">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="00997-104">Utilisez le générateur Microsoft User performance (UE-V) pour modifier les modèles d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-104">Use the Microsoft User Experience Virtualization (UE-V) Generator to edit settings location templates.</span></span> <span data-ttu-id="00997-105">Une fois les paramètres revus ajoutés aux modèles à l’aide du générateur UE-V, les informations de version au sein du modèle sont automatiquement mises à jour pour garantir que tous les modèles existants déployés dans l’entreprise soient correctement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="00997-105">When the revised settings are added to the templates using the UE-V Generator, the version information within the template is automatically updated to ensure that any existing templates deployed in the enterprise are updated correctly.</span></span>

**<span data-ttu-id="00997-106">Comment modifier un modèle d’emplacement des paramètres UE-V avec le générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="00997-106">How to edit a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="00997-107">Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **utilisation de Microsoft**, puis sur générateur de **virtualisation Microsoft User Interface**.</span><span class="sxs-lookup"><span data-stu-id="00997-107">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="00997-108">Cliquez sur **modifier un modèle d’emplacement des paramètres**.</span><span class="sxs-lookup"><span data-stu-id="00997-108">Click **Edit a settings location template**.</span></span>

3.  <span data-ttu-id="00997-109">Dans la liste des modèles que vous avez utilisés récemment, sélectionnez le modèle à modifier.</span><span class="sxs-lookup"><span data-stu-id="00997-109">In the list of recently used templates, select the template to be edited.</span></span> <span data-ttu-id="00997-110">Vous pouvez également **accéder** au fichier de modèle de paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-110">Alternatively, **Browse** to the settings template file.</span></span> <span data-ttu-id="00997-111">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="00997-111">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="00997-112">Passez en revue les emplacements **Propriétés**, emplacements **du registre** et **fichiers** pour le modèle de paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-112">Review the **Properties**, **Registry** locations, and **Files** locations for the settings template.</span></span> <span data-ttu-id="00997-113">Apportez les modifications souhaitées.</span><span class="sxs-lookup"><span data-stu-id="00997-113">Edit as needed.</span></span>

    -   <span data-ttu-id="00997-114">L’onglet **Propriétés** vous permet d’afficher et de modifier les propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="00997-114">The **Properties** tab allows you to view and edit the following properties:</span></span>

        -   <span data-ttu-id="00997-115">**Nom**de l’application: nom de l’application écrit dans la description des propriétés du fichier du programme.</span><span class="sxs-lookup"><span data-stu-id="00997-115">**Application name**: The application name written in the description of the program file properties.</span></span>

        -   <span data-ttu-id="00997-116">**Nom du programme**: nom du programme que vous avez utilisé dans les propriétés du fichier programme.</span><span class="sxs-lookup"><span data-stu-id="00997-116">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="00997-117">Ce nom est généralement l’extension. exe.</span><span class="sxs-lookup"><span data-stu-id="00997-117">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="00997-118">**Version du produit**: numéro de version du fichier. exe de l’application.</span><span class="sxs-lookup"><span data-stu-id="00997-118">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="00997-119">Cette propriété, associée à la **version du fichier**, permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-119">This property, together with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="00997-120">Cette propriété accepte un numéro de version principal.</span><span class="sxs-lookup"><span data-stu-id="00997-120">This property accepts a major version number.</span></span> <span data-ttu-id="00997-121">Si cette propriété est vide, le modèle d’emplacement des paramètres s’appliquera à toutes les versions du produit.</span><span class="sxs-lookup"><span data-stu-id="00997-121">If this property is empty, then the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="00997-122">**Version du fichier**: numéro de version du fichier the.exe de l’application.</span><span class="sxs-lookup"><span data-stu-id="00997-122">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="00997-123">Outre la **version du produit**, cette propriété permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-123">This property, along with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="00997-124">Cette propriété accepte un numéro de version principal.</span><span class="sxs-lookup"><span data-stu-id="00997-124">This property accepts a major version number.</span></span> <span data-ttu-id="00997-125">Si cette propriété est vide, le modèle d’emplacement des paramètres s’appliquera à toutes les versions du programme.</span><span class="sxs-lookup"><span data-stu-id="00997-125">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="00997-126">**Nom** de l’auteur du modèle (facultatif): nom de l’auteur du modèle de paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-126">**Template author name** (optional): The name of the settings template author.</span></span>

        -   <span data-ttu-id="00997-127">**Courrier de création de modèles** (facultatif): adresse de messagerie de l’auteur du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-127">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="00997-128">L’onglet **Registre** recense la **clé** et l' **étendue** des emplacements du Registre inclus dans le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-128">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="00997-129">Vous pouvez modifier les emplacements du Registre à l’aide du menu déroulant **tâches** .</span><span class="sxs-lookup"><span data-stu-id="00997-129">You can edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="00997-130">Il s’agit notamment de l’ajout de nouvelles clés, de la modification du nom ou de l’étendue des clés existantes, de la suppression de clés et de la consultation du Registre dans lequel se trouvent les clés.</span><span class="sxs-lookup"><span data-stu-id="00997-130">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry in which the keys are located.</span></span> <span data-ttu-id="00997-131">Lorsque vous définissez l’étendue du Registre, vous pouvez utiliser l’étendue **all settings** pour inclure tous les paramètres du Registre sous la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="00997-131">When you define the scope for the registry, you can use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="00997-132">Utilisez **tous les paramètres** et **sous-clés** pour inclure tous les paramètres de Registre sous les paramètres de clé, de sous-clé et de sous-clé spécifiés.</span><span class="sxs-lookup"><span data-stu-id="00997-132">Use **All Settings** and **Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="00997-133">L’onglet **fichiers** recense le chemin d’accès au fichier et le masque des fichiers des emplacements de fichier inclus dans le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-133">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="00997-134">Vous pouvez modifier les emplacements des fichiers à l’aide du menu déroulant **tâches** .</span><span class="sxs-lookup"><span data-stu-id="00997-134">You can edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="00997-135">Les tâches pour les emplacements de fichiers incluent l’ajout de nouveaux fichiers ou d’emplacements de dossiers, la modification de l’étendue de fichiers ou dossiers existants, la suppression de fichiers ou de dossiers et l’ouverture de l’emplacement sélectionné dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="00997-135">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="00997-136">Pour inclure tous les fichiers dans le dossier spécifié, laissez le masque de fichiers vide.</span><span class="sxs-lookup"><span data-stu-id="00997-136">To include all files in the specified folder, leave the file mask empty.</span></span>

5.  <span data-ttu-id="00997-137">Cliquez sur **Enregistrer** pour enregistrer les modifications apportées au modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-137">Click **Save** to save the changes to the settings location template.</span></span>

6.  <span data-ttu-id="00997-138">Cliquez sur **Fermer** pour fermer l’Assistant modèle de paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-138">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="00997-139">Quittez l’application de générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="00997-139">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="00997-140">Après avoir modifié le modèle d’emplacement des paramètres pour une application, vous devez tester le modèle.</span><span class="sxs-lookup"><span data-stu-id="00997-140">After editing the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="00997-141">Déployez le modèle d’emplacement des paramètres révisé dans un environnement de laboratoire avant de le mettre en production dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="00997-141">Deploy the revised settings location template in a lab environment before putting it into production in the enterprise.</span></span>

**<span data-ttu-id="00997-142">Modification manuelle d’un modèle d’emplacement des paramètres</span><span class="sxs-lookup"><span data-stu-id="00997-142">How to manually edit a settings location template</span></span>**

1.  <span data-ttu-id="00997-143">Créer une copie locale du modèle d’emplacement des paramètres (fichier. Xml).</span><span class="sxs-lookup"><span data-stu-id="00997-143">Create a local copy of the settings location template (.xml file).</span></span> <span data-ttu-id="00997-144">Les modèles d’emplacement des paramètres d’UE-V sont des fichiers. xml identifiant les emplacements où les valeurs des paramètres du magasin d’applications.</span><span class="sxs-lookup"><span data-stu-id="00997-144">UE-V settings location templates are .xml files identifying the locations where application store settings values.</span></span>

2.  <span data-ttu-id="00997-145">Ouvrez le fichier de modèle d’emplacement des paramètres à l’aide d’un éditeur XML.</span><span class="sxs-lookup"><span data-stu-id="00997-145">Open the settings location template file with an XML editor.</span></span>

3.  <span data-ttu-id="00997-146">Modifiez le fichier de modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="00997-146">Edit the settings location template file.</span></span> <span data-ttu-id="00997-147">Toutes les modifications doivent être conformes au fichier de schéma UE-V défini dans SettingsLocationTempate. xsd.</span><span class="sxs-lookup"><span data-stu-id="00997-147">All changes must conform to the UE-V schema file defined in SettingsLocationTempate.xsd.</span></span> <span data-ttu-id="00997-148">Une copie du fichier. xsd se trouve `\ProgramData\Microsoft\UEV\Templates` par défaut.</span><span class="sxs-lookup"><span data-stu-id="00997-148">A copy of the .xsd file is located in `\ProgramData\Microsoft\UEV\Templates` by default.</span></span>

4.  <span data-ttu-id="00997-149">Enregistrez le fichier de modèle d’emplacement des paramètres, puis fermez l’éditeur XML.</span><span class="sxs-lookup"><span data-stu-id="00997-149">Save the settings location template file and close the XML editor.</span></span>

5.  <span data-ttu-id="00997-150">Validez le fichier de modèle d’emplacement des paramètres modifié à l’aide du générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="00997-150">Validate the modified settings location template file with the UE-V Generator.</span></span> <span data-ttu-id="00997-151">Pour plus d’informations sur la validation du générateur UE-V, voir [valider les modèles d’emplacement des paramètres UE-v auprès d’UE-v Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span><span class="sxs-lookup"><span data-stu-id="00997-151">For more information about validating with the UE-V Generator, see [Validate UE-V Settings Location Templates with UE-V Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span></span>

## <span data-ttu-id="00997-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="00997-152">Related topics</span></span>


[<span data-ttu-id="00997-153">Utilisation de modèles UE-V personnalisés et du Générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="00997-153">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="00997-154">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="00997-154">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 






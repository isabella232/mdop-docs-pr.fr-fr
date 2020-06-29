---
title: Procédure pour créer des accélérateurs de package App-V (App-V4.6SP1)
description: Procédure pour créer des accélérateurs de package App-V (App-V4.6SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807186"
---
# <span data-ttu-id="6e096-103">Procédure pour créer des accélérateurs de package App-V (App-V4.6SP1)</span><span class="sxs-lookup"><span data-stu-id="6e096-103">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="6e096-104">Vous pouvez utiliser les accélérateurs de package App-V pour générer automatiquement un nouveau package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="6e096-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="6e096-105">Une fois que vous avez correctement créé un accélérateur de package, vous pouvez réutiliser et partager l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="6e096-105">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="6e096-106">Pour plus d’informations sur les accélérateurs de package, voir [à propos des accélérateurs de package App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="6e096-106">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span> <span data-ttu-id="6e096-107">La création d’accélérateurs de package App-V est une tâche avancée.</span><span class="sxs-lookup"><span data-stu-id="6e096-107">Creating App-V Package Accelerators is an advanced task.</span></span> <span data-ttu-id="6e096-108">Les accélérateurs de package peuvent contenir des informations relatives aux mots de passe et aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6e096-108">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="6e096-109">Par conséquent, vous devez enregistrer les accélérateurs de package et le média d’installation associé dans un emplacement sécurisé, et vous devez signer numériquement l’accélérateur de package après l’avoir créé, afin que l’éditeur puisse être vérifié lorsque l’accélérateur de package App-V est appliqué.</span><span class="sxs-lookup"><span data-stu-id="6e096-109">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V Package Accelerator is applied.</span></span>

<span data-ttu-id="6e096-110">Dans certains cas, pour créer l’accélérateur de package, vous devrez peut-être installer l’application localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="6e096-110">In some situations, to create the Package Accelerator, you might have to install the application locally on the computer running the Sequencer.</span></span> <span data-ttu-id="6e096-111">Tout d’abord, essayez de créer l’accélérateur de package à l’aide du support d’installation, et si le nombre de fichiers manquants requis est requis, installez l’application localement sur l’ordinateur exécutant le Sequencer, puis créez l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="6e096-111">First try to create the Package Accelerator by using the installation media, and if there are a number of missing files that are required, install the application locally to the computer running the Sequencer, and then create the Package Accelerator.</span></span>

**<span data-ttu-id="6e096-112">Important</span><span class="sxs-lookup"><span data-stu-id="6e096-112">Important</span></span>**  
<span data-ttu-id="6e096-113">Avant de commencer la procédure suivante, vous devez effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="6e096-113">Before you begin the following procedure, you should do the following:</span></span>

-   <span data-ttu-id="6e096-114">Copiez le package d’application virtuel que vous devez utiliser pour créer l’accélérateur de package localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="6e096-114">Copy the virtual application package that you must use to create the Package Accelerator locally to the computer running the Sequencer.</span></span>

-   <span data-ttu-id="6e096-115">Copiez tous les fichiers d’installation requis associés au package d’application virtuelle sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="6e096-115">Copy all required installation files associated with the virtual application package to the computer running the Sequencer.</span></span>



**<span data-ttu-id="6e096-116">Important</span><span class="sxs-lookup"><span data-stu-id="6e096-116">Important</span></span>**  
<span data-ttu-id="6e096-117">Exclusion de responsabilité: le Sequencer Microsoft Application Virtualization ne vous donne aucun droit de licence pour l’application logicielle que vous utilisez pour créer un accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="6e096-117">Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="6e096-118">Vous devez respecter les conditions générales du contrat de licence utilisateur final pour une telle application.</span><span class="sxs-lookup"><span data-stu-id="6e096-118">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="6e096-119">Il est de votre responsabilité de veiller à ce que les termes du contrat de licence de l’application logicielle vous permettent de créer un accélérateur de package à l’aide du Sequencer de la virtualisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="6e096-119">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="6e096-120">Pour créer un accélérateur de package App-V</span><span class="sxs-lookup"><span data-stu-id="6e096-120">To create an App-V Package Accelerator</span></span>**

1.  <span data-ttu-id="6e096-121">Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="6e096-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="6e096-122">Pour démarrer l’Assistant App-v de **création de package** , dans le Sequencer App-v, cliquez sur **Outils**  /  **créer un accélérateur de package**.</span><span class="sxs-lookup"><span data-stu-id="6e096-122">To start the App-V **Create Package Accelerator** wizard, in the App-V Sequencer, click **Tools** / **Create Package Accelerator**.</span></span>

3.  <span data-ttu-id="6e096-123">Dans la page **Sélectionner un package** , pour spécifier un package d’application virtuelle existant à utiliser pour créer l’accélérateur de package, cliquez sur **Parcourir**, puis recherchez le package d’application virtuelle existant (fichier. sprj).</span><span class="sxs-lookup"><span data-stu-id="6e096-123">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.sprj file).</span></span>

    **<span data-ttu-id="6e096-124">Astuce</span><span class="sxs-lookup"><span data-stu-id="6e096-124">Tip</span></span>**  
    <span data-ttu-id="6e096-125">Copiez les fichiers associés au package d’application virtuel que vous envisagez d’utiliser localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="6e096-125">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="6e096-126">Dans la page **fichiers d’installation** , pour spécifier le dossier contenant les fichiers d’installation que vous avez utilisés pour créer le package d’application virtuelle d’origine, cliquez sur **Parcourir**, puis sélectionnez le répertoire contenant les fichiers d’installation.</span><span class="sxs-lookup"><span data-stu-id="6e096-126">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="6e096-127">Astuce</span><span class="sxs-lookup"><span data-stu-id="6e096-127">Tip</span></span>**  
   <span data-ttu-id="6e096-128">Copiez le dossier contenant les fichiers d’installation requis sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="6e096-128">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. <span data-ttu-id="6e096-129">Dans la page **collecte d’informations** , consultez les fichiers qui n’ont pas été trouvés dans l’emplacement spécifié dans la page fichiers d' **installation** de cet Assistant.</span><span class="sxs-lookup"><span data-stu-id="6e096-129">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="6e096-130">Si les fichiers affichés ne sont pas obligatoires, sélectionnez **supprimer ces fichiers**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="6e096-130">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="6e096-131">Si les fichiers sont requis, cliquez sur **précédent** , puis copiez les fichiers requis dans le répertoire spécifié dans la page **fichiers d’installation** .</span><span class="sxs-lookup"><span data-stu-id="6e096-131">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="6e096-132">Remarque</span><span class="sxs-lookup"><span data-stu-id="6e096-132">Note</span></span>**  
   <span data-ttu-id="6e096-133">Vous devez supprimer les fichiers non requis ou cliquer sur **précédent** , puis rechercher les fichiers requis pour passer à la page suivante de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="6e096-133">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



6. <span data-ttu-id="6e096-134">Dans la page **Sélectionner des fichiers** , passez en revue les fichiers qui ont été détectés et effacez les fichiers qui doivent être supprimés de l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="6e096-134">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the Package Accelerator.</span></span> <span data-ttu-id="6e096-135">Sélectionnez uniquement les fichiers nécessaires à l’exécution correcte de l’application, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="6e096-135">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

7. <span data-ttu-id="6e096-136">Dans la page **verify applications (vérifier les applications** ), vérifiez que tous les fichiers d’installation requis pour générer le package sont affichés.</span><span class="sxs-lookup"><span data-stu-id="6e096-136">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="6e096-137">Lorsque l’accélérateur de package est utilisé pour créer un nouveau package, tous les fichiers d’installation affichés dans le volet **applications** sont requis pour créer le package.</span><span class="sxs-lookup"><span data-stu-id="6e096-137">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="6e096-138">Si nécessaire, pour ajouter d’autres fichiers du programme d’installation, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6e096-138">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="6e096-139">Pour supprimer les fichiers d’installation inutiles, sélectionnez le fichier d’installation, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6e096-139">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="6e096-140">Pour modifier les propriétés associées à un programme d’installation, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="6e096-140">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="6e096-141">Les fichiers d’installation spécifiés dans cette étape seront nécessaires lorsque l’accélérateur de package sera utilisé pour créer un nouveau package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6e096-141">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="6e096-142">Après confirmation des informations affichées, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="6e096-142">After you have confirmed the information displayed, click **Next**.</span></span>

8. <span data-ttu-id="6e096-143">Dans la page **Sélectionner des recommandations** , pour spécifier un fichier contenant des informations sur la façon dont l’accélérateur de package s’affiche, cliquez sur **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="6e096-143">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="6e096-144">Par exemple, ce fichier peut contenir des informations sur la façon dont l’ordinateur exécutant le Sequencer doit être configuré, les informations requises pour l’application pour les ordinateurs cibles et les notes générales.</span><span class="sxs-lookup"><span data-stu-id="6e096-144">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="6e096-145">Vous devez fournir toutes les informations nécessaires à l’application de l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="6e096-145">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="6e096-146">Le fichier que vous sélectionnez doit être au format texte enrichi (. rtf) ou fichier texte (. txt).</span><span class="sxs-lookup"><span data-stu-id="6e096-146">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="6e096-147">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6e096-147">Click **Next**.</span></span>

9. <span data-ttu-id="6e096-148">Dans la page **créer un accélérateur de package** , pour spécifier l’emplacement d’enregistrement de l’accélérateur de package, cliquez sur **Parcourir** , puis sélectionnez le répertoire.</span><span class="sxs-lookup"><span data-stu-id="6e096-148">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

10. <span data-ttu-id="6e096-149">Dans la page **dernière étape** , cliquez sur **Fermer**pour fermer l’Assistant Création d’un **accélérateur de package** .</span><span class="sxs-lookup"><span data-stu-id="6e096-149">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="6e096-150">Important</span><span class="sxs-lookup"><span data-stu-id="6e096-150">Important</span></span>**  
   <span data-ttu-id="6e096-151">Pour vous assurer que le package Accelerator est le plus sécurisé possible et que l’éditeur puisse être vérifié lors de l’application de l’accélérateur de package, vous devez toujours signer numériquement l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="6e096-151">To help ensure that the Package Accelerator is as secure as possible, and so that the publisher can be verified when the Package Accelerator is applied, you should always digitally sign the Package Accelerator.</span></span>



## <span data-ttu-id="6e096-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e096-152">Related topics</span></span>


<span data-ttu-id="6e096-153">Configuration du séquenceur de virtualisation d’application (App-V 4,6 SP1) [comment appliquer un accélérateur de package pour créer un package d’application virtuelle (App-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span><span class="sxs-lookup"><span data-stu-id="6e096-153">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1) [How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span></span>










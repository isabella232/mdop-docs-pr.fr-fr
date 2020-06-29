---
title: Comment créer un accélérateur de package
description: Comment créer un accélérateur de package
author: dansimp
ms.assetid: dfe305e5-7cf8-498f-9581-4805ffc722bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0710bff5e5ea420119ac3c395c2e8917f7c582dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805605"
---
# <span data-ttu-id="cd3f7-103">Comment créer un accélérateur de package</span><span class="sxs-lookup"><span data-stu-id="cd3f7-103">How to Create a Package Accelerator</span></span>


<span data-ttu-id="cd3f7-104">Les accélérateurs de package App-V 5,0 génèrent automatiquement de nouveaux packages d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-104">App-V 5.0 package accelerators automatically generate new virtual application packages.</span></span>

**<span data-ttu-id="cd3f7-105">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd3f7-105">Note</span></span>**  
<span data-ttu-id="cd3f7-106">Vous pouvez utiliser PowerShell pour créer un accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-106">You can use PowerShell to create a package accelerator.</span></span> <span data-ttu-id="cd3f7-107">Pour plus d’informations, reportez-vous [à la rubrique Création d’un accélérateur de package à l’aide de PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="cd3f7-107">For more information see [How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).</span></span>



<span data-ttu-id="cd3f7-108">Utilisez la procédure suivante pour créer un accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-108">Use the following procedure to create a package accelerator.</span></span>

**<span data-ttu-id="cd3f7-109">Important</span><span class="sxs-lookup"><span data-stu-id="cd3f7-109">Important</span></span>**  
<span data-ttu-id="cd3f7-110">Les accélérateurs de package peuvent contenir des informations relatives aux mots de passe et aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-110">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="cd3f7-111">Par conséquent, vous devez enregistrer les accélérateurs de packages et le média d’installation associé dans un emplacement sécurisé, et vous devez signer numériquement l’accélérateur de package après l’avoir créé, afin que l’éditeur puisse être vérifié lorsque l’accélérateur de package App-V 5,0 est appliqué.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-111">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>



**<span data-ttu-id="cd3f7-112">Important</span><span class="sxs-lookup"><span data-stu-id="cd3f7-112">Important</span></span>**  
<span data-ttu-id="cd3f7-113">Avant de commencer la procédure suivante, vous devez effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="cd3f7-113">Before you begin the following procedure, you should perform the following:</span></span>

-   <span data-ttu-id="cd3f7-114">Copiez le package d’application virtuel que vous utiliserez pour créer l’accélérateur de package localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-114">Copy the virtual application package that you will use to create the package accelerator locally to the computer running the sequencer.</span></span>

-   <span data-ttu-id="cd3f7-115">Copiez tous les fichiers d’installation requis associés au package d’application virtuelle sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-115">Copy all required installation files associated with the virtual application package to the computer running the sequencer.</span></span>



**<span data-ttu-id="cd3f7-116">Pour créer un accélérateur de package</span><span class="sxs-lookup"><span data-stu-id="cd3f7-116">To create a package accelerator</span></span>**

1.  **<span data-ttu-id="cd3f7-117">Important</span><span class="sxs-lookup"><span data-stu-id="cd3f7-117">Important</span></span>**  
    <span data-ttu-id="cd3f7-118">Le Sequencer App-V 5,0 n’accorde aucun droit de licence à l’application logicielle utilisée pour créer l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-118">The App-V 5.0 Sequencer does not grant any license rights to the software application you are using to create the Package Accelerator.</span></span> <span data-ttu-id="cd3f7-119">Vous devez vous conformer aux termes du contrat de licence utilisateur final de l’application que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-119">You must abide by all end user license terms for the application you are using.</span></span> <span data-ttu-id="cd3f7-120">Il est de votre responsabilité de veiller à ce que les termes du contrat de licence de l’application logicielle vous permettent de créer un accélérateur de package à l’aide d’un Sequencer App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-120">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using App-V 5.0 Sequencer.</span></span>



~~~
To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="cd3f7-121">Pour démarrer l’Assistant Création d’un **accélérateur de package** de l’application-v 5,0, dans la console de Sequencer App-v 5,0, cliquez sur **Outils**  /  **créer un accélérateur**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-121">To start the App-V 5.0 **Create Package Accelerator** wizard, in the App-V 5.0 sequencer console, click **Tools** / **Create Accelerator**.</span></span>

3. <span data-ttu-id="cd3f7-122">Dans la page **Sélectionner un package** , pour spécifier un package d’application virtuelle existant à utiliser pour créer l’accélérateur de package, cliquez sur **Parcourir**, puis recherchez le package d’application virtuelle existant (fichier. AppV).</span><span class="sxs-lookup"><span data-stu-id="cd3f7-122">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.appv file).</span></span>

   **<span data-ttu-id="cd3f7-123">Astuce</span><span class="sxs-lookup"><span data-stu-id="cd3f7-123">Tip</span></span>**  
   <span data-ttu-id="cd3f7-124">Copiez les fichiers associés au package d’application virtuel que vous envisagez d’utiliser localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-124">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="cd3f7-125">Dans la page **fichiers d’installation** , pour spécifier le dossier contenant les fichiers d’installation que vous avez utilisés pour créer le package d’application virtuelle d’origine, cliquez sur **Parcourir**, puis sélectionnez le répertoire contenant les fichiers d’installation.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-125">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="cd3f7-126">Astuce</span><span class="sxs-lookup"><span data-stu-id="cd3f7-126">Tip</span></span>**  
   <span data-ttu-id="cd3f7-127">Copiez le dossier contenant les fichiers d’installation requis sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-127">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



5. <span data-ttu-id="cd3f7-128">Si l’application est déjà installée sur l’ordinateur exécutant le Sequencer, pour spécifier le fichier d’installation, sélectionnez les **fichiers installés sur le système local**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-128">If the application is already installed on the computer running the sequencer, to specify the installation file, select **Files installed on local system**.</span></span> <span data-ttu-id="cd3f7-129">Pour utiliser cette option, l’application doit déjà être installée dans l’emplacement d’installation par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-129">To use this option, the application must already be installed in the default installation location.</span></span>

6. <span data-ttu-id="cd3f7-130">Dans la page **collecte d’informations** , consultez les fichiers qui n’ont pas été trouvés dans l’emplacement spécifié dans la page fichiers d' **installation** de cet Assistant.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-130">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="cd3f7-131">Si les fichiers affichés ne sont pas obligatoires, sélectionnez **supprimer ces fichiers**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-131">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="cd3f7-132">Si les fichiers sont requis, cliquez sur **précédent** , puis copiez les fichiers requis dans le répertoire spécifié dans la page **fichiers d’installation** .</span><span class="sxs-lookup"><span data-stu-id="cd3f7-132">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="cd3f7-133">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd3f7-133">Note</span></span>**  
   <span data-ttu-id="cd3f7-134">Vous devez supprimer les fichiers non requis ou cliquer sur **précédent** , puis rechercher les fichiers requis pour passer à la page suivante de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-134">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



7. <span data-ttu-id="cd3f7-135">Dans la page **Sélectionner des fichiers** , passez en revue les fichiers qui ont été détectés et effacez les fichiers qui doivent être supprimés de l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-135">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the package accelerator.</span></span> <span data-ttu-id="cd3f7-136">Sélectionnez uniquement les fichiers nécessaires à l’exécution correcte de l’application, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-136">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

8. <span data-ttu-id="cd3f7-137">Dans la page **verify applications (vérifier les applications** ), vérifiez que tous les fichiers d’installation requis pour générer le package sont affichés.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-137">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="cd3f7-138">Lorsque l’accélérateur de package est utilisé pour créer un nouveau package, tous les fichiers d’installation affichés dans le volet **applications** sont requis pour créer le package.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-138">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="cd3f7-139">Si nécessaire, pour ajouter d’autres fichiers du programme d’installation, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-139">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="cd3f7-140">Pour supprimer les fichiers d’installation inutiles, sélectionnez le fichier d’installation, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-140">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="cd3f7-141">Pour modifier les propriétés associées à un programme d’installation, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-141">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="cd3f7-142">Les fichiers d’installation spécifiés dans cette étape seront nécessaires lorsque l’accélérateur de package sera utilisé pour créer un nouveau package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-142">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="cd3f7-143">Après confirmation des informations affichées, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-143">After you have confirmed the information displayed, click **Next**.</span></span>

9. <span data-ttu-id="cd3f7-144">Dans la page **Sélectionner des recommandations** , pour spécifier un fichier contenant des informations sur la façon dont l’accélérateur de package s’affiche, cliquez sur **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-144">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="cd3f7-145">Par exemple, ce fichier peut contenir des informations sur la façon dont l’ordinateur exécutant le Sequencer doit être configuré, les informations requises pour l’application pour les ordinateurs cibles et les notes générales.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-145">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="cd3f7-146">Vous devez fournir toutes les informations nécessaires à l’application de l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-146">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="cd3f7-147">Le fichier que vous sélectionnez doit être au format texte enrichi (. rtf) ou fichier texte (. txt).</span><span class="sxs-lookup"><span data-stu-id="cd3f7-147">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="cd3f7-148">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-148">Click **Next**.</span></span>

10. <span data-ttu-id="cd3f7-149">Dans la page **créer un accélérateur de package** , pour spécifier l’emplacement d’enregistrement de l’accélérateur de package, cliquez sur **Parcourir** , puis sélectionnez le répertoire.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-149">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

11. <span data-ttu-id="cd3f7-150">Dans la page **dernière étape** , cliquez sur **Fermer**pour fermer l’Assistant Création d’un **accélérateur de package** .</span><span class="sxs-lookup"><span data-stu-id="cd3f7-150">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="cd3f7-151">Important</span><span class="sxs-lookup"><span data-stu-id="cd3f7-151">Important</span></span>**  
   <span data-ttu-id="cd3f7-152">Pour vous assurer que le package Accelerator est le plus sécurisé possible et que l’éditeur puisse être vérifié lors de l’application de l’accélérateur de package, vous devez toujours signer numériquement l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="cd3f7-152">To help ensure that the package accelerator is as secure as possible, and so that the publisher can be verified when the package accelerator is applied, you should always digitally sign the package accelerator.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="cd3f7-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd3f7-153">Related topics</span></span>


[<span data-ttu-id="cd3f7-154">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="cd3f7-154">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="cd3f7-155">Comment créer un package d'application virtuelle à l'aide d'un accélérateur de package App-V</span><span class="sxs-lookup"><span data-stu-id="cd3f7-155">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)










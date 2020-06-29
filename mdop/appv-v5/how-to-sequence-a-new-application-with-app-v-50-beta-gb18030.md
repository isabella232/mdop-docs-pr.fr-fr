---
title: Comment séquencer une nouvelle application avec App-V5.0
description: Comment séquencer une nouvelle application avec App-V5.0
author: dansimp
ms.assetid: a263fa84-cd6d-4219-a5c2-eb6a553b826c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 13fdda066f79d918da1970e0cab6c1d6e60f6585
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805190"
---
# <span data-ttu-id="0dce9-103">Comment séquencer une nouvelle application avec App-V5.0</span><span class="sxs-lookup"><span data-stu-id="0dce9-103">How to Sequence a New Application with App-V 5.0</span></span>


**<span data-ttu-id="0dce9-104">Pour revoir ou faire avant de commencer à effectuer le séquençage</span><span class="sxs-lookup"><span data-stu-id="0dce9-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="0dce9-105">Déterminez le type de package d’application virtualisé que vous souhaitez créer:</span><span class="sxs-lookup"><span data-stu-id="0dce9-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0dce9-106">Type d’application</span><span class="sxs-lookup"><span data-stu-id="0dce9-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="0dce9-107">Description</span><span class="sxs-lookup"><span data-stu-id="0dce9-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0dce9-108">Standard</span><span class="sxs-lookup"><span data-stu-id="0dce9-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0dce9-109">Crée un package qui contient une application ou une suite d’applications.</span><span class="sxs-lookup"><span data-stu-id="0dce9-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="0dce9-110">Il s’agit de l’option la plus appropriée pour la plupart des types d’applications.</span><span class="sxs-lookup"><span data-stu-id="0dce9-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0dce9-111">Module complémentaire ou plug-in</span><span class="sxs-lookup"><span data-stu-id="0dce9-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0dce9-112">Crée un package qui étend les fonctionnalités d’une application standard, par exemple un plug-in pour Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0dce9-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="0dce9-113">De plus, vous pouvez utiliser les plug-ins pour les applications installées en mode natif ou pour un autre package lié à l’aide de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="0dce9-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0dce9-114">Intergiciels</span><span class="sxs-lookup"><span data-stu-id="0dce9-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0dce9-115">Crée un package requis par une application standard, par exemple Java.</span><span class="sxs-lookup"><span data-stu-id="0dce9-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="0dce9-116">Les packages middleware permettent de créer des liens vers d’autres packages à l’aide de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="0dce9-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="0dce9-117">Copiez tous les fichiers d’installation requis sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="0dce9-118">Créez une image de sauvegarde de votre environnement virtuel avant de séquencer une application, puis revenez à cette image dès que vous avez fini de Sequencer une application.</span><span class="sxs-lookup"><span data-stu-id="0dce9-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="0dce9-119">Passez en revue les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="0dce9-119">Review the following items:</span></span>

    -   <span data-ttu-id="0dce9-120">Si un programme d’installation de l’application modifie l’accès de sécurité à un fichier ou un répertoire existant nouveau ou existant, ces modifications ne sont pas capturées dans le package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="0dce9-121">Si des chemins d’accès courts ont été désactivés pour le volume cible du package virtualisé, vous devez également le faire sur un volume qui a été créé et dont la trajectoire courte est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0dce9-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="0dce9-122">Ne peut pas être le volume système.</span><span class="sxs-lookup"><span data-stu-id="0dce9-122">It cannot be the system volume.</span></span>

    -   <span data-ttu-id="0dce9-123">À compter de App-V 5,0 SP3, le répertoire principal de l’application virtuelle (PVAD) est masqué, mais vous pouvez le réactiver.</span><span class="sxs-lookup"><span data-stu-id="0dce9-123">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="0dce9-124">Voir [à propos de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="0dce9-124">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>

**<span data-ttu-id="0dce9-125">Pour séquencer une nouvelle application standard</span><span class="sxs-lookup"><span data-stu-id="0dce9-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="0dce9-126">Sur l’ordinateur qui exécute le Sequencer, cliquez sur **tous les programmes**, puis sur **virtualisation d’application Microsoft**, puis sur **Sequencer Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="0dce9-127">Dans le Sequencer, cliquez sur **créer un nouveau package d’application virtuel**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="0dce9-128">Sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="0dce9-129">Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou amener le package à contenir des données inutiles.</span><span class="sxs-lookup"><span data-stu-id="0dce9-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="0dce9-130">Vous devriez résoudre tous les problèmes potentiels avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="0dce9-131">Après avoir effectué des corrections, cliquez sur **Actualiser** pour afficher les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="0dce9-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="0dce9-132">Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-132">After you have resolved all potential issues, click **Next**.</span></span>

    **<span data-ttu-id="0dce9-133">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-133">Important</span></span>**  
    <span data-ttu-id="0dce9-134">Si vous êtes tenu de désactiver le logiciel antivirus, vous devez d’abord analyser l’ordinateur qui exécute le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-134">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4.  <span data-ttu-id="0dce9-135">Dans la page **type d’application** , activez la case à cocher **application standard (par défaut)** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-135">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5.  <span data-ttu-id="0dce9-136">Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="0dce9-136">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

    **<span data-ttu-id="0dce9-137">Remarque</span><span class="sxs-lookup"><span data-stu-id="0dce9-137">Note</span></span>**  
    <span data-ttu-id="0dce9-138">Si le programme d’installation de l’application spécifiée modifie l’accès de sécurité à un fichier ou un répertoire, existant ou nouveau, les modifications associées ne seront pas capturées dans le package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-138">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="0dce9-139">Dans la page **nom du package** , tapez un nom qui sera associé au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-139">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="0dce9-140">Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-140">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="0dce9-141">Le nom du package s’affiche dans la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0dce9-141">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="0dce9-142">Le **répertoire principal de l’application virtuelle** affiche le chemin sur lequel l’application sera installée sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="0dce9-142">The **Primary Virtual Application Directory** displays the path where the application will be installed on target computers.</span></span> <span data-ttu-id="0dce9-143">Pour spécifier cet emplacement, sélectionnez **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-143">To specify this location, select **Browse**.</span></span>

   **<span data-ttu-id="0dce9-144">Remarque</span><span class="sxs-lookup"><span data-stu-id="0dce9-144">Note</span></span>**  
   <span data-ttu-id="0dce9-145">À compter de App-V 5,0 SP3, le répertoire principal de l’application virtuelle (PVAD) est masqué, mais vous pouvez le réactiver.</span><span class="sxs-lookup"><span data-stu-id="0dce9-145">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="0dce9-146">Voir [à propos de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="0dce9-146">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
**Important**  
The primary application virtual directory should match the installation location for the application that is being sequenced. For example, if you install Notepad to **C:\\Program Files\\Notepad**; you should configure **C:\\Program Files\\Notepad** as your primary virtual directory. Alternatively, you can choose to set **C:\\Notepad** as the primary virtual application directory, as long as during installation time, you configure the installer to install to **C:\\Notepad**. Editing the Application Virtualization path is an advanced configuration task. For most applications, the default path is recommended for the following reasons:

-   Application Compatibility. Some virtualized applications will not function correctly, or will fail to open if the directories are not configured with identical virtual directory paths.

-   Performance. Since no file system redirection is required, the runtime performance can improve.



**Tip**  
It is recommended that prior to Sequencing an application, you open the associated installer to determine the default installation directory, and then configure that location as the **Primary Virtual Application Directory**.



Click **Next**.
~~~

7. <span data-ttu-id="0dce9-147">Dans la page d' **installation** , lorsque le processus de séquence et de programme d’installation de l’application est prêt, vous pouvez poursuivre l’installation de l’application afin que le Sequencer puisse surveiller le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="0dce9-147">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   **<span data-ttu-id="0dce9-148">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-148">Important</span></span>**  
   <span data-ttu-id="0dce9-149">Vous devez toujours installer des applications à un emplacement sécurisé et vérifier qu’aucun utilisateur n’est connecté à l’ordinateur exécutant le Sequencer lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="0dce9-149">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="0dce9-150">Dans la page **installation** , attendez que le Sequencer configure le package de l’application virtualisée.</span><span class="sxs-lookup"><span data-stu-id="0dce9-150">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="0dce9-151">Sur la page **configurer le logiciel** , exécutez éventuellement les programmes contenus dans le package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-151">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="0dce9-152">Cette étape vous permet d’effectuer toutes les tâches de configuration ou de licence nécessaires avant de déployer et d’exécuter le package sur des ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="0dce9-152">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="0dce9-153">Pour exécuter tous les programmes en une seule fois, sélectionnez au moins un programme, puis cliquez sur **exécuter tout**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-153">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="0dce9-154">Pour exécuter des programmes spécifiques, sélectionnez le ou les programmes, puis cliquez sur **exécuter la sélection**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-154">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="0dce9-155">Effectuez les tâches de configuration requises, puis fermez les applications.</span><span class="sxs-lookup"><span data-stu-id="0dce9-155">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="0dce9-156">Il est possible que vous deviez patienter quelques minutes pour que tous les programmes s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="0dce9-156">You may need to wait several minutes for all programs to run.</span></span>

   **<span data-ttu-id="0dce9-157">Remarque</span><span class="sxs-lookup"><span data-stu-id="0dce9-157">Note</span></span>**  
   <span data-ttu-id="0dce9-158">Pour exécuter les tâches de première utilisation pour toutes les applications qui ne sont pas disponibles dans la liste, ouvrez l’application.</span><span class="sxs-lookup"><span data-stu-id="0dce9-158">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="0dce9-159">Les informations associées seront capturées au cours de cette étape.</span><span class="sxs-lookup"><span data-stu-id="0dce9-159">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="0dce9-160">Dans la page **rapport d’installation** , vous pouvez passer en revue les informations relatives au package d’application virtualisé que vous venez de séquencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-160">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="0dce9-161">Dans **informations supplémentaires**, double-cliquez sur un événement pour obtenir des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="0dce9-161">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="0dce9-162">Pour continuer, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-162">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="0dce9-163">La page **personnaliser** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0dce9-163">The **Customize** page is displayed.</span></span> <span data-ttu-id="0dce9-164">Si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 14 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="0dce9-164">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="0dce9-165">Pour effectuer l’une des personnalisations suivantes, sélectionnez **personnaliser**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-165">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="0dce9-166">Préparez le package virtuel pour la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="0dce9-166">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="0dce9-167">La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="0dce9-167">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="0dce9-168">Spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-168">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="0dce9-169">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-169">Click **Next**.</span></span>

12. <span data-ttu-id="0dce9-170">Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="0dce9-170">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="0dce9-171">L’exécution de toutes les applications peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="0dce9-171">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="0dce9-172">Après l’exécution de toutes les applications, fermez chacune d’elles, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-172">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   **<span data-ttu-id="0dce9-173">Remarque</span><span class="sxs-lookup"><span data-stu-id="0dce9-173">Note</span></span>**  
   <span data-ttu-id="0dce9-174">Si vous n’ouvrez aucune application au cours de cette étape, la méthode de diffusion en continu par défaut est remise en continu à la demande.</span><span class="sxs-lookup"><span data-stu-id="0dce9-174">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="0dce9-175">Cela signifie que les applications sont téléchargées sur un bit pour pouvoir être ouvertes, puis en fonction de la configuration du chargement en arrière-plan, le reste de l’application sera chargé.</span><span class="sxs-lookup"><span data-stu-id="0dce9-175">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="0dce9-176">Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-176">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="0dce9-177">Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, sélectionnez **permettre l’exécution de ce package sur tout système d’exploitation**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-177">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="0dce9-178">Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, sélectionnez **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** et sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-178">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="0dce9-179">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-179">Click **Next**.</span></span>

   **<span data-ttu-id="0dce9-180">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-180">Important</span></span>**  
   <span data-ttu-id="0dce9-181">Assurez-vous que les systèmes d’exploitation que vous spécifiez ici sont pris en charge par l’application que vous séquençage.</span><span class="sxs-lookup"><span data-stu-id="0dce9-181">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="0dce9-182">La page **créer un package** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0dce9-182">The **Create Package** page is displayed.</span></span> <span data-ttu-id="0dce9-183">Pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de l’éditeur de package**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-183">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="0dce9-184">Cette option ouvre le package dans la console de Sequencer de sorte que vous puissiez modifier le package avant son enregistrement.</span><span class="sxs-lookup"><span data-stu-id="0dce9-184">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="0dce9-185">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-185">Click **Next**.</span></span>

   <span data-ttu-id="0dce9-186">Pour enregistrer le package immédiatement, sélectionnez **enregistrer le package maintenant** (par défaut).</span><span class="sxs-lookup"><span data-stu-id="0dce9-186">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="0dce9-187">Ajoutez des **Commentaires** facultatifs à associer au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-187">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="0dce9-188">Les commentaires sont utiles pour identifier la version du programme ainsi que d’autres informations sur le package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-188">Comments are useful for identifying the program version and other information about the package.</span></span>

   **<span data-ttu-id="0dce9-189">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-189">Important</span></span>**  
   <span data-ttu-id="0dce9-190">Le système ne prend pas en charge les caractères non imprimables dans les **Commentaires** et les **descriptions**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-190">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="0dce9-191">La page de **fin** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0dce9-191">The **Completion** page is displayed.</span></span> <span data-ttu-id="0dce9-192">Passez en revue les informations du volet **rapport de package d’application virtuel** selon vos besoins, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-192">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="0dce9-193">Ces informations sont également disponibles dans le fichier **Report.xml** situé dans le répertoire où le package a été créé.</span><span class="sxs-lookup"><span data-stu-id="0dce9-193">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="0dce9-194">Le package est désormais disponible dans le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-194">The package is now available in the sequencer.</span></span>

   **<span data-ttu-id="0dce9-195">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-195">Important</span></span>**  
   <span data-ttu-id="0dce9-196">Une fois que vous avez créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-196">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="0dce9-197">Pour séquencer une application de complément ou une application enfichable</span><span class="sxs-lookup"><span data-stu-id="0dce9-197">To sequence an add-on or plug-in application</span></span>**

1.  

    **<span data-ttu-id="0dce9-198">Remarque</span><span class="sxs-lookup"><span data-stu-id="0dce9-198">Note</span></span>**  
    <span data-ttu-id="0dce9-199">Avant d’exécuter la procédure suivante, installez l’application parente localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-199">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="0dce9-200">Ou si l’application parent est virtualisée, vous pouvez suivre les étapes décrites dans le flux de travail du module complémentaire ou du plug-in pour décompresser l’application parent sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0dce9-200">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>

    <span data-ttu-id="0dce9-201">Par exemple, si vous séquençagez un plug-in pour Microsoft Excel, installez Microsoft Excel localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-201">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="0dce9-202">Installez également l’application parente dans le même répertoire où l’application est installée sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="0dce9-202">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="0dce9-203">Si le plug-in ou le complément doit être utilisé avec un package d’application virtuelle existant, installez l’application sur le même lecteur d’application virtuel que celui utilisé lors de la création du package d’application virtuelle parent.</span><span class="sxs-lookup"><span data-stu-id="0dce9-203">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="0dce9-204">\*<strong><em>Dans le Sequencer, cliquez sur \* </em> créer un nouveau package d’application virtuel </strong> .</span><span class="sxs-lookup"><span data-stu-id="0dce9-204">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="0dce9-205">Sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-205">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="0dce9-206">Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou entraînent l’affichage de données inutiles par le package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-206">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="0dce9-207">Vous devriez résoudre tous les problèmes potentiels avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-207">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="0dce9-208">Après avoir effectué des corrections, cliquez sur **Actualiser** pour afficher les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="0dce9-208">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="0dce9-209">Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-209">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="0dce9-210">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-210">Important</span></span>**  
   <span data-ttu-id="0dce9-211">Si vous êtes tenu de désactiver le logiciel antivirus, vous devez d’abord analyser l’ordinateur qui exécute le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-211">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="0dce9-212">Dans la page **type d’application** , sélectionnez **composant additionnel ou plug-in**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-212">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="0dce9-213">Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’extension ou du plug-in.</span><span class="sxs-lookup"><span data-stu-id="0dce9-213">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="0dce9-214">Si le module complémentaire ou le plug-in n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-214">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="0dce9-215">Dans la page principale de l' **installation** , assurez-vous que l’application principale est installée sur l’ordinateur qui exécute le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-215">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="0dce9-216">Vous pouvez également développer un package existant qui a été enregistré localement sur l’ordinateur qui exécute le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-216">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="0dce9-217">Pour cela, cliquez sur **développer le package**, puis sélectionnez le package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-217">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="0dce9-218">Après avoir développé ou installé le programme parent, sélectionnez **j’ai installé le programme parent principal**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-218">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="0dce9-219">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-219">Click **Next**.</span></span>

7. <span data-ttu-id="0dce9-220">Dans la page **nom du package** , tapez un nom qui sera associé au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-220">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="0dce9-221">Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-221">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="0dce9-222">Le nom du package s’affiche dans la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0dce9-222">The package name will be displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="0dce9-223">Le **répertoire principal de l’application virtuelle** affiche le chemin sur lequel l’application sera installée.</span><span class="sxs-lookup"><span data-stu-id="0dce9-223">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="0dce9-224">Pour spécifier cet emplacement, tapez le chemin d’accès ou cliquez sur **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-224">To specify this location, type the path, or click **Browse**.</span></span>

   **<span data-ttu-id="0dce9-225">Remarque</span><span class="sxs-lookup"><span data-stu-id="0dce9-225">Note</span></span>**  
   <span data-ttu-id="0dce9-226">À compter de App-V 5,0 SP3, le répertoire principal de l’application virtuelle (PVAD) est masqué, mais vous pouvez le réactiver.</span><span class="sxs-lookup"><span data-stu-id="0dce9-226">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="0dce9-227">Voir [à propos de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="0dce9-227">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
Click **Next**.
~~~

8. <span data-ttu-id="0dce9-228">Dans la page **installation** , lorsque le Sequencer et le programme d’installation de l’application sont prêts, vous pouvez procéder à l’installation du plug-in ou de l’application de complément de sorte que le Sequencer puisse surveiller le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="0dce9-228">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="0dce9-229">Utilisez le processus d’installation de l’application pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="0dce9-229">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="0dce9-230">Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter** et recherchez et exécutez les fichiers d’installation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0dce9-230">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="0dce9-231">Lorsque l’installation est terminée, sélectionnez J’ai **terminé d’installer**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-231">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="0dce9-232">Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives au package d’application virtuel que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-232">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="0dce9-233">Pour obtenir une explication plus détaillée des informations affichées dans **informations supplémentaires**, double-cliquez sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="0dce9-233">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="0dce9-234">Après avoir consulté les informations, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-234">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="0dce9-235">La page **personnaliser** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0dce9-235">The **Customize** page is displayed.</span></span> <span data-ttu-id="0dce9-236">Si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 12 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="0dce9-236">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="0dce9-237">Pour effectuer l’une des personnalisations suivantes, sélectionnez **personnaliser**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-237">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="0dce9-238">Optimiser la façon dont le package s’exécutera sur un réseau lent ou peu fiable.</span><span class="sxs-lookup"><span data-stu-id="0dce9-238">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="0dce9-239">Spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-239">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="0dce9-240">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-240">Click **Next**.</span></span>

11. <span data-ttu-id="0dce9-241">Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="0dce9-241">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="0dce9-242">La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur des ordinateurs cibles sur des réseaux à latence élevée.</span><span class="sxs-lookup"><span data-stu-id="0dce9-242">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="0dce9-243">L’exécution de toutes les applications peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="0dce9-243">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="0dce9-244">Après l’exécution de toutes les applications, fermez chacune des applications.</span><span class="sxs-lookup"><span data-stu-id="0dce9-244">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="0dce9-245">Vous pouvez également configurer le package de manière à ce qu’il soit entièrement téléchargé avant ouverture en activant la case à cocher **forcer le téléchargement des applications** .</span><span class="sxs-lookup"><span data-stu-id="0dce9-245">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="0dce9-246">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-246">Click **Next**.</span></span>

   **<span data-ttu-id="0dce9-247">Remarque</span><span class="sxs-lookup"><span data-stu-id="0dce9-247">Note</span></span>**  
   <span data-ttu-id="0dce9-248">Le cas échéant, vous pouvez empêcher le chargement d’une application au cours de cette étape.</span><span class="sxs-lookup"><span data-stu-id="0dce9-248">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="0dce9-249">Dans la boîte de dialogue lancement de l' **application** , cliquez sur **arrêter** et sélectionnez l’une des cases à cocher: **arrêter toutes les applications** ou **arrêter cette application uniquement**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-249">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="0dce9-250">Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-250">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="0dce9-251">Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, activez la case à cocher **autoriser ce package à s’exécuter sur tous les systèmes d’exploitation** .</span><span class="sxs-lookup"><span data-stu-id="0dce9-251">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="0dce9-252">Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, activez la case à cocher **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** , puis sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-252">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="0dce9-253">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-253">Click **Next**.</span></span>

13. <span data-ttu-id="0dce9-254">La page **créer un package** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0dce9-254">The **Create Package** page is displayed.</span></span> <span data-ttu-id="0dce9-255">Pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de la** case à cocher éditeur de package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-255">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="0dce9-256">Cette option ouvre le package dans la console de Sequencer de sorte que vous puissiez modifier le package avant son enregistrement.</span><span class="sxs-lookup"><span data-stu-id="0dce9-256">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="0dce9-257">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-257">Click **Next**.</span></span>

   <span data-ttu-id="0dce9-258">Pour enregistrer le package immédiatement, sélectionnez **enregistrer le package maintenant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-258">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="0dce9-259">Vous pouvez également ajouter une **Description** qui sera associée au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-259">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="0dce9-260">Les descriptions sont utiles pour identifier la version et d’autres informations sur le package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-260">Descriptions are useful for identifying the version and other information about the package.</span></span>

   **<span data-ttu-id="0dce9-261">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-261">Important</span></span>**  
   <span data-ttu-id="0dce9-262">Le système ne prend pas en charge les caractères non imprimables dans les commentaires et les descriptions.</span><span class="sxs-lookup"><span data-stu-id="0dce9-262">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="0dce9-263">Pour séquencer une application middleware</span><span class="sxs-lookup"><span data-stu-id="0dce9-263">To sequence a middleware application</span></span>**

1. <span data-ttu-id="0dce9-264">Sur l’ordinateur qui exécute le Sequencer, cliquez sur **tous les programmes**, puis sur **virtualisation d’application Microsoft**, puis sur **Sequencer Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-264">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="0dce9-265">\*<strong><em>Dans le Sequencer, cliquez sur \* </em> créer un nouveau package d’application virtuel </strong> .</span><span class="sxs-lookup"><span data-stu-id="0dce9-265">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="0dce9-266">Sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-266">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="0dce9-267">Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou amener le package à contenir des données inutiles.</span><span class="sxs-lookup"><span data-stu-id="0dce9-267">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="0dce9-268">Vous devriez résoudre tous les problèmes potentiels avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-268">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="0dce9-269">Après avoir effectué des corrections, cliquez sur **Actualiser** pour afficher les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="0dce9-269">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="0dce9-270">Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-270">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="0dce9-271">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-271">Important</span></span>**  
   <span data-ttu-id="0dce9-272">Si vous avez besoin de désactiver le logiciel antivirus, vous devez commencer par analyser l’ordinateur qui exécute le Sequencer App-V 5,0 pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-272">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="0dce9-273">Dans la page **type d’application** , sélectionnez **middleware**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-273">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="0dce9-274">Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="0dce9-274">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="0dce9-275">Si l’application n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-275">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="0dce9-276">Dans la page **nom du package** , tapez un nom qui sera associé au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-276">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="0dce9-277">Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-277">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="0dce9-278">Le nom du package s’affiche dans la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0dce9-278">The package name is displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="0dce9-279">Le **répertoire principal de l’application virtuelle** affiche le chemin sur lequel l’application sera installée.</span><span class="sxs-lookup"><span data-stu-id="0dce9-279">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="0dce9-280">Pour spécifier cet emplacement, tapez le chemin d’accès ou cliquez sur **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-280">To specify this location, type the path or click **Browse**.</span></span>

   <span data-ttu-id="0dce9-281">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-281">Click **Next**.</span></span>

7. <span data-ttu-id="0dce9-282">Dans la page **installation** , lorsque le programme d’installation de Sequencer et de l’application middleware est prêt, vous pouvez continuer à installer l’application afin que le Sequencer puisse surveiller le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="0dce9-282">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="0dce9-283">Utilisez le processus d’installation de l’application pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="0dce9-283">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="0dce9-284">Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter**pour rechercher et exécuter les fichiers d’installation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0dce9-284">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="0dce9-285">Lorsque l’installation est terminée, activez la case à cocher **je suis fin** de l’installation, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-285">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="0dce9-286">Dans la page **installation** , attendez que le Sequencer configure le package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0dce9-286">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="0dce9-287">Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives au package d’application virtuel que vous venez de séquencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-287">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="0dce9-288">Dans **informations supplémentaires**, double-cliquez sur un événement pour obtenir des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="0dce9-288">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="0dce9-289">Pour continuer, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-289">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="0dce9-290">Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-290">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="0dce9-291">Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, activez la case à cocher **autoriser ce package à s’exécuter sur tous les systèmes d’exploitation** .</span><span class="sxs-lookup"><span data-stu-id="0dce9-291">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="0dce9-292">Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, activez la case à cocher **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** et sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-292">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="0dce9-293">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-293">Click **Next**.</span></span>

11. <span data-ttu-id="0dce9-294">Dans la page **créer un package** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0dce9-294">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="0dce9-295">Pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de l’éditeur de package**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-295">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="0dce9-296">Cette option ouvre le package dans la console de Sequencer de sorte que vous puissiez modifier le package avant son enregistrement.</span><span class="sxs-lookup"><span data-stu-id="0dce9-296">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="0dce9-297">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-297">Click **Next**.</span></span>

    <span data-ttu-id="0dce9-298">Pour enregistrer le package immédiatement, sélectionnez **enregistrer le package maintenant**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-298">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="0dce9-299">Vous pouvez également ajouter une **Description** à associer au package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-299">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="0dce9-300">Les descriptions sont utiles pour identifier la version du programme ainsi que d’autres informations sur le package.</span><span class="sxs-lookup"><span data-stu-id="0dce9-300">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    **<span data-ttu-id="0dce9-301">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-301">Important</span></span>**  
    <span data-ttu-id="0dce9-302">Le système ne prend pas en charge les caractères non imprimables dans les commentaires et les descriptions.</span><span class="sxs-lookup"><span data-stu-id="0dce9-302">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="0dce9-303">La page de **fin** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0dce9-303">The **Completion** page is displayed.</span></span> <span data-ttu-id="0dce9-304">Passez en revue les informations du volet **rapport de package d’application virtuel** selon vos besoins, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-304">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="0dce9-305">Ces informations sont également disponibles dans le fichier **Report.xml** qui se trouve dans le répertoire spécifié à l’étape 11 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="0dce9-305">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="0dce9-306">Le package est désormais disponible dans le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-306">The package is now available in the sequencer.</span></span> <span data-ttu-id="0dce9-307">Pour modifier les propriétés du package, cliquez sur **modifier \ [nom du package \]**.</span><span class="sxs-lookup"><span data-stu-id="0dce9-307">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   **<span data-ttu-id="0dce9-308">Important</span><span class="sxs-lookup"><span data-stu-id="0dce9-308">Important</span></span>**  
   <span data-ttu-id="0dce9-309">Une fois que vous avez créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0dce9-309">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="0dce9-310">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0dce9-310">Related topics</span></span>


[<span data-ttu-id="0dce9-311">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="0dce9-311">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)










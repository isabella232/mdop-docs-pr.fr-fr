---
title: Comment séquencer une nouvelle application avec App-V5.1
description: Comment séquencer une nouvelle application avec App-V5.1
author: dansimp
ms.assetid: 7d7699b1-0cb8-450d-94e7-5af937e16c21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43edd9357e31f4884ed7baec3d35fa01bf2abe54
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805185"
---
# <span data-ttu-id="a17d9-103">Comment séquencer une nouvelle application avec App-V5.1</span><span class="sxs-lookup"><span data-stu-id="a17d9-103">How to Sequence a New Application with App-V 5.1</span></span>


**<span data-ttu-id="a17d9-104">Pour revoir ou faire avant de commencer à effectuer le séquençage</span><span class="sxs-lookup"><span data-stu-id="a17d9-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="a17d9-105">Déterminez le type de package d’application virtualisé que vous souhaitez créer:</span><span class="sxs-lookup"><span data-stu-id="a17d9-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a17d9-106">Type d’application</span><span class="sxs-lookup"><span data-stu-id="a17d9-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="a17d9-107">Description</span><span class="sxs-lookup"><span data-stu-id="a17d9-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a17d9-108">Standard</span><span class="sxs-lookup"><span data-stu-id="a17d9-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a17d9-109">Crée un package qui contient une application ou une suite d’applications.</span><span class="sxs-lookup"><span data-stu-id="a17d9-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="a17d9-110">Il s’agit de l’option la plus appropriée pour la plupart des types d’applications.</span><span class="sxs-lookup"><span data-stu-id="a17d9-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a17d9-111">Module complémentaire ou plug-in</span><span class="sxs-lookup"><span data-stu-id="a17d9-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a17d9-112">Crée un package qui étend les fonctionnalités d’une application standard, par exemple un plug-in pour Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a17d9-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="a17d9-113">De plus, vous pouvez utiliser les plug-ins pour les applications installées en mode natif ou pour un autre package lié à l’aide de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="a17d9-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a17d9-114">Intergiciels</span><span class="sxs-lookup"><span data-stu-id="a17d9-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a17d9-115">Crée un package requis par une application standard, par exemple Java.</span><span class="sxs-lookup"><span data-stu-id="a17d9-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="a17d9-116">Les packages middleware permettent de créer des liens vers d’autres packages à l’aide de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="a17d9-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="a17d9-117">Copiez tous les fichiers d’installation requis sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="a17d9-118">Créez une image de sauvegarde de votre environnement virtuel avant de séquencer une application, puis revenez à cette image dès que vous avez fini de Sequencer une application.</span><span class="sxs-lookup"><span data-stu-id="a17d9-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="a17d9-119">Passez en revue les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="a17d9-119">Review the following items:</span></span>

    -   <span data-ttu-id="a17d9-120">Si un programme d’installation de l’application modifie l’accès de sécurité à un fichier ou un répertoire existant nouveau ou existant, ces modifications ne sont pas capturées dans le package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="a17d9-121">Si des chemins d’accès courts ont été désactivés pour le volume cible du package virtualisé, vous devez également le faire sur un volume qui a été créé et dont la trajectoire courte est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a17d9-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="a17d9-122">Ne peut pas être le volume système.</span><span class="sxs-lookup"><span data-stu-id="a17d9-122">It cannot be the system volume.</span></span>

> [!NOTE]  
> <span data-ttu-id="a17d9-123">Le Sequencer App-V 5. x ne peut pas séquencer des applications avec des noms de fichier correspondant à «CO_ &lt; x &gt; », où x est une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="a17d9-123">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="a17d9-124">Le 0x8007139F d’erreur est généré.</span><span class="sxs-lookup"><span data-stu-id="a17d9-124">Error 0x8007139F will be generated.</span></span>

**<span data-ttu-id="a17d9-125">Pour séquencer une nouvelle application standard</span><span class="sxs-lookup"><span data-stu-id="a17d9-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="a17d9-126">Sur l’ordinateur qui exécute le Sequencer, cliquez sur **tous les programmes**, puis sur **virtualisation d’application Microsoft**, puis sur **Sequencer Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="a17d9-127">Dans le Sequencer, cliquez sur **créer un nouveau package d’application virtuel**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="a17d9-128">Sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="a17d9-129">Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou amener le package à contenir des données inutiles.</span><span class="sxs-lookup"><span data-stu-id="a17d9-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="a17d9-130">Vous devriez résoudre tous les problèmes potentiels avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="a17d9-131">Après avoir effectué des corrections, cliquez sur **Actualiser** pour afficher les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="a17d9-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="a17d9-132">Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-132">After you have resolved all potential issues, click **Next**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a17d9-133">Si vous êtes tenu de désactiver le logiciel antivirus, vous devez d’abord analyser l’ordinateur qui exécute le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-133">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



~~~
> [!NOTE]  
> There is currently no way to disable Windows Defender in Windows 10. If you receive a warning, you can safely ignore it. It is unlikely that Windows Defender will affect sequencing at all.
~~~



4. <span data-ttu-id="a17d9-134">Dans la page **type d’application** , activez la case à cocher **application standard (par défaut)** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-134">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5. <span data-ttu-id="a17d9-135">Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="a17d9-135">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="a17d9-136">Si le programme d’installation de l’application spécifiée modifie l’accès de sécurité à un fichier ou un répertoire, existant ou nouveau, les modifications associées ne seront pas capturées dans le package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-136">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="a17d9-137">Dans la page **nom du package** , tapez un nom qui sera associé au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-137">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="a17d9-138">Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-138">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="a17d9-139">Le nom du package s’affiche dans la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a17d9-139">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="a17d9-140">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-140">Click **Next**.</span></span>

7. <span data-ttu-id="a17d9-141">Dans la page d' **installation** , lorsque le processus de séquence et de programme d’installation de l’application est prêt, vous pouvez poursuivre l’installation de l’application afin que le Sequencer puisse surveiller le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="a17d9-141">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a17d9-142">Vous devez toujours installer des applications à un emplacement sécurisé et vérifier qu’aucun utilisateur n’est connecté à l’ordinateur exécutant le Sequencer lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a17d9-142">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="a17d9-143">Dans la page **installation** , attendez que le Sequencer configure le package de l’application virtualisée.</span><span class="sxs-lookup"><span data-stu-id="a17d9-143">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="a17d9-144">Sur la page **configurer le logiciel** , exécutez éventuellement les programmes contenus dans le package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-144">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="a17d9-145">Cette étape vous permet d’effectuer toutes les tâches de configuration ou de licence nécessaires avant de déployer et d’exécuter le package sur des ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="a17d9-145">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="a17d9-146">Pour exécuter tous les programmes en une seule fois, sélectionnez au moins un programme, puis cliquez sur **exécuter tout**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-146">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="a17d9-147">Pour exécuter des programmes spécifiques, sélectionnez le ou les programmes, puis cliquez sur **exécuter la sélection**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-147">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="a17d9-148">Effectuez les tâches de configuration requises, puis fermez les applications.</span><span class="sxs-lookup"><span data-stu-id="a17d9-148">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="a17d9-149">Il est possible que vous deviez patienter quelques minutes pour que tous les programmes s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="a17d9-149">You may need to wait several minutes for all programs to run.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="a17d9-150">Pour exécuter les tâches de première utilisation pour toutes les applications qui ne sont pas disponibles dans la liste, ouvrez l’application.</span><span class="sxs-lookup"><span data-stu-id="a17d9-150">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="a17d9-151">Les informations associées seront capturées au cours de cette étape.</span><span class="sxs-lookup"><span data-stu-id="a17d9-151">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="a17d9-152">Dans la page **rapport d’installation** , vous pouvez passer en revue les informations relatives au package d’application virtualisé que vous venez de séquencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-152">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="a17d9-153">Dans **informations supplémentaires**, double-cliquez sur un événement pour obtenir des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="a17d9-153">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="a17d9-154">Pour continuer, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-154">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="a17d9-155">La page **personnaliser** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a17d9-155">The **Customize** page is displayed.</span></span> <span data-ttu-id="a17d9-156">Si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 14 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a17d9-156">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="a17d9-157">Pour effectuer l’une des personnalisations suivantes, sélectionnez **personnaliser**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-157">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="a17d9-158">Préparez le package virtuel pour la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="a17d9-158">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="a17d9-159">La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="a17d9-159">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="a17d9-160">Spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-160">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="a17d9-161">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-161">Click **Next**.</span></span>

12. <span data-ttu-id="a17d9-162">Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="a17d9-162">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="a17d9-163">L’exécution de toutes les applications peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="a17d9-163">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="a17d9-164">Après l’exécution de toutes les applications, fermez chacune d’elles, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-164">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="a17d9-165">Si vous n’ouvrez aucune application au cours de cette étape, la méthode de diffusion en continu par défaut est remise en continu à la demande.</span><span class="sxs-lookup"><span data-stu-id="a17d9-165">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="a17d9-166">Cela signifie que les applications sont téléchargées sur un bit pour pouvoir être ouvertes, puis en fonction de la configuration du chargement en arrière-plan, le reste de l’application sera chargé.</span><span class="sxs-lookup"><span data-stu-id="a17d9-166">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="a17d9-167">Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-167">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="a17d9-168">Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, sélectionnez **permettre l’exécution de ce package sur tout système d’exploitation**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-168">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="a17d9-169">Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, sélectionnez **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** et sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-169">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="a17d9-170">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-170">Click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a17d9-171">Assurez-vous que les systèmes d’exploitation que vous spécifiez ici sont pris en charge par l’application que vous séquençage.</span><span class="sxs-lookup"><span data-stu-id="a17d9-171">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="a17d9-172">La page **créer un package** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a17d9-172">The **Create Package** page is displayed.</span></span> <span data-ttu-id="a17d9-173">Pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de l’éditeur de package**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-173">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="a17d9-174">Cette option ouvre le package dans la console de Sequencer de sorte que vous puissiez modifier le package avant son enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a17d9-174">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="a17d9-175">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-175">Click **Next**.</span></span>

   <span data-ttu-id="a17d9-176">Pour enregistrer le package immédiatement, sélectionnez **enregistrer le package maintenant** (par défaut).</span><span class="sxs-lookup"><span data-stu-id="a17d9-176">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="a17d9-177">Ajoutez des **Commentaires** facultatifs à associer au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-177">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="a17d9-178">Les commentaires sont utiles pour identifier la version du programme ainsi que d’autres informations sur le package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-178">Comments are useful for identifying the program version and other information about the package.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a17d9-179">Le système ne prend pas en charge les caractères non imprimables dans les **Commentaires** et les **descriptions**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-179">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="a17d9-180">La page de **fin** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a17d9-180">The **Completion** page is displayed.</span></span> <span data-ttu-id="a17d9-181">Passez en revue les informations du volet **rapport de package d’application virtuel** selon vos besoins, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-181">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="a17d9-182">Ces informations sont également disponibles dans le fichier **Report.xml** situé dans le répertoire où le package a été créé.</span><span class="sxs-lookup"><span data-stu-id="a17d9-182">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="a17d9-183">Le package est désormais disponible dans le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-183">The package is now available in the sequencer.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a17d9-184">Une fois que vous avez créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-184">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="a17d9-185">Pour séquencer une application de complément ou une application enfichable</span><span class="sxs-lookup"><span data-stu-id="a17d9-185">To sequence an add-on or plug-in application</span></span>**

1. > [!NOTE]  
   > <span data-ttu-id="a17d9-186">Avant d’exécuter la procédure suivante, installez l’application parente localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-186">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="a17d9-187">Ou si l’application parent est virtualisée, vous pouvez suivre les étapes décrites dans le flux de travail du module complémentaire ou du plug-in pour décompresser l’application parent sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a17d9-187">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>
   >
   > <span data-ttu-id="a17d9-188">Par exemple, si vous séquençagez un plug-in pour Microsoft Excel, installez Microsoft Excel localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-188">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="a17d9-189">Installez également l’application parente dans le même répertoire où l’application est installée sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="a17d9-189">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="a17d9-190">Si le plug-in ou le complément doit être utilisé avec un package d’application virtuelle existant, installez l’application sur le même lecteur d’application virtuel que celui utilisé lors de la création du package d’application virtuelle parent.</span><span class="sxs-lookup"><span data-stu-id="a17d9-190">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="a17d9-191">\*<strong><em>Dans le Sequencer, cliquez sur \* </em> créer un nouveau package d’application virtuel </strong> .</span><span class="sxs-lookup"><span data-stu-id="a17d9-191">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="a17d9-192">Sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-192">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="a17d9-193">Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou entraînent l’affichage de données inutiles par le package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-193">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="a17d9-194">Vous devriez résoudre tous les problèmes potentiels avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-194">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="a17d9-195">Après avoir effectué des corrections, cliquez sur **Actualiser** pour afficher les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="a17d9-195">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="a17d9-196">Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-196">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a17d9-197">Si vous êtes tenu de désactiver le logiciel antivirus, vous devez d’abord analyser l’ordinateur qui exécute le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-197">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="a17d9-198">Dans la page **type d’application** , sélectionnez **composant additionnel ou plug-in**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-198">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="a17d9-199">Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’extension ou du plug-in.</span><span class="sxs-lookup"><span data-stu-id="a17d9-199">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="a17d9-200">Si le module complémentaire ou le plug-in n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-200">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="a17d9-201">Dans la page principale de l' **installation** , assurez-vous que l’application principale est installée sur l’ordinateur qui exécute le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-201">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="a17d9-202">Vous pouvez également développer un package existant qui a été enregistré localement sur l’ordinateur qui exécute le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-202">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="a17d9-203">Pour cela, cliquez sur **développer le package**, puis sélectionnez le package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-203">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="a17d9-204">Après avoir développé ou installé le programme parent, sélectionnez **j’ai installé le programme parent principal**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-204">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="a17d9-205">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-205">Click **Next**.</span></span>

7. <span data-ttu-id="a17d9-206">Dans la page **nom du package** , tapez un nom qui sera associé au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-206">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="a17d9-207">Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-207">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="a17d9-208">Le nom du package s’affiche dans la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a17d9-208">The package name will be displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="a17d9-209">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-209">Click **Next**.</span></span>

8. <span data-ttu-id="a17d9-210">Dans la page **installation** , lorsque le Sequencer et le programme d’installation de l’application sont prêts, vous pouvez procéder à l’installation du plug-in ou de l’application de complément de sorte que le Sequencer puisse surveiller le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="a17d9-210">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="a17d9-211">Utilisez le processus d’installation de l’application pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="a17d9-211">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="a17d9-212">Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter** et recherchez et exécutez les fichiers d’installation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a17d9-212">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="a17d9-213">Lorsque l’installation est terminée, sélectionnez J’ai **terminé d’installer**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-213">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="a17d9-214">Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives au package d’application virtuel que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-214">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="a17d9-215">Pour obtenir une explication plus détaillée des informations affichées dans **informations supplémentaires**, double-cliquez sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="a17d9-215">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="a17d9-216">Après avoir consulté les informations, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-216">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="a17d9-217">La page **personnaliser** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a17d9-217">The **Customize** page is displayed.</span></span> <span data-ttu-id="a17d9-218">Si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 12 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a17d9-218">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="a17d9-219">Pour effectuer l’une des personnalisations suivantes, sélectionnez **personnaliser**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-219">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="a17d9-220">Optimiser la façon dont le package s’exécutera sur un réseau lent ou peu fiable.</span><span class="sxs-lookup"><span data-stu-id="a17d9-220">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="a17d9-221">Spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-221">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="a17d9-222">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-222">Click **Next**.</span></span>

11. <span data-ttu-id="a17d9-223">Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="a17d9-223">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="a17d9-224">La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur des ordinateurs cibles sur des réseaux à latence élevée.</span><span class="sxs-lookup"><span data-stu-id="a17d9-224">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="a17d9-225">L’exécution de toutes les applications peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="a17d9-225">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="a17d9-226">Après l’exécution de toutes les applications, fermez chacune des applications.</span><span class="sxs-lookup"><span data-stu-id="a17d9-226">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="a17d9-227">Vous pouvez également configurer le package de manière à ce qu’il soit entièrement téléchargé avant ouverture en activant la case à cocher **forcer le téléchargement des applications** .</span><span class="sxs-lookup"><span data-stu-id="a17d9-227">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="a17d9-228">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-228">Click **Next**.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="a17d9-229">Le cas échéant, vous pouvez empêcher le chargement d’une application au cours de cette étape.</span><span class="sxs-lookup"><span data-stu-id="a17d9-229">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="a17d9-230">Dans la boîte de dialogue lancement de l' **application** , cliquez sur **arrêter** et sélectionnez l’une des cases à cocher: **arrêter toutes les applications** ou **arrêter cette application uniquement**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-230">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="a17d9-231">Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-231">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="a17d9-232">Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, activez la case à cocher **autoriser ce package à s’exécuter sur tous les systèmes d’exploitation** .</span><span class="sxs-lookup"><span data-stu-id="a17d9-232">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="a17d9-233">Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, activez la case à cocher **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** , puis sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-233">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="a17d9-234">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-234">Click **Next**.</span></span>

13. <span data-ttu-id="a17d9-235">La page **créer un package** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a17d9-235">The **Create Package** page is displayed.</span></span> <span data-ttu-id="a17d9-236">Pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de la** case à cocher éditeur de package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-236">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="a17d9-237">Cette option ouvre le package dans la console de Sequencer de sorte que vous puissiez modifier le package avant son enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a17d9-237">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="a17d9-238">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-238">Click **Next**.</span></span>

    <span data-ttu-id="a17d9-239">Pour enregistrer le package immédiatement, sélectionnez **enregistrer le package maintenant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-239">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="a17d9-240">Vous pouvez également ajouter une **Description** qui sera associée au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-240">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="a17d9-241">Les descriptions sont utiles pour identifier la version et d’autres informations sur le package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-241">Descriptions are useful for identifying the version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a17d9-242">Le système ne prend pas en charge les caractères non imprimables dans les commentaires et les descriptions.</span><span class="sxs-lookup"><span data-stu-id="a17d9-242">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="a17d9-243">Pour séquencer une application middleware</span><span class="sxs-lookup"><span data-stu-id="a17d9-243">To sequence a middleware application</span></span>**

1. <span data-ttu-id="a17d9-244">Sur l’ordinateur qui exécute le Sequencer, cliquez sur **tous les programmes**, puis sur **virtualisation d’application Microsoft**, puis sur **Sequencer Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-244">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="a17d9-245">\*<strong><em>Dans le Sequencer, cliquez sur \* </em> créer un nouveau package d’application virtuel </strong> .</span><span class="sxs-lookup"><span data-stu-id="a17d9-245">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="a17d9-246">Sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-246">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="a17d9-247">Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou amener le package à contenir des données inutiles.</span><span class="sxs-lookup"><span data-stu-id="a17d9-247">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="a17d9-248">Vous devriez résoudre tous les problèmes potentiels avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-248">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="a17d9-249">Après avoir effectué des corrections, cliquez sur **Actualiser** pour afficher les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="a17d9-249">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="a17d9-250">Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-250">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a17d9-251">Si vous avez besoin de désactiver le logiciel antivirus, vous devez commencer par analyser l’ordinateur qui exécute le Sequencer App-V 5,0 pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-251">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="a17d9-252">Dans la page **type d’application** , sélectionnez **middleware**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-252">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="a17d9-253">Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="a17d9-253">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="a17d9-254">Si l’application n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-254">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="a17d9-255">Dans la page **nom du package** , tapez un nom qui sera associé au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-255">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="a17d9-256">Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-256">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="a17d9-257">Le nom du package s’affiche dans la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a17d9-257">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="a17d9-258">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-258">Click **Next**.</span></span>

7. <span data-ttu-id="a17d9-259">Dans la page **installation** , lorsque le programme d’installation de Sequencer et de l’application middleware est prêt, vous pouvez continuer à installer l’application afin que le Sequencer puisse surveiller le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="a17d9-259">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="a17d9-260">Utilisez le processus d’installation de l’application pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="a17d9-260">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="a17d9-261">Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter**pour rechercher et exécuter les fichiers d’installation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a17d9-261">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="a17d9-262">Lorsque l’installation est terminée, activez la case à cocher **je suis fin** de l’installation, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-262">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="a17d9-263">Dans la page **installation** , attendez que le Sequencer configure le package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a17d9-263">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="a17d9-264">Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives au package d’application virtuel que vous venez de séquencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-264">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="a17d9-265">Dans **informations supplémentaires**, double-cliquez sur un événement pour obtenir des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="a17d9-265">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="a17d9-266">Pour continuer, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-266">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="a17d9-267">Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-267">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="a17d9-268">Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, activez la case à cocher **autoriser ce package à s’exécuter sur tous les systèmes d’exploitation** .</span><span class="sxs-lookup"><span data-stu-id="a17d9-268">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="a17d9-269">Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, activez la case à cocher **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** et sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-269">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="a17d9-270">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-270">Click **Next**.</span></span>

11. <span data-ttu-id="a17d9-271">Dans la page **créer un package** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a17d9-271">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="a17d9-272">Pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de l’éditeur de package**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-272">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="a17d9-273">Cette option ouvre le package dans la console de Sequencer de sorte que vous puissiez modifier le package avant son enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a17d9-273">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="a17d9-274">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-274">Click **Next**.</span></span>

    <span data-ttu-id="a17d9-275">Pour enregistrer le package immédiatement, sélectionnez **enregistrer le package maintenant**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-275">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="a17d9-276">Vous pouvez également ajouter une **Description** à associer au package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-276">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="a17d9-277">Les descriptions sont utiles pour identifier la version du programme ainsi que d’autres informations sur le package.</span><span class="sxs-lookup"><span data-stu-id="a17d9-277">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a17d9-278">Le système ne prend pas en charge les caractères non imprimables dans les commentaires et les descriptions.</span><span class="sxs-lookup"><span data-stu-id="a17d9-278">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="a17d9-279">La page de **fin** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a17d9-279">The **Completion** page is displayed.</span></span> <span data-ttu-id="a17d9-280">Passez en revue les informations du volet **rapport de package d’application virtuel** selon vos besoins, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-280">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="a17d9-281">Ces informations sont également disponibles dans le fichier **Report.xml** qui se trouve dans le répertoire spécifié à l’étape 11 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a17d9-281">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="a17d9-282">Le package est désormais disponible dans le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-282">The package is now available in the sequencer.</span></span> <span data-ttu-id="a17d9-283">Pour modifier les propriétés du package, cliquez sur **modifier \ [nom du package \]**.</span><span class="sxs-lookup"><span data-stu-id="a17d9-283">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a17d9-284">Une fois que vous avez créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a17d9-284">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="a17d9-285">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a17d9-285">Related topics</span></span>


[<span data-ttu-id="a17d9-286">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="a17d9-286">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)










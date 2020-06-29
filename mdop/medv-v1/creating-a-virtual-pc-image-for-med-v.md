---
title: Création d'une image Virtual PC pour MED-V
description: Création d'une image Virtual PC pour MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810091"
---
# <span data-ttu-id="3fe4f-103">Création d'une image Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="3fe4f-103">Creating a Virtual PC Image for MED-V</span></span>


<span data-ttu-id="3fe4f-104">Pour créer une image Virtual PC (VPC) pour MED-V, vous devez effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-104">To create a Virtual PC (VPC) image for MED-V, you must perform the following:</span></span>

1.  <span data-ttu-id="3fe4f-105">[Créer une image de VPC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-105">[Create a VPC image](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span></span>

2.  <span data-ttu-id="3fe4f-106">[Installez le package MED-V Workspace. msi sur l’image VPC](#bkmk-howtoinstallthemedvworkspacemsipackage).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-106">[Install the MED-V workspace .msi package onto the VPC image](#bkmk-howtoinstallthemedvworkspacemsipackage).</span></span>

3.  <span data-ttu-id="3fe4f-107">[Exécutez l’outil de configuration de l’ordinateur virtuel MED-V sur l’image VPC](#bkmk-howtorunthevirtualmachineprerequisitestool).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-107">[Run the MED-V virtual machine prerequisites tool on the VPC image](#bkmk-howtorunthevirtualmachineprerequisitestool).</span></span>

4.  <span data-ttu-id="3fe4f-108">[Configurez manuellement les composants requis pour les machines virtuelles sur l’image VPC](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-108">[Manually configure virtual machine prerequisites on the VPC image](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span></span>

5.  <span data-ttu-id="3fe4f-109">[Configurez Sysprep pour les images MED-V](#bkmk-howtoconfiguresysprepformedvimages) (facultatif).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-109">[Configure Sysprep for MED-V images](#bkmk-howtoconfiguresysprepformedvimages) (optional).</span></span>

6.  <span data-ttu-id="3fe4f-110">[Désactivez Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-110">[Turn off Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span></span>

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="3fe4f-111">Création d’une image Virtual PC à l’aide de Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3fe4f-111">Creating a Virtual PC Image by Using Microsoft Virtual PC</span></span>


<span data-ttu-id="3fe4f-112">Pour créer une image Virtual PC à l’aide de Microsoft Virtual PC, reportez-vous à la documentation sur le PC virtuel.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-112">To create a Virtual PC image using Microsoft Virtual PC, refer to the Virtual PC documentation.</span></span>

<span data-ttu-id="3fe4f-113">Pour plus d'informations, reportez-vous aux éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-113">For more information, see the following:</span></span>

-   [<span data-ttu-id="3fe4f-114">Aide sur Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3fe4f-114">Windows Virtual PC Help</span></span>](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [<span data-ttu-id="3fe4f-115">Créer une machine virtuelle et installer un système d’exploitation invité</span><span class="sxs-lookup"><span data-stu-id="3fe4f-115">Create a virtual machine and install a guest operating system</span></span>](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a><span data-ttu-id="3fe4f-116">Installer le package MED-V Workspace. msi</span><span class="sxs-lookup"><span data-stu-id="3fe4f-116">How to Install the MED-V Workspace .msi Package</span></span>


<span data-ttu-id="3fe4f-117">Une fois l’image du PC virtuel créée, installez le package MED-V Workspace. msi sur l’image.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-117">After the Virtual PC image is created, install the MED-V workspace .msi package onto the image.</span></span>

**<span data-ttu-id="3fe4f-118">Pour installer l’image d’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="3fe4f-118">To install the MED-V workspace image</span></span>**

1.  <span data-ttu-id="3fe4f-119">Démarrez l’ordinateur virtuel et copiez le package MED-V Workspace. msi dans.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-119">Start the virtual machine, and copy the MED-V workspace .msi package inside.</span></span>

    <span data-ttu-id="3fe4f-120">Le package MED-V Workspace. msi est appelé *MED-V\_workspace\_x.msi*, où *x* correspond au numéro de version.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-120">The MED-V workspace .msi package is called *MED-V\_workspace\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="3fe4f-121">Par exemple, *MED-V\_workspace\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-121">For example, *MED-V\_workspace\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="3fe4f-122">Double-cliquez sur le package MED-V Workspace. msi, puis suivez les instructions de l’Assistant installation.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-122">Double-click the MED-V workspace .msi package, and follow the installation wizard instructions.</span></span>

    **<span data-ttu-id="3fe4f-123">Remarque</span><span class="sxs-lookup"><span data-stu-id="3fe4f-123">Note</span></span>**  
    <span data-ttu-id="3fe4f-124">Lorsque vous relâchez une nouvelle version MED-V et qu’une image virtuelle de votre PC est mise à jour, désinstallez le package d’espace de travail MED-V de l’ordinateur existant, redémarrez l’ordinateur, puis installez le nouveau package MED-V Workspace. msi.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-124">When a new MED-V version is released, and an existing Virtual PC image is updated, uninstall the existing MED-V workspace .msi package, reboot the computer, and install the new MED-V workspace .msi package.</span></span>



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a><span data-ttu-id="3fe4f-125">Exécution de l’outil Configuration requise pour les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="3fe4f-125">How to Run the Virtual Machine Prerequisites Tool</span></span>


<span data-ttu-id="3fe4f-126">L’outil Configuration requise pour machine virtuelle (VM) est un assistant qui permet d’automatiser plusieurs des éléments requis.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-126">The virtual machine (VM) prerequisites tool is a wizard that automates several of the prerequisites.</span></span>

**<span data-ttu-id="3fe4f-127">Remarque</span><span class="sxs-lookup"><span data-stu-id="3fe4f-127">Note</span></span>**  
<span data-ttu-id="3fe4f-128">Bien que de nombreux paramètres soient configurables dans l’Assistant, les propriétés requises pour le bon fonctionnement de MED-V ne sont pas configurées.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-128">Although many parameters are configurable in the wizard, the properties required for the proper functioning of MED-V are not configurable.</span></span>



**<span data-ttu-id="3fe4f-129">Pour exécuter l’outil Configuration requise pour les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="3fe4f-129">To run the virtual machine prerequisites tool</span></span>**

1.  <span data-ttu-id="3fe4f-130">Une fois le package d’espace de travail MED-V installé, dans le menu **Démarrer** de Windows, sélectionnez \*\*tous les programmes &gt; &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-130">After the MED-V workspace .msi package is installed, on the Windows **Start** menu, select **All Programs &gt; MED-V &gt; VM Prerequisites Tool**.</span></span>

    **<span data-ttu-id="3fe4f-131">Remarque</span><span class="sxs-lookup"><span data-stu-id="3fe4f-131">Note</span></span>**  
    <span data-ttu-id="3fe4f-132">L’utilisateur exécutant l’outil Configuration requise pour les machines virtuelles doit disposer de droits d’administrateur local et doit être le seul utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-132">The user running the virtual machine prerequisites tool must have local administrator rights and must be the only user logged in.</span></span>



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. <span data-ttu-id="3fe4f-133">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-133">Click **Next**.</span></span>

3. <span data-ttu-id="3fe4f-134">Dans la page **Paramètres Windows** , à partir des propriétés configurables suivantes, sélectionnez celles que vous souhaitez configurer:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-134">On the **Windows Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="3fe4f-135">Effacement des informations de l’historique personnel de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3fe4f-135">Clear users’ personal history information</span></span>**

   -   **<span data-ttu-id="3fe4f-136">Vider le répertoire temporaire des profils locaux</span><span class="sxs-lookup"><span data-stu-id="3fe4f-136">Clear local profiles temp directory</span></span>**

   -   **<span data-ttu-id="3fe4f-137">Désactiver les sons sur les événements Windows suivants: démarrage, ouverture de session</span><span class="sxs-lookup"><span data-stu-id="3fe4f-137">Disable sounds on following Windows events: start, logon, logoff</span></span>**

   **<span data-ttu-id="3fe4f-138">Remarque</span><span class="sxs-lookup"><span data-stu-id="3fe4f-138">Note</span></span>**  
   <span data-ttu-id="3fe4f-139">Ne l’activez pas dans une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-139">Do not enable Windows page saver in a group policy.</span></span>



4. <span data-ttu-id="3fe4f-140">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-140">Click **Next**.</span></span>

5. <span data-ttu-id="3fe4f-141">Dans la page **paramètres d’Internet Explorer** , à partir des propriétés configurables suivantes, sélectionnez celles que vous souhaitez configurer:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-141">On the **Internet Explorer Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="3fe4f-142">Ne pas utiliser les fonctionnalités de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="3fe4f-142">Don't use auto complete features</span></span>**

   -   **<span data-ttu-id="3fe4f-143">Désactiver la réutilisation de Windows pour les raccourcis de lancement</span><span class="sxs-lookup"><span data-stu-id="3fe4f-143">Disable reuse of windows for launching shortcuts</span></span>**

   -   **<span data-ttu-id="3fe4f-144">Effacer l’historique de navigation</span><span class="sxs-lookup"><span data-stu-id="3fe4f-144">Clear browsing history</span></span>**

   -   **<span data-ttu-id="3fe4f-145">Activation de la navigation par onglets dans Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="3fe4f-145">Enable tabbed browsing in Internet Explorer 7</span></span>**

6. <span data-ttu-id="3fe4f-146">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-146">Click **Next**.</span></span>

7. <span data-ttu-id="3fe4f-147">Dans la page **services Windows** , à partir des propriétés configurables suivantes, sélectionnez celles que vous souhaitez configurer:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-147">On the **Windows Services** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="3fe4f-148">Service du centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="3fe4f-148">Security center service</span></span>**

   -   **<span data-ttu-id="3fe4f-149">Service du planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="3fe4f-149">Task scheduler service</span></span>**

   -   **<span data-ttu-id="3fe4f-150">Service mises à jour automatiques</span><span class="sxs-lookup"><span data-stu-id="3fe4f-150">Automatic updates service</span></span>**

   -   **<span data-ttu-id="3fe4f-151">Service de restauration du système</span><span class="sxs-lookup"><span data-stu-id="3fe4f-151">System restore service</span></span>**

   -   **<span data-ttu-id="3fe4f-152">Service d’indexation</span><span class="sxs-lookup"><span data-stu-id="3fe4f-152">Indexing service</span></span>**

   -   **<span data-ttu-id="3fe4f-153">Configuration automatique sans fil</span><span class="sxs-lookup"><span data-stu-id="3fe4f-153">Wireless Zero Configuration</span></span>**

   -   **<span data-ttu-id="3fe4f-154">Compatibilité rapide du changement d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3fe4f-154">Fast User Switching Compatibility</span></span>**

8. <span data-ttu-id="3fe4f-155">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-155">Click **Next**.</span></span>

9. <span data-ttu-id="3fe4f-156">Dans la page de **connexion automatique Windows** , procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-156">On the **Windows Auto Logon** page, do the following:</span></span>

   1.  <span data-ttu-id="3fe4f-157">Cochez la case **activer la connexion automatique Windows** .</span><span class="sxs-lookup"><span data-stu-id="3fe4f-157">Select the **Enable Windows Auto Logon** check box.</span></span>

   2.  <span data-ttu-id="3fe4f-158">Attribuez un **nom d’utilisateur** et un **mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-158">Assign a **User name** and **Password**.</span></span>

10. <span data-ttu-id="3fe4f-159">Cliquez sur **appliquer**, puis, dans la boîte de confirmation qui s’affiche, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-159">Click **Apply**, and in the confirmation box that appears, click **Yes**.</span></span>

11. <span data-ttu-id="3fe4f-160">Dans la page **Résumé** , cliquez sur **Terminer** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-160">On the **Summary** page, click **Finish** to quit the wizard</span></span>

**<span data-ttu-id="3fe4f-161">Remarque</span><span class="sxs-lookup"><span data-stu-id="3fe4f-161">Note</span></span>**  
<span data-ttu-id="3fe4f-162">Vérifiez que les stratégies de groupe n’écrasent pas les paramètres obligatoires définis dans l’outil éléments requis.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-162">Verify that group policies do not overwrite the mandatory settings set in the prerequisites tool.</span></span>



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a><span data-ttu-id="3fe4f-163">Comment configurer les conditions préalables à l’installation manuelle de l’ordinateur virtuel MED-V</span><span class="sxs-lookup"><span data-stu-id="3fe4f-163">How to Configure MED-V Virtual Machine Manual Installation Prerequisites</span></span>


<span data-ttu-id="3fe4f-164">Plusieurs configurations ne peuvent pas être configurées par le biais de l’outil Configuration requise pour les machines virtuelles et doivent être effectuées manuellement.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-164">Several of the configurations cannot be configured through the virtual machine prerequisites tool and must be performed manually.</span></span>

-   <span data-ttu-id="3fe4f-165">Paramètres d’ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="3fe4f-165">Virtual Machine Settings</span></span>

    <span data-ttu-id="3fe4f-166">Il est recommandé de configurer les paramètres d’ordinateur virtuel suivants dans la console Microsoft Virtual PC:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-166">It is recommended to configure the following virtual machine settings in the Microsoft Virtual PC console:</span></span>

    -   <span data-ttu-id="3fe4f-167">Désactivez les lecteurs de disquette.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-167">Disable floppy disk drives.</span></span>

    -   <span data-ttu-id="3fe4f-168">Désactivez annuler-Disks (**paramètres d' &gt; annulation de paramètres**).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-168">Disable undo-disks (**Settings &gt; undo-disks**).</span></span>

    -   <span data-ttu-id="3fe4f-169">Assurez-vous que l’image est dotée d’un seul processeur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-169">Ensure that the image has only one virtual CPU.</span></span>

    -   <span data-ttu-id="3fe4f-170">Éliminez les interactions entre la machine virtuelle et l’utilisateur, où elles ne sont pas liées aux applications publiées (par exemple, les messages nécessitant des entrées de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-170">Eliminate interactions between the virtual machine and the user, where they are not related to published applications (such as, messages requiring user input).</span></span>

-   <span data-ttu-id="3fe4f-171">Paramètres d’image</span><span class="sxs-lookup"><span data-stu-id="3fe4f-171">Image Settings</span></span>

    <span data-ttu-id="3fe4f-172">Configurez les paramètres manuels suivants dans l’image:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-172">Configure the following manual settings inside the image:</span></span>

    1.  <span data-ttu-id="3fe4f-173">Dans la fenêtre **Propriétés de Power Options** , désactivez l’option mise en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-173">In the **Power Options Properties** window, disable hibernation and sleep.</span></span>

    2.  <span data-ttu-id="3fe4f-174">Appliquez les mises à jour Windows les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-174">Apply the most recent Windows updates.</span></span>

    3.  <span data-ttu-id="3fe4f-175">Dans la boîte de dialogue **démarrage et récupération de Windows** , dans la section **échec du système** , décochez la case **redémarrer automatiquement** .</span><span class="sxs-lookup"><span data-stu-id="3fe4f-175">In the **Windows Startup and Recovery** dialog box, in the **System Failure** section, clear the **Automatically restart** check box.</span></span>

    4.  <span data-ttu-id="3fe4f-176">Assurez-vous que l’image utilise une clé de licence VLK.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-176">Ensure that the image uses a VLK license key.</span></span>

-   <span data-ttu-id="3fe4f-177">Installation des compléments VPC</span><span class="sxs-lookup"><span data-stu-id="3fe4f-177">Installing VPC Additions</span></span>

    <span data-ttu-id="3fe4f-178">Dans le menu **action** , sélectionnez **installer ou mettre à jour les compléments d’ordinateurs virtuels**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-178">On the **Action** menu, select **Install or Update Virtual Machine Additions**.</span></span>

-   <span data-ttu-id="3fe4f-179">Configuration de l’impression</span><span class="sxs-lookup"><span data-stu-id="3fe4f-179">Configuring Printing</span></span>

    <span data-ttu-id="3fe4f-180">Vous pouvez configurer l’impression à partir de l’espace de travail MED-V de l’une des façons suivantes:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-180">You can configure printing from the MED-V workspace in either of the following ways:</span></span>

    -   <span data-ttu-id="3fe4f-181">Ajoutez une imprimante à l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-181">Add a printer to the virtual machine.</span></span>

    -   <span data-ttu-id="3fe4f-182">Autorisez l’impression avec les imprimantes configurées sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-182">Allow printing with printers that are configured on the host computer.</span></span>

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a><span data-ttu-id="3fe4f-183">Configuration de Sysprep pour les images MED-V</span><span class="sxs-lookup"><span data-stu-id="3fe4f-183">How to Configure Sysprep for MED-V Images</span></span>


<span data-ttu-id="3fe4f-184">Dans un espace de travail MED-V, Sysprep peut être configuré afin d’affecter un ID de sécurité unique, en particulier lorsque plusieurs espaces de travail MED-V sont exécutés sur un seul ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-184">In a MED-V workspace, Sysprep can be configured in order to assign unique security ID (SID), particularly when multiple MED-V workspaces are run on a single computer.</span></span> <span data-ttu-id="3fe4f-185">Il n’est pas recommandé d’utiliser Sysprep pour rejoindre un domaine. au lieu de cela, utilisez l’action de script de participation de l’utilisateur MED-V, comme décrit dans [la rubrique Configurer les actions de script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-185">It is not recommended to use Sysprep to join a domain; instead, use the MED-V join domain script action as described in [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

**<span data-ttu-id="3fe4f-186">Remarque</span><span class="sxs-lookup"><span data-stu-id="3fe4f-186">Note</span></span>**  
<span data-ttu-id="3fe4f-187">Sysprep est l’utilitaire de préparation système de Microsoft pour le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-187">Sysprep is Microsoft's system preparation utility for the Windows operating system.</span></span>



**<span data-ttu-id="3fe4f-188">Pour configurer Sysprep dans un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="3fe4f-188">To configure Sysprep in a MED-V workspace</span></span>**

1.  <span data-ttu-id="3fe4f-189">Créez un répertoire à la racine du lecteur système nommé *Sysprep*.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-189">Create a directory in the root of the system drive named *Sysprep*.</span></span>

2.  <span data-ttu-id="3fe4f-190">Sur le CD d’installation Windows, extrayez les *deploy.cab* à la racine du lecteur système ou téléchargez la mise à jour des outils de déploiement les plus récents à partir du site Web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-190">From the Windows installation CD, extract *deploy.cab* to the root of the system drive, or download the latest Deployment Tools update from the Microsoft Web site.</span></span>

    -   <span data-ttu-id="3fe4f-191">Pour Windows 2000, voir [mise à jour des outils de déploiement pour windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-191">For Windows 2000, see [Deployment Tools update for Windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span></span>

    -   <span data-ttu-id="3fe4f-192">Pour Windows XP, voir [mise à jour des outils de déploiement pour Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-192">For Windows XP, see [Deployment Tools update for Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span></span>

3.  <span data-ttu-id="3fe4f-193">Exécutez **le gestionnaire d’installation** (setupmgr.exe).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-193">Run **Setup Manager** (setupmgr.exe).</span></span>

4.  <span data-ttu-id="3fe4f-194">Suivez la procédure de l’Assistant gestion de l’installation.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-194">Follow the Setup Manager wizard.</span></span>

<span data-ttu-id="3fe4f-195">Une fois Sysprep configuré et l’espace de travail MED-V créé, Sysprep doit être exécuté.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-195">After Sysprep is configured and the MED-V workspace is created, Sysprep must be executed.</span></span>

**<span data-ttu-id="3fe4f-196">Pour exécuter Sysprep</span><span class="sxs-lookup"><span data-stu-id="3fe4f-196">To run Sysprep</span></span>**

1.  <span data-ttu-id="3fe4f-197">À partir du dossier Sysprep situé à la racine du lecteur système, exécutez l’outil de préparation du système (Sysprep.exe).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-197">From the Sysprep folder located in the root of the system drive, run the System Preparation Tool (Sysprep.exe).</span></span>

2.  <span data-ttu-id="3fe4f-198">Dans la boîte de message d’avertissement qui s’affiche, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-198">In the warning message box that appears, click **OK**.</span></span>

3.  <span data-ttu-id="3fe4f-199">Dans la boîte de dialogue **Propriétés de Sysprep** , activez la case à cocher **ne pas réinitialiser le délai de grâce pour l’activation** et utiliser la **mini-installation** .</span><span class="sxs-lookup"><span data-stu-id="3fe4f-199">In the **Sysprep Properties** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes.</span></span>

4.  <span data-ttu-id="3fe4f-200">Cliquez sur **refermer**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-200">Click **Reseal**.</span></span>

5.  <span data-ttu-id="3fe4f-201">Si vous n’êtes pas satisfait des informations indiquées dans la boîte de dialogue de confirmation qui s’affiche, cliquez sur **Annuler** et modifiez les sélections.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-201">If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and change the selections.</span></span>

6.  <span data-ttu-id="3fe4f-202">Cliquez sur **OK** pour finaliser le processus de préparation du système.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-202">Click **OK** to complete the system preparation process.</span></span>

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a><span data-ttu-id="3fe4f-203">Désactivation de Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3fe4f-203">Turning Off Microsoft Virtual PC</span></span>


<span data-ttu-id="3fe4f-204">Une fois tous les composants installés et configurés, fermez Microsoft Virtual PC et sélectionnez **éteindre**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-204">After all the components are installed and configured, close Microsoft Virtual PC and select **Turn Off**.</span></span>

## <span data-ttu-id="3fe4f-205">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fe4f-205">Related topics</span></span>


<span data-ttu-id="3fe4f-206">Création d’une image MED-V [Comment configurer des actions de script](how-to-set-up-script-actions.md)</span><span class="sxs-lookup"><span data-stu-id="3fe4f-206">Creating a MED-V Image [How to Set Up Script Actions](how-to-set-up-script-actions.md)</span></span>










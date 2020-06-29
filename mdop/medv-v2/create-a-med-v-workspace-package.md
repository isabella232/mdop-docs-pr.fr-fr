---
title: Créer un package d'espace de travail MED-V
description: Créer un package d'espace de travail MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809851"
---
# <span data-ttu-id="b255e-103">Créer un package d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b255e-103">Create a MED-V Workspace Package</span></span>


<span data-ttu-id="b255e-104">Un espace de travail MED-V est l’environnement de bureau Windows XP dans lequel les utilisateurs finaux interagissent avec l’ordinateur virtuel fourni par MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-104">A MED-V workspace is the Windows XP desktop environment where end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="b255e-105">L’administrateur crée et personnalise l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-105">The administrator creates and customizes the MED-V workspace.</span></span> <span data-ttu-id="b255e-106">L’espace de travail se compose d’une image et de la stratégie de groupe définissant les règles et les fonctionnalités de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-106">The workspace consists of an image and the Group Policy that defines the rules and functionality of the MED-V workspace.</span></span>

<span data-ttu-id="b255e-107">Vous pouvez créer plusieurs espaces de travail MED-V, chacun personnalisé avec ses propres configurations, paramètres et règles.</span><span class="sxs-lookup"><span data-stu-id="b255e-107">You can create multiple MED-V workspaces, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="b255e-108">Un utilisateur, un groupe ou plusieurs utilisateurs ou groupes peuvent être associés à chaque espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-108">A user, group, or multiple users or groups can be associated with each MED-V workspace.</span></span> <span data-ttu-id="b255e-109">La personnalisation rend l’espace de travail MED-V uniquement disponible pour cet utilisateur ou groupe.</span><span class="sxs-lookup"><span data-stu-id="b255e-109">The customization makes that MED-V workspace available only for that user or group.</span></span>

<span data-ttu-id="b255e-110">Utilisez le **Gestionnaire de package d’espace de travail MED-v** pour créer des espaces de travail MED-v.</span><span class="sxs-lookup"><span data-stu-id="b255e-110">Use the **MED-V Workspace Packager** to create MED-V workspaces.</span></span> <span data-ttu-id="b255e-111">Le **module de création de package de l’espace de travail MED-V** est divisé en deux sections principales:</span><span class="sxs-lookup"><span data-stu-id="b255e-111">The **MED-V Workspace Packager** is divided into two main sections:</span></span>

-   <span data-ttu-id="b255e-112">Panneau principal incluant trois boutons qui vous permettent de créer et de gérer des espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-112">A main panel that includes three buttons that you use to create and manage MED-V workspaces.</span></span> <span data-ttu-id="b255e-113">Le bouton **créer un package d’espace de travail MED-v** ouvre l' **Assistant créer un package d’espace de travail MED-v** qui vous permet de créer vos espaces de travail MED-v.</span><span class="sxs-lookup"><span data-stu-id="b255e-113">The **Create a MED-V Workspace Package** button opens the **Create MED-V Workspace Package Wizard** that you use to create your MED-V workspaces.</span></span>

-   <span data-ttu-id="b255e-114">**Centre d’aide** sur le côté droit de la fenêtre proposant des informations et des conseils pour vous aider à créer, tester et gérer vos espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-114">A **Help Center** on the right-hand side of the window that provides information and guidance to help you create, test, and manage your MED-V workspaces.</span></span>

**<span data-ttu-id="b255e-115">Important</span><span class="sxs-lookup"><span data-stu-id="b255e-115">Important</span></span>**  
<span data-ttu-id="b255e-116">Pour pouvoir utiliser le **Gestionnaire de package d’espace de travail MED-V**, vous devez d’abord vérifier que la stratégie d’exécution Windows PowerShell est définie sur non restreinte.</span><span class="sxs-lookup"><span data-stu-id="b255e-116">Before you can use the **MED-V Workspace Packager**, you must first make sure that the Windows PowerShell execution policy is set to Unrestricted.</span></span>

`Set-ExecutionPolicy Unrestricted`

<span data-ttu-id="b255e-117">Par ailleurs, la stratégie du réseau SAN de l’ordinateur sur lequel est exécuté le package de l' **espace de travail MED-V** doit être définie sur «tout en ligne».</span><span class="sxs-lookup"><span data-stu-id="b255e-117">In addition, the SAN policy for the computer on which the **MED-V Workspace Packager** is run must be set to “Online All”.</span></span> <span data-ttu-id="b255e-118">Pour vérifier le paramètre de la stratégie SAN, exécutez les commandes suivantes à l’invite de commandes avec les informations d’identification d’administration:</span><span class="sxs-lookup"><span data-stu-id="b255e-118">To check the setting of the SAN policy, run the following commands at a command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

<span data-ttu-id="b255e-119">Le cas échéant, modifiez la stratégie SAN en «tout en ligne» en tapant les commandes suivantes à l’invite de commandes avec les informations d’identification d’administration:</span><span class="sxs-lookup"><span data-stu-id="b255e-119">If it is necessary, change the SAN policy to "Online All" by typing the following commands at the command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**<span data-ttu-id="b255e-120">Important</span><span class="sxs-lookup"><span data-stu-id="b255e-120">Important</span></span>**  
<span data-ttu-id="b255e-121">Si un logiciel de chiffrement automatique de disque est installé sur l’ordinateur que vous utilisez pour monter le disque dur virtuel et générer le package d’espace de travail MED-V, vous devez désactiver le logiciel avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="b255e-121">If automatic disk encryption software is installed on the computer that you use to mount the virtual hard disk and build the MED-V workspace package, you must disable the software before you start.</span></span> <span data-ttu-id="b255e-122">Dans le cas contraire, vous ne pouvez pas utiliser l’espace de travail MED-V sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b255e-122">Otherwise, you cannot use the MED-V workspace on any other computer.</span></span>



<span data-ttu-id="b255e-123">Les informations fournies ici peuvent vous aider à créer votre package de déploiement d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-123">The information we provide here can help you create your MED-V workspace deployment package.</span></span>

## <a href="" id="bkmk-prereq"></a><span data-ttu-id="b255e-124">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="b255e-124">Prerequisites</span></span>


<span data-ttu-id="b255e-125">Avant de commencer à créer votre package de déploiement d’espace de travail MED-V, vérifiez que vous avez accès aux éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="b255e-125">Before you start to build your MED-V workspace deployment package, verify that you have access to the following items:</span></span>

-   **<span data-ttu-id="b255e-126">Image Windows XP préparée</span><span class="sxs-lookup"><span data-stu-id="b255e-126">A prepared Windows XP image</span></span>**

    <span data-ttu-id="b255e-127">Pour plus d’informations sur la création d’une image Windows XP à utiliser avec MED-V, voir [préparer une image med-v](prepare-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="b255e-127">For more information about how to create a Windows XP image for use with MED-V, see [Prepare a MED-V Image](prepare-a-med-v-image.md).</span></span>

-   **<span data-ttu-id="b255e-128">Fichier texte ou liste contenant des informations de redirection d’URL</span><span class="sxs-lookup"><span data-stu-id="b255e-128">A text file or list that contains URL redirection information</span></span>**

    <span data-ttu-id="b255e-129">Votre fichier texte ou liste d’URL de redirection d’URL contient les URL que vous voulez rediriger de l’ordinateur hôte vers Internet Explorer dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-129">Your URL redirection text file or list contains those URLs that you want redirected from the host computer to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="b255e-130">Lorsque vous utilisez l’Assistant Packaging pour créer votre espace de travail MED-V, vous importez, tapez ou copiez et collez ces informations de redirection comme une des étapes du processus de création de package.</span><span class="sxs-lookup"><span data-stu-id="b255e-130">When you are using the packaging wizard to create your MED-V workspace, you import, type, or copy and paste this redirection information as one of the steps in the package creation process.</span></span>

    **<span data-ttu-id="b255e-131">Remarque</span><span class="sxs-lookup"><span data-stu-id="b255e-131">Note</span></span>**  
    <span data-ttu-id="b255e-132">La redirection d’URL dans MED-V ne prend en charge que les protocoles HTTP et HTTPs.</span><span class="sxs-lookup"><span data-stu-id="b255e-132">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="b255e-133">MED-V ne fournit pas de prise en charge pour FTP ou tout autre protocole.</span><span class="sxs-lookup"><span data-stu-id="b255e-133">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## <span data-ttu-id="b255e-134">Empaquetage d’un espace de travail MED-V pour une langue autre que celle du langage de l’ordinateur de package de l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b255e-134">Packaging a MED-V Workspace for a Language Other than the Language of the MED-V Workspace Packager Computer</span></span>


<span data-ttu-id="b255e-135">Par défaut, l’espace de travail MED-V prend en charge les caractères dans la langue du système et en anglais.</span><span class="sxs-lookup"><span data-stu-id="b255e-135">By default, the MED-V workspace supports characters in both the language of the computer and in English.</span></span> <span data-ttu-id="b255e-136">Pour créer un espace de travail MED-V pour une langue autre que celle installée sur l’ordinateur, spécifiez **-loc \ [locale \]** dans le script PowerShell (. ps1) après le nom de l’espace de travail MED-v.</span><span class="sxs-lookup"><span data-stu-id="b255e-136">To create a MED-V workspace for a language other than the one installed on the computer, specify **-loc \[locale\]** in the PowerShell script (.ps1) after the MED-V workspace name.</span></span>

<span data-ttu-id="b255e-137">Pour créer un package d’espace de travail MED-V dans une langue autre que la langue par défaut de l’ordinateur de package de l’espace de travail MED-v, générez un script dans la langue par défaut en exécutant le gestionnaire de package MED-v, puis modifiez le script de sortie comme il est requis pour vos paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="b255e-137">To create a MED-V workspace package in a language other than the default language of the MED-V Workspace Packager computer, generate a script in the default language by running the MED-V Workspace Packager and then modifying the output script as required for your locale.</span></span> <span data-ttu-id="b255e-138">Le script est situé dans le répertoire de sortie de l’espace de travail MED-V qui a été spécifié lors de la création de packages.</span><span class="sxs-lookup"><span data-stu-id="b255e-138">The script is located in the MED-V workspace output directory that was specified during packaging.</span></span> <span data-ttu-id="b255e-139">Les noms des paramètres régionaux apparaissent dans la zone de recherche. Fichiers WXL dans l’annuaire suivant:</span><span class="sxs-lookup"><span data-stu-id="b255e-139">The names of the locale settings are on the .WXL files in the following directory:</span></span>

<span data-ttu-id="b255e-140">C:\\Program Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span><span class="sxs-lookup"><span data-stu-id="b255e-140">C:\\Program Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span></span>

## <span data-ttu-id="b255e-141">Création d’un package d’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b255e-141">Creating a MED-V Workspace Package</span></span>


<span data-ttu-id="b255e-142">Pour créer un package d’espace de travail MED-V, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="b255e-142">To create a MED-V workspace package, follow these steps:</span></span>

****

1.  <span data-ttu-id="b255e-143">Pour ouvrir le **Gestionnaire de package de l’espace de travail MED-v**, cliquez sur **Démarrer**, **tous les programmes**, cliquez sur **Microsoft Enterprise Desktop Virtualization**, puis sur **med-v Workspace**.</span><span class="sxs-lookup"><span data-stu-id="b255e-143">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="b255e-144">Dans le volet principal du **Gestionnaire de package de l’espace de travail MED-v** , cliquez sur **créer un package d’espace de travail MED-v**.</span><span class="sxs-lookup"><span data-stu-id="b255e-144">On the **MED-V Workspace Packager** main panel, click **Create a MED-V Workspace Package**.</span></span>

    <span data-ttu-id="b255e-145">L' **Assistant Création de package d’espace de travail MED** -v s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b255e-145">The MED-V **Create MED-V Workspace Package Wizard** appears.</span></span> <span data-ttu-id="b255e-146">L’Assistant comprend les pages suivantes:</span><span class="sxs-lookup"><span data-stu-id="b255e-146">The wizard consists of the following pages:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b255e-147">Informations de package</span><span class="sxs-lookup"><span data-stu-id="b255e-147">Package Information</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b255e-148">Spécifiez un nom pour l’espace de travail MED-V et sélectionnez un dossier dans lequel les fichiers de package d’espace de travail MED-V sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="b255e-148">Specify a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="b255e-149">Sélectionner l’image Windows XP</span><span class="sxs-lookup"><span data-stu-id="b255e-149">Select Windows XP Image</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b255e-150">Spécifiez l’image de votre PC virtuel Windows XP préparé.</span><span class="sxs-lookup"><span data-stu-id="b255e-150">Specify your prepared Windows XP Virtual PC image.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b255e-151">Configuration pour la première fois</span><span class="sxs-lookup"><span data-stu-id="b255e-151">First Time Setup</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b255e-152">Spécifiez le processus d’installation que MED-V suit lors de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="b255e-152">Specify the setup process that MED-V follows during first time setup.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="b255e-153">Messages MED-V</span><span class="sxs-lookup"><span data-stu-id="b255e-153">MED-V Messages</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b255e-154">Spécifiez les messages et l’URL facultative pour les informations d’aide que l’utilisateur final voit lors du premier démarrage.</span><span class="sxs-lookup"><span data-stu-id="b255e-154">Specify the messages and optional URL for Help information that the end user sees during first time setup.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b255e-155">Attribution d’un nom aux ordinateurs</span><span class="sxs-lookup"><span data-stu-id="b255e-155">Naming Computers</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b255e-156">Spécifiez le nom de l’ordinateur virtuel MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-156">Specify how the MED-V virtual machine is named.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="b255e-157">Copier les paramètres à partir de l’hôte</span><span class="sxs-lookup"><span data-stu-id="b255e-157">Copy Settings from Host</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b255e-158">Spécifiez le mode de définition des paramètres de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-158">Specify how the settings for the MED-V workspace are defined.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b255e-159">Démarrage et mise en réseau</span><span class="sxs-lookup"><span data-stu-id="b255e-159">Startup and Networking</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b255e-160">Spécifiez les paramètres de démarrage de l’espace de travail, de la mise en réseau et des informations d’identification de l’utilisateur MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-160">Specify the settings for starting the MED-V workspace, networking, and user credentials.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="b255e-161">Redirection Web</span><span class="sxs-lookup"><span data-stu-id="b255e-161">Web Redirection</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b255e-162">Spécifiez un fichier texte ou une liste d’URL que vous voulez rediriger vers Internet Explorer dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-162">Specify a text file or a list of the URLs you want redirected to Internet Explorer in the MED-V workspace.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="b255e-163">Résumé</span><span class="sxs-lookup"><span data-stu-id="b255e-163">Summary</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="b255e-164">Vérifiez vos paramètres d’espace de travail MED-V et commencez à créer votre package de déploiement d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-164">Verify your MED-V workspace settings and start to build your MED-V workspace deployment package.</span></span></p></td>
    </tr>
    </tbody>
    </table>



3.  <span data-ttu-id="b255e-165">Dans la page informations sur le **paquet** , entrez un nom pour l’espace de travail MED-v, puis sélectionnez un dossier dans lequel les fichiers de package d’espace de travail MED-v sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="b255e-165">On the **Package Information** page, enter a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span>

    **<span data-ttu-id="b255e-166">Warning</span><span class="sxs-lookup"><span data-stu-id="b255e-166">Warning</span></span>**  
    <span data-ttu-id="b255e-167">Vous devez nommer l’espace de travail MED-V et spécifier un dossier pour continuer.</span><span class="sxs-lookup"><span data-stu-id="b255e-167">You must name the MED-V workspace and specify a folder to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

4. <span data-ttu-id="b255e-168">Dans la page **Sélectionner une image Windows XP** , spécifiez l’emplacement de l’image de votre PC virtuel MED-V Windows XP (fichier. vhd).</span><span class="sxs-lookup"><span data-stu-id="b255e-168">On the **Select Windows XP Image** page, specify the location of your prepared MED-V Windows XP Virtual PC image (.vhd file).</span></span>

   **<span data-ttu-id="b255e-169">Warning</span><span class="sxs-lookup"><span data-stu-id="b255e-169">Warning</span></span>**  
   <span data-ttu-id="b255e-170">Vous devez spécifier une image de disque dur virtuel Windows XP pour continuer.</span><span class="sxs-lookup"><span data-stu-id="b255e-170">You must specify a Windows XP VHD image to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

5. <span data-ttu-id="b255e-171">Dans la page de **configuration initiale** , indiquez si vous souhaitez que la première configuration s’exécute lorsque vous avez effectué une assistance ou qu’il soit utilisé pour l’utilisation de l’espace de travail MED-V ou qu’il soit utilisé par tous les utilisateurs finaux sur un ordinateur partagé.</span><span class="sxs-lookup"><span data-stu-id="b255e-171">On the **First Time Setup** page, select whether you want first time setup to run while attended or unattended and whether you want the MED-V workspace used separately or used by all end users on a shared computer.</span></span>

   <span data-ttu-id="b255e-172">Si vous sélectionnez l’option **d’installation sans assistance, sans notification**, l’utilisateur final n’est pas informé avant l’exécution de la première configuration et l’ordinateur virtuel n’est pas présenté à l’utilisateur final lors de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="b255e-172">If you select **Unattended setup, without any notification**, the end user is not informed before first time setup is run and the virtual machine is not shown to the end user during first time setup.</span></span> <span data-ttu-id="b255e-173">De plus, la page **messages MED-V** de l’Assistant est masquée, car aucun message n’est requis lors de la première exécution du mode sans assistance.</span><span class="sxs-lookup"><span data-stu-id="b255e-173">In addition, the **MED-V Messages** page of the wizard is hidden because no messages are required if first time setup runs in a completely unattended mode.</span></span>

   <span data-ttu-id="b255e-174">Si vous sélectionnez l’option **d’installation sans assistance, mais que les utilisateurs finaux peuvent notifier avant le début de la première configuration**, l’utilisateur final est averti avant l’exécution de la première fois.</span><span class="sxs-lookup"><span data-stu-id="b255e-174">If you select **Unattended setup, but notify end users before first time setup begins**, the end user is informed before first time setup is run.</span></span> <span data-ttu-id="b255e-175">Toutefois, l’ordinateur virtuel n’est pas présenté à l’utilisateur final lors de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="b255e-175">However, the virtual machine is not shown to the end user during first time setup.</span></span>

   <span data-ttu-id="b255e-176">Sélectionnez **configuration assistée** si l’utilisateur final doit entrer des informations lors du premier démarrage.</span><span class="sxs-lookup"><span data-stu-id="b255e-176">Select **Attended setup** if the end user must enter information during first time setup.</span></span>

   <span data-ttu-id="b255e-177">Le comportement par défaut est le **programme d’installation sans assistance, mais avertir les utilisateurs finaux avant le premier démarrage du programme d’installation**.</span><span class="sxs-lookup"><span data-stu-id="b255e-177">The default behavior is **Unattended setup, but notify end users before first time setup begins**.</span></span>

   **<span data-ttu-id="b255e-178">Vigilance</span><span class="sxs-lookup"><span data-stu-id="b255e-178">Caution</span></span>**  
   <span data-ttu-id="b255e-179">Si vous avez créé le fichier Sysprep. inf de façon à ce que la mini-installation exige l’entrée utilisateur, vous devez sélectionner l’option **d’installation avec assistance** ou des problèmes peuvent se produire lors de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="b255e-179">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, you must select **Attended setup** or problems might occur during first time setup.</span></span>



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. <span data-ttu-id="b255e-180">Dans la page **messages MED-V** , spécifiez les messages suivants que l’utilisateur final voit lors de la première configuration:</span><span class="sxs-lookup"><span data-stu-id="b255e-180">On the **MED-V Messages** page, specify the following messages that the end user sees during first time setup:</span></span>

   -   <span data-ttu-id="b255e-181">Le message visible par l’utilisateur final lors du premier démarrage de l’installation.</span><span class="sxs-lookup"><span data-stu-id="b255e-181">The message that the end user sees when first time setup starts.</span></span>

   -   <span data-ttu-id="b255e-182">Le message qui s’affiche lorsque l’utilisateur final se trouve lors de l’échec de la première configuration ou d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="b255e-182">The message that the end user sees if first time setup fails or an error occurs.</span></span>

   **<span data-ttu-id="b255e-183">Remarque</span><span class="sxs-lookup"><span data-stu-id="b255e-183">Note</span></span>**  
   <span data-ttu-id="b255e-184">La page **messages MED-V** de l’Assistant est masquée si vous avez sélectionné **installation sans assistance, sans notification** sur la **première** page de configuration.</span><span class="sxs-lookup"><span data-stu-id="b255e-184">The **MED-V Messages** page of the wizard is hidden if you selected **Unattended setup, without any notification** on the **First Time Setup** page.</span></span>



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. <span data-ttu-id="b255e-185">Dans la page attribution d’un **nom aux ordinateurs** , vous pouvez spécifier si le nom de l’ordinateur est géré par MED-V ou par un outil de gestion du système tel que Sysprep.</span><span class="sxs-lookup"><span data-stu-id="b255e-185">On the **Naming Computers** page, you can specify whether computer naming is managed by MED-V or by a system management tool, such as Sysprep.</span></span> <span data-ttu-id="b255e-186">Par défaut, la gestion des noms d’ordinateur est gérée par un outil de gestion du système.</span><span class="sxs-lookup"><span data-stu-id="b255e-186">The default is that computer naming is managed by a system management tool.</span></span>

   <span data-ttu-id="b255e-187">Si vous spécifiez que le nom de l’ordinateur est géré par MED-V, sélectionnez une convention d’affectation de noms d’ordinateur prédéfinie (Mask) dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="b255e-187">If you specify that computer naming is managed by MED-V, select a predefined computer naming convention (mask) from the drop-down list.</span></span> <span data-ttu-id="b255e-188">Un aperçu du nom d’un exemple d’ordinateur s’affiche en fonction de l’ordinateur que vous utilisez pour créer le package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-188">A preview of a sample computer name appears that is based on the computer that you are using to build the MED-V workspace package.</span></span>

   <span data-ttu-id="b255e-189">Si vous sélectionnez l’une des conventions d’affectation de noms personnalisées, les champs que vous pouvez spécifier sont limités aux caractères suivants:</span><span class="sxs-lookup"><span data-stu-id="b255e-189">If you select one of the custom naming conventions, the fields you can specify are limited to the following characters:</span></span>

   -   <span data-ttu-id="b255e-190">Les champs préfixe et suffixe sont limités aux caractères A-Z, a-z, 0-9 et aux caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="b255e-190">The prefix and suffix fields are limited to the characters A-Z, a-z, 0-9, and the special characters !</span></span> <span data-ttu-id="b255e-191">@ \ # $% ^ & ()-\ _ _ ' {}.</span><span class="sxs-lookup"><span data-stu-id="b255e-191">@ \# $ % ^ & ( ) - \_ ' { } .</span></span> <span data-ttu-id="b255e-192">et ~.</span><span class="sxs-lookup"><span data-stu-id="b255e-192">and ~.</span></span>

   -   <span data-ttu-id="b255e-193">Les champs hostname et username sont limités aux chiffres 0 à 9.</span><span class="sxs-lookup"><span data-stu-id="b255e-193">The hostname and username fields are limited to the digits 0 through 9.</span></span>

   **<span data-ttu-id="b255e-194">Important</span><span class="sxs-lookup"><span data-stu-id="b255e-194">Important</span></span>**  
   <span data-ttu-id="b255e-195">Les noms d’ordinateurs doivent être uniques et ne comporter pas plus de 15 caractères.</span><span class="sxs-lookup"><span data-stu-id="b255e-195">Computer names must be unique and are limited to a maximum of 15 characters.</span></span> <span data-ttu-id="b255e-196">Lorsque vous déterminez la méthode d’attribution d’noms de votre ordinateur, envisagez d’utiliser des utilisateurs finaux disposant de plusieurs ordinateurs ou du partage d’un ordinateur, et évitez d’utiliser des masques de nom d’ordinateur qui pourraient provoquer une collision sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="b255e-196">When you decide on your computer naming method, consider end users who have multiple computers or that share a computer, and avoid using computer name masks that could cause a collision on the network.</span></span>



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. <span data-ttu-id="b255e-197">Dans la page **copier les paramètres à partir de l’hôte** , vous pouvez sélectionner les paramètres suivants pour spécifier la façon dont l’espace de travail MED-V est configuré:</span><span class="sxs-lookup"><span data-stu-id="b255e-197">On the **Copy Settings from Host** page, you can select the following settings to specify how the MED-V workspace is configured:</span></span>

   **<span data-ttu-id="b255e-198">Vigilance</span><span class="sxs-lookup"><span data-stu-id="b255e-198">Caution</span></span>**  
   <span data-ttu-id="b255e-199">Les paramètres que vous spécifiez sur cette page qui sont copiés à partir de l’ordinateur hôte vers l’espace de travail MED-V remplacent ceux spécifiés dans le fichier de réponses Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="b255e-199">The settings that you specify on this page that are copied from the host computer to the MED-V workspace override those specified in the Sysprep.inf answer file.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. <span data-ttu-id="b255e-200">Dans la page de **démarrage et de réseau** , vous pouvez modifier le comportement par défaut des paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="b255e-200">On the **Startup and Networking** page, you can change the default behavior for the following settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b255e-201">Démarrer l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b255e-201">Start MED-V workspace</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b255e-202">Indiquez si vous voulez démarrer l’espace de travail MED-V lors de l’ouverture de session de l’utilisateur, lors de la première utilisation, ou pour permettre à l’utilisateur final de décider du démarrage de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-202">Choose whether to start the MED-V workspace at user logon, at first use, or to let the end user decide when the MED-V workspace starts.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="b255e-203">L’espace de travail MED-V démarre de l’une des deux manières suivantes: si l’utilisateur final se connecte, ou s’il commence une action qui nécessite MED-V, comme l’ouverture d’une application publiée ou la saisie d’une URL nécessitant une redirection.</span><span class="sxs-lookup"><span data-stu-id="b255e-203">The MED-V workspace starts in one of two ways: either when the end user logs on or when they first start an action that requires MED-V, such as opening a published application or entering a URL that requires redirection.</span></span></p>
   <p><span data-ttu-id="b255e-204">Vous pouvez définir ce paramètre pour l’utilisateur final ou laisser l’utilisateur final contrôler le démarrage de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-204">You can either define this setting for the end user or let the end user control how MED-V starts.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b255e-205">Remarque</span><span class="sxs-lookup"><span data-stu-id="b255e-205">Note</span></span></strong><br/><p><span data-ttu-id="b255e-206">Si vous spécifiez une décision définie par l’utilisateur final, le comportement par défaut qu’il présente est que l’espace de travail MED-V démarre lorsqu’il se connecte.</span><span class="sxs-lookup"><span data-stu-id="b255e-206">If you specify that the end user decides, the default behavior they experience is that the MED-V workspace starts when they log on.</span></span> <span data-ttu-id="b255e-207">Les utilisateurs peuvent modifier ce paramètre par défaut en cliquant avec le bouton droit sur l’icône MED-V dans la zone de notification et en sélectionnant <strong> paramètres utilisateur med-v </strong> .</span><span class="sxs-lookup"><span data-stu-id="b255e-207">They can change the default by right-clicking the MED-V icon in the notification area and selecting <strong>MED-V User Settings</strong>.</span></span> <span data-ttu-id="b255e-208">Si vous définissez ce paramètre pour l’utilisateur final, il ne peut pas modifier le mode de démarrage de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-208">If you define this setting for the end user, they cannot change how MED-V starts.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b255e-209">Réseaux</span><span class="sxs-lookup"><span data-stu-id="b255e-209">Networking</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b255e-210">Sélectionnez <strong> partagé </strong> ou <strong> Bridged </strong> pour votre paramètre réseau.</span><span class="sxs-lookup"><span data-stu-id="b255e-210">Select <strong>Shared</strong> or <strong>Bridged</strong> for your networking setting.</span></span> <span data-ttu-id="b255e-211">La valeur par défaut est <strong> Shared </strong> .</span><span class="sxs-lookup"><span data-stu-id="b255e-211">The default is <strong>Shared</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong><span data-ttu-id="b255e-212">Partagé </strong> - l’espace de travail MED-V utilise la traduction d’adresses réseau (NAT) pour partager les adresses IP de l’hôte&#39;s pour le trafic sortant.</span><span class="sxs-lookup"><span data-stu-id="b255e-212">Shared</strong> - The MED-V workspace uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p>
   <p><strong><span data-ttu-id="b255e-213">Bridged </strong> - l’espace de travail MED-V dispose de sa propre adresse réseau, généralement obtenue via le protocole DHCP.</span><span class="sxs-lookup"><span data-stu-id="b255e-213">Bridged</strong> - The MED-V workspace has its own network address, typically obtained through DHCP.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b255e-214">Stocker les informations d’identification</span><span class="sxs-lookup"><span data-stu-id="b255e-214">Store credentials</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b255e-215">Indiquez si vous souhaitez stocker les informations d’identification de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="b255e-215">Choose whether you want to store the end user credentials.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="b255e-216">Le comportement par défaut est que le stockage des informations d’identification est désactivé de sorte que l’utilisateur final doit être authentifié à chaque ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b255e-216">The default behavior is that credential storing is disabled so that the end user must be authenticated every time that they log on.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b255e-217">Important</span><span class="sxs-lookup"><span data-stu-id="b255e-217">Important</span></span></strong><br/><p><span data-ttu-id="b255e-218">Même si la mise en cache des informations d’identification de l’utilisateur final offre une meilleure utilisation de l’utilisateur, vous devez connaître les risques liés.</span><span class="sxs-lookup"><span data-stu-id="b255e-218">Even though caching the end user’s credentials provides the best user experience, you should be aware of the risks involved.</span></span></p>
   <p><span data-ttu-id="b255e-219">Les informations d’identification de domaine de l’utilisateur final sont stockées dans un format réversible dans le gestionnaire d’informations d’identification Windows.</span><span class="sxs-lookup"><span data-stu-id="b255e-219">The end user’s domain credential is stored in a reversible format in the Windows Credential Manager.</span></span> <span data-ttu-id="b255e-220">Par conséquent, une personne malveillante pourrait écrire un programme qui récupère le mot de passe et peut accéder aux informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b255e-220">As a result, an attacker could write a program that retrieves the password and could gain access to the user’s credentials.</span></span> <span data-ttu-id="b255e-221">Vous pouvez limiter ce risque uniquement en désactivant le stockage des informations d’identification de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="b255e-221">You can only lessen this risk by disabling the storing of end-user credentials.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. <span data-ttu-id="b255e-222">Dans la page **redirection Web** , vous pouvez entrer, coller ou importer une liste des URL redirigées vers Internet Explorer dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-222">On the **Web Redirection** page, you can enter, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="b255e-223">Pour plus d’informations sur la configuration de vos informations de redirection d’URL, voir [conditions préalables](#bkmk-prereq).</span><span class="sxs-lookup"><span data-stu-id="b255e-223">For more information about how to configure your URL redirection information, see [Prerequisites](#bkmk-prereq).</span></span>

   <span data-ttu-id="b255e-224">Vous pouvez également spécifier le mode de configuration d’Internet Explorer dans l’espace de travail MED-V pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="b255e-224">You can also specify how Internet Explorer in the MED-V workspace is configured for end users.</span></span> <span data-ttu-id="b255e-225">Par défaut, le niveau de sécurité de zone Internet est réglé sur élevé.</span><span class="sxs-lookup"><span data-stu-id="b255e-225">By default, the Internet zone security level is set to High.</span></span> <span data-ttu-id="b255e-226">Par ailleurs, certaines fonctionnalités de navigation par défaut, telles que la barre d’adresse, sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="b255e-226">Also, certain default browsing capabilities, such as the address bar, are removed.</span></span> <span data-ttu-id="b255e-227">Cette configuration par défaut d’Internet Explorer dans l’espace de travail MED-V fournit un environnement de navigation plus sûr aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="b255e-227">This default configuration of Internet Explorer in the MED-V workspace provides a more secure browsing environment for end users.</span></span>

   **<span data-ttu-id="b255e-228">Vigilance</span><span class="sxs-lookup"><span data-stu-id="b255e-228">Caution</span></span>**  
   <span data-ttu-id="b255e-229">En modifiant les paramètres par défaut, vous pouvez personnaliser Internet Explorer dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-229">By changing the default settings, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="b255e-230">Sachez que si vous modifiez les paramètres par défaut afin de les rendre moins sécurisés, vous pouvez exposer votre organisation aux risques en matière de sécurité présents dans les versions antérieures d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b255e-230">However, realize that if you change the default settings so as to make them less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span> <span data-ttu-id="b255e-231">Pour plus d’informations, consultez [meilleures pratiques en matière de sécurité pour les opérations MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="b255e-231">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>



~~~
After you have finished, click **Next**.
~~~

11. <span data-ttu-id="b255e-232">Dans la page **Résumé** , vous pouvez consulter les paramètres de création de packages de cet espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b255e-232">On the **Summary** page, you can review the packaging settings for this MED-V workspace.</span></span> <span data-ttu-id="b255e-233">Si vous voulez modifier des paramètres, cliquez sur le bouton **précédent** pour revenir à la page correspondante.</span><span class="sxs-lookup"><span data-stu-id="b255e-233">If you want to change any settings, click the **Previous** button to return to the relevant page.</span></span> <span data-ttu-id="b255e-234">Lorsque vous avez terminé de vérifier les paramètres, cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="b255e-234">After you have finished reviewing the settings, click **Create**.</span></span>

   <span data-ttu-id="b255e-235">La page de **fin** de l' **Assistant Création d’un package d’espace de travail MED-V** s’ouvre pour montrer la progression de la création du package.</span><span class="sxs-lookup"><span data-stu-id="b255e-235">The **Completion** page of the **Create MED-V Workspace Package Wizard** opens to show the progress of the package creation.</span></span>

   **<span data-ttu-id="b255e-236">Remarque</span><span class="sxs-lookup"><span data-stu-id="b255e-236">Note</span></span>**  
   <span data-ttu-id="b255e-237">Le processus de création de package de l’espace de travail MED-V peut prendre plusieurs minutes en fonction de la taille de VHD spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b255e-237">The MED-V workspace package creation process might take several minutes to complete, depending on the size of the VHD specified.</span></span>



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. <span data-ttu-id="b255e-238">Cliquez sur **Fermer** pour fermer l’Assistant Création de packages et revenir au **Gestionnaire de package de l’espace de travail MED-V**.</span><span class="sxs-lookup"><span data-stu-id="b255e-238">Click **Close** to close the packaging wizard and return to the **MED-V Workspace Packager**.</span></span>

<span data-ttu-id="b255e-239">Votre package d’espace de travail MED-V est désormais prêt à être testé avant le déploiement.</span><span class="sxs-lookup"><span data-stu-id="b255e-239">Your MED-V workspace package is now ready for testing before deployment.</span></span>

## <span data-ttu-id="b255e-240">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b255e-240">Related topics</span></span>


[<span data-ttu-id="b255e-241">Configuration de paramètres avancés à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b255e-241">Configuring Advanced Settings by Using Windows PowerShell</span></span>](configuring-advanced-settings-by-using-windows-powershell.md)

[<span data-ttu-id="b255e-242">Tester le package d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b255e-242">Testing the MED-V Workspace Package</span></span>](testing-the-med-v-workspace-package.md)

[<span data-ttu-id="b255e-243">Préparer une image MED-V</span><span class="sxs-lookup"><span data-stu-id="b255e-243">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)










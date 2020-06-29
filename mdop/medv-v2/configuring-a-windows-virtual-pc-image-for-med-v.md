---
title: Configuration d'une image Windows Virtual PC pour MED-V
description: Configuration d'une image Windows Virtual PC pour MED-V
author: dansimp
ms.assetid: d87a0df8-9e08-4d1e-bfb0-9dc3cebf0d28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 340754b33576651c8ba89c85f369c48c0a0ab957
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811982"
---
# <span data-ttu-id="e61b7-103">Configuration d'une image Windows Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="e61b7-103">Configuring a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="e61b7-104">Une fois que vous avez installé toutes les données que vous voulez inclure dans votre image MED-V, vous pouvez configurer l’image pour une utilisation dans la version 2,0 de Microsoft Enterprise Desktop Virtualization.</span><span class="sxs-lookup"><span data-stu-id="e61b7-104">After you have installed everything that you want to include in your MED-V image, you can configure the image for use in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="e61b7-105">Les rubriques de cette section fournissent des instructions pour configurer votre image MED-V de façon à ce qu’elle s’exécute pour la première fois avant de créer votre package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="e61b7-105">The topics in this section provide guidance for configuring your MED-V image to run first time setup before you create your MED-V workspace package.</span></span>

<span data-ttu-id="e61b7-106">La première fois que le programme d’installation prépare l’espace de travail MED-V pour un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="e61b7-106">First time setup prepares the MED-V workspace for an end user.</span></span> <span data-ttu-id="e61b7-107">Le processus crée une machine virtuelle à partir de l’image empaquetée dans l’espace de travail MED-V, puis exécute la mini-installation de Windows sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="e61b7-107">The process creates a virtual machine from the image packaged in the MED-V workspace and then runs Windows Mini-Setup on the virtual machine.</span></span> <span data-ttu-id="e61b7-108">Cela inclut l’exécution de scripts de configuration personnalisés et la première application de réalisation de l’installation, FtsCompletion.exe.</span><span class="sxs-lookup"><span data-stu-id="e61b7-108">This includes the running of both custom setup scripts and the first time setup completion application, FtsCompletion.exe.</span></span>

<span data-ttu-id="e61b7-109">Suivez ces étapes pour configurer votre image MED-V pour l’exécution de la première fois:</span><span class="sxs-lookup"><span data-stu-id="e61b7-109">Follow these steps to configure your MED-V image for running first time setup:</span></span>

1. <span data-ttu-id="e61b7-110">En option, vous pouvez compacter le disque dur virtuel (VHD) pour récupérer l’espace libre sur le disque et réduire la taille du disque dur virtuel avant de poursuivre la configuration de l’image de PC virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="e61b7-110">As an option, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you continue with configuring the Windows Virtual PC image.</span></span> <span data-ttu-id="e61b7-111">Pour plus d’informations, voir [compactage du disque dur virtuel MED-V](compacting-the-med-v-virtual-hard-disk.md).</span><span class="sxs-lookup"><span data-stu-id="e61b7-111">For more information, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

2. <span data-ttu-id="e61b7-112">Personnalisez le processus de configuration d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e61b7-112">Customize the virtual machine setup process.</span></span>

3. <span data-ttu-id="e61b7-113">Scellez l’image MED-V en utilisant Sysprep.</span><span class="sxs-lookup"><span data-stu-id="e61b7-113">Seal the MED-V image by using Sysprep.</span></span>

   **<span data-ttu-id="e61b7-114">Personnalisation du processus de configuration d’une machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="e61b7-114">Customizing the Virtual Machine Setup Process</span></span>**

4. <span data-ttu-id="e61b7-115">Dans le cadre de la préparation de votre image pour une utilisation avec MED-V, vous pouvez configurer différents paramètres sur l’ordinateur virtuel, par exemple pour spécifier les paramètres d’exécution de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e61b7-115">As part of preparing your image for use with MED-V, you can configure various settings on the virtual machine, such as specifying the settings for running Windows Update.</span></span> <span data-ttu-id="e61b7-116">Spécifiez tous les paramètres d’ordinateur virtuel nécessaires avant de créer le package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="e61b7-116">Specify all the necessary virtual machine settings before you create the MED-V workspace package.</span></span>

5. <span data-ttu-id="e61b7-117">Avant de créer le package d’espace de travail MED-V, nous vous recommandons de désactiver les points de restauration sur l’ordinateur virtuel pour empêcher le disque de différenciation de croître.</span><span class="sxs-lookup"><span data-stu-id="e61b7-117">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="e61b7-118">Pour plus d’informations, reportez-vous à la rubrique désactivation [et activation de la restauration du système dans Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="e61b7-118">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

   **<span data-ttu-id="e61b7-119">Remarque</span><span class="sxs-lookup"><span data-stu-id="e61b7-119">Note</span></span>**  
   <span data-ttu-id="e61b7-120">Vous pouvez configurer votre fichier Sysprep. inf pour désactiver les points de restauration lors de la première exécution du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="e61b7-120">You can set up your Sysprep.inf file to disable restore points when first time setup is run.</span></span> <span data-ttu-id="e61b7-121">Pour obtenir un exemple de définition de cette clé GuiRunOnce, voir l’exemple de fichier Sysprep. inf plus loin dans cette section.</span><span class="sxs-lookup"><span data-stu-id="e61b7-121">For an example of setting this GuiRunOnce key, see the sample Sysprep.inf file later in this section.</span></span>



6. <span data-ttu-id="e61b7-122">Configurez le processus de configuration pour exécuter la mini-installation au lieu de l’accueil Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="e61b7-122">Configure the setup process to run Mini-Setup instead of the default Windows Welcome.</span></span> <span data-ttu-id="e61b7-123">Vous devez exécuter l’outil Sysprep à l’aide du **mini-** commutateur ou activer la case à cocher **MiniSetup** dans l’interface utilisateur graphique.</span><span class="sxs-lookup"><span data-stu-id="e61b7-123">You must either run the Sysprep tool by using the **-mini** switch, or select the **MiniSetup** check box in the graphical user interface.</span></span> <span data-ttu-id="e61b7-124">Pour plus d’informations, reportez-vous [à la section sceller l’image avec Sysprep](#bkmk-seal).</span><span class="sxs-lookup"><span data-stu-id="e61b7-124">For more information, see [How to Seal the Image with Sysprep](#bkmk-seal).</span></span>

   **<span data-ttu-id="e61b7-125">Appel lors de la première exécution du fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="e61b7-125">Calling the First time setup Completion File</span></span>**

   1.  <span data-ttu-id="e61b7-126">Un exécutable appelé FtsCompletion.exe est inclus dans le cadre de l’installation de l’agent d’invité MED-V.</span><span class="sxs-lookup"><span data-stu-id="e61b7-126">An executable called FtsCompletion.exe is included as part of the installation of the MED-V Guest Agent.</span></span> <span data-ttu-id="e61b7-127">Par défaut, il se trouve dans le lecteur système de votre image MED-V sous **Program Files-Microsoft Enterprise Desktop Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="e61b7-127">By default, it is located in the system drive of your MED-V image under **Program Files – Microsoft Enterprise Desktop Virtualization**.</span></span>

       **<span data-ttu-id="e61b7-128">Important</span><span class="sxs-lookup"><span data-stu-id="e61b7-128">Important</span></span>**  
       <span data-ttu-id="e61b7-129">Lors de la dernière étape du processus de configuration pour la première fois, vous devez exécuter ce programme exécutable.</span><span class="sxs-lookup"><span data-stu-id="e61b7-129">As the final step in the first time setup process, you must run this executable program.</span></span> <span data-ttu-id="e61b7-130">L’utilisateur pour lequel le programme exécutable est appelé doit être membre du groupe d’administrateurs local de l’invité.</span><span class="sxs-lookup"><span data-stu-id="e61b7-130">The user for whom the executable program is being called must be a member of the guest’s local administrator group.</span></span>



   2.  <span data-ttu-id="e61b7-131">Vous pouvez décider de la façon dont vous souhaitez appeler ce programme exécutable, par exemple par le biais d’un script déployé avec l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="e61b7-131">You can decide how you want to call this executable program, for example, through a script that is deployed with the MED-V workspace.</span></span> <span data-ttu-id="e61b7-132">Vous pouvez appeler cet exécutable en tant que dernière ligne de votre fichier Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="e61b7-132">You can call this executable as the last line of your Sysprep.inf file.</span></span> <span data-ttu-id="e61b7-133">Pour obtenir un exemple illustrant comment appeler ce programme exécutable dans votre fichier Sysprep. inf, voir l’exemple de fichier plus loin dans cette section.</span><span class="sxs-lookup"><span data-stu-id="e61b7-133">For an example of how to call this executable program in your Sysprep.inf file, see the sample file later in this section.</span></span>

<span data-ttu-id="e61b7-134">Une fois que vous avez terminé la personnalisation de votre image MED-V, vous êtes prêt à sceller l’image en utilisant Sysprep.</span><span class="sxs-lookup"><span data-stu-id="e61b7-134">After you have completed customization of your MED-V image, you are ready to seal the image by using Sysprep.</span></span>

<a href="" id="bkmk-seal"></a>**<span data-ttu-id="e61b7-135">Sceller l’image MED-V à l’aide de Sysprep</span><span class="sxs-lookup"><span data-stu-id="e61b7-135">Sealing the MED-V Image by Using Sysprep</span></span>**

1.  <span data-ttu-id="e61b7-136">L’outil de préparation du système (Sysprep) est une technologie qui vous permet d’effectuer des installations basées sur une image à l’échelle du réseau en minimisant l’intervention d’un administrateur ou d’un informaticien.</span><span class="sxs-lookup"><span data-stu-id="e61b7-136">The System Preparation tool (Sysprep) is a technology that you can use to perform image-based installations throughout the network with minimal intervention by an administrator or IT-Professional.</span></span>

2.  <span data-ttu-id="e61b7-137">Dans un environnement MED-V, vous pouvez utiliser Sysprep pour affecter des ID de sécurité (SID) uniques et d’autres paramètres à chaque espace de travail MED-V lors du premier démarrage.</span><span class="sxs-lookup"><span data-stu-id="e61b7-137">In a MED-V environment, you can use Sysprep to assign unique security IDs (SID) and other settings to each MED-V workspace the first time that they are started.</span></span>

    **<span data-ttu-id="e61b7-138">Remarque</span><span class="sxs-lookup"><span data-stu-id="e61b7-138">Note</span></span>**  
    <span data-ttu-id="e61b7-139">Pour plus d’informations sur l’utilisation de Sysprep, voir [référence technique de Sysprep](https://go.microsoft.com/fwlink/?LinkId=195930) ( https://go.microsoft.com/fwlink/?LinkId=195930) .</span><span class="sxs-lookup"><span data-stu-id="e61b7-139">For more information about how to use Sysprep, see [Sysprep Technical Reference](https://go.microsoft.com/fwlink/?LinkId=195930) (https://go.microsoft.com/fwlink/?LinkId=195930).</span></span>



~~~
**Caution**  
When you use non-ASCII characters in the Sysprep.inf file, you must save the file by using the encoding appropriate for the characters entered. Windows XP expects the Sysprep.inf file to be encoded by using the code page for the language that you are targeting.

You must also make sure that the System Locale of the computers to which the MED-V workspace is deployed is set to handle the language specific characters that might be present in the Sysprep.inf file. To change the settings for the System Locale, follow these steps:

1.  To open Region and Language, click **Start**, click **Control Panel**, and then click **Region and Language**.

2.  Click the **Administrative** tab, and then click **Change System Locale** under **Language for non-Unicode programs**.

    If you are prompted for an administrator password or confirmation, type the administrator password or provide confirmation.

3.  Select your preferred language and then click **OK**.



**To configure Sysprep on the MED-V Guest Computer**

1.  Create a folder named *Sysprep* in the root of the MED-V image system drive.

2.  Download the deploy.cab file. For more information, see [Windows XP Service Pack 3 Deployment Tools](https://go.microsoft.com/fwlink/?LinkId=195928) From the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195928).

3.  From the deploy.cab file, copy or extract the Setupmgr.exe, Sysprep.exe, and Setupcl.exe files to the Sysprep folder.

4.  In the Sysprep folder, run **Setup Manager** (Setupmgr.exe) to create a Sysprep.inf answer file.

    Or, you can create this file manually or use your company’s existing file. For more information, see [How to use the Sysprep tool to automate successful deployment of Windows XP](https://go.microsoft.com/fwlink/?LinkId=195929) (https://go.microsoft.com/fwlink/?LinkId=195929).

5.  Follow the **Setup Manager** wizard.

    **Important**  
    You must configure the MED-V guest to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.



    **Caution**  
    When you configure a proxy account for joining virtual machines to the domain, know that it is possible for an end user to obtain the proxy account credentials. Take all the necessary security precautions to minimize risk, such as limiting account user rights. For more information about security concerns when you configure a Windows Virtual PC image for MED-V, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).



    If end users must provide information during the first time setup process based on the parameters specified in the Sysprep.inf file, you must also specify that first time setup is run in **Attended** mode when you are creating your MED-V workspace package. If no information will be required from the end user, you can specify that first time setup is run in **Unattended** mode when you are creating your MED-V workspace package. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode. This requires that you provide all of the required settings information as you continue through the **Setup Manager** wizard.

    **Caution**  
    If you have set a local policy or registry entry to include a service level agreement (SLA) in your image (VHD), you must specify that first time setup is run in **Attended** mode or first time setup will fail. Or, a MED-V best practice is to enforce the SLA through Group Policy later so that the SLA is displayed to the end user after first time setup is finished.



    **Note**  
    You can configure the MED-V workspace to set certain Sysprep.inf settings based on the configuration of the host and the identity of the end user. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).



6.  Seal the MED-V image.

    **Important**  
    We recommend that you make a backup copy of the MED-V image before sealing it.



    After you have completed all the steps in the **Setup Manager** wizard, you are ready to run Sysprep to seal the MED-V image.

**To run Sysprep**

1.  Run the System Preparation Tool (Sysprep.exe) from the *Sysprep* folder that you created when you configured Sysprep in the MED-V virtual machine.

2.  In the warning message box that appears, click **OK**.

3.  In the **Options** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes. Also, make sure that the **Shutdown mode** box is set to **Shut down**.

4.  Click **Reseal**. This removes identity information and clears event logs to prepare for first time setup.

5.  If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and then change the selections.

6.  Click **OK** to complete the system preparation process.

After you have run Sysprep on your MED-V image, the virtual machine shuts down and is ready for use in creating a MED-V workspace.
~~~

## <span data-ttu-id="e61b7-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="e61b7-140">Example</span></span>


<span data-ttu-id="e61b7-141">Voici un exemple de fichier Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="e61b7-141">Here is an example of a Sysprep.inf file.</span></span>

``` syntax
;SetupMgrTag
[GuiUnattended]
    EncryptedAdminPassword=NO
    TimeZone=10
    OEMDuplicatorstring="MED_V v2 Host"
    AdminPassword="administrator"
    AutoLogon=Yes
    AutoLogonCount=1
    OEMSkipRegional=1
    OemSkipWelcome=1

[UserData]
    ProductKey=
    FullName="MED-V User"
    OrgName="Contoso"
    ComputerName=*

[Identification]
    JoinDomain=domain.corp.contoso.com
    DomainAdmin=UserName
    DomainAdminPassword=Password

[Networking]
    InstallDefaultComponents=Yes

[Branding]
    BrandIEUsingUnattended=Yes

[Proxy]
    Proxy_Enable=0
    Use_Same_Proxy=0

[Unattended]
    InstallFilesPath=C:\sysprep\i386
    TargetPath=\WINDOWS
    UpdateServerProfileDirectory=1
    OemSkipEula=Yes

[RegionalSettings]
    LanguageGroup=1
    Language=00000409

[GuiRunOnce]
    Command0="wmic /namespace:\\root\default path SystemRestore call Disable %SystemDrive%\"
    Command1="c:\Program Files\Microsoft Enterprise Desktop Virtualization\FtsCompletion.exe"

[sysprepcleanup]
```

## <span data-ttu-id="e61b7-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e61b7-142">Related topics</span></span>


[<span data-ttu-id="e61b7-143">Créer un package d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="e61b7-143">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

[<span data-ttu-id="e61b7-144">Préparer une image MED-V</span><span class="sxs-lookup"><span data-stu-id="e61b7-144">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)










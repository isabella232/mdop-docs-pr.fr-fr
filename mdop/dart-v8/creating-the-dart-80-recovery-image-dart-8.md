---
title: Création de l'image de récupération DaRT8.0
description: Création de l'image de récupération DaRT8.0
author: dansimp
ms.assetid: 39001b8e-86c0-45ef-8f34-2d6199f9922d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/21/2017
ms.openlocfilehash: 79ce5859e7d0eacf95124c2a7409ff6c21890d65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804314"
---
# <span data-ttu-id="0d374-103">Création de l'image de récupération DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="0d374-103">Creating the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="0d374-104">Après l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 8,0, vous créez une image de récupération 8,0 DaRT.</span><span class="sxs-lookup"><span data-stu-id="0d374-104">After installing Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, you create a DaRT 8.0 recovery image.</span></span> <span data-ttu-id="0d374-105">L’image de récupération démarre Windows RE, à partir duquel vous pouvez démarrer les outils DaRT.</span><span class="sxs-lookup"><span data-stu-id="0d374-105">The recovery image starts Windows RE, from which you can then start the DaRT tools.</span></span> <span data-ttu-id="0d374-106">Vous pouvez générer des fichiers ISO (International Organization for Standardization) et des images de format Windows Imaging.</span><span class="sxs-lookup"><span data-stu-id="0d374-106">You can generate International Organization for Standardization (ISO) files and Windows Imaging Format (WIM) images.</span></span> <span data-ttu-id="0d374-107">De plus, vous pouvez utiliser PowerShell pour générer des scripts qui utilisent les paramètres que vous avez sélectionnés dans l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="0d374-107">In addition, you can use PowerShell to generate scripts that use the settings you select in the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="0d374-108">Vous pouvez utiliser le script ultérieurement pour générer des images de récupération en utilisant les mêmes paramètres.</span><span class="sxs-lookup"><span data-stu-id="0d374-108">You can use the script later to rebuild recovery images by using the same settings.</span></span> <span data-ttu-id="0d374-109">L’image de récupération fournit de nombreux outils de récupération.</span><span class="sxs-lookup"><span data-stu-id="0d374-109">The recovery image provides a variety of recovery tools.</span></span> <span data-ttu-id="0d374-110">Pour obtenir une description des outils, voir [vue d’ensemble des outils dans DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="0d374-110">For a description of the tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

<span data-ttu-id="0d374-111">Après avoir amorcé l’ordinateur dans DaRT, vous pouvez exécuter les différents outils DaRT pour essayer de diagnostiquer et de réparer l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0d374-111">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span> <span data-ttu-id="0d374-112">Cette section vous guide dans le processus de création de l’image de récupération DaRT et vous permet de sélectionner les outils et fonctionnalités que vous voulez inclure dans l’image.</span><span class="sxs-lookup"><span data-stu-id="0d374-112">This section walks you through the process of creating the DaRT recovery image and lets you select the tools and features that you want to include as part of the image.</span></span>

<span data-ttu-id="0d374-113">Vous pouvez créer l’image de récupération DaRT en utilisant l’une des deux méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="0d374-113">You can create the DaRT recovery image by using either of two methods:</span></span>

-   <span data-ttu-id="0d374-114">Utilisez l’Assistant image de récupération DaRT qui s’exécute dans un environnement Windows.</span><span class="sxs-lookup"><span data-stu-id="0d374-114">Use the DaRT Recovery Image wizard, which runs in a Windows environment.</span></span>

-   <span data-ttu-id="0d374-115">Modifiez un exemple de script PowerShell avec les valeurs de votre choix.</span><span class="sxs-lookup"><span data-stu-id="0d374-115">Modify an example PowerShell script with the values you want.</span></span> <span data-ttu-id="0d374-116">Pour plus d’informations, reportez-vous à la rubrique [utilisation d’un script PowerShell pour créer l’image de récupération](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="0d374-116">For more information, see [How to Use a PowerShell Script to Create the Recovery Image](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="0d374-117">Vous pouvez enregistrer le fichier ISO sur un CD ou un DVD enregistrable, l’enregistrer sur un disque mémoire flash ou l’enregistrer dans un format que vous pouvez utiliser pour démarrer dans DaRT à partir d’une partition distante ou d’une partition de récupération.</span><span class="sxs-lookup"><span data-stu-id="0d374-117">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span>

<span data-ttu-id="0d374-118">Une fois l’image ISO créée, vous pouvez la graver sur un CD ou un DVD vierge (si votre ordinateur est équipé d’un CD ou d’un lecteur de DVD).</span><span class="sxs-lookup"><span data-stu-id="0d374-118">Once you have created the ISO image, you can burn it onto a blank CD or DVD (if your computer has a CD or DVD drive).</span></span> <span data-ttu-id="0d374-119">Si ce n’est pas le cas, si votre ordinateur ne possède pas de lecteur, vous pouvez utiliser la plupart des programmes génériques utilisés pour graver des CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="0d374-119">If your computer does not have a drive for this purpose, you can use most generic programs that are used to burn CDs or DVDs.</span></span>

## <span data-ttu-id="0d374-120">Sélectionnez l’architecture de l’image, puis spécifiez le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="0d374-120">Select the image architecture and specify the path</span></span>


<span data-ttu-id="0d374-121">Sur la page multimédia de Windows 8, vous devez indiquer si vous voulez créer une image de récupération DaRT 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0d374-121">On the Windows 8 Media page, you select whether to create a 32-bit or 64-bit DaRT recovery image.</span></span> <span data-ttu-id="0d374-122">Utilisez les fenêtres 32 bits pour générer des images de récupération DaRT 32 bits et des fenêtres 64 bits pour générer des images de récupération DaRT de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0d374-122">Use the 32-bit Windows to build 32-bit DaRT recovery images, and 64-bit Windows to build 64-bit DaRT recovery images.</span></span> <span data-ttu-id="0d374-123">Vous pouvez utiliser un ordinateur unique pour créer des images de récupération pour les deux types d’architectures, mais vous ne pouvez pas créer une image qui fonctionne sur les architectures 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0d374-123">You can use a single computer to create recovery images for both architecture types, but you cannot create one image that works on both 32-bit and 64-bit architectures.</span></span> <span data-ttu-id="0d374-124">Vous devez également indiquer le chemin d’accès du support d’installation de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0d374-124">You also indicate the path of the Windows 8 installation media.</span></span> <span data-ttu-id="0d374-125">Choisissez l’architecture qui correspond à l’une des images de récupération que vous êtes en train de créer.</span><span class="sxs-lookup"><span data-stu-id="0d374-125">Choose the architecture that matches the one of the recovery image that you are creating.</span></span>

**<span data-ttu-id="0d374-126">Pour sélectionner l’architecture de l’image et spécifier le chemin</span><span class="sxs-lookup"><span data-stu-id="0d374-126">To select the image architecture and specify the path</span></span>**

1.  <span data-ttu-id="0d374-127">Sur la page **multimédia de Windows 8** , sélectionnez l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="0d374-127">On the **Windows 8 Media** page, select one of the following:</span></span>

    -   <span data-ttu-id="0d374-128">Si vous créez une image de récupération pour les ordinateurs 64 bits, sélectionnez **créer une image au format x64 (64 bits)**.</span><span class="sxs-lookup"><span data-stu-id="0d374-128">If you are creating a recovery image for 64-bit computers, select **Create x64 (64-bit) DaRT image**.</span></span>

    -   <span data-ttu-id="0d374-129">Si vous créez une image de récupération pour les ordinateurs 32 bits, sélectionnez **créer une image de type x86 (32 bits)**.</span><span class="sxs-lookup"><span data-stu-id="0d374-129">If you are creating a recovery image for 32-bit computers, select **Create x86 (32-bit) DaRT image**.</span></span>

2.  <span data-ttu-id="0d374-130">Dans la zone \*\*Spécifiez le chemin d’accès racine de la zone de média d’installation de Windows 8 &lt; 64 bits ou 32 &gt; \*\* bits, tapez le chemin d’accès des fichiers d’installation de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0d374-130">In the **Specify the root path of the Windows 8 &lt;64-bit or 32-bit&gt; install media** box, type the path of the Windows 8 installation files.</span></span> <span data-ttu-id="0d374-131">Utilisez une variable PATH qui correspond à l’architecture de l’image de récupération que vous êtes en train de créer.</span><span class="sxs-lookup"><span data-stu-id="0d374-131">Use a path that matches the architecture of the recovery image that you are creating.</span></span>

3.  <span data-ttu-id="0d374-132">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d374-132">Click **Next**.</span></span>

## <span data-ttu-id="0d374-133">Sélectionner les outils à inclure dans l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-133">Select the tools to include on the recovery image</span></span>


<span data-ttu-id="0d374-134">Dans la page outils, vous pouvez sélectionner de nombreux outils à inclure dans l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="0d374-134">On the Tools page, you can select numerous tools to include on the recovery image.</span></span> <span data-ttu-id="0d374-135">Ces outils seront accessibles aux utilisateurs finaux au démarrage de l’image DaRT.</span><span class="sxs-lookup"><span data-stu-id="0d374-135">These tools will be available to end users when they boot into the DaRT image.</span></span> <span data-ttu-id="0d374-136">Toutefois, si vous activez la connectivité à distance lors de la création de l’image DaRT, tous les outils seront disponibles lorsque le travailleur du support technique se connecte à l’ordinateur de l’utilisateur final, quels que soient les outils que vous avez choisi d’inclure dans l’image.</span><span class="sxs-lookup"><span data-stu-id="0d374-136">However, if you enable remote connectivity when creating the DaRT image, all of the tools will be available when a help desk worker connects to the end user’s computer, regardless of which tools you chose to include on the image.</span></span>

<span data-ttu-id="0d374-137">Pour limiter l’accès de l’utilisateur final à ces outils, tout en conservant l’accès complet aux outils par le biais de la visionneuse de connexions à distance, ne sélectionnez pas ces outils dans la page outils.</span><span class="sxs-lookup"><span data-stu-id="0d374-137">To restrict end-user access to these tools, but still retain full access to the tools through the Remote Connection Viewer, do not select those tools on the Tools page.</span></span> <span data-ttu-id="0d374-138">Les utilisateurs finaux pourront uniquement utiliser une connexion distante et pourront voir les outils que vous excluez de l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="0d374-138">End users will be able to use only Remote Connection and will be able to see, but not access, any tools that you exclude from the recovery image.</span></span>

**<span data-ttu-id="0d374-139">Pour sélectionner les outils à inclure dans l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-139">To select the tools to include on the recovery image</span></span>**

1.  <span data-ttu-id="0d374-140">Dans la page **Outils** , activez la case à cocher en regard de chaque outil que vous souhaitez inclure dans l’image.</span><span class="sxs-lookup"><span data-stu-id="0d374-140">On the **Tools** page, select the check box beside each tool that you want to include on the image.</span></span>

2.  <span data-ttu-id="0d374-141">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d374-141">Click **Next**.</span></span>

## <span data-ttu-id="0d374-142">Choisir d’autoriser ou non la connectivité à distance par un support technique</span><span class="sxs-lookup"><span data-stu-id="0d374-142">Choose whether to allow remote connectivity by a help desk</span></span>


<span data-ttu-id="0d374-143">Sur la page connexion à distance, vous pouvez choisir d’autoriser un employé du support technique à se connecter aux outils DaRT et à les exécuter sur l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="0d374-143">On the Remote Connection page, you can choose to enable a help desk worker to remotely connect to and run the DaRT tools on an end user’s computer.</span></span> <span data-ttu-id="0d374-144">L’option connectivité à distance est alors affichée comme option disponible dans la fenêtre jeu d’outils de diagnostics et de récupération.</span><span class="sxs-lookup"><span data-stu-id="0d374-144">The remote connectivity option is then shown as an available option in the Diagnostics and Recovery Toolset window.</span></span> <span data-ttu-id="0d374-145">Après avoir établi une connexion à distance, les utilisateurs du support technique peuvent exécuter les outils DaRT sur l’ordinateur de l’utilisateur final à partir d’un emplacement distant.</span><span class="sxs-lookup"><span data-stu-id="0d374-145">After help desk workers establish a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

**<span data-ttu-id="0d374-146">Pour indiquer si vous souhaitez autoriser la connectivité à distance par des travailleurs du support technique</span><span class="sxs-lookup"><span data-stu-id="0d374-146">To choose whether to allow remote connectivity by help desk workers</span></span>**

1.  <span data-ttu-id="0d374-147">Dans la page **connexion à distance** , activez la case à cocher **autoriser les connexions à** distance pour autoriser les connexions à distance, ou désactivez la case à cocher pour empêcher les connexions à distance.</span><span class="sxs-lookup"><span data-stu-id="0d374-147">On the **Remote Connection** page, select the **Allow remote connections** check box to allow remote connections, or clear the check box to prevent remote connections.</span></span>

2.  <span data-ttu-id="0d374-148">Si vous avez désactivé la case à cocher **autoriser les connexions à distance** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d374-148">If you cleared the **Allow remote connections** check box, click **Next**.</span></span> <span data-ttu-id="0d374-149">Dans le cas contraire, passez à l’étape suivante pour poursuivre la configuration de la connectivité à distance.</span><span class="sxs-lookup"><span data-stu-id="0d374-149">Otherwise, go to the next step to continue configuring remote connectivity.</span></span>

3.  <span data-ttu-id="0d374-150">Sélectionnez l’un des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="0d374-150">Select one of the following:</span></span>

    -   <span data-ttu-id="0d374-151">Laisser Windows choisir un numéro de port ouvert.</span><span class="sxs-lookup"><span data-stu-id="0d374-151">Let Windows choose an open port number.</span></span>

    -   <span data-ttu-id="0d374-152">Spécifiez le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="0d374-152">Specify the port number.</span></span> <span data-ttu-id="0d374-153">Si vous sélectionnez cette option, entrez un numéro de port compris entre 1 et 65535 dans le champ en dessous de l’option.</span><span class="sxs-lookup"><span data-stu-id="0d374-153">If you select this option, enter a port number between 1 and 65535 in the field beneath the option.</span></span> <span data-ttu-id="0d374-154">Ce numéro de port sera utilisé lors de l’établissement d’une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="0d374-154">This port number will be used when establishing a remote connection.</span></span> <span data-ttu-id="0d374-155">Nous vous recommandons d’utiliser le numéro de port 1024 ou une version ultérieure pour réduire l’éventualité d’un conflit.</span><span class="sxs-lookup"><span data-stu-id="0d374-155">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

4.  <span data-ttu-id="0d374-156">(Facultatif) dans la zone message d’accueil de la **connexion à distance** , créez un message personnalisé que les utilisateurs finaux reçoivent lors de l’établissement d’une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="0d374-156">(Optional) in the **Remote connection welcome** message box, create a customized message that end users receive when they establish a remote connection.</span></span> <span data-ttu-id="0d374-157">Le message peut contenir jusqu’à 2048 caractères.</span><span class="sxs-lookup"><span data-stu-id="0d374-157">The message can be a maximum of 2048 characters.</span></span>

5.  <span data-ttu-id="0d374-158">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d374-158">Click **Next**.</span></span>

    <span data-ttu-id="0d374-159">Pour plus d’informations sur l’exécution des outils DaRT à distance, voir [Comment récupérer des ordinateurs distants à l’aide de l’image de récupération DART](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="0d374-159">For more information about running the DaRT tools remotely, see [How to Recover Remote Computers by Using the DaRT Recovery Image](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md).</span></span>

## <span data-ttu-id="0d374-160">Ajouter des pilotes à l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-160">Add drivers to the recovery image</span></span>


<span data-ttu-id="0d374-161">Dans l’onglet pilotes de la page Options avancées, vous pouvez ajouter des pilotes de périphériques supplémentaires dont vous aurez besoin lors de la réparation d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0d374-161">On the Drivers tab of the Advanced Options page, you can add additional device drivers that you may need when repairing a computer.</span></span> <span data-ttu-id="0d374-162">Celles-ci peuvent généralement inclure des contrôleurs réseau ou de stockage que Windows 8 ne fournit pas.</span><span class="sxs-lookup"><span data-stu-id="0d374-162">These may typically include storage or network controllers that Windows 8 does not provide.</span></span> <span data-ttu-id="0d374-163">Les pilotes sont installés lors de la création de l’image.</span><span class="sxs-lookup"><span data-stu-id="0d374-163">Drivers are installed when the image is created.</span></span>

<span data-ttu-id="0d374-164">**Important**  Lorsque vous sélectionnez les pilotes à inclure, sachez que la connectivité sans fil (par exemple, Bluetooth ou 802.11 a/b/g/n) n’est pas prise en charge dans DaRT.</span><span class="sxs-lookup"><span data-stu-id="0d374-164">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="0d374-165">Pour ajouter des pilotes à l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-165">To add drivers to the recovery image</span></span>**

1.  <span data-ttu-id="0d374-166">Dans la page **Options avancées** , cliquez sur l’onglet **pilotes** .</span><span class="sxs-lookup"><span data-stu-id="0d374-166">On the **Advanced Options** page, click the **Drivers** tab.</span></span>

2.  <span data-ttu-id="0d374-167">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="0d374-167">Click **Add**.</span></span>

3.  <span data-ttu-id="0d374-168">Recherchez le fichier à ajouter pour le pilote, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="0d374-168">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="0d374-169">**Remarques**  Le fichier de pilote est fourni par le fabricant du contrôleur de stockage ou de réseau.</span><span class="sxs-lookup"><span data-stu-id="0d374-169">**Note** The driver file is provided by the manufacturer of the storage or network controller.</span></span>

     

4.  <span data-ttu-id="0d374-170">Répétez les étapes 2 et 3 pour chaque pilote que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="0d374-170">Repeat Steps 2 and 3 for every driver that you want to include.</span></span>

5.  <span data-ttu-id="0d374-171">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d374-171">Click **Next**.</span></span>

## <span data-ttu-id="0d374-172">Ajouter des packages facultatifs WinPE à l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-172">Add WinPE optional packages to the recovery image</span></span>


<span data-ttu-id="0d374-173">Dans l’onglet WinPE de la page Options avancées, vous pouvez ajouter des packages facultatifs WinPE à l’image DaRT.</span><span class="sxs-lookup"><span data-stu-id="0d374-173">On the WinPE tab of the Advanced Options page, you can add WinPE optional packages to the DaRT image.</span></span> <span data-ttu-id="0d374-174">Ces packages font partie de Windows ADK, qui est une condition d’installation requise pour l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="0d374-174">These packages are part of the Windows ADK, which is an installation prerequisite for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="0d374-175">Les outils que vous pouvez sélectionner tous sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="0d374-175">The tools that you can select are all optional.</span></span> <span data-ttu-id="0d374-176">Les packages requis sont ajoutés automatiquement en fonction des outils sélectionnés sur la page outils.</span><span class="sxs-lookup"><span data-stu-id="0d374-176">Any required packages are added automatically, based on the tools you selected on the Tools page.</span></span>

<span data-ttu-id="0d374-177">Vous pouvez également spécifier la taille de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="0d374-177">You can also specify the size of the scratch space.</span></span> <span data-ttu-id="0d374-178">Espace de travail indique la quantité d’espace disque RAM qui est configurée de façon à ce qu’elle s’exécute.</span><span class="sxs-lookup"><span data-stu-id="0d374-178">Scratch space is the amount of RAM disk space that is set aside for DaRT to run.</span></span> <span data-ttu-id="0d374-179">L’espace de travail est utile si le disque dur de l’utilisateur final n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="0d374-179">The scratch space is useful in case the end user’s hard disk is not available.</span></span> <span data-ttu-id="0d374-180">Si vous exécutez des outils et des pilotes supplémentaires, vous souhaiterez probablement augmenter l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="0d374-180">If you are running additional tools and drivers, you may want to increase the scratch space.</span></span>

**<span data-ttu-id="0d374-181">Pour ajouter des packages facultatifs WinPE à l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-181">To add WinPE optional packages to the recovery image</span></span>**

1.  <span data-ttu-id="0d374-182">Dans la page **Options avancées** , cliquez sur l’onglet **WinPE** .</span><span class="sxs-lookup"><span data-stu-id="0d374-182">On the **Advanced Options** page, click the **WinPE** tab.</span></span>

2.  <span data-ttu-id="0d374-183">Activez la case à cocher en regard de chaque package que vous voulez inclure dans l’image, ou cliquez sur la case à cocher **nom** pour sélectionner tous les packages.</span><span class="sxs-lookup"><span data-stu-id="0d374-183">Select the check box beside each package that you want to include on the image, or click the **Name** check box to select all of the packages.</span></span>

3.  <span data-ttu-id="0d374-184">Dans le champ **espace de travail** , sélectionnez l’espace disque RAM à allouer pour l’exécution de DART dans le cas où le disque dur de l’utilisateur final n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="0d374-184">In the **Scratch Space** field, select the amount of RAM disk space to allocate for running DaRT in case the end user’s hard disk is not available.</span></span>

4.  <span data-ttu-id="0d374-185">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d374-185">Click **Next**.</span></span>

## <span data-ttu-id="0d374-186">Ajouter des outils de débogage pour l’analyseur d’incidents</span><span class="sxs-lookup"><span data-stu-id="0d374-186">Add the debugging tools for Crash Analyzer</span></span>


<span data-ttu-id="0d374-187">Si vous incluez l’outil Analyseur d’incident dans l’image ISO, vous devez également inclure les outils de débogage pour Windows.</span><span class="sxs-lookup"><span data-stu-id="0d374-187">If you include the Crash Analyzer tool in the ISO image, you must also include the Debugging Tools for Windows.</span></span> <span data-ttu-id="0d374-188">Dans l’onglet analyse crash de la page Options avancées, entrez le chemin d’accès des outils de débogage de Windows 8, qui est utilisé par l’analyseur d’incident pour analyser les fichiers de vidage de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0d374-188">On the Crash Analyzer tab of the Advanced Options page, you enter the path of the Windows 8 Debugging Tools, which Crash Analyzer uses to analyze memory dump files.</span></span> <span data-ttu-id="0d374-189">Vous pouvez utiliser les outils de l’ordinateur sur lequel vous exécutez l’Assistant image de récupération DaRT ou vous pouvez utiliser les outils qui se trouvent sur l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="0d374-189">You can use the tools that are on the computer where you are running the DaRT Recovery Image wizard, or you can use the tools that are on the end-user computer.</span></span> <span data-ttu-id="0d374-190">Si vous décidez d’utiliser les outils de l’ordinateur de l’utilisateur final, n’oubliez pas que tous les ordinateurs que vous diagnostiquez doivent avoir installés les outils de débogage.</span><span class="sxs-lookup"><span data-stu-id="0d374-190">If you decide to use the tools on the end-user computer, remember that every computer that you diagnose must have the Debugging Tools installed.</span></span>

<span data-ttu-id="0d374-191">Si vous avez installé le kit de développement logiciel (SDK) Microsoft Windows ou le kit de développement Microsoft Windows (WDK), les outils de débogage de Windows 8 sont ajoutés à l’image de récupération par défaut, et le chemin d’accès aux outils de débogage est automatiquement rempli.</span><span class="sxs-lookup"><span data-stu-id="0d374-191">If you installed the Microsoft Windows Software Development Kit (SDK) or the Microsoft Windows Development Kit (WDK), the Windows 8 Debugging Tools are added to the recovery image by default, and the path to the Debugging Tools is automatically filled in.</span></span> <span data-ttu-id="0d374-192">Vous pouvez modifier le chemin d’accès des outils de débogage de Windows 8 si les fichiers sont situés à un autre endroit que l’emplacement indiqué par le chemin d’accès par défaut du fichier.</span><span class="sxs-lookup"><span data-stu-id="0d374-192">You can change the path of the Windows 8 Debugging Tools if the files are located somewhere other than the location indicated by the default file path.</span></span> <span data-ttu-id="0d374-193">Un lien dans l’Assistant vous permet de télécharger et d’installer les outils de débogage pour Windows s’ils ne le sont pas déjà.</span><span class="sxs-lookup"><span data-stu-id="0d374-193">A link in the wizard lets you download and install debugging tools for Windows if they are not already installed.</span></span>

<span data-ttu-id="0d374-194">Pour télécharger les outils de débogage Windows, voir [outils de débogage pour Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="0d374-194">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span> <span data-ttu-id="0d374-195">Installez les outils de débogage à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="0d374-195">Install the Debugging Tools to the default location.</span></span>

<span data-ttu-id="0d374-196">**Remarques**  L’Assistant DaRT vérifie les outils dans la `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` clé de registre.</span><span class="sxs-lookup"><span data-stu-id="0d374-196">**Note** The DaRT wizard checks for the tools in the `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` registry key.</span></span> <span data-ttu-id="0d374-197">S’il n’y a pas de valeur de Registre, l’Assistant recherche dans l’un des emplacements suivants, selon votre architecture système:</span><span class="sxs-lookup"><span data-stu-id="0d374-197">If the registry value is not there, the wizard looks in one of the following locations, depending on your system architecture:</span></span>

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x86`

 

**<span data-ttu-id="0d374-198">Pour ajouter les outils de débogage pour crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="0d374-198">To add the debugging tools for Crash Analyzer</span></span>**

1.  <span data-ttu-id="0d374-199">Dans la page **Options avancées** , cliquez sur l’onglet **analyse crash** .</span><span class="sxs-lookup"><span data-stu-id="0d374-199">On the **Advanced Options** page, click the **Crash Analyzer** tab.</span></span>

2.  <span data-ttu-id="0d374-200">Facultatif Cliquez sur **Télécharger les outils de débogage** pour télécharger les outils de débogage pour Windows.</span><span class="sxs-lookup"><span data-stu-id="0d374-200">(Optional) Click **Download the Debugging Tools** to download the Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="0d374-201">Sélectionnez l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="0d374-201">Select one of the following options:</span></span>

    -   <span data-ttu-id="0d374-202">**Incluez les &lt; &gt; outils de débogage de Windows 64 8 ou d' 32**bits.</span><span class="sxs-lookup"><span data-stu-id="0d374-202">**Include the Windows 8 &lt;64-bit or 32-bit&gt; Debugging Tools**.</span></span> <span data-ttu-id="0d374-203">Si vous sélectionnez cette option, recherchez et sélectionnez l’emplacement des outils si le chemin n’est pas déjà affiché.</span><span class="sxs-lookup"><span data-stu-id="0d374-203">If you select this option, browse to and select the location of the tools if the path is not already displaying.</span></span>

    -   <span data-ttu-id="0d374-204">**Utilisez les outils de débogage du système en cours de débogage**.</span><span class="sxs-lookup"><span data-stu-id="0d374-204">**Use the Debugging Tools from the system that is being debugged**.</span></span> <span data-ttu-id="0d374-205">Si vous sélectionnez cette option, l’analyseur d’incident ne fonctionnera pas si les outils de débogage pour Windows ne se trouvent pas sur le problème de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0d374-205">If you select this option, the Crash Analyzer will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

4.  <span data-ttu-id="0d374-206">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d374-206">Click **Next**.</span></span>

## <span data-ttu-id="0d374-207">Ajouter des définitions pour l’outil Defender</span><span class="sxs-lookup"><span data-stu-id="0d374-207">Add definitions for the Defender tool</span></span>


<span data-ttu-id="0d374-208">Dans l’onglet Defender de la page Options avancées, vous ajoutez des définitions, qui sont utilisées par l’outil Defender pour déterminer si un logiciel qui tente d’installer, d’exécuter ou de modifier les paramètres sur un ordinateur est indésirable ou un logiciel malveillant.</span><span class="sxs-lookup"><span data-stu-id="0d374-208">On the Defender tab of the Advanced Options page, you add definitions, which are used by the Defender tool to determine whether software that is trying to install, run, or change settings on a computer is unwanted or malicious software.</span></span>

**<span data-ttu-id="0d374-209">Pour ajouter des définitions pour l’outil Defender</span><span class="sxs-lookup"><span data-stu-id="0d374-209">To add definitions for the Defender tool</span></span>**

1.  <span data-ttu-id="0d374-210">Dans la page **Options avancées** , cliquez sur l’onglet **Defender** .</span><span class="sxs-lookup"><span data-stu-id="0d374-210">On the **Advanced Options** page, click the **Defender** tab.</span></span>

2.  <span data-ttu-id="0d374-211">Sélectionnez l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="0d374-211">Select one of the following options:</span></span>

    -   <span data-ttu-id="0d374-212">**Téléchargez les dernières définitions (recommandées)** – la mise à jour de définition démarre automatiquement et les définitions sont ajoutées à l’image de récupération Dart.</span><span class="sxs-lookup"><span data-stu-id="0d374-212">**Download the latest definitions (Recommended)** – The definition update starts automatically, and the definitions are added to the DaRT recovery image.</span></span> <span data-ttu-id="0d374-213">Cette option est recommandée pour vous aider dans les situations dans lesquelles les définitions risquent de ne pas être disponibles.</span><span class="sxs-lookup"><span data-stu-id="0d374-213">This option is recommended to help you avoid cases where the definitions might not be available.</span></span> <span data-ttu-id="0d374-214">Vous devez être connecté à Internet pour télécharger les définitions.</span><span class="sxs-lookup"><span data-stu-id="0d374-214">You must be connected to the Internet to download the definitions.</span></span>

    -   <span data-ttu-id="0d374-215">**Télécharger les définitions plus tard** : les définitions ne seront pas incluses dans l’image de récupération DART et vous devrez télécharger les définitions à partir de l’ordinateur exécutant DART.</span><span class="sxs-lookup"><span data-stu-id="0d374-215">**Download the definitions later** – Definitions will not be included in the DaRT recovery image, and you will need to download the definitions from the computer that is running DaRT.</span></span>

        <span data-ttu-id="0d374-216">Si vous décidez de ne pas inclure les dernières définitions sur l’image de récupération, ou si les définitions incluses dans l’image de récupération ne sont plus actuelles lorsque vous êtes prêt à utiliser Defender, procurez-vous les dernières définitions avant de commencer une analyse en suivant les instructions fournies dans Defender.</span><span class="sxs-lookup"><span data-stu-id="0d374-216">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use Defender, obtain the latest definitions before you begin a scan by following the instructions that are provided in Defender.</span></span>

        <span data-ttu-id="0d374-217">**Important**  Vous ne pouvez pas numériser s’il n’y a pas de définition.</span><span class="sxs-lookup"><span data-stu-id="0d374-217">**Important** You cannot scan if there are no definitions.</span></span>

         

3.  <span data-ttu-id="0d374-218">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d374-218">Click **Next**.</span></span>

## <span data-ttu-id="0d374-219">Sélectionner les types de fichiers image de récupération à créer</span><span class="sxs-lookup"><span data-stu-id="0d374-219">Select the types of recovery image files to create</span></span>


<span data-ttu-id="0d374-220">Dans la page créer une image, vous choisissez un dossier de sortie pour l’image de récupération, entrez un nom d’image, puis sélectionnez les types de fichiers image de récupération DaRT à créer.</span><span class="sxs-lookup"><span data-stu-id="0d374-220">On the Create Image page, you choose an output folder for the recovery image, enter an image name, and select the types of DaRT recovery image files to create.</span></span> <span data-ttu-id="0d374-221">Pendant le processus de création d’image de récupération, les fichiers sources Windows sont décompressés et les fichiers DaRT sont copiés vers ce fichier, et l’image est alors «recompressée» dans les formats de fichier que vous avez sélectionnés sur cette page.</span><span class="sxs-lookup"><span data-stu-id="0d374-221">During the recovery image creation process, Windows source files are unpacked, DaRT files are copied to it, and the image is then “re-packed” into the file formats that you select on this page.</span></span>

<span data-ttu-id="0d374-222">Les types de fichiers image disponibles sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="0d374-222">The available image file types are:</span></span>

-   <span data-ttu-id="0d374-223">**Fichier d’imagerie Windows (WIM)** -utilisé pour déployer DART dans un environnement d’exécution prédémarrage (PXE) ou une partition locale).</span><span class="sxs-lookup"><span data-stu-id="0d374-223">**Windows Imaging File (WIM)** - used to deploy DaRT to a preboot execution environment (PXE) or local partition).</span></span>

-   <span data-ttu-id="0d374-224">**Fichier image ISO** : utilisé pour le déploiement sur CD ou DVD, ou pour une utilisation dans les machines virtuelles (VM).</span><span class="sxs-lookup"><span data-stu-id="0d374-224">**ISO image file** – used to deploy to CD or DVD, or for use in virtual machines (VM)s).</span></span> <span data-ttu-id="0d374-225">L’Assistant nécessite que l’image ISO possède une extension de nom de fichier. ISO, car la plupart des programmes permettant de graver un CD ou un DVD nécessitent cette extension.</span><span class="sxs-lookup"><span data-stu-id="0d374-225">The wizard requires that the ISO image have an .iso file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="0d374-226">Si vous ne spécifiez pas un autre emplacement, l’image ISO est créée sur votre ordinateur de bureau portant le nom DaRT8. ISO.</span><span class="sxs-lookup"><span data-stu-id="0d374-226">If you do not specify a different location, the ISO image is created on your desktop with the name DaRT8.ISO.</span></span>

-   <span data-ttu-id="0d374-227">**Script PowerShell** : crée une image de récupération DART avec des commandes qui fournissent essentiellement les mêmes options que celles que vous pouvez sélectionner à l’aide de l’Assistant image de récupération Dart.</span><span class="sxs-lookup"><span data-stu-id="0d374-227">**PowerShell script** – creates a DaRT recovery image with commands that provide essentially the same options that you can select by using the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="0d374-228">Le script vous permet également d’ajouter ou de modifier des fichiers dans l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="0d374-228">The script also enables you to add or changes files in the DaRT recovery image.</span></span>

<span data-ttu-id="0d374-229">Si vous activez la case à cocher modifier l’image sur cette page, vous pouvez personnaliser l’image de récupération lors du processus de création d’image.</span><span class="sxs-lookup"><span data-stu-id="0d374-229">If you select the Edit Image check box on this page, you can customize the recovery image during the image creation process.</span></span> <span data-ttu-id="0d374-230">Par exemple, vous pouvez modifier le fichier «winpeshl.ini» pour créer un ordre de démarrage personnalisé ou ajouter des outils tiers.</span><span class="sxs-lookup"><span data-stu-id="0d374-230">For example, you can change the “winpeshl.ini” file to create a custom startup order or to add third-party tools.</span></span>

**<span data-ttu-id="0d374-231">Pour sélectionner les types de fichiers image de récupération à créer</span><span class="sxs-lookup"><span data-stu-id="0d374-231">To select the types of recovery image files to create</span></span>**

1.  <span data-ttu-id="0d374-232">Dans la page **créer une image** , cliquez sur **Parcourir** pour choisir le dossier de sortie du fichier image.</span><span class="sxs-lookup"><span data-stu-id="0d374-232">On the **Create Image** page, click **Browse** to choose the output folder for the image file.</span></span>

    <span data-ttu-id="0d374-233">**Remarques**  La taille de l’image peut varier en fonction des outils sélectionnés et des fichiers que vous ajoutez dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="0d374-233">**Note** The size of the image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

     

2.  <span data-ttu-id="0d374-234">Dans la zone nom de l' **image** , entrez un nom pour l’image de récupération DART, ou acceptez le nom par défaut DaRT8.</span><span class="sxs-lookup"><span data-stu-id="0d374-234">In the **Image name** box, enter a name for the DaRT recovery image, or accept the default name, which is DaRT8.</span></span>

    <span data-ttu-id="0d374-235">L’Assistant crée un sous-dossier dans le chemin de sortie à l’aide de ce nom.</span><span class="sxs-lookup"><span data-stu-id="0d374-235">The wizard creates a subfolder in the output path by this name.</span></span>

3.  <span data-ttu-id="0d374-236">Sélectionnez les types de fichiers image que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="0d374-236">Select the types of image files that you want to create.</span></span>

4.  <span data-ttu-id="0d374-237">Choisissez l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="0d374-237">Choose one of the following:</span></span>

    -   <span data-ttu-id="0d374-238">Pour modifier les fichiers dans l’image de récupération avant de créer les fichiers image, activez la case à cocher **modifier l’image** , puis cliquez sur **préparer**.</span><span class="sxs-lookup"><span data-stu-id="0d374-238">To change the files in the recovery image before you create the image files, select the **Edit Image** check box, and then click **Prepare**.</span></span>

    -   <span data-ttu-id="0d374-239">Pour créer l’image de récupération sans modifier les fichiers, cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="0d374-239">To create the recovery image without changing the files, click **Create**.</span></span>

5.  

    <span data-ttu-id="0d374-240">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d374-240">Click **Next**.</span></span>

## <span data-ttu-id="0d374-241">Modifier les fichiers image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-241">Edit the recovery image files</span></span>


<span data-ttu-id="0d374-242">Vous pouvez modifier l’image de récupération uniquement si vous avez activé la case à cocher modifier l’image dans la page créer une image.</span><span class="sxs-lookup"><span data-stu-id="0d374-242">You can edit the recovery image only if you selected the Edit Image check box on the Create Image page.</span></span> <span data-ttu-id="0d374-243">Après avoir préparé l’image de récupération, vous pouvez ajouter et modifier les fichiers image de récupération avant de créer le média amorçable.</span><span class="sxs-lookup"><span data-stu-id="0d374-243">After the recovery image has been prepared for editing, you can add and modify the recovery image files before creating the bootable media.</span></span> <span data-ttu-id="0d374-244">Par exemple, vous pouvez créer une commande personnalisée pour le démarrage, ajouter différents outils tiers, etc.</span><span class="sxs-lookup"><span data-stu-id="0d374-244">For example, you can create a custom order for startup, add various third-party tools, and so on.</span></span>

**<span data-ttu-id="0d374-245">Pour modifier les fichiers image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-245">To edit the recovery image files</span></span>**

1.  <span data-ttu-id="0d374-246">Dans la page **modifier l’image** , cliquez sur **ouvrir** dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="0d374-246">On the **Edit Image** page, click **Open** in Windows Explorer.</span></span>

2.  <span data-ttu-id="0d374-247">Créez un sous-dossier dans le dossier qui est répertorié dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0d374-247">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="0d374-248">Copiez les fichiers que vous souhaitez inclure dans le nouveau sous-dossier ou supprimez ceux que vous ne voulez pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="0d374-248">Copy the files that you want to the new subfolder, or remove files that you don’t want.</span></span>

4.  <span data-ttu-id="0d374-249">Cliquez sur **créer** pour commencer à créer l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="0d374-249">Click **Create** to start creating the recovery image.</span></span>

## <span data-ttu-id="0d374-250">Générer les fichiers image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-250">Generate the recovery image files</span></span>


<span data-ttu-id="0d374-251">Sur la page générer des fichiers, l’image de récupération DaRT est générée pour les types de fichiers que vous avez sélectionnés sur la page créer une image.</span><span class="sxs-lookup"><span data-stu-id="0d374-251">On the Generate Files page, the DaRT recovery image is generated for the file types that you selected on the Create Image page.</span></span>

**<span data-ttu-id="0d374-252">Pour générer les fichiers image de récupération</span><span class="sxs-lookup"><span data-stu-id="0d374-252">To generate the recovery image files</span></span>**

-   <span data-ttu-id="0d374-253">Dans la page **générer des fichiers** , cliquez sur **suivant** pour générer les fichiers image de récupération.</span><span class="sxs-lookup"><span data-stu-id="0d374-253">On the **Generate Files** page, click **Next** to generate the recovery image files.</span></span>

## <span data-ttu-id="0d374-254">Copier l’image de récupération sur un CD, un DVD ou un lecteur USB</span><span class="sxs-lookup"><span data-stu-id="0d374-254">Copy the recovery image to a CD, DVD, or USB</span></span>


<span data-ttu-id="0d374-255">Sur la page créer un média amorçable, vous pouvez éventuellement copier le fichier image sur un CD, un DVD ou un lecteur flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="0d374-255">On the Create Bootable Media page, you can optionally copy the image file to a CD, DVD, or USB flash drive (UFD).</span></span> <span data-ttu-id="0d374-256">Vous pouvez également créer un média amorçable supplémentaire à partir de cette page en redémarrant l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="0d374-256">You can also create additional bootable media from this page by restarting the wizard.</span></span>

<span data-ttu-id="0d374-257">**Remarques**  Le déploiement de l’environnement d’exécution prédémarrage (PXE) et du déploiement d’image locale n’est pas pris en charge en mode natif par cet outil, car ils nécessitent des outils d’entreprise supplémentaires, tels que System Center Configuration Manager et le kit de ressources de développement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0d374-257">**Note** The Preboot execution environment (PXE) and local image deployment are not supported natively by this tool since they require additional enterprise tools, such as System Center Configuration Manager server and Microsoft Development Toolkit.</span></span>

 

**<span data-ttu-id="0d374-258">Pour copier l’image de récupération sur un CD, un DVD ou un lecteur USB</span><span class="sxs-lookup"><span data-stu-id="0d374-258">To copy the recovery image to a CD, DVD, or USB</span></span>**

1.  <span data-ttu-id="0d374-259">Dans la page **créer un média amorçable** , sélectionnez le fichier ISO que vous voulez copier.</span><span class="sxs-lookup"><span data-stu-id="0d374-259">On the **Create Bootable Media** page, select the iso file that you want to copy.</span></span>

2.  <span data-ttu-id="0d374-260">Insérez un CD, un DVD ou un lecteur USB, puis sélectionnez le lecteur.</span><span class="sxs-lookup"><span data-stu-id="0d374-260">Insert a CD, DVD, or USB, and then select the drive.</span></span>

    <span data-ttu-id="0d374-261">**Remarques**  Si un lecteur n’est pas reconnu et que vous installez un nouveau lecteur, vous pouvez cliquer sur **Actualiser** pour forcer l’Assistant à mettre à jour la liste des lecteurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="0d374-261">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="0d374-262">Cliquez sur le bouton **créer un média amorçable** .</span><span class="sxs-lookup"><span data-stu-id="0d374-262">Click the **Create Bootable Media** button.</span></span>

4.  <span data-ttu-id="0d374-263">Pour créer une autre image de récupération, cliquez sur redémarrer ou cliquez sur **Fermer** si vous avez fini de créer tous les éléments multimédias de votre choix.</span><span class="sxs-lookup"><span data-stu-id="0d374-263">To create another recovery image, click Restart, or click **Close** if you have finished creating all of the media that you want.</span></span>

## <span data-ttu-id="0d374-264">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d374-264">Related topics</span></span>


[<span data-ttu-id="0d374-265">Vue d'ensemble des outils de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="0d374-265">Overview of the Tools in DaRT 8.0</span></span>](overview-of-the-tools-in-dart-80-dart-8.md)

[<span data-ttu-id="0d374-266">Déploiement de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="0d374-266">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 






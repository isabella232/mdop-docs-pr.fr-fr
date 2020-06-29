---
title: Procédure d'utilisation de l'Assistant Image de récupération DaRT pour créer l'image de récupération
description: Procédure d'utilisation de l'Assistant Image de récupération DaRT pour créer l'image de récupération
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809647"
---
# <span data-ttu-id="38e68-103">Procédure d'utilisation de l'Assistant Image de récupération DaRT pour créer l'image de récupération</span><span class="sxs-lookup"><span data-stu-id="38e68-103">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="38e68-104">Microsoft Diagnostics and Recovery Tools (DaRT) 7 inclut l' **Assistant image de récupération DART** utilisé dans Windows pour créer une image ISO (International Organization for Standardization) amorçable.</span><span class="sxs-lookup"><span data-stu-id="38e68-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="38e68-105">Une image ISO est un fichier qui représente le contenu brut d’un CD.</span><span class="sxs-lookup"><span data-stu-id="38e68-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

<span data-ttu-id="38e68-106">L' **Assistant image de récupération DART** nécessite les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="38e68-106">The **DaRT Recovery Image Wizard** requires the following information:</span></span>

-   <span data-ttu-id="38e68-107">**Image de démarrage**° ° vous devez fournir le chemin d’accès d’un DVD Windows 7 ou de fichiers sources Windows 7 requis pour créer l’image de récupération Dart.</span><span class="sxs-lookup"><span data-stu-id="38e68-107">**Boot Image**˚˚You must provide the path of a Windows 7 DVD or Windows 7 source files that are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="38e68-108">**Sélection d’outil**n ° ° vous pouvez sélectionner les outils à inclure dans l’image de récupération Dart.</span><span class="sxs-lookup"><span data-stu-id="38e68-108">**Tool Selection**˚˚You can select the tools to include on the DaRT recovery image.</span></span>

-   <span data-ttu-id="38e68-109">**Connexions distantes**n ° vous pouvez indiquer si vous souhaitez que l’image de récupération DART inclue la possibilité d’établir une connexion à distance entre le support technique et l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="38e68-109">**Remote Connections**˚˚You can select whether you want the DaRT recovery image to include the ability to establish a remote connection between the helpdesk and the end-user computer.</span></span>

-   <span data-ttu-id="38e68-110">**Outils de débogage pour Windows**n ° vous êtes invité à fournir l’emplacement des outils de débogage pour Windows.</span><span class="sxs-lookup"><span data-stu-id="38e68-110">**Debugging Tools for Windows**˚˚You are asked to provide the location of the Debugging Tools for Windows.</span></span>

-   <span data-ttu-id="38e68-111">**Définitions pour le nettoyeur de systèmes autonome**n ° vous pouvez déterminer si vous souhaitez télécharger les dernières définitions au moment où vous créez l’image de récupération ou téléchargez les définitions ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="38e68-111">**Definitions for Standalone System Sweeper**˚˚You can decide whether to download the latest definitions at the time that you create the recovery image or download the definitions later.</span></span>

-   <span data-ttu-id="38e68-112">Les **pilotes**° ° vous demandent si vous souhaitez ajouter des pilotes à l’image ISO.</span><span class="sxs-lookup"><span data-stu-id="38e68-112">**Drivers**˚˚You are asked whether you want to add drivers to the ISO image.</span></span>

-   <span data-ttu-id="38e68-113">**Fichiers supplémentaires**° ° vous pouvez ajouter des fichiers à l’image ISO qui peut vous aider à diagnostiquer des problèmes.</span><span class="sxs-lookup"><span data-stu-id="38e68-113">**Additional Files**˚˚You can add files to the ISO image that might help diagnose problems.</span></span>

-   <span data-ttu-id="38e68-114">**Emplacement de l’image ISO**° ° vous êtes invité à spécifier l’emplacement de l’image ISO.</span><span class="sxs-lookup"><span data-stu-id="38e68-114">**ISO Image Location**˚˚You are asked to specify where the ISO image should be located.</span></span>

-   <span data-ttu-id="38e68-115">**Lecteur de CD-DVD**° ° vous êtes invité à indiquer si le CD ou le lecteur DVD doit être utilisé pour graver le CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="38e68-115">**CD/DVD Drive**˚˚You are asked to specify whether the CD or DVD drive should be used to burn the CD or DVD.</span></span>

<span data-ttu-id="38e68-116">**Remarques**  La taille de l’image ISO peut varier en fonction des outils sélectionnés dans l' **Assistant image de récupération DART**.</span><span class="sxs-lookup"><span data-stu-id="38e68-116">**Note** The ISO image size can vary, depending on the tools that were selected in the **DaRT Recovery Image Wizard**.</span></span>

 

## <span data-ttu-id="38e68-117">Pour créer l’image de récupération à l’aide de l’Assistant image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="38e68-117">To create the recovery image using the DaRT Recovery Image Wizard</span></span>


<span data-ttu-id="38e68-118">Suivez ces instructions pour utiliser l' **Assistant image de récupération DART** pour créer l’image de récupération Dart.</span><span class="sxs-lookup"><span data-stu-id="38e68-118">Follow these instructions to use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span>

### <span data-ttu-id="38e68-119">Pour sélectionner les outils à inclure dans l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="38e68-119">To select the tools to include on the DaRT recovery image</span></span>

<span data-ttu-id="38e68-120">L' **Assistant image de récupération DART** présente une boîte de dialogue de **sélection d’outil** .</span><span class="sxs-lookup"><span data-stu-id="38e68-120">The **DaRT Recovery Image Wizard** presents a **Tool Selection** dialog box.</span></span> <span data-ttu-id="38e68-121">Vous pouvez sélectionner ou supprimer des outils dans la liste d’outils à inclure dans l’image de récupération DaRT en mettant en surbrillance un outil, puis en cliquant sur les boutons **activer** ou **Désactiver** .</span><span class="sxs-lookup"><span data-stu-id="38e68-121">You can select or remove tools from the list of tools to be included on the DaRT recovery image by highlighting a tool and then clicking the **Enable** or **Disable** buttons.</span></span>

<span data-ttu-id="38e68-122">Lorsque vous avez sélectionné tous les outils que vous voulez inclure dans l’image de récupération, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="38e68-122">After you have selected all the tools that you want to include on the recovery image, click **Next**.</span></span>

### <span data-ttu-id="38e68-123">Pour ajouter l’option autorisant la connectivité à distance</span><span class="sxs-lookup"><span data-stu-id="38e68-123">To add the option to allow remote connectivity</span></span>

<span data-ttu-id="38e68-124">Vous pouvez activer la case à cocher **autoriser les connexions à distance** pour proposer l’option dans la fenêtre du **jeu d’outils de diagnostics et de récupération** pour établir une connexion à distance entre l’agent de support technique et un ordinateur d’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="38e68-124">You can select the **Allow remote connections** check box to provide the option in the **Diagnostics and Recovery Toolset** window to establish a remote connection between the helpdesk agent and an end-user computer.</span></span> <span data-ttu-id="38e68-125">Après avoir établi une connexion à distance, un agent de support technique peut exécuter les outils DaRT sur l’ordinateur de l’utilisateur final à partir d’un emplacement distant.</span><span class="sxs-lookup"><span data-stu-id="38e68-125">After a helpdesk agent establishes a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

<span data-ttu-id="38e68-126">Vous pouvez activer la case à cocher **spécifier le numéro de port** pour entrer un numéro de port spécifique qui sera utilisé lors de l’établissement d’une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="38e68-126">You can select the **Specify the port number** check box to enter a specific port number that will be used when establishing a remote connection.</span></span> <span data-ttu-id="38e68-127">Vous pouvez spécifier un numéro de port compris entre 1 et 65535.</span><span class="sxs-lookup"><span data-stu-id="38e68-127">You can specify a port number between 1 and 65535.</span></span> <span data-ttu-id="38e68-128">Nous vous recommandons d’utiliser le numéro de port 1024 ou une version ultérieure pour réduire l’éventualité d’un conflit.</span><span class="sxs-lookup"><span data-stu-id="38e68-128">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

<span data-ttu-id="38e68-129">Vous pouvez également créer un message personnalisé qui sera reçu par un utilisateur final lors de l’établissement d’une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="38e68-129">You can also create a customized message that an end user will receive when they establish a remote connection.</span></span> <span data-ttu-id="38e68-130">Le message peut contenir jusqu’à 2048 caractères.</span><span class="sxs-lookup"><span data-stu-id="38e68-130">The message can be a maximum of 2048 characters.</span></span>

<span data-ttu-id="38e68-131">Pour plus d’informations sur l’utilisation à distance des outils DaRT, voir récupération [d’ordinateurs distants à l’aide de l’image de récupération DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="38e68-131">For more information about remotely running the DaRT tools, see [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="38e68-132">Pour ajouter les outils de débogage pour Windows à l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="38e68-132">To add the Debugging Tools for Windows to the DaRT recovery image</span></span>

<span data-ttu-id="38e68-133">Dans la boîte de dialogue **analyse crash** de l' **Assistant image de récupération DART**, vous êtes invité à spécifier l’emplacement des outils de débogage pour Windows.</span><span class="sxs-lookup"><span data-stu-id="38e68-133">In the **Crash Analyzer** dialog box of the **DaRT Recovery Image Wizard**, you are asked to specify the location of the Debugging Tools for Windows.</span></span> <span data-ttu-id="38e68-134">Si vous n’avez pas de copie des outils, vous pouvez les télécharger à partir de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="38e68-134">If you do not have a copy of the tools, you can download them from Microsoft.</span></span> <span data-ttu-id="38e68-135">Le lien suivant pour accéder à la page de téléchargement est fourni dans l’Assistant: [Télécharger et installer les outils de débogage pour Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="38e68-135">The following link to the download page is provided in the wizard: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

<span data-ttu-id="38e68-136">Vous pouvez spécifier l’emplacement des outils de débogage sur l’ordinateur sur lequel vous exécutez l' **Assistant image de récupération DART**ou vous pouvez choisir d’utiliser les outils présents sur l’ordinateur de destination.</span><span class="sxs-lookup"><span data-stu-id="38e68-136">You can either specify the location of the debugging tools on the computer where you are running the **DaRT Recovery Image Wizard**, or you can decide to use the tools that are located on the destination computer.</span></span> <span data-ttu-id="38e68-137">Si vous décidez d’utiliser une copie sur un autre ordinateur, vous devez vous assurer que les outils sont installés sur chaque ordinateur sur lequel vous diagnostiquez un blocage.</span><span class="sxs-lookup"><span data-stu-id="38e68-137">If you decide to use a copy on another computer, you must make sure that the tools are installed on each computer on which you are diagnosing a crash.</span></span>

<span data-ttu-id="38e68-138">**Remarques**  Si vous incluez l' **analyseur d’incident** dans l’image ISO, nous vous recommandons d’inclure également les outils de débogage pour Windows.</span><span class="sxs-lookup"><span data-stu-id="38e68-138">**Note** If you include the **Crash Analyzer** in the ISO image, we recommend that you also include the Debugging Tools for Windows.</span></span>

 

<span data-ttu-id="38e68-139">Pour ajouter les outils de débogage pour Windows, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="38e68-139">Follow these steps to add the Debugging Tools for Windows:</span></span>

1.  <span data-ttu-id="38e68-140">Facultatif Cliquez sur le lien hypertexte pour télécharger les outils de débogage pour Windows.</span><span class="sxs-lookup"><span data-stu-id="38e68-140">(Optional) Click the hyperlink to download the Debugging Tools for Windows.</span></span>

2.  <span data-ttu-id="38e68-141">Sélectionnez l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="38e68-141">Select one of the following options:</span></span>

    -   <span data-ttu-id="38e68-142">**Utilisez les outils de débogage pour Windows à l’emplacement suivant**.</span><span class="sxs-lookup"><span data-stu-id="38e68-142">**Use the Debugging Tools for Windows in the following location**.</span></span> <span data-ttu-id="38e68-143">Si vous sélectionnez cette option, vous pouvez accéder à l’emplacement des outils.</span><span class="sxs-lookup"><span data-stu-id="38e68-143">If you select this option, you can browse to the location of the tools.</span></span>

    -   <span data-ttu-id="38e68-144">**Recherchez les outils de débogage pour Windows sur le système que vous réparez**.</span><span class="sxs-lookup"><span data-stu-id="38e68-144">**Locate the Debugging Tools for Windows on the system that you are repairing**.</span></span> <span data-ttu-id="38e68-145">Si vous sélectionnez cette option, l' **analyseur d’incident** ne fonctionnera pas si les outils de débogage pour Windows ne se trouvent pas sur le problème de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="38e68-145">If you select this option, the **Crash Analyzer** will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

3.  <span data-ttu-id="38e68-146">Lorsque vous avez terminé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="38e68-146">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="38e68-147">Pour ajouter les définitions du nettoyeur système autonome à l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="38e68-147">To add definitions for Standalone System Sweeper to the DaRT recovery image</span></span>

<span data-ttu-id="38e68-148">Les définitions constituent un référentiel de logiciels malveillants connus et d’autres logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="38e68-148">Definitions are a repository of known malware and other potentially unwanted software.</span></span> <span data-ttu-id="38e68-149">Dans la mesure où un logiciel malveillant est en **cours de développement, il** repose sur les définitions actuelles pour déterminer si un logiciel qui tente d’installer, d’exécuter ou de modifier des paramètres sur un ordinateur est potentiellement indésirable ou malveillant.</span><span class="sxs-lookup"><span data-stu-id="38e68-149">Because malware is being continually developed, **Standalone System Sweeper** relies on current definitions to determine whether software that is trying to install, run, or change settings on a computer is potentially unwanted or malicious software.</span></span>

<span data-ttu-id="38e68-150">Pour inclure les dernières définitions dans l’image de récupération DaRT (recommandé), cliquez sur **Oui, puis téléchargez les dernières définitions.**</span><span class="sxs-lookup"><span data-stu-id="38e68-150">To include the latest definitions in the DaRT recovery image (recommended), click **Yes, download the latest definitions.**</span></span> <span data-ttu-id="38e68-151">La mise à jour des définitions démarre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="38e68-151">The definition update starts automatically.</span></span> <span data-ttu-id="38e68-152">Vous devez être connecté à Internet pour terminer ce processus.</span><span class="sxs-lookup"><span data-stu-id="38e68-152">You must be connected to the Internet to complete this process.</span></span>

<span data-ttu-id="38e68-153">Pour ignorer la mise à jour de définition, cliquez sur **non, télécharger manuellement les définitions plus tard**.</span><span class="sxs-lookup"><span data-stu-id="38e68-153">To skip the definition update, click **No, manually download definitions later**.</span></span> <span data-ttu-id="38e68-154">Les définitions ne seront pas incluses dans l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="38e68-154">Definitions will not be included in the DaRT recovery image.</span></span>

<span data-ttu-id="38e68-155">Si vous décidez de ne pas inclure les dernières définitions sur l’image de récupération, ou si les définitions incluses dans l’image de récupération ne sont plus actuelles lorsque vous êtes prêt à utiliser un **nettoyeur système autonome**, vous pouvez obtenir les dernières définitions avant de commencer une analyse en suivant les instructions fournies dans la version **autonome du système**.</span><span class="sxs-lookup"><span data-stu-id="38e68-155">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use **Standalone System Sweeper**, obtain the latest definitions before you begin a scan by following the instructions that are provided in the **Standalone System Sweeper**.</span></span>

<span data-ttu-id="38e68-156">**Important**  Vous ne pouvez pas numériser s’il n’y a pas de définition.</span><span class="sxs-lookup"><span data-stu-id="38e68-156">**Important** You cannot scan if there are no definitions.</span></span>

 

<span data-ttu-id="38e68-157">Lorsque vous avez terminé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="38e68-157">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="38e68-158">Pour ajouter des pilotes à l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="38e68-158">To add drivers to the DaRT recovery image</span></span>

<span data-ttu-id="38e68-159">**Attention**  Par défaut, lorsque vous ajoutez un pilote à l’image de récupération DaRT, tous les fichiers et sous-dossiers situés dans ce dossier sont ajoutés à l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="38e68-159">**Caution** By default, when you add a driver to the DaRT recovery image, all additional files and subfolders that are located in that folder are added into the recovery image.</span></span> <span data-ttu-id="38e68-160">Pour plus d’informations, reportez-vous à la rubrique [résolution des problèmes DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="38e68-160">For more information, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>

 

<span data-ttu-id="38e68-161">Vous devez inclure des pilotes supplémentaires sur l’image de récupération pour DaRT7 que vous avez peut-être besoin lors de la réparation d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="38e68-161">You should include additional drivers on the recovery image for DaRT7 that you may need when repairing a computer.</span></span> <span data-ttu-id="38e68-162">En règle générale, ces contrôleurs de réseau ou de stockage ne sont pas inclus sur le DVD Windows.</span><span class="sxs-lookup"><span data-stu-id="38e68-162">These may typically include storage or network controllers that are not included on the Windows DVD.</span></span>

<span data-ttu-id="38e68-163">**Important**  Lorsque vous sélectionnez les pilotes à inclure, sachez que la connectivité sans fil (par exemple, Bluetooth ou 802.11 a/b/g/n) n’est pas prise en charge dans DaRT.</span><span class="sxs-lookup"><span data-stu-id="38e68-163">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="38e68-164">Pour ajouter un pilote de stockage ou de contrôleur de réseau à l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="38e68-164">To add a storage or network controller driver to the recovery image</span></span>**

1.  <span data-ttu-id="38e68-165">Dans la boîte de dialogue **pilotes supplémentaires** de l' **Assistant image de récupération DART**, cliquez sur **Ajouter un périphérique**.</span><span class="sxs-lookup"><span data-stu-id="38e68-165">In the **Additional Drivers** dialog box of the **DaRT Recovery Image Wizard**, click **Add Device**.</span></span>

2.  <span data-ttu-id="38e68-166">Recherchez le fichier à ajouter pour le pilote, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="38e68-166">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="38e68-167">**Remarques**  Le fichier de **pilote** est fourni par le fabricant du contrôleur de stockage ou de réseau.</span><span class="sxs-lookup"><span data-stu-id="38e68-167">**Note** The **driver** file is provided by the manufacturer of the storage or network controller.</span></span>

     

3.  <span data-ttu-id="38e68-168">Répétez les étapes 1 et 2 pour chaque pilote que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="38e68-168">Repeat Steps 1 and 2 for every driver that you want to include.</span></span>

4.  <span data-ttu-id="38e68-169">Lorsque vous avez terminé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="38e68-169">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="38e68-170">Pour ajouter des fichiers à l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="38e68-170">To add files to the DaRT recovery image</span></span>

<span data-ttu-id="38e68-171">Suivez ces étapes pour ajouter des fichiers à l’image de récupération afin de pouvoir les utiliser pour diagnostiquer des problèmes d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="38e68-171">Follow these steps to add files to the recovery image so that you can use them to diagnose computer problems.</span></span>

1.  <span data-ttu-id="38e68-172">Dans la boîte de dialogue **fichiers supplémentaires** de l' **Assistant image de récupération DART**, cliquez sur **afficher les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="38e68-172">In the **Additional Files** dialog box of the **DaRT Recovery Image Wizard**, click **Show Files**.</span></span> <span data-ttu-id="38e68-173">Une fenêtre de l’Explorateur s’ouvre et affiche le dossier contenant les fichiers partagés.</span><span class="sxs-lookup"><span data-stu-id="38e68-173">This opens an Explorer window that displays the folder that holds the shared files.</span></span>

2.  <span data-ttu-id="38e68-174">Créez un sous-dossier dans le dossier qui est répertorié dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="38e68-174">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="38e68-175">Copiez les fichiers que vous souhaitez inclure dans le nouveau sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="38e68-175">Copy the files that you want to the new subfolder.</span></span>

4.  <span data-ttu-id="38e68-176">Lorsque vous avez terminé, cliquez sur **suivant.**</span><span class="sxs-lookup"><span data-stu-id="38e68-176">After you have finished, click **Next.**</span></span>

### <span data-ttu-id="38e68-177">Pour sélectionner l’emplacement de la feuille de style ISO qui contient l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="38e68-177">To select a location for the ISO that contains the DaRT recovery image</span></span>

<span data-ttu-id="38e68-178">Suivez ces étapes pour spécifier l’emplacement de création de l’image ISO:</span><span class="sxs-lookup"><span data-stu-id="38e68-178">Follow these steps to specify the location where the ISO image is created:</span></span>

1.  <span data-ttu-id="38e68-179">Dans la boîte de dialogue **créer une image de démarrage** de l' **Assistant image de récupération DART**, cliquez sur **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="38e68-179">In the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**, click **Browse**.</span></span>

2.  <span data-ttu-id="38e68-180">Naviguez jusqu’à l’emplacement préféré dans la fenêtre **Enregistrer sous** , puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="38e68-180">Browse to the preferred location in the **Save As** window, and then click **Save**.</span></span>

3.  <span data-ttu-id="38e68-181">Lorsque vous avez terminé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="38e68-181">After you have finished, click **Next**.</span></span>

<span data-ttu-id="38e68-182">La taille de l’image ISO peut varier en fonction des outils sélectionnés et des fichiers que vous ajoutez dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="38e68-182">The size of the ISO image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

<span data-ttu-id="38e68-183">L’Assistant nécessite que l’image ISO ait une extension de nom de fichier **. ISO** , car la plupart des programmes permettant de graver un CD ou un DVD nécessitent cette extension.</span><span class="sxs-lookup"><span data-stu-id="38e68-183">The wizard requires the ISO image to have an **.iso** file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="38e68-184">Si vous ne spécifiez pas un autre emplacement, l’image ISO est créée sur votre ordinateur de bureau portant le nom **DaRT70. ISO**.</span><span class="sxs-lookup"><span data-stu-id="38e68-184">If you do not specify a different location, the ISO image is created on your desktop with the name **DaRT70.ISO**.</span></span>

### <span data-ttu-id="38e68-185">Pour graver l’image de récupération sur un CD ou un DVD</span><span class="sxs-lookup"><span data-stu-id="38e68-185">To burn the recovery image to a CD or DVD</span></span>

<span data-ttu-id="38e68-186">Si l' **Assistant image de récupération de DART** détecte un lecteur CD-RW compatible sur votre ordinateur, il propose de graver l’image ISO sur un disque.</span><span class="sxs-lookup"><span data-stu-id="38e68-186">If the **DaRT Recovery Image Wizard** detects a compatible CD-RW drive on your computer, it offers to burn the ISO image to a disc for you.</span></span> <span data-ttu-id="38e68-187">Si vous voulez graver un CD ou un DVD et que l’Assistant ne reconnaît pas votre lecteur, vous devez utiliser un autre programme, tel que le programme fourni avec votre lecteur.</span><span class="sxs-lookup"><span data-stu-id="38e68-187">If you want to burn a CD or DVD and the wizard does not recognize your drive, you must use another program, such as the program that was included with your drive.</span></span> <span data-ttu-id="38e68-188">Vous pouvez utiliser un dupliquateur, un service de duplication ou un logiciel de gravure de DVD ou de DVD pour apporter d’autres copies.</span><span class="sxs-lookup"><span data-stu-id="38e68-188">You can use a duplicator, a duplicating service, or CD or DVD-burning software to make any additional copies.</span></span>

1.  <span data-ttu-id="38e68-189">Dans la boîte de dialogue **graver un CD ou un DVD enregistrable** de l' **Assistant image de récupération de DART**, sélectionnez **graver l’image sur le lecteur de CD/DVD enregistrable suivant**.</span><span class="sxs-lookup"><span data-stu-id="38e68-189">In the **Burn to a recordable CD/DVD** dialog box of the **DaRT Recovery Image Wizard**, select **Burn the image to the following recordable CD/DVD drive**.</span></span>

2.  <span data-ttu-id="38e68-190">Sélectionnez le lecteur de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="38e68-190">Select the CD or DVD drive.</span></span>

    <span data-ttu-id="38e68-191">**Remarques**  Si un lecteur n’est pas reconnu et que vous installez un nouveau lecteur, vous pouvez cliquer sur **Actualiser la liste** des lecteurs pour obliger l’Assistant à mettre à jour la liste des lecteurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="38e68-191">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh Drive List** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="38e68-192">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="38e68-192">Click **Next**.</span></span>

## <span data-ttu-id="38e68-193">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38e68-193">Related topics</span></span>


[<span data-ttu-id="38e68-194">Création de l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="38e68-194">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 






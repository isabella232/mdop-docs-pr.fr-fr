---
title: Création d'une image Windows Virtual PC pour MED-V
description: Création d'une image Windows Virtual PC pour MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804411"
---
# <span data-ttu-id="f0bf1-103">Création d'une image Windows Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="f0bf1-103">Creating a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="f0bf1-104">Pour pouvoir livrer une entreprise MED-V aux utilisateurs, vous devez commencer par préparer un disque dur virtuel qui vous permet de générer le package d’installation de l’espace de travail MED-V pour la virtualisation de l’ordinateur de bureau Microsoft entreprise (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-104">Before you can deliver a MED-V workspace to users, you have to first prepare a virtual hard disk that you use to build the MED-V workspace installer package for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="f0bf1-105">Pour préparer le disque dur virtuel requis, vous devez créer une image de PC virtuel Windows qui contient le système d’exploitation, les mises à jour et le logiciel requis pour vous permettre de déployer plus tard les informations relatives à la redirection des applications et de la redirection d’URL vers les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-105">To prepare the necessary virtual hard disk, you must create a Windows Virtual PC image that contains the required operating system, updates, and software to let you later deploy applications and URL redirection information to users.</span></span> <span data-ttu-id="f0bf1-106">Cette section fournit des recommandations sur la création du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-106">This section provides guidance about how to create the virtual hard disk.</span></span>

<span data-ttu-id="f0bf1-107">Pour créer une image virtuelle pour MED-V, vous devez suivre les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-107">To create a virtual image for MED-V, you must follow these steps.</span></span>

1.  [<span data-ttu-id="f0bf1-108">Créer une image de PC virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="f0bf1-108">Create a Windows Virtual PC image</span></span>](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [<span data-ttu-id="f0bf1-109">Installer Windows XP sur l’image</span><span class="sxs-lookup"><span data-stu-id="f0bf1-109">Install Windows XP on the image</span></span>](#bkmk-installingwindowsxpontovpc)

3.  [<span data-ttu-id="f0bf1-110">Installation de .NET Framework sur l’image</span><span class="sxs-lookup"><span data-stu-id="f0bf1-110">Install the .NET Framework on the image</span></span>](#bkmk-installingnet)

4.  [<span data-ttu-id="f0bf1-111">Appliquer des mises à jour à l’image</span><span class="sxs-lookup"><span data-stu-id="f0bf1-111">Apply updates to the image</span></span>](#bkmk-applypatchestovpc)

5.  [<span data-ttu-id="f0bf1-112">Installer les composants d’intégration</span><span class="sxs-lookup"><span data-stu-id="f0bf1-112">Install Integration Components</span></span>](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="f0bf1-113">Créer une image de PC virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="f0bf1-113">Creating a Windows Virtual PC Image</span></span>


<span data-ttu-id="f0bf1-114">Pour créer une image de PC virtuel Windows, consultez la documentation sur le PC virtuel Windows:</span><span class="sxs-lookup"><span data-stu-id="f0bf1-114">To create a Windows Virtual PC image, see the Windows Virtual PC documentation:</span></span>

-   <span data-ttu-id="f0bf1-115">[Page d’accueil de l’ordinateur virtuel Windows](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .</span><span class="sxs-lookup"><span data-stu-id="f0bf1-115">[Windows Virtual PC Home Page](https://go.microsoft.com/fwlink/?LinkId=148103) (https://go.microsoft.com/fwlink/?LinkId=148103).</span></span>

-   <span data-ttu-id="f0bf1-116">[Aide de l’application Virtual PC Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="f0bf1-116">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="f0bf1-117">Par ailleurs, si vous disposez déjà d’un fichier d’image Windows (WIM) que vous souhaitez utiliser comme base pour votre image virtuelle, vous pouvez le convertir en VHD qui vous permet de créer l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-117">Alternately, if you already have a Windows Imaging (WIM) file that you want to use as the basis for your virtual image, you can convert it to a VHD that you use to build the MED-V workspace.</span></span> <span data-ttu-id="f0bf1-118">Pour plus d’informations sur la façon de convertir un WIM vers un disque dur virtuel, voir [prise en charge native de VHD dans Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .</span><span class="sxs-lookup"><span data-stu-id="f0bf1-118">For more information about how to convert a WIM to a virtual hard disk, see [Native VHD Support in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) (https://go.microsoft.com/fwlink/?LinkId=195922).</span></span>

<span data-ttu-id="f0bf1-119">**Important**  MED-V ne prend en charge qu’un disque dur virtuel par ordinateur virtuel et une seule partition sur chaque disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-119">**Important** MED-V only supports one virtual hard disk per virtual machine and only one partition on each virtual disk.</span></span>

 

<span data-ttu-id="f0bf1-120">Une fois que vous avez créé votre disque dur virtuel, installez Windows XP sur l’image.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-120">After you have created your virtual hard disk, install Windows XP on the image.</span></span>

## <a href="" id="bkmk-installingwindowsxpontovpc"></a><span data-ttu-id="f0bf1-121">Installation de Windows XP sur une image de PC virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="f0bf1-121">Installing Windows XP on a Windows Virtual PC Image</span></span>


<span data-ttu-id="f0bf1-122">MED-V nécessite l’installation de Windows XP SP3 sur l’image du PC virtuel Windows avant de créer l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-122">MED-V requires that Windows XP SP3 is installed on the Windows Virtual PC image before you build the MED-V workspace.</span></span>

<span data-ttu-id="f0bf1-123">Pour plus d’informations sur l’installation de Windows XP, voir [créer une machine virtuelle et installer un système d’exploitation invité](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .</span><span class="sxs-lookup"><span data-stu-id="f0bf1-123">For more information about how to install Windows XP, see [Create a virtual machine and install a guest operating system](https://go.microsoft.com/fwlink/?LinkId=182379) (https://go.microsoft.com/fwlink/?LinkId=182379).</span></span>

## <a href="" id="bkmk-installingnet"></a><span data-ttu-id="f0bf1-124">Installation de .NET Framework 3,5 SP1 sur une image de PC virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="f0bf1-124">Installing the .NET Framework 3.5 SP1 on a Windows Virtual PC Image</span></span>


<span data-ttu-id="f0bf1-125">Vous devez installer manuellement .NET Framework 3,5 SP1 et la mise à jour KB959209 dans l’image du PC virtuel Windows que vous préparez pour une utilisation avec MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-125">You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="f0bf1-126">Le [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) de mise à jour ( https://go.microsoft.com/fwlink/?LinkId=204950) résout plusieurs problèmes de compatibilité d’application connus.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-126">The update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950) addresses several known application compatibility issues.</span></span>

## <a href="" id="bkmk-applypatchestovpc"></a><span data-ttu-id="f0bf1-127">Appliquer des mises à jour à l’image du PC virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="f0bf1-127">Applying Updates to the Windows Virtual PC Image</span></span>


<span data-ttu-id="f0bf1-128">Une fois que vous avez installé Windows XP sur votre machine virtuelle, installez les mises à jour Windows XP requises sur l’image, par exemple SP3.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-128">After you have installed Windows XP on your virtual machine, install any required Windows XP updates on the image, such as SP3.</span></span> <span data-ttu-id="f0bf1-129">Vous pouvez également installer certaines mises à jour facultatives pour de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-129">You can also install certain optional updates for better performance.</span></span>

<span data-ttu-id="f0bf1-130">**Important**  Pour MED-V, Windows XP SP3 doit être en cours d’exécution sur le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-130">**Important** MED-V requires that Windows XP SP3 be running on the guest operating system.</span></span>

 

<span data-ttu-id="f0bf1-131">**Avertissement**  Lorsque vous installez les mises à jour apportées à Windows XP, assurez-vous de conserver la version d’Internet Explorer que vous envisagez d’utiliser dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-131">**Warning** When you install updates to Windows XP, make sure that you remain on the version of Internet Explorer in the guest that you intend to use in the MED-V workspace.</span></span> <span data-ttu-id="f0bf1-132">Par exemple, si vous envisagez d’exécuter Internet Explorer 6 dans l’espace de travail MED-V, assurez-vous que les mises à jour que vous installez ne comprennent pas Internet Explorer 7 ou Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-132">For example, if you intend to run Internet Explorer 6 in the MED-V workspace, make sure that any updates that you install now do not include Internet Explorer 7 or Internet Explorer 8.</span></span> <span data-ttu-id="f0bf1-133">Par ailleurs, nous vous recommandons de configurer le registre pour empêcher les mises à jour automatiques de mettre à niveau Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-133">In addition, we recommend that you configure the registry to prevent automatic updates from upgrading Internet Explorer.</span></span>

 

### <span data-ttu-id="f0bf1-134">Installation d’une mise à jour de performance facultative</span><span class="sxs-lookup"><span data-stu-id="f0bf1-134">Installing an Optional Performance Update</span></span>

<span data-ttu-id="f0bf1-135">Même s’il est facultatif, nous vous recommandons d’installer la mise à jour suivante pour [Hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) .</span><span class="sxs-lookup"><span data-stu-id="f0bf1-135">Although it is optional, we recommend that you install the following update for [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) (https://go.microsoft.com/fwlink/?LinkId=201077).</span></span> <span data-ttu-id="f0bf1-136">Cette mise à jour améliore les performances des dossiers partagés dans une session de services Terminal Server:</span><span class="sxs-lookup"><span data-stu-id="f0bf1-136">This update increases the performance of shared folders in a Terminal Services session:</span></span>

<span data-ttu-id="f0bf1-137">**Remarques**  La mise à jour est publiquement disponible.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-137">**Note** The update is publicly available.</span></span> <span data-ttu-id="f0bf1-138">Toutefois, vous pouvez être invité à accepter un contrat pour les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-138">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="f0bf1-139">Suivez les invites sur les pages Web successives pour récupérer ce correctif.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-139">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>

 

### <span data-ttu-id="f0bf1-140">Configuration d’une mise à jour de performance de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="f0bf1-140">Configuring a Group Policy Performance Update</span></span>

<span data-ttu-id="f0bf1-141">Par défaut, la stratégie de groupe est téléchargée sur un ordinateur à la fois.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-141">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="f0bf1-142">Cela entraîne des retards lorsque MED-V est joint au domaine.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-142">This causes delays while MED-V is being joined to the domain.</span></span> <span data-ttu-id="f0bf1-143">Pour améliorer les performances de la stratégie de groupe, définissez la valeur de clé de Registre suivante sur le registre:</span><span class="sxs-lookup"><span data-stu-id="f0bf1-143">To increase the performance of Group Policy, set the following registry key value to the registry:</span></span>

<span data-ttu-id="f0bf1-144">Sous-clé de Registre: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="f0bf1-144">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="f0bf1-145">Entrée: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="f0bf1-145">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="f0bf1-146">Type: DWORD</span><span class="sxs-lookup"><span data-stu-id="f0bf1-146">Type: DWORD</span></span>

<span data-ttu-id="f0bf1-147">Valeur : 1</span><span class="sxs-lookup"><span data-stu-id="f0bf1-147">Value: 1</span></span>

## <a href="" id="bkmk-installintegration"></a><span data-ttu-id="f0bf1-148">Installation des composants d’intégration</span><span class="sxs-lookup"><span data-stu-id="f0bf1-148">Installing Integration Components</span></span>


<span data-ttu-id="f0bf1-149">Windows Virtual PC inclut le package composants d’intégration.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-149">Windows Virtual PC includes the Integration Components package.</span></span> <span data-ttu-id="f0bf1-150">Cela fournit des fonctionnalités qui améliorent l’interaction entre l’environnement virtuel et l’ordinateur physique.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-150">This provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="f0bf1-151">Par exemple, le package composants d’intégration vous permet de déplacer votre souris entre l’hôte et les ordinateurs invités.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-151">For example, the Integration Components package lets your mouse move between the host and the guest computers.</span></span>

<span data-ttu-id="f0bf1-152">**Important**  MED-V nécessite l’installation du package composants d’intégration.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-152">**Important** MED-V requires the installation of the Integration Components package.</span></span>

 

<span data-ttu-id="f0bf1-153">Lorsque vous configurez l’image virtuelle pour qu’elle fonctionne avec MED-V, vous devez installer manuellement le package composants d’intégration sur le système d’exploitation invité pour pouvoir accéder aux fonctionnalités d’intégration disponibles.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-153">When you configure the virtual image to work with MED-V, you must manually install the Integration Components package on the guest operating system to make the integration features that are available.</span></span>

<span data-ttu-id="f0bf1-154">Pour plus d’informations sur l’installation et l’utilisation du package composants d’intégration, voir les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="f0bf1-154">For more information about how to install and use the Integration Components package, see the following:</span></span>

-   <span data-ttu-id="f0bf1-155">[Installer ou mettre à niveau le package des composants d’intégration](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .</span><span class="sxs-lookup"><span data-stu-id="f0bf1-155">[Install or Upgrade the Integration Components Package](https://go.microsoft.com/fwlink/?LinkId=195923) (https://go.microsoft.com/fwlink/?LinkId=195923).</span></span>

-   <span data-ttu-id="f0bf1-156">[À propos des fonctionnalités d’intégration](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .</span><span class="sxs-lookup"><span data-stu-id="f0bf1-156">[About Integration Features](https://go.microsoft.com/fwlink/?LinkId=195924) (https://go.microsoft.com/fwlink/?LinkId=195924).</span></span>

### <span data-ttu-id="f0bf1-157">Installation de la mise à jour RemoteApp</span><span class="sxs-lookup"><span data-stu-id="f0bf1-157">Installing RemoteApp Update</span></span>

<span data-ttu-id="f0bf1-158">Une fois que vous avez installé le package des composants d’intégration, vous êtes invité à installer la mise à jour suivante: «mise à jour pour Windows XP SP3 pour activer RemoteApp».</span><span class="sxs-lookup"><span data-stu-id="f0bf1-158">After you install the Integration Components package, you are prompted to install the following update: "Update for Windows XP SP3 to enable RemoteApp."</span></span> <span data-ttu-id="f0bf1-159">Il s’agit d’un composant requis pour MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-159">This is a required component for MED-V.</span></span>

<span data-ttu-id="f0bf1-160">**Important**  Si vous n’êtes pas invité à installer la mise à jour RemoteApp, vous devez la télécharger et l’installer manuellement.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-160">**Important** If you are not prompted to install the RemoteApp update, you must download and install it manually.</span></span> <span data-ttu-id="f0bf1-161">Pour plus d’informations et des instructions sur la façon de télécharger cette mise à jour, voir [mise à jour pour Windows XP SP3 pour activer](https://go.microsoft.com/fwlink/?LinkId=195925) le programme RemoteApp ( https://go.microsoft.com/fwlink/?LinkId=195925) .</span><span class="sxs-lookup"><span data-stu-id="f0bf1-161">For more information and instructions about how to download this update, see [Update for Windows XP SP3 to enable RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) (https://go.microsoft.com/fwlink/?LinkId=195925).</span></span>

 

### <span data-ttu-id="f0bf1-162">Activation de l’application Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="f0bf1-162">Enabling Remote Desktop</span></span>

<span data-ttu-id="f0bf1-163">Par défaut, la version bureau à distance est activée une fois que vous avez installé le package composants d’intégration.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-163">By default, Remote Desktop is enabled after you install the Integration Components package.</span></span> <span data-ttu-id="f0bf1-164">Pour que MED-V soit opérationnel, assurez-vous que l’option Bureau à distance est activée et ne Répartissez aucune stratégie de groupe qui la désactive.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-164">For MED-V to be operational, ensure that Remote Desktop is enabled, and do not distribute any Group Policy that disables it.</span></span>

<span data-ttu-id="f0bf1-165">Pour plus d’informations sur l’activation du Bureau à distance, voir [activer ou désactiver le Bureau à distance](https://go.microsoft.com/fwlink/?LinkId=201162) https://go.microsoft.com/fwlink/?LinkId=201162) .</span><span class="sxs-lookup"><span data-stu-id="f0bf1-165">For information about how to enable Remote Desktop, see [Enable or disable Remote Desktop](https://go.microsoft.com/fwlink/?LinkId=201162) (https://go.microsoft.com/fwlink/?LinkId=201162).</span></span>

## <span data-ttu-id="f0bf1-166">Personnalisation d’Internet Explorer à l’aide du kit d’administration d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f0bf1-166">Customizing Internet Explorer by Using the Internet Explorer Administration Kit</span></span>


<span data-ttu-id="f0bf1-167">Si vous le souhaitez, vous pouvez utiliser le kit d’administration d’Internet Explorer pour personnaliser Internet Explorer sur le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-167">If you want, you can use the Internet Explorer Administration Kit to customize Internet Explorer on the guest operating system.</span></span> <span data-ttu-id="f0bf1-168">Pour plus d’informations, reportez-vous au [Guide de déploiement et au kit d’administration d’Internet Explorer 6](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?LinkId=200007).</span><span class="sxs-lookup"><span data-stu-id="f0bf1-168">For more information, see the [Internet Explorer 6 Administration Kit and Deployment Guide](https://go.microsoft.com/fwlink/?LinkId=200007) (http:// go.microsoft.com/fwlink/?LinkId=200007).</span></span>

<span data-ttu-id="f0bf1-169">**Avertissement**  Prenez en compte les problèmes liés à la sécurité liés à la personnalisation d’Internet Explorer dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-169">**Warning** You should consider security concerns associated with customizing Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="f0bf1-170">Pour plus d’informations, consultez [meilleures pratiques en matière de sécurité pour les opérations MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f0bf1-170">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>

 

<span data-ttu-id="f0bf1-171">Après l’installation de votre disque dur virtuel avec un système d’exploitation invité à jour, vous pouvez installer des applications sur l’image.</span><span class="sxs-lookup"><span data-stu-id="f0bf1-171">After your virtual hard disk is installed with an up-to-date guest operating system, you can install applications on the image.</span></span>

## <span data-ttu-id="f0bf1-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0bf1-172">Related topics</span></span>


[<span data-ttu-id="f0bf1-173">Installation d'applications sur une image WindowsVirtualPC</span><span class="sxs-lookup"><span data-stu-id="f0bf1-173">Installing Applications on a Windows Virtual PC Image</span></span>](installing-applications-on-a-windows-virtual-pc-image.md)

[<span data-ttu-id="f0bf1-174">Configuration d'une image Windows Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="f0bf1-174">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 






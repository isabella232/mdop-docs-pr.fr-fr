---
title: Planification de la compatibilité du système d'exploitation avec les applications
description: Planification de la compatibilité du système d'exploitation avec les applications
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811172"
---
# <span data-ttu-id="71a82-103">Planification de la compatibilité du système d'exploitation avec les applications</span><span class="sxs-lookup"><span data-stu-id="71a82-103">Planning for Application Operating System Compatibility</span></span>


<span data-ttu-id="71a82-104">Cette rubrique vous aide à déterminer comment résoudre les problèmes de compatibilité du système d’exploitation de l’application et explique comment Microsoft Enterprise Desktop Virtualization (MED-V 2,0) fonctionne comme une solution pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="71a82-104">This topic helps determine how to resolve application operating system compatibility issues, and discusses how Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 works as a solution for your organization.</span></span>

<span data-ttu-id="71a82-105">Cette rubrique décrit les exigences métiers pour MED-V et compare le mode MED-V au mode Windows XP et la virtualisation des applications Microsoft (App-V):</span><span class="sxs-lookup"><span data-stu-id="71a82-105">This topic discusses the business requirements for MED-V and compares MED-V to Windows XP Mode and Microsoft Application Virtualization (App-V):</span></span>

-   [<span data-ttu-id="71a82-106">Exigences métiers pour MED-V</span><span class="sxs-lookup"><span data-stu-id="71a82-106">Business Requirements for MED-V</span></span>](#bkmk-whenmedv)

-   [<span data-ttu-id="71a82-107">Avantages du mode MED-V par rapport à Windows XP</span><span class="sxs-lookup"><span data-stu-id="71a82-107">Benefits of MED-V versus Windows XP Mode</span></span>](#bkmk-medvvsxp)

-   [<span data-ttu-id="71a82-108">Avantages de MED-V par rapport à l’application-V</span><span class="sxs-lookup"><span data-stu-id="71a82-108">Benefits of MED-V versus App-V</span></span>](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a><span data-ttu-id="71a82-109">Exigences métiers pour MED-V</span><span class="sxs-lookup"><span data-stu-id="71a82-109">Business Requirements for MED-V</span></span>


<span data-ttu-id="71a82-110">Lorsque le service informatique de votre entreprise détermine s’il est nécessaire de procéder à la mise à niveau vers Windows 7, vous devez veiller à ses applications métier et applications métier basées sur le Web pour vous assurer qu’elles peuvent être exécutées sur le nouveau système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="71a82-110">When your company’s IT department is determining whether to upgrade to Windows 7, it must pay attention to its line-of-business applications and web-based line-of-business applications to make certain that these can run on the new operating system.</span></span> <span data-ttu-id="71a82-111">Souvent, ces applications et URL ont été créées pour fonctionner en particulier avec une version plus ancienne de Windows ou d’Internet Explorer, et des problèmes peuvent se produire lorsque vous tentez de les utiliser dans le nouveau système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="71a82-111">Often, these applications and URLs were created to work specifically with an older version of Windows or Internet Explorer, and problems can occur when trying to use them in the new operating system.</span></span> <span data-ttu-id="71a82-112">Microsoft propose plusieurs méthodes différentes pour gérer les différents problèmes de compatibilité qui peuvent se produire lors de la mise à niveau, comme le kit de compatibilité des applications (ACT) et l’Assistant Compatibilité des programmes de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71a82-112">Microsoft offers many different methods for handling the various compatibility issues that can occur when you upgrade, such as the Application Compatibility Toolkit (ACT) and the Windows 7 Program Compatibility Assistant.</span></span> <span data-ttu-id="71a82-113">Même si toutes les applications ont été testées à des fins de compatibilité et de correction, il est possible que certaines applications ne fonctionnent pas correctement sur Windows 7 ou soient trop onéreuses pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="71a82-113">But even after all applications have been tested for compatibility and fixes have been determined, some applications still do not work correctly on Windows 7 or are too costly to resolve.</span></span>

<span data-ttu-id="71a82-114">À l’aide de MED-V, vous pouvez exécuter ces applications héritées par le biais d’un environnement Windows Virtual PC exécutant Windows XP.</span><span class="sxs-lookup"><span data-stu-id="71a82-114">By using MED-V, you can run these legacy applications through a Windows Virtual PC environment that is running Windows XP.</span></span> <span data-ttu-id="71a82-115">Étant donné que vous n’avez plus besoin de tester et de valider ces applications de problèmes sur le nouveau système d’exploitation avant de procéder à la mise à niveau, votre migration vers Windows 7 est beaucoup plus fluide et plus rapide.</span><span class="sxs-lookup"><span data-stu-id="71a82-115">Because you no longer have to test and validate these problem applications on the new operating system before upgrading, your migration to Windows 7 is much smoother and quicker.</span></span>

### <span data-ttu-id="71a82-116">Utilisation de la liste de vérification MED-V</span><span class="sxs-lookup"><span data-stu-id="71a82-116">Using MED-V Checklist</span></span>

<span data-ttu-id="71a82-117">Envisagez d’utiliser MED-V si l’un des scénarios suivants vous concernent:</span><span class="sxs-lookup"><span data-stu-id="71a82-117">Consider MED-V if any of the following scenarios apply to you:</span></span>

-   <span data-ttu-id="71a82-118">Vous êtes une grande organisation (par exemple, des utilisateurs 500, etc.), vous devez avoir un accord d’entreprise avec Microsoft et planifier la mise à niveau vers Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71a82-118">You are a large organization (for example, 500 users and more), have an Enterprise Agreement with Microsoft, and plan to upgrade to Windows 7.</span></span>

-   <span data-ttu-id="71a82-119">Vous avez testé vos applications métier et avez détecté certaines qui ne sont pas compatibles avec Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71a82-119">You have tested your line-of-business applications and have found some that are incompatible with Windows 7.</span></span>

-   <span data-ttu-id="71a82-120">Vous avez résolu les problèmes de compatibilité de certains de ces applications à l’aide d’une mise à niveau de l’application ou à l’aide d’un shim fourni par Microsoft tel que le kit de compatibilité des applications (ACT), mais les problèmes de compatibilité persistent pour certaines applications.</span><span class="sxs-lookup"><span data-stu-id="71a82-120">You have resolved the compatibility issues for some of these problem applications by upgrading the application or by using a Microsoft-provided shim, such as the Application Compatibility Toolkit (ACT), but compatibility issues remain for some applications.</span></span>

-   <span data-ttu-id="71a82-121">Vous avez considéré l’option App-V comme option de remise des applications incompatibles et vous avez conclu qu’après l’implémentation de App-V, vous avez encore des problèmes de compatibilité liés aux systèmes d’exploitation des applications.</span><span class="sxs-lookup"><span data-stu-id="71a82-121">You have considered App-V as an option for delivering the incompatible applications and have concluded that even after you implement App-V, you still have application operating system compatibility issues that you must address.</span></span>

-   <span data-ttu-id="71a82-122">Vous avez considéré le mode Windows XP comme une solution et déterminé qu’il ne s’agit pas d’une option efficace pour les raisons suivantes:</span><span class="sxs-lookup"><span data-stu-id="71a82-122">You have considered Windows XP Mode as a solution and have determined that it is not an efficient option because:</span></span>

    -   <span data-ttu-id="71a82-123">Vous voulez être en mesure de déployer des images virtuelles qui contiennent les applications de problèmes à tous les utilisateurs finaux en même temps, au lieu de les utiliser individuellement et de joindre automatiquement les images virtuelles au domaine.</span><span class="sxs-lookup"><span data-stu-id="71a82-123">You want to be able to deploy virtual images that contain the problem applications to all end users at the same time, instead of individually, and have the virtual images automatically joined to the domain.</span></span>

    -   <span data-ttu-id="71a82-124">Vous avez décidé qu’il est beaucoup plus rentable pour gérer ces applications héritées (fournies virtuellement) et de contrôler les paramètres du PC virtuel Windows à partir d’un emplacement centralisé plutôt que sur le Bureau de chaque utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="71a82-124">You have decided it is much more cost effective to manage these legacy applications (that are delivered virtually) and control the Windows Virtual PC settings from a centralized location instead of on each end user’s desktop.</span></span>

    -   <span data-ttu-id="71a82-125">Vous voulez être en mesure de mettre à jour et de prendre en charge les machines virtuelles en échelle au lieu de chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="71a82-125">You want to be able to update and support the virtual machines in scale instead of per desktop.</span></span>

    -   <span data-ttu-id="71a82-126">Vous souhaitez pouvoir rediriger les URL qui s’exécutent mieux sur une version antérieure d’Internet Explorer vers les machines virtuelles et gérer facilement la redirection d’URL ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="71a82-126">You want the ability to redirect URLs that run better on an older version of Internet Explorer to the virtual machines and to easily manage URL redirection later.</span></span>

-   <span data-ttu-id="71a82-127">Vous avez déterminé qu’il serait plus rentable et utile de procéder à la mise à niveau vers Windows 7 dès que possible et de décider de différer la résolution des problèmes de compatibilité restants jusqu’à une date ultérieure, sachant qu’une solution est disponible dans MED-V.</span><span class="sxs-lookup"><span data-stu-id="71a82-127">You have determined that it would be more cost effective and helpful to upgrade to Windows 7 as soon as possible and have decided to postpone resolving your remaining application compatibility issues until a later date, knowing that you have a solution available in MED-V.</span></span>

## <a href="" id="bkmk-medvvsxp"></a> <span data-ttu-id="71a82-128">Avantages du mode MED-V par rapport à Windows XP</span><span class="sxs-lookup"><span data-stu-id="71a82-128">Benefits of MED-V versus Windows XP Mode</span></span>


<span data-ttu-id="71a82-129">Le PC virtuel Windows pour Windows 7 vous permet d’exécuter plusieurs versions d’un système d’exploitation en même temps sur un seul appareil et est incluse dans Windows 7 Professionnel Edition ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="71a82-129">Windows Virtual PC for Windows 7 lets you run different versions of an operating system at the same time on a single device and is included in Windows 7 Professional Edition and higher.</span></span>

<span data-ttu-id="71a82-130">Le mode Windows XP exploite le PC virtuel Windows en fournissant une image Windows XP préconfigurée qui vous permet de créer un environnement Windows XP virtuel.</span><span class="sxs-lookup"><span data-stu-id="71a82-130">Windows XP Mode functionality takes advantage of Windows Virtual PC by providing a preconfigured Windows XP image that lets you create a virtual Windows XP environment.</span></span> <span data-ttu-id="71a82-131">Dans cet environnement virtuel, vous pouvez installer manuellement des applications qui ne sont pas compatibles avec Windows 7 et qui s’exécutent en toute transparence depuis votre bureau via un PC virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="71a82-131">In this virtual environment, you can manually install applications that are incompatible with Windows 7 and that run seamlessly from your desktop through Windows Virtual PC.</span></span>

**<span data-ttu-id="71a82-132">Le mode Windows XP vous permet d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="71a82-132">By using Windows XP Mode, you can do the following:</span></span>**

-   <span data-ttu-id="71a82-133">Exécutez des applications compatibles avec Windows XP à l’intérieur d’un ordinateur virtuel qui s’exécute sur un ordinateur virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="71a82-133">Run applications that are compatible with Windows XP inside a virtual machine that runs in Windows Virtual PC.</span></span>

-   <span data-ttu-id="71a82-134">Publiez ces applications sur le menu du programme ou du Bureau de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="71a82-134">Publish these applications to the host’s desktop or Program menu.</span></span>

<span data-ttu-id="71a82-135">Si vous voulez fournir ces machines virtuelles à une grande échelle dans le cadre d’une migration d’entreprise vers Windows 7, vous devez être en mesure de déployer rapidement les machines virtuelles, de les mettre en place et de les personnaliser efficacement, de contrôler leurs paramètres et de les prendre en charge facilement.</span><span class="sxs-lookup"><span data-stu-id="71a82-135">When you want to deliver these virtual machines on a large scale as part of an enterprise migration to Windows 7, you must be able to deploy the virtual machines quickly, provision, and customize them efficiently, control their settings, and support them easily.</span></span>

<span data-ttu-id="71a82-136">MED-V repose sur le mode Windows XP pour garantir la compatibilité des applications à l’échelle de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="71a82-136">MED-V builds upon Windows XP Mode to deliver enterprise-wide application compatibility.</span></span> <span data-ttu-id="71a82-137">Le mode Windows XP étant limité à la fourniture de fonctionnalités d’application virtuelles pour les particuliers et les petites entreprises, MED-V autorise les déploiements à grande échelle d’images Windows XP préconfigurées sur tout le réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="71a82-137">Whereas Windows XP mode is limited to providing virtual application functionality to individuals and small businesses, MED-V allows for large-scale deployments of preconfigured Windows XP images throughout your corporate network.</span></span> <span data-ttu-id="71a82-138">Il fournit une solution de gestion adaptée à l’entreprise pour la configuration, le déploiement et la maintenance de ces espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="71a82-138">It gives you an enterprise-ready management solution for the configuration, deployment, and maintenance of these virtual MED-V workspaces.</span></span> <span data-ttu-id="71a82-139">MED-V fournit également à enterpriseadministrators un ensemble de stratégies pour contrôler l’utilisation des images.</span><span class="sxs-lookup"><span data-stu-id="71a82-139">MED-V also gives enterpriseadministrators a set of policies to control image use.</span></span> <span data-ttu-id="71a82-140">Cela inclut les utilisateurs qui ont accès à des applications spécifiques au sein de ces images.</span><span class="sxs-lookup"><span data-stu-id="71a82-140">This includes which users will have access to which specific applications within these images.</span></span>

**<span data-ttu-id="71a82-141">L’utilisation de MED-V vous permet d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="71a82-141">By using MED-V, you can do the following:</span></span>**

-   <span data-ttu-id="71a82-142">Effectuez la mise à niveau vers votre nouveau système d’exploitation sans tester et résoudre chaque application ou URL incompatible.</span><span class="sxs-lookup"><span data-stu-id="71a82-142">Upgrade to your new operating system without having to test and resolve every incompatible application and URL.</span></span>

-   <span data-ttu-id="71a82-143">Déploiement d’images Windows XP virtuelles qui sont automatiquement jointes au domaine et personnalisées par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71a82-143">Deploy virtual Windows XP images that are automatically domain-joined and customized per user.</span></span>

-   <span data-ttu-id="71a82-144">Fournir des informations sur les applications et la redirection d’URL aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="71a82-144">Provision applications and URL redirection information to users.</span></span>

-   <span data-ttu-id="71a82-145">Contrôle des paramètres du PC virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="71a82-145">Control the Windows Virtual PC settings.</span></span>

-   <span data-ttu-id="71a82-146">Maintenir et prendre en charge les points de terminaison via le suivi et la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="71a82-146">Maintain and support endpoints through monitoring and troubleshooting.</span></span>

-   <span data-ttu-id="71a82-147">Assurez-vous que les ordinateurs invités sont corrigés, même en cas de suspension.</span><span class="sxs-lookup"><span data-stu-id="71a82-147">Ensure that guest computers are patched, even if in a suspended state.</span></span>

-   <span data-ttu-id="71a82-148">Automatiser la création de machines virtuelles par utilisateur et l’initialisation de Sysprep.</span><span class="sxs-lookup"><span data-stu-id="71a82-148">Automate per-user virtual machine creation and sysprep initialization.</span></span>

-   <span data-ttu-id="71a82-149">Diagnostiquer facilement les problèmes sur les ordinateurs hôte et invités.</span><span class="sxs-lookup"><span data-stu-id="71a82-149">Easily diagnose issues on the host and guest computers.</span></span>

-   <span data-ttu-id="71a82-150">Gérez en toute transparence des ordinateurs invités connectés via le mode NAT de l’ordinateur virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="71a82-150">Seamlessly manage guest computers that are connected through Windows Virtual PC NAT mode.</span></span>

## <a href="" id="bkmk-medvvsappv"></a><span data-ttu-id="71a82-151">Avantages de MED-V par rapport à l’application-V</span><span class="sxs-lookup"><span data-stu-id="71a82-151">Benefits of MED-V versus App-V</span></span>


<span data-ttu-id="71a82-152">MED-V et App-V sont deux technologies très différentes qui peuvent facilement fonctionner ensemble pour résoudre les problèmes de compatibilité de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="71a82-152">MED-V and App-V are two very different technologies that can easily work together to solve your application operating system compatibility issues.</span></span> <span data-ttu-id="71a82-153">En utilisant App-V, vous créez un package individualisé pour chaque application, chacun d’eux étant alors maintenu indépendamment des autres.</span><span class="sxs-lookup"><span data-stu-id="71a82-153">By using App-V, you create an individualized package for each application, each of which is then kept separate from the others.</span></span> <span data-ttu-id="71a82-154">Chaque application virtuelle peut ensuite être envoyée immédiatement à l’utilisateur final, ce qui est très utile pour une stratégie de déploiement de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71a82-154">Each virtual application can then be immediately delivered to the end user, which is very useful for a Windows 7 deployment strategy.</span></span>

<span data-ttu-id="71a82-155">MED-V ne gère pas les applications individuellement.</span><span class="sxs-lookup"><span data-stu-id="71a82-155">MED-V does not handle applications individually.</span></span> <span data-ttu-id="71a82-156">Au lieu de cela, il crée une instance supplémentaire de Windows XP sur le même ordinateur de bureau exécutant Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71a82-156">Instead, it creates an additional instance of Windows XP on the same desktop that is running Windows 7.</span></span> <span data-ttu-id="71a82-157">Vous pouvez installer autant d’applications que nécessaire dans cette image virtuelle et gérer l’image comme vous le feriez pour n’importe quel autre bureau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="71a82-157">You can install as many applications as necessary into this virtual image and manage the image just as you would any other desktop in your organization.</span></span>

<span data-ttu-id="71a82-158">De plus, vous pouvez utiliser MED-V avec App-V de façon à ce que les applications virtuelles exécutées par le biais d’App-v soient installées, publiées et gérées à l’aide de MED-V.</span><span class="sxs-lookup"><span data-stu-id="71a82-158">In addition, you can use MED-V together with App-V so that virtual applications that are sequenced through App-V are installed, published, and managed by using MED-V.</span></span>

## <span data-ttu-id="71a82-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71a82-159">Related topics</span></span>


[<span data-ttu-id="71a82-160">Définir et planifier votre déploiement MED-V</span><span class="sxs-lookup"><span data-stu-id="71a82-160">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

 

 






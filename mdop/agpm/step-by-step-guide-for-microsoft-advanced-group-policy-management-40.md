---
title: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft4.0
description: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft4.0
author: dansimp
ms.assetid: dc6f9b16-b1d4-48f3-88bb-f29301f0131c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 819d536451095d23080115799016aa0ac5242dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808210"
---
# <span data-ttu-id="ff719-103">Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft4.0</span><span class="sxs-lookup"><span data-stu-id="ff719-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="ff719-104">Ce guide pas à pas décrit les techniques avancées de gestion de la stratégie de groupe qui utilisent la console de gestion des stratégies de groupe (GPMC) et Microsoft Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="ff719-104">This step-by-step guide demonstrates advanced techniques for Group Policy management that use the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="ff719-105">AGPM augmente les capacités de la console de gestion des stratégies de GPMC et fournit les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="ff719-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="ff719-106">Rôles standard pour la délégation d’autorisations pour gérer les objets de stratégie de groupe à plusieurs administrateurs de stratégie de groupe, en plus de la possibilité de déléguer l’accès aux objets de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ff719-106">Standard roles for delegating permissions to manage Group Policy Objects (GPOs) to multiple Group Policy administrators, in addition to the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="ff719-107">Archive permettant aux administrateurs de stratégie de groupe de créer et de modifier des objets de stratégie de groupe hors ligne avant leur déploiement dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ff719-107">An archive to enable Group Policy administrators to create and modify GPOs offline before the GPOs are deployed into a production environment.</span></span>

-   <span data-ttu-id="ff719-108">La possibilité de revenir à une version antérieure d’un objet de stratégie de groupe dans l’archive et de limiter le nombre de versions stockées dans l’archive;</span><span class="sxs-lookup"><span data-stu-id="ff719-108">The ability to roll back to any earlier version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="ff719-109">Les fonctionnalités d’archivage et d’extraction des objets de stratégie de groupe vous permettent de vous assurer que les administrateurs de stratégie de groupe n’écrasent pas involontairement leurs tâches.</span><span class="sxs-lookup"><span data-stu-id="ff719-109">Check-in and check-out capability for GPOs to make sure that Group Policy administrators do not unintentionally overwrite each other's work.</span></span>

-   <span data-ttu-id="ff719-110">La possibilité de rechercher des objets de stratégie de groupe avec des attributs spécifiques et de filtrer la liste des objets de stratégie de groupe affichés.</span><span class="sxs-lookup"><span data-stu-id="ff719-110">The ability to search for GPOs with specific attributes and to filter the list of GPOs displayed.</span></span>

## <span data-ttu-id="ff719-111">Vue d’ensemble du scénario AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-111">AGPM scenario overview</span></span>


<span data-ttu-id="ff719-112">Pour ce scénario, vous allez utiliser un compte d’utilisateur distinct pour chaque rôle dans AGPM et montrer comment la stratégie de groupe peut être gérée dans un environnement doté de plusieurs administrateurs de stratégie de groupe disposant de différents niveaux d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="ff719-112">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment that has multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="ff719-113">Plus précisément, vous devez effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="ff719-113">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="ff719-114">À l’aide d’un compte membre du groupe administrateurs de domaine, installez le serveur AGPM et attribuez le rôle d’administrateur AGPM à un compte ou à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-114">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="ff719-115">À l’aide des comptes auxquels vous allez attribuer des rôles AGPM, installez le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-115">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="ff719-116">À l’aide d’un compte ayant le rôle d’administrateur AGPM, configurez l’accès AGPM et de délégué aux objets de stratégie de groupe en attribuant des rôles à d’autres comptes.</span><span class="sxs-lookup"><span data-stu-id="ff719-116">Using an account that has the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="ff719-117">À partir d’un compte ayant le rôle d’éditeur, demandez qu’un nouvel objet de stratégie de groupe soit créé et approuvé par le biais d’un compte doté du rôle Approbateur.</span><span class="sxs-lookup"><span data-stu-id="ff719-117">From an account that has the Editor role, request that a new GPO be created that you then approve by using an account that has the Approver role.</span></span> <span data-ttu-id="ff719-118">Utiliser le compte de l’éditeur pour extraire l’objet de stratégie de groupe de l’archive, modifier l’objet de stratégie de groupe, archiver l’objet de stratégie de groupe dans l’archive, puis demander le déploiement.</span><span class="sxs-lookup"><span data-stu-id="ff719-118">Use the Editor account to check the GPO out of the archive, edit the GPO, check the GPO into the archive, and then request deployment.</span></span>

-   <span data-ttu-id="ff719-119">À l’aide d’un compte doté du rôle Approbateur, passez en revue l’objet de stratégie de groupe et déployez-le dans votre environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ff719-119">Using an account that has the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="ff719-120">À l’aide d’un compte doté du rôle d’éditeur, créez un modèle d’objet de stratégie de groupe et utilisez-le comme point de départ pour créer un nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-120">Using an account that has the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="ff719-121">À l’aide d’un compte doté du rôle Approbateur, supprimez et restaurez un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-121">Using an account that has the Approver role, delete and restore a GPO.</span></span>

![processus de développement d’objets de stratégie de groupe](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="ff719-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff719-123">Requirements</span></span>


<span data-ttu-id="ff719-124">Les ordinateurs sur lesquels vous souhaitez installer AGPM doivent respecter les exigences suivantes et vous devez créer des comptes à utiliser dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="ff719-124">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="ff719-125">**Remarques**  Si AGPM 2,5 est installé et que vous effectuez une mise à niveau de Windows Server® 2003 vers Windows Server2008R2 ou Windows Server 2008, ou si vous effectuez une mise à niveau à partir d’Vista sans Service Pack d’Vista et de® avec Service Pack1 (SP1), vous devez mettre à niveau le système d’exploitation avant de procéder à la mise à niveau vers AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="ff719-125">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008R2 or Windows Server2008, or are upgrading from WindowsVista with no service packs installed to Windows7 or WindowsVista® with Service Pack1 (SP1), you must upgrade the operating system before you can upgrade to AGPM4.0.</span></span>

<span data-ttu-id="ff719-126">Si AGPM 3,0 est installé, vous ne devez pas mettre à niveau le système d’exploitation avant de procéder à la mise à niveau vers AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="ff719-126">If you have AGPM 3.0 installed, you do not have to upgrade the operating system before you upgrade to AGPM 4.0</span></span>

 

<span data-ttu-id="ff719-127">Dans un environnement mixte incluant des systèmes d’exploitation plus récents et plus anciens, il existe certaines limitations aux fonctionnalités, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ff719-127">In a mixed environment that includes both newer and older operating systems, there are some limitations to functionality, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff719-128">Système d’exploitation sur lequel un serveur AGPM 4,0 est exécuté</span><span class="sxs-lookup"><span data-stu-id="ff719-128">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="ff719-129">Système d’exploitation sur lequel le client AGPM 4,0 s’exécute</span><span class="sxs-lookup"><span data-stu-id="ff719-129">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="ff719-130">État de la prise en charge d’AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="ff719-130">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff719-131">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="ff719-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff719-132">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="ff719-132">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff719-133">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff719-133">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff719-134">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="ff719-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff719-135">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="ff719-135">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff719-136">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2008R2 ou la touche Windows</span><span class="sxs-lookup"><span data-stu-id="ff719-136">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff719-137">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="ff719-137">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff719-138">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="ff719-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff719-139">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff719-139">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff719-140">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="ff719-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff719-141">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="ff719-141">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ff719-142">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une icône</span><span class="sxs-lookup"><span data-stu-id="ff719-142">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ff719-143">Configuration requise pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-143">AGPM Server requirements</span></span>

<span data-ttu-id="ff719-144">Pour AGPM Server 4.0, vous avez besoin de Windows Server2008R2, Windows Server 2008, de la fonction de GPMC et de la console de gestion des logiciels distants (RSAT) ou Windows Vista avec SP1 et de la console GPMC de RSAT.</span><span class="sxs-lookup"><span data-stu-id="ff719-144">AGPM Server4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from Remote Server Administration Tools (RSAT), or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="ff719-145">Les versions 32 bits et 64 bits sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ff719-145">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="ff719-146">Avant d’installer le serveur AGPM, vous devez être membre du groupe administrateurs de domaine et les fonctionnalités Windows suivantes doivent être présentes sauf indication contraire:</span><span class="sxs-lookup"><span data-stu-id="ff719-146">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="ff719-147">GESTION</span><span class="sxs-lookup"><span data-stu-id="ff719-147">GPMC</span></span>

    -   <span data-ttu-id="ff719-148">Windows Server2008R2 ou Windows Server 2008: si le GPMC n’est pas présent, il est automatiquement installé par AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-148">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="ff719-149">-Vous: vous devez installer la console de gestion des stratégies de l’installation à partir du RSAT avant d’installer AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-149">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="ff719-150">Pour plus d’informations, reportez-vous à la rubrique [Outils d’administration de serveur distant pour Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="ff719-150">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="ff719-151">Windows Vista avec Service Pack 1: vous devez installer la console de gestion des stratégies de l’installation à partir de RSAT avant d’installer AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-151">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="ff719-152">Pour plus d’informations, reportez-vous à la rubrique [Outils d’administration de serveur distant pour Windows Vista avec Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="ff719-152">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="ff719-153">.NET Framework 3,5 ou versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="ff719-153">The .NET Framework 3.5 or later versions</span></span>

    -   <span data-ttu-id="ff719-154">Windows Server2008R2 ou une version d’Outlook: si .NET Framework 3,5 ou version ultérieure n’est pas présent, le .NET Framework 3,5 est automatiquement installé par AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-154">Windows Server2008R2 or Windows7: If the .NET Framework 3.5 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="ff719-155">Windows Server 2008 ou Windows Vista avec Service Pack 1: vous devez installer .NET Framework 3,5 ou une version ultérieure avant d’installer AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-155">Windows Server2008 or Windows Vista with SP1: You must install the .NET Framework 3.5 or a later version before you install AGPM.</span></span>

<span data-ttu-id="ff719-156">Les fonctionnalités Windows suivantes sont requises par le serveur AGPM et sont installées automatiquement s’ils ne sont pas présents:</span><span class="sxs-lookup"><span data-stu-id="ff719-156">The following Windows features are required by AGPM Server and will be automatically installed if they are not present:</span></span>

-   <span data-ttu-id="ff719-157">Activation WCF; Activation non HTTP</span><span class="sxs-lookup"><span data-stu-id="ff719-157">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="ff719-158">Service d'activation des processus Windows</span><span class="sxs-lookup"><span data-stu-id="ff719-158">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="ff719-159">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="ff719-159">Process Model</span></span>

    -   <span data-ttu-id="ff719-160">Environnement .NET</span><span class="sxs-lookup"><span data-stu-id="ff719-160">The .NET Environment</span></span>

    -   <span data-ttu-id="ff719-161">API de configuration</span><span class="sxs-lookup"><span data-stu-id="ff719-161">Configuration APIs</span></span>

### <span data-ttu-id="ff719-162">Configuration requise pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-162">AGPM Client requirements</span></span>

<span data-ttu-id="ff719-163">Le client d’AGPM est requis pour Windows Server2008R2, Windows Server 2008, la version 4 et la console GPMC de RSAT ou Windows Vista avec SP1 et la console de gestion des stratégies de poste de poste.</span><span class="sxs-lookup"><span data-stu-id="ff719-163">AGPM Client4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from RSAT, or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="ff719-164">Les versions 32 bits et 64 bits sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ff719-164">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="ff719-165">Le client AGPM peut être installé sur un ordinateur exécutant AGPM Server.</span><span class="sxs-lookup"><span data-stu-id="ff719-165">AGPM Client can be installed on a computer that is running AGPM Server.</span></span>

<span data-ttu-id="ff719-166">Les fonctionnalités Windows suivantes sont requises par le client AGPM et, sauf indication contraire, si elles ne sont pas installées, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="ff719-166">The following Windows features are required by AGPM Client and unless otherwise noted are automatically installed if they are not present:</span></span>

-   <span data-ttu-id="ff719-167">GESTION</span><span class="sxs-lookup"><span data-stu-id="ff719-167">GPMC</span></span>

    -   <span data-ttu-id="ff719-168">Windows Server2008R2 ou Windows Server 2008: si le GPMC n’est pas présent, il est automatiquement installé par AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-168">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="ff719-169">-Vous: vous devez installer la console de gestion des stratégies de l’installation à partir du RSAT avant d’installer AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-169">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="ff719-170">Pour plus d’informations, reportez-vous à la rubrique [Outils d’administration de serveur distant pour Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="ff719-170">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="ff719-171">Windows Vista avec Service Pack 1: vous devez installer la console de gestion des stratégies de l’installation à partir de RSAT avant d’installer AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-171">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="ff719-172">Pour plus d’informations, reportez-vous à la rubrique [Outils d’administration de serveur distant pour Windows Vista avec Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="ff719-172">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="ff719-173">.NET Framework 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ff719-173">The .NET Framework 3.0 or later version</span></span>

    -   <span data-ttu-id="ff719-174">Windows Server2008R2 ou une version d’Outlook: si .NET Framework 3,0 ou version ultérieure n’est pas présent, le .NET Framework 3,5 est automatiquement installé par AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-174">Windows Server2008R2 or Windows7: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="ff719-175">Windows Server 2008 ou Windows Vista avec Service Pack 1: si .NET Framework 3,0 ou version ultérieure n’est pas présent, le .NET Framework 3,0 est automatiquement installé par AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-175">Windows Server2008 or Windows Vista with SP1: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.0 is automatically installed by AGPM.</span></span>

### <span data-ttu-id="ff719-176">Exigences de scénarios</span><span class="sxs-lookup"><span data-stu-id="ff719-176">Scenario requirements</span></span>

<span data-ttu-id="ff719-177">Avant de commencer ce scénario, vous devez créer quatre comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ff719-177">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="ff719-178">Pendant le scénario, vous devez attribuer l’un des rôles AGPM suivants à chacun de ces comptes: Administrateur AGPM (contrôle total), approbateur, éditeur et relecteur.</span><span class="sxs-lookup"><span data-stu-id="ff719-178">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="ff719-179">Ces comptes doivent être en mesure d’envoyer et de recevoir des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="ff719-179">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="ff719-180">Attribution d’autorisations d’accès aux **objets liés** aux comptes disposant des rôles d’administrateur AGPM, approbateur et (facultatif).</span><span class="sxs-lookup"><span data-stu-id="ff719-180">Assign **Link GPOs** permission to the accounts that have the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="ff719-181">**Remarques** 
 L’autorisation **lier les objets de stratégie de groupe** est affectée par défaut aux membres des administrateurs de domaine et des administrateurs d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ff719-181">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="ff719-182">Pour affecter des autorisations d’accès de l’utilisateur à des utilisateurs ou des groupes supplémentaires (par exemple, des comptes ayant le rôle d’administrateur ou d’approbation AGPM), cliquez sur le nœud du domaine, cliquez sur l’onglet **délégation** , sélectionnez **lier les objets de stratégie de groupe**, cliquez sur **Ajouter**, puis sélectionnez les utilisateurs ou groupes auxquels vous voulez accorder **l’autorisation.**</span><span class="sxs-lookup"><span data-stu-id="ff719-182">To assign **Link GPOs** permission to additional users or groups (such as accounts that have the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which you want to assign the permission.</span></span>

 

## <span data-ttu-id="ff719-183">Procédures d’installation et de configuration d’AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-183">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="ff719-184">Pour installer et configurer AGPM, vous devez procéder comme suit.</span><span class="sxs-lookup"><span data-stu-id="ff719-184">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="ff719-185">Étape 1: installer le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-185">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="ff719-186">Étape 2: installer le client AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-186">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="ff719-187">Étape 3: configurer une connexion de serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-187">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="ff719-188">Étape 4: configurer les notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="ff719-188">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="ff719-189">Étape 5: accès délégué</span><span class="sxs-lookup"><span data-stu-id="ff719-189">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="ff719-190">Étape 1: installer le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-190">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="ff719-191">Dans cette étape, vous installez le serveur AGPM sur le serveur membre ou le contrôleur de domaine qui exécute le service AGPM et vous configurez l’archive.</span><span class="sxs-lookup"><span data-stu-id="ff719-191">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="ff719-192">Toutes les opérations AGPM sont gérées par le biais de ce service Windows et sont exécutées avec les informations d’identification du service.</span><span class="sxs-lookup"><span data-stu-id="ff719-192">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="ff719-193">L’archive gérée par un serveur AGPM peut être hébergée sur ce serveur ou sur un autre serveur dans la même forêt.</span><span class="sxs-lookup"><span data-stu-id="ff719-193">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="ff719-194">Pour installer le serveur AGPM sur l’ordinateur qui hébergera le service AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-194">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="ff719-195">Ouvrez une session avec un compte membre du groupe administrateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="ff719-195">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="ff719-196">Démarrez le CD-ROM Microsoft Desktop Optimization Pack et suivez les instructions qui s’affichent à l’écran pour sélectionner **Advanced Group Management Policy-Server**.</span><span class="sxs-lookup"><span data-stu-id="ff719-196">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="ff719-197">Dans la boîte de dialogue **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-197">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="ff719-198">Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-198">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

5.  <span data-ttu-id="ff719-199">Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-199">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="ff719-200">L’ordinateur sur lequel le serveur AGPM est installé doit héberger le service AGPM et gérer l’archive.</span><span class="sxs-lookup"><span data-stu-id="ff719-200">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="ff719-201">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-201">Click **Next**.</span></span>

6.  <span data-ttu-id="ff719-202">Dans la boîte de dialogue **path Archive** , sélectionnez un emplacement pour l’Archive par rapport au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-202">In the **Archive Path** dialog box, select a location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="ff719-203">Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou ailleurs.</span><span class="sxs-lookup"><span data-stu-id="ff719-203">The archive path can point to a folder on the AGPM Server or elsewhere.</span></span> <span data-ttu-id="ff719-204">Toutefois, vous devez sélectionner un emplacement disposant d’un espace suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-204">However, you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="ff719-205">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-205">Click **Next**.</span></span>

7.  <span data-ttu-id="ff719-206">Dans la boîte de dialogue **compte de service AGPM** , sélectionnez un compte de service sous lequel le service AGPM sera exécuté, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-206">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

    <span data-ttu-id="ff719-207">Ce compte doit être membre du groupe Domain Admins ou, pour une configuration de privilèges minimum, les groupes suivants dans chaque domaine géré par le serveur AGPM:</span><span class="sxs-lookup"><span data-stu-id="ff719-207">This account must be a member of the either the Domain Admins group or, for a least-privilege configuration, the following groups in each domain managed by the AGPM Server:</span></span>

    -   <span data-ttu-id="ff719-208">Propriétaires de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-208">Group Policy Creator Owners</span></span>

    -   <span data-ttu-id="ff719-209">Opérateurs de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="ff719-209">Backup Operators</span></span>

    <span data-ttu-id="ff719-210">Par ailleurs, ce compte nécessite une autorisation contrôle total pour les dossiers suivants:</span><span class="sxs-lookup"><span data-stu-id="ff719-210">Additionally, this account requires Full Control permission for the following folders:</span></span>

    -   <span data-ttu-id="ff719-211">Le dossier d’archive AGPM pour lequel cette autorisation est accordée automatiquement lors de l’installation d’AGPM Server s’il est installé sur un disque local.</span><span class="sxs-lookup"><span data-stu-id="ff719-211">The AGPM archive folder, for which this permission is automatically granted during the installation of AGPM Server if it is installed on a local drive.</span></span>

    -   <span data-ttu-id="ff719-212">Le dossier temporaire du système local, généralement%windir%\\temp.</span><span class="sxs-lookup"><span data-stu-id="ff719-212">The local system temp folder, typically %windir%\\temp.</span></span>

8.  <span data-ttu-id="ff719-213">Dans la boîte de dialogue **Archiver le propriétaire** , sélectionnez un compte ou un groupe auquel vous attribuez le rôle d’administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="ff719-213">In the **Archive Owner** dialog box, select an account or group to which you assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="ff719-214">Les administrateurs d’AGPM peuvent attribuer des rôles et autorisations d’AGPM aux autres administrateurs de stratégie de groupe, afin que vous puissiez affecter le rôle d’administrateur AGPM aux administrateurs de stratégie de groupe supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ff719-214">AGPM Administrators can assign AGPM roles and permissions to other Group Policy administrators, so that later you can assign the role of AGPM Administrator to additional Group Policy administrators.</span></span> <span data-ttu-id="ff719-215">Pour ce scénario, sélectionnez le compte que vous voulez faire dans le rôle administrateur d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-215">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="ff719-216">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-216">Click **Next**.</span></span>

9.  <span data-ttu-id="ff719-217">Dans la boîte de dialogue **configuration du port** , tapez un port sur lequel le service AGPM doit écouter.</span><span class="sxs-lookup"><span data-stu-id="ff719-217">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="ff719-218">Ne désactivez pas la case à cocher **Ajouter une exception de port à un pare-feu** sauf si vous configurez manuellement les exceptions de port ou utilisez des règles pour configurer les exceptions de port</span><span class="sxs-lookup"><span data-stu-id="ff719-218">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="ff719-219">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-219">Click **Next**.</span></span>

10. <span data-ttu-id="ff719-220">Dans la boîte de dialogue **langues** , sélectionnez une ou plusieurs langues d’affichage à installer pour le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-220">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="ff719-221">Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.</span><span class="sxs-lookup"><span data-stu-id="ff719-221">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="ff719-222">**Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ff719-222">**Caution** Do not change settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="ff719-223">Cela peut empêcher le démarrage du service AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-223">Doing this can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="ff719-224">Pour plus d’informations sur la modification des paramètres du service, voir aide pour la gestion avancée des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-224">For information about how to change settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="ff719-225">Étape 2: installer le client AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-225">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="ff719-226">Chaque administrateur de stratégie de groupe (qui crée, modifie, déploie, révise ou supprime des objets de stratégie de groupe) doit disposer d’un client AGPM sur les ordinateurs qu’il utilise pour gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-226">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="ff719-227">Le nœud de contrôle de modification, qui vous permet d’effectuer de nombreuses tâches de gestion d’objets de stratégie de groupe, s’affiche dans la console de gestion des stratégies de groupe uniquement si vous installez le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-227">The Change Control node, which you use to perform many of the GPO management tasks, appears in the Group Policy Management Console only if you install the AGPM Client.</span></span> <span data-ttu-id="ff719-228">Pour ce scénario, vous installez le client AGPM sur au moins un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ff719-228">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="ff719-229">Vous n’avez pas besoin d’installer le client AGPM sur les ordinateurs des utilisateurs finaux qui n’effectuent pas d’administration de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-229">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="ff719-230">Pour installer le client AGPM sur l’ordinateur d’un administrateur de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-230">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="ff719-231">Démarrez le CD-ROM Microsoft Desktop Optimization Pack et suivez les instructions à l’écran pour sélectionner **Advanced Group Management Policy-client**.</span><span class="sxs-lookup"><span data-stu-id="ff719-231">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="ff719-232">Dans la boîte de dialogue **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-232">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="ff719-233">Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-233">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

4.  <span data-ttu-id="ff719-234">Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-234">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="ff719-235">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-235">Click **Next**.</span></span>

5.  <span data-ttu-id="ff719-236">Dans la boîte de dialogue **serveur AGPM** , tapez le nom DNS ou l’adresse IP du serveur AGPM et le port auquel vous voulez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ff719-236">In the **AGPM Server** dialog box, type the DNS name or IP address for the AGPM Server and the port to which you want to connect.</span></span> <span data-ttu-id="ff719-237">Le port par défaut du service AGPM est 4600.</span><span class="sxs-lookup"><span data-stu-id="ff719-237">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="ff719-238">Ne désactivez pas la case à cocher **autoriser Microsoft Management Console via le pare-feu** sauf si vous configurez manuellement les exceptions de port ou utilisez des règles pour configurer les exceptions de port.</span><span class="sxs-lookup"><span data-stu-id="ff719-238">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="ff719-239">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-239">Click **Next**.</span></span>

6.  <span data-ttu-id="ff719-240">Dans la boîte de dialogue **langues** , sélectionnez une ou plusieurs langues d’affichage à installer pour le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-240">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="ff719-241">Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.</span><span class="sxs-lookup"><span data-stu-id="ff719-241">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="ff719-242">Étape 3: configurer une connexion de serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-242">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="ff719-243">AGPM stocke toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO), c’est-à-dire, chaque GPO pour lequel AGPM fournit le contrôle des modifications, dans une archive centrale.</span><span class="sxs-lookup"><span data-stu-id="ff719-243">AGPM stores all versions of each controlled Group Policy Object (GPO), that is, each GPO for which AGPM provides change control, in a central archive.</span></span> <span data-ttu-id="ff719-244">Cela permet aux administrateurs de stratégie de groupe d’afficher et de modifier les objets de stratégie de groupe hors connexion sans affecter immédiatement la version déployée de chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="ff719-244">This lets Group Policy administrators view and change GPOs offline without immediately affecting the deployed version of each GPO.</span></span>

<span data-ttu-id="ff719-245">Dans cette étape, vous configurez une connexion de serveur AGPM et assurez-vous que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-245">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="ff719-246">(Pour plus d’informations sur la configuration de plusieurs serveurs AGPM, voir aide pour la gestion avancée des stratégies de groupe.)</span><span class="sxs-lookup"><span data-stu-id="ff719-246">(For information about how to configure multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="ff719-247">Pour configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-247">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="ff719-248">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide du compte d’utilisateur que vous avez sélectionné comme propriétaire d’archive.</span><span class="sxs-lookup"><span data-stu-id="ff719-248">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="ff719-249">Cet utilisateur a le rôle d’administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="ff719-249">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="ff719-250">Cliquez sur **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur gestion de la **stratégie de groupe** pour ouvrir la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="ff719-250">Click **Start**, point to **Administrative Tools**, and then click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="ff719-251">Modification d’un objet de stratégie de groupe qui est appliqué à tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-251">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="ff719-252">Dans la fenêtre de l' **éditeur de gestion des stratégies de groupe** , double-cliquez sur **Configuration utilisateur**, **stratégies**, **modèles d’administration**, **composants Windows**et **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="ff719-252">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="ff719-253">Dans le volet Détails, double-cliquez sur **AGPM: spécifiez le serveur AGPM par défaut (tous les domaines)**.</span><span class="sxs-lookup"><span data-stu-id="ff719-253">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="ff719-254">Dans la fenêtre **Propriétés** , sélectionnez **activé** , puis entrez le nom DNS ou l’adresse IP et le port (par exemple, **Server.contoso.com:4600**) du serveur qui héberge l’archive.</span><span class="sxs-lookup"><span data-stu-id="ff719-254">In the **Properties** window, select **Enabled** and type the DNS name or IP address and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="ff719-255">Par défaut, le service AGPM utilise le port 4600.</span><span class="sxs-lookup"><span data-stu-id="ff719-255">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="ff719-256">Cliquez sur **OK**, puis fermez la fenêtre **éditeur de gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="ff719-256">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="ff719-257">Lorsque la stratégie de groupe est mise à jour, la connexion au serveur AGPM est configurée pour chaque administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-257">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="ff719-258">Étape 4: configurer les notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="ff719-258">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="ff719-259">En tant qu’administrateur AGPM (contrôle total), vous désignez les adresses de courrier des approbateurs et des administrateurs AGPM auxquels un message électronique contenant une demande est envoyé lorsqu’un éditeur tente de créer, de déployer ou de supprimer un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-259">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message that contains a request is sent when an Editor tries to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="ff719-260">Vous déterminez également l’alias à partir duquel ces messages sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="ff719-260">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="ff719-261">Pour configurer les notifications par courrier électronique pour AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-261">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="ff719-262">Dans l' **éditeur de gestion des stratégies de groupe** , accéder au dossier de contrôle de **modification**</span><span class="sxs-lookup"><span data-stu-id="ff719-262">In **Group Policy Management Editor** , navigate to the **Change Control** folder</span></span> 

2.  <span data-ttu-id="ff719-263">Dans le volet Détails, cliquez sur l’onglet **délégation de domaine** .</span><span class="sxs-lookup"><span data-stu-id="ff719-263">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="ff719-264">Dans le champ **à partir de l’adresse de messagerie** , entrez l’adresse de messagerie d’AGPM à partir de laquelle les notifications doivent être envoyées.</span><span class="sxs-lookup"><span data-stu-id="ff719-264">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="ff719-265">Dans le champ **adresse de messagerie** , entrez l’adresse de messagerie du compte d’utilisateur auquel vous souhaitez attribuer le rôle d’approbateur.</span><span class="sxs-lookup"><span data-stu-id="ff719-265">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="ff719-266">Dans le champ **serveur SMTP** , tapez un serveur de messagerie SMTP valide.</span><span class="sxs-lookup"><span data-stu-id="ff719-266">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="ff719-267">Dans les champs **nom d’utilisateur** et **mot de passe** , tapez les informations d’identification d’un utilisateur qui a accès au service SMTP.</span><span class="sxs-lookup"><span data-stu-id="ff719-267">In the **User name** and **Password** fields, type the credentials of a user who has access to the SMTP service.</span></span> <span data-ttu-id="ff719-268">Cliquez sur **Apply** (Appliquer).</span><span class="sxs-lookup"><span data-stu-id="ff719-268">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="ff719-269">Étape 5: accès délégué</span><span class="sxs-lookup"><span data-stu-id="ff719-269">Step 5: Delegate access</span></span>

<span data-ttu-id="ff719-270">En tant qu’administrateur AGPM (contrôle total), vous déléguez l’accès au niveau du domaine aux objets de stratégie de groupe, en attribuant des rôles au compte de chaque administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-270">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="ff719-271">**Remarques**  Vous pouvez également déléguer l’accès au niveau de l’objet GPO plutôt qu’au niveau du domaine.</span><span class="sxs-lookup"><span data-stu-id="ff719-271">**Note** You can also delegate access at the GPO level instead of the domain level.</span></span> <span data-ttu-id="ff719-272">Pour plus d’informations, voir aide pour la gestion avancée des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-272">For more information, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="ff719-273">**Important**  Vous devez limiter l’appartenance au groupe de propriétaires de la stratégie de groupe afin qu’elle ne puisse pas être utilisée pour contourner la gestion d’AGPM d’Access aux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-273">**Important** You should restrict membership in the Group Policy Creator Owners group so that it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="ff719-274">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="ff719-274">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="ff719-275">Pour déléguer l’accès à tous les objets de stratégie de groupe dans un domaine</span><span class="sxs-lookup"><span data-stu-id="ff719-275">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="ff719-276">Dans l’onglet **délégation de domaine** , cliquez sur le bouton **Ajouter** , sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe comme approbateur, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-276">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="ff719-277">Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez le rôle **approbateur** pour attribuer le rôle au compte, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-277">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="ff719-278">(Ce rôle inclut le rôle de réviseur.)</span><span class="sxs-lookup"><span data-stu-id="ff719-278">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="ff719-279">Cliquez sur le bouton **Ajouter** , sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe pour faire office d’éditeur, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-279">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="ff719-280">Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez le rôle d' **éditeur** pour attribuer le rôle au compte, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-280">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="ff719-281">(Ce rôle inclut le rôle de réviseur.)</span><span class="sxs-lookup"><span data-stu-id="ff719-281">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="ff719-282">Cliquez sur le bouton **Ajouter** , sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe pour qu’il serve de relecteur, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-282">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="ff719-283">Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez le rôle de **réviseur** pour affecter uniquement ce rôle au compte.</span><span class="sxs-lookup"><span data-stu-id="ff719-283">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="ff719-284">Procédure de gestion des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-284">Steps for managing GPOs</span></span>


<span data-ttu-id="ff719-285">Vous devez effectuer les étapes suivantes pour créer, modifier, réviser et déployer des objets de stratégie de groupe à l’aide d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-285">You must complete the following steps to create, edit, review, and deploy GPOs by using AGPM.</span></span> <span data-ttu-id="ff719-286">Par ailleurs, vous allez créer un modèle, supprimer un objet de stratégie de groupe, puis restaurer un objet GPO supprimé.</span><span class="sxs-lookup"><span data-stu-id="ff719-286">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="ff719-287">Étape 1: créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-287">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="ff719-288">Étape 2: modifier un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-288">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="ff719-289">Étape 3: vérifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-289">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="ff719-290">Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-290">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="ff719-291">Étape 5: supprimer et restaurer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-291">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="ff719-292">Étape 1: créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-292">Step 1: Create a GPO</span></span>

<span data-ttu-id="ff719-293">Dans un environnement doté de plusieurs administrateurs de stratégie de groupe, les utilisateurs dotés du rôle d’éditeur peuvent demander la création de nouveaux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-293">In an environment that has multiple Group Policy administrators, those with the Editor role can request that new GPOs be created.</span></span> <span data-ttu-id="ff719-294">Toutefois, cette demande doit être approuvée par une personne ayant le rôle d’approbateur.</span><span class="sxs-lookup"><span data-stu-id="ff719-294">However, that request must be approved by someone with the Approver role.</span></span>

<span data-ttu-id="ff719-295">Dans cette étape, vous utilisez un compte qui est le rôle d’éditeur pour demander la création d’un nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-295">In this step, you use an account that has the Editor role to request that a new GPO be created.</span></span> <span data-ttu-id="ff719-296">À l’aide d’un compte ayant le rôle d’approbateur, vous approuvez cette demande de création de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-296">Using an account that has the Approver role, you approve this request to create the GPO.</span></span>

**<span data-ttu-id="ff719-297">Pour demander la création et la gestion d’un objet de stratégie de groupe via AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-297">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="ff719-298">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide d’un compte d’utilisateur auquel est attribué le rôle d’éditeur dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-298">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="ff719-299">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-299">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="ff719-300">Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.</span><span class="sxs-lookup"><span data-stu-id="ff719-300">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="ff719-301">Dans la boîte de dialogue **nouvel objet GPO contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="ff719-301">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="ff719-302">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="ff719-302">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="ff719-303">Tapez **MyGPO** comme nom du nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-303">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="ff719-304">Tapez un commentaire pour le nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-304">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="ff719-305">Cliquez sur **créer en temps réel** pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation.</span><span class="sxs-lookup"><span data-stu-id="ff719-305">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="ff719-306">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-306">Click **Submit**.</span></span>

5.  <span data-ttu-id="ff719-307">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-307">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-308">Le nouvel objet GPO est affiché dans l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="ff719-308">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="ff719-309">Pour approuver la demande en attente de création d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-309">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="ff719-310">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur ayant le rôle d’approbateur dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-310">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="ff719-311">Ouvrez la boîte de réception de votre compte et notez que vous avez reçu un message électronique de l’alias AGPM avec la demande de l’éditeur pour créer un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-311">Open the e-mail inbox for the account, and notice that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="ff719-312">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-312">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="ff719-313">Dans l’onglet **contenu** , cliquez sur l’onglet **en attente** pour afficher les objets de stratégie de groupe en attente.</span><span class="sxs-lookup"><span data-stu-id="ff719-313">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="ff719-314">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **approuver**.</span><span class="sxs-lookup"><span data-stu-id="ff719-314">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="ff719-315">Cliquez sur **Oui** pour confirmer l’approbation et déplacez l’objet GPO sur l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="ff719-315">Click **Yes** to confirm approval and move the GPO to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="ff719-316">Étape 2: modifier un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-316">Step 2: Edit a GPO</span></span>

<span data-ttu-id="ff719-317">Vous pouvez utiliser les objets de stratégie de groupe pour configurer les paramètres de l’ordinateur ou de l’utilisateur et les déployer sur de nombreux ordinateurs ou utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ff719-317">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="ff719-318">Dans cette étape, vous utilisez un compte qui est le rôle d’éditeur permettant d’extraire un objet de stratégie de groupe de l’archive, de modifier l’objet de stratégie de groupe en mode hors connexion, de vérifier l’objet GPO modifié dans l’archive et de demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ff719-318">In this step, you use an account that has the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="ff719-319">Pour ce scénario, vous devez configurer un paramètre dans l’objet de stratégie de groupe pour exiger que le mot de passe comporte au moins huit caractères.</span><span class="sxs-lookup"><span data-stu-id="ff719-319">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters long.</span></span>

**<span data-ttu-id="ff719-320">Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier</span><span class="sxs-lookup"><span data-stu-id="ff719-320">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="ff719-321">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur ayant le rôle d’éditeur dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-321">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="ff719-322">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="ff719-323">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="ff719-323">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="ff719-324">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="ff719-324">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="ff719-325">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-325">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="ff719-326">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-326">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-327">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.</span><span class="sxs-lookup"><span data-stu-id="ff719-327">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="ff719-328">Pour modifier l’objet de stratégie de groupe hors connexion et configurer la longueur de mot de passe minimum</span><span class="sxs-lookup"><span data-stu-id="ff719-328">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="ff719-329">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre Éditeur de gestion des stratégies de groupe et changer une copie hors connexion de l’objet de stratégie de **groupe** .</span><span class="sxs-lookup"><span data-stu-id="ff719-329">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="ff719-330">Pour ce scénario, configurez la longueur minimale du mot de passe:</span><span class="sxs-lookup"><span data-stu-id="ff719-330">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="ff719-331">Sous **Configuration ordinateur**, double-cliquez sur **stratégies**, **Paramètres Windows**, **paramètres de sécurité**, stratégies de **compte**et **stratégie de mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="ff719-331">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="ff719-332">Dans le volet Détails, double-cliquez sur **longueur minimale du mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="ff719-332">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="ff719-333">Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie** , définissez le nombre de caractères sur **8**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-333">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="ff719-334">Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="ff719-334">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="ff719-335">Pour archiver l’objet de stratégie de groupe dans l’archive</span><span class="sxs-lookup"><span data-stu-id="ff719-335">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="ff719-336">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **Archiver**.</span><span class="sxs-lookup"><span data-stu-id="ff719-336">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="ff719-337">Tapez un commentaire, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-337">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="ff719-338">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-338">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-339">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.</span><span class="sxs-lookup"><span data-stu-id="ff719-339">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="ff719-340">Pour demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="ff719-340">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="ff719-341">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **déployer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-341">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="ff719-342">Dans la mesure où ce compte n’est pas un approbateur ou un administrateur AGPM, vous devez fournir une demande de déploiement.</span><span class="sxs-lookup"><span data-stu-id="ff719-342">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="ff719-343">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="ff719-343">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="ff719-344">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="ff719-344">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="ff719-345">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-345">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-346">**MyGPO** s’affiche dans la liste des objets de stratégie de groupe sous l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="ff719-346">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="ff719-347">Étape 3: vérifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-347">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="ff719-348">Dans le cadre de cette étape, vous agissez en tant qu’approbateur, vous créez des rapports et vous analysez les paramètres et les modifications apportées aux paramètres dans l’objet de stratégie de groupe pour déterminer s’ils doivent être approuvés.</span><span class="sxs-lookup"><span data-stu-id="ff719-348">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="ff719-349">Après avoir évalué l’objet de stratégie de groupe, vous le déployez dans l’environnement de production et le liez à un domaine ou à une unité d’organisation (UO).</span><span class="sxs-lookup"><span data-stu-id="ff719-349">After you evaluate the GPO, you deploy it to the production environment and link the GPO to a domain or an organizational unit (OU).</span></span> <span data-ttu-id="ff719-350">L’objet GPO est appliqué lorsque la stratégie de groupe est actualisée pour les ordinateurs de ce domaine ou UO.</span><span class="sxs-lookup"><span data-stu-id="ff719-350">The GPO takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="ff719-351">Pour vérifier les paramètres de l’objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-351">To review settings in the GPO</span></span>**

1. <span data-ttu-id="ff719-352">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide d’un compte d’utilisateur affecté du rôle d’approbateur dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-352">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="ff719-353">Tout administrateur de stratégie de groupe avec le rôle relecteur, qui est inclus dans tous les autres rôles, peut consulter les paramètres d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-353">Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.</span></span>

2. <span data-ttu-id="ff719-354">Ouvrez la boîte de réception du compte et notez que vous avez reçu un message électronique de l’alias AGPM avec une demande d’éditeur pour le déploiement d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-354">Open the e-mail inbox for the account and notice that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="ff719-355">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-355">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="ff719-356">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="ff719-356">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="ff719-357">Double-cliquez sur **MyGPO** pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="ff719-357">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="ff719-358">Passez en revue les paramètres dans la version la plus récente de MyGPO:</span><span class="sxs-lookup"><span data-stu-id="ff719-358">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="ff719-359">Dans la fenêtre **historique** , cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe avec le cachet d’heure le plus récent, cliquez sur **paramètres**, puis sur **rapport HTML** pour afficher un résumé des paramètres de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-359">In the **History** window, right-click the GPO version with the most recent time stamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="ff719-360">Dans le navigateur Web, cliquez sur **Afficher tout** pour afficher tous les paramètres de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-360">In the Web browser, click **show all** to display all the settings in the GPO.</span></span> <span data-ttu-id="ff719-361">Fermez le navigateur.</span><span class="sxs-lookup"><span data-stu-id="ff719-361">Close the browser.</span></span>

7. <span data-ttu-id="ff719-362">Comparez la version la plus récente de MyGPO à la première version archivée dans l’archive:</span><span class="sxs-lookup"><span data-stu-id="ff719-362">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="ff719-363">Dans la fenêtre **historique** , cliquez sur la version de l’objet de stratégie de groupe avec le cachet d’heure le plus récent.</span><span class="sxs-lookup"><span data-stu-id="ff719-363">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="ff719-364">Maintenez la touche CTRL enfoncée, puis cliquez sur la plus ancienne version d’objet de stratégie de groupe pour laquelle la version de l' **ordinateur** n’est pas \* \*.</span><span class="sxs-lookup"><span data-stu-id="ff719-364">Press CTRL and then click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="ff719-365">Cliquez sur le bouton **différences** .</span><span class="sxs-lookup"><span data-stu-id="ff719-365">Click the **Differences** button.</span></span> <span data-ttu-id="ff719-366">La section **stratégies de compte/stratégie de mot de passe** est mise en évidence en vert et précédée par **\ [+ \]**.</span><span class="sxs-lookup"><span data-stu-id="ff719-366">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**.</span></span> <span data-ttu-id="ff719-367">Cela indique que le paramètre est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-367">This indicates that the setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="ff719-368">Cliquez sur **stratégies de compte/stratégie de mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="ff719-368">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="ff719-369">Le paramètre de **longueur minimum du mot de passe** est également mis en surbrillance en vert et précédé de **\ [+ \]** indiquant qu’il est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-369">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="ff719-370">Fermez le navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="ff719-370">Close the Web browser.</span></span>

**<span data-ttu-id="ff719-371">Pour déployer l’objet de stratégie de groupe dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="ff719-371">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="ff719-372">Dans l’onglet **en attente** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **approuver**.</span><span class="sxs-lookup"><span data-stu-id="ff719-372">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="ff719-373">Tapez un commentaire à inclure dans l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-373">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="ff719-374">Cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="ff719-374">Click **Yes**.</span></span> <span data-ttu-id="ff719-375">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-375">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-376">L’objet de stratégie de groupe est déployé dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ff719-376">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="ff719-377">Pour lier l’objet de stratégie de groupe à un domaine ou une unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="ff719-377">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="ff719-378">Dans la console de gestion des stratégies de groupe, cliquez avec le bouton droit sur le domaine ou l’unité d’organisation auquel vous voulez appliquer l’objet de stratégie de groupe que vous avez configuré, puis cliquez sur **lier un objet de stratégie de groupe existant**.</span><span class="sxs-lookup"><span data-stu-id="ff719-378">In the GPMC, right-click either the domain or an organizational unit (OU) to which you want to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="ff719-379">Dans la boîte de dialogue **Sélectionner un objet GPO** , cliquez sur **MyGPO**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-379">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="ff719-380">Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-380">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="ff719-381">Dans cette étape, vous utilisez un compte doté du rôle d’éditeur pour créer et utiliser un modèle.</span><span class="sxs-lookup"><span data-stu-id="ff719-381">In this step, you use an account that has the Editor role to create and use a template.</span></span> <span data-ttu-id="ff719-382">Ce modèle est une version statique d’un objet de stratégie de groupe à utiliser comme point de départ pour la création de nouveaux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-382">That template is a static version of a GPO for use as a starting point for creating new GPOs.</span></span> <span data-ttu-id="ff719-383">Même si vous ne pouvez pas modifier un modèle, vous pouvez créer un nouvel objet de stratégie de groupe basé sur un modèle.</span><span class="sxs-lookup"><span data-stu-id="ff719-383">Although you cannot edit a template, you can create a new GPO based on a template.</span></span> <span data-ttu-id="ff719-384">Les modèles permettent de créer rapidement plusieurs objets de stratégie de groupe qui incluent un grand nombre des mêmes paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="ff719-384">Templates are useful for quickly creating multiple GPOs that include many of the same policy settings.</span></span>

**<span data-ttu-id="ff719-385">Pour créer un modèle sur la base d’un objet de stratégie de groupe existant</span><span class="sxs-lookup"><span data-stu-id="ff719-385">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="ff719-386">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide d’un compte d’utilisateur auquel le rôle d’éditeur est attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-386">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="ff719-387">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-387">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="ff719-388">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="ff719-388">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="ff719-389">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **enregistrer en tant que modèle** pour créer un modèle contenant tous les paramètres actuellement dans MyGPO.</span><span class="sxs-lookup"><span data-stu-id="ff719-389">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="ff719-390">Tapez **MyTemplate** comme nom pour le modèle et un commentaire, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-390">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="ff719-391">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-391">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-392">Le nouveau modèle s’affiche sous l’onglet **modèles** .</span><span class="sxs-lookup"><span data-stu-id="ff719-392">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="ff719-393">Pour demander la création et la gestion d’un objet de stratégie de groupe via AGPM</span><span class="sxs-lookup"><span data-stu-id="ff719-393">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="ff719-394">Cliquez sur l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="ff719-394">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="ff719-395">Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.</span><span class="sxs-lookup"><span data-stu-id="ff719-395">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="ff719-396">Dans la boîte de dialogue **nouvel objet GPO contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="ff719-396">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="ff719-397">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="ff719-397">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="ff719-398">Tapez **MyOtherGPO** comme nom du nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-398">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="ff719-399">Tapez un commentaire pour le nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-399">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="ff719-400">Cliquez sur **créer en temps réel** pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation.</span><span class="sxs-lookup"><span data-stu-id="ff719-400">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="ff719-401">Dans **modèle d’objet de stratégie de groupe**, sélectionnez **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="ff719-401">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="ff719-402">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-402">Click **Submit**.</span></span>

4.  <span data-ttu-id="ff719-403">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-404">Le nouvel objet GPO est affiché dans l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="ff719-404">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="ff719-405">Utilisez un compte auquel est attribué le rôle d’approbateur pour approuver la demande en attente de création de l’objet de stratégie de groupe, comme vous l’avez fait à l' [étape 1: créer un objet de stratégie de groupe](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="ff719-405">Use an account that is assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="ff719-406">MyTemplate incorpore tous les paramètres que vous avez configurés dans MyGPO.</span><span class="sxs-lookup"><span data-stu-id="ff719-406">MyTemplate incorporates all the settings that you configured in MyGPO.</span></span> <span data-ttu-id="ff719-407">Dans la mesure où MyOtherGPO a été créé à l’aide de MyTemplate, il s’agit d’abord de tous les paramètres MyGPO contenus au moment de la création de MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="ff719-407">Because MyOtherGPO was created using MyTemplate, it at first contains all the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="ff719-408">Pour confirmer cela, vous pouvez générer un rapport de différences et comparer MyOtherGPO à MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="ff719-408">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="ff719-409">Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier</span><span class="sxs-lookup"><span data-stu-id="ff719-409">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="ff719-410">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide d’un compte d’utilisateur auquel le rôle d’éditeur est attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff719-410">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="ff719-411">Cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="ff719-411">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="ff719-412">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-412">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="ff719-413">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-413">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-414">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.</span><span class="sxs-lookup"><span data-stu-id="ff719-414">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="ff719-415">Pour modifier l’objet de stratégie de groupe hors connexion et configurer la durée de verrouillage du compte</span><span class="sxs-lookup"><span data-stu-id="ff719-415">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="ff719-416">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre Éditeur de gestion des stratégies de groupe et changer une copie hors connexion de l’objet de stratégie de **groupe** .</span><span class="sxs-lookup"><span data-stu-id="ff719-416">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="ff719-417">Pour ce scénario, configurez la longueur minimale du mot de passe:</span><span class="sxs-lookup"><span data-stu-id="ff719-417">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="ff719-418">Sous **Configuration ordinateur**, double-cliquez sur **stratégies**, **Paramètres Windows**, **paramètres de sécurité**, stratégies de **compte**et stratégie de **verrouillage du compte**.</span><span class="sxs-lookup"><span data-stu-id="ff719-418">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="ff719-419">Dans le volet Détails, double-cliquez sur **durée de verrouillage du compte**.</span><span class="sxs-lookup"><span data-stu-id="ff719-419">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="ff719-420">Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie**, définissez une durée de **30** minutes, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-420">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="ff719-421">Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="ff719-421">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="ff719-422">Consultez MyOtherGPO dans l’archive et demandez le déploiement comme vous l’avez fait pour MyGPO à l' [étape 2: modifier un objet de stratégie de groupe](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="ff719-422">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="ff719-423">Vous pouvez comparer MyOtherGPO à MyGPO ou à MyTemplate à l’aide de rapports de différences.</span><span class="sxs-lookup"><span data-stu-id="ff719-423">You can compare MyOtherGPO to MyGPO or to MyTemplate by using difference reports.</span></span> <span data-ttu-id="ff719-424">Tout compte qui inclut le rôle de réviseur (Administrateur AGPM [contrôle total \], approbateur, éditeur ou réviseur) peut générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="ff719-424">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="ff719-425">Pour comparer un objet GPO à un autre et à un modèle</span><span class="sxs-lookup"><span data-stu-id="ff719-425">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="ff719-426">Pour comparer MyGPO et MyOtherGPO:</span><span class="sxs-lookup"><span data-stu-id="ff719-426">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="ff719-427">Dans l’onglet **contrôlé** , cliquez sur **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="ff719-427">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="ff719-428">Appuyez sur CTRL et cliquez sur **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="ff719-428">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="ff719-429">Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **rapport HTML**.</span><span class="sxs-lookup"><span data-stu-id="ff719-429">Right-click **MyOtherGPO**, point to **Differences**, and then click **HTML Report**.</span></span>

2.  <span data-ttu-id="ff719-430">Pour comparer MyOtherGPO et MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="ff719-430">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="ff719-431">Dans l’onglet **contrôlé** , cliquez sur **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="ff719-431">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="ff719-432">Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **modèle**.</span><span class="sxs-lookup"><span data-stu-id="ff719-432">Right-click **MyOtherGPO**, point to **Differences**, and then click **Template**.</span></span>

    3.  <span data-ttu-id="ff719-433">Sélectionnez **MyTemplate** et **HTML Report**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-433">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="ff719-434">Étape 5: supprimer et restaurer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-434">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="ff719-435">Dans le cadre de cette étape, vous jouerez le rôle d’approbateur pour supprimer un objet GPO.</span><span class="sxs-lookup"><span data-stu-id="ff719-435">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="ff719-436">Pour supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-436">To delete a GPO</span></span>**

1.  <span data-ttu-id="ff719-437">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur est attribué.</span><span class="sxs-lookup"><span data-stu-id="ff719-437">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver.</span></span>

2.  <span data-ttu-id="ff719-438">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-438">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="ff719-439">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="ff719-439">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="ff719-440">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-440">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="ff719-441">Cliquez sur **Supprimer l’objet GPO d’archive et de production** pour supprimer la version dans l’archive et la version déployée de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ff719-441">Click **Delete GPO from archive and production** to delete both the version in the archive and the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="ff719-442">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-442">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="ff719-443">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-443">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-444">L’objet de stratégie de groupe est supprimé de l’onglet **contrôlé** et s’affiche sous l’onglet de la **Corbeille** , où il peut être restauré ou détruit.</span><span class="sxs-lookup"><span data-stu-id="ff719-444">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="ff719-445">Occasionnellement, vous pouvez découvrir après avoir supprimé un objet de stratégie de groupe qui est toujours nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ff719-445">Occasionally you may discover after you delete a GPO that it is still needed.</span></span> <span data-ttu-id="ff719-446">Dans le cadre de cette étape, vous vous attendez en tant qu’approbateur de la restauration d’un objet de stratégie de groupe qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="ff719-446">In this step, you act as an Approver to restore a GPO that was deleted.</span></span>

**<span data-ttu-id="ff719-447">Pour restaurer un objet de stratégie de groupe supprimé</span><span class="sxs-lookup"><span data-stu-id="ff719-447">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="ff719-448">Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.</span><span class="sxs-lookup"><span data-stu-id="ff719-448">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="ff719-449">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **restaurer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-449">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="ff719-450">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff719-450">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="ff719-451">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-451">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-452">L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="ff719-452">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="ff719-453">**Remarques**  La restauration d’un objet de stratégie de groupe dans l’archive ne le redéploie pas automatiquement dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ff719-453">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="ff719-454">Pour renvoyer l’objet de stratégie de groupe à l’environnement de production, déployez l’objet GPO comme à l' [étape 3: passer en revue et déployer un objet de stratégie de groupe](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="ff719-454">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="ff719-455">Après la modification et le déploiement d’un objet de stratégie de groupe, il est possible que les modifications récentes apportées à l’objet GPO causent un problème.</span><span class="sxs-lookup"><span data-stu-id="ff719-455">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="ff719-456">Dans le cadre de cette étape, vous faites Office d’approbateur pour restaurer une version antérieure de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-456">In this step, you act as an Approver to roll back to an earlier version of the GPO.</span></span> <span data-ttu-id="ff719-457">Vous pouvez revenir à une version quelconque de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ff719-457">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="ff719-458">Vous pouvez utiliser des commentaires et des étiquettes pour identifier les versions connues et en cas de modifications spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ff719-458">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="ff719-459">Pour restaurer une version antérieure d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ff719-459">To roll back to an earlier version of a GPO</span></span>**

1.  <span data-ttu-id="ff719-460">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="ff719-460">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="ff719-461">Double-cliquez sur **MyGPO** pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="ff719-461">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="ff719-462">Cliquez avec le bouton droit sur la version que vous voulez déployer, cliquez sur **déployer**, puis sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="ff719-462">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="ff719-463">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-463">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff719-464">Dans la fenêtre **historique** , cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ff719-464">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="ff719-465">**Remarques**  Pour vérifier que la version qui a été redéployée est la version prévue, examinez un rapport de différences pour les deux versions.</span><span class="sxs-lookup"><span data-stu-id="ff719-465">**Note** To verify that the version that was redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="ff719-466">Dans la fenêtre **historique** de l’objet de stratégie de groupe, sélectionnez les deux versions, cliquez dessus avec le bouton droit, pointez sur **différence**, puis cliquez sur rapport **HTML** ou sur **rapport XML**.</span><span class="sxs-lookup"><span data-stu-id="ff719-466">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 






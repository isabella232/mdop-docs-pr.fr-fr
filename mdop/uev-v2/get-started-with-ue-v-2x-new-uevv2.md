---
title: Prise en main d'UE-V2.x
description: Prise en main d'UE-V2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809864"
---
# <span data-ttu-id="a3369-103">Prise en main d'UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="a3369-103">Get Started with UE-V 2.x</span></span>


<span data-ttu-id="a3369-104">Suivez les étapes décrites dans ce guide pour déployer rapidement Microsoft User Interface Virtualization (UE-V) 2,0 ou 2,1 dans un environnement de test de petite taille.</span><span class="sxs-lookup"><span data-stu-id="a3369-104">Follow the steps in this guide to quickly deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 in a small test environment.</span></span> <span data-ttu-id="a3369-105">Cela vous aide à déterminer si UE-V est la bonne solution pour gérer les paramètres utilisateur sur plusieurs appareils au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="a3369-105">This helps you determine whether UE-V is the right solution to manage user settings across multiple devices within your enterprise.</span></span>

<span data-ttu-id="a3369-106">**Remarques**  Les informations contenues dans cette section sont répétées plus en détail dans le reste de la documentation.</span><span class="sxs-lookup"><span data-stu-id="a3369-106">**Note** The information in this section is repeated in greater detail throughout the rest of the documentation.</span></span> <span data-ttu-id="a3369-107">Par conséquent, si vous savez déjà qu’UE-V 2 est la bonne solution et que vous n’avez pas besoin de l’évaluer, vous pouvez juste vous rendre à la [préparation d’un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="a3369-107">So if you already know that UE-V 2 is the right solution and you don’t need to evaluate it, you can just go right to [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span></span>

 

<span data-ttu-id="a3369-108">L’installation standard de UE-V synchronise les paramètres Microsoft Windows et Office par défaut ainsi que de nombreux paramètres d’application Windows.</span><span class="sxs-lookup"><span data-stu-id="a3369-108">The standard installation of UE-V synchronizes the default Microsoft Windows and Office settings and many Windows app settings.</span></span> <span data-ttu-id="a3369-109">Assurez-vous que votre environnement de test inclut au moins deux ordinateurs utilisateurs qui partagent l’accès au réseau et que vous évaluez UE-V en une courte période.</span><span class="sxs-lookup"><span data-stu-id="a3369-109">Make sure your test environment includes two or more user computers that share network access and you’ll be evaluating UE-V in just a short time.</span></span>

-   <span data-ttu-id="a3369-110">[Étape 1: confirmer les conditions préalables](#step1): s’assurer que votre environnement peut exécuter UE-V, y compris des détails sur les configurations prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a3369-110">[Step 1: Confirm Prerequisites](#step1): Make sure your environment is able to run UE-V, including details about supported configurations.</span></span>

-   <span data-ttu-id="a3369-111">[Étape 2: déployer l’emplacement de stockage des paramètres pour UE-v 2](#step2): tous les déploiements d’UE-v nécessitent un emplacement pour les packages de paramètres qui contiennent les valeurs de paramètre synchronisées.</span><span class="sxs-lookup"><span data-stu-id="a3369-111">[Step 2: Deploy the Settings Storage Location for UE-V 2](#step2): All UE-V deployments require a location for settings packages that contain the synchronized setting values.</span></span>

-   <span data-ttu-id="a3369-112">[Étape 3: déployer l’agent UE-V 2](#step3): pour synchroniser les paramètres à l’aide d’UE-v, l’agent UE-v doit être installé et exécuté sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="a3369-112">[Step 3: Deploy the UE-V 2 Agent](#step3): To synchronize settings using UE-V, devices must have the UE-V Agent installed and running.</span></span>

-   <span data-ttu-id="a3369-113">[Étape 4: testez le déploiement de votre version d’évaluation d’UE-v 2](#step4): exécutez quelques tests sur deux ordinateurs sur lesquels l’agent UE-v est installé et découvrez le fonctionnement d’UE-v.</span><span class="sxs-lookup"><span data-stu-id="a3369-113">[Step 4: Test Your UE-V 2 Evaluation Deployment](#step4): Run a few tests on two computers that have the UE-V Agent installed and see how UE-V works.</span></span>

<span data-ttu-id="a3369-114">Voilà!</span><span class="sxs-lookup"><span data-stu-id="a3369-114">That’s it!</span></span> <span data-ttu-id="a3369-115">Après avoir suivi ces étapes, vous serez en mesure d’évaluer la façon dont UE-V peut travailler au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="a3369-115">Once you follow the steps, you’ll be able to evaluate how UE-V can work in your enterprise.</span></span>

<span data-ttu-id="a3369-116">**Nouvelle évaluation:** Vous pouvez également effectuer des étapes supplémentaires pour configurer certaines applications tierces et métier pour synchroniser leurs paramètres à l’aide d’UE-V, comme décrit dans la section [déployer UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="a3369-116">**Further evaluation:** You can also perform additional steps to configure some third-party and line-of-business applications to synchronize their settings using UE-V as detailed in [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <a href="" id="step1"></a><span data-ttu-id="a3369-117">Étape 1: confirmer les conditions préalables</span><span class="sxs-lookup"><span data-stu-id="a3369-117">Step 1: Confirm Prerequisites</span></span>


<span data-ttu-id="a3369-118">Avant de continuer, assurez-vous que votre environnement inclut les exigences requises pour exécuter UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3369-118">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="a3369-119">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a3369-119">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="a3369-120">Édition</span><span class="sxs-lookup"><span data-stu-id="a3369-120">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="a3369-121">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a3369-121">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="a3369-122">Architecture système</span><span class="sxs-lookup"><span data-stu-id="a3369-122">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="a3369-123">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3369-123">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="a3369-124">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="a3369-124">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3369-125">Plus de.</span><span class="sxs-lookup"><span data-stu-id="a3369-125">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-126">Edition intégrale, entreprise ou édition professionnelle</span><span class="sxs-lookup"><span data-stu-id="a3369-126">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-127">SP1</span><span class="sxs-lookup"><span data-stu-id="a3369-127">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-128">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a3369-128">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-129">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3369-129">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-130">.NET Framework 4 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3369-130">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3369-131">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="a3369-131">Windows Server2008R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-132">Standard, entreprise, Datacenter ou serveur Web</span><span class="sxs-lookup"><span data-stu-id="a3369-132">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-133">SP1</span><span class="sxs-lookup"><span data-stu-id="a3369-133">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3369-134">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-135">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3369-135">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-136">.NET Framework 4 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3369-136">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3369-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3369-137">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-138">Entreprise ou professionnel</span><span class="sxs-lookup"><span data-stu-id="a3369-138">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-139">None</span><span class="sxs-lookup"><span data-stu-id="a3369-139">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-140">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a3369-140">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-141">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3369-141">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-142">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="a3369-142">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3369-143">Windows Server2012R2 ou Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="a3369-143">Windows Server 2012 or Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-144">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="a3369-144">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-145">None</span><span class="sxs-lookup"><span data-stu-id="a3369-145">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-146">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3369-146">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-147">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3369-147">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-148">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="a3369-148">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3369-149">Windows 10, version pre-1607</span><span class="sxs-lookup"><span data-stu-id="a3369-149">Windows 10, pre-1607 verison</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-150">Entreprise ou professionnel</span><span class="sxs-lookup"><span data-stu-id="a3369-150">Enterprise or Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a3369-151">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a3369-151">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-152">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3369-152">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-153">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="a3369-153">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3369-154">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="a3369-154">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-155">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="a3369-155">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-156">None</span><span class="sxs-lookup"><span data-stu-id="a3369-156">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-157">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3369-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-158">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a3369-158">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3369-159">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="a3369-159">.NET Framework 4.5</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a3369-160">**Remarque:** À partir de Windows 10, la version 1607, UE-V est incluse dans [Windows 10 pour les entreprises](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) et ne fait plus partie du pack d’optimisation de bureau Microsoft</span><span class="sxs-lookup"><span data-stu-id="a3369-160">**Note:** Starting with Windows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack</span></span>

<span data-ttu-id="a3369-161">En outre...</span><span class="sxs-lookup"><span data-stu-id="a3369-161">Also…</span></span>

-   <span data-ttu-id="a3369-162">**Licence MDOP:** Cette technologie fait partie du pack d’optimisation de bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="a3369-162">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="a3369-163">Les clients d’entreprise peuvent obtenir MDOP avec Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="a3369-163">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="a3369-164">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir comment obtenir MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="a3369-164">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="a3369-165">**Informations d’identification d’administration** pour les ordinateurs sur lesquels vous allez procéder à l’installation</span><span class="sxs-lookup"><span data-stu-id="a3369-165">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

## <a href="" id="step2"></a><span data-ttu-id="a3369-166">Étape 2: déployer l’emplacement de stockage des paramètres pour UE-V 2</span><span class="sxs-lookup"><span data-stu-id="a3369-166">Step 2: Deploy the Settings Storage Location for UE-V 2</span></span>


<span data-ttu-id="a3369-167">Vous devez déployer un emplacement de stockage des paramètres (un partage réseau standard où les paramètres utilisateur sont stockés dans un fichier de package de paramètres).</span><span class="sxs-lookup"><span data-stu-id="a3369-167">You’ll need to deploy a settings storage location, a standard network share where user settings are stored in a settings package file.</span></span> <span data-ttu-id="a3369-168">Lorsque vous créez le partage de stockage des paramètres, vous devez limiter l’accès aux utilisateurs qui en ont besoin.</span><span class="sxs-lookup"><span data-stu-id="a3369-168">When you create the settings storage share, you should limit access to users that require it.</span></span> <span data-ttu-id="a3369-169">[Le déploiement d’un emplacement de stockage des paramètres](https://technet.microsoft.com/library/dn458891.aspx#ssl) fournit des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="a3369-169">[Deploy a Settings Storage Location](https://technet.microsoft.com/library/dn458891.aspx#ssl) provides more detailed information.</span></span>

**<span data-ttu-id="a3369-170">Créer un partage réseau</span><span class="sxs-lookup"><span data-stu-id="a3369-170">Create a network share</span></span>**

1.  <span data-ttu-id="a3369-171">Créer un groupe de sécurité et y ajouter des utilisateurs UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3369-171">Create a new security group and add UE-V users to it.</span></span>

2.  <span data-ttu-id="a3369-172">Créez un dossier sur l’ordinateur central dans lequel sont stockés les packages de paramètres UE-V, puis accordez aux utilisateurs d’UE-V l’accès à un dossier.</span><span class="sxs-lookup"><span data-stu-id="a3369-172">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="a3369-173">L’administrateur qui prend en charge UE-V doit disposer de l’autorisation d’accès à ce dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="a3369-173">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="a3369-174">Attribuez des autorisations aux utilisateurs d’UE-V pour créer un répertoire lors de leur connexion.</span><span class="sxs-lookup"><span data-stu-id="a3369-174">Assign UE-V users permission to create a directory when they connect.</span></span> <span data-ttu-id="a3369-175">Accordez l’autorisation complète à tous les sous-répertoires de ce répertoire, mais bloquez l’accès à un élément plus haut.</span><span class="sxs-lookup"><span data-stu-id="a3369-175">Grant full permission to all subdirectories of that directory, but block access to anything above.</span></span>

    1.  <span data-ttu-id="a3369-176">Définissez les autorisations de blocs de messages serveur au niveau du partage (SMB) suivantes pour le dossier emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="a3369-176">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="a3369-177">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a3369-177">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="a3369-178">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="a3369-178">Recommended permissions</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="a3369-179">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="a3369-179">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="a3369-180">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="a3369-180">No permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="a3369-181">Groupe de sécurité des utilisateurs d’UE-V</span><span class="sxs-lookup"><span data-stu-id="a3369-181">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="a3369-182">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="a3369-182">Full control</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

    2.  <span data-ttu-id="a3369-183">Définissez les autorisations de système de fichiers NTFS suivantes pour le dossier emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="a3369-183">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="a3369-184">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a3369-184">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="a3369-185">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="a3369-185">Recommended permissions</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="a3369-186">Folder</span><span class="sxs-lookup"><span data-stu-id="a3369-186">Folder</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="a3369-187">Créateur/propriétaire</span><span class="sxs-lookup"><span data-stu-id="a3369-187">Creator/owner</span></span></p></td>
        <td align="left"><p><span data-ttu-id="a3369-188">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="a3369-188">Full control</span></span></p></td>
        <td align="left"><p><span data-ttu-id="a3369-189">Sous-dossiers et fichiers uniquement</span><span class="sxs-lookup"><span data-stu-id="a3369-189">Subfolders and files only</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="a3369-190">Groupe de sécurité des utilisateurs d’UE-V</span><span class="sxs-lookup"><span data-stu-id="a3369-190">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="a3369-191">Afficher le dossier/lire les données, créer des dossiers/ajouter des données</span><span class="sxs-lookup"><span data-stu-id="a3369-191">List folder/read data, create folders/append data</span></span></p></td>
        <td align="left"><p><span data-ttu-id="a3369-192">Ce dossier uniquement</span><span class="sxs-lookup"><span data-stu-id="a3369-192">This folder only</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

**<span data-ttu-id="a3369-193">Note de sécurité:</span><span class="sxs-lookup"><span data-stu-id="a3369-193">Security Note:</span></span>**

<span data-ttu-id="a3369-194">Si vous créez le partage de stockage de paramètres sur un ordinateur exécutant un système d’exploitation Windows Server, configurez UE-V pour vérifier que le groupe Administrateurs local ou l’utilisateur actuel est le propriétaire du dossier dans lequel les packages de paramètres sont stockés.</span><span class="sxs-lookup"><span data-stu-id="a3369-194">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="a3369-195">Pour activer cette sécurité supplémentaire, spécifiez ce paramètre dans l’éditeur du registre de Windows Server:</span><span class="sxs-lookup"><span data-stu-id="a3369-195">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="a3369-196">Ajoutez une clé de Registre **reg \ _DWORD** nommée **«RepositoryOwnerCheckEnabled»** dans **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="a3369-196">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="a3369-197">Définissez la valeur de la clé de Registre sur *1*.</span><span class="sxs-lookup"><span data-stu-id="a3369-197">Set the registry key value to *1*.</span></span>

## <a href="" id="step3"></a><span data-ttu-id="a3369-198">Étape 3: déployer l’agent UE-V 2</span><span class="sxs-lookup"><span data-stu-id="a3369-198">Step 3: Deploy the UE-V 2 Agent</span></span>


<span data-ttu-id="a3369-199">UE-V agent synchronise les paramètres d’application et de fenêtre entre les ordinateurs et appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a3369-199">The UE-V Agent synchronizes application and Windows settings between users’ computers and devices.</span></span> <span data-ttu-id="a3369-200">À des fins d’évaluation, installez l’agent sur au moins deux ordinateurs de votre environnement de test qui appartiennent au même utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3369-200">For evaluation purposes, install the agent on at least two computers in your test environment that belong to the same user.</span></span>

<span data-ttu-id="a3369-201">Exécutez le fichier AgentSetup.exe à partir de la ligne de commande pour installer l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3369-201">Run the AgentSetup.exe file from the command line to install the UE-V Agent.</span></span> <span data-ttu-id="a3369-202">Il s’installe sur les systèmes d’exploitation 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a3369-202">It installs on both 32-bit and 64-bit operating systems.</span></span>

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

<span data-ttu-id="a3369-203">Vous devez spécifier le paramètre de ligne de commande SettingsStoragePath comme partage réseau à partir de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="a3369-203">You must specify the SettingsStoragePath command line parameter as the network share from Step 2.</span></span> <span data-ttu-id="a3369-204">[Le déploiement d’un agent UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) fournit des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="a3369-204">[Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more detailed information.</span></span>

## <a href="" id="step4"></a><span data-ttu-id="a3369-205">Étape 4: tester le déploiement de votre version d’évaluation d’UE-V 2</span><span class="sxs-lookup"><span data-stu-id="a3369-205">Step 4: Test Your UE-V 2 Evaluation Deployment</span></span>


<span data-ttu-id="a3369-206">Vous pouvez maintenant exécuter quelques tests sur votre déploiement d’évaluation d’UE-V pour découvrir le fonctionnement d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3369-206">You can now run a few tests on your UE-V evaluation deployment to see how UE-V works.</span></span>

****

1.  <span data-ttu-id="a3369-207">Sur le premier ordinateur (ordinateur A), effectuez une ou plusieurs des modifications suivantes:</span><span class="sxs-lookup"><span data-stu-id="a3369-207">On the first computer (Computer A), make one or more of these changes:</span></span>

    1.  <span data-ttu-id="a3369-208">Ouvrez le bureau Windows et déplacez la barre des tâches vers un emplacement différent dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a3369-208">Open to Windows Desktop and move the taskbar to a different location in the window.</span></span>

    2.  <span data-ttu-id="a3369-209">Changer la police par défaut.</span><span class="sxs-lookup"><span data-stu-id="a3369-209">Change the default fonts.</span></span>

    3.  <span data-ttu-id="a3369-210">Ouvrez Calculator et sélectionnez **scientifique**.</span><span class="sxs-lookup"><span data-stu-id="a3369-210">Open Calculator and set to **scientific**.</span></span>

    4.  <span data-ttu-id="a3369-211">Modifiez le comportement de toutes les applications Windows, comme décrit dans [gestion d’UE-V 2. x modèles d’emplacement des paramètres à l’aide de Windows PowerShell et WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="a3369-211">Change the behavior of any Windows app, as detailed in [Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    5.  <span data-ttu-id="a3369-212">Désactivez la synchronisation des paramètres de compte Microsoft et les profils d’itinérance.</span><span class="sxs-lookup"><span data-stu-id="a3369-212">Disable Microsoft Account settings synchronization and Roaming Profiles.</span></span>

2.  <span data-ttu-id="a3369-213">Déconnectez-vous de l’ordinateur A. les paramètres sont enregistrés dans un package de paramètres d’UE-V lorsque les utilisateurs verrouillent, ferment ou quittent une application, ou lorsque le fournisseur de synchronisation s’exécute (toutes les 30 minutes par défaut).</span><span class="sxs-lookup"><span data-stu-id="a3369-213">Log off Computer A. Settings are saved in a UE-V settings package when users lock, logoff, exit an application, or when the sync provider runs (every 30 minutes by default).</span></span>

3.  <span data-ttu-id="a3369-214">Connectez-vous au deuxième ordinateur (ordinateur B) en tant qu’utilisateur de l’ordinateur A.</span><span class="sxs-lookup"><span data-stu-id="a3369-214">Log in to the second computer (Computer B) as the same user as Computer A.</span></span>

4.  <span data-ttu-id="a3369-215">Ouvrez le bureau Windows et vérifiez que l’emplacement de la barre des tâches correspond à celui de l’ordinateur A. Vérifiez que les polices par défaut correspondent et que la calculatrice est définie sur **science**.</span><span class="sxs-lookup"><span data-stu-id="a3369-215">Open to Windows Desktop and verify that the taskbar location matches that of Computer A. Verify that the default fonts match and that Calculator is set to **scientific**.</span></span> <span data-ttu-id="a3369-216">Vérifiez également la modification apportée à une application Windows.</span><span class="sxs-lookup"><span data-stu-id="a3369-216">Also verify the change you made to any Windows app.</span></span>

<span data-ttu-id="a3369-217">Vous pouvez redéfinir les paramètres de l’ordinateur B sur les paramètres de l’ordinateur d’origine.</span><span class="sxs-lookup"><span data-stu-id="a3369-217">You can change the settings in Computer B back to the original Computer A settings.</span></span> <span data-ttu-id="a3369-218">Déconnectez-vous de l’ordinateur B et connectez-vous à l’ordinateur A pour vérifier les modifications.</span><span class="sxs-lookup"><span data-stu-id="a3369-218">Then log off Computer B and log in to Computer A to verify the changes.</span></span>

## <span data-ttu-id="a3369-219">Autres ressources pour ce produit</span><span class="sxs-lookup"><span data-stu-id="a3369-219">Other resources for this product</span></span>


-   [<span data-ttu-id="a3369-220">Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="a3369-220">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="a3369-221">Préparer un déploiement UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="a3369-221">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="a3369-222">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="a3369-222">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="a3369-223">Résolution des problèmes de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="a3369-223">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="a3369-224">Informations techniques de référence sur UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="a3369-224">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 






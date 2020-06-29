---
title: Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell
description: Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell
author: dansimp
ms.assetid: 1d6c2d25-81ec-4ff8-9262-6b4cf484a376
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b7af1781a7a443a4fcfc8e7d4a92525b34986763
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805340"
---
# <span data-ttu-id="f3daf-103">Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3daf-103">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>


<span data-ttu-id="f3daf-104">Les sections suivantes vous expliquent comment effectuer différentes tâches de gestion sur un ordinateur client autonome à l’aide de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f3daf-104">The following sections explain how to perform various management tasks on a stand-alone client computer by using PowerShell:</span></span>

-   [<span data-ttu-id="f3daf-105">Pour renvoyer une liste de packages</span><span class="sxs-lookup"><span data-stu-id="f3daf-105">To return a list of packages</span></span>](#bkmk-return-pkgs-standalone-posh)

-   [<span data-ttu-id="f3daf-106">Pour ajouter un package</span><span class="sxs-lookup"><span data-stu-id="f3daf-106">To add a package</span></span>](#bkmk-add-pkgs-standalone-posh)

-   [<span data-ttu-id="f3daf-107">Pour publier un package</span><span class="sxs-lookup"><span data-stu-id="f3daf-107">To publish a package</span></span>](#bkmk-pub-pkg-standalone-posh)

-   [<span data-ttu-id="f3daf-108">Pour publier un package pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f3daf-108">To publish a package to a specific user</span></span>](#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="f3daf-109">Pour ajouter et publier un package</span><span class="sxs-lookup"><span data-stu-id="f3daf-109">To add and publish a package</span></span>](#bkmk-add-pub-pkg-standalone-posh)

-   [<span data-ttu-id="f3daf-110">Pour annuler la publication d’un package existant</span><span class="sxs-lookup"><span data-stu-id="f3daf-110">To unpublish an existing package</span></span>](#bkmk-unpub-pkg-standalone-posh)

-   [<span data-ttu-id="f3daf-111">Pour annuler la publication d’un package pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f3daf-111">To unpublish a package for a specific user</span></span>](#bkmk-unpub-pkg-specfc-use)

-   [<span data-ttu-id="f3daf-112">Pour supprimer un package existant</span><span class="sxs-lookup"><span data-stu-id="f3daf-112">To remove an existing package</span></span>](#bkmk-remove-pkg-standalone-posh)

-   [<span data-ttu-id="f3daf-113">Pour permettre uniquement aux administrateurs de publier ou de retirer des packages</span><span class="sxs-lookup"><span data-stu-id="f3daf-113">To enable only administrators to publish or unpublish packages</span></span>](#bkmk-admins-pub-pkgs)

-   [<span data-ttu-id="f3daf-114">Présentation des packages en attente (UserPending et GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="f3daf-114">Understanding pending packages (UserPending and GlobalPending)</span></span>](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a><span data-ttu-id="f3daf-115">Pour renvoyer une liste de packages</span><span class="sxs-lookup"><span data-stu-id="f3daf-115">To return a list of packages</span></span>


<span data-ttu-id="f3daf-116">Utilisez les informations suivantes pour renvoyer une liste des packages qui sont habilités à un utilisateur spécifique:</span><span class="sxs-lookup"><span data-stu-id="f3daf-116">Use the following information to return a list of packages that are entitled to a specific user:</span></span>

<span data-ttu-id="f3daf-117">**Cmdlet**: Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-117">**Cmdlet**: Get-AppvClientPackage</span></span>

<span data-ttu-id="f3daf-118">**Paramètres**:-nom-version-PackageID-VersionId</span><span class="sxs-lookup"><span data-stu-id="f3daf-118">**Parameters**: -Name -Version -PackageID -VersionID</span></span>

<span data-ttu-id="f3daf-119">**Exemple**: Get-AppvClientPackage – Name "ContosoApplication"-version 2</span><span class="sxs-lookup"><span data-stu-id="f3daf-119">**Example**: Get-AppvClientPackage –Name “ContosoApplication” -Version 2</span></span>

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a><span data-ttu-id="f3daf-120">Pour ajouter un package</span><span class="sxs-lookup"><span data-stu-id="f3daf-120">To add a package</span></span>


<span data-ttu-id="f3daf-121">Utilisez les informations suivantes pour ajouter un package à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3daf-121">Use the following information to add a package to a computer.</span></span>

<span data-ttu-id="f3daf-122">**Important**  Cet exemple n’ajoute qu’un package.</span><span class="sxs-lookup"><span data-stu-id="f3daf-122">**Important** This example only adds a package.</span></span> <span data-ttu-id="f3daf-123">Le package n’est pas publié pour l’utilisateur ou l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3daf-123">It does not publish the package to the user or the computer.</span></span>

 

<span data-ttu-id="f3daf-124">**Applet**de passe: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-124">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="f3daf-125">**Exemple**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV</span><span class="sxs-lookup"><span data-stu-id="f3daf-125">**Example**: $Contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv</span></span>

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a><span data-ttu-id="f3daf-126">Pour publier un package</span><span class="sxs-lookup"><span data-stu-id="f3daf-126">To publish a package</span></span>


<span data-ttu-id="f3daf-127">Utilisez les informations suivantes pour publier un package qui a été ajouté à un utilisateur spécifique ou globalement à un utilisateur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3daf-127">Use the following information to publish a package that has been added to a specific user or globally to any user on the computer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3daf-128">Méthode de publication</span><span class="sxs-lookup"><span data-stu-id="f3daf-128">Publishing method</span></span></th>
<th align="left"><span data-ttu-id="f3daf-129">Cmdlet et exemple</span><span class="sxs-lookup"><span data-stu-id="f3daf-129">Cmdlet and example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3daf-130">Publication pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f3daf-130">Publishing to the user</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="f3daf-131">Cmdlet </strong> : Publisher-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-131">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="f3daf-132">Exemple </strong> : Publisher-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="f3daf-132">Example</strong>: Publish-AppvClientPackage “ContosoApplication”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3daf-133">Publication globale</span><span class="sxs-lookup"><span data-stu-id="f3daf-133">Publishing globally</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="f3daf-134">Cmdlet </strong> : Publisher-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-134">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="f3daf-135">Exemple </strong> : Publisher-AppvClientPackage "ContosoApplication"-Global</span><span class="sxs-lookup"><span data-stu-id="f3daf-135">Example</strong>: Publish-AppvClientPackage “ContosoApplication” -Global</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a><span data-ttu-id="f3daf-136">Pour publier un package pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f3daf-136">To publish a package to a specific user</span></span>


<span data-ttu-id="f3daf-137">**Remarques**  Pour utiliser ce paramètre, vous devez utiliser le correctif logiciel App-V 5,0 SP2 package 5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f3daf-137">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="f3daf-138">Un administrateur peut publier un package pour un utilisateur spécifique en spécifiant le paramètre facultatif **-UserSid** avec l’applet de la cmdlet **Publisher AppvClientPackage** , où **-UserSid** représente l’identificateur de sécurité (SID) de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="f3daf-138">An administrator can publish a package to a specific user by specifying the optional **–UserSID** parameter with the **Publish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="f3daf-139">Pour utiliser ce paramètre:</span><span class="sxs-lookup"><span data-stu-id="f3daf-139">To use this parameter:</span></span>

-   <span data-ttu-id="f3daf-140">Vous pouvez exécuter cette cmdlet à partir de la session utilisateur ou administrateur.</span><span class="sxs-lookup"><span data-stu-id="f3daf-140">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="f3daf-141">Vous devez être connecté avec des informations d’identification d’administrateur pour utiliser le paramètre.</span><span class="sxs-lookup"><span data-stu-id="f3daf-141">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="f3daf-142">L’utilisateur final doit être connecté.</span><span class="sxs-lookup"><span data-stu-id="f3daf-142">The end user must be logged in.</span></span>

-   <span data-ttu-id="f3daf-143">Vous devez indiquer l’identificateur de sécurité (SID) de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="f3daf-143">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="f3daf-144">**Cmdlet**: Publisher-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-144">**Cmdlet**: Publish-AppvClientPackage</span></span>

<span data-ttu-id="f3daf-145">**Exemple**: Publisher-AppvClientPackage "ContosoApplication"-UserSid S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="f3daf-145">**Example**: Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a><span data-ttu-id="f3daf-146">Pour ajouter et publier un package</span><span class="sxs-lookup"><span data-stu-id="f3daf-146">To add and publish a package</span></span>


<span data-ttu-id="f3daf-147">Utilisez les informations suivantes pour ajouter un package à un ordinateur et le publier à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3daf-147">Use the following information to add a package to a computer and publish it to the user.</span></span>

<span data-ttu-id="f3daf-148">**Applet**de passe: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-148">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="f3daf-149">**Exemple**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publisher-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-149">**Example**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | Publish-AppvClientPackage</span></span>

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a><span data-ttu-id="f3daf-150">Pour annuler la publication d’un package existant</span><span class="sxs-lookup"><span data-stu-id="f3daf-150">To unpublish an existing package</span></span>


<span data-ttu-id="f3daf-151">Utilisez les informations suivantes pour annuler la publication d’un package ayant été autorisé à un utilisateur, mais pas de supprimer le package de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3daf-151">Use the following information to unpublish a package which has been entitled to a user but not remove the package from the computer.</span></span>

<span data-ttu-id="f3daf-152">**Cmdlet**: UNPUBLISH-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-152">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="f3daf-153">**Exemple**: UNPUBLISH-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="f3daf-153">**Example**: Unpublish-AppvClientPackage “ContosoApplication”</span></span>

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a><span data-ttu-id="f3daf-154">Pour annuler la publication d’un package pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f3daf-154">To unpublish a package for a specific user</span></span>


<span data-ttu-id="f3daf-155">**Remarques**  Pour utiliser ce paramètre, vous devez utiliser le correctif logiciel App-V 5,0 SP2 package 5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f3daf-155">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="f3daf-156">Un administrateur peut annuler la publication d’un package pour un utilisateur spécifique à l’aide du paramètre facultatif **-UserSid** avec l’applet de passe **UNPUBLISH-AppvClientPackage** , où **-UserSid** représente l’identificateur de sécurité (SID) de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="f3daf-156">An administrator can unpublish a package for a specific user by using the optional **–UserSID** parameter with the **Unpublish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="f3daf-157">Pour utiliser ce paramètre:</span><span class="sxs-lookup"><span data-stu-id="f3daf-157">To use this parameter:</span></span>

-   <span data-ttu-id="f3daf-158">Vous pouvez exécuter cette cmdlet à partir de la session utilisateur ou administrateur.</span><span class="sxs-lookup"><span data-stu-id="f3daf-158">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="f3daf-159">Vous devez être connecté avec des informations d’identification d’administrateur pour utiliser le paramètre.</span><span class="sxs-lookup"><span data-stu-id="f3daf-159">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="f3daf-160">L’utilisateur final doit être connecté.</span><span class="sxs-lookup"><span data-stu-id="f3daf-160">The end user must be logged in.</span></span>

-   <span data-ttu-id="f3daf-161">Vous devez indiquer l’identificateur de sécurité (SID) de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="f3daf-161">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="f3daf-162">**Cmdlet**: UNPUBLISH-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-162">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="f3daf-163">**Exemple**: UNPUBLISH-AppvClientPackage "ContosoApplication"-UserSid S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="f3daf-163">**Example**: Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a><span data-ttu-id="f3daf-164">Pour supprimer un package existant</span><span class="sxs-lookup"><span data-stu-id="f3daf-164">To remove an existing package</span></span>


<span data-ttu-id="f3daf-165">Utilisez les informations suivantes pour supprimer un package de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3daf-165">Use the following information to remove a package from the computer.</span></span>

<span data-ttu-id="f3daf-166">**Applet**de passe: Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3daf-166">**Cmdlet**: Remove-AppvClientPackage</span></span>

<span data-ttu-id="f3daf-167">**Exemple**: Remove-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="f3daf-167">**Example**: Remove-AppvClientPackage “ContosoApplication”</span></span>

<span data-ttu-id="f3daf-168">**Remarques**  Les applets de cmdlets App-V ont été affectées à des variables pour les exemples précédents pour plus de clarté. le devoir n’est pas une obligation.</span><span class="sxs-lookup"><span data-stu-id="f3daf-168">**Note** App-V cmdlets have been assigned to variables for the previous examples for clarity only; assignment is not a requirement.</span></span> <span data-ttu-id="f3daf-169">La plupart des cmdlets peuvent être combinées comme affichées dans [pour ajouter et publier un package](#bkmk-add-pub-pkg-standalone-posh).</span><span class="sxs-lookup"><span data-stu-id="f3daf-169">Most cmdlets can be combined as displayed in [To add and publish a package](#bkmk-add-pub-pkg-standalone-posh).</span></span> <span data-ttu-id="f3daf-170">Pour un didacticiel détaillé, voir [App-V 5,0 client PowerShell Deep plongée](https://go.microsoft.com/fwlink/?LinkId=324466).</span><span class="sxs-lookup"><span data-stu-id="f3daf-170">For a detailed tutorial, see [App-V 5.0 Client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).</span></span>

 

## <a href="" id="bkmk-admins-pub-pkgs"></a><span data-ttu-id="f3daf-171">Pour permettre uniquement aux administrateurs de publier ou de retirer des packages</span><span class="sxs-lookup"><span data-stu-id="f3daf-171">To enable only administrators to publish or unpublish packages</span></span>


<span data-ttu-id="f3daf-172">**Remarques** 
 **Cette fonctionnalité est prise en charge à partir de l’App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="f3daf-172">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="f3daf-173">Utilisez l’applet de commande et le paramètre suivants pour permettre aux administrateurs (et non aux utilisateurs finaux) de publier ou d’annuler la publication des packages:</span><span class="sxs-lookup"><span data-stu-id="f3daf-173">Use the following cmdlet and parameter to enable only administrators (not end users) to publish or unpublish packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f3daf-174">Applet de commande</span><span class="sxs-lookup"><span data-stu-id="f3daf-174">Cmdlet</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f3daf-175">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3daf-175">Set-AppvClientConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f3daf-176">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f3daf-176">Parameter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f3daf-177">-RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="f3daf-177">-RequirePublishAsAdmin</span></span></p>
<p><span data-ttu-id="f3daf-178">Valeurs de paramètres:</span><span class="sxs-lookup"><span data-stu-id="f3daf-178">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f3daf-179">0-faux</span><span class="sxs-lookup"><span data-stu-id="f3daf-179">0 - False</span></span></p></li>
<li><p><span data-ttu-id="f3daf-180">1-vrai</span><span class="sxs-lookup"><span data-stu-id="f3daf-180">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="f3daf-181">Exemple: </strong> : Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="f3daf-181">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f3daf-182">Pour utiliser la console de gestion App-V pour définir cette configuration, reportez-vous à la rubrique [publication d’un package à l’aide de la console de gestion](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="f3daf-182">To use the App-V Management console to set this configuration, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

## <a href="" id="bkmk-understd-pend-pkgs"></a><span data-ttu-id="f3daf-183">Présentation des packages en attente (UserPending et GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="f3daf-183">Understanding pending packages (UserPending and GlobalPending)</span></span>


<span data-ttu-id="f3daf-184">**À partir de l’App-V 5,0 SP2**: Si vous exécutez une applet de cmdlet PowerShell affectant un package en cours d’utilisation, la tâche que vous essayez d’effectuer se trouve dans un état d’attente.</span><span class="sxs-lookup"><span data-stu-id="f3daf-184">**Starting in App-V 5.0 SP2**: If you run a PowerShell cmdlet that affects a package that is currently in use, the task that you are trying to perform is placed in a pending state.</span></span> <span data-ttu-id="f3daf-185">Par exemple, si vous tentez de publier un package alors qu’une application de ce package est utilisée, puis exécuté **Get-AppvClientPackage**, l’État en attente apparaît dans la sortie de l’applet de connexion comme suit:</span><span class="sxs-lookup"><span data-stu-id="f3daf-185">For example, if you try to publish a package when an application in that package is being used, and then run **Get-AppvClientPackage**, the pending status appears in the cmdlet output as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3daf-186">Élément de sortie de l’applet de vente</span><span class="sxs-lookup"><span data-stu-id="f3daf-186">Cmdlet output item</span></span></th>
<th align="left"><span data-ttu-id="f3daf-187">Description</span><span class="sxs-lookup"><span data-stu-id="f3daf-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3daf-188">UserPending</span><span class="sxs-lookup"><span data-stu-id="f3daf-188">UserPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3daf-189">Indique si une tâche en attente est appliquée au package dans la liste d’utilisateurs:</span><span class="sxs-lookup"><span data-stu-id="f3daf-189">Indicates whether the listed package has a pending task that is being applied to the user:</span></span></p>
<ul>
<li><p><span data-ttu-id="f3daf-190">Vrai</span><span class="sxs-lookup"><span data-stu-id="f3daf-190">True</span></span></p></li>
<li><p><span data-ttu-id="f3daf-191">Faux</span><span class="sxs-lookup"><span data-stu-id="f3daf-191">False</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3daf-192">GlobalPending</span><span class="sxs-lookup"><span data-stu-id="f3daf-192">GlobalPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3daf-193">Indique si une tâche en attente dans le package répertorié est appliquée globalement à l’ordinateur:</span><span class="sxs-lookup"><span data-stu-id="f3daf-193">Indicates whether the listed package has a pending task that is being applied globally to the computer:</span></span></p>
<ul>
<li><p><span data-ttu-id="f3daf-194">Vrai</span><span class="sxs-lookup"><span data-stu-id="f3daf-194">True</span></span></p></li>
<li><p><span data-ttu-id="f3daf-195">Faux</span><span class="sxs-lookup"><span data-stu-id="f3daf-195">False</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f3daf-196">La tâche en attente sera exécutée plus tard, conformément aux règles suivantes:</span><span class="sxs-lookup"><span data-stu-id="f3daf-196">The pending task will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3daf-197">Type de tâche</span><span class="sxs-lookup"><span data-stu-id="f3daf-197">Task type</span></span></th>
<th align="left"><span data-ttu-id="f3daf-198">Règle applicable</span><span class="sxs-lookup"><span data-stu-id="f3daf-198">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3daf-199">Tâche basée sur l’utilisateur (par exemple, publication d’un package pour un utilisateur);</span><span class="sxs-lookup"><span data-stu-id="f3daf-199">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3daf-200">La tâche en attente sera exécutée après que l’utilisateur se déconnecte, puis se reconnecte.</span><span class="sxs-lookup"><span data-stu-id="f3daf-200">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3daf-201">Une tâche basée sur le monde (par exemple, l’activation globale d’un groupe de connexions);</span><span class="sxs-lookup"><span data-stu-id="f3daf-201">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3daf-202">La tâche en attente sera effectuée lorsque l’ordinateur sera arrêté, puis redémarré.</span><span class="sxs-lookup"><span data-stu-id="f3daf-202">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f3daf-203">Pour plus d’informations sur les tâches en attente, voir [à propos de App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span><span class="sxs-lookup"><span data-stu-id="f3daf-203">For more information about pending tasks, see [About App-V 5.0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span></span>

<span data-ttu-id="f3daf-204">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="f3daf-204">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f3daf-205">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="f3daf-205">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f3daf-206">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="f3daf-206">Got an App-V issue?</span></span>** <span data-ttu-id="f3daf-207">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f3daf-207">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f3daf-208">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3daf-208">Related topics</span></span>


[<span data-ttu-id="f3daf-209">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="f3daf-209">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="f3daf-210">Administration d'App-V à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3daf-210">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 






---
title: Comment utiliser des packages facultatifs dans les groupes de connexion
description: Comment utiliser des packages facultatifs dans les groupes de connexion
author: dansimp
ms.assetid: 67666f18-b704-4852-a1e4-d13633bd2baf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ffa29f5d62e57a60423b2041cb71787d2c96bd66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805119"
---
# <span data-ttu-id="17beb-103">Comment utiliser des packages facultatifs dans les groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="17beb-103">How to Use Optional Packages in Connection Groups</span></span>


<span data-ttu-id="17beb-104">À partir de Microsoft Application Virtualization (App-V) 5,0 SP3, vous pouvez ajouter des packages facultatifs à vos groupes de connexion pour simplifier la gestion des groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="17beb-104">Starting in Microsoft Application Virtualization (App-V) 5.0 SP3, you can add optional packages to your connection groups to simplify connection group management.</span></span> <span data-ttu-id="17beb-105">Le tableau suivant récapitule les tâches que vous pouvez effectuer plus facilement à l’aide des packages facultatifs, ainsi que des liens vers des instructions pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="17beb-105">The following table summarizes the tasks that you can complete more easily by using optional packages, and provides links to instructions for each task.</span></span>

<span data-ttu-id="17beb-106">**Remarques** 
 **Les packages facultatifs ne sont pas pris en charge dans les versions antérieures à App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="17beb-106">**Note**
**Optional packages are not supported in releases prior to App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="17beb-107">Avant d’utiliser des packages facultatifs, voir [Configuration requise pour l’utilisation de packages facultatifs dans les groupes de connexion](#bkmk-reqs-using-cg).</span><span class="sxs-lookup"><span data-stu-id="17beb-107">Before using optional packages, see [Requirements for using optional packages in connection groups](#bkmk-reqs-using-cg).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17beb-108">Lien vers des instructions</span><span class="sxs-lookup"><span data-stu-id="17beb-108">Link to instructions</span></span></th>
<th align="left"><span data-ttu-id="17beb-109">Tâche</span><span class="sxs-lookup"><span data-stu-id="17beb-109">Task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)"><span data-ttu-id="17beb-110">Utiliser un groupe de connexions avec des packages facultatifs pour plusieurs utilisateurs disposant d’un paquet d’accès différent</span><span class="sxs-lookup"><span data-stu-id="17beb-110">Use one connection group, with optional packages, for multiple users who have different packages entitled to them</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="17beb-111">Utilisez un groupe de connexion unique pour rendre différents groupes d’applications et plug-ins disponibles pour différents utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="17beb-111">Use a single connection group to make different groups of applications and plug-ins available to different end users.</span></span></p>
<p><span data-ttu-id="17beb-112">Par exemple, vous souhaitez distribuer Microsoft Office à tous les utilisateurs finaux, mais distribuer différents plug-ins à différents sous-ensembles d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="17beb-112">For example, you want to distribute Microsoft Office to all end users, but distribute different plug-ins to different subsets of users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)"><span data-ttu-id="17beb-113">Annuler la publication ou la suppression d’un package facultatif, ou annuler la publication d’un package facultatif et le republier ultérieurement sans changer le groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="17beb-113">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="17beb-114">Annulez, supprimez ou republiez un package facultatif sans avoir à désactiver, supprimer, modifier, ajouter ou réactiver le groupe de connexion sur le client App-V.</span><span class="sxs-lookup"><span data-stu-id="17beb-114">Unpublish, delete, or republish an optional package without having to disable, remove, edit, add, and re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="17beb-115">Vous pouvez également annuler la publication du package facultatif et le republier ultérieurement sans avoir à désactiver ou republier le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="17beb-115">You can also unpublish the optional package and republish it later without having to disable or republish the connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a><span data-ttu-id="17beb-116">Utiliser un groupe de connexions avec des packages facultatifs pour plusieurs utilisateurs dotés d’un package différent</span><span class="sxs-lookup"><span data-stu-id="17beb-116">Use one connection group, with optional packages, for multiple users with different packages entitled to them</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17beb-117">Description de la tâche</span><span class="sxs-lookup"><span data-stu-id="17beb-117">Task description</span></span></th>
<th align="left"><span data-ttu-id="17beb-118">Exécution d’une tâche</span><span class="sxs-lookup"><span data-stu-id="17beb-118">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="17beb-119">Avec App-V 5,0 SP3 et App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="17beb-119">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="17beb-120">Vous pouvez ajouter des packages facultatifs aux groupes de connexion, ce qui vous permet de fournir différentes combinaisons d’applications et de plug-ins à différents utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="17beb-120">You can add optional packages to connection groups, which enables you to provide different combinations of applications and plug-ins to different end users.</span></span></p>
<p><strong><span data-ttu-id="17beb-121">Par exemple </strong> : vous souhaitez distribuer Microsoft Office à vos utilisateurs finaux, mais activer un certain plug-in pour seulement un sous-ensemble d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="17beb-121">Example</strong>: You want to distribute Microsoft Office to your end users, but enable a certain plug-in for only a subset of users.</span></span></p>
<p><span data-ttu-id="17beb-122">Pour ce faire, créez un groupe de connexion contenant un package avec Office, un autre package avec les plug-ins Office, puis rendez le package de plug-ins facultatif.</span><span class="sxs-lookup"><span data-stu-id="17beb-122">To do this, create a connection group that contains a package with Office, and another package with Office plug-ins, and then make the plug-ins package optional.</span></span></p>
<p><span data-ttu-id="17beb-123">Les utilisateurs finaux qui n’ont pas le droit d’accéder au package du plug-in pourront toujours exécuter Office.</span><span class="sxs-lookup"><span data-stu-id="17beb-123">End users who are not entitled to the plug-in package will still be able to run Office.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17beb-124">Méthode</span><span class="sxs-lookup"><span data-stu-id="17beb-124">Method</span></span></th>
<th align="left"><span data-ttu-id="17beb-125">Étapes</span><span class="sxs-lookup"><span data-stu-id="17beb-125">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17beb-126">App-V Server-console de gestion</span><span class="sxs-lookup"><span data-stu-id="17beb-126">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="17beb-127">Dans la console de gestion, sélectionnez <strong> groupes </strong> de connexion pour afficher la bibliothèque de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="17beb-127">In the Management Console, select <strong>CONNECTION GROUPS</strong> to display the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="17beb-128">Sélectionnez le groupe de connexion approprié dans la bibliothèque de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="17beb-128">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="17beb-129">Cliquez sur <strong> modifier </strong> dans le volet packages connectés.</span><span class="sxs-lookup"><span data-stu-id="17beb-129">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="17beb-130">Sélectionnez <strong> facultatif </strong> en regard du nom du package.</span><span class="sxs-lookup"><span data-stu-id="17beb-130">Select <strong>Optional</strong> next to the package name.</span></span></p></li>
<li><p><span data-ttu-id="17beb-131">Activez la case <strong> </strong> à cocher Ajouter l’accès du package aux accès au groupe.</span><span class="sxs-lookup"><span data-stu-id="17beb-131">Select the <strong>ADD PACKAGE ACCESS TO GROUP ACCESS</strong> check box.</span></span> <span data-ttu-id="17beb-132">Cette étape requise ajoute au groupe de connexions les habilitations du package que vous avez configurées précédemment lorsque vous avez affecté des packages aux groupes Active Directory.</span><span class="sxs-lookup"><span data-stu-id="17beb-132">This required step adds to the connection group the package entitlements that you configured earlier when you assigned packages to Active Directory groups.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17beb-133">App-V Server-cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="17beb-133">App-V Server - PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="17beb-134">Utilisez l’applet de commande suivante et spécifiez le <strong> paramètre-facultatif </strong> :</span><span class="sxs-lookup"><span data-stu-id="17beb-134">Use the following cmdlet, and specify the <strong>-Optional</strong> parameter:</span></span></p>
<p><strong><span data-ttu-id="17beb-135">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="17beb-135">Add-AppvServerConnectionGroupPackage</span></span></strong></p>
<p><strong><span data-ttu-id="17beb-136">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17beb-136">Syntax:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong><span data-ttu-id="17beb-137">Exemple :</span><span class="sxs-lookup"><span data-stu-id="17beb-137">Example:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17beb-138">Client App-V sur un ordinateur autonome</span><span class="sxs-lookup"><span data-stu-id="17beb-138">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="17beb-139">Créez le document XML de groupe de connexion et affectez <strong> </strong> à l’attribut <strong> d’indicateur de package IsOptional la </strong> <strong> valeur «true».</span><span class="sxs-lookup"><span data-stu-id="17beb-139">Create the connection group XML document, and set the <strong>Package</strong> tag attribute <strong>IsOptional</strong> to <strong>“true”.</span></span></strong></p></li>
<li><p><span data-ttu-id="17beb-140">Utilisez les applets de commande suivantes pour ajouter et activer le groupe de connexions:</span><span class="sxs-lookup"><span data-stu-id="17beb-140">Use the following cmdlets to add and enable the connection group:</span></span></p>
<ul>
<li><p><span data-ttu-id="17beb-141">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="17beb-141">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="17beb-142">Enable-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="17beb-142">Enable-AppvClientConnectionGroup</span></span></p></li>
</ul></li>
</ol>
<p><strong><span data-ttu-id="17beb-143">Exemple de document XML de groupe de connexion avec packages facultatifs:</span><span class="sxs-lookup"><span data-stu-id="17beb-143">Example connection group XML document with optional packages:</span></span></strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="17beb-144">Avec les versions antérieures à App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="17beb-144">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="17beb-145">Vous deviez créer de nombreux groupes de connexion pour rendre des applications spécifiques et des combinaisons de plug-ins accessibles à des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="17beb-145">You had to create many connection groups to make specific application and plug-in combinations available to specific users.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a><span data-ttu-id="17beb-146">Annuler la publication ou la suppression d’un package facultatif, ou annuler la publication d’un package facultatif et le republier ultérieurement sans changer le groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="17beb-146">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17beb-147">Description de la tâche</span><span class="sxs-lookup"><span data-stu-id="17beb-147">Task description</span></span></th>
<th align="left"><span data-ttu-id="17beb-148">Exécution d’une tâche</span><span class="sxs-lookup"><span data-stu-id="17beb-148">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="17beb-149">Avec App-V 5,0 SP3 et App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="17beb-149">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="17beb-150">Vous pouvez annuler la publication, la suppression ou la republication d’un package facultatif (qui se trouve dans un groupe de connexion) sans avoir à désactiver ou réactiver le groupe de connexion sur le client App-V.</span><span class="sxs-lookup"><span data-stu-id="17beb-150">You can unpublish, delete, or republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="17beb-151">Vous pouvez également annuler la publication d’un package facultatif et le republier ultérieurement sans avoir à désactiver ou republier le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="17beb-151">You can also unpublish an optional package and republish it later without having to disable or republish the connection group.</span></span></p>
<p><strong><span data-ttu-id="17beb-152">Exemple </strong> : Si vous publiez un package facultatif contenant un plug-in Microsoft Office et que vous souhaitez supprimer le plug-in, vous pouvez annuler la publication du package sans avoir à désactiver le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="17beb-152">Example</strong>: If you publish an optional package that contains a Microsoft Office plug-in, and you want to remove the plug-in, you can unpublish the package without having to disable the connection group.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17beb-153">Méthode</span><span class="sxs-lookup"><span data-stu-id="17beb-153">Method</span></span></th>
<th align="left"><span data-ttu-id="17beb-154">Étapes</span><span class="sxs-lookup"><span data-stu-id="17beb-154">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17beb-155">App-V Server-console de gestion</span><span class="sxs-lookup"><span data-stu-id="17beb-155">App-V Server – Management Console</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="17beb-156">Pour annuler la publication du package: dans la console de gestion, sélectionnez électionnez la <strong> </strong> page Packages, cliquez ou cliquez avec le bouton droit sur le package dont vous voulez annuler la publication, puis cliquez sur <strong> annuler la publication </strong> .</span><span class="sxs-lookup"><span data-stu-id="17beb-156">To unpublish the package: In the Management Console, select elect the <strong>PACKAGES</strong> page, click or right-click the package that you want to unpublish, and click <strong>Unpublish</strong>.</span></span></p></li>
<li><p><span data-ttu-id="17beb-157">Pour supprimer un package facultatif d’un groupe de connexions: sur la <strong> page groupes de connexions </strong> , sélectionnez le package que vous voulez supprimer, puis cliquez sur la flèche droite pour supprimer le package du volet groupe de connexions en bas à gauche.</span><span class="sxs-lookup"><span data-stu-id="17beb-157">To remove an optional package from a connection group: On the <strong>CONNECTION GROUPS</strong> page, select the package that you want to remove, and click the right arrow to remove the package from the connection group pane on the bottom left.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17beb-158">Client App-V sur un ordinateur autonome</span><span class="sxs-lookup"><span data-stu-id="17beb-158">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="17beb-159">Utilisez les applets de commande existantes suivantes:</span><span class="sxs-lookup"><span data-stu-id="17beb-159">Use the following existing cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="17beb-160">Annuler la publication-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="17beb-160">Unpublish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="17beb-161">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="17beb-161">Remove-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="17beb-162">Pour plus d’informations, reportez-vous <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> à comment gérer les packages App-V 5,1 exécutés sur un ordinateur autonome à l’aide de PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="17beb-162">For more information, see <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="17beb-163">Avec les versions antérieures à App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="17beb-163">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="17beb-164">Vous deviez:</span><span class="sxs-lookup"><span data-stu-id="17beb-164">You had to:</span></span></p>
<ol>
<li><p><span data-ttu-id="17beb-165">Supprimez le groupe de connexions de chaque ordinateur client App-V sur lequel il a été activé.</span><span class="sxs-lookup"><span data-stu-id="17beb-165">Remove the connection group from each App-V Client computer where it was enabled.</span></span></p></li>
<li><p><span data-ttu-id="17beb-166">Annulez la publication du package.</span><span class="sxs-lookup"><span data-stu-id="17beb-166">Unpublish the package.</span></span></p></li>
<li><p><span data-ttu-id="17beb-167">Supprimez le package de la définition du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="17beb-167">Remove the package from the connection group’s definition.</span></span></p></li>
<li><p><span data-ttu-id="17beb-168">Republiez le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="17beb-168">Republish the connection group.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a><span data-ttu-id="17beb-169">Configuration requise pour l’utilisation de packages facultatifs dans les groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="17beb-169">Requirements for using optional packages in connection groups</span></span>


<span data-ttu-id="17beb-170">Avant d’utiliser les packages facultatifs dans les groupes de connexion, consultez la configuration requise suivante:</span><span class="sxs-lookup"><span data-stu-id="17beb-170">Review the following requirements before using optional packages in connection groups:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="17beb-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17beb-171">Requirement</span></span></th>
<th align="left"><span data-ttu-id="17beb-172">Détails</span><span class="sxs-lookup"><span data-stu-id="17beb-172">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17beb-173">Les groupes de connexions doivent contenir au moins un package non facultatif.</span><span class="sxs-lookup"><span data-stu-id="17beb-173">Connection groups must contain at least one non-optional package.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="17beb-174">Vérifiez que vous respectez cette exigence, car le serveur App-V et la cmdlet PowerShell ne vérifient pas que l’exigence a été satisfaite.</span><span class="sxs-lookup"><span data-stu-id="17beb-174">Check carefully that you meet this requirement, as the App-V Server and the PowerShell cmdlet don’t validate that the requirement has been met.</span></span></p></li>
<li><p><span data-ttu-id="17beb-175">Si vous créez par erreur un groupe de connexions qui ne contient pas au moins un package non facultatif, et que l’utilisateur final tente d’ouvrir une application empaquetée dans ce groupe de connexion, le groupe de connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="17beb-175">If you accidentally create a connection group that does not contain at least one non-optional package, and the end user tries to open a packaged application in that connection group, the connection group will fail.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="17beb-176">Les groupes de connexion publiés par l’utilisateur peuvent contenir des packages publiés globalement ou pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17beb-176">User-published connection groups can contain packages that are published globally or to the user.</span></span></p></li>
<li><p><span data-ttu-id="17beb-177">Les groupes de connexion à publication globale doivent contenir uniquement des packages publiés globalement.</span><span class="sxs-lookup"><span data-stu-id="17beb-177">Globally published connection groups must contain only globally published packages.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="17beb-178">Les groupes de connexions à publication globale doivent contenir des packages publiés globalement pour s’assurer que les packages seront disponibles lors du démarrage de l’environnement virtuel du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="17beb-178">Globally published connection groups must contain packages that are published globally to ensure that the packages will be available when starting the connection group’s virtual environment.</span></span></p>
<p><span data-ttu-id="17beb-179">Si vous tentez d’ajouter ou de désactiver des groupes de connexions à publication globale qui contiennent des packages publiés par l’utilisateur, le groupe de connexion échouera.</span><span class="sxs-lookup"><span data-stu-id="17beb-179">If you try to add or enable globally published connection groups that contain user-published packages, the connection group will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="17beb-180">Vous devez publier tous les packages non facultatifs avant de publier le groupe de connexion contenant ces packages.</span><span class="sxs-lookup"><span data-stu-id="17beb-180">You must publish all non-optional packages before publishing the connection group that contains those packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="17beb-181">L’environnement virtuel d’un groupe de connexions ne peut pas démarrer si des packages non facultatifs sont manquants.</span><span class="sxs-lookup"><span data-stu-id="17beb-181">A connection group’s virtual environment cannot start if any non-optional packages are missing.</span></span></p>
<p><span data-ttu-id="17beb-182">Le client App-V ne peut pas ajouter ou activer un groupe de connexion si des packages non facultatifs n’ont pas été publiés.</span><span class="sxs-lookup"><span data-stu-id="17beb-182">The App-V Client fails to add or enable a connection group if any non-optional packages have not been published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="17beb-183">Avant d’annuler la publication d’un package publié globalement, assurez-vous que les groupes de connexion qui sont habilités à tous les utilisateurs de cet ordinateur ne nécessitent plus le package.</span><span class="sxs-lookup"><span data-stu-id="17beb-183">Before you unpublish a globally published package, ensure that the connection groups that are entitled to all the users on that computer no longer require the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="17beb-184">Le système ne vérifie pas si le package fait partie du groupe de connexion d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17beb-184">The system does not check whether the package is part of another user’s connection group.</span></span> <span data-ttu-id="17beb-185">L’annulation de la publication d’un package global le rendra indisponible pour tous les utilisateurs de cet ordinateur, assurez-vous que les groupes de connexion de chaque utilisateur ne contiennent plus le package, ou le package facultatif.</span><span class="sxs-lookup"><span data-stu-id="17beb-185">Unpublishing a global package will make it unavailable to every user on that computer, so make sure that each user’s connection groups no longer contain the package, or alternatively make the package optional.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="17beb-186">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17beb-186">Related topics</span></span>


[<span data-ttu-id="17beb-187">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="17beb-187">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 






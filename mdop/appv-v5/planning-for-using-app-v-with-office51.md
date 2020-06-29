---
title: Planification de l'utilisation d'App-V avec Office
description: Planification de l'utilisation d'App-V avec Office
author: dansimp
ms.assetid: e7a19b43-1746-469f-bad6-8e75cf4b3f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/16/2017
ms.openlocfilehash: ae225db3c47faca5fba790fb9963bfd4dc2c66b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804957"
---
# <span data-ttu-id="df6e8-103">Planification de l'utilisation d'App-V avec Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="df6e8-104">Utilisez les informations suivantes pour planifier le déploiement d’Office à l’aide de Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="df6e8-104">Use the following information to plan how to deploy Office by using Microsoft Application Virtualization (App-V) 5.1.</span></span> <span data-ttu-id="df6e8-105">Cet article inclut les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="df6e8-105">This article includes:</span></span>

-   [<span data-ttu-id="df6e8-106">Prise en charge de App-V pour les modules linguistiques</span><span class="sxs-lookup"><span data-stu-id="df6e8-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="df6e8-107">Versions prises en charge de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="df6e8-108">Planification de l’utilisation de App-V avec les versions coexistantes d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="df6e8-109">Intégration d’Office à Windows lorsque vous déployez utiliser App-V pour déployer Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="df6e8-110">Prise en charge de App-V pour les modules linguistiques</span><span class="sxs-lookup"><span data-stu-id="df6e8-110">App-V support for Language Packs</span></span>


<span data-ttu-id="df6e8-111">Vous pouvez utiliser le Sequencer App-V 5,1 pour créer des packages de plug-in pour les modules linguistiques, les packs linguistiques LIP, les outils de vérification linguistique et les langues d’info-bulles.</span><span class="sxs-lookup"><span data-stu-id="df6e8-111">You can use the App-V 5.1 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="df6e8-112">Vous pouvez ensuite inclure les packages de plug-in dans un groupe de connexion, ainsi que le package 2013 Office que vous créez à l’aide du kit de développement logiciel de déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="df6e8-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="df6e8-113">Les applications Office et les modules linguistiques enfichables interagissent en toute transparence dans le même groupe de connexion, de la même manière que sur les autres packages regroupés dans un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="df6e8-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

><span data-ttu-id="df6e8-114">**Remarques**  Microsoft Visio et Microsoft Project ne prennent pas en charge le module linguistique thaï.</span><span class="sxs-lookup"><span data-stu-id="df6e8-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="df6e8-115">Versions prises en charge de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-115">Supported versions of Microsoft Office</span></span>

<span data-ttu-id="df6e8-116">Voir [ID de produit Microsoft Office prises en charge par l’application-V](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) pour obtenir la liste des produits Office pris en charge.</span><span class="sxs-lookup"><span data-stu-id="df6e8-116">See [Microsoft Office Product IDs that App-V supports](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) for a list of supported Office products.</span></span>
><span data-ttu-id="df6e8-117">**Note** &nbsp; Remarques &nbsp; Vous devez utiliser l’outil déploiement d’Office pour créer des packages App-V pour les applications Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="df6e8-117">**Note**&nbsp;&nbsp;You must use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="df6e8-118">La création de packages pour les versions avec licence en volume d’Office professionnel plus ou d’Office standard n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df6e8-118">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span> <span data-ttu-id="df6e8-119">Vous ne pouvez pas utiliser le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="df6e8-119">You cannot use the App-V Sequencer.</span></span>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="df6e8-120">Planification de l’utilisation de App-V avec les versions coexistantes d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-120">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="df6e8-121">Vous pouvez installer plusieurs versions de Microsoft Office côte à côte sur le même ordinateur en utilisant «coexistence Microsoft Office».</span><span class="sxs-lookup"><span data-stu-id="df6e8-121">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="df6e8-122">Vous pouvez implémenter la coexistence d’Office à l’aide de combinaisons de toutes les principales versions d’Office et de méthodes d’installation, le cas échéant, à l’aide de la version Windows Installer (MSi) d’Office, d’Office «démarrer en un clic» et d’App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="df6e8-122">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.1.</span></span> <span data-ttu-id="df6e8-123">Toutefois, l’utilisation de la coexistence Office n’est pas recommandée par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="df6e8-123">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="df6e8-124">Pour éviter les problèmes de compatibilité, nous vous conseillons de ne pas avoir de coexistence d’Office.</span><span class="sxs-lookup"><span data-stu-id="df6e8-124">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="df6e8-125">Toutefois, lorsque vous effectuez une migration vers une version plus récente d’Office, des problèmes peuvent entraîner des problèmes qui ne peuvent pas être résolus, de sorte que vous pouvez implémenter une coexistence temporaire pour faciliter la migration vers la dernière version du produit.</span><span class="sxs-lookup"><span data-stu-id="df6e8-125">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="df6e8-126">L’utilisation de la coexistence Office sur une base longue n’est jamais recommandée, et votre organisation doit être disposant d’un forfait pour une transition complète immédiate.</span><span class="sxs-lookup"><span data-stu-id="df6e8-126">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="df6e8-127">Avant de mettre en œuvre la coexistence d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-127">Before you implement Office coexistence</span></span>

<span data-ttu-id="df6e8-128">Avant d’implémenter la coexistence d’Office, consultez la documentation Office suivante.</span><span class="sxs-lookup"><span data-stu-id="df6e8-128">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="df6e8-129">Choisissez l’article qui correspond à la version la plus récente d’Office pour laquelle vous envisagez d’implémenter une coexistence.</span><span class="sxs-lookup"><span data-stu-id="df6e8-129">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="df6e8-130">Version d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-130">Office version</span></span></th>
<th align="left"><span data-ttu-id="df6e8-131">Lien vers des conseils</span><span class="sxs-lookup"><span data-stu-id="df6e8-131">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-132">Office 2013</span><span class="sxs-lookup"><span data-stu-id="df6e8-132">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="df6e8-133">Informations sur l’utilisation des suites et programmes Office 2013 (déploiement MSI) sur un ordinateur exécutant une autre version d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-133">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-134">Office 2010</span><span class="sxs-lookup"><span data-stu-id="df6e8-134">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="df6e8-135">Informations sur l’utilisation des suites et des programmes Office 2010 sur un ordinateur exécutant une autre version d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-135">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="df6e8-136">La documentation Office fournit des instructions détaillées sur la coexistence pour les installations d’Office basées sur Windows Installer (MSi) et démarrer en un clic.</span><span class="sxs-lookup"><span data-stu-id="df6e8-136">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="df6e8-137">Ce sujet App-V sur la coexistence complète les recommandations d’Office avec des informations plus spécifiques aux déploiements d’application-V.</span><span class="sxs-lookup"><span data-stu-id="df6e8-137">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="df6e8-138">Scénarios de coexistence pour Office pris en charge</span><span class="sxs-lookup"><span data-stu-id="df6e8-138">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="df6e8-139">Les tableaux suivants résument les scénarios de coexistence pris en charge.</span><span class="sxs-lookup"><span data-stu-id="df6e8-139">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="df6e8-140">Celles-ci sont organisées en fonction de la version et de la méthode de déploiement que vous démarrez avec et de la version et de la méthode de déploiement vers laquelle vous effectuez la migration.</span><span class="sxs-lookup"><span data-stu-id="df6e8-140">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="df6e8-141">Veillez à tester complètement toutes les solutions de coexistence avant de les déployer auprès d’un public de production.</span><span class="sxs-lookup"><span data-stu-id="df6e8-141">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

><span data-ttu-id="df6e8-142">**Remarques**  Microsoft ne prend pas en charge l’utilisation de plusieurs versions d’Office dans les environnements Windows Server pour lesquels le service de rôle hôte de session Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="df6e8-142">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="df6e8-143">Pour exécuter des scénarios de coexistence Office, vous devez désactiver ce service de rôle.</span><span class="sxs-lookup"><span data-stu-id="df6e8-143">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="df6e8-144">Intégrations Windows & coexistence d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-144">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="df6e8-145">Les méthodes d’installation de Windows Installer et d’Office «démarrer en un clic» s’intègrent à certains points du système d’exploitation Windows sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="df6e8-145">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="df6e8-146">Lorsque vous utilisez la coexistence, les intégrations de système d’exploitation courantes entre deux versions d’Office peuvent entrer en conflit et provoquer des problèmes de compatibilité et d’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="df6e8-146">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="df6e8-147">Avec App-V, vous pouvez effectuer une séquence de certaines versions d’Office afin d’exclure les intégrations, ce qui a pour effet d’isoler celles-ci du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="df6e8-147">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="df6e8-148">Mode dans lequel App-V peut séquencer cette version d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-148">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-149">Office 2007</span><span class="sxs-lookup"><span data-stu-id="df6e8-149">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-150">Toujours non intégré.</span><span class="sxs-lookup"><span data-stu-id="df6e8-150">Always non-integrated.</span></span> <span data-ttu-id="df6e8-151">App-V n’offre aucune intégration du système d’exploitation à une version virtualisée d’Office 2007.</span><span class="sxs-lookup"><span data-stu-id="df6e8-151">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-152">Office 2010</span><span class="sxs-lookup"><span data-stu-id="df6e8-152">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-153">Modes intégrés et non intégrés.</span><span class="sxs-lookup"><span data-stu-id="df6e8-153">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-154">Office 2013</span><span class="sxs-lookup"><span data-stu-id="df6e8-154">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-155">Toujours intégré.</span><span class="sxs-lookup"><span data-stu-id="df6e8-155">Always integrated.</span></span> <span data-ttu-id="df6e8-156">Les intégrations du système d’exploitation Windows ne peuvent pas être désactivées.</span><span class="sxs-lookup"><span data-stu-id="df6e8-156">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="df6e8-157">Microsoft vous recommande de déployer la coexistence d’Office avec une seule instance Office intégrée.</span><span class="sxs-lookup"><span data-stu-id="df6e8-157">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="df6e8-158">Par exemple, si vous utilisez App-V pour déployer Office 2010 et Office 2013, vous devez effectuer une séquence d’Office 2010 en mode non intégré.</span><span class="sxs-lookup"><span data-stu-id="df6e8-158">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="df6e8-159">Pour plus d’informations sur le séquençage d’Office dans le mode non-intégration (isolé), voir [Comment séquencé Microsoft Office 2010 dans Microsoft application virtualization 5,0](https://support.microsoft.com/kb/2830069).</span><span class="sxs-lookup"><span data-stu-id="df6e8-159">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="df6e8-160">Limitations connues des scénarios de coexistence d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-160">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="df6e8-161">Les sections suivantes décrivent certains problèmes que vous pouvez rencontrer lors de l’utilisation de App-V pour implémenter la coexistence avec Office.</span><span class="sxs-lookup"><span data-stu-id="df6e8-161">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="df6e8-162">Limitations communes aux scénarios de coexistence pour Windows Installer et démarrer en un clic et App-V pour Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-162">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="df6e8-163">Les limitations suivantes peuvent se produire lorsque vous installez les versions suivantes d’Office sur le même ordinateur:</span><span class="sxs-lookup"><span data-stu-id="df6e8-163">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="df6e8-164">Office 2010 à l’aide de la version Windows Installer</span><span class="sxs-lookup"><span data-stu-id="df6e8-164">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="df6e8-165">Office 2013 à l’aide de App-V</span><span class="sxs-lookup"><span data-stu-id="df6e8-165">Office 2013 by using App-V</span></span>

<span data-ttu-id="df6e8-166">Après avoir publié Office 2013 en utilisant App-V côte à côte avec une version antérieure de la version d’Office 2010 basée sur Windows Installer, il est possible que le programme d’installation Windows démarre.</span><span class="sxs-lookup"><span data-stu-id="df6e8-166">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="df6e8-167">En effet, la version Windows Installer ou «démarrer en un clic» d’Office 2010 tente de s’inscrire automatiquement à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="df6e8-167">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="df6e8-168">Pour ignorer l’opération d’inscription automatique pour Word 2010 natif, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="df6e8-168">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="df6e8-169">Quittez Word 2010.</span><span class="sxs-lookup"><span data-stu-id="df6e8-169">Exit Word 2010.</span></span>

2.  <span data-ttu-id="df6e8-170">Démarrez l’éditeur du registre en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="df6e8-170">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="df6e8-171">Dans Windows 7: cliquez sur **Démarrer**, tapez **regedit** dans la zone démarrer la recherche, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="df6e8-171">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="df6e8-172">Dans Windows 8,1 ou Windows 10, tapez **regedit** , puis appuyez sur entrée dans la page de démarrage, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="df6e8-172">In Windows 8.1 or Windows 10, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="df6e8-173">Si vous êtes invité à entrer un mot de passe d’administrateur ou une confirmation, tapez le mot de passe ou cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="df6e8-173">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="df6e8-174">Recherchez et sélectionnez la sous-clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="df6e8-174">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="df6e8-175">Dans le menu **édition** , cliquez sur **nouveau**, puis cliquez sur **valeur DWORD**.</span><span class="sxs-lookup"><span data-stu-id="df6e8-175">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="df6e8-176">Tapez **NoReReg**, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="df6e8-176">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="df6e8-177">Cliquez avec le bouton droit sur **NoReReg** , puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="df6e8-177">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="df6e8-178">Dans la zone **ValueData** , tapez **1**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="df6e8-178">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="df6e8-179">Dans le menu fichier, cliquez sur **quitter** pour fermer l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="df6e8-179">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="df6e8-180">Intégration d’Office à Windows lors de l’utilisation de App-V pour le déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-180">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="df6e8-181">Lorsque vous déployez Office 2013 à l’aide de App-V, Office est totalement intégré au système d’exploitation, qui fournit aux utilisateurs finaux les mêmes fonctionnalités qu’Office lorsque celui-ci est déployé sans App-V.</span><span class="sxs-lookup"><span data-stu-id="df6e8-181">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="df6e8-182">Le package App-V pour Office 2013 prend en charge les points d’intégration suivants avec le système d’exploitation Windows:</span><span class="sxs-lookup"><span data-stu-id="df6e8-182">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="df6e8-183">Point d’extension</span><span class="sxs-lookup"><span data-stu-id="df6e8-183">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="df6e8-184">Description</span><span class="sxs-lookup"><span data-stu-id="df6e8-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-185">Plug-in Lync Meeting join pour Firefox et chrome</span><span class="sxs-lookup"><span data-stu-id="df6e8-185">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-186">Les utilisateurs peuvent participer à des réunions Lync depuis Firefox et chrome</span><span class="sxs-lookup"><span data-stu-id="df6e8-186">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-187">Envoyés vers le pilote d’impression OneNote</span><span class="sxs-lookup"><span data-stu-id="df6e8-187">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-188">L’utilisateur peut imprimer dans OneNote</span><span class="sxs-lookup"><span data-stu-id="df6e8-188">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-189">Notes liées OneNote</span><span class="sxs-lookup"><span data-stu-id="df6e8-189">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-190">Notes liées OneNote</span><span class="sxs-lookup"><span data-stu-id="df6e8-190">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-191">Envoyer vers le complément OneNote sur le Web Explorer</span><span class="sxs-lookup"><span data-stu-id="df6e8-191">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-192">L’utilisateur peut envoyer à OneNote à partir d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="df6e8-192">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-193">Exception de pare-feu pour Lync et Outlook</span><span class="sxs-lookup"><span data-stu-id="df6e8-193">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-194">Exception de pare-feu pour Lync et Outlook</span><span class="sxs-lookup"><span data-stu-id="df6e8-194">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-195">Client MAPI</span><span class="sxs-lookup"><span data-stu-id="df6e8-195">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-196">Les applications et les compléments natifs peuvent interagir avec les applications virtuelles Outlook via MAPI</span><span class="sxs-lookup"><span data-stu-id="df6e8-196">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-197">Plug-in SharePoint pour Firefox</span><span class="sxs-lookup"><span data-stu-id="df6e8-197">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-198">Les utilisateurs peuvent utiliser les fonctionnalités SharePoint dans Firefox</span><span class="sxs-lookup"><span data-stu-id="df6e8-198">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-199">Applet panneau de configuration de la messagerie</span><span class="sxs-lookup"><span data-stu-id="df6e8-199">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-200">L’utilisateur obtient l’applet panneau de configuration de la messagerie dans Outlook</span><span class="sxs-lookup"><span data-stu-id="df6e8-200">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-201">Assemblys d’interopérabilité principaux</span><span class="sxs-lookup"><span data-stu-id="df6e8-201">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-202">Compléments gérés par le support</span><span class="sxs-lookup"><span data-stu-id="df6e8-202">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-203">Gestionnaire de cache de documents Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-203">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-204">Autorise le cache de documents pour les applications Office</span><span class="sxs-lookup"><span data-stu-id="df6e8-204">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-205">Gestionnaire de recherche du protocole Outlook</span><span class="sxs-lookup"><span data-stu-id="df6e8-205">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-206">L’utilisateur peut effectuer une recherche dans Outlook</span><span class="sxs-lookup"><span data-stu-id="df6e8-206">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-207">Contrôles Active X:</span><span class="sxs-lookup"><span data-stu-id="df6e8-207">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-208">Pour plus d’informations sur les contrôles ActiveX, voir informations de référence sur les <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de contrôles ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="df6e8-208">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="df6e8-209">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="df6e8-209">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-210">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-210">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="df6e8-211">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="df6e8-211">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-212">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-212">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="df6e8-213">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="df6e8-213">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-214">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-214">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="df6e8-215">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="df6e8-215">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-216">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-216">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="df6e8-217">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="df6e8-217">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-218">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-218">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="df6e8-219">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="df6e8-219">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-220">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-220">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="df6e8-221">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="df6e8-221">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-222">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-222">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="df6e8-223">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="df6e8-223">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-224">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-224">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="df6e8-225">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="df6e8-225">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-226">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-226">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="df6e8-227">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="df6e8-227">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-228">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-228">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="df6e8-229">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="df6e8-229">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-230">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-230">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="df6e8-231">Nom. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="df6e8-231">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-232">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-232">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="df6e8-233">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="df6e8-233">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-234">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-234">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="df6e8-235">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="df6e8-235">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-236">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-236">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="df6e8-237">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="df6e8-237">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-238">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="df6e8-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="df6e8-239">Programme d’assistance du navigateur OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="df6e8-239">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-240">Contrôle ActiveX</span><span class="sxs-lookup"><span data-stu-id="df6e8-240">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-241">Superpositions d’icônes OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="df6e8-241">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="df6e8-242">Icônes de l’interface utilisateur de l’Explorateur Windows lorsque les utilisateurs regardent les dossiers OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="df6e8-242">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-243">Extensions d'environnement</span><span class="sxs-lookup"><span data-stu-id="df6e8-243">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df6e8-244">Associés</span><span class="sxs-lookup"><span data-stu-id="df6e8-244">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df6e8-245">Windows Search</span><span class="sxs-lookup"><span data-stu-id="df6e8-245">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 






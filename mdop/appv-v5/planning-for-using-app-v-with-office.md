---
title: Planification de l'utilisation d'App-V avec Office
description: Planification de l'utilisation d'App-V avec Office
author: dansimp
ms.assetid: c4371869-4bfc-4d13-9198-ef19f99fc192
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff523c8f8827e295c8fb9a2d9fd0e02d5b019aa8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804968"
---
# <span data-ttu-id="c6301-103">Planification de l'utilisation d'App-V avec Office</span><span class="sxs-lookup"><span data-stu-id="c6301-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="c6301-104">Utilisez les informations suivantes pour planifier le déploiement d’Office à l’aide de App-V.</span><span class="sxs-lookup"><span data-stu-id="c6301-104">Use the following information to plan how to deploy Office by using App-V.</span></span> <span data-ttu-id="c6301-105">Cet article inclut les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="c6301-105">This article includes:</span></span>

-   [<span data-ttu-id="c6301-106">Prise en charge de App-V pour les modules linguistiques</span><span class="sxs-lookup"><span data-stu-id="c6301-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="c6301-107">Versions prises en charge de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="c6301-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="c6301-108">Planification de l’utilisation de App-V avec les versions coexistantes d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="c6301-109">Intégration d’Office à Windows lorsque vous déployez utiliser App-V pour déployer Office</span><span class="sxs-lookup"><span data-stu-id="c6301-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="c6301-110">Prise en charge de App-V pour les modules linguistiques</span><span class="sxs-lookup"><span data-stu-id="c6301-110">App-V support for Language Packs</span></span>


<span data-ttu-id="c6301-111">Vous pouvez utiliser le Sequencer App-V 5,0 pour créer des packages de plug-in pour les modules linguistiques, les packs linguistiques LIP, les outils de vérification linguistique et les langues d’info-bulles.</span><span class="sxs-lookup"><span data-stu-id="c6301-111">You can use the App-V 5.0 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="c6301-112">Vous pouvez ensuite inclure les packages de plug-in dans un groupe de connexion, ainsi que le package 2013 Office que vous créez à l’aide du kit de développement logiciel de déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="c6301-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="c6301-113">Les applications Office et les modules linguistiques enfichables interagissent en toute transparence dans le même groupe de connexion, de la même manière que sur les autres packages regroupés dans un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="c6301-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

<span data-ttu-id="c6301-114">**Remarques**  Microsoft Visio et Microsoft Project ne prennent pas en charge le module linguistique thaï.</span><span class="sxs-lookup"><span data-stu-id="c6301-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="c6301-115">Versions prises en charge de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="c6301-115">Supported versions of Microsoft Office</span></span>


<span data-ttu-id="c6301-116">Le tableau suivant répertorie les versions de Microsoft Office prises en charge par App-V, les méthodes de création de packages Office, les licences prises en charge et les déploiements pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c6301-116">The following table lists the versions of Microsoft Office that App-V supports, methods of Office package creation, supported licensing, and supported deployments.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6301-117">Version d’Office prise en charge</span><span class="sxs-lookup"><span data-stu-id="c6301-117">Supported Office Version</span></span></th>
<th align="left"><span data-ttu-id="c6301-118">Versions d’App-V prises en charge</span><span class="sxs-lookup"><span data-stu-id="c6301-118">Supported App-V Versions</span></span></th>
<th align="left"><span data-ttu-id="c6301-119">Création de package</span><span class="sxs-lookup"><span data-stu-id="c6301-119">Package Creation</span></span></th>
<th align="left"><span data-ttu-id="c6301-120">Licences prises en charge</span><span class="sxs-lookup"><span data-stu-id="c6301-120">Supported Licensing</span></span></th>
<th align="left"><span data-ttu-id="c6301-121">Déploiements pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6301-121">Supported Deployments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-122">Applications 365 Microsoft pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="c6301-122">Microsoft 365 Apps for enterprise</span></span></p>
<p><span data-ttu-id="c6301-123">Également pris en charge:</span><span class="sxs-lookup"><span data-stu-id="c6301-123">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="c6301-124">Visio Pro pour Office 365</span><span class="sxs-lookup"><span data-stu-id="c6301-124">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="c6301-125">Project Pro pour Office 365</span><span class="sxs-lookup"><span data-stu-id="c6301-125">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c6301-126">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c6301-126">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="c6301-127">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c6301-127">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="c6301-128">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="c6301-128">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="c6301-129">Outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-129">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-130">Abonnement</span><span class="sxs-lookup"><span data-stu-id="c6301-130">Subscription</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c6301-131">Bureau</span><span class="sxs-lookup"><span data-stu-id="c6301-131">Desktop</span></span></p></li>
<li><p><span data-ttu-id="c6301-132">VDI personnel</span><span class="sxs-lookup"><span data-stu-id="c6301-132">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="c6301-133">Infrastructure VDI en pool</span><span class="sxs-lookup"><span data-stu-id="c6301-133">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="c6301-134">RDS</span><span class="sxs-lookup"><span data-stu-id="c6301-134">RDS</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-135">Office professionnel plus 2013</span><span class="sxs-lookup"><span data-stu-id="c6301-135">Office Professional Plus 2013</span></span></p>
<p><span data-ttu-id="c6301-136">Également pris en charge:</span><span class="sxs-lookup"><span data-stu-id="c6301-136">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="c6301-137">Visio professionnel 2013</span><span class="sxs-lookup"><span data-stu-id="c6301-137">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="c6301-138">Project Professionnel 2013</span><span class="sxs-lookup"><span data-stu-id="c6301-138">Project Professional 2013</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c6301-139">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c6301-139">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="c6301-140">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c6301-140">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="c6301-141">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="c6301-141">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="c6301-142">Outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-142">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-143">Gestion des licences en volume</span><span class="sxs-lookup"><span data-stu-id="c6301-143">Volume Licensing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c6301-144">Bureau</span><span class="sxs-lookup"><span data-stu-id="c6301-144">Desktop</span></span></p></li>
<li><p><span data-ttu-id="c6301-145">VDI personnel</span><span class="sxs-lookup"><span data-stu-id="c6301-145">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="c6301-146">Infrastructure VDI en pool</span><span class="sxs-lookup"><span data-stu-id="c6301-146">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="c6301-147">RDS</span><span class="sxs-lookup"><span data-stu-id="c6301-147">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="c6301-148">Planification de l’utilisation de App-V avec les versions coexistantes d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-148">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="c6301-149">Vous pouvez installer plusieurs versions de Microsoft Office côte à côte sur le même ordinateur en utilisant «coexistence Microsoft Office».</span><span class="sxs-lookup"><span data-stu-id="c6301-149">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="c6301-150">Vous pouvez implémenter la coexistence d’Office à l’aide de combinaisons de toutes les versions principales d’Office et des méthodes d’installation, le cas échéant, à l’aide de la version Windows Installer (MSi) d’Office, démarrer en un clic et App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="c6301-150">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.0 SP2.</span></span> <span data-ttu-id="c6301-151">Toutefois, l’utilisation de la coexistence Office n’est pas recommandée par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6301-151">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="c6301-152">Pour éviter les problèmes de compatibilité, nous vous conseillons de ne pas avoir de coexistence d’Office.</span><span class="sxs-lookup"><span data-stu-id="c6301-152">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="c6301-153">Toutefois, lorsque vous effectuez une migration vers une version plus récente d’Office, des problèmes peuvent entraîner des problèmes qui ne peuvent pas être résolus, de sorte que vous pouvez implémenter une coexistence temporaire pour faciliter la migration vers la dernière version du produit.</span><span class="sxs-lookup"><span data-stu-id="c6301-153">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="c6301-154">L’utilisation de la coexistence Office sur une base longue n’est jamais recommandée, et votre organisation doit être disposant d’un forfait pour une transition complète immédiate.</span><span class="sxs-lookup"><span data-stu-id="c6301-154">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="c6301-155">Avant de mettre en œuvre la coexistence d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-155">Before you implement Office coexistence</span></span>

<span data-ttu-id="c6301-156">Avant d’implémenter la coexistence d’Office, consultez la documentation Office suivante.</span><span class="sxs-lookup"><span data-stu-id="c6301-156">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="c6301-157">Choisissez l’article qui correspond à la version la plus récente d’Office pour laquelle vous envisagez d’implémenter une coexistence.</span><span class="sxs-lookup"><span data-stu-id="c6301-157">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6301-158">Version d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-158">Office version</span></span></th>
<th align="left"><span data-ttu-id="c6301-159">Lien vers des conseils</span><span class="sxs-lookup"><span data-stu-id="c6301-159">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-160">Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6301-160">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="c6301-161">Informations sur l’utilisation des suites et programmes Office 2013 (déploiement MSI) sur un ordinateur exécutant une autre version d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-161">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-162">Office 2010</span><span class="sxs-lookup"><span data-stu-id="c6301-162">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="c6301-163">Informations sur l’utilisation des suites et des programmes Office 2010 sur un ordinateur exécutant une autre version d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-163">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c6301-164">La documentation Office fournit des instructions détaillées sur la coexistence pour les installations d’Office basées sur Windows Installer (MSi) et démarrer en un clic.</span><span class="sxs-lookup"><span data-stu-id="c6301-164">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="c6301-165">Ce sujet App-V sur la coexistence complète les recommandations d’Office avec des informations plus spécifiques aux déploiements d’application-V.</span><span class="sxs-lookup"><span data-stu-id="c6301-165">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="c6301-166">Scénarios de coexistence pour Office pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6301-166">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="c6301-167">Les tableaux suivants résument les scénarios de coexistence pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c6301-167">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="c6301-168">Celles-ci sont organisées en fonction de la version et de la méthode de déploiement que vous démarrez avec et de la version et de la méthode de déploiement vers laquelle vous effectuez la migration.</span><span class="sxs-lookup"><span data-stu-id="c6301-168">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="c6301-169">Veillez à tester complètement toutes les solutions de coexistence avant de les déployer auprès d’un public de production.</span><span class="sxs-lookup"><span data-stu-id="c6301-169">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

<span data-ttu-id="c6301-170">**Remarques**  Microsoft ne prend pas en charge l’utilisation de plusieurs versions d’Office dans les environnements Windows Server pour lesquels le service de rôle hôte de session Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="c6301-170">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="c6301-171">Pour exécuter des scénarios de coexistence Office, vous devez désactiver ce service de rôle.</span><span class="sxs-lookup"><span data-stu-id="c6301-171">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="c6301-172">Intégrations Windows & coexistence d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-172">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="c6301-173">Les méthodes d’installation de Windows Installer et d’Office «démarrer en un clic» s’intègrent à certains points du système d’exploitation Windows sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c6301-173">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="c6301-174">Lorsque vous utilisez la coexistence, les intégrations de système d’exploitation courantes entre deux versions d’Office peuvent entrer en conflit et provoquer des problèmes de compatibilité et d’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6301-174">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="c6301-175">Avec App-V, vous pouvez effectuer une séquence de certaines versions d’Office afin d’exclure les intégrations, ce qui a pour effet d’isoler celles-ci du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c6301-175">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="c6301-176">Mode dans lequel App-V peut séquencer cette version d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-176">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-177">Office 2007</span><span class="sxs-lookup"><span data-stu-id="c6301-177">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-178">Toujours non intégré.</span><span class="sxs-lookup"><span data-stu-id="c6301-178">Always non-integrated.</span></span> <span data-ttu-id="c6301-179">App-V n’offre aucune intégration du système d’exploitation à une version virtualisée d’Office 2007.</span><span class="sxs-lookup"><span data-stu-id="c6301-179">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-180">Office 2010</span><span class="sxs-lookup"><span data-stu-id="c6301-180">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-181">Modes intégrés et non intégrés.</span><span class="sxs-lookup"><span data-stu-id="c6301-181">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-182">Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6301-182">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-183">Toujours intégré.</span><span class="sxs-lookup"><span data-stu-id="c6301-183">Always integrated.</span></span> <span data-ttu-id="c6301-184">Les intégrations du système d’exploitation Windows ne peuvent pas être désactivées.</span><span class="sxs-lookup"><span data-stu-id="c6301-184">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c6301-185">Microsoft vous recommande de déployer la coexistence d’Office avec une seule instance Office intégrée.</span><span class="sxs-lookup"><span data-stu-id="c6301-185">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="c6301-186">Par exemple, si vous utilisez App-V pour déployer Office 2010 et Office 2013, vous devez effectuer une séquence d’Office 2010 en mode non intégré.</span><span class="sxs-lookup"><span data-stu-id="c6301-186">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="c6301-187">Pour plus d’informations sur le séquençage d’Office dans le mode non-intégration (isolé), voir [Comment séquencé Microsoft Office 2010 dans Microsoft application virtualization 5,0](https://support.microsoft.com/kb/2830069).</span><span class="sxs-lookup"><span data-stu-id="c6301-187">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="c6301-188">Limitations connues des scénarios de coexistence d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-188">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="c6301-189">Les sections suivantes décrivent certains problèmes que vous pouvez rencontrer lors de l’utilisation de App-V pour implémenter la coexistence avec Office.</span><span class="sxs-lookup"><span data-stu-id="c6301-189">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="c6301-190">Limitations communes aux scénarios de coexistence pour Windows Installer et démarrer en un clic et App-V pour Office</span><span class="sxs-lookup"><span data-stu-id="c6301-190">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="c6301-191">Les limitations suivantes peuvent se produire lorsque vous installez les versions suivantes d’Office sur le même ordinateur:</span><span class="sxs-lookup"><span data-stu-id="c6301-191">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="c6301-192">Office 2010 à l’aide de la version Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c6301-192">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="c6301-193">Office 2013 à l’aide de App-V</span><span class="sxs-lookup"><span data-stu-id="c6301-193">Office 2013 by using App-V</span></span>

<span data-ttu-id="c6301-194">Après avoir publié Office 2013 en utilisant App-V côte à côte avec une version antérieure de la version d’Office 2010 basée sur Windows Installer, il est possible que le programme d’installation Windows démarre.</span><span class="sxs-lookup"><span data-stu-id="c6301-194">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="c6301-195">En effet, la version Windows Installer ou «démarrer en un clic» d’Office 2010 tente de s’inscrire automatiquement à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c6301-195">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="c6301-196">Pour ignorer l’opération d’inscription automatique pour Word 2010 natif, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="c6301-196">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="c6301-197">Quittez Word 2010.</span><span class="sxs-lookup"><span data-stu-id="c6301-197">Exit Word 2010.</span></span>

2.  <span data-ttu-id="c6301-198">Démarrez l’éditeur du registre en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="c6301-198">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="c6301-199">Dans Windows 7: cliquez sur **Démarrer**, tapez **regedit** dans la zone démarrer la recherche, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="c6301-199">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="c6301-200">Dans Windows 8, tapez **regedit** Appuyez sur entrée dans la page de démarrage, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="c6301-200">In Windows 8, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="c6301-201">Si vous êtes invité à entrer un mot de passe d’administrateur ou une confirmation, tapez le mot de passe ou cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="c6301-201">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="c6301-202">Recherchez et sélectionnez la sous-clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="c6301-202">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="c6301-203">Dans le menu **édition** , cliquez sur **nouveau**, puis cliquez sur **valeur DWORD**.</span><span class="sxs-lookup"><span data-stu-id="c6301-203">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="c6301-204">Tapez **NoReReg**, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="c6301-204">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="c6301-205">Cliquez avec le bouton droit sur **NoReReg** , puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="c6301-205">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="c6301-206">Dans la zone **ValueData** , tapez **1**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6301-206">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="c6301-207">Dans le menu fichier, cliquez sur **quitter** pour fermer l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="c6301-207">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="c6301-208">Intégration d’Office à Windows lors de l’utilisation de App-V pour le déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="c6301-208">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="c6301-209">Lorsque vous déployez Office 2013 à l’aide de App-V, Office est totalement intégré au système d’exploitation, qui fournit aux utilisateurs finaux les mêmes fonctionnalités qu’Office lorsque celui-ci est déployé sans App-V.</span><span class="sxs-lookup"><span data-stu-id="c6301-209">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="c6301-210">Le package App-V pour Office 2013 prend en charge les points d’intégration suivants avec le système d’exploitation Windows:</span><span class="sxs-lookup"><span data-stu-id="c6301-210">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6301-211">Point d’extension</span><span class="sxs-lookup"><span data-stu-id="c6301-211">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="c6301-212">Description</span><span class="sxs-lookup"><span data-stu-id="c6301-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-213">Plug-in Lync Meeting join pour Firefox et chrome</span><span class="sxs-lookup"><span data-stu-id="c6301-213">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-214">Les utilisateurs peuvent participer à des réunions Lync depuis Firefox et chrome</span><span class="sxs-lookup"><span data-stu-id="c6301-214">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-215">Envoyés vers le pilote d’impression OneNote</span><span class="sxs-lookup"><span data-stu-id="c6301-215">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-216">L’utilisateur peut imprimer dans OneNote</span><span class="sxs-lookup"><span data-stu-id="c6301-216">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-217">Notes liées OneNote</span><span class="sxs-lookup"><span data-stu-id="c6301-217">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-218">Notes liées OneNote</span><span class="sxs-lookup"><span data-stu-id="c6301-218">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-219">Envoyer vers le complément OneNote sur le Web Explorer</span><span class="sxs-lookup"><span data-stu-id="c6301-219">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-220">L’utilisateur peut envoyer à OneNote à partir d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c6301-220">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-221">Exception de pare-feu pour Lync et Outlook</span><span class="sxs-lookup"><span data-stu-id="c6301-221">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-222">Exception de pare-feu pour Lync et Outlook</span><span class="sxs-lookup"><span data-stu-id="c6301-222">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-223">Client MAPI</span><span class="sxs-lookup"><span data-stu-id="c6301-223">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-224">Les applications et les compléments natifs peuvent interagir avec les applications virtuelles Outlook via MAPI</span><span class="sxs-lookup"><span data-stu-id="c6301-224">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-225">Plug-in SharePoint pour Firefox</span><span class="sxs-lookup"><span data-stu-id="c6301-225">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-226">Les utilisateurs peuvent utiliser les fonctionnalités SharePoint dans Firefox</span><span class="sxs-lookup"><span data-stu-id="c6301-226">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-227">Applet panneau de configuration de la messagerie</span><span class="sxs-lookup"><span data-stu-id="c6301-227">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-228">L’utilisateur obtient l’applet panneau de configuration de la messagerie dans Outlook</span><span class="sxs-lookup"><span data-stu-id="c6301-228">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-229">Assemblys d’interopérabilité principaux</span><span class="sxs-lookup"><span data-stu-id="c6301-229">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-230">Compléments gérés par le support</span><span class="sxs-lookup"><span data-stu-id="c6301-230">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-231">Gestionnaire de cache de documents Office</span><span class="sxs-lookup"><span data-stu-id="c6301-231">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-232">Autorise le cache de documents pour les applications Office</span><span class="sxs-lookup"><span data-stu-id="c6301-232">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-233">Gestionnaire de recherche du protocole Outlook</span><span class="sxs-lookup"><span data-stu-id="c6301-233">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-234">L’utilisateur peut effectuer une recherche dans Outlook</span><span class="sxs-lookup"><span data-stu-id="c6301-234">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-235">Contrôles Active X:</span><span class="sxs-lookup"><span data-stu-id="c6301-235">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-236">Pour plus d’informations sur les contrôles ActiveX, voir informations de référence sur les <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de contrôles ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="c6301-236">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c6301-237">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="c6301-237">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-238">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c6301-239">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="c6301-239">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-240">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-240">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c6301-241">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="c6301-241">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-242">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-242">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c6301-243">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="c6301-243">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-244">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-244">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c6301-245">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="c6301-245">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-246">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-246">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c6301-247">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="c6301-247">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-248">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-248">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c6301-249">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="c6301-249">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-250">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-250">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c6301-251">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="c6301-251">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-252">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-252">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c6301-253">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="c6301-253">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-254">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-254">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c6301-255">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="c6301-255">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-256">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-256">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c6301-257">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="c6301-257">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-258">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-258">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c6301-259">Nom. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="c6301-259">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-260">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-260">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c6301-261">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="c6301-261">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-262">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-262">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c6301-263">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="c6301-263">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-264">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-264">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c6301-265">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="c6301-265">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-266">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c6301-266">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c6301-267">Programme d’assistance du navigateur OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c6301-267">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-268">Contrôle ActiveX</span><span class="sxs-lookup"><span data-stu-id="c6301-268">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-269">Superpositions d’icônes OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c6301-269">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6301-270">Icônes de l’interface utilisateur de l’Explorateur Windows lorsque les utilisateurs regardent les dossiers OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c6301-270">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-271">Extensions d'environnement</span><span class="sxs-lookup"><span data-stu-id="c6301-271">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6301-272">Associés</span><span class="sxs-lookup"><span data-stu-id="c6301-272">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6301-273">Windows Search</span><span class="sxs-lookup"><span data-stu-id="c6301-273">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 






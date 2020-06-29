---
title: Préparer un déploiement UE-V 2. x
description: Préparer un déploiement UE-V 2. x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811747"
---
# <span data-ttu-id="df171-103">Préparer un déploiement UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="df171-103">Prepare a UE-V 2.x Deployment</span></span>


<span data-ttu-id="df171-104">Il est possible de planifier et préparer la mise à niveau avant de déployer Microsoft User Interface Virtualization (UE-V) 2,0 ou 2,1 en tant que solution pour synchroniser les paramètres entre les appareils auxquels les utilisateurs accèdent au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="df171-104">There is some planning and preparation to do before you deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 as a solution for synchronizing settings between devices that users access in your enterprise.</span></span> <span data-ttu-id="df171-105">Cette rubrique vous aide à déterminer le type de déploiement que vous allez effectuer et la préparation que vous pouvez effectuer au préalable pour que votre déploiement réussisse.</span><span class="sxs-lookup"><span data-stu-id="df171-105">This topic helps you determine what type of deployment you'll be doing and what preparation you can make beforehand so that your deployment is successful.</span></span>

<span data-ttu-id="df171-106">Tout d’abord, examinons les tâches que vous devez effectuer pour déployer UE-V:</span><span class="sxs-lookup"><span data-stu-id="df171-106">First, let’s look at the tasks you’ll do to deploy UE-V:</span></span>

-   <span data-ttu-id="df171-107">Planifier votre déploiement UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-107">Plan your UE-V Deployment</span></span>

    <span data-ttu-id="df171-108">Avant de déployer quoi que ce soit, il est conseillé de procéder de manière appropriée pour déterminer les fonctionnalités d’UE-V que vous déploierez.</span><span class="sxs-lookup"><span data-stu-id="df171-108">Before you deploy anything, a good first step is to do a little bit of planning so that you can determine which UE-V features you’ll deploy.</span></span> <span data-ttu-id="df171-109">Par conséquent, si vous quittez cette page, assurez-vous de revenir en revue les informations de planification ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="df171-109">So if you leave this page, make sure you come back and read through the planning information below.</span></span>

-   [<span data-ttu-id="df171-110">Déployer les fonctionnalités UE-V2.x requises</span><span class="sxs-lookup"><span data-stu-id="df171-110">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    <span data-ttu-id="df171-111">Chaque déploiement d’UE-V nécessite les activités suivantes:</span><span class="sxs-lookup"><span data-stu-id="df171-111">Every UE-V deployment requires these activities:</span></span>

    -   [<span data-ttu-id="df171-112">Définir un emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="df171-112">Define a settings storage location</span></span>](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [<span data-ttu-id="df171-113">Décider du déploiement de l’agent UE-V et de la gestion des configurations UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-113">Decide how to deploy the UE-V Agent and manage UE-V configurations</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   <span data-ttu-id="df171-114">[Installer l’agent UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) sur tous les ordinateurs des utilisateurs qui ont besoin de la synchronisation des paramètres</span><span class="sxs-lookup"><span data-stu-id="df171-114">[Install the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) on every user computer that needs settings synchronized</span></span>

-   <span data-ttu-id="df171-115">Vous pouvez également [déployer UE-V 2. x pour des applications personnalisées.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span><span class="sxs-lookup"><span data-stu-id="df171-115">Optionally, you can [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span></span>

    <span data-ttu-id="df171-116">La planification vous aidera à déterminer si vous souhaitez que UE-V prenne en charge la synchronisation des paramètres d’applications personnalisées (tiers ou métier), qui nécessitent ces fonctionnalités d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-116">Planning will help you figure out whether you want UE-V to support the synchronization of settings for custom applications (third-party or line-of-business), which requires these UE-V features:</span></span>

    -   <span data-ttu-id="df171-117">[Installer le générateur de UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) pour créer, modifier et valider les modèles d’emplacement des paramètres personnalisés requis pour synchroniser les paramètres d’application personnalisés</span><span class="sxs-lookup"><span data-stu-id="df171-117">[Install the UEV Generator](https://technet.microsoft.com/library/dn458942.aspx#uevgen) so you can create, edit, and validate the custom settings location templates required to synchronize custom application settings</span></span>

    -   <span data-ttu-id="df171-118">[Créer des modèles d’emplacement de paramètres personnalisés](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) à l’aide du générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-118">[Create custom settings location templates](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) by using the UE-V Generator</span></span>

    -   <span data-ttu-id="df171-119">[Déployer un catalogue de modèles de paramètres UE-V](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) qui vous permet de stocker vos modèles d’emplacement des paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="df171-119">[Deploy a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) that you use to store your custom settings location templates</span></span>

<span data-ttu-id="df171-120">Ce diagramme de flux de travail fournit une connaissance de haut niveau d’un déploiement UE-V et des décisions qui déterminent le mode de déploiement d’UE-V au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="df171-120">This workflow diagram provides a high-level understanding of a UE-V deployment and the decisions that determine how you deploy UE-V in your enterprise.</span></span>

![deploymentworkflow](images/deploymentworkflow.png)

<span data-ttu-id="df171-122">**Planification d’un déploiement UE-V:** Tout d’abord, vous souhaiterez peut-être effectuer un léger déploiement pour déterminer les composants UE-V que vous déploierez.</span><span class="sxs-lookup"><span data-stu-id="df171-122">**Planning a UE-V deployment:** First, you want to do a little bit of planning so that you can determine which UE-V components you’ll be deploying.</span></span> <span data-ttu-id="df171-123">La planification d’un déploiement UE-V implique les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="df171-123">Planning a UE-V deployment involves these things:</span></span>

-   [<span data-ttu-id="df171-124">Choisir de synchroniser les paramètres des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="df171-124">Decide whether to synchronize settings for custom applications</span></span>](#deciding)

    <span data-ttu-id="df171-125">Cela détermine si vous allez installer le générateur UE-V lors du déploiement, ce qui vous permet de créer des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="df171-125">This determines whether you will install the UE-V Generator during deployment, which lets you create custom settings location templates.</span></span> <span data-ttu-id="df171-126">Ce service implique les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="df171-126">It involves the following:</span></span>

    <span data-ttu-id="df171-127">Passez en revue les [paramètres qui sont synchronisés automatiquement dans un déploiement UE-V](#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="df171-127">Review the [settings that are synchronized automatically in a UE-V deployment](#autosyncsettings).</span></span>

    <span data-ttu-id="df171-128">[Déterminez si vous avez besoin que les paramètres soient synchronisés pour les autres applications](#determinesettingssync).</span><span class="sxs-lookup"><span data-stu-id="df171-128">[Determine whether you need settings synchronized for other applications](#determinesettingssync).</span></span>

-   <span data-ttu-id="df171-129">Passez en revue [d’autres considérations relatives au déploiement d’UE-V](#considerations), comme la haute disponibilité et la planification de la capacité.</span><span class="sxs-lookup"><span data-stu-id="df171-129">Review [other considerations for deploying UE-V](#considerations), such as high availability and capacity planning.</span></span>

-   [<span data-ttu-id="df171-130">Confirmer les conditions préalables et les configurations prises en charge pour UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-130">Confirm prerequisites and supported configurations for UE-V</span></span>](#prereqs)

## <a href="" id="deciding"></a><span data-ttu-id="df171-131">Choisir de synchroniser les paramètres des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="df171-131">Decide Whether to Synchronize Settings for Custom Applications</span></span>


<span data-ttu-id="df171-132">Dans un déploiement UE-V, de nombreux paramètres sont synchronisés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="df171-132">In a UE-V deployment, many settings are automatically synchronized.</span></span> <span data-ttu-id="df171-133">Toutefois, vous pouvez également personnaliser UE-V pour synchroniser les paramètres d’autres applications, telles que les applications métier et les applications tierces.</span><span class="sxs-lookup"><span data-stu-id="df171-133">But you can also customize UE-V to synchronize settings for other applications, such as line-of-business and third-party apps.</span></span>

<span data-ttu-id="df171-134">Le fait de décider d’utiliser UE-V pour synchroniser les paramètres des applications personnalisées est probablement la partie la plus importante de la planification de votre déploiement d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-134">Deciding if you want UE-V to synchronize settings for custom applications is probably the most important part of planning your UE-V deployment.</span></span> <span data-ttu-id="df171-135">Les rubriques de cette section vous aideront à prendre cette décision.</span><span class="sxs-lookup"><span data-stu-id="df171-135">The topics in this section will help you make that decision.</span></span>

### <a href="" id="autosyncsettings"></a><span data-ttu-id="df171-136">Paramètres synchronisés automatiquement dans un déploiement UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-136">Settings that are automatically synchronized in a UE-V deployment</span></span>

<span data-ttu-id="df171-137">Cette section fournit des informations sur les paramètres qui sont synchronisés par défaut dans UE-V, notamment les suivants:</span><span class="sxs-lookup"><span data-stu-id="df171-137">This section provides information about the settings that are synchronized by default in UE-V, including the following:</span></span>

<span data-ttu-id="df171-138">Applications de bureau dont les paramètres sont synchronisés par défaut</span><span class="sxs-lookup"><span data-stu-id="df171-138">Desktop applications whose settings are synchronized by default</span></span>

<span data-ttu-id="df171-139">Paramètres de bureau Windows qui sont synchronisés par défaut</span><span class="sxs-lookup"><span data-stu-id="df171-139">Windows desktop settings that are synchronized by default</span></span>

<span data-ttu-id="df171-140">Une déclaration de prise en charge de la synchronisation des paramètres d’application Windows</span><span class="sxs-lookup"><span data-stu-id="df171-140">A statement of support for Windows app setting synchronization</span></span>

<span data-ttu-id="df171-141">Pour plus d’aide sur les paramètres de Microsoft Office 2013, Microsoft Office 2010 et Microsoft Office 2007 qui sont synchronisés avec UE-V, voir modèles d’utilisation de l' [interface utilisateur (UE-v)](https://www.microsoft.com/download/details.aspx?id=46367) .</span><span class="sxs-lookup"><span data-stu-id="df171-141">See [User Experience Virtualization (UE-V) settings templates for Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) to download a complete list of the specific Microsoft Office 2013, Microsoft Office 2010, and Microsoft Office 2007 settings that are synchronized by UE-V.</span></span>

### <span data-ttu-id="df171-142">Applications de bureau synchronisées par défaut dans UE-V 2,1 et UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="df171-142">Desktop applications synchronized by default in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="df171-143">Lorsque vous installez l’agent UE-V 2,1 ou 2,1 SP1, il inscrit un groupe par défaut de modèles d’emplacement des paramètres qui capture les valeurs de paramètres pour ces applications Microsoft courantes.</span><span class="sxs-lookup"><span data-stu-id="df171-143">When you install the UE-V 2.1 or 2.1 SP1 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="df171-144">Astuce</span><span class="sxs-lookup"><span data-stu-id="df171-144">Tip</span></span>**  
<span data-ttu-id="df171-145">**Synchronisation des paramètres de Microsoft Office 2007** -dans UE-V 2,1 et 2,1 SP1, un modèle d’emplacement des paramètres n’est plus inclus par défaut pour les applications Office 2007.</span><span class="sxs-lookup"><span data-stu-id="df171-145">**Microsoft Office 2007 Settings Synchronization** – In UE-V 2.1 and 2.1 SP1, a settings location template is no longer included by default for Office 2007 applications.</span></span> <span data-ttu-id="df171-146">Toutefois, vous pouvez toujours utiliser les modèles Office 2007 d’UE-V 2,0 ou une version antérieure et télécharger les modèles à partir de la [Galerie de modèles UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="df171-146">However, you can still use Office 2007 templates from UE-V 2.0 or earlier and can get the templates from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="df171-147">Catégorie d’application</span><span class="sxs-lookup"><span data-stu-id="df171-147">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="df171-148">Description</span><span class="sxs-lookup"><span data-stu-id="df171-148">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df171-149">Applications Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="df171-149">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="df171-150">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Télécharger la liste de tous les paramètres synchronisés </a> )</span><span class="sxs-lookup"><span data-stu-id="df171-150">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-151">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="df171-151">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="df171-152">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="df171-152">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="df171-153">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="df171-153">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="df171-154">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="df171-154">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="df171-155">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="df171-155">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="df171-156">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="df171-156">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="df171-157">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="df171-157">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="df171-158">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="df171-158">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="df171-159">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="df171-159">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="df171-160">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="df171-160">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="df171-161">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="df171-161">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="df171-162">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="df171-162">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="df171-163">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="df171-163">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df171-164">Applications Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="df171-164">Microsoft Office 2013 applications</span></span></p>
<p><span data-ttu-id="df171-165">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Télécharger la liste de tous les paramètres synchronisés </a> )</span><span class="sxs-lookup"><span data-stu-id="df171-165">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-166">Microsoft Word 2013</span><span class="sxs-lookup"><span data-stu-id="df171-166">Microsoft Word 2013</span></span></p>
<p><span data-ttu-id="df171-167">Microsoft Excel 2013</span><span class="sxs-lookup"><span data-stu-id="df171-167">Microsoft Excel 2013</span></span></p>
<p><span data-ttu-id="df171-168">Microsoft Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="df171-168">Microsoft Outlook 2013</span></span></p>
<p><span data-ttu-id="df171-169">Microsoft Access 2013</span><span class="sxs-lookup"><span data-stu-id="df171-169">Microsoft Access 2013</span></span></p>
<p><span data-ttu-id="df171-170">Microsoft Project 2013</span><span class="sxs-lookup"><span data-stu-id="df171-170">Microsoft Project 2013</span></span></p>
<p><span data-ttu-id="df171-171">Microsoft PowerPoint 2013</span><span class="sxs-lookup"><span data-stu-id="df171-171">Microsoft PowerPoint 2013</span></span></p>
<p><span data-ttu-id="df171-172">Microsoft Publisher 2013</span><span class="sxs-lookup"><span data-stu-id="df171-172">Microsoft Publisher 2013</span></span></p>
<p><span data-ttu-id="df171-173">Microsoft Visio 2013</span><span class="sxs-lookup"><span data-stu-id="df171-173">Microsoft Visio 2013</span></span></p>
<p><span data-ttu-id="df171-174">Microsoft InfoPath 2013</span><span class="sxs-lookup"><span data-stu-id="df171-174">Microsoft InfoPath 2013</span></span></p>
<p><span data-ttu-id="df171-175">Microsoft Lync 2013</span><span class="sxs-lookup"><span data-stu-id="df171-175">Microsoft Lync 2013</span></span></p>
<p><span data-ttu-id="df171-176">Microsoft OneNote 2013</span><span class="sxs-lookup"><span data-stu-id="df171-176">Microsoft OneNote 2013</span></span></p>
<p><span data-ttu-id="df171-177">Microsoft SharePoint Designer 2013</span><span class="sxs-lookup"><span data-stu-id="df171-177">Microsoft SharePoint Designer 2013</span></span></p>
<p><span data-ttu-id="df171-178">Centre de téléchargement Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="df171-178">Microsoft Office 2013 Upload Center</span></span></p>
<p><span data-ttu-id="df171-179">Microsoft OneDrive entreprise 2013</span><span class="sxs-lookup"><span data-stu-id="df171-179">Microsoft OneDrive for Business 2013</span></span></p>
<p><span data-ttu-id="df171-180">Les modèles d’emplacement des paramètres d’UE-V 2,1 et 2,1 SP1 de Microsoft Office 2013 incluent une prise en charge améliorée des signatures Outlook.</span><span class="sxs-lookup"><span data-stu-id="df171-180">The UE-V 2.1 and 2.1 SP1 Microsoft Office 2013 settings location templates include improved Outlook signature support.</span></span> <span data-ttu-id="df171-181">Nous avons ajouté la synchronisation des paramètres de signature par défaut pour les courriers électroniques, les réponses et les transferts.</span><span class="sxs-lookup"><span data-stu-id="df171-181">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="df171-182">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-182">Note</span></span></strong><br/><p><span data-ttu-id="df171-183">Un profil Outlook doit être créé pour tout appareil sur lequel un utilisateur souhaite synchroniser sa signature Outlook.</span><span class="sxs-lookup"><span data-stu-id="df171-183">An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="df171-184">Si ce n’est pas le cas, l’utilisateur peut en créer un, puis redémarrer Outlook sur cet appareil pour activer la synchronisation des signatures.</span><span class="sxs-lookup"><span data-stu-id="df171-184">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df171-185">Options du navigateur: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 et Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="df171-185">Browser options: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10, and Internet Explorer 11</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-186">Favoris, page d’accueil, onglets et barres d’outils.</span><span class="sxs-lookup"><span data-stu-id="df171-186">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="df171-187">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-187">Note</span></span></strong><br/><p><span data-ttu-id="df171-188">UE-V n’utilise pas les paramètres d’itinérance pour les cookies Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="df171-188">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df171-189">Accessoires Windows</span><span class="sxs-lookup"><span data-stu-id="df171-189">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-190">Microsoft Calculator, bloc-notes, WordPad.</span><span class="sxs-lookup"><span data-stu-id="df171-190">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="df171-191">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-191">Note</span></span>**  
<span data-ttu-id="df171-192">UE-V 2,1 SP1 ne synchronise pas les paramètres entre Microsoft Calculator dans Windows 10 et Microsoft Calculator dans les systèmes d’exploitation précédents.</span><span class="sxs-lookup"><span data-stu-id="df171-192">UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>



### <span data-ttu-id="df171-193">Applications de bureau synchronisées par défaut dans UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="df171-193">Desktop applications synchronized by default in UE-V 2.0</span></span>

<span data-ttu-id="df171-194">Lors de l’installation de l’agent UE-V 2,0, il inscrit un groupe par défaut de modèles d’emplacement des paramètres qui capturent les valeurs de paramètres pour ces applications Microsoft courantes.</span><span class="sxs-lookup"><span data-stu-id="df171-194">When you install the UE-V 2.0 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="df171-195">Astuce</span><span class="sxs-lookup"><span data-stu-id="df171-195">Tip</span></span>**  
<span data-ttu-id="df171-196">**Synchronisation des paramètres de Microsoft Office 2013** -dans UE-V 2,0, un modèle d’emplacement des paramètres n’est pas inclus par défaut pour les applications Office 2013, mais il est disponible en téléchargement à partir de la [Galerie de modèles UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="df171-196">**Microsoft Office 2013 Settings Synchronization** – In UE-V 2.0, a settings location template is not included by default for Office 2013 applications, but is available for download from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span> <span data-ttu-id="df171-197">La [synchronisation d’Office 2013 avec UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) fournit des détails sur les modèles pris en charge permettant de synchroniser les paramètres d’Office 2013.</span><span class="sxs-lookup"><span data-stu-id="df171-197">[Synchronizing Office 2013 with UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) provides details about the supported templates that synchronize Office 2013 settings.</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="df171-198">Catégorie d’application</span><span class="sxs-lookup"><span data-stu-id="df171-198">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="df171-199">Description</span><span class="sxs-lookup"><span data-stu-id="df171-199">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df171-200">Applications Microsoft Office 2007</span><span class="sxs-lookup"><span data-stu-id="df171-200">Microsoft Office 2007 applications</span></span></p>
<p><span data-ttu-id="df171-201">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Télécharger la liste de tous les paramètres synchronisés </a> )</span><span class="sxs-lookup"><span data-stu-id="df171-201">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-202">Microsoft Access 2007</span><span class="sxs-lookup"><span data-stu-id="df171-202">Microsoft Access 2007</span></span></p>
<p><span data-ttu-id="df171-203">Microsoft Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="df171-203">Microsoft Communicator 2007</span></span></p>
<p><span data-ttu-id="df171-204">Microsoft Excel 2007</span><span class="sxs-lookup"><span data-stu-id="df171-204">Microsoft Excel 2007</span></span></p>
<p><span data-ttu-id="df171-205">Microsoft InfoPath 2007</span><span class="sxs-lookup"><span data-stu-id="df171-205">Microsoft InfoPath 2007</span></span></p>
<p><span data-ttu-id="df171-206">Microsoft OneNote 2007</span><span class="sxs-lookup"><span data-stu-id="df171-206">Microsoft OneNote 2007</span></span></p>
<p><span data-ttu-id="df171-207">Microsoft Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="df171-207">Microsoft Outlook 2007</span></span></p>
<p><span data-ttu-id="df171-208">Microsoft PowerPoint 2007</span><span class="sxs-lookup"><span data-stu-id="df171-208">Microsoft PowerPoint 2007</span></span></p>
<p><span data-ttu-id="df171-209">Microsoft Project 2007</span><span class="sxs-lookup"><span data-stu-id="df171-209">Microsoft Project 2007</span></span></p>
<p><span data-ttu-id="df171-210">Microsoft Publisher 2007</span><span class="sxs-lookup"><span data-stu-id="df171-210">Microsoft Publisher 2007</span></span></p>
<p><span data-ttu-id="df171-211">Microsoft SharePoint Designer 2007</span><span class="sxs-lookup"><span data-stu-id="df171-211">Microsoft SharePoint Designer 2007</span></span></p>
<p><span data-ttu-id="df171-212">Microsoft Visio 2007</span><span class="sxs-lookup"><span data-stu-id="df171-212">Microsoft Visio 2007</span></span></p>
<p><span data-ttu-id="df171-213">Microsoft Word 2007</span><span class="sxs-lookup"><span data-stu-id="df171-213">Microsoft Word 2007</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df171-214">Applications Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="df171-214">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="df171-215">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Télécharger la liste de tous les paramètres synchronisés </a> )</span><span class="sxs-lookup"><span data-stu-id="df171-215">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-216">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="df171-216">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="df171-217">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="df171-217">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="df171-218">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="df171-218">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="df171-219">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="df171-219">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="df171-220">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="df171-220">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="df171-221">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="df171-221">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="df171-222">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="df171-222">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="df171-223">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="df171-223">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="df171-224">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="df171-224">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="df171-225">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="df171-225">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="df171-226">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="df171-226">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="df171-227">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="df171-227">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="df171-228">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="df171-228">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df171-229">Options du navigateur: Internet Explorer 8, Internet Explorer 9 et Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="df171-229">Browser options: Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-230">Favoris, page d’accueil, onglets et barres d’outils.</span><span class="sxs-lookup"><span data-stu-id="df171-230">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="df171-231">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-231">Note</span></span></strong><br/><p><span data-ttu-id="df171-232">UE-V n’utilise pas les paramètres d’itinérance pour les cookies Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="df171-232">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df171-233">Accessoires Windows</span><span class="sxs-lookup"><span data-stu-id="df171-233">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-234">Microsoft Calculator, bloc-notes, WordPad.</span><span class="sxs-lookup"><span data-stu-id="df171-234">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a><span data-ttu-id="df171-235">Paramètres Windows synchronisés par défaut</span><span class="sxs-lookup"><span data-stu-id="df171-235">Windows settings synchronized by default</span></span>

<span data-ttu-id="df171-236">UE-V inclut des modèles d’emplacement des paramètres qui capturent les valeurs des paramètres de ces paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="df171-236">UE-V includes settings location templates that capture settings values for these Windows settings.</span></span>

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
<th align="left"><span data-ttu-id="df171-237">paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="df171-237">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="df171-238">Description</span><span class="sxs-lookup"><span data-stu-id="df171-238">Description</span></span></th>
<th align="left"><span data-ttu-id="df171-239">Appliquer le</span><span class="sxs-lookup"><span data-stu-id="df171-239">Apply on</span></span></th>
<th align="left"><span data-ttu-id="df171-240">Exporter sur</span><span class="sxs-lookup"><span data-stu-id="df171-240">Export on</span></span></th>
<th align="left"><span data-ttu-id="df171-241">État par défaut</span><span class="sxs-lookup"><span data-stu-id="df171-241">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df171-242">Arrière-plan du Bureau</span><span class="sxs-lookup"><span data-stu-id="df171-242">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-243">Arrière-plan ou papier peint actuellement actif.</span><span class="sxs-lookup"><span data-stu-id="df171-243">Currently active desktop background or wallpaper.</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-244">Connexion, déverrouiller, connexion à distance, événements de tâche planifiés.</span><span class="sxs-lookup"><span data-stu-id="df171-244">Logon, unlock, remote connect, Scheduled Task events.</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-245">Déconnexion, verrouillage, disconnexion distante, utilisateur cliquant sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres de l’entreprise ou intervalle de tâches planifiées</span><span class="sxs-lookup"><span data-stu-id="df171-245">Logoff, lock, remote disconnect, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-246">Activé</span><span class="sxs-lookup"><span data-stu-id="df171-246">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df171-247">Options d’ergonomie</span><span class="sxs-lookup"><span data-stu-id="df171-247">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-248">Paramètres d’accessibilité et d’entrée, loupe Microsoft, narrateur et clavier visuel.</span><span class="sxs-lookup"><span data-stu-id="df171-248">Accessibility and input settings, Microsoft Magnifier, Narrator, and on-Screen Keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-249">Connexion uniquement.</span><span class="sxs-lookup"><span data-stu-id="df171-249">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-250">Fermer la session, un utilisateur clique sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres de l’entreprise ou intervalle de tâches planifiées</span><span class="sxs-lookup"><span data-stu-id="df171-250">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-251">Activé</span><span class="sxs-lookup"><span data-stu-id="df171-251">Enabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df171-252">Paramètres de bureau</span><span class="sxs-lookup"><span data-stu-id="df171-252">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-253">Paramètres du menu Démarrer et de la barre des tâches, options des dossiers, icônes du bureau par défaut, horloges supplémentaires et paramètres régionaux et linguistiques.</span><span class="sxs-lookup"><span data-stu-id="df171-253">Start menu and Taskbar settings, Folder options, Default desktop icons, Additional clocks, and Region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-254">Connexion uniquement.</span><span class="sxs-lookup"><span data-stu-id="df171-254">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-255">Fermer la session, un utilisateur clique sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres d’une entreprise ou une tâche planifiée</span><span class="sxs-lookup"><span data-stu-id="df171-255">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-256">Activé</span><span class="sxs-lookup"><span data-stu-id="df171-256">Enabled</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="df171-257">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-257">Note</span></span>**  
<span data-ttu-id="df171-258">À partir de Windows 8, UE-V n’itinérance pas les paramètres liés à l’écran d’accueil, tels que les éléments et les emplacements.</span><span class="sxs-lookup"><span data-stu-id="df171-258">Starting in Windows 8, UE-V does not roam settings related to the Start screen, such as items and locations.</span></span> <span data-ttu-id="df171-259">Par ailleurs, UE-V ne prend pas en charge la synchronisation des éléments de la barre des tâches épinglés ou des raccourcis vers les fichiers Windows.</span><span class="sxs-lookup"><span data-stu-id="df171-259">In addition, UE-V does not support synchronization of pinned taskbar items or Windows file shortcuts.</span></span>



**<span data-ttu-id="df171-260">Important</span><span class="sxs-lookup"><span data-stu-id="df171-260">Important</span></span>**  
<span data-ttu-id="df171-261">UE-V 2,1 SP1 répartir les paramètres de la barre des tâches entre les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="df171-261">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="df171-262">Toutefois, UE-V ne synchronise pas les paramètres de la barre des tâches entre les appareils et appareils Windows 10 exécutant d’anciens systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="df171-262">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="df171-263">Groupe de paramètres</span><span class="sxs-lookup"><span data-stu-id="df171-263">Settings group</span></span></th>
<th align="left"><span data-ttu-id="df171-264">Catégorie</span><span class="sxs-lookup"><span data-stu-id="df171-264">Category</span></span></th>
<th align="left"><span data-ttu-id="df171-265">Collecte</span><span class="sxs-lookup"><span data-stu-id="df171-265">Capture</span></span></th>
<th align="left"><span data-ttu-id="df171-266">Appliquer</span><span class="sxs-lookup"><span data-stu-id="df171-266">Apply</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="df171-267">Paramètres de l’application</span><span class="sxs-lookup"><span data-stu-id="df171-267">Application Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="df171-268">Applications Windows  </span><span class="sxs-lookup"><span data-stu-id="df171-268">Windows apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-269">Fermer l’application</span><span class="sxs-lookup"><span data-stu-id="df171-269">Close app</span></span></p>
<p><span data-ttu-id="df171-270">Événement de modification des paramètres d’application Windows</span><span class="sxs-lookup"><span data-stu-id="df171-270">Windows app settings change event</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-271">Démarrer le moniteur d’application UE-V au démarrage</span><span class="sxs-lookup"><span data-stu-id="df171-271">Start the UE-V App Monitor at startup</span></span></p>
<p><span data-ttu-id="df171-272">Ouvrir l’application</span><span class="sxs-lookup"><span data-stu-id="df171-272">Open app</span></span></p>
<p><span data-ttu-id="df171-273">Événement de modification des paramètres d’application Windows</span><span class="sxs-lookup"><span data-stu-id="df171-273">Windows App Settings change event</span></span></p>
<p><span data-ttu-id="df171-274">Arrivée d’un package de paramètres</span><span class="sxs-lookup"><span data-stu-id="df171-274">Arrival of a settings package</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="df171-275">Applications de bureau</span><span class="sxs-lookup"><span data-stu-id="df171-275">Desktop applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-276">Application se ferme</span><span class="sxs-lookup"><span data-stu-id="df171-276">Application closes</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-277">L’application s’ouvre et se ferme</span><span class="sxs-lookup"><span data-stu-id="df171-277">Application opens and closes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="df171-278">Paramètres de bureau</span><span class="sxs-lookup"><span data-stu-id="df171-278">Desktop settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="df171-279">Arrière-plan du Bureau</span><span class="sxs-lookup"><span data-stu-id="df171-279">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-280">Verrouiller ou déconnecter</span><span class="sxs-lookup"><span data-stu-id="df171-280">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-281">Connexion, déverrouiller, connexion à distance, notification de nouvelle réception de package, l’utilisateur clique sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres de l’entreprise ou la tâche planifiée s’exécute.</span><span class="sxs-lookup"><span data-stu-id="df171-281">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="df171-282">Options d’ergonomie (standard: accessibilité, narrateur, loupe, clavier visuel)</span><span class="sxs-lookup"><span data-stu-id="df171-282">Ease of Access (Common – Accessibility, Narrator, Magnifier, On-Screen-Keyboard)</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-283">Verrouiller ou déconnecter</span><span class="sxs-lookup"><span data-stu-id="df171-283">Lock or Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-284">Accès</span><span class="sxs-lookup"><span data-stu-id="df171-284">Logon</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="df171-285">Facilité d’accès (interpréteur audio, accessibilité, clavier, souris)</span><span class="sxs-lookup"><span data-stu-id="df171-285">Ease of Access (Shell - Audio, Accessibility, Keyboard, Mouse)</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-286">Verrouiller ou déconnecter</span><span class="sxs-lookup"><span data-stu-id="df171-286">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-287">Connexion, déverrouiller, connexion à distance, notification de nouvelle réception de package, utilisateur clique sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres de l’entreprise ou exécution d’une tâche planifiée</span><span class="sxs-lookup"><span data-stu-id="df171-287">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="df171-288">Paramètres de bureau</span><span class="sxs-lookup"><span data-stu-id="df171-288">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-289">Verrouiller ou déconnecter</span><span class="sxs-lookup"><span data-stu-id="df171-289">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-290">Accès</span><span class="sxs-lookup"><span data-stu-id="df171-290">Logon</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="df171-291">UE-V-support pour les applications Windows</span><span class="sxs-lookup"><span data-stu-id="df171-291">UE-V-support for Windows Apps</span></span>

<span data-ttu-id="df171-292">Pour les applications Windows, le développeur de l’application spécifie les paramètres qui sont synchronisés.</span><span class="sxs-lookup"><span data-stu-id="df171-292">For Windows apps, the app developer specifies the settings that are synchronized.</span></span> <span data-ttu-id="df171-293">Vous pouvez spécifier les applications Windows activées pour la synchronisation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="df171-293">You can specify which Windows apps are enabled for settings synchronization.</span></span>

<span data-ttu-id="df171-294">Pour afficher une liste des applications Windows qui peuvent synchroniser les paramètres sur un ordinateur dont le nom de la famille de packages, le statut activée et la source activée, à l’invite de commandes Windows PowerShell, entrez:</span><span class="sxs-lookup"><span data-stu-id="df171-294">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="df171-295">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-295">Note</span></span>**  
<span data-ttu-id="df171-296">Depuis Windows 8, UE-V ne synchronise pas les paramètres de l’application Windows si l’utilisateur du domaine associe les informations d’identification de connexion à son compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="df171-296">As of Windows 8, UE-V does not synchronize Windows app settings if the domain user links their sign-in credentials to their Microsoft Account.</span></span> <span data-ttu-id="df171-297">Ce lien permet de synchroniser les paramètres avec Microsoft OneDrive pour UE-V, qui désactive la synchronisation des paramètres d’application Windows.</span><span class="sxs-lookup"><span data-stu-id="df171-297">This linking synchronizes settings to Microsoft OneDrive so UE-V, which disables synchronization of Windows app settings.</span></span>



### <span data-ttu-id="df171-298">UE-V-support pour les imprimantes itinérantes</span><span class="sxs-lookup"><span data-stu-id="df171-298">UE-V-support for Roaming Printers</span></span>

<span data-ttu-id="df171-299">UE-V 2,1 SP1 permet aux imprimantes réseau d’avoir accès aux périphériques de sorte que l’utilisateur ait accès à ses imprimantes réseau lorsqu’il est connecté à un appareil du réseau.</span><span class="sxs-lookup"><span data-stu-id="df171-299">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="df171-300">Cela comprend l’itinérance de l’imprimante définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="df171-300">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="df171-301">L’itinérance d’imprimantes dans UE-V nécessite l’un des scénarios suivants:</span><span class="sxs-lookup"><span data-stu-id="df171-301">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="df171-302">Le serveur d’impression peut télécharger le pilote requis lorsqu’il est itinérant vers un nouvel appareil.</span><span class="sxs-lookup"><span data-stu-id="df171-302">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="df171-303">Le pilote de l’imprimante du réseau errant est préinstallé sur n’importe quel appareil qui a besoin d’accéder à cette imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="df171-303">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="df171-304">Le pilote de l’imprimante peut être obtenu à partir de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="df171-304">The printer driver can be obtained from Windows Update.</span></span>

**<span data-ttu-id="df171-305">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-305">Note</span></span>**  
<span data-ttu-id="df171-306">La fonctionnalité d’itinérance d’imprimante UE-V n’effectue **pas** de paramètres d’impression ou de préférences tels que l’impression recto verso.</span><span class="sxs-lookup"><span data-stu-id="df171-306">The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>



### <a href="" id="determinesettingssync"></a><span data-ttu-id="df171-307">Déterminer si vous avez besoin des paramètres synchronisés pour d’autres applications</span><span class="sxs-lookup"><span data-stu-id="df171-307">Determine whether you need settings synchronized for other applications</span></span>

<span data-ttu-id="df171-308">Une fois que vous avez examiné les paramètres qui sont synchronisés automatiquement dans le déploiement d’UE-V, vous pouvez choisir de synchroniser les paramètres d’autres applications, car cela détermine le mode de déploiement d’UE-V au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="df171-308">After you have reviewed the settings that are synchronized automatically in a UE-V deployment, you want to decide whether you will synchronize settings for other applications since this determines how you deploy UE-V throughout your enterprise.</span></span>

<span data-ttu-id="df171-309">En tant qu’administrateur, lorsque vous considérez les applications de bureau à inclure dans votre solution UE-V, considérez les paramètres qui peuvent être personnalisés par les utilisateurs, la façon dont l’application stocke les paramètres correspondants.</span><span class="sxs-lookup"><span data-stu-id="df171-309">As an administrator, when you consider which desktop applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="df171-310">Certaines applications de bureau ne disposent pas de paramètres qui peuvent être personnalisés ou personnalisés de façon régulière par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="df171-310">Not all desktop applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="df171-311">De plus, tous les paramètres des applications de bureau ne peuvent pas être synchronisés en toute sécurité sur plusieurs ordinateurs ou environnements.</span><span class="sxs-lookup"><span data-stu-id="df171-311">In addition, not all desktop applications settings can safely be synchronized across multiple computers or environments.</span></span>

<span data-ttu-id="df171-312">En règle générale, vous pouvez synchroniser les paramètres qui répondent aux critères suivants:</span><span class="sxs-lookup"><span data-stu-id="df171-312">In general, you can synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="df171-313">Paramètres stockés dans des emplacements accessibles aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="df171-313">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="df171-314">Par exemple, ne synchronisez pas les paramètres stockés dans system32 ou en dehors de la section HKEY \ _CURRENT \ _USER (HKCU) du Registre.</span><span class="sxs-lookup"><span data-stu-id="df171-314">For example, do not synchronize settings that are stored in System32 or outside the HKEY\_CURRENT\_USER (HKCU) section of the registry.</span></span>

-   <span data-ttu-id="df171-315">Paramètres qui ne sont pas propres à l’ordinateur en particulier.</span><span class="sxs-lookup"><span data-stu-id="df171-315">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="df171-316">Par exemple, excluez les configurations réseau ou matérielles.</span><span class="sxs-lookup"><span data-stu-id="df171-316">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="df171-317">Paramètres qui peuvent être synchronisés entre ordinateurs sans risque de corruption de données.</span><span class="sxs-lookup"><span data-stu-id="df171-317">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="df171-318">Par exemple, n’utilisez pas de paramètres stockés dans un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="df171-318">For example, do not use settings that are stored in a database file.</span></span>

### <a href="" id="checklistsettingssync"></a><span data-ttu-id="df171-319">Liste de vérification relative à l’évaluation d’applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="df171-319">Checklist for evaluating custom applications</span></span>

<span data-ttu-id="df171-320">Si vous avez décidé de synchroniser les paramètres d’autres applications, vous pouvez utiliser cette liste de vérification pour déterminer les applications que vous incluez.</span><span class="sxs-lookup"><span data-stu-id="df171-320">If you’ve decided that you need settings synchronized for other applications, you can use this checklist to help figure out which applications you’ll include.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="df171-321">Description</span><span class="sxs-lookup"><span data-stu-id="df171-321">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="df171-322">Cette application contient-elle des paramètres que l’utilisateur peut personnaliser?</span><span class="sxs-lookup"><span data-stu-id="df171-322">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="df171-323">Est-il important pour l’utilisateur de synchroniser ces paramètres?</span><span class="sxs-lookup"><span data-stu-id="df171-323">Is it important for the user that these settings are synchronized?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="df171-324">Ces paramètres utilisateur sont-ils déjà gérés par une solution de gestion des applications ou de stratégie de paramètres?</span><span class="sxs-lookup"><span data-stu-id="df171-324">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="df171-325">UE-V applique les paramètres d’application au démarrage de l’application et aux paramètres Windows à l’ouverture de session, le déverrouillage ou la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="df171-325">UE-V applies application settings at application startup and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="df171-326">Si vous utilisez UE-V avec d’autres paramètres de partage de solutions, les utilisateurs peuvent rencontrer des incohérences entre les paramètres synchronisés.</span><span class="sxs-lookup"><span data-stu-id="df171-326">If you use UE-V with other settings sharing solutions, users might experience inconsistency across synchronized settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="df171-327">Les paramètres de l’application sont-ils spécifiques de votre ordinateur?</span><span class="sxs-lookup"><span data-stu-id="df171-327">Are the application settings specific to the computer?</span></span> <span data-ttu-id="df171-328">Les préférences et personnalisations apportées aux applications qui sont associées à des configurations matérielles ou spécifiques à des ordinateurs ne sont pas synchronisées uniformément entre les sessions et peuvent entraîner une mauvaise application de l’application.</span><span class="sxs-lookup"><span data-stu-id="df171-328">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently synchronize across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="df171-329">Est-ce que les paramètres du Windows Store se trouvent dans le dossier Program Files ou dans le répertoire de fichiers qui se trouve dans le répertoire <strong> utilisateurs </strong> [nom d’utilisateur] &lt; Strong &gt; </strong> &lt; &gt; LocalLow </strong> Annuaire fort?</span><span class="sxs-lookup"><span data-stu-id="df171-329">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong>[User name]&lt;strong&gt;AppData</strong>&lt;strong&gt;LocalLow</strong> directory?</span></span> <span data-ttu-id="df171-330">Les données d’application stockées dans l’un de ces emplacements ne doivent généralement pas être synchronisées avec l’utilisateur, dans la mesure où ces données sont spécifiques de l’ordinateur ou que les données sont trop volumineuses pour être synchronisées.</span><span class="sxs-lookup"><span data-stu-id="df171-330">Application data that is stored in either of these locations usually should not synchronize with the user, because this data is specific to the computer or because the data is too large to synchronize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="df171-331">L’application stocke-t-elle des paramètres dans un fichier qui contient d’autres données d’application qui ne doivent pas être synchronisées?</span><span class="sxs-lookup"><span data-stu-id="df171-331">Does the application store any settings in a file that contains other application data that should not synchronize?</span></span> <span data-ttu-id="df171-332">UE-V synchronise les fichiers comme une seule unité.</span><span class="sxs-lookup"><span data-stu-id="df171-332">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="df171-333">Si les paramètres sont stockés dans des fichiers qui incluent des données d’application autres que des paramètres, la synchronisation de ces données supplémentaires peut entraîner une médiocre application.</span><span class="sxs-lookup"><span data-stu-id="df171-333">If settings are stored in files that include application data other than settings, then synchronizing this additional data can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="df171-334">Quelle est la taille des fichiers contenant les paramètres?</span><span class="sxs-lookup"><span data-stu-id="df171-334">How large are the files that contain the settings?</span></span> <span data-ttu-id="df171-335">Les performances de la synchronisation des paramètres peuvent être affectées par de gros fichiers.</span><span class="sxs-lookup"><span data-stu-id="df171-335">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="df171-336">L’inclusion de fichiers volumineux peut affecter les performances de la synchronisation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="df171-336">Including large files can affect the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a><span data-ttu-id="df171-337">Autres considérations relatives à la préparation d’un déploiement UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-337">Other Considerations when Preparing a UE-V Deployment</span></span>


<span data-ttu-id="df171-338">Vous devez également tenir compte des éléments suivants lorsque vous préparez le déploiement d’UE-V:</span><span class="sxs-lookup"><span data-stu-id="df171-338">You should also consider these things when you are preparing to deploy UE-V:</span></span>

-   [<span data-ttu-id="df171-339">Gestion de la synchronisation des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="df171-339">Managing credentials synchronization</span></span>](#creds)

-   [<span data-ttu-id="df171-340">Synchronisation des paramètres d’application Windows</span><span class="sxs-lookup"><span data-stu-id="df171-340">Windows app settings synchronization</span></span>](#appxsettings)

-   [<span data-ttu-id="df171-341">Modèles d’emplacement des paramètres d’UE-V personnalisés</span><span class="sxs-lookup"><span data-stu-id="df171-341">Custom UE-V settings location templates</span></span>](#custom)

-   [<span data-ttu-id="df171-342">Configurations involontaires des paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="df171-342">Unintentional user settings configurations</span></span>](#prevent)

-   [<span data-ttu-id="df171-343">Performances et capacités</span><span class="sxs-lookup"><span data-stu-id="df171-343">Performance and capacity</span></span>](#capacity)

-   [<span data-ttu-id="df171-344">Haute disponibilité</span><span class="sxs-lookup"><span data-stu-id="df171-344">High availability</span></span>](#high)

-   [<span data-ttu-id="df171-345">Synchronisation de l’horloge de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="df171-345">Computer clock synchronization</span></span>](#clocksync)

### <a href="" id="creds"></a><span data-ttu-id="df171-346">Gestion de la synchronisation des informations d’identification dans UE-V 2,1 et UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="df171-346">Managing credentials synchronization in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="df171-347">Dans de nombreuses applications d’entreprise, notamment Microsoft Outlook et Lync, invitez les utilisateurs à entrer leurs informations d’identification de domaine au moment de la connexion.</span><span class="sxs-lookup"><span data-stu-id="df171-347">Many enterprise applications, including Microsoft Outlook and Lync, prompt users for their domain credentials at login.</span></span> <span data-ttu-id="df171-348">Les utilisateurs ont la possibilité d’enregistrer leurs informations d’identification sur le disque pour éviter d’avoir à les entrer à chaque ouverture de ces applications.</span><span class="sxs-lookup"><span data-stu-id="df171-348">Users have the option of saving their credentials to disk to prevent having to enter them every time they open these applications.</span></span> <span data-ttu-id="df171-349">L’activation de la synchronisation des informations d’identification d’itinérance permet aux utilisateurs d’enregistrer leurs informations d’identification sur un ordinateur et de ne pas les retaper sur chaque ordinateur qu’ils utilisent dans leur environnement.</span><span class="sxs-lookup"><span data-stu-id="df171-349">Enabling roaming credentials synchronization lets users save their credentials on one computer and avoid re-entering them on every computer they use in their environment.</span></span> <span data-ttu-id="df171-350">Les utilisateurs peuvent synchroniser certaines informations d’identification de domaine avec UE-V 2,1 et 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="df171-350">Users can synchronize some domain credentials with UE-V 2.1 and 2.1 SP1.</span></span>

**<span data-ttu-id="df171-351">Important</span><span class="sxs-lookup"><span data-stu-id="df171-351">Important</span></span>**  
<span data-ttu-id="df171-352">La synchronisation des informations d’identification est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="df171-352">Credentials synchronization is disabled by default.</span></span> <span data-ttu-id="df171-353">Pour implémenter cette fonctionnalité, vous devez activer la synchronisation des informations d’identification de manière explicite lors du déploiement.</span><span class="sxs-lookup"><span data-stu-id="df171-353">You must explicitly enable credentials synchronization during deployment to implement this feature.</span></span>



<span data-ttu-id="df171-354">UE-V 2,1 et 2,1 SP1 peuvent synchroniser les informations d’identification d’entreprise, mais pas les informations d’identification destinées à être utilisées uniquement sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="df171-354">UE-V 2.1 and 2.1 SP1 can synchronize enterprise credentials, but do not roam credentials intended only for use on the local computer.</span></span>

<span data-ttu-id="df171-355">Les informations d’identification sont des paramètres synchrones, ce qui signifie qu’elles s’appliquent à votre profil la première fois que vous vous connectez à votre ordinateur après la synchronisation d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-355">Credentials are synchronous settings, meaning they are applied to your profile the first time you log in to your computer after UE-V synchronizes.</span></span>

<span data-ttu-id="df171-356">La synchronisation des informations d’identification est gérée par son propre modèle d’emplacement des paramètres, qui est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="df171-356">Credentials synchronization is managed by its own settings location template, which is disabled by default.</span></span> <span data-ttu-id="df171-357">Vous pouvez activer ou désactiver ce modèle par le biais des méthodes utilisées pour les autres modèles.</span><span class="sxs-lookup"><span data-stu-id="df171-357">You can enable or disable this template through the same methods used for other templates.</span></span> <span data-ttu-id="df171-358">L’identificateur de modèle de cette fonctionnalité est RoamingCredentialSettings.</span><span class="sxs-lookup"><span data-stu-id="df171-358">The template identifier for this feature is RoamingCredentialSettings.</span></span>

**<span data-ttu-id="df171-359">Important</span><span class="sxs-lookup"><span data-stu-id="df171-359">Important</span></span>**  
<span data-ttu-id="df171-360">Si vous utilisez l’itinérance d’informations d’identification Active Directory dans votre environnement, nous vous recommandons de ne pas activer le modèle d’itinérance d’informations d’identification d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-360">If you are using Active Directory Credential Roaming in your environment, we recommend that you don’t enable the UE-V credential roaming template.</span></span>



<span data-ttu-id="df171-361">Pour activer la synchronisation des informations d’identification, utilisez l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="df171-361">Use one of these methods to enable credentials synchronization:</span></span>

-   <span data-ttu-id="df171-362">Centre de paramètres de la société</span><span class="sxs-lookup"><span data-stu-id="df171-362">Company Settings Center</span></span>

-   <span data-ttu-id="df171-363">PowerShell</span><span class="sxs-lookup"><span data-stu-id="df171-363">PowerShell</span></span>

-   <span data-ttu-id="df171-364">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="df171-364">Group Policy</span></span>

**<span data-ttu-id="df171-365">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-365">Note</span></span>**  
<span data-ttu-id="df171-366">Les informations d’identification sont chiffrées lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="df171-366">Credentials are encrypted during synchronization.</span></span>



<span data-ttu-id="df171-367">[Centre de paramètres de l’entreprise](https://technet.microsoft.com/library/dn458903.aspx)**:** activez la case à cocher paramètres d’informations d’identification d’itinérance sous Paramètres Windows pour activer la synchronisation des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="df171-367">[Company Settings Center](https://technet.microsoft.com/library/dn458903.aspx)**:** Check the Roaming Credential Settings check box under Windows Settings to enable credential synchronization.</span></span> <span data-ttu-id="df171-368">Décochez la case pour la désactiver.</span><span class="sxs-lookup"><span data-stu-id="df171-368">Uncheck the box to disable it.</span></span> <span data-ttu-id="df171-369">Cette case à cocher apparaît dans le centre de paramètres de la société uniquement si votre compte n’est pas configuré pour synchroniser les paramètres à l’aide d’un compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="df171-369">This check box only appears in Company Settings Center if your account is not configured to synchronize settings using a Microsoft Account.</span></span>

<span data-ttu-id="df171-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** cette applet de méthode PowerShell autorise la synchronisation des informations d’identification:</span><span class="sxs-lookup"><span data-stu-id="df171-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** This PowerShell cmdlet enables credential synchronization:</span></span>

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="df171-371">Cette applet de connexion PowerShell désactive la synchronisation des informations d’identification:</span><span class="sxs-lookup"><span data-stu-id="df171-371">This PowerShell cmdlet disables credential synchronization:</span></span>

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="df171-372">[Stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx)**:** vous devez [déployer le dernier modèle ADMX MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393944) pour activer la synchronisation des informations d’identification via une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="df171-372">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You must [deploy the latest MDOP ADMX template](https://go.microsoft.com/fwlink/p/?LinkId=393944) to enable credential synchronization through group policy.</span></span> <span data-ttu-id="df171-373">La synchronisation des informations d’identification est gérée à l’aide des paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="df171-373">Credentials synchronization is managed with the Windows settings.</span></span> <span data-ttu-id="df171-374">Pour gérer cette fonctionnalité avec une stratégie de groupe, activez la stratégie de synchronisation des paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="df171-374">To manage this feature with Group Policy, enable the Synchronize Windows settings policy.</span></span>

1.  <span data-ttu-id="df171-375">Ouvrez l’éditeur de stratégies de groupe et naviguez jusqu’à **Configuration utilisateur-modèles d’administration-Composants Windows-virtualisation**de l’utilisation de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="df171-375">Open Group Policy Editor and navigate to **User Configuration – Administrative Templates – Windows Components – Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="df171-376">Double-cliquez sur **synchroniser les paramètres Windows**.</span><span class="sxs-lookup"><span data-stu-id="df171-376">Double-click on **Synchronize Windows settings**.</span></span>

3.  <span data-ttu-id="df171-377">Si cette stratégie est activée, vous pouvez activer la synchronisation des informations d’identification en activant la case à cocher **informations d’identification d’itinérance** , ou désactiver la synchronisation des informations d’identification en la désactivant.</span><span class="sxs-lookup"><span data-stu-id="df171-377">If this policy is enabled, you can enable credentials synchronization by checking the **Roaming Credentials** check box, or disable credentials synchronization by unchecking it.</span></span>

4.  <span data-ttu-id="df171-378">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="df171-378">Click **OK**.</span></span>

### <span data-ttu-id="df171-379">Emplacement des informations d’identification synchronisées par UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-379">Credential locations synchronized by UE-V</span></span>

<span data-ttu-id="df171-380">Les fichiers d’informations d’identification enregistrés par les applications dans les emplacements suivants sont synchronisés:</span><span class="sxs-lookup"><span data-stu-id="df171-380">Credential files saved by applications into the following locations are synchronized:</span></span>

-   <span data-ttu-id="df171-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span><span class="sxs-lookup"><span data-stu-id="df171-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span></span>\\

-   <span data-ttu-id="df171-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span><span class="sxs-lookup"><span data-stu-id="df171-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span></span>\\

-   <span data-ttu-id="df171-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span><span class="sxs-lookup"><span data-stu-id="df171-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span></span>\\

-   <span data-ttu-id="df171-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span><span class="sxs-lookup"><span data-stu-id="df171-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span></span>\\

<span data-ttu-id="df171-385">Les informations d’identification enregistrées dans d’autres emplacements ne sont pas synchronisées par UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-385">Credentials saved to other locations are not synchronized by UE-V.</span></span>

### <a href="" id="appxsettings"></a><span data-ttu-id="df171-386">Synchronisation des paramètres d’application Windows</span><span class="sxs-lookup"><span data-stu-id="df171-386">Windows app settings synchronization</span></span>

<span data-ttu-id="df171-387">UE-V gère la synchronisation des paramètres d’application Windows de trois manières:</span><span class="sxs-lookup"><span data-stu-id="df171-387">UE-V manages Windows app settings synchronization in three ways:</span></span>

-   <span data-ttu-id="df171-388">**Synchroniser les applications Windows:** Autoriser ou refuser une synchronisation d’applications Windows</span><span class="sxs-lookup"><span data-stu-id="df171-388">**Sync Windows Apps:** Allow or deny any Windows app synchronization</span></span>

-   <span data-ttu-id="df171-389">**Liste des applications Windows:** Synchroniser une liste d’applications Windows</span><span class="sxs-lookup"><span data-stu-id="df171-389">**Windows App List:** Synchronize a list of Windows apps</span></span>

-   <span data-ttu-id="df171-390">**Comportement de synchronisation par défaut non répertorié:** Déterminez le comportement de synchronisation des applications Windows qui ne figurent pas dans la liste des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="df171-390">**Unlisted Default Sync Behavior:** Determine the synchronization behavior of Windows apps that are not in the Windows app list.</span></span>

<span data-ttu-id="df171-391">Pour plus d’informations, consultez la [liste des applications Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="df171-391">For more information, see the [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

### <a href="" id="custom"></a><span data-ttu-id="df171-392">Modèles d’emplacement des paramètres d’UE-V personnalisés</span><span class="sxs-lookup"><span data-stu-id="df171-392">Custom UE-V settings location templates</span></span>

<span data-ttu-id="df171-393">Si vous déployez UE-V pour synchroniser les paramètres des applications personnalisées, vous devez utiliser le générateur UE-V pour créer des modèles d’emplacement des paramètres personnalisés pour ces applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="df171-393">If you are deploying UE-V to synchronize settings for custom applications, you will use the UE-V Generator to create custom settings location templates for those desktop applications.</span></span> <span data-ttu-id="df171-394">Après avoir créé et testé un modèle d’emplacement des paramètres personnalisés dans un environnement de test, vous pouvez déployer les modèles d’emplacement des paramètres sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="df171-394">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="df171-395">Les modèles d’emplacement des paramètres personnalisés doivent être déployés avec une infrastructure de déploiement existante (par exemple, une méthode de distribution de logiciels d’entreprise) telle que System Center Configuration Manager, des préférences ou en configurant un catalogue de modèles de paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-395">Custom settings location templates must be deployed with an existing deployment infrastructure, like an enterprise software distribution (ESD) method such as System Center Configuration Manager, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="df171-396">Les modèles déployés à l’aide de Configuration Manager ou d’une stratégie de groupe doivent être enregistrés à l’aide d’UE-V WMI ou de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="df171-396">Templates that are deployed with Configuration Manager or Group Policy must be registered by using UE-V WMI or Windows PowerShell.</span></span>

<span data-ttu-id="df171-397">Pour plus d’informations sur les modèles d’emplacement des paramètres personnalisés, voir [déployer UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="df171-397">For more information about custom settings location templates, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span> <span data-ttu-id="df171-398">Pour plus d’informations sur l’utilisation de UE-V avec Configuration Manager, voir [configuration d’UE-v 2. x avec System Center Configuration manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="df171-398">For more information about using UE-V with Configuration Manager, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

### <a href="" id="prevent"></a><span data-ttu-id="df171-399">Empêcher la configuration involontaire des paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="df171-399">Prevent unintentional user settings configuration</span></span>

<span data-ttu-id="df171-400">UE-V télécharge les nouvelles informations de paramètres utilisateur à partir d’un emplacement de stockage des paramètres et applique les paramètres à l’ordinateur local dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="df171-400">UE-V downloads new user settings information from a settings storage location and applies the settings to the local computer in these instances:</span></span>

-   <span data-ttu-id="df171-401">Chaque fois qu’une application est démarrée et dispose d’un modèle UE-V enregistré.</span><span class="sxs-lookup"><span data-stu-id="df171-401">Every time an application is started that has a registered UE-V template.</span></span>

-   <span data-ttu-id="df171-402">Lorsqu’un utilisateur ouvre une session sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="df171-402">When a user logs on to a computer.</span></span>

-   <span data-ttu-id="df171-403">Lorsqu’un utilisateur déverrouille un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="df171-403">When a user unlocks a computer.</span></span>

-   <span data-ttu-id="df171-404">Lorsqu’une connexion est établie à un ordinateur de bureau distant sur lequel UE-V est installé.</span><span class="sxs-lookup"><span data-stu-id="df171-404">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

-   <span data-ttu-id="df171-405">Lors de l’exécution de la tâche planifiée du contrôleur de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="df171-405">When the Sync Controller Application scheduled task is run.</span></span>

<span data-ttu-id="df171-406">Si UE-V est installé sur l’ordinateur A et l’ordinateur B et les paramètres que vous voulez pour l’application se trouvent sur l’ordinateur A, l’ordinateur a doit d’abord ouvrir et fermer l’application.</span><span class="sxs-lookup"><span data-stu-id="df171-406">If UE-V is installed on computer A and computer B, and the settings that you want for the application are on computer A, then computer A should open and close the application first.</span></span> <span data-ttu-id="df171-407">Si l’application est ouverte et fermée sur l’ordinateur B, vous devez d’abord les paramètres de l’application sur l’ordinateur A configurés sur les paramètres de l’application sur l’ordinateur B. les paramètres sont synchronisés entre les ordinateurs en fonction de chaque application.</span><span class="sxs-lookup"><span data-stu-id="df171-407">If the application is opened and closed on computer B first, then the application settings on computer A are configured to the application settings on computer B. Settings are synchronized between computers on per-application basis.</span></span> <span data-ttu-id="df171-408">Dans le temps, les paramètres deviennent cohérents entre les ordinateurs tels qu’ils sont ouverts et fermés grâce aux paramètres préférés.</span><span class="sxs-lookup"><span data-stu-id="df171-408">Over time, settings become consistent between computers as they are opened and closed with preferred settings.</span></span>

<span data-ttu-id="df171-409">Ce scénario s’applique également aux paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="df171-409">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="df171-410">Si les paramètres Windows sur l’ordinateur B doivent être identiques aux paramètres Windows sur l’ordinateur A, l’utilisateur doit se connecter et se déconnecter de l’ordinateur A.</span><span class="sxs-lookup"><span data-stu-id="df171-410">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should log on and log off computer A first.</span></span>

<span data-ttu-id="df171-411">Si les paramètres utilisateur que l’utilisateur souhaite appliquer dans un ordre incorrect, ils peuvent être récupérés en effectuant une opération de restauration pour la configuration de l’application ou de Windows spécifique sur l’ordinateur sur lequel les paramètres ont été écrasés.</span><span class="sxs-lookup"><span data-stu-id="df171-411">If the user settings that the user wants are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="df171-412">Pour plus d’informations, reportez-vous à [gérer la sauvegarde et la restauration d’administration dans UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span><span class="sxs-lookup"><span data-stu-id="df171-412">For more information, see [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span></span>

### <a href="" id="capacity"></a><span data-ttu-id="df171-413">Planification des performances et de la capacité</span><span class="sxs-lookup"><span data-stu-id="df171-413">Performance and capacity planning</span></span>

<span data-ttu-id="df171-414">Spécifiez vos exigences pour UE-V avec la capacité de disque standard et la surveillance de l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="df171-414">Specify your requirements for UE-V with standard disk capacity and network health monitoring.</span></span>

<span data-ttu-id="df171-415">UE-V utilise un partage SMB (Server Message Block) pour le stockage des packages de paramètres.</span><span class="sxs-lookup"><span data-stu-id="df171-415">UE-V uses a Server Message Block (SMB) share for the storage of settings packages.</span></span> <span data-ttu-id="df171-416">La taille des packages varie en fonction des informations de configuration de chaque application.</span><span class="sxs-lookup"><span data-stu-id="df171-416">The size of settings packages varies depending on the settings information for each application.</span></span> <span data-ttu-id="df171-417">Bien que la plupart des packages de paramètres soient petits, la synchronisation de fichiers potentiellement volumineux, tels que les images de bureau, peut entraîner une médiocre performance, en particulier sur les réseaux plus lents.</span><span class="sxs-lookup"><span data-stu-id="df171-417">While most settings packages are small, the synchronization of potentially large files, such as desktop images, can result in poor performance, particularly on slower networks.</span></span>

<span data-ttu-id="df171-418">Pour réduire les problèmes liés à la latence du réseau, créez des emplacements de stockage des paramètres sur les mêmes réseaux locaux où résident les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="df171-418">To reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="df171-419">Nous vous recommandons d’utiliser 20 Mo d’espace disque par utilisateur pour l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="df171-419">We recommend 20 MB of disk space per user for the settings storage location.</span></span>

<span data-ttu-id="df171-420">Par défaut, la synchronisation UE-V a expiré après 2 secondes pour éviter un décalage excessif en raison d’un grand nombre de packages de paramètres volumineux.</span><span class="sxs-lookup"><span data-stu-id="df171-420">By default, UE-V synchronization times out after 2 seconds to prevent excessive lag due to a large settings package.</span></span> <span data-ttu-id="df171-421">Vous pouvez configurer le paramètre PowerSchool = SyncProvider à l’aide d' [objets de stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx).</span><span class="sxs-lookup"><span data-stu-id="df171-421">You can configure the SyncMethod=SyncProvider setting by using [Group Policy Objects](https://technet.microsoft.com/library/dn458893.aspx).</span></span>

### <a href="" id="high"></a><span data-ttu-id="df171-422">Haute disponibilité pour UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-422">High Availability for UE-V</span></span>

<span data-ttu-id="df171-423">L’emplacement de stockage des paramètres d’UE-V et le catalogue de modèles de paramètres prennent en charge le stockage des données utilisateur sur tout partage accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="df171-423">The UE-V settings storage location and settings template catalog support storing user data on any writable share.</span></span> <span data-ttu-id="df171-424">Pour garantir une haute disponibilité, utilisez les critères suivants:</span><span class="sxs-lookup"><span data-stu-id="df171-424">To ensure high availability, follow these criteria:</span></span>

-   <span data-ttu-id="df171-425">Mettre en forme le volume de stockage à l’aide d’un système de fichiers NTFS;</span><span class="sxs-lookup"><span data-stu-id="df171-425">Format the storage volume with an NTFS file system.</span></span>

-   <span data-ttu-id="df171-426">Le partage peut utiliser le système de fichiers DFS, mais il existe des restrictions.</span><span class="sxs-lookup"><span data-stu-id="df171-426">The share can use Distributed File System (DFS) but there are restrictions.</span></span>
<span data-ttu-id="df171-427">Plus précisément, la configuration de cible unique de réplication de systèmes de fichiers DFS avec ou sans espace de noms DFS-N) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df171-427">Specifically, Distributed File System Replication (DFS-R) single target configuration with or without a Distributed File System Namespace (DFS-N) is supported.</span></span>
<span data-ttu-id="df171-428">De même, seule une configuration de cible unique est prise en charge avec le système de fichiers DFS-N.</span><span class="sxs-lookup"><span data-stu-id="df171-428">Likewise, only single target configuration is supported with DFS-N.</span></span>
<span data-ttu-id="df171-429">Pour plus d’informations, consultez [l’énoncé de support de Microsoft relatif aux données de profil utilisateur répliquées](https://go.microsoft.com/fwlink/p/?LinkId=313991) ainsi que des [informations sur la politique de support Microsoft pour un scénario de déploiement DFS-R et DFS-N](https://support.microsoft.com/kb/2533009).</span><span class="sxs-lookup"><span data-stu-id="df171-429">For detailed information, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://go.microsoft.com/fwlink/p/?LinkId=313991) and also [Information about Microsoft support policy for a DFS-R and DFS-N deployment scenario](https://support.microsoft.com/kb/2533009).</span></span>

    <span data-ttu-id="df171-430">Par ailleurs, dans la mesure où SYSVOL utilise le système de fichiers DFS-R pour la réplication, SYSVOL ne peut pas être utilisé pour la réplication de fichier de données UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-430">In addition, because SYSVOL uses DFS-R for replication, SYSVOL cannot be used for UE-V data file replication.</span></span>

-   <span data-ttu-id="df171-431">Configurez les autorisations de partage et les listes de contrôle d’accès NTFS (ACL) comme indiqué dans [la section déploiement de l’emplacement de stockage des paramètres pour UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span><span class="sxs-lookup"><span data-stu-id="df171-431">Configure the share permissions and NTFS access control lists (ACLs) as specified in [Deploying the Settings Storage Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span></span>

-   <span data-ttu-id="df171-432">Utilisez la fonction de regroupement de serveurs de fichiers avec l’agent UE-V pour donner accès à des copies de données d’état utilisateur en cas d’échec des communications.</span><span class="sxs-lookup"><span data-stu-id="df171-432">Use file server clustering along with the UE-V Agent to provide access to copies of user state data in the event of communications failures.</span></span>

-   <span data-ttu-id="df171-433">Vous pouvez stocker les paramètres de données de chemin de stockage de paramètres (données utilisateur) et de modèles de catalogue de modèles sur les partages groupés, sur les partages DFS-N, ou sur les deux.</span><span class="sxs-lookup"><span data-stu-id="df171-433">You can store the settings storage path data (user data) and settings template catalog templates on clustered shares, on DFS-N shares, or on both.</span></span>

### <a href="" id="clocksync"></a><span data-ttu-id="df171-434">Synchroniser les horloges de l’ordinateur pour la synchronisation des paramètres d’UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-434">Synchronize computer clocks for UE-V settings synchronization</span></span>

<span data-ttu-id="df171-435">Les ordinateurs qui exécutent l’agent UE-V doivent utiliser un serveur de temps pour garantir une utilisation homogène des paramètres.</span><span class="sxs-lookup"><span data-stu-id="df171-435">Computers that run the UE-V Agent must use a time server to maintain a consistent settings experience.</span></span> <span data-ttu-id="df171-436">UE-V utilise des horodatages pour déterminer si les paramètres doivent être synchronisés à partir de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="df171-436">UE-V uses time stamps to determine if settings must be synchronized from the settings storage location.</span></span> <span data-ttu-id="df171-437">Si l’horloge de l’ordinateur est incorrecte, les paramètres plus anciens peuvent remplacer les paramètres plus récents, ou les nouveaux paramètres peuvent ne pas être enregistrés dans l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="df171-437">If the computer clock is inaccurate, older settings can overwrite newer settings, or the new settings might not be saved to the settings storage location.</span></span>

## <a href="" id="prereqs"></a><span data-ttu-id="df171-438">Confirmer les conditions préalables et les configurations prises en charge pour UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-438">Confirm Prerequisites and Supported Configurations for UE-V</span></span>


<span data-ttu-id="df171-439">Avant de continuer, assurez-vous que votre environnement inclut les exigences requises pour exécuter UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-439">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

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
<th align="left"><strong><span data-ttu-id="df171-440">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="df171-440">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="df171-441">Édition</span><span class="sxs-lookup"><span data-stu-id="df171-441">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="df171-442">Service Pack</span><span class="sxs-lookup"><span data-stu-id="df171-442">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="df171-443">Architecture système</span><span class="sxs-lookup"><span data-stu-id="df171-443">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="df171-444">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="df171-444">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="df171-445">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="df171-445">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df171-446">Windows7</span><span class="sxs-lookup"><span data-stu-id="df171-446">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-447">Edition intégrale, entreprise ou édition professionnelle</span><span class="sxs-lookup"><span data-stu-id="df171-447">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-448">SP1</span><span class="sxs-lookup"><span data-stu-id="df171-448">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-449">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="df171-449">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-450">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df171-450">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-451">.NET Framework 4,5 ou version ultérieure pour UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="df171-451">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="df171-452">.NET Framework 4 ou version ultérieure pour UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="df171-452">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df171-453">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="df171-453">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-454">Standard, entreprise, Datacenter ou serveur Web</span><span class="sxs-lookup"><span data-stu-id="df171-454">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-455">SP1</span><span class="sxs-lookup"><span data-stu-id="df171-455">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-456">64 bits</span><span class="sxs-lookup"><span data-stu-id="df171-456">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-457">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df171-457">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-458">.NET Framework 4,5 ou version ultérieure pour UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="df171-458">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="df171-459">.NET Framework 4 ou version ultérieure pour UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="df171-459">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df171-460">Windows 8 et Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="df171-460">Windows 8 and Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-461">Entreprise ou professionnel</span><span class="sxs-lookup"><span data-stu-id="df171-461">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-462">None</span><span class="sxs-lookup"><span data-stu-id="df171-462">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-463">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="df171-463">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-464">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df171-464">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-465">.NET Framework 4,5 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df171-465">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df171-466">Windows 10, version pré-1607</span><span class="sxs-lookup"><span data-stu-id="df171-466">Windows 10, pre-1607 version</span></span></p>
<div class="alert">
<strong><span data-ttu-id="df171-467">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-467">Note</span></span></strong><br/><p><span data-ttu-id="df171-468">Seule UE-V 2,1 SP1 prend en charge Windows 10, version antérieure-1607</span><span class="sxs-lookup"><span data-stu-id="df171-468">Only UE-V 2.1 SP1 supports Windows 10, pre-1607 version</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="df171-469">Entreprise ou professionnel</span><span class="sxs-lookup"><span data-stu-id="df171-469">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-470">None</span><span class="sxs-lookup"><span data-stu-id="df171-470">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-471">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="df171-471">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-472">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df171-472">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-473">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="df171-473">.NET Framework 4.6</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df171-474">Windows Server 2012 et Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="df171-474">Windows Server 2012 and Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-475">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="df171-475">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-476">None</span><span class="sxs-lookup"><span data-stu-id="df171-476">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-477">64 bits</span><span class="sxs-lookup"><span data-stu-id="df171-477">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-478">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df171-478">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-479">.NET Framework 4,5 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df171-479">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df171-480">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="df171-480">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-481">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="df171-481">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-482">None</span><span class="sxs-lookup"><span data-stu-id="df171-482">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-483">64 bits</span><span class="sxs-lookup"><span data-stu-id="df171-483">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-484">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df171-484">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="df171-485">.NET Framework 4,6 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df171-485">.NET Framework 4.6 or higher</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="df171-486">En outre...</span><span class="sxs-lookup"><span data-stu-id="df171-486">Also…</span></span>

-   <span data-ttu-id="df171-487">**Licence MDOP:** Cette technologie fait partie du pack d’optimisation de bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="df171-487">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="df171-488">Les clients d’entreprise peuvent obtenir MDOP avec Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="df171-488">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="df171-489">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir comment obtenir MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="df171-489">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="df171-490">**Informations d’identification d’administration** pour les ordinateurs sur lesquels vous allez procéder à l’installation</span><span class="sxs-lookup"><span data-stu-id="df171-490">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

**<span data-ttu-id="df171-491">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-491">Note</span></span>**  

-   <span data-ttu-id="df171-492">À partir de WIndows 10, la version 1607, UE-V est incluse dans [Windows 10 pour les entreprises](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) et ne fait plus partie du pack d’optimisation de bureau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="df171-492">Starting with WIndows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack.</span></span>

-   <span data-ttu-id="df171-493">Dans le cadre de l’activation de .NET Framework 4 ou d’une version ultérieure 3,0, vous devez activer l’option Windows PowerShell d’UE-V de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-493">The UE-V Windows PowerShell feature of the UE-V Agent requires .NET Framework 4 or higher and Windows PowerShell 3.0 or higher to be enabled.</span></span> <span data-ttu-id="df171-494">Téléchargez Windows PowerShell 3,0 [ici](https://go.microsoft.com/fwlink/?LinkId=309609).</span><span class="sxs-lookup"><span data-stu-id="df171-494">Download Windows PowerShell 3.0 [here](https://go.microsoft.com/fwlink/?LinkId=309609).</span></span>

-   <span data-ttu-id="df171-495">Installez .NET Framework 4 ou .NET Framework 4,5 sur les ordinateurs exécutant Windows 7 ou le système d’exploitation Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="df171-495">Install .NET Framework 4 or .NET Framework 4.5 on computers that run the Windows 7 or the Windows Server 2008 R2 operating system.</span></span> <span data-ttu-id="df171-496">.NET Framework 4,5 est fourni avec les systèmes d’exploitation Windows 8, Windows 8,1 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="df171-496">The Windows 8, Windows 8.1, and Windows Server 2012 operating systems come with .NET Framework 4.5 installed.</span></span> <span data-ttu-id="df171-497">Le système d’exploitation Windows 10 est fourni avec .NET Framework 4,6 installé.</span><span class="sxs-lookup"><span data-stu-id="df171-497">The Windows 10 operating system comes with .NET Framework 4.6 installed.</span></span>
-   <span data-ttu-id="df171-498">La stratégie «supprimer le cache d’itinérance» pour les profils obligatoires n’est pas prise en charge avec UE-V et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="df171-498">The “Delete Roaming Cache” policy for Mandatory profiles is not supported with UE-V and should not be used.</span></span>



<span data-ttu-id="df171-499">Il n’existe aucune configuration spéciale de RAM (Random Access Memory) spécifique à UE-V.</span><span class="sxs-lookup"><span data-stu-id="df171-499">There are no special random access memory (RAM) requirements specific to UE-V.</span></span>

### <span data-ttu-id="df171-500">Synchronisation des paramètres via le fournisseur de synchronisation</span><span class="sxs-lookup"><span data-stu-id="df171-500">Synchronization of Settings through the Sync Provider</span></span>

<span data-ttu-id="df171-501">Le fournisseur de synchronisation est le paramètre par défaut pour les utilisateurs qui synchronise un cache local avec l’emplacement de stockage des paramètres dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="df171-501">Sync Provider is the default setting for users, which synchronizes a local cache with the settings storage location in these instances:</span></span>

-   <span data-ttu-id="df171-502">Connexion/déconnexion</span><span class="sxs-lookup"><span data-stu-id="df171-502">Logon/logoff</span></span>

-   <span data-ttu-id="df171-503">Verrouillez/Déverrouillez</span><span class="sxs-lookup"><span data-stu-id="df171-503">Lock/unlock</span></span>

-   <span data-ttu-id="df171-504">Connexion/déconnexion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="df171-504">Remote desktop connect/disconnect</span></span>

-   <span data-ttu-id="df171-505">Ouvrir/fermer l’application</span><span class="sxs-lookup"><span data-stu-id="df171-505">Application open/close</span></span>

<span data-ttu-id="df171-506">Une tâche planifiée gère cette synchronisation des paramètres toutes les 30 minutes ou par le biais de certains événements de déclencheurs pour certaines applications.</span><span class="sxs-lookup"><span data-stu-id="df171-506">A scheduled task manages this synchronization of settings every 30 minutes or through certain trigger events for certain applications.</span></span> <span data-ttu-id="df171-507">Pour plus d’informations, reportez-vous à [modification de la fréquence des tâches planifiées UE-V 2.](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)</span><span class="sxs-lookup"><span data-stu-id="df171-507">For more information, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="df171-508">L’agent UE-V synchronise les paramètres utilisateur pour les ordinateurs qui ne sont pas toujours connectés au réseau d’entreprise (ordinateurs distants et portables) et ceux qui sont toujours connectés au réseau (ordinateurs qui exécutent Windows Server et des sessions VDI (Virtual Desktop interface).</span><span class="sxs-lookup"><span data-stu-id="df171-508">The UE-V Agent synchronizes user settings for computers that are not always connected to the enterprise network (remote computers and laptops) and computers that are always connected to the network (computers that run Windows Server and host virtual desktop interface (VDI) sessions).</span></span>

<span data-ttu-id="df171-509">**Synchronisation pour les ordinateurs disposant de connexions toujours disponibles:** Lorsque vous utilisez UE-V sur des ordinateurs qui sont toujours connectés au réseau, vous devez configurer l’agent UE-V pour synchroniser les paramètres à l’aide du paramètre *PowerSchool = None* , qui traite le serveur de stockage des paramètres comme un partage réseau standard.</span><span class="sxs-lookup"><span data-stu-id="df171-509">**Synchronization for computers with always-available connections:** When you use UE-V on computers that are always connected to the network, you must configure the UE-V Agent to synchronize settings by using the *SyncMethod=None* parameter, which treats the settings storage server as a standard network share.</span></span> <span data-ttu-id="df171-510">Dans cette configuration, l’agent UE-V peut être configuré pour notifier si l’importation des paramètres d’application est retardée.</span><span class="sxs-lookup"><span data-stu-id="df171-510">In this configuration, the UE-V Agent can be configured to notify if the import of the application settings is delayed.</span></span>

<span data-ttu-id="df171-511">Activez cette configuration en utilisant l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="df171-511">Enable this configuration through one of these methods:</span></span>

-   <span data-ttu-id="df171-512">Lors de l’installation d’UE-V, à l’invite de commandes ou dans un fichier de commandes, définissez le paramètre AgentSetup.exe *PowerSchool = aucun*.</span><span class="sxs-lookup"><span data-stu-id="df171-512">During UE-V installation, at the command prompt or in a batch file, set the AgentSetup.exe parameter *SyncMethod = None*.</span></span> <span data-ttu-id="df171-513">[Le déploiement de l’agent UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#agent) fournit des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="df171-513">[Deploying the UE-V 2.x Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more information.</span></span>

-   <span data-ttu-id="df171-514">Après l’installation d’UE-V, utilisez la fonctionnalité de gestion des paramètres de System Center 2012 Configuration Manager ou des modèles ADMX MDOP pour pousser la configuration *PowerSchool = aucune* .</span><span class="sxs-lookup"><span data-stu-id="df171-514">After the UE-V installation, use the Settings Management feature in System Center 2012 Configuration Manager or the MDOP ADMX templates to push the *SyncMethod = None* configuration.</span></span>

-   <span data-ttu-id="df171-515">Utilisez Windows PowerShell ou WMI (Windows Management Instrumentation) pour définir la configuration *PowerSchool = aucune* .</span><span class="sxs-lookup"><span data-stu-id="df171-515">Use Windows PowerShell or Windows Management Instrumentation (WMI) to set the *SyncMethod = None* configuration.</span></span>

    **<span data-ttu-id="df171-516">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-516">Note</span></span>**  
    <span data-ttu-id="df171-517">Ces deux dernières méthodes ne fonctionnent pas pour les environnements VDI (Virtual Desktop Infrastructure) en pool.</span><span class="sxs-lookup"><span data-stu-id="df171-517">These last two methods do not work for pooled virtual desktop infrastructure (VDI) environments.</span></span>



<span data-ttu-id="df171-518">Vous devez redémarrer votre ordinateur pour que les paramètres commencent à être synchronisés.</span><span class="sxs-lookup"><span data-stu-id="df171-518">You must restart the computer before the settings start to synchronize.</span></span>

**<span data-ttu-id="df171-519">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-519">Note</span></span>**  
<span data-ttu-id="df171-520">Si vous définissez *PowerSchool = aucun*, les modifications apportées aux paramètres sont enregistrées directement sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="df171-520">If you set *SyncMethod = None*, any settings changes are saved directly to the server.</span></span> <span data-ttu-id="df171-521">S’il n’y a pas de connexion réseau au chemin de stockage des paramètres, les modifications apportées aux paramètres sont mises en cache sur l’appareil et sont synchronisées lors de la prochaine exécution du fournisseur de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="df171-521">If the network connection to the settings storage path is not found, then the settings changes are cached on the device and are synchronized the next time that the sync provider runs.</span></span> <span data-ttu-id="df171-522">Si le chemin d’accès de stockage des paramètres est introuvable et que le profil utilisateur est supprimé d’un environnement VDI en pool lors de la déconnexion, les modifications apportées aux paramètres sont perdues et l’utilisateur doit réappliquer la modification lors de la reconnexion de l’ordinateur au chemin de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="df171-522">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, settings changes are lost and the user must reapply the change when the computer is reconnected to the settings storage path.</span></span>



<span data-ttu-id="df171-523">**Synchronisation pour les moteurs de synchronisation externes:** Le paramètre *PowerSchool = externe* spécifie que, si les paramètres UE-V sont écrits dans un dossier local sur l’ordinateur de l’utilisateur, tout moteur de synchronisation externe (par exemple, OneDrive entreprise, dossiers de travail, SharePoint ou Dropbox) peut être utilisé pour appliquer ces paramètres aux différents ordinateurs auxquels les utilisateurs accèdent.</span><span class="sxs-lookup"><span data-stu-id="df171-523">**Synchronization for external sync engines:** The *SyncMethod=External* parameter specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

<span data-ttu-id="df171-524">**Support pour les sessions VDI partagées:** UE-V 2,1 et 2,1 SP1 fournissent la prise en charge des sessions VDI partagées entre les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="df171-524">**Support for shared VDI sessions:** UE-V 2.1 and 2.1 SP1 provide support for VDI sessions that are shared among end users.</span></span> <span data-ttu-id="df171-525">Vous pouvez enregistrer et configurer un modèle d’infrastructure VDI spéciale, qui garantit que UE-V conserve toutes ses fonctionnalités intactes pour les sessions VDI non persistantes.</span><span class="sxs-lookup"><span data-stu-id="df171-525">You can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

**<span data-ttu-id="df171-526">Remarque</span><span class="sxs-lookup"><span data-stu-id="df171-526">Note</span></span>**  
<span data-ttu-id="df171-527">Si vous n’activez pas le mode VDI pour les sessions VDI non persistantes, il est possible que certaines fonctionnalités ne fonctionnent pas, telles que [sauvegarde et restauration et dernière bonne qualité connue (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span><span class="sxs-lookup"><span data-stu-id="df171-527">If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as [back-up/restore and last known good (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span></span>



<span data-ttu-id="df171-528">Le modèle VDI est fourni avec UE-V 2,1 et 2,1 SP1 et est en général disponible ici après l’installation: C:\\Program Files\\Microsoft user interface Virtualization\\Templates\\VdiState.xml</span><span class="sxs-lookup"><span data-stu-id="df171-528">The VDI template is provided with UE-V 2.1 and 2.1 SP1 and is typically available here after installation: C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml</span></span>

### <span data-ttu-id="df171-529">Conditions préalables pour la prise en charge du générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="df171-529">Prerequisites for UE-V Generator support</span></span>

<span data-ttu-id="df171-530">Installez le générateur UE-V sur l’ordinateur utilisé pour créer des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="df171-530">Install the UE-V Generator on the computer that is used to create custom settings location templates.</span></span> <span data-ttu-id="df171-531">Cet ordinateur doit être en mesure d’exécuter les applications dont les paramètres sont synchronisés.</span><span class="sxs-lookup"><span data-stu-id="df171-531">This computer should be able to run the applications whose settings are synchronized.</span></span> <span data-ttu-id="df171-532">Vous devez être membre du groupe Administrateurs sur l’ordinateur exécutant le logiciel UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="df171-532">You must be a member of the Administrators group on the computer that runs the UE-V Generator software.</span></span>

<span data-ttu-id="df171-533">UE-V Generator doit être installé sur un ordinateur qui utilise un système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="df171-533">The UE-V Generator must be installed on a computer that uses an NTFS file system.</span></span> <span data-ttu-id="df171-534">Le logiciel de générateur UE-V nécessite .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="df171-534">The UE-V Generator software requires .NET Framework 4.</span></span> <span data-ttu-id="df171-535">Pour plus d’informations, reportez-vous à la rubrique [déploiement d’UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="df171-535">For more information, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <span data-ttu-id="df171-536">Autres ressources pour ce produit</span><span class="sxs-lookup"><span data-stu-id="df171-536">Other resources for this product</span></span>


-   [<span data-ttu-id="df171-537">Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="df171-537">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="df171-538">Prise en main d'UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="df171-538">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="df171-539">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="df171-539">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="df171-540">Résolution des problèmes de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="df171-540">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="df171-541">Informations techniques de référence sur UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="df171-541">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)















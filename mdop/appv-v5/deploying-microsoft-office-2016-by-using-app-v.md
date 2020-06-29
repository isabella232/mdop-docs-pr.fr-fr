---
title: Déploiement de Microsoft Office2016 à l'aide d'App-V
description: Déploiement de Microsoft Office2016 à l'aide d'App-V
author: dansimp
ms.assetid: cc675cde-cb8d-4b7c-a700-6104b78f1d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/25/2017
ms.openlocfilehash: dfedab98e0bdf0a0d5f5e407d9bedadbbf56ad69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805863"
---
# <span data-ttu-id="552e2-103">Déploiement de Microsoft Office2016 à l'aide d'App-V</span><span class="sxs-lookup"><span data-stu-id="552e2-103">Deploying Microsoft Office 2016 by Using App-V</span></span>


<span data-ttu-id="552e2-104">Les informations contenues dans cet article vous permettent d’utiliser Microsoft Application Virtualization 5,0 ou une version ultérieure, de mettre Microsoft Office 2016 en tant qu’application virtualisée sur les ordinateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="552e2-104">Use the information in this article to use Microsoft Application Virtualization 5.0, or later versions, to deliver Microsoft Office 2016 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="552e2-105">Pour plus d’informations sur l’utilisation de App-V pour générer Office 2013, voir [déploiement de Microsoft Office 2013 à l’aide d’App-v](deploying-microsoft-office-2013-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="552e2-105">For information about using App-V to deliver Office 2013, see [Deploying Microsoft Office 2013 by Using App-V](deploying-microsoft-office-2013-by-using-app-v.md).</span></span> <span data-ttu-id="552e2-106">Pour plus d’informations sur l’utilisation de App-V pour générer Office 2010, voir [déploiement de Microsoft Office 2010 à l’aide d’App-v](deploying-microsoft-office-2010-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="552e2-106">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v.md).</span></span>

<span data-ttu-id="552e2-107">Cette rubrique contient les sections suivantes:</span><span class="sxs-lookup"><span data-stu-id="552e2-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="552e2-108">Ce que vous devez savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="552e2-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="552e2-109">Création d’un package 2016 Office pour App-V avec l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="552e2-109">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="552e2-110">Publication du package Office pour App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="552e2-110">Publishing the Office package for App-V 5.0</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="552e2-111">Personnalisation et gestion des packages d’application Office V</span><span class="sxs-lookup"><span data-stu-id="552e2-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="552e2-112">Ce que vous devez savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="552e2-112">What to know before you start</span></span>


<span data-ttu-id="552e2-113">Avant de déployer Office 2016 à l’aide de App-V, passez en revue les informations de planification suivantes.</span><span class="sxs-lookup"><span data-stu-id="552e2-113">Before you deploy Office 2016 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="552e2-114">Versions d’Office et coexistence Office prises en charge</span><span class="sxs-lookup"><span data-stu-id="552e2-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="552e2-115">Utilisez le tableau ci-dessous pour obtenir des informations sur les versions d’Office prises en charge et sur l’exécution des versions coexistantes d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="552e2-116">Informations à réviser</span><span class="sxs-lookup"><span data-stu-id="552e2-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="552e2-117">Description</span><span class="sxs-lookup"><span data-stu-id="552e2-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="552e2-118">Versions prises en charge de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="552e2-118">Supported versions of Microsoft Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="552e2-119">Versions d’Office prises en charge</span><span class="sxs-lookup"><span data-stu-id="552e2-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="552e2-120">Types de déploiement pris en charge (par exemple, un ordinateur de bureau, une infrastructure de bureau virtuel ou un pool d’infrastructure VDI)</span><span class="sxs-lookup"><span data-stu-id="552e2-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="552e2-121">Options de gestion des licences Office</span><span class="sxs-lookup"><span data-stu-id="552e2-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)"><span data-ttu-id="552e2-122">Planification de l’utilisation de App-V avec les versions coexistantes d’Office</span><span class="sxs-lookup"><span data-stu-id="552e2-122">Planning for Using App-V with coexisting versions of Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="552e2-123">Remarques relatives à l’installation de différentes versions d’Office sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="552e2-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="552e2-124">Exigences en matière de création de packages, de publication et de déploiement</span><span class="sxs-lookup"><span data-stu-id="552e2-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="552e2-125">Avant de déployer Office à l’aide de App-V, consultez la configuration requise suivante.</span><span class="sxs-lookup"><span data-stu-id="552e2-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="552e2-126">Tâche</span><span class="sxs-lookup"><span data-stu-id="552e2-126">Task</span></span></th>
<th align="left"><span data-ttu-id="552e2-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="552e2-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="552e2-128">Packages</span><span class="sxs-lookup"><span data-stu-id="552e2-128">Packaging</span></span></p></td>
<td align="left">
<ul>
<li><p><span data-ttu-id="552e2-129">Toutes les applications Office que vous voulez déployer pour les utilisateurs doivent se trouver dans un seul package.</span><span class="sxs-lookup"><span data-stu-id="552e2-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="552e2-130">Dans App-V 5,0 et les versions ultérieures, vous devez utiliser l’outil déploiement d’Office pour créer des packages.</span><span class="sxs-lookup"><span data-stu-id="552e2-130">In App-V 5.0 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="552e2-131">Vous ne pouvez pas utiliser le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="552e2-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="552e2-132">Si vous déployez Microsoft Visio 2016 et Microsoft Project 2016 avec Office, vous devez les inclure dans le même package qu’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-132">If you are deploying Microsoft Visio 2016 and Microsoft Project 2016 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="552e2-133">Pour plus d’informations, reportez-vous à <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> déploiement de Visio 2016 et Project 2016 avec Office </a> .</span><span class="sxs-lookup"><span data-stu-id="552e2-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2016 and Project 2016 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="552e2-134">Publishing</span><span class="sxs-lookup"><span data-stu-id="552e2-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="552e2-135">Vous ne pouvez publier qu’un seul package Office sur chaque ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="552e2-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="552e2-136">Vous devez publier le package Office globalement.</span><span class="sxs-lookup"><span data-stu-id="552e2-136">You must publish the Office package globally.</span></span> <span data-ttu-id="552e2-137">Vous ne pouvez pas publier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="552e2-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="552e2-138">Déploiement de l’un des produits suivants sur un ordinateur partagé, par exemple, à l’aide des services Bureau à distance:</span><span class="sxs-lookup"><span data-stu-id="552e2-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="552e2-139">Applications 365 Microsoft pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="552e2-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="552e2-140">Visio Pro pour Office 365</span><span class="sxs-lookup"><span data-stu-id="552e2-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="552e2-141">Project Pro pour Office 365</span><span class="sxs-lookup"><span data-stu-id="552e2-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="552e2-142">Vous devez activer <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> l’activation d’ordinateurs partagés </a> .</span><span class="sxs-lookup"><span data-stu-id="552e2-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
</td>
</tr>
</tbody>
</table>



### <span data-ttu-id="552e2-143">Exclusion d’applications Office d’un package</span><span class="sxs-lookup"><span data-stu-id="552e2-143">Excluding Office applications from a package</span></span>

<span data-ttu-id="552e2-144">Le tableau suivant décrit les méthodes recommandées pour exclure des applications Office spécifiques d’un package.</span><span class="sxs-lookup"><span data-stu-id="552e2-144">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="552e2-145">Tâche</span><span class="sxs-lookup"><span data-stu-id="552e2-145">Task</span></span></th>
<th align="left"><span data-ttu-id="552e2-146">Détails</span><span class="sxs-lookup"><span data-stu-id="552e2-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="552e2-147">Utilisez le <strong> </strong> paramètre ExcludeApp lorsque vous créez le package à l’aide de l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-147">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="552e2-148">Vous permet d’exclure des applications Office spécifiques du package lorsque l’outil déploiement d’Office crée le package.</span><span class="sxs-lookup"><span data-stu-id="552e2-148">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="552e2-149">Par exemple, vous pouvez utiliser ce paramètre pour créer un package qui contient uniquement Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="552e2-149">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="552e2-150">Pour plus d’informations, consultez <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp élément </a> .</span><span class="sxs-lookup"><span data-stu-id="552e2-150">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="552e2-151">Modifier le fichier DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="552e2-151">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="552e2-152">Modifiez le fichier DeploymentConfig.xml après la création du package.</span><span class="sxs-lookup"><span data-stu-id="552e2-152">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="552e2-153">Ce fichier contient les paramètres de package par défaut pour tous les utilisateurs sur un ordinateur exécutant le client App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-153">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="552e2-154">Pour plus d’informations, reportez-vous à <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> désactivation des applications Office 2016 </a> .</span><span class="sxs-lookup"><span data-stu-id="552e2-154">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)">Disabling Office 2016 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="552e2-155">Création d’un package 2016 Office pour App-V avec l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="552e2-155">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="552e2-156">Suivez les étapes ci-dessous pour créer un package 2016 Office pour App-V 5,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="552e2-156">Complete the following steps to create an Office 2016 package for App-V 5.0 or later.</span></span>

><span data-ttu-id="552e2-157">**Important** &nbsp; Important &nbsp; Dans App-V 5,0 et les versions ultérieures, vous devez utiliser l’outil déploiement d’Office pour créer un package.</span><span class="sxs-lookup"><span data-stu-id="552e2-157">**Important**&nbsp;&nbsp;In App-V 5.0 and later, you must use the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="552e2-158">Vous ne pouvez pas utiliser le Sequencer pour créer des packages.</span><span class="sxs-lookup"><span data-stu-id="552e2-158">You cannot use the Sequencer to create packages.</span></span>

### <span data-ttu-id="552e2-159">Consulter les conditions préalables à l’utilisation de l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="552e2-159">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="552e2-160">Sur l’ordinateur sur lequel vous installez l’outil déploiement d’Office, vous devez disposer des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="552e2-160">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="552e2-161">Prérequises</span><span class="sxs-lookup"><span data-stu-id="552e2-161">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="552e2-162">Description</span><span class="sxs-lookup"><span data-stu-id="552e2-162">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="552e2-163">Logiciels requis</span><span class="sxs-lookup"><span data-stu-id="552e2-163">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="552e2-164">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="552e2-164">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="552e2-165">Systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="552e2-165">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="552e2-166">64-version de Windows 10</span><span class="sxs-lookup"><span data-stu-id="552e2-166">64-bit version of Windows 10</span></span></p></li>
<li><p><span data-ttu-id="552e2-167">version 64 bits de Windows 8 ou 8,1</span><span class="sxs-lookup"><span data-stu-id="552e2-167">64-bit version of Windows 8 or 8.1</span></span></p></li>
<li><p><span data-ttu-id="552e2-168">version 64 bits de Windows 7</span><span class="sxs-lookup"><span data-stu-id="552e2-168">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


><span data-ttu-id="552e2-169">**Remarques**  Dans cette rubrique, le terme «Office 2016 App-V package» fait référence à la gestion des licences d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="552e2-169">**Note**  In this topic, the term “Office 2016 App-V package” refers to subscription licensing.</span></span>


### <span data-ttu-id="552e2-170">Créer des packages App-V d’Office 2016 à l’aide de l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="552e2-170">Create Office 2016 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="552e2-171">Vous pouvez créer des packages App-V d’Office 2016 à l’aide de l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-171">You create Office 2016 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="552e2-172">Les instructions suivantes vous expliquent comment créer un package App-V pour Office 2016 avec les licences d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="552e2-172">The following instructions explain how to create an Office 2016 App-V package with Subscription Licensing.</span></span>

<span data-ttu-id="552e2-173">Créer des packages App-V Office 2016 sur des ordinateurs Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="552e2-173">Create Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="552e2-174">Une fois créé, le package App-V pour Office 2016 s’exécutera 64 32 sur les ordinateurs Windows 7, Windows 8,1 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="552e2-174">Once created, the Office 2016 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="552e2-175">Télécharger l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="552e2-175">Download the Office Deployment Tool</span></span>

<span data-ttu-id="552e2-176">Les packages App-V d’Office 2016 sont créés à l’aide de l’outil déploiement d’Office qui génère un package App-V pour Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-176">Office 2016 App-V Packages are created using the Office Deployment Tool, which generates an Office 2016 App-V Package.</span></span> <span data-ttu-id="552e2-177">Le package ne peut pas être créé ou modifié via le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-177">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="552e2-178">Pour commencer à créer un package:</span><span class="sxs-lookup"><span data-stu-id="552e2-178">To begin package creation:</span></span>

1.  <span data-ttu-id="552e2-179">Télécharger l' [outil déploiement d’Office 2016 pour Office «démarrer en un clic»](https://www.microsoft.com/download/details.aspx?id=49117).</span><span class="sxs-lookup"><span data-stu-id="552e2-179">Download the [Office 2016 Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span>

> <span data-ttu-id="552e2-180">**Important** Vous devez utiliser l’outil déploiement d’Office 2016 pour créer des packages App-V d’Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-180">**Important** You must use the Office 2016 Deployment Tool to create Office 2016 App-V Packages.</span></span>
> 2. <span data-ttu-id="552e2-181">Exécutez le fichier. exe et extrayez ses fonctionnalités dans l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="552e2-181">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="552e2-182">Pour faciliter ce processus, vous pouvez créer un dossier réseau partagé dans lequel les fonctionnalités seront enregistrées.</span><span class="sxs-lookup"><span data-stu-id="552e2-182">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    Example: \\\\Server\\Office2016

3. <span data-ttu-id="552e2-183">Vérifiez qu’il existe une setup.exe et qu’un fichier configuration.xml se trouvent à l’emplacement que vous avez spécifié.</span><span class="sxs-lookup"><span data-stu-id="552e2-183">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="552e2-184">Télécharger les applications Office 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-184">Download Office 2016 applications</span></span>

<span data-ttu-id="552e2-185">Après avoir téléchargé l’outil déploiement d’Office, vous pouvez l’utiliser pour obtenir les dernières applications Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-185">After you download the Office Deployment Tool, you can use it to get the latest Office 2016 applications.</span></span> <span data-ttu-id="552e2-186">Après avoir effectué les applications Office, vous créez le package App-V pour Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-186">After getting the Office applications, you create the Office 2016 App-V package.</span></span>

<span data-ttu-id="552e2-187">Le fichier XML inclus dans l’outil déploiement d’Office spécifie les détails du produit, tels que les langues et les applications Office inclus.</span><span class="sxs-lookup"><span data-stu-id="552e2-187">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1. <span data-ttu-id="552e2-188">**Personnalisez le fichier de configuration XML d’exemple:** Utilisez l’exemple de fichier de configuration XML que vous avez téléchargé auprès de l’outil déploiement d’Office pour personnaliser les applications Office:</span><span class="sxs-lookup"><span data-stu-id="552e2-188">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

   1. <span data-ttu-id="552e2-189">Ouvrez l’exemple de fichier XML dans le bloc-notes ou dans votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="552e2-189">Open the sample XML file in Notepad or your favorite text editor.</span></span>

   2. <span data-ttu-id="552e2-190">L’exemple configuration.xml ouverture et la possibilité de le modifier, vous pouvez spécifier des produits, des langues et le chemin d’accès au dossier dans lequel vous enregistrez les applications Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-190">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2016 applications.</span></span> <span data-ttu-id="552e2-191">Voici un exemple de base du fichier configuration.xml:</span><span class="sxs-lookup"><span data-stu-id="552e2-191">The following is a basic example of the configuration.xml file:</span></span>

      ```xml
      <Configuration>
         <Add SourcePath= "\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      ><span data-ttu-id="552e2-192">**Remarques**  Le fichier XML de configuration est un exemple de fichier XML.</span><span class="sxs-lookup"><span data-stu-id="552e2-192">**Note**  The configuration XML is a sample XML file.</span></span> <span data-ttu-id="552e2-193">Le fichier inclut des lignes commentées. Vous pouvez «ne pas commenter» ces lignes pour personnaliser des paramètres supplémentaires à l’aide du fichier.</span><span class="sxs-lookup"><span data-stu-id="552e2-193">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span> <span data-ttu-id="552e2-194">Pour «annuler commenter» ces traits, supprimez le «<!</span><span class="sxs-lookup"><span data-stu-id="552e2-194">To “uncomment” these lines, remove the "<!</span></span> <span data-ttu-id="552e2-195">--«au début de la ligne» et «-->» à partir de la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="552e2-195">- -" from the beginning of the line, and the "-- >" from the end of the line.</span></span>

      <span data-ttu-id="552e2-196">Le fichier de configuration XML ci-dessus spécifie qu’Office 2016 ProPlus 32-bit Edition, y compris Visio ProPlus, sera téléchargé en anglais vers le \\\\server\\Office 2016, qui est l’emplacement où les applications Office seront enregistrées.</span><span class="sxs-lookup"><span data-stu-id="552e2-196">The above XML configuration file specifies that Office 2016 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2016, which is the location where Office applications will be saved to.</span></span> <span data-ttu-id="552e2-197">Notez que l’ID de produit des applications n’aura aucune incidence sur la licence finale d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-197">Note that the Product ID of the applications will not affect the final licensing of Office.</span></span> <span data-ttu-id="552e2-198">Les packages App-V pour Office 2016 avec différentes licences peuvent être créés à partir des mêmes applications par le biais du mode de gestion de licences à un stade ultérieur.</span><span class="sxs-lookup"><span data-stu-id="552e2-198">Office 2016 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage.</span></span> <span data-ttu-id="552e2-199">Le tableau ci-dessous résume les attributs et éléments personnalisés du fichier XML:</span><span class="sxs-lookup"><span data-stu-id="552e2-199">The table below summarizes the customizable attributes and elements of XML file:</span></span>

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left"><span data-ttu-id="552e2-200">Entrée</span><span class="sxs-lookup"><span data-stu-id="552e2-200">Input</span></span></th>
      <th align="left"><span data-ttu-id="552e2-201">Description</span><span class="sxs-lookup"><span data-stu-id="552e2-201">Description</span></span></th>
      <th align="left"><span data-ttu-id="552e2-202">Exemple</span><span class="sxs-lookup"><span data-stu-id="552e2-202">Example</span></span></th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="552e2-203">Ajouter un élément</span><span class="sxs-lookup"><span data-stu-id="552e2-203">Add element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="552e2-204">Spécifie les produits et les langues à inclure dans le package.</span><span class="sxs-lookup"><span data-stu-id="552e2-204">Specifies the products and languages to include in the package.</span></span></p></td>
      <td align="left"><p><span data-ttu-id="552e2-205">N/A</span><span class="sxs-lookup"><span data-stu-id="552e2-205">N/A</span></span></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="552e2-206">OfficeClientEdition (attribut de l’élément Add)</span><span class="sxs-lookup"><span data-stu-id="552e2-206">OfficeClientEdition (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="552e2-207">Spécifie l’édition d’un produit Office 2016 à utiliser: 32-bit ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="552e2-207">Specifies the edition of Office 2016 product to use: 32-bit or 64-bit.</span></span> <span data-ttu-id="552e2-208">L’opération échoue si <strong> OfficeClientEdition </strong> n’est pas défini sur une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="552e2-208">The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</span></span></p></td>
      <td align="left"><p><strong><span data-ttu-id="552e2-209">OfficeClientEdition </strong> = &quot; 32&quot;</span><span class="sxs-lookup"><span data-stu-id="552e2-209">OfficeClientEdition</strong>=&quot;32&quot;</span></span></p>
      <p><strong><span data-ttu-id="552e2-210">OfficeClientEdition </strong> = &quot; 64&quot;</span><span class="sxs-lookup"><span data-stu-id="552e2-210">OfficeClientEdition</strong>=&quot;64&quot;</span></span></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="552e2-211">Élément Product</span><span class="sxs-lookup"><span data-stu-id="552e2-211">Product element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="552e2-212">Spécifie l’application.</span><span class="sxs-lookup"><span data-stu-id="552e2-212">Specifies the application.</span></span> <span data-ttu-id="552e2-213">Les applications Project 2016 et Visio 2016 doivent être spécifiées ici en tant que produit supplémentaire à inclure dans les applications.</span><span class="sxs-lookup"><span data-stu-id="552e2-213">Project 2016 and Visio 2016 must be specified here as an added product to be included in the applications.</span></span>

      <span data-ttu-id="552e2-214">Pour plus d’informations sur les ID de produit, voir <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> ID de produit pris en charge par l’outil déploiement d’Office pour démarrer en un clic.</span><span class="sxs-lookup"><span data-stu-id="552e2-214">For more information about the product IDs, see <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)">Product IDs that are supported by the Office Deployment Tool for Click-to-Run</span></span></a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="552e2-215">Élément Language</span><span class="sxs-lookup"><span data-stu-id="552e2-215">Language element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="552e2-216">Spécifie la langue prise en charge dans les applications</span><span class="sxs-lookup"><span data-stu-id="552e2-216">Specifies the language supported in the applications</span></span></p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="552e2-217">Version (attribut de l’élément Add)</span><span class="sxs-lookup"><span data-stu-id="552e2-217">Version (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="552e2-218">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="552e2-218">Optional.</span></span> <span data-ttu-id="552e2-219">Spécifie une build à utiliser pour le package.</span><span class="sxs-lookup"><span data-stu-id="552e2-219">Specifies a build to use for the package</span></span></p>
      <p><span data-ttu-id="552e2-220">Utilise par défaut la version publiée la plus récente (telle qu’elle est définie dans v32.CAB au niveau de la source d’Office).</span><span class="sxs-lookup"><span data-stu-id="552e2-220">Defaults to latest advertised build (as defined in v32.CAB at the Office source).</span></span></p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="552e2-221">SourcePath (attribut de l’élément Add)</span><span class="sxs-lookup"><span data-stu-id="552e2-221">SourcePath (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="552e2-222">Spécifie l’emplacement dans lequel les applications seront enregistrées.</span><span class="sxs-lookup"><span data-stu-id="552e2-222">Specifies the location in which the applications will be saved to.</span></span></p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="552e2-223">Canal (attribut de l’élément Add)</span><span class="sxs-lookup"><span data-stu-id="552e2-223">Channel (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="552e2-224">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="552e2-224">Optional.</span></span> <span data-ttu-id="552e2-225">Spécifie le canal de mise à jour pour le produit que vous souhaitez télécharger ou installer.</span><span class="sxs-lookup"><span data-stu-id="552e2-225">Specifies the update channel for the product that you want to download or install.</span></span> </p><p><span data-ttu-id="552e2-226">Pour plus d’informations sur les canaux de mise à jour, voir présentation des canaux de mise à jour des applications 365 Microsoft pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="552e2-226">For more information about update channels, see Overview of update channels for Microsoft 365 Apps for enterprise.</span></span></p></td>
      <td align="left"><p><code>Channel=&quot;Deferred&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      <span data-ttu-id="552e2-227">Après avoir modifié le fichier configuration.xml pour spécifier le produit, les langues et également l’emplacement dans lequel enregistrer les applications 2016 Office, vous pouvez enregistrer le fichier de configuration, par exemple, en tant que Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="552e2-227">After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2016 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.</span></span>

2. <span data-ttu-id="552e2-228">**Téléchargez les applications à l’emplacement spécifié:** Utilisez une invite de commandes avec élévation de privilèges et un système d’exploitation 64 bits pour télécharger les applications Office 2016 qui seront converties ultérieurement en package App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-228">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2016 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="552e2-229">Vous trouverez ci-dessous un exemple de commande avec une description des détails:</span><span class="sxs-lookup"><span data-stu-id="552e2-229">Below is an example command with a description of details:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   <span data-ttu-id="552e2-230">Dans l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="552e2-230">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="552e2-231">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="552e2-231">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-232">est l’emplacement de partage réseau qui contient l’outil déploiement d’Office et le fichier Configuration.xml personnalisé Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="552e2-232">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="552e2-233">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="552e2-233">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-234">est l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-234">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="552e2-235">/Download</span><span class="sxs-lookup"><span data-stu-id="552e2-235">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-236">télécharge les applications Office 2016 que vous spécifiez dans le fichier customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="552e2-236">downloads the Office 2016 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="552e2-237">Ces bits peuvent être convertis ultérieurement dans un package App-V pour Office 2016 avec le programme de licence en volume.</span><span class="sxs-lookup"><span data-stu-id="552e2-237">These bits can be later converted in an Office 2016 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="552e2-238">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="552e2-238">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-239">transmet le fichier de configuration XML requis pour terminer le processus de téléchargement (dans cet exemple, customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="552e2-239">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="552e2-240">Après l’utilisation de la commande Télécharger, les applications Office se trouvent dans l’emplacement spécifié dans le fichier XML de configuration (dans cet exemple, \Server\Office2016.).</span><span class="sxs-lookup"><span data-stu-id="552e2-240">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2016.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="552e2-241">Convertir les applications Office en package App-V</span><span class="sxs-lookup"><span data-stu-id="552e2-241">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="552e2-242">Après avoir téléchargé les applications Office 2016 par le biais de l’outil déploiement d’Office, utilisez l’outil déploiement d’Office pour les convertir en package d’application Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-242">After you download the Office 2016 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2016 App-V package.</span></span> <span data-ttu-id="552e2-243">Suivez les étapes qui correspondent à votre modèle de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="552e2-243">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="552e2-244">Résumé de ce que vous devez faire:</span><span class="sxs-lookup"><span data-stu-id="552e2-244">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="552e2-245">Créez les packages App-V d’Office 2016 sur les ordinateurs Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="552e2-245">Create the Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="552e2-246">Toutefois, le package s’exécutera sur 32 des ordinateurs Windows 7, Windows 8 ou 8,1 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="552e2-246">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8 or 8.1, and Windows 10 computers.</span></span>

-   <span data-ttu-id="552e2-247">Créez un package App-V pour la gestion des licences d’abonnement à l’aide de l’outil déploiement d’Office, puis modifiez le fichier de configuration CustomConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="552e2-247">Create an Office App-V package for Subscription Licensing package by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="552e2-248">Le tableau suivant récapitule les valeurs que vous devez entrer dans le fichier CustomConfig.xml pour le modèle de gestion des licences que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="552e2-248">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="552e2-249">Les étapes des sections qui suivent le tableau spécifient les entrées exactes que vous devez effectuer.</span><span class="sxs-lookup"><span data-stu-id="552e2-249">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

><span data-ttu-id="552e2-250">**Note** &nbsp; Remarques &nbsp; Vous pouvez utiliser l’outil déploiement d’Office pour créer des packages App-V pour les applications Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="552e2-250">**Note**&nbsp;&nbsp;You can use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="552e2-251">La création de packages pour les versions avec licence en volume d’Office professionnel plus ou d’Office standard n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="552e2-251">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="552e2-252">ID produit</span><span class="sxs-lookup"><span data-stu-id="552e2-252">Product ID</span></span></th>
<th align="left"><span data-ttu-id="552e2-253">Licences d’abonnement</span><span class="sxs-lookup"><span data-stu-id="552e2-253">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="552e2-254">Office2016</span><span class="sxs-lookup"><span data-stu-id="552e2-254">Office 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="552e2-255">O365proplusretail)</span><span class="sxs-lookup"><span data-stu-id="552e2-255">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="552e2-256">Office 2016 avec Visio 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-256">Office 2016 with Visio 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="552e2-257">O365proplusretail)</span><span class="sxs-lookup"><span data-stu-id="552e2-257">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="552e2-258">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="552e2-258">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="552e2-259">Office 2016 avec Visio 2016 et Project 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-259">Office 2016 with Visio 2016 and Project 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="552e2-260">O365proplusretail)</span><span class="sxs-lookup"><span data-stu-id="552e2-260">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="552e2-261">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="552e2-261">VisioProRetail</span></span></p>
<p><span data-ttu-id="552e2-262">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="552e2-262">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="552e2-263">Convertir les applications Office en package App-V</span><span class="sxs-lookup"><span data-stu-id="552e2-263">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="552e2-264">Dans le bloc-notes, rouvrez le fichier CustomConfig.xml, puis apportez les modifications suivantes au fichier:</span><span class="sxs-lookup"><span data-stu-id="552e2-264">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="552e2-265">Paramètre</span><span class="sxs-lookup"><span data-stu-id="552e2-265">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="552e2-266">Ce à quoi changer la valeur</span><span class="sxs-lookup"><span data-stu-id="552e2-266">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="552e2-267">Chemin_source</span><span class="sxs-lookup"><span data-stu-id="552e2-267">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="552e2-268">Pointez sur les applications Office téléchargées auparavant.</span><span class="sxs-lookup"><span data-stu-id="552e2-268">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="552e2-269">ProductID</span><span class="sxs-lookup"><span data-stu-id="552e2-269">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="552e2-270">Spécifiez les licences d’abonnement, comme indiqué dans l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="552e2-270">Specify Subscription licensing, as shown in the following example:</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="552e2-271">Dans cet exemple, les modifications suivantes ont été apportées à la création d’un package avec les licences d’abonnement:</span><span class="sxs-lookup"><span data-stu-id="552e2-271">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="552e2-272">Chemin_source</span><span class="sxs-lookup"><span data-stu-id="552e2-272">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-273">est le chemin d’accès, qui a été modifié de sorte qu’il pointe vers les applications Office téléchargées auparavant.</span><span class="sxs-lookup"><span data-stu-id="552e2-273">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="552e2-274">ID produit</span><span class="sxs-lookup"><span data-stu-id="552e2-274">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-275">pour Office a changé en <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="552e2-275">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="552e2-276">ID produit</span><span class="sxs-lookup"><span data-stu-id="552e2-276">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-277">pour Visio a changé en <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="552e2-277">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="552e2-278">ExcludeApp (facultatif)</span><span class="sxs-lookup"><span data-stu-id="552e2-278">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="552e2-279">Vous permet de spécifier les programmes Office que vous ne souhaitez pas inclure dans le package App-V créé par l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-279">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="552e2-280">Par exemple, vous pouvez exclure Access et InfoPath.</span><span class="sxs-lookup"><span data-stu-id="552e2-280">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="552e2-281">PACKAGEGUID (facultatif)</span><span class="sxs-lookup"><span data-stu-id="552e2-281">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="552e2-282">Par défaut, tous les packages App-V créés par l’outil déploiement d’Office partagent le même ID de package App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-282">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="552e2-283">Vous pouvez utiliser PACKAGEGUID pour spécifier un ID de package différent pour chaque package, qui vous permet de publier plusieurs packages App-V, créés par l’outil déploiement d’Office, et de les gérer à l’aide du serveur App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-283">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="552e2-284">Un exemple d’utilisation de ce paramètre est le cas si vous créez des packages différents pour différents utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="552e2-284">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="552e2-285">Par exemple, vous pouvez créer un package uniquement avec Office 2016 pour certains utilisateurs et créer un autre package avec Office 2016 et Visio 2016 pour un autre groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="552e2-285">For example, you can create a package with just Office 2016 for some users, and create another package with Office 2016 and Visio 2016 for another set of users.</span></span></p>
<span data-ttu-id="552e2-286">&gt;<strong>Remarque </strong> même si vous utilisez des ID de package uniques, vous pouvez toujours déployer un seul package App-V sur un seul appareil.</span><span class="sxs-lookup"><span data-stu-id="552e2-286">&gt;<strong>Note</strong> Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span>
   </td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="552e2-287">Utilisez la commande/Packager pour convertir les applications Office en un package App-V pour Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-287">Use the /packager command to convert the Office applications to an Office 2016 App-V package.</span></span>

   <span data-ttu-id="552e2-288">Exemple:</span><span class="sxs-lookup"><span data-stu-id="552e2-288">For example:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   <span data-ttu-id="552e2-289">Dans l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="552e2-289">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="552e2-290">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="552e2-290">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-291">est l’emplacement de partage réseau qui contient l’outil déploiement d’Office et le fichier Configuration.xml personnalisé Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="552e2-291">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="552e2-292">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="552e2-292">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-293">est l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-293">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="552e2-294">/packager</span><span class="sxs-lookup"><span data-stu-id="552e2-294">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-295">crée le package App-V pour Office 2016 avec le type de licence spécifié dans le fichier customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="552e2-295">creates the Office 2016 App-V package with the type of licensing specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="552e2-296">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="552e2-296">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-297">transmet le fichier XML de configuration (dans ce cas, customConfig) qui a été préparé pour la phase d’emballage.</span><span class="sxs-lookup"><span data-stu-id="552e2-297">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="552e2-298">\server\share\Office 2016AppV</span><span class="sxs-lookup"><span data-stu-id="552e2-298">\server\share\Office 2016AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="552e2-299">Spécifie l’emplacement du package Office App-V nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="552e2-299">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="552e2-300">Vérifiez que le package App-V pour Office 2016 fonctionne correctement:</span><span class="sxs-lookup"><span data-stu-id="552e2-300">Verify that the Office 2016 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="552e2-301">Publiez le package App-V pour Office 2016 que vous avez créé dans le monde entier, sur un ordinateur de test et vérifiez que les raccourcis vers Office 2016 apparaissent.</span><span class="sxs-lookup"><span data-stu-id="552e2-301">Publish the Office 2016 App-V package, which you created globally, to a test computer, and verify that the Office 2016 shortcuts appear.</span></span>

   2.  <span data-ttu-id="552e2-302">Démarrez quelques applications Office 2016, telles qu’Excel ou Word, pour vous assurer que votre package fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="552e2-302">Start a few Office 2016 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="552e2-303">Publication du package Office pour App-V</span><span class="sxs-lookup"><span data-stu-id="552e2-303">Publishing the Office package for App-V</span></span>


<span data-ttu-id="552e2-304">Utilisez les informations suivantes pour publier un package Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-304">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="552e2-305">Méthodes de publication des packages App-V d’Office</span><span class="sxs-lookup"><span data-stu-id="552e2-305">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="552e2-306">Déployez le package App-V pour Office 2016 à l’aide des méthodes que vous utilisez pour les autres packages:</span><span class="sxs-lookup"><span data-stu-id="552e2-306">Deploy the App-V package for Office 2016 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="552e2-307">SystemCenterConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="552e2-307">System Center Configuration Manager</span></span>

-   <span data-ttu-id="552e2-308">App-V Server</span><span class="sxs-lookup"><span data-stu-id="552e2-308">App-V Server</span></span>

-   <span data-ttu-id="552e2-309">Commandes PowerShell autonomes</span><span class="sxs-lookup"><span data-stu-id="552e2-309">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="552e2-310">Conditions préalables et configuration requise pour la publication</span><span class="sxs-lookup"><span data-stu-id="552e2-310">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="552e2-311">Conditions préalables ou requises</span><span class="sxs-lookup"><span data-stu-id="552e2-311">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="552e2-312">Détails</span><span class="sxs-lookup"><span data-stu-id="552e2-312">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="552e2-313">Activer les scripts PowerShell sur les clients App-V</span><span class="sxs-lookup"><span data-stu-id="552e2-313">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="552e2-314">Pour publier des packages Office 2016, vous devez exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="552e2-314">To publish Office 2016 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="552e2-315">Par défaut, les scripts de package sont désactivés sur les clients App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-315">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="552e2-316">Pour activer les scripts, exécutez la commande PowerShell suivante:</span><span class="sxs-lookup"><span data-stu-id="552e2-316">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="552e2-317">Publier le package 2016 Office globalement</span><span class="sxs-lookup"><span data-stu-id="552e2-317">Publish the Office 2016 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="552e2-318">Les points d’extension dans le package d’application Office V doivent être installés au niveau de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="552e2-318">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="552e2-319">Lorsque vous publiez au niveau de l’ordinateur, aucune action ou redistribuable ne doit être requis, et le package 2016 Office autorise globalement ses applications à fonctionner comme Office en natif, ce qui évite aux administrateurs de personnaliser les packages.</span><span class="sxs-lookup"><span data-stu-id="552e2-319">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2016 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="552e2-320">Publication d’un package Office</span><span class="sxs-lookup"><span data-stu-id="552e2-320">How to publish an Office package</span></span>

<span data-ttu-id="552e2-321">Exécutez la commande suivante pour publier un package Office globalement:</span><span class="sxs-lookup"><span data-stu-id="552e2-321">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="552e2-322">À partir de la console de gestion Web sur le serveur App-V, vous pouvez ajouter des autorisations à un groupe d’ordinateurs plutôt qu’à un groupe d’utilisateurs pour permettre la publication globale des packages dans le groupe correspondant.</span><span class="sxs-lookup"><span data-stu-id="552e2-322">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="552e2-323">Personnalisation et gestion des packages d’application Office V</span><span class="sxs-lookup"><span data-stu-id="552e2-323">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="552e2-324">Pour gérer vos packages d’application Office V, utilisez les mêmes opérations que pour tous les autres packages, mais il existe quelques exceptions, comme indiqué dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="552e2-324">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="552e2-325">Activation de plug-ins Office à l’aide de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="552e2-325">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="552e2-326">Désactivation des applications Office 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-326">Disabling Office 2016 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="552e2-327">Désactivation des raccourcis d’Office 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-327">Disabling Office 2016 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="552e2-328">Gestion des mises à jour de package Office 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-328">Managing Office 2016 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="552e2-329">Déploiement de Visio 2016 et de Project 2016 avec Office</span><span class="sxs-lookup"><span data-stu-id="552e2-329">Deploying Visio 2016 and Project 2016 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="552e2-330">Activation de plug-ins Office à l’aide de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="552e2-330">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="552e2-331">Suivez les étapes décrites dans cette section pour activer les plug-ins Office avec votre package Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-331">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="552e2-332">Pour utiliser les plug-ins Office, vous devez utiliser le Sequencer App-V pour créer un package distinct contenant uniquement les plug-ins. Vous ne pouvez pas utiliser l’outil déploiement d’Office pour créer le package de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="552e2-332">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="552e2-333">Ensuite, créez un groupe de connexion contenant le package Office et le package enfichable, comme décrit dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="552e2-333">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="552e2-334">Pour activer les plug-ins pour les packages App-V pour Office</span><span class="sxs-lookup"><span data-stu-id="552e2-334">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="552e2-335">Ajoutez un groupe de connexions via App-V Server, System Center Configuration Manager ou une cmdlet PowerShell.</span><span class="sxs-lookup"><span data-stu-id="552e2-335">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="552e2-336">Séquencez les plug-ins à l’aide du Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-336">Sequence your plug-ins using the App-V Sequencer.</span></span> <span data-ttu-id="552e2-337">Assurez-vous qu’Office 2016 est installé sur l’ordinateur utilisé pour la séquence du plug-in.</span><span class="sxs-lookup"><span data-stu-id="552e2-337">Ensure that Office 2016 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="552e2-338">Nous vous recommandons d’utiliser les applications Microsoft 365 pour les entreprises (non virtuelles) sur l’ordinateur de séquençage lors de la séquence des plug-ins Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-338">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2016 plug-ins.</span></span>

3.  <span data-ttu-id="552e2-339">Créez un package App-V qui inclut les plug-ins souhaités.</span><span class="sxs-lookup"><span data-stu-id="552e2-339">Create an App-V package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="552e2-340">Ajoutez un groupe de connexions via App-V Server, System Center Configuration Manager ou une cmdlet PowerShell.</span><span class="sxs-lookup"><span data-stu-id="552e2-340">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="552e2-341">Ajoutez le package App-V d’Office 2016 et le package de plug-ins que vous avez séquencé au groupe de connexions que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="552e2-341">Add the Office 2016 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    ><span data-ttu-id="552e2-342">**Important** L’ordre des packages dans le groupe de connexions détermine l’ordre dans lequel le contenu du package est fusionné.</span><span class="sxs-lookup"><span data-stu-id="552e2-342">**Important** The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="552e2-343">Dans votre fichier de descripteur de groupe de connexion, ajoutez d’abord le package App-V pour Office 2016, puis ajoutez le package App-in App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-343">In your Connection group descriptor file, add the Office 2016 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="552e2-344">Assurez-vous que les deux packages sont publiés sur l’ordinateur cible et que le package du plug-in est publié globalement pour correspondre aux paramètres globaux du package Office 2016 App-V publié.</span><span class="sxs-lookup"><span data-stu-id="552e2-344">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2016 App-V package.</span></span>

7.  <span data-ttu-id="552e2-345">Vérifiez que le fichier de configuration de déploiement du package du plug-in a les mêmes paramètres que le package App-V pour Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-345">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2016 App-V package has.</span></span>

    <span data-ttu-id="552e2-346">Dans la mesure où le package App-V d’Office 2016 est intégré au système d’exploitation, les paramètres de package du plug-in doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="552e2-346">Since the Office 2016 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="552e2-347">Vous pouvez effectuer une recherche dans le fichier de configuration de déploiement pour «mode COM» et vous assurer que la valeur de votre package de plug-ins est «intégrée» et que les «InProcessEnabled» et «OutOfProcessEnabled» correspondent aux paramètres du package application Office 2016 V publié.</span><span class="sxs-lookup"><span data-stu-id="552e2-347">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2016 App-V package you published.</span></span>

8.  <span data-ttu-id="552e2-348">Ouvrez le fichier de configuration de déploiement et attribuez la valeur **false**aux **objets activés** .</span><span class="sxs-lookup"><span data-stu-id="552e2-348">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="552e2-349">Si vous avez apporté des modifications au fichier de configuration de déploiement après le séquençage, assurez-vous que le package du plug-in est publié avec le fichier.</span><span class="sxs-lookup"><span data-stu-id="552e2-349">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="552e2-350">Vérifiez que le groupe de connexion que vous avez créé est activé sur l’ordinateur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="552e2-350">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="552e2-351">Le groupe de connexion créé est probablement «en attente» si le package App-V d’Office 2016 est en cours d’utilisation lorsque le groupe de connexion est activé.</span><span class="sxs-lookup"><span data-stu-id="552e2-351">The Connection Group created will likely “pend” if the Office 2016 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="552e2-352">Si tel est le cas, vous devez redémarrer pour pouvoir activer le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="552e2-352">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="552e2-353">Une fois que vous avez correctement publié les deux packages et activé le groupe de connexion, démarrez l’application Office 2016 cible et vérifiez que le plug-in que vous avez publié et ajouté au groupe de connexions fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="552e2-353">After you successfully publish both packages and enable the Connection Group, start the target Office 2016 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="552e2-354">Désactivation des applications Office 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-354">Disabling Office 2016 applications</span></span>

<span data-ttu-id="552e2-355">Il est possible que vous souhaitiez désactiver des applications spécifiques dans votre package d’application Office V.</span><span class="sxs-lookup"><span data-stu-id="552e2-355">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="552e2-356">Par exemple, vous pouvez désactiver l’accès sans avoir accès au principal de l’application Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-356">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="552e2-357">Lorsque vous désactivez une application, l’utilisateur final ne verra plus le raccourci de l’application.</span><span class="sxs-lookup"><span data-stu-id="552e2-357">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="552e2-358">Vous n’avez pas besoin de relancer l’application.</span><span class="sxs-lookup"><span data-stu-id="552e2-358">You do not have to re-sequence the application.</span></span> <span data-ttu-id="552e2-359">Lorsque vous modifiez le fichier de configuration de déploiement une fois que le package App-V pour Office 2016 a été publié, vous enverrez les modifications, vous ajoutez le package App-V d’Office 2016, puis vous le republiez avec le nouveau fichier de configuration de déploiement pour appliquer les nouveaux paramètres aux applications Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-359">When you change the Deployment Configuration File after the Office 2016 App-V package has been published, you will save the changes, add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

><span data-ttu-id="552e2-360">**Remarques** Pour exclure des applications Office spécifiques (par exemple, Access et InfoPath) lors de la création du package App-V avec l’outil déploiement d’Office, utilisez le paramètre **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="552e2-360">**Note** To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span>


**<span data-ttu-id="552e2-361">Pour désactiver une application Office 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-361">To disable an Office 2016 application</span></span>**

1.  <span data-ttu-id="552e2-362">Ouvrez un fichier de configuration de déploiement avec un éditeur de texte tel que **le bloc-notes** et recherchez «applications».</span><span class="sxs-lookup"><span data-stu-id="552e2-362">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="552e2-363">Recherchez l’application Office que vous voulez désactiver, par exemple, Access 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-363">Search for the Office application you want to disable, for example, Access 2016.</span></span>

3.  <span data-ttu-id="552e2-364">Remplacez la valeur «Enabled» par «true» par «false».</span><span class="sxs-lookup"><span data-stu-id="552e2-364">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="552e2-365">Enregistrez le fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="552e2-365">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="552e2-366">Ajoutez le package App-V pour Office 2016 avec le nouveau fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="552e2-366">Add the Office 2016 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="552e2-367">Ajoutez à nouveau le package App-V pour Office 2016, puis republiez-le avec le nouveau fichier de configuration de déploiement pour appliquer les nouveaux paramètres aux applications Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="552e2-367">Re-add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="552e2-368">Désactivation des raccourcis d’Office 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-368">Disabling Office 2016 shortcuts</span></span>

<span data-ttu-id="552e2-369">Vous pouvez désactiver les raccourcis pour certaines applications Office au lieu d’annuler la publication ou de la suppression du package.</span><span class="sxs-lookup"><span data-stu-id="552e2-369">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="552e2-370">L’exemple suivant explique comment désactiver les raccourcis clavier pour Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="552e2-370">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="552e2-371">Pour désactiver les raccourcis pour les applications Office 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-371">To disable shortcuts for Office 2016 applications</span></span>**

1.  <span data-ttu-id="552e2-372">Ouvrez un fichier de configuration de déploiement dans le bloc-notes et recherchez «raccourcis».</span><span class="sxs-lookup"><span data-stu-id="552e2-372">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="552e2-373">Pour désactiver certains raccourcis, vous pouvez supprimer ou commenter les raccourcis spécifiques que vous ne voulez pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="552e2-373">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="552e2-374">Vous devez laisser le sous-système présenter et activé.</span><span class="sxs-lookup"><span data-stu-id="552e2-374">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="552e2-375">Par exemple, dans l’exemple ci-dessous, supprimez les raccourcis de Microsoft Access, tout en conservant le raccourci vers le sous-système &lt; &gt; &lt; /Shortcut &gt; intact pour désactiver le raccourci Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="552e2-375">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="552e2-376">Enregistrez le fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="552e2-376">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="552e2-377">Republiez le package App-V d’Office 2016 avec un nouveau fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="552e2-377">Republish Office 2016 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="552e2-378">Il est possible de modifier de nombreux paramètres supplémentaires par le biais de la modification de la configuration de déploiement pour les packages App-V (par exemple, associations de types de fichiers, système de fichiers virtuel, etc.).</span><span class="sxs-lookup"><span data-stu-id="552e2-378">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="552e2-379">Pour plus d’informations sur l’utilisation des fichiers de configuration de déploiement pour modifier les paramètres de package App-V, reportez-vous à la section ressources supplémentaires à la fin de ce document.</span><span class="sxs-lookup"><span data-stu-id="552e2-379">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="552e2-380">Gestion des mises à jour de package Office 2016</span><span class="sxs-lookup"><span data-stu-id="552e2-380">Managing Office 2016 package upgrades</span></span>

<span data-ttu-id="552e2-381">Pour mettre à niveau un package 2016 Office, utilisez l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-381">To upgrade an Office 2016 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="552e2-382">Pour effectuer la mise à niveau d’un package 2016 Office, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="552e2-382">To upgrade a previously deployed Office 2016 package, perform the following steps.</span></span>

**<span data-ttu-id="552e2-383">Comment mettre à niveau un package Office 2016 déjà déployé</span><span class="sxs-lookup"><span data-stu-id="552e2-383">How to upgrade a previously deployed Office 2016 package</span></span>**

1. <span data-ttu-id="552e2-384">Créer un nouveau package Office 2016 par le biais de l’outil déploiement d’Office qui utilise le logiciel d’application Office 2016 le plus récent.</span><span class="sxs-lookup"><span data-stu-id="552e2-384">Create a new Office 2016 package through the Office Deployment Tool that uses the most recent Office 2016 application software.</span></span> <span data-ttu-id="552e2-385">Les derniers bits d’Office 2016 peuvent toujours être obtenus par le biais de la phase de téléchargement de la création d’un package App-V pour Office 2016.</span><span class="sxs-lookup"><span data-stu-id="552e2-385">The most recent Office 2016 bits can always be obtained through the download stage of creating an Office 2016 App-V Package.</span></span> <span data-ttu-id="552e2-386">Le package 2016 Office qui vient d’être créé dispose des dernières mises à jour et un nouvel ID de version.</span><span class="sxs-lookup"><span data-stu-id="552e2-386">The newly created Office 2016 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="552e2-387">Tous les packages créés à l’aide de l’outil déploiement d’Office ont la même ligne.</span><span class="sxs-lookup"><span data-stu-id="552e2-387">All packages created using the Office Deployment Tool have the same lineage.</span></span>

   > <span data-ttu-id="552e2-388">**Remarques** Les packages d’application Office V possèdent deux ID de version:</span><span class="sxs-lookup"><span data-stu-id="552e2-388">**Note** Office App-V packages have two Version IDs:</span></span>
   > <ul>
   > <li><span data-ttu-id="552e2-389">ID de version d’un package App-V Office 2016 unique pour tous les packages créés à l’aide de l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-389">An Office 2016 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span></li>
   > <li><span data-ttu-id="552e2-390">Un deuxième ID de version de package App-V, x. x. x. x par exemple, dans le manifeste AppX qui changera uniquement s’il existe une nouvelle version d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-390">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="552e2-391">Par exemple, si une nouvelle version d’Office 2016 avec des mises à niveau est disponible et qu’un package est créé par le biais de l’outil déploiement d’Office pour incorporer ces mises à jour, l’ID de version X. X. X. X sera modifié de manière à refléter la modification de la version d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-391">For example, if a new Office 2016 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="552e2-392">Le serveur App-V utilisera l’ID de version X. X. X. X pour différencier ce package et détecter qu’il contient de nouvelles mises à niveau du package déjà publié et, par conséquent, le publier dans le cadre d’une mise à niveau vers le package Office 2016 existant.</span><span class="sxs-lookup"><span data-stu-id="552e2-392">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2016 package.</span></span></li>
   > </ul>


2. <span data-ttu-id="552e2-393">Publiez globalement les packages d’application Office 2016 nouvellement créés sur les ordinateurs sur lesquels vous souhaitez appliquer les nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="552e2-393">Globally publish the newly created Office 2016 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="552e2-394">Dans la mesure où le nouveau package utilise la même ligne de l’ancien package de l’application Office 2016-V, la publication du nouveau package avec les mises à jour apportera uniquement les nouvelles modifications apportées à l’ancien package et sera donc rapide.</span><span class="sxs-lookup"><span data-stu-id="552e2-394">Since the new package has the same lineage of the older Office 2016 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3. <span data-ttu-id="552e2-395">Les mises à niveau seront appliquées de la même manière que les packages App-V globalement publiés.</span><span class="sxs-lookup"><span data-stu-id="552e2-395">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="552e2-396">Étant donné que les applications seront probablement utilisées, les mises à niveau peuvent être retardées jusqu’au redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="552e2-396">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>


### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="552e2-397">Déploiement de Visio 2016 et de Project 2016 avec Office</span><span class="sxs-lookup"><span data-stu-id="552e2-397">Deploying Visio 2016 and Project 2016 with Office</span></span>

<span data-ttu-id="552e2-398">Le tableau suivant décrit les exigences et les options de déploiement de Visio 2016 et de Project 2016 avec Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-398">The following table describes the requirements and options for deploying Visio 2016 and Project 2016 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="552e2-399">Tâche</span><span class="sxs-lookup"><span data-stu-id="552e2-399">Task</span></span></th>
<th align="left"><span data-ttu-id="552e2-400">Détails</span><span class="sxs-lookup"><span data-stu-id="552e2-400">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="552e2-401">Comment puis-je empaqueter et publier Visio 2016 et Project 2016 avec Office?</span><span class="sxs-lookup"><span data-stu-id="552e2-401">How do I package and publish Visio 2016 and Project 2016 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="552e2-402">Vous devez inclure Visio 2016 et Project 2016 dans le même package qu’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-402">You must include Visio 2016 and Project 2016 in the same package with Office.</span></span></p>
<p><span data-ttu-id="552e2-403">Si vous ne déployez pas Office, vous pouvez créer un package contenant Visio et/ou Project, tant que vous respectez les exigences de création de packages, de publication et de déploiement décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="552e2-403">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow the packaging, publishing, and deployment requirements described in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="552e2-404">Comment puis-je déployer Visio 2016 et Project 2016 vers des utilisateurs spécifiques?</span><span class="sxs-lookup"><span data-stu-id="552e2-404">How can I deploy Visio 2016 and Project 2016 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="552e2-405">Appliquez l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="552e2-405">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="552e2-406">Si vous souhaitez...</span><span class="sxs-lookup"><span data-stu-id="552e2-406">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="552e2-407">... Utilisez ensuite cette méthode</span><span class="sxs-lookup"><span data-stu-id="552e2-407">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="552e2-408">Création de deux packages différents et déploiement de chacun d’eux dans un groupe d’utilisateurs différent</span><span class="sxs-lookup"><span data-stu-id="552e2-408">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="552e2-409">Créez et déployez les packages suivants:</span><span class="sxs-lookup"><span data-stu-id="552e2-409">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="552e2-410">Package qui contient uniquement Office-déploiement sur des ordinateurs pour lesquels les utilisateurs ont besoin uniquement d’Office.</span><span class="sxs-lookup"><span data-stu-id="552e2-410">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="552e2-411">Un package qui contient Office, Visio et Project-déployer sur des ordinateurs pour lesquels les utilisateurs ont besoin des trois applications.</span><span class="sxs-lookup"><span data-stu-id="552e2-411">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="552e2-412">Si vous n’avez besoin que d’un seul package pour l’ensemble de votre organisation, ou si vous avez des utilisateurs qui partagent des ordinateurs:</span><span class="sxs-lookup"><span data-stu-id="552e2-412">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="552e2-413">Procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="552e2-413">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="552e2-414">Créer un package qui contient Office, Visio et Project.</span><span class="sxs-lookup"><span data-stu-id="552e2-414">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="552e2-415">Déployer le package auprès de tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="552e2-415">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="552e2-416">Utilisez <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> pour empêcher des utilisateurs spécifiques d’utiliser Visio et Project.</span><span class="sxs-lookup"><span data-stu-id="552e2-416">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="552e2-417">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="552e2-417">Additional resources</span></span>


[<span data-ttu-id="552e2-418">Déploiement de Microsoft Office2013 à l’aide d’App-V</span><span class="sxs-lookup"><span data-stu-id="552e2-418">Deploying Microsoft Office 2013 by Using App-V</span></span>](deploying-microsoft-office-2013-by-using-app-v.md)

[<span data-ttu-id="552e2-419">Déploiement de Microsoft Office2010 à l'aide d'App-V</span><span class="sxs-lookup"><span data-stu-id="552e2-419">Deploying Microsoft Office 2010 by Using App-V</span></span>](deploying-microsoft-office-2010-by-using-app-v.md)

[<span data-ttu-id="552e2-420">Outil déploiement d’Office 2016 pour Office «démarrer en un clic»</span><span class="sxs-lookup"><span data-stu-id="552e2-420">Office 2016 Deployment Tool for Click-to-Run</span></span>](https://www.microsoft.com/download/details.aspx?id=49117)

**<span data-ttu-id="552e2-421">Groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="552e2-421">Connection Groups</span></span>**

[<span data-ttu-id="552e2-422">Déploiement de groupes de connexion dans Microsoft App-V v5</span><span class="sxs-lookup"><span data-stu-id="552e2-422">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="552e2-423">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="552e2-423">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="552e2-424">Configuration dynamique</span><span class="sxs-lookup"><span data-stu-id="552e2-424">Dynamic Configuration</span></span>**

[<span data-ttu-id="552e2-425">À propos de la configuration dynamique d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="552e2-425">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)






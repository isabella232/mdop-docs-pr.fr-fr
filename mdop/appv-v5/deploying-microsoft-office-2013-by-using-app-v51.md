---
title: Déploiement de Microsoft Office2013 à l’aide d’App-V
description: Déploiement de Microsoft Office2013 à l’aide d’App-V
author: dansimp
ms.assetid: 9a7be05e-2a7a-4874-af25-09c0f5037876
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: f6a54cadce79ff3680fd69206eba8ac3fbe83a68
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805869"
---
# <span data-ttu-id="b4648-103">Déploiement de Microsoft Office2013 à l’aide d’App-V</span><span class="sxs-lookup"><span data-stu-id="b4648-103">Deploying Microsoft Office 2013 by Using App-V</span></span>


<span data-ttu-id="b4648-104">Les informations contenues dans cet article vous permettent d’utiliser Microsoft Application Virtualization (App-V) 5,1 ou les versions ultérieures pour déconnecter Microsoft Office 2013 en tant qu’application virtualisée aux ordinateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b4648-104">Use the information in this article to use Microsoft Application Virtualization (App-V) 5.1, or later versions, to deliver Microsoft Office 2013 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="b4648-105">Pour plus d’informations sur l’utilisation de App-V pour générer Office 2010, voir [déploiement de Microsoft Office 2010 à l’aide d’App-v](deploying-microsoft-office-2010-by-using-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="b4648-105">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v51.md).</span></span> <span data-ttu-id="b4648-106">Pour réussir le déploiement d’Office 2013 avec App-V, vous devez être familiarisé avec Office 2013 et App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-106">To successfully deploy Office 2013 with App-V, you need to be familiar with Office 2013 and App-V.</span></span>

<span data-ttu-id="b4648-107">Cette rubrique contient les sections suivantes:</span><span class="sxs-lookup"><span data-stu-id="b4648-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b4648-108">Ce que vous devez savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b4648-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="b4648-109">Création d’un package 2013 Office pour App-V avec l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="b4648-109">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="b4648-110">Publication du package Office pour App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="b4648-110">Publishing the Office package for App-V 5.1</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="b4648-111">Personnalisation et gestion des packages d’application Office V</span><span class="sxs-lookup"><span data-stu-id="b4648-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="b4648-112">Ce que vous devez savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b4648-112">What to know before you start</span></span>


<span data-ttu-id="b4648-113">Avant de déployer Office 2013 à l’aide de App-V, passez en revue les informations de planification suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4648-113">Before you deploy Office 2013 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="b4648-114">Versions d’Office et coexistence Office prises en charge</span><span class="sxs-lookup"><span data-stu-id="b4648-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="b4648-115">Utilisez le tableau ci-dessous pour obtenir des informations sur les versions d’Office prises en charge et sur l’exécution des versions coexistantes d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4648-116">Informations à réviser</span><span class="sxs-lookup"><span data-stu-id="b4648-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="b4648-117">Description</span><span class="sxs-lookup"><span data-stu-id="b4648-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="b4648-118">Planification de l'utilisation d'App-V avec Office</span><span class="sxs-lookup"><span data-stu-id="b4648-118">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b4648-119">Versions d’Office prises en charge</span><span class="sxs-lookup"><span data-stu-id="b4648-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="b4648-120">Types de déploiement pris en charge (par exemple, un ordinateur de bureau, une infrastructure de bureau virtuel ou un pool d’infrastructure VDI)</span><span class="sxs-lookup"><span data-stu-id="b4648-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="b4648-121">Options de gestion des licences Office</span><span class="sxs-lookup"><span data-stu-id="b4648-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting)"><span data-ttu-id="b4648-122">Planification de l'utilisation d'App-V avec Office</span><span class="sxs-lookup"><span data-stu-id="b4648-122">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="b4648-123">Remarques relatives à l’installation de différentes versions d’Office sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="b4648-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>


### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="b4648-124">Exigences en matière de création de packages, de publication et de déploiement</span><span class="sxs-lookup"><span data-stu-id="b4648-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="b4648-125">Avant de déployer Office à l’aide de App-V, consultez la configuration requise suivante.</span><span class="sxs-lookup"><span data-stu-id="b4648-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4648-126">Tâche</span><span class="sxs-lookup"><span data-stu-id="b4648-126">Task</span></span></th>
<th align="left"><span data-ttu-id="b4648-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4648-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4648-128">Packages</span><span class="sxs-lookup"><span data-stu-id="b4648-128">Packaging</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b4648-129">Toutes les applications Office que vous voulez déployer pour les utilisateurs doivent se trouver dans un seul package.</span><span class="sxs-lookup"><span data-stu-id="b4648-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="b4648-130">Dans App-V 5,1 et les versions ultérieures, vous devez utiliser l’outil déploiement d’Office pour créer des packages.</span><span class="sxs-lookup"><span data-stu-id="b4648-130">In App-V 5.1 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="b4648-131">Vous ne pouvez pas utiliser le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="b4648-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="b4648-132">Si vous déployez Microsoft Visio 2013 et Microsoft Project 2013 avec Office, vous devez les inclure dans le même package qu’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-132">If you are deploying Microsoft Visio 2013 and Microsoft Project 2013 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="b4648-133">Pour plus d’informations, reportez-vous à <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> déploiement de Visio 2013 et Project 2013 avec Office </a> .</span><span class="sxs-lookup"><span data-stu-id="b4648-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2013 and Project 2013 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4648-134">Publishing</span><span class="sxs-lookup"><span data-stu-id="b4648-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b4648-135">Vous ne pouvez publier qu’un seul package Office sur chaque ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="b4648-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="b4648-136">Vous devez publier le package Office globalement.</span><span class="sxs-lookup"><span data-stu-id="b4648-136">You must publish the Office package globally.</span></span> <span data-ttu-id="b4648-137">Vous ne pouvez pas publier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4648-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4648-138">Déploiement de l’un des produits suivants sur un ordinateur partagé, par exemple, à l’aide des services Bureau à distance:</span><span class="sxs-lookup"><span data-stu-id="b4648-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="b4648-139">Applications 365 Microsoft pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="b4648-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="b4648-140">Visio Pro pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b4648-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="b4648-141">Project Pro pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b4648-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="b4648-142">Vous devez activer <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> l’activation d’ordinateurs partagés </a> .</span><span class="sxs-lookup"><span data-stu-id="b4648-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
<p><span data-ttu-id="b4648-143">Vous n’utilisez pas l’activation d’ordinateurs partagés si vous déployez un produit sous licence en volume, par exemple:</span><span class="sxs-lookup"><span data-stu-id="b4648-143">You don’t use shared computer activation if you’re deploying a volume licensed product, such as:</span></span></p>
<ul>
<li><p><span data-ttu-id="b4648-144">Office professionnel plus 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-144">Office Professional Plus 2013</span></span></p></li>
<li><p><span data-ttu-id="b4648-145">Visio professionnel 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-145">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="b4648-146">Project Professionnel 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-146">Project Professional 2013</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="b4648-147">Exclusion d’applications Office d’un package</span><span class="sxs-lookup"><span data-stu-id="b4648-147">Excluding Office applications from a package</span></span>

<span data-ttu-id="b4648-148">Le tableau suivant décrit les méthodes recommandées pour exclure des applications Office spécifiques d’un package.</span><span class="sxs-lookup"><span data-stu-id="b4648-148">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4648-149">Tâche</span><span class="sxs-lookup"><span data-stu-id="b4648-149">Task</span></span></th>
<th align="left"><span data-ttu-id="b4648-150">Détails</span><span class="sxs-lookup"><span data-stu-id="b4648-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4648-151">Utilisez le <strong> </strong> paramètre ExcludeApp lorsque vous créez le package à l’aide de l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-151">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b4648-152">Vous permet d’exclure des applications Office spécifiques du package lorsque l’outil déploiement d’Office crée le package.</span><span class="sxs-lookup"><span data-stu-id="b4648-152">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="b4648-153">Par exemple, vous pouvez utiliser ce paramètre pour créer un package qui contient uniquement Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="b4648-153">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="b4648-154">Pour plus d’informations, consultez <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp élément </a> .</span><span class="sxs-lookup"><span data-stu-id="b4648-154">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4648-155">Modifier le fichier DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="b4648-155">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b4648-156">Modifiez le fichier DeploymentConfig.xml après la création du package.</span><span class="sxs-lookup"><span data-stu-id="b4648-156">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="b4648-157">Ce fichier contient les paramètres de package par défaut pour tous les utilisateurs sur un ordinateur exécutant le client App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-157">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="b4648-158">Pour plus d’informations, reportez-vous à <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> désactivation des applications Office 2013 </a> .</span><span class="sxs-lookup"><span data-stu-id="b4648-158">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)">Disabling Office 2013 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="b4648-159">Création d’un package 2013 Office pour App-V avec l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="b4648-159">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="b4648-160">Suivez les étapes ci-dessous pour créer un package 2013 Office pour App-V 5,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b4648-160">Complete the following steps to create an Office 2013 package for App-V 5.1 or later.</span></span>

**<span data-ttu-id="b4648-161">Important</span><span class="sxs-lookup"><span data-stu-id="b4648-161">Important</span></span>**  
<span data-ttu-id="b4648-162">Dans App-V 5,1 et les versions ultérieures, vous devez utiliser l’outil déploiement d’Office pour créer un package.</span><span class="sxs-lookup"><span data-stu-id="b4648-162">In App-V 5.1 and later, you must the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="b4648-163">Vous ne pouvez pas utiliser le Sequencer pour créer des packages.</span><span class="sxs-lookup"><span data-stu-id="b4648-163">You cannot use the Sequencer to create packages.</span></span>



### <span data-ttu-id="b4648-164">Consulter les conditions préalables à l’utilisation de l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="b4648-164">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="b4648-165">Sur l’ordinateur sur lequel vous installez l’outil déploiement d’Office, vous devez disposer des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="b4648-165">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4648-166">Prérequises</span><span class="sxs-lookup"><span data-stu-id="b4648-166">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="b4648-167">Description</span><span class="sxs-lookup"><span data-stu-id="b4648-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4648-168">Logiciels requis</span><span class="sxs-lookup"><span data-stu-id="b4648-168">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-169">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="b4648-169">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4648-170">Systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4648-170">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b4648-171">version 64 bits de Windows 8 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b4648-171">64-bit version of Windows 8 or later</span></span></p></li>
<li><p><span data-ttu-id="b4648-172">version 64 bits de Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4648-172">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="b4648-173">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4648-173">Note</span></span>**  
<span data-ttu-id="b4648-174">Dans cette rubrique, le terme «Office 2013 App-V package» fait référence à la gestion des licences d’abonnement et au programme de licence en volume.</span><span class="sxs-lookup"><span data-stu-id="b4648-174">In this topic, the term “Office 2013 App-V package” refers to subscription licensing and volume licensing.</span></span>



### <span data-ttu-id="b4648-175">Créer des packages App-V d’Office 2013 à l’aide de l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="b4648-175">Create Office 2013 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="b4648-176">Vous pouvez créer des packages App-V d’Office 2013 à l’aide de l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-176">You create Office 2013 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="b4648-177">Les instructions suivantes vous expliquent comment créer un package App-V pour Office 2013 avec les licences en volume ou les licences d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4648-177">The following instructions explain how to create an Office 2013 App-V package with Volume Licensing or Subscription Licensing.</span></span>

<span data-ttu-id="b4648-178">Créer des packages App-V Office 2013 sur des ordinateurs Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b4648-178">Create Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="b4648-179">Une fois créé, le package App-V pour Office 2013 s’exécutera 64 32 sur les ordinateurs Windows 7, Windows 8,1 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b4648-179">Once created, the Office 2013 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="b4648-180">Télécharger l’outil déploiement d’Office</span><span class="sxs-lookup"><span data-stu-id="b4648-180">Download the Office Deployment Tool</span></span>

<span data-ttu-id="b4648-181">Les packages App-V d’Office 2013 sont créés à l’aide de l’outil déploiement d’Office qui génère un package App-V pour Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-181">Office 2013 App-V Packages are created using the Office Deployment Tool, which generates an Office 2013 App-V Package.</span></span> <span data-ttu-id="b4648-182">Le package ne peut pas être créé ou modifié via le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-182">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="b4648-183">Pour commencer à créer un package:</span><span class="sxs-lookup"><span data-stu-id="b4648-183">To begin package creation:</span></span>

1.  <span data-ttu-id="b4648-184">Télécharger l' [outil déploiement d’Office pour Office «démarrer en un clic](https://www.microsoft.com/download/details.aspx?id=36778)».</span><span class="sxs-lookup"><span data-stu-id="b4648-184">Download the [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=36778).</span></span>

2.  <span data-ttu-id="b4648-185">Exécutez le fichier. exe et extrayez ses fonctionnalités dans l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="b4648-185">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="b4648-186">Pour faciliter ce processus, vous pouvez créer un dossier réseau partagé dans lequel les fonctionnalités seront enregistrées.</span><span class="sxs-lookup"><span data-stu-id="b4648-186">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    <span data-ttu-id="b4648-187">Par exemple: \\\\Server\\Office2013</span><span class="sxs-lookup"><span data-stu-id="b4648-187">Example: \\\\Server\\Office2013</span></span>

3.  <span data-ttu-id="b4648-188">Vérifiez qu’il existe une setup.exe et qu’un fichier configuration.xml se trouvent à l’emplacement que vous avez spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4648-188">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="b4648-189">Télécharger les applications Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-189">Download Office 2013 applications</span></span>

<span data-ttu-id="b4648-190">Après avoir téléchargé l’outil déploiement d’Office, vous pouvez l’utiliser pour obtenir les dernières applications Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-190">After you download the Office Deployment Tool, you can use it to get the latest Office 2013 applications.</span></span> <span data-ttu-id="b4648-191">Après avoir effectué les applications Office, vous créez le package App-V pour Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-191">After getting the Office applications, you create the Office 2013 App-V package.</span></span>

<span data-ttu-id="b4648-192">Le fichier XML inclus dans l’outil déploiement d’Office spécifie les détails du produit, tels que les langues et les applications Office inclus.</span><span class="sxs-lookup"><span data-stu-id="b4648-192">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1.  <span data-ttu-id="b4648-193">**Personnalisez le fichier de configuration XML d’exemple:** Utilisez l’exemple de fichier de configuration XML que vous avez téléchargé auprès de l’outil déploiement d’Office pour personnaliser les applications Office:</span><span class="sxs-lookup"><span data-stu-id="b4648-193">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

    1.  <span data-ttu-id="b4648-194">Ouvrez l’exemple de fichier XML dans le bloc-notes ou dans votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="b4648-194">Open the sample XML file in Notepad or your favorite text editor.</span></span>

    2.  <span data-ttu-id="b4648-195">L’exemple configuration.xml ouverture et la possibilité de le modifier, vous pouvez spécifier des produits, des langues et le chemin d’accès au dossier dans lequel vous enregistrez les applications Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-195">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2013 applications.</span></span> <span data-ttu-id="b4648-196">Voici un exemple de base du fichier configuration.xml:</span><span class="sxs-lookup"><span data-stu-id="b4648-196">The following is a basic example of the configuration.xml file:</span></span>

        ```xml
        <Configuration>
           <Add SourcePath= ”\\Server\Office2013” OfficeClientEdition="32" >
            <Product ID="O365ProPlusRetail ">
              <Language ID="en-us" />
            </Product>
            <Product ID="VisioProRetail">
              <Language ID="en-us" />
            </Product>
          </Add>
        </Configuration>
        ```

        **<span data-ttu-id="b4648-197">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4648-197">Note</span></span>**  
        <span data-ttu-id="b4648-198">Le fichier XML de configuration est un exemple de fichier XML.</span><span class="sxs-lookup"><span data-stu-id="b4648-198">The configuration XML is a sample XML file.</span></span> <span data-ttu-id="b4648-199">Le fichier inclut des lignes commentées. Vous pouvez «ne pas commenter» ces lignes pour personnaliser des paramètres supplémentaires à l’aide du fichier.</span><span class="sxs-lookup"><span data-stu-id="b4648-199">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span>



~~~
    The above XML configuration file specifies that Office 2013 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2013, which is the location where Office applications will be saved to. Note that the Product ID of the applications will not affect the final licensing of Office. Office 2013 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage. The table below summarizes the customizable attributes and elements of XML file:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Input</th>
    <th align="left">Description</th>
    <th align="left">Example</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Add element</p></td>
    <td align="left"><p>Specifies the products and languages to include in the package.</p></td>
    <td align="left"><p>N/A</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>OfficeClientEdition (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the edition of Office 2013 product to use: 32-bit or 64-bit. The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</p></td>
    <td align="left"><p><strong>OfficeClientEdition</strong>=&quot;32&quot;</p>
    <p><strong>OfficeClientEdition</strong>=&quot;64&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Product element</p></td>
    <td align="left"><p>Specifies the application. Project 2013 and Visio 2013 must be specified here as an added product to be included in the applications.</p></td>
    <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
    <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
    <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
    <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Language element</p></td>
    <td align="left"><p>Specifies the language supported in the applications</p></td>
    <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Version (attribute of Add element)</p></td>
    <td align="left"><p>Optional. Specifies a build to use for the package</p>
    <p>Defaults to latest advertised build (as defined in v32.CAB at the Office source).</p></td>
    <td align="left"><p><code>15.1.2.3</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>SourcePath (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the location in which the applications will be saved to.</p></td>
    <td align="left"><p><code>Sourcepath = &quot;\\Server\Office2013”</code></p></td>
    </tr>
    </tbody>
    </table>



    After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2013 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.
~~~

2. <span data-ttu-id="b4648-200">**Téléchargez les applications à l’emplacement spécifié:** Utilisez une invite de commandes avec élévation de privilèges et un système d’exploitation 64 bits pour télécharger les applications Office 2013 qui seront converties ultérieurement en package App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-200">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2013 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="b4648-201">Vous trouverez ci-dessous un exemple de commande avec une description des détails:</span><span class="sxs-lookup"><span data-stu-id="b4648-201">Below is an example command with description of details:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   <span data-ttu-id="b4648-202">Dans l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="b4648-202">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b4648-203">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="b4648-203">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-204">est l’emplacement de partage réseau qui contient l’outil déploiement d’Office et le fichier Configuration.xml personnalisé Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b4648-204">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b4648-205">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="b4648-205">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-206">est l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-206">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b4648-207">/Download</span><span class="sxs-lookup"><span data-stu-id="b4648-207">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-208">télécharge les applications Office 2013 que vous spécifiez dans le fichier customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b4648-208">downloads the Office 2013 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="b4648-209">Ces bits peuvent être convertis ultérieurement dans un package App-V pour Office 2013 avec le programme de licence en volume.</span><span class="sxs-lookup"><span data-stu-id="b4648-209">These bits can be later converted in an Office 2013 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b4648-210">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="b4648-210">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-211">transmet le fichier de configuration XML requis pour terminer le processus de téléchargement (dans cet exemple, customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b4648-211">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="b4648-212">Après l’utilisation de la commande Télécharger, les applications Office se trouvent dans l’emplacement spécifié dans le fichier XML de configuration (dans cet exemple, \Server\Office2013.).</span><span class="sxs-lookup"><span data-stu-id="b4648-212">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2013.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="b4648-213">Convertir les applications Office en package App-V</span><span class="sxs-lookup"><span data-stu-id="b4648-213">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="b4648-214">Après avoir téléchargé les applications Office 2013 par le biais de l’outil déploiement d’Office, utilisez l’outil déploiement d’Office pour les convertir en package d’application Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-214">After you download the Office 2013 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2013 App-V package.</span></span> <span data-ttu-id="b4648-215">Suivez les étapes qui correspondent à votre modèle de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="b4648-215">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="b4648-216">Résumé de ce que vous devez faire:</span><span class="sxs-lookup"><span data-stu-id="b4648-216">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="b4648-217">Créez les packages App-V d’Office 2013 sur les ordinateurs Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b4648-217">Create the Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="b4648-218">Toutefois, le package s’exécute 32 sur les ordinateurs Windows 7, Windows 8 et Windows 10, et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b4648-218">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8, and Windows 10 computers.</span></span>

-   <span data-ttu-id="b4648-219">Pour créer un package App-V pour la gestion des licences d’abonnement ou le programme de licence en volume à l’aide de l’outil déploiement d’Office, vous devez modifier le fichier de configuration CustomConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b4648-219">Create an Office App-V package for either Subscription Licensing package or Volume Licensing by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="b4648-220">Le tableau suivant récapitule les valeurs que vous devez entrer dans le fichier CustomConfig.xml pour le modèle de gestion des licences que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="b4648-220">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="b4648-221">Les étapes des sections qui suivent le tableau spécifient les entrées exactes que vous devez effectuer.</span><span class="sxs-lookup"><span data-stu-id="b4648-221">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4648-222">ID produit</span><span class="sxs-lookup"><span data-stu-id="b4648-222">Product ID</span></span></th>
<th align="left"><span data-ttu-id="b4648-223">Gestion des licences en volume</span><span class="sxs-lookup"><span data-stu-id="b4648-223">Volume Licensing</span></span></th>
<th align="left"><span data-ttu-id="b4648-224">Licences d’abonnement</span><span class="sxs-lookup"><span data-stu-id="b4648-224">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b4648-225">Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-225">Office 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b4648-226">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="b4648-226">ProPlusVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-227">O365proplusretail)</span><span class="sxs-lookup"><span data-stu-id="b4648-227">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b4648-228">Office 2013 avec Visio 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-228">Office 2013 with Visio 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b4648-229">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="b4648-229">ProPlusVolume</span></span></p>
<p><span data-ttu-id="b4648-230">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="b4648-230">VisioProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-231">O365proplusretail)</span><span class="sxs-lookup"><span data-stu-id="b4648-231">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="b4648-232">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="b4648-232">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b4648-233">Office 2013 avec Visio 2013 et Project 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-233">Office 2013 with Visio 2013 and Project 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b4648-234">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="b4648-234">ProPlusVolume</span></span></p>
<p><span data-ttu-id="b4648-235">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="b4648-235">VisioProVolume</span></span></p>
<p><span data-ttu-id="b4648-236">ProjectProVolume</span><span class="sxs-lookup"><span data-stu-id="b4648-236">ProjectProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-237">O365proplusretail)</span><span class="sxs-lookup"><span data-stu-id="b4648-237">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="b4648-238">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="b4648-238">VisioProRetail</span></span></p>
<p><span data-ttu-id="b4648-239">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="b4648-239">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="b4648-240">Convertir les applications Office en package App-V</span><span class="sxs-lookup"><span data-stu-id="b4648-240">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="b4648-241">Dans le bloc-notes, rouvrez le fichier CustomConfig.xml, puis apportez les modifications suivantes au fichier:</span><span class="sxs-lookup"><span data-stu-id="b4648-241">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="b4648-242">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b4648-242">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="b4648-243">Ce à quoi changer la valeur</span><span class="sxs-lookup"><span data-stu-id="b4648-243">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4648-244">Chemin_source</span><span class="sxs-lookup"><span data-stu-id="b4648-244">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4648-245">Pointez sur les applications Office téléchargées auparavant.</span><span class="sxs-lookup"><span data-stu-id="b4648-245">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4648-246">ProductID</span><span class="sxs-lookup"><span data-stu-id="b4648-246">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4648-247">Spécifiez le type de licence, comme indiqué dans les exemples suivants:</span><span class="sxs-lookup"><span data-stu-id="b4648-247">Specify the type of licensing, as shown in the following examples:</span></span></p>
   <ul>
   <li><p><span data-ttu-id="b4648-248">Licences d’abonnement</span><span class="sxs-lookup"><span data-stu-id="b4648-248">Subscription Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="b4648-249">Dans cet exemple, les modifications suivantes ont été apportées à la création d’un package avec les licences d’abonnement:</span><span class="sxs-lookup"><span data-stu-id="b4648-249">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b4648-250">Chemin_source</span><span class="sxs-lookup"><span data-stu-id="b4648-250">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-251">est le chemin d’accès, qui a été modifié de sorte qu’il pointe vers les applications Office téléchargées auparavant.</span><span class="sxs-lookup"><span data-stu-id="b4648-251">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b4648-252">ID produit</span><span class="sxs-lookup"><span data-stu-id="b4648-252">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-253">pour Office a changé en <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="b4648-253">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b4648-254">ID produit</span><span class="sxs-lookup"><span data-stu-id="b4648-254">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-255">pour Visio a changé en <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="b4648-255">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p><span data-ttu-id="b4648-256">Gestion des licences en volume</span><span class="sxs-lookup"><span data-stu-id="b4648-256">Volume Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\Server\Office2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;ProPlusVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt;</code></pre>
   <p><span data-ttu-id="b4648-257">Dans cet exemple, les modifications suivantes ont été apportées à la création d’un package avec le programme de licence en volume:</span><span class="sxs-lookup"><span data-stu-id="b4648-257">In this example, the following changes were made to create a package with Volume licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b4648-258">Chemin_source</span><span class="sxs-lookup"><span data-stu-id="b4648-258">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-259">est le chemin d’accès, qui a été modifié de sorte qu’il pointe vers les applications Office téléchargées auparavant.</span><span class="sxs-lookup"><span data-stu-id="b4648-259">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b4648-260">ID produit</span><span class="sxs-lookup"><span data-stu-id="b4648-260">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-261">pour Office a changé en <code>ProPlusVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="b4648-261">for Office was changed to <code>ProPlusVolume</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b4648-262">ID produit</span><span class="sxs-lookup"><span data-stu-id="b4648-262">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-263">pour Visio a changé en <code>VisioProVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="b4648-263">for Visio was changed to <code>VisioProVolume</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4648-264">ExcludeApp (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b4648-264">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4648-265">Vous permet de spécifier les programmes Office que vous ne souhaitez pas inclure dans le package App-V créé par l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-265">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="b4648-266">Par exemple, vous pouvez exclure Access et InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b4648-266">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4648-267">PACKAGEGUID (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b4648-267">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4648-268">Par défaut, tous les packages App-V créés par l’outil déploiement d’Office partagent le même ID de package App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-268">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="b4648-269">Vous pouvez utiliser PACKAGEGUID pour spécifier un ID de package différent pour chaque package, qui vous permet de publier plusieurs packages App-V, créés par l’outil déploiement d’Office, et de les gérer à l’aide du serveur App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-269">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="b4648-270">Un exemple d’utilisation de ce paramètre est le cas si vous créez des packages différents pour différents utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b4648-270">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="b4648-271">Par exemple, vous pouvez créer un package uniquement avec Office 2013 pour certains utilisateurs et créer un autre package avec Office 2013 et Visio 2013 pour un autre groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b4648-271">For example, you can create a package with just Office 2013 for some users, and create another package with Office 2013 and Visio 2013 for another set of users.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b4648-272">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4648-272">Note</span></span></strong><br/><p><span data-ttu-id="b4648-273">Même si vous utilisez des ID de package uniques, vous pouvez toujours déployer un seul package d’application-V sur un seul appareil.</span><span class="sxs-lookup"><span data-stu-id="b4648-273">Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="b4648-274">Utilisez la commande/Packager pour convertir les applications Office en un package App-V pour Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-274">Use the /packager command to convert the Office applications to an Office 2013 App-V package.</span></span>

   <span data-ttu-id="b4648-275">Exemple:</span><span class="sxs-lookup"><span data-stu-id="b4648-275">For example:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   <span data-ttu-id="b4648-276">Dans l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="b4648-276">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b4648-277">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="b4648-277">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-278">est l’emplacement de partage réseau qui contient l’outil déploiement d’Office et le fichier Configuration.xml personnalisé Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b4648-278">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b4648-279">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="b4648-279">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-280">est l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-280">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b4648-281">/packager</span><span class="sxs-lookup"><span data-stu-id="b4648-281">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-282">crée le package App-V pour Office 2013 avec la licence en volume spécifiée dans le fichier customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b4648-282">creates the Office 2013 App-V package with Volume Licensing as specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b4648-283">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="b4648-283">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-284">transmet le fichier XML de configuration (dans ce cas, customConfig) qui a été préparé pour la phase d’emballage.</span><span class="sxs-lookup"><span data-stu-id="b4648-284">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b4648-285">\server\share\Office 2013AppV</span><span class="sxs-lookup"><span data-stu-id="b4648-285">\server\share\Office 2013AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b4648-286">Spécifie l’emplacement du package Office App-V nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="b4648-286">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2013 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note**  
To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="b4648-287">Vérifiez que le package App-V pour Office 2013 fonctionne correctement:</span><span class="sxs-lookup"><span data-stu-id="b4648-287">Verify that the Office 2013 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="b4648-288">Publiez le package App-V pour Office 2013 que vous avez créé dans le monde entier, sur un ordinateur de test et vérifiez que les raccourcis vers Office 2013 apparaissent.</span><span class="sxs-lookup"><span data-stu-id="b4648-288">Publish the Office 2013 App-V package, which you created globally, to a test computer, and verify that the Office 2013 shortcuts appear.</span></span>

   2.  <span data-ttu-id="b4648-289">Démarrez quelques applications Office 2013, telles qu’Excel ou Word, pour vous assurer que votre package fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="b4648-289">Start a few Office 2013 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="b4648-290">Publication du package Office pour App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="b4648-290">Publishing the Office package for App-V 5.1</span></span>


<span data-ttu-id="b4648-291">Utilisez les informations suivantes pour publier un package Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-291">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="b4648-292">Méthodes de publication des packages App-V d’Office</span><span class="sxs-lookup"><span data-stu-id="b4648-292">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="b4648-293">Déployez le package App-V pour Office 2013 à l’aide des méthodes que vous utilisez pour les autres packages:</span><span class="sxs-lookup"><span data-stu-id="b4648-293">Deploy the App-V package for Office 2013 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="b4648-294">SystemCenterConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="b4648-294">System Center Configuration Manager</span></span>

-   <span data-ttu-id="b4648-295">App-V Server</span><span class="sxs-lookup"><span data-stu-id="b4648-295">App-V Server</span></span>

-   <span data-ttu-id="b4648-296">Commandes PowerShell autonomes</span><span class="sxs-lookup"><span data-stu-id="b4648-296">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="b4648-297">Conditions préalables et configuration requise pour la publication</span><span class="sxs-lookup"><span data-stu-id="b4648-297">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4648-298">Conditions préalables ou requises</span><span class="sxs-lookup"><span data-stu-id="b4648-298">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="b4648-299">Détails</span><span class="sxs-lookup"><span data-stu-id="b4648-299">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4648-300">Activer les scripts PowerShell sur les clients App-V</span><span class="sxs-lookup"><span data-stu-id="b4648-300">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-301">Pour publier des packages Office 2013, vous devez exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="b4648-301">To publish Office 2013 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="b4648-302">Par défaut, les scripts de package sont désactivés sur les clients App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-302">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="b4648-303">Pour activer les scripts, exécutez la commande PowerShell suivante:</span><span class="sxs-lookup"><span data-stu-id="b4648-303">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4648-304">Publier le package 2013 Office globalement</span><span class="sxs-lookup"><span data-stu-id="b4648-304">Publish the Office 2013 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-305">Les points d’extension dans le package d’application Office V doivent être installés au niveau de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b4648-305">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="b4648-306">Lorsque vous publiez au niveau de l’ordinateur, aucune action ou redistribuable ne doit être requis, et le package 2013 Office autorise globalement ses applications à fonctionner comme Office en natif, ce qui évite aux administrateurs de personnaliser les packages.</span><span class="sxs-lookup"><span data-stu-id="b4648-306">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2013 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="b4648-307">Publication d’un package Office</span><span class="sxs-lookup"><span data-stu-id="b4648-307">How to publish an Office package</span></span>

<span data-ttu-id="b4648-308">Exécutez la commande suivante pour publier un package Office globalement:</span><span class="sxs-lookup"><span data-stu-id="b4648-308">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="b4648-309">À partir de la console de gestion Web sur le serveur App-V, vous pouvez ajouter des autorisations à un groupe d’ordinateurs plutôt qu’à un groupe d’utilisateurs pour permettre la publication globale des packages dans le groupe correspondant.</span><span class="sxs-lookup"><span data-stu-id="b4648-309">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="b4648-310">Personnalisation et gestion des packages d’application Office V</span><span class="sxs-lookup"><span data-stu-id="b4648-310">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="b4648-311">Pour gérer vos packages d’application Office V, utilisez les mêmes opérations que pour tous les autres packages, mais il existe quelques exceptions, comme indiqué dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4648-311">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="b4648-312">Activation de plug-ins Office à l’aide de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="b4648-312">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="b4648-313">Désactivation des applications Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-313">Disabling Office 2013 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="b4648-314">Désactivation des raccourcis d’Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-314">Disabling Office 2013 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="b4648-315">Gestion des mises à jour de package Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-315">Managing Office 2013 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="b4648-316">Gestion des mises à niveau de la gestion des licences Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-316">Managing Office 2013 licensing upgrades</span></span>](#bkmk-manage-office-lic-upgrd)

-   [<span data-ttu-id="b4648-317">Déploiement de Visio 2013 et de Project 2013 avec Office</span><span class="sxs-lookup"><span data-stu-id="b4648-317">Deploying Visio 2013 and Project 2013 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="b4648-318">Activation de plug-ins Office à l’aide de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="b4648-318">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="b4648-319">Suivez les étapes décrites dans cette section pour activer les plug-ins Office avec votre package Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-319">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="b4648-320">Pour utiliser les plug-ins Office, vous devez utiliser le Sequencer App-V pour créer un package distinct contenant uniquement les plug-ins. Vous ne pouvez pas utiliser l’outil déploiement d’Office pour créer le package de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="b4648-320">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="b4648-321">Ensuite, créez un groupe de connexion contenant le package Office et le package enfichable, comme décrit dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4648-321">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="b4648-322">Pour activer les plug-ins pour les packages App-V pour Office</span><span class="sxs-lookup"><span data-stu-id="b4648-322">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="b4648-323">Ajoutez un groupe de connexions via App-V Server, System Center Configuration Manager ou une cmdlet PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4648-323">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="b4648-324">Séquencez vos plug-ins en utilisant le Sequencer App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b4648-324">Sequence your plug-ins using the App-V 5.1 Sequencer.</span></span> <span data-ttu-id="b4648-325">Assurez-vous qu’Office 2013 est installé sur l’ordinateur utilisé pour la séquence du plug-in.</span><span class="sxs-lookup"><span data-stu-id="b4648-325">Ensure that Office 2013 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="b4648-326">Nous vous recommandons d’utiliser les applications Microsoft 365 pour les entreprises (non virtuelles) sur l’ordinateur de séquençage lors de la séquence des plug-ins Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-326">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2013 plug-ins.</span></span>

3.  <span data-ttu-id="b4648-327">Créer un package App-V 5,1 qui inclut les plug-ins souhaités.</span><span class="sxs-lookup"><span data-stu-id="b4648-327">Create an App-V 5.1 package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="b4648-328">Ajoutez un groupe de connexions via App-V Server, System Center Configuration Manager ou une cmdlet PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4648-328">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="b4648-329">Ajoutez le package App-V d’Office 2013 et le package de plug-ins que vous avez séquencé au groupe de connexions que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="b4648-329">Add the Office 2013 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    **<span data-ttu-id="b4648-330">Important</span><span class="sxs-lookup"><span data-stu-id="b4648-330">Important</span></span>**  
    <span data-ttu-id="b4648-331">L’ordre des packages dans le groupe de connexions détermine l’ordre dans lequel le contenu du package est fusionné.</span><span class="sxs-lookup"><span data-stu-id="b4648-331">The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="b4648-332">Dans votre fichier de descripteur de groupe de connexion, ajoutez d’abord le package App-V pour Office 2013, puis ajoutez le package App-in App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-332">In your Connection group descriptor file, add the Office 2013 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="b4648-333">Assurez-vous que les deux packages sont publiés sur l’ordinateur cible et que le package du plug-in est publié globalement pour correspondre aux paramètres globaux du package Office 2013 App-V publié.</span><span class="sxs-lookup"><span data-stu-id="b4648-333">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2013 App-V package.</span></span>

7.  <span data-ttu-id="b4648-334">Vérifiez que le fichier de configuration de déploiement du package du plug-in a les mêmes paramètres que le package App-V pour Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-334">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2013 App-V package has.</span></span>

    <span data-ttu-id="b4648-335">Dans la mesure où le package App-V d’Office 2013 est intégré au système d’exploitation, les paramètres de package du plug-in doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="b4648-335">Since the Office 2013 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="b4648-336">Vous pouvez effectuer une recherche dans le fichier de configuration de déploiement pour «mode COM» et vous assurer que la valeur de votre package de plug-ins est «intégrée» et que les «InProcessEnabled» et «OutOfProcessEnabled» correspondent aux paramètres du package application Office 2013 V publié.</span><span class="sxs-lookup"><span data-stu-id="b4648-336">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2013 App-V package you published.</span></span>

8.  <span data-ttu-id="b4648-337">Ouvrez le fichier de configuration de déploiement et attribuez la valeur **false**aux **objets activés** .</span><span class="sxs-lookup"><span data-stu-id="b4648-337">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="b4648-338">Si vous avez apporté des modifications au fichier de configuration de déploiement après le séquençage, assurez-vous que le package du plug-in est publié avec le fichier.</span><span class="sxs-lookup"><span data-stu-id="b4648-338">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="b4648-339">Vérifiez que le groupe de connexion que vous avez créé est activé sur l’ordinateur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b4648-339">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="b4648-340">Le groupe de connexion créé est probablement «en attente» si le package App-V d’Office 2013 est en cours d’utilisation lorsque le groupe de connexion est activé.</span><span class="sxs-lookup"><span data-stu-id="b4648-340">The Connection Group created will likely “pend” if the Office 2013 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="b4648-341">Si tel est le cas, vous devez redémarrer pour pouvoir activer le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="b4648-341">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="b4648-342">Une fois que vous avez correctement publié les deux packages et activé le groupe de connexion, démarrez l’application Office 2013 cible et vérifiez que le plug-in que vous avez publié et ajouté au groupe de connexions fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="b4648-342">After you successfully publish both packages and enable the Connection Group, start the target Office 2013 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="b4648-343">Désactivation des applications Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-343">Disabling Office 2013 applications</span></span>

<span data-ttu-id="b4648-344">Il est possible que vous souhaitiez désactiver des applications spécifiques dans votre package d’application Office V.</span><span class="sxs-lookup"><span data-stu-id="b4648-344">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="b4648-345">Par exemple, vous pouvez désactiver l’accès sans avoir accès au principal de l’application Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-345">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="b4648-346">Lorsque vous désactivez une application, l’utilisateur final ne verra plus le raccourci de l’application.</span><span class="sxs-lookup"><span data-stu-id="b4648-346">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="b4648-347">Vous n’avez pas besoin de relancer l’application.</span><span class="sxs-lookup"><span data-stu-id="b4648-347">You do not have to re-sequence the application.</span></span> <span data-ttu-id="b4648-348">Lorsque vous modifiez le fichier de configuration de déploiement une fois que le package App-V pour Office 2013 a été publié, vous enverrez les modifications, vous ajoutez le package App-V d’Office 2013, puis vous le republiez avec le nouveau fichier de configuration de déploiement pour appliquer les nouveaux paramètres aux applications Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-348">When you change the Deployment Configuration File after the Office 2013 App-V package has been published, you will save the changes, add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

**<span data-ttu-id="b4648-349">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4648-349">Note</span></span>**  
<span data-ttu-id="b4648-350">Pour exclure des applications Office spécifiques (par exemple, Access et InfoPath) lors de la création du package App-V avec l’outil déploiement d’Office, utilisez le paramètre **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="b4648-350">To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span> <span data-ttu-id="b4648-351">Pour plus d’informations, voir informations [de référence sur le fichier démarrer en un clic configuration.xml](https://technet.microsoft.com/library/jj219426.aspx).</span><span class="sxs-lookup"><span data-stu-id="b4648-351">For more information, see [Reference for Click-to-Run configuration.xml file](https://technet.microsoft.com/library/jj219426.aspx).</span></span>



**<span data-ttu-id="b4648-352">Pour désactiver une application Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-352">To disable an Office 2013 application</span></span>**

1.  <span data-ttu-id="b4648-353">Ouvrez un fichier de configuration de déploiement avec un éditeur de texte tel que **le bloc-notes** et recherchez «applications».</span><span class="sxs-lookup"><span data-stu-id="b4648-353">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="b4648-354">Recherchez l’application Office que vous voulez désactiver, par exemple, Access 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-354">Search for the Office application you want to disable, for example, Access 2013.</span></span>

3.  <span data-ttu-id="b4648-355">Remplacez la valeur «Enabled» par «true» par «false».</span><span class="sxs-lookup"><span data-stu-id="b4648-355">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="b4648-356">Enregistrez le fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="b4648-356">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="b4648-357">Ajoutez le package App-V pour Office 2013 avec le nouveau fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="b4648-357">Add the Office 2013 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot)]\officefl5\INFOPATH.EXE" Enabled="true">
      <VisualElements>
        <Name>InfoPath Filler 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[{AppVPackageRoot}]\office15\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office15\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="b4648-358">Ajoutez à nouveau le package App-V pour Office 2013, puis republiez-le avec le nouveau fichier de configuration de déploiement pour appliquer les nouveaux paramètres aux applications Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-358">Re-add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="b4648-359">Désactivation des raccourcis d’Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-359">Disabling Office 2013 shortcuts</span></span>

<span data-ttu-id="b4648-360">Vous pouvez désactiver les raccourcis pour certaines applications Office au lieu d’annuler la publication ou de la suppression du package.</span><span class="sxs-lookup"><span data-stu-id="b4648-360">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="b4648-361">L’exemple suivant explique comment désactiver les raccourcis clavier pour Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b4648-361">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="b4648-362">Pour désactiver les raccourcis pour les applications Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-362">To disable shortcuts for Office 2013 applications</span></span>**

1.  <span data-ttu-id="b4648-363">Ouvrez un fichier de configuration de déploiement dans le bloc-notes et recherchez «raccourcis».</span><span class="sxs-lookup"><span data-stu-id="b4648-363">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="b4648-364">Pour désactiver certains raccourcis, vous pouvez supprimer ou commenter les raccourcis spécifiques que vous ne voulez pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="b4648-364">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="b4648-365">Vous devez laisser le sous-système présenter et activé.</span><span class="sxs-lookup"><span data-stu-id="b4648-365">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="b4648-366">Par exemple, dans l’exemple ci-dessous, supprimez les raccourcis de Microsoft Access, tout en conservant le raccourci vers le sous-système &lt; &gt; &lt; /Shortcut &gt; intact pour désactiver le raccourci Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b4648-366">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2013\Access 2013.lnk</File>
           <Target>[{AppvPackageRoot}])office15\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office15\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="b4648-367">Enregistrez le fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="b4648-367">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="b4648-368">Republiez le package App-V d’Office 2013 avec un nouveau fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="b4648-368">Republish Office 2013 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="b4648-369">Il est possible de modifier de nombreux paramètres supplémentaires par le biais de la modification de la configuration de déploiement pour les packages App-V (par exemple, associations de types de fichiers, système de fichiers virtuel, etc.).</span><span class="sxs-lookup"><span data-stu-id="b4648-369">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="b4648-370">Pour plus d’informations sur l’utilisation des fichiers de configuration de déploiement pour modifier les paramètres de package App-V, reportez-vous à la section ressources supplémentaires à la fin de ce document.</span><span class="sxs-lookup"><span data-stu-id="b4648-370">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="b4648-371">Gestion des mises à jour de package Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-371">Managing Office 2013 package upgrades</span></span>

<span data-ttu-id="b4648-372">Pour mettre à niveau un package 2013 Office, utilisez l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-372">To upgrade an Office 2013 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="b4648-373">Pour effectuer la mise à niveau d’un package 2013 Office, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="b4648-373">To upgrade a previously deployed Office 2013 package, perform the following steps.</span></span>

**<span data-ttu-id="b4648-374">Comment mettre à niveau un package Office 2013 déjà déployé</span><span class="sxs-lookup"><span data-stu-id="b4648-374">How to upgrade a previously deployed Office 2013 package</span></span>**

1.  <span data-ttu-id="b4648-375">Créer un nouveau package Office 2013 par le biais de l’outil déploiement d’Office qui utilise le logiciel d’application Office 2013 le plus récent.</span><span class="sxs-lookup"><span data-stu-id="b4648-375">Create a new Office 2013 package through the Office Deployment Tool that uses the most recent Office 2013 application software.</span></span> <span data-ttu-id="b4648-376">Les derniers bits d’Office 2013 peuvent toujours être obtenus par le biais de la phase de téléchargement de la création d’un package App-V pour Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b4648-376">The most recent Office 2013 bits can always be obtained through the download stage of creating an Office 2013 App-V Package.</span></span> <span data-ttu-id="b4648-377">Le package 2013 Office qui vient d’être créé dispose des dernières mises à jour et un nouvel ID de version.</span><span class="sxs-lookup"><span data-stu-id="b4648-377">The newly created Office 2013 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="b4648-378">Tous les packages créés à l’aide de l’outil déploiement d’Office ont la même ligne.</span><span class="sxs-lookup"><span data-stu-id="b4648-378">All packages created using the Office Deployment Tool have the same lineage.</span></span>

    **<span data-ttu-id="b4648-379">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4648-379">Note</span></span>**  
    <span data-ttu-id="b4648-380">Les packages d’application Office V possèdent deux ID de version:</span><span class="sxs-lookup"><span data-stu-id="b4648-380">Office App-V packages have two Version IDs:</span></span>

    -   <span data-ttu-id="b4648-381">ID de version d’un package App-V Office 2013 unique pour tous les packages créés à l’aide de l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-381">An Office 2013 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span>

    -   <span data-ttu-id="b4648-382">Un deuxième ID de version de package App-V, x. x. x. x par exemple, dans le manifeste AppX qui changera uniquement s’il existe une nouvelle version d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-382">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="b4648-383">Par exemple, si une nouvelle version d’Office 2013 avec des mises à niveau est disponible et qu’un package est créé par le biais de l’outil déploiement d’Office pour incorporer ces mises à jour, l’ID de version X. X. X. X sera modifié de manière à refléter la modification de la version d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-383">For example, if a new Office 2013 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="b4648-384">Le serveur App-V utilisera l’ID de version X. X. X. X pour différencier ce package et détecter qu’il contient de nouvelles mises à niveau du package déjà publié et, par conséquent, le publier dans le cadre d’une mise à niveau vers le package Office 2013 existant.</span><span class="sxs-lookup"><span data-stu-id="b4648-384">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2013 package.</span></span>



2.  <span data-ttu-id="b4648-385">Publiez globalement les packages d’application Office 2013 nouvellement créés sur les ordinateurs sur lesquels vous souhaitez appliquer les nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b4648-385">Globally publish the newly created Office 2013 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="b4648-386">Dans la mesure où le nouveau package utilise la même ligne de l’ancien package de l’application Office 2013-V, la publication du nouveau package avec les mises à jour apportera uniquement les nouvelles modifications apportées à l’ancien package et sera donc rapide.</span><span class="sxs-lookup"><span data-stu-id="b4648-386">Since the new package has the same lineage of the older Office 2013 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3.  <span data-ttu-id="b4648-387">Les mises à niveau seront appliquées de la même manière que les packages App-V globalement publiés.</span><span class="sxs-lookup"><span data-stu-id="b4648-387">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="b4648-388">Étant donné que les applications seront probablement utilisées, les mises à niveau peuvent être retardées jusqu’au redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b4648-388">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>

### <a href="" id="bkmk-manage-office-lic-upgrd"></a><span data-ttu-id="b4648-389">Gestion des mises à niveau de la gestion des licences Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-389">Managing Office 2013 licensing upgrades</span></span>

<span data-ttu-id="b4648-390">Si un nouveau package App-V d’Office 2013 a une licence différente de celle du package App-V pour Office 2013 actuellement déployé.</span><span class="sxs-lookup"><span data-stu-id="b4648-390">If a new Office 2013 App-V Package has a different license than the Office 2013 App-V Package currently deployed.</span></span> <span data-ttu-id="b4648-391">Par exemple, le package 2013 Office déployé est un abonnement Office 2013 et le nouveau package Office 2013 est basé sur les licences en volume, les instructions suivantes doivent être suivies pour garantir la mise à niveau de la gestion des licences:</span><span class="sxs-lookup"><span data-stu-id="b4648-391">For instance, the Office 2013 package deployed is a subscription based Office 2013 and the new Office 2013 package is Volume Licensing based, the following instructions must be followed to ensure smooth licensing upgrade:</span></span>

**<span data-ttu-id="b4648-392">Comment mettre à niveau une licence Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4648-392">How to upgrade an Office 2013 License</span></span>**

1.  <span data-ttu-id="b4648-393">Annulez la publication du package App-V du programme de licence d’abonnement Office 2013 déjà déployé.</span><span class="sxs-lookup"><span data-stu-id="b4648-393">Unpublish the already deployed Office 2013 Subscription Licensing App-V package.</span></span>

2.  <span data-ttu-id="b4648-394">Supprimez le package App-V de l’abonnement Office 2013 non publié.</span><span class="sxs-lookup"><span data-stu-id="b4648-394">Remove the unpublished Office 2013 Subscription Licensing App-V package.</span></span>

3.  <span data-ttu-id="b4648-395">Redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b4648-395">Restart the computer.</span></span>

4.  <span data-ttu-id="b4648-396">Ajoutez la nouvelle version de licence en volume d’Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b4648-396">Add the new Office 2013 App-V Package Volume Licensing.</span></span>

5.  <span data-ttu-id="b4648-397">Publiez l’application Office 2013 App-V ajoutée avec le programme de licence en volume.</span><span class="sxs-lookup"><span data-stu-id="b4648-397">Publish the added Office 2013 App-V Package with Volume Licensing.</span></span>

<span data-ttu-id="b4648-398">Un package App-V pour Office 2013 avec les licences que vous avez choisies sera déployé avec succès.</span><span class="sxs-lookup"><span data-stu-id="b4648-398">An Office 2013 App-V Package with your chosen licensing will be successfully deployed.</span></span>

### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="b4648-399">Déploiement de Visio 2013 et de Project 2013 avec Office</span><span class="sxs-lookup"><span data-stu-id="b4648-399">Deploying Visio 2013 and Project 2013 with Office</span></span>

<span data-ttu-id="b4648-400">Le tableau suivant décrit les exigences et les options de déploiement de Visio 2013 et de Project 2013 avec Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-400">The following table describes the requirements and options for deploying Visio 2013 and Project 2013 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4648-401">Tâche</span><span class="sxs-lookup"><span data-stu-id="b4648-401">Task</span></span></th>
<th align="left"><span data-ttu-id="b4648-402">Détails</span><span class="sxs-lookup"><span data-stu-id="b4648-402">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4648-403">Comment puis-je empaqueter et publier Visio 2013 et Project 2013 avec Office?</span><span class="sxs-lookup"><span data-stu-id="b4648-403">How do I package and publish Visio 2013 and Project 2013 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-404">Vous devez inclure Visio 2013 et Project 2013 dans le même package qu’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-404">You must include Visio 2013 and Project 2013 in the same package with Office.</span></span></p>
<p><span data-ttu-id="b4648-405">Si vous ne déployez pas Office, vous pouvez créer un package contenant Visio et/ou Project, tant que vous suivez <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> le déploiement de Microsoft Office 2010 à l’aide de App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="b4648-405">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)">Deploying Microsoft Office 2010 by Using App-V</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4648-406">Comment puis-je déployer Visio 2013 et Project 2013 vers des utilisateurs spécifiques?</span><span class="sxs-lookup"><span data-stu-id="b4648-406">How can I deploy Visio 2013 and Project 2013 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-407">Appliquez l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="b4648-407">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4648-408">Si vous souhaitez...</span><span class="sxs-lookup"><span data-stu-id="b4648-408">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="b4648-409">... Utilisez ensuite cette méthode</span><span class="sxs-lookup"><span data-stu-id="b4648-409">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4648-410">Création de deux packages différents et déploiement de chacun d’eux dans un groupe d’utilisateurs différent</span><span class="sxs-lookup"><span data-stu-id="b4648-410">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-411">Créez et déployez les packages suivants:</span><span class="sxs-lookup"><span data-stu-id="b4648-411">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="b4648-412">Package qui contient uniquement Office-déploiement sur des ordinateurs pour lesquels les utilisateurs ont besoin uniquement d’Office.</span><span class="sxs-lookup"><span data-stu-id="b4648-412">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="b4648-413">Un package qui contient Office, Visio et Project-déployer sur des ordinateurs pour lesquels les utilisateurs ont besoin des trois applications.</span><span class="sxs-lookup"><span data-stu-id="b4648-413">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4648-414">Si vous n’avez besoin que d’un seul package pour l’ensemble de votre organisation, ou si vous avez des utilisateurs qui partagent des ordinateurs:</span><span class="sxs-lookup"><span data-stu-id="b4648-414">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4648-415">Procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="b4648-415">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="b4648-416">Créer un package qui contient Office, Visio et Project.</span><span class="sxs-lookup"><span data-stu-id="b4648-416">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="b4648-417">Déployer le package auprès de tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b4648-417">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="b4648-418">Utilisez <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> pour empêcher des utilisateurs spécifiques d’utiliser Visio et Project.</span><span class="sxs-lookup"><span data-stu-id="b4648-418">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="b4648-419">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b4648-419">Additional resources</span></span>


**<span data-ttu-id="b4648-420">Office 2013 App-V-packages de ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b4648-420">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="b4648-421">Outil déploiement d’Office pour Office «démarrer en un clic»</span><span class="sxs-lookup"><span data-stu-id="b4648-421">Office Deployment Tool for Click-to-Run</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[<span data-ttu-id="b4648-422">Scénarios pris en charge pour le déploiement de Microsoft Office en tant que package App-V séquencé</span><span class="sxs-lookup"><span data-stu-id="b4648-422">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="b4648-423">Packages App-V d’Office 2010</span><span class="sxs-lookup"><span data-stu-id="b4648-423">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="b4648-424">Kit de séquençage Microsoft Office 2010 pour Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="b4648-424">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="b4648-425">Problèmes connus lors de la création ou de l’utilisation d’un package App-V 5,0 Office 2010</span><span class="sxs-lookup"><span data-stu-id="b4648-425">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="b4648-426">Comment séquencer Microsoft Office 2010 dans Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="b4648-426">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="b4648-427">Groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="b4648-427">Connection Groups</span></span>**

[<span data-ttu-id="b4648-428">Déploiement de groupes de connexion dans Microsoft App-V v5</span><span class="sxs-lookup"><span data-stu-id="b4648-428">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="b4648-429">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="b4648-429">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="b4648-430">Configuration dynamique</span><span class="sxs-lookup"><span data-stu-id="b4648-430">Dynamic Configuration</span></span>**

[<span data-ttu-id="b4648-431">À propos de la configuration dynamique d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="b4648-431">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)















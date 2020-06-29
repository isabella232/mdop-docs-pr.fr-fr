---
title: À propos d'App-V5.1
description: À propos d'App-V5.1
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806109"
---
# <span data-ttu-id="7be1e-103">À propos d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="7be1e-103">About App-V 5.1</span></span>


<span data-ttu-id="7be1e-104">Les sections suivantes permettent de consulter des informations sur les modifications importantes apportées à l’application virtualisation des applications (App-V) 5,1:</span><span class="sxs-lookup"><span data-stu-id="7be1e-104">Use the following sections to review information about significant changes that apply to Application Virtualization (App-V) 5.1:</span></span>

[<span data-ttu-id="7be1e-105">Conditions préalables pour le logiciel App-V 5,1 et configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="7be1e-105">App-V 5.1 software prerequisites and supported configurations</span></span>](#bkmk-51-prereq-configs)

[<span data-ttu-id="7be1e-106">Migration vers App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-106">Migrating to App-V 5.1</span></span>](#bkmk-migrate-to-51)

[<span data-ttu-id="7be1e-107">Nouveautés de l’application-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-107">What’s New in App-V 5.1</span></span>](#bkmk-whatsnew)

[<span data-ttu-id="7be1e-108">Prise en charge de App-V pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="7be1e-108">App-V support for Windows 10</span></span>](#bkmk-win10support)

[<span data-ttu-id="7be1e-109">Modifications apportées à la console de gestion App-V</span><span class="sxs-lookup"><span data-stu-id="7be1e-109">App-V Management Console Changes</span></span>](#bkmk-mgmtconsole)

[<span data-ttu-id="7be1e-110">Améliorations apportées au Sequencer</span><span class="sxs-lookup"><span data-stu-id="7be1e-110">Sequencer Improvements</span></span>](#bkmk-seqimprove)

[<span data-ttu-id="7be1e-111">Améliorations apportées au convertisseur de package</span><span class="sxs-lookup"><span data-stu-id="7be1e-111">Improvements to Package Converter</span></span>](#bkmk-pkgconvimprove)

[<span data-ttu-id="7be1e-112">Prise en charge de plusieurs scripts sur un seul déclencheur d’événements</span><span class="sxs-lookup"><span data-stu-id="7be1e-112">Support for multiple scripts on a single event trigger</span></span>](#bkmk-supmultscripts)

[<span data-ttu-id="7be1e-113">Le chemin d’accès codé au dossier d’installation est redirigé vers la racine du système de fichiers virtuel</span><span class="sxs-lookup"><span data-stu-id="7be1e-113">Hardcoded path to installation folder is redirected to virtual file system root</span></span>](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a><span data-ttu-id="7be1e-114">Conditions préalables pour le logiciel App-V 5,1 et configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="7be1e-114">App-V 5.1 software prerequisites and supported configurations</span></span>


<span data-ttu-id="7be1e-115">Pour plus d’informations 5,1 sur les configurations logicielles prises en charge, voir les liens suivants:</span><span class="sxs-lookup"><span data-stu-id="7be1e-115">See the following links for the App-V 5.1 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be1e-116">Liens vers les composants requis et les configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="7be1e-116">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="7be1e-117">Description</span><span class="sxs-lookup"><span data-stu-id="7be1e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)"><span data-ttu-id="7be1e-118">Composants requis d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="7be1e-118">App-V 5.1 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="7be1e-119">Logiciels requis que vous devez installer avant de démarrer l’installation App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-119">Prerequisite software that you must install before starting the App-V 5.1 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="7be1e-120">Configurations prises en charge par App-V5.1</span><span class="sxs-lookup"><span data-stu-id="7be1e-120">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="7be1e-121">Systèmes d’exploitation pris en charge et configuration matérielle requise pour le serveur App-V, le Sequencer et les composants clients</span><span class="sxs-lookup"><span data-stu-id="7be1e-121">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7be1e-122">**Prise en charge de l’utilisation de Configuration Manager avec App-V:** App-V 5,1 prend en charge System Center 2012 R2 Configuration Manager SP1.</span><span class="sxs-lookup"><span data-stu-id="7be1e-122">**Support for using Configuration Manager with App-V:** App-V 5.1 supports System Center 2012 R2 Configuration Manager SP1.</span></span> <span data-ttu-id="7be1e-123">Pour plus d’informations sur l’intégration de votre environnement App-v au gestionnaire de configuration et à la gestion de configuration, voir [planification de l’intégration d’App-v à Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7be1e-123">See [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) for information about integrating your App-V environment with Configuration Manager and Configuration Manager.</span></span>

## <a href="" id="bkmk-migrate-to-51"></a><span data-ttu-id="7be1e-124">Migration vers App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-124">Migrating to App-V 5.1</span></span>


<span data-ttu-id="7be1e-125">Utilisez les informations ci-dessous pour effectuer une mise à niveau vers l’application-V 5,1 à partir d’une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="7be1e-125">Use the following information to upgrade to App-V 5.1 from earlier versions.</span></span> <span data-ttu-id="7be1e-126">Pour plus d’informations, reportez-vous [à la rubrique migration vers App-V 5,1 à partir d’une version précédente](migrating-to-app-v-51-from-a-previous-version.md) .</span><span class="sxs-lookup"><span data-stu-id="7be1e-126">See [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md) for more information.</span></span>

### <span data-ttu-id="7be1e-127">Avant de commencer la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="7be1e-127">Before you start the upgrade</span></span>

<span data-ttu-id="7be1e-128">Passez en revue les informations suivantes avant de commencer la mise à niveau:</span><span class="sxs-lookup"><span data-stu-id="7be1e-128">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be1e-129">Éléments à réviser avant la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="7be1e-129">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="7be1e-130">Description</span><span class="sxs-lookup"><span data-stu-id="7be1e-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-131">Composants à mettre à niveau, dans n’importe quel ordre</span><span class="sxs-lookup"><span data-stu-id="7be1e-131">Components to upgrade, in any order</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="7be1e-132">App-V Server</span><span class="sxs-lookup"><span data-stu-id="7be1e-132">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="7be1e-133">Sequencer</span><span class="sxs-lookup"><span data-stu-id="7be1e-133">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="7be1e-134">Client App-V ou App-V (service bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="7be1e-134">App-V Client or App-V Remote Desktop Services (RDS) Client</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="7be1e-135">Remarque</span><span class="sxs-lookup"><span data-stu-id="7be1e-135">Note</span></span></strong><br/><p><span data-ttu-id="7be1e-136">Avant le SP2 App-V 5,0, l’interface utilisateur de gestion des clients a été fournie avec l’installation du client App-V.</span><span class="sxs-lookup"><span data-stu-id="7be1e-136">Prior to App-V 5.0 SP2, the Client Management User Interface (UI) was provided with the App-V Client installation.</span></span> <span data-ttu-id="7be1e-137">Pour les installations d’App-V 5,0 SP2 (ou version ultérieure), vous pouvez utiliser l’interface utilisateur de gestion du client en le téléchargeant à partir de l’application de l' <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> interface utilisateur du client de virtualisation des applications 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="7be1e-137">For App-V 5.0 SP2 installations (or later), you can use the Client Management UI by downloading from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be1e-138">Mise à niveau à partir de App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="7be1e-138">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-139">Vous devez d’abord effectuer une mise à niveau vers App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7be1e-139">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="7be1e-140">Vous ne pouvez pas effectuer la mise à niveau directement de App-V 4. x vers App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be1e-140">You cannot upgrade directly from App-V 4.x to App-V 5.1.</span></span> <span data-ttu-id="7be1e-141">Pour plus d’informations, voir:</span><span class="sxs-lookup"><span data-stu-id="7be1e-141">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="7be1e-142">«Différences entre App-V 4,6 et App-V 5,0» dans <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> à propos de App-v 5,0</span><span class="sxs-lookup"><span data-stu-id="7be1e-142">“Differences between App-V 4.6 and App-V 5.0” in <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">About App-V 5.0</span></span></a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="7be1e-143">Planification d'une migration à partir d'une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="7be1e-143">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-144">Mise à niveau à partir de App-V 5,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7be1e-144">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-145">Vous pouvez effectuer une mise à niveau vers App-V 5,1 directement à partir des versions suivantes:</span><span class="sxs-lookup"><span data-stu-id="7be1e-145">You can upgrade to App-V 5.1 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="7be1e-146">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="7be1e-146">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="7be1e-147">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="7be1e-147">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="7be1e-148">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="7be1e-148">App-V 5.0 SP2</span></span></p></li>
<li><p><span data-ttu-id="7be1e-149">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="7be1e-149">App-V 5.0 SP3</span></span></p></li>
</ul>
<p><span data-ttu-id="7be1e-150">Pour effectuer une mise à niveau vers App-V 5,1, suivez les étapes décrites dans les sections restantes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7be1e-150">To upgrade to App-V 5.1, follow the steps in the remaining sections of this topic.</span></span></p>
<p><span data-ttu-id="7be1e-151">Les packages et les groupes de connexion continuent de fonctionner avec l’application-V 5,1 comme il le fait actuellement.</span><span class="sxs-lookup"><span data-stu-id="7be1e-151">Packages and connection groups will continue to work with App-V 5.1 as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="7be1e-152">Procédure de mise à niveau de l’infrastructure App-V</span><span class="sxs-lookup"><span data-stu-id="7be1e-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="7be1e-153">Suivez les étapes ci-dessous pour mettre à niveau chaque composant de l’infrastructure App-V vers App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be1e-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.1.</span></span> <span data-ttu-id="7be1e-154">L’ordre suivant n’est qu’une suggestion; vous pouvez mettre à niveau des composants dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="7be1e-154">The following order is only a suggestion; you may upgrade components in any order.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be1e-155">Étape</span><span class="sxs-lookup"><span data-stu-id="7be1e-155">Step</span></span></th>
<th align="left"><span data-ttu-id="7be1e-156">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="7be1e-156">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-157">Étape 1: mettez à niveau le serveur App-V.</span><span class="sxs-lookup"><span data-stu-id="7be1e-157">Step 1: Upgrade the App-V Server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7be1e-158">Remarque</span><span class="sxs-lookup"><span data-stu-id="7be1e-158">Note</span></span></strong><br/><p><span data-ttu-id="7be1e-159">Si vous n’utilisez pas le serveur App-V, ignorez cette étape et passez à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="7be1e-159">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="7be1e-160">Procédez comme suit: </span><span class="sxs-lookup"><span data-stu-id="7be1e-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="7be1e-161">Effectuez l’une des opérations suivantes, selon la méthode que vous utilisez pour mettre à niveau la base de données de gestion et/ou la base de données de création de rapports, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="7be1e-161">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be1e-162">Méthode de mise à niveau de base de données</span><span class="sxs-lookup"><span data-stu-id="7be1e-162">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="7be1e-163">Étape</span><span class="sxs-lookup"><span data-stu-id="7be1e-163">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-164">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7be1e-164">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-165">Ignorez cette étape et passez à l’étape 2, «si vous effectuez la mise à niveau de l’application-V Server».</span><span class="sxs-lookup"><span data-stu-id="7be1e-165">Skip this step and go to step 2, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be1e-166">Scripts SQL</span><span class="sxs-lookup"><span data-stu-id="7be1e-166">SQL scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-167">Suivez les étapes décrites dans la <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> procédure de déploiement des bases de données App-V à l’aide de scripts SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="7be1e-167">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<li><p><span data-ttu-id="7be1e-168">Si vous effectuez une mise à niveau de l’application-V Server à partir du correctif logiciel App-V 5,0 SP1 ou version ultérieure, suivez les étapes de la section <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> vérifier les clés de registre après l’installation de l’app-v 5,0 SP3 Server </a> .</span><span class="sxs-lookup"><span data-stu-id="7be1e-168">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="7be1e-169">Suivez les étapes décrites dans la <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> procédure de déploiement du serveur App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-169">Follow the steps in <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be1e-170">Étape 2: mettre à niveau le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="7be1e-170">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-171">Découvrez <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Comment installer le Sequencer </a> .</span><span class="sxs-lookup"><span data-stu-id="7be1e-171">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-172">Étape 3: mettez à niveau le client App-V ou le client RDS (App-V).</span><span class="sxs-lookup"><span data-stu-id="7be1e-172">Step 3: Upgrade the App-V Client or App-V RDS Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-173">Découvrez <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> comment déployer le client App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="7be1e-173">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7be1e-174">Conversion de packages créés à l’aide d’une version antérieure d’App-V</span><span class="sxs-lookup"><span data-stu-id="7be1e-174">Converting packages created using a prior version of App-V</span></span>

<span data-ttu-id="7be1e-175">Utilisez l’utilitaire convertisseur de package pour mettre à niveau des packages d’application virtuels créés à l’aide de versions de App-V antérieures à App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7be1e-175">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="7be1e-176">Le convertisseur de package utilise PowerShell pour convertir des packages et peut faciliter l’automatisation du processus si vous avez de nombreux packages qui nécessitent une conversion.</span><span class="sxs-lookup"><span data-stu-id="7be1e-176">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

**<span data-ttu-id="7be1e-177">Remarque</span><span class="sxs-lookup"><span data-stu-id="7be1e-177">Note</span></span>**  
<span data-ttu-id="7be1e-178">Les packages App-V 5,1 sont exactement les mêmes que les packages App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7be1e-178">App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="7be1e-179">Il n’y a aucune modification du format de package entre les versions et il n’est donc pas nécessaire de convertir les packages App-V 5,0 en packages App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be1e-179">There has been no change in the package format between the versions and so there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>



## <a href="" id="bkmk-whatsnew"></a><span data-ttu-id="7be1e-180">Nouveautés de l’application-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-180">What’s New in App-V 5.1</span></span>


<span data-ttu-id="7be1e-181">Ces sections concernent les utilisateurs qui connaissent déjà App-V et qui souhaitent savoir ce qui a changé dans App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be1e-181">These sections are for users who are already familiar with App-V and want to know what has changed in App-V 5.1.</span></span> <span data-ttu-id="7be1e-182">Si vous n’avez pas encore l’habitude d’utiliser l’application-V, vous devez commencer par lire la [planification pour App-v 5,1](planning-for-app-v-51.md).</span><span class="sxs-lookup"><span data-stu-id="7be1e-182">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.1](planning-for-app-v-51.md).</span></span>

### <a href="" id="bkmk-win10support"></a><span data-ttu-id="7be1e-183">Prise en charge de App-V pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="7be1e-183">App-V support for Windows 10</span></span>

<span data-ttu-id="7be1e-184">Le tableau suivant répertorie la prise en charge de Windows 10 pour App-V.</span><span class="sxs-lookup"><span data-stu-id="7be1e-184">The following table lists the Windows 10 support for App-V.</span></span> <span data-ttu-id="7be1e-185">Windows 10 n’est pas pris en charge dans les versions de App-V antérieures à App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be1e-185">Windows 10 is not supported in versions of App-V prior to App-V 5.1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be1e-186">Composant</span><span class="sxs-lookup"><span data-stu-id="7be1e-186">Component</span></span></th>
<th align="left"><span data-ttu-id="7be1e-187">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="7be1e-187">App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="7be1e-188">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="7be1e-188">App-V 5.0</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-189">Client App-V</span><span class="sxs-lookup"><span data-stu-id="7be1e-189">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-190">Oui</span><span class="sxs-lookup"><span data-stu-id="7be1e-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-191">Non</span><span class="sxs-lookup"><span data-stu-id="7be1e-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be1e-192">Client de RDS App-V</span><span class="sxs-lookup"><span data-stu-id="7be1e-192">App-V RDS Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-193">Oui</span><span class="sxs-lookup"><span data-stu-id="7be1e-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-194">Non</span><span class="sxs-lookup"><span data-stu-id="7be1e-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-195">Séquenceur App-V</span><span class="sxs-lookup"><span data-stu-id="7be1e-195">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-196">Oui</span><span class="sxs-lookup"><span data-stu-id="7be1e-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-197">Non</span><span class="sxs-lookup"><span data-stu-id="7be1e-197">No</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a><span data-ttu-id="7be1e-198">Modifications apportées à la console de gestion App-V</span><span class="sxs-lookup"><span data-stu-id="7be1e-198">App-V Management Console Changes</span></span>

<span data-ttu-id="7be1e-199">Cette section compare les fonctionnalités actuelles et précédentes de la console de gestion de l’application.</span><span class="sxs-lookup"><span data-stu-id="7be1e-199">This section compares the App-V Management Console’s current and previous functionality.</span></span>

### <span data-ttu-id="7be1e-200">Silverlight n’est plus nécessaire</span><span class="sxs-lookup"><span data-stu-id="7be1e-200">Silverlight is no longer required</span></span>

<span data-ttu-id="7be1e-201">L’interface utilisateur de la console de gestion n’exige plus Silverlight.</span><span class="sxs-lookup"><span data-stu-id="7be1e-201">The Management Console UI no longer requires Silverlight.</span></span> <span data-ttu-id="7be1e-202">La console de gestion 5,1 est basée sur HTML5 et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7be1e-202">The 5.1 Management Console is built on HTML5 and Javascript.</span></span>

### <span data-ttu-id="7be1e-203">Les notifications et les messages s’affichent individuellement dans une boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="7be1e-203">Notifications and messages are displayed individually in a dialog box</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be1e-204">Nouveauté de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-204">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="7be1e-205">Avant l’application-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-205">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7be1e-206">Nombre d’indicateur de messages:</span><span class="sxs-lookup"><span data-stu-id="7be1e-206">Number of messages indicator:</span></span></strong></p>
<p><span data-ttu-id="7be1e-207">Dans la barre de titre de la console de gestion App-V, un numéro est désormais affiché en regard d’une icône d’indicateur indiquant le nombre de messages en attente de lecture.</span><span class="sxs-lookup"><span data-stu-id="7be1e-207">On the title bar of the App-V Management Console, a number is now displayed next to a flag icon to indicate the number of messages that are waiting to be read.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-208">Vous ne pouviez voir qu’un seul message ou erreur à la fois, et vous n’êtes pas en mesure de déterminer le nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="7be1e-208">You could see only one message or error at a time, and you were unable to determine how many messages there were.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7be1e-209">Aspect du message:</span><span class="sxs-lookup"><span data-stu-id="7be1e-209">Message appearance:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="7be1e-210">Les messages qui requièrent une entrée utilisateur s’affichent dans une boîte de dialogue séparée qui s’affiche en haut de la page actuellement affichée et nécessitent une réponse avant de pouvoir les faire disparaître.</span><span class="sxs-lookup"><span data-stu-id="7be1e-210">Messages that require user input appear in a separate dialog box that displays on top of the current page that you were viewing, and require a response before you can dismiss them.</span></span></p></li>
<li><p><span data-ttu-id="7be1e-211">Les messages et les erreurs apparaissent dans une liste, l’un sous l’autre.</span><span class="sxs-lookup"><span data-stu-id="7be1e-211">Messages and errors appear in a list, with one beneath the other.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="7be1e-212">Vous ne pouviez voir qu’un seul message ou erreur à la fois.</span><span class="sxs-lookup"><span data-stu-id="7be1e-212">You could see only one message or error at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7be1e-213">Ignorer les messages:</span><span class="sxs-lookup"><span data-stu-id="7be1e-213">Dismissing messages:</span></span></strong></p>
<p><span data-ttu-id="7be1e-214">Utilisez le <strong> lien rejeter tout </strong> pour masquer tous les messages et erreurs en une fois, ou les ignorer un par un.</span><span class="sxs-lookup"><span data-stu-id="7be1e-214">Use the <strong>Dismiss All</strong> link to dismiss all messages and errors at one time, or dismiss them one at a time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-215">Vous pouvez faire disparaître des messages et des erreurs une seule fois.</span><span class="sxs-lookup"><span data-stu-id="7be1e-215">You could dismiss messages and errors only one at a time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7be1e-216">Les pages de console sont désormais des URL distinctes</span><span class="sxs-lookup"><span data-stu-id="7be1e-216">Console pages are now separate URLs</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be1e-217">Nouveauté de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-217">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="7be1e-218">Avant l’application-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-218">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-219">Chaque page de la console possède une autre URL qui vous permet de marquer des pages spécifiques pour un accès rapide à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="7be1e-219">Each page in the console has a different URL, which enables you to bookmark specific pages for quick access in the future.</span></span></p>
<p><span data-ttu-id="7be1e-220">Le nombre qui apparaît dans certaines URL indique le package spécifique.</span><span class="sxs-lookup"><span data-stu-id="7be1e-220">The number that appears in some URLs indicates the specific package.</span></span> <span data-ttu-id="7be1e-221">Ces numéros sont uniques.</span><span class="sxs-lookup"><span data-stu-id="7be1e-221">These numbers are unique.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-222">Toutes les pages de la console sont accessibles par le biais de la même URL.</span><span class="sxs-lookup"><span data-stu-id="7be1e-222">All console pages are accessed through the same URL.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7be1e-223">Nouvelle page de groupes de connexion séparés et option de menu</span><span class="sxs-lookup"><span data-stu-id="7be1e-223">New, separate CONNECTION GROUPS page and menu option</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be1e-224">Nouveauté de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-224">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="7be1e-225">Avant l’application-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-225">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-226">La page groupes de connexion fait désormais partie du menu principal, au même niveau que la page PACKAGES.</span><span class="sxs-lookup"><span data-stu-id="7be1e-226">The CONNECTION GROUPS page is now part of the main menu, at the same level as the PACKAGES page.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-227">Pour ouvrir la page groupes de connexions, vous naviguez dans la page PACKAGES.</span><span class="sxs-lookup"><span data-stu-id="7be1e-227">To open the CONNECTION GROUPS page, you navigate through the PACKAGES page.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7be1e-228">Les options de menu pour les packages ont changé</span><span class="sxs-lookup"><span data-stu-id="7be1e-228">Menu options for packages have changed</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be1e-229">Nouveauté de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-229">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="7be1e-230">Avant l’application-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be1e-230">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be1e-231">Les options suivantes sont désormais des boutons qui apparaissent en bas de la page PACKAGES:</span><span class="sxs-lookup"><span data-stu-id="7be1e-231">The following options are now buttons that appear at the bottom of the PACKAGES page:</span></span></p>
<ul>
<li><p><span data-ttu-id="7be1e-232">Ajouter ou mettre à niveau</span><span class="sxs-lookup"><span data-stu-id="7be1e-232">Add or Upgrade</span></span></p></li>
<li><p><span data-ttu-id="7be1e-233">Publier</span><span class="sxs-lookup"><span data-stu-id="7be1e-233">Publish</span></span></p></li>
<li><p><span data-ttu-id="7be1e-234">Annuler la publication</span><span class="sxs-lookup"><span data-stu-id="7be1e-234">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="7be1e-235">Delete</span><span class="sxs-lookup"><span data-stu-id="7be1e-235">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="7be1e-236">Les options suivantes s’affichent quand vous cliquez avec le bouton droit sur un paquet pour ouvrir le menu contextuel de menu déroulant:</span><span class="sxs-lookup"><span data-stu-id="7be1e-236">The following options will still appear when you right-click a package to open the drop-down context menu:</span></span></p>
<ul>
<li><p><span data-ttu-id="7be1e-237">Publier</span><span class="sxs-lookup"><span data-stu-id="7be1e-237">Publish</span></span></p></li>
<li><p><span data-ttu-id="7be1e-238">Annuler la publication</span><span class="sxs-lookup"><span data-stu-id="7be1e-238">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="7be1e-239">Modifier l’accès aux publicités</span><span class="sxs-lookup"><span data-stu-id="7be1e-239">Edit AD Access</span></span></p></li>
<li><p><span data-ttu-id="7be1e-240">Modifier la configuration de déploiement</span><span class="sxs-lookup"><span data-stu-id="7be1e-240">Edit Deployment Config</span></span></p></li>
<li><p><span data-ttu-id="7be1e-241">Transférer la configuration de déploiement de...</span><span class="sxs-lookup"><span data-stu-id="7be1e-241">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="7be1e-242">Transférer l’accès et la configuration de...</span><span class="sxs-lookup"><span data-stu-id="7be1e-242">Transfer access and configuration from…</span></span></p></li>
<li><p><span data-ttu-id="7be1e-243">Delete</span><span class="sxs-lookup"><span data-stu-id="7be1e-243">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="7be1e-244">Lorsque vous cliquez sur <strong> supprimer </strong> pour supprimer un package, une boîte de dialogue s’ouvre et vous demande de confirmer que vous souhaitez supprimer le package.</span><span class="sxs-lookup"><span data-stu-id="7be1e-244">When you click <strong>Delete</strong> to remove a package, a dialog box opens and asks you to confirm that you want to delete the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be1e-245">L' <strong> option Ajouter ou mettre à niveau </strong> était un bouton dans la partie supérieure droite de la page Packages.</span><span class="sxs-lookup"><span data-stu-id="7be1e-245">The <strong>Add or Upgrade</strong> option was a button at the top right of the PACKAGES page.</span></span></p>
<p><span data-ttu-id="7be1e-246">Les <strong> </strong> options publier, <strong> Annuler </strong> et <strong> supprimer </strong> étaient disponibles uniquement si vous avez cliqué avec le bouton droit sur un nom de package dans la liste packages.</span><span class="sxs-lookup"><span data-stu-id="7be1e-246">The <strong>Publish</strong>, <strong>Unpublish</strong>, and <strong>Delete</strong> options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be1e-247">Les opérations de package suivantes sont désormais des boutons de la page Détails du package pour chaque package:</span><span class="sxs-lookup"><span data-stu-id="7be1e-247">The following package operations are now buttons on the package details page for each package:</span></span></p>
<ul>
<li><p><span data-ttu-id="7be1e-248">Transfert (menu déroulant avec les options suivantes):</span><span class="sxs-lookup"><span data-stu-id="7be1e-248">Transfer (drop-down menu with the following options):</span></span></p>
<ul>
<li><p><span data-ttu-id="7be1e-249">Transférer la configuration de déploiement de...</span><span class="sxs-lookup"><span data-stu-id="7be1e-249">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="7be1e-250">Transférer l’accès et la configuration de...</span><span class="sxs-lookup"><span data-stu-id="7be1e-250">Transfer access and configuration from…</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="7be1e-251">Modifier (groupes de connexion et accès AD)</span><span class="sxs-lookup"><span data-stu-id="7be1e-251">Edit (connection groups and AD Access)</span></span></p></li>
<li><p><span data-ttu-id="7be1e-252">Annuler la publication</span><span class="sxs-lookup"><span data-stu-id="7be1e-252">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="7be1e-253">Delete</span><span class="sxs-lookup"><span data-stu-id="7be1e-253">Delete</span></span></p></li>
<li><p><span data-ttu-id="7be1e-254">Modifier la configuration par défaut</span><span class="sxs-lookup"><span data-stu-id="7be1e-254">Edit Default Configuration</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="7be1e-255">Ces options de package n’étaient disponibles que si vous avez cliqué avec le bouton droit sur un nom de package dans la liste packages.</span><span class="sxs-lookup"><span data-stu-id="7be1e-255">These package options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7be1e-256">Les icônes dans le volet de gauche contiennent de nouvelles couleurs et du texte</span><span class="sxs-lookup"><span data-stu-id="7be1e-256">Icons in left pane have new colors and text</span></span>

<span data-ttu-id="7be1e-257">Les couleurs des icônes dans le volet de gauche ont été modifiées, et le texte qui a été ajouté pour rendre les icônes cohérentes avec d’autres produits Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7be1e-257">The colors of the icons in the left pane have been changed, and text added, to make the icons consistent with other Microsoft products.</span></span>

### <span data-ttu-id="7be1e-258">La page de présentation a été supprimée</span><span class="sxs-lookup"><span data-stu-id="7be1e-258">Overview page has been removed</span></span>

<span data-ttu-id="7be1e-259">Dans le volet gauche de la console de gestion, l’option de menu vue d’ensemble et la page de vue d’ensemble qui lui sont associées ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="7be1e-259">In the left pane of the Management Console, the OVERVIEW menu option and its associated OVERVIEW page have been removed.</span></span>

### <a href="" id="bkmk-seqimprove"></a><span data-ttu-id="7be1e-260">Améliorations apportées au Sequencer</span><span class="sxs-lookup"><span data-stu-id="7be1e-260">Sequencer Improvements</span></span>

<span data-ttu-id="7be1e-261">Les améliorations suivantes ont été apportées à l’éditeur de package dans le Sequencer App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be1e-261">The following improvements have been made to the package editor in the App-V 5.1 Sequencer.</span></span>

### <span data-ttu-id="7be1e-262">Importer et exporter le fichier manifeste</span><span class="sxs-lookup"><span data-stu-id="7be1e-262">Import and export the manifest file</span></span>

<span data-ttu-id="7be1e-263">Vous pouvez importer et exporter le fichier AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="7be1e-263">You can import and export the AppxManifest.xml file.</span></span> <span data-ttu-id="7be1e-264">Pour exporter le fichier manifeste, sélectionnez l’onglet **avancé** , puis, dans la zone fichier manifeste, cliquez sur **Exporter...**. Vous pouvez modifier le fichier manifeste, tel que la suppression d’extensions d’interpréteur de fichiers ou la modification d’associations de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="7be1e-264">To export the manifest file, select the **Advanced** tab and in the Manifest File box, click **Export...**. You can make changes to the manifest file, such as removing shell extensions or editing file type associations.</span></span>

<span data-ttu-id="7be1e-265">Après avoir apporté vos modifications, cliquez sur **Importer...** , puis sélectionnez le fichier que vous avez modifié.</span><span class="sxs-lookup"><span data-stu-id="7be1e-265">After you make your changes, click **Import...** and select the file you edited.</span></span> <span data-ttu-id="7be1e-266">Après l’importation réussie, le fichier manifeste est mis à jour immédiatement dans l’éditeur de package.</span><span class="sxs-lookup"><span data-stu-id="7be1e-266">After you successfully import it back in, the manifest file is immediately updated within the package editor.</span></span>

**<span data-ttu-id="7be1e-267">Vigilance</span><span class="sxs-lookup"><span data-stu-id="7be1e-267">Caution</span></span>**  
<span data-ttu-id="7be1e-268">Lorsque vous importez le fichier, vos modifications sont validées par rapport au schéma XML.</span><span class="sxs-lookup"><span data-stu-id="7be1e-268">When you import the file, your changes are validated against the XML schema.</span></span> <span data-ttu-id="7be1e-269">Si le fichier n’est pas valide, une erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7be1e-269">If the file is not valid, you will receive an error.</span></span> <span data-ttu-id="7be1e-270">Sachez qu’il est possible d’importer un fichier qui est validé par rapport au schéma XML, mais qui peut toujours ne pas s’exécuter pour d’autres raisons.</span><span class="sxs-lookup"><span data-stu-id="7be1e-270">Be aware that it is possible to import a file that is validated against the XML schema, but that might still fail to run for other reasons.</span></span>



### <span data-ttu-id="7be1e-271">Liste des systèmes d’exploitation Windows 10</span><span class="sxs-lookup"><span data-stu-id="7be1e-271">Addition of Windows 10 to operating systems list</span></span>

<span data-ttu-id="7be1e-272">Dans l’onglet déploiement, les bits Windows 10 32 bits et Windows 10-64 qui ont été ajoutés à la liste des systèmes d’exploitation pour lesquels vous pouvez effectuer le Sequencer d’un package.</span><span class="sxs-lookup"><span data-stu-id="7be1e-272">In the Deployment tab, Windows 10 32-bit and Windows 10-64 bit have been added to the list of operating systems for which you can sequence a package.</span></span> <span data-ttu-id="7be1e-273">Si vous sélectionnez **un système d’exploitation**, Windows 10 est automatiquement inclus parmi les systèmes d’exploitation pris en charge par le package séquencé.</span><span class="sxs-lookup"><span data-stu-id="7be1e-273">If you select **Any Operating System**, Windows 10 is automatically included among the operating systems that the sequenced package will support.</span></span>

### <span data-ttu-id="7be1e-274">Le chemin actuel s’affiche en bas de l’éditeur du Registre virtuel</span><span class="sxs-lookup"><span data-stu-id="7be1e-274">Current path displays at bottom of virtual registry editor</span></span>

<span data-ttu-id="7be1e-275">Dans l’onglet registre virtuel, le chemin d’accès s’affiche désormais en bas de l’éditeur du Registre virtuel, qui vous permet de déterminer la clé actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7be1e-275">In the Virtual Registry tab, the path now displays at the bottom of the virtual registry editor, which enables you to determine the currently selected key.</span></span> <span data-ttu-id="7be1e-276">Auparavant, vous deviez faire défiler l’arborescence du Registre pour trouver la clé actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7be1e-276">Previously, you had to scroll through the registry tree to find the currently selected key.</span></span>

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a><span data-ttu-id="7be1e-277">Combinaison de la boîte de dialogue Rechercher et remplacer» et des touches de raccourci ajoutées dans l’éditeur du Registre virtuel</span><span class="sxs-lookup"><span data-stu-id="7be1e-277">Combined “find and replace” dialog box and shortcut keys added in virtual registry editor</span></span>

<span data-ttu-id="7be1e-278">Dans l’éditeur du Registre virtuel, des raccourcis clavier ont été ajoutés pour l’option Rechercher (Ctrl + F), et une boîte de dialogue qui combine les tâches «Rechercher» et «remplacer» a été ajoutée pour vous permettre de rechercher et de remplacer des valeurs et des données.</span><span class="sxs-lookup"><span data-stu-id="7be1e-278">In the virtual registry editor, shortcut keys have been added for the Find option (Ctrl+F), and a dialog box that combines the “find” and “replace” tasks has been added to enable you to find and replace values and data.</span></span> <span data-ttu-id="7be1e-279">Pour accéder à cette boîte de dialogue combinée, sélectionnez une touche et effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="7be1e-279">To access this combined dialog box, select a key and do one of the following:</span></span>

-   <span data-ttu-id="7be1e-280">Appuyez sur **Ctrl + H** .</span><span class="sxs-lookup"><span data-stu-id="7be1e-280">Press **Ctrl+H**</span></span>

-   <span data-ttu-id="7be1e-281">Cliquez avec le bouton droit sur une touche et sélectionnez **remplacer**.</span><span class="sxs-lookup"><span data-stu-id="7be1e-281">Right-click a key and select **Replace**.</span></span>

-   <span data-ttu-id="7be1e-282">Sélectionnez **Afficher** le &gt; **Registre virtuel** &gt; **remplacer**.</span><span class="sxs-lookup"><span data-stu-id="7be1e-282">Select **View** &gt; **Virtual Registry** &gt; **Replace**.</span></span>

<span data-ttu-id="7be1e-283">Auparavant, la boîte de dialogue «remplacer» n’existait pas et vous deviez apporter les modifications manuellement.</span><span class="sxs-lookup"><span data-stu-id="7be1e-283">Previously, the “Replace” dialog box did not exist, and you had to make changes manually.</span></span>

### <span data-ttu-id="7be1e-284">Renommer correctement les clés de Registre et les fichiers de package</span><span class="sxs-lookup"><span data-stu-id="7be1e-284">Rename registry keys and package files successfully</span></span>

<span data-ttu-id="7be1e-285">Vous pouvez renommer les clés et fichiers du Registre virtuel sans problèmes de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="7be1e-285">You can rename virtual registry keys and files without experiencing Sequencer issues.</span></span> <span data-ttu-id="7be1e-286">Auparavant, le Sequencer a cessé de fonctionner si vous essayez de renommer une clé.</span><span class="sxs-lookup"><span data-stu-id="7be1e-286">Previously, the Sequencer stopped working if you tried to rename a key.</span></span>

### <span data-ttu-id="7be1e-287">Importer et exporter des clés de Registre virtuelles</span><span class="sxs-lookup"><span data-stu-id="7be1e-287">Import and export virtual registry keys</span></span>

<span data-ttu-id="7be1e-288">Vous pouvez importer et exporter des clés de Registre virtuelles.</span><span class="sxs-lookup"><span data-stu-id="7be1e-288">You can import and export virtual registry keys.</span></span> <span data-ttu-id="7be1e-289">Pour importer une clé, cliquez avec le bouton droit sur le nœud sous lequel importer la clé, accédez à la clé que vous voulez importer, puis cliquez sur **Importer**.</span><span class="sxs-lookup"><span data-stu-id="7be1e-289">To import a key, right-click the node under which to import the key, navigate to the key you want to import, and then click **Import**.</span></span> <span data-ttu-id="7be1e-290">Pour exporter une clé, cliquez avec le bouton droit sur la clé et sélectionnez **Exporter**.</span><span class="sxs-lookup"><span data-stu-id="7be1e-290">To export a key, right-click the key and select **Export**.</span></span>

### <span data-ttu-id="7be1e-291">Importer un annuaire dans le système de fichiers virtuel</span><span class="sxs-lookup"><span data-stu-id="7be1e-291">Import a directory into the virtual file system</span></span>

<span data-ttu-id="7be1e-292">Vous pouvez importer un répertoire dans le VFS.</span><span class="sxs-lookup"><span data-stu-id="7be1e-292">You can import a directory into the VFS.</span></span> <span data-ttu-id="7be1e-293">Pour importer un répertoire, cliquez sur l’onglet **fichiers de package** , puis cliquez sur **Afficher** le &gt; répertoire d’importation du système de **fichiers virtuel** &gt; **Import Directory**.</span><span class="sxs-lookup"><span data-stu-id="7be1e-293">To import a directory, click the **Package Files** tab, and then click **View** &gt; **Virtual File System** &gt; **Import Directory**.</span></span> <span data-ttu-id="7be1e-294">Si vous essayez d’importer un répertoire contenant des fichiers déjà présents sur le VFS, l’importation échoue et un message explicatif s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7be1e-294">If you try to import a directory that contains files that are already in the VFS, the import fails, and an explanatory message is displayed.</span></span> <span data-ttu-id="7be1e-295">Avant l’application-V 5,1, il est impossible d’importer des répertoires.</span><span class="sxs-lookup"><span data-stu-id="7be1e-295">Prior to App-V 5.1, you could not import directories.</span></span>

### <span data-ttu-id="7be1e-296">Importez ou exportez un fichier VFS sans le supprimer, puis rajoutez-le dans le package.</span><span class="sxs-lookup"><span data-stu-id="7be1e-296">Import or export a VFS file without having to delete and then add it back to the package</span></span>

<span data-ttu-id="7be1e-297">Vous pouvez importer ou exporter des fichiers à partir du VFS sans supprimer le fichier, puis l’ajouter de nouveau au package.</span><span class="sxs-lookup"><span data-stu-id="7be1e-297">You can import files to or export files from the VFS without having to delete the file and then add it back to the package.</span></span> <span data-ttu-id="7be1e-298">Par exemple, vous pouvez utiliser cette fonctionnalité pour exporter un journal de modification sur un disque local, modifier le fichier à l’aide d’un éditeur externe, puis importer à nouveau le fichier dans le VFS.</span><span class="sxs-lookup"><span data-stu-id="7be1e-298">For example, you might use this feature to export a change log to a local drive, edit the file using an external editor, and then re-import the file into the VFS.</span></span>

<span data-ttu-id="7be1e-299">Pour exporter un fichier, sélectionnez l’onglet **fichiers du package** , cliquez avec le bouton droit sur le fichier dans le VFS, cliquez sur **Exporter**, puis choisissez un emplacement d’exportation à partir duquel vous pouvez effectuer les modifications.</span><span class="sxs-lookup"><span data-stu-id="7be1e-299">To export a file, select the **Package Files** tab, right-click the file in the VFS, click **Export**, and choose an export location from which you can make your edits.</span></span>

<span data-ttu-id="7be1e-300">Pour importer un fichier, sélectionnez l’onglet **fichiers du package** , puis cliquez avec le bouton droit sur le fichier que vous avez exporté.</span><span class="sxs-lookup"><span data-stu-id="7be1e-300">To import a file, select the **Package Files** tab and right-click the file that you had exported.</span></span> <span data-ttu-id="7be1e-301">Recherchez le fichier que vous avez modifié, puis cliquez sur **Importer**.</span><span class="sxs-lookup"><span data-stu-id="7be1e-301">Browse to the file that you edited, and then click **Import**.</span></span> <span data-ttu-id="7be1e-302">Le fichier importé remplacera le fichier existant.</span><span class="sxs-lookup"><span data-stu-id="7be1e-302">The imported file will overwrite the existing file.</span></span>

<span data-ttu-id="7be1e-303">Lorsque vous importez un fichier, vous devez **l’enregistrer en cliquant sur** &gt; **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7be1e-303">After you import a file, you must save the package by clicking **File** &gt; **Save**.</span></span>

### <span data-ttu-id="7be1e-304">Le menu pour l’ajout d’un fichier de package a été déplacé</span><span class="sxs-lookup"><span data-stu-id="7be1e-304">Menu for adding a package file has moved</span></span>

<span data-ttu-id="7be1e-305">L’option de menu pour l’ajout d’un fichier de package a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="7be1e-305">The menu option for adding a package file has been moved.</span></span> <span data-ttu-id="7be1e-306">Pour accéder à l’option Ajouter, sélectionnez l’onglet **fichiers du package** , puis cliquez sur **Afficher** le &gt; **système de fichiers virtuel** &gt; **Ajouter un fichier**.</span><span class="sxs-lookup"><span data-stu-id="7be1e-306">To find the Add option, select the **Package Files** tab, then click **View** &gt; **Virtual File System** &gt; **Add File**.</span></span> <span data-ttu-id="7be1e-307">Auparavant, cliquez avec le bouton droit sur un dossier sous le nœud VFS et sélectionnez **Ajouter un fichier**.</span><span class="sxs-lookup"><span data-stu-id="7be1e-307">Previously, you right-clicked a folder under the VFS node, and chose **Add File**.</span></span>

### <span data-ttu-id="7be1e-308">Le nœud de Registre virtuel développe les ruches d’ordinateur et d’utilisateur par défaut</span><span class="sxs-lookup"><span data-stu-id="7be1e-308">Virtual registry node expands MACHINE and USER hives by default</span></span>

<span data-ttu-id="7be1e-309">Lorsque vous ouvrez le registre virtuel, les ruches ordinateur et utilisateur sont affichées sous le nœud de registre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="7be1e-309">When you open the virtual registry, the MACHINE and USER hives are shown below the top-level REGISTRY node.</span></span> <span data-ttu-id="7be1e-310">Auparavant, vous deviez développer le nœud REGISTRY pour afficher les ruches au-dessous.</span><span class="sxs-lookup"><span data-stu-id="7be1e-310">Previously, you had to expand the REGISTRY node to show the hives beneath.</span></span>

### <span data-ttu-id="7be1e-311">Activer ou désactiver les objets d’assistance du navigateur</span><span class="sxs-lookup"><span data-stu-id="7be1e-311">Enable or disable Browser Helper Objects</span></span>

<span data-ttu-id="7be1e-312">Vous pouvez activer ou désactiver les objets d’assistance du navigateur en activant une nouvelle case à cocher, activer les objets d’assistance du navigateur, sous l’onglet avancé de l’interface utilisateur de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="7be1e-312">You can enable or disable Browser Helper Objects by selecting a new check box, Enable Browser Helper Objects, on the Advanced tab of the Sequencer user interface.</span></span> <span data-ttu-id="7be1e-313">Si les objets d’assistance du navigateur:</span><span class="sxs-lookup"><span data-stu-id="7be1e-313">If Browser Helper Objects:</span></span>

-   <span data-ttu-id="7be1e-314">Existe dans le package et activés, la case à cocher est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="7be1e-314">Exist in the package and are enabled, the check box is selected by default.</span></span>

-   <span data-ttu-id="7be1e-315">Existe dans le package et sont désactivés, la case à cocher est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="7be1e-315">Exist in the package and are disabled, the check box is clear by default.</span></span>

-   <span data-ttu-id="7be1e-316">Existe dans le package, avec un ou plusieurs activés et un ou plusieurs désactivé, la case à cocher est définie sur indéterminé par défaut.</span><span class="sxs-lookup"><span data-stu-id="7be1e-316">Exist in the package, with one or more enabled and one or more disabled, the check box is set to indeterminate by default.</span></span>

-   <span data-ttu-id="7be1e-317">Qui n’existent pas dans le package, la case à cocher est désactivée.</span><span class="sxs-lookup"><span data-stu-id="7be1e-317">Do not exist in the package, the check box is disabled.</span></span>

### <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="7be1e-318">Améliorations apportées au convertisseur de package</span><span class="sxs-lookup"><span data-stu-id="7be1e-318">Improvements to Package Converter</span></span>

<span data-ttu-id="7be1e-319">Vous pouvez désormais utiliser le convertisseur de package pour convertir les packages App-V 4,6 qui contiennent des scripts, et les informations de Registre et les scripts des fichiers source. OSD sont désormais inclus dans la sortie du convertisseur de package.</span><span class="sxs-lookup"><span data-stu-id="7be1e-319">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="7be1e-320">Pour plus d’informations, y compris des exemples, voir [migration vers App-V 5,1 à partir d’une version précédente](migrating-to-app-v-51-from-a-previous-version.md).</span><span class="sxs-lookup"><span data-stu-id="7be1e-320">For more information including examples, see [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md).</span></span>

### <a href="" id="bkmk-supmultscripts"></a><span data-ttu-id="7be1e-321">Prise en charge de plusieurs scripts sur un seul déclencheur d’événements</span><span class="sxs-lookup"><span data-stu-id="7be1e-321">Support for multiple scripts on a single event trigger</span></span>

<span data-ttu-id="7be1e-322">App-V 5,1 prend en charge l’utilisation de plusieurs scripts sur un seul déclencheur d’événements pour les packages App-V, notamment les packages que vous convertissez de App-V 4,6 à l’application-V 5,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7be1e-322">App-V 5.1 supports the use of multiple scripts on a single event trigger for App-V packages, including packages that you are converting from App-V 4.6 to App-V 5.0 or later.</span></span> <span data-ttu-id="7be1e-323">Pour activer l’utilisation de plusieurs scripts, App-V 5,1 utilise une application de lancement de script, nommée ScriptRunner.exe, installée dans le cadre de l’installation du client App-V.</span><span class="sxs-lookup"><span data-stu-id="7be1e-323">To enable the use of multiple scripts, App-V 5.1 uses a script launcher application, named ScriptRunner.exe, which is installed as part of the App-V client installation.</span></span>

<span data-ttu-id="7be1e-324">Pour plus d’informations, y compris une liste de déclencheurs d’événements et le contexte dans lequel les scripts peuvent être exécutés, voir la section scripts dans [à propos de la configuration dynamique App-V 5,1](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="7be1e-324">For more information, including a list of event triggers and the context under which scripts can be run, see the Scripts section in [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

### <a href="" id="bkmk-hardcodepath"></a><span data-ttu-id="7be1e-325">Le chemin d’accès codé au dossier d’installation est redirigé vers la racine du système de fichiers virtuel</span><span class="sxs-lookup"><span data-stu-id="7be1e-325">Hardcoded path to installation folder is redirected to virtual file system root</span></span>

<span data-ttu-id="7be1e-326">Lorsque vous convertissez des packages de App-V 4,6 en 5,1, le package App-V 5,1 peut accéder au lecteur codé en dur que vous avez besoin d’utiliser lors de la création de packages 4,6.</span><span class="sxs-lookup"><span data-stu-id="7be1e-326">When you convert packages from App-V 4.6 to 5.1, the App-V 5.1 package can access the hardcoded drive that you were required to use when you created 4.6 packages.</span></span> <span data-ttu-id="7be1e-327">La lettre de lecteur sera le lecteur que vous avez sélectionné comme lecteur d’installation sur le système de séquençage 4,6.</span><span class="sxs-lookup"><span data-stu-id="7be1e-327">The drive letter will be the drive you selected as the installation drive on the 4.6 sequencing machine.</span></span> <span data-ttu-id="7be1e-328">(La lettre du lecteur par défaut est Q:\\.)</span><span class="sxs-lookup"><span data-stu-id="7be1e-328">(The default drive letter is Q:\\.)</span></span>

<span data-ttu-id="7be1e-329">Auparavant, le dossier racine 4,6 n’était pas reconnu et n’était pas accessible par les packages App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7be1e-329">Previously, the 4.6 root folder was not recognized and could not be accessed by App-V 5.0 packages.</span></span> <span data-ttu-id="7be1e-330">Les packages App-V 5,1 peuvent accéder aux fichiers en dur par le chemin d’accès complet ou peuvent énumérer par programme les fichiers sous la racine d’installation App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="7be1e-330">App-V 5.1 packages can access hardcoded files by their full path or can programmatically enumerate files under the App-V 4.6 installation root.</span></span>

<span data-ttu-id="7be1e-331">**Détails techniques:** Le convertisseur d’application de package App-V 5,1 enregistre le dossier racine d’installation App-V 4,6 et les noms de dossiers courts dans le fichier FilesystemMetadata.xml de l’élément FileSystem.</span><span class="sxs-lookup"><span data-stu-id="7be1e-331">**Technical Details:** The App-V 5.1 package converter will save the App-V 4.6 installation root folder and short folder names in the FilesystemMetadata.xml file in the Filesystem element.</span></span> <span data-ttu-id="7be1e-332">Lorsque le client App-V 5,1 crée le processus virtuel, il mappera les demandes de la racine d’installation de l’application-V 4,6 à la racine du système de fichiers virtuel.</span><span class="sxs-lookup"><span data-stu-id="7be1e-332">When the App-V 5.1 client creates the virtual process, it will map requests from the App-V 4.6 installation root to the virtual file system root.</span></span>

## <span data-ttu-id="7be1e-333">Obtention de technologies MDOP</span><span class="sxs-lookup"><span data-stu-id="7be1e-333">How to Get MDOP Technologies</span></span>


<span data-ttu-id="7be1e-334">App-V est un composant du pack d’optimisation du bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="7be1e-334">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="7be1e-335">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="7be1e-335">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="7be1e-336">Pour plus d’informations sur l’utilisation de Microsoft Software Assurance et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="7be1e-336">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="7be1e-337">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7be1e-337">Related topics</span></span>


[<span data-ttu-id="7be1e-338">Notes de publication pour App-V5.1</span><span class="sxs-lookup"><span data-stu-id="7be1e-338">Release Notes for App-V 5.1</span></span>](release-notes-for-app-v-51.md)










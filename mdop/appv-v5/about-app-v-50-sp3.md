---
title: À propos d'App-V5.0 SP3
description: À propos d'App-V5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806121"
---
# <span data-ttu-id="908c5-103">À propos d'App-V5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-103">About App-V 5.0 SP3</span></span>


<span data-ttu-id="908c5-104">Les sections suivantes permettent de consulter des informations sur les modifications importantes qui s’appliquent à la virtualisation des applications Microsoft (App-V) 5,0 SP3:</span><span class="sxs-lookup"><span data-stu-id="908c5-104">Use the following sections to review information about significant changes that apply to Microsoft Application Virtualization (App-V) 5.0 SP3:</span></span>

-   [<span data-ttu-id="908c5-105">Configuration logicielle requise pour App-V 5,0 SP3 et configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="908c5-105">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>](#bkmk-sp3-prereq-configs)

-   [<span data-ttu-id="908c5-106">Migration vers App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-106">Migrating to App-V 5.0 SP3</span></span>](#bkmk-migrate-to-50sp3)

-   [<span data-ttu-id="908c5-107">Le fichier XML de groupe de connexion créé manuellement nécessite une mise à jour du schéma</span><span class="sxs-lookup"><span data-stu-id="908c5-107">Manually created connection group xml file requires update to schema</span></span>](#bkmk-update-schema-cg)

-   [<span data-ttu-id="908c5-108">Améliorations apportées aux groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="908c5-108">Improvements to connection groups</span></span>](#bkmk-cg-improvements)

-   [<span data-ttu-id="908c5-109">Les administrateurs peuvent publier et annuler la publication de packages pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="908c5-109">Administrators can publish and unpublish packages for a specific user</span></span>](#bkmk-usersid-pub-pkgs-specf-user)

-   [<span data-ttu-id="908c5-110">Autoriser uniquement les administrateurs à publier et à retirer des packages</span><span class="sxs-lookup"><span data-stu-id="908c5-110">Enable only administrators to publish and unpublish packages</span></span>](#bkmk-admins-only-pub-unpub-pkgs)

-   [<span data-ttu-id="908c5-111">La clé de Registre RunVirtual prend en charge les packages publiés pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="908c5-111">RunVirtual registry key supports packages that are published to the user</span></span>](#bkmk-runvirtual-reg-key)

-   [<span data-ttu-id="908c5-112">Nouvelles cmdlets PowerShell et aide sur les cmdlets</span><span class="sxs-lookup"><span data-stu-id="908c5-112">New PowerShell cmdlets and updateable cmdlet help</span></span>](#bkmk-posh-cmdlets-help)

-   [<span data-ttu-id="908c5-113">Le répertoire principal de l’application virtuelle (PVAD) est masqué, mais peut être activé.</span><span class="sxs-lookup"><span data-stu-id="908c5-113">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>](#bkmk-pvad-hidden)

-   [<span data-ttu-id="908c5-114">ClientVersion est requis pour afficher les métadonnées de publication d’application-V</span><span class="sxs-lookup"><span data-stu-id="908c5-114">ClientVersion is required to view App-V publishing metadata</span></span>](#bkmk-pub-metadata-clientversion)

-   [<span data-ttu-id="908c5-115">Les journaux des événements App-V ont été consolidés</span><span class="sxs-lookup"><span data-stu-id="908c5-115">App-V event logs have been consolidated</span></span>](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a><span data-ttu-id="908c5-116">Configuration logicielle requise pour App-V 5,0 SP3 et configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="908c5-116">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>


<span data-ttu-id="908c5-117">Pour plus d’informations 5,0 sur les configurations logicielles prises en charge, voir les liens suivants:</span><span class="sxs-lookup"><span data-stu-id="908c5-117">See the following links for the App-V 5.0 SP3 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-118">Liens vers les composants requis et les configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="908c5-118">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="908c5-119">Description</span><span class="sxs-lookup"><span data-stu-id="908c5-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)"><span data-ttu-id="908c5-120">Composants requis d'App-V5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-120">App-V 5.0 SP3 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="908c5-121">Logiciels requis que vous devez installer avant de démarrer l’installation App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-121">Prerequisite software that you must install before starting the App-V 5.0 SP3 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"><span data-ttu-id="908c5-122">Configurations prises en charge d'App-V5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-122">App-V 5.0 SP3 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="908c5-123">Systèmes d’exploitation pris en charge et configuration matérielle requise pour le serveur App-V, le Sequencer et les composants clients</span><span class="sxs-lookup"><span data-stu-id="908c5-123">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a><span data-ttu-id="908c5-124">Migration vers App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-124">Migrating to App-V 5.0 SP3</span></span>


<span data-ttu-id="908c5-125">Utilisez les informations ci-dessous pour effectuer une mise à niveau vers App-V 5,0 SP3 à partir d’une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="908c5-125">Use the following information to upgrade to App-V 5.0 SP3 from earlier versions.</span></span>

### <span data-ttu-id="908c5-126">Avant de commencer la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="908c5-126">Before you start the upgrade</span></span>

<span data-ttu-id="908c5-127">Passez en revue les informations suivantes avant de commencer la mise à niveau:</span><span class="sxs-lookup"><span data-stu-id="908c5-127">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-128">Éléments à réviser avant la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="908c5-128">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="908c5-129">Description</span><span class="sxs-lookup"><span data-stu-id="908c5-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-130">Composants à mettre à niveau</span><span class="sxs-lookup"><span data-stu-id="908c5-130">Components to upgrade</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="908c5-131">App-V Server</span><span class="sxs-lookup"><span data-stu-id="908c5-131">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="908c5-132">Sequencer</span><span class="sxs-lookup"><span data-stu-id="908c5-132">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="908c5-133">Client App-V ou App-V (service bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="908c5-133">App-V client or App-V Remote Desktop Services (RDS) client</span></span></p></li>
<li><p><span data-ttu-id="908c5-134">Groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="908c5-134">Connection groups</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="908c5-135">Remarque</span><span class="sxs-lookup"><span data-stu-id="908c5-135">Note</span></span></strong><br/><p><span data-ttu-id="908c5-136">Pour utiliser l’interface utilisateur du client App-V, téléchargez la version existante à partir de l’application de l’interface utilisateur du <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> client Microsoft application virtualization 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="908c5-136">To use the App-V client user interface, download the existing version from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Microsoft Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-137">Mise à niveau à partir de App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="908c5-137">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-138">Vous devez d’abord effectuer une mise à niveau vers App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="908c5-138">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="908c5-139">Vous ne pouvez pas effectuer la mise à niveau directement de App-V 4. x vers App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="908c5-139">You cannot upgrade directly from App-V 4.x to App-V 5.0 SP3.</span></span></p>
<p><span data-ttu-id="908c5-140">Pour plus d’informations, voir:</span><span class="sxs-lookup"><span data-stu-id="908c5-140">For more information, see:</span></span></p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"><span data-ttu-id="908c5-141">À propos d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="908c5-141">About App-V 5.0</span></span></a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="908c5-142">Planification d'une migration à partir d'une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="908c5-142">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-143">Mise à niveau à partir de App-V 5,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="908c5-143">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-144">Vous pouvez effectuer une mise à niveau vers App-V 5,0 SP3 directement à partir des versions suivantes:</span><span class="sxs-lookup"><span data-stu-id="908c5-144">You can upgrade to App-V 5.0 SP3 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="908c5-145">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="908c5-145">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="908c5-146">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="908c5-146">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="908c5-147">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="908c5-147">App-V 5.0 SP2</span></span></p></li>
</ul>
<p><span data-ttu-id="908c5-148">Pour effectuer une mise à niveau vers App-V 5,0 SP3, suivez les étapes décrites dans les sections restantes de cet article.</span><span class="sxs-lookup"><span data-stu-id="908c5-148">To upgrade to App-V 5.0 SP3, follow the steps in the remaining sections of this article.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-149">Modifications requises apportées aux packages et aux groupes de connexion après la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="908c5-149">Required changes to packages and connection groups after upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-150">Aucune.</span><span class="sxs-lookup"><span data-stu-id="908c5-150">None.</span></span> <span data-ttu-id="908c5-151">Les packages et les groupes de connexion continuent de fonctionner comme il le fera actuellement.</span><span class="sxs-lookup"><span data-stu-id="908c5-151">Packages and connection groups will continue to work as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="908c5-152">Procédure de mise à niveau de l’infrastructure App-V</span><span class="sxs-lookup"><span data-stu-id="908c5-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="908c5-153">Suivez les étapes ci-dessous pour mettre à niveau chaque composant de l’infrastructure App-V vers App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="908c5-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.0 SP3.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-154">Étape</span><span class="sxs-lookup"><span data-stu-id="908c5-154">Step</span></span></th>
<th align="left"><span data-ttu-id="908c5-155">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="908c5-155">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-156">Étape 1: mettez à niveau le serveur App-V.</span><span class="sxs-lookup"><span data-stu-id="908c5-156">Step 1: Upgrade the App-V Server.</span></span></p>
<p><span data-ttu-id="908c5-157">Si vous n’utilisez pas le serveur App-V, ignorez cette étape et passez à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="908c5-157">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="908c5-158">Remarque</span><span class="sxs-lookup"><span data-stu-id="908c5-158">Note</span></span></strong><br/><p><span data-ttu-id="908c5-159">Le client App-V 5,0 SP3 est compatible avec le serveur App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="908c5-159">The App-V 5.0 SP3 client is compatible with the App-V 5.0 SP1 Server.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="908c5-160">Procédez comme suit: </span><span class="sxs-lookup"><span data-stu-id="908c5-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="908c5-161">Consultez les <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> notes de publication pour App-V 5,0 SP3 </a> pour les problèmes qui peuvent affecter l’installation de l’application-v Server.</span><span class="sxs-lookup"><span data-stu-id="908c5-161">Review the <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)">Release Notes for App-V 5.0 SP3</a> for issues that may affect the App-V Server installation.</span></span></p></li>
<li><p><span data-ttu-id="908c5-162">Effectuez l’une des opérations suivantes, selon la méthode que vous utilisez pour mettre à niveau la base de données de gestion et/ou la base de données de création de rapports, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="908c5-162">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-163">Méthode de mise à niveau de base de données</span><span class="sxs-lookup"><span data-stu-id="908c5-163">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="908c5-164">Étape</span><span class="sxs-lookup"><span data-stu-id="908c5-164">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-165">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="908c5-165">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-166">Ignorez cette étape et passez à l’étape 3, «si vous effectuez la mise à niveau de l’application-V Server».</span><span class="sxs-lookup"><span data-stu-id="908c5-166">Skip this step and go to step 3, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-167">Scripts SQL</span><span class="sxs-lookup"><span data-stu-id="908c5-167">SQL scripts</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="908c5-168">Base de données de gestion</span><span class="sxs-lookup"><span data-stu-id="908c5-168">Management database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="908c5-169">Pour procéder à l’installation ou à la mise à niveau, voir <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts SQL pour installer ou mettre à niveau la base de données du serveur de gestion de l’application-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="908c5-169">To install or upgrade, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="908c5-170">Base de données de création de rapports</span><span class="sxs-lookup"><span data-stu-id="908c5-170">Reporting database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="908c5-171">Suivez les étapes décrites dans la <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> procédure de déploiement des bases de données App-V à l’aide de scripts SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="908c5-171">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p><span data-ttu-id="908c5-172">Si vous effectuez une mise à niveau de l’application-V Server à partir du correctif logiciel App-V 5,0 SP1 ou version ultérieure, suivez les étapes de la section <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> vérifier les clés de registre après l’installation de l’app-v 5,0 SP3 Server </a> .</span><span class="sxs-lookup"><span data-stu-id="908c5-172">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="908c5-173">Suivez les étapes décrites dans la <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> procédure de déploiement du serveur App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="908c5-173">Follow the steps in <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-174">Étape 2: mettre à niveau le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="908c5-174">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-175">Découvrez <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Comment installer le Sequencer </a> .</span><span class="sxs-lookup"><span data-stu-id="908c5-175">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-176">Étape 3: mettez à niveau le client App-V ou le client RDS (App-V).</span><span class="sxs-lookup"><span data-stu-id="908c5-176">Step 3: Upgrade the App-V client or App-V RDS client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-177">Découvrez <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> comment déployer le client App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="908c5-177">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a><span data-ttu-id="908c5-178">Vérifier les clés de Registre avant d’installer le serveur App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-178">Check registry keys before installing the App-V 5.0 SP3 Server</span></span>

<span data-ttu-id="908c5-179">Étape 3 du tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="908c5-179">This is step 3 from the previous table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="908c5-180">Lorsque cette étape est nécessaire</span><span class="sxs-lookup"><span data-stu-id="908c5-180">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="908c5-181">Vous effectuez une mise à niveau à partir de App-V SP1 avec les packages de correctifs suivants que vous avez installés à l’aide d’un fichier. msp.</span><span class="sxs-lookup"><span data-stu-id="908c5-181">You are upgrading from App-V SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="908c5-182">Quels composants nécessitent cette étape</span><span class="sxs-lookup"><span data-stu-id="908c5-182">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="908c5-183">Uniquement les composants serveur App-V que vous effectuez une mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="908c5-183">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="908c5-184">Lorsque vous devez effectuer cette étape</span><span class="sxs-lookup"><span data-stu-id="908c5-184">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="908c5-185">Avant de mettre à niveau l’application-V Server vers App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-185">Before you upgrade the App-V Server to App-V 5.0 SP3</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="908c5-186">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="908c5-186">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="908c5-187">À l’aide des informations contenues dans les tableaux ci-dessous, vous devez mettre à jour chaque valeur de clé de registre en <code>HKLM\Software\Microsoft\AppV\Server</code> fonction de la valeur que vous avez fournie lors de votre installation de serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="908c5-187">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="908c5-188">Cette étape restaure les valeurs de Registre susceptibles d’avoir été supprimées lors de l’installation des packages de correctifs App-V SP1.</span><span class="sxs-lookup"><span data-stu-id="908c5-188">Completing this step restores registry values that may have been removed when App-V SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="908c5-189">Clé ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="908c5-189">ManagementDatabase key</span></span>**

<span data-ttu-id="908c5-190">Si vous installez la base de données de gestion, définissez les clés de Registre suivantes `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="908c5-190">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-191">Nom de la clé</span><span class="sxs-lookup"><span data-stu-id="908c5-191">Key name</span></span></th>
<th align="left"><span data-ttu-id="908c5-192">Description</span><span class="sxs-lookup"><span data-stu-id="908c5-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="908c5-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-194">Indique si un compte d’accès public est requis pour accéder aux bases de données de gestion non locales.</span><span class="sxs-lookup"><span data-stu-id="908c5-194">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="908c5-195">La valeur est définie sur «1» s’il est requis.</span><span class="sxs-lookup"><span data-stu-id="908c5-195">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-196">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="908c5-196">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-197">Nom de la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="908c5-197">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="908c5-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-199">Compte utilisé pour l’accès en lecture (public) à la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="908c5-199">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="908c5-200">Utilisé lorsque <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="908c5-200">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="908c5-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-202">ID de sécurité (SID) du compte utilisé pour l’accès en lecture (public) à la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="908c5-202">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="908c5-203">Utilisé lorsque <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="908c5-203">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-204">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="908c5-204">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-205">Instance SQL Server de la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="908c5-205">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="908c5-206">Si la valeur est vide, l’instance de base de données par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="908c5-206">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="908c5-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-208">Compte utilisé pour l’accès en écriture (administrateur) à la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="908c5-208">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="908c5-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-210">ID de sécurité (SID) du compte utilisé pour l’accès en écriture (administrateur) à la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="908c5-210">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="908c5-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-212">Compte d’ordinateur distant du serveur de gestion (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="908c5-212">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="908c5-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-214">Connexion administrateur d’installation pour le serveur de gestion (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="908c5-214">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="908c5-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-216">Valeurs valides:</span><span class="sxs-lookup"><span data-stu-id="908c5-216">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="908c5-217">1 </strong> – le service de gestion est sur l’ordinateur local, c’est-à-dire MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT est vide.</span><span class="sxs-lookup"><span data-stu-id="908c5-217">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="908c5-218">0 </strong> - le service de gestion est sur un ordinateur différent de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="908c5-218">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="908c5-219">Clé ManagementService</span><span class="sxs-lookup"><span data-stu-id="908c5-219">ManagementService key</span></span>**

<span data-ttu-id="908c5-220">Si vous installez le serveur de gestion, définissez les clés de Registre suivantes `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="908c5-220">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-221">Nom de la clé</span><span class="sxs-lookup"><span data-stu-id="908c5-221">Key name</span></span></th>
<th align="left"><span data-ttu-id="908c5-222">Description</span><span class="sxs-lookup"><span data-stu-id="908c5-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-223">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="908c5-223">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-224">Le compte ou le groupe AD DS (Active Directory Domain Services) qui est autorisé à gérer App-V (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="908c5-224">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-225">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="908c5-225">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-226">Instance SQL Server qui contient la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="908c5-226">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="908c5-227">Si la valeur est vide, l’instance de base de données par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="908c5-227">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-228">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="908c5-228">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-229">Nom du serveur SQL distant doté de la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="908c5-229">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="908c5-230">Si la valeur est vide, l’ordinateur local est utilisé.</span><span class="sxs-lookup"><span data-stu-id="908c5-230">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="908c5-231">Clé ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="908c5-231">ReportingDatabase key</span></span>**

<span data-ttu-id="908c5-232">Si vous installez la base de données de création de rapports, définissez ces clés de Registre sous `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="908c5-232">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-233">Nom de la clé</span><span class="sxs-lookup"><span data-stu-id="908c5-233">Key name</span></span></th>
<th align="left"><span data-ttu-id="908c5-234">Description</span><span class="sxs-lookup"><span data-stu-id="908c5-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="908c5-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-236">Indique si un compte d’accès public est requis pour accéder aux bases de données de création de rapports non locales.</span><span class="sxs-lookup"><span data-stu-id="908c5-236">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="908c5-237">La valeur est définie sur «1» s’il est requis.</span><span class="sxs-lookup"><span data-stu-id="908c5-237">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-238">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="908c5-238">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-239">Nom de la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="908c5-239">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="908c5-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-241">Compte utilisé pour l’accès en lecture (public) à la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="908c5-241">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="908c5-242">Utilisé lorsque <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="908c5-242">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="908c5-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-244">ID de sécurité (SID) du compte utilisé pour l’accès en lecture (public) à la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="908c5-244">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="908c5-245">Utilisé lorsque <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="908c5-245">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-246">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="908c5-246">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-247">Instance SQL Server de la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="908c5-247">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="908c5-248">Si la valeur est vide, l’instance de base de données par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="908c5-248">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="908c5-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="908c5-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="908c5-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-252">Compte d’ordinateur distant du serveur de rapports (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="908c5-252">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="908c5-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-254">Connexion administrateur d’installation pour le serveur de rapports (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="908c5-254">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="908c5-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-256">Valeurs valides:</span><span class="sxs-lookup"><span data-stu-id="908c5-256">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="908c5-257">1 </strong> – le service de création de rapports est sur l’ordinateur local, c’est-à-dire REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT est vide.</span><span class="sxs-lookup"><span data-stu-id="908c5-257">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="908c5-258">0 </strong> - le service de création de rapports est sur un ordinateur différent de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="908c5-258">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="908c5-259">Clé ReportingService</span><span class="sxs-lookup"><span data-stu-id="908c5-259">ReportingService key</span></span>**

<span data-ttu-id="908c5-260">Si vous installez le serveur de création de rapports, définissez ces clés de Registre sous `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="908c5-260">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-261">Nom de la clé</span><span class="sxs-lookup"><span data-stu-id="908c5-261">Key name</span></span></th>
<th align="left"><span data-ttu-id="908c5-262">Description</span><span class="sxs-lookup"><span data-stu-id="908c5-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-263">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="908c5-263">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-264">Instance SQL Server de la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="908c5-264">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="908c5-265">Si la valeur est vide, l’instance de base de données par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="908c5-265">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-266">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="908c5-266">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-267">Nom du serveur SQL distant avec la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="908c5-267">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="908c5-268">Si la valeur est vide, l’ordinateur local est utilisé.</span><span class="sxs-lookup"><span data-stu-id="908c5-268">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a><span data-ttu-id="908c5-269">Le fichier XML de groupe de connexion créé manuellement nécessite une mise à jour du schéma</span><span class="sxs-lookup"><span data-stu-id="908c5-269">Manually created connection group xml file requires update to schema</span></span>


<span data-ttu-id="908c5-270">Si vous créez manuellement le fichier XML de groupe de connexion et souhaitez utiliser les nouvelles fonctionnalités «packages facultatifs» et «utiliser les versions» décrites dans [améliorations apportées aux groupes de connexion](#bkmk-cg-improvements), vous devez spécifier le schéma suivant dans le fichier XML:</span><span class="sxs-lookup"><span data-stu-id="908c5-270">If you are manually creating the connection group XML file, and want to use the new “optional packages” and “use any version” features that are described in [Improvements to connection groups](#bkmk-cg-improvements), you must specify the following schema in the XML file:</span></span>

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

<span data-ttu-id="908c5-271">Pour des exemples et des informations supplémentaires, voir [à propos du fichier de groupe de connexion](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="908c5-271">For examples and more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

## <a href="" id="bkmk-cg-improvements"></a><span data-ttu-id="908c5-272">Améliorations apportées aux groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="908c5-272">Improvements to connection groups</span></span>


<span data-ttu-id="908c5-273">Vous pouvez gérer les groupes de connexion plus facilement en utilisant des packages facultatifs et d’autres améliorations qui ont été ajoutées dans App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="908c5-273">You can manage connection groups more easily by using optional packages and other improvements that have been added in App-V 5.0 SP3.</span></span> <span data-ttu-id="908c5-274">Le tableau suivant récapitule les tâches que vous pouvez effectuer à l’aide des nouvelles fonctionnalités de groupe de connexion, ainsi que des liens vers des informations plus détaillées sur chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="908c5-274">The following table summarizes the tasks that you can perform by using the new connection group features, and links to more detailed information about each task.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-275">Tâche/fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="908c5-275">Task/feature</span></span></th>
<th align="left"><span data-ttu-id="908c5-276">Description</span><span class="sxs-lookup"><span data-stu-id="908c5-276">Description</span></span></th>
<th align="left"><span data-ttu-id="908c5-277">Liens vers des informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="908c5-277">Links to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-278">Permettre à un groupe de connexions d’inclure des packages facultatifs</span><span class="sxs-lookup"><span data-stu-id="908c5-278">Enable a connection group to include optional packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-279">L’inclusion de packages facultatifs dans un groupe de connexions vous permet de déterminer dynamiquement les applications qui seront incluses dans l’environnement virtuel du groupe de connexions, en fonction des applications auxquelles les utilisateurs sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="908c5-279">Including optional packages in a connection group enables you to dynamically determine which applications will be included in the connection group’s virtual environment, based on the applications that users are entitled to.</span></span></p>
<p><span data-ttu-id="908c5-280">Vous n’avez pas besoin de gérer autant de groupes de connexions, car vous pouvez mélanger des packages facultatifs et non facultatifs dans le même groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="908c5-280">You don’t need to manage as many connection groups because you can mix optional and non-optional packages in the same connection group.</span></span> <span data-ttu-id="908c5-281">Le mélange de packages permet à différents groupes d’utilisateurs d’utiliser le même groupe de connexion, même si les utilisateurs ne peuvent avoir qu’un seul package en commun.</span><span class="sxs-lookup"><span data-stu-id="908c5-281">Mixing packages allows different groups of users to use the same connection group, even though users might have only one package in common.</span></span></p>
<p><strong><span data-ttu-id="908c5-282">Par exemple </strong> : vous pouvez activer un package avec Microsoft Office pour tous les utilisateurs, mais activer différents packages facultatifs, qui contiennent différents composants Office, à différents sous-ensembles d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="908c5-282">Example</strong>: You can enable a package with Microsoft Office for all users, but enable different optional packages, which contain different Office plug-ins, to different subsets of users.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="908c5-283">Comment utiliser des packages facultatifs dans les groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="908c5-283">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-284">Annuler la publication ou la suppression d’un package facultatif sans changer le groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="908c5-284">Unpublish or delete an optional package without changing the connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-285">Annulez ou supprimez, ou annulez ou republiez un package facultatif, qui se trouve dans un groupe de connexion, sans avoir besoin de désactiver ou réactiver le groupe de connexion sur le client App-V.</span><span class="sxs-lookup"><span data-stu-id="908c5-285">Unpublish or delete, or unpublish and republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V client.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="908c5-286">Comment utiliser des packages facultatifs dans les groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="908c5-286">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-287">Publier des groupes de connexion contenant des packages publiés par l’utilisateur et globalement publiés</span><span class="sxs-lookup"><span data-stu-id="908c5-287">Publish connection groups that contain user-published and globally published packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-288">Créer un groupe de connexion publié par l’utilisateur contenant des packages publiés par l’utilisateur et globalement publiés.</span><span class="sxs-lookup"><span data-stu-id="908c5-288">Create a user-published connection group that contains user-published and globally published packages.</span></span></p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="908c5-289">Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement</span><span class="sxs-lookup"><span data-stu-id="908c5-289">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-290">Créer un groupe de connexions ignorer la version du package</span><span class="sxs-lookup"><span data-stu-id="908c5-290">Make a connection group ignore the package version</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-291">Configurez un groupe de connexion pour accepter n’importe quelle version d’un package, qui vous permet de mettre à niveau un package sans avoir à désactiver le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="908c5-291">Configure a connection group to accept any version of a package, which enables you to upgrade a package without having to disable the connection group.</span></span> <span data-ttu-id="908c5-292">Par ailleurs, s’il existe un package facultatif dont la version n’est pas correcte dans le groupe de connexion, le package est ignoré et ne bloque pas la création de l’environnement virtuel du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="908c5-292">In addition, if there is an optional package with an incorrect version in the connection group, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)"><span data-ttu-id="908c5-293">Comment faire en sorte qu'un groupe de connexion ignore la version du package</span><span class="sxs-lookup"><span data-stu-id="908c5-293">How to Make a Connection Group Ignore the Package Version</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-294">Limiter les capacités de publication des utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="908c5-294">Limit end users’ publishing capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-295">Activez uniquement les administrateurs (pas les utilisateurs finaux) pour publier des packages et activer les groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="908c5-295">Enable only administrators (not end users) to publish packages and to enable connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-296">Pour plus d’informations sur les groupes de connexion, voir <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> interdire uniquement aux administrateurs d’activer les groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="908c5-296">For information about connection groups, see <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)">How to Allow Only Administrators to Enable Connection Groups</span></span></a></p>
<p><span data-ttu-id="908c5-297">Pour plus d’informations sur les packages, voir les articles suivants:</span><span class="sxs-lookup"><span data-stu-id="908c5-297">For information about packages, see the following articles:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-298">Méthode</span><span class="sxs-lookup"><span data-stu-id="908c5-298">Method</span></span></th>
<th align="left"><span data-ttu-id="908c5-299">Lien vers plus d’informations</span><span class="sxs-lookup"><span data-stu-id="908c5-299">Link to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-300">Console de gestion</span><span class="sxs-lookup"><span data-stu-id="908c5-300">Management console</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="908c5-301">Comment publier un package à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="908c5-301">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-302">PowerShell</span><span class="sxs-lookup"><span data-stu-id="908c5-302">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="908c5-303">Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="908c5-303">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-304">Système de remise de logiciels électroniques tiers</span><span class="sxs-lookup"><span data-stu-id="908c5-304">Third-party electronic software delivery system</span></span></p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)"><span data-ttu-id="908c5-305">Comment autoriser uniquement les administrateurs à publier des packages à l'aide d'un système ESD</span><span class="sxs-lookup"><span data-stu-id="908c5-305">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-306">Activer ou désactiver un groupe de connexions pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="908c5-306">Enable or disable a connection group for a specific user</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-307">Les administrateurs peuvent activer ou désactiver un groupe de connexions pour un utilisateur spécifique à l’aide du <strong> paramètre facultatif-UserSid </strong> avec les applets de commande suivantes:</span><span class="sxs-lookup"><span data-stu-id="908c5-307">Administrators can enable or disable a connection group for a specific user by using the optional <strong>–UserSID</strong> parameter with the following cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="908c5-308">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="908c5-308">Enable-AppVClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="908c5-309">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="908c5-309">Disable-AppVClientConnectionGroup</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)"><span data-ttu-id="908c5-310">Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="908c5-310">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-311">Fusion de chemins de package identiques dans un répertoire virtuel dans les groupes de connexions</span><span class="sxs-lookup"><span data-stu-id="908c5-311">Merging identical package paths into one virtual directory in connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-312">Si au moins deux packages d’un groupe de connexion contiennent des chemins d’accès identiques, les chemins d’accès sont fusionnés dans un répertoire virtuel unique à l’intérieur de l’environnement virtuel du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="908c5-312">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span></p>
<p><span data-ttu-id="908c5-313">Cette fusion des chemins d’accès permet à une application dans un même package d’accéder aux fichiers d’un autre package.</span><span class="sxs-lookup"><span data-stu-id="908c5-313">This merging of paths allows an application in one package to access files that are in a different package.</span></span></p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)"><span data-ttu-id="908c5-314">À propos de l’environnement virtuel du groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="908c5-314">About the Connection Group Virtual Environment</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a><span data-ttu-id="908c5-315">Les administrateurs peuvent publier et annuler la publication de packages pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="908c5-315">Administrators can publish and unpublish packages for a specific user</span></span>


<span data-ttu-id="908c5-316">Les administrateurs peuvent utiliser les applets de commande suivantes pour publier ou annuler la publication de packages pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="908c5-316">Administrators can use the following cmdlets to publish or unpublish packages for a specific user.</span></span> <span data-ttu-id="908c5-317">Pour utiliser les applets de applet, entrez le paramètre **– UserSid** , suivi de l’identificateur de sécurité (SID) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="908c5-317">To use the cmdlets, enter the **–UserSID** parameter, followed by the user’s security identifier (SID).</span></span> <span data-ttu-id="908c5-318">Pour plus d’informations, voir:</span><span class="sxs-lookup"><span data-stu-id="908c5-318">For more information, see:</span></span>

-   [<span data-ttu-id="908c5-319">Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="908c5-319">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="908c5-320">Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="908c5-320">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-321">Applet de commande</span><span class="sxs-lookup"><span data-stu-id="908c5-321">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="908c5-322">Exemples</span><span class="sxs-lookup"><span data-stu-id="908c5-322">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-323">Publisher-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="908c5-323">Publish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-324">Publisher-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="908c5-324">Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-325">Annuler la publication-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="908c5-325">Unpublish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-326">Unpublish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="908c5-326">Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a><span data-ttu-id="908c5-327">Autoriser uniquement les administrateurs à publier et à retirer des packages</span><span class="sxs-lookup"><span data-stu-id="908c5-327">Enable only administrators to publish and unpublish packages</span></span>


<span data-ttu-id="908c5-328">Vous pouvez activer uniquement les administrateurs (pas les utilisateurs finaux) pour publier et annuler la publication des packages à l’aide de l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="908c5-328">You can enable only administrators (not end users) to publish and unpublish packages by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-329">Méthode</span><span class="sxs-lookup"><span data-stu-id="908c5-329">Method</span></span></th>
<th align="left"><span data-ttu-id="908c5-330">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="908c5-330">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-331">Paramètre de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="908c5-331">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-332">Accédez au nœud d’objet de stratégie de groupe suivant:</span><span class="sxs-lookup"><span data-stu-id="908c5-332">Navigate to the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="908c5-333">&gt;Stratégies de Configuration ordinateur &gt; modèles d’administration &gt; &gt; application de la publication de l’application-V &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="908c5-333">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</strong>.</span></span></p>
<p><span data-ttu-id="908c5-334">Activez le <strong> paramètre exiger une stratégie de groupe publier en tant qu’administrateur </strong> .</span><span class="sxs-lookup"><span data-stu-id="908c5-334">Enable the <strong>Require publish as administrator</strong> Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-335">PowerShell</span><span class="sxs-lookup"><span data-stu-id="908c5-335">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)"><span data-ttu-id="908c5-336">Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="908c5-336">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a><span data-ttu-id="908c5-337">La clé de Registre RunVirtual prend en charge les packages publiés pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="908c5-337">RunVirtual registry key supports packages that are published to the user</span></span>


<span data-ttu-id="908c5-338">App-V 5,0 SP3 ajoute une prise en charge de l’utilisation de la clé de Registre **RunVirtual** avec des applications virtualisées dans des packages publiés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="908c5-338">App-V 5.0 SP3 adds support for using the **RunVirtual** registry key with virtualized applications that are in user-published packages.</span></span> <span data-ttu-id="908c5-339">La clé de Registre **RunVirtual** vous permet d’exécuter une application installée localement dans un environnement virtuel, ainsi que des applications virtualisées à l’aide de App-V.</span><span class="sxs-lookup"><span data-stu-id="908c5-339">The **RunVirtual** registry key lets you run a locally installed application in a virtual environment, along with applications that have been virtualized by using App-V.</span></span>

<span data-ttu-id="908c5-340">Auparavant, les applications virtualisées des packages App-V devaient être publiées globalement.</span><span class="sxs-lookup"><span data-stu-id="908c5-340">Previously, the virtualized applications in App-V packages had to be published globally.</span></span> <span data-ttu-id="908c5-341">Pour plus d’informations sur **RunVirtual** et sur d’autres méthodes d’exécution des applications installées en local dans un environnement virtuel avec des applications virtualisées, voir [exécution d’une application installée localement dans un environnement virtuel avec des applications virtualisées](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="908c5-341">For more about **RunVirtual** and about other methods of running locally installed applications in a virtual environment with virtualized applications, see [Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span></span>

## <a href="" id="bkmk-posh-cmdlets-help"></a><span data-ttu-id="908c5-342">Nouvelles cmdlets PowerShell et aide sur les cmdlets</span><span class="sxs-lookup"><span data-stu-id="908c5-342">New PowerShell cmdlets and updateable cmdlet help</span></span>


<span data-ttu-id="908c5-343">Les nouvelles cmdlets PowerShell et l’aide à la mise à jour des applets de service sont inclus dans App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="908c5-343">New PowerShell cmdlets and updateable cmdlet help are included in App-V 5.0 SP3.</span></span> <span data-ttu-id="908c5-344">Pour télécharger les modules de cmdlet, voir [Comment charger les applets de cmdlet PowerShell et obtenir une aide pour les cmdlets](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span><span class="sxs-lookup"><span data-stu-id="908c5-344">To download the cmdlet modules, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span></span>

### <span data-ttu-id="908c5-345">Nouvelle applet de cmdlet PowerShell Server App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-345">New App-V 5.0 SP3 Server PowerShell cmdlets</span></span>

<span data-ttu-id="908c5-346">De nouvelles cmdlets Windows PowerShell pour le serveur App-V ont été ajoutées pour vous permettre de gérer les groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="908c5-346">New Windows PowerShell cmdlets for the App-V Server have been added to help you manage connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-347">Applet de commande</span><span class="sxs-lookup"><span data-stu-id="908c5-347">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="908c5-348">Description</span><span class="sxs-lookup"><span data-stu-id="908c5-348">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-349">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="908c5-349">Add-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-350">Ajoute un package à la fin d’un groupe de connexion&#39;liste des packages et vous permet de configurer le package en option et/ou sans version dans le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="908c5-350">Appends a package to the end of a connection group&#39;s package list and enables you to configure the package as optional and/or with no version within the connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-351">Set-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="908c5-351">Set-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-352">Vous permet de modifier les détails relatifs au package de groupe de connexion, par exemple, s’il est facultatif.</span><span class="sxs-lookup"><span data-stu-id="908c5-352">Enables you to edit details about the connection group package, such as whether it is optional.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-353">Remove-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="908c5-353">Remove-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-354">Supprime un package d’un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="908c5-354">Removes a package from a connection group.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="908c5-355">Obtenir de l’aide pour les applets de applet PowerShell</span><span class="sxs-lookup"><span data-stu-id="908c5-355">Getting help for the PowerShell cmdlets</span></span>

<span data-ttu-id="908c5-356">L’aide de l’applet de commande est disponible dans les formats suivants:</span><span class="sxs-lookup"><span data-stu-id="908c5-356">Cmdlet help is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-357">Format</span><span class="sxs-lookup"><span data-stu-id="908c5-357">Format</span></span></th>
<th align="left"><span data-ttu-id="908c5-358">Description</span><span class="sxs-lookup"><span data-stu-id="908c5-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-359">Module téléchargeable</span><span class="sxs-lookup"><span data-stu-id="908c5-359">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-360">Pour obtenir la dernière aide après le téléchargement du module de cmdlet:</span><span class="sxs-lookup"><span data-stu-id="908c5-360">To get the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="908c5-361">Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.</span><span class="sxs-lookup"><span data-stu-id="908c5-361">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="908c5-362">Tapez l’une des commandes suivantes pour charger les applets de commande pour le module souhaité:</span><span class="sxs-lookup"><span data-stu-id="908c5-362">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-363">Composant App-V</span><span class="sxs-lookup"><span data-stu-id="908c5-363">App-V component</span></span></th>
<th align="left"><span data-ttu-id="908c5-364">Commande pour taper</span><span class="sxs-lookup"><span data-stu-id="908c5-364">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-365">App-V Server</span><span class="sxs-lookup"><span data-stu-id="908c5-365">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-366">Mise à jour-aide-module AppvServer</span><span class="sxs-lookup"><span data-stu-id="908c5-366">Update-Help-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-367">Séquenceur App-V</span><span class="sxs-lookup"><span data-stu-id="908c5-367">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-368">Mise à jour-aide-module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="908c5-368">Update-Help-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-369">Client App-V</span><span class="sxs-lookup"><span data-stu-id="908c5-369">App-V client</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-370">Mise à jour-aide-module AppvClient</span><span class="sxs-lookup"><span data-stu-id="908c5-370">Update-Help-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-371">Sur TechNet en tant que pages Web</span><span class="sxs-lookup"><span data-stu-id="908c5-371">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-372">Pour plus d’information, voir le nœud App-V sous l' <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Automation Microsoft Desktop Optimization with Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="908c5-372">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="908c5-373">Pour plus d’informations, voir [Comment charger les applets de cmdlet PowerShell et obtenir une aide pour les cmdlets](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span><span class="sxs-lookup"><span data-stu-id="908c5-373">For more information, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span></span>

## <a href="" id="bkmk-pvad-hidden"></a><span data-ttu-id="908c5-374">Le répertoire principal de l’application virtuelle (PVAD) est masqué, mais peut être activé.</span><span class="sxs-lookup"><span data-stu-id="908c5-374">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>


<span data-ttu-id="908c5-375">Le répertoire principal de l’application virtuelle (PVAD) est masqué dans App-V 5,0 SP3, mais vous pouvez le réactiver en utilisant l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="908c5-375">The primary virtual application directory (PVAD) is hidden in App-V 5.0 SP3, but you can turn it back on and make it visible by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-376">Méthode</span><span class="sxs-lookup"><span data-stu-id="908c5-376">Method</span></span></th>
<th align="left"><span data-ttu-id="908c5-377">Étapes</span><span class="sxs-lookup"><span data-stu-id="908c5-377">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="908c5-378">Utiliser un paramètre de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="908c5-378">Use a command line parameter</span></span></p></td>
<td align="left"><p><span data-ttu-id="908c5-379">Transmettez le <strong> paramètre-EnablePVADControl </strong> à <strong> l' </strong>Sequencer.exe.</span><span class="sxs-lookup"><span data-stu-id="908c5-379">Pass the <strong>–EnablePVADControl</strong> parameter to the <strong>Sequencer.exe</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="908c5-380">Créer une sous-clé de Registre</span><span class="sxs-lookup"><span data-stu-id="908c5-380">Create a registry subkey</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="908c5-381">Dans l’éditeur du Registre, accédez à:</span><span class="sxs-lookup"><span data-stu-id="908c5-381">In the Registry Editor, navigate to:</span></span> <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong><span data-ttu-id="908c5-382">Remarque</span><span class="sxs-lookup"><span data-stu-id="908c5-382">Note</span></span></strong><br/><p><span data-ttu-id="908c5-383">S' <code>Compatibility</code> il n’existe pas, vous devez le créer.</span><span class="sxs-lookup"><span data-stu-id="908c5-383">If the <code>Compatibility</code> subkey doesn’t exist, you must create it.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="908c5-384">Créez une valeur DWORD nommée <strong> EnablePVADControl </strong> et définissez la valeur sur <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="908c5-384">Create a DWORD Value named <strong>EnablePVADControl</strong>, and set the value to <strong>1</strong>.</span></span></p>
<p><span data-ttu-id="908c5-385">La valeur <strong> 0 </strong> indique que PVAD est masqué.</span><span class="sxs-lookup"><span data-stu-id="908c5-385">A value of <strong>0</strong> means that PVAD is hidden.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>



<span data-ttu-id="908c5-386">En **savoir plus sur PVAD:** Lorsque vous utilisez le Sequencer pour créer un package, vous pouvez entrer un chemin d’installation pour le package.</span><span class="sxs-lookup"><span data-stu-id="908c5-386">**More about PVAD:** When you use the Sequencer to create a package, you can enter any installation path for the package.</span></span> <span data-ttu-id="908c5-387">Dans les versions précédentes de App-V, vous deviez spécifier le répertoire de l’application virtuelle (PVAD) principal de l’application comme chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="908c5-387">In past versions of App-V, you were required to specify the primary virtual application directory (PVAD) of the application as the path.</span></span> <span data-ttu-id="908c5-388">PVAD est le répertoire dans lequel vous devez généralement installer une application sur votre ordinateur local si vous n’utilisez pas App-V.</span><span class="sxs-lookup"><span data-stu-id="908c5-388">PVAD is the directory to which you would typically install an application on your local computer if you weren’t using App-V.</span></span> <span data-ttu-id="908c5-389">Par exemple, si vous avez installé Office sur un ordinateur, le PVAD est généralement C:\\Program Files\\Microsoft Office\\.</span><span class="sxs-lookup"><span data-stu-id="908c5-389">For example, if you were installing Office on a computer, the PVAD typically would be C:\\Program Files\\Microsoft Office\\.</span></span>

## <a href="" id="bkmk-pub-metadata-clientversion"></a><span data-ttu-id="908c5-390">ClientVersion est requis pour afficher les métadonnées de publication d’application-V</span><span class="sxs-lookup"><span data-stu-id="908c5-390">ClientVersion is required to view App-V publishing metadata</span></span>


<span data-ttu-id="908c5-391">Dans App-V 5,0 SP3, vous devez fournir les valeurs suivantes dans l’adresse lorsque vous interrogez le serveur de publication App-V pour les métadonnées:</span><span class="sxs-lookup"><span data-stu-id="908c5-391">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="908c5-392">Valeur</span><span class="sxs-lookup"><span data-stu-id="908c5-392">Value</span></span></th>
<th align="left"><span data-ttu-id="908c5-393">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="908c5-393">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="908c5-394">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="908c5-394">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="908c5-395">Si vous omettez le <strong> </strong> paramètre ClientVersion de la requête, les métadonnées excluent les nouvelles fonctionnalités d’App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="908c5-395">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="908c5-396">Clientos</span><span class="sxs-lookup"><span data-stu-id="908c5-396">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="908c5-397">Vous devez renseigner cette valeur uniquement si vous sélectionnez des systèmes d’exploitation de clients spécifiques lors du séquencé du package.</span><span class="sxs-lookup"><span data-stu-id="908c5-397">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="908c5-398">Si vous sélectionnez la valeur par défaut (tous les systèmes d’exploitation), ne spécifiez pas cette valeur dans la requête.</span><span class="sxs-lookup"><span data-stu-id="908c5-398">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="908c5-399">Si vous omettez le <strong> paramètre clientos </strong> dans la requête, seuls les packages qui ont été séquencés pour prendre en charge tout système d’exploitation apparaissent dans les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="908c5-399">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="908c5-400">Pour obtenir une syntaxe et des exemples de cette requête, consultez [affichage des métadonnées de publication d’App-V Server](viewing-app-v-server-publishing-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="908c5-400">For syntax and examples of this query, see [Viewing App-V Server Publishing Metadata](viewing-app-v-server-publishing-metadata.md).</span></span>

## <a href="" id="bkmk-event-logs-moved"></a><span data-ttu-id="908c5-401">Les journaux des événements App-V ont été consolidés</span><span class="sxs-lookup"><span data-stu-id="908c5-401">App-V event logs have been consolidated</span></span>


<span data-ttu-id="908c5-402">Les journaux d’événements suivants, précédemment situés dans \*\*les journaux d’application et de service journaux/Microsoft/AppV/ &lt; App-V &gt; \*\*, ont été déplacés vers **journaux des applications et services/Microsoft/AppV/ServiceLog**.</span><span class="sxs-lookup"><span data-stu-id="908c5-402">The following event logs, previously located at **Applications and Services Logs/Microsoft/AppV/&lt;App-V component&gt;**, have been moved to **Applications and Services Logs/Microsoft/AppV/ServiceLog**.</span></span>

<span data-ttu-id="908c5-403">Pour afficher les journaux, sélectionnez **affichage** &gt; **afficher les journaux d’analyse et de débogage** dans l’application Observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="908c5-403">To view the logs, select **View** &gt; **Show Analytic and Debug Logs** in the Event Viewer application.</span></span>

<span data-ttu-id="908c5-404">Client-client de catalogue-client d’intégration-client de catalogue-client d’orchestration-client-PackageConfig-client-client-service client-Vemgr-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary de sous-systèmes-sous-systèmes-appPath-FTA</span><span class="sxs-lookup"><span data-stu-id="908c5-404">Client-Catalog Client-Integration Client-Orchestration Client-PackageConfig Client-Scripting Client-Service Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary Subsystems-ActiveX Subsystems-AppPath Subsystems-Com Subsystems-fta</span></span>

## <span data-ttu-id="908c5-405">Obtention de technologies MDOP</span><span class="sxs-lookup"><span data-stu-id="908c5-405">How to Get MDOP Technologies</span></span>


<span data-ttu-id="908c5-406">App-V est un composant du pack d’optimisation du bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="908c5-406">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="908c5-407">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="908c5-407">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="908c5-408">Pour plus d’informations sur l’utilisation de Microsoft Software Assurance et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="908c5-408">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="908c5-409">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="908c5-409">Related topics</span></span>


[<span data-ttu-id="908c5-410">Notes de publication pour App-V5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="908c5-410">Release Notes for App-V 5.0 SP3</span></span>](release-notes-for-app-v-50-sp3.md)










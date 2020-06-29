---
title: Mise à niveau vers MBAM2.5 ou MBAM2.5 SP1 àpartir de versions antérieures
description: Mise à niveau vers MBAM2.5 ou MBAM2.5 SP1 àpartir de versions antérieures
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804464"
---
# <span data-ttu-id="df391-103">Mise à niveau vers MBAM2.5 ou MBAM2.5 SP1 àpartir de versions antérieures</span><span class="sxs-lookup"><span data-stu-id="df391-103">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>


<span data-ttu-id="df391-104">Cette rubrique décrit la procédure de mise à niveau du serveur d’administration et de surveillance Microsoft BitLocker (MBAM) et du client MBAM à partir des versions précédentes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="df391-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server and the MBAM Client from earlier versions of MBAM.</span></span>

<span data-ttu-id="df391-105">**Remarques**  Vous pouvez effectuer une mise à niveau directement vers MBAM 2,5 ou MBAM 2,5 SP1 à partir de n’importe quelle version précédente d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="df391-105">**Note** You can upgrade directly to MBAM 2.5 or MBAM 2.5 SP1 from any previous version of MBAM.</span></span>

 

## <span data-ttu-id="df391-106">Avant de commencer la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="df391-106">Before you start the upgrade</span></span>


<span data-ttu-id="df391-107">Passez en revue les informations suivantes avant de commencer la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="df391-107">Review the following information before you start the upgrade.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="df391-108">Ce que vous devez savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="df391-108">What to know before you start</span></span></th>
<th align="left"><span data-ttu-id="df391-109">Détails</span><span class="sxs-lookup"><span data-stu-id="df391-109">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df391-110">Si vous installez les sites Web MBAM sur un serveur et les services Web sur un autre serveur, vous devez utiliser les applets de cmdlets Windows PowerShell pour les configurer.</span><span class="sxs-lookup"><span data-stu-id="df391-110">If you are installing the MBAM websites on one server and the web services on another server, you have to use Windows PowerShell cmdlets to configure them.</span></span></p></td>
<td align="left"><p><span data-ttu-id="df391-111">L’Assistant Configuration du serveur MBAM ne prend pas en charge la configuration des sites Web sur un serveur et les services Web sur un autre serveur.</span><span class="sxs-lookup"><span data-stu-id="df391-111">The MBAM Server Configuration wizard does not support configuring the websites on one server and the web services on a different server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df391-112">Si vous effectuez une mise à niveau vers MBAM 2.5 ou 2,5 SP1 à partir de MBAM 2.0 ou 2,0 SP1 dans Windows Server 2008 R2:</span><span class="sxs-lookup"><span data-stu-id="df391-112">If you are upgrading to MBAM2.5 or 2.5 SP1 from MBAM2.0 or 2.0 SP1 in Windows Server2008 R2:</span></span></p>
<p><span data-ttu-id="df391-113">Le site Web d’administration et de contrôle, le portail libre-service ne fonctionnera pas si vous installez le logiciel .NET Framework 4.5 requis après l’installation d’Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="df391-113">The Administration and Monitoring Website and the Self-Service Portal will not work if you install the required .NET Framework4.5 software after Internet Information Services (IIS) is already installed.</span></span></p>
<p><span data-ttu-id="df391-114">Ce problème survient parce que ASP.NET ne peut pas être correctement inscrit dans IIS si .NET Framework est installé après l’installation d’IIS.</span><span class="sxs-lookup"><span data-stu-id="df391-114">This issue occurs because ASP.NET cannot be registered correctly with IIS if the .NET Framework is installed after IIS has already been installed.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="df391-115">Pour résoudre ce problème:</span><span class="sxs-lookup"><span data-stu-id="df391-115">To resolve this issue:</span></span></strong></p>
<p><span data-ttu-id="df391-116">Exécutez <strong> aspnet_regiis, </strong> à partir de l’emplacement suivant:</span><span class="sxs-lookup"><span data-stu-id="df391-116">Run <strong>aspnet_regiis –i</strong> from the following location:</span></span></p>
<p><span data-ttu-id="df391-117">C:\windows\microsoft.net\Framework\v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="df391-117">C:\windows\microsoft.net\Framework\v4.0.30319</span></span></p>
<p><span data-ttu-id="df391-118">Pour plus d’informations, reportez-vous à la rubrique: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> ASP.net de l’outil d’inscription </a> .</span><span class="sxs-lookup"><span data-stu-id="df391-118">For more information, see: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)">ASP.NET IIS Registration Tool</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df391-119">Enregistrez un SPN sur le compte du pool d’applications si toutes les conditions suivantes sont vraies:</span><span class="sxs-lookup"><span data-stu-id="df391-119">Register an SPN on the application pool account if all of the following are true:</span></span></p>
<ul>
<li><p><span data-ttu-id="df391-120">Vous effectuez une mise à niveau à partir d’une version précédente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="df391-120">You are upgrading from a previous version of MBAM.</span></span></p></li>
<li><p><span data-ttu-id="df391-121">Pour le moment, vous n’utilisez pas le site Web MBAM dans une configuration à charge équilibrée ou distribuée, mais vous aimeriez le faire lorsque vous effectuez une mise à niveau vers MBAM 2.5 ou 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="df391-121">Currently, you are not running the MBAM websites in a load-balanced or distributed configuration, but you would like to do so when you upgrade to MBAM2.5 or 2.5 SP1.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="df391-122">Pour obtenir des instructions, voir <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> planification de la sécurisation des sites Web MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="df391-122">For instructions, see <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)">Planning How to Secure the MBAM Websites</a>.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="df391-123">Ce que nous recommandons</span><span class="sxs-lookup"><span data-stu-id="df391-123">What we recommend</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="df391-124">Enregistrez un nom de principal de service (SPN) pour le compte du pool d’applications, même si vous disposez déjà de SPN enregistrés pour le compte d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="df391-124">Register a service principal name (SPN) for the application pool account, even though you may already have registered SPNs for the machine account.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="df391-125">Pourquoi nous le recommandons</span><span class="sxs-lookup"><span data-stu-id="df391-125">Why we recommend it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="df391-126">Il est nécessaire de procéder à l’inscription d’un SPN sur le compte du pool d’applications pour configurer les sites Web dans une configuration distribuée ou dont le chargement est équilibré.</span><span class="sxs-lookup"><span data-stu-id="df391-126">Registering an SPN on the application pool account is required to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="df391-127">Que se passe-t-il si le SPN est déjà configuré sur un compte d’ordinateur?</span><span class="sxs-lookup"><span data-stu-id="df391-127">What happens if SPNs are already configured on a machine account?</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="df391-128">MBAM utilisera les SPN que vous avez déjà inscrits et vous n’avez pas besoin de configurer des SPN supplémentaires, mais vous n’êtes pas en mesure de configurer les sites Web dans une configuration à charge équilibrée ou distribuée.</span><span class="sxs-lookup"><span data-stu-id="df391-128">MBAM will use the SPNs that you have already registered, and you don’t need to configure additional SPNs, but you are not able to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="df391-129">Procédure de mise à niveau de l’infrastructure du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="df391-129">Steps to upgrade the MBAM Server infrastructure</span></span>


<span data-ttu-id="df391-130">Suivez les étapes décrites dans les sections suivantes pour mettre à niveau MBAM pour la topologie autonome ou la topologie d’intégration de System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="df391-130">Use the steps in the following sections to upgrade MBAM for the Stand-alone topology or the System Center Configuration Manager Integration topology.</span></span>

**<span data-ttu-id="df391-131">Pour mettre à niveau l’infrastructure du serveur MBAM pour une topologie autonome</span><span class="sxs-lookup"><span data-stu-id="df391-131">To upgrade the MBAM Server infrastructure for Stand-alone topology</span></span>**

1.  <span data-ttu-id="df391-132">Désinstallez les versions précédentes de MBAM à partir de **programmes et fonctionnalités** , et de serveurs Web pour vous assurer que les informations ne sont pas écrites à partir des clients MBAM vers l’infrastructure MBAM.</span><span class="sxs-lookup"><span data-stu-id="df391-132">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="df391-133">Pour obtenir des instructions, voir [suppression des fonctionnalités ou logiciels du serveur MBAM](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="df391-133">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="df391-134">Sauvegardez vos bases de données.</span><span class="sxs-lookup"><span data-stu-id="df391-134">Back up your databases.</span></span>

3.  <span data-ttu-id="df391-135">Désinstallez les versions précédentes de MBAM à partir de SQL Server à l’aide de **programmes et fonctionnalités**, y compris SQL Server hébergeant les rapports MBAM via SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="df391-135">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="df391-136">Supprimez tous les fichiers ou dossiers temporaires du serveur MBAM du serveur de base de données et de Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="df391-136">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

    <span data-ttu-id="df391-137">**Remarques**  Les bases de données ne seront pas supprimées, et toutes les données de conformité et de récupération sont conservées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="df391-137">**Note** The databases will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

4.  <span data-ttu-id="df391-138">Installez et configurez les bases de données, rapports et applications Web MBAM 2.5 ou 2,5 SP1 dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="df391-138">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, and web applications, in that order.</span></span> <span data-ttu-id="df391-139">Les bases de données sont mises à niveau en place.</span><span class="sxs-lookup"><span data-stu-id="df391-139">The databases are upgraded in place.</span></span>

5.  <span data-ttu-id="df391-140">Mettez à jour les objets de stratégie de groupe à l’aide des modèles MBAM 2,5 pour tirer parti des nouvelles fonctionnalités de MBAM, telles que le chiffrement appliqué.</span><span class="sxs-lookup"><span data-stu-id="df391-140">Update the Group Policy Objects (GPOs) using the MBAM 2.5 Templates to leverage the new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="df391-141">Si vous ne mettez pas à jour les objets de stratégie de groupe et le client MBAM sur MBAM 2,5, les versions antérieures de clients MBAM continuent de créer des rapports sur vos objets de stratégie de groupe actuels avec des fonctionnalités réduites.</span><span class="sxs-lookup"><span data-stu-id="df391-141">If you do not update the GPOs and the MBAM client to MBAM 2.5, earlier versions of MBAM clients will continue to report against your current GPOs with reduced functionality.</span></span> <span data-ttu-id="df391-142">Découvrez [Comment obtenir des modèles de stratégie de groupe MDOP (. admx)](https://www.microsoft.com/download/details.aspx?id=41183) pour télécharger les derniers modèles ADMX.</span><span class="sxs-lookup"><span data-stu-id="df391-142">See [How to Get MDOP Group Policy (.admx) Templates](https://www.microsoft.com/download/details.aspx?id=41183) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="df391-143">Après avoir effectué la mise à niveau de l’infrastructure du serveur MBAM, les ordinateurs clients existants continuent de rapporter au serveur MBAM 2.5 ou 2,5 SP1, et les données de récupération continuent d’être stockées.</span><span class="sxs-lookup"><span data-stu-id="df391-143">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

6.  <span data-ttu-id="df391-144">Installez la dernière version de MBAM ou du client 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="df391-144">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="df391-145">Il n’est pas nécessaire de redémarrer les ordinateurs clients après le déploiement.</span><span class="sxs-lookup"><span data-stu-id="df391-145">Client computers do not need to be rebooted after the deployment.</span></span>

**<span data-ttu-id="df391-146">Pour mettre à niveau la topologie d’intégration de l’infrastructure MBAM pour System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="df391-146">To upgrade the MBAM infrastructure for System Center Configuration Manager Integration topology</span></span>**

1.  <span data-ttu-id="df391-147">Désinstallez les versions précédentes de MBAM à partir de **programmes et fonctionnalités** , et de serveurs Web pour vous assurer que les informations ne sont pas écrites à partir des clients MBAM vers l’infrastructure MBAM.</span><span class="sxs-lookup"><span data-stu-id="df391-147">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="df391-148">Pour obtenir des instructions, voir [suppression des fonctionnalités ou logiciels du serveur MBAM](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="df391-148">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="df391-149">Sauvegardez vos bases de données.</span><span class="sxs-lookup"><span data-stu-id="df391-149">Back up your databases.</span></span>

3.  <span data-ttu-id="df391-150">Désinstallez les versions précédentes de MBAM à partir de SQL Server à l’aide de **programmes et fonctionnalités**, y compris SQL Server hébergeant les rapports MBAM via SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="df391-150">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="df391-151">Supprimez tous les fichiers ou dossiers temporaires du serveur MBAM du serveur de base de données et de Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="df391-151">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

4.  <span data-ttu-id="df391-152">Désinstaller MBAM à partir du serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="df391-152">Uninstall MBAM from the Configuration Manager server.</span></span>

    <span data-ttu-id="df391-153">**Remarques**  Les bases de données et les objets de Configuration Manager (Planning de référence, collection d’ordinateurs pris en charge par MBAM et rapports) ne seront pas supprimés, et toutes les données de conformité et de récupération sont conservées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="df391-153">**Note** The databases and the Configuration Manager objects (baseline, MBAM supported computers collection, and Reports) will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

5.  <span data-ttu-id="df391-154">Mettez à jour les fichiers. mof.</span><span class="sxs-lookup"><span data-stu-id="df391-154">Update the .mof files.</span></span>

6.  <span data-ttu-id="df391-155">Installez et configurez les bases de données, rapports, applications Web et intégration du gestionnaire de configuration MBAM 2.5 ou 2,5 SP1 dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="df391-155">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, web applications, and Configuration Manager integration, in that order.</span></span> <span data-ttu-id="df391-156">Les bases de données et les objets gestionnaires de configuration sont mis à niveau en place.</span><span class="sxs-lookup"><span data-stu-id="df391-156">The databases and Configuration Manager objects are upgraded in place.</span></span>

7.  <span data-ttu-id="df391-157">Vous pouvez également mettre à jour les objets de stratégie de groupe (GPO) et modifier les paramètres si vous voulez implémenter de nouvelles fonctionnalités dans MBAM, par exemple un chiffrement appliqué.</span><span class="sxs-lookup"><span data-stu-id="df391-157">Optionally, update the Group Policy Objects (GPOs), and edit the settings if you want to implement new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="df391-158">Si vous ne mettez pas à jour les objets de stratégie de groupe, MBAM continuera à créer des rapports sur vos objets de stratégie de groupe actuels.</span><span class="sxs-lookup"><span data-stu-id="df391-158">If you do not update the GPOs, MBAM will continue to report against your current GPOs.</span></span> <span data-ttu-id="df391-159">Découvrez [Comment obtenir des modèles de stratégie de groupe MDOP (. admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) pour télécharger les derniers modèles ADMX.</span><span class="sxs-lookup"><span data-stu-id="df391-159">See [How to Get MDOP Group Policy (.admx) Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="df391-160">Après avoir effectué la mise à niveau de l’infrastructure du serveur MBAM, les ordinateurs clients existants continuent de rapporter au serveur MBAM 2.5 ou 2,5 SP1, et les données de récupération continuent d’être stockées.</span><span class="sxs-lookup"><span data-stu-id="df391-160">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

8.  <span data-ttu-id="df391-161">Installez la dernière version de MBAM ou du client 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="df391-161">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="df391-162">Il n’est pas nécessaire de redémarrer les ordinateurs clients après le déploiement.</span><span class="sxs-lookup"><span data-stu-id="df391-162">Client computers do not need to be rebooted after the deployment.</span></span>

## <span data-ttu-id="df391-163">Prise en charge de la mise à niveau du client MBAM</span><span class="sxs-lookup"><span data-stu-id="df391-163">Upgrade support for the MBAM Client</span></span>


<span data-ttu-id="df391-164">MBAM prend en charge les mises à jour du client MBAM 2.5 à partir de n’importe quelle version antérieure du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="df391-164">MBAM supports upgrades to the MBAM2.5 Client from any earlier version of the MBAM Client.</span></span>

**<span data-ttu-id="df391-165">Procédures d’installation du client MBAM:</span><span class="sxs-lookup"><span data-stu-id="df391-165">Ways to install the MBAM Client:</span></span>**

-   <span data-ttu-id="df391-166">Mettez à niveau les ordinateurs exécutant le client MBAM en une seule fois ou progressivement après l’installation de l’infrastructure du serveur MBAM 2.5.</span><span class="sxs-lookup"><span data-stu-id="df391-166">Upgrade the computers running MBAM Client all at once or gradually after you install the MBAM2.5 Server infrastructure.</span></span>

-   <span data-ttu-id="df391-167">Installez le client MBAM par le biais d’un système de distribution de logiciels électronique ou via des outils tels que Active Directory Domain Services ou System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="df391-167">Install the MBAM Client through an electronic software distribution system or through tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>



## <span data-ttu-id="df391-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df391-168">Related topics</span></span>


[<span data-ttu-id="df391-169">Déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="df391-169">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="df391-170">Déploiement du client MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="df391-170">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="df391-171">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="df391-171">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="df391-172">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="df391-172">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="df391-173">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="df391-173">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="df391-174">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="df391-174">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 






---
title: Vérifier les clés de Registre avant d'installer App-V5.x Server
description: Vérifier les clés de Registre avant d'installer App-V5.x Server
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805929"
---
# <span data-ttu-id="81a10-103">Vérifier les clés de Registre avant d'installer App-V5.x Server</span><span class="sxs-lookup"><span data-stu-id="81a10-103">Check Registry Keys before installing App-V 5.x Server</span></span>

<span data-ttu-id="81a10-104">Si vous procédez à la mise à niveau de l’application-V Server du correctif logiciel pour App-V 5,0 SP1 ou version ultérieure, suivez les étapes décrites dans cette section avant d’installer l’App-V 5. x Server.</span><span class="sxs-lookup"><span data-stu-id="81a10-104">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in this section before installing the App-V 5.x Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="81a10-105">Lorsque cette étape est nécessaire</span><span class="sxs-lookup"><span data-stu-id="81a10-105">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="81a10-106">Vous procédez à la mise à niveau de App-V 5,0 SP1 avec les packages de correctifs suivants que vous avez installés à l’aide d’un fichier. msp.</span><span class="sxs-lookup"><span data-stu-id="81a10-106">You are upgrading from App-V 5.0 SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="81a10-107">Quels composants nécessitent cette étape</span><span class="sxs-lookup"><span data-stu-id="81a10-107">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="81a10-108">Uniquement les composants serveur App-V que vous effectuez une mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="81a10-108">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="81a10-109">Lorsque vous devez effectuer cette étape</span><span class="sxs-lookup"><span data-stu-id="81a10-109">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="81a10-110">Avant de mettre à niveau l’application-V Server vers App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="81a10-110">Before you upgrade the App-V Server to App-V 5.x</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="81a10-111">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="81a10-111">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="81a10-112">À l’aide des informations contenues dans les tableaux ci-dessous, vous devez mettre à jour chaque valeur de clé de registre en <code>HKLM\Software\Microsoft\AppV\Server</code> fonction de la valeur que vous avez fournie lors de votre installation de serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="81a10-112">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="81a10-113">Cette étape restaure les valeurs de Registre susceptibles d’avoir été supprimées lors de l’installation des packages de correctifs App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="81a10-113">Completing this step restores registry values that may have been removed when App-V 5.0 SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="81a10-114">Clé ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="81a10-114">ManagementDatabase key</span></span>**

<span data-ttu-id="81a10-115">Si vous installez la base de données de gestion, définissez les clés de Registre suivantes `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="81a10-115">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81a10-116">Nom de la clé</span><span class="sxs-lookup"><span data-stu-id="81a10-116">Key name</span></span></th>
<th align="left"><span data-ttu-id="81a10-117">Description</span><span class="sxs-lookup"><span data-stu-id="81a10-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="81a10-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-119">Indique si un compte d’accès public est requis pour accéder aux bases de données de gestion non locales.</span><span class="sxs-lookup"><span data-stu-id="81a10-119">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="81a10-120">La valeur est définie sur «1» s’il est requis.</span><span class="sxs-lookup"><span data-stu-id="81a10-120">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-121">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="81a10-121">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-122">Nom de la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="81a10-122">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="81a10-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-124">Compte utilisé pour l’accès en lecture (public) à la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="81a10-124">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="81a10-125">Utilisé lorsque <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="81a10-125">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="81a10-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-127">ID de sécurité (SID) du compte utilisé pour l’accès en lecture (public) à la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="81a10-127">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="81a10-128">Utilisé lorsque <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="81a10-128">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-129">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="81a10-129">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-130">Instance SQL Server de la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="81a10-130">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="81a10-131">Si la valeur est vide, l’instance de base de données par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="81a10-131">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="81a10-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-133">Compte utilisé pour l’accès en écriture (administrateur) à la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="81a10-133">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="81a10-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-135">ID de sécurité (SID) du compte utilisé pour l’accès en écriture (administrateur) à la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="81a10-135">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="81a10-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-137">Compte d’ordinateur distant du serveur de gestion (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="81a10-137">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="81a10-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-139">Connexion administrateur d’installation pour le serveur de gestion (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="81a10-139">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="81a10-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-141">Valeurs valides:</span><span class="sxs-lookup"><span data-stu-id="81a10-141">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="81a10-142">1 </strong> – le service de gestion est sur l’ordinateur local, c’est-à-dire MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT est vide.</span><span class="sxs-lookup"><span data-stu-id="81a10-142">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="81a10-143">0 </strong> - le service de gestion est sur un ordinateur différent de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="81a10-143">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="81a10-144">Clé ManagementService</span><span class="sxs-lookup"><span data-stu-id="81a10-144">ManagementService key</span></span>**

<span data-ttu-id="81a10-145">Si vous installez le serveur de gestion, définissez les clés de Registre suivantes `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="81a10-145">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81a10-146">Nom de la clé</span><span class="sxs-lookup"><span data-stu-id="81a10-146">Key name</span></span></th>
<th align="left"><span data-ttu-id="81a10-147">Description</span><span class="sxs-lookup"><span data-stu-id="81a10-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-148">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="81a10-148">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-149">Le compte ou le groupe AD DS (Active Directory Domain Services) qui est autorisé à gérer App-V (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="81a10-149">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-150">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="81a10-150">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-151">Instance SQL Server qui contient la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="81a10-151">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="81a10-152">Si la valeur est vide, l’instance de base de données par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="81a10-152">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-153">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="81a10-153">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-154">Nom du serveur SQL distant doté de la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="81a10-154">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="81a10-155">Si la valeur est vide, l’ordinateur local est utilisé.</span><span class="sxs-lookup"><span data-stu-id="81a10-155">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="81a10-156">Clé ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="81a10-156">ReportingDatabase key</span></span>**

<span data-ttu-id="81a10-157">Si vous installez la base de données de création de rapports, définissez ces clés de Registre sous `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="81a10-157">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81a10-158">Nom de la clé</span><span class="sxs-lookup"><span data-stu-id="81a10-158">Key name</span></span></th>
<th align="left"><span data-ttu-id="81a10-159">Description</span><span class="sxs-lookup"><span data-stu-id="81a10-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="81a10-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-161">Indique si un compte d’accès public est requis pour accéder aux bases de données de création de rapports non locales.</span><span class="sxs-lookup"><span data-stu-id="81a10-161">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="81a10-162">La valeur est définie sur «1» s’il est requis.</span><span class="sxs-lookup"><span data-stu-id="81a10-162">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-163">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="81a10-163">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-164">Nom de la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="81a10-164">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="81a10-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-166">Compte utilisé pour l’accès en lecture (public) à la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="81a10-166">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="81a10-167">Utilisé lorsque <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="81a10-167">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="81a10-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-169">ID de sécurité (SID) du compte utilisé pour l’accès en lecture (public) à la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="81a10-169">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="81a10-170">Utilisé lorsque <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="81a10-170">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-171">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="81a10-171">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-172">Instance SQL Server de la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="81a10-172">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="81a10-173">Si la valeur est vide, l’instance de base de données par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="81a10-173">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="81a10-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="81a10-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="81a10-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-177">Compte d’ordinateur distant du serveur de rapports (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="81a10-177">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="81a10-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-179">Connexion administrateur d’installation pour le serveur de rapports (domaine\compte).</span><span class="sxs-lookup"><span data-stu-id="81a10-179">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="81a10-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-181">Valeurs valides:</span><span class="sxs-lookup"><span data-stu-id="81a10-181">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="81a10-182">1 </strong> – le service de création de rapports est sur l’ordinateur local, c’est-à-dire REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT est vide.</span><span class="sxs-lookup"><span data-stu-id="81a10-182">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="81a10-183">0 </strong> - le service de création de rapports est sur un ordinateur différent de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="81a10-183">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="81a10-184">Clé ReportingService</span><span class="sxs-lookup"><span data-stu-id="81a10-184">ReportingService key</span></span>**

<span data-ttu-id="81a10-185">Si vous installez le serveur de création de rapports, définissez ces clés de Registre sous `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="81a10-185">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81a10-186">Nom de la clé</span><span class="sxs-lookup"><span data-stu-id="81a10-186">Key name</span></span></th>
<th align="left"><span data-ttu-id="81a10-187">Description</span><span class="sxs-lookup"><span data-stu-id="81a10-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81a10-188">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="81a10-188">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-189">Instance SQL Server de la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="81a10-189">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="81a10-190">Si la valeur est vide, l’instance de base de données par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="81a10-190">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81a10-191">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="81a10-191">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="81a10-192">Nom du serveur SQL distant avec la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="81a10-192">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="81a10-193">Si la valeur est vide, l’ordinateur local est utilisé.</span><span class="sxs-lookup"><span data-stu-id="81a10-193">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>


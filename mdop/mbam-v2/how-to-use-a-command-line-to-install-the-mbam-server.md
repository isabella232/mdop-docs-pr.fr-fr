---
title: Utilisation d'une ligne de commande pour installer le serveur MBAM
description: Utilisation d'une ligne de commande pour installer le serveur MBAM
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811279"
---
# <span data-ttu-id="bc7f1-103">Utilisation d'une ligne de commande pour installer le serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="bc7f1-103">How to Use a Command Line to Install the MBAM Server</span></span>


<span data-ttu-id="bc7f1-104">Vous pouvez utiliser une ligne de commande pour installer le serveur MBAM à l’aide du topologie autonome ou du gestionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-104">You can use a command line to install the MBAM Server with either the Stand-alone or Configuration Manager topology.</span></span> <span data-ttu-id="bc7f1-105">L’exemple de ligne de commande suivant concerne le déploiement d’MBAM sur un serveur unique, qui est une architecture qui doit être utilisée uniquement dans un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-105">The following command line example is for deploying MBAM on a single server, which is an architecture that should be used only in a test environment.</span></span> <span data-ttu-id="bc7f1-106">Vous devez modifier la ligne de commande en conséquence lorsque vous déployez MBAM dans un environnement de production, qui doit avoir plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-106">You will need to change the command line accordingly when you deploy MBAM to a production environment, which should have multiple servers.</span></span>

## <span data-ttu-id="bc7f1-107">Ligne de commande pour le déploiement du serveur MBAM 2.0 avec la topologie autonome</span><span class="sxs-lookup"><span data-stu-id="bc7f1-107">Command Line for Deploying the MBAM2.0 Server with the Stand-alone Topology</span></span>


<span data-ttu-id="bc7f1-108">Vous pouvez utiliser une ligne de commande similaire à celle ci-dessous pour installer le serveur MBAM avec la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-108">You can use a command line that is similar to the following to install the MBAM Server with the Stand-alone topology.</span></span>

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="bc7f1-109">Le tableau suivant décrit les paramètres de ligne de commande pour le déploiement du serveur MBAM avec la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-109">The following table describes the command line parameters for deploying the MBAM Server with the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc7f1-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="bc7f1-110">Parameter</span></span></th>
<th align="left"><span data-ttu-id="bc7f1-111">Valeur du paramètre</span><span class="sxs-lookup"><span data-stu-id="bc7f1-111">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="bc7f1-112">Description</span><span class="sxs-lookup"><span data-stu-id="bc7f1-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-113">TOPOLOGIE</span><span class="sxs-lookup"><span data-stu-id="bc7f1-113">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-114">0,4</span><span class="sxs-lookup"><span data-stu-id="bc7f1-114">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-115">0-topologie autonome</span><span class="sxs-lookup"><span data-stu-id="bc7f1-115">0 – Stand-alone topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc7f1-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="bc7f1-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-117">nommée</span><span class="sxs-lookup"><span data-stu-id="bc7f1-117">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-118">0 – n’acceptez pas le contrat de licence agreement1: acceptez le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-118">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-119">ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="bc7f1-119">ADDLOCAL</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-120">Fonctionnalités devant être installées sur le serveur</span><span class="sxs-lookup"><span data-stu-id="bc7f1-120">Features to be installed on the Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-121">Keydatabase</span><span class="sxs-lookup"><span data-stu-id="bc7f1-121">KeyDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-122">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="bc7f1-122">Recovery Database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-123">ReportsDatabase</span><span class="sxs-lookup"><span data-stu-id="bc7f1-123">ReportsDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-124">Base de données des rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="bc7f1-124">Compliance and Audit Reports Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-125">Rapports</span><span class="sxs-lookup"><span data-stu-id="bc7f1-125">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-126">Rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="bc7f1-126">Compliance and Audit Reports</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-127">AdministrationMonitoringServer</span><span class="sxs-lookup"><span data-stu-id="bc7f1-127">AdministrationMonitoringServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-128">Site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="bc7f1-128">Administration and Monitoring website</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-129">SelfServiceServer</span><span class="sxs-lookup"><span data-stu-id="bc7f1-129">SelfServiceServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-130">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="bc7f1-130">Self-Service Portal</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-131">PolicyTemplate</span><span class="sxs-lookup"><span data-stu-id="bc7f1-131">PolicyTemplate</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-132">Modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="bc7f1-132">MBAM Group Policy template</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc7f1-133">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc7f1-133">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-134">UserDomain [UserName1]</span><span class="sxs-lookup"><span data-stu-id="bc7f1-134">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-135">Domaine et compte d’utilisateur du compte Reporting Services qui accèdent à la base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="bc7f1-135">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-136">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="bc7f1-136">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-137">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="bc7f1-137">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-138">Mot de passe du compte de service Reporting Services qui accède à la base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="bc7f1-138">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc7f1-139">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc7f1-139">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-140">masque</span><span class="sxs-lookup"><span data-stu-id="bc7f1-140">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-141">Nom de l’instance SQL Server pour la base de données d’audit et de conformité: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-141">SQL Server instance name for the Compliance and Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-142">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc7f1-142">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-143">masque</span><span class="sxs-lookup"><span data-stu-id="bc7f1-143">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-144">Nom de l’instance SQL Server pour la base de données de récupération: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-144">SQL Server instance name for the Recovery Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc7f1-145">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="bc7f1-145">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-146">masque</span><span class="sxs-lookup"><span data-stu-id="bc7f1-146">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-147">Instance SQL Server Reporting Server sur laquelle sont installés les rapports de conformité et d’audit: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-147">SQL Server Reporting Server instance where the Compliance and Audit reports will be installed – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-148">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="bc7f1-148">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-149">83</span><span class="sxs-lookup"><span data-stu-id="bc7f1-149">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-150">Port pour le site Web d’administration et de surveillance; «83» n’est qu’un exemple</span><span class="sxs-lookup"><span data-stu-id="bc7f1-150">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc7f1-151">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="bc7f1-151">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-152">83</span><span class="sxs-lookup"><span data-stu-id="bc7f1-152">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-153">Port pour le site Web du portail libre-service; «83» n’est qu’un exemple</span><span class="sxs-lookup"><span data-stu-id="bc7f1-153">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bc7f1-154">Ligne de commande pour le déploiement du serveur MBAM 2.0 avec la topologie Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bc7f1-154">Command Line for Deploying the MBAM2.0 Server with the Configuration Manager Topology</span></span>


<span data-ttu-id="bc7f1-155">Vous pouvez utiliser une ligne de commande semblable à ce qui suit pour installer le serveur MBAM avec la topologie Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-155">You can use a command line that is similar to the following to install the MBAM Server with the Configuration Manager topology.</span></span>

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="bc7f1-156">Le tableau suivant décrit les paramètres de ligne de commande pour l’installation du serveur MBAM 2.0 avec la topologie Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-156">The following table describes the command line parameters for installing the MBAM2.0 Server with the Configuration Manager topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc7f1-157">Paramètre</span><span class="sxs-lookup"><span data-stu-id="bc7f1-157">Parameter</span></span></th>
<th align="left"><span data-ttu-id="bc7f1-158">Valeur du paramètre</span><span class="sxs-lookup"><span data-stu-id="bc7f1-158">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="bc7f1-159">Description</span><span class="sxs-lookup"><span data-stu-id="bc7f1-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-160">TOPOLOGIE</span><span class="sxs-lookup"><span data-stu-id="bc7f1-160">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-161">1</span><span class="sxs-lookup"><span data-stu-id="bc7f1-161">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-162">1-topologie de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bc7f1-162">1 – Configuration Manager topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc7f1-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="bc7f1-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-164">nommée</span><span class="sxs-lookup"><span data-stu-id="bc7f1-164">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-165">0 – n’acceptez pas le contrat de licence agreement1: acceptez le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-165">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-166">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc7f1-166">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-167">masque</span><span class="sxs-lookup"><span data-stu-id="bc7f1-167">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-168">Nom de l’instance SQL Server pour la base de données d’audit: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-168">SQL Server instance name for the Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc7f1-169">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc7f1-169">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-170">masque</span><span class="sxs-lookup"><span data-stu-id="bc7f1-170">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-171">Nom de l’instance SQL Server pour la base de données de récupération: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-171">SQL Server instance name for the Recovery Database - replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-172">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="bc7f1-172">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-173">masque</span><span class="sxs-lookup"><span data-stu-id="bc7f1-173">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-174">Instance SQL Server Reporting Server sur laquelle les rapports d’audit seront installés: remplacez% ComputerName% par le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bc7f1-174">SQL Server Reporting Server instance where the Audit reports will be installed – replace %computername% with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc7f1-175">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc7f1-175">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-176">UserDomain [UserName1]</span><span class="sxs-lookup"><span data-stu-id="bc7f1-176">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-177">Domaine et compte d’utilisateur du compte Reporting Services qui accèdent à la base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="bc7f1-177">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-178">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="bc7f1-178">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-179">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="bc7f1-179">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-180">Mot de passe du compte de service Reporting Services qui accède à la base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="bc7f1-180">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc7f1-181">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="bc7f1-181">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-182">83</span><span class="sxs-lookup"><span data-stu-id="bc7f1-182">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-183">Port pour le site Web d’administration et de surveillance; «83» n’est qu’un exemple</span><span class="sxs-lookup"><span data-stu-id="bc7f1-183">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc7f1-184">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="bc7f1-184">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-185">83</span><span class="sxs-lookup"><span data-stu-id="bc7f1-185">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc7f1-186">Port pour le site Web du portail libre-service; «83» n’est qu’un exemple</span><span class="sxs-lookup"><span data-stu-id="bc7f1-186">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bc7f1-187">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc7f1-187">Related topics</span></span>


[<span data-ttu-id="bc7f1-188">Déploiement de l'infrastructure de serveur MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="bc7f1-188">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 






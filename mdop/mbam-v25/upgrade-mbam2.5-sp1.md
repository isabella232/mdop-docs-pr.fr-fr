---
title: Mise à niveau de MBAM 2,5 vers MBAM 2,5 SP1 de maintenance de la mise à jour de maintenance
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804476"
---
# <span data-ttu-id="05067-102">Mise à niveau de MBAM 2,5 vers MBAM 2,5 SP1 maintenance Release Update</span><span class="sxs-lookup"><span data-stu-id="05067-102">Upgrade from MBAM 2.5 to MBAM 2.5 SP1 Servicing Release Update</span></span>

<span data-ttu-id="05067-103">Cet article fournit des instructions pas à pas pour mettre à niveau l’administration et la surveillance de Microsoft BitLocker (MBAM) 2,5 vers MBAM 2,5 Service Pack 1 (SP1) conjointement avec le [2019 Pack d’optimisation de bureau Microsoft](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)</span><span class="sxs-lookup"><span data-stu-id="05067-103">This article provides step-by-step instructions to upgrade Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 to MBAM 2.5 Service Pack 1 (SP1) together with the [Microsoft Desktop Optimization Pack (MDOP) May 2019 servicing update](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) in a standalone configuration.</span></span>

<span data-ttu-id="05067-104">Dans ce guide, nous allons utiliser une configuration à deux serveurs.</span><span class="sxs-lookup"><span data-stu-id="05067-104">In this guide, we will use a two-server configuration.</span></span> <span data-ttu-id="05067-105">Un serveur sera un serveur de base de données exécutant Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="05067-105">One server will be a database server that's running Microsoft SQL Server 2016.</span></span> <span data-ttu-id="05067-106">Ce serveur va héberger les bases de données et les rapports MBAM.</span><span class="sxs-lookup"><span data-stu-id="05067-106">This server will host the MBAM databases and reports.</span></span> <span data-ttu-id="05067-107">L’autre serveur sera un serveur Web Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="05067-107">The other server will be a Windows Server 2012 R2 web server.</span></span> <span data-ttu-id="05067-108">Ce serveur va héberger «administration et surveillance» et «portail libre-service».</span><span class="sxs-lookup"><span data-stu-id="05067-108">This server will host "Administration and Monitoring" and "Self-Service Portal."</span></span>

## <span data-ttu-id="05067-109">Préparer la mise à niveau de MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="05067-109">Prepare to upgrade MBAM 2.5 SP1</span></span>

### <span data-ttu-id="05067-110">Familiarisez-vous avec les serveurs MBAM dans votre environnement</span><span class="sxs-lookup"><span data-stu-id="05067-110">Know the MBAM servers in your environment</span></span>

1. <span data-ttu-id="05067-111">Moteur de base de données SQL Server: serveur qui héberge les bases de données MBAM.</span><span class="sxs-lookup"><span data-stu-id="05067-111">SQL Server Database Engine: Server that hosts the MBAM databases.</span></span>
2. <span data-ttu-id="05067-112">SQL Server Reporting Services: serveur qui héberge les rapports MBAM.</span><span class="sxs-lookup"><span data-stu-id="05067-112">SQL Server Reporting Services: Server that hosts the MBAM reports.</span></span>
3. <span data-ttu-id="05067-113">Serveurs Web Internet Information Services (IIS): serveur qui héberge les applications Web MBAM et services MBAM.</span><span class="sxs-lookup"><span data-stu-id="05067-113">Internet Information Services (IIS) web servers: Server that hosts MBAM Web Applications and MBAM services.</span></span>
4. <span data-ttu-id="05067-114">Facultatif Serveur de site principal Microsoft System Center Configuration Manager: l’application de configuration MBAM est exécutée sur ce serveur pour intégrer les rapports MBAM avec Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="05067-114">(Optional) Microsoft System Center Configuration Manager primary site server: The MBAM configuration application is run on this server to integrate MBAM reports with Configuration Manager.</span></span> <span data-ttu-id="05067-115">Ces rapports sont ensuite fusionnés avec des rapports Configuration Manager existants dans l’instance de configuration de SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="05067-115">These reports are then merged with existing Configuration Manager reports on the Configuration Manager SQL Server Reporting Services (SSRS) instance.</span></span>

### <span data-ttu-id="05067-116">Identifier les comptes de service, les groupes, le nom du serveur et l’URL des rapports</span><span class="sxs-lookup"><span data-stu-id="05067-116">Identify service accounts, groups, server name, and reports URL</span></span>

1. <span data-ttu-id="05067-117">Identifiez le compte de service de pool d’applications MBAM utilisé par les serveurs Web IIS pour lire et écrire des données dans des bases de données MBAM.</span><span class="sxs-lookup"><span data-stu-id="05067-117">Identify the MBAM application pool service account that's used by IIS web servers to read and write data to MBAM databases.</span></span>
2. <span data-ttu-id="05067-118">Identifiez les groupes qui sont utilisés dans le cadre de la configuration des fonctionnalités Web MBAM et l’URL du service Web de rapports.</span><span class="sxs-lookup"><span data-stu-id="05067-118">Identify the groups that are used during the MBAM web features configuration and the reports web service URL.</span></span>
3. <span data-ttu-id="05067-119">Identifiez le nom du serveur SQL et le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="05067-119">Identify the SQL Server name and instance name.</span></span> <span data-ttu-id="05067-120">Regardez cette vidéo pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="05067-120">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. <span data-ttu-id="05067-121">Identifiez le compte SQL Server Reporting Services utilisé pour lire les données de conformité de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="05067-121">Identify the SQL Server Reporting Services Account that's used for reading compliance data from the Compliance and Audit database.</span></span> <span data-ttu-id="05067-122">Regardez cette vidéo pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="05067-122">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## <span data-ttu-id="05067-123">Mettez à niveau l’infrastructure MBAM vers la dernière version disponible.</span><span class="sxs-lookup"><span data-stu-id="05067-123">Upgrade the MBAM infrastructure to the latest version available</span></span>

<span data-ttu-id="05067-124">MBAM ou la mise à niveau de l’infrastructure du serveur est toujours effectuée dans l’ordre indiqué ci-dessous:</span><span class="sxs-lookup"><span data-stu-id="05067-124">MBAM Server infrastructure installation or upgrade is always performed in the order listed below:</span></span>

- <span data-ttu-id="05067-125">Moteur de base de données SQL Server: bases de données</span><span class="sxs-lookup"><span data-stu-id="05067-125">SQL Server Database Engine: Databases</span></span>
- <span data-ttu-id="05067-126">SQL Server Reporting Services: rapports</span><span class="sxs-lookup"><span data-stu-id="05067-126">SQL Server Reporting Services: Reports</span></span>
- <span data-ttu-id="05067-127">Serveur Web: applications Web</span><span class="sxs-lookup"><span data-stu-id="05067-127">Web Server: Web Applications</span></span>
- <span data-ttu-id="05067-128">Serveur SCCM: rapports intégrés SCCM, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="05067-128">SCCM Server: SCCM Integrated Reports if applicable</span></span>
- <span data-ttu-id="05067-129">Clients: mise à jour de l’agent ou du client MBAM</span><span class="sxs-lookup"><span data-stu-id="05067-129">Clients: MBAM Agent or Client Update</span></span>
- <span data-ttu-id="05067-130">Modèles de stratégie de groupe: mettez à jour la stratégie de groupe existante avec de nouveaux modèles et activez les nouveaux paramètres sur une stratégie de groupe MBAM existante.</span><span class="sxs-lookup"><span data-stu-id="05067-130">Group Policy Templates: Update the existing Group Policy with new templates and enable new settings on existing MBAM Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="05067-131">Nous vous recommandons de créer une sauvegarde de base de données complète des bases de données MBAM avant d’exécuter les mises à niveau.</span><span class="sxs-lookup"><span data-stu-id="05067-131">We recommend that you create a full database backup of the MBAM databases before you run the upgrades.</span></span>

### <span data-ttu-id="05067-132">Mettre à niveau MBAM SQL Server</span><span class="sxs-lookup"><span data-stu-id="05067-132">Upgrade the MBAM SQL Server</span></span>

<span data-ttu-id="05067-133">Regardez cette vidéo pour découvrir comment mettre à niveau le serveur SQL MBAM:</span><span class="sxs-lookup"><span data-stu-id="05067-133">Watch this video to learn how to upgrade the MBAM SQL Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### <span data-ttu-id="05067-134">Mettre à niveau le serveur Web MBAM</span><span class="sxs-lookup"><span data-stu-id="05067-134">Upgrade the MBAM Web Server</span></span>

<span data-ttu-id="05067-135">Regardez cette vidéo pour découvrir comment mettre à niveau le serveur Web MBAM:</span><span class="sxs-lookup"><span data-stu-id="05067-135">Watch this video to learn how to upgrade the MBAM Web Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## <span data-ttu-id="05067-136">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="05067-136">More information</span></span>

<span data-ttu-id="05067-137">Pour plus d’informations sur les problèmes connus dans MBAM 2,5 SP1, voir [notes de publication pour MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span><span class="sxs-lookup"><span data-stu-id="05067-137">For more information about known issues in MBAM 2.5 SP1, see [Release Notes for MBAM 2.5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span></span>

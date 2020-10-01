---
title: Mise à niveau de MBAM2.5 vers MBAM2.5SP1
description: Mise à niveau de MBAM2.5 vers MBAM2.5SP1
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 330ded822dd9da96a1c33eabcb31d744044dc28e
ms.sourcegitcommit: ae34c5cb5e7979b472b257a4691142e493d5d6fe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2020
ms.locfileid: "11091619"
---
# <span data-ttu-id="35c32-103">Mise à niveau de MBAM2.5 vers MBAM2.5SP1</span><span class="sxs-lookup"><span data-stu-id="35c32-103">Upgrading to MBAM 2.5 SP1 from MBAM 2.5</span></span>
<span data-ttu-id="35c32-104">Cette rubrique décrit la procédure de mise à niveau du client d’administration et de surveillance Microsoft BitLocker (MBAM) Server 2,5 et du client MBAM 2,5 vers MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="35c32-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 and the MBAM Client from 2.5 to MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="35c32-105">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="35c32-105">Before you begin</span></span>
#### <span data-ttu-id="35c32-106">Télécharger la version de service de 2019</span><span class="sxs-lookup"><span data-stu-id="35c32-106">Download the May 2019 servicing release</span></span>
[<span data-ttu-id="35c32-107">Pack d’optimisation de bureau</span><span class="sxs-lookup"><span data-stu-id="35c32-107">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=58345)

#### <span data-ttu-id="35c32-108">Télécharger la version de maintenance 2018 de juillet</span><span class="sxs-lookup"><span data-stu-id="35c32-108">Download the July 2018 servicing release</span></span>
[<span data-ttu-id="35c32-109">Pack d’optimisation de bureau</span><span class="sxs-lookup"><span data-stu-id="35c32-109">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)


#### <span data-ttu-id="35c32-110">Vérification de l’installation de documentaion</span><span class="sxs-lookup"><span data-stu-id="35c32-110">Verify the installation documentaion</span></span>
<span data-ttu-id="35c32-111">Vérifiez que vous disposez d’une documentation actuelle sur votre environnement MBAM, y compris tous les noms des serveurs, les noms de base de données, les comptes de service et leurs mots de passe.</span><span class="sxs-lookup"><span data-stu-id="35c32-111">Verify you have a current documentation of your MBAM environment, including all server names, database names, service accounts and their passwords.</span></span>

### <span data-ttu-id="35c32-112">Étapes de mise à niveau</span><span class="sxs-lookup"><span data-stu-id="35c32-112">Upgrade steps</span></span>
#### <span data-ttu-id="35c32-113">Procédure de mise à niveau de la base de données MBAM (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="35c32-113">Steps to upgrade the MBAM Database (SQL Server)</span></span>
1. <span data-ttu-id="35c32-114">À l’aide du configurateur MBAM; Supprimez le rôle rapports sur le serveur SQL Server, ou à partir de l’emplacement de la base de données SSRS.</span><span class="sxs-lookup"><span data-stu-id="35c32-114">Using the MBAM Configurator; remove the Reports role from the SQL server, or wherever the SSRS database is hosted.</span></span> <span data-ttu-id="35c32-115">En fonction de votre environnement, il peut s’agir du même serveur ou d’un autre serveur.</span><span class="sxs-lookup"><span data-stu-id="35c32-115">Depending on your environment, this can be the same server or a separate one.</span></span>
  > [!NOTE]
  > <span data-ttu-id="35c32-116">Vous ne verrez pas les options de suppression des bases de données. C’est attendu.</span><span class="sxs-lookup"><span data-stu-id="35c32-116">You will not see an option to remove the Databases; this is expected.</span></span>  
2. <span data-ttu-id="35c32-117">Installez 2,5 SP1 (qui se trouve avec MDOP-Microsoft Desktop Optimization Pack 2015 à partir du site Centre de gestion de licences en volume:</span><span class="sxs-lookup"><span data-stu-id="35c32-117">Install 2.5 SP1(Located with MDOP - Microsoft Desktop Optimization Pack 2015 from the Volume Licensing Service Center site:</span></span>  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. <span data-ttu-id="35c32-118">Ne pas configurer pour le moment</span><span class="sxs-lookup"><span data-stu-id="35c32-118">Do not configure it at this time</span></span> 
4. <span data-ttu-id="35c32-119">À l’aide du configurateur MBAM; rajouter le rôle de rapport</span><span class="sxs-lookup"><span data-stu-id="35c32-119">Using the MBAM Configurator; re-add the Reports role</span></span>
5. <span data-ttu-id="35c32-120">À l’aide du configurateur MBAM; rajouter le rôle de base de données SQL sur le serveur SQL Server</span><span class="sxs-lookup"><span data-stu-id="35c32-120">Using the MBAM Configurator; re-add the SQL Database role on the SQL Server</span></span>
6. <span data-ttu-id="35c32-121">À la fin, vous recevez un avertissement indiquant que la BD existe déjà et qu’elle n’a pas été créée, mais cela est attendu.</span><span class="sxs-lookup"><span data-stu-id="35c32-121">At the end, you will be warned that the DBs already exist and  weren’t created, but this is expected</span></span>
7. <span data-ttu-id="35c32-122">Ce processus met à jour les bases de données existantes vers la version actuelle installée.</span><span class="sxs-lookup"><span data-stu-id="35c32-122">This process updates the existing databases to the current version being installed.</span></span>              

#### <span data-ttu-id="35c32-123">Procédure de mise à niveau du serveur MBAM (exécutant MBAM et IIS)</span><span class="sxs-lookup"><span data-stu-id="35c32-123">Steps to upgrade the MBAM Server (Running MBAM and IIS)</span></span>
1. <span data-ttu-id="35c32-124">À l’aide du configurateur MBAM; supprimer les portails d’administration et d’auto-service du serveur IIS</span><span class="sxs-lookup"><span data-stu-id="35c32-124">Using the MBAM Configurator; remove the Admin and Self Service Portals from  the IIS server</span></span>
2. <span data-ttu-id="35c32-125">Installer MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="35c32-125">Install MBAM 2.5 SP1</span></span>
3. <span data-ttu-id="35c32-126">Ne pas configurer pour le moment</span><span class="sxs-lookup"><span data-stu-id="35c32-126">Do not configure it at this time</span></span>  
4. <span data-ttu-id="35c32-127">À l’aide du configurateur MBAM; rajouter les portails d’administrateur et libre-service au serveur IIS</span><span class="sxs-lookup"><span data-stu-id="35c32-127">Using the MBAM Configurator; re-add the Admin and Self Service Portals to the IIS server</span></span> 
5. <span data-ttu-id="35c32-128">Ouvrez une invite de commandes avec élévation de privilèges, tapez **IISReset**, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="35c32-128">Open an elevated command prompt, type **IISRESET**, and hit Enter.</span></span>
 
#### <span data-ttu-id="35c32-129">Procédure de mise à niveau des clients/points de terminaison MBAM</span><span class="sxs-lookup"><span data-stu-id="35c32-129">Steps to upgrade the MBAM Clients/Endpoints</span></span>
1. <span data-ttu-id="35c32-130">Désinstaller l’agent 2,5 des points de terminaison client</span><span class="sxs-lookup"><span data-stu-id="35c32-130">Uninstall the 2.5 Agent from client endpoints</span></span>
2. <span data-ttu-id="35c32-131">Installer l’agent 2,5 SP1 sur les points de terminaison client</span><span class="sxs-lookup"><span data-stu-id="35c32-131">Install the 2.5 SP1 Agent on the client endpoints</span></span>
3. <span data-ttu-id="35c32-132">Faire basculer la mise à jour du client de la 2019 ROLLUP pour les clients exécutant l’agent 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="35c32-132">Push out the May 2019 Rollup Client update to clients running the 2.5 SP1 Agent</span></span> 
4. <span data-ttu-id="35c32-133">Il n’est pas nécessaire de désinstaller le client existant avant de procéder à l’installation du 2019 ROLLUP.</span><span class="sxs-lookup"><span data-stu-id="35c32-133">There is no need to uninstall the existing client prior to installing the May 2019 Rollup.</span></span>  

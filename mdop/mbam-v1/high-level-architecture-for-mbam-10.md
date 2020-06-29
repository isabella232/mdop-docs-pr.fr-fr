---
title: Architecture de haut niveau pour MBAM1.0
description: Architecture de haut niveau pour MBAM1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811034"
---
# <span data-ttu-id="33979-103">Architecture de haut niveau pour MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="33979-103">High Level Architecture for MBAM 1.0</span></span>


<span data-ttu-id="33979-104">Le programme d’administration et de surveillance de BitLocker Microsoft (MBAM) est une solution de chiffrement de données client/serveur qui vous permet de simplifier la mise en service et le déploiement de BitLocker, d’améliorer la conformité et la création de rapports de BitLocker et de réduire les coûts de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="33979-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server data encryption solution that can help you simplify BitLocker provisioning and deployment, improve BitLocker compliance and reporting, and reduce support costs.</span></span> <span data-ttu-id="33979-105">MBAM inclut les fonctionnalités décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="33979-105">MBAM includes the features that are described in this topic.</span></span>

<span data-ttu-id="33979-106">De plus, il existe une vidéo qui offre une vue d’ensemble de l’architecture MBAM et de la configuration MBAM.</span><span class="sxs-lookup"><span data-stu-id="33979-106">Additionally, there is a video that provides an overview of the MBAM architecture and MBAM Setup.</span></span> <span data-ttu-id="33979-107">Pour plus d’informations, voir [vue d’ensemble de l’architecture et du déploiement MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span><span class="sxs-lookup"><span data-stu-id="33979-107">For more information, see [MBAM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span></span>

## <span data-ttu-id="33979-108">Présentation de l’architecture</span><span class="sxs-lookup"><span data-stu-id="33979-108">Architecture Overview</span></span>


<span data-ttu-id="33979-109">Le diagramme suivant illustre l’architecture MBAM.</span><span class="sxs-lookup"><span data-stu-id="33979-109">The following diagram displays the MBAM architecture.</span></span> <span data-ttu-id="33979-110">La topologie de déploiement MBAM à serveur unique est proposée pour présenter les fonctionnalités MBAM.</span><span class="sxs-lookup"><span data-stu-id="33979-110">The single-server MBAM deployment topology is shown to introduce the MBAM features.</span></span> <span data-ttu-id="33979-111">Toutefois, cette topologie de déploiement MBAM est recommandée uniquement dans les environnements de laboratoire.</span><span class="sxs-lookup"><span data-stu-id="33979-111">However, this MBAM deployment topology is recommended only for lab environments.</span></span>

<span data-ttu-id="33979-112">**Remarques**  Au moins une topologie de déploiement MBAM à trois ordinateurs est recommandée pour un déploiement en production.</span><span class="sxs-lookup"><span data-stu-id="33979-112">**Note** At least a three-computer MBAM deployment topology is recommended for a production deployment.</span></span> <span data-ttu-id="33979-113">Pour plus d’informations sur les topologies de déploiement MBAM, voir [déploiement de l’infrastructure de serveur 1,0 MBAM](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="33979-113">For more information about MBAM deployment topologies, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

![topologie de déploiement de serveur unique MBAM](images/mbam-1-server.jpg)

1.  <span data-ttu-id="33979-115">**Serveur d’administration et de surveillance**.</span><span class="sxs-lookup"><span data-stu-id="33979-115">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="33979-116">Le serveur d’administration et de surveillance MBAM est installé sur un serveur Windows et héberge le site Web d’administration et de gestion MBAM, ainsi que les services Web d’analyse.</span><span class="sxs-lookup"><span data-stu-id="33979-116">The MBAM Administration and Monitoring Server is installed on a Windows server and hosts the MBAM Administration and Management website and the monitoring web services.</span></span> <span data-ttu-id="33979-117">Le site Web d’administration et de gestion d’MBAM est utilisé pour déterminer l’état de la conformité d’entreprise, pour vérifier l’activité, pour gérer les fonctionnalités matérielles et pour accéder aux données de récupération, telles que les clés de récupération BitLocker.</span><span class="sxs-lookup"><span data-stu-id="33979-117">The MBAM Administration and Management website is used to determine enterprise compliance status, to audit activity, to manage hardware capability, and to access recovery data, such as the BitLocker recovery keys.</span></span> <span data-ttu-id="33979-118">Le serveur d’administration et de surveillance se connecte aux bases de données et services suivants:</span><span class="sxs-lookup"><span data-stu-id="33979-118">The Administration and Monitoring Server connects to the following databases and services:</span></span>

    -   <span data-ttu-id="33979-119">Restauration et base de données matérielle.</span><span class="sxs-lookup"><span data-stu-id="33979-119">Recovery and Hardware Database.</span></span> <span data-ttu-id="33979-120">La base de données de récupération et de matériel est installée sur un serveur Windows et sur une instance SQLServer prise en charge.</span><span class="sxs-lookup"><span data-stu-id="33979-120">The Recovery and Hardware database is installed on a Windows-based server and supported SQLServer instance.</span></span> <span data-ttu-id="33979-121">Cette base de données stocke les données de récupération et les informations matérielles collectées à partir des ordinateurs clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="33979-121">This database stores recovery data and hardware information that is collected from MBAM client computers.</span></span>

    -   <span data-ttu-id="33979-122">Base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="33979-122">Compliance and Audit Database.</span></span> <span data-ttu-id="33979-123">La base de données d’audit et de conformité est installée sur un serveur Windows et sur une instance SQLServer prise en charge.</span><span class="sxs-lookup"><span data-stu-id="33979-123">The Compliance and Audit Database is installed on a Windows server and supported SQLServer instance.</span></span> <span data-ttu-id="33979-124">Cette base de données stocke les données de conformité pour les ordinateurs clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="33979-124">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="33979-125">Ces données sont principalement utilisées pour les rapports hébergés par SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="33979-125">This data is used primarily for reports that are hosted by SQL Server Reporting Services (SSRS).</span></span>

    -   <span data-ttu-id="33979-126">Rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="33979-126">Compliance and Audit Reports.</span></span> <span data-ttu-id="33979-127">Les rapports de conformité et d’audit sont installés sur un serveur Windows et une instance SQLServer prise en charge, avec la fonctionnalité SSRS installée.</span><span class="sxs-lookup"><span data-stu-id="33979-127">The Compliance and Audit Reports are installed on a Windows-based server and supported SQLServer instance that has the SSRS feature installed.</span></span> <span data-ttu-id="33979-128">Ces rapports fournissent des rapports d’administration et de surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="33979-128">These reports provide Microsoft BitLocker Administration and Monitoring reports.</span></span> <span data-ttu-id="33979-129">Vous pouvez accéder à ces rapports à partir du site Web d’administration et de gestion de MBAM, ou directement à partir du serveur SSRS.</span><span class="sxs-lookup"><span data-stu-id="33979-129">These reports can be accessed from the MBAM Administration and Management website or directly from the SSRS Server.</span></span>

2.  <span data-ttu-id="33979-130">**Client MBAM**.</span><span class="sxs-lookup"><span data-stu-id="33979-130">**MBAM Client**.</span></span> <span data-ttu-id="33979-131">Le client d’administration et de surveillance de Microsoft BitLocker effectue les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="33979-131">The Microsoft BitLocker Administration and Monitoring Client performs the following tasks:</span></span>

    -   <span data-ttu-id="33979-132">Utilise une stratégie de groupe pour appliquer le chiffrement BitLocker d’ordinateurs clients au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="33979-132">Uses Group Policy to enforce the BitLocker encryption of client computers in the enterprise.</span></span>

    -   <span data-ttu-id="33979-133">Collecte la clé de récupération pour les trois types de lecteurs de données BitLocker: lecteurs du système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).</span><span class="sxs-lookup"><span data-stu-id="33979-133">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

    -   <span data-ttu-id="33979-134">Recueille des informations de récupération et des informations matérielles sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="33979-134">Collects recovery information and hardware information about the client computers.</span></span>

    -   <span data-ttu-id="33979-135">Collecte les données de conformité de l’ordinateur et transmet les données au système de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="33979-135">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

3.  <span data-ttu-id="33979-136">**Modèle de stratégie**.</span><span class="sxs-lookup"><span data-stu-id="33979-136">**Policy Template**.</span></span> <span data-ttu-id="33979-137">Le modèle de stratégie de groupe MBAM est installé sur un ordinateur client ou serveur Windows pris en charge.</span><span class="sxs-lookup"><span data-stu-id="33979-137">The MBAM Group Policy template is installed on a supported Windows-based server or client computer.</span></span> <span data-ttu-id="33979-138">Ce modèle permet de spécifier les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="33979-138">This template is used to specify the MBAM implementation settings for BitLocker drive encryption.</span></span>

## <span data-ttu-id="33979-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33979-139">Related topics</span></span>


[<span data-ttu-id="33979-140">Prise en main de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="33979-140">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)

 

 






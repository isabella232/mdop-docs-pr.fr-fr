---
title: Déploiement de l'infrastructure de serveur MBAM2.0
description: Déploiement de l'infrastructure de serveur MBAM2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810746"
---
# <span data-ttu-id="a3d15-103">Déploiement de l'infrastructure de serveur MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="a3d15-103">Deploying the MBAM 2.0 Server Infrastructure</span></span>


<span data-ttu-id="a3d15-104">Les fonctionnalités de serveur d’administration et de surveillance de BitLocker pour la topologie autonome peuvent être installées dans différentes configurations sur deux serveurs ou plus dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="a3d15-104">Microsoft BitLocker Administration and Monitoring (MBAM) Server features for the Stand-alone topology can be installed in different configurations on two or more servers in a production environment.</span></span> <span data-ttu-id="a3d15-105">La configuration recommandée consiste à deux serveurs pour un environnement de production, en fonction de vos besoins en matière d’évolutivité.</span><span class="sxs-lookup"><span data-stu-id="a3d15-105">The recommended configuration is two servers for a production environment, depending on your scalability requirements.</span></span> <span data-ttu-id="a3d15-106">Utilisez un serveur unique pour une installation MBAM uniquement dans les environnements de test.</span><span class="sxs-lookup"><span data-stu-id="a3d15-106">Use a single server for an MBAM installation only in test environments.</span></span> <span data-ttu-id="a3d15-107">Pour plus d’informations sur la planification du déploiement de la fonctionnalité MBAM Server, voir [planification du déploiement de MBAM 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="a3d15-107">For more information about planning for the MBAM Server feature deployment, see [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md).</span></span>

<span data-ttu-id="a3d15-108">Le diagramme suivant montre un exemple de la façon dont vous pouvez configurer le déploiement recommandé sur deux serveurs MBAM.</span><span class="sxs-lookup"><span data-stu-id="a3d15-108">The following diagram shows an example of how you can configure the recommended two-server MBAM deployment.</span></span> <span data-ttu-id="a3d15-109">Cette configuration prend en charge jusqu’à 200 000 clients MBAM dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="a3d15-109">This configuration supports up to 200,000 MBAM clients in a production environment.</span></span> <span data-ttu-id="a3d15-110">Les fonctionnalités de serveur et bases de données de l’architecture de l’architecture sont décrites dans la section suivante, qui s’affichent sur votre ordinateur ou serveur pour lequel nous vous recommandons de les installer.</span><span class="sxs-lookup"><span data-stu-id="a3d15-110">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

![MBAM 2 2-topologie de déploiement de serveur](images/mbam2-3-servers.gif)

## <span data-ttu-id="a3d15-112">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="a3d15-112">Administration and Monitoring Server</span></span>


<span data-ttu-id="a3d15-113">Les fonctionnalités suivantes sont installées sur ce serveur:</span><span class="sxs-lookup"><span data-stu-id="a3d15-113">The following features are installed on this server:</span></span>

-   <span data-ttu-id="a3d15-114">**Serveur d’administration et de surveillance**.</span><span class="sxs-lookup"><span data-stu-id="a3d15-114">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="a3d15-115">La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur Windows et se compose du site Web du support technique et des services Web de surveillance.</span><span class="sxs-lookup"><span data-stu-id="a3d15-115">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Help Desk website and the monitoring web services.</span></span>

-   <span data-ttu-id="a3d15-116">**Portail libre-service**.</span><span class="sxs-lookup"><span data-stu-id="a3d15-116">**Self-Service Portal**.</span></span> <span data-ttu-id="a3d15-117">Le portail libre-service est installé sur un serveur Windows.</span><span class="sxs-lookup"><span data-stu-id="a3d15-117">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="a3d15-118">Le portail libre-service permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web, à partir duquel ils peuvent obtenir une clé de récupération pour récupérer un volume BitLocker verrouillé.</span><span class="sxs-lookup"><span data-stu-id="a3d15-118">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="a3d15-119">Serveur de base de données</span><span class="sxs-lookup"><span data-stu-id="a3d15-119">Database Server</span></span>


<span data-ttu-id="a3d15-120">Les fonctionnalités suivantes sont installées sur ce serveur:</span><span class="sxs-lookup"><span data-stu-id="a3d15-120">The following features are installed on this server:</span></span>

-   <span data-ttu-id="a3d15-121">**Base de données de récupération**.</span><span class="sxs-lookup"><span data-stu-id="a3d15-121">**Recovery Database**.</span></span> <span data-ttu-id="a3d15-122">La base de données de récupération est installée sur un serveur Windows et sur une instance de Microsoft SQLServer qui est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a3d15-122">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="a3d15-123">Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="a3d15-123">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="a3d15-124">**Base de données d’audit et de conformité**.</span><span class="sxs-lookup"><span data-stu-id="a3d15-124">**Compliance and Audit Database**.</span></span> <span data-ttu-id="a3d15-125">La base de données d’audit et de conformité est installée sur un serveur Windows et sur une instance de SQLServer prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a3d15-125">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="a3d15-126">Cette base de données stocke les données de conformité pour les ordinateurs clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="a3d15-126">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="a3d15-127">Ces données sont principalement utilisées pour les rapports hébergés par SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="a3d15-127">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="a3d15-128">**Rapports de conformité et d’audit**.</span><span class="sxs-lookup"><span data-stu-id="a3d15-128">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="a3d15-129">Les rapports de conformité et d’audit sont installés sur un serveur Windows et une instance prise en charge de SQLServer pour lequel la fonctionnalité SQL Server Reporting Services (SSRS) est installée.</span><span class="sxs-lookup"><span data-stu-id="a3d15-129">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="a3d15-130">Ces rapports fournissent des rapports MBAM auxquels vous pouvez accéder à partir du site Web de l’assistance ou directement à partir du serveur SSRS.</span><span class="sxs-lookup"><span data-stu-id="a3d15-130">These reports provide MBAM reports that you can access from the Help Desk website or directly from the SSRS server.</span></span>

## <span data-ttu-id="a3d15-131">Station de travail de gestion</span><span class="sxs-lookup"><span data-stu-id="a3d15-131">Management Workstation</span></span>


<span data-ttu-id="a3d15-132">La fonctionnalité suivante est installée sur la station de travail de gestion, qui peut être un ordinateur Windows Server ou un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="a3d15-132">The following feature is installed on the Management Workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="a3d15-133">**Modèle de stratégie**.</span><span class="sxs-lookup"><span data-stu-id="a3d15-133">**Policy Template**.</span></span> <span data-ttu-id="a3d15-134">Le modèle de stratégie est composé de stratégies de groupe définissant les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a3d15-134">The Policy Template consists of Group Policies that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="a3d15-135">Vous pouvez installer le modèle de stratégie sur n’importe quel serveur ou station de travail, mais il est généralement installé sur une station de travail de gestion (ordinateur client ou client pris en charge).</span><span class="sxs-lookup"><span data-stu-id="a3d15-135">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="a3d15-136">La station de travail ne doit pas nécessairement être un ordinateur dédié.</span><span class="sxs-lookup"><span data-stu-id="a3d15-136">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="a3d15-137">Client MBAM</span><span class="sxs-lookup"><span data-stu-id="a3d15-137">MBAM Client</span></span>


<span data-ttu-id="a3d15-138">Le client MBAM est installé sur un ordinateur Windows et il présente les caractéristiques suivantes:</span><span class="sxs-lookup"><span data-stu-id="a3d15-138">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="a3d15-139">Utilise une stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker d’ordinateurs clients au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="a3d15-139">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="a3d15-140">Collecte la clé de récupération pour les trois types de lecteurs de données BitLocker: lecteurs du système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).</span><span class="sxs-lookup"><span data-stu-id="a3d15-140">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="a3d15-141">Collecte les données de conformité de l’ordinateur et transmet les données au système de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="a3d15-141">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="a3d15-142">Autres ressources pour le déploiement des fonctionnalités du serveur MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="a3d15-142">Other Resources for Deploying MBAM 2.0 Server Features</span></span>


[<span data-ttu-id="a3d15-143">Déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="a3d15-143">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 






---
title: Architecture de hautniveau pour MBAM2.0
description: Architecture de hautniveau pour MBAM2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810715"
---
# <span data-ttu-id="7a50f-103">Architecture de hautniveau pour MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="7a50f-103">High-Level Architecture for MBAM 2.0</span></span>


<span data-ttu-id="7a50f-104">Le programme d’administration et de surveillance de Microsoft BitLocker (MBAM) est une solution client/serveur qui vous permet de simplifier la mise en service et le déploiement de BitLocker, d’améliorer la conformité et la création de rapports sur BitLocker et de réduire les coûts de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7a50f-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server solution that can help you simplify BitLocker provisioning and deployment, improve compliance and reporting on BitLocker, and reduce support costs.</span></span> <span data-ttu-id="7a50f-105">L’administration et la surveillance de Microsoft BitLocker incluent les fonctionnalités décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7a50f-105">Microsoft BitLocker Administration and Monitoring includes the features that are described in this topic.</span></span>

<span data-ttu-id="7a50f-106">L’administration et le suivi de BitLocker peuvent être déployés dans la topologie autonome ou dans une topologie intégrée à Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012.</span><span class="sxs-lookup"><span data-stu-id="7a50f-106">Microsoft BitLocker Administration and Monitoring can be deployed in the Stand-alone topology, or in a topology that is integrated with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="7a50f-107">Cette rubrique décrit l’architecture de la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="7a50f-107">This topic describes the architecture for the Stand-alone topology.</span></span> <span data-ttu-id="7a50f-108">Pour plus d’informations sur le déploiement dans la topologie intégré de Configuration Manager, voir [utilisation de MBAM avec Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="7a50f-108">For information about deploying in the integrated Configuration Manager topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

<span data-ttu-id="7a50f-109">Le diagramme suivant illustre l’architecture recommandée de MBAM pour un environnement de production, qui comprend deux serveurs et une station de travail de gestion.</span><span class="sxs-lookup"><span data-stu-id="7a50f-109">The following diagram shows the MBAM recommended architecture for a production environment, which consists of two servers and a management workstation.</span></span> <span data-ttu-id="7a50f-110">Cette architecture prend en charge jusqu’à 200 000 clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="7a50f-110">This architecture supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="7a50f-111">Les fonctionnalités de serveur et bases de données de l’architecture de l’architecture sont décrites dans la section suivante, qui s’affichent sur votre ordinateur ou serveur pour lequel nous vous recommandons de les installer.</span><span class="sxs-lookup"><span data-stu-id="7a50f-111">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

<span data-ttu-id="7a50f-112">**Remarques**  Une architecture à serveur unique doit être utilisée uniquement dans les environnements de test.</span><span class="sxs-lookup"><span data-stu-id="7a50f-112">**Note** A single-server architecture should be used only in test environments.</span></span>

 

![MBAM 2 2-topologie de déploiement de serveur](images/mbam2-3-servers.gif)

## <span data-ttu-id="7a50f-114">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="7a50f-114">Administration and Monitoring Server</span></span>


<span data-ttu-id="7a50f-115">Les fonctionnalités suivantes sont installées sur ce serveur:</span><span class="sxs-lookup"><span data-stu-id="7a50f-115">The following features are installed on this server:</span></span>

-   <span data-ttu-id="7a50f-116">**Serveur d’administration et de surveillance**.</span><span class="sxs-lookup"><span data-stu-id="7a50f-116">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="7a50f-117">La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur Windows et se compose du site Web d’administration et de surveillance, qui inclut les rapports et le portail du support technique, ainsi que les services Web de surveillance.</span><span class="sxs-lookup"><span data-stu-id="7a50f-117">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Administration and Monitoring website, which includes the reports and the Help Desk Portal, and the monitoring web services.</span></span>

-   <span data-ttu-id="7a50f-118">**Portail libre-service**.</span><span class="sxs-lookup"><span data-stu-id="7a50f-118">**Self-Service Portal**.</span></span> <span data-ttu-id="7a50f-119">Le portail libre-service est installé sur un serveur Windows.</span><span class="sxs-lookup"><span data-stu-id="7a50f-119">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="7a50f-120">Le portail libre-service permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web, à partir duquel ils peuvent obtenir une clé de récupération pour récupérer un volume BitLocker verrouillé.</span><span class="sxs-lookup"><span data-stu-id="7a50f-120">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="7a50f-121">Serveur de base de données</span><span class="sxs-lookup"><span data-stu-id="7a50f-121">Database Server</span></span>


<span data-ttu-id="7a50f-122">Les fonctionnalités suivantes sont installées sur ce serveur:</span><span class="sxs-lookup"><span data-stu-id="7a50f-122">The following features are installed on this server:</span></span>

-   <span data-ttu-id="7a50f-123">**Base de données de récupération**.</span><span class="sxs-lookup"><span data-stu-id="7a50f-123">**Recovery Database**.</span></span> <span data-ttu-id="7a50f-124">La base de données de récupération est installée sur un serveur Windows et sur une instance de Microsoft SQLServer qui est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7a50f-124">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="7a50f-125">Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="7a50f-125">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="7a50f-126">**Base de données d’audit et de conformité**.</span><span class="sxs-lookup"><span data-stu-id="7a50f-126">**Compliance and Audit Database**.</span></span> <span data-ttu-id="7a50f-127">La base de données d’audit et de conformité est installée sur un serveur Windows et sur une instance de SQLServer prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7a50f-127">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="7a50f-128">Cette base de données stocke les données de conformité pour les ordinateurs clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="7a50f-128">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="7a50f-129">Ces données sont principalement utilisées pour les rapports hébergés par SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="7a50f-129">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="7a50f-130">**Rapports de conformité et d’audit**.</span><span class="sxs-lookup"><span data-stu-id="7a50f-130">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="7a50f-131">Les rapports de conformité et d’audit sont installés sur un serveur Windows et une instance prise en charge de SQLServer pour lequel la fonctionnalité SQL Server Reporting Services (SSRS) est installée.</span><span class="sxs-lookup"><span data-stu-id="7a50f-131">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="7a50f-132">Ces rapports fournissent des rapports MBAM auxquels vous pouvez accéder à partir du site Web d’administration et de surveillance ou directement à partir du serveur SSRS.</span><span class="sxs-lookup"><span data-stu-id="7a50f-132">These reports provide MBAM reports that you can access from the Administration and Monitoring website or directly from the SSRS server.</span></span>

## <span data-ttu-id="7a50f-133">Station de travail de gestion</span><span class="sxs-lookup"><span data-stu-id="7a50f-133">Management Workstation</span></span>


<span data-ttu-id="7a50f-134">La fonctionnalité suivante est installée sur la station de travail de gestion, qui peut être un ordinateur Windows Server ou un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="7a50f-134">The following feature is installed on the Management workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="7a50f-135">**Modèle de stratégie**.</span><span class="sxs-lookup"><span data-stu-id="7a50f-135">**Policy Template**.</span></span> <span data-ttu-id="7a50f-136">Le modèle de stratégie est composé de paramètres de stratégie de groupe définissant les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7a50f-136">The Policy Template consists of Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="7a50f-137">Vous pouvez installer le modèle de stratégie sur n’importe quel serveur ou station de travail, mais il est généralement installé sur une station de travail de gestion (ordinateur client ou client pris en charge).</span><span class="sxs-lookup"><span data-stu-id="7a50f-137">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="7a50f-138">La station de travail ne doit pas nécessairement être un ordinateur dédié.</span><span class="sxs-lookup"><span data-stu-id="7a50f-138">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="7a50f-139">Client MBAM</span><span class="sxs-lookup"><span data-stu-id="7a50f-139">MBAM Client</span></span>


<span data-ttu-id="7a50f-140">Le client MBAM est installé sur un ordinateur Windows et il présente les caractéristiques suivantes:</span><span class="sxs-lookup"><span data-stu-id="7a50f-140">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="7a50f-141">Utilise une stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker d’ordinateurs clients au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7a50f-141">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="7a50f-142">Collecte la clé de récupération pour les trois types de lecteurs de données BitLocker: lecteurs du système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).</span><span class="sxs-lookup"><span data-stu-id="7a50f-142">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="7a50f-143">Collecte les données de conformité de l’ordinateur et transmet les données au système de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="7a50f-143">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="7a50f-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a50f-144">Related topics</span></span>


[<span data-ttu-id="7a50f-145">Prise en main de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="7a50f-145">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 






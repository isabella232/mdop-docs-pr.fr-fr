---
title: Utilisation de serveurs Application Virtualization Server comme solution de gestion des packages
description: Utilisation de serveurs Application Virtualization Server comme solution de gestion des packages
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806181"
---
# <span data-ttu-id="a09b7-103">Utilisation de serveurs Application Virtualization Server comme solution de gestion des packages</span><span class="sxs-lookup"><span data-stu-id="a09b7-103">Using Application Virtualization Servers as a Package Management Solution</span></span>


<span data-ttu-id="a09b7-104">Si vous ne disposez pas d’un système de gestion des opérations de déploiement de votre application, ou si vous ne souhaitez pas en utiliser un, vous devez installer un ou plusieurs serveurs de gestion de la virtualisation des applications en tant que cœur de votre architecture système.</span><span class="sxs-lookup"><span data-stu-id="a09b7-104">If you do not have an existing ESD system to deploy your Application Virtualization solution or do not wish to use one, you will need to install one or more Application Virtualization Management Servers as the core of your system architecture.</span></span> <span data-ttu-id="a09b7-105">Le serveur de gestion de la virtualisation des applications nécessite un ordinateur serveur dédié et a besoin d’une base de données Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a09b7-105">The Application Virtualization Management Server requires a dedicated server computer and needs a Microsoft SQL Server database.</span></span> <span data-ttu-id="a09b7-106">La base de données peut se trouver sur le même serveur ou être configurée sur un serveur de base de données d’entreprise accessible par le serveur de gestion de la virtualisation des applications par le biais d’une connexion réseau haut débit.</span><span class="sxs-lookup"><span data-stu-id="a09b7-106">The database can be on the same server, or it can be configured on a corporate database server that is accessible to the Application Virtualization Management Server over a high-speed LAN connection.</span></span> <span data-ttu-id="a09b7-107">Par ailleurs, vous devez installer la console de gestion des applications Microsoft application, sur le serveur de gestion de la virtualisation des applications ou sur une station de travail de gestion désignée, et vous devrez installer le service Web Microsoft Application Virtualization Management, qui peut également être installé sur le serveur de gestion des applications virtuelles ou sur un serveur IIS distinct.</span><span class="sxs-lookup"><span data-stu-id="a09b7-107">In addition, you will need to install the Microsoft Application Virtualization Management Console, on either the Application Virtualization Management Server or on a designated management workstation, and you will need to install the Microsoft Application Virtualization Management Web Service, which can also be installed on the Application Virtualization Management Server or on a separate IIS server.</span></span> <span data-ttu-id="a09b7-108">La console de gestion de l’application virtualisation est utilisée pour la connexion au service Web de gestion des applications, permettant ainsi à l’administrateur système d’interagir avec le serveur de gestion de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="a09b7-108">The Application Virtualization Management Console is used to connect to the Application Virtualization Management Web Service, enabling the system administrator to interact with the Application Virtualization Management Server.</span></span>

<span data-ttu-id="a09b7-109">**Remarques**  L’accès aux applications est contrôlé par le biais des groupes de sécurité dans les services de domaine Active Directory (AD FS), vous devez donc planifier un processus de configuration d’un groupe de sécurité pour chaque application virtualisée et de gestion des utilisateurs ajoutés à chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="a09b7-109">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process to set up a security group for each virtualized application and for managing which users are added to each group.</span></span> <span data-ttu-id="a09b7-110">L’administrateur du serveur de gestion des applications configure le serveur pour utiliser ces groupes Active Directory et le serveur contrôle automatiquement l’accès aux packages en fonction de l’appartenance aux groupes Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a09b7-110">The Application Virtualization Management Server administrator configures the server to use these Active Directory groups, and the server then automatically controls access to the packages based on Active Directory group membership.</span></span>

 

## <span data-ttu-id="a09b7-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a09b7-111">In This Section</span></span>


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[<span data-ttu-id="a09b7-112">Présentation des composants du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="a09b7-112">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)  
<span data-ttu-id="a09b7-113">Répertorie et décrit les principaux composants du système de gestion de Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="a09b7-113">Lists and describes the primary components of the Microsoft Application Virtualization Management System.</span></span>

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[<span data-ttu-id="a09b7-114">Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="a09b7-114">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
<span data-ttu-id="a09b7-115">Fournit une vue d’ensemble de la façon dont les applications virtuelles sont publiées dans un scénario de déploiement basé sur un serveur de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="a09b7-115">Provides a brief overview of how virtual applications are published in an Application Virtualization Server-based deployment scenario.</span></span>

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[<span data-ttu-id="a09b7-116">Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="a09b7-116">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
<span data-ttu-id="a09b7-117">Décrit les options disponibles pour l’utilisation des serveurs de diffusion en continu d’applications en conjonction avec votre implémentation basée sur le serveur de gestion de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="a09b7-117">Describes available options for using Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation.</span></span>

## <span data-ttu-id="a09b7-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a09b7-118">Related topics</span></span>


[<span data-ttu-id="a09b7-119">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="a09b7-119">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="a09b7-120">Planification du déploiement du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="a09b7-120">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 






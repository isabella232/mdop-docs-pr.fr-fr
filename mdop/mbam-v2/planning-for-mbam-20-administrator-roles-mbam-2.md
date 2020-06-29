---
title: Planification des rôles administrateur de MBAM2.0
description: Planification des rôles administrateur de MBAM2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810829"
---
# <span data-ttu-id="b8ffe-103">Planification des rôles administrateur de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="b8ffe-103">Planning for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="b8ffe-104">Cette rubrique répertorie et décrit les rôles d’administrateur disponibles dans le cadre de l’administration et de la surveillance de BitLocker (MBAM), ainsi que les emplacements serveur où sont créés les groupes locaux.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-104">This topic lists and describes the available administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM) as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="b8ffe-105">Rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="b8ffe-105">MBAM Administrator Roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="b8ffe-106">Administrateurs système MBAM</span><span class="sxs-lookup"><span data-stu-id="b8ffe-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="b8ffe-107">Les administrateurs de ce rôle ont accès à toutes les fonctionnalités d’administration et de contrôle de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-107">Administrators in this role have access to all Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="b8ffe-108">Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="b8ffe-109">Utilisateurs du support technique MBAM</span><span class="sxs-lookup"><span data-stu-id="b8ffe-109">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="b8ffe-110">Les administrateurs de ce rôle ont accès aux fonctionnalités du support technique de MBAM.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-110">Administrators in this role have access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="b8ffe-111">Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-report-users"></a> **<span data-ttu-id="b8ffe-112">Utilisateurs de rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="b8ffe-112">MBAM Report Users</span></span>**  
<span data-ttu-id="b8ffe-113">Les administrateurs de ce rôle ont accès aux rapports de conformité et d’audit de MBAM.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-113">Administrators in this role have access to the Compliance and Audit Reports from MBAM.</span></span> <span data-ttu-id="b8ffe-114">Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance, la base de données d’audit et de conformité, ainsi que sur le serveur qui héberge les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-114">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **<span data-ttu-id="b8ffe-115">Utilisateurs du support technique avancée MBAM</span><span class="sxs-lookup"><span data-stu-id="b8ffe-115">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="b8ffe-116">Les administrateurs de ce rôle ont accès aux fonctionnalités du support technique de MBAM.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-116">Administrators in this role have increased access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="b8ffe-117">Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-117">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="b8ffe-118">Si un utilisateur est membre des utilisateurs du support technique MBAM et des utilisateurs du support technique avancé MBAM, les autorisations de l’utilisateur du support technique avancé MBAM remplacent les autorisations des utilisateurs du support technique MBAM.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-118">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will override the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="b8ffe-119">**Important**  Pour afficher les rapports, un utilisateur administratif doit être membre du groupe de sécurité des **utilisateurs du rapport MBAM** sur la fonctionnalité d’administration et de surveillance du serveur, de la conformité et de la base de données d’audit, et sur le serveur qui héberge la fonctionnalité de rapport d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-119">**Important** To view reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports feature.</span></span> <span data-ttu-id="b8ffe-120">Il est recommandé de créer un groupe de sécurité dans les services de domaine Active Directory (AD FS) avec des droits sur le groupe de sécurité des **utilisateurs de rapports MBAM** locaux sur le serveur d’administration et de surveillance et sur le serveur qui héberge les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="b8ffe-120">As a best practice, create a security group in Active Directory Domain Services with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and the server that hosts the Compliance and Audit Reports.</span></span>

 

## <span data-ttu-id="b8ffe-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8ffe-121">Related topics</span></span>


[<span data-ttu-id="b8ffe-122">Préparation de votre environnement pour MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="b8ffe-122">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 






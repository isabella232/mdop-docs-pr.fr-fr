---
title: Planification des rôles administrateur de MBAM1.0
description: Planification des rôles administrateur de MBAM1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811424"
---
# <span data-ttu-id="62b06-103">Planification des rôles administrateur de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="62b06-103">Planning for MBAM 1.0 Administrator Roles</span></span>


<span data-ttu-id="62b06-104">Cette rubrique inclut et décrit les rôles d’administrateur disponibles dans le cadre de la gestion et de l’analyse de BitLocker (MBAM), ainsi que les emplacements serveur où les groupes locaux sont créés.</span><span class="sxs-lookup"><span data-stu-id="62b06-104">This topic includes and describes the administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM), as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="62b06-105">Rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="62b06-105">MBAM Administrator roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="62b06-106">Administrateurs système MBAM</span><span class="sxs-lookup"><span data-stu-id="62b06-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="62b06-107">Les administrateurs de ce rôle ont accès à toutes les fonctionnalités de MBAM.</span><span class="sxs-lookup"><span data-stu-id="62b06-107">Administrators in this role have access to all MBAM features.</span></span> <span data-ttu-id="62b06-108">Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="62b06-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-hardware-users"></a> **<span data-ttu-id="62b06-109">Utilisateurs de matériel MBAM</span><span class="sxs-lookup"><span data-stu-id="62b06-109">MBAM Hardware Users</span></span>**  
<span data-ttu-id="62b06-110">Les administrateurs de ce rôle ont accès aux fonctionnalités de fonctionnalités matérielles de MBAM.</span><span class="sxs-lookup"><span data-stu-id="62b06-110">Administrators in this role have access to the Hardware Capability features from MBAM.</span></span> <span data-ttu-id="62b06-111">Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="62b06-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="62b06-112">Utilisateurs du support technique MBAM</span><span class="sxs-lookup"><span data-stu-id="62b06-112">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="62b06-113">Les administrateurs de ce rôle ont accès aux fonctionnalités de support technique de MBAM.</span><span class="sxs-lookup"><span data-stu-id="62b06-113">Administrators in this role have access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="62b06-114">Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="62b06-114">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam--report-users"></a> **<span data-ttu-id="62b06-115">Utilisateurs de rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="62b06-115">MBAM Report Users</span></span>**  
<span data-ttu-id="62b06-116">Les administrateurs de ce rôle ont accès à la fonction rapports de conformité et d’audit à partir de MBAM.</span><span class="sxs-lookup"><span data-stu-id="62b06-116">Administrators in this role have access to the Compliance and Audit Reports feature from MBAM.</span></span> <span data-ttu-id="62b06-117">Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance, la base de données d’audit et de conformité, ainsi que sur le serveur qui héberge les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="62b06-117">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **<span data-ttu-id="62b06-118">Utilisateurs du support technique avancée MBAM</span><span class="sxs-lookup"><span data-stu-id="62b06-118">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="62b06-119">Les administrateurs de ce rôle ont accès aux fonctionnalités de support technique de MBAM.</span><span class="sxs-lookup"><span data-stu-id="62b06-119">Administrators in this role have increased access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="62b06-120">Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="62b06-120">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="62b06-121">Si un utilisateur est membre des utilisateurs du support technique MBAM et des utilisateurs du support technique avancé MBAM, les autorisations de l’utilisateur du support technique MBAM MBAM seront remplacées par les autorisations des utilisateurs du support technique.</span><span class="sxs-lookup"><span data-stu-id="62b06-121">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will overwrite the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="62b06-122">**Important**  Pour afficher les rapports, un utilisateur administratif doit être membre du groupe de sécurité des **utilisateurs du rapport MBAM** sur le serveur d’administration et de surveillance, de la base de données d’audit et de conformité, ainsi que du serveur hébergeant la fonctionnalité de conformité et de rapports.</span><span class="sxs-lookup"><span data-stu-id="62b06-122">**Important** To view the reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Reports feature.</span></span> <span data-ttu-id="62b06-123">Il est recommandé de créer un groupe de sécurité dans Active Directory grâce aux droits du groupe de sécurité des **utilisateurs du rapport MBAM** local à la fois sur le serveur d’administration et de surveillance et sur le serveur qui héberge la conformité et les rapports.</span><span class="sxs-lookup"><span data-stu-id="62b06-123">As a best practice, create a security group in Active Directory with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and on the server that hosts the Compliance and Reports.</span></span>

 

## <span data-ttu-id="62b06-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62b06-124">Related topics</span></span>


[<span data-ttu-id="62b06-125">Préparation de votre environnement pour MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="62b06-125">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)

 

 






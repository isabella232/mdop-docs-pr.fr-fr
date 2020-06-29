---
title: Gérer des rôles d'administrateur MBAM
description: Gérer des rôles d'administrateur MBAM
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804626"
---
# <span data-ttu-id="eff70-103">Gérer des rôles d'administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="eff70-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="eff70-104">Une fois l’installation de Microsoft BitLocker administration et surveillance (MBAM) terminée pour toutes les fonctionnalités du serveur, les utilisateurs administratifs doivent avoir accès à ces fonctionnalités serveur.</span><span class="sxs-lookup"><span data-stu-id="eff70-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="eff70-105">Il est recommandé que les administrateurs qui gèrent ou utilisent les fonctionnalités du serveur MBAM doivent être assignés aux groupes de sécurité Active Directory, puis ces groupes doivent être ajoutés au groupe local administratif approprié MBAM.</span><span class="sxs-lookup"><span data-stu-id="eff70-105">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="eff70-106">Pour gérer les appartenances aux rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="eff70-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="eff70-107">Affectez des utilisateurs administratifs à des groupes de sécurité dans ActiveDirectoryDomain services.</span><span class="sxs-lookup"><span data-stu-id="eff70-107">Assign administrative users to security groups in ActiveDirectoryDomain Services.</span></span>

2.  <span data-ttu-id="eff70-108">Ajoutez des groupes de sécurité ActiveDirectoryDomain services aux rôles pour les groupes locaux d’administration de MBAM sur le serveur d’administration et de surveillance Microsoft BitLocker pour les fonctionnalités correspondantes.</span><span class="sxs-lookup"><span data-stu-id="eff70-108">Add ActiveDirectoryDomain Services security groups to the roles for MBAM administrative local groups on the Microsoft BitLocker Administration and Monitoring server for the respective features.</span></span> <span data-ttu-id="eff70-109">Les rôles d’utilisateur sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="eff70-109">The user roles are as follows:</span></span>

    -   <span data-ttu-id="eff70-110">Les **administrateurs système MBAM** ont accès à toutes les fonctionnalités d’administration et de surveillance de Microsoft BitLocker dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="eff70-110">**MBAM System Administrators** have access to all Microsoft BitLocker Administration and Monitoring features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="eff70-111">**Les utilisateurs de matériel MBAM** ont accès aux fonctionnalités de compatibilité matérielle dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="eff70-111">**MBAM Hardware Users** have access to the Hardware Compatibility features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="eff70-112">**Les utilisateurs du support technique MBAM** ont accès aux options de gestion du TPM et de récupération des lecteurs dans le site Web d’administration MBAM, mais doivent remplir tous les champs lorsqu’ils utilisent une des deux options.</span><span class="sxs-lookup"><span data-stu-id="eff70-112">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM administration website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="eff70-113">**MBAM les utilisateurs de rapports** ont accès aux rapports de conformité et d’audit figurant sur le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="eff70-113">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM administration website.</span></span>

    -   <span data-ttu-id="eff70-114">Les options de **support technique avancée MBAM** ont accès aux options gérer le TPM et récupération de lecteur du site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="eff70-114">**MBAM Advanced Helpdesk Uses** have access to the Manage TPM and Drive Recovery options in the MBAM administration website.</span></span> <span data-ttu-id="eff70-115">Ces utilisateurs ne sont pas obligés de renseigner tous les champs lorsqu’ils utilisent l’une des options.</span><span class="sxs-lookup"><span data-stu-id="eff70-115">These users are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="eff70-116">Pour plus d’informations sur les rôles d’administration et de contrôle Microsoft BitLocker, voir [planification des rôles d’administrateur MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="eff70-116">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

## <span data-ttu-id="eff70-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eff70-117">Related topics</span></span>


[<span data-ttu-id="eff70-118">Administration des composants de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="eff70-118">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 






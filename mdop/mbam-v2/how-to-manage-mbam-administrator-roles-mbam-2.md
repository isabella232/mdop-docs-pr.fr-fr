---
title: Gérer des rôles d'administrateur MBAM
description: Gérer des rôles d'administrateur MBAM
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810962"
---
# <span data-ttu-id="fac9d-103">Gérer des rôles d'administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="fac9d-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="fac9d-104">Une fois l’installation de Microsoft BitLocker administration et surveillance (MBAM) terminée pour toutes les fonctionnalités du serveur, les utilisateurs administratifs doivent y avoir accès.</span><span class="sxs-lookup"><span data-stu-id="fac9d-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users will have to be granted access to them.</span></span> <span data-ttu-id="fac9d-105">Il est recommandé que les administrateurs qui gèrent ou utilisent les fonctionnalités d’administration de Microsoft BitLocker et de surveillance du serveur doivent être assignés aux groupes de sécurité de services de domaine, et ils doivent alors être ajoutés au groupe local d’administration MBAM approprié.</span><span class="sxs-lookup"><span data-stu-id="fac9d-105">As a best practice, administrators who will manage or use Microsoft BitLocker Administration and Monitoring Server features should be assigned to Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="fac9d-106">Pour gérer les appartenances aux rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="fac9d-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="fac9d-107">Assigner des utilisateurs à des groupes de sécurité dans les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fac9d-107">Assign administrative users to security groups in ActiveDirectory Domain Services.</span></span>

2.  <span data-ttu-id="fac9d-108">Ajoutez des groupes de sécurité ActiveDirectory aux rôles pour les groupes locaux d’administration MBAM sur le serveur MBAM pour les fonctionnalités respectives.</span><span class="sxs-lookup"><span data-stu-id="fac9d-108">Add ActiveDirectory security groups to the roles for MBAM administrative local groups on the MBAM server for the respective features.</span></span>

    -   <span data-ttu-id="fac9d-109">Les **administrateurs système MBAM** ont accès à toutes les fonctionnalités de MBAM dans le site Web d’administration et de surveillance de MBAM.</span><span class="sxs-lookup"><span data-stu-id="fac9d-109">**MBAM System Administrators** have access to all MBAM features in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="fac9d-110">**Les utilisateurs du support technique MBAM** ont accès aux options de gestion du TPM et de récupération des lecteurs dans le site Web d’administration et de surveillance de MBAM, mais doivent remplir tous les champs lorsqu’ils utilisent l’une des deux options.</span><span class="sxs-lookup"><span data-stu-id="fac9d-110">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="fac9d-111">**MBAM les utilisateurs de rapports** peuvent accéder aux rapports de conformité et d’audit dans le site Web d’administration et de surveillance de MBAM.</span><span class="sxs-lookup"><span data-stu-id="fac9d-111">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="fac9d-112">**Les utilisateurs de l’assistance technique avancée MBAM** ont accès aux options de gestion du TPM et de récupération des lecteurs dans le site Web d’administration et de surveillance de MBAM, mais ils ne sont pas tenus de remplir tous les champs lorsqu’ils utilisent l’une des options.</span><span class="sxs-lookup"><span data-stu-id="fac9d-112">**MBAM Advanced Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="fac9d-113">Pour plus d’informations sur les rôles d’administration et de contrôle Microsoft BitLocker, voir [planification des rôles d’administrateur MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="fac9d-113">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="fac9d-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fac9d-114">Related topics</span></span>


[<span data-ttu-id="fac9d-115">Administration des composants de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="fac9d-115">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 






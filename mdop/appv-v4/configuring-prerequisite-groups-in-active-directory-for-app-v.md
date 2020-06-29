---
title: Configuration des groupes prérequis dans Active Directory pour App-V
description: Configuration des groupes prérequis dans Active Directory pour App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809011"
---
# <span data-ttu-id="47bff-103">Configuration des groupes prérequis dans Active Directory pour App-V</span><span class="sxs-lookup"><span data-stu-id="47bff-103">Configuring Prerequisite Groups in Active Directory for App-V</span></span>


<span data-ttu-id="47bff-104">Avant d’installer le serveur de gestion Microsoft Application Virtualization (App-V), vous devez créer les objets suivants dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="47bff-104">Before you install the Microsoft Application Virtualization (App-V) Management Server, you must create the following objects in Active Directory.</span></span> <span data-ttu-id="47bff-105">App-V utilise des groupes Active Directory pour contrôler l’accès aux applications et aux fonctions d’administration.</span><span class="sxs-lookup"><span data-stu-id="47bff-105">App-V uses Active Directory groups to control access to applications and administrative functions.</span></span> <span data-ttu-id="47bff-106">Vous utiliserez ces groupes lors du processus d’installation du serveur et lors de la publication d’applications.</span><span class="sxs-lookup"><span data-stu-id="47bff-106">You will use these groups during the server installation process and when publishing applications.</span></span>

## <span data-ttu-id="47bff-107">Configuration des groupes d’éléments requis dans Active Directory pour la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="47bff-107">Configuring Prerequisite Groups in Active Directory for Application Virtualization</span></span>


<span data-ttu-id="47bff-108">Le tableau suivant répertorie les groupes Active Directory requis pour l’installation de App-V.</span><span class="sxs-lookup"><span data-stu-id="47bff-108">This table lists the Active Directory groups that are required for installing App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47bff-109">Object</span><span class="sxs-lookup"><span data-stu-id="47bff-109">Object</span></span></th>
<th align="left"><span data-ttu-id="47bff-110">Description</span><span class="sxs-lookup"><span data-stu-id="47bff-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47bff-111">Unité d’organisation (UO)</span><span class="sxs-lookup"><span data-stu-id="47bff-111">Organizational Unit (OU)</span></span></p></td>
<td align="left"><p><span data-ttu-id="47bff-112">Créez une unité d’organisation dans Active Directory pour les groupes spécifiques requis pour App-V.</span><span class="sxs-lookup"><span data-stu-id="47bff-112">Create an OU in Active Directory for the specific groups required for App-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47bff-113">Groupe d’administration App-V</span><span class="sxs-lookup"><span data-stu-id="47bff-113">App-V Administrative Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="47bff-114">Lors de l’installation du serveur de gestion App-V, vous devez sélectionner un groupe Active Directory à utiliser en tant que groupe administrateurs d’applications-V pour contrôler l’accès administratif à la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="47bff-114">During installation of the App-V Management Server, you must select an Active Directory group to use as the App-V Administrators group to control administrative access to the Management Console.</span></span> <span data-ttu-id="47bff-115">Créer un groupe de sécurité pour les administrateurs d’application-V et ajouter à ce groupe chaque utilisateur qui a besoin d’utiliser la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="47bff-115">Create a security group for App-V administrators, and add to this group every user who needs to use the Management Console.</span></span> <span data-ttu-id="47bff-116">Vous ne pouvez pas créer ce groupe directement à partir du programme d’installation d’application-V Management Server.</span><span class="sxs-lookup"><span data-stu-id="47bff-116">You cannot create this group directly from the App-V Management Server installer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47bff-117">Groupe utilisateurs d’App-V</span><span class="sxs-lookup"><span data-stu-id="47bff-117">App-V Users Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="47bff-118">App-V nécessite que chaque compte d’utilisateur qui accède aux fonctions App-V soit membre d’une stratégie de fournisseur associée à un seul groupe pour un accès général à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="47bff-118">App-V requires that every User account that accesses App-V functions be a member of a provider policy associated with a single group for general platform access.</span></span> <span data-ttu-id="47bff-119">Utiliser un groupe existant; par exemple, les utilisateurs du domaine, si tous les utilisateurs ont accès à l’application-V ou créent un nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="47bff-119">Use an existing group; for example, Domain Users, if all users are to have access to App-V, or create a new group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47bff-120">Groupes d’applications</span><span class="sxs-lookup"><span data-stu-id="47bff-120">Application Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="47bff-121">App-V associe le droit d’utiliser une application individuelle avec un groupe Active Directory.</span><span class="sxs-lookup"><span data-stu-id="47bff-121">App-V associates the right to use an individual application with an Active Directory group.</span></span> <span data-ttu-id="47bff-122">Créez un groupe Active Directory pour chaque application et attribuez-lui des utilisateurs pour contrôler l’accès des utilisateurs aux applications.</span><span class="sxs-lookup"><span data-stu-id="47bff-122">Create an Active Directory group for each application, and assign users to these groups as needed to control user access to the applications.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="47bff-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47bff-123">Related topics</span></span>


[<span data-ttu-id="47bff-124">Configuration requise pour le déploiement d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="47bff-124">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="47bff-125">Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="47bff-125">How to Configure Windows Server 2008 for App-V Management Servers</span></span>](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 






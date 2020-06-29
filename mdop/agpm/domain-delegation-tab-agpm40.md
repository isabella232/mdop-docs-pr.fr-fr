---
title: Onglet Délégation de domaine
description: Onglet Délégation de domaine
author: dansimp
ms.assetid: 5be5841e-92fb-4af6-aa68-0ae50f8d5141
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c5f3b5c3b7d8799b383ab48870fcccad0b0c3f73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807586"
---
# <span data-ttu-id="72127-103">Onglet Délégation de domaine</span><span class="sxs-lookup"><span data-stu-id="72127-103">Domain Delegation Tab</span></span>


<span data-ttu-id="72127-104">L’onglet **délégation de domaine** du volet de contrôle des **modifications** fournit une liste des administrateurs de stratégie de groupe qui disposent d’un accès au niveau du domaine pour l’archive et indiquent les rôles de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="72127-104">The **Domain Delegation** tab on the **Change Control** pane provides a list of Group Policy administrators who have domain-level access to the archive and indicates the roles of each.</span></span> <span data-ttu-id="72127-105">Par ailleurs, cet onglet permet aux administrateurs d’AGPM (contrôle total) de configurer des autorisations au niveau du domaine pour les éditeurs, approbateurs, réviseurs et autres administrateurs d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="72127-105">Additionally, this tab enables AGPM Administrators (Full Control) to configure domain-level permissions for Editors, Approvers, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="72127-106">Il existe deux sections sous l’onglet **délégation de domaine** (configuration de la notification par courrier électronique et de la délégation basée sur le rôle pour une gestion avancée de la stratégie de groupe) au niveau du domaine.</span><span class="sxs-lookup"><span data-stu-id="72127-106">There are two sections on the **Domain Delegation** tab—configuration of e-mail notification and role-based delegation for Advanced Group Policy Management (AGPM) at the domain level.</span></span>

## <span data-ttu-id="72127-107">Configuration de la notification par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="72127-107">Configuration of e-mail notification</span></span>


<span data-ttu-id="72127-108">La section notification par courrier électronique de cet onglet identifie les approbateurs qui recevront une notification lorsque les opérations seront en attente dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="72127-108">The e-mail notification section of this tab identifies the Approvers that will receive notification when operations are pending in AGPM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72127-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="72127-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="72127-110">Description</span><span class="sxs-lookup"><span data-stu-id="72127-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72127-111">À partir de l’adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="72127-111">From e-mail address</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-112">Alias AGPM à partir duquel la notification est envoyée aux approbateurs.</span><span class="sxs-lookup"><span data-stu-id="72127-112">The AGPM alias from which notification is sent to Approvers.</span></span> <span data-ttu-id="72127-113">Dans un environnement à plusieurs domaines, il peut s’agir du même alias dans l’environnement ou d’un alias différent pour chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="72127-113">In an environment with multiple domains, this can be the same alias throughout the environment or a different alias for each domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72127-114">À l’adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="72127-114">To e-mail address</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-115">Liste séparée par des virgules des adresses de courrier des approbateurs auprès desquels la notification doit être envoyée</span><span class="sxs-lookup"><span data-stu-id="72127-115">A comma-delimited list of e-mail addresses of Approvers to whom notification is to be sent</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72127-116">Serveur SMTP</span><span class="sxs-lookup"><span data-stu-id="72127-116">SMTP server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-117">Nom du serveur de messagerie, par exemple mail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72127-117">The name of the e-mail server, such as mail.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72127-118">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="72127-118">User name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-119">Utilisateur ayant accès au serveur SMTP</span><span class="sxs-lookup"><span data-stu-id="72127-119">A user with access to the SMTP server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72127-120">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="72127-120">Password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-121">Mot de passe de l’utilisateur pour l’authentification auprès du serveur SMTP</span><span class="sxs-lookup"><span data-stu-id="72127-121">User's password for authentication to the SMTP server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72127-122">Confirmer le mot de passe</span><span class="sxs-lookup"><span data-stu-id="72127-122">Confirm password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-123">Confirmer le mot de passe d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="72127-123">Confirm user's password</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72127-124">Délégation basée sur le rôle au niveau du domaine</span><span class="sxs-lookup"><span data-stu-id="72127-124">Domain-level role-based delegation</span></span>


<span data-ttu-id="72127-125">La section délégation basée sur le rôle de cet onglet s’affiche, et permet à un administrateur AGPM de déléguer les autorisations autorisées, refusées et héritées pour chaque groupe et utilisateur sur le domaine avec accès à l’archive.</span><span class="sxs-lookup"><span data-stu-id="72127-125">The role-based delegation section of this tab displays and enables an AGPM Administrator to delegate allowed, denied, and inherited permissions for each group and user on the domain with access to the archive.</span></span> <span data-ttu-id="72127-126">Un administrateur AGPM peut configurer les autorisations à l’échelle d’un domaine à l’aide de rôles AGPM standard (éditeur, approbateur, réviseur et administrateur AGPM) ou d’une combinaison personnalisée d’autorisations pour chaque administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="72127-126">An AGPM Administrator can configure domain-wide permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions for each Group Policy administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72127-127">Bouton</span><span class="sxs-lookup"><span data-stu-id="72127-127">Button</span></span></th>
<th align="left"><span data-ttu-id="72127-128">Effet</span><span class="sxs-lookup"><span data-stu-id="72127-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72127-129">Add</span><span class="sxs-lookup"><span data-stu-id="72127-129">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-130">Ajoutez une nouvelle entrée au descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="72127-130">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="72127-131">Les administrateurs de stratégie de groupe peuvent ajouter des utilisateurs ou des groupes dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="72127-131">Any users or groups in Active Directory can be added as Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72127-132">Supprimer</span><span class="sxs-lookup"><span data-stu-id="72127-132">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-133">Supprimer les administrateurs de stratégie de groupe sélectionnés de la liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="72127-133">Remove the selected Group Policy administrators from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="72127-134">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72127-134">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-135">Afficher les propriétés pour les administrateurs de stratégie de groupe sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="72127-135">Display the properties for the selected Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="72127-136">Avancé</span><span class="sxs-lookup"><span data-stu-id="72127-136">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="72127-137">Ouvrez l' <strong> éditeur de liste de contrôle d’accès </strong> .</span><span class="sxs-lookup"><span data-stu-id="72127-137">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="72127-138">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="72127-138">Additional considerations</span></span>

-   <span data-ttu-id="72127-139">Pour plus d’informations sur les rôles et les autorisations liées à des tâches spécifiques, voir les tâches d' [exécution des tâches d’administration d’AGPM](performing-agpm-administrator-tasks-agpm40.md), exécution de tâches d' [éditeur](performing-editor-tasks-agpm40.md), [exécution des tâches approbateurs](performing-approver-tasks-agpm40.md)et [exécution des tâches de relecteur](performing-reviewer-tasks-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="72127-139">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks-agpm40.md), [Performing Editor Tasks](performing-editor-tasks-agpm40.md), [Performing Approver Tasks](performing-approver-tasks-agpm40.md), and [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md).</span></span>

### <span data-ttu-id="72127-140">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="72127-140">Additional references</span></span>

-   [<span data-ttu-id="72127-141">Interface utilisateur: gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="72127-141">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="72127-142">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="72127-142">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 






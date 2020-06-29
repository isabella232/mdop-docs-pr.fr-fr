---
title: Déléguer l'accès au niveau du domaine à l'archive
description: Déléguer l'accès au niveau du domaine à l'archive
author: dansimp
ms.assetid: 11ca1d40-4b5c-496e-8922-d01412717858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b33c0ec8821248ab4eddc051e67e7f0e6c073a9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807621"
---
# <span data-ttu-id="8a1f9-103">Déléguer l'accès au niveau du domaine à l'archive</span><span class="sxs-lookup"><span data-stu-id="8a1f9-103">Delegate Domain-Level Access to the Archive</span></span>


<span data-ttu-id="8a1f9-104">Configurez la délégation pour votre environnement de sorte que les administrateurs de stratégie de groupe aient l’accès approprié et contrôlent les objets de stratégie de groupe dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-104">Set up delegation for your environment so that Group Policy administrators have the appropriate access to and control over Group Policy Objects (GPOs) in the archive.</span></span> <span data-ttu-id="8a1f9-105">Il existe des autorisations de base que vous pouvez appliquer pour rendre les opérations plus efficaces.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-105">There are baseline permissions you can apply to make operation more efficient.</span></span> <span data-ttu-id="8a1f9-106">Vous pouvez accorder des autorisations d’une manière qui répond aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="8a1f9-107">Un compte d’utilisateur disposant du rôle Administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="8a1f9-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8a1f9-109">Pour déléguer l’accès de sorte que les utilisateurs et les groupes disposent des autorisations appropriées pour tous les objets de stratégie de groupe au sein d’un domaine</span><span class="sxs-lookup"><span data-stu-id="8a1f9-109">To delegate access so that users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="8a1f9-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8a1f9-111">Cliquez sur l’onglet **délégation de domaine** , puis configurez l’accès à tous les objets de stratégie de groupe du domaine:</span><span class="sxs-lookup"><span data-stu-id="8a1f9-111">Click the **Domain Delegation** tab, and configure access to all GPOs in the domain:</span></span>

    1.  <span data-ttu-id="8a1f9-112">Pour ajouter l’accès d’un utilisateur ou d’un groupe, cliquez sur le bouton **Ajouter** , sélectionnez l’utilisateur ou le groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="8a1f9-113">Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez un rôle, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="8a1f9-114">Pour supprimer l’accès d’un utilisateur ou d’un groupe, sélectionnez-le, puis cliquez sur le bouton **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="8a1f9-114">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

    3.  <span data-ttu-id="8a1f9-115">Pour modifier les rôles et autorisations délégués à un utilisateur ou à un groupe, sélectionnez cliquez sur le bouton **avancé** .</span><span class="sxs-lookup"><span data-stu-id="8a1f9-115">To modify the roles and permissions delegated to a user or group, select click the **Advanced** button.</span></span> <span data-ttu-id="8a1f9-116">Dans la boîte de dialogue **autorisations** , sélectionnez l’utilisateur ou le groupe, activez la case à cocher en regard de chaque rôle à attribuer à l’utilisateur ou au groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="8a1f9-117">**Remarques**  Éditeur et approbateur incluent les autorisations de relecteur.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="8a1f9-118">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="8a1f9-118">Additional considerations</span></span>

-   <span data-ttu-id="8a1f9-119">Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8a1f9-120">Plus précisément, vous devez disposer des autorisations de modification de la **sécurité** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="8a1f9-121">Pour déléguer l’accès en lecture aux administrateurs de stratégie de groupe qui utilisent AGPM, vous devez leur attribuer le contenu de la **liste** et les autorisations de **paramètres de lecture** .</span><span class="sxs-lookup"><span data-stu-id="8a1f9-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="8a1f9-122">Cela leur permet d’afficher des objets de stratégie de groupe dans l’onglet **contenu** d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="8a1f9-123">D’autres autorisations doivent être déléguées explicitement.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="8a1f9-124">Les éditeurs doivent disposer d’une autorisation de **lecture** pour la copie déployée d’un objet de stratégie de groupe, afin de pouvoir tirer parti de l’installation de logiciels de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-124">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="8a1f9-125">L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte, soit n’est pas utilisé pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8a1f9-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="8a1f9-126">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="8a1f9-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="8a1f9-127">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="8a1f9-127">Additional references</span></span>

-   [<span data-ttu-id="8a1f9-128">Gestion de l'archivage</span><span class="sxs-lookup"><span data-stu-id="8a1f9-128">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 






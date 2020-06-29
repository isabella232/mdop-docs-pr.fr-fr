---
title: Accès au niveau du domaine de délégué
description: Accès au niveau du domaine de délégué
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808530"
---
# <span data-ttu-id="2a499-103">Accès au niveau du domaine de délégué</span><span class="sxs-lookup"><span data-stu-id="2a499-103">Delegate Domain-Level Access</span></span>


<span data-ttu-id="2a499-104">Configurez la délégation pour votre environnement de sorte que les administrateurs de stratégie de groupe disposent de l’accès approprié et contrôlent les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2a499-104">Set up delegation for your environment so Group Policy administrators have the appropriate access to and control over Group Policy objects (GPOs).</span></span> <span data-ttu-id="2a499-105">Il existe des autorisations de base que vous pouvez appliquer pour rendre plus efficaces le fonctionnement de la gestion de la stratégie de groupe avancée.</span><span class="sxs-lookup"><span data-stu-id="2a499-105">There are baseline permissions you can apply to make the operation of Advanced Group Policy Management (AGPM) more efficient.</span></span> <span data-ttu-id="2a499-106">Vous pouvez accorder des autorisations d’une manière qui répond aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2a499-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="2a499-107">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2a499-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="2a499-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2a499-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2a499-109">Pour déléguer l’accès de sorte que les utilisateurs et les groupes disposent des autorisations appropriées pour tous les objets de stratégie de groupe dans un domaine</span><span class="sxs-lookup"><span data-stu-id="2a499-109">To delegate access so users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="2a499-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2a499-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2a499-111">Cliquez sur l’onglet **délégation de domaine** , puis cliquez sur le bouton **avancé** .</span><span class="sxs-lookup"><span data-stu-id="2a499-111">Click the **Domain Delegation** tab, then click the **Advanced** button.</span></span>

3.  <span data-ttu-id="2a499-112">Dans la boîte de dialogue **autorisations** , activez la case à cocher de chaque rôle à attribuer à une personne, puis cliquez sur le bouton **avancé** .</span><span class="sxs-lookup"><span data-stu-id="2a499-112">In the **Permissions** dialog box, click the check box for each role to be assigned to an individual, and then click the **Advanced** button.</span></span>

    <span data-ttu-id="2a499-113">**Remarques**  Éditeur et approbateur incluent les autorisations de relecteur.</span><span class="sxs-lookup"><span data-stu-id="2a499-113">**Note** Editor and Approver include Reviewer permissions.</span></span>

     

4.  <span data-ttu-id="2a499-114">Dans la boîte de dialogue **paramètres de sécurité avancés** , sélectionnez un administrateur de stratégie de groupe, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="2a499-114">In the **Advanced Security Settings** dialog box, select a Group Policy administrator, and then click **Edit**.</span></span>

5.  <span data-ttu-id="2a499-115">Pour **appliquer**à, sélectionnez **cet objet et les objets imbriqués**, configurez des autorisations spéciales au-delà des rôles AGPM standard, puis cliquez sur **OK** dans la boîte de dialogue **entrée** d' **autorisation** .</span><span class="sxs-lookup"><span data-stu-id="2a499-115">For **Apply onto**, select **This object and nested objects**, configure any special permissions beyond the standard AGPM roles, then click **OK** in the **Permission** **Entry** dialog box.</span></span>

6.  <span data-ttu-id="2a499-116">Dans la boîte de dialogue **paramètres de sécurité avancés** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a499-116">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

7.  <span data-ttu-id="2a499-117">Dans la boîte de dialogue **autorisations** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a499-117">In the **Permissions** dialog box, click **OK**.</span></span>

### <span data-ttu-id="2a499-118">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="2a499-118">Additional considerations</span></span>

-   <span data-ttu-id="2a499-119">Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2a499-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="2a499-120">Plus précisément, vous devez disposer des autorisations de modification de la **sécurité** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="2a499-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="2a499-121">Pour déléguer l’accès en lecture aux administrateurs de stratégie de groupe qui utilisent AGPM, vous devez leur attribuer le contenu de la **liste** et les autorisations de **paramètres de lecture** .</span><span class="sxs-lookup"><span data-stu-id="2a499-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="2a499-122">Cela leur permet d’afficher des objets de stratégie de groupe dans l’onglet **contenu** d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="2a499-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="2a499-123">Définissez l’autorisation à appliquer à **cet objet et aux objets imbriqués**.</span><span class="sxs-lookup"><span data-stu-id="2a499-123">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="2a499-124">D’autres autorisations doivent être déléguées explicitement.</span><span class="sxs-lookup"><span data-stu-id="2a499-124">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="2a499-125">Les éditeurs doivent disposer d’une autorisation de **lecture** pour la copie déployée d’un objet de stratégie de groupe, afin de pouvoir tirer parti de l’installation de logiciels de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2a499-125">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="2a499-126">L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte afin qu’elle ne soit pas utilisée pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2a499-126">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="2a499-127">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="2a499-127">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="2a499-128">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2a499-128">Additional references</span></span>

-   [<span data-ttu-id="2a499-129">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="2a499-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 






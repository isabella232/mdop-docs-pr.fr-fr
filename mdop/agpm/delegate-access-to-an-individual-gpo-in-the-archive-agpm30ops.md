---
title: Déléguer l'accès à un objet de stratégie de groupe dans l'archive
description: Déléguer l'accès à un objet de stratégie de groupe dans l'archive
author: dansimp
ms.assetid: 7b37b188-2b6b-4e52-be97-8ef899e9893b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 592937a28b0e2556991b0c338b88b2cfa88ba83d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807638"
---
# <span data-ttu-id="2339d-103">Déléguer l'accès à un objet de stratégie de groupe dans l'archive</span><span class="sxs-lookup"><span data-stu-id="2339d-103">Delegate Access to an Individual GPO in the Archive</span></span>


<span data-ttu-id="2339d-104">En tant qu’administrateur d’AGPM (contrôle total), vous pouvez déléguer la gestion d’un objet de stratégie de groupe contrôlé (GPO) dans l’archive de sorte que les groupes et éditeurs sélectionnés puissent le modifier, que les réviseurs puissent le consulter, et les approbateurs peuvent l’approuver.</span><span class="sxs-lookup"><span data-stu-id="2339d-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy Object (GPO) in the archive so that selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="2339d-105">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe ou un compte d’utilisateur disposant des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2339d-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="2339d-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2339d-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2339d-107">Pour déléguer la gestion d’un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="2339d-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="2339d-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2339d-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2339d-109">Dans l’onglet **Sommaire** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés, puis cliquez sur l’objet de stratégie de groupe à déléguer:</span><span class="sxs-lookup"><span data-stu-id="2339d-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="2339d-110">Pour ajouter l’accès d’un utilisateur ou d’un groupe, cliquez sur le bouton **Ajouter** , sélectionnez l’utilisateur ou le groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2339d-110">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="2339d-111">Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez un rôle, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2339d-111">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="2339d-112">Pour supprimer l’accès d’un utilisateur ou d’un groupe, sélectionnez-le, puis cliquez sur le bouton **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="2339d-112">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

        <span data-ttu-id="2339d-113">**Remarques**  Si un utilisateur ou un groupe hérite de l’accès à l’échelle du domaine, le bouton **supprimer** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="2339d-113">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="2339d-114">Vous pouvez modifier l’accès à l’échelle du domaine sous l’onglet **délégation de domaine** .</span><span class="sxs-lookup"><span data-stu-id="2339d-114">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="2339d-115">Pour modifier les rôles et autorisations délégués à un utilisateur ou à un groupe, cliquez sur le bouton **avancé** .</span><span class="sxs-lookup"><span data-stu-id="2339d-115">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="2339d-116">Dans la boîte de dialogue **autorisations** , sélectionnez l’utilisateur ou le groupe, activez la case à cocher de chaque rôle à affecter à l’utilisateur ou au groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2339d-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and click **OK**.</span></span>

        <span data-ttu-id="2339d-117">**Remarques**  Éditeur et approbateur incluent les autorisations de relecteur.</span><span class="sxs-lookup"><span data-stu-id="2339d-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="2339d-118">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="2339d-118">Additional considerations</span></span>

-   <span data-ttu-id="2339d-119">Par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2339d-119">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="2339d-120">Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine et modifier les autorisations de **sécurité** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2339d-120">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="2339d-121">Pour déléguer l’accès en lecture aux administrateurs de stratégie de groupe qui utilisent AGPM, vous devez leur attribuer le contenu de la **liste** et les autorisations de **paramètres de lecture** .</span><span class="sxs-lookup"><span data-stu-id="2339d-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="2339d-122">Cela leur permet d’afficher des objets de stratégie de groupe dans l’onglet **contenu** d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="2339d-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="2339d-123">D’autres autorisations doivent être déléguées explicitement.</span><span class="sxs-lookup"><span data-stu-id="2339d-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="2339d-124">Les éditeurs doivent disposer d’une autorisation de **lecture** pour la copie déployée d’un objet de stratégie de groupe pour tirer pleinement parti de l’installation de logiciels de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2339d-124">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="2339d-125">L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte, soit n’est pas utilisé pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2339d-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="2339d-126">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="2339d-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="2339d-127">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2339d-127">Additional references</span></span>

-   [<span data-ttu-id="2339d-128">Gestion de l'archivage</span><span class="sxs-lookup"><span data-stu-id="2339d-128">Managing the Archive</span></span>](managing-the-archive.md)

 

 






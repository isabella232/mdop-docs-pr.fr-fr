---
title: Déléguer la gestion d'un objet de stratégie de groupe contrôlé
description: Déléguer la gestion d'un objet de stratégie de groupe contrôlé
author: dansimp
ms.assetid: 509b02e7-ce0b-4919-b58a-c3a33051152e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d34231f25c172951cd0176b3e490dab84b98f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807618"
---
# <span data-ttu-id="b8eaa-103">Déléguer la gestion d'un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="b8eaa-103">Delegate Management of a Controlled GPO</span></span>


<span data-ttu-id="b8eaa-104">Un approbateur peut déléguer la gestion d’un objet de stratégie de groupe contrôlé (GPO) qui a été créé par cet approbateur.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-104">An Approver can delegate the management of a controlled Group Policy Object (GPO) that was created by that Approver.</span></span> <span data-ttu-id="b8eaa-105">À l’instar d’un administrateur AGPM (contrôle total), l’approbateur peut déléguer l’accès à un tel objet GPO de telle sorte que les éditeurs sélectionnés puissent le modifier, les réviseurs pourront le consulter et permettre à d’autres approbateurs de l’approuver.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO so that selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="b8eaa-106">Par défaut, un approbateur ne peut pas déléguer l’accès aux objets de stratégie de groupe créés par un autre administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="b8eaa-107">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe ou un compte d’utilisateur disposant des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="b8eaa-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="b8eaa-109">Pour déléguer la gestion d’un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="b8eaa-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="b8eaa-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="b8eaa-111">Dans l’onglet **Sommaire** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés, puis cliquez sur l’objet de stratégie de groupe à déléguer:</span><span class="sxs-lookup"><span data-stu-id="b8eaa-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="b8eaa-112">Pour ajouter l’accès d’un utilisateur ou d’un groupe, cliquez sur le bouton **Ajouter** , sélectionnez l’utilisateur ou le groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="b8eaa-113">Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez un rôle, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="b8eaa-114">Pour supprimer l’accès d’un utilisateur ou d’un groupe, sélectionnez-le, puis cliquez sur le bouton **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="b8eaa-114">To remove access for a user or group, select the user or group, and then click the **Remove** button.</span></span>

        <span data-ttu-id="b8eaa-115">**Remarques**  Si un utilisateur ou un groupe hérite de l’accès à l’échelle du domaine, le bouton **supprimer** n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-115">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="b8eaa-116">Vous pouvez modifier l’accès à l’échelle du domaine sous l’onglet **délégation de domaine** .</span><span class="sxs-lookup"><span data-stu-id="b8eaa-116">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="b8eaa-117">Pour modifier les rôles et autorisations délégués à un utilisateur ou à un groupe, cliquez sur le bouton **avancé** .</span><span class="sxs-lookup"><span data-stu-id="b8eaa-117">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="b8eaa-118">Dans la boîte de dialogue **autorisations** , sélectionnez l’utilisateur ou le groupe, activez la case à cocher en regard de chaque rôle à attribuer à l’utilisateur ou au groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-118">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="b8eaa-119">**Remarques**  Éditeur et approbateur incluent les autorisations de relecteur.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-119">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="b8eaa-120">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="b8eaa-120">Additional considerations</span></span>

-   <span data-ttu-id="b8eaa-121">Par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-121">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="b8eaa-122">Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine et modifier les autorisations de **sécurité** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-122">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="b8eaa-123">Pour déléguer l’accès en lecture aux administrateurs de stratégie de groupe qui utilisent AGPM, vous devez leur attribuer le contenu de la **liste** et les autorisations de **paramètres de lecture** .</span><span class="sxs-lookup"><span data-stu-id="b8eaa-123">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="b8eaa-124">Cela leur permet d’afficher des objets de stratégie de groupe dans l’onglet **contenu** d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-124">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="b8eaa-125">D’autres autorisations doivent être déléguées explicitement.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-125">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="b8eaa-126">Les éditeurs doivent disposer d’une autorisation de **lecture** pour la copie déployée d’un objet de stratégie de groupe pour tirer pleinement parti de l’installation de logiciels de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b8eaa-126">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

### <span data-ttu-id="b8eaa-127">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b8eaa-127">Additional references</span></span>

-   [<span data-ttu-id="b8eaa-128">Création, contrôle ou importation d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b8eaa-128">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 






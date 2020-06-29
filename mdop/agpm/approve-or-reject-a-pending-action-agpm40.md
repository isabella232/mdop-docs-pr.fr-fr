---
title: Approuver ou rejeter une action en attente
description: Approuver ou rejeter une action en attente
author: dansimp
ms.assetid: 078ea8b5-9ac5-45fc-9ac1-a1aa629c10b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61014ec46db2beb9a525abe8d9b2b0902b3aa78d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807821"
---
# <span data-ttu-id="2439d-103">Approuver ou rejeter une action en attente</span><span class="sxs-lookup"><span data-stu-id="2439d-103">Approve or Reject a Pending Action</span></span>


<span data-ttu-id="2439d-104">Le responsable d’un approbateur est d’évaluer et de rejeter les demandes de création, de déploiement et de suppression d’objets de stratégie de groupe (GPO) dans les éditeurs ou réviseurs qui n’ont pas l’autorisation d’effectuer ces actions.</span><span class="sxs-lookup"><span data-stu-id="2439d-104">The core responsibility of an Approver is to evaluate and then approve or reject requests for Group Policy Object (GPO) creation, deployment, and deletion from Editors or Reviewers who do not have permission to complete those actions.</span></span> <span data-ttu-id="2439d-105">Les rapports peuvent aider un approbateur à évaluer une nouvelle version d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2439d-105">Reports can assist an Approver with evaluating a new version of a GPO.</span></span>

<span data-ttu-id="2439d-106">Un compte d’utilisateur disposant du rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2439d-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="2439d-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2439d-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2439d-108">Pour approuver ou rejeter une demande en attente</span><span class="sxs-lookup"><span data-stu-id="2439d-108">To approve or reject a pending request</span></span>**

1.  <span data-ttu-id="2439d-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2439d-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2439d-110">Dans l’onglet **contenu** , cliquez sur l’onglet **en attente** pour afficher les objets de stratégie de groupe en attente.</span><span class="sxs-lookup"><span data-stu-id="2439d-110">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

3.  <span data-ttu-id="2439d-111">Cliquez avec le bouton droit sur un objet de stratégie de groupe en attente, puis cliquez sur **approuver** ou **rejeter**.</span><span class="sxs-lookup"><span data-stu-id="2439d-111">Right-click a pending GPO, and then click either **Approve** or **Reject**.</span></span>

4.  <span data-ttu-id="2439d-112">Si vous approuvez le déploiement, cliquez sur **Options avancées** dans la boîte de dialogue **approuver l’opération en attente** pour examiner les liens vers l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2439d-112">If approving deployment, click **Advanced** in the **Approve Pending Operation** dialog box to review links to the GPO.</span></span> <span data-ttu-id="2439d-113">Placez le pointeur de la souris sur un élément de l’arborescence pour afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="2439d-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="2439d-114">Par défaut, tous les liens vers l’objet GPO sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="2439d-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="2439d-115">Pour empêcher la restauration d’un lien, désactivez la case à cocher en regard de ce lien.</span><span class="sxs-lookup"><span data-stu-id="2439d-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="2439d-116">Pour empêcher la restauration de tous les liens, décochez la case **restaurer les liaisons** dans la boîte de dialogue **déployer l’objet GPO** .</span><span class="sxs-lookup"><span data-stu-id="2439d-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="2439d-117">Cliquez sur **Oui** ou **OK** pour confirmer l’approbation ou le rejet de l’action en attente.</span><span class="sxs-lookup"><span data-stu-id="2439d-117">Click **Yes** or **OK** to confirm approval or rejection of the pending action.</span></span> <span data-ttu-id="2439d-118">Si vous avez approuvé la demande, l’objet de stratégie de groupe est déplacé vers l’onglet approprié pour l’action exécutée.</span><span class="sxs-lookup"><span data-stu-id="2439d-118">If you have approved the request, the GPO is moved to the appropriate tab for the action performed.</span></span>

    <span data-ttu-id="2439d-119">**Remarques**  Si l’adresse de messagerie d’un approbateur est incluse dans le champ **à l’adresse de messagerie** sous l’onglet **délégation** de **domaine** , l’approbateur reçoit du courrier électronique de l’alias AGPM lorsqu’un éditeur ou réviseur envoie une demande.</span><span class="sxs-lookup"><span data-stu-id="2439d-119">**Note** If an Approver's e-mail address is included in the **To e-mail address** field on the **Domain** **Delegation** tab, the Approver will receive e-mail from the AGPM alias when an Editor or Reviewer submits a request.</span></span>

     

### <span data-ttu-id="2439d-120">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="2439d-120">Additional considerations</span></span>

-   <span data-ttu-id="2439d-121">Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2439d-121">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="2439d-122">Plus précisément, vous devez disposer des autorisations nécessaires pour effectuer la demande d’approbation.</span><span class="sxs-lookup"><span data-stu-id="2439d-122">Specifically, you must have the permissions required to perform the request that you are approving.</span></span>

### <span data-ttu-id="2439d-123">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2439d-123">Additional references</span></span>

-   [<span data-ttu-id="2439d-124">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="2439d-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

 

 






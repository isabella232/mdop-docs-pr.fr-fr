---
title: Vérifier les liens objet de stratégie de groupe
description: Vérifier les liens objet de stratégie de groupe
author: dansimp
ms.assetid: 3aaba9da-f0aa-466f-bd1c-49f11d00ea54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3884a6f3852986cf02e499af59bb56fcaf404ef8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807470"
---
# <span data-ttu-id="34fed-103">Vérifier les liens objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="34fed-103">Review GPO Links</span></span>


<span data-ttu-id="34fed-104">Vous pouvez afficher un diagramme qui indique l’emplacement d’un objet de stratégie de groupe ou d’objets de stratégie de groupe que vous sélectionnez et qui sont liés à des unités d’organisation.</span><span class="sxs-lookup"><span data-stu-id="34fed-104">You can display a diagram showing where a Group Policy Object (GPO) or GPOs that you select are linked to organizational units.</span></span> <span data-ttu-id="34fed-105">Les diagrammes de liens d’objets de stratégie de groupe sont mis à jour chaque fois que l’objet de stratégie de groupe est contrôlé, importé ou archivé.</span><span class="sxs-lookup"><span data-stu-id="34fed-105">GPO link diagrams are updated each time the GPO is controlled, imported, or checked in.</span></span>

<span data-ttu-id="34fed-106">Un compte d’utilisateur disposant du rôle de relecteur, d’éditeur, d’approbateur ou d’un administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="34fed-106">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM)is required to complete this procedure.</span></span> <span data-ttu-id="34fed-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="34fed-107">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="34fed-108">Examen des liens d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="34fed-108">Reviewing GPO links</span></span>


-   [<span data-ttu-id="34fed-109">Pour un ou plusieurs objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="34fed-109">For one or more GPOs</span></span>](#bkmk-gpos)

-   [<span data-ttu-id="34fed-110">Pour une ou plusieurs versions d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="34fed-110">For one or more versions of a GPO</span></span>](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**<span data-ttu-id="34fed-111">Pour afficher les liens d’objets de stratégie de groupe pour un ou plusieurs objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="34fed-111">To display GPO links for one or more GPOs</span></span>**

1.  <span data-ttu-id="34fed-112">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="34fed-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="34fed-113">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé**, **en attente**ou **Corbeille** pour afficher les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="34fed-113">On the **Contents** tab in the details pane, click the **Controlled**, **Pending**, or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="34fed-114">Sélectionnez un ou plusieurs objets de stratégie de groupe pour lesquels afficher les liens, cliquez avec le bouton droit sur un objet de stratégie de groupe sélectionné, cliquez sur **paramètres**, puis cliquez sur **liens d’objets de stratégie** de groupe pour afficher un diagramme de domaines et d’unités d’organisation avec des liens vers les objets de stratégie de groupe sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="34fed-114">Select one or more GPOs for which to display links, right-click a selected GPO, click **Settings**, and then click **GPO Links** to display a diagram of domains and organizational units with links to the selected GPO(s).</span></span>

### <a href="" id="bkmk-gpo-versions"></a>

**<span data-ttu-id="34fed-115">Pour afficher les liens d’objets de stratégie de groupe pour une ou plusieurs versions d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="34fed-115">To display GPO links for one or more versions of a GPO</span></span>**

1.  <span data-ttu-id="34fed-116">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="34fed-116">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="34fed-117">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôle** ou **Corbeille** pour afficher les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="34fed-117">On the **Contents** tab in the details pane, click the **Controlled** or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="34fed-118">Double-cliquez sur l’objet de stratégie de groupe pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="34fed-118">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="34fed-119">Cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe dont vous souhaitez examiner les paramètres, cliquez sur **paramètres**, puis sur **rapport HTML** ou **État XML** pour afficher un récapitulatif des paramètres de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="34fed-119">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="34fed-120">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="34fed-120">Additional considerations</span></span>

-   <span data-ttu-id="34fed-121">Par défaut, vous devez être un réviseur, un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="34fed-121">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="34fed-122">En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="34fed-122">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="34fed-123">Par ailleurs, pour afficher la liste des objets de stratégie de groupe, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="34fed-123">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="34fed-124">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="34fed-124">Additional references</span></span>

-   [<span data-ttu-id="34fed-125">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="34fed-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 






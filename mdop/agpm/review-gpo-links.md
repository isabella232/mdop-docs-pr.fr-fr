---
title: Vérifier les liens objet de stratégie de groupe
description: Vérifier les liens objet de stratégie de groupe
author: dansimp
ms.assetid: 3c472448-f16a-493c-a229-5ca60a470965
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe8b40b4401f08a36217237487bf2b2c0c6c0689
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807469"
---
# <span data-ttu-id="5cfe5-103">Vérifier les liens objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5cfe5-103">Review GPO Links</span></span>


<span data-ttu-id="5cfe5-104">Vous pouvez afficher un diagramme qui indique l’emplacement d’un objet de stratégie de groupe ou d’objets de stratégie de groupe que vous sélectionnez et qui sont liés à des unités d’organisation.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-104">You can display a diagram showing where a Group Policy object (GPO) or GPOs that you select are linked to organizational units.</span></span> <span data-ttu-id="5cfe5-105">Les diagrammes de liens d’objets de stratégie de groupe sont mis à jour chaque fois que l’objet de stratégie de groupe est contrôlé, importé ou archivé.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-105">GPO link diagrams are updated each time the GPO is controlled, imported, or checked in.</span></span>

<span data-ttu-id="5cfe5-106">Un compte d’utilisateur disposant du rôle de réviseur, d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-106">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="5cfe5-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-107">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="5cfe5-108">Examen des liens d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5cfe5-108">Reviewing GPO links</span></span>


-   [<span data-ttu-id="5cfe5-109">Pour un ou plusieurs objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5cfe5-109">For one or more GPOs</span></span>](#bkmk-gpos)

-   [<span data-ttu-id="5cfe5-110">Pour une ou plusieurs versions d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5cfe5-110">For one or more versions of a GPO</span></span>](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**<span data-ttu-id="5cfe5-111">Pour afficher les liens d’objets de stratégie de groupe pour un ou plusieurs objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5cfe5-111">To display GPO links for one or more GPOs</span></span>**

1.  <span data-ttu-id="5cfe5-112">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5cfe5-113">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé**, **en attente**ou **Corbeille** pour afficher les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-113">On the **Contents** tab in the details pane, click the **Controlled**, **Pending**, or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="5cfe5-114">Sélectionnez un ou plusieurs objets de stratégie de groupe pour lesquels afficher les liens, cliquez avec le bouton droit sur un objet de stratégie de groupe sélectionné, cliquez sur **paramètres**, puis cliquez sur **liens d’objets de stratégie** de groupe pour afficher un diagramme de domaines et d’unités d’organisation avec des liens vers les objets de stratégie de groupe sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-114">Select one or more GPOs for which to display links, right-click a selected GPO, click **Settings**, and then click **GPO Links** to display a diagram of domains and organizational units with links to the selected GPO(s).</span></span>

### <a href="" id="bkmk-gpo-versions"></a>

**<span data-ttu-id="5cfe5-115">Pour afficher les liens d’objets de stratégie de groupe pour une ou plusieurs versions d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5cfe5-115">To display GPO links for one or more versions of a GPO</span></span>**

1.  <span data-ttu-id="5cfe5-116">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-116">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5cfe5-117">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôle** ou **Corbeille** pour afficher les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-117">On the **Contents** tab in the details pane, click the **Controlled** or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="5cfe5-118">Double-cliquez sur l’objet de stratégie de groupe pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-118">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="5cfe5-119">Cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe dont vous souhaitez examiner les paramètres, cliquez sur **paramètres**, puis sur **rapport HTML** ou **État XML** pour afficher un récapitulatif des paramètres de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-119">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="5cfe5-120">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="5cfe5-120">Additional considerations</span></span>

-   <span data-ttu-id="5cfe5-121">Par défaut, vous devez être un réviseur, un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-121">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="5cfe5-122">En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-122">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="5cfe5-123">Par ailleurs, pour afficher la liste des objets de stratégie de groupe, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="5cfe5-123">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="5cfe5-124">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="5cfe5-124">Additional references</span></span>

-   [<span data-ttu-id="5cfe5-125">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="5cfe5-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 






---
title: Vérifier les paramètres de l'objet de stratégie de groupe
description: Vérifier les paramètres de l'objet de stratégie de groupe
author: dansimp
ms.assetid: e82570b2-d8ce-4bf0-8ad7-8910409f3041
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 681492f423266ce3722bb1a657ee93527c6bdd7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807465"
---
# <span data-ttu-id="352d6-103">Vérifier les paramètres de l'objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="352d6-103">Review GPO Settings</span></span>


<span data-ttu-id="352d6-104">Vous pouvez générer des rapports HTML et XML pour vérifier les paramètres dans n’importe quelle version d’un objet de stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="352d6-104">You can generate HTML-based and XML-based reports for reviewing settings within any version of a Group Policy object (GPO).</span></span>

<span data-ttu-id="352d6-105">Un compte d’utilisateur disposant du rôle de réviseur, d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="352d6-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="352d6-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="352d6-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="352d6-107">Pour vérifier les paramètres de n’importe quelle version d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="352d6-107">To review settings in any version of a GPO</span></span>**

1.  <span data-ttu-id="352d6-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="352d6-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="352d6-109">Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="352d6-109">On the **Contents** tab in the details pane, click a tab to display GPOs.</span></span>

3.  <span data-ttu-id="352d6-110">Double-cliquez sur l’objet de stratégie de groupe pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="352d6-110">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="352d6-111">Cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe dont vous souhaitez examiner les paramètres, cliquez sur **paramètres**, puis sur **rapport HTML** ou **État XML** pour afficher un récapitulatif des paramètres de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="352d6-111">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="352d6-112">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="352d6-112">Additional considerations</span></span>

-   <span data-ttu-id="352d6-113">Par défaut, vous devez être un réviseur, un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="352d6-113">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="352d6-114">En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="352d6-114">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="352d6-115">Par ailleurs, pour afficher la liste des objets de stratégie de groupe, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="352d6-115">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="352d6-116">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="352d6-116">Additional references</span></span>

-   [<span data-ttu-id="352d6-117">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="352d6-117">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 






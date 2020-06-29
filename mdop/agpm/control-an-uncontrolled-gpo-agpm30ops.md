---
title: Contrôler un objet de stratégie de groupe non contrôlé
description: Contrôler un objet de stratégie de groupe non contrôlé
author: dansimp
ms.assetid: 603f00f9-1e65-4b2f-902a-e53dafedbd8d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 904c3f76ce89f3814b739ee958fc14198899fb14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807685"
---
# <span data-ttu-id="9ef20-103">Contrôler un objet de stratégie de groupe non contrôlé</span><span class="sxs-lookup"><span data-stu-id="9ef20-103">Control an Uncontrolled GPO</span></span>


<span data-ttu-id="9ef20-104">Pour proposer le contrôle de modification d’un objet de stratégie de groupe, vous devez tout d’abord contrôler l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="9ef20-104">To provide change control for a Group Policy Object (GPO), you must first control the GPO.</span></span>

<span data-ttu-id="9ef20-105">Un compte d’utilisateur disposant du rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="9ef20-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="9ef20-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9ef20-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="9ef20-107">Pour contrôler un objet de stratégie de groupe non contrôlé</span><span class="sxs-lookup"><span data-stu-id="9ef20-107">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="9ef20-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9ef20-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9ef20-109">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet non **contrôlé** pour afficher les objets de stratégie de groupe non contrôlés.</span><span class="sxs-lookup"><span data-stu-id="9ef20-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="9ef20-110">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à contrôler avec AGPM, puis cliquez sur **contrôle**.</span><span class="sxs-lookup"><span data-stu-id="9ef20-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="9ef20-111">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ef20-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="9ef20-112">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="9ef20-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9ef20-113">L’objet de stratégie de groupe est supprimé de la liste sous l’onglet non **contrôlé** et ajouté à l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="9ef20-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="9ef20-114">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="9ef20-114">Additional considerations</span></span>

-   <span data-ttu-id="9ef20-115">Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="9ef20-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="9ef20-116">Plus précisément, vous devez disposer du **contenu de liste** et créer des autorisations d’objet de **stratégie de groupe** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="9ef20-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="9ef20-117">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9ef20-117">Additional references</span></span>

-   [<span data-ttu-id="9ef20-118">Création, contrôle ou importation d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9ef20-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 






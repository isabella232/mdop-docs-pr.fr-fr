---
title: Demander le contrôle d'un objet de stratégie de groupe précédemment non contrôlé
description: Demander le contrôle d'un objet de stratégie de groupe précédemment non contrôlé
author: dansimp
ms.assetid: 00e8725d-5d7f-4eed-a5e6-c3631632cfbd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a92db48d87398568900fc0031e688c862a69b417
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807517"
---
# <span data-ttu-id="804ce-103">Demander le contrôle d'un objet de stratégie de groupe précédemment non contrôlé</span><span class="sxs-lookup"><span data-stu-id="804ce-103">Request Control of a Previously Uncontrolled GPO</span></span>


<span data-ttu-id="804ce-104">Pour utiliser le système de gestion de la stratégie de groupe avancé (AGPM) pour proposer le contrôle des modifications d’un objet de stratégie de groupe existant (GPO), l’objet GPO doit être contrôlé avec AGPM.</span><span class="sxs-lookup"><span data-stu-id="804ce-104">To use Advanced Group Policy Management (AGPM) to provide change control for an existing Group Policy object (GPO), the GPO must be controlled with AGPM.</span></span> <span data-ttu-id="804ce-105">Si vous n’êtes pas un approbateur ou un administrateur AGPM (contrôle total), vous devez demander le contrôle de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="804ce-105">Unless you are an Approver or an AGPM Administrator (Full Control), you must request that the GPO be controlled.</span></span>

<span data-ttu-id="804ce-106">Un compte d’utilisateur disposant de l’éditeur ou du rôle de réviseur ou des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="804ce-106">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="804ce-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="804ce-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="804ce-108">Pour contrôler un objet GPO précédemment non contrôlé</span><span class="sxs-lookup"><span data-stu-id="804ce-108">To control a previously uncontrolled GPO</span></span>**

1.  <span data-ttu-id="804ce-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="804ce-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="804ce-110">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet non **contrôlé** pour afficher les objets de stratégie de groupe non contrôlés.</span><span class="sxs-lookup"><span data-stu-id="804ce-110">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="804ce-111">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à contrôler avec AGPM, puis cliquez sur **contrôle**.</span><span class="sxs-lookup"><span data-stu-id="804ce-111">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="804ce-112">Si vous n’avez pas l’autorisation spéciale pour contrôler les objets de stratégie de groupe, vous devez en demander le contrôle.</span><span class="sxs-lookup"><span data-stu-id="804ce-112">Unless you have special permission to control GPOs, you must submit a request for control.</span></span> <span data-ttu-id="804ce-113">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="804ce-113">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="804ce-114">Tapez un commentaire à afficher dans l' **historique** de l’objet de stratégie de groupe, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="804ce-114">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="804ce-115">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="804ce-115">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="804ce-116">L’objet de stratégie de groupe est supprimé de la liste sous l’onglet non **contrôlé** et ajouté à l’onglet **en attente** . Lorsqu’un approbateur a approuvé votre demande, l’objet de stratégie de groupe est déplacé vers l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="804ce-116">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="804ce-117">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="804ce-117">Additional considerations</span></span>

-   <span data-ttu-id="804ce-118">Par défaut, vous devez être un éditeur ou un relecteur pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="804ce-118">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="804ce-119">En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="804ce-119">Specifically, you must have **List Contents** and **Read Settings** permissions for the domain.</span></span>

-   <span data-ttu-id="804ce-120">Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**.</span><span class="sxs-lookup"><span data-stu-id="804ce-120">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="804ce-121">L’objet GPO sera renvoyé à l’onglet non **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="804ce-121">The GPO will be returned to the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="804ce-122">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="804ce-122">Additional references</span></span>

-   [<span data-ttu-id="804ce-123">Création, contrôle ou importation d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="804ce-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 






---
title: Demander le contrôle d'un objet de stratégie de groupe non contrôlé
description: Demander le contrôle d'un objet de stratégie de groupe non contrôlé
author: dansimp
ms.assetid: b668a67a-5a2c-4f6a-8b1c-efa3ca0794d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8cf1ede496a54d6d3d211c2e3cfc23c506217ca7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807513"
---
# <span data-ttu-id="d2038-103">Demander le contrôle d'un objet de stratégie de groupe non contrôlé</span><span class="sxs-lookup"><span data-stu-id="d2038-103">Request Control of an Uncontrolled GPO</span></span>


<span data-ttu-id="d2038-104">Pour proposer le contrôle de modification d’un objet de stratégie de groupe existant (GPO), l’objet GPO doit être contrôlé.</span><span class="sxs-lookup"><span data-stu-id="d2038-104">To provide change control for an existing Group Policy Object (GPO), the GPO must be controlled.</span></span> <span data-ttu-id="d2038-105">Si vous n’êtes pas un approbateur ou un administrateur AGPM (contrôle total), vous devez demander le contrôle de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2038-105">Unless you are an Approver or an AGPM Administrator (Full Control), you must request that the GPO be controlled.</span></span>

<span data-ttu-id="d2038-106">Un compte d’utilisateur ayant le rôle éditeur ou réviseur ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="d2038-106">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="d2038-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d2038-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d2038-108">Pour contrôler un objet de stratégie de groupe non contrôlé</span><span class="sxs-lookup"><span data-stu-id="d2038-108">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="d2038-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2038-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d2038-110">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet non **contrôlé** pour afficher les objets de stratégie de groupe non contrôlés.</span><span class="sxs-lookup"><span data-stu-id="d2038-110">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="d2038-111">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à contrôler avec AGPM, puis cliquez sur **contrôle**.</span><span class="sxs-lookup"><span data-stu-id="d2038-111">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="d2038-112">Si vous n’avez pas l’autorisation spéciale pour contrôler les objets de stratégie de groupe, vous devez en demander le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d2038-112">Unless you have special permission to control GPOs, you must submit a request for control.</span></span> <span data-ttu-id="d2038-113">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="d2038-113">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="d2038-114">Tapez un commentaire à afficher dans l' **historique** de l’objet de stratégie de groupe, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="d2038-114">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="d2038-115">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2038-115">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2038-116">L’objet de stratégie de groupe est supprimé de la liste sous l’onglet non **contrôlé** et ajouté à l’onglet **en attente** . Lorsqu’un approbateur a approuvé votre demande, l’objet de stratégie de groupe est déplacé vers l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="d2038-116">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="d2038-117">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="d2038-117">Additional considerations</span></span>

-   <span data-ttu-id="d2038-118">Par défaut, vous devez être un éditeur ou un relecteur pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="d2038-118">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="d2038-119">En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="d2038-119">Specifically, you must have **List Contents** and **Read Settings** permissions for the domain.</span></span>

-   <span data-ttu-id="d2038-120">Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**.</span><span class="sxs-lookup"><span data-stu-id="d2038-120">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="d2038-121">L’objet GPO sera renvoyé à l’onglet non **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="d2038-121">The GPO will be returned to the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="d2038-122">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="d2038-122">Additional references</span></span>

-   [<span data-ttu-id="d2038-123">Création, contrôle ou importation d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2038-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 






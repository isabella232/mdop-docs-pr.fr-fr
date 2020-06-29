---
title: Demander la création d'un objet de stratégie de groupe contrôlé
description: Demander la création d'un objet de stratégie de groupe contrôlé
author: dansimp
ms.assetid: e1875d81-8553-42ee-8f3a-023d6ced86ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7994e1af80c0ae32940d52955f7e5f773d1ee6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808257"
---
# <span data-ttu-id="0dc79-103">Demander la création d'un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="0dc79-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="0dc79-104">Si vous n’êtes pas un approbateur ou un administrateur AGPM (contrôle total), vous devez demander la création d’un objet de stratégie de groupe (objet de stratégie de groupe) s’il doit être géré à l’aide d’AGPM (Advanced Group Policy Management).</span><span class="sxs-lookup"><span data-stu-id="0dc79-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy object (GPO) if it is to be managed using Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="0dc79-105">Un compte d’utilisateur disposant de l’éditeur ou du rôle de réviseur ou des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="0dc79-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="0dc79-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0dc79-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="0dc79-107">Pour créer un nouvel objet de stratégie de groupe avec le contrôle de modification géré via AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc79-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="0dc79-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="0dc79-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="0dc79-109">Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.</span><span class="sxs-lookup"><span data-stu-id="0dc79-109">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="0dc79-110">Si vous n’avez pas l’autorisation spéciale pour créer des objets de stratégie de groupe, vous devez en créer une.</span><span class="sxs-lookup"><span data-stu-id="0dc79-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="0dc79-111">Dans la boîte de dialogue **nouvel objet GPO contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="0dc79-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="0dc79-112">Pour recevoir une copie de la demande, entrez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="0dc79-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="0dc79-113">Tapez un nom pour le nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="0dc79-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="0dc79-114">Facultatif: tapez un commentaire pour le nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="0dc79-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="0dc79-115">Pour déployer le nouvel objet GPO dans l’environnement de production immédiatement après approbation, cliquez sur **créer en direct**.</span><span class="sxs-lookup"><span data-stu-id="0dc79-115">To deploy the new GPO to the production environment immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="0dc79-116">Pour créer le nouvel objet GPO hors connexion sans le déployer immédiatement après approbation, cliquez sur créer un fichier **hors connexion**.</span><span class="sxs-lookup"><span data-stu-id="0dc79-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="0dc79-117">Sélectionnez le modèle d’objet de stratégie de groupe à utiliser comme point de départ pour le nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="0dc79-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="0dc79-118">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="0dc79-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="0dc79-119">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0dc79-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc79-120">Le nouvel objet GPO est affiché dans la liste des objets de stratégie de groupe de l’onglet **en attente** . Lorsqu’un approbateur a approuvé votre demande, l’objet de stratégie de groupe est déplacé vers l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="0dc79-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="0dc79-121">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="0dc79-121">Additional considerations</span></span>

-   <span data-ttu-id="0dc79-122">Par défaut, vous devez être un éditeur ou un relecteur pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="0dc79-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="0dc79-123">Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="0dc79-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="0dc79-124">Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**.</span><span class="sxs-lookup"><span data-stu-id="0dc79-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="0dc79-125">L’objet GPO sera détruit.</span><span class="sxs-lookup"><span data-stu-id="0dc79-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="0dc79-126">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0dc79-126">Additional references</span></span>

-   [<span data-ttu-id="0dc79-127">Création, contrôle ou importation d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="0dc79-127">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 






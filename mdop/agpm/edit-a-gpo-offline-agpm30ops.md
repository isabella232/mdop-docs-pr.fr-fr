---
title: Modifier un objet de stratégie de groupe hors connexion
description: Modifier un objet de stratégie de groupe hors connexion
author: dansimp
ms.assetid: 51677d8a-6209-41b5-82ed-4f3be817abc0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74b6ae9fdf11456a9a45cb5504ed97a9bc6aecb4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807581"
---
# <span data-ttu-id="9229a-103">Modifier un objet de stratégie de groupe hors connexion</span><span class="sxs-lookup"><span data-stu-id="9229a-103">Edit a GPO Offline</span></span>


<span data-ttu-id="9229a-104">Pour apporter des modifications à un objet de stratégie de groupe contrôlé (GPO), vous devez d’abord extraire une copie de l’objet GPO de l’archive.</span><span class="sxs-lookup"><span data-stu-id="9229a-104">To make changes to a controlled Group Policy Object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="9229a-105">Personne ne peut modifier l’objet de stratégie de groupe tant qu’il n’a pas été réintégré, ce qui empêche l’introduction de modifications conflictuelles de plusieurs administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9229a-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="9229a-106">Lorsque vous avez fini de modifier l’objet de stratégie de groupe, vous le consultez dans l’archive afin qu’il puisse être examiné et déployé dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="9229a-106">When you have finished modifying the GPO, you check it into the archive so that it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="9229a-107">Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe, ou un compte d’utilisateur disposant des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="9229a-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="9229a-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9229a-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="9229a-109">Modification d’un objet de stratégie de groupe hors connexion</span><span class="sxs-lookup"><span data-stu-id="9229a-109">Editing a GPO offline</span></span>


<span data-ttu-id="9229a-110">Pour modifier un objet de stratégie de groupe, vous pouvez extraire l’objet de stratégie de groupe à partir de l’archive, modifier l’objet de stratégie de groupe en mode hors connexion, puis vérifier l’objet GPO dans l’archive afin qu’il puisse être consulté et déployé (ou modifié par d’autres éditeurs).</span><span class="sxs-lookup"><span data-stu-id="9229a-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive so that it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="9229a-111">Extraire un objet de stratégie de groupe à partir de l’archive en vue de le modifier</span><span class="sxs-lookup"><span data-stu-id="9229a-111">Check out a GPO from the archive for editing</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="9229a-112">Modification d’un objet de stratégie de groupe hors connexion</span><span class="sxs-lookup"><span data-stu-id="9229a-112">Edit a GPO offline</span></span>](#bkmk-edit)

-   [<span data-ttu-id="9229a-113">Archiver un objet GPO dans l’archive</span><span class="sxs-lookup"><span data-stu-id="9229a-113">Check a GPO into the archive</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="9229a-114">Pour extraire un objet GPO de l’archive en vue de le modifier</span><span class="sxs-lookup"><span data-stu-id="9229a-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="9229a-115">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9229a-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9229a-116">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="9229a-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="9229a-117">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à modifier, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="9229a-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="9229a-118">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="9229a-118">Type a comment to be displayed in the History of the GPO while it is checked out, and then click **OK**.</span></span>

5.  <span data-ttu-id="9229a-119">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="9229a-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9229a-120">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est désormais identifié comme **extrait**.</span><span class="sxs-lookup"><span data-stu-id="9229a-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="9229a-121">Pour modifier un objet GPO hors connexion</span><span class="sxs-lookup"><span data-stu-id="9229a-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="9229a-122">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur l’objet de stratégie de groupe à modifier, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="9229a-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="9229a-123">Dans la fenêtre **éditeur de gestion des stratégies de groupe** , apporter des modifications à une copie hors connexion de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9229a-123">In the **Group Policy Management Editor** window, make changes to an offline copy of the GPO.</span></span>

    <span data-ttu-id="9229a-124">**Remarques**  Pour désactiver tous les paramètres de configuration de l’ordinateur ou tous les paramètres de configuration de l’utilisateur, cliquez avec le bouton droit sur l’objet dans la fenêtre **éditeur de gestion des stratégies de groupe** , puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="9229a-124">**Note** To disable all Computer Configuration settings or all User Configuration settings, right-click the GPO in the **Group Policy Management Editor** window and click **Properties**.</span></span> <span data-ttu-id="9229a-125">Sélectionnez **Désactiver les paramètres de configuration** de l’ordinateur ou **Désactiver les paramètres de configuration** de l’utilisateur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9229a-125">Select **Disable Computer Configuration settings** or **Disable User Configuration settings** as appropriate.</span></span>

     

3.  <span data-ttu-id="9229a-126">Lorsque vous avez terminé de modifier l’objet de stratégie de **groupe** , fermez la fenêtre Éditeur de gestion des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="9229a-126">When you have finished modifying the GPO, close the **Group Policy Management Editor** window.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="9229a-127">Pour archiver un objet GPO dans l’archive</span><span class="sxs-lookup"><span data-stu-id="9229a-127">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="9229a-128">Dans l’onglet **contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="9229a-128">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="9229a-129">Si vous n’avez apporté aucune modification à l’objet de stratégie de groupe, cliquez avec le bouton droit sur celui-ci, puis cliquez sur **Annuler l’extraction**, puis sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="9229a-129">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="9229a-130">Si vous avez apporté des modifications à l’objet de stratégie de groupe, cliquez avec le bouton droit sur celui-ci, puis cliquez sur **Archiver**.</span><span class="sxs-lookup"><span data-stu-id="9229a-130">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="9229a-131">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="9229a-131">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="9229a-132">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="9229a-132">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9229a-133">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.</span><span class="sxs-lookup"><span data-stu-id="9229a-133">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="9229a-134">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="9229a-134">Additional considerations</span></span>

-   <span data-ttu-id="9229a-135">Pour extraire et modifier un objet de stratégie de groupe, par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe, un éditeur ou un administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="9229a-135">To check out and edit a GPO, by default you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="9229a-136">Plus précisément, vous devez disposer du **contenu de liste** et des autorisations de **modification des paramètres** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9229a-136">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="9229a-137">En outre, pour modifier l’objet de stratégie de groupe, vous devez être la personne qui a extrait l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9229a-137">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="9229a-138">Pour archiver un objet de stratégie de groupe par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="9229a-138">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="9229a-139">Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres** ou les autorisations de l’objet de **stratégie** de groupe pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="9229a-139">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="9229a-140">Si vous n’êtes pas un approbateur ou un administrateur AGPM (ou un autre administrateur de stratégie de groupe ayant une autorisation de **déploiement d’objets** de stratégie de groupe), vous devez être l’éditeur qui a extrait l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9229a-140">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="9229a-141">Lors de la modification d’un objet de stratégie de groupe, toute mise à niveau de l’installation de logiciels de stratégie de groupe d’un package dans un autre objet de stratégie de groupe doit référencer l’objet de stratégie de groupe déployé et non la copie</span><span class="sxs-lookup"><span data-stu-id="9229a-141">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, and not the checked-out copy.</span></span>

### <span data-ttu-id="9229a-142">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9229a-142">Additional references</span></span>

-   [<span data-ttu-id="9229a-143">Modification d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9229a-143">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

-   <span data-ttu-id="9229a-144">Révision d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9229a-144">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="9229a-145">Vérifier les paramètres de l'objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9229a-145">Review GPO Settings</span></span>](review-gpo-settings-agpm30ops.md)

    -   [<span data-ttu-id="9229a-146">Vérifier les liens objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9229a-146">Review GPO Links</span></span>](review-gpo-links-agpm30ops.md)

    -   [<span data-ttu-id="9229a-147">Identifier les différences entre les objets de stratégie de groupe, les versions ou les modèles d'objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9229a-147">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md)

-   <span data-ttu-id="9229a-148">Déploiement d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9229a-148">Deploying a GPO</span></span>

    -   [<span data-ttu-id="9229a-149">Demander le déploiement d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9229a-149">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm30ops.md)

    -   [<span data-ttu-id="9229a-150">Déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9229a-150">Deploy a GPO</span></span>](deploy-a-gpo-agpm30ops.md)

 

 






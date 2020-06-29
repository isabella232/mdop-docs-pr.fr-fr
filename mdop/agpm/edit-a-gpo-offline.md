---
title: Modifier un objet de stratégie de groupe hors connexion
description: Modifier un objet de stratégie de groupe hors connexion
author: dansimp
ms.assetid: 4a148952-9fe9-4ec4-8df1-b25e37c97a54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6753ad21adb810e60e0b284204a61d4dd58c2384
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808486"
---
# <span data-ttu-id="bd7f0-103">Modifier un objet de stratégie de groupe hors connexion</span><span class="sxs-lookup"><span data-stu-id="bd7f0-103">Edit a GPO Offline</span></span>


<span data-ttu-id="bd7f0-104">Pour apporter des modifications à un objet de stratégie de groupe contrôlé (GPO), vous devez d’abord extraire une copie de l’objet GPO de l’archive.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-104">To make changes to a controlled Group Policy object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="bd7f0-105">Personne ne peut modifier l’objet de stratégie de groupe tant qu’il n’a pas été réintégré, ce qui empêche l’introduction de modifications conflictuelles de plusieurs administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="bd7f0-106">Lorsque vous avez fini de modifier l’objet de stratégie de groupe, vous le consultez dans l’archive, afin qu’il puisse être examiné et déployé dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-106">When you have finished modifying the GPO, you check it into the archive, so it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="bd7f0-107">Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe ou un compte d’utilisateur disposant des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="bd7f0-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="bd7f0-109">Modification d’un objet de stratégie de groupe hors connexion</span><span class="sxs-lookup"><span data-stu-id="bd7f0-109">Editing a GPO offline</span></span>


<span data-ttu-id="bd7f0-110">Pour modifier un objet de stratégie de groupe, vous pouvez extraire l’objet de stratégie de groupe à partir de l’archive, modifier l’objet de stratégie de groupe en mode hors connexion, puis vérifier l’objet GPO dans l’archive, afin qu’il puisse être consulté et déployé (ou modifié par d’autres éditeurs).</span><span class="sxs-lookup"><span data-stu-id="bd7f0-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive, so it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="bd7f0-111">Extraire un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-111">Check out a GPO</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="bd7f0-112">Modification d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-112">Edit a GPO</span></span>](#bkmk-edit)

-   [<span data-ttu-id="bd7f0-113">Archiver un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-113">Check in a GPO</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="bd7f0-114">Pour extraire un objet GPO de l’archive en vue de le modifier</span><span class="sxs-lookup"><span data-stu-id="bd7f0-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="bd7f0-115">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="bd7f0-116">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-116">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="bd7f0-117">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à modifier, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="bd7f0-118">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe pendant son extraction, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-118">Type a comment to be displayed in the History of the GPO while it is checked out, then click **OK**.</span></span>

5.  <span data-ttu-id="bd7f0-119">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="bd7f0-120">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est désormais identifié comme **extrait**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="bd7f0-121">Pour modifier un objet GPO hors connexion</span><span class="sxs-lookup"><span data-stu-id="bd7f0-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="bd7f0-122">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur l’objet de stratégie de groupe à modifier, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="bd7f0-123">Dans l' **éditeur d’objets de stratégie de groupe**, apporter des modifications à une copie hors connexion de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-123">In the **Group Policy Object Editor**, make changes to an offline copy of the GPO.</span></span>

3.  <span data-ttu-id="bd7f0-124">Lorsque vous avez terminé de modifier l’objet de stratégie de **groupe**, fermez l’éditeur d’objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-124">When you have finished modifying the GPO, close the **Group Policy Object Editor**.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="bd7f0-125">Pour archiver un objet GPO dans l’archive</span><span class="sxs-lookup"><span data-stu-id="bd7f0-125">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="bd7f0-126">Dans l’onglet **contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="bd7f0-126">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="bd7f0-127">Si vous n’avez apporté aucune modification à l’objet de stratégie de groupe, cliquez avec le bouton droit sur celui-ci, puis cliquez sur **Annuler l’extraction**, puis sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-127">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="bd7f0-128">Si vous avez apporté des modifications à l’objet de stratégie de groupe, cliquez avec le bouton droit sur celui-ci, puis cliquez sur **Archiver**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-128">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="bd7f0-129">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-129">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="bd7f0-130">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-130">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="bd7f0-131">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-131">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="bd7f0-132">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="bd7f0-132">Additional considerations</span></span>

-   <span data-ttu-id="bd7f0-133">Par défaut, pour extraire et modifier un objet de stratégie de groupe, vous devez être l’Approbateur ayant créé ou contrôlé l’objet de stratégie de groupe, un éditeur ou un administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="bd7f0-133">To check out and edit a GPO, by default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="bd7f0-134">Plus précisément, vous devez disposer du **contenu de liste** et des autorisations de **modification des paramètres** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-134">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="bd7f0-135">En outre, pour modifier l’objet de stratégie de groupe, vous devez être la personne qui a extrait l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-135">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="bd7f0-136">Pour archiver un objet de stratégie de groupe par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="bd7f0-136">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="bd7f0-137">Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres** ou les autorisations de l’objet de **stratégie** de groupe pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-137">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="bd7f0-138">Si vous n’êtes pas un approbateur ou un administrateur AGPM (ou un autre administrateur de stratégie de groupe ayant une autorisation de **déploiement d’objets** de stratégie de groupe), vous devez être l’éditeur qui a extrait l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-138">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="bd7f0-139">Lors de la modification d’un objet de stratégie de groupe, toute mise à niveau de l’installation de logiciels de stratégie de groupe d’un package dans un autre objet de stratégie de groupe doit référencer l’objet de stratégie de groupe déployé, et non</span><span class="sxs-lookup"><span data-stu-id="bd7f0-139">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, not the checked-out copy.</span></span>

### <span data-ttu-id="bd7f0-140">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="bd7f0-140">Additional references</span></span>

-   [<span data-ttu-id="bd7f0-141">Modification d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-141">Editing a GPO</span></span>](editing-a-gpo.md)

-   <span data-ttu-id="bd7f0-142">Révision d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-142">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="bd7f0-143">Vérifier les paramètres de l'objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-143">Review GPO Settings</span></span>](review-gpo-settings.md)

    -   [<span data-ttu-id="bd7f0-144">Vérifier les liens objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-144">Review GPO Links</span></span>](review-gpo-links.md)

    -   [<span data-ttu-id="bd7f0-145">Identifier les différences entre les objets de stratégie de groupe, les versions ou les modèles d'objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-145">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates.md)

-   <span data-ttu-id="bd7f0-146">Déploiement d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-146">Deploying a GPO</span></span>

    -   [<span data-ttu-id="bd7f0-147">Demander le déploiement d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-147">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo.md)

    -   [<span data-ttu-id="bd7f0-148">Déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-148">Deploy a GPO</span></span>](deploy-a-gpo.md)

 

 






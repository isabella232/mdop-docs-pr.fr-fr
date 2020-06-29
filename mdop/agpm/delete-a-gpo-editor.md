---
title: Supprimer un objet de stratégie de groupe
description: Supprimer un objet de stratégie de groupe
author: dansimp
ms.assetid: 66be3dde-653e-4c25-8cb7-00e7090c8d31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c27ddf87a12ed6010c481d93bfc85bb531f3d4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808521"
---
# <span data-ttu-id="2fe24-103">Supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2fe24-103">Delete a GPO</span></span>


<span data-ttu-id="2fe24-104">En tant qu’éditeur, il est possible que vous ne disposiez pas de l’autorisation de terminer la suppression d’un objet de stratégie de groupe, mais que vous disposez de l’autorisation nécessaire pour commencer le processus et transmettre votre demande à un approbateur.</span><span class="sxs-lookup"><span data-stu-id="2fe24-104">As an Editor, you may not have permission to complete the deletion of a Group Policy object (GPO), but you do have the permission necessary to begin the process and submit your request to an Approver.</span></span>

<span data-ttu-id="2fe24-105">Un compte d’utilisateur ayant le rôle d’éditeur ou les autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2fe24-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="2fe24-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2fe24-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2fe24-107">Pour demander la suppression d’un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="2fe24-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="2fe24-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2fe24-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2fe24-109">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="2fe24-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="2fe24-110">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à supprimer, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="2fe24-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="2fe24-111">Pour supprimer l’objet GPO de l’archive tout en laissant la version déployée de l’objet de stratégie de groupe intacte dans l’environnement de production, cliquez sur **Supprimer l’objet de stratégie de groupe à partir de l’archive uniquement (annuler le contrôle)**.</span><span class="sxs-lookup"><span data-stu-id="2fe24-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="2fe24-112">Pour supprimer l’objet GPO de l’environnement d’archivage et de production, cliquez sur **Supprimer l’objet GPO de l’archive et**de la production.</span><span class="sxs-lookup"><span data-stu-id="2fe24-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

        <span data-ttu-id="2fe24-113">Sauf si vous avez une autorisation spéciale pour supprimer des objets de stratégie de groupe, vous devez demander la suppression de l’objet de stratégie de groupe déployé.</span><span class="sxs-lookup"><span data-stu-id="2fe24-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="2fe24-114">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="2fe24-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="2fe24-115">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="2fe24-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

4.  <span data-ttu-id="2fe24-116">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2fe24-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="2fe24-117">L’objet de stratégie de groupe est affiché dans la liste des objets de stratégie de groupe de l’onglet **en attente** . Lorsqu’un approbateur a approuvé votre demande, l’objet de stratégie de groupe est déplacé de l’onglet **en attente** vers l’onglet **Corbeille** , où il peut être restauré ou détruit.</span><span class="sxs-lookup"><span data-stu-id="2fe24-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="2fe24-118">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="2fe24-118">Additional considerations</span></span>

-   <span data-ttu-id="2fe24-119">Par défaut, vous devez être un éditeur pour demander la suppression d’un objet de stratégie de groupe déployé.</span><span class="sxs-lookup"><span data-stu-id="2fe24-119">By default, you must be an Editor to request the deletion of a deployed GPO.</span></span> <span data-ttu-id="2fe24-120">Plus précisément, vous devez disposer du **contenu de liste** et des autorisations de **modification des paramètres** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2fe24-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="2fe24-121">Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour supprimer un objet GPO de l’archive.</span><span class="sxs-lookup"><span data-stu-id="2fe24-121">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="2fe24-122">Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres** ou supprimer des autorisations d' **objet** de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2fe24-122">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="2fe24-123">Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**.</span><span class="sxs-lookup"><span data-stu-id="2fe24-123">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="2fe24-124">L’objet GPO sera renvoyé à l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="2fe24-124">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="2fe24-125">Pour supprimer un objet GPO non contrôlé de l’environnement de production sans le contrôler d’abord, dans la **console de gestion des stratégies de groupe**, cliquez sur **forêt**, cliquez sur **domaines**, sur \*\* &lt; MyDomain &gt; \*\*, puis cliquez sur objets de stratégie de **groupe**.</span><span class="sxs-lookup"><span data-stu-id="2fe24-125">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="2fe24-126">Cliquez avec le bouton droit sur l’objet de stratégie de groupe non contrôlé, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="2fe24-126">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="2fe24-127">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2fe24-127">Additional references</span></span>

-   [<span data-ttu-id="2fe24-128">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="2fe24-128">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

 

 






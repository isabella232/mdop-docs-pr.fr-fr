---
title: Supprimer un objet de stratégie de groupe
description: Supprimer un objet de stratégie de groupe
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808525"
---
# <span data-ttu-id="00c7d-103">Supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="00c7d-103">Delete a GPO</span></span>


<span data-ttu-id="00c7d-104">Advanced Group Policy Management (AGPM) permet aux approbateurs de supprimer un objet de stratégie de groupe contrôlé (GPO) et de le déplacer vers la corbeille.</span><span class="sxs-lookup"><span data-stu-id="00c7d-104">Advanced Group Policy Management (AGPM) enables Approvers to delete a controlled Group Policy object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="00c7d-105">Un compte d’utilisateur ayant le rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="00c7d-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="00c7d-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="00c7d-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="00c7d-107">Pour supprimer un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="00c7d-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="00c7d-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="00c7d-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="00c7d-109">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="00c7d-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="00c7d-110">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à supprimer, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="00c7d-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="00c7d-111">Pour supprimer l’objet GPO de l’archive tout en laissant la version déployée de l’objet de stratégie de groupe intacte dans l’environnement de production, cliquez sur **Supprimer l’objet de stratégie de groupe à partir de l’archive uniquement (annuler le contrôle)**.</span><span class="sxs-lookup"><span data-stu-id="00c7d-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="00c7d-112">Pour supprimer l’objet GPO de l’environnement d’archivage et de production, cliquez sur **Supprimer l’objet GPO de l’archive et**de la production.</span><span class="sxs-lookup"><span data-stu-id="00c7d-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="00c7d-113">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="00c7d-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="00c7d-114">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="00c7d-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="00c7d-115">L’objet de stratégie de groupe est supprimé de l’onglet **contrôlé** et s’affiche sous l’onglet de la **Corbeille** , où il peut être restauré ou détruit.</span><span class="sxs-lookup"><span data-stu-id="00c7d-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="00c7d-116">Si l’objet de stratégie de groupe a été supprimé uniquement de l’archive, il apparaît également sous l’onglet non **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="00c7d-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="00c7d-117">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="00c7d-117">Additional considerations</span></span>

-   <span data-ttu-id="00c7d-118">Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour supprimer un objet de stratégie de groupe déployé.</span><span class="sxs-lookup"><span data-stu-id="00c7d-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to delete a deployed GPO.</span></span> <span data-ttu-id="00c7d-119">Plus précisément, vous devez disposer d’autorisations de **liste** et de **Suppression d’objets** de stratégie de groupe pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="00c7d-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="00c7d-120">Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour supprimer un objet GPO de l’archive.</span><span class="sxs-lookup"><span data-stu-id="00c7d-120">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="00c7d-121">Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres** ou supprimer des autorisations d' **objet** de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="00c7d-121">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="00c7d-122">Pour supprimer un objet GPO non contrôlé de l’environnement de production sans le contrôler d’abord, dans la **console de gestion des stratégies de groupe**, cliquez sur **forêt**, cliquez sur **domaines**, sur \*\* &lt; MyDomain &gt; \*\*, puis cliquez sur objets de stratégie de **groupe**.</span><span class="sxs-lookup"><span data-stu-id="00c7d-122">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="00c7d-123">Cliquez avec le bouton droit sur l’objet de stratégie de groupe non contrôlé, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="00c7d-123">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="00c7d-124">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="00c7d-124">Additional references</span></span>

-   [<span data-ttu-id="00c7d-125">Suppression, restauration ou destruction d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="00c7d-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 






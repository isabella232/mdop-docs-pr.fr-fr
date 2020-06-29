---
title: Supprimer un objet de stratégie de groupe contrôlé
description: Supprimer un objet de stratégie de groupe contrôlé
author: dansimp
ms.assetid: 2a461018-aa0b-4ae3-b079-efc554ca4a3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 103d2f7de9fa8055fdc57505e0e5ac4e0a50bbfa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808526"
---
# <span data-ttu-id="1cda1-103">Supprimer un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="1cda1-103">Delete a Controlled GPO</span></span>


<span data-ttu-id="1cda1-104">Les approbateurs peuvent supprimer un objet de stratégie de groupe contrôlé (GPO) et le déplacer vers la corbeille.</span><span class="sxs-lookup"><span data-stu-id="1cda1-104">Approvers can delete a controlled Group Policy Object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="1cda1-105">Un compte d’utilisateur disposant du rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="1cda1-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="1cda1-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="1cda1-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="1cda1-107">Pour supprimer un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="1cda1-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="1cda1-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="1cda1-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1cda1-109">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="1cda1-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="1cda1-110">Cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous voulez supprimer, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="1cda1-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="1cda1-111">Pour supprimer l’objet GPO de l’archive tout en laissant la version déployée de l’objet GPO intact dans l’environnement de production, cliquez sur **Supprimer l’objet GPO de l’archive uniquement**.</span><span class="sxs-lookup"><span data-stu-id="1cda1-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="1cda1-112">Pour supprimer l’objet GPO de l’environnement d’archivage et de production du domaine, cliquez sur **Supprimer l’objet GPO d’archive et de production**.</span><span class="sxs-lookup"><span data-stu-id="1cda1-112">To delete the GPO from both the archive and production environment of the domain, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="1cda1-113">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cda1-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="1cda1-114">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="1cda1-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="1cda1-115">L’objet de stratégie de groupe est supprimé de l’onglet **contrôlé** et s’affiche sous l’onglet de la **Corbeille** , où il peut être restauré ou détruit.</span><span class="sxs-lookup"><span data-stu-id="1cda1-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="1cda1-116">Si l’objet de stratégie de groupe a été supprimé uniquement de l’archive, il apparaît également sous l’onglet non **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="1cda1-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="1cda1-117">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="1cda1-117">Additional considerations</span></span>

-   <span data-ttu-id="1cda1-118">Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="1cda1-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="1cda1-119">Plus précisément, vous devez disposer d’autorisations de **liste** et de **Suppression d’objets** de stratégie de groupe pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="1cda1-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="1cda1-120">Pour supprimer un objet GPO non contrôlé de l’environnement de production sans le contrôler d’abord, dans la **console de gestion des stratégies de groupe**, cliquez sur **forêt**, cliquez sur **domaines**, sur \*\* &lt; MyDomain &gt; \*\*, puis cliquez sur objets de stratégie de **groupe**.</span><span class="sxs-lookup"><span data-stu-id="1cda1-120">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="1cda1-121">Cliquez avec le bouton droit sur l’objet de stratégie de groupe non contrôlé, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="1cda1-121">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="1cda1-122">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="1cda1-122">Additional references</span></span>

-   [<span data-ttu-id="1cda1-123">Suppression, restauration ou destruction d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="1cda1-123">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

 

 






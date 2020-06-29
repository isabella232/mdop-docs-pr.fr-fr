---
title: Détruire un objet de stratégie de groupe
description: Détruire un objet de stratégie de groupe
author: dansimp
ms.assetid: d74941a3-beef-46cd-a4ca-80a324dcfadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5545918c417fce16bfc2369ebc6fc2199390adc6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807590"
---
# <span data-ttu-id="751ec-103">Détruire un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="751ec-103">Destroy a GPO</span></span>


<span data-ttu-id="751ec-104">La gestion avancée de la stratégie de groupe permet aux approbateurs de détruire un objet de stratégie de groupe, de le supprimer de la corbeille et de le supprimer définitivement pour qu’il ne puisse plus être restauré.</span><span class="sxs-lookup"><span data-stu-id="751ec-104">Advanced Group Policy Management (AGPM) enables Approvers to destroy a Group Policy object (GPO), removing it from the Recycle Bin and permanently deleting it so that it can no longer be restored.</span></span>

<span data-ttu-id="751ec-105">Un compte d’utilisateur ayant le rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="751ec-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="751ec-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="751ec-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="751ec-107">Pour supprimer définitivement un objet GPO de sorte qu’il ne puisse plus être restauré</span><span class="sxs-lookup"><span data-stu-id="751ec-107">To permanently delete a GPO so it can no longer be restored</span></span>**

1.  <span data-ttu-id="751ec-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="751ec-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="751ec-109">Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.</span><span class="sxs-lookup"><span data-stu-id="751ec-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="751ec-110">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à supprimer, puis cliquez sur **détruire**.</span><span class="sxs-lookup"><span data-stu-id="751ec-110">Right-click the GPO to destroy, and then click **Destroy**.</span></span>

4.  <span data-ttu-id="751ec-111">Cliquez sur **Oui** pour confirmer que vous voulez supprimer définitivement l’objet de stratégie de groupe sélectionné et toutes les sauvegardes de l’archive.</span><span class="sxs-lookup"><span data-stu-id="751ec-111">Click **Yes** to confirm that you want to permanently delete the selected GPO and all backups from the archive.</span></span>

5.  <span data-ttu-id="751ec-112">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="751ec-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="751ec-113">L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et est supprimé de manière définitive.</span><span class="sxs-lookup"><span data-stu-id="751ec-113">The GPO is removed from the **Recycle Bin** tab and is permanently deleted.</span></span>

### <span data-ttu-id="751ec-114">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="751ec-114">Additional considerations</span></span>

-   <span data-ttu-id="751ec-115">Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="751ec-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="751ec-116">Plus précisément, vous devez disposer d’autorisations de **liste** et de **Suppression d’objets** de stratégie de groupe pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="751ec-116">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="751ec-117">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="751ec-117">Additional references</span></span>

-   [<span data-ttu-id="751ec-118">Suppression, restauration ou destruction d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="751ec-118">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 






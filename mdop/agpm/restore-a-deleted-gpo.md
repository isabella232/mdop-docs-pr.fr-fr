---
title: Restaurer un objet de stratégie de groupe supprimé
description: Restaurer un objet de stratégie de groupe supprimé
author: dansimp
ms.assetid: e6953296-7b7d-4d1e-ad82-d4a23044cdd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2cba097ecd651a91f828901d8115a7020d6da819
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807497"
---
# <span data-ttu-id="7bdbd-103">Restaurer un objet de stratégie de groupe supprimé</span><span class="sxs-lookup"><span data-stu-id="7bdbd-103">Restore a Deleted GPO</span></span>


<span data-ttu-id="7bdbd-104">Gestion de la stratégie de groupe avancée (AGPM) permet aux approbateurs de restaurer un objet de stratégie de groupe supprimé de la corbeille, en le renvoyant à l’archive.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-104">Advanced Group Policy Management (AGPM) enables Approvers to restore a deleted Group Policy object (GPO) from the Recycle Bin, returning it to the archive.</span></span>

<span data-ttu-id="7bdbd-105">Un compte d’utilisateur ayant le rôle d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-105">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="7bdbd-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="7bdbd-107">Pour restaurer un objet de stratégie de groupe supprimé</span><span class="sxs-lookup"><span data-stu-id="7bdbd-107">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="7bdbd-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="7bdbd-109">Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="7bdbd-110">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à restaurer, puis cliquez sur **restaurer**.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-110">Right-click the GPO to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="7bdbd-111">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="7bdbd-112">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7bdbd-113">L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="7bdbd-113">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="7bdbd-114">**Remarques**  Si un objet de stratégie de groupe a été supprimé de l’environnement de production, sa restauration sur l’archive ne le redéploiera pas automatiquement dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-114">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="7bdbd-115">Pour renvoyer l’objet GPO vers l’environnement de production, déployez l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-115">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="7bdbd-116">Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="7bdbd-116">For information, see [Deploy a GPO](deploy-a-gpo.md).</span></span>

 

### <span data-ttu-id="7bdbd-117">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="7bdbd-117">Additional considerations</span></span>

-   <span data-ttu-id="7bdbd-118">Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="7bdbd-119">Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres**, déployer l’objet de stratégie de **groupe**ou **supprimer** des autorisations d’objet GPO pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="7bdbd-119">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="7bdbd-120">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="7bdbd-120">Additional references</span></span>

-   [<span data-ttu-id="7bdbd-121">Suppression, restauration ou destruction d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7bdbd-121">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 






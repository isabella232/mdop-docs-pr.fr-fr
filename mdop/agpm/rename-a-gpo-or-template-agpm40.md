---
title: Renommer un objet de stratégie de groupe ou un modèle
description: Renommer un objet de stratégie de groupe ou un modèle
author: dansimp
ms.assetid: 84293f7a-4ff7-497e-bdbc-cabb70189a03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 642622ae0242e614733e8f33ea5840c8b6758db8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807537"
---
# <span data-ttu-id="f5bb2-103">Renommer un objet de stratégie de groupe ou un modèle</span><span class="sxs-lookup"><span data-stu-id="f5bb2-103">Rename a GPO or Template</span></span>


<span data-ttu-id="f5bb2-104">Vous pouvez renommer un objet de stratégie de groupe contrôlé (GPO) ou un modèle.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-104">You can rename a controlled Group Policy Object (GPO) or a template.</span></span>

<span data-ttu-id="f5bb2-105">Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe, ou un compte d’utilisateur disposant des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-105">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="f5bb2-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f5bb2-107">Pour renommer un objet ou un modèle d’objet</span><span class="sxs-lookup"><span data-stu-id="f5bb2-107">To rename a GPO or template</span></span>**

1.  <span data-ttu-id="f5bb2-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f5bb2-109">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** ou **modèles** pour afficher l’élément à renommer.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-109">On the **Contents** tab, click the **Controlled** or **Templates** tab to display the item to rename.</span></span>

3.  <span data-ttu-id="f5bb2-110">Cliquez avec le bouton droit sur l’objet ou le modèle à renommer, puis cliquez sur **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-110">Right-click the GPO or template to rename and click **Rename**.</span></span>

4.  <span data-ttu-id="f5bb2-111">Tapez le nouveau nom de l’objet GPO ou du modèle, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-111">Type the new name for the GPO or template and a comment, and then click **OK**.</span></span>

5.  <span data-ttu-id="f5bb2-112">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f5bb2-113">L’objet ou le modèle s’affiche sous le nouveau nom dans l’onglet **contenu** .</span><span class="sxs-lookup"><span data-stu-id="f5bb2-113">The GPO or template appears under the new name on the **Contents** tab.</span></span>

### <span data-ttu-id="f5bb2-114">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="f5bb2-114">Additional considerations</span></span>

-   <span data-ttu-id="f5bb2-115">Par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe, un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-115">By default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="f5bb2-116">En particulier, vous devez disposer du **contenu de liste** et de l’autorisation de **modification des paramètres** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-116">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="f5bb2-117">Lorsque vous renommez un objet de stratégie de groupe qui a été déployé, le nom est immédiatement modifié dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-117">When you rename a GPO that has been deployed, the name is immediately changed in the archive.</span></span> <span data-ttu-id="f5bb2-118">Le nom est modifié dans l’environnement de production uniquement lorsque l’objet de stratégie de groupe est redéployé.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-118">The name is changed in the production environment only when the GPO is redeployed.</span></span> <span data-ttu-id="f5bb2-119">Tant que l’objet de stratégie de groupe n’est pas redéployé (ou la copie de production est supprimée), l’ancien nom est toujours utilisé dans l’environnement de production et ne peut donc pas être utilisé pour un autre objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-119">Until the GPO is redeployed (or the production copy is deleted), the old name is still in use in the production environment and therefore cannot be used for another GPO.</span></span> <span data-ttu-id="f5bb2-120">De même, l’objet de stratégie de groupe dans l’archive ne peut pas renommer son nom d’origine tant qu’il n’a pas été déployé (en changeant le nom de la copie de production) ou que la copie de production a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="f5bb2-120">Likewise, the GPO in the archive cannot be renamed back to its original name until the GPO has been deployed (changing the name of the production copy) or the production copy has been deleted.</span></span>

### <span data-ttu-id="f5bb2-121">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f5bb2-121">Additional references</span></span>

-   [<span data-ttu-id="f5bb2-122">Modification d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="f5bb2-122">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

 

 






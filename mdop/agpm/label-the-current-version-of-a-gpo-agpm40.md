---
title: Étiqueter la version actuelle d'un objet de stratégie de groupe
description: Étiqueter la version actuelle d'un objet de stratégie de groupe
author: dansimp
ms.assetid: cadc8769-21da-44b0-8122-6cafdb448913
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b15a4d3ee006fb37db4ce7362a2f5c92d7c233e5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808397"
---
# <span data-ttu-id="5cc95-103">Étiqueter la version actuelle d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5cc95-103">Label the Current Version of a GPO</span></span>


<span data-ttu-id="5cc95-104">Vous pouvez étiqueter la version actuelle d’un objet de stratégie de groupe pour faciliter l’identification de son historique.</span><span class="sxs-lookup"><span data-stu-id="5cc95-104">You can label the current version of a Group Policy Object (GPO) for easy identification in its history.</span></span> <span data-ttu-id="5cc95-105">Vous pouvez utiliser une étiquette pour identifier une version correcte connue vers laquelle vous pouvez revenir en cas de problème.</span><span class="sxs-lookup"><span data-stu-id="5cc95-105">You can use a label to identify a known good version to which you could roll back if a problem occurs.</span></span> <span data-ttu-id="5cc95-106">Par ailleurs, en attribuant une étiquette à plusieurs objets de stratégie de groupe avec la même étiquette à la fois, vous pouvez marquer les objets de stratégie de groupe associés qui doivent être restaurés au même point si la restauration doit être nécessaire ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="5cc95-106">Also, by labeling multiple GPOs with the same label at one time, you can mark related GPOs that should be rolled back to the same point if rollback should later be necessary.</span></span>

<span data-ttu-id="5cc95-107">Un compte d’utilisateur ayant le rôle d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="5cc95-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="5cc95-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5cc95-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="5cc95-109">Pour étiqueter la version actuelle d’objets de stratégie de groupe dans leur historique</span><span class="sxs-lookup"><span data-stu-id="5cc95-109">To label the current version of GPOs in their histories</span></span>**

1.  <span data-ttu-id="5cc95-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5cc95-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5cc95-111">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="5cc95-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="5cc95-112">Cliquez sur un objet de stratégie de groupe pour lequel étiqueter la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="5cc95-112">Click a GPO for which to label the current version.</span></span> <span data-ttu-id="5cc95-113">Pour sélectionner plusieurs objets de stratégie de groupe, appuyez sur Maj et cliquez sur le dernier objet GPO d’un groupe contigu d’objets de stratégie de groupe, ou appuyez sur CTRL et cliquez sur objets de stratégie de groupe individuels.</span><span class="sxs-lookup"><span data-stu-id="5cc95-113">To select multiple GPOs, press SHIFT and click the last GPO in a contiguous group of GPOs, or press CTRL and click individual GPOs.</span></span> <span data-ttu-id="5cc95-114">Cliquez avec le bouton droit sur un objet de stratégie de groupe sélectionné, puis cliquez sur **étiquette**.</span><span class="sxs-lookup"><span data-stu-id="5cc95-114">Right-click a selected GPO, and then click **Label**.</span></span>

4.  <span data-ttu-id="5cc95-115">Tapez une étiquette et un commentaire à afficher dans l’historique de chaque GPO sélectionné, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cc95-115">Type a label and a comment to be displayed in the history of each GPO selected, and then click **OK**.</span></span>

5.  <span data-ttu-id="5cc95-116">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="5cc95-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

### <span data-ttu-id="5cc95-117">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="5cc95-117">Additional considerations</span></span>

-   <span data-ttu-id="5cc95-118">Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="5cc95-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="5cc95-119">Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres** ou les autorisations de l’objet de **stratégie** de groupe pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="5cc95-119">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="5cc95-120">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="5cc95-120">Additional references</span></span>

-   [<span data-ttu-id="5cc95-121">Modification d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5cc95-121">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

 

 






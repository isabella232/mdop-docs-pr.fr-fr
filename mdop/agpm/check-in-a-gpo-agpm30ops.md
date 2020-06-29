---
title: Enregistrer un objet de stratégie de groupe
description: Enregistrer un objet de stratégie de groupe
author: dansimp
ms.assetid: 437397db-c94b-4940-b1a4-05442619ebee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c37144cb7c2d150d46dd1172a37717743f76ee3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807806"
---
# <span data-ttu-id="c0a4b-103">Enregistrer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c0a4b-103">Check In a GPO</span></span>


<span data-ttu-id="c0a4b-104">En règle générale, les éditeurs doivent vérifier les objets de stratégie de groupe qu’ils ont modifiés lorsque leurs modifications sont terminées.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-104">Ordinarily, Editors should check in Group Policy Objects (GPOs) that they have edited when their modifications are complete.</span></span> <span data-ttu-id="c0a4b-105">(Pour plus d’informations, voir [modifier un objet GPO hors connexion](edit-a-gpo-offline-agpm30ops.md).) Toutefois, si l’éditeur n’est pas disponible, un approbateur peut également archiver un objet GPO.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-105">(For details, see [Edit a GPO Offline](edit-a-gpo-offline-agpm30ops.md).) However, if the Editor is unavailable, an Approver can also check in a GPO.</span></span>

<span data-ttu-id="c0a4b-106">Un compte d’utilisateur ayant le rôle d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-106">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="c0a4b-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="c0a4b-108">Pour archiver un objet de stratégie de groupe qui a été extrait par un éditeur</span><span class="sxs-lookup"><span data-stu-id="c0a4b-108">To check in a GPO that has been checked out by an Editor</span></span>**

1.  <span data-ttu-id="c0a4b-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c0a4b-110">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

    -   <span data-ttu-id="c0a4b-111">Pour annuler les modifications apportées par l’éditeur, cliquez avec le bouton droit sur l’objet, cliquez sur **Annuler l’extraction**, puis sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-111">To discard any changes made by the Editor, right-click the GPO, click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="c0a4b-112">Pour conserver les modifications apportées par l’éditeur, cliquez avec le bouton droit sur l’objet, puis cliquez sur **Archiver**.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-112">To retain changes made by the Editor, right-click the GPO and then click **Check In**.</span></span>

3.  <span data-ttu-id="c0a4b-113">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-113">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="c0a4b-114">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c0a4b-115">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-115">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="c0a4b-116">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="c0a4b-116">Additional considerations</span></span>

-   <span data-ttu-id="c0a4b-117">Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-117">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="c0a4b-118">Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres** ou les autorisations de l’objet de **stratégie** de groupe pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-118">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="c0a4b-119">Si vous n’êtes pas un approbateur ou un administrateur AGPM (ou un autre administrateur de stratégie de groupe ayant une autorisation de **déploiement d’objets** de stratégie de groupe), vous devez être l’éditeur qui a extrait l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c0a4b-119">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

### <span data-ttu-id="c0a4b-120">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c0a4b-120">Additional references</span></span>

-   [<span data-ttu-id="c0a4b-121">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="c0a4b-121">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="c0a4b-122">Modifier un objet de stratégie de groupe hors connexion</span><span class="sxs-lookup"><span data-stu-id="c0a4b-122">Edit a GPO Offline</span></span>](edit-a-gpo-offline-agpm30ops.md)

 

 






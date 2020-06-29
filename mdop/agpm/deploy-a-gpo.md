---
title: Déployer un objet de stratégie de groupe
description: Déployer un objet de stratégie de groupe
author: dansimp
ms.assetid: a0a3f292-e3ab-46ae-a0fd-d7b2b4ad8883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a98bdd758937d86cf8c30c5abf0b49302d377360
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807610"
---
# <span data-ttu-id="6f6b7-103">Déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="6f6b7-103">Deploy a GPO</span></span>


<span data-ttu-id="6f6b7-104">La gestion avancée de la stratégie de groupe permet à un approbateur de déployer un objet de stratégie de groupe nouveau ou modifié dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-104">Advanced Group Policy Management (AGPM) enables an Approver to deploy a new or edited Group Policy object (GPO) to the production environment.</span></span> <span data-ttu-id="6f6b7-105">Pour plus d’informations sur le redéploiement d’une version antérieure d’un objet de stratégie de groupe, voir [restaurer une version précédente d’un objet de stratégie de groupe](roll-back-to-a-previous-version-of-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="6f6b7-105">For information about redeploying a previous version of a GPO, see [Roll Back to a Previous Version of a GPO](roll-back-to-a-previous-version-of-a-gpo.md).</span></span>

<span data-ttu-id="6f6b7-106">Un compte d’utilisateur ayant le rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="6f6b7-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="6f6b7-108">Pour déployer un objet de stratégie de groupe dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="6f6b7-108">To deploy a GPO to the production environment</span></span>**

1.  <span data-ttu-id="6f6b7-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="6f6b7-110">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="6f6b7-111">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à déployer, puis cliquez sur **déployer**.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-111">Right-click the GPO to be deployed and then click **Deploy**.</span></span>

4.  <span data-ttu-id="6f6b7-112">Pour examiner les liens d’objets de stratégie de groupe, cliquez sur **avancé**.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-112">To review links to the GPO, click **Advanced**.</span></span> <span data-ttu-id="6f6b7-113">Placez le pointeur de la souris sur un nœud dans l’arborescence pour afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-113">Pause the mouse pointer on a node in the tree to display details.</span></span>

    -   <span data-ttu-id="6f6b7-114">Par défaut, tous les liens vers l’objet GPO sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="6f6b7-115">Pour empêcher la restauration d’un lien, désactivez la case à cocher en regard de ce lien.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="6f6b7-116">Pour empêcher la restauration de tous les liens, décochez la case **restaurer les liaisons** dans la boîte de dialogue **déployer l’objet GPO** .</span><span class="sxs-lookup"><span data-stu-id="6f6b7-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="6f6b7-117">Cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-117">Click **Yes**.</span></span> <span data-ttu-id="6f6b7-118">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-118">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

<span data-ttu-id="6f6b7-119">**Remarques**  Pour vérifier si la version la plus récente d’un objet de stratégie de groupe a été déployée, dans l’onglet **contrôlé** , double-cliquez sur l’objet de stratégie de groupe pour afficher son **historique**.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-119">**Note** To verify whether the most recent version of a GPO has been deployed, on the **Controlled** tab, double-click the GPO to display its **History**.</span></span> <span data-ttu-id="6f6b7-120">Dans l' **historique** de l’objet de stratégie de groupe, la colonne **État** indique s’il s’agit d’un objet de stratégie de groupe déployé.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-120">In the **History** for the GPO, the **State** column indicates whether a GPO has been deployed.</span></span>

 

### <span data-ttu-id="6f6b7-121">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="6f6b7-121">Additional considerations</span></span>

-   <span data-ttu-id="6f6b7-122">Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-122">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="6f6b7-123">Plus précisément, vous devez disposer du **contenu de liste** et déployer des autorisations d' **objet** de stratégie de groupe pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="6f6b7-123">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="6f6b7-124">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6f6b7-124">Additional references</span></span>

-   [<span data-ttu-id="6f6b7-125">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="6f6b7-125">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

 

 






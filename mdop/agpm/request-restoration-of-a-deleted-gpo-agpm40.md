---
title: Demander la restauration d'un objet de stratégie de groupe supprimé
description: Demander la restauration d'un objet de stratégie de groupe supprimé
author: dansimp
ms.assetid: bac5ca3b-be47-49b5-bf1b-96280625fda8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 606690554ca1f813e1c20787bca59cfe2de6432d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808281"
---
# <span data-ttu-id="ab0bf-103">Demander la restauration d'un objet de stratégie de groupe supprimé</span><span class="sxs-lookup"><span data-stu-id="ab0bf-103">Request Restoration of a Deleted GPO</span></span>


<span data-ttu-id="ab0bf-104">Sauf si vous êtes un approbateur ou un administrateur AGPM (contrôle total), vous devez demander la restauration d’un objet de stratégie de groupe (GPO) supprimé de la corbeille.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the restoration of a deleted Group Policy Object (GPO) from the Recycle Bin to return it to the archive.</span></span>

<span data-ttu-id="ab0bf-105">Un compte d’utilisateur ayant le rôle d’éditeur ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ab0bf-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ab0bf-107">Pour demander la restauration d’un objet de stratégie de groupe supprimé</span><span class="sxs-lookup"><span data-stu-id="ab0bf-107">To request the restoration of a deleted GPO</span></span>**

1.  <span data-ttu-id="ab0bf-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ab0bf-109">Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="ab0bf-110">Cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous voulez restaurer, puis cliquez sur **restaurer**.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-110">Right-click the GPO you want to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="ab0bf-111">Sauf si vous disposez d’une autorisation spéciale pour restaurer des objets de stratégie de groupe, vous devez demander la restauration de l’objet de stratégie de groupe supprimé.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-111">Unless you have special permission to restore GPOs, you must submit a request for restoration of the deleted GPO.</span></span> <span data-ttu-id="ab0bf-112">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="ab0bf-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="ab0bf-113">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-113">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="ab0bf-114">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ab0bf-115">L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="ab0bf-115">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="ab0bf-116">**Remarques**  Si un objet de stratégie de groupe a été supprimé de l’environnement de production, sa restauration sur l’archive ne le redéploiera pas automatiquement dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-116">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="ab0bf-117">Pour renvoyer l’objet GPO vers l’environnement de production, déployez l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-117">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="ab0bf-118">Pour plus d’informations, voir [demander le déploiement d’un objet de stratégie de groupe](request-deployment-of-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ab0bf-118">For information, see [Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md).</span></span>

 

### <span data-ttu-id="ab0bf-119">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="ab0bf-119">Additional considerations</span></span>

-   <span data-ttu-id="ab0bf-120">Par défaut, vous devez être un éditeur pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-120">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="ab0bf-121">En particulier, vous devez disposer du **contenu de liste** et de l’autorisation de **modification des paramètres** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-121">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="ab0bf-122">Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-122">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="ab0bf-123">L’objet GPO sera renvoyé à l’onglet **Corbeille** .</span><span class="sxs-lookup"><span data-stu-id="ab0bf-123">The GPO will be returned to the **Recycle Bin** tab.</span></span>

### <span data-ttu-id="ab0bf-124">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ab0bf-124">Additional references</span></span>

-   [<span data-ttu-id="ab0bf-125">Suppression ou restauration d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ab0bf-125">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

 

 






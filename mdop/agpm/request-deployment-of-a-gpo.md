---
title: Demander le déploiement d'un objet de stratégie de groupe
description: Demander le déploiement d'un objet de stratégie de groupe
author: dansimp
ms.assetid: 9aa9af29-4754-4f72-b624-bb3e1087cbe1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a9e5fdbbd352adb6d542932c7180c513cfac8b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808282"
---
# <span data-ttu-id="727fc-103">Demander le déploiement d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="727fc-103">Request Deployment of a GPO</span></span>


<span data-ttu-id="727fc-104">Une fois que vous avez modifié et archivé un objet de stratégie de groupe, vous devez le déployer pour qu’il prenne effet dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="727fc-104">After you have modified and checked in a Group Policy object (GPO), deploy the GPO, so it will take effect in the production environment.</span></span>

<span data-ttu-id="727fc-105">Un compte d’utilisateur ayant le rôle d’éditeur ou les autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="727fc-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="727fc-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="727fc-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="727fc-107">Pour demander le déploiement d’un objet de stratégie de groupe dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="727fc-107">To request the deployment of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="727fc-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="727fc-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="727fc-109">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="727fc-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="727fc-110">Cliquez avec le bouton droit sur l’objet de stratégie de groupe à déployer, puis cliquez sur **déployer**.</span><span class="sxs-lookup"><span data-stu-id="727fc-110">Right-click the GPO to be deployed, and then click **Deploy**.</span></span>

4.  <span data-ttu-id="727fc-111">À moins que vous ne soyez un approbateur ou un administrateur AGPM ou que vous ne disposiez pas des autorisations spéciales pour déployer des objets de stratégie de groupe, vous devez demander un déploiement.</span><span class="sxs-lookup"><span data-stu-id="727fc-111">Unless you are an Approver or AGPM Administrator or have special permission to deploy GPOs, you must submit a request for deployment.</span></span> <span data-ttu-id="727fc-112">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="727fc-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="727fc-113">Tapez un commentaire à afficher dans l' **historique** de l’objet de stratégie de groupe, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="727fc-113">Type a comment to be displayed in the **History** for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="727fc-114">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="727fc-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="727fc-115">L’objet de stratégie de groupe est affiché dans la liste des objets de stratégie de groupe de l’onglet **en attente** . Lorsqu’un approbateur a approuvé votre demande, l’objet GPO est déplacé de l’onglet **en attente** vers l’onglet **contrôlé** et sera déployé.</span><span class="sxs-lookup"><span data-stu-id="727fc-115">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Controlled** tab and be deployed.</span></span>

### <span data-ttu-id="727fc-116">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="727fc-116">Additional considerations</span></span>

-   <span data-ttu-id="727fc-117">Par défaut, vous devez être un éditeur pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="727fc-117">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="727fc-118">Plus précisément, vous devez disposer du **contenu de liste** et des autorisations de **modification des paramètres** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="727fc-118">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="727fc-119">Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**.</span><span class="sxs-lookup"><span data-stu-id="727fc-119">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="727fc-120">L’objet GPO sera renvoyé à l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="727fc-120">The GPO will be returned to the **Controlled** tab.</span></span>

### <span data-ttu-id="727fc-121">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="727fc-121">Additional references</span></span>

-   [<span data-ttu-id="727fc-122">Modification d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="727fc-122">Editing a GPO</span></span>](editing-a-gpo.md)

 

 






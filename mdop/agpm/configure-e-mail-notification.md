---
title: Configurer la notification par courrier électronique
description: Configurer la notification par courrier électronique
author: dansimp
ms.assetid: 6e152de0-4376-4963-8d1a-3e7f5866d30f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e8d00c2446a0185de30bbd1f39a7e3eaf90080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807722"
---
# <span data-ttu-id="e96d3-103">Configurer la notification par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="e96d3-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="e96d3-104">Lorsqu’un éditeur ou un relecteur tente de créer, de déployer ou de supprimer un objet de stratégie de groupe (GPO), une demande de cette action est envoyée à une ou des adresses de messagerie désignées de telle sorte qu’un approbateur puisse évaluer la demande et l’implémenter ou la refuser.</span><span class="sxs-lookup"><span data-stu-id="e96d3-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="e96d3-105">Vous déterminez l’adresse ou les adresses de messagerie à laquelle les notifications sont envoyées, ainsi que l’alias à partir duquel les notifications sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="e96d3-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="e96d3-106">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="e96d3-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="e96d3-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e96d3-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="e96d3-108">Pour configurer les notifications par courrier électronique pour AGPM</span><span class="sxs-lookup"><span data-stu-id="e96d3-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="e96d3-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e96d3-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e96d3-110">Dans le volet Détails, cliquez sur l’onglet **délégation de domaine** .</span><span class="sxs-lookup"><span data-stu-id="e96d3-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="e96d3-111">Dans le champ **de** , tapez l’alias de messagerie pour AGPM à partir duquel envoyer les notifications.</span><span class="sxs-lookup"><span data-stu-id="e96d3-111">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="e96d3-112">Dans le champ **à** , entrez une liste délimitée par des virgules des adresses de courrier des approbateurs qui doivent recevoir des demandes d’approbation.</span><span class="sxs-lookup"><span data-stu-id="e96d3-112">In the **To** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="e96d3-113">Dans le champ **serveur SMTP** , tapez un serveur de messagerie SMTP valide.</span><span class="sxs-lookup"><span data-stu-id="e96d3-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="e96d3-114">Dans les champs **nom d’utilisateur** et **mot de passe** , tapez les informations d’identification d’un utilisateur ayant accès au service SMTP.</span><span class="sxs-lookup"><span data-stu-id="e96d3-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="e96d3-115">Cliquez sur **Apply** (Appliquer).</span><span class="sxs-lookup"><span data-stu-id="e96d3-115">Click **Apply**.</span></span>

### <span data-ttu-id="e96d3-116">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="e96d3-116">Additional considerations</span></span>

-   <span data-ttu-id="e96d3-117">Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="e96d3-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e96d3-118">En particulier, vous devez disposer du **contenu de liste** et des autorisations de **modification des options** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="e96d3-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="e96d3-119">La notification par courrier électronique pour AGPM est un paramètre au niveau du domaine.</span><span class="sxs-lookup"><span data-stu-id="e96d3-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="e96d3-120">Vous pouvez fournir différentes adresses de messagerie d’approbateur ou alias de messagerie d’AGPM sur l’onglet **délégation de domaine** de chaque domaine, ou utiliser les mêmes adresses de messagerie dans l’ensemble de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="e96d3-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

### <span data-ttu-id="e96d3-121">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e96d3-121">Additional references</span></span>

-   [<span data-ttu-id="e96d3-122">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="e96d3-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 






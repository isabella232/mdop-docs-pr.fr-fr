---
title: Exécution de tâches d'éditeur
description: Exécution de tâches d'éditeur
author: dansimp
ms.assetid: 81976a01-2a95-4256-b703-9fb3c884ef34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8e23bb91d8762d19eed9ae817967ba5a57505a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808294"
---
# <span data-ttu-id="7ff6a-103">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="7ff6a-103">Performing Editor Tasks</span></span>


<span data-ttu-id="7ff6a-104">Dans Advanced Group Policy Management (AGPM), un éditeur est une personne autorisée par un administrateur AGPM (contrôle total) pour modifier les objets de stratégie de groupe (GPO) et créer des modèles d’objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7ff6a-104">In Advanced Group Policy Management (AGPM), an Editor is a person authorized by an AGPM Administrator (Full Control) to change Group Policy Objects (GPOs) and create GPO templates.</span></span> <span data-ttu-id="7ff6a-105">Par ailleurs, un éditeur peut demander la création, la suppression et la restauration d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7ff6a-105">Additionally, an Editor can request that a GPO be created, deleted, or restored.</span></span> <span data-ttu-id="7ff6a-106">Un approbateur doit approuver la demande d’implémentation du programme.</span><span class="sxs-lookup"><span data-stu-id="7ff6a-106">An Approver must approve the request for it to be implemented.</span></span> <span data-ttu-id="7ff6a-107">Un éditeur peut exporter un objet de stratégie de groupe vers un fichier afin qu’il puisse être copié vers un domaine d’une autre forêt et importer un objet de stratégie de groupe copié à partir d’un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="7ff6a-107">An Editor can export a GPO to a file so that it can be copied to a domain in another forest, and import a GPO that was copied from another domain.</span></span>

<span data-ttu-id="7ff6a-108">**Important**  Assurez-vous que vous vous connectez à l’archive centrale pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7ff6a-108">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="7ff6a-109">Pour plus d’informations, voir [configurer une connexion de serveur AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7ff6a-109">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="7ff6a-110">Création ou contrôle d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7ff6a-110">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

-   [<span data-ttu-id="7ff6a-111">Modification d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7ff6a-111">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   [<span data-ttu-id="7ff6a-112">Utilisation d'un environnement de test</span><span class="sxs-lookup"><span data-stu-id="7ff6a-112">Using a Test Environment</span></span>](using-a-test-environment.md)

-   [<span data-ttu-id="7ff6a-113">Demander le déploiement d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7ff6a-113">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="7ff6a-114">Création d'un modèle et définition d'un modèle par défaut</span><span class="sxs-lookup"><span data-stu-id="7ff6a-114">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="7ff6a-115">Suppression ou restauration d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7ff6a-115">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

<span data-ttu-id="7ff6a-116">**Remarques**  Dans la mesure où le rôle d’éditeur inclut les autorisations pour le rôle de réviseur, un éditeur peut également consulter les paramètres et comparer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7ff6a-116">**Note** Because the Editor role includes the permissions for the Reviewer role, an Editor can also review settings and compare GPOs.</span></span> <span data-ttu-id="7ff6a-117">Pour plus d’informations, voir [exécution de tâches de réviseur](performing-reviewer-tasks-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff6a-117">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="7ff6a-118">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="7ff6a-118">Additional considerations</span></span>

<span data-ttu-id="7ff6a-119">Par défaut, les autorisations suivantes sont fournies pour le rôle d’éditeur:</span><span class="sxs-lookup"><span data-stu-id="7ff6a-119">By default, the following permissions are provided for the Editor role:</span></span>

-   <span data-ttu-id="7ff6a-120">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="7ff6a-120">List Contents</span></span>

-   <span data-ttu-id="7ff6a-121">Lire les paramètres</span><span class="sxs-lookup"><span data-stu-id="7ff6a-121">Read Settings</span></span>

-   <span data-ttu-id="7ff6a-122">Modifier les paramètres</span><span class="sxs-lookup"><span data-stu-id="7ff6a-122">Edit Settings</span></span>

-   <span data-ttu-id="7ff6a-123">Exporter un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7ff6a-123">Export GPO</span></span>

-   <span data-ttu-id="7ff6a-124">Importer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7ff6a-124">Import GPO</span></span>

-   <span data-ttu-id="7ff6a-125">Créer un modèle</span><span class="sxs-lookup"><span data-stu-id="7ff6a-125">Create Template</span></span>

 

 






---
title: Exécution de tâches d'approbateur
description: Exécution de tâches d'approbateur
author: dansimp
ms.assetid: 6f6310b3-19c1-47c9-8615-964ddd10ce14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fc77a1dd9a3d54e637ae4baeb452d327672ed250
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808302"
---
# <span data-ttu-id="c35f9-103">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="c35f9-103">Performing Approver Tasks</span></span>


<span data-ttu-id="c35f9-104">Un approbateur est une personne autorisée par un administrateur d’AGPM (contrôle total) pour créer, déployer et supprimer des objets de stratégie de groupe (GPO) et approuver ou refuser des demandes (en général des éditeurs) pour créer, déployer ou supprimer des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c35f9-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="c35f9-105">**Important**  Assurez-vous que vous vous connectez à l’archive centrale pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c35f9-105">**Important** Ensure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="c35f9-106">Pour plus d’informations, voir [configurer la connexion au serveur AGPM](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="c35f9-106">For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

 

-   [<span data-ttu-id="c35f9-107">Approuver ou rejeter une action en attente</span><span class="sxs-lookup"><span data-stu-id="c35f9-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action.md)

-   [<span data-ttu-id="c35f9-108">Création, contrôle ou importation d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c35f9-108">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

-   [<span data-ttu-id="c35f9-109">Enregistrer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c35f9-109">Check In a GPO</span></span>](check-in-a-gpo-approver.md)

-   [<span data-ttu-id="c35f9-110">Déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c35f9-110">Deploy a GPO</span></span>](deploy-a-gpo.md)

-   [<span data-ttu-id="c35f9-111">Revenir à une version précédente d'objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c35f9-111">Roll Back to a Previous Version of a GPO</span></span>](roll-back-to-a-previous-version-of-a-gpo.md)

-   [<span data-ttu-id="c35f9-112">Suppression, restauration ou destruction d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c35f9-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

<span data-ttu-id="c35f9-113">**Remarques**  Dans la mesure où le rôle Approbateur inclut les autorisations pour le rôle de réviseur, un approbateur peut également consulter les paramètres et comparer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c35f9-113">**Note** Because the Approver role includes the permissions for the Reviewer role, an Approver can also review settings and compare GPOs.</span></span> <span data-ttu-id="c35f9-114">Pour plus d’informations, voir [exécution de tâches de réviseur](performing-reviewer-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="c35f9-114">See [Performing Reviewer Tasks](performing-reviewer-tasks.md) for more information.</span></span>

 

### <span data-ttu-id="c35f9-115">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="c35f9-115">Additional considerations</span></span>

<span data-ttu-id="c35f9-116">Par défaut, les autorisations suivantes sont fournies pour le rôle Approbateur:</span><span class="sxs-lookup"><span data-stu-id="c35f9-116">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="c35f9-117">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="c35f9-117">List Contents</span></span>

-   <span data-ttu-id="c35f9-118">Lire les paramètres</span><span class="sxs-lookup"><span data-stu-id="c35f9-118">Read Settings</span></span>

-   <span data-ttu-id="c35f9-119">Créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c35f9-119">Create GPO</span></span>

-   <span data-ttu-id="c35f9-120">Déploiement d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c35f9-120">Deploy GPO</span></span>

-   <span data-ttu-id="c35f9-121">Supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c35f9-121">Delete GPO</span></span>

<span data-ttu-id="c35f9-122">Par ailleurs, un approbateur contrôle entièrement les objets de stratégie de groupe qu’il a créés ou contrôlés.</span><span class="sxs-lookup"><span data-stu-id="c35f9-122">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 






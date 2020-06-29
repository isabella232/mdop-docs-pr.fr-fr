---
title: Exécution de tâches d'approbateur
description: Exécution de tâches d'approbateur
author: dansimp
ms.assetid: e0a4b7fe-ce69-4755-9104-c7f523ea6b62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a0815bdd6c34a7a23b27075b3b5367757c1f84e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808318"
---
# <span data-ttu-id="e41ca-103">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="e41ca-103">Performing Approver Tasks</span></span>


<span data-ttu-id="e41ca-104">Un approbateur est une personne autorisée par un administrateur d’AGPM (contrôle total) pour créer, déployer et supprimer des objets de stratégie de groupe (GPO) et approuver ou refuser des demandes (en général des éditeurs) pour créer, déployer ou supprimer des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e41ca-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="e41ca-105">**Important**  Assurez-vous que vous vous connectez à l’archive centrale pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e41ca-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="e41ca-106">Pour plus d’informations, voir [configurer une connexion de serveur AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e41ca-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="e41ca-107">Approuver ou rejeter une action en attente</span><span class="sxs-lookup"><span data-stu-id="e41ca-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm40.md)

-   [<span data-ttu-id="e41ca-108">Création ou contrôle d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e41ca-108">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

-   [<span data-ttu-id="e41ca-109">Enregistrer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e41ca-109">Check In a GPO</span></span>](check-in-a-gpo-agpm40.md)

-   [<span data-ttu-id="e41ca-110">Déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e41ca-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="e41ca-111">Revenir à une version antérieure d'objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e41ca-111">Roll Back to an Earlier Version of a GPO</span></span>](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="e41ca-112">Suppression, restauration ou destruction d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e41ca-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

<span data-ttu-id="e41ca-113">**Remarques**  Avant l’approbation d’un objet de stratégie de groupe, un approbateur doit consulter les paramètres de stratégie qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="e41ca-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="e41ca-114">Le rôle Approbateur inclut les autorisations du rôle de relecteur, de sorte qu’un approbateur puisse consulter les paramètres de stratégie et comparer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e41ca-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="e41ca-115">Pour plus d’informations, voir [exécution de tâches de réviseur](performing-reviewer-tasks-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="e41ca-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="e41ca-116">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="e41ca-116">Additional considerations</span></span>

<span data-ttu-id="e41ca-117">Par défaut, les autorisations suivantes sont fournies pour le rôle Approbateur:</span><span class="sxs-lookup"><span data-stu-id="e41ca-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="e41ca-118">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="e41ca-118">List Contents</span></span>

-   <span data-ttu-id="e41ca-119">Lire les paramètres</span><span class="sxs-lookup"><span data-stu-id="e41ca-119">Read Settings</span></span>

-   <span data-ttu-id="e41ca-120">Créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e41ca-120">Create GPO</span></span>

-   <span data-ttu-id="e41ca-121">Déploiement d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e41ca-121">Deploy GPO</span></span>

-   <span data-ttu-id="e41ca-122">Supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e41ca-122">Delete GPO</span></span>

<span data-ttu-id="e41ca-123">Par ailleurs, un approbateur contrôle entièrement les objets de stratégie de groupe qu’il a créés ou contrôlés.</span><span class="sxs-lookup"><span data-stu-id="e41ca-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 






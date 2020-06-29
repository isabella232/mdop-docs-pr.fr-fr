---
title: Exécution de tâches d'administrateur AGPM
description: Exécution de tâches d'administrateur AGPM
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808322"
---
# <span data-ttu-id="e1e8a-103">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="e1e8a-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="e1e8a-104">Un administrateur AGPM (contrôle total) configure les autorisations à l’échelle du domaine et délègue les autorisations aux approbateurs, éditeurs, réviseurs et autres administrateurs d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="e1e8a-104">An AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="e1e8a-105">Par défaut, un administrateur AGPM est une personne disposant du contrôle total (toutes les autorisations de gestion de la stratégie de groupe avancées \ [AGPM \]) et peut également effectuer des tâches associées à n’importe quel rôle.</span><span class="sxs-lookup"><span data-stu-id="e1e8a-105">By default, an AGPM Administrator is an individual with Full Control (all Advanced Group Policy Management \[AGPM\] permissions) and therefore can also perform tasks associated with any role.</span></span>

<span data-ttu-id="e1e8a-106">Dans un environnement dans lequel plusieurs personnes développent des objets de stratégie de groupe, vous pouvez choisir si tous les utilisateurs de gestion de la stratégie de groupe avancés (AGPM) effectuent les mêmes tâches et disposent du même niveau d’accès, ou si les administrateurs d’AGPM délèguent des autorisations aux éditeurs qui apportent des modifications à des objets de stratégie de groupe et à l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="e1e8a-106">In an environment in which multiple people develop Group Policy objects (GPOs), you can choose whether all Advanced Group Policy Management (AGPM) users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="e1e8a-107">Les administrateurs d’AGPM peuvent configurer les autorisations pour répondre aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e1e8a-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   [<span data-ttu-id="e1e8a-108">Configurer la connexion au serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="e1e8a-108">Configure the AGPM Server Connection</span></span>](configure-the-agpm-server-connection.md)

-   [<span data-ttu-id="e1e8a-109">Configurer la notification par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="e1e8a-109">Configure E-Mail Notification</span></span>](configure-e-mail-notification.md)

-   [<span data-ttu-id="e1e8a-110">Accès au niveau du domaine de délégué</span><span class="sxs-lookup"><span data-stu-id="e1e8a-110">Delegate Domain-Level Access</span></span>](delegate-domain-level-access.md)

-   [<span data-ttu-id="e1e8a-111">Déléguer l'accès à un objet de stratégie de groupe individuel</span><span class="sxs-lookup"><span data-stu-id="e1e8a-111">Delegate Access to an Individual GPO</span></span>](delegate-access-to-an-individual-gpo.md)

-   [<span data-ttu-id="e1e8a-112">Configurer la journalisation et suivi</span><span class="sxs-lookup"><span data-stu-id="e1e8a-112">Configure Logging and Tracing</span></span>](configure-logging-and-tracing.md)

-   [<span data-ttu-id="e1e8a-113">Gestion du service AGPM</span><span class="sxs-lookup"><span data-stu-id="e1e8a-113">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

    -   [<span data-ttu-id="e1e8a-114">Démarrer et arrêter le service AGPM</span><span class="sxs-lookup"><span data-stu-id="e1e8a-114">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service.md)

    -   [<span data-ttu-id="e1e8a-115">Modifier le chemin d'accès de l'archive</span><span class="sxs-lookup"><span data-stu-id="e1e8a-115">Modify the Archive Path</span></span>](modify-the-archive-path.md)

    -   [<span data-ttu-id="e1e8a-116">Modifier le compte du service AGPM</span><span class="sxs-lookup"><span data-stu-id="e1e8a-116">Modify the AGPM Service Account</span></span>](modify-the-agpm-service-account.md)

    -   [<span data-ttu-id="e1e8a-117">Modifier le port sur lequel le service AGPM écoute</span><span class="sxs-lookup"><span data-stu-id="e1e8a-117">Modify the Port on Which the AGPM Service Listens</span></span>](modify-the-port-on-which-the-agpm-service-listens.md)

<span data-ttu-id="e1e8a-118">Par ailleurs, dans la mesure où le rôle d’administrateur AGPM inclut les autorisations de tous les autres rôles, un administrateur AGPM peut effectuer les tâches normalement associées à un autre rôle.</span><span class="sxs-lookup"><span data-stu-id="e1e8a-118">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="e1e8a-119">[Exécution des tâches approbateurs](performing-approver-tasks.md), telles que la création, le déploiement et la suppression d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e1e8a-119">[Performing Approver Tasks](performing-approver-tasks.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="e1e8a-120">[Exécution de tâches d’éditeur](performing-editor-tasks.md), telles que la modification, le changement de nom, l’étiquetage ou l’importation d’objets de stratégie de groupe, la création de modèles ou la définition d’un modèle par défaut</span><span class="sxs-lookup"><span data-stu-id="e1e8a-120">[Performing Editor Tasks](performing-editor-tasks.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="e1e8a-121">[Exécution des tâches de relecteur](performing-reviewer-tasks.md), telles que la révision des paramètres et la comparaison d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e1e8a-121">[Performing Reviewer Tasks](performing-reviewer-tasks.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="e1e8a-122">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="e1e8a-122">Additional considerations</span></span>

<span data-ttu-id="e1e8a-123">Par défaut, le rôle d’administrateur AGPM possède le contrôle total, c’est-à-dire les autorisations AGPM suivantes:</span><span class="sxs-lookup"><span data-stu-id="e1e8a-123">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="e1e8a-124">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="e1e8a-124">List Contents</span></span>

-   <span data-ttu-id="e1e8a-125">Lire les paramètres</span><span class="sxs-lookup"><span data-stu-id="e1e8a-125">Read Settings</span></span>

-   <span data-ttu-id="e1e8a-126">Modifier les paramètres</span><span class="sxs-lookup"><span data-stu-id="e1e8a-126">Edit Settings</span></span>

-   <span data-ttu-id="e1e8a-127">Créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e1e8a-127">Create GPO</span></span>

-   <span data-ttu-id="e1e8a-128">Déploiement d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e1e8a-128">Deploy GPO</span></span>

-   <span data-ttu-id="e1e8a-129">Supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e1e8a-129">Delete GPO</span></span>

-   <span data-ttu-id="e1e8a-130">Modification des options</span><span class="sxs-lookup"><span data-stu-id="e1e8a-130">Modify Options</span></span>

-   <span data-ttu-id="e1e8a-131">Modifier la sécurité</span><span class="sxs-lookup"><span data-stu-id="e1e8a-131">Modify Security</span></span>

-   <span data-ttu-id="e1e8a-132">Créer un modèle</span><span class="sxs-lookup"><span data-stu-id="e1e8a-132">Create Template</span></span>

<span data-ttu-id="e1e8a-133">Les **options de modification** et de modification des autorisations de **sécurité** sont propres au rôle d’administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="e1e8a-133">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 






---
title: Exécution de tâches d'administrateur AGPM
description: Exécution de tâches d'administrateur AGPM
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809347"
---
# <span data-ttu-id="2a42f-103">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="2a42f-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="2a42f-104">Dans Advanced Group Policy Management (AGPM), un administrateur AGPM (contrôle total) configure les autorisations à l’échelle du domaine et délègue les autorisations aux approbateurs, aux éditeurs, aux réviseurs et aux autres administrateurs d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="2a42f-104">In Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="2a42f-105">Par défaut, un administrateur AGPM est une personne disposant du contrôle total, toutes les autorisations d’AGPM, qui peuvent donc effectuer des tâches associées à n’importe quel rôle.</span><span class="sxs-lookup"><span data-stu-id="2a42f-105">By default, an AGPM Administrator is an individual with Full Control—all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="2a42f-106">Dans un environnement dans lequel plusieurs personnes développent des objets de stratégie de groupe, vous pouvez choisir si tous les utilisateurs d’AGPM effectuent les mêmes tâches et disposent du même niveau d’accès, ou si les administrateurs AGPM délèguent des autorisations aux éditeurs qui apportent des modifications à des objets de stratégie de groupe et à des approbateurs qui déploient des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2a42f-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose whether all AGPM users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="2a42f-107">Les administrateurs d’AGPM peuvent configurer les autorisations pour répondre aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2a42f-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="2a42f-108">[Configuration de la gestion avancée](configuring-advanced-group-policy-management.md)de la stratégie de groupe: configurez la connexion à un serveur AGPM et la notification par courrier électronique, déléguez l’accès aux objets de stratégie de groupe dans l’environnement de production et configurez la journalisation et le suivi</span><span class="sxs-lookup"><span data-stu-id="2a42f-108">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="2a42f-109">[Gestion de l’archive](managing-the-archive.md): déléguez l’accès aux objets de stratégie de groupe dans l’archive et limitez le nombre de versions de chaque GPO stockées.</span><span class="sxs-lookup"><span data-stu-id="2a42f-109">[Managing the Archive](managing-the-archive.md): Delegate access to GPOs in the archive and limit the number of versions of each GPO stored.</span></span>

-   <span data-ttu-id="2a42f-110">[Gestion du service AGPM](managing-the-agpm-service-agpm30ops.md): Arrêtez et démarrez le service AGPM ou modifiez le chemin d’archive, le compte de service AGPM ou le port sur lequel le service AGPM écoute.</span><span class="sxs-lookup"><span data-stu-id="2a42f-110">[Managing the AGPM Service](managing-the-agpm-service-agpm30ops.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="2a42f-111">[Déplacement du serveur et de l’archive AGPM](move-the-agpm-server-and-the-archive.md): déplacez le service AGPM, l’archive ou les deux vers un autre serveur.</span><span class="sxs-lookup"><span data-stu-id="2a42f-111">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="2a42f-112">Par ailleurs, dans la mesure où le rôle d’administrateur AGPM inclut les autorisations de tous les autres rôles, un administrateur AGPM peut effectuer les tâches normalement associées à un autre rôle.</span><span class="sxs-lookup"><span data-stu-id="2a42f-112">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="2a42f-113">[Exécution des tâches approbateurs](performing-approver-tasks-agpm30ops.md), telles que la création, le déploiement et la suppression d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2a42f-113">[Performing Approver Tasks](performing-approver-tasks-agpm30ops.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="2a42f-114">[Exécution de tâches d’éditeur](performing-editor-tasks-agpm30ops.md), telles que la modification, le changement de nom, l’étiquetage ou l’importation d’objets de stratégie de groupe, la création de modèles ou la définition d’un modèle par défaut</span><span class="sxs-lookup"><span data-stu-id="2a42f-114">[Performing Editor Tasks](performing-editor-tasks-agpm30ops.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="2a42f-115">[Exécution des tâches de relecteur](performing-reviewer-tasks-agpm30ops.md), telles que la révision des paramètres et la comparaison d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2a42f-115">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="2a42f-116">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="2a42f-116">Additional considerations</span></span>

<span data-ttu-id="2a42f-117">Par défaut, le rôle d’administrateur AGPM possède le contrôle total, c’est-à-dire les autorisations AGPM suivantes:</span><span class="sxs-lookup"><span data-stu-id="2a42f-117">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="2a42f-118">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="2a42f-118">List Contents</span></span>

-   <span data-ttu-id="2a42f-119">Lire les paramètres</span><span class="sxs-lookup"><span data-stu-id="2a42f-119">Read Settings</span></span>

-   <span data-ttu-id="2a42f-120">Modifier les paramètres</span><span class="sxs-lookup"><span data-stu-id="2a42f-120">Edit Settings</span></span>

-   <span data-ttu-id="2a42f-121">Créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2a42f-121">Create GPO</span></span>

-   <span data-ttu-id="2a42f-122">Déploiement d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2a42f-122">Deploy GPO</span></span>

-   <span data-ttu-id="2a42f-123">Supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2a42f-123">Delete GPO</span></span>

-   <span data-ttu-id="2a42f-124">Modification des options</span><span class="sxs-lookup"><span data-stu-id="2a42f-124">Modify Options</span></span>

-   <span data-ttu-id="2a42f-125">Modifier la sécurité</span><span class="sxs-lookup"><span data-stu-id="2a42f-125">Modify Security</span></span>

-   <span data-ttu-id="2a42f-126">Créer un modèle</span><span class="sxs-lookup"><span data-stu-id="2a42f-126">Create Template</span></span>

<span data-ttu-id="2a42f-127">Les **options de modification** et de modification des autorisations de **sécurité** sont propres au rôle d’administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="2a42f-127">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 






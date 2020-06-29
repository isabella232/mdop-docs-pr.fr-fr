---
title: Exécution de tâches d'administrateur AGPM
description: Exécution de tâches d'administrateur AGPM
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809342"
---
# <span data-ttu-id="5ba8d-103">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="5ba8d-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="5ba8d-104">Gestion de la stratégie de groupe avancée (AGPM) permet à un administrateur AGPM (contrôle total) de configurer les options à l’échelle du domaine et de déléguer les autorisations aux approbateurs, aux éditeurs, aux réviseurs et aux administrateurs d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-104">Advanced Group Policy Management (AGPM) lets an AGPM Administrator (Full Control) configure domain-wide options and delegate permissions to Approvers, Editors, Reviewers, and AGPM Administrators.</span></span> <span data-ttu-id="5ba8d-105">Par défaut, un administrateur d’AGPM est une personne disposant du contrôle total (toutes les autorisations d’AGPM) et qui peut donc effectuer des tâches associées à n’importe quel rôle.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-105">By default, an AGPM Administrator is someone who has Full Control— all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="5ba8d-106">Dans un environnement dans lequel plusieurs personnes développent des objets de stratégie de groupe, vous pouvez choisir de laisser tous les administrateurs de stratégie de groupe effectuer les mêmes tâches et disposer du même niveau d’accès.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose to let all Group Policy administrators perform the same tasks and have the same level of access.</span></span> <span data-ttu-id="5ba8d-107">Ou bien, vous pouvez choisir de permettre aux administrateurs d’AGPM de déléguer des autorisations aux éditeurs qui peuvent modifier des objets de stratégie de groupe et aux approbateurs qui déploient les objets GPO dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-107">Or, you can choose to let AGPM Administrators delegate permissions to Editors who can change GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="5ba8d-108">Les administrateurs d’AGPM peuvent configurer les autorisations pour répondre aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-108">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="5ba8d-109">[Configuration de la gestion avancée](configuring-advanced-group-policy-management-agpm40.md)de la stratégie de groupe: configurez la connexion à un serveur AGPM et la notification par courrier électronique, déléguez l’accès aux objets de stratégie de groupe dans l’environnement de production et configurez la journalisation et le suivi</span><span class="sxs-lookup"><span data-stu-id="5ba8d-109">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management-agpm40.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="5ba8d-110">[Gestion de l’archive](managing-the-archive-agpm40.md): accès délégué aux objets de stratégie de groupe dans l’archive, limitez le nombre de versions de chaque GPO stockées, importez un objet GPO d’un autre domaine, puis sauvegardez et restaurez l’archive.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-110">[Managing the Archive](managing-the-archive-agpm40.md): Delegate access to GPOs in the archive, limit the number of versions of each GPO stored, import a GPO from another domain, and back up and restore the archive.</span></span>

-   <span data-ttu-id="5ba8d-111">[Gestion du service AGPM](managing-the-agpm-service-agpm40.md): Arrêtez et démarrez le service AGPM ou modifiez le chemin d’archive, le compte de service AGPM ou le port sur lequel le service AGPM écoute.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-111">[Managing the AGPM Service](managing-the-agpm-service-agpm40.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="5ba8d-112">[Déplacement du serveur et de l’archive AGPM](move-the-agpm-server-and-the-archive-agpm40.md): déplacez le service AGPM, l’archive ou les deux vers un autre serveur.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-112">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="5ba8d-113">**Remarques**  Dans la mesure où le rôle d’administrateur AGPM inclut les autorisations de tous les autres rôles, un administrateur AGPM peut effectuer les tâches généralement associées à un autre rôle.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-113">**Note** Because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks usually associated with any other role.</span></span>

<span data-ttu-id="5ba8d-114">[Exécution des tâches approbateurs](performing-approver-tasks-agpm40.md), telles que la création, le déploiement et la suppression d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5ba8d-114">[Performing Approver Tasks](performing-approver-tasks-agpm40.md), such as creating, deploying, or deleting GPOs</span></span>

<span data-ttu-id="5ba8d-115">[Exécution de tâches d’éditeur](performing-editor-tasks-agpm40.md), telles que la modification, le changement de nom, l’étiquetage ou l’importation d’objets de stratégie de groupe, la création de modèles ou la définition d’un modèle par défaut</span><span class="sxs-lookup"><span data-stu-id="5ba8d-115">[Performing Editor Tasks](performing-editor-tasks-agpm40.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

<span data-ttu-id="5ba8d-116">[Exécution des tâches de relecteur](performing-reviewer-tasks-agpm40.md), telles que la révision des paramètres et la comparaison d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5ba8d-116">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md), such as reviewing settings and comparing GPOs</span></span>

 

### <span data-ttu-id="5ba8d-117">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="5ba8d-117">Additional considerations</span></span>

<span data-ttu-id="5ba8d-118">Par défaut, le rôle d’administrateur AGPM possède le contrôle total, c’est-à-dire les autorisations AGPM suivantes:</span><span class="sxs-lookup"><span data-stu-id="5ba8d-118">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="5ba8d-119">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="5ba8d-119">List Contents</span></span>

-   <span data-ttu-id="5ba8d-120">Lire les paramètres</span><span class="sxs-lookup"><span data-stu-id="5ba8d-120">Read Settings</span></span>

-   <span data-ttu-id="5ba8d-121">Modifier les paramètres</span><span class="sxs-lookup"><span data-stu-id="5ba8d-121">Edit Settings</span></span>

-   <span data-ttu-id="5ba8d-122">Créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5ba8d-122">Create GPO</span></span>

-   <span data-ttu-id="5ba8d-123">Déploiement d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5ba8d-123">Deploy GPO</span></span>

-   <span data-ttu-id="5ba8d-124">Supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5ba8d-124">Delete GPO</span></span>

-   <span data-ttu-id="5ba8d-125">Exporter un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5ba8d-125">Export GPO</span></span>

-   <span data-ttu-id="5ba8d-126">Importer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="5ba8d-126">Import GPO</span></span>

-   <span data-ttu-id="5ba8d-127">Créer un modèle</span><span class="sxs-lookup"><span data-stu-id="5ba8d-127">Create Template</span></span>

-   <span data-ttu-id="5ba8d-128">Modification des options</span><span class="sxs-lookup"><span data-stu-id="5ba8d-128">Modify Options</span></span>

-   <span data-ttu-id="5ba8d-129">Modifier la sécurité</span><span class="sxs-lookup"><span data-stu-id="5ba8d-129">Modify Security</span></span>

<span data-ttu-id="5ba8d-130">Les **options de modification** et de modification des autorisations de **sécurité** sont propres au rôle d’administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="5ba8d-130">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 






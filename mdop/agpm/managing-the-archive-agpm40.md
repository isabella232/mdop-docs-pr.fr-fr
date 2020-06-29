---
title: Gestion de l'archivage
description: Gestion de l'archivage
author: dansimp
ms.assetid: b11a3d71-74ea-4dd7-b243-6f2880b7af2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 682d720b4095dbfa6a7cc4d868109f57c4f54641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808354"
---
# <span data-ttu-id="c6225-103">Gestion de l'archivage</span><span class="sxs-lookup"><span data-stu-id="c6225-103">Managing the Archive</span></span>


<span data-ttu-id="c6225-104">Dans Advanced Group Policy Management (AGPM), en tant qu’administrateur AGPM (contrôle total), vous gérez l’accès à l’archive et avez la possibilité de limiter le nombre de versions de chaque objet de stratégie de groupe stockées dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="c6225-104">In Advanced Group Policy Management (AGPM), as an AGPM Administrator (Full Control), you manage access to the archive and have the option to limit the number of versions of each Group Policy Object (GPO) stored in the archive.</span></span> <span data-ttu-id="c6225-105">Vous pouvez déléguer l’accès à des objets de stratégie de groupe au niveau du domaine ou de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c6225-105">You can delegate access to GPOs in the archive at the domain level or GPO level.</span></span> <span data-ttu-id="c6225-106">De plus, vous pouvez sauvegarder l’Archive pour pouvoir la récupérer en cas de sinistre.</span><span class="sxs-lookup"><span data-stu-id="c6225-106">Additionally, you can back up the archive so that you may be able to recover it if a disaster occurs.</span></span>

<span data-ttu-id="c6225-107">En tant qu’administrateur AGPM, vous pouvez exporter un objet GPO vers un fichier, copier le fichier dans une autre forêt, puis importer l’objet GPO dans un domaine de cette forêt.</span><span class="sxs-lookup"><span data-stu-id="c6225-107">As an AGPM Administrator, you can export a GPO to a file, copy the file to another forest, and then import the GPO into a domain in that forest.</span></span> <span data-ttu-id="c6225-108">Contrairement à un éditeur, vous pouvez importer les paramètres de stratégie d’une sauvegarde d’objet de stratégie de groupe directement dans un nouvel objet de stratégie de groupe contrôlé lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="c6225-108">Unlike an Editor, you can import policy settings from a GPO backup directly into a new controlled GPO when you create it.</span></span> <span data-ttu-id="c6225-109">Pour plus d’informations sur l’exportation d’un objet de stratégie de groupe, voir [exporter un objet GPO vers un fichier](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="c6225-109">For information about how to export a GPO, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

-   [<span data-ttu-id="c6225-110">Déléguer l'accès au niveau du domaine à l'archive</span><span class="sxs-lookup"><span data-stu-id="c6225-110">Delegate Domain-Level Access to the Archive</span></span>](delegate-domain-level-access-to-the-archive-agpm40.md)

-   [<span data-ttu-id="c6225-111">Déléguer l'accès à un objet de stratégie de groupe dans l'archive</span><span class="sxs-lookup"><span data-stu-id="c6225-111">Delegate Access to an Individual GPO in the Archive</span></span>](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)

-   [<span data-ttu-id="c6225-112">Limiter les versions d'objet de stratégie de groupe stockées</span><span class="sxs-lookup"><span data-stu-id="c6225-112">Limit the GPO Versions Stored</span></span>](limit-the-gpo-versions-stored-agpm40.md)

-   [<span data-ttu-id="c6225-113">Importer un objet de stratégie de groupe à partir d'un fichier</span><span class="sxs-lookup"><span data-stu-id="c6225-113">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-agpmadmin.md)

-   [<span data-ttu-id="c6225-114">Sauvegarder l'archive</span><span class="sxs-lookup"><span data-stu-id="c6225-114">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="c6225-115">Restaurer l'archive à partir d'une sauvegarde</span><span class="sxs-lookup"><span data-stu-id="c6225-115">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

### <span data-ttu-id="c6225-116">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c6225-116">Additional references</span></span>

-   <span data-ttu-id="c6225-117">Pour plus d’informations sur la façon de déléguer l’accès aux objets de stratégie de groupe dans l’environnement de production, voir [délégation de l’accès à l’environnement de production](delegate-access-to-the-production-environment-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="c6225-117">For information about how to delegate access to GPOs in the production environment, see [Delegate Access to the Production Environment](delegate-access-to-the-production-environment-agpm40.md).</span></span>

-   <span data-ttu-id="c6225-118">Pour plus d’informations sur le déplacement de l’archive, voir [déplacer le serveur AGPM et l’archive](move-the-agpm-server-and-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="c6225-118">For information about how to move the archive, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md).</span></span>

-   [<span data-ttu-id="c6225-119">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="c6225-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 






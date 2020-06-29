---
title: Restaurer l'archive à partir d'une sauvegarde
description: Restaurer l'archive à partir d'une sauvegarde
author: dansimp
ms.assetid: 49666337-d72c-4e44-99e4-9eb59b2355a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b00d2e5e612e2ac43f965e4adf6175e2fd159007
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807477"
---
# <span data-ttu-id="63949-103">Restaurer l'archive à partir d'une sauvegarde</span><span class="sxs-lookup"><span data-stu-id="63949-103">Restore the Archive from a Backup</span></span>


<span data-ttu-id="63949-104">En cas de sinistre et si l’archive de la gestion de la stratégie de groupe avancée (AGPM) est endommagée ou détruite, un administrateur AGPM (contrôle total) peut restaurer l’archive à partir d’une copie de sauvegarde préparée à l’avance, puis importer à partir de l’environnement de production les objets de stratégie de groupe qui ne figurent pas dans l’archive ou dont la version en production est plus</span><span class="sxs-lookup"><span data-stu-id="63949-104">If a disaster occurs and the archive for Advanced Group Policy Management (AGPM) is damaged or destroyed, an AGPM Administrator (Full Control) can restore the archive from a backup copy prepared in advance and then import from the production environment any Group Policy Objects (GPOs) that are not in the archive or for which the version in production is more current than that in the archive.</span></span> <span data-ttu-id="63949-105">Pour plus d’informations sur la restauration d’une sauvegarde d’archive sur un serveur différent, voir [déplacer le serveur AGPM et l’archive](move-the-agpm-server-and-the-archive.md).</span><span class="sxs-lookup"><span data-stu-id="63949-105">For information about how to restore an archive backup to a different server, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md).</span></span>

<span data-ttu-id="63949-106">Un compte d’utilisateur ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le service AGPM) et au dossier qui contient l’archive est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="63949-106">A user account that has access to the AGPM Server (the computer on which the AGPM Service is installed) and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="63949-107">Pour restaurer l’archive à partir d’une sauvegarde</span><span class="sxs-lookup"><span data-stu-id="63949-107">To restore the archive from a backup</span></span>**

1.  <span data-ttu-id="63949-108">Arrêtez le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="63949-108">Stop the AGPM Service.</span></span> <span data-ttu-id="63949-109">Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="63949-109">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

2.  <span data-ttu-id="63949-110">Supprimez l’archive existante.</span><span class="sxs-lookup"><span data-stu-id="63949-110">Remove the existing archive.</span></span> <span data-ttu-id="63949-111">Par défaut, le dossier d’archivage est%ProgramData%\\Microsoft\\AGPM, mais l’Administrateur AGPM qui a installé Microsoft Advanced Group Policy Management-Server a peut-être entré un autre emplacement lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="63949-111">By default, the archive folder is %ProgramData%\\Microsoft\\AGPM, however the AGPM Administrator who installed Microsoft Advanced Group Policy Management - Server may have entered a different location during setup.</span></span>

3.  <span data-ttu-id="63949-112">Recréez le dossier archive en configurant le chemin d’archive, le compte de service AGPM, le propriétaire de l’archivage et le port d’écoute.</span><span class="sxs-lookup"><span data-stu-id="63949-112">Re-create the archive folder by configuring the archive path, AGPM Service Account, Archive Owner, and listening port.</span></span> <span data-ttu-id="63949-113">Il n’est pas nécessaire d’utiliser les mêmes valeurs que celles utilisées lors de l’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="63949-113">Using the same values as used during the original installation is not necessary.</span></span> <span data-ttu-id="63949-114">Pour plus d’informations, voir [modifier le service AGPM](modify-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="63949-114">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

4.  <span data-ttu-id="63949-115">Copiez le contenu de la sauvegarde d’archive dans le dossier d’archivage, en copiant les sous-dossiers et les fichiers pour vous assurer que chaque sous-dossier et fichier héritent des autorisations du dossier d’archivage.</span><span class="sxs-lookup"><span data-stu-id="63949-115">Copy the contents of the archive backup to the archive folder, copying the subfolders and files to make sure that each subfolder and file inherits the permissions of the archive folder.</span></span> <span data-ttu-id="63949-116">Veillez à ne pas écraser le dossier d’archivage.</span><span class="sxs-lookup"><span data-stu-id="63949-116">Be careful not to overwrite the archive folder.</span></span>

5.  <span data-ttu-id="63949-117">Si vous ne savez pas si un objet GPO dans la sauvegarde d’archive est plus à jour que la copie de cet objet GPO en production, générez un rapport de différences et comparez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="63949-117">If you not sure about whether a GPO in the archive backup is more current than the copy of that GPO in production, generate a difference report and compare their settings.</span></span> <span data-ttu-id="63949-118">Pour plus d’informations, voir [identifier les différences entre les objets de stratégie de groupe, les versions](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md)d’objets de stratégie de groupe et les modèles.</span><span class="sxs-lookup"><span data-stu-id="63949-118">For more information, see [Identify Differences Between GPOs, GPO Versions, or Templates](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md).</span></span>

6.  <span data-ttu-id="63949-119">Redémarrez le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="63949-119">Restart the AGPM Service.</span></span> <span data-ttu-id="63949-120">Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="63949-120">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

### <span data-ttu-id="63949-121">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="63949-121">Additional references</span></span>

-   [<span data-ttu-id="63949-122">Sauvegarder l'archive</span><span class="sxs-lookup"><span data-stu-id="63949-122">Back Up the Archive</span></span>](back-up-the-archive.md)

-   [<span data-ttu-id="63949-123">Déplacer le serveur AGPM et l'archive</span><span class="sxs-lookup"><span data-stu-id="63949-123">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive.md)

-   [<span data-ttu-id="63949-124">Gestion de l'archivage</span><span class="sxs-lookup"><span data-stu-id="63949-124">Managing the Archive</span></span>](managing-the-archive.md)

 

 






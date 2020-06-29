---
title: Sauvegarder l'archive
description: Sauvegarder l'archive
author: dansimp
ms.assetid: 400176da-3518-4475-ad19-c96cda6ca7ba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a75099e7a6624850ee0511cf65feddf63909a0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807814"
---
# <span data-ttu-id="69543-103">Sauvegarder l'archive</span><span class="sxs-lookup"><span data-stu-id="69543-103">Back Up the Archive</span></span>


<span data-ttu-id="69543-104">Pour vous aider dans la restauration de l’Archive pour la gestion avancée des stratégies de groupe (AGPM) en cas de sinistre, un administrateur AGPM (contrôle total) doit sauvegarder fréquemment l’archive.</span><span class="sxs-lookup"><span data-stu-id="69543-104">To help in the recovery of the archive for Advanced Group Policy Management (AGPM) if there is a disaster, an AGPM Administrator (Full Control) should back up the archive frequently.</span></span> <span data-ttu-id="69543-105">Par défaut, l’archive est créée dans%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="69543-105">By default, the archive is created in %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="69543-106">Toutefois, vous pouvez spécifier un chemin d’accès différent lors de l’installation de Microsoft Advanced Group Policy-Server.</span><span class="sxs-lookup"><span data-stu-id="69543-106">However, you can specify a different path during the setup of Microsoft Advanced Group Policy Management - Server.</span></span>

<span data-ttu-id="69543-107">Un compte d’utilisateur ayant accès au serveur AGPM (ordinateur sur lequel est installé le service AGPM) et au dossier qui contient l’archive est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="69543-107">A user account that has access to both the AGPM Server—the computer on which the AGPM Service is installed—and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="69543-108">Pour sauvegarder l’archive</span><span class="sxs-lookup"><span data-stu-id="69543-108">To back up the archive</span></span>**

1.  <span data-ttu-id="69543-109">Arrêtez le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="69543-109">Stop the AGPM Service.</span></span> <span data-ttu-id="69543-110">Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="69543-110">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

2.  <span data-ttu-id="69543-111">Sauvegardez le dossier d’archivage à l’aide de l’Explorateur Windows, de xcopy, de Windows Server® de sauvegarde ou d’un autre outil de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="69543-111">Back up the archive folder by using Windows Explorer, Xcopy, Windows Server® Backup, or another backup tool.</span></span> <span data-ttu-id="69543-112">Assurez-vous de sauvegarder les fichiers masqués, systèmes et en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="69543-112">Make sure that you back up hidden, system, and read-only files.</span></span>

3.  <span data-ttu-id="69543-113">Stockez la sauvegarde d’archive en lieu sûr.</span><span class="sxs-lookup"><span data-stu-id="69543-113">Store the archive backup in a secure location.</span></span>

4.  <span data-ttu-id="69543-114">Redémarrez le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="69543-114">Restart the AGPM Service.</span></span> <span data-ttu-id="69543-115">Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="69543-115">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

<span data-ttu-id="69543-116">**Remarques**  Si un administrateur AGPM sauvegarde l’archive fréquemment, les objets de stratégie de groupe de la sauvegarde d’archivage ne seront pas actualisés.</span><span class="sxs-lookup"><span data-stu-id="69543-116">**Note** If an AGPM Administrator backs up the archive infrequently, the Group Policy Objects (GPOs) in the archive backup will not be current.</span></span> <span data-ttu-id="69543-117">Pour vous assurer que la sauvegarde d’archivage est à jour, sauvegardez l’archive dans le cadre de la stratégie de sauvegarde quotidienne de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="69543-117">To better ensure that the archive backup is current, back up the archive as part of your organization’s daily backup strategy.</span></span>

 

### <span data-ttu-id="69543-118">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="69543-118">Additional references</span></span>

-   [<span data-ttu-id="69543-119">Restaurer l'archive à partir d'une sauvegarde</span><span class="sxs-lookup"><span data-stu-id="69543-119">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup.md)

-   [<span data-ttu-id="69543-120">Déplacer le serveur AGPM et l'archive</span><span class="sxs-lookup"><span data-stu-id="69543-120">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive.md)

-   [<span data-ttu-id="69543-121">Gestion de l'archivage</span><span class="sxs-lookup"><span data-stu-id="69543-121">Managing the Archive</span></span>](managing-the-archive.md)

 

 






---
title: Liste de vérification administration du serveur et de l’archivage AGPM
description: Liste de vérification administration du serveur et de l’archivage AGPM
author: dansimp
ms.assetid: d9c60203-90c2-48a7-9318-197e0ec5038b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e464dafa68b9d93c5a1051c986a0efde4702c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807781"
---
# <span data-ttu-id="255e9-103">Liste de contrôle: administrer le serveur AGPM et l'archivage</span><span class="sxs-lookup"><span data-stu-id="255e9-103">Checklist: Administer the AGPM Server and Archive</span></span>


<span data-ttu-id="255e9-104">Dans Advanced Group Policy Management (AGPM), le service AGPM et l’archive sont gérés par les administrateurs d’AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="255e9-104">In Advanced Group Policy Management (AGPM), both the AGPM Service and the archive are managed by AGPM Administrators (Full Control).</span></span> <span data-ttu-id="255e9-105">Voici des tâches typiques pour un administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="255e9-105">The following are typical tasks for an AGPM Administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="255e9-106">Tâches fréquentes</span><span class="sxs-lookup"><span data-stu-id="255e9-106">Frequent Task</span></span></th>
<th align="left"><span data-ttu-id="255e9-107">Référence</span><span class="sxs-lookup"><span data-stu-id="255e9-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="255e9-108">Déléguez l’accès à des objets de stratégie de groupe dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="255e9-108">Delegate access to Group Policy Objects (GPOs) in the archive.</span></span></p></td>
<td align="left"><p><a href="delegate-domain-level-access-to-the-archive-agpm40.md" data-raw-source="[Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm40.md)"><span data-ttu-id="255e9-109">Déléguer l'accès au niveau du domaine à l'archive</span><span class="sxs-lookup"><span data-stu-id="255e9-109">Delegate Domain-Level Access to the Archive</span></span></a></p>
<p><a href="delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md" data-raw-source="[Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)"><span data-ttu-id="255e9-110">Déléguer l'accès à un objet de stratégie de groupe dans l'archive</span><span class="sxs-lookup"><span data-stu-id="255e9-110">Delegate Access to an Individual GPO in the Archive</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="255e9-111">Sauvegardez l’Archive pour activer la reprise après sinistre.</span><span class="sxs-lookup"><span data-stu-id="255e9-111">Back up the archive to enable disaster recovery.</span></span></p></td>
<td align="left"><p><a href="back-up-the-archive-agpm40.md" data-raw-source="[Back Up the Archive](back-up-the-archive-agpm40.md)"><span data-ttu-id="255e9-112">Sauvegarder l'archive</span><span class="sxs-lookup"><span data-stu-id="255e9-112">Back Up the Archive</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="255e9-113">Tâches rares</span><span class="sxs-lookup"><span data-stu-id="255e9-113">Infrequent Task</span></span></th>
<th align="left"><span data-ttu-id="255e9-114">Référence</span><span class="sxs-lookup"><span data-stu-id="255e9-114">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="255e9-115">Restaurez l’archive à partir d’une sauvegarde pour résoudre un problème.</span><span class="sxs-lookup"><span data-stu-id="255e9-115">Restore the archive from a backup to recover from a disaster.</span></span></p></td>
<td align="left"><p><a href="restore-the-archive-from-a-backup-agpm40.md" data-raw-source="[Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md)"><span data-ttu-id="255e9-116">Restaurer l'archive à partir d'une sauvegarde</span><span class="sxs-lookup"><span data-stu-id="255e9-116">Restore the Archive from a Backup</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="255e9-117">Déplacez le service AGPM, l’archive ou les deux sur un autre serveur.</span><span class="sxs-lookup"><span data-stu-id="255e9-117">Move the AGPM Service, the archive, or both to a different server.</span></span></p></td>
<td align="left"><p><a href="move-the-agpm-server-and-the-archive-agpm40.md" data-raw-source="[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md)"><span data-ttu-id="255e9-118">Déplacer le serveur AGPM et l'archive</span><span class="sxs-lookup"><span data-stu-id="255e9-118">Move the AGPM Server and the Archive</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="255e9-119">Modifiez le chemin d’archive, le compte de service AGPM ou le port sur lequel le service AGPM écoute.</span><span class="sxs-lookup"><span data-stu-id="255e9-119">Change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span></p></td>
<td align="left"><p><a href="modify-the-agpm-service-agpm40.md" data-raw-source="[Modify the AGPM Service](modify-the-agpm-service-agpm40.md)"><span data-ttu-id="255e9-120">Modifier le service AGPM</span><span class="sxs-lookup"><span data-stu-id="255e9-120">Modify the AGPM Service</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="255e9-121">Résoudre les problèmes courants liés au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="255e9-121">Troubleshoot common problems with the AGPM Server.</span></span></p></td>
<td align="left"><p><a href="troubleshooting-agpm-agpm40.md" data-raw-source="[Troubleshooting AGPM](troubleshooting-agpm-agpm40.md)"><span data-ttu-id="255e9-122">Résolution des problèmes d'AGPM</span><span class="sxs-lookup"><span data-stu-id="255e9-122">Troubleshooting AGPM</span></span></a></p>
<p><a href="configure-logging-and-tracing-agpm40.md" data-raw-source="[Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md)"><span data-ttu-id="255e9-123">Configurer la journalisation et suivi</span><span class="sxs-lookup"><span data-stu-id="255e9-123">Configure Logging and Tracing</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="255e9-124">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="255e9-124">Additional references</span></span>

-   [<span data-ttu-id="255e9-125">Gestion avancée des stratégies de groupe4.0</span><span class="sxs-lookup"><span data-stu-id="255e9-125">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 






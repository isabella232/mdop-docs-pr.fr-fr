---
title: Onglet Serveur AGPM
description: Onglet Serveur AGPM
author: dansimp
ms.assetid: a6689437-233e-4f33-a0d6-f7d432c96c00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7ffaa3f55d4ae1c2a59287d9dc302aec3dd00aed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807845"
---
# <span data-ttu-id="e1148-103">Onglet Serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="e1148-103">AGPM Server Tab</span></span>


<span data-ttu-id="e1148-104">L’onglet **serveur AGPM** du volet de **contrôle des modifications** vous permet de sélectionner un serveur AGPM en entrant un nom d’ordinateur et un port complets et de supprimer les versions antérieures d’objets de stratégie de groupe de l’Archive pour économiser de l’espace disque sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="e1148-104">The **AGPM Server** tab on the **Change Control** pane enables you to select an AGPM Server by entering a fully-qualified computer name and port, and to delete older versions of Group Policy Objects (GPOs) from the archive to conserve disk space on the AGPM Server.</span></span>

## <span data-ttu-id="e1148-105">Spécification du serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="e1148-105">Specifying the AGPM Server</span></span>


<span data-ttu-id="e1148-106">Le serveur AGPM sélectionné détermine le type d’archive qui s’affiche dans l’onglet **Sommaire** et à quel emplacement les paramètres de **délégation de domaine** sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="e1148-106">The AGPM Server selected determines which archive is displayed for you on the **Contents** tab and to which location the **Domain Delegation** settings are applied.</span></span> <span data-ttu-id="e1148-107">Le port par défaut pour la gestion de la stratégie de groupe avancée (AGPM) est le port 4600.</span><span class="sxs-lookup"><span data-stu-id="e1148-107">The default port for Advanced Group Policy Management (AGPM) is port 4600.</span></span>

<span data-ttu-id="e1148-108">Si la connexion au serveur AGPM est configurée de façon centralisée à l’aide des paramètres de modèle d’administration, les options de cet onglet pour configurer la connexion ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="e1148-108">If the AGPM Server connection is centrally configured using Administrative template settings, the options on this tab for configuring the connection are unavailable.</span></span> <span data-ttu-id="e1148-109">Pour plus d’informations, voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e1148-109">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

## <span data-ttu-id="e1148-110">Suppression des anciennes versions de l’objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e1148-110">Deleting old GPO versions</span></span>


<span data-ttu-id="e1148-111">Par défaut, toutes les versions de chaque GPO contrôlé sont conservées dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="e1148-111">By default, all versions of every controlled GPO are retained in the archive.</span></span> <span data-ttu-id="e1148-112">Toutefois, vous pouvez configurer le service AGPM pour limiter le nombre de versions conservées pour chaque objet de stratégie de groupe et supprimer automatiquement la version la plus ancienne lorsque cette limite est dépassée.</span><span class="sxs-lookup"><span data-stu-id="e1148-112">However, you can configure the AGPM Service to limit the number of versions retained for each GPO and automatically delete the oldest version when that limit is exceeded.</span></span> <span data-ttu-id="e1148-113">Uniquement les versions d’objets de stratégie de groupe affichées sous l’onglet **versions uniques** de la fenêtre **historique** vers la limite.</span><span class="sxs-lookup"><span data-stu-id="e1148-113">Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

<span data-ttu-id="e1148-114">**Remarques**  Le nombre maximal de versions uniques à stocker pour chaque objet de stratégie de groupe n’inclut pas la version actuelle, donc la saisie de 0 conserve uniquement la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="e1148-114">**Note** The maximum number of unique versions to store for each GPO does not include the current version, so entering 0 retains only the current version.</span></span> <span data-ttu-id="e1148-115">La limite ne doit pas être supérieure à 999 versions.</span><span class="sxs-lookup"><span data-stu-id="e1148-115">The limit must be no greater than 999 versions.</span></span>

<span data-ttu-id="e1148-116">Lors de la suppression d’une version d’un objet de stratégie de groupe, un enregistrement de cette version reste dans l’historique de l’objet de stratégie de groupe, mais la version de l’objet de stratégie de groupe est supprimée de l’archive.</span><span class="sxs-lookup"><span data-stu-id="e1148-116">When a GPO version is deleted, a record of that version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span> <span data-ttu-id="e1148-117">Vous pouvez empêcher la suppression d’une version d’un objet de stratégie de groupe en le sélectionnant dans l’historique en tant que non supprimable.</span><span class="sxs-lookup"><span data-stu-id="e1148-117">You can prevent a GPO version from being deleted by marking it in the history as not deletable.</span></span>

 

### <span data-ttu-id="e1148-118">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1148-118">Additional references</span></span>

-   [<span data-ttu-id="e1148-119">Interface utilisateur: gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="e1148-119">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="e1148-120">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="e1148-120">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="e1148-121">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="e1148-121">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 






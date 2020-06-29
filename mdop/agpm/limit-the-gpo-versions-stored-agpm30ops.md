---
title: Limiter les versions d'objet de stratégie de groupe stockées
description: Limiter les versions d'objet de stratégie de groupe stockées
author: dansimp
ms.assetid: da14edc5-0c36-4c54-b122-861c86b99eb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20a3ae60cc330c27cbd19e943ba7f071d4ec60b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808381"
---
# <span data-ttu-id="33c29-103">Limiter les versions d'objet de stratégie de groupe stockées</span><span class="sxs-lookup"><span data-stu-id="33c29-103">Limit the GPO Versions Stored</span></span>


<span data-ttu-id="33c29-104">Par défaut, toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO) sont conservées dans l’archive sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="33c29-104">By default, all versions of every controlled Group Policy Object (GPO) are retained in the archive on the AGPM Server.</span></span> <span data-ttu-id="33c29-105">Toutefois, vous pouvez limiter le nombre de versions conservées pour chaque objet de stratégie de groupe et supprimer les versions antérieures lorsque cette limite est dépassée.</span><span class="sxs-lookup"><span data-stu-id="33c29-105">However, you can limit the number of versions retained for each GPO and delete older versions when that limit is exceeded.</span></span> <span data-ttu-id="33c29-106">Lors de la suppression des versions d’objets de stratégie de groupe, un enregistrement de la version reste dans l’historique de l’objet de stratégie de groupe, mais la version de l’objet de stratégie de groupe est supprimée de l’archive.</span><span class="sxs-lookup"><span data-stu-id="33c29-106">When GPO versions are deleted, a record of the version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span>

<span data-ttu-id="33c29-107">Un compte d’utilisateur disposant du rôle Administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="33c29-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="33c29-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="33c29-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="33c29-109">Pour limiter le nombre de versions d’objets de stratégie de groupe stockées</span><span class="sxs-lookup"><span data-stu-id="33c29-109">To limit the number of GPO versions stored</span></span>**

1.  <span data-ttu-id="33c29-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="33c29-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="33c29-111">Dans le volet Détails, cliquez sur l’onglet **serveur AGPM** .</span><span class="sxs-lookup"><span data-stu-id="33c29-111">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="33c29-112">Activez les cases à cocher **Supprimer les anciennes versions de chaque GPO de la** case à cocher archiver, puis tapez le nombre maximal de versions d’objets de stratégie de groupe à stocker pour chaque objet de stratégie de groupe, sans inclure la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="33c29-112">Select the **Delete old versions of each GPO from the archive** check box, and type the maximum number of GPO versions to store for each GPO, not including the current version.</span></span> <span data-ttu-id="33c29-113">Pour conserver uniquement la version actuelle, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="33c29-113">To retain only the current version, enter 0.</span></span> <span data-ttu-id="33c29-114">La valeur maximale ne doit pas être supérieure à 999.</span><span class="sxs-lookup"><span data-stu-id="33c29-114">The maximum must be no greater than 999.</span></span>

    <span data-ttu-id="33c29-115">**Important**  Uniquement les versions d’objets de stratégie de groupe affichées sous l’onglet **versions uniques** de la fenêtre **historique** vers la limite.</span><span class="sxs-lookup"><span data-stu-id="33c29-115">**Important** Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

     

4.  <span data-ttu-id="33c29-116">Cliquez sur le bouton **appliquer** .</span><span class="sxs-lookup"><span data-stu-id="33c29-116">Click the **Apply** button.</span></span>

### <span data-ttu-id="33c29-117">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="33c29-117">Additional considerations</span></span>

-   <span data-ttu-id="33c29-118">Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="33c29-118">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="33c29-119">En particulier, vous devez disposer du **contenu de liste** et des autorisations de **modification des options** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="33c29-119">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="33c29-120">Vous pouvez empêcher la suppression d’une version de l’objet GPO en le marquant dans l’historique comme inéligible pour suppression.</span><span class="sxs-lookup"><span data-stu-id="33c29-120">You can prevent a GPO version from being deleted by marking it in the history as ineligible for deletion.</span></span> <span data-ttu-id="33c29-121">Pour cela, cliquez avec le bouton droit sur la version dans l’historique de l’objet de stratégie de groupe et cliquez sur **ne pas supprimer**.</span><span class="sxs-lookup"><span data-stu-id="33c29-121">To do so, right-click the version in the history of the GPO and click **Do Not Delete**.</span></span>

### <span data-ttu-id="33c29-122">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="33c29-122">Additional references</span></span>

-   [<span data-ttu-id="33c29-123">Gestion de l'archivage</span><span class="sxs-lookup"><span data-stu-id="33c29-123">Managing the Archive</span></span>](managing-the-archive.md)

 

 






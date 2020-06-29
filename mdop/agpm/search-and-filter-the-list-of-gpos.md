---
title: Rechercher et filtrer la liste des objets de stratégie de groupe (GPO)
description: Rechercher et filtrer la liste des objets de stratégie de groupe (GPO)
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808237"
---
# <span data-ttu-id="530e9-103">Rechercher et filtrer la liste des objets de stratégie de groupe (GPO)</span><span class="sxs-lookup"><span data-stu-id="530e9-103">Search and Filter the List of GPOs</span></span>


<span data-ttu-id="530e9-104">Dans Advanced Group Policy Management (AGPM), vous pouvez effectuer une recherche dans la liste des objets de stratégie de groupe et leurs attributs pour filtrer la liste des objets de stratégie de groupe affichés.</span><span class="sxs-lookup"><span data-stu-id="530e9-104">In Advanced Group Policy Management (AGPM), you can search the list of Group Policy Objects (GPOs) and their attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="530e9-105">Par exemple, vous pouvez rechercher des objets de stratégie de groupe avec un nom, un État ou un commentaire particulier.</span><span class="sxs-lookup"><span data-stu-id="530e9-105">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="530e9-106">Vous pouvez également rechercher les objets de stratégie de groupe qui ont été modifiés en dernier par un administrateur de stratégie de groupe particulier ou à une date particulière.</span><span class="sxs-lookup"><span data-stu-id="530e9-106">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

## <span data-ttu-id="530e9-107">Exécution d’une recherche complexe</span><span class="sxs-lookup"><span data-stu-id="530e9-107">Performing a complex search</span></span>


<span data-ttu-id="530e9-108">Vous pouvez effectuer une recherche complexe en utilisant l’attribut de l' *objet de stratégie de groupe format 1: chaîne de recherche 1, attribut 2: chaîne de recherche 2... chaînes de recherche dans toutes les colonnes*.</span><span class="sxs-lookup"><span data-stu-id="530e9-108">You can perform a complex search by using the format *GPO attribute 1: search string 1 GPO attribute 2: search string 2…all-column search strings*.</span></span> <span data-ttu-id="530e9-109">La recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="530e9-109">The search is not case-sensitive.</span></span>

-   <span data-ttu-id="530e9-110">**Attribut d’objet de stratégie de groupe:** Tout en-tête de colonne dans la liste d’objets de stratégie de groupe dans AGPM autre que la version de l' **ordinateur** ou la version de l' **utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="530e9-110">**GPO attribute:** Any column heading in the list of GPOs in AGPM other than **Computer Version** or **User Version**.</span></span> <span data-ttu-id="530e9-111">Les attributs de l’objet GPO incluent le nom de l’objet de stratégie de groupe, l’État, l’utilisateur qui a modifié le plus récemment l’objet de stratégie de groupe, la date et l’heure de la dernière modification de celui-ci, des commentaires et des filtres WMI appliqués à l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="530e9-111">GPO attributes include the GPO name, state, user who most recently changed the GPO, date and time when the GPO was most recently changed, comment, GPO status, and WMI filter applied to the GPO.</span></span>

-   <span data-ttu-id="530e9-112">**Chaîne de recherche:** Texte pour lequel rechercher dans la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="530e9-112">**Search string:** Text for which to search in the specified column.</span></span> <span data-ttu-id="530e9-113">Si une chaîne comporte des espaces, vous devez encadrer la chaîne de guillemets.</span><span class="sxs-lookup"><span data-stu-id="530e9-113">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

-   <span data-ttu-id="530e9-114">**Chaînes de recherche dans toutes les colonnes:** Texte pour lequel rechercher dans toutes les colonnes de la liste d’objets de stratégie de groupe dans AGPM, à l’exception de la version de l' **ordinateur** et de la **version utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="530e9-114">**All-column search strings:** Text for which to search in all columns in the list of GPOs in AGPM other than **Computer Version** and **User Version**.</span></span> <span data-ttu-id="530e9-115">Vous pouvez inclure plusieurs chaînes séparées par des espaces.</span><span class="sxs-lookup"><span data-stu-id="530e9-115">You can include multiple strings separated by spaces.</span></span> <span data-ttu-id="530e9-116">Si une chaîne comporte des espaces, vous devez encadrer la chaîne de guillemets.</span><span class="sxs-lookup"><span data-stu-id="530e9-116">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

<span data-ttu-id="530e9-117">Chaque attribut d’objet GPO et paire de chaînes de recherche et chaque chaîne de recherche en toutes les colonnes sont combinés à l’aide d’une opération AND logique.</span><span class="sxs-lookup"><span data-stu-id="530e9-117">Each GPO attribute and search string pair and each all-column search string are combined by using a logical AND operation.</span></span> <span data-ttu-id="530e9-118">Le résultat est une liste de tous les objets de stratégie de groupe pour lesquels chaque attribut spécifié inclut la chaîne de recherche spécifiée et pour lequel les chaînes de recherche de toutes les colonnes apparaissent dans au moins une colonne.</span><span class="sxs-lookup"><span data-stu-id="530e9-118">The result is a list of all GPOs for which each specified attribute includes the specified search string and for which any all-column search strings appear in at least one column.</span></span> <span data-ttu-id="530e9-119">La recherche renvoie des correspondances partielles pour les chaînes, afin que vous puissiez entrer une partie du nom de l’objet GPO ou du nom d’utilisateur et afficher la liste de tous les objets de stratégie de groupe qui incluent ce texte dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="530e9-119">The search returns any partial matches for strings so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="530e9-120">Voici quelques exemples de recherche:</span><span class="sxs-lookup"><span data-stu-id="530e9-120">The following are examples of searches:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="530e9-121">Description du résultat de la recherche</span><span class="sxs-lookup"><span data-stu-id="530e9-121">Description of search result</span></span></th>
<th align="left"><span data-ttu-id="530e9-122">Requête de recherche</span><span class="sxs-lookup"><span data-stu-id="530e9-122">Search query</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="530e9-123">Tous les objets de stratégie de groupe dont les noms incluent la sécurité du texte <strong> </strong> et l' <strong> Amérique du Nord </strong> .</span><span class="sxs-lookup"><span data-stu-id="530e9-123">All GPOs with names that include the text <strong>security</strong> and <strong>North America</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="530e9-124">nom: </strong><strong> nom de sécurité </strong><strong> : </strong> &quot; <strong> Amérique du Nord</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="530e9-124">name:</strong><strong>security</strong><strong>name:</strong>&quot;<strong>North America</strong>&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="530e9-125">Tous les objets de stratégie de groupe extraits.</span><span class="sxs-lookup"><span data-stu-id="530e9-125">All checked out GPOs.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="530e9-126">État: </strong> &quot; <strong> extrait</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="530e9-126">state:</strong>&quot;<strong>checked out</strong>&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="530e9-127">Tous les objets de stratégie de groupe modifiés le plus récemment par l’utilisateur nommé <strong> administrateur </strong> et récemment modifiés au cours du mois précédent.</span><span class="sxs-lookup"><span data-stu-id="530e9-127">All GPOs most recently changed by the user named <strong>Administrator</strong> and most recently changed within the previous month.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="530e9-128">modifié par: </strong><strong> Date de modification de l’administrateur </strong><strong> : </strong><strong> lastmonth</span><span class="sxs-lookup"><span data-stu-id="530e9-128">changed by:</strong><strong>Administrator</strong><strong>change date:</strong><strong>lastmonth</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="530e9-129">Tous les objets de stratégie de groupe dans lesquels le <strong> pare-feu Word </strong> est inclus dans le commentaire le plus récent et dans lequel la sécurité du mot <strong> </strong> apparaît dans n’importe quelle colonne.</span><span class="sxs-lookup"><span data-stu-id="530e9-129">All GPOs in which the word <strong>firewall</strong> is included in the most recent comment and in which the word <strong>security</strong> appears in any column.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="530e9-130">Commentaire: </strong><strong> sécurité du pare-feu </strong><strong></span><span class="sxs-lookup"><span data-stu-id="530e9-130">comment:</strong><strong>firewall</strong><strong>security</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="530e9-131">Tous les objets de stratégie de groupe dont le statut est <strong> désactivé </strong> .</span><span class="sxs-lookup"><span data-stu-id="530e9-131">All GPOs that have a status of <strong>All Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="530e9-132">État de l’objet GPO: </strong><strong> tout</span><span class="sxs-lookup"><span data-stu-id="530e9-132">gpo status:</strong><strong>all</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="530e9-133">Tous les objets de stratégie de groupe qui disposent d’un filtre WMI appelé <strong> filtre WMI </strong> appliqué et dont le statut de configuration de l' <strong> utilisateur est désactivé </strong> .</span><span class="sxs-lookup"><span data-stu-id="530e9-133">All GPOs that have a WMI filter named <strong>My WMI Filter</strong> applied and that have a status of <strong>User Configuration Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="530e9-134">filtre WMI: </strong> &quot; <strong> mon état de GPO filtre WMI </strong> &quot; <strong> : </strong><strong> utilisateur</span><span class="sxs-lookup"><span data-stu-id="530e9-134">wmi filter:</strong>&quot;<strong>My WMI Filter</strong>&quot;<strong>gpo status:</strong><strong>user</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="530e9-135">Spécification de dates</span><span class="sxs-lookup"><span data-stu-id="530e9-135">Specifying dates</span></span>


<span data-ttu-id="530e9-136">Vous pouvez rechercher des objets de stratégie de groupe modifiés à une date spécifique, à une heure spécifique ou pendant un laps de temps en utilisant les mêmes conditions spéciales disponibles lorsque vous recherchez dans Windows.</span><span class="sxs-lookup"><span data-stu-id="530e9-136">You can search for GPOs changed on a specific date, at a specific time, or during a span of time by using the same special terms available when you search in Windows.</span></span> <span data-ttu-id="530e9-137">Si vous entrez une date ou une heure spécifique, vous devez utiliser le format utilisé dans la colonne de **Date de modification** .</span><span class="sxs-lookup"><span data-stu-id="530e9-137">If entering a specific date or time, you must use the format that is used in the **Change Date** column.</span></span> <span data-ttu-id="530e9-138">Vous trouverez ci-dessous des exemples de recherches dans la colonne **Date de modification** :</span><span class="sxs-lookup"><span data-stu-id="530e9-138">The following are examples of searches of the **Change Date** column:</span></span>

-   <span data-ttu-id="530e9-139">**changer la date:\*\*\*\*10/10/2009**</span><span class="sxs-lookup"><span data-stu-id="530e9-139">**change date:\*\*\*\*10/10/2009**</span></span>

-   <span data-ttu-id="530e9-140">**modification de la date:\*\*\*\*10/10/2009 9:00:00 AM**</span><span class="sxs-lookup"><span data-stu-id="530e9-140">**change date:\*\*\*\*10/10/2009 9:00:00 AM**</span></span>

-   <span data-ttu-id="530e9-141">**changer la date:\*\*\*\*thisweek**</span><span class="sxs-lookup"><span data-stu-id="530e9-141">**change date:\*\*\*\*thisweek**</span></span>

<span data-ttu-id="530e9-142">Vous pouvez utiliser les conditions spéciales suivantes, qui ne respectent pas la casse, lorsque vous effectuez une recherche dans la colonne **changer la date** :</span><span class="sxs-lookup"><span data-stu-id="530e9-142">You can use the following special terms, which are not case-sensitive, when you search the **Change Date** column:</span></span>

-   **<span data-ttu-id="530e9-143">Aujourd’hui</span><span class="sxs-lookup"><span data-stu-id="530e9-143">Today</span></span>**

-   **<span data-ttu-id="530e9-144">Hier</span><span class="sxs-lookup"><span data-stu-id="530e9-144">Yesterday</span></span>**

-   **<span data-ttu-id="530e9-145">ThisWeek</span><span class="sxs-lookup"><span data-stu-id="530e9-145">ThisWeek</span></span>**

-   **<span data-ttu-id="530e9-146">LastWeek</span><span class="sxs-lookup"><span data-stu-id="530e9-146">LastWeek</span></span>**

-   **<span data-ttu-id="530e9-147">ThisMonth</span><span class="sxs-lookup"><span data-stu-id="530e9-147">ThisMonth</span></span>**

-   **<span data-ttu-id="530e9-148">LastMonth</span><span class="sxs-lookup"><span data-stu-id="530e9-148">LastMonth</span></span>**

-   **<span data-ttu-id="530e9-149">TwoMonths</span><span class="sxs-lookup"><span data-stu-id="530e9-149">TwoMonths</span></span>**

-   **<span data-ttu-id="530e9-150">ThreeMonths</span><span class="sxs-lookup"><span data-stu-id="530e9-150">ThreeMonths</span></span>**

-   **<span data-ttu-id="530e9-151">ThisYear</span><span class="sxs-lookup"><span data-stu-id="530e9-151">ThisYear</span></span>**

-   **<span data-ttu-id="530e9-152">LastYear</span><span class="sxs-lookup"><span data-stu-id="530e9-152">LastYear</span></span>**

### <span data-ttu-id="530e9-153">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="530e9-153">Additional considerations</span></span>

-   <span data-ttu-id="530e9-154">Par défaut, vous devez être un réviseur, un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="530e9-154">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="530e9-155">Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="530e9-155">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="530e9-156">Pour plus d’informations sur les attributs d’objets de stratégie de groupe, voir fonctionnalités de l' [onglet contenu](contents-tab-features-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="530e9-156">For more information about GPO attributes, see [Contents Tab Features](contents-tab-features-agpm40.md).</span></span>

### <span data-ttu-id="530e9-157">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="530e9-157">Additional references</span></span>

-   [<span data-ttu-id="530e9-158">Gestion avancée des stratégies de groupe4.0</span><span class="sxs-lookup"><span data-stu-id="530e9-158">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 






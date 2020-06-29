---
title: Fonctionnalités courantes de l'onglet secondaire
description: Fonctionnalités courantes de l'onglet secondaire
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807766"
---
# <span data-ttu-id="2c99c-103">Fonctionnalités courantes de l'onglet secondaire</span><span class="sxs-lookup"><span data-stu-id="2c99c-103">Common Secondary Tab Features</span></span>


<span data-ttu-id="2c99c-104">Chaque onglet secondaire comporte deux sections:**objets** et **groupes de stratégie de**groupe.</span><span class="sxs-lookup"><span data-stu-id="2c99c-104">Each secondary tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="2c99c-105">Section objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2c99c-105">Group Policy objects section</span></span>


<span data-ttu-id="2c99c-106">La section **objets de stratégie de groupe** affiche la liste filtrée d’objets de stratégie de groupe et identifie les caractéristiques suivantes pour chaque GPO:</span><span class="sxs-lookup"><span data-stu-id="2c99c-106">The **Group Policy objects** section displays a filtered list of Group Policy objects (GPOs) and identifies the following characteristics for each GPO:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2c99c-107">Caractéristique de l’objet GPO</span><span class="sxs-lookup"><span data-stu-id="2c99c-107">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="2c99c-108">Description</span><span class="sxs-lookup"><span data-stu-id="2c99c-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2c99c-109">Name</span><span class="sxs-lookup"><span data-stu-id="2c99c-109">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-110">Nom de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2c99c-110">Name of the Group Policy object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2c99c-111">Ordinateur (COMP.)</span><span class="sxs-lookup"><span data-stu-id="2c99c-111">Computer (Comp.)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-112">Version générée automatiquement de la partie configuration de l’ordinateur de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2c99c-112">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2c99c-113">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="2c99c-113">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-114">Version générée automatiquement de la section Configuration utilisateur de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2c99c-114">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2c99c-115">État</span><span class="sxs-lookup"><span data-stu-id="2c99c-115">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-116">État de l’objet de stratégie de groupe sélectionné:</span><span class="sxs-lookup"><span data-stu-id="2c99c-116">The state of the selected GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="2c99c-117">Non contrôlé: </strong> non géré par AGPM.</span><span class="sxs-lookup"><span data-stu-id="2c99c-117">Uncontrolled:</strong> Not managed by AGPM.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="2c99c-118">Archivé: </strong> disponible pour les éditeurs autorisés à vérifier en modification ou à un administrateur de stratégie de groupe pour procéder au déploiement.</span><span class="sxs-lookup"><span data-stu-id="2c99c-118">Checked In:</strong> Available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="2c99c-119">Extrait: </strong> actuellement modifié.</span><span class="sxs-lookup"><span data-stu-id="2c99c-119">Checked Out:</strong> Currently being edited.</span></span> <span data-ttu-id="2c99c-120">Non disponible pour les autres éditeurs pour le contrôle tant que l’éditeur qui l’a réintégré ou un administrateur AGPM l’a archivé.</span><span class="sxs-lookup"><span data-stu-id="2c99c-120">Unavailable for other Editors to check out until the Editor who checked it out or an AGPM Administrator checks it in.</span></span></p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong><span data-ttu-id="2c99c-121">En attente: en </strong> attente d’approbation d’un administrateur de stratégie de groupe avant de créer, contrôler, déployer ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="2c99c-121">Pending:</strong> Awaiting approval from a Group Policy administrator before being created, controlled, deployed, or deleted.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="2c99c-122">Supprimé: </strong> supprimé de l’archive, mais peut toujours être restauré.</span><span class="sxs-lookup"><span data-stu-id="2c99c-122">Deleted:</strong> Deleted from the archive, but still able to be restored.</span></span></p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong><span data-ttu-id="2c99c-123">Modèle: </strong> version statique d’un objet de stratégie de groupe à utiliser comme point de départ lors de la création de nouveaux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2c99c-123">Template:</strong> A static version of a GPO for use as a starting point when creating new GPOs.</span></span></p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong><span data-ttu-id="2c99c-124">Modèle (par défaut): </strong> par défaut, ce modèle est le point de départ utilisé lors de la création d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2c99c-124">Template (default):</strong> By default, this template is the starting point used when creating a new GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2c99c-125">État de l’objet GPO</span><span class="sxs-lookup"><span data-stu-id="2c99c-125">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-126">La configuration de l’ordinateur et la configuration de l’utilisateur peuvent être gérées séparément.</span><span class="sxs-lookup"><span data-stu-id="2c99c-126">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="2c99c-127">L’état de l’objet de stratégie de groupe indique quelles parties de l’objet de stratégie de groupe sont activées.</span><span class="sxs-lookup"><span data-stu-id="2c99c-127">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2c99c-128">Filtre WMI</span><span class="sxs-lookup"><span data-stu-id="2c99c-128">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-129">Afficher les filtres WMI appliqués à cet objet GPO.</span><span class="sxs-lookup"><span data-stu-id="2c99c-129">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="2c99c-130">Les filtres WMI sont gérés par le <strong> nœud filtres WMI </strong> pour le domaine dans l’arborescence de la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="2c99c-130">WMI filters are managed under the <strong>WMI Filters</strong> node for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2c99c-131">Modifié</span><span class="sxs-lookup"><span data-stu-id="2c99c-131">Modified</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-132">S’il s’agit d’un objet de stratégie de groupe contrôlé, date la plus récente lors de sa modification ou de son extraction.</span><span class="sxs-lookup"><span data-stu-id="2c99c-132">For a controlled GPO, the most recent date when it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="2c99c-133">S’il s’agit d’un objet de stratégie de groupe non contrôlé, date de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="2c99c-133">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2c99c-134">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="2c99c-134">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-135">Éditeur ayant archivé l’objet de stratégie de groupe et l’approbateur qui l’a déployé.</span><span class="sxs-lookup"><span data-stu-id="2c99c-135">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2c99c-136">Section groupes et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2c99c-136">Groups and Users section</span></span>


<span data-ttu-id="2c99c-137">Lorsqu’un objet de stratégie de groupe est sélectionné, la section **groupes et utilisateurs** affiche une liste des groupes et des utilisateurs ayant accès à cet objet.</span><span class="sxs-lookup"><span data-stu-id="2c99c-137">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="2c99c-138">Les autorisations et l’héritage autorisés sont affichés pour chaque groupe ou utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c99c-138">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="2c99c-139">Un administrateur AGPM peut configurer les autorisations à l’aide de rôles AGPM standard (éditeur, approbateur et relecteur) ou d’une combinaison personnalisée d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="2c99c-139">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, and Reviewer) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2c99c-140">Bouton</span><span class="sxs-lookup"><span data-stu-id="2c99c-140">Button</span></span></th>
<th align="left"><span data-ttu-id="2c99c-141">Effet</span><span class="sxs-lookup"><span data-stu-id="2c99c-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2c99c-142">Add</span><span class="sxs-lookup"><span data-stu-id="2c99c-142">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-143">Ajoutez une nouvelle entrée au descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2c99c-143">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="2c99c-144">Tout utilisateur ou groupe dans Active Directory peut être ajouté.</span><span class="sxs-lookup"><span data-stu-id="2c99c-144">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2c99c-145">Supprimer</span><span class="sxs-lookup"><span data-stu-id="2c99c-145">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-146">Supprimer l’entrée sélectionnée de la liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="2c99c-146">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2c99c-147">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c99c-147">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-148">Afficher les propriétés de l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2c99c-148">Display the properties for the selected object.</span></span> <span data-ttu-id="2c99c-149">La page Propriétés est la même que celle affichée pour un objet dans <strong> utilisateurs et ordinateurs Active Directory </strong> .</span><span class="sxs-lookup"><span data-stu-id="2c99c-149">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2c99c-150">Avancé</span><span class="sxs-lookup"><span data-stu-id="2c99c-150">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2c99c-151">Ouvrez l' <strong> éditeur de liste de contrôle d’accès </strong> .</span><span class="sxs-lookup"><span data-stu-id="2c99c-151">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="2c99c-152">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="2c99c-152">Additional considerations</span></span>

-   <span data-ttu-id="2c99c-153">Pour plus d’informations sur les rôles et les autorisations liées à des tâches spécifiques, voir les tâches d' [exécution des tâches d’administration d’AGPM](performing-agpm-administrator-tasks.md), exécution de tâches d' [éditeur](performing-editor-tasks.md), [exécution des tâches approbateurs](performing-approver-tasks.md)et [exécution des tâches de relecteur](performing-reviewer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="2c99c-153">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="2c99c-154">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2c99c-154">Additional references</span></span>

-   [<span data-ttu-id="2c99c-155">Onglet Contenu</span><span class="sxs-lookup"><span data-stu-id="2c99c-155">Contents Tab</span></span>](contents-tab.md)

 

 






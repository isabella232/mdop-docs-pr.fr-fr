---
title: Paramètres de visibilité des fonctionnalités
description: Paramètres de visibilité des fonctionnalités
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808454"
---
# <span data-ttu-id="132e3-103">Paramètres de visibilité des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="132e3-103">Feature Visibility Settings</span></span>


<span data-ttu-id="132e3-104">Les paramètres de modèle d’administration de Advanced Group Policy Management (AGPM) vous permettent de configurer de manière centralisée la visibilité des nœuds de **contrôle de modification** et de l’onglet **historique** pour les administrateurs de stratégie de groupe pour lesquels un objet de stratégie de groupe avec ces paramètres est appliqué.</span><span class="sxs-lookup"><span data-stu-id="132e3-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure the visibility of the **Change Control** node and **History** tab for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="132e3-105">Les paramètres suivants sont disponibles sous utilisateurs Configuration\\Administrative Templates\\Windows Components\\Microsoft de la console de gestion \ \ restrictions/autorisation Snap-ins\\Extension dans l' **éditeur d’objets de stratégie de groupe** lors de la modification d’un objet de stratégie de groupe dans la console de gestion des stratégies de groupe (GPMC).</span><span class="sxs-lookup"><span data-stu-id="132e3-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\Microsoft Management Console\\Restricted/Permitted Snap-ins\\Extension Snap-ins in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="132e3-106">Si ce chemin d’accès n’est pas visible, cliquez avec le bouton droit sur **modèles d’administration**, puis ajoutez le modèle AGPM. admx ou AGPM. adm.</span><span class="sxs-lookup"><span data-stu-id="132e3-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="132e3-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="132e3-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="132e3-108">Effet</span><span class="sxs-lookup"><span data-stu-id="132e3-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="132e3-109">Contrôle du changement d’AGPM</span><span class="sxs-lookup"><span data-stu-id="132e3-109">AGPM Change Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="132e3-110">S’il est activé ou non configuré, le <strong> nœud de contrôle de modification </strong> est visible dans la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="132e3-110">If enabled or not configured, the <strong>Change Control</strong> node is visible in the GPMC.</span></span></p>
<p><span data-ttu-id="132e3-111">S’il est désactivé, le <strong> nœud de contrôle de modification </strong> n’est pas visible dans la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="132e3-111">If disabled, the <strong>Change Control</strong> node is not visible in the GPMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="132e3-112">Extension de lien AGPM</span><span class="sxs-lookup"><span data-stu-id="132e3-112">AGPM Link Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="132e3-113">S’il est activé ou non configuré, un <strong> </strong> onglet historique s’affiche dans la console GPMC pour chaque objet GPO lié.</span><span class="sxs-lookup"><span data-stu-id="132e3-113">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each linked GPO.</span></span></p>
<p><span data-ttu-id="132e3-114">S’il est désactivé, l' <strong> </strong> onglet historique n’est pas visible pour les objets de stratégie de groupe liés.</span><span class="sxs-lookup"><span data-stu-id="132e3-114">If disabled, the <strong>History</strong> tab is not visible for linked GPOs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="132e3-115">Extension d’objet de stratégie de groupe AGPM</span><span class="sxs-lookup"><span data-stu-id="132e3-115">AGPM GPO Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="132e3-116">S’il est activé ou non configuré, un <strong> </strong> onglet historique s’affiche dans la console GPMC pour chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="132e3-116">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each GPO.</span></span></p>
<p><span data-ttu-id="132e3-117">S’il est désactivé, l' <strong> </strong> onglet historique n’est pas visible pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="132e3-117">If disabled, the <strong>History</strong> tab is not visible for GPOs.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="132e3-118">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="132e3-118">Additional references</span></span>

-   [<span data-ttu-id="132e3-119">Paramètres de modèles d'administration</span><span class="sxs-lookup"><span data-stu-id="132e3-119">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 






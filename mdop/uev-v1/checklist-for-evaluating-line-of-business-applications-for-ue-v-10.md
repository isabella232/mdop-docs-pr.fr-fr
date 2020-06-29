---
title: Liste de contrôle pour l'évaluation des applications cœur de métier pour UE-V1.0
description: Liste de contrôle pour l'évaluation des applications cœur de métier pour UE-V1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811766"
---
# <span data-ttu-id="13338-103">Liste de contrôle pour l'évaluation des applications cœur de métier pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="13338-103">Checklist for Evaluating Line-of-Business Applications for UE-V 1.0</span></span>


<span data-ttu-id="13338-104">Pour évaluer les applications métier qui doivent être incluses dans votre déploiement UE-V, envisagez ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="13338-104">To evaluate which line-of-business applications should be included in your UE-V deployment, consider the following:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="13338-105">Description</span><span class="sxs-lookup"><span data-stu-id="13338-105">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="13338-106">Cette application contient-elle des paramètres que l’utilisateur peut personnaliser?</span><span class="sxs-lookup"><span data-stu-id="13338-106">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="13338-107">Est-il important de l’itinérance de ces paramètres?</span><span class="sxs-lookup"><span data-stu-id="13338-107">Is it important for the user that these settings roam?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="13338-108">Ces paramètres utilisateur sont-ils déjà gérés par une solution de gestion des applications ou de stratégie de paramètres?</span><span class="sxs-lookup"><span data-stu-id="13338-108">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="13338-109">UE-V applique les paramètres d’application au lancement de l’application et aux paramètres Windows lors de l’ouverture de session, du déverrouillage ou des événements de connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="13338-109">UE-V applies application settings at application launch and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="13338-110">Si vous utilisez UE-V avec d’autres solutions de stratégie de contrôle, les utilisateurs peuvent observer une incohérence entre les paramètres errants.</span><span class="sxs-lookup"><span data-stu-id="13338-110">If you use UE-V with other settings policy solutions, users might experience inconsistency across roamed settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="13338-111">Les paramètres de l’application sont-ils spécifiques de votre ordinateur?</span><span class="sxs-lookup"><span data-stu-id="13338-111">Are the application settings specific to the computer?</span></span> <span data-ttu-id="13338-112">Les préférences et personnalisations apportées à l’application qui sont associées à des configurations matérielles ou spécifiques à des ordinateurs ne sont pas toujours itinérantes entre les sessions et peuvent entraîner une faible connaissance de l’application.</span><span class="sxs-lookup"><span data-stu-id="13338-112">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently roam across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="13338-113">Est-ce que les paramètres du Windows Store se trouvent dans le dossier Program Files ou dans le répertoire de fichiers qui se trouve dans le répertoire <strong> Users </strong> \ [user name] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ?</span><span class="sxs-lookup"><span data-stu-id="13338-113">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong> \ [User name] \ <strong>AppData</strong> \ <strong>LocalLow</strong> directory?</span></span> <span data-ttu-id="13338-114">Les données d’application stockées dans l’un de ces emplacements ne doivent généralement pas être itinérantes avec l’utilisateur, car ces données sont spécifiques à l’ordinateur ou les données sont trop volumineuses pour une itinérance.</span><span class="sxs-lookup"><span data-stu-id="13338-114">Application data that is stored in either of these locations usually should not roam with the user, because this data is specific to the computer or because the data is too large to roam.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="13338-115">L’application stocke-t-elle des paramètres dans un fichier qui contient d’autres données d’application qui ne doivent pas être itinérantes?</span><span class="sxs-lookup"><span data-stu-id="13338-115">Does the application store any settings in a file that contains other application data that should not roam?</span></span> <span data-ttu-id="13338-116">UE-V synchronise les fichiers comme une seule unité.</span><span class="sxs-lookup"><span data-stu-id="13338-116">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="13338-117">Si les paramètres sont stockés dans des fichiers qui incluent des données d’application autres que des paramètres, la synchronisation de ces données supplémentaires risque de provoquer une médiocre application.</span><span class="sxs-lookup"><span data-stu-id="13338-117">If settings are stored in files that include application data other than settings, then synchronizing this additional data may cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="13338-118">Quelle est la taille des fichiers contenant les paramètres?</span><span class="sxs-lookup"><span data-stu-id="13338-118">How large are the files that contain the settings?</span></span> <span data-ttu-id="13338-119">Les performances de la synchronisation des paramètres peuvent être affectées par de gros fichiers.</span><span class="sxs-lookup"><span data-stu-id="13338-119">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="13338-120">L’inclusion de fichiers volumineux peut avoir un impact sur les performances de la synchronisation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="13338-120">Including large files can impact the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="13338-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13338-121">Related topics</span></span>


[<span data-ttu-id="13338-122">Planification de méthodes de configuration d'UE-V</span><span class="sxs-lookup"><span data-stu-id="13338-122">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

[<span data-ttu-id="13338-123">Planification pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="13338-123">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

 

 






---
title: DELETE APP
description: DELETE APP
author: dansimp
ms.assetid: 2f89c0c0-373b-4389-a26d-67b3f9712957
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c27c70ef3227ebaf6b16bcb1fbb4b4e65b7cb7f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808922"
---
# <span data-ttu-id="ba9f9-103">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="ba9f9-103">DELETE APP</span></span>


<span data-ttu-id="ba9f9-104">Supprime un enregistrement d’application du cache du système de fichiers pour ne plus être visible.</span><span class="sxs-lookup"><span data-stu-id="ba9f9-104">Removes an application record from the file system cache to make it no longer visible.</span></span> <span data-ttu-id="ba9f9-105">Les raccourcis des utilisateurs et les associations de types de fichiers sont masqués mais ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="ba9f9-105">Users’ shortcuts and file type associations are hidden but not deleted.</span></span> <span data-ttu-id="ba9f9-106">Aucun paramètre utilisateur n’est supprimé.</span><span class="sxs-lookup"><span data-stu-id="ba9f9-106">No user settings are removed.</span></span>

`SFTMIME DELETE APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ba9f9-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ba9f9-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="ba9f9-108">Description</span><span class="sxs-lookup"><span data-stu-id="ba9f9-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba9f9-109">Application: &lt; application&gt;</span><span class="sxs-lookup"><span data-stu-id="ba9f9-109">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba9f9-110">Nom et version (facultatif) de l’application à supprimer.</span><span class="sxs-lookup"><span data-stu-id="ba9f9-110">The name and version (optional) of the application to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba9f9-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="ba9f9-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba9f9-112">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="ba9f9-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba9f9-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="ba9f9-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba9f9-114">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="ba9f9-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba9f9-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="ba9f9-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba9f9-116">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="ba9f9-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ba9f9-117">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="ba9f9-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba9f9-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="ba9f9-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba9f9-119">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="ba9f9-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ba9f9-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba9f9-120">Related topics</span></span>


[<span data-ttu-id="ba9f9-121">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="ba9f9-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






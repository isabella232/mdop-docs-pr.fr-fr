---
title: DELETE OBJ
description: DELETE OBJ
author: dansimp
ms.assetid: fb17a261-f378-4ce6-a538-ab2f0ada0f2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d74fc1ac098d7dc4dd2f28633e9ca58d4211d74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808915"
---
# <span data-ttu-id="35dbd-103">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="35dbd-103">DELETE OBJ</span></span>


<span data-ttu-id="35dbd-104">Supprime tous les enregistrements de votre application.</span><span class="sxs-lookup"><span data-stu-id="35dbd-104">Removes all of your application records.</span></span>

`SFTMIME DELETE OBJ:APP [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="35dbd-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="35dbd-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="35dbd-106">Description</span><span class="sxs-lookup"><span data-stu-id="35dbd-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="35dbd-107">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="35dbd-107">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="35dbd-108">Si cette valeur est spécifiée, toutes les applications sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="35dbd-108">If specified, all applications are removed.</span></span> <span data-ttu-id="35dbd-109">Par défaut, seules les applications auxquelles l’utilisateur actuel a accès sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="35dbd-109">By default, only applications the current user has access to are removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="35dbd-110">/LOG</span><span class="sxs-lookup"><span data-stu-id="35dbd-110">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="35dbd-111">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="35dbd-111">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="35dbd-112">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="35dbd-112">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="35dbd-113">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="35dbd-113">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="35dbd-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="35dbd-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="35dbd-115">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="35dbd-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="35dbd-116">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="35dbd-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="35dbd-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="35dbd-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="35dbd-118">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="35dbd-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="35dbd-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35dbd-119">Related topics</span></span>


[<span data-ttu-id="35dbd-120">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="35dbd-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






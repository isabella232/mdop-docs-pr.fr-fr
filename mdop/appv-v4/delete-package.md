---
title: DELETE PACKAGE
description: DELETE PACKAGE
author: dansimp
ms.assetid: 8f7a4598-610d-490e-a224-426acce01a9f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0051967ca308e88d143b8116330f5d770d6086d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808910"
---
# <span data-ttu-id="58e72-103">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="58e72-103">DELETE PACKAGE</span></span>


<span data-ttu-id="58e72-104">Supprime un enregistrement de package et les applications qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="58e72-104">Removes a package record and the applications associated with it.</span></span>

`SFTMIME DELETE PACKAGE:package-name                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="58e72-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="58e72-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="58e72-106">Description</span><span class="sxs-lookup"><span data-stu-id="58e72-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="58e72-107">PACKAGE: &lt; nom du package&gt;</span><span class="sxs-lookup"><span data-stu-id="58e72-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="58e72-108">Nom du package à supprimer.</span><span class="sxs-lookup"><span data-stu-id="58e72-108">The name of the package to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="58e72-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="58e72-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="58e72-110">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="58e72-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="58e72-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="58e72-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="58e72-112">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="58e72-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="58e72-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="58e72-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="58e72-114">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="58e72-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="58e72-115">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="58e72-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="58e72-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="58e72-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="58e72-117">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="58e72-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="58e72-118">**Important**  La commande supprimer le PACKAGE effectue toujours une suppression globale du package et supprime uniquement les types et raccourcis de fichiers globaux.</span><span class="sxs-lookup"><span data-stu-id="58e72-118">**Important** The DELETE PACKAGE command always performs a global delete of the package and deletes only global file types and shortcuts.</span></span>

<span data-ttu-id="58e72-119">S’il s’agit d’un package global, cette commande doit être exécutée en tant qu’administrateur local; dans le cas contraire, seule une autorisation **DeleteApp** est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="58e72-119">If the package is global, this command must be run as local Administrator; otherwise, only **DeleteApp** permission is needed.</span></span>

 

## <span data-ttu-id="58e72-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58e72-120">Related topics</span></span>


[<span data-ttu-id="58e72-121">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="58e72-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






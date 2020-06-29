---
title: DELETE TYPE
description: DELETE TYPE
author: dansimp
ms.assetid: f2852723-c894-49f3-a3c5-56f9648bb9ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0df68c0a0efcd0e269410d1580f7b0a82301c46d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808904"
---
# <span data-ttu-id="3ac26-103">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="3ac26-103">DELETE TYPE</span></span>


<span data-ttu-id="3ac26-104">Supprime l’Association de type de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3ac26-104">Removes the specified file type association.</span></span>

`SFTMIME DELETE TYPE:file-extension [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3ac26-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3ac26-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="3ac26-106">Description</span><span class="sxs-lookup"><span data-stu-id="3ac26-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac26-107">TYPE: &lt; fichier-extension&gt;</span><span class="sxs-lookup"><span data-stu-id="3ac26-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac26-108">Extension de nom de fichier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="3ac26-108">The file name extension to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac26-109">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="3ac26-109">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac26-110">Spécifie si l’Association globale de l’extension de nom de fichier doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="3ac26-110">If specified, indicates that the global association for the file name extension should be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac26-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="3ac26-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac26-112">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="3ac26-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac26-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="3ac26-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac26-114">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="3ac26-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac26-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="3ac26-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac26-116">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="3ac26-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3ac26-117">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="3ac26-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac26-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="3ac26-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac26-119">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="3ac26-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3ac26-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ac26-120">Related topics</span></span>


[<span data-ttu-id="3ac26-121">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="3ac26-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






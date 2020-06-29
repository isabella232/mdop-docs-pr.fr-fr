---
title: LOCK APP
description: LOCK APP
author: dansimp
ms.assetid: 30673433-4364-499f-8116-cb135fe2716f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 319271640c2550fc94479e876a59b30d3b2bf7ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806629"
---
# <span data-ttu-id="c2776-103">LOCK APP</span><span class="sxs-lookup"><span data-stu-id="c2776-103">LOCK APP</span></span>


<span data-ttu-id="c2776-104">Verrouille l’application spécifiée dans le cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c2776-104">Locks the application specified in the file system cache.</span></span>

`SFTMIME LOCK APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2776-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c2776-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="c2776-106">Description</span><span class="sxs-lookup"><span data-stu-id="c2776-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2776-107">Application: &lt; application&gt;</span><span class="sxs-lookup"><span data-stu-id="c2776-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2776-108">Nom et version (facultatif) de l’application à verrouiller.</span><span class="sxs-lookup"><span data-stu-id="c2776-108">The name and version (optional) of the application to lock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2776-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="c2776-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2776-110">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="c2776-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2776-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="c2776-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2776-112">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="c2776-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2776-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="c2776-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2776-114">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="c2776-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2776-115">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="c2776-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2776-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="c2776-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2776-117">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c2776-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c2776-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2776-118">Related topics</span></span>


[<span data-ttu-id="c2776-119">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="c2776-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






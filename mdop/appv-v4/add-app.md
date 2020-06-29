---
title: ADD APP
description: ADD APP
author: dansimp
ms.assetid: 329fd0c8-a795-49be-b0fd-1367c5b4a34b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac83c0cf130e8de1d34d42d74e946716e4503246
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808090"
---
# <span data-ttu-id="fc844-103">ADD APP</span><span class="sxs-lookup"><span data-stu-id="fc844-103">ADD APP</span></span>


<span data-ttu-id="fc844-104">Ajoute un enregistrement d’application.</span><span class="sxs-lookup"><span data-stu-id="fc844-104">Adds an application record.</span></span>

`SFTMIME ADD APP:application /OSD osd-pathname [/ICON icon-pathname] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc844-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="fc844-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="fc844-106">Description</span><span class="sxs-lookup"><span data-stu-id="fc844-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc844-107">Application: &lt; application&gt;</span><span class="sxs-lookup"><span data-stu-id="fc844-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc844-108">Nom et version (facultatif) de l’application.</span><span class="sxs-lookup"><span data-stu-id="fc844-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc844-109">/OSD &lt; OSD-nomchemin&gt;</span><span class="sxs-lookup"><span data-stu-id="fc844-109">/OSD &lt;osd-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc844-110">Chemin ou URL du fichier OSD.</span><span class="sxs-lookup"><span data-stu-id="fc844-110">The path or URL for the OSD file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc844-111">&lt;Icône/Icon-chemin&gt;</span><span class="sxs-lookup"><span data-stu-id="fc844-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc844-112">Path ou URL du fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="fc844-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc844-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="fc844-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc844-114">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="fc844-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc844-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="fc844-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc844-116">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="fc844-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc844-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="fc844-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc844-118">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="fc844-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fc844-119">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="fc844-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc844-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="fc844-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc844-121">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="fc844-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fc844-122">**Remarques**  Le nom obtenu pour l’application sera tiré du fichier OSD et non du nom fourni dans &lt; application: application &gt; .</span><span class="sxs-lookup"><span data-stu-id="fc844-122">**Note** The resulting name of the application will be taken from the OSD file and not from the name provided in APP:&lt;application&gt;.</span></span>

 

## <span data-ttu-id="fc844-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc844-123">Related topics</span></span>


[<span data-ttu-id="fc844-124">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="fc844-124">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






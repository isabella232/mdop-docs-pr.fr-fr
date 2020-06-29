---
title: CONFIGURE APP
description: CONFIGURE APP
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807882"
---
# <span data-ttu-id="8f3b5-103">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="8f3b5-103">CONFIGURE APP</span></span>


<span data-ttu-id="8f3b5-104">Permet à l’utilisateur de modifier l’icône associée à une application, mais ne met pas à jour l’icône sur les raccourcis existants ou les associations de types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8f3b5-104">Enables the user to change the icon associated with an application but does not update the icon on existing shortcuts or file type associations.</span></span>

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8f3b5-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8f3b5-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="8f3b5-106">Description</span><span class="sxs-lookup"><span data-stu-id="8f3b5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f3b5-107">Application: &lt; application&gt;</span><span class="sxs-lookup"><span data-stu-id="8f3b5-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f3b5-108">Nom et version (facultatif) de l’application.</span><span class="sxs-lookup"><span data-stu-id="8f3b5-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8f3b5-109">&lt;Icône/Icon-chemin&gt;</span><span class="sxs-lookup"><span data-stu-id="8f3b5-109">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f3b5-110">Path ou URL du fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="8f3b5-110">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f3b5-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="8f3b5-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f3b5-112">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="8f3b5-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8f3b5-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="8f3b5-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f3b5-114">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="8f3b5-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f3b5-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="8f3b5-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f3b5-116">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="8f3b5-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8f3b5-117">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="8f3b5-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f3b5-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="8f3b5-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f3b5-119">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="8f3b5-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8f3b5-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f3b5-120">Related topics</span></span>


[<span data-ttu-id="8f3b5-121">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="8f3b5-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






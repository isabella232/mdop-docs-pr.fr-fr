---
title: UNLOAD PACKAGE
description: UNLOAD PACKAGE
author: dansimp
ms.assetid: a076eb5a-ce3d-49e4-ac7a-4d4df10e3477
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fbee040f97bf5675ace7e873741a4270a993a911
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806190"
---
# <span data-ttu-id="9cd2d-103">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="9cd2d-103">UNLOAD PACKAGE</span></span>


<span data-ttu-id="9cd2d-104">Décharge le package du cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9cd2d-104">Unloads the package from the file system cache.</span></span>

`SFTMIME UNLOAD PACKAGE:package-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9cd2d-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="9cd2d-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="9cd2d-106">Description</span><span class="sxs-lookup"><span data-stu-id="9cd2d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9cd2d-107">PACKAGE: &lt; nom du package&gt;</span><span class="sxs-lookup"><span data-stu-id="9cd2d-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="9cd2d-108">Nom du package à décharger.</span><span class="sxs-lookup"><span data-stu-id="9cd2d-108">The name of the package to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9cd2d-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="9cd2d-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="9cd2d-110">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="9cd2d-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9cd2d-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="9cd2d-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="9cd2d-112">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="9cd2d-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9cd2d-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="9cd2d-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="9cd2d-114">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="9cd2d-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9cd2d-115">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="9cd2d-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9cd2d-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="9cd2d-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="9cd2d-117">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="9cd2d-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9cd2d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9cd2d-118">Related topics</span></span>


[<span data-ttu-id="9cd2d-119">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="9cd2d-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






---
title: UNLOCK APP
description: UNLOCK APP
author: dansimp
ms.assetid: 91fc8ceb-b4f5-4a06-8193-05189f830943
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ea47191450014856b4a9823728e3e275c7fb4cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806189"
---
# <span data-ttu-id="3b415-103">UNLOCK APP</span><span class="sxs-lookup"><span data-stu-id="3b415-103">UNLOCK APP</span></span>


<span data-ttu-id="3b415-104">Déverrouille l’application spécifiée dans le cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3b415-104">Unlocks the application specified in the file system cache.</span></span>

`SFTMIME UNLOCK APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3b415-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3b415-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="3b415-106">Description</span><span class="sxs-lookup"><span data-stu-id="3b415-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3b415-107">Application: &lt; application&gt;</span><span class="sxs-lookup"><span data-stu-id="3b415-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3b415-108">Nom et version (facultatif) de l’application à déverrouiller.</span><span class="sxs-lookup"><span data-stu-id="3b415-108">The name and version (optional) of the application to unlock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3b415-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="3b415-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="3b415-110">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="3b415-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3b415-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="3b415-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3b415-112">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="3b415-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3b415-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="3b415-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="3b415-114">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="3b415-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3b415-115">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="3b415-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3b415-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="3b415-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="3b415-117">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="3b415-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3b415-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b415-118">Related topics</span></span>


[<span data-ttu-id="3b415-119">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="3b415-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






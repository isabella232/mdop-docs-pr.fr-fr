---
title: UNLOAD APP
description: UNLOAD APP
author: dansimp
ms.assetid: f0d729ae-8772-498b-be11-1a4b35499c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1ae30f5b8c788f8763c2c2b9d1c1956182750d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806193"
---
# <span data-ttu-id="19bc5-103">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="19bc5-103">UNLOAD APP</span></span>


<span data-ttu-id="19bc5-104">Décharge l’application et toutes les autres applications du package à partir du cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="19bc5-104">Unloads the application and all other applications in the package from the file system cache.</span></span>

`SFTMIME UNLOAD APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="19bc5-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="19bc5-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="19bc5-106">Description</span><span class="sxs-lookup"><span data-stu-id="19bc5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19bc5-107">Application: &lt; application&gt;</span><span class="sxs-lookup"><span data-stu-id="19bc5-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="19bc5-108">Nom et version (facultatif) de l’application à décharger.</span><span class="sxs-lookup"><span data-stu-id="19bc5-108">The name and version (optional) of the application to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19bc5-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="19bc5-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="19bc5-110">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="19bc5-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19bc5-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="19bc5-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="19bc5-112">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="19bc5-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19bc5-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="19bc5-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="19bc5-114">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="19bc5-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="19bc5-115">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="19bc5-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19bc5-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="19bc5-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="19bc5-117">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="19bc5-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="19bc5-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19bc5-118">Related topics</span></span>


[<span data-ttu-id="19bc5-119">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="19bc5-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






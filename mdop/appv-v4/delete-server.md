---
title: DELETE SERVER
description: DELETE SERVER
author: dansimp
ms.assetid: 4c929639-1c1d-47c3-9225-cc4d7a8736f0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92af31a818174fb4b0e82a11c918af2484ac2bce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808909"
---
# <span data-ttu-id="3d299-103">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="3d299-103">DELETE SERVER</span></span>


<span data-ttu-id="3d299-104">Supprime un serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="3d299-104">Removes a publishing server.</span></span>

<span data-ttu-id="3d299-105">**Remarques**  Cette commande n’entraîne pas la suppression des applications ou packages publiés sur le client par le serveur.</span><span class="sxs-lookup"><span data-stu-id="3d299-105">**Note** This command does not remove any applications or packages published to the client by the server.</span></span> <span data-ttu-id="3d299-106">Pour chaque application, utilisez la commande SFTMIME **Clear app** suivie de la commande **supprimer le package** pour supprimer complètement ces applications et packages du client.</span><span class="sxs-lookup"><span data-stu-id="3d299-106">For each application, use the SFTMIME **CLEAR APP** command followed by the **DELETE PACKAGE** command to completely remove those applications and packages from the client.</span></span>

 

`SFTMIME DELETE SERVER:server-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d299-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3d299-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="3d299-108">Description</span><span class="sxs-lookup"><span data-stu-id="3d299-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d299-109">SERVEUR: &lt; nom du serveur&gt;</span><span class="sxs-lookup"><span data-stu-id="3d299-109">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d299-110">Nom d’affichage du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="3d299-110">The display name of the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d299-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="3d299-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d299-112">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="3d299-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d299-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="3d299-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d299-114">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="3d299-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d299-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="3d299-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d299-116">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="3d299-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3d299-117">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="3d299-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d299-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="3d299-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d299-119">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="3d299-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3d299-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d299-120">Related topics</span></span>


[<span data-ttu-id="3d299-121">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="3d299-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






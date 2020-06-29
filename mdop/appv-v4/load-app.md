---
title: LOAD APP
description: LOAD APP
author: dansimp
ms.assetid: 7b727d0c-5423-419d-92ef-7ebbc6343e79
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02bd6e35da898f5b34f7efc21cbc01a72d555b8d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806630"
---
# <span data-ttu-id="e37be-103">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="e37be-103">LOAD APP</span></span>


<span data-ttu-id="e37be-104">Charge l’application spécifiée et toutes les autres applications du package dans le cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e37be-104">Loads the specified application and all other applications in the package into the file system cache.</span></span>

<span data-ttu-id="e37be-105">**Remarques**  La commande **charger l’application** démarre le processus de chargement et une barre de progression s’affiche dans la zone de notification du bureau.</span><span class="sxs-lookup"><span data-stu-id="e37be-105">**Note** The **LOAD APP** command starts the load process and a progress bar is displayed in the Desktop Notification Area.</span></span> <span data-ttu-id="e37be-106">La commande s’arrête immédiatement après le démarrage du processus, de sorte que toutes les erreurs de chargement apparaissent au même endroit.</span><span class="sxs-lookup"><span data-stu-id="e37be-106">The command exits immediately after starting this process, so any load errors are displayed in the same location.</span></span> <span data-ttu-id="e37be-107">Utilisez la commande **charger le package** si vous voulez démarrer le processus de chargement à partir de la ligne de commande sans utiliser la zone de notification du bureau.</span><span class="sxs-lookup"><span data-stu-id="e37be-107">Use the **LOAD PACKAGE** command if you want to start the load process from the command line without using the Desktop Notification Area.</span></span>

 

`SFTMIME LOAD APP:application [/LOG log-pathname | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e37be-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e37be-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="e37be-109">Description</span><span class="sxs-lookup"><span data-stu-id="e37be-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e37be-110">Application: &lt; application&gt;</span><span class="sxs-lookup"><span data-stu-id="e37be-110">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e37be-111">Nom et version (facultatif) de l’application à charger.</span><span class="sxs-lookup"><span data-stu-id="e37be-111">The name and version (optional) of the application to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e37be-112">/LOG</span><span class="sxs-lookup"><span data-stu-id="e37be-112">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="e37be-113">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="e37be-113">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e37be-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="e37be-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="e37be-115">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="e37be-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e37be-116">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="e37be-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e37be-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="e37be-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="e37be-118">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e37be-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e37be-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e37be-119">Related topics</span></span>


[<span data-ttu-id="e37be-120">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="e37be-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






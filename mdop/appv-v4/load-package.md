---
title: LOAD PACKAGE
description: LOAD PACKAGE
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806626"
---
# <span data-ttu-id="87610-103">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="87610-103">LOAD PACKAGE</span></span>


<span data-ttu-id="87610-104">Charge le package spécifié dans le cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="87610-104">Loads the specified package into the file system cache.</span></span>

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87610-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="87610-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="87610-106">Description</span><span class="sxs-lookup"><span data-stu-id="87610-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87610-107">PACKAGE: &lt; nom du package&gt;</span><span class="sxs-lookup"><span data-stu-id="87610-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="87610-108">Nom du package à charger.</span><span class="sxs-lookup"><span data-stu-id="87610-108">The name of the package to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87610-109">/SFTPATH &lt; SFT-nomchemin&gt;</span><span class="sxs-lookup"><span data-stu-id="87610-109">/SFTPATH &lt;sft-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="87610-110">Spécifie le chemin d’accès d’un fichier SFT à partir duquel charger.</span><span class="sxs-lookup"><span data-stu-id="87610-110">If specified, the path to an SFT file to load from.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87610-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="87610-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="87610-112">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="87610-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87610-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="87610-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="87610-114">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="87610-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87610-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="87610-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="87610-116">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="87610-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="87610-117">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="87610-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87610-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="87610-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="87610-119">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="87610-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="87610-120">**Remarques**  Si aucun SFTPATH n’est spécifié, le client charge le package à l’aide du chemin d’accès configuré pour une utilisation, en fonction du fichier OSD, de la valeur de clé de registre ApplicationSourceRoot ou du paramètre OverrideURL.</span><span class="sxs-lookup"><span data-stu-id="87610-120">**Note** If no SFTPATH is specified, the client will load the package by using the path it has been configured to use, based on the OSD file, the ApplicationSourceRoot registry key value, or the OverrideURL setting.</span></span>

<span data-ttu-id="87610-121">La commande **charger le package** exécute une charge synchrone et ne sera pas exécutée tant que le package n’est pas entièrement chargé ou qu’il rencontre une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="87610-121">The **LOAD PACKAGE** command performs a synchronous load and will not be complete until the package is fully loaded or until it encounters an error condition.</span></span>

 

## <span data-ttu-id="87610-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87610-122">Related topics</span></span>


[<span data-ttu-id="87610-123">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="87610-123">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






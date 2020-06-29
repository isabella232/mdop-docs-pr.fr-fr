---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806458"
---
# <span data-ttu-id="38ff0-103">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="38ff0-103">PUBLISH APP</span></span>


<span data-ttu-id="38ff0-104">Publie le raccourci d’une application dans le menu Démarrer, le bureau ou un autre emplacement spécifié de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38ff0-104">Publishes an application shortcut to the user's Start menu, desktop, or other specified location.</span></span>

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="38ff0-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="38ff0-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="38ff0-106">Description</span><span class="sxs-lookup"><span data-stu-id="38ff0-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38ff0-107">APPLICATION: &lt; application&gt;</span><span class="sxs-lookup"><span data-stu-id="38ff0-107">APPLICATION:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-108">Nom et version (facultatif) de l’application.</span><span class="sxs-lookup"><span data-stu-id="38ff0-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="38ff0-109">/DESKTOP</span><span class="sxs-lookup"><span data-stu-id="38ff0-109">/DESKTOP</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-110">Publie un raccourci vers le Bureau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38ff0-110">Publishes a shortcut to the user's desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38ff0-111">/START</span><span class="sxs-lookup"><span data-stu-id="38ff0-111">/START</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-112">Publie un raccourci vers le dossier applications de virtualisation des applications dans le dossier programmes du menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="38ff0-112">Publishes a shortcut to the Application Virtualization Applications folder in the Programs folder of the Start menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="38ff0-113">/TARGET &lt; target-Path&gt;</span><span class="sxs-lookup"><span data-stu-id="38ff0-113">/TARGET &lt;target-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-114">Le chemin d’accès absolu dans lequel le raccourci doit être publié.</span><span class="sxs-lookup"><span data-stu-id="38ff0-114">The absolute path where the shortcut should be published.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38ff0-115">&lt;Icône/Icon-chemin&gt;</span><span class="sxs-lookup"><span data-stu-id="38ff0-115">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-116">Path ou URL du fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="38ff0-116">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="38ff0-117">&lt;Nom d’affichage de/Display&gt;</span><span class="sxs-lookup"><span data-stu-id="38ff0-117">/DISPLAY &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-118">Nom d’affichage pour le raccourci.</span><span class="sxs-lookup"><span data-stu-id="38ff0-118">The display name for the shortcut.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38ff0-119">&lt;Commande/args&gt;</span><span class="sxs-lookup"><span data-stu-id="38ff0-119">/ARGS &lt;command-args&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-120">Paramètres à transmettre à l’application.</span><span class="sxs-lookup"><span data-stu-id="38ff0-120">Parameters to be passed to the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="38ff0-121">/LOG</span><span class="sxs-lookup"><span data-stu-id="38ff0-121">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-122">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="38ff0-122">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38ff0-123">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="38ff0-123">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-124">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="38ff0-124">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="38ff0-125">/GUI</span><span class="sxs-lookup"><span data-stu-id="38ff0-125">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-126">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="38ff0-126">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="38ff0-127">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="38ff0-127">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38ff0-128">/LOGU</span><span class="sxs-lookup"><span data-stu-id="38ff0-128">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="38ff0-129">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="38ff0-129">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="38ff0-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38ff0-130">Related topics</span></span>


[<span data-ttu-id="38ff0-131">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="38ff0-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






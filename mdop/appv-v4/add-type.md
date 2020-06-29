---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809323"
---
# <span data-ttu-id="84a79-103">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="84a79-103">ADD TYPE</span></span>


<span data-ttu-id="84a79-104">Ajoute l’Association de type de fichier spécifiée.</span><span class="sxs-lookup"><span data-stu-id="84a79-104">Adds the specified file type association.</span></span>

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84a79-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="84a79-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="84a79-106">Description</span><span class="sxs-lookup"><span data-stu-id="84a79-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84a79-107">TYPE: &lt; fichier-extension&gt;</span><span class="sxs-lookup"><span data-stu-id="84a79-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-108">L’extension de nom de fichier qui sera associée à l’application spécifiée.</span><span class="sxs-lookup"><span data-stu-id="84a79-108">The file name extension that will be associated with the application specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84a79-109">&lt;Application/App&gt;</span><span class="sxs-lookup"><span data-stu-id="84a79-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-110">Nom et version (facultatif) de l’application.</span><span class="sxs-lookup"><span data-stu-id="84a79-110">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84a79-111">&lt;Icône/Icon-chemin&gt;</span><span class="sxs-lookup"><span data-stu-id="84a79-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-112">Path ou URL du fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="84a79-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84a79-113">&lt;Type de type/Description-DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="84a79-113">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-114">Nom convivial du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="84a79-114">The user-friendly name for the file type.</span></span> <span data-ttu-id="84a79-115">Par défaut, il s’agit du &quot; fichier d’extension.&quot;</span><span class="sxs-lookup"><span data-stu-id="84a79-115">Defaults to &quot;EXTENSION File.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84a79-116">&lt;Type de contenu/Content-type&gt;</span><span class="sxs-lookup"><span data-stu-id="84a79-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-117">Le type de contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="84a79-117">The content type of the file.</span></span> <span data-ttu-id="84a79-118">Utilise par défaut la valeur &quot; application/Softricity-extension.&quot;</span><span class="sxs-lookup"><span data-stu-id="84a79-118">Defaults to &quot;application/softricity-extension.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84a79-119">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="84a79-119">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-120">Le cas échéant, le package est disponible pour tous les utilisateurs de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="84a79-120">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84a79-121">/PERCEIVED-TYPE &lt; perçu-type&gt;</span><span class="sxs-lookup"><span data-stu-id="84a79-121">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-122">Type perçu du fichier.</span><span class="sxs-lookup"><span data-stu-id="84a79-122">The perceived type of the file.</span></span> <span data-ttu-id="84a79-123">Valeur par défaut est aucune.</span><span class="sxs-lookup"><span data-stu-id="84a79-123">Defaults to nothing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84a79-124">&lt;ProgID/ProgID&gt;</span><span class="sxs-lookup"><span data-stu-id="84a79-124">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-125">Identificateur programmatique pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="84a79-125">The programmatic identifier for the file type.</span></span> <span data-ttu-id="84a79-126">Utilise par défaut la valeur App Virt. extension. file.</span><span class="sxs-lookup"><span data-stu-id="84a79-126">Defaults to App Virt.extension.File.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84a79-127">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="84a79-127">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-128">Indique si les utilisateurs qui téléchargent un fichier de ce type doivent être invités à ouvrir ou enregistrer le fichier.</span><span class="sxs-lookup"><span data-stu-id="84a79-128">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span> <span data-ttu-id="84a79-129">Valeur par défaut: Oui.</span><span class="sxs-lookup"><span data-stu-id="84a79-129">Defaults to YES.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84a79-130">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="84a79-130">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-131">Indique si l’extension du fichier doit toujours être affichée, même si l’utilisateur a demandé que toutes les extensions soient masquées.</span><span class="sxs-lookup"><span data-stu-id="84a79-131">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span> <span data-ttu-id="84a79-132">Par défaut, la valeur est non.</span><span class="sxs-lookup"><span data-stu-id="84a79-132">Defaults to NO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84a79-133">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="84a79-133">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-134">Indique si une entrée doit être ajoutée au menu nouveau de l’environnement <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="84a79-134">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span> <span data-ttu-id="84a79-135">Par défaut, la valeur est non.</span><span class="sxs-lookup"><span data-stu-id="84a79-135">Defaults to NO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84a79-136">/LOG</span><span class="sxs-lookup"><span data-stu-id="84a79-136">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-137">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="84a79-137">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84a79-138">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="84a79-138">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-139">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="84a79-139">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84a79-140">/GUI</span><span class="sxs-lookup"><span data-stu-id="84a79-140">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-141">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="84a79-141">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="84a79-142">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="84a79-142">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84a79-143">/LOGU</span><span class="sxs-lookup"><span data-stu-id="84a79-143">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="84a79-144">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="84a79-144">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="84a79-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84a79-145">Related topics</span></span>


[<span data-ttu-id="84a79-146">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="84a79-146">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






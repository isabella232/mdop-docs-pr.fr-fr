---
title: CONFIGURE TYPE
description: CONFIGURE TYPE
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809054"
---
# <span data-ttu-id="04c16-103">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="04c16-103">CONFIGURE TYPE</span></span>


<span data-ttu-id="04c16-104">Permet à l’utilisateur de modifier les paramètres d’une association de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="04c16-104">Enables the user to change settings for a file type association.</span></span>

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04c16-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="04c16-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="04c16-106">Description</span><span class="sxs-lookup"><span data-stu-id="04c16-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04c16-107">TYPE: &lt; fichier-extension&gt;</span><span class="sxs-lookup"><span data-stu-id="04c16-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-108">Extension de nom de fichier à configurer.</span><span class="sxs-lookup"><span data-stu-id="04c16-108">The file name extension to be configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04c16-109">&lt;Application/App&gt;</span><span class="sxs-lookup"><span data-stu-id="04c16-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-110">Nom et version (facultatif) de l’application à laquelle associer ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="04c16-110">The name and version (optional) of the application to associate this file type with.</span></span> <span data-ttu-id="04c16-111">Ne peut pas être spécifié avec PROGID.</span><span class="sxs-lookup"><span data-stu-id="04c16-111">Cannot be specified with PROGID.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04c16-112">&lt;Icône/Icon-chemin&gt;</span><span class="sxs-lookup"><span data-stu-id="04c16-112">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-113">Path ou URL du fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="04c16-113">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04c16-114">&lt;Type de type/Description-DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="04c16-114">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-115">Nom convivial du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="04c16-115">The user-friendly name for the file type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04c16-116">&lt;Type de contenu/Content-type&gt;</span><span class="sxs-lookup"><span data-stu-id="04c16-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-117">Le type de contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="04c16-117">The content type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04c16-118">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="04c16-118">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-119">Le cas échéant, indique que l’Association qui s’applique à tous les utilisateurs doit être modifiée, et non à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04c16-119">If present, indicates that the association that applies to all users should be edited, not the user-specific one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04c16-120">/PERCEIVED-TYPE &lt; perçu-type&gt;</span><span class="sxs-lookup"><span data-stu-id="04c16-120">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-121">Type perçu du fichier.</span><span class="sxs-lookup"><span data-stu-id="04c16-121">The perceived type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04c16-122">&lt;ProgID/ProgID&gt;</span><span class="sxs-lookup"><span data-stu-id="04c16-122">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-123">Indique que l’extension doit être associée à un autre type de fichier.</span><span class="sxs-lookup"><span data-stu-id="04c16-123">Indicates that the extension should be associated with a different file type.</span></span> <span data-ttu-id="04c16-124">Le type de fichier précédent n’est pas supprimé.</span><span class="sxs-lookup"><span data-stu-id="04c16-124">The previous file type is not deleted.</span></span> <span data-ttu-id="04c16-125">Ne peut pas être spécifié avec l’application, l’icône, la DESCRIPTION, CONFIRMOPEN ou SHOWEXT.</span><span class="sxs-lookup"><span data-stu-id="04c16-125">Cannot be specified with APP, ICON, DESCRIPTION, CONFIRMOPEN, or SHOWEXT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04c16-126">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="04c16-126">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-127">Indique si les utilisateurs qui téléchargent un fichier de ce type doivent être invités à ouvrir ou enregistrer le fichier.</span><span class="sxs-lookup"><span data-stu-id="04c16-127">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04c16-128">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="04c16-128">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-129">Indique si l’extension du fichier doit toujours être affichée, même si l’utilisateur a demandé que toutes les extensions soient masquées.</span><span class="sxs-lookup"><span data-stu-id="04c16-129">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04c16-130">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="04c16-130">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-131">Indique si une entrée doit être ajoutée au menu nouveau de l’environnement <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="04c16-131">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04c16-132">/LOG</span><span class="sxs-lookup"><span data-stu-id="04c16-132">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-133">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="04c16-133">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04c16-134">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="04c16-134">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-135">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="04c16-135">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04c16-136">/GUI</span><span class="sxs-lookup"><span data-stu-id="04c16-136">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-137">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="04c16-137">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="04c16-138">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="04c16-138">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04c16-139">/LOGU</span><span class="sxs-lookup"><span data-stu-id="04c16-139">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="04c16-140">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="04c16-140">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="04c16-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04c16-141">Related topics</span></span>


[<span data-ttu-id="04c16-142">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="04c16-142">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






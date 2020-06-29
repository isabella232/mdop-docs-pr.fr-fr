---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807870"
---
# <span data-ttu-id="1928d-103">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="1928d-103">CONFIGURE PACKAGE</span></span>


<span data-ttu-id="1928d-104">Permet à l’utilisateur de modifier un fichier de manifeste de package, une source de package, des types de déclencheurs de chargement ou la cible de charge d’un package.</span><span class="sxs-lookup"><span data-stu-id="1928d-104">Enables the user to change a package manifest file, package source, load trigger types, or load target for a package.</span></span>

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1928d-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1928d-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="1928d-106">Description</span><span class="sxs-lookup"><span data-stu-id="1928d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1928d-107">PACKAGE: &lt; nom du package&gt;</span><span class="sxs-lookup"><span data-stu-id="1928d-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-108">Nom convivial et visible par l’utilisateur pour le package.</span><span class="sxs-lookup"><span data-stu-id="1928d-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1928d-109">&lt;Fichier/MANIFEST-chemin&gt;</span><span class="sxs-lookup"><span data-stu-id="1928d-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-110">Chemin d’accès du fichier manifeste qui recense les applications incluses dans le package et toutes les informations de publication.</span><span class="sxs-lookup"><span data-stu-id="1928d-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1928d-111">&lt;URL/OVERRIDEURL&gt;</span><span class="sxs-lookup"><span data-stu-id="1928d-111">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-112">Emplacement du fichier SFT du package.</span><span class="sxs-lookup"><span data-stu-id="1928d-112">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1928d-113">/AUTOLOADNEVER</span><span class="sxs-lookup"><span data-stu-id="1928d-113">/AUTOLOADNEVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-114">Le chargement en arrière-plan est désactivé pour le package.</span><span class="sxs-lookup"><span data-stu-id="1928d-114">Background loading is turned off for the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1928d-115">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="1928d-115">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-116">Le chargement en arrière-plan est effectué après une actualisation de publication.</span><span class="sxs-lookup"><span data-stu-id="1928d-116">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1928d-117">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="1928d-117">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-118">Le chargement en arrière-plan est effectué lorsqu’un utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="1928d-118">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1928d-119">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="1928d-119">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-120">Le chargement en arrière-plan est effectué après le démarrage d’une application à partir du package par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1928d-120">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1928d-121">/AUTOLOADTARGET &lt; cible&gt;</span><span class="sxs-lookup"><span data-stu-id="1928d-121">/AUTOLOADTARGET &lt;target&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-122">Indique quelles applications du package doivent être chargées de façon automatique.</span><span class="sxs-lookup"><span data-stu-id="1928d-122">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1928d-123">NÉANT</span><span class="sxs-lookup"><span data-stu-id="1928d-123">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-124">Aucun chargement automatique ne sera effectué malgré la présence d’indicateurs/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="1928d-124">No autoloading will be performed despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1928d-125">SES</span><span class="sxs-lookup"><span data-stu-id="1928d-125">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-126">S’il s’agit d’une opération de déclenchement du déclencheur de charge, toutes les applications du package sont chargées dans le cache, qu’elles aient été ou non démarrées.</span><span class="sxs-lookup"><span data-stu-id="1928d-126">If an autoload trigger is enabled, all applications in the package will be loaded into cache regardless of whether they have ever been launched.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1928d-127">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="1928d-127">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-128">Si un déclencheur de chargement automatique est activé, le package se charge si une application de ce package a déjà été démarrée par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1928d-128">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1928d-129">/LOG</span><span class="sxs-lookup"><span data-stu-id="1928d-129">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-130">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="1928d-130">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1928d-131">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="1928d-131">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-132">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="1928d-132">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1928d-133">/GUI</span><span class="sxs-lookup"><span data-stu-id="1928d-133">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-134">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="1928d-134">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1928d-135">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="1928d-135">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1928d-136">/LOGU</span><span class="sxs-lookup"><span data-stu-id="1928d-136">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-137">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="1928d-137">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1928d-138">Pour la version 4.6 SP2, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="1928d-138">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1928d-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</span><span class="sxs-lookup"><span data-stu-id="1928d-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-140">Si elle a la valeur TRUE, une valeur de Registre est créée pour le package, soit par utilisateur, soit globalement si l’indicateur/GLOBAL est spécifié.</span><span class="sxs-lookup"><span data-stu-id="1928d-140">If set to TRUE, a registry value is created for the package, either per user, or globally if the /GLOBAL flag is specified.</span></span></p>
<p><span data-ttu-id="1928d-141">Si elle est définie sur FALSe, la valeur du Registre est supprimée et les associations de types de fichier (FTA) du package sont réinstallées.</span><span class="sxs-lookup"><span data-stu-id="1928d-141">If set to FALSE, the registry value is removed and the file type associations (FTA) for the package are reinstalled.</span></span></p>
<p><span data-ttu-id="1928d-142">En l’absence de spécification, le comportement normal de FTA et de publication des raccourcis est déclenché.</span><span class="sxs-lookup"><span data-stu-id="1928d-142">If not specified, normal FTA and shortcut publishing behavior occurs.</span></span> <span data-ttu-id="1928d-143">Si vous effectuez des opérations d’actualisation de publication ultérieures sur le client App-V 4,6 SP2, les raccourcis et FTAs pour les packages qui ont ce jeu de valeurs de registre ne seront pas modifiés, et les raccourcis et FTAs ne seront pas inscrits au démarrage du système ou à la connexion de l’utilisateur, sauf si vous réinitialisez l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="1928d-143">If you perform any subsequent publishing refresh operations on the App-V 4.6 SP2 client, the shortcuts and FTAs for packages that have this registry value set will not be changed, and the shortcuts and FTAs will not be registered at system startup or user login unless you reset the flag.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1928d-144">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="1928d-144">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="1928d-145">Fonctionne conjointement avec l’indicateur/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="1928d-145">Works in conjunction with the /NO-UPDATE-FTA-SHORTCUT flag.</span></span> <span data-ttu-id="1928d-146">Si l’indicateur/GLOBAL est présent, il indique qu’une valeur de registre sera créée pour ce package pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1928d-146">If the /GLOBAL flag is present, it indicates that a registry value will be created for that package for all users.</span></span> <span data-ttu-id="1928d-147">Par défaut, la valeur Registry est uniquement créée pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1928d-147">By default, the registry value is created only for this user.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1928d-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1928d-148">Related topics</span></span>


[<span data-ttu-id="1928d-149">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="1928d-149">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






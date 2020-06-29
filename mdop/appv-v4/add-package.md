---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809330"
---
# <span data-ttu-id="6420e-103">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="6420e-103">ADD PACKAGE</span></span>


<span data-ttu-id="6420e-104">Ajoute un enregistrement de package.</span><span class="sxs-lookup"><span data-stu-id="6420e-104">Adds a package record.</span></span> <span data-ttu-id="6420e-105">Si le package existe déjà, cette commande met à jour la configuration du package existant.</span><span class="sxs-lookup"><span data-stu-id="6420e-105">If the package already exists, this command will update the configuration of the existing package.</span></span>

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6420e-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6420e-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="6420e-107">Description</span><span class="sxs-lookup"><span data-stu-id="6420e-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6420e-108">PACKAGE: &lt; nom du package&gt;</span><span class="sxs-lookup"><span data-stu-id="6420e-108">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-109">Nom convivial et visible par l’utilisateur pour le package.</span><span class="sxs-lookup"><span data-stu-id="6420e-109">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6420e-110">&lt;Fichier/MANIFEST-chemin&gt;</span><span class="sxs-lookup"><span data-stu-id="6420e-110">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-111">Chemin d’accès du fichier manifeste qui recense les applications incluses dans le package et toutes les informations de publication.</span><span class="sxs-lookup"><span data-stu-id="6420e-111">The path of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6420e-112">&lt;URL/OVERRIDEURL&gt;</span><span class="sxs-lookup"><span data-stu-id="6420e-112">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-113">Emplacement du fichier SFT du package.</span><span class="sxs-lookup"><span data-stu-id="6420e-113">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6420e-114">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="6420e-114">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-115">Le chargement en arrière-plan est effectué après une actualisation de publication.</span><span class="sxs-lookup"><span data-stu-id="6420e-115">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6420e-116">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="6420e-116">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-117">Le chargement en arrière-plan est effectué lorsqu’un utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="6420e-117">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6420e-118">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="6420e-118">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-119">Le chargement en arrière-plan est effectué après le démarrage d’une application à partir du package par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6420e-119">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6420e-120">/AUTOLOADTARGET cible</span><span class="sxs-lookup"><span data-stu-id="6420e-120">/AUTOLOADTARGET target</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-121">Indique quelles applications du package doivent être chargées de façon automatique.</span><span class="sxs-lookup"><span data-stu-id="6420e-121">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6420e-122">NÉANT</span><span class="sxs-lookup"><span data-stu-id="6420e-122">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-123">Aucun chargement automatique ne sera effectué, malgré la présence d’indicateurs/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="6420e-123">No autoloading will be performed, despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6420e-124">SES</span><span class="sxs-lookup"><span data-stu-id="6420e-124">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-125">Dans le cas contraire, toutes les applications du package sont chargées dans le cache, qu’elles aient été ou non déjà démarrées.</span><span class="sxs-lookup"><span data-stu-id="6420e-125">If an autoload trigger is enabled, all applications in the package will be loaded into cache whether or not they have been previously started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6420e-126">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="6420e-126">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-127">Si un déclencheur de chargement automatique est activé, le package se charge si une application de ce package a déjà été démarrée par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6420e-127">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6420e-128">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="6420e-128">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-129">Le cas échéant, le package est disponible pour tous les utilisateurs de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6420e-129">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6420e-130">/LOG</span><span class="sxs-lookup"><span data-stu-id="6420e-130">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-131">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="6420e-131">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6420e-132">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="6420e-132">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-133">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="6420e-133">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6420e-134">/GUI</span><span class="sxs-lookup"><span data-stu-id="6420e-134">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-135">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="6420e-135">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6420e-136">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="6420e-136">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6420e-137">/LOGU</span><span class="sxs-lookup"><span data-stu-id="6420e-137">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="6420e-138">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="6420e-138">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6420e-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6420e-139">Related topics</span></span>


[<span data-ttu-id="6420e-140">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="6420e-140">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






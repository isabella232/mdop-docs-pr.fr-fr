---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806457"
---
# <span data-ttu-id="dd7a6-103">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="dd7a6-103">PUBLISH PACKAGE</span></span>


<span data-ttu-id="dd7a6-104">Publie le contenu d’un package entier.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-104">Publishes the contents of an entire package.</span></span>

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dd7a6-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dd7a6-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="dd7a6-106">Description</span><span class="sxs-lookup"><span data-stu-id="dd7a6-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd7a6-107">PACKAGE: &lt; nom du package&gt;</span><span class="sxs-lookup"><span data-stu-id="dd7a6-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd7a6-108">Nom convivial et visible par l’utilisateur pour le package.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd7a6-109">&lt;Fichier/MANIFEST-chemin&gt;</span><span class="sxs-lookup"><span data-stu-id="dd7a6-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd7a6-110">Chemin d’accès du fichier manifeste qui recense les applications incluses dans le package et toutes les informations de publication.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd7a6-111">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="dd7a6-111">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd7a6-112">Le cas échéant, le package est disponible pour tous les utilisateurs de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-112">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd7a6-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="dd7a6-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd7a6-114">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd7a6-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="dd7a6-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd7a6-116">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="dd7a6-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dd7a6-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="dd7a6-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd7a6-118">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="dd7a6-119">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dd7a6-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="dd7a6-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="dd7a6-121">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="dd7a6-122">**Important**  Le package doit déjà avoir été ajouté au client de virtualisation d’application et le fichier manifeste est requis.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-122">**Important** The package must already have been added to the Application Virtualization Client, and the manifest file is required.</span></span>

<span data-ttu-id="dd7a6-123">Pour utiliser le paramètre **Global** , la commande publier le package doit être exécutée en tant qu’administrateur local. dans le cas contraire, seules les autorisations **ManageTypes** et **PublishShortcut** sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-123">To use the **GLOBAL** parameter, the PUBLISH PACKAGE command must be run as local Administrator; otherwise, only **ManageTypes** and **PublishShortcut** permissions are needed.</span></span>

<span data-ttu-id="dd7a6-124">La publication sans le paramètre **Global** octroie aux utilisateurs l’accès aux applications du package et publie les types de fichiers et les raccourcis répertoriés dans le manifeste dans le profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-124">Publishing without the **GLOBAL** parameter grants the user access to the applications in the package and publishes the file types and shortcuts listed in the manifest to the user’s profile.</span></span>

<span data-ttu-id="dd7a6-125">La publication avec le paramètre **Global** ajoute les types de fichiers et les raccourcis répertoriés dans le manifeste au profil «All Users».</span><span class="sxs-lookup"><span data-stu-id="dd7a6-125">Publishing with the **GLOBAL** parameter adds the file types and shortcuts listed in the manifest to the “All Users” profile.</span></span>

<span data-ttu-id="dd7a6-126">Si le package n’est pas global avant l’utilisation de l’appel et du paramètre **Global** , le package est alors rendu global et disponible pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="dd7a6-126">If the package is not global before the call and the **GLOBAL** parameter is used, the package is made global and available to all users.</span></span>

 

## <span data-ttu-id="dd7a6-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd7a6-127">Related topics</span></span>


[<span data-ttu-id="dd7a6-128">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="dd7a6-128">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






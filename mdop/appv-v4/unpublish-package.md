---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806185"
---
# <span data-ttu-id="13a50-103">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="13a50-103">UNPUBLISH PACKAGE</span></span>


<span data-ttu-id="13a50-104">Vous permet de supprimer les raccourcis et les types de fichiers pour l’ensemble d’un package.</span><span class="sxs-lookup"><span data-stu-id="13a50-104">Enables you to remove the shortcuts and file types for an entire package.</span></span>

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13a50-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="13a50-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="13a50-106">Description</span><span class="sxs-lookup"><span data-stu-id="13a50-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13a50-107">PACKAGE: &lt; nom du package&gt;</span><span class="sxs-lookup"><span data-stu-id="13a50-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="13a50-108">Nom du package.</span><span class="sxs-lookup"><span data-stu-id="13a50-108">The name of the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13a50-109">/CLEAR</span><span class="sxs-lookup"><span data-stu-id="13a50-109">/CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="13a50-110">Le cas échéant, les paramètres utilisateur sont également supprimés.</span><span class="sxs-lookup"><span data-stu-id="13a50-110">If present, user settings will also be removed.</span></span> <span data-ttu-id="13a50-111">(Pour plus d’informations, consultez la note important plus loin dans cette rubrique.)</span><span class="sxs-lookup"><span data-stu-id="13a50-111">(For more information, see the Important note later in this topic.)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13a50-112">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="13a50-112">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="13a50-113">Le cas échéant, le package sera annulé pour tous les utilisateurs de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="13a50-113">If present, the package will be unpublished for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13a50-114">/LOG</span><span class="sxs-lookup"><span data-stu-id="13a50-114">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="13a50-115">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="13a50-115">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13a50-116">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="13a50-116">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="13a50-117">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="13a50-117">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13a50-118">/GUI</span><span class="sxs-lookup"><span data-stu-id="13a50-118">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="13a50-119">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="13a50-119">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="13a50-120">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="13a50-120">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13a50-121">/LOGU</span><span class="sxs-lookup"><span data-stu-id="13a50-121">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="13a50-122">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="13a50-122">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="13a50-123">**Important**  Avant d’exécuter la commande **annuler la publication** d’un package, le package doit déjà avoir été ajouté au client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="13a50-123">**Important** Before you can run the **UNPUBLISH PACKAGE** command, the package must already have been added to the Application Virtualization Client.</span></span>

<span data-ttu-id="13a50-124">Pour utiliser **Global**, la publication d’un **package** doit être exécutée en tant qu’administrateur local. dans le cas contraire, seule une autorisation **ClearApp** est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="13a50-124">To use **GLOBAL**, **UNPUBLISH PACKAGE** must be run as local Administrator; otherwise, only **ClearApp** permission is needed.</span></span>

<span data-ttu-id="13a50-125">L’utilisation de la fonction de suppression de **package** avec l’option **Global** entraîne la suppression de tous les types de fichiers globaux et raccourcis du package.</span><span class="sxs-lookup"><span data-stu-id="13a50-125">Using **UNPUBLISH PACKAGE** with **GLOBAL** removes any global file types and shortcuts for the package.</span></span> <span data-ttu-id="13a50-126">**Clear** n’est pas applicable.</span><span class="sxs-lookup"><span data-stu-id="13a50-126">**CLEAR** is not applicable.</span></span>

<span data-ttu-id="13a50-127">L’utilisation de l’option annuler la publication d’un **package** sans **Global** entraîne celle de l’utilisateur et du type de fichier pour le package et, si la valeur est définie sur **Effacer** , supprime également les paramètres d’utilisateur et arrête les chargements en arrière-plan dans le contexte de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="13a50-127">Using **UNPUBLISH PACKAGE** without **GLOBAL** removes the user shortcuts and file types for the package and, if **CLEAR** is set, also removes user settings and stops background loads under the user’s context.</span></span>

<span data-ttu-id="13a50-128">L’annulation de la publication d’un **package** fonctionne sur les applications provenant du même nom de package ou du GUID utilisé en tant qu’ID source pour l' **Ajout**, la **modification**et la publication d’un **package**.</span><span class="sxs-lookup"><span data-stu-id="13a50-128">**UNPUBLISH PACKAGE** works on applications from the same package name or GUID that was used as the source ID for **ADD**, **EDIT**, and **PUBLISH PACKAGE**.</span></span>

<span data-ttu-id="13a50-129">L’annulation de la publication d’un **package** efface toujours l’ensemble des paramètres utilisateur, des raccourcis et des types de fichiers, quelle que soit l’utilisation du commutateur/Clear.</span><span class="sxs-lookup"><span data-stu-id="13a50-129">**UNPUBLISH PACKAGE** always clears all the user settings, shortcuts, and file types regardless of the use of the /CLEAR switch.</span></span>

 

## <span data-ttu-id="13a50-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13a50-130">Related topics</span></span>


[<span data-ttu-id="13a50-131">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="13a50-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806426"
---
# <span data-ttu-id="0cddb-103">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="0cddb-103">QUERY OBJ</span></span>


<span data-ttu-id="0cddb-104">Renvoie une liste délimitée par des tabulations des applications actuelles, packages, associations de types de fichiers ou serveurs de publication.</span><span class="sxs-lookup"><span data-stu-id="0cddb-104">Returns a tab-delimited list of current applications, packages, file type associations, or publishing servers.</span></span>

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0cddb-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0cddb-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="0cddb-106">Description</span><span class="sxs-lookup"><span data-stu-id="0cddb-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cddb-107">APPLI</span><span class="sxs-lookup"><span data-stu-id="0cddb-107">APP</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-108">Renvoie une liste d’applications.</span><span class="sxs-lookup"><span data-stu-id="0cddb-108">Returns a list of applications.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0cddb-109">GESTIONNAIRE</span><span class="sxs-lookup"><span data-stu-id="0cddb-109">PACKAGE</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-110">Renvoie une liste de packages.</span><span class="sxs-lookup"><span data-stu-id="0cddb-110">Returns a list of packages.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cddb-111">TYPE</span><span class="sxs-lookup"><span data-stu-id="0cddb-111">TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-112">Renvoie une liste des associations de types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0cddb-112">Returns a list of file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0cddb-113">SERVEURS</span><span class="sxs-lookup"><span data-stu-id="0cddb-113">SERVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-114">Renvoie une liste de serveurs de publication.</span><span class="sxs-lookup"><span data-stu-id="0cddb-114">Returns a list of publishing servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cddb-115">/SHORT</span><span class="sxs-lookup"><span data-stu-id="0cddb-115">/SHORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-116">Sans afficher les propriétés complètes de chacune d’elles, renvoie une liste de noms d’application, de packages, d’associations ou de noms de serveurs.</span><span class="sxs-lookup"><span data-stu-id="0cddb-116">Without displaying the full properties of each, returns a list of application names, packages, associations, or server names.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0cddb-117">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="0cddb-117">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-118">Pour les applications, retourne toutes les applications connues au lieu de celles auxquelles l’utilisateur actuel a accès.</span><span class="sxs-lookup"><span data-stu-id="0cddb-118">For applications, returns all known applications instead of only the ones the current user has access to.</span></span> <span data-ttu-id="0cddb-119">Pour les packages, renvoie tous les packages connus au lieu de ceux auxquels l’utilisateur actuel a accès.</span><span class="sxs-lookup"><span data-stu-id="0cddb-119">For packages, returns all known packages instead of only the ones the current user has access to.</span></span> <span data-ttu-id="0cddb-120">Pour les associations, renvoie uniquement les associations qui s’appliquent à tous les utilisateurs, et non spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0cddb-120">For associations, returns only associations that apply to all users, not user-specific ones.</span></span> <span data-ttu-id="0cddb-121">Non valide pour les serveurs.</span><span class="sxs-lookup"><span data-stu-id="0cddb-121">Not valid for servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cddb-122">/LOG</span><span class="sxs-lookup"><span data-stu-id="0cddb-122">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-123">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="0cddb-123">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0cddb-124">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="0cddb-124">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-125">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="0cddb-125">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0cddb-126">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="0cddb-126">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cddb-127">/LOGU</span><span class="sxs-lookup"><span data-stu-id="0cddb-127">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-128">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="0cddb-128">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0cddb-129">**Remarques**  Dans la version 4,6, une nouvelle colonne a été ajoutée à la sortie de la requête SFTMIME OBJ: APP \ [/GLOBAL\].</span><span class="sxs-lookup"><span data-stu-id="0cddb-129">**Note** In version 4.6, a new column has been added to the output of SFTMIME QUERY OBJ:APP \[/GLOBAL\].</span></span> <span data-ttu-id="0cddb-130">La dernière colonne de la sortie est une valeur numérique qui indique si une application est publiée ou non.</span><span class="sxs-lookup"><span data-stu-id="0cddb-130">The last column of the output is a numeric value that indicates whether an application is published or not.</span></span>

<span data-ttu-id="0cddb-131">PUBLIÉ = 1 signifie que l’application a été publiée par une actualisation du serveur de publication, en installant l’application à l’aide d’un fichier Windows Installer (. MSI), ou en exécutant une commande SFTMIME ajouter un PACKAGE, configurer le PACKAGE ou publier le PACKAGE à l’aide d’un manifeste du package.</span><span class="sxs-lookup"><span data-stu-id="0cddb-131">PUBLISHED=1 means the application was published by a Publishing Server refresh, by installing the application by using a Windows Installer file (.MSI), or by running an SFTMIME ADD PACKAGE, CONFIGURE PACKAGE or PUBLISH PACKAGE command by using a package manifest.</span></span>

<span data-ttu-id="0cddb-132">PUBLIÉ = 0 indique que l’application n’a pas été publiée ou qu’elle n’est plus publiée suite à l’exécution d’une opération Clear ou d’exécution d’une commande SFTMIME UNPUBLISH.</span><span class="sxs-lookup"><span data-stu-id="0cddb-132">PUBLISHED=0 means the application has not been published or it is no longer published as a result of performing a Clear operation or running an SFTMIME UNPUBLISH command.</span></span>

<span data-ttu-id="0cddb-133">Si vous utilisez le paramètre/GLOBAL, l’État publié sera 1 pour les applications publiées globalement et 0 pour les applications qui ont été publiées sous contextes utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0cddb-133">If you use the /GLOBAL parameter, the PUBLISHED state will be 1 for applications that were published globally and 0 for those applications that were published under user contexts.</span></span> <span data-ttu-id="0cddb-134">Sans le paramètre/GLOBAL, un État publié de 1 est retourné pour les applications publiées dans le contexte de l’utilisateur exécutant la commande, et l’État 0 est retourné pour les applications qui sont publiées globalement.</span><span class="sxs-lookup"><span data-stu-id="0cddb-134">Without the /GLOBAL parameter, a PUBLISHED state of 1 is returned for applications published in the context of the user running the command, and a state of 0 is returned for those applications that are published globally.</span></span>

 

<span data-ttu-id="0cddb-135">La commande OBJ de la requête SFTMIME peut être utilisée pour rechercher des informations sur tous les objets indiqués ci-dessus: applications, packages, associations de types de fichiers et serveurs.</span><span class="sxs-lookup"><span data-stu-id="0cddb-135">The SFTMIME QUERY OBJ command can be used to query for information on all of the objects shown above—applications, packages, file type associations, and servers.</span></span><span data-ttu-id="0cddb-136">Pour illustrer la façon dont vous pouvez utiliser la commande SFTMIME de requête OBJ dans vos tâches d’opérations normales, l’exemple suivant illustre le processus que vous devez suivre si vous vouliez définir la valeur de paramètre OVERRIDEURL d’un package spécifique pour spécifier un nouveau chemin d’accès au contenu du package.</span><span class="sxs-lookup"><span data-stu-id="0cddb-136">To show how you might use the SFTMIME QUERY OBJ command in your normal operations tasks, the following example demonstrates the process you would follow if you wanted to set the OVERRIDEURL parameter value for a specific package to specify a new path to the package content.</span></span> 

1.  <span data-ttu-id="0cddb-137">Pour rechercher le package que vous voulez configurer, exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="0cddb-137">To find the package that you want to configure, run the following command:</span></span>

    `SFTMIME QUERY OBJ:PACKAGE`

    <span data-ttu-id="0cddb-138">Cette commande renvoie chaque nom de package détecté en tant que GUID dans la première colonne de sortie, par exemple, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span><span class="sxs-lookup"><span data-stu-id="0cddb-138">This command returns each discovered package name as a GUID in the first column of output—for example, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span></span>

2.  <span data-ttu-id="0cddb-139">Pour définir la valeur de paramètre OVERRIDEURL, vous utilisez la commande SFTMIME [configurer le package](configure-package.md) .</span><span class="sxs-lookup"><span data-stu-id="0cddb-139">To set the OVERRIDEURL parameter value, you use the SFTMIME [CONFIGURE PACKAGE](configure-package.md) command.</span></span> <span data-ttu-id="0cddb-140">Par exemple, pour définir la valeur OVERRIDEURL de ce package sur une valeur de *\\\\server\\share\\mypackage.SFT*, utilisez la commande SFTMIME configure package et attribuez-lui le GUID de package sélectionné à partir de la sortie de la commande SFTMIME de requête obj à l’étape 1, suivi du paramètre OVERRIDEURL et de sa nouvelle valeur, comme suit:</span><span class="sxs-lookup"><span data-stu-id="0cddb-140">For example, to set the OVERRIDEURL value for this package to a value of *\\\\server\\share\\mypackage.sft*, use the SFTMIME CONFIGURE PACKAGE command and give it the selected package GUID from the output of the SFTMIME QUERY OBJ command in step 1, followed by the OVERRIDEURL parameter and its new value, as follows:</span></span>

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

<span data-ttu-id="0cddb-141">Pour la version 4.6 SP2, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="0cddb-141">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0cddb-142">/NO-UPDATE-FTA-SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="0cddb-142">/NO-UPDATE-FTA-SHORTCUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="0cddb-143">Indique l’état actuel de l’indicateur/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="0cddb-143">Indicates the current state of the /NO-UPDATE-FTA-SHORTCUT flag.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0cddb-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cddb-144">Related topics</span></span>


[<span data-ttu-id="0cddb-145">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="0cddb-145">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






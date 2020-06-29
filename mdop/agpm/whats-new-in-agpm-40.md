---
title: Nouveautés d'AGPM4.0
description: Nouveautés d'AGPM4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808173"
---
# <span data-ttu-id="20a15-103">Nouveautés d'AGPM4.0</span><span class="sxs-lookup"><span data-stu-id="20a15-103">What's New in AGPM 4.0</span></span>


<span data-ttu-id="20a15-104">Microsoft Advanced Group Policy Management (AGPM) 4.0 inclut de nouvelles fonctionnalités qui vous permettent de rechercher des objets de stratégie de groupe (GPO), de filtrer la liste des objets de stratégie de groupe qui s’affichent, d’exporter et d’importer un objet de stratégie de groupe dans une autre forêt et d’installer AGPM sur des ordinateurs exécutant le logiciel Server2008R2 et Windows.</span><span class="sxs-lookup"><span data-stu-id="20a15-104">Microsoft Advanced Group Policy Management (AGPM)4.0 includes new features that let you search for Group Policy Objects (GPOs), filter the list of GPOs displayed, export and import a GPO to a different forest, and install AGPM on computers running Windows7 and Windows Server2008R2.</span></span>

## <span data-ttu-id="20a15-105">Recherchez et filtrez des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="20a15-105">Search and filter GPOs</span></span>


<span data-ttu-id="20a15-106">Dans le 4,0 d’AGPM, vous pouvez effectuer une recherche dans la liste d’objets de stratégie de groupe pour des attributs spécifiques et filtrer la liste des objets de stratégie de groupe affichés.</span><span class="sxs-lookup"><span data-stu-id="20a15-106">In AGPM 4.0, you can search the list of GPOs for specific attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="20a15-107">Par exemple, vous pouvez rechercher des objets de stratégie de groupe avec un nom, un État ou un commentaire particulier.</span><span class="sxs-lookup"><span data-stu-id="20a15-107">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="20a15-108">Vous pouvez également rechercher les objets de stratégie de groupe qui ont été modifiés en dernier par un administrateur de stratégie de groupe particulier ou à une date particulière.</span><span class="sxs-lookup"><span data-stu-id="20a15-108">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

<span data-ttu-id="20a15-109">Vous pouvez créer une chaîne de recherche complexe à l’aide de l’attribut «format de l’objet de stratégie de groupe» 1: champ d’objet de l’objet de recherche *2: Rechercher le texte 2*</span><span class="sxs-lookup"><span data-stu-id="20a15-109">You can create a complex search string by using the format *GPO attribute 1: search text 1 GPO attribute 2: search text 2…*, where a GPO attribute is any column heading in the list of GPOs in AGPM.</span></span> <span data-ttu-id="20a15-110">Par exemple, pour rechercher tous les objets de stratégie de groupe avec des noms, y compris le texte «MyGPO» archivé et modifié pour la dernière fois par l’utilisateur Editor03, vous devez taper ce qui suit dans la zone de recherche: **nom: MyGPO État:\*\*\*\*Archivé\*\*\*\*modifié par: Editor03**.</span><span class="sxs-lookup"><span data-stu-id="20a15-110">For example, to search for all GPOs with names including the text "MyGPO" that are checked in and were last changed by the user Editor03, you would type the following in the Search box: **name: MyGPO state:\*\*\*\*checked in\*\*\*\*changed by: Editor03**.</span></span> <span data-ttu-id="20a15-111">La recherche renvoie des correspondances partielles afin que vous puissiez entrer une partie du nom de l’objet GPO ou du nom d’utilisateur et afficher la liste de tous les objets de stratégie de groupe qui incluent ce texte dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="20a15-111">The search returns partial matches so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="20a15-112">De plus, vous pouvez utiliser les mêmes conditions spéciales disponibles lorsque vous recherchez dans Windows pour rechercher des objets de stratégie de groupe modifiés à une date ou une plage de dates spécifique.</span><span class="sxs-lookup"><span data-stu-id="20a15-112">Additionally, you can use the same special terms available when you search in Windows to search for GPOs changed on a specific date or range of dates.</span></span> <span data-ttu-id="20a15-113">Par exemple, **Modifiez Date:\*\*\*\*lastmonth** ou **changer la date:\*\*\*\*thisweek**.</span><span class="sxs-lookup"><span data-stu-id="20a15-113">For example, **change date:\*\*\*\*lastmonth** or **change date:\*\*\*\*thisweek**.</span></span>

## <span data-ttu-id="20a15-114">Exporter et importer des objets de stratégie de groupe dans différentes forêts</span><span class="sxs-lookup"><span data-stu-id="20a15-114">Export and import GPOs to different forests</span></span>


<span data-ttu-id="20a15-115">À l’aide d’AGPM 4,0, vous pouvez copier un objet GPO contrôlé d’un domaine d’une forêt vers un domaine dans une deuxième forêt.</span><span class="sxs-lookup"><span data-stu-id="20a15-115">Using AGPM 4.0, you can copy a controlled GPO from a domain in one forest to a domain in a second forest.</span></span> <span data-ttu-id="20a15-116">Par exemple, vous pouvez exporter un objet de stratégie de groupe à partir d’un domaine d’une forêt vers un fichier CAB en utilisant AGPM, copier ce fichier CAB sur un lecteur USB, brancher le lecteur USB à un ordinateur d’un domaine dans une deuxième forêt et importer l’objet GPO dans AGPM dans un domaine de la deuxième forêt.</span><span class="sxs-lookup"><span data-stu-id="20a15-116">For example, you can export a GPO from a domain in one forest to a CAB file by using AGPM, copy that CAB file to a USB drive, plug the USB drive into a computer in a domain in a second forest, and import the GPO into AGPM in a domain in the second forest.</span></span> <span data-ttu-id="20a15-117">Vous pouvez importer l’objet de stratégie de groupe en tant que nouvel objet de stratégie de groupe contrôlé ou l’importer pour remplacer les paramètres d’un objet de stratégie de groupe existant qui a été extrait.</span><span class="sxs-lookup"><span data-stu-id="20a15-117">You can either import the GPO as a new controlled GPO, or import it to replace the settings of an existing GPO that is checked out.</span></span>

## <span data-ttu-id="20a15-118">Prise en charge de Windows Server 2008 R2 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="20a15-118">Support for Windows Server 2008 R2 and Windows 7</span></span>


<span data-ttu-id="20a15-119">Le 4,0 d’AGPM prend en charge Windows Server2008R2 et la version de Windows, tout en prenant en charge Windows Server 2008 et Vista® avec Service Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="20a15-119">AGPM 4.0 supports Windows Server2008R2 and Windows7, yet still supports Windows Server2008 and WindowsVista® with Service Pack1 (SP1).</span></span> <span data-ttu-id="20a15-120">Néanmoins, il existe des limitations dans un environnement mixte qui inclut les systèmes d’exploitation plus récents et les plus anciens, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="20a15-120">However, there are limitations in a mixed environment that includes both the newer and older operating systems, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="20a15-121">Système d’exploitation sur lequel un serveur AGPM 4,0 est exécuté</span><span class="sxs-lookup"><span data-stu-id="20a15-121">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="20a15-122">Système d’exploitation sur lequel le client AGPM 4,0 s’exécute</span><span class="sxs-lookup"><span data-stu-id="20a15-122">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="20a15-123">État de la prise en charge d’AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="20a15-123">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20a15-124">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="20a15-124">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="20a15-125">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="20a15-125">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="20a15-126">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="20a15-126">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20a15-127">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="20a15-127">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="20a15-128">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="20a15-128">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="20a15-129">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2008R2 ou la touche Windows</span><span class="sxs-lookup"><span data-stu-id="20a15-129">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="20a15-130">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="20a15-130">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="20a15-131">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="20a15-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="20a15-132">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="20a15-132">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="20a15-133">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="20a15-133">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="20a15-134">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="20a15-134">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="20a15-135">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une icône</span><span class="sxs-lookup"><span data-stu-id="20a15-135">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 






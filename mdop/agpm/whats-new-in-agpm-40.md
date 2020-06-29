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
# Nouveautés d'AGPM4.0


Microsoft Advanced Group Policy Management (AGPM) 4.0 inclut de nouvelles fonctionnalités qui vous permettent de rechercher des objets de stratégie de groupe (GPO), de filtrer la liste des objets de stratégie de groupe qui s’affichent, d’exporter et d’importer un objet de stratégie de groupe dans une autre forêt et d’installer AGPM sur des ordinateurs exécutant le logiciel Server2008R2 et Windows.

## Recherchez et filtrez des objets de stratégie de groupe


Dans le 4,0 d’AGPM, vous pouvez effectuer une recherche dans la liste d’objets de stratégie de groupe pour des attributs spécifiques et filtrer la liste des objets de stratégie de groupe affichés. Par exemple, vous pouvez rechercher des objets de stratégie de groupe avec un nom, un État ou un commentaire particulier. Vous pouvez également rechercher les objets de stratégie de groupe qui ont été modifiés en dernier par un administrateur de stratégie de groupe particulier ou à une date particulière.

Vous pouvez créer une chaîne de recherche complexe à l’aide de l’attribut «format de l’objet de stratégie de groupe» 1: champ d’objet de l’objet de recherche *2: Rechercher le texte 2* Par exemple, pour rechercher tous les objets de stratégie de groupe avec des noms, y compris le texte «MyGPO» archivé et modifié pour la dernière fois par l’utilisateur Editor03, vous devez taper ce qui suit dans la zone de recherche: **nom: MyGPO État:****Archivé****modifié par: Editor03**. La recherche renvoie des correspondances partielles afin que vous puissiez entrer une partie du nom de l’objet GPO ou du nom d’utilisateur et afficher la liste de tous les objets de stratégie de groupe qui incluent ce texte dans leur nom.

De plus, vous pouvez utiliser les mêmes conditions spéciales disponibles lorsque vous recherchez dans Windows pour rechercher des objets de stratégie de groupe modifiés à une date ou une plage de dates spécifique. Par exemple, **Modifiez Date:****lastmonth** ou **changer la date:****thisweek**.

## Exporter et importer des objets de stratégie de groupe dans différentes forêts


À l’aide d’AGPM 4,0, vous pouvez copier un objet GPO contrôlé d’un domaine d’une forêt vers un domaine dans une deuxième forêt. Par exemple, vous pouvez exporter un objet de stratégie de groupe à partir d’un domaine d’une forêt vers un fichier CAB en utilisant AGPM, copier ce fichier CAB sur un lecteur USB, brancher le lecteur USB à un ordinateur d’un domaine dans une deuxième forêt et importer l’objet GPO dans AGPM dans un domaine de la deuxième forêt. Vous pouvez importer l’objet de stratégie de groupe en tant que nouvel objet de stratégie de groupe contrôlé ou l’importer pour remplacer les paramètres d’un objet de stratégie de groupe existant qui a été extrait.

## Prise en charge de Windows Server 2008 R2 et Windows 7


Le 4,0 d’AGPM prend en charge Windows Server2008R2 et la version de Windows, tout en prenant en charge Windows Server 2008 et Vista® avec Service Pack1 (SP1). Néanmoins, il existe des limitations dans un environnement mixte qui inclut les systèmes d’exploitation plus récents et les plus anciens, comme indiqué dans le tableau suivant.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation sur lequel un serveur AGPM 4,0 est exécuté</th>
<th align="left">Système d’exploitation sur lequel le client AGPM 4,0 s’exécute</th>
<th align="left">État de la prise en charge d’AGPM 4,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2008R2 ou la touche Windows</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une icône</p></td>
</tr>
</tbody>
</table>

 

 

 






---
title: À propos de l’environnement virtuel du groupe de connexion
description: À propos de l’environnement virtuel du groupe de connexion
author: dansimp
ms.assetid: b7bb0e3d-8cd5-45a9-b84e-c9ab4196a18c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43f30c2100fc982170f15c305b03cd338b5d8afd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806061"
---
# À propos de l’environnement virtuel du groupe de connexion


**Contenu de cet article:**

-   [Déterminer la priorité du package](#bkmk-pkg-priority-deter)

-   [Fusion de chemins de package identiques dans un répertoire virtuel dans les groupes de connexions](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a>Déterminer la priorité du package


L’environnement virtuel et son état actuel sont associés au groupe de connexions, et non aux packages individuels. Si un package App-V est supprimé du groupe de connexion, l’État qui existait dans le cadre du groupe de connexion n’est pas migré avec le package.

Si le même package fait partie de deux groupes de connexion différents, vous devez indiquer le groupe de connexions qu’il doit utiliser. Par exemple, vous pouvez avoir deux packages dans un groupe de connexion, qui définissent chacun la même valeur DWORD Registry.

Le groupe de connexion utilisé est basé sur l’ordre dans lequel un package s’affiche à l’intérieur du document XML **AppConnectionGroup** :

-   Le premier package a la priorité la plus élevée.

-   Le deuxième package a la deuxième priorité la plus élevée.

Prenez en considération la section exemple suivant:

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

Supposez que la même valeur DWORD ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) est définie dans les premier et troisième packages, par exemple:

-   Package 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5

-   Package 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10

Dans la mesure où Package 1 apparaît en premier, l’environnement virtuel de AppConnectionGroup aura la valeur DWORD unique de 5 (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5). Cela signifie que les applications virtuelles dans le package 1, le package 2 et le package 3 verront tous la valeur 5 lors de la recherche de HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.

Les autres ressources de l’environnement virtuel sont résolues de façon similaire, mais le cas échéant, c’est que les collisions se produisent dans le registre.

## <a href="" id="bkmk-merged-root-ve-exp"></a>Fusion de chemins de package identiques dans un répertoire virtuel dans les groupes de connexions


Si au moins deux packages d’un groupe de connexion contiennent des chemins d’accès identiques, les chemins d’accès sont fusionnés dans un répertoire virtuel unique à l’intérieur de l’environnement virtuel du groupe de connexion. Cette fusion des chemins d’accès permet à une application dans un même package d’accéder aux fichiers d’un autre package.

Lorsque vous supprimez un package d’un groupe de connexions, les applications de ce package supprimé ne peuvent plus accéder aux fichiers figurant dans les packages restants du groupe de connexion.

L’ordre dans lequel l’application-V recherche le nom d’un fichier dans le groupe de connexion est spécifié par l’ordre dans lequel les packages App-V apparaissent dans le fichier manifeste de groupe de connexion.

L’exemple suivant montre l’ordre et la relation d’une recherche de nom de fichier dans un groupe de connexion pour le **package a et le** **package B**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Package A</th>
<th align="left">Package B</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>C:\Windows\System32</p></td>
<td align="left"><p>C:\Windows\System32</p></td>
</tr>
<tr class="even">
<td align="left"><p>C:\AppTest</p></td>
<td align="left"><p>C:\AppTest</p></td>
</tr>
</tbody>
</table>

 

Dans l’exemple ci-dessus, lorsqu’une application virtualisée tente de rechercher un fichier spécifique, le package A recherche d’abord un chemin de fichier correspondant. Si aucun chemin d’accès correspondant n’est trouvé, le package B est recherché en utilisant les règles de mappage suivantes:

-   Si un fichier nommé **test.txt** existe dans la même hiérarchie de dossiers virtuels dans les deux packages d’application, le premier fichier correspondant est utilisé.

-   Si un fichier nommé **bar.txt** existe dans la hiérarchie des dossiers virtuels d’un package d’application, mais pas dans l’autre, le premier fichier correspondant est utilisé.






## Rubriques connexes


[Gestion des groupes de connexion](managing-connection-groups51.md)

 

 






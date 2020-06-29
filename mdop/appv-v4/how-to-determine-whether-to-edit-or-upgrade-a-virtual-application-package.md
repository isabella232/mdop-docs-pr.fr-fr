---
title: Procédure pour déterminer si un package d'application virtuelle doit être modifié ou mis à jour
description: Procédure pour déterminer si un package d'application virtuelle doit être modifié ou mis à jour
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807133"
---
# Procédure pour déterminer si un package d'application virtuelle doit être modifié ou mis à jour


Utilisez le tableau suivant pour déterminer si un package d’application virtuel peut être ouvert pour modification, si vous avez besoin de créer une nouvelle version du package, ou si l’une des options est disponible à l’aide du Sequencer App-V.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Action</th>
<th align="left">Ouvrir pour modification</th>
<th align="left">Ouvrir pour la mise à niveau</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Afficher les propriétés du package.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Afficher l’historique des modifications de package.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Afficher les fichiers de package associés.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modifier les paramètres du Registre.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Passez en revue les paramètres de package supplémentaires (sauf les propriétés du fichier système d’exploitation).</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Créer un programme d’installation Windows (MSI) associé.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modifiez le fichier OSD.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Compresser et décompresser un package.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ajouter des associations de types de fichiers.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Renommer des raccourcis.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Définissez l’état de clé de Registre virtualisé (override/Merge).</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Définir l’état de dossier virtualisé.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modifier les mappages du système de fichiers virtuel.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Examinez toutes les propriétés de fichier du système d’exploitation associées pour un package.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ajoutez d’autres services.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ajoutez des fichiers supplémentaires.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Recueillez et configurez les descripteurs de sécurité associés.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Appliquer des mises à jour de sécurité ou effectuer une mise à niveau vers une nouvelle version.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ajoutez une autre application.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Appliquez les mises à jour qui nécessitent l’ouverture de l’application.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Appliquez les mises à jour qui nécessitent le redémarrage de l’ordinateur.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
</tr>
</tbody>
</table>

 

## Rubriques associées


[Procédure pour modifier une application virtuelle existante](how-to-edit-an-existing-virtual-application.md)

[Procédure pour mettre à niveau une application virtuelle existante](how-to-upgrade-an-existing-virtual-application.md)

 

 






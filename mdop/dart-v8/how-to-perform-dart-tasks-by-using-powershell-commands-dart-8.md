---
title: Procédure pour effectuer des tâches DaRT à l'aide des commandes PowerShell
description: Procédure pour effectuer des tâches DaRT à l'aide des commandes PowerShell
author: dansimp
ms.assetid: bc788b00-38c7-4f57-a832-916b68264d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f8ff87aa09555b93ca04a6ec7fa5dd4ba8504514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810475"
---
# Procédure pour effectuer des tâches DaRT à l'aide des commandes PowerShell


Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 fournit l’ensemble d’applets de commande Windows PowerShell suivant. Les administrateurs peuvent utiliser les applets de commande PowerShell suivants pour effectuer différentes tâches du serveur DaRT 8,0 à partir de l’invite de commandes plutôt que de l’Assistant image de récupération DaRT.

## Pour administrer DaRT à l’aide de commandes PowerShell


Utilisez les applets de commande PowerShell décrites ici pour gérer DaRT.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copy-DartImage</p></td>
<td align="left"><p>Brûlure d’une connexion ISO sur un CD, un DVD ou un lecteur USB.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Export-DartImage</p></td>
<td align="left"><p>Permet de convertir le fichier WIM source contenant une image DaRT en fichier ISO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nouveau-DartConfiguration</p></td>
<td align="left"><p>Crée un objet de configuration DaRT requis pour appliquer un ensemble d’outils DaRT à une image Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-DartImage</p></td>
<td align="left"><p>Applique un objet DartConfiguration à une image Windows montée. Cela inclut l’ajout de tous les fichiers, de la configuration et des dépendances du package.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Administration de DaRT8.0 à l'aide de PowerShell](administering-dart-80-using-powershell-dart-8.md)

 

 






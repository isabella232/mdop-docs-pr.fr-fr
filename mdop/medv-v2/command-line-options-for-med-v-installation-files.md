---
title: Options de ligne de commande pour les fichiers d'installation de MED-V
description: Options de ligne de commande pour les fichiers d'installation de MED-V
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811772"
---
# Options de ligne de commande pour les fichiers d'installation de MED-V


Lors de l’installation ou de la désinstallation de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, vous avez la possibilité d’exécuter les fichiers d’installation à l’invite de commandes. Cette section décrit les différentes options que vous pouvez spécifier lorsque vous installez ou désinstallez MED-V à l’invite de commandes.

### Arguments de ligne de commande

Vous pouvez utiliser les arguments de ligne de commande suivants avec leurs fichiers d’installation MED-V correspondants.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fichier d’installation</th>
<th align="left">Argument</th>
<th align="left">Valeurs acceptées</th>
<th align="left">Type</th>
<th align="left">Description</th>
<th align="left">Par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Agent hôte</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;chemin d’installation&gt;</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Changer le répertoire installé</p></td>
<td align="left"><p>L’installation accède à Program Files\Microsoft Enterprise Desktop Virtualization.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Module de création de package de l’espace de travail MED-V</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;chemin d’installation&gt;</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Changer le répertoire installé</p></td>
<td align="left"><p>L’installation accède à Program Files\Microsoft Enterprise Desktop Virtualization.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espace de travail MED-V</p></td>
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;chemin d’installation&gt;</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Changer le répertoire installé</p></td>
<td align="left"><p>Installation de ProgramData\Microsoft\Medv\Workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espace de travail MED-V</p></td>
<td align="left"><p>REMPLACEMENT DU VHD</p></td>
<td align="left"><p>0 ou 1</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Échec de l’installation si le disque dur virtuel existe (0) ou écrasez le disque dur virtuel existant (1).</p></td>
<td align="left"><p>Le remplacement ne se produit pas et l’installation échoue s’il existe déjà un disque dur virtuel (VHD).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espace de travail MED-V</p></td>
<td align="left"><p>SUPPRESSMEDVLAUNCH</p></td>
<td align="left"><p>0 ou 1</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Démarrez (0) ou ne démarrez pas (1) MED-V après l’installation d’un espace de travail MED-V.</p></td>
<td align="left"><p>Si l’espace de travail MED-V a été installé à l’aide de l’interface utilisateur (UI), une case à cocher sur la <strong> </strong> page terminer détermine s’il convient de démarrer la technologie med-v.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espace de travail MED-V</p></td>
<td align="left"><p>DELETEDIFFDISKS</p></td>
<td align="left"><p>0 ou 1</p></td>
<td align="left"><p>Désinstallation</p></td>
<td align="left"><p>Conserver (0) ou supprimer (1) des VHD créés par MED-V</p></td>
<td align="left"><p>Aucun VHD n’est supprimé.</p></td>
</tr>
</tbody>
</table>

 

### Exemples d’arguments de ligne de commande

L’exemple suivant installe l’espace de travail MED-V créé par le gestionnaire de package de l’espace de travail MED-V. Le fichier d’installation crée un fichier journal dans le répertoire temporaire et exécute le fichier d’installation en mode quiet, mais ne démarre pas l’agent hôte MED-V à l’achèvement. Le fichier d’installation remplace tout VHD laissé par une installation précédente portant le même nom.

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

Dans l’exemple suivant, l’espace de travail MED-V est désinstallé. Le fichier d’installation crée un fichier journal dans le répertoire temporaire et exécute le fichier d’installation en mode quiet. Le fichier d’installation supprime les fichiers de disque dur virtuel restants du système de fichiers.

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## Rubriques connexes


[Déployer les composants MED-V](deploy-the-med-v-components.md)

[Informations techniques de référence pour MED-V](technical-reference-for-med-v.md)

 

 






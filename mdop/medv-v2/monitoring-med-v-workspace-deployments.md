---
title: Surveillance des déploiements d'espace de travail MED-V
description: Surveillance des déploiements d'espace de travail MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812221"
---
# Surveillance des déploiements d'espace de travail MED-V


La fonctionnalité de contrôle de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 vous permet d’exécuter des requêtes sur des espaces de travail MED-V pour déterminer si la première configuration a été effectuée dans l’ensemble de votre entreprise après le déploiement des espaces de travail MED-V. Il est important de surveiller la réussite de l’installation pour la première fois, car MED-V n’est pas disponible tant qu’il n’a pas été correctement configuré pour la première fois.

Cette section fournit des informations et des instructions pour vous aider à surveiller la réussite ou l’échec de la première configuration.

## Pour surveiller les déploiements d’espaces de travail MED-V


La fonctionnalité de surveillance est composée d’un fournisseur WMI (Windows Management Instrumentation) intégré qui vous permet de lancer une requête à l’aide du langage de requête WMI pour découvrir l’état de la première configuration de tous les utilisateurs finaux sur un espace de travail MED-V.

Le fournisseur WMI est implémenté à l’aide de l’infrastructure d’extension du fournisseur WMI à partir de Microsoft .NET Framework 3,5. Le fournisseur WMI s’exécute dans le contexte de LocalService et enregistre l’état de la première installation de façon sécurisée sous \\ProgramData.

Le fournisseur WMI est implémenté dans l’espace de noms **root\\microsoft\\medv** et implémente la classe **FTS \ _Status**, qui expose la méthode **SetFtsState**. MED-V utilise **SetFtsState** pour définir le premier État de l’installation.

La classe contient les propriétés suivantes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Ordinateur</strong></p></td>
<td align="left"><p><strong>Propriété en lecture seule </strong> qui contient le nom de l’ordinateur virtuel invité approvisionnée par le programme de configuration pour la première fois. Cette clé contient le nom que l’invité aurait eu lors du premier échec de la configuration.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>StatusCode</strong></p></td>
<td align="left"><p><strong>Propriété en lecture seule </strong> qui contient zéro si la première configuration a réussi. Toute autre valeur renvoyée est égale à l’ID d’événement de l’erreur qui est journalisée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Heure</strong></p></td>
<td align="left"><p>Heure UTC de fin de la première configuration.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Utilisateur</strong></p></td>
<td align="left"><p>Utilisateur pour la première fois.</p></td>
</tr>
</tbody>
</table>

 

Le code suivant montre le fichier MOF (Managed Object Format) qui définit la classe **FTS \ _Status** .

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

Dans la mesure où il est très probable que les espaces de travail MED-V pour lesquels le programme d’installation n’a pas été exécuté pour la première fois, vous pouvez écrire votre requête de telle sorte qu’elle ne se termine pas correctement, par exemple:

``` syntax
Select * from FTS_Status where StatusCode != 0
```

Dans ce cas, la fonctionnalité de surveillance renvoie une liste des espaces de travail MED-V qui n’ont pas été configurés pour la première fois, que vous pouvez utiliser pour effectuer les actions appropriées à la résolution de l’échec.

## Rubriques connexes


[Surveiller des espaces de travail MED-V](monitor-med-v-workspaces.md)

[Comment vérifier les paramètres de première installation](how-to-verify-first-time-setup-settings.md)

 

 






---
title: Choisir une méthode de publication
description: Choisir une méthode de publication
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808898"
---
# Choisir une méthode de publication


Après avoir séquencé une application à l’aide du séquence de virtualisation d’application, vous devez la *publier* pour vos utilisateurs. La publication de l’application consiste à fournir les icônes, les informations de définition de package et l’emplacement de la source de contenu sur les ordinateurs sur lesquels le client de virtualisation d’application a été installé. Le tableau suivant décrit les méthodes de publication prises en charge lorsque vous déployez la virtualisation d’application à l’aide d’un système de distribution de logiciels électroniques.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Avantages</th>
<th align="left">Inconvénients</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Générer un fichier du programme d’installation Windows durant le séquençage, sous la forme d’une solution autonome.</p></td>
<td align="left"><ul>
<li><p>Facile à utiliser.</p></li>
<li><p>Package chargé dans le cache localement sur chaque ordinateur.</p></li>
<li><p>Icônes affichées pour l’utilisateur.</p></li>
<li><p>Similaire au déploiement de logiciels traditionnels.</p></li>
<li><p>Il n’est pas nécessaire de utiliser des serveurs de streaming.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Il n’y a aucune souplesse quant à l’emplacement du contenu des packages sur les ordinateurs, même emplacement sur tous les ordinateurs.</p></li>
<li><p>Ne doit utiliser que l’ajout/suppression de programmes ou msiexec pour supprimer des applications.</p></li>
<li><p>Enlèvement et remplacement avec la nouvelle version requise pour la mise à jour du package.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Générez un fichier du programme d’installation Windows pendant le séquençage, utilisé avec des propriétés de ligne de commande du MODE, de chargement et de OVERRIDEURL et le manifeste du package.</p></td>
<td align="left"><ul>
<li><p>Facile à utiliser mais avec une souplesse accrue.</p></li>
<li><p>Icônes affichées pour l’utilisateur.</p></li>
<li><p>Le fichier SFT contenant les applications peut être placé sur un emplacement de la source en continu, dont les clients sont configurés pour utiliser cet emplacement.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Flexibilité limitée: seul l’emplacement du contenu du package peut être contrôlé au moment de l’exécution.</p></li>
<li><p>Ne devez utiliser que l’application Ajout/suppression de programmes ou msiexec pour supprimer l’application.</p></li>
<li><p>Enlèvement et remplacement avec la nouvelle version requise pour la mise à jour du package, sauf si vous utilisez un serveur de diffusion.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Exécutez des commandes SFTMIME.</p></td>
<td align="left"><ul>
<li><p>Flexibilité totale: contrôle total de toutes les fonctions de gestion des packages.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Les commandes doivent être utilisées pour une utilisation avec le système ESD.</p></li>
<li><p>Les commandes doivent être exécutées sur chaque ordinateur avec une séquence correcte.</p></li>
<li><p>Compréhension détaillée du langage de commande et de la planification soigneuse requise.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Pour plus d’informations sur l’utilisation de ces méthodes de publication, voir [Comment publier une application virtuelle sur le client](how-to-publish-a-virtual-application-on-the-client.md).

## Rubriques connexes


[Choisir une méthode de diffusion en continu](determine-your-streaming-method.md)

[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Présentation du scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario-overview.md)

[Procédure pour publier une application virtuelle sur le client](how-to-publish-a-virtual-application-on-the-client.md)

[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 






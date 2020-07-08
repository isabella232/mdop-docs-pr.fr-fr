---
title: Comment appliquer des paramètres réseau à un espace de travail MED-V
description: Comment appliquer des paramètres réseau à un espace de travail MED-V
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811802"
---
# Comment appliquer des paramètres réseau à un espace de travail MED-V


Les administrateurs peuvent définir les paramètres réseau de chaque espace de travail MED-V.

Tous les paramètres réseau sont configurés dans le module de **stratégie** sous l’onglet **réseau** .

**Pour appliquer les paramètres réseau à un espace de travail MED-V**

1.  Cliquez sur l’espace de travail MED-V à configurer.

2.  Dans le volet **réseau** , configurez les paramètres comme décrit dans le tableau suivant.

3.  Dans le menu **stratégie** , cliquez sur **valider**.

**Propriétés du réseau d’espace de travail MED-V**

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
<td align="left"><p>Propriétés TCP/IP</p></td>
<td align="left"><ul>
<li><p><strong>Utiliser l’adresse IP de l’hôte (NAT) </strong> : l’espace de travail utilisera la traduction d’adresses réseau pour partager l’adresse IP de l’hôte pour le trafic sortant.</p></li>
<li><p><strong>Utiliser une adresse IP différente de celle de l’hôte (pont) </strong> : l’espace de travail MED-V dispose de sa propre adresse réseau, généralement obtenue par le biais du protocole DHCP.</p></li>
</ul>
<p>Activez la case <strong> à cocher mapper plusieurs cartes dans l’espace de travail </strong> lorsque l’ordinateur hôte est doté de plusieurs cartes. Nous vous recommandons de l’utiliser lorsque l’hôte passe d’un réseau à un autre à l’aide de différentes cartes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur DNS</p></td>
<td align="left"><ul>
<li><p><strong>Ne pas modifier </strong> : les paramètres DNS définis dans l’ordinateur virtuel de l’espace de travail MED-V ne seront pas modifiés.</p></li>
<li><p><strong>Utiliser l’adresse DNS de l’hôte </strong> : les paramètres DNS de l’espace de travail MED-V seront synchronisés pour correspondre aux paramètres de l’hôte. La synchronisation DNS est dynamique. Il est synchronisé périodiquement avec l’hôte de sorte que, s’il est modifié sur l’hôte, il change dynamiquement dans l’espace de travail MED-V.</p></li>
<li><p><strong>Utiliser des adresses DNS spécifiques </strong> : l’espace de travail MED-V utilisera un DNS spécifique, tel qu’il est spécifié.</p>
<p>Dans les <strong> </strong> champs principal et <strong> secondaire </strong> , entrez les adresses DNS principales et secondaires.</p>
<p>Cochez la <strong> case Ajouter les adresses DNS de l’hôte </strong> pour ajouter l’hôte aux adresses DNS configurées.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Affecter des suffixes DNS</p></td>
<td align="left"><ul>
<li><p><strong>Attribuez les suffixes suivants </strong> : activez cette case à cocher pour attribuer des suffixes DNS spécifiques; dans la zone, entrez un ou plusieurs suffixes séparés par des virgules.</p></li>
<li><p><strong>Ajouter des suffixes </strong> d’hôte: activez cette case à cocher pour ajouter les suffixes d’hôte à l’adresse DNS.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Création d'un espace de travail MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

 

 






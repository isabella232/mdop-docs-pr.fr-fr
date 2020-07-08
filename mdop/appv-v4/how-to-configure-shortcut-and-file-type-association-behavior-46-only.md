---
title: Procédure pour configurer le comportement d'association de type de fichier et de raccourci
description: Procédure pour configurer le comportement d'association de type de fichier et de raccourci
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807297"
---
# Procédure pour configurer le comportement d'association de type de fichier et de raccourci


La stratégie de publication de type raccourci et Association de types de fichier (FTA) est définie et contrôlée par le fichier XML de publication, qui est envoyé aux clients par un serveur de publication lors d’une opération d’actualisation de publication. Lorsque le client reçoit ces informations, il ajoute les données nouvellement publiées relatives aux applications telles que les icônes et FTAs. Ensuite, elle supprime toutes les données de publication obsolètes.

Dans l’App-V version 4,6, deux valeurs de clé de Registre ont été définies pour permettre aux administrateurs de contrôler ce comportement. Par défaut, les raccourcis créés localement à l’aide de la console client sont désormais conservés.

## Comment modifier le raccourci et le comportement de FTA


Deux nouvelles valeurs de Registre DWORD ont été définies pour la clé de registre de configuration du client, «FileTypePolicy» et «ShortcutPolicy». Ces valeurs de Registre DWORD ne sont pas présentes par défaut, mais peuvent être ajoutées manuellement. La clé de registre de configuration se trouve dans HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.

Il existe quatre valeurs de stratégie définies dans le tableau ci-dessous, qui s’appliquent aux deux valeurs de clé de registre. La liste suivante indique les valeurs numériques des paramètres du Registre et le comportement appliqué aux types de fichiers ou aux raccourcis d’une opération d’actualisation de la publication.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Nom</p></td>
<td align="left"><p>Type</p></td>
<td align="left"><p>Données (exemples)</p></td>
<td align="left"><p>Description</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileTypePolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0X2 (App-V 4,6)</p></td>
<td align="left"><p>(0x0)-«ClientOnly»-supprimer tous les éléments existants de la même source d’informations de publication et conserver uniquement les éléments ajoutés localement</p>
<p>(0x1) – "ServerOnly": supprimez tous les éléments obsolètes de la même source d’informations de publication et des éléments ajoutés localement, et ajoutez les nouveaux éléments.</p>
<p>(0X2)-«ClientAndServer»-supprimer tous les éléments obsolètes de la même source d’informations de publication, conserver les éléments ajoutés localement et ajouter les nouveaux éléments (par défaut en cas de non-présentation pour App-V 4,6)</p>
<p>(0x3) – "tout changer"-apporter des modifications aux types de fichiers ou aux raccourcis</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ShortcutPolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0X2</p></td>
<td align="left"><p>(0x0)-«ClientOnly»-supprimer tous les éléments existants de la même source d’informations de publication et conserver uniquement les éléments ajoutés localement</p>
<p>(0x1) – "ServerOnly"-supprimer tous les éléments obsolètes de la même source d’informations de publication et des éléments ajoutés localement, et ajouter les nouveaux éléments</p>
<p>(0X2)-«ClientAndServer»-supprimer tous les éléments obsolètes de la même source d’informations de publication, conserver les éléments ajoutés localement et ajouter les nouveaux éléments (par défaut en cas de non-présentation)</p>
<p>(0x3) – "tout changer"-apporter des modifications aux types de fichiers ou aux raccourcis</p></td>
</tr>
</tbody>
</table>

 

**Remarques**  Les valeurs de texte font référence aux valeurs des attributs XML dans le fichier XML de publication.Vous pouvez définir ces valeurs manuellement si vous avez implémenté une solution de publication HTTP personnalisée.

 

 

 






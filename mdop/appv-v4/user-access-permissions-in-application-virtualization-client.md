---
title: Autorisations d'accès utilisateur dans Application Virtualization Client
description: Autorisations d'accès utilisateur dans Application Virtualization Client
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806178"
---
# Autorisations d'accès utilisateur dans Application Virtualization Client


Dans l’onglet **autorisations** de la boîte de dialogue **Propriétés** , accessible en cliquant avec le bouton droit sur le nœud **virtualisation** de l’application dans la console de gestion du client de virtualisation des applications, les administrateurs peuvent accorder des autorisations aux utilisateurs pour utiliser les diverses fonctions client.

**Remarques**  Avant de modifier les autorisations des utilisateurs, assurez-vous que les modifications apportées aux autorisations sont conformes aux instructions de l’Organisation concernant l’octroi d’autorisations utilisateur.

 

Le tableau suivant répertorie et décrit les autorisations qui peuvent être accordées aux utilisateurs.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de l’autorisation</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ajouter des applications</p></td>
<td align="left"><p>Enregistrez de nouvelles applications en passant un nouveau fichier OSD au client à l’aide du sfttray.exe, sftmime.exe ou la console MMC.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Changer la taille de cache du système de fichiers</p></td>
<td align="left"><p>Augmenter la taille du cache du système de fichiers.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Changer de lecteur système de fichiers</p></td>
<td align="left"><p>Sélectionnez une autre lettre de lecteur préférée pour le système de fichiers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modifier les paramètres du journal</p></td>
<td align="left"><p>Modifiez le niveau du journal ou le chemin d’accès du journal du fichier journal du client.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Changer de fichier OSD</p></td>
<td align="left"><p>Modifiez les fichiers OSD pour les applications enregistrées et transmettez-les au client. Cela n’affecte pas l’actualisation de la publication.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Effacer les paramètres de l’application</p></td>
<td align="left"><p>Supprimez des types de fichiers, des raccourcis et des configurations pour l’utilisateur actuel.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Supprimer des applications</p></td>
<td align="left"><p>Supprimez toutes les références à une application du système de fichiers et du cache OSD pour tous les utilisateurs de l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Importer des applications dans le cache</p></td>
<td align="left"><p>Chargez les données d’application directement à partir d’un fichier SFT spécifié dans le cache du système de fichiers. Ce problème affecte tous les utilisateurs.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Charger des applications dans le cache</p></td>
<td align="left"><p>Démarrez un chargement du fichier SFT pour une application à partir de la source configurée, par exemple un serveur de streaming App-V. Cette opération charge l’application pour tous les utilisateurs de l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verrouillage et déverrouillage d’applications dans le cache</p></td>
<td align="left"><p>Interdisez ou autorisez les applications d’être déchargées à partir du cache du système de fichiers. Ce problème affecte tous les utilisateurs de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestion des associations de types de fichiers</p></td>
<td align="left"><p>Ajoutez, modifiez ou supprimez des associations de types de fichiers pour l’utilisateur actuel uniquement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gérer les paramètres d’actualisation de publication</p></td>
<td align="left"><p>Modifiez les paramètres qui contrôlent le minutage des mises à jour de publication de tous les utilisateurs de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gérer les serveurs de publication</p></td>
<td align="left"><p>Ajoutez, modifiez ou supprimez des serveurs de publication pour tous les utilisateurs de l’ordinateur. Cette autorisation inclut implicitement l’autorisation de gérer les paramètres d’actualisation de la publication.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Raccourcis clavier</p></td>
<td align="left"><p>Créer de nouveaux raccourcis vers des applications enregistrées. L’utilisateur doit également disposer de l’autorisation de créer des fichiers dans le système de fichiers local.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Réparer des applications</p></td>
<td align="left"><p>Supprimer des configurations spécifiques aux applications pour l’utilisateur actuel, sans supprimer les raccourcis ou les types de fichiers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Démarrer une actualisation de publication</p></td>
<td align="left"><p>Démarrer une actualisation de publication non planifiée pour l’utilisateur actuel.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Basculer en mode hors connexion</p></td>
<td align="left"><p>Changer le client entier en mode hors connexion pour tous les utilisateurs.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Décharger les applications du cache</p></td>
<td align="left"><p>Effacez les données d’application du cache du système de fichiers pour tous les utilisateurs sans supprimer les paramètres spécifiques à l’utilisateur, les raccourcis ou les associations de types de fichiers.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Afficher toutes les applications</p></td>
<td align="left"><p>Permettre à l’utilisateur de voir les applications virtuelles pour tous les utilisateurs enregistrés sur l’ordinateur.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Procédure pour modifier les autorisations d'accès utilisateur](how-to-change-user-access-permissions.md)

 

 






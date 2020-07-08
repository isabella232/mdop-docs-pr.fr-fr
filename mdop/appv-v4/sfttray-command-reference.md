---
title: Référence à la commande SFTTRAY
description: Référence à la commande SFTTRAY
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806273"
---
# Référence à la commande SFTTRAY


L’application de barre d’état système du client Microsoft Application Virtualization (App-V), sfttray.exe, est l’élément d’interface utilisateur principal du client App-V sur lequel les utilisateurs interagiront pendant une utilisation normale. Ce programme contrôle la diffusion et le démarrage de toutes les applications virtuelles et est accessible en cliquant avec le bouton droit sur l’icône affichée dans la zone de notification pour afficher le menu des fonctions client. Ce menu permet à l’utilisateur de charger des applications, de lancer une actualisation de publication, d’annuler une demande ou de basculer le client en mode hors connexion. L’utilisateur peut également fermer l’application de barre des tâches du client de virtualisation des applications et toutes les applications actives en cliquant sur **quitter**.

Par défaut, l’icône s’affiche chaque fois qu’une application virtuelle est démarrée, même si vous pouvez contrôler ce comportement à l’aide de commandes SFTTRAY. L’application de la barre d’état système du client de virtualisation des applications affiche également une barre de progression pour chaque application démarrée ainsi que des messages d’État sur les applications actives. Lorsque vous cliquez sur la barre de progression, un message s’affiche pour vous permettre d’annuler le chargement ou le démarrage d’une application.

## Commandes SFTTRAY


Vous pouvez afficher la liste des commandes et des commutateurs de ligne de commande en exécutant la commande suivante à partir d’une fenêtre de commande.

**Remarque**  
Il n’y a qu’une seule instance de barre d’État du client de virtualisation d’application pour chaque contexte d’utilisateur, de sorte que si vous démarrez une nouvelle commande SFTTRAY, celle-ci sera transmise au programme déjà en cours d’exécution.



`Sfttray.exe /?`

### Utilisation des commandes

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### Commutateurs de ligne de commande

Le tableau suivant décrit les commutateurs de la ligne de commande SFTTRAY.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Commutateur</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/HIDE</p></td>
<td align="left"><p>Masque l’icône SFTTRAY dans la zone de notification Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOW</p></td>
<td align="left"><p>Affiche l’icône SFTTRAY dans la zone de notification Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/QUIET</p></td>
<td align="left"><p>Prend en charge l’utilisation sans assistance en empêchant les erreurs d’affichage des boîtes de message qui nécessitent un accusé de réception de l’utilisateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/EXE &lt; -exe alternatif&gt;</p></td>
<td align="left"><p>Utilisé avec/LAUNCH pour spécifier qu’un programme exécutable doit être démarré dans l’environnement virtuel lorsqu’une application virtuelle est démarrée à la place du fichier cible spécifié dans l’OSD.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Par exemple, utilisez «SFTTRAY.EXE/EXE REGEDIT.EXE &lt; application/Launch &gt; » pour examiner le registre de l’environnement virtuel dans lequel l’application s’exécute.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Application/Launch &gt; [ &lt; args &gt; ]</p></td>
<td align="left"><p>Démarre une application virtuelle. Spécifiez le nom et la version d’une application ou son chemin d’accès à un fichier OSD. Les arguments de ligne de commande peuvent éventuellement être transmis à l’application virtuelle.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Utilisez la commande «SFTMIME.EXE/QUERY OBJ: APP/SHORT» pour obtenir une liste des noms et versions des applications virtuelles disponibles.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>/LOAD</p></td>
<td align="left"><p>Charge ou importe une application virtuelle.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOADALL</p></td>
<td align="left"><p>Charge toutes les applications dans le cache.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/REFRESHALL</p></td>
<td align="left"><p>Lance une actualisation de publication pour toutes les applications.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;ID unique de/LAUNCHRESULT&gt;</p></td>
<td align="left"><p>Retourne le code de résultat de lancement du processus qui lance sfttray.exe à l’aide d’un événement global et d’un fichier mappé en mémoire qui est basé sur le nom de racine spécifié pour l’ID UNIQUE. ¹</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SFTFILE &lt; SFT&gt;</p></td>
<td align="left"><p>Commutateur facultatif utilisé avec/LOAD pour spécifier le chemin d’accès au fichier SFT de l’application. Si ce paramètre est spécifié, l’application est importée au lieu d’être chargée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/EXIT</p></td>
<td align="left"><p>Ferme le programme SFTTRAY et toutes les applications virtuelles actives, et supprime l’icône dans la zone de notification Windows.</p></td>
</tr>
</tbody>
</table>



**Remarque**  
¹ le paramètre de ligne de commande */LAUNCHRESULT* fournit un moyen pour le processus qui lance sfttray.exe pour spécifier le nom racine d’un événement global et un fichier mappé en mémoire qui sont utilisés pour renvoyer le code de résultat de lancement au processus. Le nom de l’identificateur unique doit commencer par «SFT» pour empêcher la virtualisation du nom de l’événement lorsque le processus de lancement est appelé dans un environnement virtuel. La taille de la région mappée en mémoire sera de 64 bits.

Pour utiliser ce paramètre, le processus de lancement crée un événement avec le nom « &lt; ID unique &gt; -result \ _Event», un fichier mappé en mémoire portant le nom «ID unique- &lt; result \ &gt; _Value» et éventuellement un événement portant le nom «ID &lt; unique &gt; --Shutdown \ _Event», puis le processus de lancement démarre sfttray.exe et attend que l’événement soit signalé. Après que l’événement « &lt; ID unique &gt; -result \ _Event» est signalé, le processus de lancement récupère le code de retour de 64 bits à partir de la région mappée en mémoire.

Si l’événement facultatif « &lt; ID unique &gt; -shutdown \ _Event» existe lors de la fermeture de l’application virtuelle, sfttray.exe s’ouvre et signale l’événement. Le processus de lancement attend ce événement d’arrêt s’il a besoin de déterminer à quel moment l’application virtuelle s’arrête.












---
title: À propos d'App-V5.0 SP2
description: À propos d'App-V5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806126"
---
# À propos d'App-V5.0 SP2


App-V 5.0 SP2 fournit une plateforme intégrée améliorée, une virtualisation plus flexible et une gestion puissante des applications virtualisées. Pour plus d’informations, voir [vue d’ensemble de l’application-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .

## Modifications apportées aux fonctionnalités standard App-V 5.0 SP2


Les sections suivantes contiennent des informations sur les modifications apportées aux fonctionnalités standard pour App-V 5.0 SP2.

### <a href="" id="bkmk-sp2-supported-cfg"></a>Prise en charge de Windows Server 2012 R2 et Windows 8,1

App-V 5,0 prend en charge Windows Server 2012 R2 et Windows 8,1

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> App-V 5.0 SP2 prend désormais en charge la redirection de dossiers pour le répertoire AppData d’itinérance de l’utilisateur.

App-V 5.0 SP2 prend en charge l’itinérance. redirection de dossier. Pour plus d’informations, reportez-vous [à la planification de l’utilisation de la redirection de dossiers avec App-V](planning-to-use-folder-redirection-with-app-v.md).

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a>Améliorations de la mise à niveau du package et des tâches en attente

Dans App-V 5.0 SP2, vous n’êtes plus invité à fermer une application virtuelle en cours d’exécution quand une nouvelle version du package ou du groupe de connexions est publiée. S’il s’agit d’un package ou d’un groupe de connexion utilisé lorsque vous essayez d’effectuer une tâche associée, un message s’affiche pour indiquer que l’objet est en cours d’utilisation et que l’opération sera tentée ultérieurement.

Les tâches qui ont été placées dans un état d’attente seront exécutées conformément aux règles suivantes:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de tâche</th>
<th align="left">Règle applicable</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tâche basée sur l’utilisateur (par exemple, publication d’un package pour un utilisateur);</p></td>
<td align="left"><p>La tâche en attente sera exécutée après que l’utilisateur se déconnecte, puis se reconnecte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Une tâche basée sur le monde (par exemple, l’activation globale d’un groupe de connexions);</p></td>
<td align="left"><p>La tâche en attente sera effectuée lorsque l’ordinateur sera arrêté, puis redémarré.</p></td>
</tr>
</tbody>
</table>

 

Lorsqu’une tâche est placée dans un état d’attente, le client App-V génère également une clé de Registre pour la tâche en attente, comme suit:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche basée sur le niveau utilisateur ou global</th>
<th align="left">Emplacement de génération de la clé de Registre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tâches basées sur l’utilisateur</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tâches globalement basées</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

### Virtualisation de Microsoft Office 2013 et Microsoft Office 2010 à l’aide de App-V 5,0

Utilisez le lien suivant pour plus d’informations sur les scénarios Microsoft Office pris en charge par App-V 5,0.

[Virtualisation de MicrosoftOffice2013 pour Application Virtualization (App-V)5.0](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

**Remarques**  Ce document porte sur la création d’un package Microsoft Office 2013 App-V 5,0. Toutefois, elle fournit également des informations sur les scénarios pour Microsoft Office 2010 avec App-V 5,0.

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> Application d’interface utilisateur de gestion des clients App-V 5,0

Dans les versions précédentes de App-V 5,0, l’interface utilisateur de gestion des clients a été fournie avec l’installation du client App-V 5,0. Ce n’est plus le cas avec l’App-V 5.0 SP2. Les administrateurs ont désormais la possibilité de déployer l’interface utilisateur du client App-V 5,0 en tant qu’application virtuelle (à l’aide des configurations de déploiement App-V prises en charge) ou d’une application installée.

Pour plus d’informations, voir [application de l’interface utilisateur du client Microsoft application virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .

### Déploiement et déploiement automatique d’assemblys côte à côte (SxS)

App-V 5.0 SP2 détecte automatiquement les assemblys côte à côte (SxS) et le déploiement sur l’ordinateur exécutant le client App-V 5.0 SP2. Un assemblage SxS se compose essentiellement des dépendances du runtime VC + + ou de MSXML. Dans les versions précédentes d’App-V, les applications virtuelles qui disposaient de dépendances sur l’exécution de VC nécessitent ces dépendances pour être effectuées localement sur l’ordinateur exécutant le client App-V 5.0 SP2.

Les fonctionnalités suivantes sont désormais prises en charge:

-   Le Sequencer App-V 5,0 capture automatiquement l’assembly SxS dans le package, que l’exécution du VC soit déjà installée sur l’ordinateur exécutant le Sequencer.

-   Le client App-V 5,0 installe automatiquement l’assembly SxS requis vers l’ordinateur exécutant le client selon les besoins au moment de la publication.

-   Le Sequencer App-V 5,0 signale la dépendance au moment de l’exécution VC à l’aide du mécanisme de création de rapports de Sequencer.

-   Le Sequencer App-V 5,0 vous permet désormais d’exclure la dépendance au moment de l’exécution VC dans l’éventualité où la dépendance est déjà disponible sur l’ordinateur exécutant le Sequencer.

### Améliorations de l’actualisation de la publication

App-V 5,0 prend en charge plusieurs fonctionnalités qui ont été ajoutées pour améliorer l’utilisation globale de l’actualisation d’un ensemble d’applications pour un utilisateur spécifique.

La liste suivante présente les améliorations de l’actualisation de publication:

La liste suivante contient des informations supplémentaires sur l’activation des nouvelles améliorations de l’actualisation de la publication.

-   **EnablePublishingRefreshUI** : permet d’activer la barre de progression de l’actualisation de la publication pour l’ordinateur exécutant le client App-V 5,0.

-   **HideUI** -masque la barre de progression de l’actualisation de la publication lors d’une synchronisation manuelle.

### Paramètre de configuration du nouveau client

Le paramètre de configuration de client suivant est disponible avec App-V 5,0 SP2:

**EnableDynamicVirtualization** -permet d’utiliser les extensions d’interpréteur de navigateur, les objets d’assistance du navigateur et les contrôles Active X pour être virtualisé et exécuté avec des applications virtuelles.

Pour plus d’informations, voir [à propos des paramètres de configuration du client](about-client-configuration-settings.md).

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> Extensions d’environnement App-V 5,0

App-V 5,0 SP2 prend désormais en charge les extensions d’environnement.

Pour plus d’informations, reportez-vous à la section **prise en charge** de la [création et de la gestion des Applications virtuelles 5,0 App](creating-and-managing-app-v-50-virtualized-applications.md)-v 5.0 SP2.

## <a href="" id="---------app-v-5-0-documentation-updates"></a> Mises à jour de la documentation App-V 5,0


App-V 5,0 SP2 fournit une documentation mise à jour pour les scénarios suivants:

-   [Migration à partir d'une version précédente](migrating-from-a-previous-version-app-v-50.md)

-   [À propos d'App-V5.0](about-app-v-50.md)

-   [À propos de la création de rapports App-V 5,0](about-app-v-50-reporting.md) (section Forum aux questions)

## Obtention de technologies MDOP


App-V 5,0 fait partie du pack d’optimisation du bureau Microsoft (MDOP). MDOP fait partie de Microsoft Software Assurance. Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .






## Rubriques connexes


[Notes de publication pour App-V5.0 SP2](release-notes-for-app-v-50-sp2.md)

 

 






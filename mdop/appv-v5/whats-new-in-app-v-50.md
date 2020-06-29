---
title: Nouveautés dans App-V5.0
description: Nouveautés dans App-V5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804813"
---
# Nouveautés dans App-V5.0


Cette section s’utilise pour les utilisateurs qui connaissent déjà App-V et qui souhaitent savoir ce qui a changé dans l’app-v 5,0 si vous ne connaissez pas encore l’application-v, vous devez commencer par lire [planification pour App-v 5,0](planning-for-app-v-50-rc.md).

## Modifications apportées aux fonctionnalités standard


Les sections suivantes contiennent des informations sur les modifications apportées aux fonctionnalités standard pour App-V 5,0.

### Modifications apportées aux systèmes d’exploitation pris en charge

Pour plus d’informations, voir [configurations App-V 5,0 prises en charge](app-v-50-supported-configurations.md).

## Modifications apportées au Sequencer


Les sections suivantes contiennent des informations sur les modifications apportées au Sequencer App-V 5,0.

### Modification spécifique au Sequencer

Le tableau suivant contient des informations sur les modifications apportées avec le Sequencer App-V 5,0

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fonction Sequencer</th>
<th align="left">Fonctionnalité Sequencer App-V 5,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Traitement du redémarrage</p></td>
<td align="left"><p>Lorsqu’une application vous invite à redémarrer, vous devez autoriser l’application à redémarrer l’ordinateur exécutant le Sequencer. L’ordinateur exécutant le Sequencer redémarre et le Sequencer reprend en mode d’analyse.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Spécification du répertoire d’application virtuel</p></td>
<td align="left"><p>Le répertoire d’application virtuel est un paramètre obligatoire. Pour obtenir de meilleurs résultats, il doit correspondre au répertoire d’installation du programme d’installation de l’application. Cela a pour effet d’optimiser les performances et la compatibilité des applications.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modification des raccourcis/FTAs</p></td>
<td align="left"><p>La page raccourcis/FTA s’affiche sur <strong> la </strong> page modification avancée une fois l’Assistant séquençage terminé.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Onglet Historique des modifications</p></td>
<td align="left"><p>L’onglet historique des modifications a été supprimé pour App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Onglet OSD</p></td>
<td align="left"><p>L’onglet OSD a été supprimé pour App-V 5,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Onglet Services virtuels</p></td>
<td align="left"><p>L’onglet services virtuels a été supprimé pour App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Onglet fichiers/système de fichiers virtuel</p></td>
<td align="left"><p>Ces onglets sont combinés et vous permettent de modifier les fichiers de package.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Onglet Déploiement</p></td>
<td align="left"><p>Il n’existe plus d’options de configuration de l’URL du serveur dans les packages. À présent, vous devez configurer cette opération à l’aide de la configuration de déploiement ou du serveur de gestion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outil convertisseur de package</p></td>
<td align="left"><p>Vous pouvez désormais utiliser PowerShell pour convertir des packages créés dans des versions antérieures.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Module complémentaire/middleware</p></td>
<td align="left"><p>Vous pouvez développer des packages parents lors du séquençage d’une application de complément ou middleware. Les modules complémentaires et les packages middleware doivent être connectés à l’aide de groupes de connexion dans l’application-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sortie de fichiers</p></td>
<td align="left"><p>Les fichiers suivants sont créés à l’aide de App-V 5,0, du programme d’installation Windows (. msi), de la configuration du déploiement, de la configuration utilisateur et du Report.XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Packages de compression/de sécurité/packages MSI</p></td>
<td align="left"><p>La compression et la création d’un fichier Windows Installer (. msi) s’exécutent automatiquement pour tous les packages et vous ne pouvez plus remplacer les descripteurs de sécurité.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outils/options</p></td>
<td align="left"><p>La fenêtre Diagnostics a été supprimée ainsi que d’autres paramètres.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Lecteur d’installation</p></td>
<td align="left"><p>Un lecteur d’installation n’est plus nécessaire lorsque vous installez une application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Flux OOS</p></td>
<td align="left"><p>S’il n’y a pas d’optimisation de flux, les packages sont défectueux lorsque ceux-ci sont invités par des ordinateurs exécutant le client App-V 5,0 jusqu’à ce qu’ils puissent lancer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Q: &lt; /p&gt;</td>
<td align="left"><p>App-V 5,0 utilise le système de fichiers natif et ne nécessite plus de Q:.</p></td>
</tr>
</tbody>
</table>

 

## Détection des erreurs de séquençage


Le Sequencer App-V 5,0 peut détecter les problèmes courants de séquençage lors du séquençage. La page **rapport d’installation** à la fin de l’Assistant séquençage affiche les messages de diagnostic classés en **erreurs**, **avertissements**et **informations** en fonction de la gravité du problème.

Pour afficher des informations plus détaillées sur un événement, double-cliquez sur l’élément que vous souhaitez consulter dans le rapport. Les problèmes de séquençage, ainsi que des suggestions sur la façon de résoudre les problèmes, sont affichées. Les informations issues du rapport de préparation du système et du rapport d’installation sont synthétisées lorsque vous avez terminé la création d’un package. La liste suivante indique les types de problèmes disponibles dans le rapport:

-   Fichiers exclus.

-   Informations sur le pilote.

-   Différences du système COM+.

-   Conflits côte à côte (SxS).

-   Extensions Shell.

-   Informations sur les services non pris en charge.

-   Protocole.

## Groupes de connexion


La fonctionnalité App-V auparavant appelée **composition suite dynamique** est désormais désignée sous le nom de **groupes de connexion** dans App-v 5,0. Pour plus d’informations sur l’utilisation des groupes de connexion, voir [gestion des groupes de connexion](managing-connection-groups.md).

## Fonctionnalité de gestion des licences et de mesure


La fonctionnalité d’application et de gestion des licences a été supprimée dans App-V 5,0. Le positionnement réel des licences dans votre environnement dépend des droits de licence et d’utilisation de votre logiciel spécifiques accordés par les termes du contrat de licence.

## Cache de fichiers et d’applications


Il n’y a pas de cache de fichiers ou d’application disponible avec App-V 5,0.






## Rubriques connexes


[À propos d'App-V5.0](about-app-v-50.md)

 

 






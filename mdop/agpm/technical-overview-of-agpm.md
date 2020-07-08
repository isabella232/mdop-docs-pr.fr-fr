---
title: Présentation technique d'AGPM
description: Présentation technique d'AGPM
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807450"
---
# Présentation technique d'AGPM


Microsoft Advanced Group Policy Management (AGPM) est une application client/serveur. Le serveur AGPM stocke les objets de stratégie de groupe hors connexion dans l’archive créée par AGPM sur le système de fichiers du serveur. Les administrateurs de stratégie de groupe utilisent le composant logiciel enfichable AGPM pour la console de gestion des stratégies de groupe (GPMC) pour fonctionner avec les objets de stratégie de groupe sur le serveur qui héberge l’archive. Le fait de comprendre les parties d’AGPM et des éléments apparentés, la façon dont les objets de stratégie de groupe peuvent être stockés dans le système de fichiers et la manière dont les autorisations contrôlent les actions disponibles pour chaque rôle d’utilisateur peuvent améliorer l’efficacité des administrateurs de stratégie de groupe pour AGPM.

## Terminology


Les informations suivantes décrivent les termes d’AGPM de base.

-   **Client AGPM:** Un ordinateur qui exécute le composant logiciel enfichable AGPM pour la console de gestion des stratégies de groupe (GPMC) et dont les administrateurs de stratégie de groupe gèrent les objets de stratégie de groupe.

-   **Composant logiciel enfichable AGPM:** Composants logiciels d’AGPM installés sur les clients AGPM de sorte qu’ils puissent gérer des objets de stratégie de groupe.

-   **Serveur AGPM:** Serveur qui exécute le service AGPM et gère une archive. Chaque serveur AGPM ne peut gérer qu’une seule archive, mais un serveur AGPM peut gérer les données d’archivage de plusieurs domaines dans une même archive. Une archive peut être hébergée sur un ordinateur autre qu’un serveur AGPM.

-   **Service AGPM:** Composant logiciel d’AGPM qui s’exécute sur un serveur AGPM en tant que service. Le service gère les objets de stratégie de groupe dans l’archive et dans l’environnement de production de cette forêt.

-   **Archive:** Dans AGPM, magasin central qui contient les objets de stratégie de groupe contrôlés gérés par le serveur AGPM associé, en plus de l’historique de chacun de ces objets. Cela inclut toutes les versions contrôlées précédentes de chaque GPO. Une archive est composée d’un fichier d’index d’archive et de données d’archive associées qui peuvent inclure des données pour les objets de stratégie de groupe dans plusieurs domaines. Une archive peut être hébergée sur un ordinateur autre qu’un serveur AGPM.

-   **GPO contrôlé:** Un objet de stratégie de groupe géré par AGPM. AGPM gère l’historique et les autorisations des objets de stratégie de groupe contrôlés qu’il stocke dans l’archive.

-   **Objet de stratégie de groupe non contrôlé:** Un objet GPO dans l’environnement de production d’un domaine et n’est pas géré par AGPM.

## Quelles installations d’AGPM, création et incidences;


Sur un serveur AGPM, le programme d’installation d’AGPM installe le service AGPM. AGPM ne modifie pas le service Active Directory® Directory ou le schéma. Par défaut, les fichiers du programme serveur AGPM sont installés dans%ProgramFiles%\\Microsoft\\AGPM\\Server. Vous pouvez installer le service AGPM sur un contrôleur de domaine, si nécessaire. Toutefois, nous vous recommandons d’installer le service AGPM sur un serveur membre.

Sur un client AGPM, le programme d’installation d’AGPM installe le composant logiciel enfichable AGPM, puis ajoute un dossier de **contrôle de modification** à chaque domaine figurant dans la console GPMC. Par défaut, les fichiers du programme client AGPM sont installés dans%ProgramFiles%\\Microsoft\\AGPM\\Client.

Le tableau 1 décrit à la fois les éléments installés ou créés par AGPM et les composants du système d’exploitation qui affectent le fonctionnement d’AGPM.

**Tableau 1: éléments installés, créés ou affectés par AGPM**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Service AGPM</p></td>
<td align="left"><p>Le service AGPM s’exécute sur le serveur AGPM. Le service gère l’archive qui contient les objets de stratégie de groupe hors ligne et les objets de stratégie de groupe contrôlés dans l’environnement de production. La configuration par défaut du service AGPM est la suivante:</p>
<ul>
<li><p><strong>Nom du service: </strong> service AGPM</p></li>
<li><p><strong>Nom d’affichage: </strong> service AGPM</p></li>
<li><p><strong>Chemin d’accès au fichier exécutable: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</p></li>
<li><p><strong>Démarrage: </strong> automatique</p></li>
<li><p><strong>Ouvrez une session en tant que: </strong> compte de service AGPM spécifié lors de l’installation d’AGPM Server, qui peut être modifié à l’aide <strong> de programmes et fonctionnalités </strong> dans le <strong> panneau de configuration </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Archive AGPM</p></td>
<td align="left"><p>Par défaut, AGPM crée l’archive dans%ProgramData%\Microsoft\AGPM sur le serveur AGPM. L’archive fournit un espace de stockage pour les objets de stratégie de connexion hors connexion et peut stocker plusieurs versions de chaque GPO. Les modifications apportées par AGPM aux objets de stratégie de groupe dans l’archive n’affectent pas l’environnement de production tant qu’un administrateur ou approbateur AGPM a déployé l’objet de stratégie de groupe dans l’environnement de production et relie l’objet de stratégie de groupe à une unité d’organisation.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pare-feu Windows</p></td>
<td align="left"><p>Lors de l’installation, AGPM autorise une règle de pare-feu Windows entrant qui permet au client AGPM de communiquer avec le serveur AGPM. La règle de pare-feu Windows par défaut est la suivante:</p>
<ul>
<li><p><strong>Nom: </strong> service AGPM</p></li>
<li><p><strong>Action: </strong> autoriser la connexion</p></li>
<li><p><strong>Programmes: </strong> tous les programmes qui répondent aux conditions spécifiées.</p></li>
<li><p><strong>Type de protocole: </strong> TCP</p></li>
<li><p><strong>Port local: </strong> 4600</p></li>
<li><p><strong>Port distant: </strong> tous les ports</p></li>
<li><p><strong>Adresse IP locale: </strong> tout</p></li>
<li><p><strong>Adresse IP distante: </strong> tout</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur de courrier</p></td>
<td align="left"><p>AGPM utilise le protocole SMTP (Simple Mail Transfer Protocol) pour envoyer des demandes de courrier électronique aux adresses configurées dans l' <strong> onglet délégation de domaine </strong> . Par exemple, lorsqu’un éditeur demande la création d’un objet de stratégie de groupe, AGPM avertit chaque adresse de messagerie spécifiée sous l' <strong> onglet délégation de domaine </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Composant logiciel enfichable AGPM</p></td>
<td align="left"><p>Le composant logiciel enfichable AGPM pour la console GPMC s’exécute sur les clients AGPM et est utilisé par les administrateurs de stratégie de groupe pour gérer les objets de stratégie de groupe. Le composant logiciel enfichable s’affiche dans la boîte de dialogue GPMC en tant que <strong> </strong> dossier de contrôle de modification dans chaque domaine.</p></td>
</tr>
</tbody>
</table>

 

### Références supplémentaires

Pour plus d’informations sur les fichiers installés par AGPM, voir le [Guide de planification pour AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).

## Archive


Par défaut, le processus d’installation d’AGPM Server crée l’archive sur le disque dur local du serveur AGPM sur%ProgramData%\\Microsoft\\AGPM. Toutefois, vous pouvez modifier la trajectoire au cours de l’installation et même créer l’archive sur un serveur autre que le serveur AGPM.

L’archive contient un sous-dossier pour chaque version de chaque GPO contenu dans l’archive. Le nom de chaque sous-dossier est un GUID qui identifie une version de l’objet de stratégie de groupe.

Le fichier gpostate.xml enregistre l’état de chaque GPO dans l’archive. Le fichier est un manifeste qui décrit le contenu de l’archive. Par exemple, un objet de stratégie de groupe peut avoir plusieurs versions et chaque version figure dans son propre sous-dossier dans l’archive. Le fichier gpostate.xml indique quels sous-dossiers contiennent différentes versions d’un objet de stratégie de groupe unique. De plus, les modèles d’objets de stratégie de groupe possèdent des sous-dossiers dans l’archive, mais gpostate.xml indiquent qu’il s’agit de modèles et non de GPO contrôlés. De la même manière, lorsque les administrateurs de stratégie de groupe suppriment des objets de stratégie de groupe, AGPM modifie leurs États dans gpostate.xml pour indiquer qu’ils se trouvent dans la **Corbeille** , mais ne supprime pas réellement les sous-dossiers de l’archive.

**Attention**  Ne modifiez pas manuellement gpostate.xml ou les objets de stratégie de groupe qu’il contient. Ces informations sont fournies uniquement pour améliorer la compréhension de l’archive AGPM. À la place, utilisez le composant logiciel enfichable AGPM pour modifier les objets de stratégie de groupe.

 

Lorsque AGPM crée l’archive, il accorde le contrôle total au système, aux administrateurs et au compte de service AGPM (spécifié dans le programme d’installation d’AGPM Server). La modification des autorisations à l’aide de l’interface utilisateur d’AGPM sur le composant additionnel AGPM ne modifie pas les autorisations sur l’archive, car le compte de service AGPM effectue toutes les opérations au nom de l’utilisateur connecté.

### Références supplémentaires

Pour plus d’informations sur la sauvegarde de l’archive, la restauration de celle-ci à partir d’une sauvegarde ou le déplacement du serveur et de l’archive AGPM, voir la section «exécuter les tâches d’administration AGPM» dans le [Guide des opérations pour AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).

## Rôles et autorisations


Les rôles simplifient la délégation. Au lieu d’affecter des autorisations détaillées aux administrateurs de stratégie de groupe, les administrateurs d’AGPM peuvent attribuer un des quatre rôles aux administrateurs de stratégie de groupe pour leur permettre d’effectuer le fonctionnement lié à ce rôle.

-   **Administrateur AGPM:** Les administrateurs de stratégie de groupe disposant du rôle Administrateur AGPM (contrôle total) peuvent effectuer n’importe quelle tâche dans AGPM. Les administrateurs d’AGPM peuvent configurer des options à l’échelle du domaine et des autorisations de délégué aux autres administrateurs de stratégie de groupe.

-   **Approbateur:** Les administrateurs de stratégie de groupe auxquels le rôle Approbateur peut déployer des objets de stratégie de groupe dans l’environnement de production d’un domaine. Les approbateurs peuvent également créer et supprimer des objets de stratégie de groupe et approuver ou refuser des demandes d’éditeur. Les approbateurs peuvent afficher la liste des objets de stratégie de groupe dans un domaine, afficher les paramètres de stratégie dans les objets de stratégie de groupe et créer et afficher des rapports sur les paramètres de stratégie d’un objet de stratégie de groupe. Ils ne peuvent pas modifier les paramètres de stratégie dans les objets de stratégie de groupe, sauf s’ils reçoivent également le rôle d’éditeur.

-   **Éditeur:** Les administrateurs de stratégie de groupe auxquels le rôle d’éditeur peut afficher la liste des objets de stratégie de groupe dans un domaine, afficher les paramètres de stratégie dans les objets de stratégie de groupe, modifier les paramètres de stratégie dans les objets de stratégie de groupe et créer et afficher des rapports sur les paramètres de stratégie d’un objet Sauf si le rôle Approbateur lui est également affecté, les éditeurs ne peuvent pas créer, déployer ou supprimer des objets de stratégie de groupe. Toutefois, ils peuvent demander la création, le déploiement et la suppression d’objets de stratégie de groupe.

-   **Relecteur:** Les administrateurs de stratégie de groupe qui ont attribué le rôle de réviseur peuvent afficher la liste des objets de stratégie de groupe dans un domaine et créer et afficher des rapports sur les paramètres de stratégie d’un objet de stratégie de groupe. Sauf si un rôle d’éditeur lui est affecté, il ne peut pas modifier les paramètres de stratégie d’un objet de stratégie de groupe.

AGPM fournit aux administrateurs d’AGPM la possibilité de configurer des autorisations pour un niveau plus détaillé que les rôles à l’aide du composant logiciel enfichable AGPM. Le tableau 2 décrit ces autorisations et indique les autorisations accordées à chaque rôle par défaut.

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
<th align="left">Autorisation</th>
<th align="left">Description</th>
<th align="left">Administrateur d’AGPM</th>
<th align="left">Approbateur</th>
<th align="left">Dacteur</th>
<th align="left">Relecteur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Contrôle total</strong></p></td>
<td align="left"><p>Disposer de toutes les autorisations.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Créer un objet de stratégie de groupe</strong></p></td>
<td align="left"><p>Créer des objets de stratégie de groupe dans un domaine.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Contenu de la liste</strong></p></td>
<td align="left"><p>Répertorier les objets de stratégie de groupe dans un domaine.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Lire les paramètres</strong></p></td>
<td align="left"><p>Lire les paramètres de stratégie au sein d’un objet de stratégie de groupe.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modifier les paramètres</strong></p></td>
<td align="left"><p>Modifiez les paramètres de stratégie d’un objet de stratégie de groupe.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Supprimer un objet de stratégie de groupe</strong></p></td>
<td align="left"><p>Supprimer un objet de stratégie de groupe</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modifier la sécurité</strong></p></td>
<td align="left"><p>Déléguez l’accès au niveau du domaine, déléguez l’accès à un objet GPO unique et déléguez l’accès à l’environnement de production.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Déploiement d’objets de stratégie de groupe</strong></p></td>
<td align="left"><p>Déploiement d’un objet de stratégie de groupe à partir de l’archive dans l’environnement de production.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Créer un modèle</strong></p></td>
<td align="left"><p>Créer un modèle d’objet de stratégie de groupe dans AGPM.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Modification des options</strong></p></td>
<td align="left"><p>Configurer les notifications par courrier électronique AGPM et limiter les versions d’objets de stratégie de groupe stockées dans l’archive.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Exporter un objet de stratégie de groupe</strong></p></td>
<td align="left"><p>Exporter un objet de stratégie de groupe dans un fichier.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Importer un objet de stratégie de groupe</strong></p></td>
<td align="left"><p>Importer un objet de stratégie de groupe à partir d’un fichier.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Remarques** 
 Les autorisations d' **exportation** d’objets de stratégie de groupe et d' **importation** ne sont pas disponibles dans AGPM 3,0 ou 2,5.

La possibilité de déléguer l’accès à des objets de stratégie de groupe dans l’environnement de production d’un domaine et la possibilité de limiter le nombre de versions d’objets de stratégie de groupe stockées ne sont pas disponibles dans AGPM 2,5.

 

### Références supplémentaires

Pour plus d’informations sur les tâches qui peuvent être effectuées par les administrateurs de stratégie de groupe ayant attribué un rôle particulier ou concernant les autorisations nécessaires à l’exécution d’une tâche spécifique, voir le [Guide des opérations pour AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).

 

 






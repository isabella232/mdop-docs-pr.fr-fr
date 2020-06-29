---
title: Vue d'ensemble d'Application Virtualization
description: Vue d'ensemble d'Application Virtualization
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806557"
---
# Vue d'ensemble d'Application Virtualization


Microsoft Application Virtualization (App-V) permet de rendre les applications accessibles aux utilisateurs finaux sans avoir à installer les applications directement sur ces ordinateurs. C’est possible par le biais d’un processus connu sous le nom de *Sequencer de l’application*, qui permet à chaque application de s’exécuter dans son propre environnement virtuel autonome sur l’ordinateur client. Les applications séquencées sont isolées les unes des autres. Cela élimine les conflits d’application, mais les applications peuvent quand même interagir avec l’ordinateur client.

Le client App-V est une fonctionnalité qui permet à l’utilisateur final d’interagir avec les applications une fois qu’elles ont été publiées sur l’ordinateur. Le client gère l’environnement virtuel dans lequel les applications virtuelles s’exécutent sur chaque ordinateur. Après avoir installé le client sur un ordinateur, les applications doivent être mises à disposition de l’ordinateur par le biais d’un processus connu sous le nom de *publication*, qui permet à l’utilisateur final d’exécuter les applications virtuelles. Le processus de publication copie les icônes et raccourcis des applications virtuelles sur l’ordinateur, généralement sur le bureau Windows ou dans le menu **Démarrer** , et copie également les informations de définition de package et d’association de type de fichier sur l’ordinateur. La publication rend également le contenu du package d’application disponible pour l’ordinateur de l’utilisateur final.

Le contenu du package d’application virtuel peut être copié sur un ou plusieurs serveurs de virtualisation des applications de sorte qu’il puisse être diffusé aux clients à la demande et mis en cache localement. Les serveurs de fichiers et les serveurs Web peuvent également être utilisés en tant que serveurs de diffusion en continu, ou être copiés directement sur l’ordinateur de l’utilisateur final, par exemple, si vous utilisez un système de distribution de logiciels électronique, tel que Microsoft Endpoint Manager. Dans une implémentation multiserveur, la mise à jour du contenu du package et sa mise à jour sur tous les serveurs de diffusion en continu nécessite une solution complète de gestion des packages. En fonction de la taille de votre organisation, il se peut que vous deviez disposer de nombreux applications virtuelles accessibles aux utilisateurs finaux dans le monde entier. Gestion des packages pour vous assurer que les applications appropriées sont disponibles pour tous les utilisateurs dans lesquels et quand ils ont besoin d’y accéder.

## Fonctionnalités du système de virtualisation des applications Microsoft


Le tableau suivant décrit les principales fonctionnalités du système de gestion de la virtualisation des applications Microsoft.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fonctionnalité</th>
<th align="left">Fonction</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serveur de gestion de Microsoft Application Virtualization</p></td>
<td align="left"><p>Responsable de la diffusion du contenu du package et de la publication des raccourcis et des associations de types de fichiers sur le client de virtualisation des applications.</p></td>
<td align="left"><p>Le serveur de gestion des applications virtuelles prend en charge la mise à niveau active, la gestion des licences et une base de données qui peut être utilisée pour la création de rapports.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Dossier de contenu </strong></p></td>
<td align="left"><p>Indique l’emplacement des packages de virtualisation d’application pour la diffusion en continu.</p></td>
<td align="left"><p>Ce dossier peut être localisé sur un serveur de gestion de la virtualisation des applications.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Management Console</p></td>
<td align="left"><p>Cette console est un outil de gestion des composants enfichables 3,0 de MMC utilisé pour l’administration de serveur Microsoft Application Virtualization.</p></td>
<td align="left"><p>Cet outil peut être installé sur le serveur Microsoft Application Virtualization ou situé sur une station de travail distincte qui comporte Microsoft Management Console (MMC) 3.0 et Microsoft. NETFramework 2,0 est installé.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Service Web de gestion de Microsoft Application Virtualization</p></td>
<td align="left"><p>Responsable de la communication de toutes les demandes de lecture et d’écriture dans le magasin de données de virtualisation des applications.</p></td>
<td align="left"><p>Le service Web de gestion peut être installé sur le serveur de gestion Microsoft Application Virtualization ou sur un autre ordinateur sur lequel Microsoft Internet Information Services (IIS) est installé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Magasin de données de Microsoft Application Virtualization</p></td>
<td align="left"><p>La base de données SQL Server App-V chargée du stockage de toutes les informations relatives à l’infrastructure de virtualisation des applications.</p></td>
<td align="left"><p>Ces informations incluent tous les enregistrements d’application, les affectations d’application et les groupes responsables de la gestion de l’environnement de virtualisation des applications.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur de diffusion de Microsoft Application Virtualization</p></td>
<td align="left"><p>Responsable de l’hébergement des packages de virtualisation d’application destinés à la diffusion en continu vers des clients dans une succursale, où le lien retour au serveur de gestion de l’application virtualisation est considéré comme une connexion de réseau de grande variété.</p></td>
<td align="left"><p>Ce serveur est doté de la fonctionnalité de diffusion en continu uniquement et ne fournit ni la console de gestion des applications virtuelles, ni le service Web de gestion des applications.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequencer Microsoft Application Virtualization</p></td>
<td align="left"><p>Le Sequencer est utilisé pour surveiller et capturer l’installation des applications afin de créer des packages d’applications virtuelles.</p></td>
<td align="left"><p>La sortie se compose d’icônes de l’application, d’un fichier. OSD contenant des informations de définition de package, d’un fichier manifeste de package et du fichier. SFT contenant les fichiers de contenu du programme d’application.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client Microsoft Application Virtualization</p></td>
<td align="left"><p>Le client de bureau et le client de virtualisation des applications pour les services Bureau à distance fournissent et gèrent l’environnement virtuel pour les applications virtualisées.</p></td>
<td align="left"><p>Le client de virtualisation d’applications Microsoft gère la diffusion du package dans le cache, l’actualisation de la publication, le transport et toute interaction avec les serveurs de virtualisation des applications.</p></td>
</tr>
</tbody>
</table>

 

 

 






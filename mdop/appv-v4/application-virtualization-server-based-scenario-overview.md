---
title: Présentation du scénario basé sur un serveur Application Virtualization Server
description: Présentation du scénario basé sur un serveur Application Virtualization Server
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809149"
---
# Présentation du scénario basé sur un serveur Application Virtualization Server


Si vous envisagez d’utiliser un scénario de déploiement basé sur serveur pour votre environnement Microsoft Application Virtualization, il est important de comprendre les différences entre le serveur de gestion de la *virtualisation des applications* et le serveur de diffusion de la virtualisation de l' *application*. Cette rubrique décrit ces différences et fournit des informations sur les méthodes de remise des packages, les protocoles de transmission et les composants externes que vous devez prendre en considération lorsque vous effectuez votre déploiement.

## Serveur de gestion Application Virtualization


Le serveur de gestion de la virtualisation des applications effectue la fonction de publication et la fonction streaming. Le serveur publie des icônes d’application, des raccourcis et des associations de type de fichier vers les clients App-V pour les utilisateurs autorisés. Lors de la réception de demandes d’applications par l’utilisateur, le serveur transmet les flux de données à la demande aux utilisateurs autorisés utilisant des protocoles RTSP ou RTSP. Dans la plupart des configurations utilisant ce serveur, un ou plusieurs serveurs de gestion partagent un magasin de données commun pour la configuration et les informations de package.

Les serveurs d’administration de la virtualisation des applications utilisent des groupes Active Directory pour gérer les autorisations des utilisateurs. Outre les services de domaine Active Directory (AD FS), vous avez installé SQL Server pour gérer la base de données et le magasin de données. Le serveur de gestion est contrôlé par le biais de la console de gestion des applications virtuelles, un composant logiciel enfichable à la console de gestion Microsoft.

Étant donné que les serveurs de gestion de l’application de la virtualisation de l’application les applications en utilisateurs finaux à la demande, ces serveurs sont idéalement adaptés aux configurations système qui disposent de réseaux locaux de grande bande passante et fiable.

## Serveur de streaming de la virtualisation des applications


Le serveur de diffusion en continu d’application fournit les mêmes fonctionnalités de mise à niveau de package et de mise à niveau de package fournies par le serveur de gestion, mais sans application Active Directory ou SQL Server requise. Toutefois, le serveur de diffusion en continu ne possède pas de service de publication et ne dispose pas de capacités de licence ou de mesure de la gestion des licences. Le service de publication d’un serveur de gestion App-V distinct est utilisé conjointement avec le serveur de streaming App-V. Le serveur de streaming App-V répond aux besoins des entreprises qui souhaitent utiliser la virtualisation des applications à plusieurs endroits grâce aux fonctionnalités de streaming de la configuration de serveur classique, mais peut ne pas disposer de l’infrastructure pour la prise en charge des serveurs d’administration d’applications-V dans chaque emplacement.

Le serveur de diffusion en continu d’applications peut également être utilisé dans les environnements avec un système de distribution de logiciels électronique (ESD) existant. La gestion des applications de diffusion en continu utilise une utilisation ESD. Contrairement au serveur de gestion de la virtualisation des applications, le serveur de diffusion en continu n’utilise pas SQL ou la console de gestion. Ces serveurs utilisent des listes de contrôle d’accès (ACL) pour accorder l’autorisation de l’utilisateur.

## Méthodes de remise du package


Si vous envisagez d’utiliser un serveur de virtualisation d’application en tant que méthode de remise de publication, vous devez déterminer qui utilise les méthodes de remise de package suivantes:

-   *Remise de package dynamique*

-   *Charger à partir du fichier remise du package*

### Remise de package dynamique

Lors de la remise d’un package dynamique, le serveur (Application Virtualization Management Server, serveur de diffusion en continu d’applications ou serveur IIS) fournit aux utilisateurs finaux des applications virtualisées par le biais du déploiement à la demande. Le serveur fournit les applications et packages virtualisés à un ordinateur client uniquement lorsqu’un utilisateur tente d’abord de lancer une application (à la demande). Le serveur transmet uniquement les blocs nécessaires pour démarrer l’application (bloc de fonctionnalité principal). Lorsque le bloc de fonctionnalité principal est remis au client, l’application s’exécute. le client ne reçoit pas l’application complète (déploiement incrémental), sauf si le client a besoin d’accéder à une partie de l’application qui n’est pas incluse dans le bloc de fonctionnalités principal. Lorsque cela se produit, le client effectue une requête d’absence de séquence et le bloc de fonctionnalité secondaire est transmis au client. La remise de packages dynamique permet un lancement rapide des applications.

### Charger à partir du fichier remise du package

Dans le cas d’un chargement à partir d’un package de fichier, le serveur remet l’intégralité du package de l’application virtualisée sur un ordinateur client avant que l’utilisateur ne lance l’application. Dans ce scénario, les applications virtualisées sont transmises en tant que package complet, plutôt que par le biais de la méthode dynamique et incrémentielle utilisée par le modèle de remise dynamique.

**Remarques**  Pour chaque méthode de remise, le processus de remise initial des applications virtuelles et le processus de mise à jour des applications virtuelles sont les mêmes. le package d’application virtuelle mis à jour remplace le package d’application d’origine.

 

Le tableau suivant compare les avantages et inconvénients de chaque méthode de remise du package.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Avantages</th>
<th align="left">Inconvénients</th>
<th align="left">Commentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Remise de package dynamique</p></td>
<td align="left"><p>Les applications sont transmises et mises à jour à la demande.</p>
<p>Les applications sont transmises et mises à jour de façon incrémentielle pour optimiser le temps de démarrage.</p>
<p>Des mises à jour sont automatiquement transmises au Bureau du client.</p></td>
<td align="left"><p>Encombrement plus important dans la topologie d’entreprise en raison de la configuration requise du serveur.</p>
<p>La diffusion d’application doit être via un réseau local. les scénarios de déploiement sur un réseau WAN ou qui utilisent une connexion intermittente ou peu fiable entre le serveur et le client peuvent être inutilisables.</p></td>
<td align="left"><p>Nécessite une infrastructure de diffusion en continu.</p>
<p>Programme d’installation Windows utilisé pour déployer le logiciel client de bureau de virtualisation des applications sur les ordinateurs des utilisateurs finaux.</p>
<p>Les grandes entreprises doivent utiliser des serveurs de streaming de la virtualisation des applications comme points de distribution.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Charger à partir du fichier remise du package</p></td>
<td align="left"><p>Conformément aux pratiques de gestion standard de l’entreprise.</p>
<p>Prend en charge le scénario de configuration autonome.</p>
<p>Fournit une solution au problème de micro-succursale.</p></td>
<td align="left"><p>La livraison et la mise à jour de l’application ne peuvent pas être à la demande.</p>
<p>La livraison et la mise à jour de l’application ne sont pas incrémentielles; Cela augmente la consommation de ressources par rapport au service de remise dynamique.</p></td>
<td align="left"><p>L’organisation informatique est souvent responsable de la gestion des licences d’applications, de l’autorisation des utilisateurs et de l’authentification.</p></td>
</tr>
</tbody>
</table>

 

## Protocoles liés au serveur et composants externes


Le tableau suivant répertorie les types de serveurs qui peuvent être utilisés dans les scénarios serveur de virtualisation des applications, ainsi que les protocoles de transport correspondants et les composants externes nécessaires à la prise en charge de la configuration du serveur spécifique. La table inclut également le mécanisme de création de rapports et le mécanisme de mise à niveau actif pour chaque type de serveur. Dans la mesure où ces scénarios utilisent tous le serveur de gestion des applications virtuelles, vous pouvez utiliser la fonctionnalité de création de rapports interne intégrée au système. Si vous utilisez une gestion de la virtualisation des applications ou un serveur de diffusion en continu de l’application pour obtenir des packages sur le client, les packages sur le serveur sont automatiquement mis à niveau lorsqu’un utilisateur se connecte au client. Si vous utilisez des serveurs IIS ou un fichier pour livrer les packages au client, les packages sur le client doivent être mis à niveau manuellement.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de serveur</th>
<th align="left">Protocoles</th>
<th align="left">Composants externes nécessaires</th>
<th align="left">Rapports</th>
<th align="left">Mise à niveau active</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serveur de gestion Application Virtualization</p></td>
<td align="left"><p>RTSP</p>
<p>RTSP</p></td>
<td align="left"><p>Dans le cadre de l’utilisation de HTTPs, utilisez un serveur IIS pour télécharger des fichiers ICO et OSD ainsi qu’un pare-feu afin de protéger le serveur contre toute exposition à Internet.</p></td>
<td align="left"><p>Interne</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur de streaming de la virtualisation des applications</p></td>
<td align="left"><p>RTSP</p>
<p>RTSP</p></td>
<td align="left"><p>Utilisez un mécanisme pour synchroniser le contenu entre le serveur de gestion et le serveur de diffusion. Dans le cadre de l’utilisation de HTTPs, utilisez un serveur IIS pour télécharger des fichiers ICO et OSD et utiliser un pare-feu pour protéger votre serveur contre toute exposition à Internet.</p></td>
<td align="left"><p>Interne</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Serveur IIS</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Utilisez un mécanisme pour synchroniser le contenu entre le serveur de gestion et le serveur de diffusion. Dans le cadre de l’utilisation de HTTP ou HTTPs, utilisez un serveur IIS pour télécharger des fichiers ICO et OSD ainsi qu’un pare-feu afin de protéger le serveur contre toute exposition à Internet.</p></td>
<td align="left"><p>Interne</p></td>
<td align="left"><p>Non prise en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fichier</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>Vous avez besoin d’un moyen de synchroniser le contenu entre le serveur de gestion et le serveur de diffusion. Vous avez besoin d’un ordinateur client doté d’une fonctionnalité de partage de fichiers ou de flux.</p></td>
<td align="left"><p>Interne</p></td>
<td align="left"><p>Non prise en charge</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Procédure pour configurer des serveurs pour un déploiement basé sur un serveur](how-to-configure-servers-for-server-based-deployment.md)

[Procédure pour installer les serveurs et les composants système](how-to-install-the-servers-and-system-components.md)

 

 






---
title: Analyse des serveurs Application Virtualization Server
description: Analyse des serveurs Application Virtualization Server
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806589"
---
# Analyse des serveurs Application Virtualization Server


Pour simplifier la gestion de serveur de la virtualisation des applications (App-V), vous pouvez utiliser le pack d’administration Manager2007 Operations Center. Ce module d’administration prend uniquement en charge les serveurs 4,5 de virtualisation des applications (App-V). elle ne prend pas en charge les versions antérieures du serveur. Le pack d’administration maximise la disponibilité du serveur App-V pour gérer les demandes des clients App-V.

## Indicateurs d’État


Les indicateurs d’état d’intégrité du serveur App-V sont des codes de couleur. Les couleurs représentent les valeurs d’État suivantes:

-   Aucune couleur indique que le serveur fonctionne sans erreur non récupérable.

-   Le jaune indique que l’un des composants ne fonctionne pas correctement. La fonctionnalité globale du serveur est détériorée, mais le serveur est toujours disponible.

-   Rouge indique que le serveur n’est pas disponible et qu’il ne peut pas fournir de services clés ou communiquer avec des dépendances de service externe.

## Critères d’analyse


Le pack d’administration analyse les aspects suivants du fonctionnement du serveur:

-   État du serveur: analyse les événements du serveur pour vérifier que le serveur fournit ses services attendus.

-   Accès au magasin de données: permet de suivre la capacité d’un ou de plusieurs serveurs d’administration de l’application à accéder à la Banque de données App-V et à communiquer avec celle-ci.

-   Accès aux données de contenu: contrôle l’accès au répertoire \\Content, qui peut être un répertoire local ou un partage réseau, et la possibilité de lire les fichiers demandés.

-   Sécurité: signale les erreurs liées au certificat du serveur App-V et aux communications sécurisées.

-   Gestion des demandes de clients: surveille la capacité d’un ou de plusieurs serveurs App-V à gérer et à répondre correctement aux demandes des clients. Il s’agit notamment de publier des éléments tels que des demandes de configuration, des demandes de chargement de packages et des demandes hors séquence.

-   Configuration du serveur: vérifie les paramètres de configuration du serveur App-V. Ces paramètres de configuration incluent les paramètres du Registre et du magasin de données App-V.

## Différences de serveur


Les principales différences entre le serveur de gestion App-V et le serveur de streaming d’applications-V sont les suivantes:

-   Les serveurs de gestion App-V peuvent fournir des services de publication, de diffusion, de gestion et de création de rapports. Par conséquent, le pack d’administration peut gérer davantage de aspects du serveur de gestion d’application-V qu’il peut gérer sur le serveur de streaming App-V, qui fournit uniquement du streaming de package.

-   Le serveur de streaming App-V n’ayant pas de magasin de données App-V, l’accès au magasin de données n’est pas surveillé. Les informations de configuration du serveur de streaming App-V sont gérées dans le registre.

-   Le serveur de streaming App-V n’utilise pas l’interface de la console App-V Server Management. utiliser d’autres outils pour gérer la configuration.

## Rubriques connexes


[Application Virtualization Server](application-virtualization-server.md)

 

 






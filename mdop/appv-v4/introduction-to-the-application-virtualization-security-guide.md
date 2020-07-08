---
title: Introduction au Guide de sécurité d’application Virtualization
description: Introduction au Guide de sécurité d’application Virtualization
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806638"
---
# Introduction au Guide de sécurité d’application Virtualization


Ce guide de sécurité de Microsoft Application Virtualization (App-V) fournit des instructions pour les administrateurs chargés de la configuration des fonctionnalités de sécurité sélectionnées pour le déploiement d’App-V.

**Remarques**  Cette documentation ne fournit pas d’aide pour choisir les options de sécurité spécifiques. Ces informations sont fournies dans le livre blanc App-V Security meilleures pratiques disponible sur le <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

En tant qu’administrateur d’application-V utilisant ce guide, vous devez être familiarisé avec les technologies suivantes en matière de sécurité:

-   Services de domaine ActiveDirectory

-   Infrastructure à clé publique (PKI)

-   Sécurité du protocole Internet (IPsec)

-   Stratégies de groupe

-   Internet Information Services (IIS)

## Composants d’infrastructure APP-V


Lors de la planification d’un environnement d’application de sécurité améliorée, vous pouvez envisager différents modèles d’infrastructure.

**Remarques**  Pour plus d’informations sur les modèles d’infrastructure App-V, voir la documentation suivante:

-   [Guide de planification et de déploiement d’App-V](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [Série de guides de planification et de conception d’infrastructure](https://go.microsoft.com/fwlink/?LinkId=151986)

 

Ces modèles utilisent certains composants de l’application-V, mais ce n’est pas tout illustré dans l’illustration suivante.

![diagramme d’intersuccursales App-v](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Serveur de gestion Application Virtualization (App-V)  
Le serveur de gestion App-V diffuse le contenu du package et publie les raccourcis et les associations de types de fichiers sur le client App-V. Le serveur de gestion App-V prend également en charge la mise à niveau active, la gestion des licences et une base de données qui peut être utilisée pour la création de rapports.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Serveur de diffusion en continu d’applications (App-V)  
Le serveur de streaming App-V héberge les packages de diffusion en continu pour les clients App-v dans les environnements, tels que les succursales, où la bande passante pour la connexion au serveur de gestion de l’application-V est insuffisante pour le contenu du package de diffusion en continu vers les clients. Le serveur de diffusion en continu comporte uniquement une fonctionnalité de diffusion en continu et ne vous permet pas d’utiliser la console de gestion des applications ou le service Web App-V.

<a href="" id="application-virtualization--app-v--data-store"></a>Magasin de données Application Virtualization (App-V)  
Le magasin de données App-V, dans la base de données SQL, conserve les informations relatives à l’infrastructure App-V. Les informations contenues dans le magasin de données App-V incluent tous les enregistrements d’application, les affectations d’application et les groupes qui gèrent l’environnement de virtualisation des applications.

<a href="" id="application-virtualization--app-v--management-service"></a>Service de gestion Application Virtualization (App-V)  
Le service de gestion App-V transmet les demandes en lecture/écriture au magasin de données de virtualisation des applications. Ce composant peut être installé sur le même ordinateur que le serveur de gestion de l’application-V ou sur un autre ordinateur sur lequel IIS est installé.

<a href="" id="application-virtualization--app-v--management-console"></a>Console de gestion Application Virtualization (App-V)  
La console de gestion App-V est un utilitaire de gestion des composants enfichables pour l’administration de l’application-V Server. Ce composant peut être installé sur le même ordinateur que le serveur App-V ou sur une station de travail distincte disposant de MMC 3.0 et. .NET 2.0 installé.

<a href="" id="application-virtualization--app-v--sequencer"></a>Sequencer Application Virtualization (App-V)  
Le Sequencer App-V surveille et capture l’installation d’applications et crée des packages d’application virtuelle. La sortie du Sequencer se compose de l’icône de l’application, du fichier OSD contenant des informations de définition d’application, d’un fichier manifeste de package et d’un fichier SFT contenant les fichiers de contenu de l’application. Vous pouvez également créer un fichier Windows Installer pour installer le package sans utiliser l’infrastructure App-V.

<a href="" id="application-virtualization--app-v--client"></a>Client Application Virtualization (App-V)  
Le client App-V est installé sur l’ordinateur client de bureau App-v ou sur l’ordinateur client de services Terminal Server App-v. Il fournit l’environnement virtuel pour les packages d’applications virtuelles. Le client App-V gère le package en flux continu sur le cache, l’actualisation de la publication des applications virtuelles et l’interaction avec les serveurs de virtualisation des applications.

 

 






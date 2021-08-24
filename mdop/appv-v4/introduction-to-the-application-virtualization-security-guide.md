---
title: Présentation du Guide de sécurité d’Application Virtualization
description: Présentation du Guide de sécurité d’Application Virtualization
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
ms.openlocfilehash: 82914de48a5a5777f6ce4b50fe3e8af34dd82494
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910779"
---
# <a name="introduction-to-the-application-virtualization-security-guide"></a>Présentation du Guide de sécurité d’Application Virtualization


Ce guide de sécurité Microsoft Application Virtualization (App-V) fournit des instructions aux administrateurs chargés de configurer les fonctionnalités de sécurité sélectionnées pour le déploiement d’App-V.

**Remarque**  
Cette documentation ne fournit pas de conseils pour choisir les options de sécurité spécifiques. Ces informations sont fournies dans le livre blanc Sur les meilleures pratiques en matière de sécurité d’App-V disponible sur <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

En tant qu’administrateur App-V utilisant ce guide, vous devez connaître les technologies de sécurité suivantes :

-   Services de domaine Active Directory

-   Infrastructure à clé publique (PKI)

-   IPsec (Internet Protocol Security)

-   Stratégies de groupe

-   Internet Information Services (IIS)

## <a name="app-v-infrastructure-components"></a>Composants d’infrastructure APP-V


Lors de la planification d’un environnement App-V de sécurité renforcée, vous pouvez prendre en compte plusieurs modèles d’infrastructure différents.

**Remarque**  
Pour plus d’informations sur les modèles d’infrastructure App-V, voir la documentation suivante :

-   [Guide de planification et de déploiement d’App-V](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [Série de guides de planification et de conception d’infrastructure](https://go.microsoft.com/fwlink/?LinkId=151986)

 

Ces modèles utilisent certains des composants App-V illustrés dans l’illustration suivante.

![Diagramme de la filiale app-v.](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Application Virtualization (App-V) Management Server  
Le serveur de gestion App-V diffuse le contenu du package et publie les raccourcis et les associations de types de fichiers sur le client App-V. Le serveur de gestion App-V prend également en charge la mise à niveau active, la gestion des licences et une base de données qui peut être utilisée pour la rapports.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Serveur de diffusion en continu Application Virtualization (App-V)  
Le serveur de diffusion en continu App-V héberge les packages pour la diffusion en continu vers les clients App-V dans des environnements tels que les succursales, où la bande passante de la connexion au serveur de gestion App-V est insuffisante pour le contenu du package de diffusion en continu pour les clients. Le serveur de diffusion en continu contient uniquement la fonctionnalité de diffusion en continu et ne vous fournit pas la console de gestion App-V ou le service Web de gestion App-V.

<a href="" id="application-virtualization--app-v--data-store"></a>Magasin de données Application Virtualization (App-V)  
Le magasin de données App-V, dans la base de données SQL, conserve les informations relatives à l’infrastructure App-V. Les informations du magasin de données App-V incluent tous les enregistrements d’application, les affectations d’applications et les groupes qui gèrent l’environnement Application Virtualization.

<a href="" id="application-virtualization--app-v--management-service"></a>Service de gestion Application Virtualization (App-V)  
Le service de gestion App-V communique les demandes de lecture/écriture au magasin de données Application Virtualization. Ce composant peut être installé sur le même ordinateur que le serveur de gestion App-V ou sur un ordinateur distinct où IIS est installé.

<a href="" id="application-virtualization--app-v--management-console"></a>Console de gestion Application Virtualization (App-V)  
La console de gestion App-V est un utilitaire de gestion en snap-in pour l’administration d’App-V Server. Ce composant peut être installé sur le même ordinateur que le serveur App-V ou sur une station de travail distincte où MMC 3.0 et .NET 2.0 sont installés.

<a href="" id="application-virtualization--app-v--sequencer"></a>Séquenceur Application Virtualization (App-V)  
Le séquenceur App-V surveille et capture l’installation des applications et crée des packages d’applications virtuelles. La sortie de Sequencer se compose de l’icône de l’application, du fichier OSD contenant les informations de définition d’application, d’un fichier manifeste de package et d’un fichier SFT contenant les fichiers de contenu de l’application. Éventuellement, un fichier Windows Installer peut être créé pour l’installation du package sans utiliser l’infrastructure App-V.

<a href="" id="application-virtualization--app-v--client"></a>Application Virtualization (App-V) Client  
Le client App-V est installé sur l’ordinateur client de bureau App-V ou sur l’ordinateur client des services Terminal Services App-V. Il fournit l’environnement virtuel pour les packages d’application virtuelle. Le client App-V gère la diffusion en continu du package dans le cache, l’actualisation de la publication d’applications virtuelles et l’interaction avec les serveurs Application Virtualization.

 

 






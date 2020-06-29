---
title: Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server
description: Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809030"
---
# Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server


Après avoir terminé le processus de mise en service des certificats et modifié les autorisations de clé privée pour prendre en charge l’installation de l’application-V, vous pouvez lancer le programme d’installation du serveur de gestion ou du serveur de diffusion. Lors de l’installation, si un certificat est configuré avant d’exécuter le programme d’installation, l’Assistant affiche le certificat dans l’écran **mode de sécurité** de la connexion et, par défaut, la case à cocher **utiliser la sécurité améliorée** est activée.

**Remarques**  Sélectionnez le certificat configuré pour App-V s’il existe plusieurs certificats approvisionnés pour ce serveur.

 

**Important**  Lors de la mise à niveau de la version 4,2 vers la version 4,5, le programme d’installation propose une option d’utilisation de la **sécurité améliorée**. Toutefois, la sélection de cette option ne désactive pas la diffusion en continu sur RTSP. Vous devez utiliser la console de gestion pour désactiver RTSP après l’installation.

 

Sélectionnez le port TCP utilisé par le service pour les communications client. Le port par défaut est TCP 322; Toutefois, vous pouvez remplacer le port par un port personnalisé pour votre environnement.

Les étapes restantes de l’Assistant sont identiques à celles de déploiement d’une application ou d’un serveur de diffusion en continu sans utilisation de la fonctionnalité de **sécurité améliorée** .

## Configuration de certificats pour les environnements NLB


Pour prendre en charge des entreprises de grande taille, le serveur de gestion est souvent placé dans un cluster d’équilibrage de charge réseau (NLB) pour prendre en charge un grand nombre de connexions. Cela nécessite au moins deux serveurs d’administration qui semblent être un serveur de gestion unique. Lorsque votre environnement utilise un cluster NLB avec plusieurs serveurs de gestion, vous avez besoin d’une configuration avancée du certificat utilisé pour le cluster NLB.

Le certificat App-V est soumis à une autorité de certification qui est configurée sur un ordinateur exécutant Windows Server2003. Le SAN vous permet de vous connecter à un nom d’hôte de cluster de votre serveur de gestion NLB en utilisant un nom DNS (Domain Name System) qui peut différer du nom de l’ordinateur réel, car il peut y avoir jusqu’à 32 serveurs qui comprennent le cluster NLB.

Cette configuration est nécessaire uniquement lors de l’utilisation d’un cluster NLB. Lorsque le client se connecte au serveur, il se connecte à l’aide du nom de domaine complet (FQDN) du cluster NLB et non du nom de domaine complet d’un serveur individuel. Si vous n’ajoutez pas la propriété SAN avec le nom de domaine complet (FQDN) des nœuds serveur dans le groupe, toutes les connexions client ne correspondent pas, car le nom commun du certificat ne correspond pas au nom du serveur.

Pour plus d’informations sur la configuration des certificats avec l’attribut SAN, voir <https://go.microsoft.com/fwlink/?LinkId=133228> .

## Rubriques connexes


[Configuration de certificats pour prendre en charge la diffusion en continu sécurisée](configuring-certificates-to-support-secure-streaming.md)

[Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 






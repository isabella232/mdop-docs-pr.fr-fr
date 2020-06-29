---
title: Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server
description: Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806942"
---
# Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server


Pour prendre en charge une installation App-V plus sécurisée, vous pouvez utiliser les procédures suivantes pour modifier les clés privées dans Windows Server2003 ou Windows Server 2008. Pour modifier les autorisations de la clé privée, vous pouvez utiliser l’outil Kit de ressources Windows Server2003 `WinHttpCertCfg.exe` .

Pour Windows Server 2003, la procédure exige qu’un certificat qui répond aux conditions préalables répertoriées dans ce document soit installé sur l’ordinateur ou sur les ordinateurs sur lesquels vous installez la gestion de l’application-V ou du serveur de diffusion. Des informations supplémentaires sur l’utilisation de l' `WinHttpCertCfg.exe` outil sont disponibles à l’adresse <https://go.microsoft.com/fwlink/?LinkId=151981> .

Dans Windows Server 2008, le processus de modification des ACL sur la clé privée est beaucoup plus simple. L’interface utilisateur du certificat peut être utilisée pour gérer les autorisations de clés privées.

**Remarques**  Le contexte de sécurité par défaut est service réseau. Toutefois, un compte de domaine peut être utilisé à la place.

 

**Pour gérer les clés privées dans Windows Server2003**

1.  Sur l’ordinateur qui deviendra la gestion de l’App-V ou du serveur de diffusion en continu, tapez la commande suivante dans une invite de commandes pour répertorier les autorisations actuelles affectées à un certificat spécifique:

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  Le cas échéant, modifiez les autorisations du certificat afin d’offrir un accès en lecture au contexte de sécurité qui sera utilisé pour la gestion ou le service de diffusion en continu:

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  Vérifiez que le contexte de sécurité a été correctement ajouté en indiquant les autorisations sur le certificat:

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**Pour gérer les clés privées dans Windows Server 2008**

1.  Créez une console MMC en utilisant le composant logiciel enfichable *certificats* qui cible le magasin de certificats de l' *ordinateur local* .

2.  Développez la console MMC et sélectionnez **gérer les clés privées**.

3.  Dans l’onglet **sécurité** , ajoutez le compte **service réseau** avec accès **en lecture** .

## Rubriques connexes


[Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[Configuration de certificats pour prendre en charge la diffusion en continu sécurisée](configuring-certificates-to-support-secure-streaming.md)

 

 






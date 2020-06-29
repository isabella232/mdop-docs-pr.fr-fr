---
title: Installation d'App-V Management Server ou Streaming Server en toute sécurité
description: Installation d'App-V Management Server ou Streaming Server en toute sécurité
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806662"
---
# Installation d'App-V Management Server ou Streaming Server en toute sécurité


Les rubriques de cette section fournissent des informations sur l’installation d’une version de sécurité améliorée du serveur d’administration d’applications-V ou du serveur de streaming d’applications-V.

**Remarques**  Pour utiliser la sécurité améliorée (par exemple, Transport Layer Security ou TLS), l’installation ou la configuration d’une gestion d’application-V ou d’un serveur de diffusion en continu nécessite le mise en service d’un certificat X. 509 v3 sur le serveur App-V.

 

Lorsque vous préparez l’installation ou la configuration d’une gestion sécurisée ou d’un serveur de diffusion en continu, prenez en compte les exigences techniques suivantes:

-   Le certificat doit être valide. Si le certificat n’est pas valide, le client arrête la connexion.

-   Le certificat doit contenir l' *utilisation améliorée* de l’utilisation de la clé (EKU), authentification serveur (OID 1.3.6.1.5.5.7.3.1). Si ce n’est pas le cas, le client arrête la connexion.

-   Le nom de domaine complet (FQDN) du certificat doit correspondre au serveur sur lequel il est installé. Par exemple, si le client appelle `RTSPS://Myserver.mycompany.com/content/MyApp.sft` et que le certificat **émis pour** le champ est défini sur `Server1.mycompany.com` , le client ne se connecte pas au serveur et la session se termine. L’erreur est signalée à l’utilisateur.

    **Remarques**  Si vous utilisez App-V dans un cluster d’équilibrage de charge réseau, vous devez configurer le certificat avec d’autres noms de sujet (San) pour prendre en charge les RTSP. Pour plus d’informations sur la configuration de l’autorité de certification et la création de certificats avec des réseaux SAN, voir <https://go.microsoft.com/fwlink/?LinkId=133228> .

     

-   Le client et le serveur doivent faire confiance à l’autorité de certification racine; l’autorité de certification émettant le certificat au serveur App-V doit être approuvée par le client se connectant au serveur. Si ce n’est pas le cas, le client arrête la connexion.

-   La clé privée du certificat doit être modifiée pour permettre au compte de service App-V d’accéder au certificat. Par défaut, l’application-V utilise le compte de service réseau, et par défaut, le compte de service réseau n’a pas l’autorisation d’accéder à la clé privée, ce qui empêchera les connexions sécurisées.

## Dans cette section


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[Configuration de certificats pour prendre en charge la diffusion en continu sécurisée](configuring-certificates-to-support-secure-streaming.md)  
Fournit des informations sur l’obtention, la configuration et l’installation de certificats pour la prise en charge de la diffusion en continu sécurisée.

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
Fournit des procédures que vous pouvez utiliser pour modifier des clés dans Windows Server2003 et Windows Server 2008.

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
Fournit des informations sur la configuration des certificats pour la gestion des applications ou des serveurs de diffusion en continu, y compris des informations sur la configuration des certificats pour les environnements d’équilibrage de charge réseau.

 

 






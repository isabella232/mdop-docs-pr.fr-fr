---
title: Vue d'ensemble de la sécurité et de la protection
description: Vue d'ensemble de la sécurité et de la protection
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806394"
---
# Vue d'ensemble de la sécurité et de la protection


Microsoft Application Virtualization 4.5 fournit les fonctionnalités de sécurité améliorées suivantes pour vous aider à planifier et à implémenter une stratégie de déploiement plus sécurisée:

-   La virtualisation des applications prend désormais en charge le protocole TLS (Transport Layer Security) à l’aide de certificats X. 509 v3. Dans la mesure où un certificat de serveur a été configuré pour la gestion des applications planifiées ou le serveur de diffusion en continu, l’installation sera sécurisée par défaut en utilisant le protocole RTSP sur le port 322. L’utilisation de RTSPs vous permet de garantir que les communications entre les serveurs de virtualisation des applications et les clients de virtualisation d’application sont signées et chiffrées. Si aucun certificat n’est attribué au serveur lors de l’installation du serveur de virtualisation des applications, la communication sera définie sur RTSP sur le port 554.

    **Note de sécurité:**

    Pour garantir la sécurité de l’installation du serveur, vous devez vous assurer que les ports RTSP sont désactivés, même si tous les packages sont configurés pour utiliser les RTSP.

    Si vous ajoutez des certificats de sécurité au serveur après l’installation du serveur, il est possible que le serveur ne détecte pas les certificats. Pour garantir la détection des certificats de sécurité, redémarrez le serveur une fois que vous avez ajouté les certificats.

-   Le client doit être configuré pour utiliser le même protocole et port que le serveur, mais il ne sera pas en mesure de communiquer avec le serveur. Le client doit également approuver l’émetteur du certificat et est fourni avec plusieurs des fournisseurs principaux dans son magasin de racines de confiance. Vous pouvez utiliser des certificats auto-signés, mais vous devrez mettre à jour les clients.

-   Lorsque vous configurez des serveurs IIS pour utiliser le protocole HTTPs pour la diffusion en continu, vous devez configurer SSL (Secure Sockets Layer) sur le serveur IIS et approvisionner le certificat du serveur. Les clients devront également être configurés de manière à approuver l’autorité de certification racine qui a émis le certificat de serveur.

-   L’authentification Kerberos a été ajoutée à la virtualisation d’application Microsoft comme mécanisme d’authentification par défaut. Les versions antérieures étaient réutilisables avec NTLM v2 pour l’authentification. L’authentification Kerberos renforce la sécurité de la communication entre le client et le serveur de virtualisation des applications. Lors de l’initialisation d’une connexion à partir du client, le serveur de virtualisation des applications vérifie le ticket de session avec le centre de distribution principal.

-   En raison de la prise en charge de l’utilisation des certificats de serveur et de l’utilisation des protocoles RTSP ou HTTPs, vous pouvez désormais prendre en charge des clients en dehors du réseau d’entreprise. Cela peut vous aider à éviter que les utilisateurs mobiles aient configuré une connexion sécurisée au réseau d’entreprise (VPN, RAS, etc.) avant de lancer des applications de virtualisation de l’application.

Voici d’autres considérations importantes en matière de sécurité à prendre en compte:

-   Veillez à toujours mettre à jour et à protéger les serveurs.

-   Pour ajouter un certificat afin d’offrir des communications plus sûres au serveur de gestion des applications, les critères suivants doivent être satisfaits:

    -   L’utilisateur qui va ajouter le certificat doit être administrateur sur le serveur sur lequel se trouve le magasin de certificats.

    -   Le service serveur doit être démarré.

    -   Le port 139 du serveur de gestion doit être ouvert au service Web server’sIP.

-   Utilisez les listes de contrôle d’accès (ACL) pour vous assurer que les packages d’application et tous les fichiers de package sont protégés et ne peuvent pas être falsifiés. Les listes de Contrã’le d’accès restreignent l’accès à l’emplacement ou au dossier où vous stockez les packages, autorisant uniquement l’accès à certains comptes.

-   Vérifiez que le canal entre le serveur de gestion de la virtualisation des applications et la base de données est sécurisé (par exemple, en utilisant IPsec).

-   Si les packages sont stockés sur un réseau SAN ou NAS, assurez-vous que la connexion entre le périphérique de stockage central et les serveurs de virtualisation des applications est assurée.

-   Tous les canaux de communication vers le client doivent être protégés (y compris les connexions au serveur de publication, le serveur de virtualisation des applications, ainsi que le chemin d’accès aux fichiers OSD et ICO) en utilisant un protocole tel que HTTPs ou IPsec. 

-   Les autorisations client doivent être configurées pour vous assurer que les packages ne peuvent pas être falsifiés par les utilisateurs. Il est particulièrement important que vous ne soyez pas autorisé à autoriser les utilisateurs à ajouter ou à mettre à jour des packages sur des systèmes, tels que des serveurs d’hôte de session Bureau à distance (RDSession) partagés avec plusieurs utilisateurs.

-   L’authentification Kerberos doit être autorisée sur les environnements de domaine ou de forêt pour que la console de gestion du serveur fonctionne correctement.

-   Cette version du logiciel n’est pas prise en charge par l’hébergement d’un serveur RTSP utilisant Kerberos et d’un serveur IIS Microsoft NTLM uniquement sur le même ordinateur. Pour héberger un serveur RTSP et un serveur IIS sur le même ordinateur, supprimez le SPN du serveur IIS et utilisez l’authentification NTLM.

## Rubriques connexes


[Planification du déploiement du système Application Virtualization](planning-for-application-virtualization-system-deployment.md)

 

 






---
title: Planification de la sécurité du serveur
description: Planification de la sécurité du serveur
author: dansimp
ms.assetid: c7cd8227-b359-41e7-a8ae-d0d5718a76a2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bea1bd8287a15385200bbfb425ed8e00fbcdb02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806493"
---
# Planification de la sécurité du serveur


Pour renforcer la sécurité d’un environnement, vous devez examiner l’exposition à des menaces potentielles dans l’environnement. Pour garantir la sécurité d’une infrastructure App-V, vous devez utiliser les fonctionnalités de sécurité d’application V spécifiques, ainsi que les pratiques de sécurité et les fonctionnalités de l’infrastructure sous-jacente. La sécurisation de l’infrastructure sous-jacente de services tels que les services Internet (IIS), les services de domaine Active Directory et SQL Server renforce la sécurité globale de votre système d’application-V.

Les paramètres par défaut de l’installation du serveur fournissent le niveau de sécurité le plus élevé. Toutefois, certains composants dépendent de l’infrastructure sous-jacente qui n’est pas configurée dans le cadre de l’installation. Le suivi des étapes après l’installation permet d’améliorer la sécurité de l’infrastructure App-V.

Le répertoire de contenu contient tous les packages à transmettre aux clients. Ces ressources doivent être aussi sécurisées que possible pour éliminer de nombreuses menaces potentielles en matière de sécurité. La liste suivante fournit des recommandations supplémentaires:

-   Publication et/ou diffusion UNC: les autorisations de cet élément doivent être les plus restrictives dans l’environnement. Utilisez les autorisations NTFS pour implémenter les listes de contrôle d’accès (ACL) les plus restrictives pour le répertoire de contenu (utilisateurs = lu, administrateurs = lecture et écriture).

-   Services Internet (IIS) utilisés pour la publication et/ou la diffusion en continu: configurez IIS pour prendre en charge uniquement l’authentification intégrée à Windows Supprimez l’accès anonyme au serveur IIS et restreignez l’accès à l’annuaire avec des autorisations NTFS.

-   RTSP/RTSP vers les packages d’application en flux: configurez la stratégie de fournisseur application-V de façon à ce qu’elle exige une authentification, appliquez les autorisations d’accès et activez uniquement les groupes requis pour avoir accès à la stratégie du fournisseur. Configurez des applications avec les autorisations appropriées dans la base de données.

Limitez le nombre d’utilisateurs dotés de privilèges d’administration à un minimum pour réduire les risques possibles pour les données dans le magasin de données et pour éviter de publier des applications malveillantes dans l’infrastructure.

## Sécurité de la virtualisation des applications


App-V utilise plusieurs méthodes de communication entre les différents composants de l’infrastructure. Lorsque vous planifiez votre infrastructure App-V, la sécurisation des communications entre les serveurs peut limiter les risques en matière de sécurité qui seraient déjà présents sur le réseau existant.

### Magasin de données

Le serveur de gestion des applications et le service de gestion des applications de virtualisation des applications communiquent avec le magasin de données à l’aide d’une connexion SQL via le port TCP 1433. Le serveur de gestion utilise le magasin de données pour récupérer les données d’application et de configuration et il enregistre les informations d’utilisation dans la base de données. Le service de gestion communique avec le magasin de données de la part d’un administrateur qui configure l’infrastructure App-V. Dans la mesure où le magasin de données contient des informations critiques, il est important de limiter les risques pesant sur ces données.

Il est recommandé que les communications entre le serveur de gestion de l’application-V, le service de gestion et le magasin de données soient sécurisées avec la sécurité du protocole Internet (IPsec). En particulier, créez des stratégies permettant de sécuriser le canal de communication entre le magasin de données (SQL) et le serveur de gestion, ainsi que le magasin de données et le service de gestion. Vous pouvez également déployer l’isolation de serveur et de domaine avec IPsec, ce qui garantit que tous les composants d’infrastructure App-V communiquent uniquement avec des canaux sécurisés. Pour plus d’informations sur l’implémentation d’IPsec, consultez la documentation suivante:

-   Pour Windows Server2003, voir <https://go.microsoft.com/fwlink/?LinkId=133226> ( https://go.microsoft.com/fwlink/?LinkId=133226) .

-   Pour Windows Server 2008, voir <https://go.microsoft.com/fwlink/?LinkId=133227> ( https://go.microsoft.com/fwlink/?LinkId=133227) .

### Répertoire de contenu

Dans le cas d’une installation d’un serveur de gestion application-V, l’emplacement du répertoire de contenu est configuré. Ce répertoire est l’emplacement de stockage des packages d’application virtualisé. Cet emplacement peut être local pour le serveur ou placé sur un partage réseau distant. Par conséquent, implémentez IPsec pour sécuriser la communication avec un emplacement distant pour le répertoire de contenu.

Vous pouvez également utiliser un répertoire virtuel sur un serveur IIS pour diffuser des packages aux clients. Si le répertoire virtuel qui est créé pour le contenu se trouve sur une source distante, utilisez IPsec pour sécuriser la communication entre le serveur IIS et l’emplacement de stockage distant.

Le répertoire de contenu contient tous les packages transmis aux clients. Ces ressources doivent être aussi sécurisées que possible pour éliminer de nombreuses menaces potentielles en matière de sécurité.

### Protocoles de sécurité

Vous pouvez utiliser les protocoles RTSP ou HTTPs pour des communications sécurisées améliorées. RTSP est le protocole utilisé par les serveurs App-V et HTTPs est le protocole utilisé par les serveurs IIS. Ces protocoles sont utilisés lors de la publication d’applications du serveur vers le client de bureau de la virtualisation des applications. Après avoir déterminé le protocole souhaité, ajoutez un serveur de publication qui utilise ce protocole.

### <a href="" id="configuring-app-v-servers-for-rtsps-"></a>Configuration de serveurs App-V pour RTSP

Pour utiliser la sécurité améliorée (par exemple, TLS), l’installation ou la configuration d’un serveur de gestion d’applications-V ou d’un serveur en flux continu pour une utilisation améliorée (TLS, par exemple) nécessite le mise en service du serveur App-V. Lorsque vous préparez l’installation ou la configuration de la sécurité d’un serveur, vous devez répondre à des exigences spécifiques. La configuration requise pour le déploiement et la configuration de certificats pour un serveur de gestion ou un serveur de flux d’applications plus sécurisé comprend les éléments suivants:

-   Le certificat doit être valide. Dans le cas contraire, le client arrête la connexion.

-   Le certificat doit contenir l’utilisation améliorée de la clé (EKU)-Server Authentication (OID 1.3.6.1.5.5.7.3.1). Dans le cas contraire, le client arrête la connexion.

-   Le nom de domaine complet (FQDN) du certificat doit correspondre au serveur sur lequel il est installé. Par exemple, si le client appelle `RTSPS://Myserver.mycompany.com/content/MyApp.sft` , mais que le champ certificat **délivré à** contient `Myserver1.mycompany.com` , le client ne se connecte pas au serveur et la session est arrêtée, même si `Myserver.mycompany.com` elle est `Myserver1.mycompany.com` résolue en une même adresse IP.

    **Remarques**  Si vous utilisez App-V dans un cluster à équilibrage de charge réseau, le certificat doit être configuré avec des *noms secondaires* de l’objet pour prendre en charge les RTSP. Pour plus d’informations sur la configuration de l’autorité de certification et la création de certificats avec des réseaux SAN, voir <https://go.microsoft.com/fwlink/?LinkId=133228> ( https://go.microsoft.com/fwlink/?LinkId=133228) .

     

-   L’autorité de certification émettant le certificat sur le serveur App-V doit être approuvée par le client qui se connecte au serveur. Dans le cas contraire, le client arrête la connexion.

-   Vous devez modifier les autorisations pour la *clé privée du certificat* afin d’autoriser l’accès par le service Server App-V. Par défaut, le serveur de gestion de l’application et les services de serveur en continu s’exécutent sous le compte de service réseau. Lors de la génération d’une #10 PKCS \ sur le serveur, une clé privée est créée. Seuls les groupes système local et administrateurs ont accès à cette clé. Ces ACL par défaut empêchent l’application du serveur App-V d’accepter des connexions sécurisées.

    **Remarques**  Pour plus d’informations sur la configuration d’une infrastructure à clé publique (PKI), voir <https://go.microsoft.com/fwlink/?LinkId=133229> ( https://go.microsoft.com/fwlink/?LinkId=133229) .

     

### Configuration de serveurs IIS avec HTTPs

App-V peut utiliser les serveurs IIS dans certaines configurations d’infrastructure. Pour plus d’informations sur la configuration des serveurs IIS, voir <https://go.microsoft.com/fwlink/?LinkId=133230> ( https://go.microsoft.com/fwlink/?LinkId=133230) .

**Remarques**  Si vous utilisez IIS pour publier les fichiers ICO et OSD, configurez un type MIME pour OSD = TXT; dans le cas contraire, les services Internet (IIS) ne peuvent pas utiliser les fichiers ICO et OSD pour les clients.

 

### Sécurité au niveau de l’application

Vous pouvez configurer les serveurs pour diffuser des applications spécifiques sur le Bureau d’un utilisateur. Toutefois, l’autorisation d’accès est réellement accordée au niveau du package et non au niveau de l’application. Même si une application spécifique ne peut pas être publiée sur le Bureau de l’utilisateur, si celle-ci est autorisée à ajouter des applications ou est un administrateur sur l’ordinateur client, l’utilisateur peut créer et utiliser un raccourci sur le client pour exécuter toutes les applications d’un package.

## Configuration de l'administration d'App-V pour les environnements distribués


Lors de la conception de l’infrastructure pour votre organisation spécifique, vous pouvez installer le service Web d’administration des applications sur un ordinateur autre que celui sur lequel vous installez le serveur de gestion des applications-V. Voici quelques raisons courantes de séparation de ces composants d’application-V:

-   Niveau de performance

-   Fiabilité

-   Disponibilité

-   Extensibilité

Pour que l’infrastructure fonctionne correctement, la séparation de la console de gestion App-V, du serveur de gestion et du service Web de gestion nécessite une configuration supplémentaire. Pour plus d’informations sur la configuration du serveur, voir [Comment configurer le serveur pour être approuvé pour la délégation](how-to-configure-the-server-to-be-trusted-for-delegation.md).

## Rubriques connexes


[Planification de la sécurité et de la protection](planning-for-security-and-protection.md)

 

 






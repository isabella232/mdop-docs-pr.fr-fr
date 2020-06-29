---
title: Planification de la sécurité du client
description: Planification de la sécurité du client
author: dansimp
ms.assetid: 4840a60f-4c91-489c-ad0b-6671882abf9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0038f7cbc8592d6c7fcdfa485111da88c17791d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806505"
---
# Planification de la sécurité du client


Le client App-V fournit plusieurs améliorations en matière de sécurité qui n’ont pas été présentes dans les versions précédentes du produit. Ces modifications fournissent une sécurité améliorée après l’installation et la configuration ultérieure des paramètres du client. Cette rubrique décrit certaines de ces améliorations et identifie plusieurs paramètres de configuration importants liés à la sécurité que vous devez prendre en compte lors de votre processus de planification. Il est important de garder à l’esprit que les applications virtuelles sont toujours exécutables et que vous devez vous assurer que ces ressources ne peuvent pas être falsifiées par des personnes non autorisées. C’est la raison pour laquelle le cache de fichiers Open Software Descriptor (OSD) est protégé comme décrit plus loin dans cette rubrique et nous vous recommandons vivement d’utiliser les protocoles RTSP, HTTPs et IPsec pour protéger la publication et le streaming.

## Sécurité du client App-V


Par défaut, lors de l’installation, le client App-V est configuré avec les autorisations minimales requises pour permettre à un utilisateur d’effectuer une actualisation de publication et de lancer des applications. D’autres améliorations apportées à la sécurité fournies dans le client App-V incluent les éléments suivants:

-   Par défaut, le cache de fichiers OSD peut être mis à jour uniquement par les administrateurs et à l’aide du processus d’actualisation de publication.

-   Le fichier journal (sftlog.txt) est accessible uniquement par les comptes disposant d’un accès administratif local au client.

-   La taille du fichier journal est désormais maximale.

### Associations de types de fichiers

Par défaut, l’installation du client inscrit les associations de types de fichier (FTAs) pour les fichiers OSD, qui permet aux utilisateurs de démarrer des applications directement à partir de fichiers OSD au lieu des raccourcis publiés. Si un utilisateur disposant de droits d’administrateur local reçoit un fichier OSD contenant du code malveillant, que ce soit par courrier électronique ou téléchargé à partir d’un site Web, l’utilisateur peut ouvrir le fichier OSD et lancer l’application même si le client a été configuré pour restreindre l’autorisation d' **Ajout d’applications** . Vous pouvez annuler l’enregistrement de FTAs pour l’OSD pour réduire ce risque. Envisagez également de bloquer cette extension dans le système de courrier et dans le pare-feu. Pour plus d’informations sur la configuration d’Outlook pour bloquer les extensions, voir <https://go.microsoft.com/fwlink/?LinkId=133278> .

**Note de sécurité:**

À partir de l’app-version 4.6, l’Association de type de fichier n’est plus créée pour les fichiers OSD lors d’une nouvelle installation du client, bien que les paramètres existants soient conservés lors d’une mise à niveau à partir de la version 4,2 ou 4,5 du client App-V. Si pour une raison quelconque, il est essentiel de créer l’Association de type de fichier, vous pouvez créer les clés de Registre suivantes et définir leurs valeurs comme suit:

    Create HKEY\_CLASSES\_ROOT\\.osd with a default value of SoftGrid.osd.File

    Under HKEY\_LOCAL\_MACHINE\\software\\classes\\Softgrid.osd.file, create a string value named AppUserModelID with a data value of Microsoft.AppV.Client.Tray

### Authorization

Lors de l’installation, vous pouvez utiliser le paramètre **RequireAuthorizationIfCached** pour configurer le client de telle sorte qu’il exige une autorisation du serveur lorsque l’utilisateur tente de démarrer une application. Prenez soin de définir ce paramètre. Si le serveur App-V n’est pas disponible pour une raison quelconque, l’application utilise l’État stocké le plus récent de ce paramètre pour contrôler l’accès de l’utilisateur à l’application. Si l’utilisateur n’a pas démarré l’application correctement avant que le serveur App-V ne soit plus disponible, elle ne pourra pas lancer l’application tant qu’elle ne peut pas communiquer avec le serveur et recevoir une autorisation. Toutefois, si vous définissez le paramètre de sorte que le client n’exige pas l’autorisation et si le serveur n’est pas disponible, toutes les applications précédemment mises en cache peuvent être démarrées, le cas échéant. Par ailleurs, si l’utilisateur est autorisé à modifier le mode hors connexion par le biais des autorisations ou s’il s’agit d’un administrateur local, il peut ouvrir tous les packages mis en cache comme si l’infrastructure App-V n’était pas disponible.

### Analyse antivirus

Un logiciel antivirus exécuté sur un ordinateur client App-V peut détecter et signaler un fichier infecté dans l’environnement virtuel. Toutefois, il ne peut pas désinfecter le fichier. Si un virus est détecté dans l’environnement virtuel, le logiciel antivirus effectue l’opération de mise en quarantaine ou de réparation dans le cache, et non dans le package actuel. Configurez le logiciel antivirus à l’aide d’une exception pour le fichier Sftfs. FSD. Ce fichier est le fichier cache qui stocke les packages sur le client App-V.

**Note de sécurité:**

Si un virus est détecté dans une application ou un package déployé dans l’environnement de production, remplacez l’application ou le package par une version sans virus.

## Communication entre le client et le serveur


Les actualisations de publication et le flux de package sont également des domaines dans lesquels les considérations en matière de sécurité relatives aux communications client-serveur sont importantes.

### Actualisation de la publication

Lorsque le client communique avec le serveur pour effectuer une actualisation de publication, il utilise les informations d’identification de l’utilisateur connecté pour demander des informations sur les packages d’application. Nous vous conseillons de sécuriser la communication entre le client App-V et le serveur de gestion App-V pour vous assurer qu’aucune des informations de publication ne peut être falsifiée lors du transit. Pour ce faire, vous devez utiliser l’option de sécurité améliorée, qui utilisera RTSP/HTTPs. La communication entre le client et l’emplacement de stockage des fichiers. ICO et OSD doit utiliser IPsec pour les partages SMB/CIFS et HTTPs pour un serveur IIS.

**Remarques**  Si vous utilisez IIS pour publier les fichiers ICO et OSD, configurez un type MIME pour OSD = TXT; dans le cas contraire, les services Internet (IIS) ne peuvent pas utiliser les fichiers ICO et OSD pour les clients.

 

### Streaming de package

Lorsqu’un utilisateur lance une application pour la première fois ou que des paramètres de chargement automatique ont été définis sur le client, le package d’application est transmis à partir d’un serveur vers le cache client. Ce processus prend en charge les protocoles RTSP/RTSP, HTTP/HTTPs et SMB/CIFS. Les fichiers OSD contrôlent les protocoles utilisés, sauf si le paramètre **APPLICATIONSOURCEROOT** ou **OVERRIDEURL** a été configuré sur les clients. Vous devez configurer la communication sur RTSP, HTTPs ou IPsec pour SMB/CIFS afin d’obtenir des niveaux de sécurité plus élevés. Pour plus d’informations sur le choix de la méthode de communication à utiliser, voir le Guide de planification et de déploiement de l’application V à l’adresse <https://go.microsoft.com/fwlink/?LinkId=122063> .

**Remarques**  Si vous utilisez les services Internet pour publier des packages (fichiers SFT), configurez un type MIME pour SFT = Binary; dans le cas contraire, IIS refusera d’utiliser les fichiers SFT pour les clients.

 

### Profils itinérants et redirection de dossiers

Le système App-V enregistre les modifications spécifiques à l’utilisateur apportées aux packages dans le usrvol \ _sftfs \ _v1. pkg. Ce fichier se trouve dans le dossier Application Data du profil d’un utilisateur. Dans la mesure où le profil ou un dossier de données d’application redirigées est transféré entre le client et le serveur, utilisez IPsec pour sécuriser la communication.

## Considérations relatives aux clients Internet


Pour les clients Internet, il est important de savoir si le client est joint à un domaine ou qu’il n’est pas un domaine.

### Client joint au domaine

Par défaut, les clients App-V utilisent les tickets Kerberos émis par les services de domaine Active Directory pour l’authentification et l’autorisation sur l’intranet. Ce ticket Kerberos est valide pendant 10 heures par défaut. Le client utilisera ce ticket pour accéder au serveur App-V tant que le ticket est valide, même si l’ordinateur n’est pas en mesure de se connecter au contrôleur de domaine pour actualiser le ticket. Si le ticket Kerberos expire, le client App-V rétablit l’authentification NTLM et utilise les informations d’identification mises en cache de l’utilisateur.

### Client non associé au domaine

S’il s’agit d’un utilisateur domestique et que l’ordinateur n’est pas joint au domaine de l’entreprise, l’application-V peut toujours prendre en charge la livraison d’applications. Pour authentifier et autoriser un utilisateur à procéder à une actualisation de publication et à démarrer des applications, configurez le compte d’utilisateur sur l’ordinateur client de manière à stocker le nom d’utilisateur et le mot de passe ayant accès à l’environnement App-V, puis fournissez les autorisations appropriées aux applications.

## Rubriques connexes


[Planification de la sécurité et de la protection](planning-for-security-and-protection.md)

 

 






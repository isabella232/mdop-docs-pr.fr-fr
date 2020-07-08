---
title: Présentation du scénario basé sur une distribution électronique de logiciels
description: Présentation du scénario basé sur une distribution électronique de logiciels
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808850"
---
# Présentation du scénario basé sur une distribution électronique de logiciels


Si vous envisagez d’utiliser une solution de distribution de logiciel électronique (ESD) pour déployer des applications virtuelles, il est important de bien comprendre les facteurs qui entrent en vigueur ou qui sont affectés par cette décision. Cette rubrique décrit les avantages liés à l’utilisation d’un scénario de type ESD et fournit des informations sur les méthodes de publication et de flux de package que vous devez prendre en compte lors de votre déploiement.

**Important**  Quelle que soit la solution ESD utilisée, vous devez être familiarisé avec les exigences de votre solution particulière. Si vous utilisez Microsoft Endpoint Configuration Manager, consultez la documentation de Configuration Manager à l’adresse <https://go.microsoft.com/fwlink/?LinkId=66999> .

 

L’utilisation d’un système de gestion des opérations ESD existant vous offre les avantages suivants:

-   Elimine les infrastructures à double gestion

-   Réduit le coût de votre matériel supplémentaire

-   Réduit le coût des licences de systèmes d’exploitation et de bases de données supplémentaires

## Méthodes de publication


Lors de l’utilisation d’un scénario de type ESD, vous avez le choix entre les options suivantes pour publier l’application sur les clients:

-   **Programme d’installation Windows autonome.** Le fichier du programme d’installation Windows contient le manifeste ainsi que les fichiers OSD et ICO utilisés par les clients pour configurer un package. Le fichier Windows Installer copie également le fichier SFT sur le client, car ce scénario n’utilise pas de serveur.

-   **Windows Installer avec le manifeste du package.** Le fichier du programme d’installation Windows contient le manifeste ainsi que les fichiers OSD et ICO utilisés par les clients pour configurer un package. Le fichier SFT est stocké sur un serveur. Un paramètre de ligne de commande dirige le client vers l’emplacement du fichier SFT.

-   **Commandes SFTMIME.** Les commandes SFTMIME sont utilisées avec les fichiers Manifest, OSD, ICO et SFT pour ajouter des packages au client. Le fichier manifeste doit être disponible sur l’ordinateur client ou être accessible par le biais d’un chemin UNC. En fonction de la configuration du client et des options de ligne de commande, les fichiers OSD, ICO et SFT peuvent être situés sur l’ordinateur client ou sur un serveur.

Pour plus d’informations sur les méthodes de publication précédentes, voir [déterminer votre méthode de publication](determine-your-publishing-method.md).

## Méthodes de diffusion de package


Vous devez déterminer la méthode utilisée par votre système de virtualisation d’application pour diffuser en continu les packages d’application virtuelle ou les fichiers SFT du serveur aux clients. Les options de streaming suivantes sont disponibles:

-   **Serveur de diffusion en continu d’applications.** Si vous utilisez un serveur de diffusion en continu d’applications dans votre configuration, les fichiers SFT sont transmis aux clients à partir de ce serveur à l’aide de protocoles RTSP ou RTSP. Pour installer le logiciel serveur sur un ordinateur, vous devez le configurer par le biais du Registre, mais cette configuration ne dépend pas de services tels que SQL ou services de domaine Active Directory. Les fichiers SFT sont stockés sur le serveur à un emplacement accessible aux clients. Les informations de publication peuvent être distribuées aux clients via tout mécanisme de distribution. Néanmoins, lors de la configuration, le client reçoit les mises à jour de package automatiquement et la mise à niveau active est prise en charge.

-   **Serveur de gestion des applications.** Si vous utilisez un serveur de gestion d’application de la virtualisation dans votre configuration, les fichiers SFT sont transmis aux clients à partir de ce serveur à l’aide de protocoles RTSP ou RTSP. Pour gérer ce serveur, vous devez utiliser la console de gestion Application Virtualization. Cette configuration utilise une base de données SQL et des services Active Directory. Le serveur peut distribuer des informations de publication aux clients afin de ne pas avoir besoin de mécanismes de publication supplémentaires.

-   **Serveur de fichiers.** Si vous utilisez un serveur de fichiers dans votre configuration, les fichiers SFT sont transmis à l’aide de protocoles SMB. Pour gérer les serveurs de fichiers utilisés dans cette configuration, vous devez créer des listes de contrôle d’accès (ACL) sur le partage de fichiers et des fichiers SFT. Il est nécessaire de rediriger les clients vers les fichiers appropriés sur le serveur de fichiers.

-   **Serveur IIS.** Si vous utilisez un serveur IIS dans votre configuration, les fichiers SFT sont transmis aux clients à partir de ce serveur à l’aide de protocoles HTTP ou HTTPs. Le serveur IIS est facile à configurer et à gérer. Il est nécessaire de rediriger les clients vers les fichiers appropriés sur le serveur IIS.

Pour plus d’informations sur les méthodes de streaming précédentes, voir [déterminer la méthode de diffusion en continu](determine-your-streaming-method.md).

## Rubriques connexes


[Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client](application-virtualization-client-installer-command-line-parameters.md)

[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Choisir une méthode de publication](determine-your-publishing-method.md)

[Choisir une méthode de diffusion en continu](determine-your-streaming-method.md)

[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 






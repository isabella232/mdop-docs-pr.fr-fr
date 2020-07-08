---
title: Procédure pour configurer les serveurs Application Virtualization Streaming Server
description: Procédure pour configurer les serveurs Application Virtualization Streaming Server
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807261"
---
# Procédure pour configurer les serveurs Application Virtualization Streaming Server


Pour que les applications virtuelles puissent être diffusées sur le client de bureau de la virtualisation des applications ou sur le client pour les services Bureau à distance, Lorsque vous configurez les serveurs, vous configurez le *Répertoire de contenu* dans lequel les fichiers SFT sont chargés et stockés. Les fichiers SFT contiennent les applications virtuelles (ou applications).

**Important**  Les serveurs de virtualisation des applications diffusent des fichiers SFT au client de bureau et au client pour les services Bureau à distance en utilisant uniquement les protocoles RTSP ou RTSP. Il est possible de configurer le fichier ICO (icône) et l’OSD (Open Software Descriptor) sur un autre fichier ou serveur HTTP.

 

**Pour configurer les serveurs de streaming de la virtualisation des applications**

1.  Terminez la procédure d’installation du serveur de diffusion de contenu de l’application. Au cours de la procédure d’installation, vous spécifiez l’emplacement du répertoire \\Content sur l’écran de **chemin d’accès** .

2.  Naviguez jusqu’à l’emplacement que vous avez spécifié pour le répertoire \\Content et, si nécessaire, créez le répertoire.

3.  Lorsque le répertoire de contenu est créé, configurez-le en tant que partage de fichiers standard.

4.  Configurez les autorisations du système de fichiers NTFS sur le répertoire de contenu et les dossiers du package sous le répertoire de contenu. Dans les services de domaine Active Directory, vous devez utiliser des groupes de sécurité qui définissent les utilisateurs qui peuvent accéder à chaque application.

## Rubriques connexes


[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Procédure pour configurer les serveurs Application Virtualization Management Server](how-to-configure-the-application-virtualization-management-servers.md)

[Procédure pour configurer le serveur de fichiers](how-to-configure-the-file-server.md)

[Procédure pour configurer le serveur IIS](how-to-configure-the-server-for-iis.md)

 

 






---
title: Configuration du pare-feu pour les serveurs App-V Server
description: Configuration du pare-feu pour les serveurs App-V Server
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808982"
---
# Configuration du pare-feu pour les serveurs App-V Server


Après l’installation de Microsoft Application Virtualization (App-V) Server Management Server ou de Streaming Server et de sa configuration pour utiliser le protocole RTSP ou RTSP, vous devez créer des exceptions de pare-feu pour les programmes App-V.

## Configuration des exceptions de pare-feu pour le serveur de gestion de la virtualisation des applications


Créez une exception de pare-feu pour **sghwdsptr.exe** et **sghwsvr.exe**. Ces programmes se trouvent dans le dossier C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin sur un système d’exploitation 32 bits. Si vous utilisez une version de système d’exploitation 64 bits, le dossier se trouve sous C:\\Program Files (x86) \\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.

## Configuration des exceptions de pare-feu pour le serveur de diffusion de la virtualisation des applications


Créez une exception de pare-feu pour **sglwdsptr.exe** et **sglwsvr.exe**. Ces programmes se trouvent dans le dossier C:\\Program Files\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin sur un système d’exploitation 32 bits. Si vous utilisez une version de système d’exploitation 64 bits, le dossier se trouve sous C:\\Program Files (x86) \\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.

## Rubriques connexes


[Procédure pour configurer des serveurs pour un déploiement basé sur un serveur](how-to-configure-servers-for-server-based-deployment.md)

[Procédure pour installer et configurer l'application par défaut](how-to-install-and-configure-the-default-application.md)

 

 






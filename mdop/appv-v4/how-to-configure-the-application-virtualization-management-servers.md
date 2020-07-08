---
title: Procédure pour configurer les serveurs Application Virtualization Management Server
description: Procédure pour configurer les serveurs Application Virtualization Management Server
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807269"
---
# Procédure pour configurer les serveurs Application Virtualization Management Server


Pour que les applications virtuelles puissent être diffusées sur le client de bureau de la virtualisation des applications ou sur le client pour les services Bureau à distance (auparavant services Terminal Server), le serveur de gestion des applications doit être configuré. Lorsque vous configurez le serveur, vous configurez le *Répertoire de contenu* dans lequel les fichiers SFT sont chargés et stockés. Les fichiers SFT contiennent l’application virtualisée (ou les applications).

**Important**  Les serveurs de virtualisation des applications diffusent des fichiers SFT au client de bureau et au client pour les services Bureau à distance en utilisant uniquement les protocoles RTSP ou RTSP. Il est possible de configurer le fichier ICO (icône) et l’OSD (Open Software Descriptor) sur un autre fichier ou serveur HTTP.

 

**Pour configurer le serveur de gestion de la virtualisation des applications**

1.  Procédez comme suit:

    [Procédure pour installer le serveur Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

    **Remarques**  Au cours de la procédure d’installation, vous spécifiez l’emplacement du répertoire \\Content sur l’écran de **chemin d’accès** .

     

2.  Naviguez jusqu’à l’emplacement que vous avez spécifié pour le répertoire \\Content et, si nécessaire, créez le répertoire.

3.  Lorsque le répertoire de contenu est créé, configurez-le en tant que partage de fichiers standard.

## Rubriques connexes


[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Configuration système requise pour Application Virtualization](application-virtualization-system-requirements.md)

[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Procédure pour configurer des serveurs pour un déploiement basé sur un serveur](how-to-configure-servers-for-server-based-deployment.md)

 

 






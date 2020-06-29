---
title: Procédure pour configurer le serveur de fichiers
description: Procédure pour configurer le serveur de fichiers
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807245"
---
# Procédure pour configurer le serveur de fichiers


Vous pouvez suivre la procédure ci-dessous pour configurer un ordinateur local utilisé en tant que partage de fichier et flux d’applications sur le client de bureau de virtualisation des applications et sur le client pour les services Bureau à distance. Ce scénario est utilisé lorsque vous ne souhaitez pas ajouter d’infrastructure serveur supplémentaire à votre environnement matériel existant.

Si vous utilisez un serveur de gestion de la virtualisation des applications comme point de distribution sur le partage de fichiers installé dans les bureaux locaux, vous devez configurer ce serveur pour que les applications virtuelles puissent être diffusées sur les ordinateurs utilisés comme partages de fichiers. Lorsque vous configurez les serveurs et les partages de fichiers, vous configurez le répertoire de contenu dans lequel les fichiers SFT sont chargés et stockés. Les fichiers SFT contiennent les applications virtuelles (ou applications).

**Important**  Pour que les applications soient correctement diffusées sur le client de bureau de la virtualisation des applications et sur le client pour les services Bureau à distance, le flux de fichiers SFT provient du répertoire de contenu du serveur sur lequel vous stockez l’application virtuelle; le fichier ICO (Icon) et l’OSD (Open Software Descriptor) peuvent être configurés pour être diffusés en continu sur un autre serveur.

 

**Pour configurer le serveur de fichiers de virtualisation des applications**

1.  Procédez de la manière décrite ci-dessous pour configurer le serveur utilisé comme point de distribution:

    [Procédure pour installer le serveur Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

    **Remarques**  Au cours de la procédure d’installation, vous spécifiez l’emplacement du répertoire \\Content sur l’écran de **chemin d’accès** .

     

2.  Créez un répertoire \\Content qui correspond à l’annuaire que vous avez spécifié lors de l’installation du serveur, sur chaque ordinateur que vous utilisez en tant que partage de fichiers.

    **Important**  Configurez les clients de bureau de la virtualisation des applications pour diffuser en continu des applications à partir de l’ordinateur que vous utilisez en tant que partage de fichiers plutôt que d’un serveur de virtualisation des applications ou d’un serveur IIS.

     

3.  Lorsque le répertoire \\Content est créé, configurez-le en tant que partage de fichiers standard.

## Rubriques connexes


[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Procédure pour configurer les serveurs Application Virtualization Management Server](how-to-configure-the-application-virtualization-management-servers.md)

[Procédure pour configurer les serveurs Application Virtualization Streaming Server](how-to-configure-the-application-virtualization-streaming-servers.md)

[Procédure pour configurer le serveur IIS](how-to-configure-the-server-for-iis.md)

 

 






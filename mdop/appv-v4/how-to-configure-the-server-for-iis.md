---
title: Procédure pour configurer le serveur IIS
description: Procédure pour configurer le serveur IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807229"
---
# Procédure pour configurer le serveur IIS


Pour que les applications virtuelles puissent être diffusées sur le client de bureau de la virtualisation des applications et sur le client pour les services Bureau à distance (auparavant services Terminal Server), les serveurs IIS doivent être configurés. Lorsque vous configurez les serveurs, vous configurez le répertoire de contenu dans lequel les fichiers SFT sont chargés et stockés. Les fichiers SFT contiennent les applications virtuelles (ou applications).

**Pour configurer le répertoire de contenu sur le serveur IIS**

1.  Sur le serveur exécutant IIS, recherchez le répertoire que vous souhaitez utiliser comme répertoire de contenu ou créez le répertoire s’il n’existe pas. Configurer ce répertoire comme partage de fichiers standard.

2.  Sur le serveur exécutant IIS, ouvrez le **Gestionnaire des services Internet (IIS)**, puis, sous le site Web par défaut, créez un répertoire virtuel correspondant au répertoire de contenu que vous avez créé sur le serveur. Assurez-vous que la case à cocher **lecture** est activée.

3.  Donnez au répertoire virtuel nouvellement créé le **contenu**de l’alias.

4.  Acceptez tous les autres paramètres par défaut pour ce répertoire virtuel.

5.  Configurez les autorisations du système de fichiers NTFS sur le répertoire de contenu et les dossiers du package sous le répertoire de contenu à l’aide des groupes de sécurité dans les services de domaine Active Directory définis précédemment.

**Remarques**  Si vous utilisez IIS pour publier les fichiers ICO et OSD, vous devez configurer un type MIME pour OSD = TXT; dans le cas contraire, il n’utilisera pas les fichiers ICO et OSD pour les clients. Si vous utilisez les services Internet pour publier des packages (fichiers SFT), vous devez configurer un type MIME pour SFT = Binary; dans le cas contraire, IIS ne servira pas les fichiers SFT aux clients.

 

## Rubriques connexes


[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Procédure pour configurer les serveurs Application Virtualization Management Server](how-to-configure-the-application-virtualization-management-servers.md)

[Procédure pour configurer les serveurs Application Virtualization Streaming Server](how-to-configure-the-application-virtualization-streaming-servers.md)

[Procédure pour configurer le serveur de fichiers](how-to-configure-the-file-server.md)

 

 






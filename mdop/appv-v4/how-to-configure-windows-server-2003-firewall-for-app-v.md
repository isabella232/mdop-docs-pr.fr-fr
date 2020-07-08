---
title: Procédure pour configurer le Pare-feu Windows Server2003 pour App-V
description: Procédure pour configurer le Pare-feu Windows Server2003 pour App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807222"
---
# Procédure pour configurer le Pare-feu Windows Server2003 pour App-V


Suivez la procédure ci-dessous pour configurer le pare-feu windowsserver2003 2003 pour App-V.

**Pour configurer le pare-feu de windowsserver2003 2003 pour App-V**

1.  Dans le **panneau de configuration**, ouvrez le **pare-feu Windows**.

    **Remarques**  Si le serveur n’a pas été configuré pour exécuter le service de pare-feu avant cette étape, vous serez invité à démarrer le service de pare-feu.

     

2.  Si les fichiers ICO et OSD sont publiés via SMB, assurez-vous que le **partage de fichiers et d’imprimantes** est activé sous l’onglet **exceptions** .

    **Remarques**  Si des fichiers. ICO et OSD sont publiés par le biais du protocole HTTP/HTTPs sur le serveur de gestion, vous devrez peut-être ajouter une exception pour HTTP ou HTTPs. Si le serveur IIS hébergeant les fichiers ICO et OSD est hébergé sur un ordinateur distinct du serveur de gestion, vous devez ajouter l’exception à cet ordinateur. Pour optimiser les performances, nous vous recommandons d’héberger les fichiers ICO et OSD sur un serveur distinct à partir du serveur de gestion.

     

3.  Ajoutez une exception de programme pour `sghwdsptr.exe` , qui est le fichier exécutable du service du serveur de gestion. Le chemin d’accès par défaut à cet exécutable est `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

    **Remarques**  Si le serveur de gestion utilise RTSP pour la communication, vous devez également ajouter une exception de programme pour `sghwsvr.exe` .

    Le serveur de streaming App-V nécessite une exception `sglwdsptr.exe` de programme pour la communication RTSP. Le serveur de streaming App-V qui utilise RTSP pour la communication nécessite également une exception de programme pour `sglwsvr.exe` .

     

4.  Assurez-vous que l’étendue correcte est configurée pour chaque exception. Pour réduire les risques, supprimez tous les ordinateurs et limitez strictement les adresses IP auxquelles le serveur répond.

## Rubriques connexes


[Procédure pour configurer le Pare-feu Windows Server2008 pour App-V](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 






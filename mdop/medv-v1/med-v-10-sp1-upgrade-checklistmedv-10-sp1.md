---
title: Liste de contrôle pour la mise à niveau de MED-V1.0 SP1
description: Liste de contrôle pour la mise à niveau de MED-V1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812252"
---
# Liste de contrôle pour la mise à niveau de MED-V1.0 SP1


Pour procéder à la mise à niveau de Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 vers MED-V 1.0 Service Pack1 (SP1), le client doit être mis à niveau. Le serveur peut éventuellement être mis à niveau.

## Mise à niveau du serveur


**Pour mettre à niveau le serveur MED-V 1.0 vers MED-V 1.0 SP1**

1.  Sauvegardez les fichiers suivants situés dans le répertoire * &lt; INSTALLDIR &gt; /Servers/ConfigurationServer* :

    -   OrganizationalPolicy.XML

    -   ClientPolicy.XML

    -   WorkspaceKeys.XML

2.  Sauvegardez le fichier * &lt; INSTALLDIR &gt; /serveurs/ServerSettings.xml* .

3.  Désinstaller le serveur MED-V 1.0.

4.  Installez le serveur de MED-V 1.0 SP1.

5.  Restaurez les fichiers de sauvegarde dans les répertoires appropriés.

6.  Redémarrez le service du serveur MED-V.

**Remarques**  Si la configuration de serveur a changé par défaut, les fichiers peuvent être stockés à un autre emplacement.

 

## Mise à niveau du client


Pour mettre à niveau le client MED-V 1.0 vers MED-V 1.0 SP1, installez le fichier. msp sur un client MED-V 1.0. Le client et MED-V sont automatiquement mis à niveau.

 

 






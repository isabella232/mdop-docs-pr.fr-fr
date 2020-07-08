---
title: Procédure pour configurer le client pour la prise en charge du domaine MIT Kerberos
description: Procédure pour configurer le client pour la prise en charge du domaine MIT Kerberos
author: dansimp
ms.assetid: 46102f4c-270c-4115-8eb4-7ff5ae3be32d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ae5cd73d00f340bc50070fdd0a5fd3e038cc3789
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807257"
---
# Procédure pour configurer le client pour la prise en charge du domaine MIT Kerberos


Dans Application Virtualization (App-V) 4,5 SP1, la prise en charge des domaines Kerberos MIT est ajoutée. Cette rubrique fournit des informations détaillées sur l’activation de cette assistance.

**Pour activer la prise en charge des domaines Kerberos MIT**

-   Créez une nouvelle clé de Registre nommée **UseMitKerberos** de type DWORD, comme suit, puis définissez-la sur la valeur 1.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos

 

 






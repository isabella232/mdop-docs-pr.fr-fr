---
title: Informations pour résoudre les problèmes liés au serveur Application Virtualization Server
description: Informations pour résoudre les problèmes liés au serveur Application Virtualization Server
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806206"
---
# Informations pour résoudre les problèmes liés au serveur Application Virtualization Server


Cette rubrique contient des informations que vous pouvez utiliser pour résoudre divers problèmes sur les serveurs de virtualisation des applications (App-V).

## Message d’avertissement 25017 dans le journal d’installation après l’installation du serveur


Le message suivant peut apparaître dans le journal de configuration du serveur après l’installation.

*Avertissement 25017. Le programme d’installation n’a pas pu créer l’objet marqueur Active Directory pour le serveur. Le compte utilisé pour l’installation ne disposait pas des droits suffisants pour écrire dans Active Directory ou Active Directory n’était pas disponible.*

Le programme d’installation de l’application-V ou du programme d’installation de serveur en continu crée une entrée de point de connexion de service sous l’objet ordinateur dans les services de domaine Active Directory (AD DS) qui correspond à l’ordinateur sur lequel le serveur est installé, si le compte utilisé pour exécuter le programme d’installation dispose des droits appropriés. L’impossibilité de créer cette entrée n’entraînera pas l’échec de l’installation, sans conséquence du fonctionnement du produit. La cause probable de tout échec réside dans le fait que le compte d’utilisateur utilisé pour exécuter l’installation ne dispose pas des droits suffisants pour écrire dans ADDS. Même si l’inscription du serveur App-V dans ADDS est facultative, l’un des avantages d’une telle action est d’activer les outils de gestion centralisés pour localiser le serveur App-V à des fins d’inventaire et de gestion.

## Rubriques connexes


[Application Virtualization Server](application-virtualization-server.md)

 

 






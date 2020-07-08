---
title: Configuration d'App-V pour l'administration sécurisée
description: Configuration d'App-V pour l'administration sécurisée
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809035"
---
# Configuration d'App-V pour l'administration sécurisée


Dans un environnement où les opérations d’administration sécurisées sont importantes, App-V autorise une communication sécurisée entre le service de gestion des applications Web de l’application et la console de gestion de l’application-V. Étant donné que le service de gestion est une application basée sur le Web, il est nécessaire de sécuriser l’application serveur de gestion des applications sur le serveur Web qui héberge le service de gestion. Comme le montre l’illustration suivante, ce processus inclut l’utilisation de HTTPs pour la communication et la configuration du serveur IIS pour autoriser uniquement l’authentification intégrée à Windows.

![configuration du réseau de service Web de l’application v](images/appvmgmtwebservice.gif)

Le service de gestion des applications Web App-V est installé en tant qu’application Web sur IIS. Pour que le service de gestion des sites Web prenne en charge les connexions sécurisées (SSL) entre la console de gestion des applications et le service de gestion des sites Web, vous devez configurer le serveur IIS sur lequel le service de gestion des sites Web est installé et configurer la console de gestion des applications V.

## Dans cette section


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Configuration de certificats pour prendre en charge le service de gestion Web App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Fournit des informations utiles sur la configuration des certificats pour la prise en charge des connexions SSL, pour vous aider à sécuriser la communication pour le service de gestion des applications Web App-V.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[Comment installer et configurer App-V Management Console pour un environnement plus sécurisé](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Fournit une procédure pas à pas de connexion à un service de gestion des applications Web App-V via une connexion sécurisée.

 

 






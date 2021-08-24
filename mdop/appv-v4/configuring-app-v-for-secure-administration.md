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
ms.openlocfilehash: c95fab4b2b4f402df4ff0f82f2f346c9bd226e00
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910479"
---
# <a name="configuring-app-v-for-secure-administration"></a>Configuration d'App-V pour l'administration sécurisée


Dans un environnement où la sécurisation des opérations d’administration est importante, App-V permet une communication sécurisée entre le service de gestion Web App-V et la console de gestion App-V. Étant donné que le service de gestion est une application Web, il requiert la sécurisation de l’application App-V Management Server sur le serveur Web qui héberge le service de gestion. Comme indiqué dans l’illustration suivante, ce processus inclut l’utilisation du protocole HTTPS pour la communication et la configuration du serveur IIS pour autoriser uniquement l’authentification Windows intégrée.

![configuration du réseau du service web app-v.](images/appvmgmtwebservice.gif)

Le service de gestion Web App-V est installé en tant qu’application Web sur IIS. Pour que le service de gestion Web soit en charge des connexions sécurisées (SSL) entre la console de gestion App-V et le service de gestion Web, vous devez configurer le serveur IIS où le service de gestion Web est installé et configurer la console de gestion App-V.

## <a name="in-this-section"></a>Dans cette section


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Configuration de certificats pour prendre en charge le service de gestion Web App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Fournit des informations utiles sur la configuration des certificats pour prendre en charge les connexions basées sur SSL, afin de sécuriser la communication pour le service de gestion Web App-V.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[Comment installer et configurer App-V Management Console pour un environnement plus sécurisé](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Fournit une procédure pas à pas pour la connexion à un service de gestion Web App-V à l’aide d’une connexion sécurisée.

 

 






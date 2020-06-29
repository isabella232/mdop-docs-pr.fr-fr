---
title: Comment installer et configurer App-V Management Console pour un environnement plus sécurisé
description: Comment installer et configurer App-V Management Console pour un environnement plus sécurisé
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807081"
---
# Comment installer et configurer App-V Management Console pour un environnement plus sécurisé


L’installation par défaut de la console de gestion App-V prend en charge les communications sécurisées. Chaque console de gestion est configurée sur une base par connexion lorsque la console est démarrée pour la première fois ou lors d’une connexion à un service de gestion des applications Web supplémentaire. La configuration par défaut utilise SSL via le port TCP 443. Vous pouvez modifier le numéro de port si le numéro de port a été modifié sur le serveur. Vous pouvez utiliser la procédure suivante pour vous connecter à un service de gestion des applications Web App-V via une connexion sécurisée.

**Se connecter à un service de gestion d’application-V à l’aide d’une connexion SSL**

1.  Démarrez la console de gestion Application Virtualization.

2.  Cliquez sur **configurer la connexion** dans le volet actions de la console.

3.  Entrez le **nom d’hôte du service Web**, puis vérifiez que l’option **utiliser une connexion sécurisée** est sélectionnée.

    **Important**  Le nom fourni dans le nom d’hôte du service Web doit correspondre au nom usuel du certificat ou la connexion échoue.

     

4.  Sélectionnez les informations d’identification appropriées, puis cliquez sur **OK**.

## Rubriques connexes


[Configuration de certificats pour prendre en charge le service de gestion Web App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 






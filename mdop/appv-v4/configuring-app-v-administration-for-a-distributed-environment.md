---
title: Configuration de l'administration d'App-V pour les environnements distribués
description: Configuration de l'administration d'App-V pour les environnements distribués
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809041"
---
# Configuration de l'administration d'App-V pour les environnements distribués


Lors de la conception de l’infrastructure pour votre organisation spécifique, vous pouvez installer le service Web d’administration des applications sur un ordinateur autre que celui sur lequel vous installez le serveur de gestion des applications-V. Voici quelques raisons courantes de séparation de ces composants d’application-V:

-   Niveau de performance

-   Fiabilité

-   Disponibilité

-   Extensibilité

La séparation du serveur de gestion et du service Web de gestion nécessite une configuration supplémentaire pour que l’infrastructure fonctionne correctement. Lorsque vous séparez ces deux fonctionnalités sans suivre les procédures décrites dans cette rubrique, la console de gestion se connecte au service Web de gestion mais ne peut pas s’authentifier correctement auprès du magasin de données. La console de gestion ne se charge pas correctement et l’administrateur ne peut pas effectuer d’tâches administratives.

Ce comportement se produit parce que le service Web de gestion ne peut pas utiliser les informations d’identification qui lui sont transmises à partir de la console de gestion pour accéder au magasin de données. La solution consiste à configurer le serveur de service Web de gestion pour être «approuvé pour la délégation».

## Configurer les services de domaine Active Directory


Il est également nécessaire de configurer correctement les services de domaine Active Directory pour fonctionner dans un environnement distribué. Cette section inclut les informations dont vous avez besoin pour configurer les services de domaine Active Directory.

### Lorsque le service SQL utilise le compte système local

Pour configurer l’environnement dans lequel le service SQL utilise le compte système local, modifiez les propriétés du compte d’ordinateur du service Web de gestion pour qu’il soit approuvé pour la délégation. Pour plus d’informations sur la façon de procéder, voir [Comment configurer le serveur pour être approuvé pour la délégation](how-to-configure-the-server-to-be-trusted-for-delegation.md)

### Lorsque le service SQL utilise un compte basé sur un domaine

Pour configurer l’environnement dans lequel les serveurs SQL utilisent des comptes de service basés sur le domaine, vous devez déterminer si un certain nombre de facteurs s’appliquent, y compris:

-   Regroupement de SQL Server

-   Réplication

-   Tâches automatisées

-   Serveurs liés

Pour plus d’informations sur la configuration des services de domaine Active Directory lorsque le service SQL utilise un compte basé sur un domaine, reportez-vous à la rubrique <https://go.microsoft.com/fwlink/?LinkId=151968> .

 

 






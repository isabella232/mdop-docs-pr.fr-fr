---
title: Procédure pour se connecter à un système Application Virtualization
description: Procédure pour se connecter à un système Application Virtualization
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807217"
---
# Procédure pour se connecter à un système Application Virtualization


Pour pouvoir utiliser la console de gestion pour gérer des applications, des associations de types de fichiers, des packages, des licences d’application, des groupes de serveurs, des stratégies de fournisseur et des administrateurs, vous devez connecter la console de gestion du serveur d’applications. La procédure suivante décrit les étapes à suivre pour connecter la console à un système de virtualisation des applications.

**Pour se connecter à un système de virtualisation des applications**

1. Dans le volet **étendue** , cliquez avec le bouton droit sur le nœud système de virtualisation des applications, puis sélectionnez **se connecter au système de virtualisation d’applications** dans le menu contextuel.

   **Remarque**  
   Il existe trois composants pour la gestion de serveur de la virtualisation des applications: la console de gestion des applications, le service Web de gestion et la Banque de magasin SQL. Si ces composants sont répartis sur différentes machines physiques, vous devez configurer la sécurité correctement pour que les composants puissent communiquer sur le système. Pour plus d’informations, consultez les manuels et articles suivants:

   [Comment configurer le serveur pour qu’il soit approuvé pour la délégation](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)

   [Guide de planification et de déploiement pour le système de virtualisation des applications](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)

   [Guide des opérations pour le système de virtualisation des applications](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)

   [Article 930472](https://go.microsoft.com/fwlink/?LinkId=114647) de la base de connaissances Microsoft (https://go.microsoft.com/fwlink/?LinkId=114647)

   [Article 930565](https://go.microsoft.com/fwlink/?LinkId=114648) de la base de connaissances Microsoft (https://go.microsoft.com/fwlink/?LinkId=114648)

     

2. Remplissez les champs de la boîte de dialogue **connexion à l’application de virtualisation du système** :

   1. **Nom d’hôte du service Web**: entrez le nom du système de virtualisation d’applications auquel vous voulez vous connecter, ou entrez **localhost** pour vous connecter au serveur local.

   2. **Utiliser la connexion sécurisée**: activez cette case à cocher si vous voulez vous connecter au serveur avec une connexion sécurisée.

   3. **Port**: entrez le numéro de port que vous voulez utiliser pour la connexion. **80** est le numéro de port standard par défaut et **443** correspond au numéro de port sécurisé.

   4. **Utiliser le compte Windows actuel**: sélectionnez cette case d’option pour utiliser les informations d’identification actuelles du compte Windows.

   5. **Spécifier le compte Windows**: sélectionnez cette case d’option si vous voulez vous connecter au serveur en tant qu’autre utilisateur.

   6. **Nom**— entrez le nom du nouvel utilisateur en utilisant le *DOMAIN\\username* ou le format du <em> username@domain </em> .

   7. **Mot de passe**: entrez le mot de passe correspondant au nouvel utilisateur.

3. Cliquez sur **OK**.

## Rubriques connexes


[Procédure pour effectuer des tâches d'administration dans Application Virtualization Server Management Console](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 






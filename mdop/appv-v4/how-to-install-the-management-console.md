---
title: Procédure pour installer la console de gestion
description: Procédure pour installer la console de gestion
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807053"
---
# Procédure pour installer la console de gestion


Vous pouvez utiliser la procédure suivante pour installer la console de gestion des applications de virtualisation sur un ordinateur cible sur le réseau. Vous devez utiliser un compte réseau qui dispose de privilèges d’administrateur sur l’ordinateur cible. Vous pouvez utiliser la console pour configurer et gérer la plateforme de système de virtualisation des applications.

Pour pouvoir effectuer cette procédure, vous devez installer le service Web Application Virtualization Management sur cet ordinateur ou sur un autre ordinateur. Le service Web de gestion vous permet d’accéder au magasin de données et au contrôleur de domaine. Pour plus d’informations sur l’installation du service Web, voir [Comment installer le service Web de gestion](how-to-install-the-management-web-service.md).

**Pour installer la console de gestion**

1.  Vérifiez qu’aucune version antérieure de la console de gestion n’est installée sur l’ordinateur cible.

2.  Naviguez jusqu’à l’emplacement du programme d’installation du système de virtualisation des applications sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur **Setup.exe**.

3.  Dans la **page Bienvenue**, cliquez sur **suivant**.

4.  Dans la page **contrat de licence** , pour accepter le contrat de licence, cliquez sur **J’accepte les termes du**contrat de licence, puis cliquez sur **suivant**.

5.  Dans la page **informations d’inscription** , spécifiez le **nom d’utilisateur** et les informations de l' **organisation** , puis cliquez sur **suivant**.

6.  Dans la page **type d’installation** , cliquez sur **personnalisé** , puis sur **suivant**.

7.  Dans la page **configuration personnalisée** , désélectionnez tous les composants du système de virtualisation des applications, à l’exception de la **console de gestion**, puis cliquez sur **suivant**.

    **Remarques**  Si un composant est déjà installé sur l’ordinateur, vous devez le désélectionner sur l’écran de configuration personnalisé pour le désinstaller automatiquement.

     

8.  Dans l’écran êtes-vous **prêt à modifier l’application** , cliquez sur **installer**.

    **Remarques**  S’il s’agit du premier composant que vous installez, la page **prêt à installer le programme** s’affiche. Pour démarrer l’installation, cliquez sur **installer**.

     

9.  Dans l’écran de l' **Assistant installation terminé** , cliquez sur **Terminer**. Cliquez sur **OK** pour redémarrer l’ordinateur et terminer l’installation.

10. Dans le panneau de configuration Windows, double-cliquez sur **Outils d’administration** , puis cliquez sur **console de gestion des applications** pour afficher la console de gestion.

11. Cliquez sur l’icône de **connexion** ou cliquez avec le bouton droit sur le conteneur **Application Virtualization Systems** , puis cliquez sur **se connecter au système de virtualisation des applications**.

12. Dans l’écran **connexion au système de virtualisation des applications** , entrez le nom d’hôte et le port de l’ordinateur de service Web de gestion, modifiez les informations de sécurité et les informations d’identification d’ouverture de session si nécessaire, puis cliquez sur **OK**.

13. Après vous être connecté à l’ordinateur de service Web de gestion, cliquez sur **fichier** dans le menu de la **console** , puis cliquez sur **quitter**. Cliquez sur **Oui** pour enregistrer les paramètres de la console.

## Rubriques connexes


[Procédure pour installer les serveurs et les composants système](how-to-install-the-servers-and-system-components.md)

 

 






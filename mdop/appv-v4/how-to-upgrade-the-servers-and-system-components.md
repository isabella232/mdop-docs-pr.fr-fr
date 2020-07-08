---
title: Procédure pour mettre à niveau les serveurs et les composants système
description: Procédure pour mettre à niveau les serveurs et les composants système
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806701"
---
# Procédure pour mettre à niveau les serveurs et les composants système


Utilisez la procédure suivante pour mettre à niveau les composants logiciels installés sur tous les ordinateurs système de virtualisation des applications. Le service système de virtualisation des applications sera redémarré automatiquement sur chaque ordinateur après la mise à niveau.

**Remarque**  
-   Le processus de mise à niveau arrête tous les services du système de virtualisation des applications, ce qui a pour effet d’arrêter le service du système. Les sessions utilisateur doivent être arrêtées avant de commencer le processus de mise à niveau, et vous devez arrêter l’ensemble des services serveur de virtualisation des applications dans votre environnement.

-   Si vous disposez de plusieurs serveurs partageant l’accès à la base de données de virtualisation des applications, tous les serveurs doivent être déconnectés pendant la mise à niveau de la base de données. Nous vous conseillons de suivre les pratiques normales de votre entreprise pour la mise à niveau de la base de données, mais il est recommandé de tester la mise à niveau de la base de données en utilisant d’abord une copie de sauvegarde de la base de données sur un serveur de test. Ensuite, vous devez sélectionner l’un des serveurs pour la première mise à niveau, qui mettra à niveau le schéma de la base de données. Après avoir effectué la mise à niveau de la base de données de production, vous pouvez mettre à niveau les autres serveurs.

-   Vous pouvez effectuer une mise à niveau vers Microsoft Application Virtualization (App-V) 4.5 uniquement à partir de Microsoft Application Virtualization (App-V) 4.1 ou 4.1 SP1. Pour pouvoir procéder à la mise à niveau vers App-V 4.5, vous devez désinstaller ou mettre à niveau App-V 4.0 ou une version antérieure.

 

**Pour mettre à niveau les composants logiciels sur les ordinateurs système de virtualisation des applications**

1.  Naviguez jusqu’à l’emplacement du programme d’installation sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur le fichier Setup.exe.

2.  Dans la page **Bienvenue** de l’Assistant Installation, cliquez sur **suivant**.

3.  Sur la page **contrat de licence** , lisez le contrat de licence, activez la case à cocher **accepter les termes du contrat de licence**, puis cliquez sur **suivant**.

4.  Lorsque la page **logiciel installé** s’ouvre et affiche la liste des composants du système de virtualisation des applications installés et la version de chaque composant, cliquez sur **suivant**.

5.  Dans la page **avertissement de perte de session** , lisez le message affiché, puis cliquez sur **suivant**.

6.  Dans la page **connexion à la base de données de configuration** , examinez le contenu de la page, puis cliquez sur **suivant**.

7.  Si la page **obligatoire mise à niveau de la base de données** est affichée, une mise à niveau de la base de données est requise. Entrez les informations d’identification d’administration de la base de données, puis cliquez sur **suivant**. Si cette page n’est pas affichée, passez à l’étape 9.

8.  Dans la page **de la base de données de configuration de sauvegarde** , activez les cases à cocher appropriées pour effectuer la sauvegarde et exporter celle-ci vers un emplacement existant, puis cliquez sur **suivant**.

    **Important**  Si vous voulez être en mesure de revenir à la version précédente en cas d’échec de la mise à niveau, veillez à activer la case à cocher **effectuer une sauvegarde de la base de données de configuration** ou vous allez perdre les données de configuration.

    Lorsque vous voulez restaurer une base de données avec le service VSS, vous devez d’abord arrêter le service App-V Server sur le serveur de gestion. Vous devez effectuer cette opération sur chaque serveur de gestion s’il existe plusieurs serveurs connectés à la même base de données.

     

9.  Sur la première page de **validation du package** , lisez le contenu, puis cliquez sur **suivant**.

10. Sur la deuxième page de **validation du package** , vous avez la possibilité d’afficher les détails de la validation du package dans une fenêtre bloc-notes. Pour afficher les détails, cliquez sur **Détails**. dans le cas contraire, cliquez sur **suivant**.

11. Dans la page **prêt pour la mise à niveau du programme** , cliquez sur **suivant**.

12. Dans la page terminé de l' **Assistant Installation** , cliquez sur **Terminer**.

13. Répétez les étapes 1 à 12 sur tous les autres ordinateurs sur lesquels vous avez installé la console de gestion des applications ou le composant logiciel serveur Application Virtualization.

    Après avoir effectué la mise à niveau du magasin de données, vous pouvez reprendre le fonctionnement normal. (Le magasin de données est mis à niveau lors de la mise à niveau d’un serveur ou du service Web de gestion des applications.)

## Rubriques connexes


[Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md)

 

 






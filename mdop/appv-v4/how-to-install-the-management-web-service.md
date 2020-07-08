---
title: Procédure pour installer le service de gestion Web
description: Procédure pour installer le service de gestion Web
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807042"
---
# Procédure pour installer le service de gestion Web


Suivez la procédure ci-dessous pour installer le service Web Application Virtualization Management sur un ordinateur cible sur le réseau, avec un compte de connexion doté de privilèges d’administrateur local. Même si ce n’est pas le cas, nous vous recommandons d’installer ce composant sur votre serveur Web.

**Pour installer le service Web de gestion**

1.  Vérifiez qu’aucune version antérieure du service Web Application Virtualization n’est installée sur l’ordinateur cible.

2.  Naviguez jusqu’à l’emplacement du programme d’installation du système de virtualisation des applications sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur **Setup.exe**.

3.  Après l’ouverture de l’Assistant Installation, dans la page **Bienvenue** , cliquez sur **suivant**.

4.  Dans la page **contrat de licence** , pour accepter le contrat de licence, cliquez sur **J’accepte les termes du**contrat de licence, puis cliquez sur **suivant**.

5.  Dans la page **informations d’inscription** , spécifiez le **nom d’utilisateur** et les informations de l’organisation, puis cliquez sur **suivant**.

6.  Dans la page **type d’installation** , cliquez sur **personnalisé**, puis sur **suivant**.

    **Remarques**  S’il ne s’agit pas du premier composant que vous avez installé sur votre ordinateur, la page **maintenance du programme** s’affiche. Dans la page **maintenance du programme** , cliquez sur **modifier**.

     

7.  Dans la page **configuration personnalisée** , effacez tous les composants du système de virtualisation des applications, à l’exception de **App Virt Management Service**, puis cliquez sur **suivant**.

    **Remarques**  Si un composant est déjà installé sur l’ordinateur, vous devez le supprimer de la page de **configuration personnalisée** pour le désinstaller automatiquement.

     

8.  Dans la page **serveur de base de données** , cliquez sur **se connecter à une base de données disponible**, puis sur **suivant**.

    **Remarques**  Dans un environnement de production, Microsoft part du principe que vous êtes connecté à une base de données existante. Pour installer une base de données, reportez-vous [à la rubrique installation d’une base de données](how-to-install-a-database.md). Après l’installation de la base de données, passez à l’étape 13.

     

9.  Dans la page **type du serveur de base de données** , sélectionnez un type de base de données dans la liste, puis cliquez sur **suivant**.

10. Sur la **page emplacement du serveur de base de données** , sélectionnez un serveur de base de données dans la liste des serveurs disponibles ou ajouter un serveur en activant la case à cocher **utiliser le nom d’hôte suivant** et en entrant les informations dans les zones **nom du serveur** et numéro de **port** , puis cliquez sur **suivant**.

11. Dans la page **Sélectionner une base de données** , sélectionnez la base de données souhaitée, puis cliquez sur **suivant**.

12. Dans la page **Configuration utilisateur de la base de données** , entrez les informations d’identification que le service Web de gestion doit utiliser pour accéder au magasin de données, puis cliquez sur **suivant**.

13. Dans la page **êtes-vous prêt à modifier le programme** , cliquez sur **installer**.

    **Remarques**  S’il s’agit du premier composant que vous installez, la page **prêt à installer le programme** s’affiche. Dans la page, cliquez sur **installer**.

     

14. Dans la page terminé de l' **Assistant Installation** , cliquez sur **Terminer**.

## Rubriques connexes


[Procédure pour installer les serveurs et les composants système](how-to-install-the-servers-and-system-components.md)

 

 






---
title: Comment appliquer des paramètres généraux à un espace de travail MED-V
description: Comment appliquer des paramètres généraux à un espace de travail MED-V
author: dansimp
ms.assetid: 6152dced-e301-4fa2-bfa0-aecf3c23f23a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 176564ae1d22b27a24625d988f46c9746b291748
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811814"
---
# Comment appliquer des paramètres généraux à un espace de travail MED-V


Les paramètres généraux vous permettent de configurer l’expérience utilisateur de base lors de l’utilisation d’un espace de travail MED-V et de définir si l’espace de travail MED-V s’affichera en intégration transparente ou en mode Bureau complet. L’intégration transparente inclut des applications héritées sur le bureau hôte, de sorte qu’elles apparaissent comme s’ils étaient installés directement sur l’hôte. Bureau complet présente le Bureau du système d’exploitation MED-V dans une fenêtre séparée sur l’hôte.

Tous les paramètres généraux sont configurés dans le module de **stratégie** sous l’onglet **général** .

**Pour appliquer les paramètres généraux à un espace de travail MED-V**

1.  Cliquez sur l’espace de travail MED-V à configurer.

2.  Configurez les propriétés générales comme décrit dans le tableau suivant.

3.  Dans le menu **stratégie** , cliquez sur **valider**.

**Propriétés générales de l’espace de travail**

*Propriétés de* la description de propriété

Nom

Nom de l’espace de travail MED-V.

**Avertissement**  Ne renommez pas un espace de travail MED-V existant alors qu’il s’exécute sur un ordinateur client.

 

Description

Description de l’espace de travail MED-V, qui peut inclure le contenu ou l’état de l’espace de travail MED-V ainsi que d’autres informations utiles.

**Remarques**  La description est destinée aux administrateurs et n’a aucun impact sur celle-ci.

 

Coordonnées du support technique

Coordonnées du support technique. Les informations entrées apparaissent dans l’écran informations de contact du support technique qui sont accessibles à partir de la zone de notification du client MED-V.

*Interface utilisateur d’espace de travail*

Intégration transparente

Sélectionnez cette option pour que les icônes des fenêtres de l’espace de travail, de la barre des tâches et de la zone de notification MED-V s’intègrent parfaitement au bureau hôte.

Dessiner un cadre à l’intérieur de chaque fenêtre d’espace de travail

Lorsque vous utilisez une intégration transparente, activez cette option pour créer une bordure de couleur autour de toutes les applications qui s’exécutent dans l’espace de travail MED-V et un arrière-plan en couleur pour toutes les icônes de boutons de la barre des tâches. Dans le champ **couleur du cadre** , sélectionnez la couleur.

Bureau complet

Sélectionnez cette option pour afficher l’espace de travail MED-V en tant que bureau complet, sans l’intégrer à l’hôte.

*Vérification de l’hôte*

Ligne de commande

Tapez une ligne de commande à exécuter sur l’hôte avant de démarrer l’espace de travail MED-V.

Ne pas démarrer l’espace de travail en cas d’échec de la vérification (le code de sortie n’est pas «0»)

Activez cette case à cocher si vous utilisez une ligne de commande et souhaitez lancer l’espace de travail MED-V uniquement si le script est terminé correctement.

 

Une ligne de commande peut être exécutée sur l’hôte avant de démarrer l’espace de travail MED-V.

**Pour exécuter une ligne de commande avant le démarrage d’un espace de travail MED-V**

1.  Dans le champ **ligne de commande** , entrez une ligne de commande.

2.  Pour démarrer l’espace de travail MED-V uniquement si la ligne de commande est réussie, activez la case à cocher **ne pas démarrer l’espace de travail en cas d’échec de la vérification** .

## Rubriques connexes


[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

[Création d'un espace de travail MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

 

 






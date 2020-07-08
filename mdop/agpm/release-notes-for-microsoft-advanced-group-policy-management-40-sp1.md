---
title: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP1
description: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP1
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807545"
---
# Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP1


Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.

Lisez attentivement ces notes de publication avant d’installer la gestion de la stratégie de groupe Microsoft avancée (AGPM) 4,0 SP1. Ces notes de publication contiennent des informations nécessaires pour l’installation d’AGPM 4,0 SP1 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et une autre documentation AGPM, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu fourni avec ce produit.

## Problèmes connus d’AGPM 4,0 SP1


Cette section contient des notes de publication pour AGPM 4,0 SP1.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>L’outil «désinstaller» du panneau de configuration peut ne pas fonctionner lorsque vous tentez de modifier les paramètres du serveur AGPM

L’outil du panneau de configuration qui vous permet de désinstaller ou de modifier un programme risque de ne pas fonctionner lorsque vous tentez de modifier les paramètres du serveur AGPM.

Solution de contournement: avant d’essayer de modifier les paramètres de serveur AGPM à l’aide du panneau de configuration, effectuez une copie du dossier d’archive AGPM. Vous pouvez ensuite utiliser Setup.exe pour réinstaller le serveur AGPM et sélectionner les paramètres de configuration de votre choix.

### Les rapports n’affichent pas les liens ajoutés à un objet de stratégie de groupe

Les paramètres d’AGPM et les rapports de différences n’affichent pas les liens ajoutés à un objet de stratégie de groupe.

SOLUTION: pour afficher les liens dans les rapports, sélectionnez l’objet GPO dans la console de gestion des stratégies de groupe (GPMC), puis cliquez sur l’onglet **paramètres** dans le volet droit.

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a>Les rapports n’affichent pas toutes les valeurs «propriétés des options choix»

Les paramètres d’AGPM et les rapports de différences n’affichent pas tous les paramètres qui ont été sélectionnés dans la fenêtre de propriétés options de choix de l’éditeur d’objets de stratégie de groupe.

Solution de contournement: utilisez la console GPMC pour afficher les paramètres de propriétés options de choix sélectionnés dans les rapports.

### Les rapports n’affichent pas les onglets Afficher et masquer dans certains navigateurs

Les onglets Afficher et masquer qui s’affichent à droite des paramètres d’AGPM et des rapports de différences ne s’affichent pas lorsque vous affichez les rapports dans Google Chrome ou Mozilla Firefox.

Solution de contournement: Affichez les rapports à l’aide d’Internet Explorer.

### Les paramètres d’AGPM et les rapports de différences risquent d’afficher du contenu différent des rapports GPMC

Les paramètres et les différences d’AGPM risquent de ne pas afficher le même contenu que les rapports dans la console de gestion des stratégies de groupe (GPMC).

Solution de contournement: utilisez la console GPMC pour afficher les rapports AGPM.

### Le service AGPM ne démarre pas si le contrôleur de domaine n’est pas connecté

Lorsque le service AGPM est installé sur un contrôleur de domaine sous Windows 8, le service n’est pas démarré si le contrôleur de domaine n’est pas connecté.

Solution de contournement: démarrez manuellement le service AGPM après que le contrôleur de domaine est en ligne.

### La mise à niveau d’AGPM Server vers AGPM 4,0 SP1 est bloquée lors de la mise à niveau à partir de la version d’AGPM 4,0 plus le correctif

Si vous essayez de mettre à niveau le serveur AGPM vers AGPM 4,0. SP1 après l’installation d’AGPM 4,0, puis l’installation du correctif AGPM (Voir l’article de la base de connaissances [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), la mise à niveau échoue et ne peut pas être effectuée.

Solution de contournement: désinstallez le serveur AGPM 4,0, puis installez AGPM 4,0 SP1.

### Rapports ne pas afficher les liens d’unité d’organisation

Si vous liez un objet de stratégie de groupe non contrôlé à une unité d’organisation, puis le contrôle à l’aide d’AGPM, les paramètres et les rapports d’AGPM n’affichent pas les liens d’unité d’organisation.

Solution de contournement: à partir de l’onglet **contrôlé** du nœud **modifier les paramètres** , cliquez avec le bouton droit sur l’objet de stratégie de groupe, cliquez sur **paramètres** , puis cliquez sur liens d’objets de **stratégie de groupe** pour afficher les liens d’organisation. Vous pouvez également utiliser la console GPMC pour afficher les liens d’un objet de stratégie de groupe à partir de l’onglet **étendue** .

## Rubriques connexes


[Gestion avancée des stratégies de groupe](index.md)

[Nouveautés d'AGPM4.0SP1](whats-new-in-agpm-40-sp1.md)

 

 






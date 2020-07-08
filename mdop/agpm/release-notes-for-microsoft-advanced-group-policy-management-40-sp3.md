---
title: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP3
description: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP3
author: dansimp
ms.assetid: 955d7674-a8d9-4fc5-b18a-5a1639e38014
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 6e0da04d67b3d29135071e0bc82b8e01789e4e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807541"
---
# Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP3


Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.

Lisez attentivement ces notes de publication avant d’installer Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack3 (SP3). Ces notes de publication contiennent des informations nécessaires à l’installation d’AGPM 4.0 SP3 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et toute autre documentation AGPM, envisagez la dernière modification faisant autorité. Ces notes de publication remplacent le contenu fourni avec ce produit.

## Problèmes connus d’AGPM 4.0 SP3


Cette section décrit les problèmes connus d’AGPM 4,0 SP3.

### Échec de l’installation d’AGPM dans Windows 10

AGPM active en interne le mode d’activation Windows Communication Foundation (WCF)-non HTTP lors de l’installation. Dans Windows 10, WCF inclut désormais une configuration requise pour redémarrer Windows après l’activation de la fonctionnalité de non-activation de WCF. Toutefois, le code du programme d’installation d’AGPM ne gère pas cette exigence de redémarrage et ne répond plus pendant que le service doit être activé.

**Solution de contournement:** Avant d’exécuter le programme d’installation d’AGPM, activez la fonctionnalité d’activation non HTTP WCF, puis redémarrez Windows.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>L’outil «désinstaller» du panneau de configuration peut ne pas fonctionner lorsque vous tentez de modifier les paramètres du serveur AGPM

L’outil du panneau de configuration que vous utilisez pour désinstaller ou modifier un programme risque de ne pas fonctionner lorsque vous tentez de modifier les paramètres du serveur AGPM.

**Solution de contournement:** Avant d’essayer de modifier les paramètres du serveur AGPM à l’aide du panneau de configuration, effectuez une copie du dossier d’archive AGPM. Vous pouvez ensuite utiliser Setup.exe pour réinstaller le serveur AGPM et sélectionner les paramètres de configuration de votre choix.

### Les rapports n’affichent pas les liens ajoutés à un objet de stratégie de groupe

Les paramètres d’AGPM et les rapports de différences n’affichent pas les liens ajoutés à un objet de stratégie de groupe.

**Solution de contournement:** Pour afficher les liens dans les rapports, sélectionnez l’objet GPO dans la console de gestion des stratégies de groupe (GPMC), puis cliquez sur l’onglet **paramètres** dans le volet droit.

### Les rapports n’affichent pas toutes les options de propriétés options de choix

Les paramètres d’AGPM et les rapports de différences n’affichent pas tous les paramètres qui ont été sélectionnés dans la fenêtre de **Propriétés options de choix** de l’éditeur d’objets de stratégie de groupe.

**Solution de contournement:** Utilisez la console GPMC pour afficher les paramètres de **Propriétés options de choix** sélectionnés dans les rapports.

### Il est possible que les rapports n’affichent pas les onglets Afficher et masquer dans certains navigateurs

Les onglets **Afficher** et **Masquer** , situés dans la partie droite des rapports d’AGPM et des rapports de différences, risquent de ne pas apparaître lorsque vous affichez les rapports dans Google Chrome ou Mozilla Firefox.

**Solution de contournement:** Affichez les rapports à l’aide du navigateur Internet Explorer.

### Les paramètres d’AGPM et les rapports de différences risquent d’afficher du contenu différent des rapports GPMC

Les rapports et les paramètres d’AGPM risquent de ne pas afficher le même contenu que les rapports dans la console GPMC.

**Solution de contournement:** Utilisez la console GPMC pour afficher les rapports AGPM.

### Le service AGPM ne démarre pas si le contrôleur de domaine est hors connexion

Lorsque le service AGPM est installé sur un contrôleur de domaine sur les systèmes d’exploitation Windows® 8 ou version ultérieure, le service ne démarre pas si le contrôleur de domaine est hors connexion.

**Solution de contournement:** Démarrez manuellement le service AGPM une fois le contrôleur de domaine connecté.

### La mise à niveau d’AGPM Server vers AGPM 4.0 SP2 est bloquée lors de la mise à niveau à partir d’AGPM 4.0 version plus HotFix1

Si vous essayez de mettre à niveau le serveur AGPM vers AGPM 4,0. SP2 après l’installation d’AGPM 4,0 Server, puis l’installation de la mise à jour d’AGPM nommée AGPM 4,0 signale les différences incorrectes dans le rapport HTML (Voir l’article de la base de connaissances [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), la mise à niveau échoue et ne peut pas être effectuée.

**Solution de contournement:** Désinstallez le serveur 4,0 AGPM, puis installez AGPM 4,0 SP2.

### Rapports ne pas afficher les liens d’unité d’organisation

Si vous liez un objet de stratégie de groupe non contrôlé à une unité d’organisation, puis le contrôle à l’aide d’AGPM, les paramètres et les rapports d’AGPM n’affichent pas les liens d’unité d’organisation.

**Solution de contournement:** Dans l’onglet **contrôlé** du nœud **modifier les paramètres** , cliquez avec le bouton droit sur l’objet de stratégie de groupe, cliquez sur **paramètres**, puis sur liens d’objets de **stratégie de groupe** pour afficher les liens d’organisation. Vous pouvez également utiliser la console GPMC pour afficher les liens d’un objet de stratégie de groupe à partir de l’onglet **étendue** .

### AGPM affiche une erreur si vous cliquez sur le bouton précédent dans la boîte de dialogue Modifier, réparer ou supprimer le client AGPM

Si vous naviguez jusqu’à **programmes et fonctionnalités** dans le panneau de configuration et sélectionnez gestion de la **stratégie de groupe Microsoft avancé-client**, AGPM affiche une erreur si vous cliquez sur **modifier** , puis cliquez sur le bouton **précédent** dans la boîte de dialogue **modifier, réparer ou supprimer le client AGPM** .

**Solution de contournement:** Cliquez sur **Annuler** pour supprimer l’erreur, puis redémarrez le processus. Ne cliquez pas sur le bouton **précédent** lorsque vous cliquez sur **modifier** .

### Le commentaire ne s’affiche pas dans la fenêtre historique lorsque l’approbateur déploie un objet de stratégie de groupe et entre un commentaire

Si un utilisateur qui dispose du rôle d’éditeur envoie une demande de déploiement d’un objet de stratégie de groupe et l’utilisateur qui a le rôle Approbateur déploie ensuite l’objet de stratégie de groupe et entre un commentaire, le commentaire ne peut pas s’afficher dans la fenêtre de l' **historique** .

**Solution de contournement:** Néant.

### Mécanisme ajouté pour la substitution du comportement par défaut d’AGPM lors de la suppression des modifications d’autorisation d’objet GPO

À partir de HF02, AGPM a ajouté une clé de Registre permettant de remplacer le comportement d’autorisation par défaut de l’objet AGPM. Pour plus d’informations, consultez [les modifications apportées aux autorisations d’objets de stratégie de groupe par le biais d’AGPM sont ignorées](https://support.microsoft.com/kb/3174540)

## Rubriques connexes


[Gestion avancée des stratégies de groupe](index.md)

[Nouveautés d'AGPM4.0SP3](whats-new-in-agpm-40-sp3.md)

 

 






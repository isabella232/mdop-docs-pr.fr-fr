---
title: Procédure pour configurer des serveurs de publication
description: Procédure pour configurer des serveurs de publication
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806742"
---
# Procédure pour configurer des serveurs de publication


Vous pouvez utiliser les procédures suivantes pour ajouter et configurer des serveurs de virtualisation d’application directement à partir de la console de gestion des clients.

**Pour ajouter un serveur de publication d’applications**

1.  Dans le volet **résultats** , cliquez avec le bouton droit et sélectionnez **nouveau serveur** dans le menu contextuel pour démarrer l’Assistant Nouveau serveur d’applications de virtualisation ou cliquez avec le bouton droit sur le nœud du **serveur de publication** et sélectionnez **nouveau serveur** dans le menu contextuel.

2.  Dans la page de l’Assistant, entrez le nom du serveur dans le champ **nom d’affichage** , puis sélectionnez le type de serveur dans la liste déroulante **type** . Dans la liste déroulante des types de serveurs, vous pouvez choisir **serveur de virtualisation des applications**, serveur de virtualisation des applications de **sécurité améliorée**, serveur **http standard**ou **serveur http de sécurité améliorée** .

3.  Cliquez sur **Suivant**.

4.  Dans la page 2 de l’Assistant, tapez les informations appropriées dans les champs **nom d’hôte** et **port** . Le champ **path** ne peut pas être modifié pour les serveurs de virtualisation des applications. Entrez le chemin d’accès du serveur HTTP standard ou du serveur HTTP de sécurité améliorée.

5.  Cliquez sur **Terminer** pour ajouter le serveur.

**Pour configurer un serveur de publication d’application**

1.  Dans le volet **résultats** , cliquez avec le bouton droit sur le serveur de votre choix, puis sélectionnez **Propriétés** dans le menu contextuel.

2.  Cliquez sur l’onglet **général** , dans lequel vous pouvez modifier le nom du serveur, sélectionnez un type dans la liste déroulante des types de serveurs, puis spécifiez le nom d’hôte et le port. Lorsque le type du serveur est standard HTTP Server ou serveur HTTP de sécurité améliorée, le champ **path** peut également être modifié.

3.  Cliquez sur l’onglet **Actualiser** , dans lequel la case à cocher **Actualiser la publication sur l’utilisateur** est activée par défaut. Pour modifier la fréquence d’actualisation, activez la case à cocher **Actualiser la publication chaque fois** et entrez un nombre qui représente la fréquence dans le champ. Dans le menu déroulant, sélectionnez **minutes**, **heures**et **jours** . (La durée minimum que vous pouvez entrer est de 30 minutes.)

4.  Cliquez sur **appliquer** pour modifier la configuration.

5.  Lorsque vous avez terminé la publication, cliquez sur **OK** pour quitter la boîte de dialogue et revenir à la console de gestion des clients.

## Rubriques connexes


[Procédure pour désactiver ou modifier des paramètres de mode de fonctionnement déconnecté](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 






---
title: Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.1
description: Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.1
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805641"
---
# Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.1


Vous pouvez utiliser une configuration dynamique pour personnaliser un package App-V 5,1 pour un utilisateur spécifique. Toutefois, vous devez commencer par créer le fichier de configuration de l’utilisateur dynamique (. Xml) ou de configuration du déploiement dynamique avant de pouvoir utiliser les fichiers. La création du fichier est une opération manuelle avancée. Pour obtenir des informations générales sur les fichiers de configuration utilisateur dynamique, voir [à propos de la configuration dynamique App-V 5,1](about-app-v-51-dynamic-configuration.md).

Utilisez la procédure suivante pour créer un fichier de configuration utilisateur dynamique à l’aide de la console de gestion App-V 5,1.

**Pour créer un fichier de configuration utilisateur dynamique**

1.  Cliquez avec le bouton droit sur le nom du package que vous souhaitez afficher, puis sélectionnez **modifier l’accès Active Directory** pour afficher la configuration affectée à un groupe d’utilisateurs donné. Vous pouvez également sélectionner le package, puis cliquer sur **modifier**.

2.  À l’aide de la liste d' **entités publicitaires avec Access**, sélectionnez le groupe d’annonces que vous voulez personnaliser. Sélectionnez **personnalisé** dans la liste déroulante, si ce n’est pas déjà fait. Un lien intitulé **modifier** s’affichera.

3.  Cliquez sur **Modifier**. La configuration utilisateur dynamique affectée au groupe d’annonces est affichée.

4.  Cliquez sur **avancé**, puis sur **Exporter la configuration**. Tapez un nom de fichier, puis cliquez sur **Enregistrer**. Vous pouvez à présent modifier le fichier pour configurer un package pour un utilisateur.

    **Remarque**  
    Pour exporter une configuration en exécutant sur Windows Server, vous devez désactiver «configuration de la sécurité améliorée d’Internet Explorer». Si cette option est activée et définie pour bloquer les téléchargements, vous ne pouvez pas télécharger un fichier à partir de l’App-V Server.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)










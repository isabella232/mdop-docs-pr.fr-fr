---
title: Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.0
description: Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.0
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805646"
---
# Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.0


Vous pouvez utiliser une configuration dynamique pour personnaliser un package App-V 5,0 pour un utilisateur spécifique. Toutefois, vous devez commencer par créer le fichier de configuration de l’utilisateur dynamique (. Xml) ou de configuration du déploiement dynamique avant de pouvoir utiliser les fichiers. La création du fichier est une opération manuelle avancée. Pour obtenir des informations générales sur les fichiers de configuration utilisateur dynamique, voir [à propos de la configuration dynamique App-V 5,0](about-app-v-50-dynamic-configuration.md).

Utilisez la procédure suivante pour créer un fichier de configuration utilisateur dynamique à l’aide de la console de gestion App-V 5,0.

**Pour créer un fichier de configuration utilisateur dynamique**

1.  Cliquez avec le bouton droit sur le nom du package que vous souhaitez afficher, puis sélectionnez **modifier l’accès Active Directory** pour afficher la configuration affectée à un groupe d’utilisateurs donné. Vous pouvez également sélectionner le package, puis cliquer sur **modifier**.

2.  À l’aide de la liste d' **entités publicitaires avec Access**, sélectionnez le groupe d’annonces que vous voulez personnaliser. Sélectionnez **personnalisé** dans la liste déroulante, si ce n’est pas déjà fait. Un lien intitulé **modifier** s’affichera.

3.  Cliquez sur **Modifier**. La configuration utilisateur dynamique affectée au groupe d’annonces est affichée.

4.  Cliquez sur **avancé**, puis sur **Exporter la configuration**. Tapez un nom de fichier, puis cliquez sur **Enregistrer**. Vous pouvez à présent modifier le fichier pour configurer un package pour un utilisateur.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 






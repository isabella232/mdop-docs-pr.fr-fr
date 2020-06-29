---
title: Comment personnaliser les extensions d’applications virtuelles d’un groupe AD spécifique à l’aide de la console de gestion
description: Comment personnaliser les extensions d’applications virtuelles d’un groupe AD spécifique à l’aide de la console de gestion
author: dansimp
ms.assetid: 4f249ee3-cc2d-4b1e-afe5-d1cbf9cabd88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57ce4b82cc552e0a4adc2272f849111d8da0be71
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805587"
---
# Comment personnaliser les extensions d’applications virtuelles d’un groupe AD spécifique à l’aide de la console de gestion


Utilisez la procédure suivante pour personnaliser les extensions d’application virtuelles pour un groupe Active Directory (AD).

**Pour personnaliser les extensions d’applications virtuelles pour un groupe d’annonces**

1.  Pour afficher le package que vous voulez configurer, ouvrez la console de gestion App-V 5,0. Pour afficher la configuration affectée à un groupe d’utilisateurs donné, sélectionnez le package, cliquez avec le bouton droit sur le nom du package, puis sélectionnez **modifier l’accès Active Directory**. Vous pouvez également sélectionner le package et cliquer sur **modifier** dans le volet accès à la **publicité** .

2.  Pour personnaliser un groupe d’annonces, vous pouvez le trouver dans la liste des **entités publicitaires ayant accès**. Ensuite, à l’aide de la zone de liste déroulante du volet **configuration affectée** , sélectionnez **personnalisé**, puis cliquez sur **modifier**.

3.  Pour désactiver toutes les extensions pour une application donnée, décochez la case **activer**.

    Pour ajouter un nouveau raccourci pour l’application sélectionnée, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** , puis sélectionnez **Ajouter un nouveau raccourci**. Pour supprimer un raccourci, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** , puis sélectionnez **supprimer le raccourci**. Pour modifier un raccourci existant, cliquez avec le bouton droit sur l’application, puis sélectionnez **modifier le raccourci**.

4.  Pour afficher d’autres extensions d’application, cliquez sur **avancé**, puis cliquez sur **Exporter la configuration**. Tapez un nom de fichier, puis cliquez sur **Enregistrer**. Vous pouvez afficher toutes les extensions d’application associées au package à l’aide du fichier de configuration.

5.  Pour modifier d’autres extensions d’application, vous pouvez modifier le fichier de configuration et cliquer sur **Importer et remplacer cette configuration**. Sélectionnez le fichier modifié, puis cliquez sur **ouvrir**. Dans la boîte de dialogue, cliquez sur **remplacer** pour terminer le processus.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 






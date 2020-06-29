---
title: Comment configurer l’accès aux packages à l’aide de la console de gestion
description: Comment configurer l’accès aux packages à l’aide de la console de gestion
author: dansimp
ms.assetid: 8f4c91e4-f4e6-48cf-aa94-6085a054e8f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e1f5b51b118dc7b783a4a550e19fd39a61a0ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805713"
---
# Comment configurer l’accès aux packages à l’aide de la console de gestion


Avant de déployer un package virtualisé App-V 5,0, vous devez configurer les groupes de sécurité AD DS (Active Directory Domain Services) qui seront autorisés à accéder aux applications et à les exécuter. Les groupes de sécurité peuvent contenir des ordinateurs ou des utilisateurs. Le faire d’un package à un groupe d’ordinateurs publie le package globalement sur tous les ordinateurs du groupe.

Utilisez la procédure suivante pour configurer l’accès aux packages virtualisés.

**Pour accorder l’accès à un package App-V 5,0**

1.  Recherchez le package que vous souhaitez configurer:

    1.  Ouvrez la console de gestion App-V 5,0.

    2.  Pour afficher la page d’accès à la **publicité** , cliquez avec le bouton droit sur le package à configurer, puis sélectionnez **modifier l’accès Active Directory**. Vous pouvez également sélectionner le package et cliquer sur **modifier** dans le volet accès à la **publicité** .

2.  Mettre en service un groupe de sécurité pour le package:

    1.  Accédez à la page **Rechercher des noms Active Directory et des autorisations d’accès** .

    2.  À l’aide de la mise en forme **mondomaine**  \\  **nom_groupe**, tapez le nom ou une partie du nom d’un objet de groupe Active Directory, puis cliquez sur **vérifier**.

        **Remarques**  Vérifiez que vous fournissez un nom de domaine associé au groupe que vous recherchez.

         

3.  Pour accorder l’accès au package, sélectionnez le groupe de votre choix, puis cliquez sur **accorder l’accès**. Le groupe que vous venez d’ajouter apparaît dans le volet **entités publicitaires avec** le volet accès.

4.  

    Pour accepter les paramètres de configuration par défaut et fermer la page d' **accès à la publicité** , cliquez sur **Fermer**.

    Pour personnaliser des configurations pour un groupe spécifique, cliquez sur la liste déroulante **configurations affectées** , puis sélectionnez **personnalisée**. Pour configurer les configurations personnalisées, cliquez sur **modifier**. Après avoir accordé l’accès, cliquez sur **Fermer**.

**Pour supprimer l’accès à un package App-V 5,0**

1.  Recherchez le package que vous souhaitez configurer:

    1.  Ouvrez la console de gestion App-V 5,0.

    2.  Pour afficher la page d’accès à la **publicité** , cliquez avec le bouton droit sur le package à configurer, puis sélectionnez **modifier l’accès Active Directory**. Vous pouvez également sélectionner le package et cliquer sur **modifier** dans le volet accès à la **publicité** .

2.  Sélectionnez le groupe que vous voulez supprimer, puis cliquez sur **supprimer**.

3.  Pour fermer la page d’accès à la **publicité** , cliquez sur **Fermer**.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 






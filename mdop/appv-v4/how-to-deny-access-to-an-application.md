---
title: Procédure pour refuser l'accès à une application
description: Procédure pour refuser l'accès à une application
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807138"
---
# Procédure pour refuser l'accès à une application


Les utilisateurs doivent figurer dans la liste des **autorisations d’accès** d’une application pour charger et utiliser l’application. Bien que la console de gestion du serveur d’applications ne prenne pas en charge explicitement le refus d’accès à une application par un groupe d’utilisateurs, vous pouvez supprimer les groupes d’utilisateurs des propriétés d’une application pour y parvenir.

**Pour refuser l’accès à une application**

1.  Pour une application existante, cliquez sur le nœud **applications** dans le volet gauche.

2.  Cliquez avec le bouton droit sur une application dans le volet droit, puis sélectionnez **Propriétés**. Puis sélectionnez l’onglet **autorisations d’accès** .

3.  Pour supprimer l’accès d’un groupe d’utilisateurs, sélectionnez le groupe d’utilisateurs et cliquez sur **supprimer**.

4.  Cliquez sur **OK**.

    **Remarques**  Pour contrôler l’accès aux applications, vous pouvez également limiter les licences d’application. La configuration des groupes d’utilisateurs appropriés dans les services de domaine Active Directory (AD FS) constitue le moyen le plus facile d’octroyer et de refuser l’accès à des groupes d’utilisateurs spécifiques.

     

## Rubriques connexes


[Procédure pour accorder l'accès à une application](how-to-grant-access-to-an-application.md)

[Procédure pour gérer des licences d'applications dans Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Procédure pour gérer des applications dans Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 






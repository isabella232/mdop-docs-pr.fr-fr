---
title: Configurer la notification par courrier électronique
description: Configurer la notification par courrier électronique
author: dansimp
ms.assetid: 6e152de0-4376-4963-8d1a-3e7f5866d30f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e8d00c2446a0185de30bbd1f39a7e3eaf90080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807722"
---
# Configurer la notification par courrier électronique


Lorsqu’un éditeur ou un relecteur tente de créer, de déployer ou de supprimer un objet de stratégie de groupe (GPO), une demande de cette action est envoyée à une ou des adresses de messagerie désignées de telle sorte qu’un approbateur puisse évaluer la demande et l’implémenter ou la refuser. Vous déterminez l’adresse ou les adresses de messagerie à laquelle les notifications sont envoyées, ainsi que l’alias à partir duquel les notifications sont envoyées.

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour configurer les notifications par courrier électronique pour AGPM**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans le volet Détails, cliquez sur l’onglet **délégation de domaine** .

3.  Dans le champ **de** , tapez l’alias de messagerie pour AGPM à partir duquel envoyer les notifications.

4.  Dans le champ **à** , entrez une liste délimitée par des virgules des adresses de courrier des approbateurs qui doivent recevoir des demandes d’approbation.

5.  Dans le champ **serveur SMTP** , tapez un serveur de messagerie SMTP valide.

6.  Dans les champs **nom d’utilisateur** et **mot de passe** , tapez les informations d’identification d’un utilisateur ayant accès au service SMTP.

7.  Cliquez sur **Apply** (Appliquer).

### Autres éléments à prendre en considération

-   Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure. En particulier, vous devez disposer du **contenu de liste** et des autorisations de **modification des options** pour le domaine.

-   La notification par courrier électronique pour AGPM est un paramètre au niveau du domaine. Vous pouvez fournir différentes adresses de messagerie d’approbateur ou alias de messagerie d’AGPM sur l’onglet **délégation de domaine** de chaque domaine, ou utiliser les mêmes adresses de messagerie dans l’ensemble de votre environnement.

### Références supplémentaires

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks.md)

 

 






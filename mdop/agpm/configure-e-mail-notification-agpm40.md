---
title: Configurer la notification par courrier électronique
description: Configurer la notification par courrier électronique
author: dansimp
ms.assetid: 06f19556-f296-4a80-86a4-4f446c992204
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b751a49d3d22f893c420be7fef9714b242d1f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807730"
---
# Configurer la notification par courrier électronique


Lorsqu’un éditeur ou un relecteur tente de créer, de déployer ou de supprimer un objet de stratégie de groupe (GPO), une demande de cette action est envoyée à une ou des adresses de messagerie désignées de telle sorte qu’un approbateur puisse évaluer la demande et l’implémenter ou la refuser. Vous déterminez l’adresse ou les adresses de messagerie à laquelle les notifications sont envoyées, ainsi que l’alias à partir duquel les notifications sont envoyées.

Un compte d’utilisateur disposant du rôle Administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour configurer les notifications par courrier électronique pour AGPM**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans le volet Détails, cliquez sur l’onglet **délégation de domaine** .

3.  Dans le champ **à partir de l’adresse de messagerie** , entrez l’adresse de messagerie d’AGPM à partir de laquelle les notifications doivent être envoyées.

4.  Dans le champ **adresse de messagerie** , entrez une liste délimitée par des virgules des adresses de courrier des approbateurs qui doivent recevoir des demandes d’approbation.

5.  Dans le champ **serveur SMTP** , tapez un serveur de messagerie SMTP valide.

6.  Dans les champs **nom d’utilisateur** et **mot de passe** , tapez les informations d’identification d’un utilisateur ayant accès au service SMTP.

7.  Cliquez sur **Apply** (Appliquer).

### Autres éléments à prendre en considération

-   Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure. En particulier, vous devez disposer du **contenu de liste** et des autorisations de **modification des options** pour le domaine.

-   La notification par courrier électronique pour AGPM est un paramètre au niveau du domaine. Vous pouvez fournir différentes adresses de messagerie d’approbateur ou alias de messagerie d’AGPM sur l’onglet **délégation de domaine** de chaque domaine, ou utiliser les mêmes adresses de messagerie dans l’ensemble de votre environnement.

-   Par défaut, les messages électroniques envoyés comme résultat d’actions dans la gestion de stratégie de groupe avancée (AGPM) ne sont pas chiffrés. Toutefois, vous pouvez configurer la sécurité de la messagerie électronique pour AGPM à l’aide des paramètres de Registre pour spécifier l’utilisation du chiffrement SSL (Secure Sockets Layer) et le port SMTP à utiliser. Pour plus d’informations, voir [configurer la sécurité de messagerie électronique pour AGPM](configure-e-mail-security-for-agpm-agpm40.md).

### Références supplémentaires

-   [Configuration de la Gestion avancée des stratégies de groupe](configuring-advanced-group-policy-management-agpm40.md)

 

 






---
title: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0
description: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0
author: dansimp
ms.assetid: 44c19e61-c8e8-48aa-a2c2-20396d14d5bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c4a279893d4da4121e422af99e7c1708a0126b4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808289"
---
# Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0


Octobre 2009

## À propos de Microsoft Advanced Group Policy Management 4,0


La gestion de la stratégie de groupe Microsoft avancée (AGPM) 4,0 étend les fonctionnalités de la console de gestion des stratégies de groupe (GPMC). AGPM fournit un contrôle de modification complet et une gestion améliorée des objets de stratégie de groupe.

Les documents suivants peuvent vous aider à commencer à utiliser AGPM 4,0.

-   Pour une vue d’ensemble des fonctionnalités d’AGPM, voir [vue d’ensemble de la gestion de la stratégie de groupe Microsoft Advanced](https://go.microsoft.com/fwlink/?LinkID=162671) ( https://go.microsoft.com/fwlink/?LinkID=162671) .

-   Pour plus d’informations sur la façon dont AGPM 4,0 diffère d’AGPM 3,0, voir [Nouveautés d’agpm 4,0](https://go.microsoft.com/fwlink/?LinkId=160058) ( https://go.microsoft.com/fwlink/?LinkId=160058) .

-   Pour obtenir des instructions sur la façon de déterminer si AGPM 4,0, AGPM 3,0 ou AGPM 2,5 est approprié pour votre environnement, voir [choisir la version d’AGPM à installer](https://go.microsoft.com/fwlink/?LinkId=145981) ( https://go.microsoft.com/fwlink/?LinkId=145981) .

-   Pour obtenir des instructions de base sur l’installation d’AGPM et un exemple illustrant l’utilisation d’AGPM, voir [le guide étape par étape pour le Guide d’utilisation de la stratégie de groupe Microsoft Advanced 4,0](https://go.microsoft.com/fwlink/?LinkID=153505) ( https://go.microsoft.com/fwlink/?LinkID=153505) . Ce guide est essentiellement conçu pour faciliter l’utilisation d’évaluateurs et d’utilisateurs au départ.

-   Pour plus d’informations sur la mise à niveau à partir d’une version antérieure d’AGPM ou des recommandations détaillées sur la planification du déploiement d’AGPM au sein de votre organisation, voir le [Guide de planification de Microsoft Advanced Group Policy Management 4,0](https://go.microsoft.com/fwlink/?LinkID=156883) ( https://go.microsoft.com/fwlink/?LinkID=156883) .

-   Pour plus d’informations sur l’utilisation d’AGPM dans le cadre d’une tâche spécifique, voir l’aide de l’aide de l’application 4,0 de gestion des stratégies de groupe ( [4,0](https://go.microsoft.com/fwlink/?LinkId=159872) en anglais) https://go.microsoft.com/fwlink/?LinkId=159872) .

## Informations supplémentaires


Pour plus d’informations sur AGPM, voir les rubriques suivantes:

-   [Bibliothèque TechNet avancée](https://go.microsoft.com/fwlink/?LinkID=146846) sur la gestion des stratégies de groupe (https://go.microsoft.com/fwlink/?LinkID=146846)

-   [TechCenter Microsoft Desktop Optimization Pack](https://go.microsoft.com/fwlink/?LinkId=159870) (https://www.microsoft.com/technet/mdop)

-   [TechCenter de stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=145531) (https://www.microsoft.com/gp)

## Envoi de commentaires


Vous pouvez publier des commentaires ou poser des questions sur AGPM sur le Forum de la [stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=145532) ( https://go.microsoft.com/fwlink/?LinkId=145532) .

## Problèmes connus avec le 4,0 d’AGPM


### La commande Importer à partir de la production ne permet pas d’importer les paramètres d’un objet de stratégie de groupe extrait

Si vous modifiez un objet GPO dans l’environnement de production, vous devez importer l’objet GPO de production pour mettre à jour l’objet GPO dans l’archive hors connexion. La commande **Importer à partir de la production** vous permet d’effectuer une sauvegarde de production finale avant de procéder à la modification, afin que vous puissiez revenir à la sauvegarde de production, le cas échéant.

Si l’objet de stratégie de groupe est extrait lors de l’exécution de la commande **Importer à partir de la production** , les modifications de production ne sont pas incorporées à la version extraite de l’objet de stratégie de groupe. Toutefois, la version importée de l’objet de stratégie de groupe est ajoutée à l’historique de l’objet de stratégie de groupe, même si cette version ne peut pas être modifiée. Lorsque l’objet de stratégie de groupe est archivé, cette version remplace la version importée de l’archive, mais les deux sont disponibles dans l’historique de l’objet de stratégie de groupe.

**Solution de contournement:** Assurez-vous que l’objet de stratégie de groupe est archivé avant de l’importer de production. Si l’objet de stratégie de groupe n’a pas été archivé avant de l’avoir importé, vous pouvez utiliser la commande **Annuler l’extraction** pour ignorer vos modifications et revenir à la version de l’objet de stratégie de groupe importée à partir de la production.

### Les objets de stratégie de groupe extraits ne peuvent pas être modifiés pendant quelques minutes dans un environnement qui utilise une topologie Active Directory multisite

AGPM utilise un modèle client/serveur. Le serveur et le client AGPM déterminent chacun leur propre contrôleur de domaine le plus proche pour les opérations de stratégie de groupe. Lors de l’extraction d’un objet de stratégie de groupe à l’aide d’un client AGPM, il s’agit en réalité du serveur AGPM qui vérifie l’objet de stratégie de groupe de l’archive hors connexion dans un dossier temporaire dans le dossier SYSVOL.

Si le serveur et le client AGPM se trouvent dans des sites différents, l’objet de stratégie de groupe temporaire extrait ne peut pas être présent sur le contrôleur de domaine du site local pendant quelques minutes ou jusqu’à 30 minutes en raison de la latence de réplication SYSVOL. Dans ce cas, vous ne pouvez pas modifier l’objet de stratégie de groupe extrait à l’aide de la console GPMC sur un client AGPM tant que la réplication SYSVOL de l’objet de stratégie de groupe extrait s’est produit.

**Solution de contournement:** Nous vous conseillons de positionner les clients AGPM dans le même site que le serveur AGPM sur lequel ils se connectent afin de ne pas avoir besoin d’attendre la fin de la réplication SYSVOL avant de pouvoir modifier un objet de stratégie de groupe extrait.

### AGPM ne peut pas lire la limite de sauvegarde si votre compte n’est pas autorisé à utiliser l’archive

Sur un client AGPM, si vous vous connectez à l’aide d’un compte qui n’a pas reçu d’autorisations déléguées sur l’archive AGPM, démarrez la console de gestion des stratégies de groupe (GPMC), puis cliquez sur **modifier le contrôle**, le message d’erreur suivant s’affiche.

``` syntax
Failed to read backup purge limit for this domain. 

The following error occurred: 
You do not have sufficient permissions to perform this operation. 
Microsoft.Agpm.AccessDeniedException (80070005)
```

**Solution de contournement:** Contactez un administrateur AGPM (contrôle total) et demandez-lui d’avoir accès à AGPM pour votre compte. Si vous êtes un administrateur AGPM, connectez-vous à l’aide d’un compte auquel le rôle d’administrateur AGPM est attribué afin de pouvoir déléguer l’accès du compte supplémentaire. Pour plus d’informations, voir «déléguer l’accès au niveau du domaine à l’archive» dans l’aide d’AGPM.

## Informations de copyright des notes de publication


Les informations contenues dans ce document, y compris les URL et autres références de site Web Internet, peuvent faire l’objet de modifications sans préavis et sont fournies à titre informatif uniquement. L’ensemble des risques liés à l’utilisation ou aux résultats de l’utilisation de ce document par le biais de l’utilisateur et Microsoft Corporation ne garantit aucune garantie, expresse ou implicite. Les exemples de sociétés, d’organisations, de produits, de personnes et d’événements décrits dans les présentes sont fictifs. Il n’est pas possible d’associer une entreprise, une organisation, un produit, une personne ou un événement réel. Conformément à toutes les lois applicables en matière de copyright, il incombe à l’utilisateur. Sans limiter les droits découlant du droit d’auteur, aucune partie de ce document ne pourra être reproduite, stockée ou introduite dans un système de récupération, ni transmise à l’aide d’un moyen quelconque (électronique, mécanique, photocopie, enregistrement ou autre), ou à d’autres fins, sans l’autorisation écrite rapide de Microsoft Corporation.

Microsoft peut être doté d’un brevet, d’une demande de brevet, de marques commerciales, de droits d’auteur ou d’autres droits de propriété intellectuelle concernant le sujet figurant dans ce document. À l’exception de ce que prévoit expressément un contrat de licence écrit de la part de Microsoft, la fourniture de ce document ne vous donne aucune licence pour ces brevets, marques commerciales, droits d’auteur ou toute autre propriété intellectuelle.



Microsoft, MS-DOS, Windows, windowsserver2003 et Windows Vista sont des marques commerciales ou des marques commerciales déposées de MicrosoftCorporation aux États-Unis et/ou dans d’autres pays.

Les noms des sociétés et produits réels mentionnés dans le présent document pourront être des marques de leurs propriétaires respectifs.

 

 






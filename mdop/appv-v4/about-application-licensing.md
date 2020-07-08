---
title: À propos de l'octroi de licence pour les applications
description: À propos de l'octroi de licence pour les applications
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808170"
---
# À propos de l'octroi de licence pour les applications


Vous pouvez gérer les licences d’application directement à partir de la console de gestion du serveur d’applications.

## Types de licence


Le système de virtualisation des applications System Center prend actuellement en charge les types de licence suivants:

-   **Licence illimitée**: permet d’accéder à l’application par n’importe quel nombre d’utilisateurs simultanés. Cette méthode de gestion des licences est appropriée lorsque vous voulez associer une licence à l’échelle de l’entreprise à une application.

-   **Licence simultanée**: permet de définir le nombre maximal d’utilisateurs simultanés autorisés à utiliser l’application.

-   **Licence nommée**: vous permet d’attribuer une licence à un utilisateur individuel. Une licence nommée peut être utilisée pour s’assurer qu’un utilisateur particulier sera toujours en mesure d’exécuter l’application.

Vous pouvez combiner des licences concomitantes et nommées pour la même application.

La gestion des licences est désactivée par défaut, mais vous pouvez l’activer à partir de l’onglet **pipeline du fournisseur** de la boîte de dialogue **Propriétés du fournisseur** . Pour plus d’informations sur l’activation et la désactivation de la gestion des licences, voir [Comment configurer ou désactiver la gestion des licences d’applications](how-to-set-up-or-disable-application-licensing.md).

## Stratégies du fournisseur


Des stratégies de fournisseur ont été développées pour le modèle de fournisseur de services d’application (ASP). Dans ce modèle, un seul ASP peut héberger un système de virtualisation d’application unique pour plusieurs clients, où chaque client doit rester isolé. Les clients peuvent avoir considérablement différentes exigences (par exemple, un client peut nécessiter une authentification alors qu’il n’en existe pas). Vous pouvez utiliser des stratégies de fournisseur pour associer des autorisations aux clients de sorte que seuls les utilisateurs approuvés puissent accéder à chaque application virtuelle ou package d’application virtuelle.

Pour les clients d’entreprise, vous pouvez utiliser cette fonctionnalité lorsque vous avez strictement besoin des licences pour une ou plusieurs applications. Dans cette situation, le composant gestion des licences est désactivé sous l’onglet **pipeline du fournisseur** de la boîte de dialogue **Propriétés du fournisseur** .

L’onglet **pipeline du fournisseur** comporte également des cases à cocher pour activer l’authentification, l’autorisation (**appliquer les paramètres d’autorisation d’accès**) et la mesure (informations d'**utilisation du journal**). Si votre configuration présente des exigences spéciales, vous pouvez écrire vos propres composants de pipeline et les ajouter au système en cliquant sur le bouton **avancé** .

## Autorités de compte


L’autorité de compte est le domaine dans lequel le serveur de virtualisation d’application est installé. Lorsque vous parcourez l’installation du serveur, vous êtes invité à fournir un nom de domaine; le domaine dans lequel l’ordinateur est installé est détecté et utilisé par défaut. Lorsque les utilisateurs essaient de se connecter au système, ils sont invités à entrer leurs informations d’identification avant de pouvoir accéder à ce domaine.

Le système de virtualisation des applications prend en charge plusieurs domaines. Vous pouvez accorder l’accès à l’application aux groupes d’utilisateurs dans d’autres domaines si une relation d’approbation est établie entre les domaines. Les utilisateurs doivent fournir des informations d’identification reconnues par chaque domaine.

Dans la console de gestion du serveur d’applications, vous pouvez modifier le domaine principal (autorité de compte) et les informations d’identification qui sont utilisées pour y accéder.

## Authentification


L’authentification est le mécanisme utilisé pour confirmer l’identité d’un utilisateur. Tout utilisateur disposant d’un nom d’utilisateur et d’un mot de passe reconnus a accès.

Dans le système de virtualisation des applications, vous pouvez activer ou désactiver l’authentification par le biais d’une case à cocher sous l’onglet **pipeline du fournisseur** . Par défaut, l’authentification Windows est activée.

## Authorization


Authorization est le processus utilisé pour confirmer l’identité d’un utilisateur. Après confirmation de l’identité de l’utilisateur, le système détermine s’il a accordé l’accès au système et aux applications auxquelles l’utilisateur a été autorisé à accéder. La console de gestion du serveur d’applications est doté de la case à cocher **appliquer les paramètres d’autorisation d’accès** dans l’onglet **pipeline du fournisseur** pour activer ou désactiver l’autorisation.

Dans le système de virtualisation des applications, Access est accordé uniquement à un groupe d’utilisateurs, et non à des utilisateurs individuels.

## Rubriques connexes


[Procédure pour gérer des licences d'applications dans Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Procédure pour configurer ou désactiver l'octroi de licence pour les applications](how-to-set-up-or-disable-application-licensing.md)

[Server Management Console: nœud Stratégies du fournisseur](server-management-console-provider-policies-node.md)

 

 






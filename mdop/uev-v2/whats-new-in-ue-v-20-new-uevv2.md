---
title: Nouveautés dans UE-V2.0
description: Nouveautés dans UE-V2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810871"
---
# Nouveautés dans UE-V2.0


La virtualisation de l’interface utilisateur de Microsoft (UE-V) 2,0 fournit ces nouvelles fonctionnalités et les fonctionnalités de UE-V 1,0. Les [notes de publication de Microsoft User Interface Virtualization (UE-v) 2,0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) fournissent des informations supplémentaires sur la version d’UE-v 2,0.

## Le cache côté client (CSC) n’est plus requis


Cette version de UE-V introduit le **fournisseur de synchronisation**, qui remplace l’exigence de la fonctionnalité fichiers en mode hors connexion de Windows pour la prise en charge d’un cache côté client de paramètres.

Considérant que UE-V a utilisé pour synchroniser les paramètres uniquement lorsqu’une application est ouverte, fermée ou lorsque Windows est verrouillé ou déverrouillé, ou à l’ouverture ou à la fermeture de session, le fournisseur de synchronisation...

-   Synchronise les paramètres de l’application locale et de Windows hors-bande à l’aide d’un**déclencheur d’événements**

-   Utilise une **tâche planifiée** pour synchroniser le package de stockage des paramètres dans tout intervalle que vous choisissez pour les besoins de votre entreprise (toutes les 30 minutes par défaut)

Certaines conditions permettent une synchronisation plus fréquente.

-   Les paramètres sont synchronisés quand l’utilisateur clique sur le bouton **Synchroniser maintenant** dans l’application Centre de paramètres de nouvelle société.

-   Le fournisseur de synchronisation peut également démarrer pour une application unique sans attendre la tâche de synchronisation planifiée. Par exemple, quand une application est fermée, les modifications apportées aux paramètres sont écrites dans le cache local, et le processus du fournisseur de synchronisation s’exécute de manière asynchrone pour déplacer ces modifications de paramètres vers l’emplacement de stockage des paramètres.

## Synchronisation d’applications Windows


Le développeur d’une application Windows peut définir les paramètres, le cas échéant, à synchroniser, et ces paramètres peuvent désormais être capturés et synchronisés avec UE-V.

Par défaut, UE-V synchronise les paramètres de nombreux logiciels Windows inclus dans Windows 8 et Windows 8,1. Vous pouvez modifier la liste des applications synchronisées avec Windows PowerShell, Windows Management Instrumentation (WMI) ou une stratégie de groupe.

**Remarques**  UE-V ne synchronise pas les paramètres des applications Windows si les utilisateurs du domaine lient leurs informations d’identification de connexion à leur compte Microsoft. Ce lien permet de synchroniser les paramètres avec Microsoft OneDrive de manière à ce que UE-V ne synchronise que les applications de bureau.

 

## Liaison de compte Microsoft


La synchronisation des paramètres via OneDrive est une nouveauté de Windows 8 lorsque vous êtes connecté avec un compte Microsoft ou si vous liez votre compte Microsoft à votre compte de domaine. Si un utilisateur du domaine utilise UE-V et s’est connecté à un compte Microsoft, alors...

-   UE-V ne synchronise que les paramètres des applications de bureau.

-   Le compte Microsoft gère les paramètres d’application Windows et les paramètres de bureau Windows

## Centre de paramètres de la société


Vous pouvez fournir aux utilisateurs un contrôle sur les paramètres qui sont synchronisés par le biais d’une application dans UE-V 2 appelé centre de paramètres de l’entreprise. Le centre de gestion des paramètres de l’entreprise est installé avec l’agent UE-V, et les utilisateurs peuvent y accéder à partir du panneau de configuration, du menu **Démarrer** ou de l’écran d' **Accueil** , et à partir de l’icône de zone de notification UE-v.

Le centre de paramètres de la société affiche les paramètres qui sont synchronisés et permet aux utilisateurs d’afficher l’état de synchronisation d’UE-V. Si vous les autorisez, les utilisateurs peuvent utiliser le centre de paramètres d’une entreprise pour sélectionner les paramètres de synchronisation. Ils peuvent également cliquer sur le bouton **Synchroniser maintenant** pour synchroniser tous les paramètres immédiatement.






## Rubriques connexes


[Prise en main d'UE-V2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Préparer un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 






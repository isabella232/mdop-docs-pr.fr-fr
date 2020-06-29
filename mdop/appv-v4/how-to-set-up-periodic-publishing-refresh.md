---
title: Procédure pour configurer une actualisation de publication périodique
description: Procédure pour configurer une actualisation de publication périodique
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806753"
---
# Procédure pour configurer une actualisation de publication périodique


Vous pouvez utiliser la procédure suivante pour configurer le client de manière à actualiser régulièrement les informations de publication des serveurs App-V. Une fois le client configuré, l’opération d’actualisation est automatique. Ces paramètres configurent les paramètres par défaut pour le client de sorte que tous les utilisateurs de cet ordinateur puissent voir les mêmes paramètres.

**Remarques**  Après avoir effectué cette procédure, les informations de publication sont actualisées conformément aux nouveaux paramètres après la première actualisation à la connexion. Lors de la première actualisation, le serveur peut remplacer les paramètres de l’ordinateur par d’autres paramètres, selon la manière dont il est configuré. L’onglet **Actualiser** de la boîte de dialogue **Propriétés** affiche les paramètres de l’ordinateur client configurés en local ainsi que les paramètres susceptibles d’avoir été configurés pour l’utilisateur par le serveur de publication.

 

**Pour actualiser régulièrement les informations de publication des serveurs de virtualisation des applications**

1.  Cliquez sur **serveurs de publication** dans le volet de l' **étendue** .

2.  Dans le volet **résultats** , cliquez avec le bouton droit sur le serveur de votre choix, puis sélectionnez **Propriétés** dans le menu contextuel.

3.  Dans la boîte de dialogue **Propriétés** , sous l’onglet **Actualiser** , activez la case à cocher **Actualiser la configuration chaque fois** et entrez un nombre qui représente la fréquence dans le champ. Dans le menu déroulant, sélectionnez **minutes**, **heures**et **jours** .

    **Remarques**  Ce paramètre force le client à actualiser les informations de publication chaque fois que la période configurée est écoulée. Si l’utilisateur n’est pas connecté quand il est temps de procéder à une actualisation, l’actualisation intervient lors de la prochaine connexion de l’utilisateur. Le minuteur est alors redémarré pour la période suivante.

     

4.  Cliquez sur **appliquer** pour modifier la configuration.

5.  Lorsque vous avez terminé de configurer le serveur, cliquez sur **OK** pour quitter la boîte de dialogue et revenir à la console de gestion des clients Application Virtualization.

## Rubriques connexes


[Procédure pour configurer le client dans Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 






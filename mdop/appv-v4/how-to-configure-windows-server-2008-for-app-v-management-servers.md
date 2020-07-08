---
title: Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server
description: Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807221"
---
# Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server


Le serveur Windows Server 2008 sur lequel vous installez le service Web de gestion de Microsoft Application Virtualization (App-V) nécessite l’installation d’Internet Information Services (IIS) en tant que rôle sur le serveur. Suivez la procédure ci-dessous pour configurer Windows Server 2008 de manière à prendre en charge l’installation de l’application vserver.

**Pour installer les services Internet (IIS) sur un ordinateur Windows Server 2008**

1.  Sur l’ordinateur Windows Server 2008, cliquez sur **Démarrer**, sur **tous les programmes**, sur **Outils d’administration**, puis sur **Gestionnaire de serveur** pour démarrer le gestionnaire de serveur. Dans le gestionnaire de serveur, cliquez avec le bouton droit sur le nœud **rôles** , puis cliquez sur **Ajouter des rôles** pour démarrer l' **Assistant Ajout de rôles**.

2.  Dans l' **Assistant Ajout de rôles**, dans la page **Sélectionner des rôles de serveurs** , sélectionnez **serveur Web (IIS)**. Lorsque vous y êtes invité, cliquez sur **Ajouter les fonctionnalités requises** pour ajouter les fonctionnalités dépendantes.

3.  Dans la page **Sélectionner des rôles de serveur** , cliquez sur **suivant**, puis de nouveau sur **suivant** .

4.  Dans l' **Assistant Ajout de rôles**, dans la page **Sélectionner des services de rôle** :

    1.  Sous **développement d’applications**, sélectionnez **ASP.net** , puis, lorsque vous y êtes invité, cliquez sur Ajouter les **services de rôle requis** pour ajouter les services et fonctionnalités de rôles dépendants.

    2.  Sous **sécurité**, sélectionnez **authentification Windows**.

    3.  Dans le nœud **outils de gestion** , sélectionnez **scripts et outils de gestion IIS**. Sous **compatibilité avec la gestion IIS6**, assurez-vous que la compatibilité avec la **métabase Iis6** et la **compatibilité WMI IIS6** sont sélectionnées, puis cliquez sur **suivant**.

5.  Dans la page **confirmer les sélections** de l’installation, cliquez sur **installer**, puis suivez les instructions de l’Assistant.

6.  Cliquez sur **Fermer** pour quitter l' **Assistant Ajout de rôles**, puis fermez le gestionnaire de serveur.

## Rubriques connexes


[Configuration requise pour le déploiement d'Application Virtualization](application-virtualization-deployment-requirements.md)

[Listes de contrôle pour le déploiement et la mise à niveau d'Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

 

 






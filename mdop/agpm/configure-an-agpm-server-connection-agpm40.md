---
title: Configurer une connexion au serveur AGPM
description: Configurer une connexion au serveur AGPM
author: dansimp
ms.assetid: 409cbbcf-3b0e-459d-9bd2-75cb7b9430b0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7fdc26045b478da14957cdfe6000d58ab72a064
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807765"
---
# Configurer une connexion au serveur AGPM


Pour vous assurer que vous êtes connecté à l’archive centrale appropriée, vérifiez la configuration de la connexion au serveur AGPM. Si un administrateur AGPM (contrôle total) n’a pas configuré de connexion de serveur AGPM pour vous, vous devez le configurer manuellement.

**Pour sélectionner un serveur AGPM**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans le volet Détails, cliquez sur l’onglet **serveur AGPM** :

    -   Si les options sous l’onglet **serveur AGPM** ne sont pas disponibles, cela a été configuré de manière centralisée par un administrateur AGPM.

    -   Si les options sous l’onglet **serveur AGPM** sont disponibles, tapez le nom complet de l’ordinateur pour le serveur AGPM (par exemple, Server.contoso.com) et le port sur lequel le service AGPM écoute (par défaut, le port 4600). Cliquez sur **appliquer**, puis sur **Oui** pour confirmer.

### Autres éléments à prendre en considération

-   Les serveurs AGPM sélectionnés déterminent les objets de stratégie de groupe qui s’affichent dans l’onglet **Sommaire** et à quel emplacement les paramètres de l’onglet **délégation de domaine** sont appliqués. S’ils ne sont pas gérés de manière centralisée par le biais du modèle d’administration, chaque administrateur de stratégie de groupe doit configurer ce paramètre pour qu’il pointe vers le serveur AGPM du domaine.

### Références supplémentaires

-   [Exécution de tâches de réviseur](performing-reviewer-tasks-agpm40.md)

 

 






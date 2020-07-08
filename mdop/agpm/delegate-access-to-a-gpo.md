---
title: Déléguer l'accès à un objet de stratégie de groupe
description: Déléguer l'accès à un objet de stratégie de groupe
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807645"
---
# Déléguer l'accès à un objet de stratégie de groupe


Un approbateur peut déléguer la gestion d’un objet de stratégie de groupe contrôlé (GPO) qui a été **créé par cet approbateur**. À l’instar d’un administrateur AGPM (contrôle total), l’approbateur peut déléguer l’accès à un tel objet de stratégie de groupe, de sorte que les éditeurs sélectionnés puissent le modifier, les réviseurs pourront le consulter et permettre à d’autres approbateurs de l’approuver. Par défaut, un approbateur ne peut pas déléguer l’accès aux objets de stratégie de groupe créés par un autre administrateur de stratégie de groupe.

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe ou un compte d’utilisateur disposant des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour déléguer la gestion d’un objet de stratégie de groupe contrôlé**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **Sommaire** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés, puis cliquez sur l’objet de stratégie de groupe à déléguer.

3.  Cliquez sur le bouton **Ajouter** , sélectionnez les utilisateurs ou les groupes auxquels vous avez accès autorisé, puis cliquez sur **OK**.

4.  Pour personnaliser les autorisations pour chacun d’eux, cliquez sur le bouton **avancé** sous l’onglet **Sommaire** et activez la case à cocher autorisations de rôle à autoriser ou à refuser. (Pour un contrôle plus détaillé, cliquez sur **Options avancées** dans la boîte de dialogue **autorisations** .)

5.  Cliquez sur **appliquer**, puis sur **OK** dans la boîte de dialogue **autorisations** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine et modifier les autorisations de **sécurité** pour l’objet de stratégie de groupe.

### Références supplémentaires

-   [Création, contrôle ou importation d'un objet de stratégie de groupe](creating-controlling-or-importing-a-gpo-approver.md)

 

 






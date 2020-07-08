---
title: Renommer un objet de stratégie de groupe ou un modèle
description: Renommer un objet de stratégie de groupe ou un modèle
author: dansimp
ms.assetid: 84293f7a-4ff7-497e-bdbc-cabb70189a03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 642622ae0242e614733e8f33ea5840c8b6758db8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807537"
---
# Renommer un objet de stratégie de groupe ou un modèle


Vous pouvez renommer un objet de stratégie de groupe contrôlé (GPO) ou un modèle.

Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe, ou un compte d’utilisateur disposant des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour renommer un objet ou un modèle d’objet**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** ou **modèles** pour afficher l’élément à renommer.

3.  Cliquez avec le bouton droit sur l’objet ou le modèle à renommer, puis cliquez sur **Renommer**.

4.  Tapez le nouveau nom de l’objet GPO ou du modèle, puis cliquez sur **OK**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. L’objet ou le modèle s’affiche sous le nouveau nom dans l’onglet **contenu** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe, un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. En particulier, vous devez disposer du **contenu de liste** et de l’autorisation de **modification des paramètres** pour l’objet de stratégie de groupe.

-   Lorsque vous renommez un objet de stratégie de groupe qui a été déployé, le nom est immédiatement modifié dans l’archive. Le nom est modifié dans l’environnement de production uniquement lorsque l’objet de stratégie de groupe est redéployé. Tant que l’objet de stratégie de groupe n’est pas redéployé (ou la copie de production est supprimée), l’ancien nom est toujours utilisé dans l’environnement de production et ne peut donc pas être utilisé pour un autre objet de stratégie de groupe. De même, l’objet de stratégie de groupe dans l’archive ne peut pas renommer son nom d’origine tant qu’il n’a pas été déployé (en changeant le nom de la copie de production) ou que la copie de production a été supprimée.

### Références supplémentaires

-   [Modification d'un objet de stratégie de groupe](editing-a-gpo-agpm40.md)

 

 






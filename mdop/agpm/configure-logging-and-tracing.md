---
title: Configurer la journalisation et suivi
description: Configurer la journalisation et suivi
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807721"
---
# Configurer la journalisation et suivi


Vous pouvez configurer la journalisation et le suivi facultatifs pour une gestion avancée des stratégies de groupe (AGPM) à l’aide de modèles d’administration.

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer ces procédures. Par ailleurs, un compte d’utilisateur ayant accès au serveur AGPM est requis pour lancer la journalisation sur le serveur AGPM. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour configurer la journalisation et le suivi pour AGPM**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe pour lesquels vous souhaitez activer la journalisation et le suivi. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md).

2.  Dans l' **éditeur d’objets de stratégie de groupe**, cliquez sur Configuration de l' **ordinateur**, **modèles d’administration**et **composants Windows**.

3.  Si **AGPM** ne figure pas dans la liste **composants Windows**:

    1.  Cliquez avec le bouton droit sur **modèles d’administration** et sélectionnez **Ajouter/supprimer des modèles**.

    2.  Cliquez **sur Ajouter**, sélectionnez **AGPM. admx** ou **AGPM. adm**, cliquez sur **ouvrir**, puis sur **Fermer**.

4.  Sous **composants Windows**, double-cliquez sur **AGPM**.

5.  Dans le volet Détails, double-cliquez sur **journalisation d’AGPM**.

6.  Dans la fenêtre **Propriétés de journalisation AGPM** , cliquez sur **activé**, puis configurez le niveau de détail à enregistrer dans les journaux.

7.  Cliquez sur **OK**.

8.  Fermez l' **éditeur d’objets de stratégie de groupe**. Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md). Après la mise à jour de la stratégie de groupe, vous devez redémarrer le service AGPM pour commencer à vous connecter au serveur AGPM. Les administrateurs de stratégie de groupe doivent fermer et redémarrer la console GPMC pour commencer à se connecter sur leur ordinateur.

    **Emplacement des fichiers de suivi**:

    -   Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

    -   Serveur:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Autres éléments à prendre en considération

-   Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour configurer la journalisation et le suivi d’AGPM. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md)

### Références supplémentaires

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks.md)

 

 






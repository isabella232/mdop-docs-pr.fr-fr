---
title: Configurer la journalisation et suivi
description: Configurer la journalisation et suivi
author: dansimp
ms.assetid: 4f89552f-e949-48b0-9325-23746034eaa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6edcb643dd34a20a845cb3d44a0fe8b353a6291
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807725"
---
# Configurer la journalisation et suivi


Vous pouvez configurer la journalisation et le suivi facultatifs à l’aide de modèles d’administration. Cela pourrait s’avérer utile lors du diagnostic de problèmes liés à la gestion de stratégie de groupe avancée (AGPM).

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe (GPO) utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans AGPM est requis pour effectuer ces procédures. Par ailleurs, un compte d’utilisateur ayant accès au serveur AGPM est requis pour lancer la journalisation sur le serveur AGPM. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour configurer la journalisation et le suivi pour AGPM**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe pour lesquels vous souhaitez activer la journalisation et le suivi. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm30ops.md).

2.  Dans la fenêtre **éditeur de gestion des stratégies de groupe** , cliquez sur Configuration de l' **ordinateur**, **stratégies**, **modèles d’administration**, **composants Windows**et **AGPM**.

3.  Dans le volet Détails, double-cliquez sur **AGPM: configurer la journalisation**.

4.  Dans la fenêtre **Propriétés** , cliquez sur **activé**, puis configurez le niveau de détail à enregistrer dans les journaux.

5.  Cliquez sur **OK**.

6.  Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** . Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm30ops.md). Après la mise à jour de la stratégie de groupe, vous devez redémarrer le service AGPM pour démarrer, modifier ou arrêter la journalisation sur le serveur AGPM. Les administrateurs de stratégie de groupe doivent fermer et redémarrer le GPMC pour démarrer, modifier ou arrêter la journalisation sur leur ordinateur.

    **Emplacement des fichiers de suivi**:

    -   Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

    -   Serveur:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Autres éléments à prendre en considération

-   Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour configurer la journalisation et le suivi d’AGPM. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm30ops.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm30ops.md)

### Références supplémentaires

-   [Configuration de la Gestion avancée des stratégies de groupe](configuring-advanced-group-policy-management.md)

 

 






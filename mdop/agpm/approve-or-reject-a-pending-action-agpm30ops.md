---
title: Approuver ou rejeter une action en attente
description: Approuver ou rejeter une action en attente
author: dansimp
ms.assetid: 6d78989a-b600-4876-9dd9-bc6207ff2ce7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a787e032a441a8b33a48667afecfc98ec2a3642
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807830"
---
# Approuver ou rejeter une action en attente


Le responsable d’un approbateur est d’évaluer et de rejeter les demandes de création, de déploiement et de suppression d’objets de stratégie de groupe (GPO) dans les éditeurs ou réviseurs qui n’ont pas l’autorisation d’effectuer ces actions. Les rapports peuvent aider un approbateur à évaluer une nouvelle version d’un objet de stratégie de groupe.

Un compte d’utilisateur disposant du rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour approuver ou rejeter une demande en attente**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **en attente** pour afficher les objets de stratégie de groupe en attente.

3.  Cliquez avec le bouton droit sur un objet de stratégie de groupe en attente, puis cliquez sur **approuver** ou **rejeter**.

4.  Si vous approuvez le déploiement, cliquez sur **Options avancées** dans la boîte de dialogue **approuver l’opération en attente** pour examiner les liens vers l’objet de stratégie de groupe. Placez le pointeur de la souris sur un élément de l’arborescence pour afficher les détails.

    -   Par défaut, tous les liens vers l’objet GPO sont restaurés.

    -   Pour empêcher la restauration d’un lien, désactivez la case à cocher en regard de ce lien.

    -   Pour empêcher la restauration de tous les liens, décochez la case **restaurer les liaisons** dans la boîte de dialogue **déployer l’objet GPO** .

5.  Cliquez sur **Oui** ou **OK** pour confirmer l’approbation ou le rejet de l’action en attente. Si vous avez approuvé la demande, l’objet de stratégie de groupe est déplacé vers l’onglet approprié pour l’action exécutée.

    **Remarques**  Si l’adresse de messagerie d’un approbateur est incluse dans le champ **à l’adresse de messagerie** sous l’onglet **délégation** de **domaine** , l’approbateur reçoit du courrier électronique de l’alias AGPM lorsqu’un éditeur ou réviseur envoie une demande.

     

### Autres éléments à prendre en considération

-   Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer des autorisations nécessaires pour effectuer la demande d’approbation.

### Références supplémentaires

-   [Exécution de tâches d'approbateur](performing-approver-tasks-agpm30ops.md)

 

 






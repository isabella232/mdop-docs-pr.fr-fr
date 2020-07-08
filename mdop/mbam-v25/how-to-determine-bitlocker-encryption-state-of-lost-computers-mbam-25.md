---
title: Détermination de l'état de chiffrement BitLocker des ordinateurs perdus
description: Détermination de l'état de chiffrement BitLocker des ordinateurs perdus
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810577"
---
# Détermination de l'état de chiffrement BitLocker des ordinateurs perdus


Utilisez cette procédure avec le site Web d’administration et de contrôle pour déterminer les éléments suivants:

-   Le dernier état du chiffrement BitLocker connu des ordinateurs perdus ou volés

-   Le chiffrement des volumes sur un ordinateur perdu ou volé

Pour effectuer cette tâche, vous devez accéder à la zone **rapports** du site Web d’administration et de surveillance. Pour pouvoir accéder à cette zone, vous devez avoir le rôle d’utilisateur de rapport MBAM. Il est possible que vous ayez attribué un nom différent aux rôles lorsque vous les avez créés. Pour plus d’informations, reportez-vous [à planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

**Remarques**  La conformité de l’appareil est déterminée par les stratégies BitLocker déployées par votre entreprise. Il est possible que vous souhaitiez vérifier vos stratégies déployées avant d’essayer de déterminer l’état de chiffrement BitLocker d’un appareil.

 

**Pour déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus**

1.  Ouvrez un navigateur Web, puis accédez au **site Web d’administration et de surveillance**.

2.  Dans le volet gauche, sélectionnez **rapports** pour ouvrir la page rapports.

3.  Sélectionnez le **rapport de conformité**de l’ordinateur.

4.  Utilisez les champs de filtre dans le volet droit pour affiner les résultats de la recherche, puis cliquez sur **Rechercher**. Les résultats sont affichés sous votre requête de recherche.

5.  Prenez l’action appropriée, déterminée par votre politique pour les appareils perdus.



## Rubriques connexes


[Gestion de BitLocker avec MBAM2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 






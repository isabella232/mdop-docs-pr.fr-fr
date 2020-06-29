---
title: Gérer des rôles d'administrateur MBAM
description: Gérer des rôles d'administrateur MBAM
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810962"
---
# Gérer des rôles d'administrateur MBAM


Une fois l’installation de Microsoft BitLocker administration et surveillance (MBAM) terminée pour toutes les fonctionnalités du serveur, les utilisateurs administratifs doivent y avoir accès. Il est recommandé que les administrateurs qui gèrent ou utilisent les fonctionnalités d’administration de Microsoft BitLocker et de surveillance du serveur doivent être assignés aux groupes de sécurité de services de domaine, et ils doivent alors être ajoutés au groupe local d’administration MBAM approprié.

**Pour gérer les appartenances aux rôles d’administrateur MBAM**

1.  Assigner des utilisateurs à des groupes de sécurité dans les services de domaine Active Directory.

2.  Ajoutez des groupes de sécurité ActiveDirectory aux rôles pour les groupes locaux d’administration MBAM sur le serveur MBAM pour les fonctionnalités respectives.

    -   Les **administrateurs système MBAM** ont accès à toutes les fonctionnalités de MBAM dans le site Web d’administration et de surveillance de MBAM.

    -   **Les utilisateurs du support technique MBAM** ont accès aux options de gestion du TPM et de récupération des lecteurs dans le site Web d’administration et de surveillance de MBAM, mais doivent remplir tous les champs lorsqu’ils utilisent l’une des deux options.

    -   **MBAM les utilisateurs de rapports** peuvent accéder aux rapports de conformité et d’audit dans le site Web d’administration et de surveillance de MBAM.

    -   **Les utilisateurs de l’assistance technique avancée MBAM** ont accès aux options de gestion du TPM et de récupération des lecteurs dans le site Web d’administration et de surveillance de MBAM, mais ils ne sont pas tenus de remplir tous les champs lorsqu’ils utilisent l’une des options.

    Pour plus d’informations sur les rôles d’administration et de contrôle Microsoft BitLocker, voir [planification des rôles d’administrateur MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).

## Rubriques connexes


[Administration des composants de MBAM2.0](administering-mbam-20-features-mbam-2.md)

 

 






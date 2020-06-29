---
title: Gérer des rôles d'administrateur MBAM
description: Gérer des rôles d'administrateur MBAM
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804626"
---
# Gérer des rôles d'administrateur MBAM


Une fois l’installation de Microsoft BitLocker administration et surveillance (MBAM) terminée pour toutes les fonctionnalités du serveur, les utilisateurs administratifs doivent avoir accès à ces fonctionnalités serveur. Il est recommandé que les administrateurs qui gèrent ou utilisent les fonctionnalités du serveur MBAM doivent être assignés aux groupes de sécurité Active Directory, puis ces groupes doivent être ajoutés au groupe local administratif approprié MBAM.

**Pour gérer les appartenances aux rôles d’administrateur MBAM**

1.  Affectez des utilisateurs administratifs à des groupes de sécurité dans ActiveDirectoryDomain services.

2.  Ajoutez des groupes de sécurité ActiveDirectoryDomain services aux rôles pour les groupes locaux d’administration de MBAM sur le serveur d’administration et de surveillance Microsoft BitLocker pour les fonctionnalités correspondantes. Les rôles d’utilisateur sont les suivants:

    -   Les **administrateurs système MBAM** ont accès à toutes les fonctionnalités d’administration et de surveillance de Microsoft BitLocker dans le site Web d’administration MBAM.

    -   **Les utilisateurs de matériel MBAM** ont accès aux fonctionnalités de compatibilité matérielle dans le site Web d’administration MBAM.

    -   **Les utilisateurs du support technique MBAM** ont accès aux options de gestion du TPM et de récupération des lecteurs dans le site Web d’administration MBAM, mais doivent remplir tous les champs lorsqu’ils utilisent une des deux options.

    -   **MBAM les utilisateurs de rapports** ont accès aux rapports de conformité et d’audit figurant sur le site Web d’administration MBAM.

    -   Les options de **support technique avancée MBAM** ont accès aux options gérer le TPM et récupération de lecteur du site Web d’administration MBAM. Ces utilisateurs ne sont pas obligés de renseigner tous les champs lorsqu’ils utilisent l’une des options.

    Pour plus d’informations sur les rôles d’administration et de contrôle Microsoft BitLocker, voir [planification des rôles d’administrateur MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

## Rubriques connexes


[Administration des composants de MBAM1.0](administering-mbam-10-features.md)

 

 






---
title: Déploiement d'objets de stratégie de groupe MBAM1.0
description: Déploiement d'objets de stratégie de groupe MBAM1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808622"
---
# Déploiement d'objets de stratégie de groupe MBAM1.0


Pour réussir le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM), vous devez d’abord déterminer les stratégies de groupe que vous utiliserez dans votre implémentation de MBAM. Pour plus d’informations sur les différentes stratégies disponibles, voir [planification des exigences de la stratégie de groupe MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md). Une fois que vous avez déterminé les stratégies que vous allez utiliser, vous devez utiliser le modèle de stratégie de groupe MBAM 1,0 pour créer et déployer un ou plusieurs objets de stratégie de groupe (GPO) incluant les paramètres de stratégie MBAM.

## Installer le modèle de stratégie de groupe MBAM 1,0


Outre la fourniture de fonctionnalités relatives au serveur de MBAM, l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM. Vous pouvez installer ce modèle sur n’importe quel ordinateur qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).

[Installation du modèle de stratégie de groupe MBAM1.0](how-to-install-the-mbam-10-group-policy-template.md)

## Déploiement des paramètres de stratégie de groupe de MBAM 1,0


Après avoir créé les objets de stratégie de groupe nécessaires, vous devez déployer les paramètres de stratégie de groupe MBAM sur les ordinateurs clients de votre organisation.

[Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0](how-to-edit-mbam-10-gpo-settings.md)

## Afficher l’MBAM panneau de configuration dans Windows


Comme MBAM propose un panneau de configuration MBAM personnalisé qui peut remplacer le panneau de configuration Windows BitLocker par défaut, vous pouvez également choisir de masquer le panneau de configuration BitLocker par défaut aux utilisateurs finaux à l’aide d’une stratégie de groupe.

[Masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## Autres ressources pour le déploiement d’objets de stratégie de groupe MBAM 1,0


[Déploiement de MBAM1.0](deploying-mbam-10.md)

 

 






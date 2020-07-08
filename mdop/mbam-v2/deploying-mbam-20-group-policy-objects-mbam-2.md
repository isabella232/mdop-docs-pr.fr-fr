---
title: Déploiement d'objets de stratégie de groupe MBAM2.0
description: Déploiement d'objets de stratégie de groupe MBAM2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809989"
---
# Déploiement d'objets de stratégie de groupe MBAM2.0


Pour réussir le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM), vous devez d’abord déterminer les stratégies de groupe que vous utiliserez dans votre implémentation de l’administration et de la surveillance de Microsoft BitLocker. Pour plus d’informations sur les différentes stratégies disponibles, voir [planification des exigences de la stratégie de groupe MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) . Lorsque vous déterminez les stratégies que vous allez utiliser, vous devez créer et déployer un ou plusieurs objets de stratégie de groupe qui incluent les paramètres de stratégie pour MBAM à l’aide du modèle de stratégie de groupe MBAM 2,0.

## Installer le modèle de stratégie de groupe MBAM 2,0


Outre les fonctionnalités d’administration et de surveillance de Microsoft BitLocker associées au serveur, l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM. Ce modèle peut être installé sur n’importe quel ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).

[Installation du modèle de stratégie de groupe MBAM2.0](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## Déploiement des paramètres de stratégie de groupe de MBAM 2,0


Après avoir créé les objets de stratégie de groupe nécessaires, vous devez déployer les paramètres de stratégie de groupe MBAM sur les ordinateurs clients de votre organisation.

[Procédure de modification des paramètres d'objet de stratégie de groupe MBAM2.0](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## Afficher l’MBAM panneau de configuration dans Windows


Comme MBAM propose un panneau de configuration MBAM personnalisé qui peut remplacer le panneau de configuration Windows BitLocker par défaut, vous pouvez également choisir de masquer le panneau de configuration BitLocker par défaut aux utilisateurs finaux à l’aide d’une stratégie de groupe.

[Comment masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## Autres ressources pour le déploiement d’objets de stratégie de groupe MBAM 2,0


[Déploiement de MBAM2.0](deploying-mbam-20-mbam-2.md)

 

 






---
title: Application de correctifs sur MBAM2.5SP1
description: Application de correctifs sur MBAM2.5SP1
ms.author: dansimp
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: ea564d93a3eec6a46ec7d4c1be0f794abba9c93e
ms.sourcegitcommit: 8ecbf818a6ff2ddafd80b93614c01256484737ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2020
ms.locfileid: "11014988"
---
# Application de correctifs sur MBAM2.5SP1
Cette rubrique décrit la procédure d’application des correctifs pour l’administration et la surveillance de Microsoft BitLocker (MBAM) Server 2,5 SP1

### Avant de commencer, téléchargez la dernière version du correctif de l’administration et de la surveillance de BitLocker (MBAM) Server 2,5 SP1
[Pack d’optimisation de bureau](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> Pour plus d’informations sur les versions d’Hotfix, voir le [graphique de version MBAM](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).

#### Procédure de mise à jour du serveur MBAM pour l’environnement MBAM existant 
1. Supprimez la fonctionnalité du serveur MBAM (pour ce faire, ouvrez l’outil Configuration de MBAM Server, puis sélectionnez Supprimer des fonctionnalités).
2. Supprimez MDOP MBAM du panneau de configuration | Programmes et fonctionnalités.
3. Installez les composants serveur MBAM 2,5 SP1 RTM.
4. Installez le dernier correctif cumulatif MBAM 2,5 SP1.
5. Configurer les fonctionnalités d’MBAM à l’aide de MBAM Server Configurator.

#### Procédures d’installation du nouveau correctif MBAM 2,5 SP1 pour le serveur
Reportez-vous au document pour l' [installation d’un nouveau serveur](deploying-the-mbam-25-server-infrastructure.md).

---
title: Installation du modèle de stratégie de groupe MBAM2.0
description: Installation du modèle de stratégie de groupe MBAM2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811645"
---
# Installation du modèle de stratégie de groupe MBAM2.0


Outre les fonctionnalités d’administration et de surveillance de l’application Microsoft BitLocker associées au serveur, l’application de configuration du serveur inclut un modèle de stratégie de groupe d’administration et de surveillance de BitLocker. Ce modèle peut être installé sur n’importe quel ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou la gestion avancée des stratégies de groupe (AGPM).

Les étapes suivantes expliquent comment installer le modèle de stratégie de groupe MBAM.

**Remarques**  Vérifiez que vous utilisez la configuration de 32 bits sur les serveurs 32 bits et la configuration 64 bits sur les serveurs 64.

 

**Pour installer le modèle de stratégie de groupe MBAM**

1.  Sur le serveur sur lequel vous souhaitez installer MBAM, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation d’MBAM.

2.  Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.

3.  Lisez et acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

4.  Par défaut, toutes les fonctionnalités d’administration et de contrôle Microsoft BitLocker sont sélectionnées pour l’installation. Désactivez toutes les options de fonctionnalité sauf pour le **modèle de stratégie**, puis cliquez sur **suivant** pour continuer l’installation.

    **Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes. Si toutes les conditions préalables sont remplies, l’installation continue. Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**. Une fois que toutes les conditions préalables sont remplies, l’installation reprend.

     

5.  Pour obtenir des instructions détaillées sur la manière d’installer les modèles, voir [Comment télécharger et déployer des modèles de stratégie de groupe MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).

6.  Lorsque l’Assistant Configuration de l’administration et de la surveillance de Microsoft BitLocker affiche les pages d’installation pour les fonctionnalités sélectionnées, cliquez sur **Terminer** pour fermer MBAM.

## Rubriques connexes


[Déploiement d'objets de stratégie de groupe MBAM2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 






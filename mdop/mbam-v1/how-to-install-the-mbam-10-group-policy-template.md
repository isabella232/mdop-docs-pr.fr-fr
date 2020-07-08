---
title: Installation du modèle de stratégie de groupe MBAM1.0
description: Installation du modèle de stratégie de groupe MBAM1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811094"
---
# Installation du modèle de stratégie de groupe MBAM1.0


Outre les fonctionnalités liées au serveur de l’administration et de la surveillance de BitLocker Microsoft (MBAM), l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM. Vous pouvez installer ce modèle sur n’importe quel ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).

Les étapes suivantes expliquent comment installer le modèle de stratégie de groupe MBAM.

**Remarques**  Vérifiez que vous utilisez la configuration de 32 bits sur les serveurs 32 bits et la configuration 64 bits sur les serveurs 64.

 

**Pour installer le modèle de stratégie de groupe MBAM**

1.  Démarrez l’Assistant Installation de MBAM; dans la page Bienvenue, cliquez sur **installer** .

2.  Lisez et acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

3.  Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation. Désactivez toutes les options de fonctionnalité sauf pour le **modèle de stratégie**, puis cliquez sur **suivant** pour continuer l’installation.

    **Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes. Si toutes les conditions préalables sont remplies, l’installation continue. Si un prérequis manquant est détecté, vous devez résoudre le prérequis manquant, puis cliquez **à nouveau sur vérifier les conditions préalables**. Une fois que toutes les conditions préalables sont remplies, l’installation reprend.

     

4.  À l’issue de l’Assistant Installation de MBAM, cliquez sur **Terminer** pour fermer MBAM de configuration des fonctionnalités sélectionnées.

## Rubriques connexes


[Déploiement d'objets de stratégie de groupe MBAM1.0](deploying-mbam-10-group-policy-objects.md)

 

 






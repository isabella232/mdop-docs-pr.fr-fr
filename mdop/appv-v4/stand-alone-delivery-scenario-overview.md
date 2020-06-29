---
title: Présentation du scénario de distribution autonome
description: Présentation du scénario de distribution autonome
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806254"
---
# Présentation du scénario de distribution autonome


Le scénario de remise autonome est une solution idéale pour les environnements dans lesquels une connectivité à faible bande passante ou aucune connectivité ne limite la capacité du client de bureau de virtualisation des applications à diffuser des applications à partir de serveurs centralisés. Dans ces environnements, les utilisateurs travaillent souvent à distance et les propriétaires d’appareils peuvent installer des applications à l’aide des fichiers du programme d’installation Windows.

Vous pouvez utiliser le Sequencer Application Virtualization pour créer des applications séquencées incluant des fichiers Windows Installer. Ces packages incluent les applications virtualisées, les informations de composition et les routines de programme d’installation nécessaires pour l’installation des packages sur les systèmes clients. Le programme d’installation ajoute le package d’application virtuel au client de bureau Microsoft Application Virtualization. Les informations de composition sont configurées pour charger des applications à partir d’un emplacement local plutôt que de les diffuser sur un réseau étendu. Les utilisateurs peuvent se connecter temporairement à un réseau pour récupérer les fichiers Windows Installer ou les exécuter à partir d’un DVD.

Le scénario de remise autonome fournit aux utilisateurs les avantages suivants:

-   Opération de déploiement simple.

-   Réseau et serveurs non nécessaires à l’exécution.

-   Applications déjà mises en cache et disponibles pour tous les utilisateurs.

Le scénario de remise autonome comporte les limitations suivantes:

-   Les rapports automatisés intégrés ne sont pas disponibles; les rapports doivent être générés à l’aide d’outils de création de rapports externes.

-   Les applications doivent être transmises au client manuellement, comme les fichiers Windows Installer d’origine.

## Rubriques connexes


[Procédure pour installer manuellement Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Procédure pour publier une application virtuelle sur le client](how-to-publish-a-virtual-application-on-the-client.md)

 

 






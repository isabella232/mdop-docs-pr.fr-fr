---
title: Configurer la configuration requise de l'environnement
description: Configurer la configuration requise de l'environnement
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811760"
---
# Configurer la configuration requise de l'environnement


Avant de déployer et d’exécuter Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, vous devez vous assurer que votre environnement répond aux conditions minimales requises suivantes.

**Windows7**

L’agent hôte MED-V et le module de création de package de l’espace de travail MED-V sont uniquement pris en charge dans Windows 7 ou une version ultérieure.

**Windows XP SP3**

L’agent d’invité MED-V est uniquement pris en charge par Windows XP SP3.

**.NET Framework 3,5 SP1**

Les agents d’accueil et les agents invités de MED-V et le package de l’espace de travail MED-V nécessitent Microsoft .NET Framework 3,5 SP1.

**Important**  Vous devez également installer la mise à jour [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) qui répond aux problèmes de compatibilité des applications connus.

 

**Remarques**  Vous devez installer manuellement .NET Framework 3,5 SP1 et la mise à jour KB959209 dans l’image du PC virtuel Windows que vous préparez pour une utilisation avec MED-V. Toutefois, par défaut, Microsoft .NET Framework 3,5 SP1 et la mise à jour sont inclus lorsque vous installez Windows 7 sur l’ordinateur hôte.

 

**Une infrastructure Active Directory**

La stratégie de groupe fournit la gestion et la configuration centralisées des systèmes d’exploitation, des applications et des paramètres des utilisateurs dans un environnement Active Directory.

## Rubriques connexes


[Configurer les composants requis pour l'installation](configure-installation-prerequisites.md)

[Architecture de haut niveau](high-level-architecturemedv2.md)

[Configurations prises en charge par MED-V2.0](med-v-20-supported-configurations.md)

 

 






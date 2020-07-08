---
title: Installation d'applications sur une image WindowsVirtualPC
description: Installation d'applications sur une image WindowsVirtualPC
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811993"
---
# Installation d'applications sur une image WindowsVirtualPC


Une fois que vous avez créé une image de PC virtuel Windows pour une utilisation avec la version 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V), vous pouvez installer d’autres composants utiles lors de l’exécution de MED-V, tel qu’un système de distribution de logiciels électroniques et un logiciel antivirus.

La section suivante fournit des informations pour vous aider à installer des logiciels sur l’image MED-V.

**Attention**  Pour faciliter la gestion de l’espace de travail MED-V après le déploiement, nous vous recommandons de limiter le nombre de composants installés sur l’image MED-V aux composants requis ou utiles lors de l’utilisation de MED-V. Par exemple, même si elles ne sont pas requises pour exécuter MED-V, vous pouvez installer un système ESD à utiliser ultérieurement pour l’installation d’applications sur un espace de travail et un logiciel antivirus MED-V pour la sécurité de l’image.

 

**Installation de logiciels sur une image MED-V**

1.  S’il n’est pas en cours d’exécution, ouvrez votre machine virtuelle MED-V.

    1.  Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows** , puis sur **PC virtuel Windows**.

    2.  Double-cliquez sur votre machine virtuelle MED-V.

2.  À partir du système d’exploitation de l’ordinateur virtuel, recherchez les fichiers d’installation pour le logiciel que vous voulez installer.

3.  Suivez les instructions d’installation fournies par le fabricant du logiciel.

    **Remarques**  Une fois l’installation terminée, vous devrez peut-être fermer, puis redémarrer l’ordinateur virtuel.

     

Répétez ces étapes pour tout logiciel ou application que vous souhaitez installer sur l’image MED-V. Nous vous recommandons de limiter le nombre d’applications que vous préinstallez sur l’image. Le processus recommandé pour l’installation d’applications et d’autres logiciels sur l’image consiste à préinstaller un système ESD dès maintenant et à l’utiliser ultérieurement pour déployer le logiciel sur l’image. Vous pouvez également utiliser une stratégie de groupe ou App-V pour ajouter ou supprimer des applications sur un espace de travail MED-V. Pour plus d’informations, reportez-vous [à gestion des applications déployées dans les espaces de travail MED-V](managing-applications-deployed-to-med-v-workspaces.md).

Pour plus d’informations sur l’installation de logiciels sur une image virtuelle, voir les articles suivants:

-   [Publier et utiliser des applications virtuelles](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .

-   [Aide de l’application Virtual PC Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

Une fois que vous avez installé le logiciel souhaité sur l’image MED-V, votre image est prête à être empaquetée.

## Rubriques connexes


[Configuration d'une image Windows Virtual PC pour MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Préparer une image MED-V](prepare-a-med-v-image.md)

 

 






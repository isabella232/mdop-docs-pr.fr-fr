---
title: Planification de l'implémentation d'Application Virtualization Sequencer
description: Planification de l'implémentation d'Application Virtualization Sequencer
author: dansimp
ms.assetid: 052f32fe-ad13-4921-a8ce-4a657eb2b2bf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac62991e290dcd2da1c42f025a19365bda239fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806489"
---
# Planification de l'implémentation d'Application Virtualization Sequencer


Le processus utilisé par la virtualisation des applications pour créer des applications virtuelles et des packages d’application nécessite l’utilisation d’un ordinateur sur lequel est installé le logiciel de Sequencer de virtualisation d’applications.

Pendant le processus de séquençage, le Sequencer est placé en mode moniteur et l’application à séquencé est installée sur l’ordinateur de séquençage. Ensuite, l’application séquencée est démarrée et ses fonctions les plus importantes et les plus fréquemment utilisées sont exercées afin que le processus d’analyse puisse configurer le bloc de fonctionnalités principal, qui contient le contenu minimal d’un package d’application qui est nécessaire pour qu’une application s’exécute. Une fois ces étapes terminées, le mode de surveillance est arrêté et l’application séquencé est enregistrée et testée pour vérifier l’opération correcte.

Lorsque vous choisissez les applications à choisir pour le séquençage, n’oubliez pas que certaines applications ne peuvent pas être séquencées. Celles-ci incluent certaines parties du système d’exploitation Windows, telles qu’Internet Explorer, les pilotes de périphériques et les applications qui démarrent les services au moment du démarrage.

Pour obtenir des informations détaillées sur l’installation de Sequencer, voir [Comment installer le Sequencer de virtualisation des applications](how-to-install-the-application-virtualization-sequencer.md).

**Important**  Tout le plan de processus de séquençage doit être réexaminé et approuvé par l’équipe de sécurité de votre entreprise. Les opérations de Sequencer sont généralement maintenues en dehors de l’environnement de production dans le laboratoire. C’est aussi simple que nécessaire, en fonction des besoins de votre entreprise. Le séquençage des ordinateurs doit avoir besoin d’une connectivité au réseau d’entreprise pour copier les packages finalisés sur les serveurs de production. Toutefois, étant donné qu’ils sont généralement utilisés sans protection antivirus, ils ne doivent pas se trouver sur le réseau d’entreprise non protégé (par exemple, vous pouvez utiliser un pare-feu ou un segment réseau isolé). L’utilisation de machines virtuelles configurées pour partager un réseau virtuel isolé peut également être une approche acceptable. Pour résoudre ce problème, suivez les stratégies de sécurité de votre entreprise.

 

Les étapes clés de la planification du processus de séquençage sont les suivantes:

-   Prenez en compte le nombre d’applications que vous vous attendez à traiter chaque mois, la taille de ces applications et ajoutez une allocation pour le séquençage des mises à jour ultérieures. La taille des packages peut atteindre 4 Go, compressée ou décompressée.

-   Préparez et documentez un processus méthodique et reproductible que votre organisation doit suivre lors du séquençage de chaque application. Cela doit comprendre l’utilisation d’une liste de vérification pour chaque exécution, ainsi qu’un processus de contrôle de version. Vous pouvez également utiliser un journal de suivi pour chaque application séquencée lors de l’examen des problèmes techniques potentiels d’un package.

-   Pour le séquençage des applications, utilisez des ordinateurs à forte performance qui sont optimisés pour le débit de traitement, avec au moins 4 Go de RAM et un processeur rapide (3 GHz ou plus rapide). Les disques durs rapides et l’utilisation de volumes de disque séparés peuvent également améliorer les performances. Les machines virtuelles sont idéales pour le séquençage, car elles peuvent être facilement réinitialisées, ou vous pouvez utiliser un ordinateur physique disposant d’une image saine sur une partition locale pour permettre une nouvelle image rapide après chaque opération de séquençage de package.

    **Important**  L’exécution du Sequencer App-V en mode sans échec n’est pas prise en charge.

     

-   Vérifiez que vous comprenez l’environnement d’exploitation de l’application séquencée, y compris les éléments d’intégration tels que Microsoft Office ou l’environnement d’exécution Java, car cela détermine souvent si un élément doit être installé sur l’ordinateur de séquençage avant de séquencer l’application.

-   Assurez-vous que chaque nouvelle opération de séquençage commence toujours par une nouvelle image de base. Assurez-vous que l’ordinateur de séquençage a été réinitialisé en restaurant l’image enregistrée sur un ordinateur physique ou en redémarrant un ordinateur virtuel après le rejet de toutes les modifications. L’image de base doit avoir les dernières mises à jour appliquées à partir de Windows Update avant de procéder à l’enregistrement.

-   Vous pouvez désactiver tout élément sur l’ordinateur de séquençage qui peut interférer avec le processus de surveillance de l’installation, ces analyseurs antivirus et Windows Update, car il est essentiel d’avoir une plate-forme stable lors du processus de séquençage. Dans la mesure où cette étape entraîne des risques importants pour la sécurité, assurez-vous que les précautions appropriées sont prises pour protéger l’ordinateur et le réseau ainsi que le package d’application séquencé. Nous vous recommandons d’effectuer une analyse antivirus des packages d’application avant de les séquencer.

-   Incluez un processus détaillé pour tester chaque application après le séquençage. Le test de l’application séquencée détermine s’il fonctionne correctement et est une partie essentielle du processus avant le déploiement de l’application virtualisée aux utilisateurs finaux. Dans le cadre de la dernière étape de test avant le déploiement à grande échelle aux utilisateurs finaux, vous devez également prévoir un déploiement pilote vers un groupe de test.

-   Lorsque vous testez des applications séquencées, choisissez des équipements informatiques du même type et en utilisant les mêmes systèmes d’exploitation utilisés dans l’environnement de production de l’entreprise. Tant qu’ils sont configurés correctement, des machines virtuelles ou physiques peuvent être utilisées.

## Rubriques connexes


[Configuration matérielle et logicielle requise pour Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)

[Procédure pour installer Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)

[Procédure pour mettre à niveau Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

[Vue d'ensemble de la sécurité et de la protection](security-and-protection-overview.md)

 

 






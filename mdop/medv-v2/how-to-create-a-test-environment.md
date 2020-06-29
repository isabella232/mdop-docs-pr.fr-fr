---
title: Comment créer un environnement de test
description: Comment créer un environnement de test
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812264"
---
# Comment créer un environnement de test


Vous trouverez ci-dessous des étapes et des instructions pour vous aider à créer un environnement de test que vous pouvez utiliser pour tester votre package d’espace de travail MED-V en local avant de le déployer dans l’ensemble de votre entreprise. Cette section fournit des recommandations sur la création d’un environnement de test, que ce soit manuellement ou à l’aide d’un système de distribution de logiciels électronique.

**Pour créer un environnement de test en utilisant une ESD**

1.  Utilisez la méthode de déploiement de logiciels au sein de votre entreprise pour déployer les composants nécessaires suivants sur un ordinateur de test. Installez-les dans l’ordre suivant:

    -   **PC virtuel Windows** , s’il n’est pas déjà installé. Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).

    -   **Ajouts et mises à jour pour PC virtuel**, le cas échéant. Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).

    -   **Fichier d’installation de l’agent hôte MED-v** : installation de l’agent hôte (med-v \ _HostAgent _setup fichier d’installation). Pour plus d’informations, reportez-vous à la rubrique [installation manuelle de l’agent hôte MED-V](how-to-manually-install-the-med-v-host-agent.md).

    -   **Exécutable du programme d’espace de travail MED-v, VHD et de l’installation,** créé dans le **Gestionnaire de package med-v** Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).

        **Important**  Le fichier de disque dur virtuel et de configuration doit se trouver dans le même dossier que le programme d’installation de l’espace de travail MED-V. Ensuite, installez le programme d’installation de l’espace de travail MED-V en exécutant setup.exe.

         

2.  Une fois tous les composants installés sur l’ordinateur de test, exécutez l’agent d’hébergement MED-V pour commencer la première configuration.

    Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **ordinateur de bureau Microsoft**, puis sur agent d' **hébergement MED-V**.

    **Remarques**  Si vous ne pouvez pas exécuter physiquement l’agent hôte MED-V sur l’ordinateur de test, la première fois que le programme d’installation s’exécute automatiquement au prochain redémarrage de l’ordinateur.

     

Le premier démarrage du programme d’installation et peut prendre 10 minutes ou plus pour terminer.

Pour plus d’informations sur le test de vos paramètres de configuration lors de la première exécution du programme d’installation, voir vérifier les paramètres de configuration de la [première fois](how-to-verify-first-time-setup-settings.md).

**Pour créer un environnement de test manuellement**

1.  Installez l’agent d’hébergement MED-V dans un environnement de test local incluant des éléments requis pour la fonction MED-V, tels que le PC virtuel Windows, avec des ajouts et des mises à jour. Pour plus d’informations, reportez-vous à la rubrique [installation manuelle de l’agent hôte MED-V](how-to-manually-install-the-med-v-host-agent.md).

2.  Copiez les fichiers de l’espace de travail MED-V dans votre environnement de test. Les fichiers d’espace de travail MED-V se trouvent dans le dossier de destination que vous avez spécifié dans le package de création de package de l' **espace de travail MED-v**.

    **Important**  Le fichier de disque dur virtuel et de configuration doit se trouver dans le même dossier de votre environnement de test que le programme d’installation de l’espace de travail MED-V.

     

3.  Installez l’espace de travail MED-V en exécutant setup.exe.

4.  Commencez par configurer pour la première fois en exécutant l’agent hôte MED-V.

    Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **ordinateur de bureau Microsoft**, puis sur agent d' **hébergement MED-V**.

Le premier démarrage du programme d’installation et peut prendre plusieurs minutes en fonction de la taille du VHD spécifié.

Vous êtes maintenant prêt à tester les différents paramètres de configuration, de publication d’application et de redirection d’URL que vous avez spécifiés pour votre espace de travail MED-V.

**Remarques**  Par défaut, MED-V remplace la stratégie de verrouillage de l’écran dans l’invité. Toutefois, cela ne pose pas de problème de sécurité, car l’ordinateur hôte continue à respecter la stratégie de verrouillage de l’écran.

 

## Rubriques connexes


[Comment vérifier les paramètres de première installation](how-to-verify-first-time-setup-settings.md)

[Comment tester la publication d'applications](how-to-test-application-publishing.md)

[Comment tester la redirection d'URL](how-to-test-url-redirection.md)

 

 






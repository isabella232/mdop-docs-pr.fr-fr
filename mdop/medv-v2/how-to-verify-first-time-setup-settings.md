---
title: Comment vérifier les paramètres de première installation
description: Comment vérifier les paramètres de première installation
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804668"
---
# Comment vérifier les paramètres de première installation


Pendant l’exécution de votre test de configuration pour la première fois ou après la fin de celle-ci, vous pouvez vérifier les paramètres que vous avez configurés dans votre espace de travail MED-V en effectuant les tâches suivantes.

**Remarques**  Pour plus d’informations sur la façon de surveiller la réussite de la première configuration au sein de votre entreprise après le déploiement, voir [surveiller les déploiements de l’espace de travail MED-V](monitoring-med-v-workspace-deployments.md).

 

**Pour vérifier les paramètres lors de la première configuration**

1.  Lors de la première exécution du programme d’installation, vérifiez les points suivants:

    Si vous avez spécifié le mode **inattendé** , vérifiez que l’ordinateur virtuel ne s’affiche pas lors de la première exécution du programme d’installation.

    Si vous avez spécifié le mode assistance, vérifiez que l’ordinateur virtuel apparaît et que tous les champs qui nécessitent une entrée utilisateur sont affichés.

2.  Vous pouvez également surveiller le processus de configuration de la première utilisation lors de l’affichage de l’ordinateur virtuel lors de la première exécution du programme d’installation. Pour cela, procédez comme suit:

    1.  Ouvrez la console de l’ordinateur virtuel Windows.

        Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, puis sur **PC virtuel Windows**.

    2.  Démarrez MED-V s’il n’est pas encore en cours d’exécution.

        Si ce n’est pas déjà le cas, une machine virtuelle portant le nom de l’espace de travail MED-V s’affiche dans la liste des machines virtuelles.

    3.  Double-cliquez sur la machine virtuelle MED-V pour l’ouvrir.

        Vous pouvez observer la machine virtuelle MED-V lorsque celle-ci est en cours de configuration et vous pouvez résoudre les problèmes liés à la mini-installation. Vérifiez les informations des différents écrans au fur et à mesure qu’ils sont, par exemple, la configuration des paramètres de mise en réseau, les informations de joint de domaine d’ordinateur, la configuration de l’agent invité, la configuration des paramètres personnels et l’arrêt.

    4.  L’ordinateur virtuel se ferme automatiquement à la fin de la première configuration.

        **Remarques**  Vous pouvez fermer la fenêtre de l’ordinateur virtuel à tout moment et le programme de configuration pour la première fois.

         

**Pour vérifier les paramètres après la configuration initiale**

1.  Assurez-vous que la première fois que vous avez terminé.

2.  Vérifiez que l’espace de travail MED-V est configuré correctement.

    1.  Ouvrez la console de l’ordinateur virtuel Windows.

        Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, puis sur **PC virtuel Windows**.

    2.  Double-cliquez sur l’espace de travail MED-V que vous avez installé.

        Si l’espace de travail MED-V exécute déjà une application virtuelle, vous serez peut-être invité à fermer l’application avant de pouvoir ouvrir l’ordinateur virtuel.

    3.  Dans l’espace de travail MED-V, cliquez avec le bouton droit sur **poste**de travail, puis cliquez sur **Propriétés**.

    4.  Vérifiez que l’espace de travail MED-V a rejoint le domaine approprié. S’il s’applique à votre organisation, testez la jointure de domaines en spécifiant deux domaines différents pour vérifier que le domaine invité est substitué par le domaine hôte.

    5.  Vérifiez que l’espace de travail MED-V a rejoint l’unité d’organisation du domaine que vous avez spécifiée.

    6.  Si vous avez spécifié le masque de nom de l’ordinateur, vérifiez que le nom de l’ordinateur correspond au nom spécifié.

3.  Vérifiez que les paramètres régionaux spécifiés sont corrects.

    1.  Dans l’espace de travail MED-V, cliquez sur **Démarrer** , puis sur **panneau de configuration**.

    2.  Vérifiez vos paramètres de configuration spécifiés, par exemple, **date et heure** , **Options régionales et linguistiques**.

**Remarques**  Si vous rencontrez des problèmes lors de la vérification des paramètres de configuration pour la première fois, voir [résolution des](operations-troubleshooting-medv2.md)problèmes d’opérations.

 

Une fois que vous avez vérifié que les paramètres de votre première utilisation sont corrects, vous pouvez tester les autres configurations d’espace de travail MED-V pour vérifier qu’elles fonctionnent comme prévu, par exemple pour la publication d’applications et la redirection d’URL.

Après avoir effectué tous les tests de votre package d’espace de travail MED-V et vérifié qu’il fonctionne comme prévu, vous pouvez déployer l’espace de travail MED-V dans votre entreprise.

## Rubriques connexes


[Comment tester la publication d'applications](how-to-test-application-publishing.md)

[Comment tester la redirection d'URL](how-to-test-url-redirection.md)

[Déploiement du package d'espace de travail MED-V](deploying-the-med-v-workspace-package.md)

[Gérer les paramètres de l'espace de travail MED-V](manage-med-v-workspace-settings.md)

 

 






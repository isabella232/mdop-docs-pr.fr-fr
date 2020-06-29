---
title: Planification de la compatibilité du système d'exploitation avec les applications
description: Planification de la compatibilité du système d'exploitation avec les applications
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811172"
---
# Planification de la compatibilité du système d'exploitation avec les applications


Cette rubrique vous aide à déterminer comment résoudre les problèmes de compatibilité du système d’exploitation de l’application et explique comment Microsoft Enterprise Desktop Virtualization (MED-V 2,0) fonctionne comme une solution pour votre organisation.

Cette rubrique décrit les exigences métiers pour MED-V et compare le mode MED-V au mode Windows XP et la virtualisation des applications Microsoft (App-V):

-   [Exigences métiers pour MED-V](#bkmk-whenmedv)

-   [Avantages du mode MED-V par rapport à Windows XP](#bkmk-medvvsxp)

-   [Avantages de MED-V par rapport à l’application-V](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a>Exigences métiers pour MED-V


Lorsque le service informatique de votre entreprise détermine s’il est nécessaire de procéder à la mise à niveau vers Windows 7, vous devez veiller à ses applications métier et applications métier basées sur le Web pour vous assurer qu’elles peuvent être exécutées sur le nouveau système d’exploitation. Souvent, ces applications et URL ont été créées pour fonctionner en particulier avec une version plus ancienne de Windows ou d’Internet Explorer, et des problèmes peuvent se produire lorsque vous tentez de les utiliser dans le nouveau système d’exploitation. Microsoft propose plusieurs méthodes différentes pour gérer les différents problèmes de compatibilité qui peuvent se produire lors de la mise à niveau, comme le kit de compatibilité des applications (ACT) et l’Assistant Compatibilité des programmes de Windows 7. Même si toutes les applications ont été testées à des fins de compatibilité et de correction, il est possible que certaines applications ne fonctionnent pas correctement sur Windows 7 ou soient trop onéreuses pour résoudre le problème.

À l’aide de MED-V, vous pouvez exécuter ces applications héritées par le biais d’un environnement Windows Virtual PC exécutant Windows XP. Étant donné que vous n’avez plus besoin de tester et de valider ces applications de problèmes sur le nouveau système d’exploitation avant de procéder à la mise à niveau, votre migration vers Windows 7 est beaucoup plus fluide et plus rapide.

### Utilisation de la liste de vérification MED-V

Envisagez d’utiliser MED-V si l’un des scénarios suivants vous concernent:

-   Vous êtes une grande organisation (par exemple, des utilisateurs 500, etc.), vous devez avoir un accord d’entreprise avec Microsoft et planifier la mise à niveau vers Windows 7.

-   Vous avez testé vos applications métier et avez détecté certaines qui ne sont pas compatibles avec Windows 7.

-   Vous avez résolu les problèmes de compatibilité de certains de ces applications à l’aide d’une mise à niveau de l’application ou à l’aide d’un shim fourni par Microsoft tel que le kit de compatibilité des applications (ACT), mais les problèmes de compatibilité persistent pour certaines applications.

-   Vous avez considéré l’option App-V comme option de remise des applications incompatibles et vous avez conclu qu’après l’implémentation de App-V, vous avez encore des problèmes de compatibilité liés aux systèmes d’exploitation des applications.

-   Vous avez considéré le mode Windows XP comme une solution et déterminé qu’il ne s’agit pas d’une option efficace pour les raisons suivantes:

    -   Vous voulez être en mesure de déployer des images virtuelles qui contiennent les applications de problèmes à tous les utilisateurs finaux en même temps, au lieu de les utiliser individuellement et de joindre automatiquement les images virtuelles au domaine.

    -   Vous avez décidé qu’il est beaucoup plus rentable pour gérer ces applications héritées (fournies virtuellement) et de contrôler les paramètres du PC virtuel Windows à partir d’un emplacement centralisé plutôt que sur le Bureau de chaque utilisateur final.

    -   Vous voulez être en mesure de mettre à jour et de prendre en charge les machines virtuelles en échelle au lieu de chaque ordinateur.

    -   Vous souhaitez pouvoir rediriger les URL qui s’exécutent mieux sur une version antérieure d’Internet Explorer vers les machines virtuelles et gérer facilement la redirection d’URL ultérieurement.

-   Vous avez déterminé qu’il serait plus rentable et utile de procéder à la mise à niveau vers Windows 7 dès que possible et de décider de différer la résolution des problèmes de compatibilité restants jusqu’à une date ultérieure, sachant qu’une solution est disponible dans MED-V.

## <a href="" id="bkmk-medvvsxp"></a> Avantages du mode MED-V par rapport à Windows XP


Le PC virtuel Windows pour Windows 7 vous permet d’exécuter plusieurs versions d’un système d’exploitation en même temps sur un seul appareil et est incluse dans Windows 7 Professionnel Edition ou version ultérieure.

Le mode Windows XP exploite le PC virtuel Windows en fournissant une image Windows XP préconfigurée qui vous permet de créer un environnement Windows XP virtuel. Dans cet environnement virtuel, vous pouvez installer manuellement des applications qui ne sont pas compatibles avec Windows 7 et qui s’exécutent en toute transparence depuis votre bureau via un PC virtuel Windows.

**Le mode Windows XP vous permet d’effectuer les opérations suivantes:**

-   Exécutez des applications compatibles avec Windows XP à l’intérieur d’un ordinateur virtuel qui s’exécute sur un ordinateur virtuel Windows.

-   Publiez ces applications sur le menu du programme ou du Bureau de l’hôte.

Si vous voulez fournir ces machines virtuelles à une grande échelle dans le cadre d’une migration d’entreprise vers Windows 7, vous devez être en mesure de déployer rapidement les machines virtuelles, de les mettre en place et de les personnaliser efficacement, de contrôler leurs paramètres et de les prendre en charge facilement.

MED-V repose sur le mode Windows XP pour garantir la compatibilité des applications à l’échelle de l’entreprise. Le mode Windows XP étant limité à la fourniture de fonctionnalités d’application virtuelles pour les particuliers et les petites entreprises, MED-V autorise les déploiements à grande échelle d’images Windows XP préconfigurées sur tout le réseau d’entreprise. Il fournit une solution de gestion adaptée à l’entreprise pour la configuration, le déploiement et la maintenance de ces espaces de travail MED-V. MED-V fournit également à enterpriseadministrators un ensemble de stratégies pour contrôler l’utilisation des images. Cela inclut les utilisateurs qui ont accès à des applications spécifiques au sein de ces images.

**L’utilisation de MED-V vous permet d’effectuer les opérations suivantes:**

-   Effectuez la mise à niveau vers votre nouveau système d’exploitation sans tester et résoudre chaque application ou URL incompatible.

-   Déploiement d’images Windows XP virtuelles qui sont automatiquement jointes au domaine et personnalisées par utilisateur.

-   Fournir des informations sur les applications et la redirection d’URL aux utilisateurs.

-   Contrôle des paramètres du PC virtuel Windows.

-   Maintenir et prendre en charge les points de terminaison via le suivi et la résolution des problèmes.

-   Assurez-vous que les ordinateurs invités sont corrigés, même en cas de suspension.

-   Automatiser la création de machines virtuelles par utilisateur et l’initialisation de Sysprep.

-   Diagnostiquer facilement les problèmes sur les ordinateurs hôte et invités.

-   Gérez en toute transparence des ordinateurs invités connectés via le mode NAT de l’ordinateur virtuel Windows.

## <a href="" id="bkmk-medvvsappv"></a>Avantages de MED-V par rapport à l’application-V


MED-V et App-V sont deux technologies très différentes qui peuvent facilement fonctionner ensemble pour résoudre les problèmes de compatibilité de votre système d’exploitation. En utilisant App-V, vous créez un package individualisé pour chaque application, chacun d’eux étant alors maintenu indépendamment des autres. Chaque application virtuelle peut ensuite être envoyée immédiatement à l’utilisateur final, ce qui est très utile pour une stratégie de déploiement de Windows 7.

MED-V ne gère pas les applications individuellement. Au lieu de cela, il crée une instance supplémentaire de Windows XP sur le même ordinateur de bureau exécutant Windows 7. Vous pouvez installer autant d’applications que nécessaire dans cette image virtuelle et gérer l’image comme vous le feriez pour n’importe quel autre bureau de votre organisation.

De plus, vous pouvez utiliser MED-V avec App-V de façon à ce que les applications virtuelles exécutées par le biais d’App-v soient installées, publiées et gérées à l’aide de MED-V.

## Rubriques connexes


[Définir et planifier votre déploiement MED-V](define-and-plan-your-med-v-deployment.md)

 

 






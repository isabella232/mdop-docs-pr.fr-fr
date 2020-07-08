---
title: Gérer la compatibilité matérielle
description: Gérer la compatibilité matérielle
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804638"
---
# Gérer la compatibilité matérielle


Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) peut collecter des informations sur le fabricant et le modèle d’ordinateurs clients après le déploiement de la stratégie de groupe autoriser le contrôle de compatibilité matérielle. Si vous configurez cette stratégie, l’agent MBAM rapporte les informations sur la marque et le modèle de l’ordinateur au serveur MBAM lorsque le client MBAM est déployé sur un ordinateur client.

La fonctionnalité de compatibilité matérielle est utile si votre organisation a des matériels informatiques ou des ordinateurs plus anciens qui ne prennent pas en charge les puces de module de plateforme sécurisée (TPM). Dans ces cas, vous pouvez utiliser la fonctionnalité de compatibilité matérielle pour vous assurer que le chiffrement BitLocker est appliqué uniquement aux modèles d’ordinateur qui le prennent en charge. Si tous les ordinateurs de votre organisation prennent en charge BitLocker, vous n’avez pas besoin d’utiliser la fonctionnalité de compatibilité matérielle.

**Remarques**  Par défaut, la fonctionnalité de compatibilité matérielle MBAM n’est pas activée. Pour l’activer, sélectionnez la fonctionnalité **compatibilité matérielle** sous la fonctionnalité **administration et analyse du serveur** lors de l’installation. Pour plus d’informations sur la configuration et la configuration de la compatibilité matérielle, reportez-vous à [la rubrique déploiement de l’infrastructure du serveur MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).

 

La fonctionnalité de compatibilité matérielle fonctionne de la manière suivante.

****

1.  L’agent client MBAM Découvre des informations d’ordinateur de base, telles que le fabricant, le modèle, le BIOS, la version du BIOS, le module de plateforme sécurisée et la version TPM, puis transmet ces informations au serveur MBAM.

2.  Le serveur MBAM génère une liste de modèles et de modèles d’ordinateur client pour vous permettre de distinguer les personnes qui peuvent ou ne peuvent pas prendre en charge BitLocker.

3.  Les agents clients MBAM déployés dans l’entreprise effectuent automatiquement la mise à jour de cette liste à l’aide de tous les nouveaux modèles et modes d’ordinateur identifiés avec l’état **inconnu**. Un administrateur peut ensuite utiliser le site Web d’administration de MBAM pour modifier les entrées de liste afin de spécifier une marque et un modèle d’ordinateur particulier comme **compatible** ou **incompatible**.

4.  Pour que l’agent client MBAM commence à chiffrer un lecteur, l’agent vérifie d’abord la compatibilité de chiffrement BitLocker du matériel sur lequel il s’exécute.

    -   Si le matériel est marqué comme étant compatible, le processus de chiffrement BitLocker démarre. MBAM revérifiera également l’état de compatibilité matérielle de l’ordinateur une fois par jour.

    -   Si le matériel est marqué comme incompatible, l’agent enregistre un événement et transmet un état «matériel exempté» dans le cadre du rapport de conformité. L’agent vérifie chaque semaine pour déterminer si l’État a changé en «compatible».

    -   Si le matériel est marqué comme inconnu, le processus de chiffrement BitLocker ne démarre pas. L’agent client MBAM revérifiera l’état de compatibilité matérielle de l’ordinateur une fois par jour.

**Avertissement**  Si l’agent client MBAM tente de chiffrer un ordinateur qui ne prend pas en charge le chiffrement de lecteur BitLocker, il est possible que l’ordinateur soit endommagé. Assurez-vous que la fonctionnalité de compatibilité matérielle est correctement configurée lorsque votre organisation dispose d’un matériel ancien qui ne prend pas en charge BitLocker.

 

**Pour gérer la compatibilité du matériel**

1.  Ouvrez un navigateur Web, puis accédez au site Web d’administration et de contrôle de Microsoft BitLocker. Dans la barre de menus de gauche, sélectionnez **matériel** .

2.  Dans le volet droit, cliquez sur **recherche avancée**, puis filtrez pour afficher une liste de tous les modèles d’ordinateur dont le statut de **fonctionnalité** est **inconnu**. La liste des modèles d’ordinateur correspondant au critère de recherche s’affiche. Les administrateurs peuvent ajouter, modifier ou supprimer de nouveaux types d’ordinateurs à partir de cette page.

3.  Vérifiez chaque configuration matérielle inconnue pour déterminer si la configuration doit être **compatible** ou **incompatible**.

4.  Sélectionnez une ou plusieurs lignes, puis cliquez sur **définir** la compatibilité ou sur définir **incompatible** pour définir la compatibilité BitLocker, le cas échéant, pour les modèles d’ordinateurs sélectionnés. S’il est défini sur **compatible**, BitLocker tente d’appliquer une stratégie de chiffrement de lecteur sur des ordinateurs qui correspondent au modèle pris en charge. S’il est défini sur **incompatible**, BitLocker n’applique pas la stratégie de chiffrement de lecteur sur ces ordinateurs.

    **Remarques**  Après avoir configuré un modèle d’ordinateur comme compatible, il peut s’écouler plus de 24 heures pour que le client MBAM commence le chiffrement BitLocker sur les ordinateurs correspondant à ce modèle matériel.

     

5.  Les administrateurs doivent surveiller régulièrement la liste de compatibilité matérielle pour passer en revue les nouveaux modèles détectés par l’agent MBAM, puis mettre à jour leur paramètre de compatibilité sur **compatible** ou **incompatible** , le cas échéant.

## Rubriques connexes


[Administration des composants de MBAM1.0](administering-mbam-10-features.md)

 

 






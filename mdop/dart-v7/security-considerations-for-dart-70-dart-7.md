---
title: Considérations relatives à la sécurité pour DaRT7.0
description: Considérations relatives à la sécurité pour DaRT7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809533"
---
# Considérations relatives à la sécurité pour DaRT7.0


Microsoft Diagnostics and Recovery Tools (DaRT) 7 inclut une fonctionnalité qui permet à un administrateur d’exécuter les outils DaRT à distance pour résoudre les problèmes sur un ordinateur d’utilisateur final. Dans les versions précédentes de DaRT, un technicien du support technique ou un administrateur devait se trouver physiquement sur un ordinateur d’un utilisateur final et démarrer dans DaRT en utilisant le CD ou DVD qui incluait l’image de récupération DaRT. À présent, le technicien de support technique ou l’administrateur peut effectuer les mêmes procédures à distance.

Dans DaRT7, en plus de graver un CD ou un DVD, vous pouvez désormais enregistrer l’image ISO (International Organization for Standardization) sur une clé USB. Vous pouvez également placer l’image ISO sur un réseau ou inclure son contenu comme partition de récupération sur le disque dur de votre ordinateur.

La fonctionnalité de **connexion à distance** de DaRT7 permet aux utilisateurs finaux d’accéder au DART en utilisant l’une de ces nouvelles méthodes de déploiement. C’est pourquoi il est plus facile de démarrer DaRT et d’accéder aux outils DaRT.

Les nouvelles fonctionnalités de DaRT7 fournissent une plus grande flexibilité dans le mode d’utilisation de DaRT dans votre entreprise. Toutefois, ils créent également un ensemble de problèmes de sécurité qui doivent être résolus. Nous vous recommandons de prendre en compte les conseils de sécurité suivants lorsque vous configurez DaRT.

## Pour garantir la sécurité lors de la création de l’image de récupération DaRT


Lorsque vous créez l’image de récupération DaRT, vous pouvez sélectionner les outils que vous souhaitez inclure. Pour des raisons de sécurité, vous souhaiterez peut-être limiter l’accès de l’utilisateur final aux outils DaRT plus puissants, tels que l’effacement de disque et Locksmith. Dans DaRT7, vous pouvez désactiver certains outils lors de la configuration tout en les rendant accessibles aux agents de support technique lorsque l’utilisateur final démarre la fonctionnalité de connexion à distance.

Vous pouvez même configurer l’image DaRT de telle sorte que la possibilité de démarrer une session de connexion à distance est le seul outil disponible pour un utilisateur final.

**Important**  Une fois la connexion distante établie, tous les outils que vous avez inclus dans l’image de récupération, y compris ceux qui ne sont pas disponibles pour l’utilisateur final, deviennent disponibles pour l’agent du support technique fonctionnant sur l’ordinateur de l’utilisateur final.

 

Pour plus d’informations sur l’ajout d’outils dans l’image de récupération DaRT, voir [utilisation de l’Assistant image de récupération DART pour créer l’image de récupération](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).

## Pour garantir la sécurité par le chiffrement de l’image de récupération DaRT


Si vous utilisez l’une des options de déploiement nouvelles dans DaRT7, par exemple, l’enregistrement sur un lecteur flash USB ou la création d’une partition distante ou d’une partition de récupération, vous pouvez inclure la méthode de chiffrement de lecteur préférée de votre entreprise sur la norme ISO. Cela permet de s’assurer qu’un utilisateur final ne peut pas utiliser les fonctionnalités de DaRT pour accéder à l’image de récupération. Par ailleurs, il est également certain que les utilisateurs non autorisés ne peuvent pas démarrer dans DaRT sur des ordinateurs qui appartiennent à une autre personne.

Votre méthode de chiffrement doit être déployée et activée sur tous les ordinateurs.

**Remarques**  DaRT7 prend en charge BitLocker en mode natif.

 

## Pour garantir la sécurité entre deux ordinateurs lors de la connexion à distance


Par défaut, la communication entre deux ordinateurs ayant établi une session de **connexion à distance** n’est pas chiffrée. Par conséquent, pour renforcer la sécurité entre les deux ordinateurs, nous vous conseillons de faire en sorte que les deux ordinateurs font partie du même réseau.

## Rubriques connexes


[Opérations de DaRT7.0](operations-for-dart-70-new-ia.md)

 

 






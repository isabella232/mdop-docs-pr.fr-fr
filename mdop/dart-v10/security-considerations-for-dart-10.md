---
title: Considérations relatives à la sécurité pour DaRT10
description: Considérations relatives à la sécurité pour DaRT10
author: dansimp
ms.assetid: c653daf1-f12a-4667-98cc-f0c89fa38e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f10ecf81021d41fbc08b288573c05a8d64c47d7c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809725"
---
# Considérations relatives à la sécurité pour DaRT10


Cette rubrique fournit une vue d’ensemble sur les comptes et les groupes, les fichiers journaux et les autres considérations relatives à la sécurité de Microsoft Diagnostics and Recovery Tools (DaRT) 10. Pour plus d’informations, suivez les liens fournis dans cet article.

## Considérations générales en matière de sécurité


**Comprenez les risques en matière de sécurité**. DaRT 10 inclut des fonctionnalités qui permettent à un administrateur ou à un service de support technique d’exécuter les outils DaRT à distance pour résoudre les problèmes sur un ordinateur d’utilisateur final. De plus, vous pouvez enregistrer l’image ISO (International Organization for Standardization) sur un lecteur flash USB ou placer l’image ISO sur un réseau afin d’inclure son contenu comme partition de récupération sur le disque dur de l’ordinateur. Ces fonctionnalités permettent d’offrir une plus grande souplesse et de créer des risques de sécurité potentiels que vous devez prendre en compte lors de la configuration de DaRT.

**Sécurisez vos ordinateurs de façon sécurisée**. Lorsque des administrateurs et des travailleurs de bureau d’assistance ne sont pas physiquement sur leur ordinateur, ils doivent verrouiller leurs ordinateurs et utiliser un écran de veille sécurisé.

**Appliquez les mises à jour de sécurité les plus récentes à tous les ordinateurs**. Restez informé des nouvelles mises à jour de systèmes d’exploitation en vous abonnant au service de notification de sécurité ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).

## Limiter l’accès des utilisateurs finaux aux outils DaRT


Lorsque vous créez l’image de récupération DaRT, vous pouvez sélectionner les outils que vous souhaitez inclure. Pour des raisons de sécurité, vous souhaiterez peut-être limiter l’accès de l’utilisateur final aux outils DaRT plus puissants, tels que l’effacement de disque et Locksmith. Dans DaRT 10, vous pouvez désactiver certains outils lors de la configuration tout en les rendant accessibles aux travailleurs du Bureau lorsque l’utilisateur final démarre la fonction de connexion à distance.

Vous pouvez même configurer l’image DaRT de telle sorte que la possibilité de démarrer une session de connexion à distance est le seul outil disponible pour un utilisateur final.

**Important**  Une fois la connexion distante établie, tous les outils que vous avez inclus dans l’image de récupération, y compris ceux qui ne sont pas disponibles pour l’utilisateur final, sont mis à la disposition de tout travailleur du support technique qui travaille sur l’ordinateur de l’utilisateur final.

 

Pour plus d’informations sur l’ajout d’outils dans l’image de récupération DaRT, voir [vue d’ensemble des outils dans DART 10](overview-of-the-tools-in-dart-10.md).

## Sécuriser l’image de récupération DaRT


Si vous déployez l’image de récupération DaRT en l’enregistrant sur un disque mémoire USB ou en créant une partition distante ou une partition de récupération, vous souhaiterez peut-être inclure la méthode de chiffrement de lecteur préférée de votre entreprise sur la norme ISO. Le chiffrement de l’ISO permet aux utilisateurs finaux de s’assurer que les utilisateurs finaux ne peuvent pas utiliser la fonctionnalité DaRT s’ils accèdent à l’image de récupération, de sorte que les utilisateurs non autorisés ne peuvent pas démarrer dans DaRT sur des ordinateurs qui appartiennent à une autre personne. Si vous utilisez une méthode de chiffrement, assurez-vous de la déployer et de l’activer sur tous les ordinateurs.

**Remarques**  DaRT 10 prend en charge BitLocker en mode natif.

 

Pour inclure le chiffrement de lecteur, ajoutez les fichiers de solution de chiffrement lors de la création de l’image de récupération. Votre solution de chiffrement doit être capable de s’exécuter sur WinPE. Les utilisateurs finaux qui démarrent à partir de l’ISO peuvent alors accéder à cette solution de chiffrement et débloquer le lecteur.

## Préservation de la sécurité entre deux ordinateurs lorsque vous utilisez une connexion à distance.


Par défaut, la communication entre deux ordinateurs ayant établi une session de **connexion à distance** n’est pas chiffrée. Par conséquent, pour renforcer la sécurité entre les deux ordinateurs, nous vous conseillons de faire en sorte que les deux ordinateurs font partie du même réseau.

## Rubriques connexes


[Sécurité et confidentialité pour DaRT10](security-and-privacy-for-dart-10.md)

 

 






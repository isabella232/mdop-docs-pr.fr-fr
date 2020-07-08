---
title: À propos de la puce TPM de l'ordinateur
description: À propos de la puce TPM de l'ordinateur
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810013"
---
# À propos de la puce TPM de l'ordinateur


BitLocker fournit une protection supplémentaire lorsqu’il est utilisé avec un processeur de module de plateforme sécurisée (TPM). Le module de plateforme sécurisée est un composant matériel qui est installé sur de nombreux ordinateurs plus récents par les fabricants d’ordinateurs. Le programme d’administration et de surveillance de BitLocker utilise BitLocker, ainsi que le processeur du TPM, pour vous aider à fournir une protection supplémentaire de vos données et pour vous assurer que votre ordinateur n’a pas été falsifié.

## Comment configurer votre TPM


Lorsque vous démarrez l’Assistant chiffrement de lecteur BitLocker sur votre ordinateur, BitLocker vérifie s’il s’agit d’un processeur de TPM si votre organisation a configuré BitLocker pour utiliser un processeur de TPM. Si BitLocker trouve un processeur de TPM compatible, vous pouvez être invité à redémarrer votre ordinateur pour activer le processeur du TPM. Dès que vous avez redémarré votre ordinateur, suivez les instructions pour configurer le processeur du TPM dans le BIOS (le BIOS est une couche pré-Windows de votre logiciel informatique).

Une fois BitLocker configuré, vous pouvez accéder à des informations supplémentaires sur le processeur du TPM en ouvrant l’outil options de chiffrement BitLocker dans le panneau de configuration Windows et en sélectionnant **administration du TPM**.

**Remarques**  Vous devez disposer des informations d’identification d’administration sur votre ordinateur pour accéder à cet outil.

 

Dans un échec de module de plateforme sécurisée, une modification du BIOS ou certaines mises à jour Windows, BitLocker verrouille votre ordinateur et vous demandent de contacter l’assistance technique pour la déverrouiller. Vous devez indiquer le nom de votre ordinateur ainsi que le domaine de votre ordinateur. Le support technique peut vous donner un fichier de mot de passe qui peut être utilisé pour déverrouiller votre ordinateur.

## Résolution des problèmes liés au TPM


En cas d’échec du module de plateforme sécurisée (TPM), de changement du BIOS ou de certaines mises à jour Windows, BitLocker verrouille votre ordinateur et vous demande de contacter l’assistance technique pour le déverrouiller. Vous devez indiquer le nom de votre ordinateur ainsi que le domaine de votre ordinateur. Le support technique peut vous donner un fichier de mot de passe que vous pouvez utiliser pour déverrouiller votre ordinateur.

## Rubriques connexes


[Aider les utilisateurs finaux à gérer BitLocker](helping-end-users-manage-bitlocker.md)

[Utilisation de votre code PIN ou de votre mot de passe](using-your-pin-or-password.md)

 

 






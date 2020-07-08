---
title: Meilleures pratiques de sécurité pour les opérations de MED-V
description: Meilleures pratiques de sécurité pour les opérations de MED-V
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811130"
---
# Meilleures pratiques de sécurité pour les opérations de MED-V


En tant qu’administrateur autorisé, vous êtes tenu de protéger les informations des utilisateurs et de préserver la sécurité de votre organisation pendant et après le déploiement d’espaces de travail MED-V. Prenez en particulier en considération les points suivants:

**Personnalisation d’Internet Explorer dans l’espace de travail MED-V**. Les versions antérieures du système d’exploitation Windows et d’Internet Explorer ne sont pas aussi sécurisées que les versions actuelles. Par conséquent, Internet Explorer dans l’espace de travail MED-V est configuré pour empêcher la navigation et d’autres activités susceptibles de poser des problèmes de sécurité. Par ailleurs, le paramètre de la zone de sécurité Internet pour Internet Explorer dans l’espace de travail MED-V est défini sur le niveau le plus élevé. Par défaut, ces deux configurations sont définies dans le gestionnaire de package d’espace de travail MED-V lors de la création de votre package d’espace de travail MED-V.

À l’aide du kit d’administration d’Internet Explorer (IEAK) ou en modifiant les valeurs par défaut dans le gestionnaire de package MED-V, vous pouvez personnaliser Internet Explorer dans l’espace de travail MED-V. Sachez que si vous personnalisez Internet Explorer dans l’espace de travail MED-V de telle sorte qu’il soit moins sécurisé, vous pouvez exposer votre organisation aux risques en matière de sécurité présents dans les versions antérieures d’Internet Explorer.

D’un point de vue de la sécurité, les meilleures pratiques en matière de gestion d’Internet Explorer dans l’espace de travail MED-V sont les suivantes:

-   Lors de la création de votre package d’espace de travail MED-V, conservez les paramètres par défaut configurés de manière à ce qu’Internet Explorer dans l’espace de travail MED-V soit configuré pour empêcher la navigation et d’autres activités qui peuvent poser des risques en matière de sécurité.

-   Lorsque vous créez votre package d’espace de travail MED-V, conservez les paramètres par défaut définis de telle sorte que le paramètre de sécurité pour la zone de sécurité Internet reste au niveau le plus élevé.

-   Configurez votre proxy d’entreprise ou le gestionnaire de contenu d’Internet Explorer pour bloquer les domaines extérieurs à l’intranet de votre entreprise.

**Configuration d’un espace de travail MED-V pour tous les utilisateurs sur un ordinateur partagé.** Lorsque vous configurez un espace de travail MED-V de façon à ce qu’il soit accessible à tous les utilisateurs sur un ordinateur partagé, réalisez que l’ordinateur virtuel invité (VHD) est placé à un emplacement permettant l’accès en lecture et en écriture à tous les utilisateurs de ce système.

**Configuration d’un compte proxy pour la participation au domaine.** Lorsque vous configurez un compte proxy pour joindre des machines virtuelles au domaine, vous devez savoir qu’un utilisateur final peut obtenir les informations d’identification du compte proxy. Les précautions nécessaires doivent donc être prises, par exemple pour limiter les droits d’utilisateur du compte, afin d’empêcher un utilisateur final d’utiliser les informations d’identification pour cause de dégâts.

**Configuration de Sysprep.** Même si le fichier Sysprep. inf est chiffré par défaut, son contenu peut être déchiffré et lu par tout utilisateur final déterminé qui peut se connecter à l’ordinateur virtuel. Cela soulève des problèmes de sécurité, car le fichier Sysprep. inf peut contenir des informations d’identification en plus d’une clé de produit Windows.

Vous pouvez réduire ce risque en configurant un compte limité pour joindre des machines virtuelles au domaine et en spécifiant les informations d’identification pour ce compte lors de la configuration de Sysprep. Vous pouvez également configurer Sysprep et la première fois que vous exécutez le programme d’exécution en mode d' **assistance** et exiger que les utilisateurs finaux fournissent leurs informations d’identification pour joindre l’ordinateur virtuel au domaine.

Dans le cadre d’une meilleure pratique MED-V, vous pouvez spécifier que la FtsCompletion.exe est exécutée sous un compte qui donne aux utilisateurs finaux la connexion à l’invité via le client de connexion Bureau à distance.

**Authentification de l’utilisateur final.** L’activation de la mise en cache des informations d’identification de l’utilisateur final fournit la meilleure utilisation de MED-V, mais crée le potentiel qu’une personne a pu avoir pour accéder aux informations d’identification de l’utilisateur final. Le seul moyen de limiter ce risque consiste à spécifier sur le programme de création de **package d’espace de travail MED-V** que les informations d’identification de l’utilisateur final ne sont pas stockées. Pour plus d’informations sur l’authentification des utilisateurs finaux, voir [authentification des utilisateurs finaux MED-V](authentication-of-med-v-end-users.md).

## Rubriques connexes


[Résolution des problèmes d'opérations](operations-troubleshooting-medv2.md)

[Microsoft Enterprise Desktop Virtualization 2,0](index.md)

 

 






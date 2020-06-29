---
title: Déploiement d'un espace de travail MED-V à l'aide d'un système de distribution de logiciels d'entreprise
description: Déploiement d'un espace de travail MED-V à l'aide d'un système de distribution de logiciels d'entreprise
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810068"
---
# Déploiement d'un espace de travail MED-V à l'aide d'un système de distribution de logiciels d'entreprise


Le client MED-V peut être distribué à l’aide d’un système de distribution de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager.

**Remarques**  Si MED-V est installé à l’aide de Microsoft System Center Configuration Manager, lors de la création d’un package pour MED-V, définissez le mode d’exécution sur droits d’administration.

 

Avant de déployer MED-V à l’aide d’un système de distribution de logiciels d’entreprise, assurez-vous que vous avez créé une image MED-V prête pour le déploiement. Pour plus d’informations sur la création d’une image MED-V, voir [création d’une image med-v](creating-a-med-v-image.md).

Après avoir préparé l’image MED-V, considérez la meilleure méthode de distribution de l’image dans votre environnement. L’image peut être distribuée de l’une des façons suivantes:

-   Téléchargé sur le Web et distribué via le téléchargement Web, en utilisant éventuellement la technologie de transfert de découpage.

-   Distribués à l’aide de la version préliminaire d’image.

## Déploiement de l’image par le biais du Web


Si vous déployez l’image par le biais du Web, téléchargez l’image MED-V sur un serveur de distribution Web image. Pour plus d’informations sur la configuration d’un serveur de distribution Web d’images, voir [Comment configurer le serveur de distribution Web d’images](how-to-configure-the-image-web-distribution-server.md). Pour plus d’informations sur le téléchargement d’une image sur le serveur, voir [Comment télécharger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md).

## Déploiement de l’image par pré-Staging


Si vous déployez l’image par le biais d’une préinstallation d’image, configurez le dossier pre-Staging et transmettez l’image MED-V au dossier. Pour plus d’informations sur la configuration d’une préinstallation d’image, voir [Comment configurer la](how-to-configure-image-pre-staging.md)préinstallation d’une image.

**Remarques**  Si vous utilisez le prédéploiement d’image, il est important de configurer le dossier d’image avant de pousser le package client. msi. Le chemin d’accès au dossier doit être inclus dans le package client. msi.

 

Enfin, envoyez le package client. msi à l’aide du centre de distribution de logiciels de votre entreprise. MED-V peut alors être installé et l’image déployée. Pour plus d’informations sur l’installation du client MED-V, voir [Comment installer le client med-v](how-to-install-med-v-clientesds.md). Pour plus d’informations sur le déploiement de l’image, reportez-vous [à la rubrique déploiement d’une image d’espace de travail](how-to-deploy-a-workspace-imageesds.md).

 

 






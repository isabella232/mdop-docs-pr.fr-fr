---
title: Déploiement d'une image d'espace de travail
description: Déploiement d'une image d'espace de travail
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812095"
---
# Déploiement d'une image d'espace de travail


Lors de l’utilisation d’un système de distribution de logiciels d’entreprise, une nouvelle image peut être déployée sur les ordinateurs clients de l’une des façons suivantes:

-   [Téléchargement Web](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Pré-échelonnement d’image](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Déploiement d’une image d’espace de travail via le Web


**Pour déployer une image d’espace de travail via le Web**

1.  Téléchargez l’image MED-V sur le serveur.

    Pour plus d’informations sur le téléchargement de l’image, voir [Comment télécharger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md).

2.  À l’aide de votre système de distribution de logiciels d’entreprise, installez le package client. msi MED-V sur les ordinateurs des utilisateurs.

    Pour plus d’informations sur l’installation du package client. msi MED-V, voir [Comment installer le client med-v](how-to-install-med-v-clientesds.md).

    Le client MED-V est installé et démarré pour la première fois. Lors du premier démarrage, le client télécharge l’image à partir de l’adresse du serveur spécifiée dans l’installation du client.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>Déploiement d’une image d’espace de travail à l’aide du pré-Staging d’image


**Pour déployer une image d’espace de travail à l’aide de la préinstallation d’image**

1.  Créer un dossier d’image en version préliminaire et le déplacer vers le dossier.

    Pour plus d’informations sur la configuration d’une préinstallation d’image, voir [Comment configurer la](how-to-configure-image-pre-staging.md)préinstallation d’une image.

2.  À l’aide de votre système de distribution de logiciels d’entreprise, installez le package client. msi MED-V sur les ordinateurs des utilisateurs.

    Pour plus d’informations sur l’installation du package client. msi MED-V, voir [Comment installer le client med-v](how-to-install-med-v-clientesds.md).

    Le client MED-V est installé et démarré pour la première fois. Lors du premier démarrage, le client récupère l’image à partir du dossier pre-stage spécifié dans l’installation du client.

## Rubriques connexes


[Comment configurer le serveur de distribution Web d'images](how-to-configure-the-image-web-distribution-server.md)

 

 






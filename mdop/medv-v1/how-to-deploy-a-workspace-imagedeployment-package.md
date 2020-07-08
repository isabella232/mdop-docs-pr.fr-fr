---
title: Déploiement d'une image d'espace de travail
description: Déploiement d'une image d'espace de travail
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812101"
---
# Déploiement d'une image d'espace de travail


Lors de l’utilisation d’un package de déploiement, une nouvelle image peut être déployée sur les ordinateurs clients de l’une des façons suivantes:

-   [Téléchargement Web](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Pré-échelonnement d’image](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [Déploiement de l’image dans le package de déploiement](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Déploiement d’une image d’espace de travail via le Web


**Pour déployer une image d’espace de travail via le Web**

1.  Téléchargez l’image MED-V sur le serveur.

    Pour plus d’informations sur le téléchargement de l’image, voir [Comment télécharger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md).

2.  Créez un package de déploiement, puis incluez le chemin d’accès du serveur à l’emplacement de l’image.

    Pour plus d’informations sur la création d’un package de déploiement, voir [Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md).

3.  Déployer le package auprès des utilisateurs finaux.

    Pour plus d’informations sur le déploiement du package, voir [Comment installer le client MED-V](how-to-install-med-v-clientdeployment-package.md).

    Le client MED-V est installé et démarré pour la première fois. Lors du premier démarrage, le client télécharge l’image à partir de l’adresse du serveur spécifiée dans l’installation du client.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>Déploiement d’une image d’espace de travail à l’aide du pré-Staging d’image


**Pour déployer une image d’espace de travail à l’aide de la préinstallation d’image**

1.  Créer un dossier d’image en version préliminaire et le déplacer vers le dossier.

    Pour plus d’informations sur la configuration d’une préinstallation d’image, voir [Comment configurer la](how-to-configure-image-pre-staging.md)préinstallation d’une image.

2.  Créez un package de déploiement, puis incluez le chemin d’accès au dossier d’image au préalable.

    Pour plus d’informations sur la création d’un package de déploiement, voir [Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md).

3.  Déployer le package auprès des utilisateurs finaux.

    Pour plus d’informations sur le déploiement du package, voir [Comment installer le client MED-V](how-to-install-med-v-clientdeployment-package.md).

    Le client MED-V est installé et démarré pour la première fois. Lors du premier démarrage, le client récupère l’image à partir du dossier pre-stage spécifié dans l’installation du client.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a>Déploiement d’une image d’espace de travail à l’aide d’un package de déploiement


**Pour déployer une image d’espace de travail à l’aide d’un package de déploiement**

1.  Créez un package de déploiement, puis incluez l’image dans le package.

    Pour plus d’informations sur la création d’un package de déploiement, voir [Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md).

2.  Déployer le package auprès des utilisateurs finaux.

    Pour plus d’informations sur le déploiement du package, voir [Comment installer le client MED-V](how-to-install-med-v-clientdeployment-package.md).

    L’image est importée dans l’hôte dans le cadre de l’installation du package.

## Rubriques connexes


[Comment configurer le serveur de distribution Web d'images](how-to-configure-the-image-web-distribution-server.md)

[Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md)

 

 






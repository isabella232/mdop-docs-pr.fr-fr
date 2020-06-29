---
title: Déploiement d'un espace de travail MED-V à l'aide d'un package de déploiement
description: Déploiement d'un espace de travail MED-V à l'aide d'un package de déploiement
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810073"
---
# Déploiement d'un espace de travail MED-V à l'aide d'un package de déploiement


L’installation du package de déploiement fournit une méthode d’installation du client MED-V et de l’ensemble de ses éléments requis, ainsi que des paramètres prédéfinis par l’administrateur.

Lors de l’utilisation d’un package de déploiement, le package est distribué via un réseau partagé ou un média amovible. L’image peut être incluse dans le package ou être distribuée séparément.

Avant de créer un package de déploiement, assurez-vous que vous avez créé une image MED-V prête pour le déploiement. Pour plus d’informations sur la création d’une image MED-V, voir [création d’une image med-v](creating-a-med-v-image.md).

Après avoir préparé l’image MED-V, considérez la meilleure méthode de distribution de l’image dans votre environnement. L’image peut être distribuée de l’une des façons suivantes:

-   Téléchargé sur le Web et distribué via le téléchargement Web, en utilisant éventuellement la technologie de transfert de découpage.

-   Distribués à l’aide de la version préliminaire d’image.

-   Inclus dans le package de déploiement et répartis avec tous les autres composants MED-V.

Si l’image sera incluse dans le package, aucune autre configuration n’est nécessaire pour l’image. Si l’image ne sera pas incluse dans le package de déploiement, effectuez l’une des opérations suivantes:

-   Si vous déployez l’image par le biais du Web, téléchargez l’image MED-V sur le serveur de distribution Web d’images. Pour plus d’informations sur la configuration d’un serveur de distribution Web d’images, voir [Comment configurer le serveur de distribution Web d’images](how-to-configure-the-image-web-distribution-server.md). Pour plus d’informations sur le téléchargement d’une image sur le serveur, voir [Comment télécharger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md).

-   Si vous déployez l’image par le biais d’une préinstallation d’image, configurez le dossier pre-Staging et transmettez l’image MED-V au dossier. Pour plus d’informations sur la configuration de la pré-version d’image, voir [Comment configurer](how-to-configure-image-pre-staging.md)la préinstallation d’une image.

**Remarques**  Si vous utilisez le prédéploiement d’image, il est important de configurer le dossier d’image avant de créer le package de déploiement. Le chemin d’accès au dossier doit être inclus dans le package de déploiement.

 

Enfin, créez le package de déploiement. Pour plus d’informations sur la création d’un package de déploiement, voir [Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md). Une fois le package terminé, distribuez-le pour le déploiement.

Une fois le package de déploiement distribué, le client MED-V peut être installé et l’image déployée. Pour plus d’informations sur l’installation du client MED-V, voir [Comment installer le client med-v](how-to-install-med-v-clientdeployment-package.md). Pour plus d’informations sur le déploiement de l’image, reportez-vous [à la rubrique déploiement d’une image d’espace de travail](how-to-deploy-a-workspace-imagedeployment-package.md).

 

 






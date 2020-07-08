---
title: Mise à jour d'une image d'espace de travail MED-V
description: Mise à jour d'une image d'espace de travail MED-V
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811405"
---
# Mise à jour d'une image d'espace de travail MED-V


Il est possible de mettre à jour une image de l’une des façons suivantes:

-   La mise à jour peut être poussée vers le système d’exploitation invité à l’aide de votre système de distribution de logiciels d’entreprise.

-   La mise à jour peut être téléchargée sur le serveur de distribution Web d’images, puis téléchargée par le client et appliquée à l’image MED-V.

-   L’image de base MED-V peut être mise à jour et redéployée.

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a>Comment mettre à jour une image MED-V à l’aide d’un système de distribution de logiciels d’entreprise


**Pour mettre à jour une image MED-V à l’aide d’un système de distribution de logiciels d’entreprise**

-   Reportez-vous à la documentation du système que vous utilisez.

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a>Comment mettre à jour une image MED-V à l’aide du téléchargement Web


**Pour mettre à jour une image MED-V à l’aide du téléchargement Web**

1.  Dans le cadre de la gestion de MED-V, sur l’onglet **machine virtuelle** , assurez-vous que les paramètres suivants s’appliquent aux stratégies d’espace de travail MED-v qui sont associées à la mise à jour de l’image med-v:

    -   La case à cocher **suggérer une mise à jour lorsqu’une nouvelle version est disponible** est activée.

    -   Le cas échéant, les **clients doivent utiliser l’option découper lors du téléchargement d’images pour cet espace de travail** est activée.

    Pour plus d’informations, reportez-vous [à la rubrique Comment appliquer des paramètres d’ordinateur virtuel à un espace de travail MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).

2.  Téléchargez la mise à jour d’image vers le serveur de distribution Web d’images.

    Tous les clients contenant des images qui doivent être mises à jour sont automatiquement téléchargés et appliqués à l’image.

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a>Comment mettre à jour une image de base MED-V


**Pour mettre à jour une image de base MED-V**

1.  Ouvrez l’image existante dans PC2007 virtuel.

2.  Apportez les modifications requises à l’image, en mettant à jour l’image (par exemple, l’installation d’un nouveau logiciel).

3.  Fermez les PC2007 virtuelles.

4.  Testez l’image.

5.  Une fois l’image testée, empaquetez-la sur le référentiel local en utilisant le même nom que l’image existante.

    **Remarques**  Si vous nommez l’image un nom différent de la version existante, une nouvelle image sera créée plutôt qu’une nouvelle version de l’image existante.

     

6.  Téléchargez la nouvelle version sur le serveur, encadrez-la dans le dossier d’image prédéfinie ou distribuez-la par le biais d’un package de déploiement.

## Rubriques connexes


[Création d'une image MED-V](creating-a-med-v-image.md)

[Comment mettre à jour une image MED-V](how-to-update-a-med-v-image.md)

[Configuration de stratégies d'espace de travail MED-V](configuring-med-v-workspace-policies.md)

[Comment configurer le serveur de distribution Web d'images](how-to-configure-the-image-web-distribution-server.md)

 

 






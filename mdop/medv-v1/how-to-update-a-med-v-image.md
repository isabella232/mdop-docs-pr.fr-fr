---
title: Comment mettre à jour une image MED-V
description: Comment mettre à jour une image MED-V
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804272"
---
# Comment mettre à jour une image MED-V


## Comment mettre à jour une image MED-V


Une image MED-V existante peut être mise à jour, créant ainsi une nouvelle version de l’image. La nouvelle version peut ensuite être déployée sur des ordinateurs client, ce qui remplace l’image existante.

**Remarques**  Lorsqu’une nouvelle version est déployée sur le client, elle remplace l’image existante. Lors de la mise à jour d’une image, assurez-vous qu’aucune donnée ne doit être enregistrée sur le client.

 

**Pour mettre à jour une image MED-V**

1.  Ouvrez l’image existante dans PC2007 virtuel.

2.  Apportez les modifications requises à l’image, en mettant à jour l’image (par exemple, l’installation d’un nouveau logiciel).

3.  Fermez les PC2007 virtuelles.

4.  Testez l’image.

5.  Une fois l’image testée, empaquetez-la sur le référentiel local en utilisant le même nom que l’image existante.

    **Remarques**  Si vous nommez l’image un nom différent de la version existante, une nouvelle image sera créée plutôt qu’une nouvelle version de l’image existante.

     

6.  Téléchargez la nouvelle version sur le serveur ou Répartissez-la par le biais d’un package de déploiement.

## Rubriques connexes


[Création d'une image Virtual PC pour MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Comment créer et tester une image MED-V](how-to-create-and-test-a-med-v-image.md)

[Comment empaqueter une image MED-V](how-to-pack-a-med-v-image.md)

[Comment charger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md)

[Mise à jour d'une image d'espace de travail MED-V](updating-a-med-v-workspace-image.md)

 

 






---
title: Gestion des mises à jour de logiciels pour les espaces de travail MED-V
description: Gestion des mises à jour de logiciels pour les espaces de travail MED-V
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810781"
---
# Gestion des mises à jour de logiciels pour les espaces de travail MED-V


Différentes options sont à votre disposition pour vous proposer des mises à jour logicielles pour les applications dans l’espace de travail MED-V.

**Remarques**  Pour plus d’informations sur la façon de spécifier les paramètres de configuration qui définissent la façon dont MED-V reçoit les mises à jour automatiques, voir [gestion des mises à jour automatiques pour les espaces de travail MED-v](managing-automatic-updates-for-med-v-workspaces.md).

 

**Mise à jour des logiciels dans un espace de travail MED-V**

1.  **Utilisation d’un système de distribution de logiciels électronique**

    Si votre organisation utilise un système de distribution de logiciels électroniques pour déployer le logiciel, vous pouvez l’utiliser pour fournir des mises à jour logicielles pour les applications sur les espaces de travail MED-V, de la même façon que vous fournissez des mises à jour pour les applications sur des ordinateurs physiques.

2.  **Utilisation d’une stratégie de groupe**

    Si votre organisation déploie le logiciel à l’aide d’une stratégie de groupe, vous pouvez l’utiliser pour fournir des mises à jour logicielles pour les applications sur les espaces de travail MED-V, de la même façon que vous fournissez des mises à jour pour les applications sur des ordinateurs physiques.

3.  **Utilisation de la virtualisation des applications (APP-V)**

    Si vous utilisez MED-V conjointement avec App-V, vous pouvez fournir des mises à jour logicielles aux applications dans l’espace de travail MED-V en suivant les étapes requises par App-V pour la mise à jour du logiciel. Pour plus d’informations, voir [virtualisation des applications](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

4.  **Mise à jour des logiciels dans l’image principale**

    Même si vous n’avez pas envisagé de meilleures pratiques MED-V, vous pouvez installer des mises à jour logicielles sur des applications sur l’image principale. Après avoir installé les mises à jour, vous pouvez redéployer l’espace de travail MED-V vers votre entreprise tout comme vous l’avez déployé à l’origine.

    **Important**  Nous déconseillons cette méthode de gestion des mises à jour logicielles. De plus, si vous effectuez la mise à jour du logiciel dans l’image principale et que vous redéployez l’espace de travail MED-V dans votre entreprise, la première fois que vous devez réexécuter le programme d’installation, les données enregistrées dans l’ordinateur virtuel sont perdues.

     

## Rubriques connexes


[Gestion des mises à jour automatiques pour les espaces de travail MED-V](managing-automatic-updates-for-med-v-workspaces.md)

[Comment tester la publication d'applications](how-to-test-application-publishing.md)

[Comment publier et annuler la publication d'une application sur l'espace de travail MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 






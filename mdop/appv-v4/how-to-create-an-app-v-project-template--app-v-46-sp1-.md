---
title: Procédure pour créer un modèle de projet App-V (App-V4.6 SP1)
description: Procédure pour créer un modèle de projet App-V (App-V4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807190"
---
# Procédure pour créer un modèle de projet App-V (App-V4.6 SP1)


Vous pouvez utiliser un modèle de projet App-V pour enregistrer les paramètres fréquemment appliqués associés à un package d’application virtuel existant. Ces paramètres peuvent ensuite être appliqués lorsque vous créez de nouveaux packages d’application virtuelle dans votre environnement, ce qui peut vous aider à rationaliser le processus de création de packages d’applications virtuelles.

**Remarques**  Vous pouvez appliquer un modèle de projet App-V uniquement lorsque vous créez un nouveau package d’application virtuelle. L’application de modèles de projet aux packages d’applications virtuelles existants n’est pas prise en charge.

 

Pour plus d’informations sur l’application d’un modèle de projet App-V, voir [comment appliquer un modèle de projet App-v (App-V 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).

Les modèles de projet App-V diffèrent des accélérateurs d’applications App-v, car ils sont propres aux applications et les modèles de projets App-v peuvent être appliqués à plusieurs applications. Par ailleurs, vous ne pouvez pas utiliser un modèle de projet lorsque vous utilisez un accélérateur de package pour créer un package d’application virtuelle.

Les paramètres généraux suivants sont enregistrés avec un modèle de projet App-V:

-   **Options de surveillance avancée**. Autorise l’exécution de Microsoft Update lors de l’analyse, rebase **. dll**.

-   **Paramètres de déploiement de package**. Contient le **protocole**, le **nom d’hôte**, le **port**, le **chemin d’accès**, les **systèmes d’exploitation**, l' **application des DEscripteurs de sécurité**, la création d’un **package** **MSI**

-   **Options générales**. Vous permet de **générer le package Microsoft Windows Installer (MSI)** , **de permettre la virtualisation des événements**, **de la virtualisation des services**, **d’ajouter la version du package à un nom de fichier**.

-   **Éléments d’exclusion**. Contient la liste modèle d’exclusion.

**Pour créer un modèle de projet**

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2.  Si le package d’application virtuelle est actuellement ouvert dans le Sequencer App-V, passez à l’étape 3 de cette procédure. Pour ouvrir le package d’application virtuelle existant qui contient les paramètres que vous souhaitez enregistrer avec le modèle de projet App-V, cliquez sur **fichier**  /  **ouvrir** , puis sur **modifier** le **package**. Dans la page **Sélectionner un package** , cliquez sur **Parcourir** et recherchez le package d’application virtuel que vous voulez ouvrir. Cliquez sur **Modifier**.

3.  Dans la console App-V du Sequencer, cliquez sur **fichier**  /  **enregistrer en tant que modèle**. Après avoir consulté les paramètres qui seront enregistrés avec le nouveau modèle, cliquez sur **OK**. Spécifiez un nom qui sera associé au nouveau modèle de projet App-V. Cliquez sur **Save**.

    Le nouveau modèle de projet App-V est enregistré dans l’annuaire indiqué à l’étape 3 de cette procédure.

## Rubriques connexes


[Tâches pour Application Virtualization Sequencer (App-V4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Procédure pour appliquer un modèle de projet App-V (App-V4.6SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 






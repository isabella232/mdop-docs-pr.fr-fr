---
title: Comment créer et utiliser un modèle de projet
description: Comment créer et utiliser un modèle de projet
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805593"
---
# Comment créer et utiliser un modèle de projet


Vous pouvez utiliser un modèle de projet App-V 5,0 pour enregistrer les paramètres fréquemment appliqués associés à un package d’application virtuel existant. Ces paramètres peuvent ensuite être appliqués lors de la création de nouveaux packages d’application virtuelle dans votre environnement. L’utilisation d’un modèle de projet peut simplifier le processus de création de packages d’applications virtuelles.

**Remarques**  Vous pouvez également appliquer un modèle de projet App-V 5,0 lors d’une mise à niveau de package. Par exemple, si vous avez séquencé une application avec une liste d’exclusion personnalisée, il est recommandé qu’un modèle associé soit créé et enregistré pour une utilisation ultérieure lors de la mise à niveau de l’application séquencée.

Les modèles de projet App-V 5,0 diffèrent des accélérateurs d’application à l’application-V 5,0, car les accélérateurs d’application-V 5,0 sont propres à l’application et les modèles de projets App-V 5,0 peuvent être appliqués à plusieurs applications.

Pour créer et appliquer un nouveau modèle, procédez comme suit.

**Pour créer un modèle de projet**

1.  Pour démarrer le Sequencer App-V 5,0, sur l’ordinateur exécutant le Sequencer, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft  /  **Application Virtualization Sequencer**.

**Remarques**  Si le package d’application virtuelle est actuellement ouvert dans la console App-V 5,0 Sequencer, passez à l’étape 3 de cette procédure.

2. Pour ouvrir le package d’application virtuelle existant qui contient les paramètres que vous souhaitez enregistrer avec le modèle de projet App-V 5,0, cliquez sur **fichier**  /  **ouvrir**, puis sur **modifier le package**. Dans la page **Sélectionner un package** , cliquez sur **Parcourir** et recherchez le package d’application virtuel que vous voulez ouvrir. Cliquez sur **Modifier**.

3. Dans la console App-V 5,0, pour enregistrer le fichier de modèle, cliquez sur **fichier**  /  **enregistrer en tant que modèle**. Après avoir consulté les paramètres qui seront enregistrés avec le nouveau modèle, cliquez sur **OK**. Spécifiez un nom qui sera associé au nouveau modèle de projet App-V 5,0. Cliquez sur Save.
   Le nouveau modèle de projet App-V 5,0 est enregistré dans l’annuaire indiqué à l’étape 3 de cette procédure.

**Pour appliquer un modèle de projet**

**Important**  La création d’un package d’application virtuelle à l’aide d’un modèle de projet en conjonction avec un accélérateur de package n’est pas prise en charge.

1.  Pour démarrer le Sequencer App-V 5,0, sur l’ordinateur exécutant le Sequencer, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft  /  **Application Virtualization Sequencer**.

2.  Pour créer ou mettre à niveau un nouveau package d’application virtuelle à l’aide d’un modèle de projet App-V 5,0, cliquez sur **fichier**  /  **nouveau à partir d’un modèle**.

3.  Pour sélectionner le modèle de projet que vous voulez utiliser, accédez au répertoire où le modèle de projet est enregistré, sélectionnez le modèle de projet, puis cliquez sur **ouvrir**.

    Créez le nouveau package d’application virtuelle. Les paramètres enregistrés avec le modèle spécifié seront appliqués au nouveau package d’application virtuel que vous êtes en train de créer.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)










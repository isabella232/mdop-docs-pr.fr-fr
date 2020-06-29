---
title: Comment créer et utiliser un modèle de projet
description: Comment créer et utiliser un modèle de projet
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805586"
---
# Comment créer et utiliser un modèle de projet


Vous pouvez utiliser un modèle de projet App-V 5,1 pour enregistrer les paramètres fréquemment appliqués associés à un package d’application virtuel existant. Ces paramètres peuvent ensuite être appliqués lors de la création de nouveaux packages d’application virtuelle dans votre environnement. L’utilisation d’un modèle de projet peut simplifier le processus de création de packages d’applications virtuelles.

**Remarque**  
Vous pouvez également appliquer un modèle de projet App-V 5,1 lors d’une mise à niveau de package. Par exemple, si vous avez séquencé une application avec une liste d’exclusion personnalisée, il est recommandé qu’un modèle associé soit créé et enregistré pour une utilisation ultérieure lors de la mise à niveau de l’application séquencée.



Les modèles de projet App-V 5,1 diffèrent des accélérateurs d’application à l’application-V 5,1, car les accélérateurs d’application-V 5,1 sont propres à l’application et les modèles de projets App-V 5,1 peuvent être appliqués à plusieurs applications.

Pour créer et appliquer un nouveau modèle, procédez comme suit.

**Pour créer un modèle de projet**

1.  Pour démarrer le Sequencer App-V 5,1, sur l’ordinateur exécutant le Sequencer, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft  /  **Application Virtualization Sequencer**.

2.  **Remarque**  
    Si le package d’application virtuelle est actuellement ouvert dans la console App-V 5,1 Sequencer, passez à l’étape 3 de cette procédure.



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. Dans la console App-V 5,1, pour enregistrer le fichier de modèle, cliquez sur **fichier**  /  **enregistrer en tant que modèle**. Après avoir consulté les paramètres qui seront enregistrés avec le nouveau modèle, cliquez sur **OK**. Spécifiez un nom qui sera associé au nouveau modèle de projet App-V 5,1. Cliquez sur Save.

   Le nouveau modèle de projet App-V 5,1 est enregistré dans l’annuaire indiqué à l’étape 3 de cette procédure.

**Pour appliquer un modèle de projet**

1.  **Important**  
    La création d’un package d’application virtuelle à l’aide d’un modèle de projet en conjonction avec un accélérateur de package n’est pas prise en charge.



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. Pour créer ou mettre à niveau un nouveau package d’application virtuelle à l’aide d’un modèle de projet App-V 5,1, cliquez sur **fichier**  /  **nouveau à partir d’un modèle**.

3. Pour sélectionner le modèle de projet que vous voulez utiliser, accédez au répertoire où le modèle de projet est enregistré, sélectionnez le modèle de projet, puis cliquez sur **ouvrir**.

   Créez le nouveau package d’application virtuelle. Les paramètres enregistrés avec le modèle spécifié seront appliqués au nouveau package d’application virtuel que vous êtes en train de créer.

   Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)










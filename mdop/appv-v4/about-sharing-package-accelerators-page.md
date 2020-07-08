---
title: Page À propos du partage d'accélérateurs de package
description: Page À propos du partage d'accélérateurs de package
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808129"
---
# Page À propos du partage d'accélérateurs de package


Les informations suivantes fournissent des informations pratiques recommandées sur le partage des accélérateurs de package. Si vous envisagez de partager des fichiers accélérateurs de package, des informations telles que les noms d’ordinateur, les informations de compte d’utilisateur et les informations relatives aux applications incluses dans les transformations peuvent être incluses dans le fichier accélérateurs de package. Vous devez examiner les paramètres ou les fichiers de configuration associés au package d’application virtuelle pour vous assurer que les applications ne contiennent aucune information personnelle. Cette page contient les éléments suivants.

-   **Nom d’utilisateur**. Lorsque vous ouvrez une session sur l’ordinateur exécutant le Sequencer Microsoft App-V, vous devez utiliser un compte utilisateur générique, tel que le compte d' **administrateur** intégré. Vous ne devez pas utiliser un compte basé sur un nom d’utilisateur existant.

-   **Nom**de l’ordinateur. Spécifiez un nom général et non identifiant de l’ordinateur exécutant le Sequencer.

-   **URL du serveur**. Dans la console App-V Sequencer, dans l’onglet **déploiement** , utilisez les paramètres par défaut pour les informations sur la configuration de l’URL du serveur.

-   **Applications**. Si vous ne voulez pas partager la liste des applications installées sur l’ordinateur exécutant le Sequencer lors de la création de l’accélérateur de package, vous devez supprimer le fichier **appv\_manifest.xml** . Ce fichier se trouve dans le répertoire racine du package du package d’application virtuel.

## Rubriques connexes


[Assistant Créer un accélérateur de package (AppV4.6SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

[À propos des accélérateurs de package App-V (App-V4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 






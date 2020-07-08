---
title: À propos des accélérateurs de package App-V (App-V4.6 SP1)
description: À propos des accélérateurs de package App-V (App-V4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808169"
---
# À propos des accélérateurs de package App-V (App-V4.6 SP1)


Vous pouvez utiliser les accélérateurs de package App-V pour effectuer une séquence automatique de grandes applications complexes. Par ailleurs, lorsque vous appliquez un accélérateur de package App-V, il n’est pas toujours nécessaire d’installer manuellement une application pour créer le package d’application virtuelle.

**Remarques**  Dans certains cas, vous êtes invité à installer une application localement sur l’ordinateur exécutant le Sequencer App-V avant de pouvoir utiliser l’accélérateur de package. Si vous devez installer une application, vous devez installer l’application à l’emplacement par défaut de l’application. Cette installation n’est pas gérée par le Sequencer App-V. Lorsque l’accélérateur de package App-V est créé, l’auteur de l’accélérateur de package détermine s’il est nécessaire d’installer une application localement.

 

Le Sequencer App-V extrait les fichiers requis de l’accélérateur de package App-V et du support d’installation associé pour créer un package virtuel sans avoir à surveiller l’installation de l’application.

**Important**  Exclusion de responsabilité: le Sequencer Microsoft Application Virtualization ne vous donne aucun droit de licence pour l’application logicielle que vous utilisez pour créer un accélérateur de package. Vous devez respecter les conditions générales du contrat de licence utilisateur final pour une telle application. Il est de votre responsabilité de veiller à ce que les termes du contrat de licence de l’application logicielle vous permettent de créer un accélérateur de package à l’aide du Sequencer de la virtualisation de l’application.

 

Les accélérateurs et les modèles de projet App-V diffèrent les uns des autres. Les accélérateurs de package sont propres à l’application. Les modèles Project permettent aux utilisateurs d’enregistrer les paramètres fréquemment utilisés spécifiques à une organisation et de les appliquer à plusieurs applications. Vous pouvez également créer des modèles de projet à l’invite de commandes, en revanche, vous devez utiliser la console de Sequencer App-V pour créer des accélérateurs de package. En outre, la création d’un package à l’aide d’un accélérateur de package et l’application d’un modèle de projet ne sont pas prises en charge.

## Partage d’application-V package Accelerators


Cette section fournit des informations pratiques recommandées sur le partage des accélérateurs de package. Si vous envisagez de partager des accélérateurs de package, des informations telles que les noms d’ordinateur, les informations de compte d’utilisateur et les informations relatives aux applications associées peuvent être incluses dans les accélérateurs de package. la liste suivante décrit les méthodes que vous devez prendre en compte lors de la création d’accélérateurs de package:

-   **Nom d’utilisateur**. Lorsque vous ouvrez une session sur l’ordinateur exécutant le Sequencer App-V, vous devez utiliser un compte utilisateur générique, tel que le compte d' **administrateur** intégré pour l’administration de l’ordinateur/domaine. Vous ne devez pas utiliser un compte basé sur un nom d’utilisateur existant.

-   **Nom**de l’ordinateur. Spécifiez un nom général et non identifiant de l’ordinateur exécutant le Sequencer.

-   **URL du serveur**. Dans l’onglet **déploiement** de la console de Sequencer, utilisez les paramètres par défaut pour les informations sur la configuration de l’URL du serveur.

-   **Applications**. Si vous ne voulez pas partager la liste des applications installées sur l’ordinateur exécutant le Sequencer lors de la création de l’accélérateur de package, vous devez supprimer le fichier **appv\_manifest.xml** . Ce fichier se trouve dans le répertoire racine du package du package d’application virtuel.

Vous devez également consulter les paramètres ou les fichiers de configuration associés au package d’application virtuelle pour vous assurer que les applications ne contiennent aucune information personnelle.

## Sécurisation des accélérateurs de package App-V


Enregistrez toujours les accélérateurs de packages App-V et tout support d’installation associé à un emplacement sécurisé sur le réseau pour protéger les accélérateurs d’application et les fichiers d’installation contre la falsification ou la corruption. Étant donné que les accélérateurs de package peuvent également contenir des informations relatives au mot de passe et à l’utilisateur, vous devez enregistrer les accélérateurs d’applications-V dans un emplacement sécurisé, et vous devez signer numériquement l’accélérateur de package après l’avoir créé, afin que l’éditeur puisse être vérifié lorsque l’accélérateur de package est appliqué. Pour plus d’informations sur les signatures numériques, voir [recommandations en matière de signature numérique pour la sécurité des critères communs](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .

## Rubriques connexes


[Procédure pour créer des accélérateurs de package App-V (App-V4.6SP1)](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[Comment appliquer un accélérateur de package pour créer un package d’application virtuelle (App-V 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 






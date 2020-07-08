---
title: À propos des phases de séquencement
description: À propos des phases de séquencement
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808133"
---
# À propos des phases de séquencement


Le séquençage est le processus par lequel vous créez un package d’application séquencé en utilisant le Sequencer Microsoft Application Virtualization (App-V). Lors du séquençage, le Sequencer analyse et enregistre tous les processus d’installation et de configuration pour une application et crée les fichiers suivants: ICO, OSD, SFT et SPRJ. Ces fichiers contiennent toutes les informations nécessaires sur une application et permettent à cette application de s’exécuter dans un environnement virtuel.

Les quatre phases pour séquençager une application et la création d’un package d’application virtuelle sont l’installation, le lancement, la personnalisation et l’enregistrement. La liste suivante fournit des informations sur chacune des phases:

1.  **Phase d’installation**: vous spécifiez le nom du package et un commentaire associé facultatif qui sera associé au package. Vous pouvez également configurer des options de surveillance avancées au cours de cette phase. Les options de surveillance avancée incluent la spécification de la taille du bloc et l’installation des mises à jour automatiques lors de l’analyse. Le Sequencer enregistre toutes les informations et configurations nécessaires nécessaires pour créer un package d’application virtuelle et les paramètres de fichier et de Registre associés.

    **Important**  Pour afficher les options avancées, sélectionnez **afficher les options de surveillance avancée** dans la page informations sur le **package** .

     

2.  **Phase de lancement**: lors de la phase de lancement, vous pouvez spécifier les associations de fichiers et les descripteurs de sécurité nécessaires qui doivent être configurés avec le package. Vous devriez ouvrir l’application autant de fois que nécessaire pour garantir la stabilité et la fonctionnalité de l’application.

3.  **Phase de personnalisation**-lors de la phase de personnalisation, vous pouvez configurer votre package à l’aide des fichiers. OSD associés. Vous pouvez spécifier si tous les scripts associés doivent s’exécuter à l’intérieur ou à l’extérieur de l’environnement virtuel, spécifier d’autres actions qui doivent être exécutées, spécifier la façon dont les scripts associés sont exécutés (de manière synchrone ou asynchrone) et spécifier d’autres scripts qui doivent être exécutés dans le contexte de l’utilisateur.

4.  **Phase de sauvegarde**: lors de la phase de sauvegarde, tous les fichiers requis pour le package d’application virtuelle sont créés. Les fichiers créés sont. sprj,. SFT,. OSD,. ico,. xml et le fichier Windows Installer (. msi).

## Rubriques connexes


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 






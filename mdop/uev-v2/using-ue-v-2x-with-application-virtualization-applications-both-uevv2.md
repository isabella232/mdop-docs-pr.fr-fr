---
title: Utilisation d’UE-V 2. x avec les applications de virtualisation des applications
description: Utilisation d’UE-V 2. x avec les applications de virtualisation des applications
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812257"
---
# Utilisation d’UE-V 2. x avec les applications de virtualisation des applications


Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 prennent en charge les applications Microsoft Application Virtualization (App-v) sans modification requise du package App-V ou du modèle UE-V. Toutefois, une étape supplémentaire est nécessaire, car vous ne pouvez pas exécuter le générateur UE-V directement sur une application application-V virtualisée. Au lieu de cela, vous devez installer l’application localement, générer le modèle, puis appliquer le modèle à l’application virtualisée. UE-V prend en charge les packages App-v 4,5, App-V 4,6 et App-V 5,0.

## Synchronisation des paramètres d’UE-V pour les applications App-v


UE-V vérifie qu’une application s’ouvre à l’aide du nom du programme et, facultativement, des numéros de version des fichiers et des numéros de version des produits, que l’application soit installée en local ou virtuellement à l’aide de App-V. Au démarrage de l’application, UE-V surveille le processus App-V, applique les paramètres stockés dans le chemin de stockage des paramètres de l’utilisateur, puis permet à l’application de démarrer normalement. Dans le cadre de l’utilisation des applications App-V, UE-V effectue une conversion automatique des chemins de fichier et du registre appropriés vers l’emplacement virtualisé plutôt que de l’emplacement physique hors de l’environnement d’application-V.

 **Pour implémenter la synchronisation des paramètres pour une application virtualisée**

1.  Exécutez le générateur UE-V pour collecter les paramètres de l’application installée localement dont vous voulez synchroniser les paramètres entre les ordinateurs. Ce processus crée un modèle d’emplacement des paramètres. Si vous utilisez un modèle intégré tel que le modèle Microsoft Office 2010, ignorez cette étape. Pour plus d’informations sur l’exécution du générateur UE-V, voir [déployer UE-v 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).

2.  Si vous ne l’avez pas déjà fait, installez le package d’application App-V.

3.  Publiez le modèle à l’emplacement de votre catalogue de modèles de paramètres ou installez-le manuellement à l’aide de l’applet de la `Register-UEVTemplate` cmdlet Windows PowerShell.

    **Remarques**  Si vous publiez le modèle qui vient d’être créé dans le catalogue de modèles paramètres, le client ne reçoit pas le modèle tant que le fournisseur de synchronisation n’a pas mis à jour les paramètres. Pour démarrer manuellement le processus, ouvrez **le planificateur de tâches**, développez Bibliothèque du planificateur de **tâches**, développez **Microsoft**, puis **UE-V**. Dans le volet résultats, cliquez avec le bouton droit sur **mise à jour automatique de modèle**, puis cliquez sur **exécuter**.

     

4.  Démarrez le package App-V.






## Rubriques connexes


[Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 






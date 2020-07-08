---
title: Configuration du centre de paramètres de société pour UE-V 2. x
description: Configuration du centre de paramètres de société pour UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809869"
---
# Configuration du centre de paramètres de société pour UE-V 2. x


La virtualisation de l’interface utilisateur de Microsoft (UE-V) 2,0, 2,1 et 2,1 SP1 inclut une nouvelle application, le centre de paramètres de l’entreprise, qui aide les utilisateurs à gérer les paramètres à synchroniser. Le centre de paramètres d’une entreprise est installé à l’aide de l’agent UE-V. Les utilisateurs accèdent au centre de paramètres d’une entreprise dans le panneau de configuration, dans le menu **Démarrer** ou l’écran d' **Accueil** , puis via l’icône de zone de notification UE-V. Le centre de paramètres de la société affiche les paramètres qui sont synchronisés et aide les utilisateurs à consulter l’état de synchronisation d’UE-V. Les utilisateurs peuvent utiliser le centre de paramètres de la société pour sélectionner les applications ou fonctionnalités Windows qui synchronisent leurs paramètres entre eux. Ils peuvent également cliquer sur le bouton **Synchroniser maintenant** pour synchroniser tous les paramètres immédiatement. L’administrateur peut également inclure un lien pour le support dans le centre de paramètres de l’entreprise.

## À propos du centre de paramètres de la société


L’application de bureau centre de paramètres de l’entreprise fournit aux utilisateurs des informations relatives à la synchronisation des paramètres d’UE-V. Le centre de paramètres d’une entreprise est accessible de différentes manières:

-   Icône de la zone de notification: avec le paramètre de stratégie de groupe icône de la **barre d’État** ou configuration Windows PowerShell activée, l’icône UE-V apparaît dans la zone de notification. Cliquez sur l’icône UE-V pour ouvrir le centre de paramètres de la société.

    **Remarques**  L’icône zone de notification peut être désactivée en utilisant les paramètres suivants:

    -   Paramètre de stratégie de groupe: `Policy Tray Icon`

    -   Cmdlet Windows PowerShell: `TrayIconEnabled`

    -   Élément de configuration dans le Pack de configuration UE-V pour SystemCenter2012 ConfigurationManager: `Tray icon enabled`

     

-   Application du panneau de configuration: dans le panneau de configuration, accédez à **apparence et personnalisation**, puis cliquez sur Centre de gestion des **entreprises**.

-   Notification d’utilisation initiale: sauf si elle est désactivée, l’agent UE-V avertit l’utilisateur que les paramètres sont maintenant synchronisés lorsque l’agent UE-V est exécuté pour la première fois sur un ordinateur. Cliquez sur la boîte de dialogue de notification pour ouvrir le centre de paramètres de la société.

-   L’écran d' **Accueil** ou le menu **Démarrer** inclut un lien vers le centre de paramètres de l’entreprise. La recherche du centre de paramètres de la société trouve l’application.

## Configuration du lien support dans le centre de paramètres de la société


Le centre de paramètres de la société peut inclure un lien hypertexte sur lequel les utilisateurs peuvent cliquer pour obtenir de l’aide sur les problèmes de synchronisation des paramètres d’UE-V. Ce lien peut ouvrir des protocoles d’URL valides, tels que http://pour une page Web ou mailto://pour un message électronique. Le lien support peut être configuré à l’aide d’une stratégie de groupe, de Windows PowerShell ou du Pack de configuration de System Center 2012 Configuration Manager UE-V.

**Comment configurer le lien du support du centre de paramètres de la société**

1.  Ouvrez l’outil de gestion de votre choix:

    -   **Stratégie de groupe** : Si vous ne l’avez pas déjà fait, téléchargez le modèle ADMX pour UE-V 2 à partir des [modèles d’administration de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941).

    -   **Windows PowerShell** : sur un ordinateur sur lequel l’agent UE-V est installé, ouvrez **Windows PowerShell**. Pour plus d’informations sur l’administration de UE-V à l’aide de Windows PowerShell, voir [administration d’UE-v 2. x avec Windows PowerShell et WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).

    -   **Module de configuration de System Center 2012 pour l’utilisation de Microsoft User Interface Virtualization (UE-v)** – importez le Pack de configuration pour UE-V et suivez la documentation du module de configuration pour créer des éléments de configuration. Pour plus d’informations sur le Pack de configuration pour UE-V, voir [configuration d’UE-v 2. x avec System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

2.  Modifiez les paramètres des stratégies suivantes:

    -   **Texte du lien vers le contact** : ce paramètre spécifie le texte du lien hypertexte d’URL de contact dans le centre de paramètres de l’entreprise. Si vous activez ce paramètre, le centre de paramètres de la société affiche le texte spécifié dans le lien vers l’URL du contact.

        -   Paramètres de stratégie de groupe: `Contact IT Link Text`

        -   Cmdlet Windows PowerShell: `ContactITDescription`

        -   Élément de configuration du module de configuration: `IT contact descriptive text`

    -   **URL du contact** : ce paramètre spécifie l’URL du lien de contact dans le centre de paramètres de la société dans un protocole d’URL valide tel que http://pour une page web ou mailto://pour un message électronique.

        -   Paramètres de stratégie de groupe: `Contact IT URL`

        -   Cmdlet Windows PowerShell: `ContactITUrl`

        -   Élément de configuration du module de configuration: `IT contact URL`

3.  Déployez les paramètres sur les ordinateurs des utilisateurs à l’aide de l’outil de gestion.






 

 






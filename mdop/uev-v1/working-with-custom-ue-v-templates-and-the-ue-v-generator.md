---
title: Utilisation de modèles UE-V personnalisés et du Générateur UE-V
description: Utilisation de modèles UE-V personnalisés et du Générateur UE-V
author: dansimp
ms.assetid: 7bb2583a-b032-4800-9bf9-eb33528e1d0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db5387254842bfdcf3898089bc12a8e929e3813a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810278"
---
# Utilisation de modèles UE-V personnalisés et du Générateur UE-V


Pour rendre itinérantes les applications entre les ordinateurs des utilisateurs, la virtualisation de l’utilisation de Microsoft (UE-V) utilise des *modèles d’emplacement des paramètres*. Certains modèles d’emplacement des paramètres sont inclus dans la virtualisation de l’utilisation de l’utilisateur. Vous pouvez également créer, modifier ou valider des modèles d’emplacements de paramètres personnalisés avec le générateur UE-V.

Le générateur UE-V analyse une application afin de détecter et de capturer les emplacements où l’application stocke ses paramètres. L’application surveillée doit être une application classique. Le générateur UE-V ne peut pas créer de modèle d’emplacement des paramètres pour les types d’applications suivants:

-   Applications virtualisées

-   Application proposée via les services Terminal Server

-   Applications Java

-   Applications Windows 8

## Créer des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V


Utilisation du générateur UE-V pour créer des modèles d’emplacement des paramètres.

[Créer des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V](create-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Modifier des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V


Utilisation du générateur UE-V pour modifier les modèles d’emplacement des paramètres.

[Modifier des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V](edit-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Valider des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V


Utilisation du générateur UE-V pour valider les modèles d’emplacement des paramètres modifiés hors du générateur UE-V.

[Valider des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V](validate-ue-v-settings-location-templates-with-ue-v-generator.md)

## <a href="" id="bkmk-standardnonstandardsettingslocations"></a>Emplacements des paramètres standard et non standard


Le générateur UE-V vous permet d’identifier l’emplacement des applications afin de détecter les fichiers de paramètres et les paramètres de Registre utilisés par les applications pour le stockage des informations de paramètres. Vous pouvez utiliser le générateur UE-V pour ouvrir l’application dans le cadre du processus de découverte et capturer les paramètres à l’emplacement standard. Les emplacements standard sont les suivants:

-   **Paramètres du Registre** – emplacements du Registre sous **HKEY \ _CURRENT \ _USER**

-   **Fichiers de paramètres d’application** : fichiers stockés dans \ \ **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **itinérance**

Le générateur UE-V exclut les emplacements dans lesquels le stockage des fichiers de logiciels d’application ne se déplace pas correctement entre les ordinateurs ou les environnements des utilisateurs. Le générateur UE-V exclut ces emplacements. Les emplacements exclus sont les suivants:

-   HKEY \ _CURRENT \ _USER clés de Registre et les fichiers auxquels l’utilisateur connecté ne peut pas écrire de valeurs

-   HKEY \ _CURRENT \ _USER clés de Registre et fichiers associés à la fonctionnalité principale du système d’exploitation Windows.

-   Toutes les clés de Registre situées dans la ruche HKEY \ _LOCAL \ _MACHINE (nécessite des droits d’administrateur et peuvent nécessiter un accord UAC)

-   Fichiers situés dans les répertoires de fichiers du programme (nécessite des droits d’administrateur et peuvent nécessiter un contrat d’UAC)

-   Fichiers situés dans les utilisateurs \ \ \ [nom d’utilisateur \] \ \ AppData \ \ LocalLow

-   Fichiers du système d’exploitation Windows situés dans% SystemRoot% (nécessite des droits d’administrateur et peuvent nécessiter un contrat de contrôle de l’utilisateur)

Si les clés de Registre et les fichiers stockés dans ces emplacements sont requis pour itinérance des paramètres d’application, vous pouvez ajouter manuellement les emplacements exclus au modèle d’emplacement paramètres lors du processus de création de modèle.

## Autres ressources pour ce produit


[Opérations d'UE-V1.0](operations-for-ue-v-10.md)

[Administration d'UE-V1.0](administering-ue-v-10.md)

 

 






---
title: Créer des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V
description: Créer des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811879"
---
# Créer des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V


La virtualisation de l’utilisation de l’utilisation de Microsoft (UE-V) utilise des *modèles d’emplacement des paramètres* pour itinérance des paramètres d’application entre les ordinateurs des utilisateurs. Certains modèles d’emplacement des paramètres standard sont inclus avec la virtualisation de l’utilisation de l’utilisateur. Vous pouvez également créer, modifier ou valider des modèles d’emplacements de paramètres personnalisés avec le générateur UE-V.

Le générateur UE-V analyse une application afin de détecter et de capturer les emplacements où l’application stocke ses paramètres. L’application surveillée doit être une application classique. Le générateur UE-V ne peut pas créer de modèle d’emplacement des paramètres à partir des types d’applications suivants:

-   Applications virtualisées

-   Application proposée via les services Terminal Server

-   Applications Java

-   Applications Windows 8

**Remarques**  Les modèles UE-V ne peuvent pas être créés à partir d’applications virtuelles ou d’applications de services Terminal Server. Néanmoins, il est possible d’appliquer des paramètres synchronisés à l’aide des modèles à ces applications. Pour créer des modèles qui prennent en charge les applications VDI (Virtual Desktop Infrastructure) et Terminal Services, ouvrez une version du fichier Windows Installer (. msi) de l’application auprès d’UE-V Generator.

 

**Emplacements exclus**

Le processus de découverte exclut les emplacements dans lesquels les fichiers de logiciels d’application stockés habituellement sur les ordinateurs des utilisateurs et les environnements. Les éléments suivants sont exclus:

-   HKEY \ _CURRENT \ _USER clés de Registre et les fichiers auxquels l’utilisateur connecté ne peut pas écrire de valeurs

-   HKEY \ _CURRENT \ _USER clés de Registre et fichiers associés aux fonctionnalités principales du système d’exploitation Windows

-   Toutes les clés de Registre se trouvant dans la ruche du _MACHINE HKEY \ _LOCAL

-   Fichiers situés dans les répertoires de fichiers du programme

-   Fichiers situés dans les utilisateurs \ \ \ [nom d’utilisateur \] \ \ AppData \ \ LocalLow

-   Fichiers du système d’exploitation Windows situés dans% SystemRoot%

Si les clés de Registre et les fichiers stockés dans ces emplacements exclus sont requis pour pouvoir itinérance des paramètres d’application, les administrateurs peuvent ajouter manuellement les emplacements au modèle d’emplacement des paramètres pendant le processus de création de modèle.

## Créer des modèles UE-V


Utilisez le générateur UE-V pour créer des modèles d’emplacement des paramètres pour applications métier ou d’autres applications. Une fois le modèle créé pour une application créée, vous pouvez déployer le modèle sur des ordinateurs pour permettre aux utilisateurs d’effectuer les réglages de l’application.

**Pour créer un modèle d’emplacement des paramètres UE-V avec le générateur UE-V**

1.  Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **utilisation de Microsoft**, puis sur générateur de **virtualisation Microsoft User Interface**.

2.  Cliquez sur **créer un modèle d’emplacement des paramètres**.

3.  Spécifiez l’application. Naviguez jusqu’au chemin d’accès de l’application (. exe) ou du raccourci de l’application (. lnk) pour lequel vous voulez créer un modèle d’emplacement des paramètres. Spécifiez les arguments de ligne de commande, le cas échéant, et le répertoire de travail, le cas échéant. Cliquez sur **Suivant** pour poursuivre.

    **Remarques**  Avant le démarrage de l’application, le système affiche une invite de **contrôle de compte d’utilisateur**. Une autorisation est requise pour contrôler les emplacements du Registre et des fichiers utilisés par l’application pour le stockage des paramètres.

     

4.  Après le démarrage de l’application, fermez l’application. Le générateur UE-V enregistre les emplacements où l’application stocke ses paramètres.

5.  Une fois le processus terminé, cliquez sur **suivant** pour continuer.

6.  Activez et désactivez les cases à cocher en regard des emplacements et paramètres de fichier de paramètres du registre appropriés à déplacer pour cette application. La liste inclut les deux catégories suivantes pour les emplacements de paramètres:

    -   **Standard**: les paramètres de l’application qui sont stockés dans le Registre sous les clés HKEY \ _CURRENT \ _USER ou dans les dossiers de fichiers sous \ \ **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **itinérance**. UE-V Generator inclut ces paramètres par défaut.

    -   Non **standard**: paramètres d’application stockés en dehors des emplacements spécifiés dans les recommandations en matière de stockage des données de paramètres (facultatif). Il s’agit des fichiers et dossiers sous **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **local**. Passez en revue ces emplacements pour déterminer s’ils doivent figurer dans le modèle d’emplacement des paramètres. Activez les cases à cocher emplacements pour les inclure.

    Cliquez sur **Suivant** pour poursuivre.

7.  Examinez et modifiez les **Propriétés**, emplacements **du Registre** et emplacements des **fichiers** pour le modèle d’emplacement des paramètres.

    -   Modifiez les propriétés suivantes sous l’onglet **Propriétés** :

        -   **Nom**de l’application: nom de l’application rédigée dans la description des propriétés du programme files.

        -   **Nom du programme**: nom du programme que vous avez utilisé dans les propriétés du fichier programme. Ce nom est généralement l’extension. exe.

        -   **Version du produit**: numéro de version du fichier. exe de l’application. En conjonction avec la version du fichier, cette propriété permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres. Cette propriété accepte un numéro de version principal. Si cette propriété est vide, le modèle d’emplacement des paramètres s’applique à toutes les versions du produit.

        -   **Version du fichier**: numéro de version du fichier the.exe de l’application. Combinée à la version du produit, cette propriété permet d’identifier les applications ciblées par le modèle d’emplacement des paramètres. Cette propriété accepte un numéro de version principal. Si cette propriété est vide, le modèle d’emplacement des paramètres s’appliquera à toutes les versions du programme.

        -   **Nom** de l’auteur du modèle (facultatif): nom de l’auteur du modèle d’emplacement des paramètres.

        -   **Courrier de création de modèles** (facultatif): adresse de messagerie de l’auteur du modèle d’emplacement des paramètres.

    -   L’onglet **Registre** recense la **clé** et l' **étendue** des emplacements du Registre inclus dans le modèle d’emplacement des paramètres. Modifiez les emplacements du Registre à l’aide du menu déroulant **tâches** . Il s’agit notamment de l’ajout de nouvelles clés, de la modification du nom ou de l’étendue des clés existantes, de la suppression de clés et de la consultation du registre où se trouvent les clés. Utilisez l’étendue **all settings** pour inclure tous les paramètres de Registre sous la clé spécifiée. Utilisez les **paramètres et** sous-clés pour inclure tous les paramètres de Registre sous les paramètres de clé, de sous-clé et de sous-clé spécifiés.

    -   L’onglet **fichiers** recense le chemin d’accès au fichier et le masque des fichiers des emplacements de fichier inclus dans le modèle d’emplacement des paramètres. Modifiez les emplacements des fichiers à l’aide du menu déroulant **tâches** . Les tâches pour les emplacements de fichiers incluent l’ajout de nouveaux fichiers ou d’emplacements de dossiers, la modification de l’étendue de fichiers ou dossiers existants, la suppression de fichiers ou de dossiers et l’ouverture de l’emplacement sélectionné dans l’Explorateur Windows. Laissez le masque de fichiers vide pour inclure tous les fichiers dans le dossier spécifié.

8.  Cliquez sur **créer** , puis enregistrez le modèle d’emplacement des paramètres sur l’ordinateur.

9.  Cliquez sur **Fermer** pour fermer l’Assistant modèle de paramètres. Quittez l’application de générateur UE-V.

    Après avoir créé le modèle d’emplacement des paramètres pour une application, vous devez tester le modèle. Déployez le modèle dans un environnement de laboratoire avant de le mettre en production dans l’entreprise.

## Rubriques connexes


[Utilisation de modèles UE-V personnalisés et du Générateur UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Opérations d'UE-V1.0](operations-for-ue-v-10.md)

 

 






---
title: Modifier des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V
description: Modifier des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812161"
---
# Modifier des modèles d'emplacement des paramètres UE-V à l'aide du Générateur UE-V


Utilisez le générateur Microsoft User performance (UE-V) pour modifier les modèles d’emplacement des paramètres. Une fois les paramètres revus ajoutés aux modèles à l’aide du générateur UE-V, les informations de version au sein du modèle sont automatiquement mises à jour pour garantir que tous les modèles existants déployés dans l’entreprise soient correctement mis à jour.

**Comment modifier un modèle d’emplacement des paramètres UE-V avec le générateur UE-V**

1.  Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **utilisation de Microsoft**, puis sur générateur de **virtualisation Microsoft User Interface**.

2.  Cliquez sur **modifier un modèle d’emplacement des paramètres**.

3.  Dans la liste des modèles que vous avez utilisés récemment, sélectionnez le modèle à modifier. Vous pouvez également **accéder** au fichier de modèle de paramètres. Cliquez sur **Suivant** pour poursuivre.

4.  Passez en revue les emplacements **Propriétés**, emplacements **du registre** et **fichiers** pour le modèle de paramètres. Apportez les modifications souhaitées.

    -   L’onglet **Propriétés** vous permet d’afficher et de modifier les propriétés suivantes:

        -   **Nom**de l’application: nom de l’application écrit dans la description des propriétés du fichier du programme.

        -   **Nom du programme**: nom du programme que vous avez utilisé dans les propriétés du fichier programme. Ce nom est généralement l’extension. exe.

        -   **Version du produit**: numéro de version du fichier. exe de l’application. Cette propriété, associée à la **version du fichier**, permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres. Cette propriété accepte un numéro de version principal. Si cette propriété est vide, le modèle d’emplacement des paramètres s’appliquera à toutes les versions du produit.

        -   **Version du fichier**: numéro de version du fichier the.exe de l’application. Outre la **version du produit**, cette propriété permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres. Cette propriété accepte un numéro de version principal. Si cette propriété est vide, le modèle d’emplacement des paramètres s’appliquera à toutes les versions du programme.

        -   **Nom** de l’auteur du modèle (facultatif): nom de l’auteur du modèle de paramètres.

        -   **Courrier de création de modèles** (facultatif): adresse de messagerie de l’auteur du modèle d’emplacement des paramètres.

    -   L’onglet **Registre** recense la **clé** et l' **étendue** des emplacements du Registre inclus dans le modèle d’emplacement des paramètres. Vous pouvez modifier les emplacements du Registre à l’aide du menu déroulant **tâches** . Il s’agit notamment de l’ajout de nouvelles clés, de la modification du nom ou de l’étendue des clés existantes, de la suppression de clés et de la consultation du Registre dans lequel se trouvent les clés. Lorsque vous définissez l’étendue du Registre, vous pouvez utiliser l’étendue **all settings** pour inclure tous les paramètres du Registre sous la clé spécifiée. Utilisez **tous les paramètres** et **sous-clés** pour inclure tous les paramètres de Registre sous les paramètres de clé, de sous-clé et de sous-clé spécifiés.

    -   L’onglet **fichiers** recense le chemin d’accès au fichier et le masque des fichiers des emplacements de fichier inclus dans le modèle d’emplacement des paramètres. Vous pouvez modifier les emplacements des fichiers à l’aide du menu déroulant **tâches** . Les tâches pour les emplacements de fichiers incluent l’ajout de nouveaux fichiers ou d’emplacements de dossiers, la modification de l’étendue de fichiers ou dossiers existants, la suppression de fichiers ou de dossiers et l’ouverture de l’emplacement sélectionné dans l’Explorateur Windows. Pour inclure tous les fichiers dans le dossier spécifié, laissez le masque de fichiers vide.

5.  Cliquez sur **Enregistrer** pour enregistrer les modifications apportées au modèle d’emplacement des paramètres.

6.  Cliquez sur **Fermer** pour fermer l’Assistant modèle de paramètres. Quittez l’application de générateur UE-V.

    Après avoir modifié le modèle d’emplacement des paramètres pour une application, vous devez tester le modèle. Déployez le modèle d’emplacement des paramètres révisé dans un environnement de laboratoire avant de le mettre en production dans l’entreprise.

**Modification manuelle d’un modèle d’emplacement des paramètres**

1.  Créer une copie locale du modèle d’emplacement des paramètres (fichier. Xml). Les modèles d’emplacement des paramètres d’UE-V sont des fichiers. xml identifiant les emplacements où les valeurs des paramètres du magasin d’applications.

2.  Ouvrez le fichier de modèle d’emplacement des paramètres à l’aide d’un éditeur XML.

3.  Modifiez le fichier de modèle d’emplacement des paramètres. Toutes les modifications doivent être conformes au fichier de schéma UE-V défini dans SettingsLocationTempate. xsd. Une copie du fichier. xsd se trouve `\ProgramData\Microsoft\UEV\Templates` par défaut.

4.  Enregistrez le fichier de modèle d’emplacement des paramètres, puis fermez l’éditeur XML.

5.  Validez le fichier de modèle d’emplacement des paramètres modifié à l’aide du générateur UE-V. Pour plus d’informations sur la validation du générateur UE-V, voir [valider les modèles d’emplacement des paramètres UE-v auprès d’UE-v Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).

## Rubriques connexes


[Utilisation de modèles UE-V personnalisés et du Générateur UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Opérations d'UE-V1.0](operations-for-ue-v-10.md)

 

 






---
title: Utilisation de modèles UE-V 2 ou x personnalisés et du générateur UE-V 2. x
description: Utilisation de modèles UE-V 2 ou x personnalisés et du générateur UE-V 2. x
author: dansimp
ms.assetid: f0bb4920-0132-472c-a564-abf06a884275
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a8d863896e4ccfa92161f8a8f5e2b8955f139872
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807849"
---
# Utilisation de modèles UE-V 2 ou x personnalisés et du générateur UE-V 2. x


Pour synchroniser les paramètres de l’application entre les ordinateurs des utilisateurs, la virtualisation de l’interface utilisateur de Microsoft (UE-V) 2,0, 2,1 et 2,1 SP1 utilise les *modèles d’emplacement des paramètres*. Certains modèles d’emplacement des paramètres sont inclus dans la virtualisation de l’utilisation de l’utilisateur. Vous pouvez également créer, modifier ou valider des modèles d’emplacements de paramètres personnalisés à l’aide du générateur UE-V.

Le générateur UE-V analyse les applications de bureau Windows pour détecter et capturer les emplacements où l’application stocke les paramètres associés. L’application qui est surveillée doit être une application de bureau. Le générateur UE-V ne peut pas créer de modèle d’emplacement des paramètres pour les types d’applications suivants:

-   Applications virtualisées

-   Applications proposées via les services Terminal Server

-   Applications Java

-   Applications Windows  

Ce sujet

**Emplacements des paramètres standard et non standard:** Le générateur UE-V vous permet d’identifier l’endroit où les applications recherchent les fichiers de paramètres et les paramètres de Registre utilisés par les applications pour le stockage des informations de paramètres. Le générateur Découvre uniquement les paramètres des emplacements accessibles à un utilisateur standard. Les paramètres stockés dans d’autres emplacements sont exclus. Les paramètres détectés sont regroupés en deux catégories: **standard** et **non standard**. Il est recommandé de procéder aux réglages standard pour la synchronisation, et UE-V peut facilement les capturer et les appliquer. Les paramètres non standard peuvent éventuellement synchroniser les paramètres, mais en raison des règles utilisées par UE-V, ces paramètres risquent de ne pas synchroniser les paramètres de manière homogène ou fiable. Ces paramètres peuvent varier en fonction des fichiers temporaires, ce qui peut entraîner une synchronisation peu fiable ou ne pas être utile. Ces paramètres sont présentés dans le générateur UE-V. Vous pouvez décider de les inclure ou de les exclure au cas par cas.

Le générateur UE-V ouvre l’application dans le cadre du processus de découverte. Le générateur peut capturer les paramètres aux emplacements suivants:

-   **Paramètres du Registre** – emplacements du Registre sous **HKEY \ _CURRENT \ _USER**

-   **Fichiers de paramètres d’application** : fichiers stockés dans \ \ **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **itinérance**

Le générateur UE-V exclut les emplacements, qui stockent généralement les fichiers de logiciels d’application, mais ne se synchronisent pas correctement entre les ordinateurs ou les environnements des utilisateurs. Le générateur UE-V exclut ces emplacements. Les emplacements exclus sont les suivants:

-   HKEY \ _CURRENT \ _USER clés de Registre et les fichiers auxquels l’utilisateur connecté ne peut pas écrire de valeurs

-   HKEY \ _CURRENT \ _USER clés de Registre et fichiers associés à la fonctionnalité principale du système d’exploitation Windows.

-   Toutes les clés de Registre situées dans la ruche HKEY \ _LOCAL \ _MACHINE, qui nécessitent des droits d’administrateur, et peuvent nécessiter la définition d’un accord de contrôle de compte d’utilisateur (UAC).

-   Les fichiers situés dans des répertoires de fichiers de programmes, qui nécessitent des droits d’administrateur, peuvent être requis pour définir un accord UAC;

-   Fichiers situés sous utilisateurs \ \ \ [nom d’utilisateur \] \ \ AppData \ \ LocalLow

-   Fichiers du système d’exploitation Windows situés dans% SystemRoot% qui nécessitent des droits d’administrateur et nécessitent éventuellement de définir un accord UAC

Si les clés de Registre et les fichiers qui sont stockés dans ces emplacements sont requis pour synchroniser les paramètres d’application, vous pouvez ajouter manuellement les emplacements exclus au modèle d’emplacement des paramètres lors du processus de création de modèle (à l’exception des entrées de Registre dans le fichier HKEY \ _LOCAL \ _MACHINE Hive).

## <a href="" id="edit"></a>Modifier les modèles d’emplacement des paramètres avec le générateur UE-V


Utilisez le générateur UE-V pour modifier les modèles d’emplacement des paramètres. Lorsque les paramètres revus sont ajoutés aux modèles à l’aide du générateur UE-V, les informations de version au sein du modèle sont automatiquement mises à jour pour vous assurer que tous les modèles existants qui sont déployés dans l’entreprise soient correctement mis à jour.

**Remarques**  Si vous modifiez un modèle 1,0 UE-V à l’aide du générateur UE-V 2, le modèle est automatiquement converti en modèle UE-V 2. UE-V 1,0 agent ne peut plus utiliser le modèle modifié.

 

**Pour modifier un modèle d’emplacement des paramètres UE-V avec le générateur UE-V**

1.  Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **utilisation de Microsoft**, puis sur générateur de **virtualisation Microsoft User Interface**.

2.  Cliquez sur **modifier un modèle d’emplacement des paramètres**.

3.  Dans la liste des modèles que vous avez utilisés récemment, sélectionnez le modèle à modifier. Vous pouvez également cliquer sur **Parcourir** pour rechercher le fichier de modèle de paramètres. Cliquez sur **Suivant** pour poursuivre.

4.  Passez en revue les emplacements **Propriétés**, emplacements **du registre** et **fichiers** pour le modèle de paramètres. Apportez les modifications souhaitées.

    -   Dans l’onglet **Propriétés** , vous pouvez afficher et modifier les propriétés suivantes:

        -   **Nom**de l’application: nom de l’application qui est écrite dans la description des propriétés du fichier du programme.

        -   **Nom du programme**: nom du programme provenant des propriétés du fichier programme. Ce nom est généralement l’extension de nom de fichier. exe.

        -   **Version du produit**: numéro de version du fichier. exe de l’application. Cette propriété, associée à la **version du fichier**, permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres. Cette propriété accepte un numéro de version principal. Si cette propriété est vide, le modèle d’emplacement des paramètres s’applique à toutes les versions du produit.

        -   **Version du fichier**: numéro de version du fichier. exe de l’application. Outre la **version du produit**, cette propriété permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres. Cette propriété accepte un numéro de version principal. Si cette propriété est vide, le modèle d’emplacement des paramètres s’applique à toutes les versions du programme.

        -   **Nom** de l’auteur du modèle (facultatif): nom de l’auteur du modèle de paramètres.

        -   **Courrier de création de modèles** (facultatif): adresse de messagerie de l’auteur du modèle d’emplacement des paramètres.

    -   L’onglet **Registre** recense la **clé** et l' **étendue** des emplacements du Registre inclus dans le modèle d’emplacement des paramètres. Vous pouvez modifier les emplacements du Registre à l’aide du menu déroulant **tâches** . Dans le menu tâches, vous pouvez ajouter de nouvelles clés, modifier le nom ou l’étendue des clés existantes, supprimer des clés et parcourir le registre dans lequel se trouvent les clés. Lorsque vous définissez l’étendue du Registre, vous pouvez utiliser l’étendue **all settings** pour inclure tous les paramètres du Registre sous la clé spécifiée. Utilisez **tous les paramètres** et **sous-clés** pour inclure tous les paramètres de Registre sous les paramètres de clé, de sous-clé et de sous-clé spécifiés.

    -   L’onglet **fichiers** recense le chemin d’accès au fichier et le masque des fichiers des emplacements de fichier inclus dans le modèle d’emplacement des paramètres. Vous pouvez modifier les emplacements des fichiers à l’aide du menu déroulant **tâches** . Dans le menu **tâches** pour l’emplacement des fichiers, vous pouvez ajouter de nouveaux fichiers ou dossiers, modifier l’étendue des fichiers ou dossiers existants, supprimer des fichiers ou des dossiers, et ouvrir l’emplacement sélectionné dans l’Explorateur Windows. Pour inclure tous les fichiers dans le dossier spécifié, laissez le masque de fichiers vide.

5.  Cliquez sur **Enregistrer** pour enregistrer les modifications apportées au modèle d’emplacement des paramètres.

6.  Cliquez sur **Fermer** pour fermer l’Assistant modèle de paramètres. Quittez l’application de générateur UE-V.

    Après avoir modifié le modèle d’emplacement des paramètres pour une application, vous devez tester le modèle. Déployez le modèle d’emplacement des paramètres révisé dans un environnement de laboratoire avant de le mettre en production dans l’entreprise.

**Modification manuelle d’un modèle d’emplacement des paramètres**

1.  Créez une copie locale du fichier modèle d’emplacement des paramètres. Xml. Les modèles d’emplacement des paramètres d’UE-V sont des fichiers. XML qui identifient les emplacements où les valeurs des paramètres du magasin d’applications.

    **Remarques**  Un modèle d’emplacement des paramètres est unique en raison de l' **ID**du modèle. Si vous copiez le modèle et renommez le fichier. xml, l’inscription du modèle échoue car UE-V lit la balise d' **ID** de modèle dans le fichier XML pour déterminer le nom et non le nom de fichier du fichier. Xml. UE-V lit également le numéro de **version** pour savoir s’il a changé. Si le numéro de version est supérieur, UE-V met à jour le modèle.

     

2.  Ouvrez le fichier de modèle d’emplacement des paramètres à l’aide d’un éditeur XML.

3.  Modifiez le fichier de modèle d’emplacement des paramètres. Toutes les modifications doivent être conformes au fichier de schéma UE-V qui est défini dans [SettingsLocationTempate. xsd](https://technet.microsoft.com/library/dn763947.aspx). Par défaut, une copie du fichier. xsd est située dans \\ProgramData\\Microsoft\\UEV\\Templates.

4.  Incrémentez le numéro de **version** du modèle d’emplacement des paramètres.

5.  Enregistrez le fichier de modèle d’emplacement des paramètres, puis fermez l’éditeur XML.

6.  Validez le fichier de modèle d’emplacement des paramètres modifié à l’aide du générateur UE-V.

7.  Vous devez inscrire le modèle d’emplacement des paramètres UE-V modifié pour pouvoir synchroniser les paramètres entre les ordinateurs clients. Pour inscrire un modèle, ouvrez Windows PowerShell, puis exécutez l’applet de commande suivante: `update-uevtemplate [templatefilename]` . Vous pouvez ensuite copier le fichier dans le catalogue de stockage des paramètres. L’agent UE-V sur les ordinateurs des utilisateurs doit alors procéder à la mise à jour selon la planification de la tâche planifiée.

## <a href="" id="validate"></a>Valider les modèles d’emplacement des paramètres avec le générateur UE-V


Il est possible de créer ou de modifier des modèles d’emplacement des paramètres dans un éditeur XML sans utiliser le générateur UE-V. Dans le cas contraire, vous pouvez utiliser le générateur UE-V pour vérifier que le code XML nouveau ou modifié correspond au schéma défini pour le modèle.

**Pour valider un modèle d’emplacement des paramètres UE-V avec le générateur UE-V**

1.  Cliquez sur **Démarrer**, pointez sur **tous les programmes**, sur virtualisation de l' **utilisation de Microsoft**, puis cliquez sur générateur de virtualisation de l’utilisation de **Microsoft**.

2.  Cliquez sur **valider un modèle d’emplacement des paramètres**.

3.  Dans la liste des modèles que vous avez utilisés récemment, sélectionnez le modèle à modifier. Vous pouvez également **accéder** au fichier de modèle de paramètres. Cliquez sur **Suivant** pour poursuivre.

4.  Cliquez sur **valider** pour continuer.

5.  Cliquez sur **Fermer** pour fermer l’Assistant modèle de paramètres. Quittez l’application de générateur UE-V.

    Après avoir validé le modèle d’emplacement des paramètres pour une application, vous devez tester le modèle. Déployez le modèle dans un environnement de laboratoire avant de le placer dans un environnement de production dans l’entreprise.

## <a href="" id="share"></a>Partager des modèles d’emplacement des paramètres avec la Galerie de modèles


La Galerie de modèles 2,0 de Microsoft User performance (UE-V) permet aux administrateurs de partager leurs modèles d’emplacement des paramètres d’UE-V. Dans la Galerie, vous pouvez télécharger les modèles d’emplacement de vos paramètres pour que d’autres utilisateurs puissent les utiliser et télécharger les modèles créés par d’autres utilisateurs. La Galerie de modèles UE-V est située sur Microsoft TechNet [ici](https://go.microsoft.com/fwlink/p/?LinkId=246589).

Avant de partager un modèle d’emplacement des paramètres dans la Galerie de modèles UE-V, assurez-vous qu’il ne contient pas d’informations personnelles ou professionnelles. Vous pouvez utiliser n’importe quelle visionneuse XML pour ouvrir et afficher le contenu d’un fichier de modèle d’emplacement des paramètres. Les valeurs de modèle suivantes doivent être revues avant de partager un modèle avec n’importe quelle personne extérieure à votre entreprise.

-   Nom de l’auteur du modèle – spécifiez un nom général, sans identification pour le nom de l’auteur du modèle ou excluez ces données du modèle.

-   Adresse de messagerie de l’auteur du modèle – spécifiez une adresse de messagerie de création de modèle générale et non identifiant ou excluez ces données du modèle.

Avant de déployer un modèle d’emplacement des paramètres que vous avez téléchargé à partir de la Galerie UE-V, vous devez commencer par tester le modèle pour vous assurer que les paramètres de l’application synchronisent correctement les paramètres dans un environnement de test.






## Rubriques connexes


[Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Déployer UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 






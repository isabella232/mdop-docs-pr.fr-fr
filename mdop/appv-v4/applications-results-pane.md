---
title: Volet de résultats Applications
description: Volet de résultats Applications
author: dansimp
ms.assetid: 977a4d35-5344-41fa-af66-14957b38ed47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdabaeee0b9aaa1c96b6ae732ae4bb5b6d63ef3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807929"
---
# Volet de résultats Applications


Le volet de **résultats applications** de la console de gestion des clients de l’application virtualisation affiche une liste des applications disponibles. Les utilisateurs peuvent consulter la liste des applications pour lesquelles ils ont reçu des privilèges d’accès.

Pour plus d’informations sur les procédures que vous pouvez effectuer dans ce volet, voir [Comment gérer des applications dans la console de gestion des clients](how-to-manage-applications-in-the-client-management-console.md).

Cliquez avec le bouton droit sur n’importe quelle application pour afficher un menu contextuel contenant les éléments suivants.

<a href="" id="new-shortcut"></a>**Nouveau raccourci**  
Cet élément de menu affiche le nouvel Assistant raccourci. Cet Assistant comporte trois pages:

1.  Sélectionnez une icône, puis spécifiez un nom pour le raccourci:

    1.  **Icône modifier**: affiche un navigateur d’icônes Windows standard. Recherchez et sélectionnez l’icône souhaitée.

    2.  **Titre du raccourci**— entrez le nom que vous voulez donner au raccourci. Par défaut, il s’agit du nom existant et de la version de l’application.

2.  Déterminez l’emplacement du raccourci publié.

    1.  **Emplacement du raccourci**: sélectionnez un emplacement en sélectionnant l’une des cases à cocher. Les emplacements disponibles pour le **Bureau**, la **barre d’outils Lancement rapide**, le **menu Envoyer vers**, le **menu Démarrer**et **un autre emplacement**.

    2.  **Programmes dans le menu Démarrer**: lorsque vous activez la case à cocher **menu Démarrer** , ce champ devient actif. Ne renseignez pas ce champ pour publier le raccourci directement à la racine du dossier programmes ou entrez un nom de dossier ou une hiérarchie (par exemple, «mon \ _Computer applications \\Office»). Les raccourcis créés de cette manière sont disponibles uniquement pour l’utilisateur actuel.

    3.  **Un autre emplacement et un** bouton Parcourir: lorsque vous activez la case à cocher **autre emplacement** , ce champ devient actif. Entrez tout emplacement valide sur votre ordinateur ou tout chemin UNC (Universal Naming Convention) disponible (fichier ou répertoire partagé sur un réseau). Le bouton Parcourir permet d’afficher une boîte de dialogue d' **ouverture de fichier** Windows standard.

3.  Entrez les paramètres de ligne de commande souhaités, puis cliquez sur **Terminer** pour quitter l’Assistant.

<a href="" id="new-association"></a>**Nouvelle association**  
Cet élément de menu affiche la nouvelle Assistant Association. Cet Assistant comporte deux pages:

1.  Entrez une extension de nom de fichier, puis associez l’extension à un type de fichier.

    1.  **Extension**: entrez une extension de nom de fichier. Ce champ est vide par défaut.

    2.  **Créer un nouveau type de fichier à l’aide de cette description**: sélectionnez cette case d’option pour entrer une nouvelle description de type de fichier dans le champ actif. Ce bouton est sélectionné par défaut et le champ actif est vide.

    3.  **Appliquer ce type de fichier à tous les utilisateurs**: activez cette case à cocher si vous voulez que cette association soit globale pour tous les utilisateurs. Par défaut, cette case n’est pas cochée.

    4.  **Lier cette extension avec un type de fichier existant**: sélectionnez cette case d’option pour associer l’extension au type de fichier existant. Sélectionnez un type de fichier dans la liste déroulante. Lorsque vous sélectionnez cette option, l’option **suivant** est remplacée par **Terminer**.

2.  Sélectionnez l’application qui doit ouvrir les fichiers portant l’extension spécifiée:

    1.  **Ouvrir des fichiers avec l’application sélectionnée**: sélectionnez cette case d’option pour ouvrir le fichier avec une application existante. Dans la liste déroulante des applications disponibles, choisissez une application.

    2.  **Ouvrez le fichier avec l’Association décrite dans ce fichier OSD**, puis sélectionnez cette case d’option pour spécifier un fichier d’OSD (Open Software Descriptor) qui détermine l’application utilisée pour ouvrir le fichier. Utilisez le bouton Parcourir pour sélectionner un emplacement existant ou entrez un chemin d’accès ou une URL au format HTTP dans ce champ.

<a href="" id="repair"></a>**Repair**  
Rétablit les paramètres par défaut de l’application et élimine tous les paramètres définis par l’utilisateur pour l’application sélectionnée.

<a href="" id="load-or-unload"></a>**Charger** ou **décharger**  
Charge ou décharge l’application sélectionnée dans le cache. Cette commande n’est pas disponible si 100% de l’application se trouve dans le cache.

<a href="" id="clear"></a>**Clear**  
Supprime les paramètres, raccourcis et associations de type de fichier de l’utilisateur pour l’application sélectionnée. Cet élément n’est pas disponible si un utilisateur exécute une application à partir d’une suite d’applications. Affiche une invite de confirmation.

<a href="" id="lock-or-unlock"></a>**Verrouiller** ou **déverrouiller**  
Verrouille ou déverrouille une application dans le cache. Lorsqu’une application est verrouillée, elle ne peut pas être supprimée ou écrasée.

<a href="" id="import"></a>**Import**  
Importe une application dans le cache directement à partir de cette commande dans le nœud **applications** .

<a href="" id="delete"></a>**Delete**  
Supprime une application dans le volet **résultats** et à partir de l’ordinateur, et efface l’application du cache.

<a href="" id="refresh"></a>**Actualiser**  
Actualise le contenu du volet **résultats** .

<a href="" id="properties"></a>**Propriétés**  
Affiche la boîte de dialogue **Propriétés** pour l’application sélectionnée. Cette boîte de dialogue comporte deux onglets:

1.  L’onglet **général** affiche l’icône et le nom de l’application, l’emplacement à partir duquel l’application a été diffusée et le chemin d’accès au fichier OSD local. À partir de cet onglet, vous pouvez modifier l’icône de l’application ou effacer les paramètres (pour supprimer les raccourcis ainsi que les associations de types de fichiers).

2.  L’onglet **package** affiche des informations sur le package de l’application, et vous pouvez **Verrouiller**, **déverrouiller**, **charger**, **décharger**et **Importer** des applications.

<a href="" id="help"></a>**Help**  
Affiche le système d’aide de la console de gestion des clients.

## Affichage des options générales pour le volet résultats


Cliquez avec le bouton droit n’importe où dans le volet **résultats** pour afficher un menu contextuel contenant les éléments suivants.

<a href="" id="new-application"></a>**Nouvelle application**  
Cet élément de menu affiche l’Assistant Nouvelle application. Cet Assistant comporte une page dans laquelle vous pouvez sélectionner une icône pour l’application, puis rechercher ou entrer une URL ou un chemin d’accès au fichier OSD:

1.  **Icône modifier**: affiche un navigateur d’icônes Windows standard. Recherchez et sélectionnez l’icône souhaitée.

2.  **URL ou chemin d’accès au fichier OSD**: entrez un chemin d’accès absolu local, un chemin d’accès UNC complet ou une URL http.

3.  **... (Bouton Parcourir OSD)** : Affiche la boîte de dialogue **ouvrir un fichier** Windows standard. Recherchez le fichier souhaité.

<a href="" id="refresh"></a>**Actualiser**  
Actualise le volet **résultats** .

<a href="" id="export-list"></a>**Exporter la liste**  
Vous pouvez utiliser cet élément de menu pour créer un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** . Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.

<a href="" id="view"></a>**View (Afficher)**  
Cette liste déroulante des éléments de menu vous permet de changer l’apparence et le contenu du volet **résultats** .

<a href="" id="arrange-line-up-icons"></a>**Icônes réorganiser/aligner sur les lignes**  
Les éléments de menu suivants peuvent être utilisés pour modifier l’affichage des icônes dans le volet **résultats** .

<a href="" id="help"></a>**Help**  
Affiche le système d’aide pour la console de gestion.

## Rubriques connexes


[Nœud Applications](applications-node.md)

[Colonnes du volet de résultats Applications](applications-results-pane-columns.md)

[Référence d'Application Virtualization Client Management Console](application-virtualization-client-management-console-reference.md)

[Procédure pour gérer des applications dans Client Management Console](how-to-manage-applications-in-the-client-management-console.md)

 

 






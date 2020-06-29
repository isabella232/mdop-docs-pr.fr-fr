---
title: Volet Résultats d'association de types de fichier
description: Volet Résultats d'association de types de fichier
author: dansimp
ms.assetid: bc5ceb48-1b9f-45d9-a770-1bac90629c76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 73ea8e0e4145aeae309abff362a790287f19f6af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808831"
---
# Volet Résultats d'association de types de fichier


Le volet **résultats** de l' **Association de fichiers** est un niveau sous le volet **système** dans la console de gestion du client de virtualisation des applications, qui affiche une liste des associations de types de fichiers disponibles. Les utilisateurs peuvent voir la liste des extensions de type de fichier et celles auxquelles elles correspondent.

Pour afficher des options spécifiques pour les types de fichiers, cliquez avec le bouton droit sur n’importe quelle extension d’application pour afficher un menu contextuel contenant les éléments suivants.

<a href="" id="delete"></a>**Delete**  
Supprime l’extension de nom de fichier de la liste et supprime l’Association au type de fichier.

<a href="" id="properties"></a>**Propriétés**  
Affiche la boîte de dialogue **Propriétés** de l’extension d’application sélectionnée. Cette boîte de dialogue comporte deux onglets:

-   L’onglet **général** affiche des informations générales sur l’Association de type de fichier, y compris l’icône et le nom de l’application:

    -   **Icône**: affiche l’icône sélectionnée pour le type de fichier associé.

    -   **Nom**de l’Association: affiche le nom du type de fichier.

    -   **Changer d’icône**: cliquez sur ce bouton pour modifier l’icône de l’Association de type de fichier.

    -   **Extension**: affiche l’extension ou les extensions associées à un type de fichier particulier.

    -   **Supprimer**: ce bouton est activé lorsque plusieurs extensions sont associées à une application. Cliquez sur **supprimer le lien** pour gérer l’extension de type de fichier séparément de l’extension avec laquelle elle est actuellement liée.

    -   **Application spécifiée**: sélectionnez cette case d’option, puis choisissez une application dans la liste déroulante des applications disponibles. Vous modifiez l’application utilisée par l’action par défaut. Vous pouvez également rechercher une application, si elle n’est pas disponible dans la liste déroulante.

    -   **Fichier OSD**: sélectionnez cette case d’option et spécifiez un chemin d’accès à un fichier d’OSD (Open Software Descriptor). Vous pouvez également accéder à un fichier OSD.

-   L’onglet **avancé** affiche des informations détaillées sur l’Association de type de fichier:

    -   **Action**: affiche la liste des actions disponibles pour le type de fichier associé.

    -   **Type de contenu**: affiche une description du type de fichier. Si ce champ est laissé vide, le client le remplira.

    -   **Type perçu**: affiche le type de fichier. Vous pouvez sélectionner l’une des options dans la liste déroulante ou ajouter votre propre.

    -   **Confirmer l’ouverture après téléchargement**: activez cette case à cocher pour afficher un message de confirmation après le chargement d’un fichier. Si cette case est cochée, lorsque vous essayez d’ouvrir un fichier de ce type en le téléchargeant dans un navigateur Web, le navigateur vous invite à vérifier si vous voulez enregistrer le fichier directement dans le navigateur sans confirmation.

    -   **Toujours afficher l’extension**: activez cette case à cocher pour spécifier que les extensions doivent être affichées même lorsque l’utilisateur demande que le système doit masquer les extensions des fichiers dont le type est connu.

    -   **Menu Ajouter au nouveau-** activez cette case à cocher pour indiquer que l’extension ou les extensions doivent figurer dans le menu contextuel du **nouveau** Shell.

    -   **Appliquer à tous les utilisateurs**: activez cette case à cocher pour spécifier que les extensions doivent être disponibles pour tous les utilisateurs.

<a href="" id="help"></a>**Help**  
Affiche le système d’aide de la console de gestion des clients.

Pour afficher les options générales du volet **résultats** , cliquez avec le bouton droit n’importe où dans le volet **résultats** pour afficher un menu contextuel contenant les éléments suivants.

<a href="" id="new-association"></a>**Nouvelle association**  
Cet élément de menu affiche la nouvelle Assistant Association. Cet Assistant comporte deux pages:

1.  Entrez une extension de nom de fichier nouvelle ou existante, puis associez l’extension à un type de fichier:

    -   **Extension**— entrez une nouvelle extension de nom de fichier. Ce champ est vide par défaut.

    -   **Créer un nouveau type de fichier à l’aide de cette description**: sélectionnez cette case d’option pour entrer une nouvelle description de type de fichier dans le champ actif. Ce bouton est sélectionné par défaut et le champ actif est vide.

    -   **Appliquer ce type de fichier à tous les utilisateurs**: activez cette case à cocher si vous voulez que cette association soit globale pour tous les utilisateurs. Par défaut, cette case n’est pas cochée.

    -   **Lier cette extension avec un type de fichier existant**: sélectionnez cette case d’option pour associer l’extension au type de fichier existant. Sélectionnez un type de fichier dans la liste déroulante. Lorsque vous sélectionnez cette option, l’option **suivant** est remplacée par **Terminer**.

2.  Sélectionnez l’application qui doit ouvrir les fichiers portant l’extension spécifiée:

    -   **Ouvrir des fichiers avec l’application sélectionnée**: sélectionnez cette case d’option pour ouvrir le fichier avec une application existante. Dans la liste déroulante des applications disponibles, choisissez une application.

    -   **Ouvrez le fichier avec l’Association décrite dans ce fichier OSD**: sélectionnez cette case d’option pour spécifier un fichier OSD qui détermine l’application utilisée pour ouvrir le fichier. Utilisez le bouton Parcourir pour sélectionner un emplacement existant ou entrez un chemin d’accès ou une URL au format HTTP dans ce champ.

<a href="" id="refresh"></a>**Actualiser**  
Cet élément actualise le volet **résultats** .

<a href="" id="export-list"></a>**Exporter la liste**  
Cet élément de menu vous permet de créer un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** . Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.

<a href="" id="view"></a>**View (Afficher)**  
Cette liste déroulante de l’élément de menu vous permet de changer l’apparence et le contenu du volet **résultats** .

<a href="" id="arrange-line-up-icons"></a>**Icônes réorganiser/aligner sur les lignes**  
Les éléments de menu suivants peuvent être utilisés pour modifier l’affichage des icônes dans le volet **résultats** .

<a href="" id="help"></a>**Help**  
Cet élément affiche le système d’aide pour la console de gestion.

## Rubriques connexes


[Procédure pour modifier une icône d'application](how-to-change-an-application-icon.md)

[Nœud Associations de types de fichier](file-type-associations-node-client.md)

[Colonnes du volet Résultats d'association de types de fichier](file-type-association-results-pane-columns.md)

 

 






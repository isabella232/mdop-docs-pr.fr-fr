---
title: Procédure pour gérer manuellement des applications virtuelles
description: Procédure pour gérer manuellement des applications virtuelles
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806977"
---
# Procédure pour gérer manuellement des applications virtuelles


Vous pouvez utiliser la console de gestion des clients Application Virtualization (App-V) pour gérer les applications virtuelles dans le client de bureau App-V ou le client App-V pour les services Bureau à distance. Les administrateurs d’applications-V peuvent utiliser les tâches suivantes:

## Charger ou décharger une application application-V


Vous pouvez utiliser les procédures suivantes pour charger ou décharger une application à partir du cache, directement à partir du volet **résultats** du nœud **application** dans la console de gestion du client de virtualisation des applications. Lorsque vous sélectionnez ce nœud, le volet **résultats** affiche une liste des applications.

**Remarques**  Lorsque vous chargez ou déchargez un package, toutes les applications du package sont chargées ou supprimées du cache. Lors du chargement d’un package, si vous ne disposez pas de suffisamment d’espace dans le cache pour charger les applications, augmentez la taille de cache. Pour plus d’informations sur la taille de cache, voir [modification de la taille de cache et de la désignation de lettre de lecteur](how-to-change-the-cache-size-and-the-drive-letter-designation.md).

 

**Pour charger une application application-V**

1.  Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **charger** dans le menu contextuel.

2.  L’application est automatiquement chargée. Le suivi de l’avancement est effectué dans la colonne intitulé **État du package**. Vous devez actualiser l’affichage pour voir que le chargement est terminé ou pour voir la progression.

**Pour décharger une application application-V**

1.  Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **décharger** dans le menu contextuel.

2.  L’application est automatiquement déchargée et la colonne **État du package** est mise à jour pour refléter la modification.

## Comment effacer une application application-V


Vous pouvez effacer une application de la console directement dans le volet **résultats** du nœud de l' **application** dans la console de gestion du client de virtualisation d’applications. Lorsque vous effacez une application, le système supprime les paramètres, raccourcis et associations de type de fichier qui correspondent à l’application et supprime également l’application de la liste des applications de l’utilisateur.

**Remarques**  Lorsque vous effacez une application de la console, vous ne pouvez plus utiliser cette application. Toutefois, l’application reste en cache et reste disponible pour les autres utilisateurs du même système. Après une actualisation de publication, les applications effacées seront de nouveau accessibles. S’il existe plusieurs applications dans un package, celles-ci ne sont pas supprimées tant que toutes les applications n’ont pas été effacées.

 

**Pour effacer une application de la console**

1.  Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **Effacer** dans le menu contextuel.

2.  Dans l’invite de confirmation, cliquez sur **Oui** pour supprimer l’application ou cliquez sur **non** pour annuler l’opération.

## Comment réparer une application application-V


Pour réparer une application sélectionnée, vous pouvez effectuer la procédure suivante directement à partir du volet **résultats** du nœud **application** dans la console de gestion du client de virtualisation d’applications. Lorsque vous réparez une application, vous supprimez les paramètres utilisateur personnalisés et restaurez les paramètres par défaut. Cette action ne modifie pas ou ne supprime aucun raccourci ou association de type de fichier, et ne supprime pas l’application du cache.

**Pour réparer une application application-V**

1.  Déplacer le curseur dans le volet **résultats** .

2.  Cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **réparer** dans le menu contextuel.

3.  Dans l’invite de confirmation, cliquez sur **Oui** pour réparer l’application ou sur **non** pour annuler.

## Comment importer une application application-V


Vous pouvez utiliser la procédure suivante pour importer une application dans le cache directement à partir du volet **résultats** du nœud de l' **application** dans la console de gestion du client de virtualisation d’applications.

**Pour importer une application application-V**

1.  Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **Importer** dans le menu contextuel.

2.  Dans la fenêtre **Parcourir** , accédez à l’emplacement du fichier de package de l’application voulue, puis cliquez sur **OK**.

    **Remarques**  Si vous avez déjà configuré un chemin de recherche d’importation ou si le fichier SFT figure dans le même chemin que la dernière importation réussie, l’étape 2 n’est pas obligatoire.

     

## Verrouiller ou déverrouiller une application App-V


Vous pouvez utiliser les procédures suivantes pour verrouiller ou déverrouiller n’importe quelle application dans le cache du client de bureau de la virtualisation de l’application ou le client pour les services Bureau à distance. Une application verrouillée ne peut pas être supprimée du cache pour libérer de l’espace pour les nouvelles applications. Pour supprimer une application verrouillée du cache du client de bureau de la virtualisation des applications ou du client du cache des services Bureau à distance, vous devez d’abord la déverrouiller.

**Pour verrouiller une application**

1.  Déplacer le curseur dans le volet **résultats** .

2.  Cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **Verrouiller** dans le menu contextuel. L’application sélectionnée est verrouillée dans le cache.

**Pour déverrouiller une application**

1.  Déplacer le curseur dans le volet **résultats** .

2.  Cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **déverrouiller** dans le menu contextuel. L’application sélectionnée est déverrouillée dans le cache et peut être supprimée.

## Comment supprimer une application application-V


Lorsque vous sélectionnez le nœud d' **application** dans la console de gestion du client de virtualisation des applications, le volet **résultats** affiche une liste d’applications. Vous pouvez utiliser la procédure suivante pour supprimer une application du volet **résultats** , qui supprime également l’application du cache.

**Remarques**  Lorsque vous supprimez une application, l’application sélectionnée ne sera plus disponible pour les utilisateurs de ce client. Les raccourcis et les associations de types de fichiers sont masqués et l’application est supprimée du cache. Toutefois, si une autre application fait référence à des données du cache du système de fichiers pour l’application sélectionnée, ces éléments ne seront pas supprimés.

Après une actualisation de publication, les applications supprimées vous sont à nouveau accessibles.

 

**Pour supprimer une application**

1.  Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **supprimer** dans le menu contextuel.

2.  Dans l’invite de confirmation, cliquez sur **Oui** pour supprimer l’application ou cliquez sur **non** pour annuler l’opération.

## Comment modifier l’icône d’une application application V


Vous pouvez utiliser la procédure suivante pour modifier une icône associée à l’application sélectionnée directement dans le volet **résultats** du nœud **application** de la console de gestion du client de virtualisation d’applications.

**Pour modifier l’icône d’une application**

1.  Positionnez le curseur dans le volet **résultats** , puis cliquez avec le bouton droit sur l’application de votre choix.

2.  Sélectionnez **Propriétés**.

3.  Dans l’onglet **général** , cliquez sur **modifier l’icône**.

4.  Sélectionnez l’icône souhaitée ou naviguez jusqu’à un autre emplacement pour sélectionner l’icône. Après avoir sélectionné l’icône, cliquez sur **OK**. La nouvelle icône s’affiche dans le volet **résultats** .

## Comment ajouter une application application-V


Vous pouvez utiliser la procédure suivante pour ajouter une application directement à partir du volet **résultats** du nœud de l' **application** dans la console de gestion du client de virtualisation d’applications.

**Pour ajouter une application**

1.  Dans le volet **résultats** , cliquez avec le bouton droit et sélectionnez **nouvelle application** dans le menu contextuel.

2.  Dans la page de l’Assistant, vous pouvez effectuer les tâches suivantes:

    1.  **Icône modifier**: affiche un navigateur d’icônes Windows standard. Recherchez et sélectionnez l’icône souhaitée.

    2.  **URL ou chemin d’accès au fichier OSD**: entrez un chemin d’accès absolu local, un chemin d’accès UNC complet (fichier ou répertoire partagé sur un réseau), ou une URL http.

    3.  **(Bouton Parcourir l’OSD)**: affiche la boîte de dialogue **ouvrir un fichier** Windows standard. Recherchez le fichier souhaité.

3.  Cliquez sur **Terminer** pour ajouter l’application au volet **résultats** .

## Publier le raccourci d’une application application V


Vous pouvez utiliser la procédure suivante pour publier des raccourcis vers une application directement à partir du volet **résultats** du nœud de l' **application** dans la console de gestion du client de virtualisation d’applications.

**Pour publier des raccourcis d’application**

1.  Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **nouveau raccourci** dans le menu contextuel pour afficher l’assistant nouveau raccourci.

2.  Dans la première page de l’assistant nouveau raccourci, sélectionnez une icône et attribuez un nom au raccourci.

    1.  **Icône modifier**: affiche un navigateur d’icônes Windows standard. Recherchez et sélectionnez l’icône souhaitée.

    2.  **Titre du raccourci**— entrez le nom que vous voulez donner au raccourci. Par défaut, il s’agit du nom existant et de la version de l’application.

3.  Sur la deuxième page de l’Assistant, déterminez l’emplacement du raccourci publié.

    1.  **Bureau**: activez cette case à cocher pour publier le raccourci sur le bureau.

    2.  **Barre d’outils Lancement rapide**: activez cette case à cocher pour publier le raccourci dans la barre d’outils Lancement rapide.

    3.  **Menu Envoyer vers**: activez cette case à cocher pour publier le raccourci dans le menu **Envoyer vers** .

    4.  **Programmes dans le menu Démarrer**: lorsque vous activez la case à cocher **menu Démarrer** , ce champ devient actif. Ne renseignez pas ce champ pour publier le raccourci directement à la racine du dossier programmes ou entrez un nom de dossier ou une hiérarchie (par exemple, «mon \ _Computer applications \\Office»). Les raccourcis créés de cette manière sont disponibles uniquement pour l’utilisateur actuel.

    5.  **Un autre emplacement et un** bouton **Parcourir** : lorsque vous activez la case à cocher **autre emplacement** , ce champ devient actif. Entrez un emplacement valide sur votre ordinateur ou un chemin d’accès UNC disponible (fichier ou répertoire partagé sur un réseau). Le bouton **Parcourir** permet d’afficher une boîte de dialogue d' **ouverture de fichier** Windows standard.

4.  Dans la troisième page de l’Assistant, entrez les paramètres de ligne de commande souhaités.

5.  Cliquez sur **Terminer** pour publier les raccourcis et quitter le volet **résultats** .

## Comment ajouter une association de type de fichier pour une application application-V


Vous pouvez utiliser la procédure suivante pour ajouter une association de type de fichier à l’aide du nœud **type de fichier** dans la console de gestion du client de virtualisation d’applications.

**Pour ajouter une association de type de fichier**

1.  Cliquez avec le bouton droit sur le nœud **type de fichier** , puis sélectionnez **nouvelle association** dans le menu contextuel.

2.  Terminez la première étape de la boîte de dialogue en complétant les informations suivantes, puis cliquez sur **suivant**:

    1.  **Extension**— entrez une nouvelle extension de nom de fichier. Ce champ est vide par défaut.

    2.  **Créer un nouveau type de fichier à l’aide de cette description**: sélectionnez cette case d’option pour entrer une nouvelle description de type de fichier dans le champ actif. Ce bouton est sélectionné par défaut et le champ actif est vide.

    3.  **Appliquer ce type de fichier à tous les utilisateurs**: activez cette case à cocher si vous voulez que cette association soit globale pour tous les utilisateurs. Par défaut, cette option est désactivée.

    4.  **Lier cette extension avec un type de fichier existant**: sélectionnez cette case d’option pour associer l’extension au type de fichier existant. Sélectionnez un type de fichier dans la liste déroulante. Lorsque vous sélectionnez cette option, l’option **suivant** est remplacée par **Terminer**.

3.  Terminez la deuxième étape de la boîte de dialogue en complétant les informations suivantes, puis cliquez sur **Terminer** pour revenir à la console de gestion du client:

    1.  **Changer d’icône**: cliquez sur ce bouton pour modifier l’icône de l’application. Sélectionnez l’une des icônes disponibles ou accédez à un nouvel emplacement, puis sélectionnez une icône.

    2.  **Ouvrir des fichiers avec l’application sélectionnée**: sélectionnez cette case d’option pour ouvrir le fichier avec une application existante. Dans la liste déroulante des applications disponibles, choisissez une application.

    3.  **Ouvrez le fichier avec l’Association décrite dans ce fichier OSD**, puis sélectionnez cette case d’option pour spécifier un fichier d’OSD (Open Software Descriptor) qui détermine l’application utilisée pour ouvrir le fichier. Utilisez le bouton Parcourir pour sélectionner un emplacement existant ou entrez un chemin d’accès ou une URL au format HTTP dans ce champ.

## Comment supprimer une association de type de fichier pour une application application-V


Vous pouvez utiliser la procédure suivante pour supprimer une association de type de fichier. Le nœud de **type de fichier** est un niveau sous le nœud **Application Virtualization** dans le volet de l' **étendue** . Lorsque vous sélectionnez ce nœud, le volet **résultats** affiche une liste des associations de types de fichiers.

**Pour supprimer une association de type de fichier**

1.  Dans le volet **résultats** , cliquez avec le bouton droit sur l’extension de l’Association de type de fichier que vous voulez supprimer.

2.  Dans le menu contextuel, sélectionnez **supprimer** .

3.  Cliquez sur **Oui** pour supprimer l’Association ou cliquez sur **non** pour revenir au volet **résultats** .

## Rubriques connexes


[Application Virtualization Client](application-virtualization-client.md)

 

 






---
title: Nœud Licences d'applications
description: Nœud Licences d'applications
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807937"
---
# Nœud Licences d'applications


Le nœud **applications licenses** est le niveau inférieur au nœud système de virtualisation des applications dans le volet de l' **étendue** de la console de gestion du serveur d’applications. Lorsque vous sélectionnez ce nœud, le volet **résultats** affiche une liste de licences et de groupes de licences. Les types de licence suivants sont disponibles:

-   **Licence illimitée**: permet d’accéder à un nombre d’utilisateurs simultanés. Cette méthode de gestion des licences est appropriée lorsque vous voulez associer une licence à l’échelle de l’entreprise à une application.

-   **Licence simultanée**: permet de définir le nombre maximal d’utilisateurs simultanés autorisés à utiliser l’application.

-   **Licence nommée**: vous permet d’attribuer une licence à un utilisateur individuel. Une licence nommée peut être utilisée pour s’assurer qu’un utilisateur particulier sera toujours en mesure d’exécuter l’application.

**Remarques**  Vous pouvez combiner des licences concomitantes et nommées pour la même application.

 

Cliquez avec le bouton droit sur le nœud **applications** pour afficher un menu contextuel contenant les éléments suivants.

<a href="" id="new-unlimited-license"></a>**Nouvelle licence illimitée**  
Affiche la nouvelle licence illimité de l’Assistant. Cet Assistant comprend les pages suivantes:

1.  Entrez le nom du groupe de licences dans le champ **nom du groupe de licences applications** , puis entrez une valeur (en minutes) dans le champ **Avertissement d’expiration** de la licence. (Vous pouvez entrer n’importe quelle valeur comprise entre 0 et 100.) Vous pouvez également utiliser les flèches vers le haut et le bas pour sélectionner le nombre de minutes.

2.  Entrez un texte descriptif bref dans le champ de **Description de licence** , puis activez la case à cocher **activé** pour activer la licence.

    Vous pouvez également utiliser le champ **Date d’expiration** pour spécifier une date d’expiration pour la licence. Vous pouvez activer la case à cocher pour utiliser la date d’expiration affichée ou vous pouvez utiliser l’utilitaire calendrier pour accéder à la date d’expiration souhaitée.

3.  Cliquez sur **Terminer** pour ajouter la nouvelle licence.

<a href="" id="new-concurrent-license"></a>**Nouvelle licence simultanée**  
Affiche le nouvel Assistant licence concomitante. Cet Assistant comporte les trois pages suivantes et est presque identique au nouvel Assistant licence illimité:

1.  Entrez le nom du groupe de licences dans le champ **nom du groupe de licences applications** , puis entrez une valeur (en minutes) dans le champ **Avertissement d’expiration** de la licence. (Vous pouvez entrer n’importe quelle valeur comprise entre 0 et 100.) Vous pouvez également utiliser les flèches vers le haut et le bas pour sélectionner le nombre de minutes.

2.  Entrez un texte descriptif bref dans le champ Description de la **licence** , puis entrez une valeur dans le champ **nombre de licences simultanées** .

    Vous pouvez également utiliser les flèches haut et bas pour spécifier le nombre de licences simultanées. Cochez la case **activé** pour activer la licence.

    Vous pouvez également utiliser le champ **Date d’expiration** pour spécifier une date d’expiration pour la licence. Vous pouvez activer la case à cocher pour utiliser la date d’expiration affichée ou vous pouvez utiliser l’utilitaire calendrier pour accéder à la date d’expiration souhaitée.

3.  Cliquez sur **Terminer** pour ajouter les nouvelles licences.

<a href="" id="new-named-license"></a>**Nouvelle licence nommée**  
Affiche la nouvelle Assistant licence nommée. Cet Assistant comporte les quatre pages suivantes:

1.  Entrez le nom du groupe de licences dans le champ **nom du groupe de licences applications** , puis entrez une valeur (en minutes) dans le champ **Avertissement d’expiration** de la licence. (Vous pouvez entrer n’importe quelle valeur comprise entre 0 et 100). Vous pouvez également utiliser les flèches vers le haut et le bas pour sélectionner le nombre de minutes.

2.  Entrez un texte descriptif bref dans le champ de **Description de licence** , puis activez la case à cocher **activé** pour activer la licence.

    Vous pouvez également utiliser le champ **Date d’expiration** pour spécifier une date d’expiration pour la licence. Vous pouvez activer la case à cocher pour utiliser la date d’expiration affichée ou vous pouvez utiliser l’utilitaire calendrier pour accéder à la date d’expiration souhaitée.

3.  Cliquez sur **Ajouter**, **modifier**ou **supprimer** des utilisateurs nommés.

4.  Cliquez sur **Terminer** pour ajouter la nouvelle licence.

<a href="" id="view"></a>**View (Afficher)**  
Change l’aspect et le contenu du volet **résultats** .

<a href="" id="new-window-from-here"></a>**Nouvelle fenêtre à partir de cet emplacement**  
Ouvre une nouvelle console de gestion avec le nœud sélectionné en tant que nœud racine.

<a href="" id="refresh"></a>**Actualiser**  
Actualise l’affichage du serveur.

<a href="" id="export-list"></a>**Exporter la liste**  
Crée un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** . Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.

<a href="" id="help"></a>**Help**  
Affiche le système d’aide pour la console de gestion du serveur d’applications.

Si vous cliquez sur un groupe de licences ou une licence qui s’affiche sous le nœud **licences d’application** dans le volet de l' **étendue** , les éléments suivants sont disponibles.

<a href="" id="view"></a>**View (Afficher)**  
Change l’aspect et le contenu du volet **résultats** .

<a href="" id="new-window-from-here"></a>**Nouvelle fenêtre à partir de cet emplacement**  
Ouvre une nouvelle console de gestion avec le nœud sélectionné en tant que nœud racine.

<a href="" id="delete"></a>**Delete**  
Supprime un package du volet **résultats** .

<a href="" id="rename"></a>**Rename**  
Modifie le nom d’un package dans le volet **résultats** .

<a href="" id="export-list"></a>**Exporter la liste**  
Crée un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** . Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.

<a href="" id="properties"></a>**Propriétés**  
Affiche la boîte de dialogue **Propriétés** du groupe de licences sélectionné. L’onglet **général** de la boîte de dialogue **Propriétés** affiche des informations sur le groupe de licences et vous permet de changer la valeur d’heure dans le champ **Avertissement d’expiration** de la licence. L’onglet **applications** affiche la liste des applications associées au groupe de licences.

<a href="" id="help"></a>**Help**  
Affiche le système d’aide pour la console de gestion du serveur d’applications.

## Rubriques connexes


[À propos de l'octroi de licence pour les applications](about-application-licensing.md)

[Procédure pour gérer des licences d'applications dans Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Server Management Console: nœud Licences d'applications](server-management-console-application-licenses-node.md)

 

 






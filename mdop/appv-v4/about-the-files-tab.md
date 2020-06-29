---
title: À propos de l'onglet Fichiers
description: À propos de l'onglet Fichiers
author: dansimp
ms.assetid: 3c20e720-4b0f-465b-b7c4-3013dae1c815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e71cd0b60f9722da9736fc6987100f5c7bf53ab
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808102"
---
# À propos de l'onglet Fichiers


L’onglet **fichiers** affiche la liste complète des fichiers inclus dans un package d’application séquencé. Le volet de gauche affiche, dans un format de navigation standard, la liste complète des fichiers du package créé lors du séquençage de l’application. Ces fichiers incluent le répertoire racine du package (le répertoire que vous avez spécifié lors de la phase d’installation de l’application), le dossier système de fichiers virtuel (VFS) et les fichiers de l’environnement virtuel. Le volet droit affiche le nom de fichier, les attributs de fichier et les attributs de Sequencer.

## Nom de fichier et nom court


<a href="" id="file-name"></a>**Nom de fichier**  
Le nom du fichier se trouve dans le volet gauche. Les fichiers qui s’affichent dans le volet gauche sont créés lors du séquençage.

<a href="" id="short-name"></a>**Nom court**  
Il s’agit du nom d’un fichier sélectionné dans le volet gauche, écrit dans la Convention d’affectation de noms de format 8,3.

## Attributs de fichier


<a href="" id="file-size"></a>**Taille du fichier**  
Taille du fichier en octets.

<a href="" id="file-version"></a>**Version du fichier**  
Version du fichier sélectionné.

<a href="" id="date-created"></a>**Date de création**  
Date et heure de création du fichier sélectionné.

<a href="" id="date-modified"></a>**Date de modification**  
Date et heure auxquelles le fichier sélectionné a été modifié pour la dernière fois.

<a href="" id="file-id"></a>**File ID**  
GUID du fichier.

## Attributs de Sequencer


<a href="" id="user-data"></a>**Données utilisateur**  
Sélectionnez cet attribut pour spécifier qu’une application doit conserver les informations d’un utilisateur individuel.

<a href="" id="application-data"></a>**Données d’application**  
Sélectionnez cet attribut pour spécifier qu’une application doit conserver les informations générales d’un groupe d’utilisateurs.

<a href="" id="override"></a>**Remplacer**  
Lorsqu’il est sélectionné, le client de bureau de virtualisation des applications remplace le fichier correspondant lors de la mise à niveau du package d’application séquencé et de son flux vers le client. Si cette case n’est pas cochée, le client détermine s’il souhaite remplacer le fichier sélectionné.

## Rubriques connexes


[Procédure pour modifier les fichiers inclus dans un package](how-to-modify-the-files-included-in-a-package.md)

[Console Sequencer](sequencer-console.md)

 

 






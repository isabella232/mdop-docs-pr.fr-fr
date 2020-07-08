---
title: Notes de publication d'App-V4.6SP1
description: Notes de publication d'App-V4.6SP1
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808066"
---
# Notes de publication d'App-V4.6SP1


Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.

**Important**  Lisez attentivement ces notes de publication avant d’installer le système de gestion Microsoft Application Virtualization (App-V). Ces notes de publication contiennent des informations qui vous permettent d’installer correctement la virtualisation des applications (App-V) 4.6 SP1. Ce document contient des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents App-V, la dernière modification doit être considérée comme faisant autorité.

 

## Se protéger contre les failles de sécurité et les virus


Pour vous aider à vous protéger contre les failles de sécurité et les virus, il est important d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé. Pour plus d’informations, consultez le [site Web de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) sur la sécurité ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problèmes connus liés à la virtualisation d’application 4.6 SP1


Cette section fournit les informations les plus récentes sur les problèmes liés à Microsoft Application Virtualization (App-V) 4.6 SP1. Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire. Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures.

### Le chemin d’accès à partir de SPRT est perdu s’il ne se termine pas par une barre oblique (/)

Si le chemin d’accès dans une expression HREF dans un modèle de projet ne se termine pas par une barre oblique ( **/** ), le chemin d’accès généré n’inclut pas le chemin. Cela se produit lorsque l’utilisateur manipule manuellement le fichier **. SPRT** . Si vous utilisez le Sequencer, il ajoute toujours la barre oblique ( **/** ) après la trajectoire.

Solution de contournement Assurez-vous que l’adresse HREF comporte une barre oblique de fin ( **/** ).

### Le nom du dossier utilisateur ne correspond pas au nom du package

Les dossiers contenant des fichiers user et global. pkg n’incluent plus le nom du package. Auparavant, le client App-V a utilisé pour utiliser le nom court du dossier racine du package 8,3 dans le cadre du nom du dossier. Cela vous permet de l’identifier facilement. Lorsque vous utilisez le Sequencer App-V 4,6 SP1, le dossier racine du package 8,3 noms courts est désormais une chaîne aléatoire. Ainsi, il est difficile d’identifier les dossiers contenant les fichiers **. pkg** du package sur l’ordinateur exécutant le client App-V.

Solution de contournement utilisez l’une des méthodes suivantes pour identifier les dossiers de packages plus facilement:

1.  Lorsque vous créez le package en utilisant le Sequencer, spécifiez un nom de dossier qui suit la Convention d’affectation de noms 8,3 pour le dossier d’application principal. Ce nom sera utilisé comme partie intégrante du nom du dossier utilisateur, comme dans le cas de l’App-V 4,6.

2.  Le fichier. sprj contient désormais une balise qui affiche la chaîne utilisée comme début du nom du dossier utilisateur. Vous pouvez utiliser l’élément **ShortName** de l’élément **PACKAGEROOTFOLDER** pour déterminer le nom.

### Exécution de App-V 4,6 SP1 sur des ordinateurs dotés de plus de 64 processeurs

Lorsque vous exécutez App-V 4,6 SP1 sur des ordinateurs dotés de plus de 64 processeurs, le client App-V échoue.

Solution de contournement aucune. Cette configuration n’est pas prise en charge. Vous devez exécuter des ordinateurs App-V 4,6 SP1on dont le nombre est inférieur à 64 processeurs.

### La mise à jour de la virtualisation des applications 4,6 SP1 n’est pas proposée pour les paramètres régionaux qui utilisent Microsoft Update

Lorsque vous utilisez Microsoft Update, la mise à jour pour App-V 4,6 SP1 n’est pas disponible pour les paramètres régionaux de langue suivants:

-   Kazakh

-   Hindi

-   Serbe-cyrillique

Solution de contournement si vous utilisez Microsoft Windows Server Update Services (WSUS) utilisez la version anglaise de la mise à jour ou téléchargez la mise à jour à partir du catalogue Microsoft Update.

### Après avoir développé le package parent, vous ne pouvez pas séquencer un plug-in avec des composants côte à côte.

Lorsque vous développez un package parent en utilisant les **Outils**  /  **développer le package sur le système local** dans la console de Sequencer App-V et que vous séquencez un plug-in avec des composants côte à côte, une erreur d’installation est renvoyée. Exemple:

-   **HRESULT 0x80073712**

Cela est dû au moment où le Sequencer écrit le composant côte à côte dans le registre, mais n’efface pas la valeur de la clé de Registre suivante:

HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

Solution de contournement après avoir développé le package parent sur l’ordinateur qui exécute le Sequencer, vous devez supprimer la valeur pour la clé de Registre suivante:

HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

Après avoir supprimé la valeur, séquencez le plug-in.

### Informations de copyright des notes de publication

Ce document est fourni «en l’absence». Les informations et les modes d’affichage exprimés dans ce document, tels que les URL et les autres références de site Web Internet, risquent de changer sans préavis. Vous assumez le risque d’utilisation.

Quelques exemples présentés dans les présentes sont fournis à titre indicatif uniquement et sont fictifs. Aucune association ou connexion réelle ne doit être intentionnelle ou intentionnelle.

Ce document ne vous fournit aucun droit légal de propriété intellectuelle de tout produit Microsoft. Vous pouvez copier le présent document pour une utilisation interne à des fins de référence. Vous pouvez modifier ce document à des fins de référence interne.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server et Windows Vista sont des marques commerciales du groupe Microsoft de sociétés.

Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.

 

 






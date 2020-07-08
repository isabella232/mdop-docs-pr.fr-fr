---
title: Comment gérer la redirection d'URL à l'aide du Gestionnaire de package de l'espace de travail MED-V
description: Comment gérer la redirection d'URL à l'aide du Gestionnaire de package de l'espace de travail MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810782"
---
# Comment gérer la redirection d'URL à l'aide du Gestionnaire de package de l'espace de travail MED-V


Vous pouvez utiliser le gestionnaire de package d’espace de travail MED-V pour gérer la redirection d’URL dans l’espace de travail MED-V.

**Pour gérer la redirection d’adresse Web dans un espace de travail MED-V**

1.  Pour ouvrir le **Gestionnaire de package de l’espace de travail MED-v**, cliquez sur **Démarrer**, **tous les programmes**, cliquez sur **Microsoft Enterprise Desktop Virtualization**, puis sur **med-v Workspace**.

2.  Dans le volet principal de l' **empaquetage de l’espace de travail MED-V** , cliquez sur **gérer la redirection Web**.

3.  Dans la fenêtre **gérer la redirection Web** , vous pouvez taper, coller ou importer une liste d’URL redirigées vers Internet Explorer dans l’espace de travail MED-V.

    **Remarque**  
    La redirection d’URL dans MED-V ne prend en charge que les protocoles HTTP et HTTPs. MED-V ne fournit pas de prise en charge pour FTP ou tout autre protocole.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. Cliquez sur **Enregistrer sous...** pour enregistrer les fichiers de redirection d’URL mis à jour dans le dossier spécifié. MED-V crée un fichier de Registre qui contient les informations de redirection d’URL mises à jour. Déployez la clé de Registre mise à jour à l’aide d’une stratégie de groupe. Pour plus d’informations sur l’utilisation d’une stratégie de groupe, voir [installation de logiciels de stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   MED-V crée également un script Windows PowerShell dans le dossier spécifié que vous pouvez utiliser pour recréer le package d’espace de travail MED-V mis à jour.

## Rubriques connexes


[Comment ajouter ou supprimer des informations de redirection des URL dans un espace de travail MED-V déployé](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[Gérer la redirection d'URL MED-V](manage-med-v-url-redirection.md)










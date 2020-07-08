---
title: Comment convertir un package créé dans une version précédente d'App-V
description: Comment convertir un package créé dans une version précédente d'App-V
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805670"
---
# Comment convertir un package créé dans une version précédente d'App-V


Vous pouvez utiliser l’utilitaire convertisseur de package pour mettre à niveau des packages d’application virtuels qui ont été créés dans des versions antérieures d’App-V.

**Remarque**  
Si vous utilisez un ordinateur avec une architecture 64 bits, vous devez utiliser la version x86 de PowerShell.



Le convertisseur de package peut uniquement convertir les packages qui ont été créés à l’aide du Sequencer App-V 4,5 ou d’une version ultérieure. Les packages créés à l’aide d’une version antérieure à App-V 4,5 doivent être mis à niveau vers le format App-V 4,5 ou App-V 4,6 avant la conversion.

Les informations suivantes fournissent une direction pour la conversion des packages d’application virtuelle existants.

**Important**  
Vous devez configurer le convertisseur de package de façon à ce qu’il enregistre toujours le fichier de composants du package dans un emplacement et un répertoire sécurisés. Un emplacement sécurisé est accessible uniquement par un administrateur. Par ailleurs, lorsque vous déployez le package, vous devez enregistrer le package à un emplacement sécurisé ou vérifier qu’aucun autre utilisateur ne peut être connecté lors du processus de conversion.



**Prise en main**

1.  Installez le Sequencer App-V sur un ordinateur de votre environnement. Pour plus d’informations sur la façon d’installer le Sequencer, voir [Comment installer le Sequencer](how-to-install-the-sequencer-beta-gb18030.md).

2. Importer le module PowerShell requis

```powershell
Import-Module AppVPkgConverter
```

3. Les applets de commande suivantes sont disponibles:

   -   Test-AppvLegacyPackage: cette applet de contrôle est conçue pour vérifier les packages. Il renverra des informations sur les échecs liés au package, tels que les fichiers **. SFT** manquants, une source non valide, des erreurs de fichier **. OSD** ou une version de package non valide. Cette applet de contrôle n’analyse pas le fichier **. SFT** ou effectue une validation approfondie. Pour plus d’informations sur les options et les fonctionnalités de base pour cette applet de cmdlet, utilisez la fonction de saisie semi-seule PowerShell `Test-AppvLegacyPackage -?` .

   -   ConvertFrom-AppvLegacyPackage: pour convertir un package existant, tapez `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` . Dans cette commande, `c:\contentStore` représente l’emplacement du package existant et `c:\convertedPackages` est le répertoire de sortie dans lequel le fichier de package d’application virtuelle App-V 5,0 doit être enregistré. Par défaut, si vous ne spécifiez pas de nouveau nom, le nom de l’ancien package sera utilisé pour le nom de fichier App-V 5,0.

       Par ailleurs, le convertisseur de package optimise les performances des packages dans l’application-V 5,0 en définissant le package sur l’erreur de mise en flux du package App-V.  C’est plus performant que le bloc de fonctionnalités principal et qu’il télécharge entièrement le package. L’indicateur **DownloadFullPackageOnFirstLaunch** vous permet de convertir le package et de définir le package comme étant entièrement téléchargé par défaut.

       **Remarque**  
       Avant de spécifier le répertoire de sortie, vous devez créer le répertoire de sortie.



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)










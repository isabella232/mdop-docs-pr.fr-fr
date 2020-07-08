---
title: Procédure pour publier une application virtuelle sur le client
description: Procédure pour publier une application virtuelle sur le client
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806881"
---
# Procédure pour publier une application virtuelle sur le client


Lorsque vous déployez la virtualisation d’application à l’aide d’un système de distribution de logiciels électronique, vous pouvez utiliser l’une des procédures suivantes pour publier un package d’application pour vos utilisateurs.

**Pour publier un package à l’aide d’un fichier Windows Installer autonome**

1.  Le client doit être installé avec le paramètre *RequireAuthorizationIfCached* défini sur 0 (zéro). Pour plus d’informations sur la définition de ce paramètre, voir [paramètres de ligne de commande du programme d’installation de l’application virtualisation du client](application-virtualization-client-installer-command-line-parameters.md)

2.  Copiez le fichier Windows Installer et le fichier SFT dans le même dossier sur l’ordinateur cible.

3.  Exécutez la commande suivante sur votre ordinateur:

    `Msiexec.exe /I "packagename.msi" /q`

**Pour publier un package à l’aide du programme d’installation Windows et du manifeste du package**

1.  Copiez le fichier du programme d’installation Windows sur l’ordinateur cible et le fichier SFT dans le partage de contenu sur le serveur de diffusion.

2.  Exécutez la commande suivante sur l’ordinateur de l’utilisateur:

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    **Important**  Pour OVERRIDEURL, tous les caractères de barre oblique inverse doivent être placés dans une séquence d’échappement en utilisant une barre oblique inverse précédente ou le chemin OVERRIDEURL ne sera pas analysé correctement. De plus, les propriétés et les valeurs doivent être entrées en majuscules sauf si la valeur est un chemin d’accès à un fichier.

     

**Pour publier un package à l’aide de SFTMIME**

-   Pour obtenir un exemple de publication d’une application pour tous les utilisateurs sur un ordinateur, exécutez la commande suivante sur l’ordinateur de l’utilisateur:

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    Pour plus d’informations sur ces commandes de SFTMIME et d’autres, voir [référence aux commandes SFTMIME](sftmime--command-reference.md).

## Rubriques connexes


[Choisir une méthode de publication](determine-your-publishing-method.md)

[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Référence de commande SFTMIME](sftmime--command-reference.md)

[Scénario de distribution autonome pour les clients Application Virtualization Client](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 






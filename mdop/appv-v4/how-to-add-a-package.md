---
title: Procédure pour ajouter un package
description: Procédure pour ajouter un package
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808730"
---
# Procédure pour ajouter un package


Vous pouvez ajouter un package à partir de la console de gestion du serveur d’applications, de la manière suivante:

-   Importer une application, qui crée le package automatiquement dans le processus.

-   Ajoutez un package manuellement.

Il est recommandé d’importer des applications au lieu de les ajouter manuellement. Pour plus d’informations sur l’importation d’applications, voir [Comment importer une application](how-to-import-an-applicationserver.md).

**Pour ajouter manuellement un package**

1.  Dans la console de gestion de l’application virtualisation du serveur, cliquez avec le bouton droit sur le nœud **packages** dans le volet gauche, puis sélectionnez **nouveau package**.

2.  Dans la boîte de dialogue **nouveau package** , tapez un nom dans le champ **nom du package** .

3.  Recherchez ou tapez un nom de chemin d’accès dans le champ chemin d’accès **complet du fichier de package** . Il doit s’agir d’un fichier SFT.

    **Remarques**  Si vous naviguez jusqu’au fichier SFT, remplacez le chemin d’accès local (par exemple, C:\\Program Files\\User\ _Apps \\Virtual\ _App \ _Server \\Content) par le nom d’hôte statique ou l’adresse IP du serveur. L’utilisation de la variable *% SFT \ _SOFTGRIDSERVER%* nécessite une configuration d’ordinateur par client.

    Dans les boîtes de dialogue qui font référence aux serveurs d’applications virtuelles, vous devez utiliser un emplacement réseau, tel que le nom d’hôte statique ou l’adresse IP du serveur auquel vos utilisateurs peuvent accéder. Le fichier OSD (Open Software Descriptor) de l’application peut remplacer la variable d’espace réservé *% SFT \ _SOFTGRIDSERER%* par le nom d’hôte statique ou l’adresse IP du serveur. Si vous laissez la variable PlaceHolder, vous devez définir cette variable sur chaque ordinateur client qui accédera à ce serveur. Définissez une variable utilisateur ou système sur chaque ordinateur pour la fonction SFT \ _SOFTGRIDSERVER. La valeur de la variable doit correspondre au nom d’hôte statique ou à l’adresse IP du serveur. Si vous définissez une variable, quittez la session du client, déconnectez-vous et reconnectez-vous à Microsoft Windows, puis redémarrez la session sur chaque ordinateur sur lequel une session est en cours d’exécution et où la variable a été définie.

     

4.  Cliquez sur **Suivant**.

5.  La boîte de dialogue **récapitulative** indique l’emplacement du fichier et vous invite à copier le fichier dans l’emplacement si vous ne l’avez pas déjà fait. Cliquez sur **Terminer** une fois que vous avez vérifié les informations.

    **Remarques**  Si vous gérez des applications sur un serveur distant, dans la boîte de dialogue suivante, tapez uniquement le chemin d’accès du fichier relatif à la racine de contenu du serveur.

     

## Rubriques connexes


[Procédure pour importer une application](how-to-import-an-applicationserver.md)

[Procédure pour gérer les packages dans Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 






---
title: Procédure pour déployer l'image de récupération DaRT à l'aide d'une clé USB
description: Procédure pour déployer l'image de récupération DaRT à l'aide d'une clé USB
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810092"
---
# Procédure pour déployer l'image de récupération DaRT à l'aide d'une clé USB


Lorsque vous avez fini d’exécuter l' **Assistant image de récupération DART**, vous pouvez utiliser l’outil sur <https://go.microsoft.com/fwlink/?LinkId=218888> pour copier le fichier image ISO sur un disque mémoire flash USB (UFD).

Vous pouvez également copier manuellement le fichier image ISO sur un disque UFD en suivant les étapes décrites dans cette section.

**Pour enregistrer l’image de récupération DaRT sur une clé USB**

1.  Mettre en forme la clé USB.

    1.  À partir d’un système d’exploitation valide ou d’une session WindowsPE, insérez votre UFD.

    2.  À l’invite de commandes avec des autorisations d’administrateur, tapez **diskpart** , puis tapez **List Disk**.

        La fenêtre d’invite de commandes affiche le numéro de disque de votre UFD (par exemple, **Disk 1**).

    3.  Entrez les commandes suivantes une à la fois à l’invite de commandes.

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        **Remarques**  L’exemple de code précédent suppose que Disk1 est le UFD. Le cas échéant, remplacez le disque 1 par le numéro de votre disque.

         

2.  À l’aide de la méthode de montage préférée d’une image par votre entreprise, montez le fichier image ISO que vous avez créé dans la boîte de dialogue **créer une image de démarrage** de l' **Assistant image de récupération DART**. Pour cela, il est nécessaire d’avoir une méthode disponible pour monter un fichier image.

3.  Ouvrez le fichier image ISO monté et copiez son contenu sur la clé USB mise en forme.

    **Remarques**  Si vous avez gravé un CD ou un DVD de l’image de récupération, vous pouvez ouvrir les fichiers sur le CD ou DVD et copier le contenu sur le UFD. Cela vous permet d’ignorer la nécessité de monter l’image.

     

## Rubriques connexes


[Déploiement de l'image de récupération DaRT7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 






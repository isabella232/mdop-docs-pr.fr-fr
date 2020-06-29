---
title: Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération
description: Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810026"
---
# Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération


Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition de récupération dans une image Windows 7.

**Pour déployer DaRT dans la partition de récupération d’une image Windows 7**

1.  Créez une partition cible dans votre image Windows 7 qui est égale ou supérieure à la taille du fichier image ISO que vous avez créé à l’aide de l' **Assistant image de récupération DART**.

    La taille minimale requise pour une partition DaRT est d’environ 300 Mo. Toutefois, nous recommandons à 450MB de prendre en charge les fonctionnalités de connexion à distance dans DaRT.

2.  Extrayez le fichier Boot. wim du fichier image ISO DaRT.

    1.  Montez le fichier image ISO que vous avez créé dans la boîte de dialogue **créer une image de démarrage** en utilisant la méthode préférée de montage d’une image par votre entreprise.

    2.  Ouvrez le fichier image ISO et copiez le fichier Boot. wim du dossier \\sources de l’image montée vers un emplacement sur votre ordinateur ou sur un lecteur externe.

        **Remarques**  Si vous avez gravé un CD ou un DVD de l’image de récupération, vous pouvez ouvrir les fichiers sur le CD-ROM ou le DVD et copier le fichier Boot. wim à partir du dossier \\sources. Cela vous permet d’ignorer la nécessité de monter l’image.

         

3.  Utilisez le fichier Boot. wim pour créer une partition de récupération démarrable en utilisant la méthode standard de votre entreprise pour créer une image Windows RE personnalisée.

    Pour plus d’informations sur la création et la personnalisation d’une partition de récupération, voir [Personnalisation de l’utilisation de Windows RE](https://go.microsoft.com/fwlink/?LinkId=214222).

4.  Remplacez la partition cible dans votre image Windows 7 par la partition de récupération.

Lorsque votre image de Windows 7 est prête, répartir l’image sur les ordinateurs de votre entreprise à l’aide du processus de déploiement d’images standard de votre entreprise. Pour plus d’informations sur la création d’une image Windows 7, voir [création d’une image standard de Windows 7: guide étape par étape](https://go.microsoft.com/fwlink/?LinkId=212103).

Pour plus d’informations sur le déploiement d’une solution de récupération pour réinstaller l’image de fabrique en cas de panne du système, voir [déployer une image de récupération du système](https://go.microsoft.com/fwlink/?LinkId=214221).

## Rubriques connexes


[Déploiement de l'image de récupération DaRT7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 






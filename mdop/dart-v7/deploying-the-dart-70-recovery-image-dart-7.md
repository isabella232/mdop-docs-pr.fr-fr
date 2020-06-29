---
title: Déploiement de l'image de récupération DaRT7.0
description: Déploiement de l'image de récupération DaRT7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804392"
---
# Déploiement de l'image de récupération DaRT7.0


Une fois que vous avez créé le fichier ISO (International Organization for Standardization) qui contient l’image de récupération du Microsoft Diagnostics and Recovery Tools (DaRT) 7, vous pouvez déployer l’image de récupération DaRT dans l’ensemble de votre entreprise afin qu’elle soit disponible pour les utilisateurs finaux et les agents du support technique. Il existe quatre méthodes prises en charge que vous pouvez utiliser pour déployer l’image de récupération DaRT.

-   Gravez le fichier image ISO sur un CD ou un DVD

-   Enregistrez le contenu du fichier image ISO sur un disque mémoire flash USB (UFD).

-   Extraire le fichier Boot. wim de l’image ISO et le déployer en tant que partition distante disponible sur les ordinateurs des utilisateurs finaux

-   Extraire le fichier Boot. wim de l’image ISO et le déployer dans la partition de récupération d’une nouvelle installation de Windows 7

**Important**  L' **Assistant image de récupération DART** vous permet uniquement de graver un CD ou un DVD. Toutes les autres méthodes d’enregistrement et de déploiement de l’image de récupération nécessitent des étapes supplémentaires qui impliquent des outils qui ne sont pas inclus dans DaRT. Des conseils et des liens pour ces autres méthodes sont fournis dans cette section.

 

## Déploiement de l’image de récupération DaRT à l’aide d’un lecteur flash USB


Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT, vous pouvez utiliser l’outil sur <https://go.microsoft.com/fwlink/?LinkId=218888> pour copier le fichier image ISO sur un disque mémoire flash USB (UFD).

[Procédure pour déployer l'image de récupération DaRT à l'aide d'une clé USB](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## Déploiement de l’image de récupération DaRT dans le cadre d’une partition de récupération


Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition de récupération dans une image Windows 7.

[Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## Déploiement de l’image de récupération DaRT en tant que partition distante


Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition distante sur le réseau.

[Procédure pour déployer l'image de récupération DaRT sous forme de partition distante](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## Autres ressources pour la mise à jour du déploiement de l’image de récupération DaRT


-   [Déploiement de DaRT7.0](deploying-dart-70-new-ia.md)

 

 






---
title: Déploiement de l'image de récupération DaRT
description: Déploiement de l'image de récupération DaRT
author: dansimp
ms.assetid: df5cb54a-be8c-4ed2-89ea-d3c67c2ef4d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e445873324f005455ba3c96319847dea8ba761ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810361"
---
# Déploiement de l'image de récupération DaRT


Une fois que vous avez créé le fichier ISO (International Organization for Standardization) qui contient l’image de récupération du Microsoft Diagnostics and Recovery Tools (DaRT 8,0), vous pouvez déployer l’image de récupération de DaRT 8,0 au sein de votre entreprise afin qu’elle soit disponible aux utilisateurs finaux et aux travailleurs du support technique. Il existe quatre méthodes prises en charge que vous pouvez utiliser pour déployer l’image de récupération DaRT. Pour connaître les avantages et inconvénients de chaque méthode, voir [planification de l’enregistrement et du déploiement de l’image de récupération 8,0 de DART](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

Gravez le fichier image ISO sur un CD ou un DVD à l’aide de l’Assistant image de récupération DaRT

Enregistrez le contenu du fichier image ISO sur un lecteur flash USB à l’aide de l’Assistant image de récupération DaRT.

Extraire le fichier Boot. wim de l’image ISO et le déployer en tant que partition distante disponible sur les ordinateurs des utilisateurs finaux

Extraire le fichier Boot. wim de l’image ISO et le déployer dans la partition de récupération d’une nouvelle installation de Windows 8

**Important**  L' **Assistant image de récupération DART** vous permet de graver l’image sur un CD, un DVD ou un lecteur USB, mais les autres méthodes d’enregistrement et de déploiement de l’image de récupération nécessitent des étapes supplémentaires qui impliquent des outils qui ne sont pas inclus dans DART. Des conseils et des liens pour ces autres méthodes sont fournis dans cette section.

 

## Déploiement de l’image de récupération DaRT dans le cadre d’une partition de récupération


Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition de récupération dans une image Windows 8.

[Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-8.md)

## Déploiement de l’image de récupération DaRT en tant que partition distante


Vous pouvez héberger l’image de récupération sur un serveur de démarrage réseau central, tel que les services de déploiement Windows, et autoriser les utilisateurs ou l’équipe de support à diffuser une image sur des ordinateurs à la demande.

[Procédure pour déployer l'image de récupération DaRT sous forme de partition distante](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-8.md)

## Autres ressources pour le déploiement de l’image de récupération DaRT


[Déploiement de DaRT8.0](deploying-dart-80-dart-8.md)

 

 






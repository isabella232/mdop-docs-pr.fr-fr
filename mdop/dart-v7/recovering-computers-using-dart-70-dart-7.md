---
title: Récupération des ordinateurs à l'aide de DaRT7.0
description: Récupération des ordinateurs à l'aide de DaRT7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809552"
---
# Récupération des ordinateurs à l'aide de DaRT7.0


Deux méthodes sont disponibles pour récupérer des ordinateurs à l’aide de Microsoft Diagnostics and Recovery Tools (DaRT) 7. Vous pouvez exécuter l’image de récupération DaRT7 localement ou utiliser la fonctionnalité de connexion à distance disponible dans DaRT7 pour récupérer un ordinateur distant. Les deux méthodes sont décrites plus en détail dans cette section.

## Récupérer des ordinateurs locaux en utilisant l’image de récupération DaRT


Pour récupérer un ordinateur local à l’aide de DaRT7, vous devez avoir une présentation physique de l’ordinateur de l’utilisateur final rencontrant des problèmes qui nécessitent DaRT.

Vous avez le choix entre différentes méthodes pour démarrer DaRT, en fonction du déploiement de l’image de récupération DaRT.

-   Insérez un CD, un DVD ou un lecteur flash USB dans l’ordinateur défectueux, puis utilisez-le pour démarrer l’ordinateur.

-   Démarrez dans DaRT à partir d’une partition de récupération sur l’ordinateur qui pose problème.

-   Démarrez dans DaRT à partir d’une partition distante sur le réseau.

Pour plus d’informations sur les avantages et inconvénients de chaque méthode, voir [planification de l’enregistrement et du déploiement de l’image de récupération 7,0 de DART](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).

Quelle que soit la méthode que vous utilisez pour démarrer dans DaRT, vous devez activer le périphérique de démarrage dans le BIOS pour l’option de démarrage ou les options que vous voulez mettre à disposition de l’utilisateur final.

**Remarques**  La configuration du BIOS est unique, en fonction du type de disque dur, de cartes réseau et d’autres éléments utilisés au sein de votre organisation.

 

[Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## Récupérer des ordinateurs distants à l’aide de l’image de récupération DaRT


Grâce à la fonctionnalité de connexion à distance de DaRT, un administrateur informatique exécute les outils DaRT à distance sur un ordinateur d’utilisateur final. Lorsque certaines informations sont fournies par l’utilisateur final (ou par un professionnel du support technique travaillant sur l’ordinateur de l’utilisateur final), l’administrateur informatique ou l’agent de support technique peut prendre le contrôle de l’ordinateur de l’utilisateur final et exécuter les outils DaRT nécessaires à distance.

**Important**  Les deux ordinateurs qui établissent une connexion à distance doivent faire partie du même réseau.

 

La fenêtre du **jeu d’outils de diagnostics et de récupération** inclut la possibilité d’exécuter le DART sur un ordinateur d’utilisateur final à distance à partir d’un ordinateur d’administration. L’utilisateur final ouvre les outils DaRT sur le problème et démarre la session à distance en cliquant sur **connexion à distance**.

La fonctionnalité de connexion à distance sur l’ordinateur de l’utilisateur final crée les informations de connexion suivantes: un numéro de ticket, un port et une liste de toutes les adresses IP disponibles. Le numéro de ticket et le port sont générés de manière aléatoire.

L’administrateur informatique ou l’agent de support technique entre ces informations dans la **visionneuse de connexion à distance DART** pour établir la connexion aux services Terminal Server à l’ordinateur de l’utilisateur final. La connexion de services Terminal Server établie permet à un administrateur informatique d’interagir à distance avec les outils DaRT sur l’ordinateur de l’utilisateur final. L’ordinateur de l’utilisateur final traite alors les informations de connexion, partage son écran et répond aux instructions de l’ordinateur de l’administrateur informatique.

[Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## Autres ressources pour récupérer des ordinateurs à l’aide de DaRT7


[Opérations de DaRT7.0](operations-for-dart-70-new-ia.md)

 

 






---
title: Publication d'applications virtuelles à l'aide de la distribution électronique de logiciels
description: Publication d'applications virtuelles à l'aide de la distribution électronique de logiciels
author: dansimp
ms.assetid: 295fbc1d-ed1c-43b4-aeee-0df384d4e630
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0354fc1226aa78d947dd764a0ab6157b563a321
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806429"
---
# Publication d'applications virtuelles à l'aide de la distribution électronique de logiciels


Un système de distribution de logiciels électronique (ESD) est conçu pour déplacer efficacement des logiciels vers de nombreux ordinateurs en fonction de la vitesse de connexion réseau lente ou rapide. Avec la virtualisation des applications, à l’aide d’un système ESD, vous pouvez utiliser l’une des méthodes suivantes pour distribuer vos packages d’application virtuelle:

-   Configurez votre système de ESD pour distribuer les packages directement à chaque ordinateur client à l’aide de la version Windows Installer du package généré par le Sequencer. Le fichier du programme d’installation Windows contient les icônes, les informations de définition du package et le contenu et, lorsque vous utilisez le programme d’installation Windows, il publie les icônes sur le bureau Windows et le menu Démarrer, et charge le contenu du package dans le cache du client de virtualisation des applications. L’utilisateur peut commencer immédiatement à utiliser les applications sans configuration requise. Pour procéder à la mise à niveau d’un package vers une version plus récente, vous pouvez utiliser le programme d’installation Windows pour désinstaller le fichier package.msi, puis installer la nouvelle version.

-   Placez le contenu du package sur un serveur de diffusion de logiciels ou un serveur de diffusion en continu qui est facilement accessible aux ordinateurs clients par le biais d’une connexion réseau ayant une bande passante suffisante, par exemple un réseau local. Par exemple, vous pouvez utiliser les ordinateurs aux points de distribution système ESD existants dans chaque succursale. Utiliser des paramètres de ligne de commande pour définir la source de diffusion en continu à partir de laquelle les clients fluxront sur le package d’application virtuelle, le système ESD déploierait la version Windows Installer du package sur chaque client. Le système ESD peut également être utilisé pour copier le fichier SFT qui contient le contenu du package vers le partage de fichiers sur tous les serveurs de diffusion. Pour procéder à la mise à niveau d’un package vers une version plus récente, vous pouvez utiliser le programme d’installation Windows pour désinstaller le fichier package.msi, puis installer la nouvelle version.

-   À l’instar de l’utilisation du fichier Windows Installer autonome dans l’un ou l’autre des modes de déploiement des packages, vous pouvez contrôler le déploiement d’une manière bien plus détaillée à l’aide de l’application virtualisation d’application SFTMIME. Cela fournit de nombreuses commandes permettant de contrôler tous les aspects de la gestion des packages. Même si SFTMIME est puissant, il est également complexe, de sorte que les administrateurs doivent envisager de créer toutes les commandes en tant que scripts et de les tester complètement dans un environnement de test avant d’être utilisés en production. Pour plus d’informations sur les commandes SFTMIME disponibles, voir [référence aux commandes SFTMIME](sftmime--command-reference.md).

## Rubriques connexes


[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Planification du déploiement du système Application Virtualization](planning-for-application-virtualization-system-deployment.md)

[Planification de votre solution de diffusion en continu dans une implémentation de distribution électronique de logiciels](planning-your-streaming-solution-in-an-electronic-software-distribution-implementation.md)

[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 






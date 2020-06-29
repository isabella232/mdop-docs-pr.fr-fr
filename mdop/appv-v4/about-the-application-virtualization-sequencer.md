---
title: À propos d'Application Virtualization Sequencer
description: À propos d'Application Virtualization Sequencer
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808130"
---
# À propos d'Application Virtualization Sequencer


Le Sequencer Microsoft Application Virtualization (App-V) vérifie et enregistre tous les processus d’installation et de configuration pour une application et crée les fichiers suivants: **ico**, **OSD**, **SFT**et **SPRJ**. Ces fichiers contiennent toutes les informations nécessaires sur une application afin que l’application puisse s’exécuter dans un environnement virtuel sur des ordinateurs cibles. Vous pouvez utiliser le Sequencer Microsoft Application Virtualization (App-V) pour créer des applications virtuelles. Après avoir séquencé une application, celle-ci peut être diffusée sur des ordinateurs cibles, ou les ordinateurs cibles peuvent exécuter l’application virtuelle en téléchargeant le contenu du package d’application virtuelle et en exécutant l’application localement.

**Important**  Pour exécuter un package d’application virtuelle, l’ordinateur cible doit exécuter la version appropriée du client App-V.

 

Les packages d’applications virtuelles s’exécutent sur des ordinateurs cibles sans interagir avec le système d’exploitation sous-jacent sur l’ordinateur cible, car chaque application s’exécute dans un environnement virtuel et est isolé d’autres applications installées ou exécutées sur l’ordinateur cible. Cette isolation peut réduire les conflits d’application et permettre de réduire le nombre d’applications de test avant déploiement nécessaires.

## Terminologie de Sequencer


<a href="" id="application-virtualization-drive"></a>Lecteur de virtualisation des applications  
Le lecteur d’applications virtuelles est le lecteur par défaut (Q:\) de l’ordinateur cible à partir duquel les applications séquencées sont exécutées.

<a href="" id="ico-file"></a>Fichier ICO  
Fichier d’icône sur le Bureau du client utilisé pour lancer une application séquencée.

<a href="" id="installation-directory"></a>Répertoire d’installation  
Répertoire utilisé par le Sequencer pour placer les fichiers d’installation lors de l’installation.

<a href="" id="open-software-descriptor--osd--file"></a>Ouvrir un fichier d’OSD (Open Software Descriptor)  
Fichier XML demandant au client App-V de récupérer l’application séquencée à partir du serveur de streaming App-V et l’exécution de l’application séquencée dans l’environnement virtuel.

<a href="" id="package-root-directory"></a>Répertoire racine du package  
Le répertoire sur l’ordinateur de séquençage sur lequel sont installés les fichiers pour le package d’application séquencé. Ce répertoire existe également virtuellement sur l’ordinateur sur lequel une application séquencée sera diffusée.

<a href="" id="sequenced-application"></a>Application séquencée  
Application surveillée par le Sequencer, réparties dans des blocs de fonctionnalités principaux et secondaires, diffusées sur un ordinateur cible exécutant le client App-V et exécutant un environnement virtuel.

<a href="" id="sequenced-application-package"></a>Package d’application séquencé  
Fichiers comprenant une application virtuelle et autorisant l’exécution d’une application virtuelle. Ces fichiers sont créés après le séquençage et incluent spécifiquement les fichiers **. OSD**, **. SFT**, **. sprj**et **. ico** .

<a href="" id="sequencing"></a>Séquençage  
Processus de création d’un package d’application à l’aide du Sequencer App-V. Dans ce processus, une application est surveillée, ses raccourcis sont configurés et un package d’application séquencé est créé.

<a href="" id="sequencing-computer"></a>Séquençage d’un ordinateur  
Ordinateur utilisé pour séquencer une application.

<a href="" id="virtual-application"></a>Application virtuelle  
Application empaquetée par le Sequencer pour s’exécuter dans un environnement virtuel autonome. L’environnement virtuel contient les informations nécessaires à l’exécution de l’application sur le client sans installer l’application localement.

<a href="" id="primary-feature-block"></a>Bloc de fonctions principal  
Le contenu minimal d’un package d’application virtuel qui est nécessaire pour qu’une application s’exécute sur un ordinateur cible. Le contenu du bloc de fonctionnalité principal est identifié lors de la phase d’application du séquençage et se compose généralement du contenu des fonctionnalités d’application les plus utilisées.

## <a href="" id="sequencing-applications-"></a>Séquençage des applications


Il existe deux méthodes pour créer et modifier des packages d’application virtuels dans votre environnement. La première méthode consiste à utiliser l’Assistant **séquençage** . L’Assistant **séquençage** vous permet de créer de nouveaux packages d’applications virtuelles ou de modifier ceux-ci. Pour plus d’informations sur l’utilisation de l’Assistant **séquençage** , voir [Comment séquencer une nouvelle application](how-to-sequence-a-new-application.md). La deuxième méthode consiste à utiliser la ligne de commande. La ligne de commande vous permet de créer de nouveaux packages d’applications virtuelles ou de modifier ceux-ci à l’aide de l’invite de commandes. Pour plus d’informations sur l’utilisation de la ligne de commande, voir [Comment gérer des applications virtuelles à l’aide de la ligne de commande](how-to-manage-virtual-applications-using-the-command-line.md).

L’Assistant **séquençage** fournit les fonctions suivantes pour créer des packages d’applications virtuelles:

1.  **Configuration du package**: l’Assistant de **séquençage** invite à entrer les informations de configuration de package nécessaires pour compléter le fichier d’affichage de description du logiciel (OSD) ouvert, qui est un fichier requis pour le démarrage d’un package d’application séquencé.

2.  **Installation**de l’application: l’Assistant **séquençage** recueille des informations sur les configurations de démarrage et d’installation d’une application. Il surveille et enregistre les informations d’installation et de démarrage associées à l’application afin de créer les fichiers nécessaires à la création d’un package d’application virtuelle.

3.  **Démarrage**de l’application: l’Assistant **séquençage** recueille des informations pour compiler et commander les blocs de code nécessaires à l’exécution initiale du package d’application séquencé sur l’ordinateur cible. Le bloc de code de compilation est appelé bloc de fonctionnalité principal.

## Considérations en matière de sécurité du séquenceur d’applications


Le Sequencer App-V exécute tous les services détectés au moment du séquençage à l’aide du compte système local et n’applique pas les descripteurs de sécurité sur les demandes de contrôle de service. Si le service a été installé à l’aide d’un autre compte d’utilisateur ou si les descripteurs de sécurité sont destinés à accorder des autorisations de service spécifiques à différents groupes d’utilisateurs, Déterminez soigneusement si le service doit être virtualisé. Dans certains cas, vous devez installer le service localement pour vous assurer que la sécurité de service prévue est préservée.

**Important**  Vous devez toujours enregistrer les packages d’application virtuels dans un emplacement sécurisé.

 

## Rubriques connexes


[Vue d'ensemble d'Application Virtualization Sequencer](application-virtualization-sequencer-overview.md)

 

 






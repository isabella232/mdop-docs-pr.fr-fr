---
title: Meilleures pratiques pour Application Virtualization Sequencer
description: Meilleures pratiques pour Application Virtualization Sequencer
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809090"
---
# Meilleures pratiques pour Application Virtualization Sequencer


Cette rubrique décrit les meilleures pratiques pour exécuter le Sequencer Microsoft Application Virtualization (App-V). Examinez et prenez en compte les recommandations suivantes lors de la planification et de l’utilisation du Sequencer dans votre environnement.

## Pratiques recommandées pour la configuration de l’ordinateur


Pour configurer l’ordinateur exécutant le Sequencer App-V, les meilleures pratiques suivantes doivent être prises en compte:

-   **Séquence sur un ordinateur ayant une configuration similaire et exécutant une version antérieure du système d’exploitation que les ordinateurs cibles.**

    Assurez-vous que l’ordinateur exécutant le Sequencer exécute une version antérieure du système d’exploitation que les ordinateurs cibles. Cela inclut les versions du Service Pack et de mise à jour. Par exemple, si les ordinateurs cibles exécutent Vista et WindowsXP, il est préférable de séquencer les applications sur un ordinateur exécutant WindowsXP. La possibilité de séquencer sur un système d’exploitation et d’exécuter l’application virtualisée sur un autre système d’exploitation n’est pas garantie et dépend de l’application et du système d’exploitation spécifiques. Si vous rencontrez des problèmes, il est possible que vous deviez effectuer une séquence sur le même environnement de système d’exploitation que celui sur lequel le client App-V est en cours d’exécution.

-   **Configurer l’ordinateur exécutant le Sequencer avec plusieurs partitions.**

    Vous devez configurer l’ordinateur exécutant le Sequencer avec au moins deux partitions principales. La première partition (**C:**) doit contenir le système d’exploitation et elle doit être mise en forme à l’aide du système de fichiers NTFS. La deuxième partition (**Q:**) est utilisée en tant que chemin de destination de l’installation de l’application virtuelle et doit également être mise en forme à l’aide du système de fichiers NTFS.

-   **Configurez le répertoire temporaire avec suffisamment d’espace libre sur le disque.**

    Le Sequencer utilise le répertoire **% tmp%** ou **% temp%** , ainsi que le répertoire de **travail** pour le stockage des fichiers temporaires lors du séquençage. Vous devez configurer ces répertoires sur l’ordinateur exécutant le Sequencer dont l’espace disque disponible correspond à la configuration estimée requise pour l’installation de l’application. Pour vérifier l’emplacement du répertoire de **travail** , vous pouvez ouvrir la console de Sequencer et sélectionner des **Outils**, des **options**, puis sélectionner l’onglet **chemins d’accès** . la configuration des répertoires TEMP et du répertoire de **travail** sur différentes partitions de disque dur peut améliorer les performances lors du séquençage.

-   **Séquencez des applications à l’aide de Microsoft VirtualPC.**

    Vous allez séquentiellement la plupart des applications. Pour faciliter cela, vous devez envisager le séquençage sur un ordinateur exécutant un environnement virtuel. Cela vous permettra de séquencer une application et de revenir à un état propre, avec une reconfiguration minimale, sur l’ordinateur exécutant le Sequencer.

    Si vous exécutez Microsoft Hyper-V dans votre environnement, le Sequencer App-V sera exécuté lorsque l’ordinateur virtuel Hyper-V sur lequel il s’exécute est:

    -   en pause et en reprise.

    -   a son état enregistré et restauré.

    -   enregistré en tant qu’instantané et est restauré.

    -   migration vers un autre matériel dans le cadre d’une migration dynamique.

-   **Avant de séquencer une nouvelle application, arrêtez les autres programmes en cours d’exécution.**

    Les processus et tâches planifiées qui s’exécutent normalement sur l’ordinateur de séquençage peuvent ralentir le processus de séquençage et provoquer la collecte de données inappropriées lors du séquençage. Toutes les applications et tous les programmes inutiles doivent être fermés avant de commencer à effectuer le séquençage.

-   **Séquence sur un ordinateur exécutant un service Terminal Server**

    Vous ne devez pas configurer le mode installation sur un ordinateur exécutant les services Terminal Server avant d’installer le Sequencer.

## Recommandations en matière de séquençage


Les meilleures pratiques suivantes doivent être envisagées lors du séquençage d’une nouvelle application:

-   

    **Remarques**  Si vous exécutez App-V 4,6 SP1, vous n’avez pas besoin d’effectuer de séquence vers un répertoire qui suit la Convention de nommage 8,3.

     

-   **Séquence vers un répertoire unique qui suit la Convention d’affectation de noms 8,3.**

    Vous devez effectuer une séquence de toutes les applications dans un répertoire qui suit la Convention d’affectation de noms 8,3. Le nom du répertoire spécifié ne peut pas contenir plus de huit caractères, suivi d’une extension de nom de fichier à trois caractères (par exemple, **Q:\\MYAPP. ABC**.

-   **Séquence vers un dossier de destination à la racine du lecteur, et non vers un sous-répertoire.**

    Si la suite d’applications est composée de plusieurs parties, installez chaque application dans un sous-répertoire du répertoire principal. Par exemple, si un package contient une application conjointement avec un client, utilisez **Q:\\AppSuite** en tant qu’annuaire principal, puis séquencez l’application principale sur **Q:\\AppSuite\\Main**, puis séquencez le client sur **Q:\\AppSuite\\Client**.

-   **Configurez et testez l’application lors de la phase d’installation.**

    L’exécution de l’installation d’une application implique souvent d’effectuer plusieurs étapes manuelles qui ne font pas partie du processus d’installation de l’application. Cette procédure peut impliquer la configuration d’une connexion à une base de données ou la copie des fichiers mis à jour. Vous devez effectuer ces configurations lors de la phase d’installation, puis exécuter l’application pour vérifier qu’elle fonctionne.

-   **Exécutez l’application autant de fois que nécessaire, jusqu’à ce que le programme soit stable.**

    Vous devez exécuter l’application plusieurs fois pendant l’installation pour garantir que toutes les configurations d’inscription et de boîte de dialogue associées aient été effectuées. L’ouverture de l’application à plusieurs reprises lors de l’installation permet de garantir que seules les fonctionnalités d’application pertinentes sont chargées dans le **bloc de fonctionnalités principal**.

-   **Désactiver toutes les fonctionnalités de mise à jour automatique associées à l’application.**

    Certaines applications peuvent vérifier automatiquement les mises à jour les plus récentes lors de l’installation. Pour vous aider à effectuer le contrôle de version des packages d’application virtuelle, vous devez désactiver cette fonctionnalité lors du séquençage. S’il existe des mises à jour requises, vous devez effectuer une nouvelle création de package d’application virtuelle avec les mises à jour associées installées.

## Rubriques connexes


[Planification du déploiement du système Application Virtualization](planning-for-application-virtualization-system-deployment.md)

 

 






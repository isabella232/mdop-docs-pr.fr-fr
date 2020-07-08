---
title: Vue d'ensemble de la console Application Virtualization Sequencer
description: Vue d'ensemble de la console Application Virtualization Sequencer
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809209"
---
# Vue d'ensemble de la console Application Virtualization Sequencer


Le Sequencer Application Virtualization (App-V) crée des applications pour pouvoir s’exécuter dans un environnement virtuel, en tant qu’applications virtuelles. Après avoir séquencé une application, celle-ci peut être exécutée à partir d’un serveur App-V pour cibler les ordinateurs qui exécutent le client de bureau App-v ou le client App-V pour les services Bureau à distance (auparavant services Terminal Server) à l’aide d’un processus appelé streaming. Le Sequencer App-V analyse le processus d’installation et de configuration des applications, et enregistre toutes les informations nécessaires à l’exécution de l’application dans l’environnement virtuel. Ce processus détermine également les fichiers et configurations applicables à tous les utilisateurs et aux configurations que les utilisateurs peuvent personnaliser. Les applications virtuelles s’exécutent sur des ordinateurs cibles et n’ont aucun effet sur le système d’exploitation exécuté sur l’ordinateur cible ou sur toutes les applications installées sur l’ordinateur cible.

## Considérations en matière de sécurité du séquenceur d’applications


Le Sequencer App-V exécute tous les services détectés au moment du séquençage à l’aide du compte système local et n’applique pas les descripteurs de sécurité sur les demandes de contrôle de service. Si le service a été installé à l’aide d’un autre compte d’utilisateur ou si les descripteurs de sécurité sont destinés à accorder des autorisations de service spécifiques à différents groupes d’utilisateurs, Déterminez soigneusement si le service doit être virtualisé. Dans certains cas, vous devez installer le service localement pour vous assurer que la sécurité de service prévue est préservée.

## Options de menu de la console de numérotation des applications


Les éléments de menu suivants sont disponibles dans la console App-V du Sequencer:

-   **Fichier**: contient différentes commandes pour vous permettre de créer, d’ouvrir, de modifier et d’enregistrer des applications séquencées.

-   **Edit**: contient différentes commandes permettant de modifier des applications virtuelles existantes.

-   **Affichage**: contient diverses commandes permettant d’afficher les propriétés d’une application virtuelle.

-   **Outils**— contient différents outils et diagnostics pour la configuration des applications virtuelles.

## Options de la barre d’outils de la barre de la console Application Virtualization


Les boutons de la barre d’outils suivants sont disponibles dans la console App-V du Sequencer:

-   **Nouveau package**: cliquez sur pour créer une application séquencée.

-   **Ouvrir**: cliquez pour ouvrir un package d’application séquencé dans la console de Sequencer App-V.

-   **Ouvrir pour la mise à niveau**: cliquez sur pour ouvrir une application séquencée afin de mettre à niveau ou d’appliquer une mise à jour.

-   **Enregistrer**: cliquez sur pour enregistrer une application virtuelle séquencée.

-   **Assistant de séquençage**: cliquez sur pour ouvrir l’Assistant séquençage. Utilisez ce bouton pour démarrer l’Assistant séquençage si vous apportez des modifications sous l’onglet **général** , sous options **Outils**  /  **Options**.

## Onglets des applications virtuelles


Les onglets suivants sont affichés lors de l’affichage d’une application virtuelle dans la console de Sequencer App-V:

-   **Propriétés**: affiche des informations sur l’application virtuelle sélectionnée. Vous pouvez mettre à jour le **nom du package** et les **Commentaires** associés à l’application virtuelle.

-   **Déploiement**: affiche des informations sur la façon dont l’application virtuelle est accessible par les ordinateurs cibles. Vous pouvez configurer la méthode de remise des applications virtuelles et vous pouvez configurer les systèmes d’exploitation qui doivent s’exécuter sur l’ordinateur cible. Vous pouvez également configurer les options de sortie associées. Si vous envisagez de demander aux clients d’accéder à une application virtuelle à partir d’un fichier, utilisez le format suivant lorsque vous spécifiez le chemin d’accès: **file://Server/Share/Path/.SFT**. Activez l’option **appliquer les descripteurs de sécurité** afin de préserver la sécurité associée au package lors d’une mise à niveau ou les autorisations seront réinitialisées lors de la mise à niveau.

-   **Historique des modifications**: affiche des informations sur les mises à jour apportées à l’application virtuelle.

-   **Fichiers**: affiche les fichiers associés à l’application virtuelle sélectionnée. Vous pouvez effectuer des révisions secondaires des propriétés de fichier associées en utilisant les champs appropriés.

-   **Registre virtuel**: affiche le registre virtuel associé à l’application virtuelle sélectionnée. Vous pouvez ajouter ou supprimer des clés de registre en cliquant avec le bouton droit sur l’entrée appropriée.

-   **Système de fichiers virtuel**: affiche les systèmes de fichiers virtuels associés à l’application virtuelle sélectionnée. Vous pouvez ajouter, supprimer ou modifier des entrées dans le système de fichiers dans cet onglet en cliquant avec le bouton droit sur l’entrée appropriée et en sélectionnant l’option.

-   **Services virtuels**: affiche les services associés à l’application virtuelle sélectionnée.

-   **OSD**: affiche les informations relatives à l’ouverture de l’OSD (Open Software Descriptor) associée à l’application virtuelle. Vous pouvez mettre à jour les fichiers associés au fichier OSD en cliquant avec le bouton droit sur l’entrée appropriée et en sélectionnant l’action souhaitée.

## Rubriques connexes


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 






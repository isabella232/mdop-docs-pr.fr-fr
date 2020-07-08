---
title: Procédure d'utilisation du fichier Differential SFT
description: Procédure d'utilisation du fichier Differential SFT
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806686"
---
# Procédure d'utilisation du fichier Differential SFT


Lorsque vous séquençagez une application, le Sequencer Microsoft Application Virtualization (App-V) crée des fichiers SFT (. sft) pour stocker tout le contenu et les informations de configuration de chaque application virtuelle. Dans la version 4.5 de App-V, le fichier SFT SFT (. dsft) a été introduit. Après avoir utilisé le Sequencer pour créer une mise à niveau d’un package existant, vous pouvez choisir de générer ce fichier pour stocker uniquement les différences entre le package d’application séquencé d’origine et la nouvelle version. C’est donc beaucoup plus petit que le fichier SFT complet serait destiné à la nouvelle version de l’application et réduit l’impact de la mise à jour des mises à jour de package sur une connexion réseau à faible bande passante. Toutefois, son utilisation est uniquement prise en charge dans certaines situations restreintes. Cette fonctionnalité était conçue pour une utilisation spécifique lorsque vous utilisez un système de distribution de logiciels électroniques pour gérer un groupe d’utilisateurs à l’aide d’un serveur de fichiers local par le biais d’une connexion à faible bande passante et que vous n’utilisez pas les serveurs de streaming App-V.

Vous n’avez pas besoin d’utiliser le fichier SFT différentielle si vous utilisez la configuration Manager2007 pour gérer les utilisateurs, car Configuration Manager prend en charge les déploiements à faible bande passante déjà intégrés. Ce n’est pas non plus obligatoire si vous utilisez la gestion des applications (App-V) ou les serveurs de streaming avec la mise à niveau active, car le client récupère uniquement les différences entre les anciennes et les nouvelles versions de package.

La procédure suivante vous explique comment utiliser la mkdiffpkg.exe incluse dans l’installation de Sequencer pour créer le fichier SFT différentielle, après avoir effectué la mise à niveau du package d’application virtuelle et déployé le fichier SFT différentielle. Cette procédure permet de s’assurer que si le package est d’une grande utilisation de l’ordinateur client, lors de la prochaine tentative d’exécution de l’application par l’utilisateur, le client revient à l’URL de remplacement, qui est définie pour diffuser en continu la version complète du package v2. SFT du partage de fichiers local. Cela évite tout échec de l’utilisateur au démarrage de l’application. Si le client entier est endommagé ou a été désinstallé, il est recommandé de configurer le système ESD pour déployer la version complète du package mis à niveau, v2. SFT, sur le client.

Pour plus d’informations sur la mise à niveau d’un package, voir la section «Comment mettre à niveau une application virtuelle existante» dans le guide des opérations App-V 4.5 à <https://go.microsoft.com/fwlink/?LinkId=133129>

**Remarques**  Le cas échéant, tous les ordinateurs utilisateur ciblés par la fonction ESD doivent disposer du fichier v1. SFT dans leur cache local, et le flux de fichiers doit être activé sur tous les ordinateurs.

 

**Pour utiliser le fichier SFT différentielle**

1.  Connectez-vous à l’ordinateur Sequencer à l’aide d’un compte disposant de droits d’administrateur. Ouvrez le package d’origine (v1) pour la mise à niveau dans le Sequencer, puis mettez à niveau le package vers la nouvelle version (v2) et enregistrez-le en tant que nouveau v2. sft.

2.  Ouvrez une fenêtre de commande dans le dossier d’installation du Sequencer App-V 4.5, puis exécutez la commande suivante:

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  À l’aide du système ESD ou d’un autre processus de copie de fichiers, copiez le fichier de contenu de package V2 complet, v2. SFT, sur un partage de fichiers local accessible aux ordinateurs des utilisateurs sur une connexion réseau bien connectée.

4.  À l’aide du système ESD, placez une copie du fichier SFT différentielle, v2. dsft, sur chaque ordinateur d’utilisateur.

5.  Pour importer le fichier v2. dsft, exécutez la commande SFTMIME suivante sur les ordinateurs des utilisateurs:

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  Exécutez la commande SFTMIME suivante sur les ordinateurs des utilisateurs pour définir l’URL de remplacement de telle sorte qu’elle pointe vers le fichier v2. sft:

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**Remarque**  
-   Les fichiers SFT différentielle doivent être appliqués aux clients dans l’ordre approprié. Par exemple, la version v2. dsft doit être appliquée à une application v1 avant la version v3. dsft est appliquée.

-   La fonctionnalité **générer le package Microsoft Windows Installer (MSI)** du Sequencer ne peut pas être utilisée avec le fichier SFT différentielle.

 

## Rubriques connexes


[Comment créer ou mettre à niveau des applications virtuelles à l’aide du Sequencer App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 






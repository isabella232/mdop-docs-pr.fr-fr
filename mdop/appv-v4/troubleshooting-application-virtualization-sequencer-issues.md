---
title: Résolution des problèmes liés à Application Virtualization Sequencer
description: Résolution des problèmes liés à Application Virtualization Sequencer
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806229"
---
# Résolution des problèmes liés à Application Virtualization Sequencer


Cette rubrique contient des informations que vous pouvez utiliser pour résoudre les problèmes d’ordre général sur le Sequencer Application Virtualization (App-V).

## La création d’un fichier SFTD à l’aide du Sequencer App-V augmente le numéro de version de manière inattendue


Utilisez la ligne de commande pour générer un nouveau fichier. sft. Pour créer le fichier. SFT à l’aide de la ligne de commande, entrez ce qui suit à l’invite de commandes:

**mkdiffpkg.exe &lt; nom de fichier SFT de base &gt; &lt;&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>Le nom de fichier du fichier OSD n’est pas correct après la mise à niveau du package


Lorsque vous ouvrez un package pour la mise à niveau, vous devez spécifier le lecteur Q:\\ racine en tant qu’emplacement de sortie du package. Ne spécifiez pas un nom de fichier associé avec l’emplacement de sortie.

## L’installation par défaut de Microsoft Word2003 génère une erreur lors d’un flux vers un client


Lorsque vous diffusez en continu Microsoft Word2003 sur un client, une erreur est retournée, mais Microsoft Word continue de s’exécuter.

**Solution**

Reséquencez le package d’application virtuel et sélectionnez **installation complète**.

## La mise à niveau active ne fonctionne pas lors de la création d’un package dépendant


Lorsque vous créez un package dépendant en utilisant la mise à niveau active et en ajoutant de nouvelles entrées de Registre, ce dernier semble fonctionner correctement, mais les entrées de Registre mises à jour ne sont pas disponibles.

**Solution**

Les paramètres de Registre étant toujours stockés avec la version d’origine du package, les mises à jour apportées au package ne semblent pas être disponibles sauf si vous réparez le package d’origine.

## Les informations détaillées ne sont pas visibles pour les documents Microsoft Office2007 à l’aide de la page de propriétés


Lorsque vous essayez d’afficher des informations détaillées associées à un document Microsoft Office2007 à l’aide de la page de propriétés, les informations détaillées ne sont pas visibles.

**Solution**

App-V ne prend pas en charge les extensions d’environnement requises pour ces pages de propriétés.

## Certaines clés de registre ne sont pas capturées lors de la séquence des applications 16 bits


Dans App-V 4,5, le raccordement du registre a été déplacé du mode noyau au mode utilisateur. Si vous souhaitez séquencer une application 16 bits ou une application qui utilise un programme d’installation 16 bits, vous devez commencer par configurer l’ordinateur Sequencer de manière à ce que le processus s’exécute dans sa propre copie de la machine DOS virtuelle Windows NT (NTVDM).

**Solution**

Avant de séquencer l’application, définissez la valeur de clé de Registre REGSZ globale suivante sur «Yes» sur l’ordinateur de séquençage:

HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM

Vous devez redémarrer votre ordinateur pour que cette action soit prise en compte.

## Rubriques connexes


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 






---
title: Résolution des problèmes liés à Application Virtualization Sequencer
description: Résolution des problèmes liés à Application Virtualization Sequencer
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806205"
---
# Résolution des problèmes liés à Application Virtualization Sequencer


Cette rubrique contient des informations que vous pouvez utiliser pour résoudre les problèmes d’ordre général sur le Sequencer Application Virtualization (App-V).

## La création d’un fichier SFTD à l’aide du Sequencer App-V augmente le numéro de version de manière inattendue


Le numéro de version associé à un fichier SFTD augmente de manière inattendue.

**Solution**

Utilisez la ligne de commande pour générer un nouveau fichier. sft. Pour créer le fichier. SFT à l’aide de la ligne de commande, entrez ce qui suit à l’invite de commandes:

**mkdiffpkg.exe &lt; nom de fichier SFT de base &gt; &lt;&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>Le nom de fichier du fichier OSD n’est pas correct après la mise à niveau du package


Après avoir effectué la mise à niveau d’un package existant, le nom du fichier n’est pas correct.

**Solution**

Lorsque vous ouvrez un package pour la mise à niveau, vous devez spécifier le lecteur Q:\\ racine en tant qu’emplacement de sortie du package. Ne spécifiez pas un nom de fichier associé avec l’emplacement de sortie.

## L’installation par défaut de Microsoft Word2003 génère une erreur lors d’un flux vers un client


Lorsque vous diffusez en continu Microsoft Word2003 sur un client, une erreur est retournée, mais Microsoft Word continue de s’exécuter.

**Solution**

Reséquencez le package d’application virtuel, puis sélectionnez **installation complète**.

## La mise à niveau du package ne fonctionne pas lorsque vous créez un package dépendant


Lorsque vous créez un package dépendant en utilisant la mise à niveau du package et en ajoutant de nouvelles entrées de Registre, il semble fonctionner correctement, mais les entrées de Registre mises à jour ne sont pas disponibles.

**Solution**

Les paramètres de Registre étant toujours stockés avec la version d’origine du package, les mises à jour apportées au package ne semblent pas être disponibles sauf si vous réparez le package d’origine.

## Erreur lors de la tentative de séquence. .NET 2.0


Lorsque vous séquencez un package qui nécessite. .NET 2.0 vous obtenez un message d’erreur.

**Solution**

Séquençage des packages qui nécessitent. NET 2.0 n’est pas pris en charge.

## Rubriques connexes


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 






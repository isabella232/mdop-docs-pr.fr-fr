---
title: Notes de publication pour DaRT8.0SP1
description: Notes de publication pour DaRT8.0SP1
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810757"
---
# Notes de publication pour DaRT8.0SP1


**Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.**

Lisez attentivement ces notes de publication avant de procéder à l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 Service Pack 1 (SP1).

Ces notes de publication contiennent des informations requises pour installer correctement les outils de diagnostics et de récupération d’outils de récupération 8,0 SP1. Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents DaRT, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## À propos de la documentation relative aux produits


Pour plus d’informations sur la documentation pour DaRT, consultez la [page d’accueil de DART](https://go.microsoft.com/fwlink/?LinkID=252096) sur Microsoft TechNet.

## Problèmes connus avec DaRT 8,0 SP1


### La restauration du système échoue lorsque vous exécutez Locksmith ou l’éditeur du Registre

Si vous exécutez Locksmith, l’éditeur du Registre et éventuellement d’autres outils, la restauration du système échoue.

**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez la restauration du système.

### L’analyse SFC ne peut pas s’exécuter lorsque vous démarrez et fermez Locksmith ou la gestion de l’ordinateur

Si vous démarrez, puis fermez l’Locksmith ou les outils de gestion de l’ordinateur, le vérificateur de fichiers système ne s’exécute pas.

**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez SFC.

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> Le programme d’installation de DaRT ne fonctionne pas lorsque ADK n’a pas été installé

Si vous installez DaRT 8,0 SP1 à l’aide de la ligne de commande pour exécuter le MSI et que le ADK n’a pas été installé, l’installation de DaRT échoue. Pour l’instant, le programme d’installation de DaRT 8,0 SP1 installe tous les composants, à l’exception de l’image de récupération DaRT.

**Solution de contournement:** Néant.

### Le système Defender ne peut pas être lancé après le lancement de Locksmith, de l’analyseur de blocage et de la gestion de l’ordinateur

Le logiciel Defender ne se lance pas si vous avez déjà lancé Locksmith, RegEdit, analyse de blocage et gestion de l’ordinateur.

**Solution de contournement:** Fermez et redémarrez DaRT, puis lancez Defender.

### Le démarrage de Defender est ralenti

Le lancement de Defender peut prendre quelques minutes. La barre de progression indique l’état de chargement actuel.

**Solution de contournement:** Néant.

## Informations de copyright des notes de publication


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft. Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.



## Rubriques connexes


[À propos de DaRT8.0SP1](about-dart-80-sp1.md)

 

 






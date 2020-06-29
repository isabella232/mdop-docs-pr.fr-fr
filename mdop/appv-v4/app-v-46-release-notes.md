---
title: Notes de publication d'App-V4.6
description: Notes de publication d'App-V4.6
author: dansimp
ms.assetid: a3eba129-edac-48bf-a933-3bf43a9873e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9eee3c309a927a72155dec707d8dd95f43e90fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809312"
---
# Notes de publication d'App-V4.6


Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.

**Important**  Lisez attentivement ces notes de publication avant d’installer le système de gestion Microsoft Application Virtualization (App-V). Ces notes de publication contiennent des informations dont vous avez besoin pour installer correctement la virtualisation des applications (App-V) 4.6. Ce document contient des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents App-V, la dernière modification doit être considérée comme faisant autorité.

 

## Se protéger contre les failles de sécurité et les virus


Pour vous aider à vous protéger contre les failles de sécurité et les virus, il est important d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé. Pour plus d’informations, consultez le [site Web de Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problèmes connus liés à la virtualisation des applications 4.6


Cette section fournit les informations les plus récentes sur les problèmes liés à Microsoft Application Virtualization (App-V) 4.6. Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire. Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures.

### Erreur de chargement/installation lors de l’exécution d’un fichier Windows Installer généré par le Sequencer App-V 4.5

L’exécution d’un fichier d’installation Windows généré par le Sequencer App-V 4.5 génère une erreur de chargement/installation lors de la tentative d’exécution sur un client App-V 4,6. Le message suivant s’affiche: «ce package nécessite le client Microsoft Application Virtualization 4.5 ou version ultérieure». Vous pouvez utiliser la solution de contournement suivante.

WORKAROUNDOpen l’ancien package avec le Sequencer App-V 4,5 SP1 ou le Sequencer App-V 4,6 et générer un nouveau fichier. msi pour le package.

**Remarques**  Par ailleurs, à l’invite de commandes, le Sequencer App-V peut générer le nouveau fichier. msi en utilisant les paramètres */Open* et */MSI* , par exemple, `SFTSequencer /Open:”package.sprj” /MSI` . Pour plus d’informations, reportez-vous [à la rubrique mise à niveau d’une application virtuelle à l’aide de la ligne de commande](how-to-upgrade-a-virtual-application-by-using-the-command-line.md).

 

### Informations de copyright des notes de publication

Ce document est fourni «en l’absence». Les informations contenues dans ce document, y compris les URL et autres références de sites Web, pourront faire l’objet de modifications sans préavis. Vous assumez le risque d’utilisation.

Quelques exemples présentés dans les présentes sont fournis à titre indicatif uniquement et sont fictifs.Aucune association ou connexion réelle ne doit être intentionnelle ou intentionnelle.

Ce document ne vous fournit aucun droit légal de propriété intellectuelle de tout produit Microsoft. Vous pouvez copier le présent document pour une utilisation interne à des fins de référence. Vous pouvez modifier ce document à des fins de référence interne.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server et Windows Vista sont des marques commerciales du groupe Microsoft de sociétés.

Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.

 

 






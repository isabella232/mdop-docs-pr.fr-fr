---
title: Notes de publication d'App-V4.6 SP3
description: Notes de publication d'App-V4.6 SP3
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808049"
---
# Notes de publication d'App-V4.6 SP3


Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.

Lisez attentivement ces notes de publication avant d’installer le système de gestion Microsoft Application Virtualization (App-V). Ces notes de publication contiennent des informations qui vous permettent d’installer correctement Application Virtualization (App-V) 4.6 SP3. Ce document contient des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents App-V, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## Se protéger contre les failles de sécurité et les virus


Pour vous aider à vous protéger contre les failles de sécurité et les virus, il est important d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé. Pour plus d’informations, consultez le [site Web de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) sur la sécurité ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problèmes connus liés à la virtualisation des applications 4.6 SP3


Cette section fournit les informations les plus récentes sur les problèmes liés à Microsoft Application Virtualization (App-V) 4.6 SP3. Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire. Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures.

### Impossible d’ouvrir des liens hypertexte à l’aide d’Internet Explorer11 sur Microsoft Windows 8,1 au sein de l’environnement virtuel

Toute tentative d’ouverture des liens hypertexte à partir d’un environnement virtuel échoue sur Windows 8,1 à l’aide d’Internet Explorer 11. En effet, Internet Explorer 11 est désormais fourni avec le mode de protection améliorée (EPM) activé par défaut, et l’application-V ne peut pas accéder aux clés de Registre, aux fichiers et aux objets de port de communication requis.

Solution de contournement: désactivez EPM dans Internet Explorer11 avant d’ouvrir un package App-V. Cela vous permettra d’ouvrir Internet Explorer à partir de l’environnement virtuel.

## Rubriques connexes


[À propos de Microsoft Application Virtualization4.6 SP3](about-microsoft-application-virtualization-46-sp3.md)

 

 






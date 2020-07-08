---
title: Interopérabilité d'App-V et de Windows AppLocker
description: Interopérabilité d'App-V et de Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809281"
---
# Interopérabilité d'App-V et de Windows AppLocker


La version 4,5 SP1 du client Microsoft Application Virtualization (App-V) prend en charge la fonctionnalité AppLocker de Windows 7. La fonctionnalité AppLocker permet aux administrateurs informatiques de spécifier les applications qui ne sont pas exécutées sur un ordinateur. Ce document décrit comment configurer les règles AppLocker pour fonctionner avec l’environnement virtuel App-V et les applications virtualisées.

**Remarques**  Windows AppLocker doit d’abord être activé avant de configurer des règles Windows AppLocker pour les applications virtuelles. Pour plus d’informations sur l’activation de Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .

 

## Configuration de règles Windows AppLocker pour les applications virtuelles


Les administrateurs locaux peuvent créer des règles AppLocker Windows qui limitent l’exécution de fichiers exécutables de programme (fichiers. exe), de fichiers Windows Installer (fichiers. msi et. msp) et de scripts (. PS,. bat,. cmd,. vbs et. js). L’administrateur effectue cette opération à l’aide d’un ordinateur de référence sur lequel est installé le client App-V et qui a toutes les applications virtuelles pertinentes transmises au cache client. L’administrateur utilise ensuite la section Windows AppLocker de la stratégie de sécurité locale du composant logiciel enfichable Microsoft Management Console (MMC) sur l’ordinateur de référence pour créer des règles.

Lorsque vous naviguez vers le chemin d’accès d’un répertoire ou un fichier spécifique pour lequel vous voulez créer une règle, vous pouvez accéder au lecteur App-V en utilisant son chemin d’accès. Par exemple, vous pouvez accéder à \\\\localhost\\Q $, où le lecteur App-V est Drive Q. Toutefois, pour créer la règle, vous devez modifier le chemin d’accès pour supprimer la référence à \\\\localhost\\Q $ et utiliser Q:\\ à la place. Pour accéder aux fichiers de l’application, vous devez démarrer chaque application sur l’ordinateur de référence, et les droits d’administration sont requis pour accéder à \\\\localhost\\Q $.

 

 






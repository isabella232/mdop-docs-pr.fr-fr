---
title: Codes des erreurs de ligne de commande de Sequencer
description: Codes des erreurs de ligne de commande de Sequencer
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806354"
---
# Codes des erreurs de ligne de commande de Sequencer


Utilisez la liste suivante pour vous aider à identifier les erreurs liées au séquençage des applications à l’aide de la ligne de commande. Vous pouvez également consulter ces informations en consultant le fichier journal App-V du Sequencer associé.

**Remarques**  Plusieurs erreurs peuvent se produire durant le séquençage et, si tel est le cas, le code d’erreur affiché peut être la somme de deux codes d’erreur. Par exemple, si les paramètres */InstallPath* et */outputfile* sont manquants, le Sequencer App-V renverra **96**, c’est-à-dire la somme des deux codes d’erreur.

 

<a href="" id="01"></a>nommée  
Il n’y a pas eu d’erreur non spécifiée.

<a href="" id="02"></a>Arrêtés  
Le répertoire d’installation spécifié (/INSTALLPACKAGE) n’est pas valide.

<a href="" id="04"></a>04  
Le répertoire racine du package spécifié (/INSTALLPATH) n’est pas valide.

<a href="" id="08"></a>0,08  
Le paramètre */outputfile* spécifié n’est pas valide.

<a href="" id="16"></a>Seiz  
Le répertoire d’installation (/INSTALLPACKAGE) n’est pas spécifié.

<a href="" id="32"></a>32  
Le répertoire racine du package (/INSTALLPATH) n’est pas spécifié.

<a href="" id="64"></a>64  
Le paramètre */outputfile* n’est pas spécifié.

<a href="" id="128"></a>128  
Le lecteur de virtualisation des applications spécifié n’est pas valide.

<a href="" id="256"></a>256  
Le programme d’installation a échoué.

<a href="" id="512"></a>512  
Le séquençage de l’application a échoué.

<a href="" id="1024"></a>1024  
Échec de l’évaluation des raccourcis installés.

<a href="" id="2048"></a>2048  
Le package d’application séquencé ne peut pas être enregistré.

<a href="" id="4096"></a>4096  
Le nom du package spécifié (/PACKAGENAME) n’est pas valide.

<a href="" id="8192"></a>8192  
La taille de bloc spécifiée (/BLOCKSIZE) n’est pas valide.

<a href="" id="16384"></a>16384  
Le type de compression spécifié (/COMPRESSION) n’est pas valide.

<a href="" id="32768"></a>32768  
Le chemin de projet spécifié n’est pas valide.

<a href="" id="65536"></a>65536  
Le paramètre de mise à niveau spécifié n’est pas valide.

<a href="" id="131072"></a>131072  
Le paramètre de Project de mise à niveau spécifié n’est pas valide.

<a href="" id="262144"></a>262144  
Le paramètre de chemin d’accès de décodage spécifié n’est pas valide.

<a href="" id="525288"></a>525288  
Le nom du package n’est pas spécifié.

## Rubriques connexes


[Référence d'Application Virtualization Sequencer](application-virtualization-sequencer-reference.md)

[Paramètres de ligne de commande de Sequencer](sequencer-command-line-parameters.md)

 

 






---
title: Procédure pour gérer le cache d'App-V Client à l'aide des compteurs de performances
description: Procédure pour gérer le cache d'App-V Client à l'aide des compteurs de performances
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806985"
---
# Procédure pour gérer le cache d'App-V Client à l'aide des compteurs de performances


Vous pouvez suivre la procédure ci-dessous pour déterminer la quantité d’espace libre disponible dans le cache du client de virtualisation des applications (App-V) en utilisant l’outil Performance Monitor pour afficher les informations sous forme graphique. Ces informations sont capturées sur l’ordinateur client par le biais d’un compteur de performance appelé «App Virt Client cache», qui inclut les compteurs suivants: «taille du cache (Mo)», «mettre en cache l’espace disponible (Mo)» et «% Free Space».

**Pour déterminer l’utilisation de l’espace cache du client**

1.  Ouvrez une invite de commandes en tant qu’administrateur ou cliquez sur **Démarrer**, **exécuter**, tapez **perfmon.exe**, puis cliquez sur **OK**.

2.  En fonction du système d’exploitation Windows utilisé, cliquez sur l’outil Moniteur de performance ou moniteur système après l’ouverture de la fenêtre MMC.

3.  Pour ajouter des compteurs, cliquez avec le bouton droit sur la zone du graphique, puis sélectionnez **Ajouter des compteurs**.

4.  Cliquez sur la liste déroulante pour afficher la liste des compteurs disponibles, faites défiler pour trouver l' **application Virt du cache du client**, puis ajoutez les trois compteurs.

    **Important**  Les compteurs de performance App-V sont implémentés dans une DLL 32 bits, de sorte que pour les voir, vous devez utiliser la commande suivante pour démarrer la version 32 bits de performance Monitor: **MMC/32 Perfmon. msc**. Cette commande doit être exécutée directement sur l’ordinateur surveillé et ne peut pas être utilisée pour surveiller un ordinateur distant exécutant un système d’exploitation 64 bits.

     

## Rubriques connexes


[Procédure pour gérer toutes les applications virtuelles à l'aide de la ligne de commande](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 






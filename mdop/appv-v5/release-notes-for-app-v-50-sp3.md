---
title: Notes de publication pour App-V5.0 SP3
description: Notes de publication pour App-V5.0 SP3
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804891"
---
# Notes de publication pour App-V5.0 SP3


Vous trouverez ci-après des problèmes connus dans Microsoft Application Virtualization (App-V) 5,0 SP3.

## Les fichiers du serveur ne peuvent pas être supprimés après l’installation d’une nouvelle application-V 5,0 SP3


Si vous désinstallez le serveur App-V 5,0 SP1, puis installez le serveur App-V 5,0 SP3, l’installation échoue et la mauvaise version du serveur de gestion est installée. Les erreurs suivantes sont affichées:

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

Le problème se produit parce que les fichiers serveur ne sont pas supprimés lorsque vous désinstallez App-V 5,0 SP1, de sorte que le processus d’installation de l’application-V 5,0 SP3 effectue une mise à niveau au lieu d’une nouvelle installation.

**Solution**: supprimez la clé de Registre suivante avant de commencer à installer App-V 5,0 SP3:

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## L’interrogation d’AD DS peut entraîner le fonctionnement incorrect de certaines applications


Lorsque vous recevez des packages mis à jour en interrogeant les services de domaine Active Directory (AD FS) pour des appartenances aux groupes mises à jour, cela peut entraîner le fonctionnement incorrect de certaines applications si celles-ci dépendent du jeton d’accès de l’utilisateur. De plus, les requêtes d’appartenance au groupe fréquentes peuvent entraîner la surcharge du contrôleur de domaine. Pour plus d’informations sur les jetons d’accès utilisateur, voir [jetons d’accès](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).

**Solution de contournement**: patientez jusqu’à ce que l’utilisateur se déconnecte, puis reconnectez-vous avant de rechercher des appartenances aux groupes mises à jour. N’utilisez pas la clé de Registre décrite dans l' [application Hotfix package 2 de Microsoft application virtualization 5,0 Service Pack 1](https://support.microsoft.com/kb/2897087)pour rechercher des appartenances aux groupes mises à jour.






## Rubriques connexes


[À propos d'App-V5.0 SP3](about-app-v-50-sp3.md)

 

 






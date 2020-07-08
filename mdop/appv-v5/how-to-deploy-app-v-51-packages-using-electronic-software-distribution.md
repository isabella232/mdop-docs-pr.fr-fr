---
title: Déploiement de packages App-V5.1 à l'aide d'une solution de distribution électronique de logiciels
description: Déploiement de packages App-V5.1 à l'aide d'une solution de distribution électronique de logiciels
author: dansimp
ms.assetid: e1957a5a-1f18-42da-b2c1-a5ae5a4cca7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a9ed5fbb264f8fb9676d7fa18fe4de8019ea8e79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805538"
---
# Déploiement de packages App-V5.1 à l'aide d'une solution de distribution électronique de logiciels


Vous pouvez utiliser un système de distribution de logiciels électronique (ESD) pour déployer des applications virtuelles App-V 5,1 pour les clients App-V. Pour plus d’informations, consultez la documentation disponible avec la fonction ESD que vous utilisez.

Pour connaître la configuration requise et les options d’utilisation d’une application ESD pour déployer des packages App-V, voir [planification du déploiement de App-v 5,1 avec un système de distribution de logiciels électronique](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).

Appliquez l’une des méthodes suivantes pour publier des packages sur les ordinateurs clients App-V avec une application ESD:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Fonctionnalités fournies par un tiers ESD</p></td>
<td align="left"><p>Utilisez les fonctionnalités d’un fournisseur de ESD tiers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Programme d’installation Windows autonome</p></td>
<td align="left"><p>Installez l’application sur l’ordinateur client cible à l’aide du fichier Windows Installer (. msi) associé qui est créé lors de la séquence initiale d’une application. Le fichier d’installation Windows contient les informations du fichier de package App-V 5,1 utilisées pour configurer un package et copie les fichiers de package requis sur le client.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Utilisez les cmdlets PowerShell pour déployer des applications virtualisées. Pour plus d’informations sur l’utilisation des applications PowerShell et App-V 5,1, voir <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)"> administration d’App-v 5,1 à l’aide de PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

 

**Pour déployer des packages App-V 5,1 en utilisant une ESD**

1.  Installez le Sequencer App-V 5,1 sur un ordinateur de votre environnement. Pour plus d’informations sur l’installation de Sequencer, voir [Comment installer le Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).

2.  Utilisez le Sequencer App-V 5,1 pour créer une application virtuelle. Pour plus d’informations sur la création d’une application virtuelle, voir [création et gestion des applications virtuelles App-V 5,1](creating-and-managing-app-v-51-virtualized-applications.md).

3.  Une fois que vous avez créé l’application virtuelle, déployez le package à l’aide de votre solution ESD.

    Pour plus d’informations sur l’utilisation de System Center Configuration Manager, voir présentation de la [gestion des applications dans Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) pour plus d’informations sur l’utilisation d’App-V 5,1 et de System Center2012 Configuration Manager.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)

 

 






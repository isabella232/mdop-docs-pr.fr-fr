---
title: Déploiement du client MBAM àl'aide d'une ligne de commande
description: Déploiement du client MBAM àl'aide d'une ligne de commande
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810584"
---
# Déploiement du client MBAM àl'aide d'une ligne de commande


Vous pouvez utiliser une ligne de commande pour déployer le logiciel client Microsoft BitLocker Administration and Analysis (MBAM).

## Ligne de commande pour déployer le logiciel client MBAM


Tapez la commande suivante à l’invite de commandes pour accepter automatiquement le contrat de licence utilisateur final lors du déploiement du logiciel client MBAM.

**MBAMClientSetup.exe/acceptEula = Oui**

**Remarques**  Les options de la ligne de commande **/Ju** et **/JM** ne sont pas prises en charge et ne peuvent pas être utilisées pour installer le logiciel client MBAM.

 

Tapez la commande suivante à l’invite de commandes pour extraire et installer le MSP:

**MBAMClientSetup.exe le &lt; chemin d’accès/Extract pour extraire MSI &gt; /AcceptEULA = Yes**

Ensuite, installez la version MSI silencieusement en exécutant la commande suivante:

**msiexec/i &lt; path pour extraire le MSI &gt; /qb = 1 redémarrage = ReallySuppress**

**Remarques**  À partir de MBAM 2,5 SP1, un MSI distinct n’est plus inclus dans le produit MBAM. Toutefois, vous pouvez extraire le MSI du fichier exécutable (. exe) qui est inclus dans le produit, après avoir accepté le CLUF.

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a>OPTIN \ _FOR \ _MICROSOFT \ _UPDATES = 1 option de ligne de commande


Si vous le souhaitez, vous pouvez spécifier l’option de ligne de commande `OPTIN_FOR_MICROSOFT_UPDATES=1` lors de l’installation du logiciel client pour installer automatiquement les mises à jour de Microsoft sur les ordinateurs clients. Cette option permet à Microsoft Update de démarrer automatiquement et de rechercher les mises à jour disponibles à installer après la fin de l’installation du logiciel client.

Vous pouvez utiliser cette option de ligne de commande avec l’une des méthodes d’installation suivantes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Installez le logiciel client MBAM à l’aide de</th>
<th align="left">Exemple</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>MBAMClientSetup.exe</strong></p></td>
<td align="left"><p><strong>MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>msiexec/i MBAMClient.msi</strong></p></td>
<td align="left"><p><strong>msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
</tbody>
</table>

 


## Rubriques connexes


[Déploiement du client MBAM2.5](deploying-the-mbam-25-client.md)

 

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).





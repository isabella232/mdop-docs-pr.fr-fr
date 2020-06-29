---
title: Utilisation de Windows PowerShell pour administrer MBAM2.5
description: Utilisation de Windows PowerShell pour administrer MBAM2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804452"
---
# Utilisation de Windows PowerShell pour administrer MBAM2.5


Cette rubrique décrit les applets de contrôle Windows PowerShell pour le contrôle de l’administration et de la surveillance de Microsoft BitLocker (MBAM) qui concernent la récupération d’ordinateurs ou de lecteurs lorsque les utilisateurs sont verrouillés.

Pour les applets de fonction qui vous permettent de configurer les fonctionnalités du serveur MBAM, voir [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a>Cmdlets permettant de récupérer des ordinateurs ou des lecteurs gérés par MBAM


Utilisez les applets de commande Windows PowerShell suivantes pour récupérer des ordinateurs ou des lecteurs gérés par MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Demande une clé de récupération MBAM qui permet aux utilisateurs de déverrouiller un ordinateur ou un lecteur chiffré.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Fournit aux utilisateurs un mot de passe de propriétaire de TPM qu’ils peuvent utiliser pour déverrouiller un module de plateforme sécurisée (TPM) lorsque le TPM les a verrouillés et ne acceptera plus son code confidentiel.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> Aide de l’applet de MBAM


L’aide de Windows PowerShell pour les applets de commande MBAM est disponible dans les formats suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Format d’aide de Windows PowerShell</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>À l’invite de commandes Windows PowerShell, tapez <strong> get- </strong> &lt; <em> cmdlet cmdlet.</em>&gt;</p></td>
<td align="left"><p>Pour télécharger les dernières applets de cmdlet Windows PowerShell, suivez les instructions de <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell.</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Sur TechNet en tant que pages Web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dans le centre de téléchargement en tant que fichier Word. docx</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Dans le centre de téléchargement sous forme de fichier. pdf</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## Rubriques connexes


[Administration des composants de MBAM2.5](administering-mbam-25-features.md)

[Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 






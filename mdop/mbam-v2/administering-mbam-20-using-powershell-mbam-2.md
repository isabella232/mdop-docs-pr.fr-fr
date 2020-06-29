---
title: Administration de MBAM2.0 à l'aide de PowerShell
description: Administration de MBAM2.0 à l'aide de PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809995"
---
# Administration de MBAM2.0 à l'aide de PowerShell


La surveillance et l’administration de BitLocker Microsoft (MBAM) fournissent l’ensemble d’applets de commande Windows PowerShell suivant. Les administrateurs peuvent utiliser les applets de commande PowerShell suivants pour effectuer diverses tâches d’administration et de surveillance du serveur Microsoft BitLocker à partir de la ligne de commande plutôt que sur le site Web d’administration MBAM.

## Administration de MBAM à l’aide de PowerShell


Utilisez les applets de commande PowerShell décrites ici pour administrer MBAM.

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
<td align="left"><p>Installation-MBAM</p></td>
<td align="left"><p>Installe les fonctionnalités MBAM qui fournissent une stratégie avancée, le chiffrement, la récupération de clés et le rapport de conformité.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Désinstaller-MBAM</p></td>
<td align="left"><p>Supprime les fonctionnalités MBAM qui fournissent une stratégie avancée, le chiffrement, la récupération de clés et les outils de création de rapports de conformité.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Demande une clé de récupération MBAM qui permettra aux utilisateurs de déverrouiller un ordinateur ou un lecteur chiffré.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Fournit aux utilisateurs un mot de passe de propriétaire de TPM qu’ils peuvent utiliser pour déverrouiller un module de plateforme sécurisée (TPM) lorsque le TPM les a verrouillés et ne acceptera plus son code confidentiel.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Opérations de MBAM2.0](operations-for-mbam-20-mbam-2.md)

 

 






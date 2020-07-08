---
title: Administration de MBAM1.0 à l'aide de PowerShell
description: Administration de MBAM1.0 à l'aide de PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810974"
---
# Administration de MBAM1.0 à l'aide de PowerShell


La surveillance et l’administration de BitLocker Microsoft (MBAM) fournissent l’ensemble d’applets de commande Windows PowerShell suivant. Les administrateurs peuvent utiliser les applets de commande PowerShell suivants pour effectuer diverses tâches serveur MBAM à partir de l’invite de commandes plutôt que du site Web d’administration MBAM.

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
<td align="left"><p>Add-MbamHardwareType</p></td>
<td align="left"><p>Ajoute un nouveau modèle matérielle à l’inventaire matériel MBAM. Cette applet de commande peut également indiquer si le matériel est pris en charge ou n’est pas pris en charge pour le chiffrement de lecteur BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Demande une clé de récupération MBAM qui permettra à un utilisateur de déverrouiller un ordinateur ou un lecteur chiffré.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamHardwareType</p></td>
<td align="left"><p>Obtient un inventaire matériel principal qui contient des données indiquant si les modèles matériels sont compatibles ou incompatibles avec le chiffrement de lecteur BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Fournit un mot de passe de propriétaire de TPM à un utilisateur pour gérer son accès au module de plateforme sécurisée (TPM). Aide les utilisateurs lorsque le TPM les a verrouillés et n’accepte plus son code confidentiel.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installation-MBAM</p></td>
<td align="left"><p>Installe des fonctionnalités MBAM qui fournissent des outils avancés de stratégie de groupe, de chiffrement, de récupération de clés et de création de rapports de conformité.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Remove-MbamHardwareType</p></td>
<td align="left"><p>Supprime les modèles matériels de l’inventaire matériel.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Set-MbamHardwareType</p></td>
<td align="left"><p>Permet la gestion d’un inventaire principal du matériel pour indiquer si les modèles matériels sont compatibles ou ne peuvent pas effectuer le chiffrement BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Désinstaller-MBAM</p></td>
<td align="left"><p>Supprime les fonctionnalités MBAM déjà installées qui fournissent des outils avancés de stratégie, de chiffrement, de récupération de clés et de création de rapports de conformité.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Opérations de MBAM1.0](operations-for-mbam-10.md)

 

 






---
title: Déterminer pourquoi un appareil reçoit un message de non-conformité
description: Déterminer pourquoi un appareil reçoit un message de non-conformité
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810637"
---
# Déterminer pourquoi un appareil reçoit un message de non-conformité


Les codes de non-conformité suivants sont fournis par WMI et décrivent les raisons pour lesquelles un appareil particulier est signalé par MBAM comme non conforme.

Vous pouvez utiliser votre méthode préférée pour afficher WMI. Si vous utilisez PowerShell, exécutez `gwmi -class mbam_volume -Namespace root\microsoft\mbam` à partir d’une invite PowerShell et recherchez ReasonsForNoncompliance.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Code de non-conformité</th>
<th align="left">Raison de l’absence de conformité</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>0,4</p></td>
<td align="left"><p>Niveau de cryptage non AES 256.</p></td>
</tr>
<tr class="even">
<td align="left"><p>1</p></td>
<td align="left"><p>La stratégie MBAM nécessite que ce volume soit crypté, mais pas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>deuxième</p></td>
<td align="left"><p>La stratégie MBAM nécessite ce volume pour qu’elle soit chiffrée, mais elle est.</p></td>
</tr>
<tr class="even">
<td align="left"><p>3D</p></td>
<td align="left"><p>La stratégie MBAM nécessite ce volume utilise un protecteur de module de plateforme sécurisée, mais ce n’est pas le cas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>n°4</p></td>
<td align="left"><p>Pour utiliser une stratégie de MBAM, le volume doit utiliser un protecteur de plateforme sécurisée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>n°5</p></td>
<td align="left"><p>La stratégie MBAM ne permet pas à un ordinateur de TPM de signaler comme compatible.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>6</p></td>
<td align="left"><p>Le volume possède un protecteur de TPM, mais le TPM n’est pas visible (amorcé avec la clé de récupération après la désactivation du TPM dans le BIOS?).</p></td>
</tr>
<tr class="even">
<td align="left"><p>6</p></td>
<td align="left"><p>La stratégie MBAM nécessite que ce volume utilise un protecteur de mot de passe, mais qu’il n’en possède pas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>version8</p></td>
<td align="left"><p>La stratégie MBAM nécessite que ce volume n’utilise pas un protecteur de mot de passe, mais qu’il en possède un.</p></td>
</tr>
<tr class="even">
<td align="left"><p>09</p></td>
<td align="left"><p>La stratégie MBAM nécessite que ce volume utilise un protecteur de déverrouillage automatique, mais qu’il n’en possède pas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>0,10</p></td>
<td align="left"><p>La stratégie MBAM nécessite que ce volume n’utilise pas de protecteur de déverrouillage automatique, mais il en possède un.</p></td>
</tr>
<tr class="even">
<td align="left"><p>27,9</p></td>
<td align="left"><p>Conflit de stratégie détecté qui empêche MBAM de signaler ce volume comme compatible.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>midi</p></td>
<td align="left"><p>Un volume système est requis pour chiffrer le volume du système d’exploitation, mais il n’est pas disponible.</p></td>
</tr>
<tr class="even">
<td align="left"><p>n°13</p></td>
<td align="left"><p>La protection est suspendue pour le volume.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>13</p></td>
<td align="left"><p>Déverrouillez le code sans être sûr, sauf si le volume du système d’exploitation est crypté.</p></td>
</tr>
<tr class="even">
<td align="left"><p>0,15</p></td>
<td align="left"><p>La stratégie nécessite un minimum de Cypher, XTS-AES-128 bits, la force Cypher réelle est plus faible.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Seiz</p></td>
<td align="left"><p>La stratégie nécessite un minimum de Cypher, XTS-AES-256 bits, la force Cypher réelle est plus faible.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Document de référence technique pour MBAM2.5](technical-reference-for-mbam-25.md)

[Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 






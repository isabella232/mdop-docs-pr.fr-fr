---
title: Modification des paramètres de stratégie de groupe MBAM2.5
description: Modification des paramètres de stratégie de groupe MBAM2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804345"
---
# Modification des paramètres de stratégie de groupe MBAM2.5


Pour réussir le déploiement de l’administration et de la surveillance de BitLocker Microsoft (MBAM), vous devez:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copiez les modèles de stratégie de groupe MBAM 2,5.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copie des modèles de stratégie de groupe MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Déterminez les objets de stratégie de groupe que vous voulez utiliser dans votre implémentation de MBAM. En fonction des besoins de votre organisation, il se peut que vous deviez configurer des paramètres de stratégie de groupe supplémentaires.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)">Planification de la stratégie de groupe MBAM 2,5 </a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Définissez les paramètres de stratégie de groupe pour votre organisation.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Important**  Ne modifiez pas les paramètres de stratégie de groupe du nœud **BitLocker Drive Encryption** , ou MBAM ne fonctionne pas correctement. Lorsque vous configurez les paramètres de stratégie de groupe dans le nœud **MDOP MBAM (gestion du BitLocker)** , MBAM configure automatiquement les paramètres de **chiffrement de lecteur BitLocker** pour vous.

 

**Pour modifier les paramètres de stratégie de groupe du client MBAM**

1.  Sur un ordinateur sur lequel sont installés les modèles de stratégie de groupe de MBAM, assurez-vous que les services MBAM sont activés.

2.  À l’aide de la console de gestion **des stratégies de** groupe (GPMC. msc) ou du produit de gestion de stratégie de groupe Microsoft avancée sur un ordinateur sur lequel sont installés &gt; **Policies** les modèles de &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** stratégie de groupe MBAM

3.  Modifiez les paramètres de stratégie de groupe requis pour activer les services clients MBAM sur des ordinateurs clients. Pour chaque stratégie figurant dans le tableau suivant, sélectionnez **groupe de stratégies**, cliquez sur la **stratégie** souhaitée, puis configurez les paramètres.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Groupe de stratégies</th>
    <th align="left">Stratégie</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Gestion des clients</p></td>
    <td align="left"><p>Configurer les services de MBAM</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Lecteur du système d’exploitation</p></td>
    <td align="left"><p>Paramètres de chiffrement de lecteur du système d’exploitation</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Lecteur amovible</p></td>
    <td align="left"><p>Contrôler l’utilisation de BitLocker sur des lecteurs amovibles</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Lecteur fixe</p></td>
    <td align="left"><p>Contrôler l’utilisation de BitLocker sur des disques fixes</p></td>
    </tr>
    </tbody>
    </table>

     

## Rubriques connexes


[Planification des exigences en matière de stratégie de groupe MBAM2.5](planning-for-mbam-25-group-policy-requirements.md)

[Copie des modèles de stratégie de groupe MBAM2.5](copying-the-mbam-25-group-policy-templates.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 






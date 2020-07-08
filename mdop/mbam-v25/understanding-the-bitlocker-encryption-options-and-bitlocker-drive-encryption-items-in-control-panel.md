---
title: Présentation des éléments Options de chiffrement BitLocker et Chiffrement de lecteur BitLocker du Panneau de configuration
description: Présentation des éléments Options de chiffrement BitLocker et Chiffrement de lecteur BitLocker du Panneau de configuration
author: dansimp
ms.assetid: f8a01cc2-0c77-48b9-8351-8194e80b0cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739b65680ebfdf19f006ee8f3079f7c7e602f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804477"
---
# Présentation des éléments Options de chiffrement BitLocker et Chiffrement de lecteur BitLocker du Panneau de configuration


Cette rubrique décrit les **options de chiffrement BitLocker** et les éléments du panneau de configuration **BitLocker Drive Encryption** et explique ce qui suit:

-   Création de ces éléments

-   Tâches qu’ils vous permettent d’effectuer

-   **Gérer BitLocker** «cliquer avec le bouton droit» dans le menu contextuel, lorsqu’il est visible ou masqué et comment le configurer comme affiché par défaut

## Options de chiffrement BitLocker et éléments du panneau de configuration BitLocker Drive Encryption


Le tableau suivant répertorie les tâches que vous pouvez effectuer dans chaque élément du panneau de configuration, ainsi que le mode de création de ces éléments.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Options de chiffrement BitLocker (MBAM)</th>
<th align="left">Chiffrement de lecteur BitLocker (Windows)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tâches possibles</p></td>
<td align="left"><ul>
<li><p>Modifier votre code confidentiel ou votre mot de passe</p></li>
<li><p>Vérifier l’état de chiffrement d’un lecteur</p></li>
<li><p>Ouvrez la console de gestion du TPM.</p></li>
<li><p>Activer BitLocker</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Suspendre la protection d’un lecteur</p></li>
<li><p>Sauvegarder votre clé de récupération</p></li>
<li><p>Changer votre code confidentiel</p></li>
<li><p>Désactiver BitLocker pour un lecteur</p></li>
<li><p>Activation de BitLocker pour un lecteur</p></li>
<li><p>Ouvrez la console de gestion du TPM.</p></li>
<li><p>Déchiffrer un lecteur (s’affiche uniquement si le client MBAM n’est pas installé)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Création de l’élément panneau de configuration</p></td>
<td align="left"><p>Créé dans le panneau de configuration lors de l’installation du client MBAM. Cet élément ne peut pas être masqué.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Cet élément apparaît en plus de l’élément, mais ne remplace pas le panneau de configuration par défaut du chiffrement de lecteurs BitLocker.</p>
</div>
<div>

</div></td>
<td align="left"><p>Apparaît par défaut dans le panneau de configuration en tant que composant du système d’exploitation Windows, mais vous pouvez la masquer.</p>
<p>Pour le masquer, voir <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)"> masquage de l’élément chiffrement de lecteur BitLocker par défaut dans le panneau de configuration </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="-manage-bitlocker--shortcut-menu"></a>Menu contextuel «gérer BitLocker»


Le tableau suivant décrit la manière dont le menu contextuel **gérer BitLocker** est différent selon que le client MBAM est installé ou non. Le terme «menu contextuel» fait référence aux options qui s’affichent lorsque vous cliquez avec le bouton droit sur un lecteur de l’Explorateur Windows.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Lors de l’installation du client MBAM</th>
<th align="left">Lorsque le client MBAM n’est pas installé</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Visibilité du menu contextuel</p></td>
<td align="left"><p>L’option gérer BitLocker est masquée.</p>
<p>Pour que l’option gérer BitLocker soit visible dans le menu contextuel, qui affiche l’option de déchiffrement d’un lecteur, supprimez la clé de Registre suivante:</p>
<pre class="syntax" space="preserve"><code>HKEY_CLASSES_ROOT\Drive\Shell\manage-bde \REG_SZ LegacyDisable</code></pre></td>
<td align="left"><p>L’option gérer BitLocker apparaît dans le menu contextuel.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ce que les utilisateurs peuvent faire</p></td>
<td align="left"><p>Lorsque le raccourci est masqué, les utilisateurs peuvent ouvrir l’élément panneau de configuration du chiffrement de lecteurs BitLocker, mais l’option permettant de déchiffrer un lecteur n’est pas disponible.</p></td>
<td align="left"><p>Lorsque le raccourci est visible, la sélection de l' <strong> option gérer BitLocker </strong> ouvre l’élément panneau de configuration du chiffrement de lecteur BitLocker qui affiche l’option de déchiffrement d’un lecteur.</p></td>
</tr>
</tbody>
</table>




## Rubriques connexes


[Administration des composants de MBAM2.5](administering-mbam-25-features.md)



## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 






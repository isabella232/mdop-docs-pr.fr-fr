---
title: Récupération d'un lecteur endommagé
description: Récupération d'un lecteur endommagé
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809425"
---
# Récupération d'un lecteur endommagé


Vous pouvez utiliser cette procédure avec le site Web d’administration et de contrôle (également appelé support technique) pour récupérer un lecteur endommagé qui est protégé par BitLocker. Pour cela, vous devez effectuer les tâches indiquées dans le tableau suivant.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Détails et informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Créez un fichier de package de clé de récupération en accédant à la <strong> </strong> zone de récupération du lecteur sur le site Web d’administration et de surveillance.</p></td>
<td align="left"><p>Pour accéder à la <strong> zone de récupération du lecteur </strong> , vous devez disposer du rôle utilisateurs du support technique MBAM ou du rôle MBAM Advanced support Users. Il est possible que vous ayez attribué un nom différent aux rôles lorsque vous les avez créés. Pour plus d’informations, reportez-vous <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> à planification pour les comptes et groupes MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copiez le fichier de package sur l’ordinateur qui contient le lecteur endommagé.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utiliser la <code>repair-bde</code> commande pour terminer le processus de récupération.</p></td>
<td align="left"><p>Pour éviter une perte de données potentielle, il est vivement recommandé de revoir la <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> commande Manage-bde </a> avant de l’utiliser.</p></td>
</tr>
</tbody>
</table>

 

**Pour récupérer un lecteur endommagé**

1.  Ouvrez un navigateur Web, puis accédez au **site Web d’administration et de surveillance**.

2.  Dans le volet gauche, sélectionnez **récupération de lecteur** pour ouvrir la page **récupérer l’accès à un lecteur chiffré** .

3.  Entrez le nom d’utilisateur et le domaine d’ouverture de session Windows de l’utilisateur final, la raison pour laquelle vous pouvez déverrouiller le lecteur et l’ID du mot de passe de récupération de l’utilisateur final.

    **Remarques**  Si vous êtes membre du groupe Advanced support Users Access, vous n’êtes pas obligé d’entrer le nom de domaine ou le nom d’utilisateur de l’utilisateur.

     

4.  Cliquez sur **Envoyer**. La clé de récupération s’affiche.

5.  Cliquez sur **Enregistrer**, puis sélectionnez **package de clé de récupération**. Le package de clé de récupération sera créé sur votre ordinateur.

6.  Copiez le package de clé de récupération sur l’ordinateur sur lequel le lecteur est endommagé.

7.  Ouvrez une invite de commandes avec élévation de privilèges. Pour cela, cliquez sur **Démarrer** , puis tapez `cmd` dans la zone de texte Rechercher dans les **programmes et fichiers** . Cliquez avec le bouton droit sur **cmd.exe**et sélectionnez **exécuter en tant qu’administrateur**.

8.  À l’invite de commandes, tapez ce qui suit:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Remarques**  Remplacez &lt; un *lecteur fixe* &gt; par un disque dur disponible dont l’espace disponible est supérieur ou égal à celui des données sur le disque endommagé. Les données du lecteur endommagé sont récupérées et déplacées sur le disque dur spécifié.

     


## Rubriques connexes


[Gestion de BitLocker avec MBAM2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 






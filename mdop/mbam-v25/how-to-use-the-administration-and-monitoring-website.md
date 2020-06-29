---
title: Utilisation du site web d'administration et de surveillance
description: Utilisation du site web d'administration et de surveillance
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804681"
---
# Utilisation du site web d'administration et de surveillance


Le site Web d’administration et de surveillance, également appelé support technique, est une interface d’administration pour le chiffrement de lecteur BitLocker. Utilisez le site Web pour passer en revue les rapports, récupérer les lecteurs des utilisateurs finaux et gérer les TPMs des utilisateurs finaux, comme décrit dans les sections suivantes.

**Remarques**  Si vous utilisez MBAM dans la topologie autonome, vous pouvez afficher tous les rapports à partir du site Web Administration et analyse. Si vous utilisez la topologie d’intégration Configuration Manager, vous pouvez afficher tous les rapports dans Configuration Manager, à l’exception du rapport d’audit de récupération, que vous continuez à consulter à partir du site Web d’administration et de surveillance. Pour plus d’informations sur les rapports, voir [surveillance et signalement de la conformité avec BitLocker avec MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).

 

## Rôles requis pour l’utilisation du site Web d’administration et de surveillance


Pour accéder à certaines zones du site Web d’administration et de surveillance, vous devez disposer de l’un des rôles suivants, qui sont des groupes que vous créez dans Active Directory. Vous pouvez utiliser n’importe quel nom pour ces groupes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Compte</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utilisateurs du support technique avancée MBAM</p></td>
<td align="left"><p>Permet d’accéder à toutes les zones du site Web d’administration et de surveillance. Les utilisateurs qui ont ce rôle ne peuvent entrer que la clé de récupération, et non le domaine et le nom d’utilisateur de l’utilisateur final, pour aider les utilisateurs finaux à récupérer leurs lecteurs. Si un utilisateur est membre du groupe utilisateurs du support technique MBAM et du groupe utilisateurs du support technique avancé MBAM, les autorisations de groupe utilisateurs du support technique avancée MBAM sont prioritaires sur les autorisations du groupe utilisateurs du support technique MBAM.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateurs du support technique MBAM</p></td>
<td align="left"><p>Permet d’accéder aux zones gérer le module de plateforme sécurisée et de récupération des lecteurs du site Web d’administration et de surveillance. Les personnes qui ont ce rôle doivent remplir tous les champs, y compris le nom de domaine et le nom du compte de l’utilisateur final, lorsqu’ils utilisent l’une de ces zones.</p>
<p>Si un utilisateur est membre du groupe utilisateurs du support technique MBAM et du groupe utilisateurs du support technique avancé MBAM, les autorisations de groupe utilisateurs du support technique avancée MBAM sont prioritaires sur les autorisations du groupe utilisateurs du support technique MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs de rapports MBAM</p></td>
<td align="left"><p>Donne accès aux rapports figurant dans la <strong> </strong> zone rapports du site Web d’administration et de surveillance.</p></td>
</tr>
</tbody>
</table>

 

## Tâches que vous pouvez effectuer sur le site Web d’administration et de surveillance


Le tableau suivant récapitule les tâches que vous pouvez effectuer sur le site Web d’administration et de contrôle, ainsi que des liens vers des informations supplémentaires sur chaque tâche.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Zone du site Web où vous accédez à la tâche</th>
<th align="left">Description</th>
<th align="left">Pour plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Affichage des rapports</p></td>
<td align="left"><p>Rapports</p></td>
<td align="left"><p>Vous permet d’exécuter des rapports pour surveiller l’activité d’utilisation, de conformité et de récupération de clés de BitLocker. Les rapports fournissent des données concernant la conformité d’entreprise, des ordinateurs individuels et la personne qui a demandé les clés de récupération ou le package OwnerAuth TPM pour un ordinateur spécifique.</p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)">Affichage de rapports MBAM2.5 pour la topologie autonome</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Déterminer l’état de chiffrement de BitLocker des ordinateurs perdus ou volés</p></td>
<td align="left"><p>Rapports</p></td>
<td align="left"><p>Déterminer si un volume a été chiffré en cas de perte ou de vol de l’ordinateur.</p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)">Détermination de l'état de chiffrement BitLocker des ordinateurs perdus</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Récupérer des lecteurs perdus</p></td>
<td align="left"><p>Récupération des lecteurs</p></td>
<td align="left"><p>Récupérer des lecteurs:</p>
<ul>
<li><p>En mode récupération</p></li>
<li><p>Ont été déplacés</p></li>
<li><p>Sont endommagés</p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)">Procédure de récupération d'un lecteur en mode de récupération</a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)">Récupération d'un lecteur déplacé</a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)">Récupération d'un lecteur endommagé</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Réinitialiser un verrouillage du TPM</p></td>
<td align="left"><p>Gérer le TPM</p></td>
<td align="left"><p>Donne accès aux données du TPM collectées par le client MBAM. Dans un verrouillage de module de plateforme sécurisée, utilisez le site Web d’administration et de surveillance pour extraire le fichier de mot de passe nécessaire pour déverrouiller le TPM.</p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)">Réinitialisation d'un verrouillage TPM</a></p></td>
</tr>
</tbody>
</table>

 


## Rubriques connexes


[Gestion de BitLocker avec MBAM2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 






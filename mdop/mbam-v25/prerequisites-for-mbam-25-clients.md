---
title: Conditions préalables pour les clients MBAM2.5
description: Conditions préalables pour les clients MBAM2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812072"
---
# Conditions préalables pour les clients MBAM2.5


Avant d’installer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux, assurez-vous que votre environnement et vos ordinateurs clients répondent aux conditions préalables suivantes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Le domaine d’entreprise doit contenir au moins un contrôleur de domaine Windows Server 2008 (ou version ultérieure).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>L’ordinateur client doit être connecté à l’intranet de l’entreprise.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pour les ordinateurs clients Windows 7 uniquement: chaque client doit disposer de la fonctionnalité de module de plateforme sécurisée (TPM 1,2 ou version ultérieure).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Pour les ordinateurs clients Windows 8,1, Windows 10 ou Windows 10 version 1511 uniquement: Si vous souhaitez que MBAM puisse stocker et gérer les clés de récupération du TPM, la fonction de configuration automatique du TPM doit être désactivée, et MBAM doit être défini en tant que propriétaire du TPM avant le déploiement d’MBAM.</p>
<p>Dans MBAM 2,5 SP1 uniquement, il n’est plus nécessaire de désactiver la mise en service automatique du module de plateforme sécurisée, mais vous devez vous assurer que les objets de stratégie de groupe du TPM sont définis sur not TRUSTed OwnerAuth to Active Directory.</p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)">Considérations relatives à la sécurité pour MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pour Windows 10, version 1607 ou ultérieure, seules les fenêtres peuvent prendre possession du module de plateforme sécurisée. Dans addiiton, Windows ne conserve pas le mot de passe du propriétaire du TPM lors de la mise en service du module de plateforme sécurisée.</p>
<p>Dans MBAM 2,5 SP1, vous devez activer la configuration automatique.</p>
</p></td>
<td align="left"><p>Pour en savoir <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> plus, voir mot de passe </a> du propriétaire du TPM.
</p></td>
</tr>
<tr class="even">
<td align="left"><p>Le processeur du TPM doit être activé dans le BIOS et être Resettable du système d’exploitation.</p></td>
<td align="left"><p>Pour plus d’informations, consultez la documentation relative au BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Le disque dur de l’ordinateur doit avoir au moins deux partitions et doit être mis en forme avec le système de fichiers NTFS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Le disque dur de l’ordinateur doit être équipé d’un BIOS compatible avec le TPM et prenant en charge les appareils USB au démarrage de l’ordinateur.</p></td>
<td align="left"><div class="alert">
<strong>Remarque</strong><br/><p>Assurez-vous que le clavier, la vidéo ou la souris sont directement connectés et ne sont pas gérés par le biais d’un clavier, d’une vidéo ou d’un commutateur de souris (KVM). Un commutateur KVM peut interférer avec la capacité de l’ordinateur à détecter la présence physique du matériel.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Si vous utilisez un proxy, il doit être visible dans le contexte système. MBAM s’exécute dans le contexte du système, et non dans le contexte de l’utilisateur.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**Important**  
Si BitLocker a été utilisé sans MBAM, MBAM peut être installé et utiliser les informations existantes du TPM.




## Rubriques connexes


[Configurations prises en charge par MBAM2.5](mbam-25-supported-configurations.md)

[Planification du déploiement de MBAM2.5](planning-to-deploy-mbam-25.md)


## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).







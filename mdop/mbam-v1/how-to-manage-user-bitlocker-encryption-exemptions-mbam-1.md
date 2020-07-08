---
title: Gestion des exemptions de chiffrement BitLocker d'utilisateur
description: Gestion des exemptions de chiffrement BitLocker d'utilisateur
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804621"
---
# Gestion des exemptions de chiffrement BitLocker d'utilisateur


L’utilisation de Microsoft BitLocker administration et de la surveillance (MBAM) peut être utilisée pour gérer la protection de BitLocker en exemptant les utilisateurs qui n’ont pas besoin ou veulent que leurs lecteurs soient chiffrés.

Pour exempter les utilisateurs de la protection de BitLocker, une organisation doit d’abord créer une infrastructure pour prendre en charge ces exemptions. L’infrastructure de support technique peut inclure un numéro de téléphone de contact, une page Web ou une adresse postale pour demander une exemption. De plus, tous les utilisateurs exemptés devront être ajoutés à un groupe de sécurité pour une stratégie de groupe créée spécifiquement pour les utilisateurs exemptés. Lorsque les membres de ce groupe de sécurité se connectent à un ordinateur, la stratégie de groupe d’utilisateurs indique que l’utilisateur est exempté de la protection BitLocker. La stratégie de l’utilisateur remplace la stratégie de l’ordinateur, et celle-ci reste exemptée du chiffrement BitLocker.

**Remarques**  Si l’ordinateur est déjà protégé par BitLocker, la stratégie d’exemption d’utilisateur n’a aucun effet.

 

Le tableau suivant indique la façon dont la protection de BitLocker est appliquée en fonction de la façon dont les exemptions sont définies.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">État de l’utilisateur</th>
<th align="left">Ordinateur non exempté</th>
<th align="left">Exonéré d’ordinateur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Utilisateur non exempté</strong></p></td>
<td align="left"><p>La protection BitLocker est appliquée à l’ordinateur.</p></td>
<td align="left"><p>La protection BitLocker n’est pas appliquée à l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Exonéré d’utilisateur</strong></p></td>
<td align="left"><p>La protection BitLocker n’est pas appliquée à l’ordinateur.</p></td>
<td align="left"><p>La protection BitLocker n’est pas appliquée à l’ordinateur.</p></td>
</tr>
</tbody>
</table>

 

**Pour exempter un utilisateur d’un chiffrement BitLocker**

1.  Créer un groupe de sécurité ActiveDirectoryDomainServices qui sera utilisé pour gérer les exemptions d’utilisateur à partir du chiffrement BitLocker.

2.  Créer un paramètre d’objet de stratégie de groupe à l’aide du modèle de stratégie de groupe MBAM. Associez l’objet de stratégie de groupe au groupe Active Directory que vous avez créé à l’étape précédente. Pour plus d’informations sur les paramètres de stratégie nécessaires et permettre aux utilisateurs de demander une exemption du chiffrement BitLocker, voir la section configurer une stratégie d’exemption d’utilisateur pour la [planification des spécifications de la stratégie de groupe MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).

3.  Après avoir créé un groupe de sécurité pour les utilisateurs exemptés de BitLocker, ajoutez à ce groupe les noms des utilisateurs qui demandent une exemption. Lorsqu’un utilisateur ouvre une session sur un ordinateur contrôlé par BitLocker, le client MBAM vérifie le paramètre de stratégie d’exemption des utilisateurs et suspend la protection en fonction de la présence de l’utilisateur dans le groupe de sécurité d’exemption BitLocker.

    **Remarques**  Les scénarios d’ordinateurs partagés nécessitent une prise en considération particulière concernant l’exemption des utilisateurs. Si un utilisateur non exempté se connecte à un ordinateur partagé avec un utilisateur exempté, il est possible que l’ordinateur soit crypté.

     

**Pour permettre aux utilisateurs de demander une exemption du chiffrement BitLocker**

1.  Après avoir configuré les stratégies d’exemption des utilisateurs en usingwith le modèle de stratégie MBAM, un utilisateur peut demander une exemption de protection BitLocker via le client MBAM.

2.  Lorsqu’un utilisateur ouvre une session sur un ordinateur marqué comme **compatible** dans la liste de compatibilité matérielle MBAM, le système présente à l’utilisateur une notification indiquant que l’ordinateur va être chiffré. L’utilisateur peut sélectionner l' **exemption de demande** et différer le chiffrement en le sélectionnant **plus tard**, ou sélectionnez **Démarrer** pour accepter le chiffrement BitLocker.

    **Remarques**  La sélection de l' **exemption de requête** différera la protection de BitLocker jusqu’à la durée maximale définie dans la stratégie d’exemption de l’utilisateur.

     

3.  Lorsqu’un utilisateur sélectionne une **exemption de requête**, il est prévenu de contacter le groupe d’administration BitLocker de l’organisation. En fonction du mode de configuration de la stratégie d’exemption d’utilisateur, les utilisateurs disposent d’une ou plusieurs des méthodes de contact suivantes:

    -   Numéro de téléphone

    -   URL de la page Web

    -   Adresse postale

    Après l’envoi de la demande, l’administrateur MBAM peut décider s’il convient d’ajouter l’utilisateur au groupe Active Directory d’exemption BitLocker.

    **Remarques**  Lorsque la limite de temps de report de la stratégie d’exemption des utilisateurs a expiré, les utilisateurs ne voient pas l’option de demande d’exemption de la stratégie de chiffrement. À ce stade, les utilisateurs doivent contacter l’administrateur MBAM directement pour pouvoir bénéficier d’une exemption de la protection de BitLocker.

     

## Rubriques connexes


[Administration des composants de MBAM1.0](administering-mbam-10-features.md)

 

 






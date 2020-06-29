---
title: Gestion des exemptions de chiffrement BitLocker d'utilisateur
description: Gestion des exemptions de chiffrement BitLocker d'utilisateur
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810937"
---
# Gestion des exemptions de chiffrement BitLocker d'utilisateur


Le contrôle de la protection BitLocker par le biais de l’administration et de la surveillance de Microsoft BitLocker (MBAM) permet d’exempter les utilisateurs si des utilisateurs n’ont pas besoin ou veulent que leurs lecteurs soient chiffrés.

Pour exempter les utilisateurs de la protection de BitLocker, une organisation doit créer une infrastructure pour prendre en charge les utilisateurs exemptés, comme le fait de fournir à l’utilisateur un numéro de téléphone, une page Web ou une adresse de messagerie à utiliser pour demander une exemption. Par ailleurs, un utilisateur exempté doit être ajouté à un groupe de sécurité pour un objet de stratégie de groupe qui a été créé spécifiquement pour les utilisateurs exemptés. Lorsque les membres de ce groupe de sécurité se connectent à un ordinateur, le paramètre de stratégie de groupe de l’utilisateur indique que l’utilisateur est exempté de la protection de BitLocker. Le paramètre de stratégie de groupe de l’utilisateur remplace la stratégie de l’ordinateur et l’ordinateur reste exempt du chiffrement BitLocker.

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
<td align="left"><p>La protection BitLocker est appliquée sur un ordinateur</p></td>
<td align="left"><p>La protection BitLocker n’est pas appliquée sur l’ordinateur</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Exonéré d’utilisateur</strong></p></td>
<td align="left"><p>La protection BitLocker n’est pas appliquée sur l’ordinateur</p></td>
<td align="left"><p>La protection BitLocker n’est pas appliquée sur l’ordinateur</p></td>
</tr>
</tbody>
</table>

 

**Pour exempter un utilisateur d’un chiffrement BitLocker**

1.  Créer un groupe de sécurité ActiveDirectoryDomainServices qui sera utilisé pour gérer les exemptions des utilisateurs des exigences de chiffrement de BitLocker.

2.  Créez un paramètre d’objet de stratégie de groupe à l’aide du modèle Microsoft BitLocker Administration and Monitoring Policy et associez-le au groupe Active Directory que vous avez créé à l’étape précédente. Les paramètres de stratégie permettant d’exempter les utilisateurs sont accessibles sous **UserConfiguration\\Administrative Templates\\Windows COMPONENTS\\MDOP MBAM (gestion de BitLocker)**.

3.  Après avoir créé un groupe de sécurité pour les utilisateurs exemptés de BitLocker, ajoutez à ce groupe les noms des utilisateurs qui demandent une exemption. Lorsque les utilisateurs se connectent à un ordinateur contrôlé par BitLocker, le client MBAM vérifie le paramètre de stratégie d’exemption des utilisateurs et suspend la protection en fonction de la présence de l’utilisateur dans le groupe de sécurité d’exemption BitLocker.

    **Important**  Les scénarios d’ordinateurs partagés nécessitent une prise en considération particulière lors de l’utilisation d’exemptions utilisateur. Si un utilisateur non exempté se connecte à un ordinateur partagé avec un utilisateur exempté, il est possible que l’ordinateur soit crypté.

     

**Pour permettre aux utilisateurs de demander une exemption du chiffrement BitLocker**

1.  Si vous avez configuré des stratégies d’exemption utilisateur à l’aide du modèle de stratégie MBAM, un utilisateur peut demander une exemption de protection BitLocker via le client MBAM.

2.  Lorsque les utilisateurs se connectent à un ordinateur qui est tenu d’être chiffrés, ils reçoivent une notification indiquant que leur ordinateur va être chiffré. Ils peuvent sélectionner l' **exemption de demande** et différer le chiffrement en sélectionnant **plus tard**, ou sélectionnez **Démarrer** pour accepter le chiffrement BitLocker.

    **Remarques**  Le fait de sélectionner **dispense de requête** permet de différer la protection BitLocker jusqu’au délai maximal défini dans la stratégie d’exemption des utilisateurs.

     

3.  Si les utilisateurs sélectionnent une **exemption de demande**, ils reçoivent une notification leur indiquant de contacter le groupe d’administration BitLocker de votre organisation. En fonction du mode de configuration de la stratégie d’exemption d’utilisateur, les utilisateurs disposent d’une ou plusieurs des méthodes de contact suivantes:

    -   Numéro de téléphone

    -   URL de la page Web

    -   Adresse postale

    Après la réception de la demande d’exemption, l’administrateur MBAM peut décider s’il convient d’ajouter l’utilisateur au groupe Active Directory d’exemption BitLocker.

    **Remarques**  Dès qu’un utilisateur envoie une demande d’exemption, l’agent MBAM signale que l’utilisateur est «exempt provisoire», puis attend un nombre de jours configuré avant de vérifier la compatibilité de l’ordinateur. Si l’administrateur MBAM rejette la demande d’exemption, l’option de demande d’exemption est désactivée, ce qui permet à l’utilisateur d’être à nouveau en mesure de demander l’exemption.

     

## Rubriques connexes


[Administration des composants de MBAM2.0](administering-mbam-20-features-mbam-2.md)

 

 






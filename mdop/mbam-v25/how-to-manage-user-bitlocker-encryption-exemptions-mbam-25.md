---
title: Gestion des exemptions de chiffrement BitLocker d'utilisateur
description: Gestion des exemptions de chiffrement BitLocker d'utilisateur
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811969"
---
# Gestion des exemptions de chiffrement BitLocker d'utilisateur


Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) vous permet d’exempter les utilisateurs des exigences relatives au chiffrement de lecteur BitLocker.

Pour exempter les utilisateurs de la protection BitLocker, vous devez:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Créez une infrastructure pour prendre en charge les utilisateurs exemptés.</p></td>
<td align="left"><p>Dans le cas d’une telle infrastructure, il est possible de fournir aux utilisateurs un numéro de téléphone de contact, une page Web ou une adresse postale qu’ils peuvent utiliser pour demander une exemption.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ajoutez l’utilisateur exempté à un groupe de sécurité pour un objet de stratégie de groupe qui est configuré spécifiquement pour les utilisateurs exemptés.</p></td>
<td align="left"><p>Lorsque les membres de ce groupe de sécurité se connectent à un ordinateur, le paramètre de stratégie de groupe de l’utilisateur exempte l’utilisateur de la protection BitLocker. Le paramètre de stratégie de groupe de l’utilisateur remplace la stratégie de l’ordinateur et l’ordinateur reste exempt du chiffrement BitLocker.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>MBAM ne prend pas en charge la stratégie de chiffrement si l’ordinateur est déjà protégé par BitLocker et qu’il est exempté. Toutefois, si un autre utilisateur qui n’est pas exempt de la stratégie de cryptage se connecte à l’ordinateur, le chiffrement aura lieu.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Les étapes suivantes décrivent ce qui se produit lorsque les utilisateurs finaux demandent une exemption du processus d’exemption du chiffrement de lecteur BitLocker par le biais du client MBAM ou du processus utilisé par votre organisation. Vous devez configurer des paramètres de stratégie de groupe MBAM pour autoriser les utilisateurs finaux à demander une exemption du chiffrement de lecteur BitLocker.

1.  Lorsque les utilisateurs finaux se connectent à un ordinateur requis pour être chiffrés, ils reçoivent une notification indiquant que leur ordinateur va être chiffré. Ils peuvent sélectionner l' **exemption de demande** et différer le chiffrement en sélectionnant **différer**, ou ils peuvent sélectionner **commencer le chiffrement** pour accepter le chiffrement BitLocker.

    **Remarque**  
    Le fait de sélectionner **dispense de requête** permet de différer la protection BitLocker jusqu’au délai maximal défini dans la stratégie d’exemption des utilisateurs.



2.  Si les utilisateurs finaux sélectionnent une **demande d’exemption**, ils reçoivent une notification leur demandant de contacter le groupe d’administration BitLocker de l’organisation. En fonction du mode de configuration de la **stratégie d’exemption d’utilisateur** , les utilisateurs disposent d’une ou plusieurs des méthodes de contact suivantes:

    -   Numéro de téléphone

    -   URL de la page Web

    -   Adresse postale

3.  Après la réception de la demande d’exemption, l’administrateur MBAM décide s’il doit ajouter l’utilisateur au groupe AD DS (Active Directory Domain Services) d’exemption BitLocker.

4.  Après l’envoi d’une demande d’exemption par un utilisateur final, le client MBAM signale que l’utilisateur est «exempté temporaire». Le client attend alors un nombre de jours spécifié, qu’il doit configurer, avant de vérifier à nouveau la conformité de l’ordinateur. Si l’administrateur MBAM rejette la demande d’exemption, l’option de demande d’exemption est désactivée, ce qui empêche l’utilisateur de demander de nouveau l’exemption.

Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) vous permet d’exempter les utilisateurs des exigences relatives au chiffrement de lecteur BitLocker.

Pour exempter les utilisateurs de la protection BitLocker, vous devez:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Créez une infrastructure pour prendre en charge les utilisateurs exemptés.</p></td>
<td align="left"><p>Dans le cas d’une telle infrastructure, il est possible de fournir aux utilisateurs un numéro de téléphone de contact, une page Web ou une adresse postale qu’ils peuvent utiliser pour demander une exemption.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ajoutez l’utilisateur exempté à un groupe de sécurité pour un objet de stratégie de groupe qui est configuré spécifiquement pour les utilisateurs exemptés.</p></td>
<td align="left"><p>Lorsque les membres de ce groupe de sécurité se connectent à un ordinateur, le paramètre de stratégie de groupe de l’utilisateur exempte l’utilisateur de la protection BitLocker. Le paramètre de stratégie de groupe de l’utilisateur remplace la stratégie de l’ordinateur et l’ordinateur reste exempt du chiffrement BitLocker.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si l’ordinateur est déjà protégé par BitLocker, la stratégie d’exemption d’utilisateur n’a aucun effet. De plus, si un autre utilisateur se connecte à un ordinateur qui n’est pas exempt de la stratégie de chiffrement, le chiffrement aura lieu.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Les étapes suivantes décrivent ce qui se produit lorsque les utilisateurs finaux demandent une exemption du processus d’exemption du chiffrement de lecteur BitLocker par le biais du client MBAM ou du processus utilisé par votre organisation. Vous devez configurer des paramètres de stratégie de groupe MBAM pour autoriser les utilisateurs finaux à demander une exemption du chiffrement de lecteur BitLocker.

1.  Lorsque les utilisateurs finaux se connectent à un ordinateur requis pour être chiffrés, ils reçoivent une notification indiquant que leur ordinateur va être chiffré. Ils peuvent sélectionner l' **exemption de demande** et différer le chiffrement en sélectionnant **différer**, ou ils peuvent sélectionner **commencer le chiffrement** pour accepter le chiffrement BitLocker.

    **Remarque**  
    Le fait de sélectionner **dispense de requête** permet de différer la protection BitLocker jusqu’au délai maximal défini dans la stratégie d’exemption des utilisateurs.



2.  Si les utilisateurs finaux sélectionnent une **demande d’exemption**, ils reçoivent une notification leur demandant de contacter le groupe d’administration BitLocker de l’organisation. En fonction du mode de configuration de la **stratégie d’exemption d’utilisateur** , les utilisateurs disposent d’une ou plusieurs des méthodes de contact suivantes:

    -   Numéro de téléphone

    -   URL de la page Web

    -   Adresse postale

3.  Après la réception de la demande d’exemption, l’administrateur MBAM décide s’il doit ajouter l’utilisateur au groupe AD DS (Active Directory Domain Services) d’exemption BitLocker.

4.  Après l’envoi d’une demande d’exemption par un utilisateur final, le client MBAM signale que l’utilisateur est «exempté temporaire». Le client attend alors un nombre de jours spécifié, qu’il doit configurer, avant de vérifier à nouveau la conformité de l’ordinateur. Si l’administrateur MBAM rejette la demande d’exemption, l’option de demande d’exemption est désactivée, ce qui empêche l’utilisateur de demander de nouveau l’exemption.

**Pour exempter un utilisateur d’un chiffrement de lecteur BitLocker**

1.  Créer un groupe de sécurité AD DS qui sera utilisé pour gérer les exemptions des utilisateurs des exigences de chiffrement de BitLocker.

2.  Création d’un objet de stratégie de groupe à l’aide des modèles de stratégie de groupe Microsoft et administration de BitLocker.

3.  Associez l’objet de stratégie de groupe au groupe AD DS que vous avez créé à l’étape précédente. Les paramètres de stratégie permettant d’exempter les utilisateurs se trouvent dans l’emplacement suivant: **UserConfiguration** des &gt; **modèles d’administration** &gt; **composants** &gt; **MBAM MDOP (gestion de BitLocker)**.

4.  Pour le groupe de sécurité que vous avez créé pour les utilisateurs exemptés de BitLocker, ajoutez le nom des utilisateurs demandant une exemption.

    Lorsqu’un utilisateur se connecte à un ordinateur contrôlé par BitLocker, le client MBAM vérifie le paramètre de stratégie d’exemption de l’utilisateur. Si l’ordinateur est déjà crypté, la protection BitLocker n’est pas suspendue. Si l’ordinateur n’est pas chiffré, MBAM ne demande pas à l’utilisateur d’effectuer le chiffrement.

    **Important**  
    Les scénarios d’ordinateurs partagés nécessitent une prise en considération particulière lors de l’utilisation d’exemptions d’utilisateur BitLocker. Si un utilisateur non exempté se connecte à un ordinateur partagé avec un utilisateur exempté, il est possible que l’ordinateur soit crypté.




## Rubriques connexes


[Administration des composants de MBAM2.5](administering-mbam-25-features.md)

[Planification des exigences en matière de stratégie de groupe MBAM2.5](planning-for-mbam-25-group-policy-requirements.md)




## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).





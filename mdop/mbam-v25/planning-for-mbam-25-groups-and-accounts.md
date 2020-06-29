---
title: Planification des comptes et groupes MBAM2.5
description: Planification des comptes et groupes MBAM2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811375"
---
# Planification des comptes et groupes MBAM2.5


Cette rubrique répertorie les rôles et comptes que vous devez créer dans les services de domaine Active Directory (AD DS) pour fournir de la sécurité et des droits d’accès pour les bases de données, rapports et applications Web Microsoft BitLocker (MBAM). Pour chaque rôle et compte, le champ correspondant dans l’Assistant Configuration de MBAM Server est fourni. Pour obtenir la liste des cmdlets et paramètres Windows PowerShell qui correspondent à ces comptes, voir [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).

**Remarque**  
MBAM ne prend pas en charge l’utilisation des comptes de service géré.



## Comptes de base de données


Créez les comptes suivants pour la base de données d’audit et de compatibilité et pour la base de données de récupération.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom du compte et objet</th>
<th align="left">Type de compte</th>
<th align="left">Champ Assistant Configuration de MBAM Server qui correspond à ce compte</th>
<th align="left">Description du champ de l’Assistant Configuration de MBAM Server qui correspond à ce compte.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Compatibilité et audit de la base de données et de la base de données de récupération utilisateur ou groupe en lecture/écriture pour les rapports</p></td>
<td align="left"><p>Utilisateur ou groupe</p></td>
<td align="left"><p>Utilisateur ou groupe d’accès en lecture/écriture</p></td>
<td align="left"><p>Utilisateur ou groupe qui dispose d’un accès en lecture/écriture à la base de données de conformité et d’audit et à la base de données de récupération pour permettre aux applications Web d’accéder aux données et rapports dans ces bases de données.</p>
<p>Si vous entrez un nom d’utilisateur dans ce champ, il doit être de la même valeur que la valeur dans le <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> .</p>
<p>Si vous entrez un nom de groupe dans ce champ, la valeur du <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> doit être membre du groupe que vous entrez dans ce champ.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformité et audit de la base de données utilisateur ou groupe en lecture seule pour les rapports</p></td>
<td align="left"><p>Utilisateur ou groupe</p></td>
<td align="left"><p>Utilisateur ou groupe d’accès en lecture seule</p></td>
<td align="left"><p>Nom de l’utilisateur ou du groupe qui dispose d’un accès en lecture seule à la base de données d’audit et de conformité pour permettre aux rapports d’accéder aux données de conformité et d’audit de cette base de données.</p>
<p>Si vous entrez un nom d’utilisateur dans ce champ, il doit être le même que celui que vous avez spécifié dans le <strong> champ domaine de la base de données de conformité et d’audit </strong> de la <strong> page configurer des rapports </strong> .</p>
<p>Si vous entrez un nom de groupe dans ce champ, la valeur que vous spécifiez dans le <strong> champ domaine de la base de données de conformité et d’audit de </strong> la <strong> page configurer des rapports </strong> doit être membre du groupe que vous spécifiez dans ce champ.</p></td>
</tr>
</tbody>
</table>



## Comptes de création de rapports


Créez les comptes suivants pour la fonction rapports.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom/objectif du compte</th>
<th align="left">Type de compte</th>
<th align="left">Champ Assistant Configuration de MBAM Server qui correspond à ce compte</th>
<th align="left">Description du champ de l’Assistant Configuration de MBAM Server qui correspond à ce compte.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Rapport de groupe d’accès de domaine en lecture seule</p></td>
<td align="left"><p>Groupe</p></td>
<td align="left"><p>Groupe de domaine de rôle de rapport</p></td>
<td align="left"><p>Spécifie le groupe d’utilisateurs de domaine qui dispose d’un accès en lecture seule aux rapports figurant sur le site Web d’administration et de surveillance. Le groupe que vous spécifiez doit être le même que celui que vous avez spécifié pour le paramètre rapport de groupe d’accès en lecture seule lorsque les applications Web sont activées.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Compte d’utilisateur de base de données et de conformité</p></td>
<td align="left"><p>Utilisateur</p></td>
<td align="left"><p>Vérification de la conformité et de la base de données du compte de domaine</p></td>
<td align="left"><p>Compte d’utilisateur de domaine et mot de passe que l’instance SQL Server Reporting Services locale utilise pour accéder à la base de données d’audit et de conformité. Ce compte nécessite <strong> le droit d’ouverture de session par lot </strong> du serveur SQL Server Reporting Services.</p>
<p>Si la valeur que vous entrez dans le <strong> champ nom d’utilisateur ou de groupe d’accès en lecture seule </strong> de la <strong> page Configurer les bases de données </strong> est un nom d’utilisateur, vous devez entrer cette même valeur dans ce champ.</p>
<p>Si la valeur que vous entrez dans le <strong> champ nom d’utilisateur ou de groupe d’accès en lecture seule </strong> de la <strong> page Configurer les bases de données </strong> est un nom de groupe, la valeur que vous entrez dans ce champ doit être membre du groupe.</p>
<p>Configurez le mot de passe de ce compte pour qu’il n’expire jamais. Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles pour le groupe utilisateurs de reports MBAM.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a>Site Web d’administration et de surveillance (support technique)


Créez les comptes suivants pour le site Web d’administration et de surveillance.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom/objectif du compte</th>
<th align="left">Type de compte</th>
<th align="left">Champ Assistant Configuration de MBAM Server qui correspond à ce compte</th>
<th align="left">Description du champ de l’Assistant Configuration de MBAM Server qui correspond à ce compte.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Compte de domaine du pool d’applications de service Web</p></td>
<td align="left"><p>Utilisateur</p></td>
<td align="left"><p>Compte de domaine du pool d’applications de service Web</p></td>
<td align="left"><p>Compte d’utilisateur de domaine devant être utilisé par le pool d’applications pour les applications Web.</p>
<p>Si vous entrez un nom d’utilisateur dans le <strong> champ d’utilisateur ou de groupe de domaine d’accès en lecture/écriture </strong> sur la <strong> page configurer des bases de données </strong> , vous devez entrer cette même valeur dans ce champ.</p>
<p>Si vous entrez un nom de groupe dans le <strong> champ User ou Group (lecture/écriture </strong> ) sur la <strong> page configure databases </strong> , la valeur que vous entrez dans ce champ doit être membre du groupe.</p>
<p>Si vous ne spécifiez pas les informations d’identification, les informations d’identification spécifiées pour une application Web précédemment activée seront utilisées. Toutes les applications Web doivent utiliser les mêmes informations d’identification de pool d’applications. Si vous spécifiez des informations d’identification différentes pour différentes applications Web, la valeur la plus récemment spécifiée est utilisée.</p>
<div class="alert">
<strong>Important</strong><br/><p>Pour une sécurité améliorée, définissez le compte spécifié dans les informations d’identification pour disposer de droits d’utilisateur limités.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Groupe d’accès utilisateurs du support technique avancée MBAM</p></td>
<td align="left"><p>Groupe</p></td>
<td align="left"><p>Utilisateurs du support technique avancée MBAM</p></td>
<td align="left"><p>Groupe d’utilisateurs de domaine dont les membres ont accès à toutes les zones de récupération du site Web d’administration et de surveillance. Les utilisateurs disposant de ce rôle doivent entrer uniquement la clé de récupération, et non le domaine et le nom d’utilisateur de l’utilisateur final, pour aider les utilisateurs finaux à récupérer leurs lecteurs. Si un utilisateur est membre du groupe utilisateurs du support technique MBAM et du groupe utilisateurs du support technique avancée MBAM, les autorisations du groupe utilisateurs du support technique avancé MBAM remplacent les autorisations du groupe assistance technique MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Groupe d’accès utilisateurs du support MBAM</p></td>
<td align="left"><p>Groupe</p></td>
<td align="left"><p>Utilisateurs du support technique MBAM</p></td>
<td align="left"><p>Groupe d’utilisateurs de domaine dont les membres ont accès aux zones gérer le module de plateforme sécurisée et de récupération des lecteurs du site Web d’administration et de contrôle MBAM. Les personnes qui ont ce rôle doivent remplir tous les champs, y compris le nom de domaine et le nom du compte de l’utilisateur final, lorsqu’ils utilisent une option.</p>
<p>Si un utilisateur est membre du groupe utilisateurs du support technique MBAM et du groupe utilisateurs du support technique avancée MBAM, les autorisations du groupe utilisateurs du support technique avancé MBAM remplacent les autorisations du groupe assistance technique MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Groupe accéder aux utilisateurs du rapport MBAM</p></td>
<td align="left"><p>Groupe</p></td>
<td align="left"><p>Utilisateurs de rapports MBAM</p></td>
<td align="left"><p>Groupe d’utilisateurs de domaine dont les membres ont un accès en lecture seule aux rapports figurant dans la zone rapports du site Web Administration et analyse.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Groupe d’utilisateurs de la migration des données MBAM</p></td>
<td align="left"><p>Groupe</p></td>
<td align="left"><p>Utilisateurs de la migration des données MBAM</p></td>
<td align="left"><p>Groupe d’utilisateurs de domaine facultatif dont les membres ont l’autorisation d’écrire des données dans MBAM à l’aide du service de récupération et de matériel de MBAM exécuté sur le serveur MBAM. Ce compte est généralement utilisé avec les applets de contrôle Write-MBAM * pour écrire des données de récupération et de TPM à partir d’Active Directory dans la base de données MBAM.</p>
<p>Pour plus d’informations, consultez <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considérations relatives à la sécurité de MBAM 2,5 </a> .</p></td>
</tr>
</tbody>
</table>




## Rubriques connexes


[Préparation de votre environnement pour MBAM2.5](preparing-your-environment-for-mbam-25.md)

[Conditions préalables au déploiement de MBAM2.5](mbam-25-deployment-prerequisites.md)



## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 






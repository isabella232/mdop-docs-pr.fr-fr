---
title: Considérations relatives à la sécurité pour MBAM1.0
description: Considérations relatives à la sécurité pour MBAM1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811609"
---
# Considérations relatives à la sécurité pour MBAM1.0


Cette rubrique fournit une vue d’ensemble des comptes et des groupes, des fichiers journaux et d’autres considérations relatives à la sécurité relatives à l’administration et à la surveillance de Microsoft BitLocker (MBAM). Pour plus d’informations, suivez les liens de cet article.

## Considérations générales en matière de sécurité


**Comprenez les risques en matière de sécurité.** Le risque le plus sérieux pour MBAM est qu’il peut être détourné par un utilisateur non autorisé qui peut ensuite reconfigurer le chiffrement BitLocker et obtenir les données de clé de chiffrement BitLocker sur les clients MBAM. Toutefois, la perte de fonctionnalités MBAM pendant une courte période à cause d’une attaque par déni de service n’a pas d’impact négatif.

**Sécurisez vos ordinateurs de façon sécurisée**. La sécurité est incomplète sans sécurité physique. Toute personne disposant d’un accès physique à un serveur MBAM risque d’attaquer la base de clients entière. Tout risque d’attaques physiques potentielles doit être considéré comme présentant un risque élevé et atténué de manière appropriée. Les serveurs MBAM doivent être stockés dans une salle serveur sécurisée avec un accès contrôlé. Sécurisez ces ordinateurs lorsque les administrateurs ne sont pas présents physiquement en faisant en sorte que le système d’exploitation verrouille l’ordinateur ou à l’aide d’un économiseur d’écran sécurisé.

**Appliquez les mises à jour de sécurité les plus récentes à tous les ordinateurs**. Restez informé des nouvelles mises à jour de systèmes d’exploitation, de Microsoft SQL Server et de MBAM en vous abonnant au service de notification de sécurité ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).

**Utiliser des mots de passe forts ou des expressions de passe**. Utilisez toujours des mots de passe forts avec au moins 15 caractères pour tous les comptes d’administrateur MBAM et MBAM. N’utilisez jamais de mots de passe vides. Pour plus d’informations sur les concepts de mot de passe, consultez le livre blanc «mots de passe et stratégies de compte» sur TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Comptes et groupes dans MBAM


Pour la gestion des comptes d’utilisateur, il est recommandé de créer des groupes globaux de domaine et d’y ajouter des comptes d’utilisateurs. Ajoutez ensuite les comptes globaux Domain aux groupes locaux MBAM nécessaires sur les serveurs MBAM.

### Groupes ActiveDirectoryDomainServices

Aucun groupe n’est créé automatiquement lors de la configuration de MBAM. Toutefois, vous devez créer les groupes globaux ActiveDirectoryDomainServices suivants pour gérer les opérations MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom du groupe</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utilisateurs du support technique avancée MBAM</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local de l’assistance technique avancée MBAM créé lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accès aux BD d’audit de conformité MBAM</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local d’audit de compatibilité MBAM qui a été créé lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs de matériel MBAM</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local utilisateurs de matériel MBAM qui a été créé lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateurs du support technique MBAM</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local du support technique MBAM créé lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM de récupération et de BDD matériel</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local de récupération MBAM et de la base de ressources matérielle pour la configuration de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateurs de rapports MBAM</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local utilisateurs de rapports MBAM créés lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrateurs système MBAM</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local Administrateurs de systèmes MBAM qui a été créé lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Exemptions de chiffrement BitLocker</p></td>
<td align="left"><p>Créez ce groupe pour gérer les comptes d’utilisateurs qui doivent être exemptés du chiffrement BitLocker en commençant sur les ordinateurs sur lesquels ils se connectent.</p></td>
</tr>
</tbody>
</table>

 

### Groupes locaux du serveur MBAM

Le programme d’installation d’MBAM crée des groupes locaux pour prendre en charge les opérations MBAM. Vous devez ajouter les groupes globaux ActiveDirectoryDomainServices aux groupes locaux MBAM appropriés pour configurer les autorisations de sécurité et d’accès aux données MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom du groupe</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utilisateurs du support technique avancée MBAM</p></td>
<td align="left"><p>Les membres de ce groupe ont étendu l’accès aux fonctionnalités de support technique de Microsoft BitLocker administration et de la surveillance.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accès aux BD d’audit de conformité MBAM</p></td>
<td align="left"><p>Ce groupe contient les ordinateurs qui ont accès à la base de données d’audit de conformité MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs de matériel MBAM</p></td>
<td align="left"><p>Les membres de ce groupe ont accès à certaines des fonctionnalités de fonctionnalité matérielle de l’administration et de la surveillance de Microsoft BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateurs du support technique MBAM</p></td>
<td align="left"><p>Les membres de ce groupe ont accès à certaines des fonctionnalités de support technique de Microsoft BitLocker administration et de la surveillance.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM de récupération et de BDD matériel</p></td>
<td align="left"><p>Ce groupe contient les ordinateurs qui ont accès à la base de données MBAM et de récupération de la base de données matérielle.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateurs de rapports MBAM</p></td>
<td align="left"><p>Les membres de ce groupe ont accès aux rapports de conformité et d’audit de Microsoft BitLocker administration et de la surveillance.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrateurs système MBAM</p></td>
<td align="left"><p>Les membres de ce groupe ont accès à toutes les fonctionnalités d’administration et de surveillance de Microsoft BitLocker.</p></td>
</tr>
</tbody>
</table>

 

### Compte d’accès aux rapports SSRS

Le compte de service des rapports SQL Server Reporting Services (SSRS) fournit le contexte de sécurité permettant d’exécuter les rapports MBAM disponibles via SSRS. Ce compte est configuré dans le cadre de la configuration de MBAM.

## Fichiers journaux de MBAM


Lors de l’installation d’MBAM, les fichiers journaux d’installation de MBAM suivants sont créés dans le dossier% Temp% de l’utilisateur qui installe le

**Fichiers journaux de configuration de MBAM Server**

<a href="" id="msi-five-random-characters--log"></a>Fichiers MSI de <em> &lt; cinq caractères aléatoires &gt; </em>  
Enregistre les actions effectuées lors de l’installation d’MBAM et de la fonctionnalité de MBAM Server.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Consigne les actions effectuées pour créer la configuration de la base de données d’état de conformité MBAM.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Consigne les actions entreprises pour créer la base de données de récupération et de MBAM de données matérielle.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Consigne les actions effectuées pour créer les connexions SQL Server sur la base de données d’état de conformité d’MBAM et autoriser le service Web d’assistance technique pour les rapports.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Consigne les actions entreprises pour autoriser les services Web dans la base de données pour la récupération de clés et créer des connexions sur la base de données de récupération et de matériel MBAM.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Consigne les actions entreprises pour autoriser les services Web à MBAM la base de données d’état de conformité pour le rapport de conformité.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Consigne les actions entreprises pour autoriser les services Web à MBAM la restauration de la clé matérielle et de la base de données matérielle.

**Remarques**  Pour obtenir d’autres fichiers journaux d’installation d’MBAM, vous devez installer l’administration et la surveillance de BitLocker en utilisant le package **msiexec** et l’option **/l** &lt; emplacement &gt; . Les fichiers journaux sont créés à l’emplacement spécifié.

 

**Fichiers journaux d’installation du client MBAM**

<a href="" id="msi-five-random-characters--log"></a>Fichiers MSI de <em> &lt; cinq caractères aléatoires &gt; </em>  
Enregistre les actions effectuées lors de l’installation du client MBAM.

## Remarques sur les TDE de base de données MBAM


La fonctionnalité de chiffrement de données transparente (TDE) disponible dans SQL Server 2008 est une condition requise d’installation requise pour les instances de base de données qui hébergent les fonctionnalités de base de données MBAM.

Avec TDE, vous pouvez effectuer un chiffrement complet en temps réel au niveau de la base de données. TDE est un choix idéal pour le chiffrement en bloc pour répondre aux exigences réglementaires ou à la sécurité des données d’entreprise. TDE fonctionne au niveau fichier, qui est semblable à deux fonctionnalités Windows: le système de fichiers de chiffrement (EFS) et le chiffrement de lecteur BitLocker, qui chiffrent également les données sur le disque dur. TDE ne remplace pas le chiffrement au niveau de la cellule, EFS ou BitLocker.

Lorsque TDE est activé sur une base de données, toutes les sauvegardes sont chiffrées. Par conséquent, il est nécessaire de veiller à ce que le certificat utilisé pour protéger la clé de chiffrement de la base de données (DEK) soit sauvegardé et entretenu par la sauvegarde de la base de données. Sans certificat, les données ne seront pas lisibles. Sauvegardez le certificat en même temps que la base de données. Chaque sauvegarde de certificat doit comporter deux fichiers. ces deux fichiers doivent être archivés. Il est préférable de les archiver indépendamment du fichier de sauvegarde de base de données à des fins de sécurité.

Pour obtenir un exemple de la façon d’activer TDE pour les instances de base de données MBAM, voir [évaluation d’MBAM 1,0](evaluating-mbam-10.md).

Pour plus d’informations sur TDE dans SQLServer 2008, voir [chiffrement de base de données dans SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).

## Rubriques connexes


[Sécurité et confidentialité de MBAM1.0](security-and-privacy-for-mbam-10.md)

 

 






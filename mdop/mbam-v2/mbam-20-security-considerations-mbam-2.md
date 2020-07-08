---
title: Considérations relatives à la sécurité pour MBAM2.0
description: Considérations relatives à la sécurité pour MBAM2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810241"
---
# Considérations relatives à la sécurité pour MBAM2.0


Cette rubrique fournit une vue d’ensemble sur les comptes et les groupes, les fichiers journaux et les autres considérations relatives à la sécurité relatives à l’administration et à la surveillance de Microsoft BitLocker (MBAM). Pour plus d’informations, suivez les liens fournis dans cet article.

## Considérations générales en matière de sécurité


**Comprenez les risques en matière de sécurité.** Le risque le plus sérieux découlant de l’administration et de la surveillance de BitLocker est que ses fonctionnalités peuvent être piratées par un utilisateur non autorisé qui peut ensuite reconfigurer le chiffrement BitLocker et obtenir les données de clé de chiffrement BitLocker sur les clients MBAM. Toutefois, en raison d’une attaque par déni de service, la perte de fonctionnalité MBAM n’a pas d’impact négatif, contrairement à la messagerie électronique, aux communications réseau, au faible potentiel et à l’alimentation.

**Sécurisez vos ordinateurs de façon sécurisée**. Il n’y a aucune sécurité sans sécurité physique. Un attaquant qui obtient l’accès physique à un serveur MBAM peut peut-être l’utiliser pour attaquer la base de clients tout entière. Toutes les attaques physiques potentielles doivent être considérées comme présentant un risque élevé et atténuées de manière appropriée. Les serveurs MBAM doivent être stockés dans une salle serveur sécurisée avec un accès contrôlé. Sécurisez ces ordinateurs lorsque les administrateurs ne sont pas présents physiquement en faisant en sorte que le système d’exploitation verrouille l’ordinateur ou à l’aide d’un économiseur d’écran sécurisé.

**Appliquez les mises à jour de sécurité les plus récentes à tous les ordinateurs**. Restez informé des nouvelles mises à jour de systèmes d’exploitation, de Microsoft SQL Server et de MBAM en vous abonnant au service de notification de sécurité ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).

**Utiliser des mots de passe forts ou des expressions de passe**. Utilisez toujours des mots de passe forts avec au moins 15 caractères pour tous les comptes d’administrateur MBAM et MBAM. N’utilisez jamais de mots de passe vides. Pour plus d’informations sur les concepts de mot de passe, consultez le livre blanc «mots de passe et stratégies de compte» sur TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).

## Comptes et groupes dans MBAM


La meilleure pratique pour gérer les comptes d’utilisateur consiste à créer des groupes globaux de domaine et à y ajouter des comptes d’utilisateurs. Ajoutez ensuite les comptes globaux Domain aux groupes locaux MBAM nécessaires sur les serveurs MBAM.

### Groupes ActiveDirectoryDomainServices

Aucun groupe Active Directory n’est créé automatiquement lors du processus de configuration de MBAM. Néanmoins, il est recommandé de créer les groupes globaux ActiveDirectoryDomainServices suivants pour gérer les opérations MBAM.

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
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local du support technique MBAM avancée créé lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accès aux BD d’audit de conformité MBAM</p></td>
<td align="left"><p>Créer ce groupe pour gérer les membres du groupe local d’audit de compatibilité MBAM qui a été créé lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs du support technique MBAM</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local du support technique MBAM créés lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM de récupération et de BDD matériel</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local de restauration MBAM et de la base de ressources matérielle pour l’installation d’MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs de rapports MBAM</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe d’utilisateurs de rapports MBAM créés lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Administrateurs système MBAM</p></td>
<td align="left"><p>Créez ce groupe pour gérer les membres du groupe local Administrateurs de systèmes MBAM créés lors de l’installation d’MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exemptions de chiffrement BitLocker</p></td>
<td align="left"><p>Créez ce groupe pour gérer les comptes d’utilisateurs qui doivent être exemptés du chiffrement BitLocker en commençant sur les ordinateurs sur lesquels ils se connectent.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> Groupes locaux du serveur MBAM

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
<td align="left"><p>Les membres de ce groupe ont un accès accru aux fonctionnalités du support technique de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accès aux BD d’audit de conformité MBAM</p></td>
<td align="left"><p>Contient les ordinateurs qui ont accès à la base de données de compatibilité et d’audit MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs du support technique MBAM</p></td>
<td align="left"><p>Les membres de ce groupe ont accès à certaines des fonctionnalités du support technique de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM de récupération et de BDD matériel</p></td>
<td align="left"><p>Contient les ordinateurs qui ont accès à la base de données de récupération MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs de rapports MBAM</p></td>
<td align="left"><p>Les membres de ce groupe ont accès aux rapports de conformité et d’audit de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Administrateurs système MBAM</p></td>
<td align="left"><p>Les membres de ce groupe ont accès à toutes les fonctionnalités de MBAM.</p></td>
</tr>
</tbody>
</table>

 

### Compte de service des rapports SSRS

Le compte de service des rapports SSRS fournit le contexte de sécurité permettant d’exécuter les rapports MBAM disponibles via SSRS. Il est configuré lors de la configuration de MBAM.

Lorsque vous configurez le compte de service des rapports SSRS, spécifiez un compte d’utilisateur de domaine et configurez le mot de passe pour qu’il n’expire jamais.

**Remarques**  Si vous modifiez le nom du compte de service après avoir déployé MBAM, vous devez reconfigurer la source de données de création de rapports pour utiliser les informations d’identification du compte de service. Dans le cas contraire, vous ne pourrez pas accéder au portail du support technique.

 

## <a href="" id="---------mbam-log-files"></a> Fichiers journaux de MBAM


Les fichiers journaux d’installation de MBAM suivants sont créés dans le dossier% Temp% de l’installation de l’utilisateur lors de l’installation d’MBAM:

**Fichiers journaux de configuration de MBAM Server**

<a href="" id="msi-five-random-characters--log"></a>Fichiers MSI de <em> &lt; cinq caractères aléatoires &gt; </em>  
Enregistre les actions effectuées lors de l’installation d’MBAM et de la fonctionnalité de MBAM Server.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Consigne les actions effectuées pour créer la configuration de la base de données d’audit et de conformité MBAM.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Consigne les actions entreprises pour créer la base de données de récupération de MBAM.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Consigne les actions effectuées pour créer les connexions SQL Server sur la base de données de conformité et d’audit MBAM et autoriser le service Web d’assistance technique pour les rapports.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Consigne les actions d’autorisation d’accès aux services Web dans la base de données pour la récupération de clés et de création de connexion dans la base de données de récupération MBAM.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Consigne les actions entreprises pour autoriser les services Web à MBAM la conformité et l’audit de la base de données pour la création de rapports de conformité.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Consigne les actions entreprises pour autoriser les services Web dans la base de données de récupération MBAM pour la récupération de clé.

**Remarques**  Pour obtenir d’autres fichiers journaux d’installation d’MBAM, vous devez installer MBAM à l’aide du package msiexec et de &lt; l' &gt; option/l emplacement. Les fichiers journaux sont créés à l’emplacement spécifié.

 

**Fichiers journaux d’installation du client MBAM**

<a href="" id="msi-five-random-characters--log"></a>Fichiers MSI de <em> &lt; cinq caractères aléatoires &gt; </em>  
Enregistre les actions effectuées lors de l’installation du client MBAM.

## <a href="" id="---------mbam-database-tde-considerations"></a> Remarques sur les TDE de base de données MBAM


La fonction de chiffrement de données (TDE) qui est disponible dans SQL Server est une installation facultative pour les instances de base de données qui hébergent les fonctionnalités de base de données MBAM.

Avec TDE, vous pouvez effectuer un chiffrement complet en temps réel au niveau de la base de données. TDE est le choix le plus optimal pour le chiffrement en bloc pour répondre aux exigences de conformité aux réglementations ou à la sécurité des données d’entreprise. TDE fonctionne au niveau fichier, qui est semblable à deux fonctionnalités Windows: le système de fichiers de chiffrement (EFS) et le chiffrement de lecteur BitLocker, qui chiffrent également les données sur le disque dur. TDE ne remplace pas le chiffrement au niveau de la cellule, EFS ou BitLocker.

Lorsque TDE est activé sur une base de données, toutes les sauvegardes sont chiffrées. Par conséquent, il est nécessaire de veiller à ce que le certificat utilisé pour protéger la clé de chiffrement de la base de données soit sauvegardé et entretenu par la sauvegarde de la base de données. En cas de perte de ce (ou ces certificats), les données ne seront pas lisibles. Sauvegardez le certificat en même temps que la base de données. Chaque sauvegarde de certificat doit comporter deux fichiers. Ces deux fichiers doivent être archivés (idéalement dans le fichier de sauvegarde de la base de données). Vous pouvez également envisager d’utiliser la fonctionnalité de gestion des clés extensible (EKM) (voir gestion de clés extensible) pour stocker et gérer les clés utilisées pour TDE.

Pour obtenir un exemple de la façon d’activer TDE pour les instances de base de données MBAM, voir [évaluation d’MBAM 2,0](evaluating-mbam-20-mbam-2.md).

Pour plus d’informations sur TDE dans SQLServer 2008, voir [chiffrement SQL Server]( https://go.microsoft.com/fwlink/?LinkId=299883).

## Rubriques connexes


[Sécurité et confidentialité de MBAM2.0](security-and-privacy-for-mbam-20-mbam-2.md)

 

 






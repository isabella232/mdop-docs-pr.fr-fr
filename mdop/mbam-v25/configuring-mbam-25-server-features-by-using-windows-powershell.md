---
title: Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell
description: Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809594"
---
# Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell


Après avoir installé le logiciel de serveur MBAM 2,5, vous pouvez utiliser les fonctionnalités de serveur MBAM 2,5 à l’aide d’applets de cmdlet Windows PowerShell ou de l’Assistant Configuration de MBAM Server. Cette rubrique décrit comment configurer MBAM 2,5 à l’aide des cmdlets Windows PowerShell. Pour utiliser l’Assistant à la place, reportez-vous à [Configuration des fonctionnalités du serveur MBAM 2,5](configuring-the-mbam-25-server-features.md).

## Dans cette rubrique


Cette rubrique inclut les informations suivantes sur l’utilisation de Windows PowerShell pour configurer MBAM:

-   [Chargement de l’aide de Windows PowerShell pour MBAM 2,5](#bkmk-load-posh-help)

-   [Comment obtenir de l’aide sur une cmdlet Windows PowerShell MBAM](#bkmk-help-specific-cmdlet)

-   [Configurations que vous pouvez effectuer uniquement avec Windows PowerShell, mais pas avec l’Assistant Configuration de MBAM Server](#bkmk-config-only-posh)

-   [Conditions préalables et configuration requise pour l’utilisation de Windows PowerShell pour configurer les fonctionnalités du serveur MBAM](#bkmk-prereqs-posh-mbamsvr)

-   [Utilisation de Windows PowerShell pour configurer MBAM sur un ordinateur distant](#bkmk-remote-config)

-   [Comptes requis et paramètres de cmdlet Windows PowerShell correspondants](#bkmk-reqd-posh-accts)

Pour plus d’informations sur les applets de applet de passe **Get-MbamBitLockerRecoveryKey** et **Get-MbamTPMOwnerPassword** , qui sont utilisées pour gérer MBAM, voir [utilisation de Windows PowerShell pour gérer MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).

## <a href="" id="bkmk-load-posh-help"></a>Chargement de l’aide de Windows PowerShell pour MBAM 2,5


Pour obtenir la liste des cmdlets Windows PowerShell sur TechNet, voir [automatisation du pack d’optimisation du bureau Microsoft avec Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).

**Pour charger l’aide 2,5 de MBAM pour les applets de cmdlet Windows PowerShell après l’installation du logiciel serveur MBAM**

1.  Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.

2.  Tapez **Update-aide – module Microsoft. mbam**.

## <a href="" id="bkmk-help-specific-cmdlet"></a>Comment obtenir de l’aide sur une cmdlet Windows PowerShell MBAM


L’aide de Windows PowerShell pour MBAM est disponible dans les formats suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Format d’aide de Windows PowerShell</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>À l’invite de commandes Windows PowerShell, tapez <strong> get- </strong> &lt; <em> cmdlet cmdlet.</em>&gt;</p></td>
<td align="left"><p>Pour télécharger les dernières cmdlets Windows PowerShell, suivez les instructions de la section précédente sur le chargement de l’aide de Windows PowerShell pour MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sur TechNet en tant que pages Web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dans le centre de téléchargement en tant que fichier Word. docx</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Dans le centre de téléchargement sous forme de fichier. pdf</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a>Configurations que vous pouvez effectuer uniquement avec Windows PowerShell, mais pas avec l’Assistant Configuration de MBAM Server


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configurations que vous pouvez effectuer uniquement à l’aide de Windows PowerShell</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Installez les services Web sur un autre ordinateur à partir des applications Web.</p></td>
<td align="left"><p>À l’aide de l’Assistant, vous devez installer les services Web et les applications Web sur le même ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Activez des rapports sur un point de services de Reporting autonome sans installer tous les objets de Configuration Manager.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Supprimez tous les objets de Configuration Manager.</p></td>
<td align="left"><p>La suppression des objets entraîne la suppression de toutes les données de conformité de Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Entrez une chaîne de connexion personnalisée pour les bases de données.</p></td>
<td align="left"><p>Exemple: pour configurer les applications Web de manière à utiliser la mise en miroir, vous devez utiliser l' <strong> </strong> applet de connexion Enable-MbamWebApplication pour spécifier la syntaxe de partenaire de basculement appropriée dans la chaîne de connexion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ignorez la validation et configurez une fonctionnalité même si la vérification préalable a échoué.</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

**Remarques**  Vous ne pouvez pas désactiver la base de données MBAM avec une applet de cmdlet Windows PowerShell ou l’Assistant Configuration de MBAM Server. Pour éviter toute suppression accidentelle de vos données de conformité et d’audit, les administrateurs de base de données doivent supprimer manuellement des bases de données.

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a>Conditions préalables et configuration requise pour l’utilisation de Windows PowerShell pour configurer les fonctionnalités du serveur MBAM


Avant de démarrer la configuration, remplissez les conditions préalables suivantes.

**Prérequis liés au compte**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Détails ou informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Créez les comptes nécessaires.</p></td>
<td align="left"><p><strong> </strong> Pour plus d’plus d’rubriques, voir la section comptes requis et les paramètres de cmdlet Windows PowerShell correspondants.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Les comptes d’utilisateurs et les groupes que vous transmettez en tant que paramètres aux cmdlets Windows PowerShell doivent être des comptes valides dans le domaine.</p></td>
<td align="left"><p>Vous ne pouvez pas utiliser les comptes locaux.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spécifiez des comptes au format de niveau inférieur.</p></td>
<td align="left"><p>Exemples:</p>
<p>domainNetBiosName\userdomainNetBiosName\group</p></td>
</tr>
</tbody>
</table>

 

**Prérequis liés aux autorisations**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Détails ou informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Vous devez être administrateur de l’ordinateur local sur lequel vous configurez la fonctionnalité MBAM.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisez une invite de commandes Windows PowerShell avec élévation de privilèges pour exécuter toutes les applets de commande Windows PowerShell.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pour l' <strong> applet de passe Enable-MbamDatabase </strong> uniquement:</p>
<p>Vous devez &quot; créer des autorisations de base de données &quot; sur l’instance de la base de données Microsoft SQL Server cible.</p>
<p>Ce compte d’utilisateur doit être membre du groupe Administrateurs local ou du groupe opérateurs de sauvegarde pour pouvoir inscrire le scripteur du service de cliché instantané de volume MBAM.</p></td>
<td align="left"><p>Par défaut, l’administrateur de base de données ou l’administrateur système dispose de l' &quot; autorisation de création de base de données requise &quot; .</p>
<p></p>
<p>Pour plus d’informations sur le scripteur VSS, voir <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> service de cliché instantané de volume </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pour la <strong> fonctionnalité d’intégration de System Center Configuration Manager </strong> uniquement:</p>
<p>L’utilisateur qui a activé cette fonctionnalité doit avoir les autorisations suivantes dans Configuration Manager:</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de droits dans Configuration Manager</th>
<th align="left">Droits requis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Droits de site Configuration Manager:</p></td>
<td align="left"><p>- Read</p></td>
</tr>
<tr class="even">
<td align="left"><p>Droits de collection de Configuration Manager:</p></td>
<td align="left"><p>- Création-suppression-lecture-modification-déploiement des éléments de configuration</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Droits des éléments de configuration du gestionnaire de configuration:</p></td>
<td align="left"><p>- Création-suppression-lecture</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a>Utilisation de Windows PowerShell pour configurer MBAM sur un ordinateur distant


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Quand utiliser cette fonctionnalité</strong></p></td>
<td align="left"><p>Lorsque vous voulez configurer les fonctionnalités du serveur MBAM 2,5 sur un ordinateur distant. Les applets de commande Windows PowerShell s’exécutent sur un ordinateur et vous configurez celles-ci sur un autre ordinateur distant.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ce que vous devez faire</strong></p></td>
<td align="left"><p>Pour utiliser Windows PowerShell afin de configurer les fonctionnalités du serveur MBAM 2,5 sur un ordinateur distant, vous devez:</p>
<ul>
<li><p>Assurez-vous que le logiciel serveur MBAM 2,5 est installé sur l’ordinateur distant.</p></li>
<li><p>Utilisez le protocole CredSSP (Credential Security Support Provider) pour ouvrir la session Windows PowerShell.</p></li>
<li><p>Activez la gestion à distance de Windows (WinRM). Si vous ne parvenez pas à activer le service WinRM et à le configurer correctement, l' <strong> applet de commande New-PSSession </strong> décrite dans ce tableau affiche une erreur et explique comment résoudre le problème. Pour plus d’informations sur WinRM, voir utilisation de la <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> gestion à distance de Windows </a> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Raison pour laquelle vous devez le faire</strong></p></td>
<td align="left"><p>Ce protocole permet aux cmdlets Windows PowerShell de se connecter à des services de domaine Active Directory (AD FS) en utilisant les informations d’identification d’administrateur de l’utilisateur. Il est possible que vous obteniez une erreur de validation si vous démarrez la session Windows PowerShell sans ce protocole.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Démarrer une session Windows PowerShell avec le protocole CredSSP</strong></p></td>
<td align="left"><p>Tapez le code suivant à l’invite Windows PowerShell:</p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p>Le code qui suit montre un exemple.</p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a>Comptes requis et paramètres de cmdlet Windows PowerShell correspondants


Le tableau suivant décrit les comptes nécessaires à la configuration des fonctionnalités du serveur MBAM 2,5. Il indique également la cmdlet et le paramètre Windows PowerShell correspondants pour lesquels vous devez spécifier le compte lors de la configuration.

Type de paramètre cmdlet (utilisateur ou groupe) Description-MBAMDatabase

AccessAccount

Utilisateur ou groupe

Spécifiez un utilisateur ou un groupe de domaine ayant une autorisation en lecture/écriture sur cette base de données pour permettre aux applications Web d’accéder aux données et aux rapports de cette base de données. Si la valeur est un utilisateur de domaine, le paramètre **WebServiceApplicationPoolCredential** qui est utilisé lors de l’exécution de l’applet de passe **Enable-MbamWebApplication** doit utiliser le même compte d’utilisateur. Si la valeur est un groupe d’utilisateurs du domaine, le compte de domaine utilisé par le paramètre **WebServiceApplicationPoolCredential** doit être membre du groupe.

ReportAccount

Utilisateur ou groupe

Spécifiez un groupe d’utilisateurs ou d’utilisateurs de domaine disposant de droits en lecture seule sur cette base de données pour indiquer à MBAM d’accéder aux données d’audit et de conformité. Si la valeur est un utilisateur de domaine, le paramètre **ComplianceAndAuditDBCredential** de l’applet de passe **Enable-MbamReport** doit utiliser le même compte d’utilisateur. Si la valeur est un groupe d’utilisateurs du domaine, le compte de domaine utilisé par le paramètre **ComplianceAndAuditDBCredential** doit être membre du groupe.

Enable-MbamReport

ComplianceAndAuditDBCredential

Utilisateur

Spécifie les informations d’identification d’administration que l’instance SSRS locale utilise pour se connecter à la base de données de conformité et d’audit MBAM. L’utilisateur de domaine dans les informations d’identification d’administration doit être le même que le compte d’utilisateur utilisé pour le paramètre **ReportAccount** , qui est utilisé lors de l’exécution de l’applet de connexion **Enable-MbamDatabase** . Si un groupe d’utilisateurs de domaine a été utilisé avec le paramètre **ReportAccount** , ce compte doit être membre du groupe.

**Important**  Le compte spécifié dans les informations d’identification d’administration doit disposer de droits d’utilisateur limités pour renforcer la sécurité. Par ailleurs, le mot de passe du compte doit être configuré pour ne pas arriver à expiration.

 

ReportsReadOnlyAccessGroup

Groupe

Spécifie le groupe d’utilisateurs de domaine ayant des autorisations de lecture pour les rapports. Le groupe spécifié doit être le même que celui utilisé pour le paramètre **ReportsReadOnlyAccessGroup** dans l’applet de passe **Enable-MbamWebApplication** .

Enable-MBAMWebApplication

AdvancedHelpdeskAccessGroup

Groupe

Spécifie le groupe utilisateurs du domaine qui a accès à toutes les zones du site Web d’administration et de contrôle, à l’exception de la zone rapports.

HelpdeskAccessGroup

Groupe

Spécifie le groupe utilisateurs du domaine qui a accès aux zones **gérer le module de plateforme sécurisée** et de **récupération des lecteurs** du site Web d’administration et de surveillance.

ReportsReadOnlyAccessGroup

Groupe

Spécifie le groupe utilisateurs du domaine disposant de droits d’accès en lecture à la zone **rapports** du site Web d’administration et de surveillance. Le groupe spécifié doit être le même que celui utilisé pour le paramètre **ReportsReadOnlyAccessGroup** dans l’applet de passe **Enable-MbamReport** .

WebServiceApplicationPoolCredential

Utilisateur

Spécifie l’utilisateur de domaine à utiliser par le pool d’applications pour les applications Web MBAM. Ce compte d’utilisateur doit être le même que celui indiqué dans le paramètre **AccessAccount** de l’applet de passe **Enable-MbamDatabase** . Si un groupe d’utilisateurs de domaine a été utilisé par le paramètre **AccessAccount** lors de l’exécution de l’applet de passe **Enable-MbamDatabase** , l’utilisateur de domaine spécifié ici doit être membre du groupe. Si vous ne spécifiez pas les informations d’identification d’administration, les informations d’identification d’administration spécifiées par une application Web précédemment activée sont utilisées. Toutes les applications Web utilisent la même identité de pool d’applications. S’il est spécifié plusieurs fois, la valeur la plus récemment spécifiée est utilisée.

**Important**  Pour une sécurité accrue, configurez le compte spécifié dans les informations d’identification d’administration sur des droits d’utilisateur limités. Définissez également le mot de passe du compte pour qu’il n’expire jamais. Assurez-vous que le compte intégré IIS \ _IUSRS ou le compte utilisé pour le paramètre **WebServiceApplicationPoolCredential** a été ajouté au paramètre d' **identité d’un client après l’authentification** .

Pour afficher le paramètre de sécurité local, ouvrez l' **éditeur de stratégie de sécurité local**, développez le nœud **stratégies locales** , sélectionnez le nœud d' **attribution de droits d’utilisateur** , puis double-cliquez sur l’option emprunter l’identité d' **un client après authentification** et **ouvrez une session en tant que** paramètres de la stratégie de groupe dans le volet Détails.

 

 




## Rubriques connexes


[Configuration des composants du serveur MBAM2.5](configuring-the-mbam-25-server-features.md)

[Validation de la configuration des composants serveur de MBAM2.5](validating-the-mbam-25-server-feature-configuration.md)

[Utilisation de Windows PowerShell pour administrer MBAM2.5](using-windows-powershell-to-administer-mbam-25.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 






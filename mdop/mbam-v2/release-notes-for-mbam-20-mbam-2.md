---
title: Notes de publication de MBAM2.0
description: Notes de publication de MBAM2.0
author: dansimp
ms.assetid: c3f16cf3-94f2-47ac-b3a4-3dc505c6a8dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d5d3c7d539cf2828d28c1844321bc34ab7736ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811244"
---
# Notes de publication de MBAM2.0


Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.

Lisez attentivement ces notes de publication avant d’installer Microsoft BitLockerAdministration et surveillance (MBAM) 2.0. Ces notes de publication contiennent des informations nécessaires à l’installation d’BitLockerAdministration et de la surveillance 2.0 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents MBAM 2.0, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## <a href="" id="---------mbam-2-0-known-issues"></a> Problèmes connus de MBAM 2.0


Cette section contient des notes de publication pour MBAM 2.0.

### Le champ nom de l’ordinateur risque de ne pas s’afficher dans les rapports sur les détails de la conformité de l’ordinateur BitLocker et de BitLocker entreprise lors de l’exécution de MBAM avec Microsoft System Center Configuration Manager 2007

Le champ nom de l’ordinateur est susceptible d’être vide dans les rapports sur les détails de conformité de l’ordinateur et BitLocker Enterprise lorsque vous utilisez MBAM avec Configuration Manager 2007.

Solution de contournement: aucune.

### Échec de la mise à jour du rapport de conformité d’entreprise après la mise à niveau de l’infrastructure de serveur MBAM autonome

Si vous utilisez la topologie autonome MBAM et que vous effectuez une mise à niveau de l’infrastructure de serveur de la version 1,0 vers 2,0, le rapport de conformité d’entreprise ne peut pas être mis à jour.

Solution de contournement: après la mise à niveau, exécutez le script suivant sur la base de données d’audit et de conformité:

```sql
-- =============================================
-- Script Template
-- =============================================

DECLARE @DatabaseName nvarchar(255);
SET @DatabaseName = DB_NAME()

USE msdb;

DECLARE @JobID BINARY(16)
SELECT @JobID = job_id
FROM msdb.dbo.sysjobs
WHERE (name = N'CreateCache')

if (@JobID IS NOT NULL)
BEGIN
    EXEC dbo.sp_delete_job
         @job_name = N'CreateCache';
END

EXEC dbo.sp_add_job
    @job_name = N'CreateCache',
    @enabled = 1;

EXEC dbo.sp_add_jobstep
     @job_name = N'CreateCache',
     @step_name = N'Copy Data',
     @subsystem = N'TSQL',
     @command = N'EXEC [ComplianceCore].UpdateCache',
     @database_name = @DatabaseName,
     @retry_attempts = 5,
     @retry_interval = 5;


EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 010000,
     @active_end_time = 020000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 070000,
     @active_end_time = 080000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 130000,
     @active_end_time = 140000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1pm';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 190000,
     @active_end_time = 200000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7pm';

EXEC dbo.sp_add_jobserver
     @job_name = N'CreateCache';
```

### Des rapports dans le portail du support technique affichent un avertissement si SSL n’est pas configuré dans SSRS

Si SQL Server Reporting Services (SSRS) n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL des rapports sera définie sur HTTP au lieu de HTTPs lors de l’installation du serveur MBAM. Si vous naviguez jusqu’au portail d’assistance technique et sélectionnez un rapport, le message suivant s’affiche: «seul le contenu sécurisé est affiché».

SOLUTION: pour afficher l’État, cliquez sur **Afficher tout le contenu**. Pour résoudre ce problème, accédez à l’MBAM ordinateur sur lequel SQL Server Reporting Services est installé, exécutez le **Gestionnaire de configuration de Reporting Services**, puis cliquez sur **URL du service Web**. Sélectionnez le certificat SSL approprié pour le serveur, entrez le port SSL approprié (le port par défaut est 443), puis cliquez sur **appliquer**.

### Les instances non par défaut de la base de données du gestionnaire de configuration ne sont pas prises en charge.

MBAM recherche uniquement l’instance par défaut de la base de données du gestionnaire de configuration dans Configuration Manager 2007 et SystemCenter2012 ConfigurationManager. Si vous utilisez une instance autre qu’une instance par défaut, vous ne pouvez pas installer MBAM.

Solution de contournement: aucune.

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a>Cliquer sur «retour» dans le rapport synthèse de conformité peut générer une erreur

Si vous explorez un rapport de synthèse de conformité, puis cliquez sur le lien **retour** dans le rapport SSRS, une erreur peut être levée.

Solution de contournement: aucune.

### Le chiffrement de l’espace utilisé uniquement ne fonctionne pas correctement

Si vous chiffrez un ordinateur pour la première fois après avoir installé le client MBAM, et que vous avez défini un objet de stratégie de groupe pour implémenter l’espace utilisé uniquement pour le chiffrement, MBAM chiffre par erreur le disque entier au lieu de chiffrer uniquement l’espace utilisé du disque. Si un ordinateur est déjà crypté lors de l’installation du client MBAM et si vous avez défini le même objet de stratégie de groupe, le chiffrement fonctionne correctement et chiffre uniquement l’espace disque utilisé sur votre ordinateur.

Solution de contournement: aucune.

### Le niveau de cryptage ne s’affiche pas correctement dans le rapport de conformité ordinateur

Si vous ne définissez pas de niveau de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** la stratégie de groupe force de chiffrement, le rapport de conformité de l’ordinateur dans la topologie d’intégration de Configuration Manager affiche toujours «inconnu» pour la puissance de chiffrement, même si la puissance de chiffrement utilise la valeur par défaut du chiffrement 128. Le rapport affiche le niveau de cryptage approprié si vous définissez un niveau de cryptage spécifique dans l’objet de stratégie de groupe.

Solution de contournement: définissez toujours une clé de chiffrement spécifique dans la **méthode sélectionner le chiffrement de lecteur et** l’objet de stratégie de groupe niveau de mesure du chiffrement.

### Distribution de l’état de conformité par type de lecteur affiche les anciennes données après la mise à jour des éléments de configuration

Après avoir mis à jour les éléments de configuration MBAM dans SystemCenter2012 ConfigurationManager, le graphique barre de distribution de l’état de conformité par type de lecteur sur le tableau de bord de conformité de BitLocker Enterprise affiche des données basées sur des informations provenant de versions antérieures des éléments de configuration.

Solution de contournement: aucune. La modification des éléments de configuration MBAM n’est pas prise en charge et le rapport risque de ne pas apparaître comme prévu.

### La configuration de la sécurité améliorée risque de provoquer l’affichage incorrect des États

Si la configuration de sécurité améliorée d’Internet Explorer (ESC) est activée, un message «accès refusé» peut s’afficher lorsque vous tentez d’afficher des rapports sur le serveur MBAM. Par défaut, la fonction Échap est activée pour protéger le serveur en diminuant son exposition aux attaques potentielles qui peuvent se produire via le contenu Web et les scripts d’application.

SOLUTION: si le message «accès refusé» s’affiche lorsque vous essayez d’afficher des rapports sur le serveur MBAM, vous pouvez définir un objet de stratégie de groupe ou modifier manuellement la valeur par défaut de votre image pour désactiver la configuration de sécurité améliorée. Vous pouvez également afficher les rapports à partir d’un autre ordinateur sur lequel ESC n’est pas activé.

### Échec de l’installation de MBAM Server lors de la mise à niveau de SQL Server 2008 vers SQL Server 2012

Si vous effectuez une mise à niveau de SQL Server 2008 vers SQL Server 2012, puis que vous essayez d’installer la base de données de conformité et d’audit ou la base de données de récupération, l’installation échoue et restaure. L’échec se produit parce que le fichier SQLCMD.exe requis a été supprimé lors de la mise à niveau SQL et qu’il est introuvable par le programme d’installation MBAM. Les lignes du fichier journal MSI risquent de ressembler à ce qui suit:

CA Recovery DB RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript de récupération de la base de connaissances: dbInstance-xxxxxx\\I01RunDbInstallScript récupération de la base de connaissances: sqlScript-C:\\Program Files\\Microsoft\\Microsoft BitLocker administration et Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript de la _Recovery base de connaissances: DefaultFilename-MBAM AUTORITÉ de I01\\MSSQL\\DATA\\RunDbInstallScript de récupération de la base de connaissances: defaultLogPath-K:\\MSSQL\\MSSQL10. CA Recovery DB I01\\MSSQL\\Data\\RunDbInstallScript: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Program Files\\Microsoft\\Microsoft BitLocker and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript de récupération de la base de connaissances: commencez à exécuter l’installation de la base de données de récupération scriptRunDbInstallScript de la base de données de récupération: le fichier journal de récupération de la base de données de récupération se trouve dans C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript exception de l’autorité de certification.

Le programme d’installation de l’application MBAM Server Windows est codé en dur pour trouver le chemin d’accès SQLCMD.exe en consultant la valeur de chaîne Path dans le Registre sous HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup. La clé est toujours présente lors de la migration de SQL Server 2008 vers SQL Server 2012, mais le chemin d’accès référencé par la valeur Data ne contient pas le fichier SQLCMD.exe, car le processus de mise à niveau SQL a supprimé le fichier.

Solution de contournement: renommez de manière temporaire la valeur de chaîne de chemin d’accès à HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup dans **path \ _OLD**, puis exécutez de nouveau le programme d’installation de MBAM Server. Lorsque l’installation est réussie et crée les bases de données dans SQL Server 2012, renommez le **chemin d’accès \ _OLD** valeur **path**.

## Articles sur les correctifs et les Articles de la base de connaissances pour MBAM 2.0


Cette section contient des correctifs et des Articles de la base de connaissances pour MBAM 2.0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Article de la base de connaissances</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>L’installation de Microsoft BitLocker administration et surveillance (MBAM) 2,0 échoue avec les &quot; objets System Center cm déjà installés&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Les utilisateurs ne peuvent pas récupérer la clé de récupération BitLocker à l’aide du portail libre-service MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>Le client MBAM échoue avec l’ID d’événement 4 et le code d’erreur 0x8004100E dans la description de l’événement.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Message d’erreur «erreur serveur dans l’application «/Reports» lorsque vous cliquez sur l’onglet rapports dans MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Erreur lors de l’ouverture des rapports de conformité entreprise ou ordinateur dans MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM entreprise n’a pas effectué de mise à jour</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>L’installation de MBAM sur un contrôleur de domaine n’est pas prise en charge.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Vous recevez le code d’erreur 0x80071a90 lors de l’installation d’MBAM 2.0 dans le cadre d’une intégration autonome ou du gestionnaire de configuration</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM et sécuriser la communication réseau</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>Échec de l’installation d’MBAM 2.0 lors du scénario d’intégration de Configuration Manager avec SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>Échec de la configuration d’MBAM si le SSRS SQL n’est pas configuré correctement</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>Le programme d’installation de MBAM 2,0 est en échec avec &quot; récupération d’erreur dans les paramètres de rôle du serveur Configuration Manager pour &#39;Reporting Services Point&#39;&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>Les rapports d’entreprise MBAM 2.0 ne sont pas actualisés dans la topologie autonome MBAM 2.0 en raison de l’échec du CreateCache de travail SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM entreprise n’a pas effectué de mise à jour</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>MBAM-XX XXXXXXXXX xxxxxxxxx xxxxxxxxx</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>L’enregistrement d’ordinateur est rejeté dans MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[À propos de MBAM2.0](about-mbam-20-mbam-2.md)

 

 






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
# <span data-ttu-id="dc37b-103">Notes de publication de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="dc37b-103">Release Notes for MBAM 2.0</span></span>


<span data-ttu-id="dc37b-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="dc37b-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="dc37b-105">Lisez attentivement ces notes de publication avant d’installer Microsoft BitLockerAdministration et surveillance (MBAM) 2.0.</span><span class="sxs-lookup"><span data-stu-id="dc37b-105">Read these release notes thoroughly before you install Microsoft BitLockerAdministration and Monitoring(MBAM)2.0.</span></span> <span data-ttu-id="dc37b-106">Ces notes de publication contiennent des informations nécessaires à l’installation d’BitLockerAdministration et de la surveillance 2.0 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="dc37b-106">These release notes contain information that is required to successfully install BitLockerAdministration and Monitoring2.0 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="dc37b-107">S’il existe une différence entre ces notes de publication et d’autres documents MBAM 2.0, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="dc37b-107">If there is a difference between these release notes and other MBAM2.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="dc37b-108">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="dc37b-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-known-issues"></a> <span data-ttu-id="dc37b-109">Problèmes connus de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="dc37b-109">MBAM2.0 Known Issues</span></span>


<span data-ttu-id="dc37b-110">Cette section contient des notes de publication pour MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="dc37b-110">This section contains release notes for MBAM2.0.</span></span>

### <span data-ttu-id="dc37b-111">Le champ nom de l’ordinateur risque de ne pas s’afficher dans les rapports sur les détails de la conformité de l’ordinateur BitLocker et de BitLocker entreprise lors de l’exécution de MBAM avec Microsoft System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="dc37b-111">Computer Name field may not appear in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007</span></span>

<span data-ttu-id="dc37b-112">Le champ nom de l’ordinateur est susceptible d’être vide dans les rapports sur les détails de conformité de l’ordinateur et BitLocker Enterprise lorsque vous utilisez MBAM avec Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="dc37b-112">The Computer Name field may be blank in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you use MBAM with Configuration Manager 2007.</span></span>

<span data-ttu-id="dc37b-113">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="dc37b-113">WORKAROUND: None.</span></span>

### <span data-ttu-id="dc37b-114">Échec de la mise à jour du rapport de conformité d’entreprise après la mise à niveau de l’infrastructure de serveur MBAM autonome</span><span class="sxs-lookup"><span data-stu-id="dc37b-114">Enterprise Compliance Report fails to update after you upgrade the Stand-alone MBAM server infrastructure</span></span>

<span data-ttu-id="dc37b-115">Si vous utilisez la topologie autonome MBAM et que vous effectuez une mise à niveau de l’infrastructure de serveur de la version 1,0 vers 2,0, le rapport de conformité d’entreprise ne peut pas être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="dc37b-115">If you are using the MBAM Stand-alone topology, and you upgrade the server infrastructure from version 1.0 to 2.0, the Enterprise Compliance Report fails to update.</span></span>

<span data-ttu-id="dc37b-116">Solution de contournement: après la mise à niveau, exécutez le script suivant sur la base de données d’audit et de conformité:</span><span class="sxs-lookup"><span data-stu-id="dc37b-116">WORKAROUND: After the upgrade, run the following script on the Compliance and Audit Database:</span></span>

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

### <span data-ttu-id="dc37b-117">Des rapports dans le portail du support technique affichent un avertissement si SSL n’est pas configuré dans SSRS</span><span class="sxs-lookup"><span data-stu-id="dc37b-117">Reports in the Help Desk Portal display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="dc37b-118">Si SQL Server Reporting Services (SSRS) n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL des rapports sera définie sur HTTP au lieu de HTTPs lors de l’installation du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc37b-118">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="dc37b-119">Si vous naviguez jusqu’au portail d’assistance technique et sélectionnez un rapport, le message suivant s’affiche: «seul le contenu sécurisé est affiché».</span><span class="sxs-lookup"><span data-stu-id="dc37b-119">If you then browse to the Help Desk Portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="dc37b-120">SOLUTION: pour afficher l’État, cliquez sur **Afficher tout le contenu**.</span><span class="sxs-lookup"><span data-stu-id="dc37b-120">WORKAROUND: To show the report, click **Show All Content**.</span></span> <span data-ttu-id="dc37b-121">Pour résoudre ce problème, accédez à l’MBAM ordinateur sur lequel SQL Server Reporting Services est installé, exécutez le **Gestionnaire de configuration de Reporting Services**, puis cliquez sur **URL du service Web**.</span><span class="sxs-lookup"><span data-stu-id="dc37b-121">To address this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="dc37b-122">Sélectionnez le certificat SSL approprié pour le serveur, entrez le port SSL approprié (le port par défaut est 443), puis cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="dc37b-122">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="dc37b-123">Les instances non par défaut de la base de données du gestionnaire de configuration ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="dc37b-123">Non-default instances of the Configuration Manager database are not supported</span></span>

<span data-ttu-id="dc37b-124">MBAM recherche uniquement l’instance par défaut de la base de données du gestionnaire de configuration dans Configuration Manager 2007 et SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="dc37b-124">MBAM looks only for the default instance of the Configuration Manager database in Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="dc37b-125">Si vous utilisez une instance autre qu’une instance par défaut, vous ne pouvez pas installer MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc37b-125">If you use a non-default instance, you cannot install MBAM.</span></span>

<span data-ttu-id="dc37b-126">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="dc37b-126">WORKAROUND: None.</span></span>

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a><span data-ttu-id="dc37b-127">Cliquer sur «retour» dans le rapport synthèse de conformité peut générer une erreur</span><span class="sxs-lookup"><span data-stu-id="dc37b-127">Clicking “Back” in the Compliance Summary report might throw an error</span></span>

<span data-ttu-id="dc37b-128">Si vous explorez un rapport de synthèse de conformité, puis cliquez sur le lien **retour** dans le rapport SSRS, une erreur peut être levée.</span><span class="sxs-lookup"><span data-stu-id="dc37b-128">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="dc37b-129">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="dc37b-129">WORKAROUND: None.</span></span>

### <span data-ttu-id="dc37b-130">Le chiffrement de l’espace utilisé uniquement ne fonctionne pas correctement</span><span class="sxs-lookup"><span data-stu-id="dc37b-130">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="dc37b-131">Si vous chiffrez un ordinateur pour la première fois après avoir installé le client MBAM, et que vous avez défini un objet de stratégie de groupe pour implémenter l’espace utilisé uniquement pour le chiffrement, MBAM chiffre par erreur le disque entier au lieu de chiffrer uniquement l’espace utilisé du disque.</span><span class="sxs-lookup"><span data-stu-id="dc37b-131">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="dc37b-132">Si un ordinateur est déjà crypté lors de l’installation du client MBAM et si vous avez défini le même objet de stratégie de groupe, le chiffrement fonctionne correctement et chiffre uniquement l’espace disque utilisé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dc37b-132">If a computer is already encrypted when you install the MBAM Client, and you have set the same Group Policy Object, the encryption works correctly and encrypts only the used disk space on your computer.</span></span>

<span data-ttu-id="dc37b-133">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="dc37b-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="dc37b-134">Le niveau de cryptage ne s’affiche pas correctement dans le rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="dc37b-134">Cipher strength displays incorrectly on the Computer Compliance report</span></span>

<span data-ttu-id="dc37b-135">Si vous ne définissez pas de niveau de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** la stratégie de groupe force de chiffrement, le rapport de conformité de l’ordinateur dans la topologie d’intégration de Configuration Manager affiche toujours «inconnu» pour la puissance de chiffrement, même si la puissance de chiffrement utilise la valeur par défaut du chiffrement 128.</span><span class="sxs-lookup"><span data-stu-id="dc37b-135">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager Integration topology always displays “unknown” for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="dc37b-136">Le rapport affiche le niveau de cryptage approprié si vous définissez un niveau de cryptage spécifique dans l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="dc37b-136">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="dc37b-137">Solution de contournement: définissez toujours une clé de chiffrement spécifique dans la **méthode sélectionner le chiffrement de lecteur et** l’objet de stratégie de groupe niveau de mesure du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="dc37b-137">WORKAROUND: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="dc37b-138">Distribution de l’état de conformité par type de lecteur affiche les anciennes données après la mise à jour des éléments de configuration</span><span class="sxs-lookup"><span data-stu-id="dc37b-138">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="dc37b-139">Après avoir mis à jour les éléments de configuration MBAM dans SystemCenter2012 ConfigurationManager, le graphique barre de distribution de l’état de conformité par type de lecteur sur le tableau de bord de conformité de BitLocker Enterprise affiche des données basées sur des informations provenant de versions antérieures des éléments de configuration.</span><span class="sxs-lookup"><span data-stu-id="dc37b-139">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="dc37b-140">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="dc37b-140">WORKAROUND: None.</span></span> <span data-ttu-id="dc37b-141">La modification des éléments de configuration MBAM n’est pas prise en charge et le rapport risque de ne pas apparaître comme prévu.</span><span class="sxs-lookup"><span data-stu-id="dc37b-141">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="dc37b-142">La configuration de la sécurité améliorée risque de provoquer l’affichage incorrect des États</span><span class="sxs-lookup"><span data-stu-id="dc37b-142">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="dc37b-143">Si la configuration de sécurité améliorée d’Internet Explorer (ESC) est activée, un message «accès refusé» peut s’afficher lorsque vous tentez d’afficher des rapports sur le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc37b-143">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an “Access Denied” message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="dc37b-144">Par défaut, la fonction Échap est activée pour protéger le serveur en diminuant son exposition aux attaques potentielles qui peuvent se produire via le contenu Web et les scripts d’application.</span><span class="sxs-lookup"><span data-stu-id="dc37b-144">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="dc37b-145">SOLUTION: si le message «accès refusé» s’affiche lorsque vous essayez d’afficher des rapports sur le serveur MBAM, vous pouvez définir un objet de stratégie de groupe ou modifier manuellement la valeur par défaut de votre image pour désactiver la configuration de sécurité améliorée.</span><span class="sxs-lookup"><span data-stu-id="dc37b-145">WORKAROUND: If the “Access Denied” message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="dc37b-146">Vous pouvez également afficher les rapports à partir d’un autre ordinateur sur lequel ESC n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="dc37b-146">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="dc37b-147">Échec de l’installation de MBAM Server lors de la mise à niveau de SQL Server 2008 vers SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc37b-147">MBAM Server installation fails when you upgrade from SQL Server 2008 to SQL Server 2012</span></span>

<span data-ttu-id="dc37b-148">Si vous effectuez une mise à niveau de SQL Server 2008 vers SQL Server 2012, puis que vous essayez d’installer la base de données de conformité et d’audit ou la base de données de récupération, l’installation échoue et restaure.</span><span class="sxs-lookup"><span data-stu-id="dc37b-148">If you upgrade from SQL Server 2008 to SQL Server 2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="dc37b-149">L’échec se produit parce que le fichier SQLCMD.exe requis a été supprimé lors de la mise à niveau SQL et qu’il est introuvable par le programme d’installation MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc37b-149">The failure occurs because the required SQLCMD.exe file was removed during the SQL upgrade and cannot be found by the MBAM installer.</span></span> <span data-ttu-id="dc37b-150">Les lignes du fichier journal MSI risquent de ressembler à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="dc37b-150">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="dc37b-151">CA Recovery DB RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript de récupération de la base de connaissances: dbInstance-xxxxxx\\I01RunDbInstallScript récupération de la base de connaissances: sqlScript-C:\\Program Files\\Microsoft\\Microsoft BitLocker administration et Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript de la _Recovery base de connaissances: DefaultFilename-MBAM AUTORITÉ de I01\\MSSQL\\DATA\\RunDbInstallScript de récupération de la base de connaissances: defaultLogPath-K:\\MSSQL\\MSSQL10. CA Recovery DB I01\\MSSQL\\Data\\RunDbInstallScript: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Program Files\\Microsoft\\Microsoft BitLocker and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript de récupération de la base de connaissances: commencez à exécuter l’installation de la base de données de récupération scriptRunDbInstallScript de la base de données de récupération: le fichier journal de récupération de la base de données de récupération se trouve dans C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript exception de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="dc37b-151">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="dc37b-152">Le programme d’installation de l’application MBAM Server Windows est codé en dur pour trouver le chemin d’accès SQLCMD.exe en consultant la valeur de chaîne Path dans le Registre sous HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="dc37b-152">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="dc37b-153">La clé est toujours présente lors de la migration de SQL Server 2008 vers SQL Server 2012, mais le chemin d’accès référencé par la valeur Data ne contient pas le fichier SQLCMD.exe, car le processus de mise à niveau SQL a supprimé le fichier.</span><span class="sxs-lookup"><span data-stu-id="dc37b-153">The key is still present during the migration from SQL Server 2008 to SQL Server 2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQL upgrade process removed the file.</span></span>

<span data-ttu-id="dc37b-154">Solution de contournement: renommez de manière temporaire la valeur de chaîne de chemin d’accès à HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup dans **path \ _OLD**, puis exécutez de nouveau le programme d’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="dc37b-154">WORKAROUND: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path string value to **Path\_old**, and then re-run the MBAM Server Windows Installer.</span></span> <span data-ttu-id="dc37b-155">Lorsque l’installation est réussie et crée les bases de données dans SQL Server 2012, renommez le **chemin d’accès \ _OLD** valeur **path**.</span><span class="sxs-lookup"><span data-stu-id="dc37b-155">When the installation completes successfully and creates the databases in SQL Server 2012, rename the **Path\_old** value to **Path**.</span></span>

## <span data-ttu-id="dc37b-156">Articles sur les correctifs et les Articles de la base de connaissances pour MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="dc37b-156">Hotfixes and Knowledge Base articles for MBAM2.0</span></span>


<span data-ttu-id="dc37b-157">Cette section contient des correctifs et des Articles de la base de connaissances pour MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="dc37b-157">This section contains hotfixes and KB articles for MBAM2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="dc37b-158">Article de la base de connaissances</span><span class="sxs-lookup"><span data-stu-id="dc37b-158">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="dc37b-159">Title</span><span class="sxs-lookup"><span data-stu-id="dc37b-159">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="dc37b-160">Link</span><span class="sxs-lookup"><span data-stu-id="dc37b-160">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc37b-161">2831166</span><span class="sxs-lookup"><span data-stu-id="dc37b-161">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-162">L’installation de Microsoft BitLocker administration et surveillance (MBAM) 2,0 échoue avec les &quot; objets System Center cm déjà installés&quot;</span><span class="sxs-lookup"><span data-stu-id="dc37b-162">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="dc37b-163">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-163">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc37b-164">2870849</span><span class="sxs-lookup"><span data-stu-id="dc37b-164">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-165">Les utilisateurs ne peuvent pas récupérer la clé de récupération BitLocker à l’aide du portail libre-service MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="dc37b-165">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="dc37b-166">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-166">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc37b-167">2756402</span><span class="sxs-lookup"><span data-stu-id="dc37b-167">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-168">Le client MBAM échoue avec l’ID d’événement 4 et le code d’erreur 0x8004100E dans la description de l’événement.</span><span class="sxs-lookup"><span data-stu-id="dc37b-168">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="dc37b-169">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-169">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc37b-170">2620287</span><span class="sxs-lookup"><span data-stu-id="dc37b-170">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-171">Message d’erreur «erreur serveur dans l’application «/Reports» lorsque vous cliquez sur l’onglet rapports dans MBAM</span><span class="sxs-lookup"><span data-stu-id="dc37b-171">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="dc37b-172">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-172">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc37b-173">2639518</span><span class="sxs-lookup"><span data-stu-id="dc37b-173">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-174">Erreur lors de l’ouverture des rapports de conformité entreprise ou ordinateur dans MBAM</span><span class="sxs-lookup"><span data-stu-id="dc37b-174">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="dc37b-175">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-175">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc37b-176">2620269</span><span class="sxs-lookup"><span data-stu-id="dc37b-176">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-177">MBAM entreprise n’a pas effectué de mise à jour</span><span class="sxs-lookup"><span data-stu-id="dc37b-177">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="dc37b-178">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-178">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc37b-179">2712461</span><span class="sxs-lookup"><span data-stu-id="dc37b-179">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-180">L’installation de MBAM sur un contrôleur de domaine n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dc37b-180">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="dc37b-181">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-181">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc37b-182">2876732</span><span class="sxs-lookup"><span data-stu-id="dc37b-182">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-183">Vous recevez le code d’erreur 0x80071a90 lors de l’installation d’MBAM 2.0 dans le cadre d’une intégration autonome ou du gestionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="dc37b-183">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="dc37b-184">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-184">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc37b-185">2754259</span><span class="sxs-lookup"><span data-stu-id="dc37b-185">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-186">MBAM et sécuriser la communication réseau</span><span class="sxs-lookup"><span data-stu-id="dc37b-186">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="dc37b-187">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-187">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc37b-188">2870842</span><span class="sxs-lookup"><span data-stu-id="dc37b-188">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-189">Échec de l’installation d’MBAM 2.0 lors du scénario d’intégration de Configuration Manager avec SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc37b-189">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="dc37b-190">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-190">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc37b-191">2668533</span><span class="sxs-lookup"><span data-stu-id="dc37b-191">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-192">Échec de la configuration d’MBAM si le SSRS SQL n’est pas configuré correctement</span><span class="sxs-lookup"><span data-stu-id="dc37b-192">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="dc37b-193">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-193">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc37b-194">2870847</span><span class="sxs-lookup"><span data-stu-id="dc37b-194">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-195">Le programme d’installation de MBAM 2,0 est en échec avec &quot; récupération d’erreur dans les paramètres de rôle du serveur Configuration Manager pour &#39;Reporting Services Point&#39;&quot;</span><span class="sxs-lookup"><span data-stu-id="dc37b-195">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="dc37b-196">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-196">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc37b-197">2870839</span><span class="sxs-lookup"><span data-stu-id="dc37b-197">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-198">Les rapports d’entreprise MBAM 2.0 ne sont pas actualisés dans la topologie autonome MBAM 2.0 en raison de l’échec du CreateCache de travail SQL</span><span class="sxs-lookup"><span data-stu-id="dc37b-198">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="dc37b-199">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-199">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc37b-200">2620269</span><span class="sxs-lookup"><span data-stu-id="dc37b-200">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-201">MBAM entreprise n’a pas effectué de mise à jour</span><span class="sxs-lookup"><span data-stu-id="dc37b-201">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="dc37b-202">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-202">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc37b-203">2935997</span><span class="sxs-lookup"><span data-stu-id="dc37b-203">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-204">MBAM-XX XXXXXXXXX xxxxxxxxx xxxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="dc37b-204">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="dc37b-205">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-205">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc37b-206">2612822</span><span class="sxs-lookup"><span data-stu-id="dc37b-206">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc37b-207">L’enregistrement d’ordinateur est rejeté dans MBAM</span><span class="sxs-lookup"><span data-stu-id="dc37b-207">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="dc37b-208">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="dc37b-208">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="dc37b-209">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc37b-209">Related topics</span></span>


[<span data-ttu-id="dc37b-210">À propos de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="dc37b-210">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

 

 






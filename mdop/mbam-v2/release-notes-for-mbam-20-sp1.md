---
title: Notes de publication de MBAM2.0 SP1
description: Notes de publication de MBAM2.0 SP1
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811243"
---
# <span data-ttu-id="4da70-103">Notes de publication de MBAM2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="4da70-103">Release Notes for MBAM 2.0 SP1</span></span>


<span data-ttu-id="4da70-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="4da70-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="4da70-105">Lisez attentivement ces notes de publication avant d’installer Microsoft BitLocker administration et l’analyse (MBAM) 2,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4da70-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="4da70-106">Ces notes de publication contiennent des informations nécessaires pour l’installation réussie de l’administration et de la surveillance de 2,0 SP1 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="4da70-106">These release notes contain information that is required to successfully install BitLocker Administration and Monitoring 2.0 SP1, and they contain information that is not available in the product documentation.</span></span> <span data-ttu-id="4da70-107">S’il existe une différence entre ces notes de publication et d’autres documents MBAM 2,0 SP1, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="4da70-107">If there is a difference between these release notes and other MBAM 2.0 SP1 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="4da70-108">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="4da70-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> <span data-ttu-id="4da70-109">Problèmes connus de MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="4da70-109">MBAM 2.0 SP1 known issues</span></span>


<span data-ttu-id="4da70-110">Cette section contient des problèmes connus de MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="4da70-110">This section contains known issues for MBAM 2.0 SP1.</span></span>

### <span data-ttu-id="4da70-111">La mise à niveau d’MBAM avec la topologie intégrée de Configuration Manager vers MBAM 2,0 SP1 nécessite une suppression manuelle des objets Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4da70-111">Upgrade of MBAM with Configuration Manager Integrated topology to MBAM 2.0 SP1 requires manual removal of Configuration Manager objects</span></span>

<span data-ttu-id="4da70-112">Si vous utilisez MBAM avec Configuration Manager et que vous souhaitez effectuer une mise à niveau vers MBAM 2,0 SP1, vous devez supprimer manuellement tous les objets de Configuration Manager installés dans Configuration Manager dans le cadre de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="4da70-112">If you are using MBAM with Configuration Manager, and you want to upgrade to MBAM 2.0 SP1, you must manually remove all of the Configuration Manager objects that were installed into Configuration Manager as a part of the MBAM installation.</span></span> <span data-ttu-id="4da70-113">Les objets que vous devez supprimer manuellement sont les rapports MBAM, la collection MBAM d’ordinateurs pris en charge et la ligne de base de configuration de protection de BitLocker ainsi que les éléments de configuration associés.</span><span class="sxs-lookup"><span data-stu-id="4da70-113">The objects that you must manually remove are the MBAM reports, MBAM Supported Computers collection, and the BitLocker Protection Configuration Baseline and its associated configuration items.</span></span>

<span data-ttu-id="4da70-114">**Solution de contournement**: mettez à niveau les objets de Configuration Manager en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="4da70-114">**Workaround**: Upgrade the Configuration Manager objects by completing the following steps:</span></span>

1.  <span data-ttu-id="4da70-115">Sauvegardez des données de conformité existantes dans un fichier externe, comme décrit dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4da70-115">Back up existing compliance data to an external file, as described in the following steps.</span></span>

    <span data-ttu-id="4da70-116">**Remarques**  Toutes les données de conformité BitLocker existantes seront supprimées lorsque vous supprimez le planning de référence existant dans Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4da70-116">**Note** All existing BitLocker compliance data will be deleted when you delete the existing baseline in Configuration Manager.</span></span> <span data-ttu-id="4da70-117">Les données seront régénérées dans le temps, mais nous vous conseillons d’enregistrer une copie des données dans le cas où vous aurez besoin des informations de conformité d’un ordinateur particulier avant la régénération des données de conformité.</span><span class="sxs-lookup"><span data-stu-id="4da70-117">The data will be regenerated over time, but it is recommended that you save a copy of the data in case you need the compliance data for a particular computer before the compliance data has been regenerated.</span></span>

     

    1.  <span data-ttu-id="4da70-118">Pour enregistrer les données de conformité BitLocker historiques, ouvrez le rapport **Détails de conformité de BitLocker Enterprise** .</span><span class="sxs-lookup"><span data-stu-id="4da70-118">To save historical BitLocker compliance data, open the **BitLocker Enterprise Compliance Details** Report.</span></span>

    2.  <span data-ttu-id="4da70-119">Cliquez sur l’icône **Enregistrer** dans le rapport et sélectionnez **Excel**.</span><span class="sxs-lookup"><span data-stu-id="4da70-119">Click the **Save** icon in the report and select **Excel**.</span></span>

        <span data-ttu-id="4da70-120">Le rapport enregistré contient des données telles que le nom de l’ordinateur, le nom de domaine, l’état de conformité, l’exemption, les utilisateurs de l’appareil, les détails de l’état de la conformité et la date/heure du dernier contact.</span><span class="sxs-lookup"><span data-stu-id="4da70-120">The saved report will contain data such as the computer name, domain name, compliance status, exemption, device users, compliance status details, and last contact date/time.</span></span> <span data-ttu-id="4da70-121">Des informations, telles que les informations détaillées sur le volume et la force de cryptage, ne sont pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="4da70-121">Some information, such as detailed volume information and encryption strength, are not saved.</span></span>

2.  <span data-ttu-id="4da70-122">Désinstaller **MBAM** du serveur à l’aide du programme d’installation de **MBAM** .</span><span class="sxs-lookup"><span data-stu-id="4da70-122">Uninstall **MBAM** from the server by using the **MBAM** installer.</span></span>

3.  <span data-ttu-id="4da70-123">Supprimez manuellement les objets suivants de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="4da70-123">Manually delete the following objects from Configuration Manager:</span></span>

    -   <span data-ttu-id="4da70-124">Collection d’ordinateurs pris en charge par MBAM</span><span class="sxs-lookup"><span data-stu-id="4da70-124">MBAM Supported Computers collection</span></span>

    -   <span data-ttu-id="4da70-125">Baseline protection de BitLocker</span><span class="sxs-lookup"><span data-stu-id="4da70-125">BitLocker Protection baseline</span></span>

    -   <span data-ttu-id="4da70-126">Élément de configuration de protection de lecteur du système d’exploitation BitLocker</span><span class="sxs-lookup"><span data-stu-id="4da70-126">BitLocker Operating System Drive Protection configuration item</span></span>

    -   <span data-ttu-id="4da70-127">Élément de configuration de protection de périphériques de données fixes BitLocker</span><span class="sxs-lookup"><span data-stu-id="4da70-127">BitLocker Fixed Data Drives Protection configuration item</span></span>

4.  <span data-ttu-id="4da70-128">Supprimez manuellement le dossier MBAM rapports dans le site SQL Server Reporting Services Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4da70-128">Manually delete the MBAM Reports folder in the Configuration Manager SQL Server Reporting Services site.</span></span> <span data-ttu-id="4da70-129">Pour cela, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="4da70-129">To do this:</span></span>

    1.  <span data-ttu-id="4da70-130">Utilisez Internet Explorer pour accéder au point Reporting Services, par exemple http:// &lt; yourcmserver &gt; /reports.</span><span class="sxs-lookup"><span data-stu-id="4da70-130">Use Internet Explorer to browse to the reporting services point, for example, http://&lt;yourcmserver&gt;/reports.</span></span>

    2.  <span data-ttu-id="4da70-131">Cliquez sur le lien correspondant au code du site gestionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="4da70-131">Click the appropriate Configuration Manager site code link.</span></span>

    3.  <span data-ttu-id="4da70-132">Supprimez le dossier MBAM.</span><span class="sxs-lookup"><span data-stu-id="4da70-132">Delete the MBAM folder.</span></span>

5.  <span data-ttu-id="4da70-133">Utilisez le programme d’installation de MBAM Server pour réinstaller les objets d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4da70-133">Use the MBAM Server installer to reinstall the Configuration Manager Integration objects.</span></span> <span data-ttu-id="4da70-134">Les ordinateurs client vont commencer à télécharger les données de compatibilité de BitLocker au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="4da70-134">The client computers will begin to upload BitLocker compliance data again over time.</span></span>

### <span data-ttu-id="4da70-135">Le bouton d’envoi du portail libre-service ne fonctionne pas dans Internet Explorer10</span><span class="sxs-lookup"><span data-stu-id="4da70-135">Submit button on Self-Service Portal does not work in Internet Explorer10</span></span>

<span data-ttu-id="4da70-136">Lorsque vous utilisez Internet Explorer10 pour accéder au site Web d’administration et de contrôle, le bouton d' **envoi** sur le site Web ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="4da70-136">When you use Internet Explorer10 to access the Administration and Monitoring Website, the **Submit** button on the website does not work.</span></span>

<span data-ttu-id="4da70-137">**Solution**: sur le serveur sur lequel vous avez installé le site Web d’administration et de surveillance, installez le [correctif pour les fichiers de définition de navigateur ASP.net](https://go.microsoft.com/fwlink/?LinkId=317798).</span><span class="sxs-lookup"><span data-stu-id="4da70-137">**Workaround**: On the server where you installed the Administration and Monitoring Website, install [Hotfix for ASP.NET browser definition files](https://go.microsoft.com/fwlink/?LinkId=317798).</span></span>

### <span data-ttu-id="4da70-138">Les noms de domaines internationaux ne sont pas pris en charge</span><span class="sxs-lookup"><span data-stu-id="4da70-138">International domain names are not supported</span></span>

<span data-ttu-id="4da70-139">MBAM 2,0 SP1 ne prend pas en charge les noms de domaines internationaux.</span><span class="sxs-lookup"><span data-stu-id="4da70-139">MBAM 2.0 SP1 does not support international domain names.</span></span>

<span data-ttu-id="4da70-140">**Solution de contournement**: aucune.</span><span class="sxs-lookup"><span data-stu-id="4da70-140">**Workaround**: None.</span></span>

### <span data-ttu-id="4da70-141">Les rapports figurant sur le site Web d’administration et de surveillance affichent un avertissement si SSL n’est pas configuré dans SSRS</span><span class="sxs-lookup"><span data-stu-id="4da70-141">Reports in the Administration and Monitoring website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="4da70-142">Si SQLServer Reporting Services (SSRS) n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL des rapports sera définie sur HTTP au lieu de HTTPs lors de l’installation du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="4da70-142">If SQLServer Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="4da70-143">Si vous naviguez jusqu’au site Web Administration et surveillance et sélectionnez un rapport, le message suivant s’affiche: «seul le contenu sécurisé est affiché».</span><span class="sxs-lookup"><span data-stu-id="4da70-143">If you then browse to the Administration and Monitoring website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="4da70-144">**Solution**: pour résoudre ce problème, configurez SSL dans le **Gestionnaire de configuration Reporting Services** sur le serveur MBAM sur lequel SqlServer Reporting Services est installé.</span><span class="sxs-lookup"><span data-stu-id="4da70-144">**Workaround**: To correct this issue, configure SSL in **Reporting Services Configuration Manager** on the MBAM server where SQLServer Reporting Services is installed.</span></span> <span data-ttu-id="4da70-145">Désinstallez, puis réinstallez le site Web du serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="4da70-145">Uninstall and then reinstall the Administration and Monitoring Server website.</span></span>

### <span data-ttu-id="4da70-146">Cliquer sur retour dans le rapport synthèse de conformité peut générer une erreur</span><span class="sxs-lookup"><span data-stu-id="4da70-146">Clicking Back in the Compliance Summary report might create an error</span></span>

<span data-ttu-id="4da70-147">Si vous explorez un rapport de synthèse de conformité, puis cliquez sur le lien **retour** dans le rapport SSRS, une erreur peut se produire.</span><span class="sxs-lookup"><span data-stu-id="4da70-147">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might occur.</span></span>

<span data-ttu-id="4da70-148">**Solution de contournement**: aucune.</span><span class="sxs-lookup"><span data-stu-id="4da70-148">**Workaround**: None.</span></span>

### <span data-ttu-id="4da70-149">Le chiffrement de l’espace utilisé uniquement ne fonctionne pas correctement</span><span class="sxs-lookup"><span data-stu-id="4da70-149">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="4da70-150">Si vous chiffrez un ordinateur pour la première fois après avoir installé le client MBAM, et que vous avez défini un objet de stratégie de groupe pour implémenter l’espace utilisé uniquement pour le chiffrement, MBAM chiffre par erreur le disque entier au lieu de chiffrer uniquement l’espace utilisé du disque.</span><span class="sxs-lookup"><span data-stu-id="4da70-150">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only Encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="4da70-151">Si un ordinateur est déjà chiffré avec un chiffrement de l’espace utilisé uniquement avant d’installer le client MBAM, et que vous avez défini l’espace utilisé uniquement pour le chiffrement de l’objet de stratégie de groupe, MBAM reconnaît ce paramètre et signale correctement le chiffrement dans les rapports de conformité.</span><span class="sxs-lookup"><span data-stu-id="4da70-151">If a computer is already encrypted with Used Space Only Encryption before you install the MBAM Client, and you have set the same Used Space Only Encryption Group Policy Object, MBAM recognizes the setting and reports the encryption correctly in the compliance reports.</span></span>

<span data-ttu-id="4da70-152">**Solution de contournement**: aucune.</span><span class="sxs-lookup"><span data-stu-id="4da70-152">**Workaround**: None.</span></span>

### <span data-ttu-id="4da70-153">Le niveau de cryptage ne s’affiche pas correctement dans le rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="4da70-153">Cipher strength displays incorrectly in the Computer Compliance report</span></span>

<span data-ttu-id="4da70-154">Si vous ne définissez pas de niveau de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** la stratégie de groupe force de chiffrement, le rapport de conformité de l’ordinateur dans la topologie intégrée de Configuration Manager s’affiche toujours comme **inconnu** pour la puissance de chiffrement, même si la puissance de chiffrement utilise la valeur par défaut du chiffrement de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="4da70-154">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager integrated topology always displays **Unknown** for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="4da70-155">Le rapport affiche le niveau de cryptage approprié si vous définissez un niveau de cryptage spécifique dans l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4da70-155">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="4da70-156">**Solution de contournement**: définissez toujours une clé de chiffrement spécifique dans la **méthode sélectionner le chiffrement de lecteur et** l’objet de stratégie de groupe niveau de mesure du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="4da70-156">**Workaround**: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="4da70-157">Distribution de l’état de conformité par type de lecteur affiche les anciennes données après la mise à jour des éléments de configuration</span><span class="sxs-lookup"><span data-stu-id="4da70-157">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="4da70-158">Après avoir mis à jour les éléments de configuration MBAM dans SystemCenter2012 ConfigurationManager, le graphique barre de distribution de l’état de conformité par type de lecteur sur le tableau de bord de conformité de BitLocker Enterprise affiche des données basées sur des informations provenant de versions antérieures des éléments de configuration.</span><span class="sxs-lookup"><span data-stu-id="4da70-158">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="4da70-159">**Solution de contournement**: aucune.</span><span class="sxs-lookup"><span data-stu-id="4da70-159">**Workaround**: None.</span></span> <span data-ttu-id="4da70-160">La modification des éléments de configuration MBAM n’est pas prise en charge et le rapport risque de ne pas apparaître comme prévu.</span><span class="sxs-lookup"><span data-stu-id="4da70-160">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="4da70-161">La configuration de la sécurité améliorée risque de provoquer l’affichage incorrect des États</span><span class="sxs-lookup"><span data-stu-id="4da70-161">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="4da70-162">Si la configuration de sécurité améliorée d’Internet Explorer (ESC) est activée, un message d' **accès refusé** peut s’afficher lorsque vous tentez d’afficher des rapports sur le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="4da70-162">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an **Access Denied** message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="4da70-163">Par défaut, la configuration de la sécurité améliorée est activée pour protéger le serveur en diminuant l’exposition du serveur aux attaques potentielles qui peuvent se produire via le contenu Web et les scripts d’application.</span><span class="sxs-lookup"><span data-stu-id="4da70-163">By default, Enhanced Security Configuration is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="4da70-164">**Solution**: si le message **accès refusé** s’affiche lorsque vous essayez d’afficher des rapports sur le serveur MBAM, vous pouvez définir un objet de stratégie de groupe ou modifier le paramètre par défaut manuellement dans votre image pour désactiver la configuration de sécurité améliorée.</span><span class="sxs-lookup"><span data-stu-id="4da70-164">**Workaround**: If the **Access Denied** message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="4da70-165">Vous pouvez également afficher les rapports à partir d’un autre ordinateur sur lequel la configuration de la sécurité améliorée n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="4da70-165">You can also alternatively view the reports from another computer on which Enhanced Security Configuration is not enabled.</span></span>

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> <span data-ttu-id="4da70-166">Échec de l’installation de MBAM Server lors de la mise à niveau de SQLServer2008 vers SQLServer2012</span><span class="sxs-lookup"><span data-stu-id="4da70-166">MBAM Server installation fails when you upgrade from SQLServer2008 to SQLServer2012</span></span>

<span data-ttu-id="4da70-167">Si vous effectuez une mise à niveau de SQLServer2008 vers SQLServer2012, puis essayez d’installer la base de données de conformité et d’audit ou la base de données de récupération, l’installation échoue et restaure.</span><span class="sxs-lookup"><span data-stu-id="4da70-167">If you upgrade from SQLServer2008 to SQLServer2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="4da70-168">L’échec se produit parce que le fichier SQLCMD.exe requis a été supprimé lors de la mise à niveau de SQLServer et qu’il est introuvable par le programme d’installation MBAM.</span><span class="sxs-lookup"><span data-stu-id="4da70-168">The failure occurs because the required SQLCMD.exe file was removed during the SQLServer upgrade, and it cannot be found by the MBAM installer.</span></span> <span data-ttu-id="4da70-169">Les lignes du fichier journal MSI risquent de ressembler à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="4da70-169">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="4da70-170">CA Recovery DB RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript de récupération de la base de connaissances: dbInstance-xxxxxx\\I01RunDbInstallScript récupération de la base de connaissances: sqlScript-C:\\Program Files\\Microsoft\\Microsoft BitLocker administration et Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript de la _Recovery base de connaissances: DefaultFilename-MBAM AUTORITÉ de I01\\MSSQL\\DATA\\RunDbInstallScript de récupération de la base de connaissances: defaultLogPath-K:\\MSSQL\\MSSQL10. CA Recovery DB I01\\MSSQL\\Data\\RunDbInstallScript: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Program Files\\Microsoft\\Microsoft BitLocker and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript de récupération de la base de connaissances: commencez à exécuter l’installation de la base de données de récupération scriptRunDbInstallScript de la base de données de récupération: le fichier journal de récupération de la base de données de récupération se trouve dans C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript exception de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="4da70-170">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="4da70-171">Le programme d’installation de l’application MBAM Server Windows est codé en dur pour trouver le chemin d’accès SQLCMD.exe en consultant la valeur de chaîne Path dans le Registre sous HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="4da70-171">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="4da70-172">La clé est toujours présente lors de la migration de SQLServer2008 vers SQLServer2012, mais le chemin d’accès référencé par la valeur Data ne contient pas le fichier SQLCMD.exe, car le processus SQLupgrade a supprimé le fichier.</span><span class="sxs-lookup"><span data-stu-id="4da70-172">The key is still present during the migration from SQLServer2008 to SQLServer2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQLupgrade process removed the file.</span></span>

<span data-ttu-id="4da70-173">**Solution de contournement**: renommez temporairement la valeur de chaîne de chemin d’accès SQLServer\\100\\Tools\\ClientSetup HKLM\\Software\\Microsoft\\Microsoft sur **path \ _OLD**, puis exécutez de nouveau Windows Installer sur le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="4da70-173">**Workaround**: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup path string value to **Path\_old**, and then run Windows Installer on the MBAM Server again.</span></span> <span data-ttu-id="4da70-174">Lorsque l’installation est terminée, et crée les bases de données dans SQLServer2012, renommez **path \ _OLD** sur **path**.</span><span class="sxs-lookup"><span data-stu-id="4da70-174">When the installation completes successfully and creates the databases in SQLServer2012, rename **Path\_old** to **Path**.</span></span>

## <span data-ttu-id="4da70-175">HotFix et Articles de la base de connaissances pour MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="4da70-175">Hotfixes and Knowledge Base articles for MBAM 2.0 SP1</span></span>


<span data-ttu-id="4da70-176">Cette section contient des correctifs et des Articles de la base de connaissances pour MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="4da70-176">This section contains hotfixes and KB articles for MBAM 2.0 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="4da70-177">Article de la base de connaissances</span><span class="sxs-lookup"><span data-stu-id="4da70-177">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="4da70-178">Title</span><span class="sxs-lookup"><span data-stu-id="4da70-178">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="4da70-179">Link</span><span class="sxs-lookup"><span data-stu-id="4da70-179">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4da70-180">2831166</span><span class="sxs-lookup"><span data-stu-id="4da70-180">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-181">L’installation de Microsoft BitLocker administration et surveillance (MBAM) 2,0 échoue avec les &quot; objets System Center cm déjà installés&quot;</span><span class="sxs-lookup"><span data-stu-id="4da70-181">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="4da70-182">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-182">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4da70-183">2870849</span><span class="sxs-lookup"><span data-stu-id="4da70-183">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-184">Les utilisateurs ne peuvent pas récupérer la clé de récupération BitLocker à l’aide du portail libre-service MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4da70-184">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="4da70-185">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-185">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4da70-186">2756402</span><span class="sxs-lookup"><span data-stu-id="4da70-186">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-187">Le client MBAM échoue avec l’ID d’événement 4 et le code d’erreur 0x8004100E dans la description de l’événement.</span><span class="sxs-lookup"><span data-stu-id="4da70-187">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="4da70-188">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-188">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4da70-189">2620287</span><span class="sxs-lookup"><span data-stu-id="4da70-189">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-190">Message d’erreur «erreur serveur dans l’application «/Reports» lorsque vous cliquez sur l’onglet rapports dans MBAM</span><span class="sxs-lookup"><span data-stu-id="4da70-190">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="4da70-191">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-191">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4da70-192">2639518</span><span class="sxs-lookup"><span data-stu-id="4da70-192">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-193">Erreur lors de l’ouverture des rapports de conformité entreprise ou ordinateur dans MBAM</span><span class="sxs-lookup"><span data-stu-id="4da70-193">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="4da70-194">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-194">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4da70-195">2620269</span><span class="sxs-lookup"><span data-stu-id="4da70-195">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-196">MBAM entreprise n’a pas effectué de mise à jour</span><span class="sxs-lookup"><span data-stu-id="4da70-196">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="4da70-197">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-197">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4da70-198">2712461</span><span class="sxs-lookup"><span data-stu-id="4da70-198">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-199">L’installation de MBAM sur un contrôleur de domaine n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4da70-199">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="4da70-200">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-200">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4da70-201">2876732</span><span class="sxs-lookup"><span data-stu-id="4da70-201">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-202">Vous recevez le code d’erreur 0x80071a90 lors de l’installation d’MBAM 2.0 dans le cadre d’une intégration autonome ou du gestionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="4da70-202">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="4da70-203">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-203">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4da70-204">2754259</span><span class="sxs-lookup"><span data-stu-id="4da70-204">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-205">MBAM et sécuriser la communication réseau</span><span class="sxs-lookup"><span data-stu-id="4da70-205">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="4da70-206">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-206">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4da70-207">2870842</span><span class="sxs-lookup"><span data-stu-id="4da70-207">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-208">Échec de l’installation d’MBAM 2.0 lors du scénario d’intégration de Configuration Manager avec SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="4da70-208">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="4da70-209">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-209">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4da70-210">2668533</span><span class="sxs-lookup"><span data-stu-id="4da70-210">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-211">Échec de la configuration d’MBAM si le SSRS SQL n’est pas configuré correctement</span><span class="sxs-lookup"><span data-stu-id="4da70-211">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="4da70-212">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-212">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4da70-213">2870847</span><span class="sxs-lookup"><span data-stu-id="4da70-213">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-214">Le programme d’installation de MBAM 2,0 est en échec avec &quot; récupération d’erreur dans les paramètres de rôle du serveur Configuration Manager pour &#39;Reporting Services Point&#39;&quot;</span><span class="sxs-lookup"><span data-stu-id="4da70-214">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="4da70-215">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-215">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4da70-216">2870839</span><span class="sxs-lookup"><span data-stu-id="4da70-216">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-217">Les rapports d’entreprise MBAM 2.0 ne sont pas actualisés dans la topologie autonome MBAM 2.0 en raison de l’échec du CreateCache de travail SQL</span><span class="sxs-lookup"><span data-stu-id="4da70-217">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="4da70-218">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-218">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4da70-219">2620269</span><span class="sxs-lookup"><span data-stu-id="4da70-219">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-220">MBAM entreprise n’a pas effectué de mise à jour</span><span class="sxs-lookup"><span data-stu-id="4da70-220">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="4da70-221">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-221">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4da70-222">2935997</span><span class="sxs-lookup"><span data-stu-id="4da70-222">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-223">MBAM-XX XXXXXXXXX xxxxxxxxx xxxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="4da70-223">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="4da70-224">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-224">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4da70-225">2612822</span><span class="sxs-lookup"><span data-stu-id="4da70-225">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="4da70-226">L’enregistrement d’ordinateur est rejeté dans MBAM</span><span class="sxs-lookup"><span data-stu-id="4da70-226">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="4da70-227">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="4da70-227">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4da70-228">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4da70-228">Related topics</span></span>


[<span data-ttu-id="4da70-229">À propos de MBAM2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="4da70-229">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)

 

 






---
title: Résolution des problèmes d’installation de MBAM2.5
description: Découvrez comment résoudre les problèmes d’installation d’MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804548"
---
# <span data-ttu-id="ec88a-103">Résolution des problèmes d’installation de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ec88a-103">Troubleshooting MBAM 2.5 installation problems</span></span>

<span data-ttu-id="ec88a-104">Cet article présente la procédure de résolution des problèmes d’installation de Microsoft BitLocker administration et de surveillance (MBAM) 2,5 dans une configuration autonome.</span><span class="sxs-lookup"><span data-stu-id="ec88a-104">This article introduces how to troubleshoot Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 installation issues in a standalone configuration.</span></span>

## <span data-ttu-id="ec88a-105">Référencement des fichiers journaux de MBAM pour la résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="ec88a-105">Referring MBAM log files for troubleshooting</span></span>

<span data-ttu-id="ec88a-106">MBAM inclut la journalisation de l’installation du serveur, de l’installation du client et des événements.</span><span class="sxs-lookup"><span data-stu-id="ec88a-106">MBAM includes logging for server installation, client installation, and events.</span></span> <span data-ttu-id="ec88a-107">Cette journalisation devrait faire l’appel de la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="ec88a-107">This logging should be referred to for troubleshooting.</span></span> 
 
### <span data-ttu-id="ec88a-108">Fichiers journaux d’installation de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="ec88a-108">MBAM server installation log files</span></span>

<span data-ttu-id="ec88a-109">MBAMServerSetup.exe génère les fichiers journaux suivants dans le dossier% Temp% de l’utilisateur lors de l’installation d’MBAM:</span><span class="sxs-lookup"><span data-stu-id="ec88a-109">MBAMServerSetup.exe generates the following log files in the user’s %temp% folder during MBAM installation:</span></span><br /> **<span data-ttu-id="ec88a-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 numéros>. log</span><span class="sxs-lookup"><span data-stu-id="ec88a-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 numbers>.log</span></span>**

<span data-ttu-id="ec88a-111">MBAMServerSetup.exe enregistre les actions effectuées lors de l’installation d’MBAM et de la fonctionnalité MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="ec88a-111">MBAMServerSetup.exe logs the actions that were taken during MBAM setup and MBAM server feature installation:</span></span><br /> **<span data-ttu-id="ec88a-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="ec88a-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log</span></span>**

<span data-ttu-id="ec88a-113">MBAMServerSetup.exe enregistre les actions supplémentaires effectuées lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="ec88a-113">MBAMServerSetup.exe logs additional actions that were taken during installation.</span></span>

### <span data-ttu-id="ec88a-114">Fichier journal d’installation du client MBAM</span><span class="sxs-lookup"><span data-stu-id="ec88a-114">MBAM client installation log file</span></span>

<span data-ttu-id="ec88a-115">L’installation du client est enregistrée dans le fichier journal suivant dans le dossier% Temp% (ou un emplacement personnalisé, selon la façon dont le client a été installé):</span><span class="sxs-lookup"><span data-stu-id="ec88a-115">The client installation is recorded in the following log file in the %temp% folder (or a custom location, depending on how the client was installed):</span></span> <br />**<span data-ttu-id="ec88a-116">MSI \<five random characters\> . log</span><span class="sxs-lookup"><span data-stu-id="ec88a-116">MSI\<five random characters\>.log</span></span>**

<span data-ttu-id="ec88a-117">Ce journal contient les actions effectuées lors de l’installation du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-117">This log contains the actions that are taken during MBAM client installation.</span></span>
 
### <span data-ttu-id="ec88a-118">Événement client MBAM-canal de journalisation</span><span class="sxs-lookup"><span data-stu-id="ec88a-118">MBAM client event-logging channel</span></span>

<span data-ttu-id="ec88a-119">MBAM a des canaux de journalisation des événements séparés.</span><span class="sxs-lookup"><span data-stu-id="ec88a-119">MBAM has separate event-logging channels.</span></span> <span data-ttu-id="ec88a-120">Les fichiers du journal d’administration, de l’analyse et du fonctionnement se trouvent dans l’observateur d’événements, sous **applications et services consignent**  >  **Microsoft**  >  **Windows**  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-120">The Admin, Analytical, and Operational log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span>

<span data-ttu-id="ec88a-121">Le tableau suivant fournit une description succincte de chaque journal des événements.</span><span class="sxs-lookup"><span data-stu-id="ec88a-121">The following table provides a brief description of each event log.</span></span>
 
|<span data-ttu-id="ec88a-122">Journal des événements</span><span class="sxs-lookup"><span data-stu-id="ec88a-122">Event log</span></span>| <span data-ttu-id="ec88a-123">Description</span><span class="sxs-lookup"><span data-stu-id="ec88a-123">Description</span></span>|
|----------|-------|
|<span data-ttu-id="ec88a-124">Microsoft-Windows-MBAM/admin</span><span class="sxs-lookup"><span data-stu-id="ec88a-124">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="ec88a-125">Contient des messages d’erreur</span><span class="sxs-lookup"><span data-stu-id="ec88a-125">Contains error messages</span></span>|
|<span data-ttu-id="ec88a-126">Microsoft-Windows-MBAM/analyse</span><span class="sxs-lookup"><span data-stu-id="ec88a-126">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="ec88a-127">Contient des informations de journalisation avancées</span><span class="sxs-lookup"><span data-stu-id="ec88a-127">Contains advanced logging information</span></span>|
|<span data-ttu-id="ec88a-128">Microsoft-Windows-MBAM/opérationnel</span><span class="sxs-lookup"><span data-stu-id="ec88a-128">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="ec88a-129">Contient des messages de réussite</span><span class="sxs-lookup"><span data-stu-id="ec88a-129">Contains success messages</span></span>|

### <span data-ttu-id="ec88a-130">MBAM-canal de journalisation des événements serveur</span><span class="sxs-lookup"><span data-stu-id="ec88a-130">MBAM server event-logging channel</span></span>

<span data-ttu-id="ec88a-131">Les fichiers journaux sont situés dans l’observateur d’événements, sous **les journaux d’application et de service journaux**de  >  **Microsoft**  >  **Windows**  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-131">The log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span> <span data-ttu-id="ec88a-132">Le tableau suivant inclut les journaux des événements serveur introduits dans MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="ec88a-132">The following table includes server event logs that were introduced in MBAM 2.5:</span></span>

|<span data-ttu-id="ec88a-133">Journal des événements</span><span class="sxs-lookup"><span data-stu-id="ec88a-133">Event log</span></span>| <span data-ttu-id="ec88a-134">Description</span><span class="sxs-lookup"><span data-stu-id="ec88a-134">Description</span></span>|
|--------|-------------|
|<span data-ttu-id="ec88a-135">Microsoft-Windows-MBAM/admin</span><span class="sxs-lookup"><span data-stu-id="ec88a-135">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="ec88a-136">Contient des messages d’erreur</span><span class="sxs-lookup"><span data-stu-id="ec88a-136">Contains error messages</span></span>|
|<span data-ttu-id="ec88a-137">Microsoft-Windows-MBAM/analyse</span><span class="sxs-lookup"><span data-stu-id="ec88a-137">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="ec88a-138">Contient des informations de journalisation avancées</span><span class="sxs-lookup"><span data-stu-id="ec88a-138">Contains advanced logging information</span></span>|
|<span data-ttu-id="ec88a-139">Microsoft-Windows-MBAM/opérationnel</span><span class="sxs-lookup"><span data-stu-id="ec88a-139">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="ec88a-140">Contient des messages de réussite</span><span class="sxs-lookup"><span data-stu-id="ec88a-140">Contains success messages</span></span>|

### <span data-ttu-id="ec88a-141">Journaux de service Web MBAM</span><span class="sxs-lookup"><span data-stu-id="ec88a-141">MBAM web service logs</span></span>

<span data-ttu-id="ec88a-142">Chaque journal de service Web MBAM écrit les informations de journalisation dans un fichier SVCLOG.</span><span class="sxs-lookup"><span data-stu-id="ec88a-142">Each MBAM web service log writes logging information to an SVCLOG file.</span></span> <span data-ttu-id="ec88a-143">Par défaut, chaque service Web écrit le fichier de suivi sous un dossier qui utilise son nom dans le dossier Solution\Logs de gestion C:\inetpub\Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec88a-143">By default, each web service writes the trace file under a folder that uses its name in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span>

<span data-ttu-id="ec88a-144">Vous pouvez utiliser l’outil visionneuse de suivi des services (intégré à Microsoft Visual Studio) pour passer en revue les traces de svclog.</span><span class="sxs-lookup"><span data-stu-id="ec88a-144">You can use the service trace viewer tool (part of Microsoft Visual Studio) to review the svclog traces.</span></span>

## <span data-ttu-id="ec88a-145">Résolution des problèmes de chiffrement et de création de rapports</span><span class="sxs-lookup"><span data-stu-id="ec88a-145">Troubleshooting encryption and reporting issues</span></span>

<span data-ttu-id="ec88a-146">Cette section contient des informations permettant de résoudre les problèmes liés aux fonctionnalités du serveur, aux fonctionnalités client, aux paramètres de configuration et aux problèmes connus:</span><span class="sxs-lookup"><span data-stu-id="ec88a-146">This section contains troubleshooting information for server functionality, client functionality, configuration settings, and known issues:</span></span>
 
### <span data-ttu-id="ec88a-147">Installation du client MBAM, paramètres de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ec88a-147">MBAM client installation, Group Policy settings</span></span>

<span data-ttu-id="ec88a-148">Déterminez si l’agent MBAM est installé sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="ec88a-148">Determine whether the MBAM agent is installed on the client computer.</span></span> <span data-ttu-id="ec88a-149">Lorsque MBAM est installé, il crée un service intitulé service du client de gestion BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec88a-149">When MBAM is installed, it creates a service that is named BitLocker Management Client Service.</span></span> <span data-ttu-id="ec88a-150">Ce service est configuré pour démarrer automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ec88a-150">This service is configured to start automatically.</span></span> <span data-ttu-id="ec88a-151">Déterminez si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ec88a-151">Determine whether the service is running.</span></span>

<span data-ttu-id="ec88a-152">Assurez-vous que les paramètres de stratégie de groupe MBAM sont appliqués sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="ec88a-152">Make sure that MBAM Group Policy settings are applied on the client computer.</span></span> <span data-ttu-id="ec88a-153">La sous-clé de Registre suivante est créée si les paramètres de stratégie de groupe ont été appliqués sur l’ordinateur client: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**</span><span class="sxs-lookup"><span data-stu-id="ec88a-153">The following registry subkey is created if the Group Policy settings were applied on the client computer: **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**</span></span>

<span data-ttu-id="ec88a-154">Vérifiez que cette clé existe et qu’elle est remplie à l’aide de valeurs par paramètre de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ec88a-154">Verify that this key exists and is populated by using values per Group Policy settings.</span></span>

### <span data-ttu-id="ec88a-155">Agent MBAM au cours de la période de délai initial</span><span class="sxs-lookup"><span data-stu-id="ec88a-155">MBAM Agent in the initial delay period</span></span>

<span data-ttu-id="ec88a-156">Le client MBAM ne démarre pas l’opération immédiatement après l’installation.</span><span class="sxs-lookup"><span data-stu-id="ec88a-156">The MBAM client doesn't start the operation immediately after installation.</span></span> <span data-ttu-id="ec88a-157">Le délai initial d’un délai de 1 à 18 minutes avant le démarrage de l’agent MBAM est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ec88a-157">There is an initial random delay of 1–18 minutes before the MBAM Agent starts its operation.</span></span> <span data-ttu-id="ec88a-158">Outre le délai initial, il y a un délai d’au moins 90 minutes.</span><span class="sxs-lookup"><span data-stu-id="ec88a-158">In addition to the initial delay, there is a delay of at least 90 minutes.</span></span> <span data-ttu-id="ec88a-159">(Le délai dépend des paramètres de stratégie de groupe qui sont configurés pour la fréquence de vérification de l’état du client.) Par conséquent, le délai total précédant l’opération de démarrage d’un client correspond au délai de *démarrage aléatoire*permettant de  +  *vérifier le délai de fréquence*.</span><span class="sxs-lookup"><span data-stu-id="ec88a-159">(The delay depends on the Group Policy settings that are configured for the frequency of checking the client status.) Therefore, the total delay before a client starts operation is *random startup delay* + *client checking frequency delay*.</span></span>

<span data-ttu-id="ec88a-160">Si les journaux des événements de fonctionnement et d’administration sont vides, le client n’a pas encore commencé l’opération et a atteint la période de délai mentionnée auparavant.</span><span class="sxs-lookup"><span data-stu-id="ec88a-160">If the Operational and Admin event logs are blank, the client has not started the operation yet and is in the delay period that was mentioned earlier.</span></span> <span data-ttu-id="ec88a-161">Pour éviter ce délai, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="ec88a-161">If you want to bypass the delay, follow these steps:</span></span>
 
1. <span data-ttu-id="ec88a-162">Arrêtez le service du client de gestion BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec88a-162">Stop the BitLocker Management Client Service service.</span></span>

2. <span data-ttu-id="ec88a-163">Sous HKEY_LOCAL_MACHINE la sous-clé de Registre **\software\microsoft\mbam** , créez la valeur de Registre **NoStartupDelay** , définissez son type sur **REG_DWORD**, puis définissez sa valeur sur **1**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-163">Under the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** registry subkey, create the **NoStartupDelay** registry value, set its type to **REG_DWORD**, and then set its value to **1**.</span></span>

3. <span data-ttu-id="ec88a-164">Sous **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**, définissez les valeurs **ClientWakeupFrequency** et **StatusReportingFrequency** sur **1**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-164">Under **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**, set the **ClientWakeupFrequency** and **StatusReportingFrequency** values to **1**.</span></span> <span data-ttu-id="ec88a-165">Ces valeurs seront restaurées dans leurs paramètres d’origine après la mise à jour de la stratégie de groupe sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ec88a-165">These values will revert to their original settings after Group Policy updates are on the computer.</span></span>

4. <span data-ttu-id="ec88a-166">Démarrez le service du client de gestion BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec88a-166">Start the BitLocker Management Client Service service.</span></span>

<span data-ttu-id="ec88a-167">Après le démarrage du service, si vous ouvrez une session locale sur l’ordinateur et qu’il n’y a pas d’erreurs, vous devriez recevoir une demande de chiffrer l’ordinateur dans une minute.</span><span class="sxs-lookup"><span data-stu-id="ec88a-167">After the service starts, if you log in locally on the computer and there are no errors, you should receive a request to encrypt the computer within one minute.</span></span> <span data-ttu-id="ec88a-168">Si vous ne recevez pas de requête, consultez les journaux d’administration MBAM pour toute erreur.</span><span class="sxs-lookup"><span data-stu-id="ec88a-168">If you do not receive a request, you should review the MBAM Admin logs for any error entries.</span></span>

### <span data-ttu-id="ec88a-169">L’ordinateur n’est pas équipé d’un module de plateforme sécurisée, ou le module de plateforme sécurisée n’est pas activé dans le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ec88a-169">Computer does not have a TPM device, or the TPM device is not enabled in the BIOS</span></span>

<span data-ttu-id="ec88a-170">Examinez le journal des événements d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-170">Review the MBAM Admin event log.</span></span> <span data-ttu-id="ec88a-171">Vous verrez une entrée d’événement semblable à celle qui suit dans le journal des événements d’administration MBAM:</span><span class="sxs-lookup"><span data-stu-id="ec88a-171">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

<span data-ttu-id="ec88a-172">Ouvrez le module de gestion de la plateforme sécurisée (TPM. msc) et vérifiez que l’ordinateur dispose d’un appareil de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="ec88a-172">Open TPM Management (tpm.msc), and check whether the computer has a TPM device.</span></span> <span data-ttu-id="ec88a-173">Si TPM. msc ne montre pas d’appareil, ouvrez le gestionnaire de périphériques (devmgmt. msc) et recherchez un module de plateforme sécurisée sous dispositifs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ec88a-173">If tpm.msc does not show a device, open Device Manager (devmgmt.msc), and check for a Trusted Platform Module under Security Devices.</span></span> <span data-ttu-id="ec88a-174">Si vous ne voyez pas d’appareil de module de plateforme sécurisée, il est possible que cela soit vrai pour l’une des raisons suivantes:</span><span class="sxs-lookup"><span data-stu-id="ec88a-174">If you do not see a Trusted Platform Module device, this might be true for one of the following reasons:</span></span>

* <span data-ttu-id="ec88a-175">Votre système ne possède pas de périphérique de module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="ec88a-175">Your system doesn't have a Trusted Platform Module (TPM/Security) device.</span></span>

* <span data-ttu-id="ec88a-176">Le périphérique TPM est désactivé dans le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ec88a-176">The TPM device is disabled in the BIOS.</span></span>

* <span data-ttu-id="ec88a-177">Le module de plateforme sécurisée est activé dans le BIOS, mais la gestion du périphérique TPM à partir du système d’exploitation est désactivée dans le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ec88a-177">TPM Device is enabled in the BIOS, but management of the TPM device from the operating system setting is disabled in the BIOS.</span></span>

* <span data-ttu-id="ec88a-178">Vous n’utilisez pas un pilote Microsoft pour le périphérique GPC.</span><span class="sxs-lookup"><span data-stu-id="ec88a-178">You aren't using a Microsoft driver for the TPM device.</span></span> <span data-ttu-id="ec88a-179">Passez en revue les périphériques qui sont répertoriés dans le gestionnaire de périphériques pour identifier le pilote de périphérique Microsoft GPC.</span><span class="sxs-lookup"><span data-stu-id="ec88a-179">Review the devices that are listed in device manager to identify the Microsoft TPM device driver.</span></span>

<span data-ttu-id="ec88a-180">Si le module de plateforme sécurisée n’utilise pas le pilote C:\Windows\System32\tpm.sys, vous devez mettre à jour le pilote en sélectionnant le fichier C:\Windows\Inf\tpm.inf.</span><span class="sxs-lookup"><span data-stu-id="ec88a-180">If the TPM device is not using the C:\Windows\System32\tpm.sys driver, you should update the driver by selecting the C:\Windows\Inf\tpm.inf file.</span></span>

### <span data-ttu-id="ec88a-181">Votre ordinateur ne possède pas de partition système valide</span><span class="sxs-lookup"><span data-stu-id="ec88a-181">Computer does not have a valid SYSTEM partition</span></span>

<span data-ttu-id="ec88a-182">Examinez le journal des événements d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-182">Review the MBAM Admin event log.</span></span> <span data-ttu-id="ec88a-183">Vous verrez une entrée d’événement semblable à celle qui suit dans le journal des événements d’administration MBAM:</span><span class="sxs-lookup"><span data-stu-id="ec88a-183">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

<span data-ttu-id="ec88a-184">BitLocker nécessite une partition système pour activer le chiffrement ([chiffrement de lecteur BitLocker dans Windows 7: Forum aux questions](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span><span class="sxs-lookup"><span data-stu-id="ec88a-184">BitLocker requires a SYSTEM partition to enable encryption ([BitLocker Drive Encryption in Windows 7: Frequently Asked Questions](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span></span>

<span data-ttu-id="ec88a-185">MBAM ne crée pas automatiquement la partition système.</span><span class="sxs-lookup"><span data-stu-id="ec88a-185">MBAM doesn't create the system partition automatically.</span></span> <span data-ttu-id="ec88a-186">Vous pouvez utiliser l’utilitaire de préparation de lecteur BitLocker (bdehdcfg.exe) pour créer la partition système et déplacer les fichiers de démarrage requis.</span><span class="sxs-lookup"><span data-stu-id="ec88a-186">You can use the BitLocker drive preparation utility (bdehdcfg.exe) to create the system partition and move the required startup files.</span></span>

<span data-ttu-id="ec88a-187">Par exemple, vous pouvez utiliser la commande **% windir% \system32\bdeHdCfg.exe-Target par défaut-size 300 – quiet** pour préparer le lecteur en silence avant de déployer MBAM pour chiffrer les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="ec88a-187">For example, you can use the command **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** to prepare the drive silently before you deploy MBAM to encrypt the drives.</span></span> <span data-ttu-id="ec88a-188">Cela nécessite un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="ec88a-188">This requires a restart.</span></span> <span data-ttu-id="ec88a-189">Vous pouvez également Scripter l’action si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ec88a-189">You can also script the action if this is required.</span></span> <span data-ttu-id="ec88a-190">Le document suivant décrit l’outil de préparation du lecteur BitLocker:</span><span class="sxs-lookup"><span data-stu-id="ec88a-190">The following document describes the BitLocker Drive Preparation Tool:</span></span>

[<span data-ttu-id="ec88a-191">Description de l’outil de préparation du lecteur BitLocker</span><span class="sxs-lookup"><span data-stu-id="ec88a-191">Description of the BitLocker Drive Preparation Tool</span></span>](https://support.microsoft.com/help/933246)

### <span data-ttu-id="ec88a-192">Les lecteurs ne sont pas mis en forme pour disposer d’un système de fichiers compatible</span><span class="sxs-lookup"><span data-stu-id="ec88a-192">Drives are not formatted to have a compatible file system</span></span>

<span data-ttu-id="ec88a-193">Consultez l' [article TechNet relatif à la configuration requise pour le système de fichiers pour BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span><span class="sxs-lookup"><span data-stu-id="ec88a-193">See the [TechNet article for file system requirements for BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span></span>

### <span data-ttu-id="ec88a-194">Conflit de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ec88a-194">Group Policy conflict</span></span>

<span data-ttu-id="ec88a-195">Vous verrez une entrée d’événement semblable à celle qui suit dans le journal des événements d’administration MBAM:</span><span class="sxs-lookup"><span data-stu-id="ec88a-195">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

<span data-ttu-id="ec88a-196">Vérifiez les paramètres de stratégie de groupe pour vérifier que vous n’avez pas de paramètre en conflit entre les paramètres de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-196">Verify your Group Policy settings to make sure that you do not have a conflicting setting among the MBAM Group Policy settings.</span></span>

<span data-ttu-id="ec88a-197">Vous devez configurer une stratégie de groupe à l’aide du modèle MDOP MBAM et non du modèle de chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec88a-197">You should configure Group Policy by using the MDOP MBAM template and not the BitLocker Drive Encryption template.</span></span>

<span data-ttu-id="ec88a-198">Exemple:</span><span class="sxs-lookup"><span data-stu-id="ec88a-198">For example:</span></span>

<span data-ttu-id="ec88a-199">Sous paramètres de chiffrement de lecteur du système d’exploitation, vous avez sélectionné TPM en tant que protecteur, et vous pouvez également sélectionner **autoriser les codes confidentiels optimisés pour le démarrage**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-199">Under Operating system drive encryption settings, you selected TPM as the protector, and you also selected **Allow enhanced PINs for startup**.</span></span> <span data-ttu-id="ec88a-200">Il s’agit de paramètres en conflit, car la protection GPC uniquement ne nécessite pas de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="ec88a-200">These are conflicting settings because TPM-only protection doesn't require a PIN.</span></span> <span data-ttu-id="ec88a-201">Par conséquent, vous devez désactiver le paramètre épingles améliorées.</span><span class="sxs-lookup"><span data-stu-id="ec88a-201">Therefore, you should disable the enhanced PINs setting.</span></span>

### <span data-ttu-id="ec88a-202">L’utilisateur a pu demander une exonération</span><span class="sxs-lookup"><span data-stu-id="ec88a-202">User may have requested an exemption</span></span>

<span data-ttu-id="ec88a-203">Si vous avez activé l’ordinateur d’administration\Composants Templates\Windows Components\MDOP MBAM (gestion de BitLocker) \Client Management\Configure paramètre de stratégie d’exemption des utilisateurs, les utilisateurs pourront demander une exemption.</span><span class="sxs-lookup"><span data-stu-id="ec88a-203">If you enabled the Computer Configuration\Administrative Templates\Windows Components\MDOP MBAM (BitLocker Management)\Client Management\Configure user exemption policy Group Policy setting, users will be offered the option to request an exemption.</span></span>

<span data-ttu-id="ec88a-204">Par défaut, si l’utilisateur demande une exemption, l’exemption est valide pendant 7 jours, et l’utilisateur ne reçoit pas les invites de chiffrement au cours de cette période.</span><span class="sxs-lookup"><span data-stu-id="ec88a-204">By default, if the user requests an exemption, the exemption will be valid for 7 days, and the user will not receive prompts to encrypt during this period.</span></span> <span data-ttu-id="ec88a-205">(La valeur par défaut peut être augmentée ou réduite lors de la configuration de la stratégie.) Au terme de la période d’exemption, l’utilisateur est invité à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="ec88a-205">(The default value can be increased or decreased during policy configuration.) After the exemption period is over, the user is prompted to encrypt.</span></span>

<span data-ttu-id="ec88a-206">Vous verrez l’entrée suivante dans le journal des événements d’administration MBAM lorsqu’un ordinateur est soumis à une exemption d’utilisation:</span><span class="sxs-lookup"><span data-stu-id="ec88a-206">You will see the following entry in the MBAM Admin event log when a computer is under user exemption:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

<span data-ttu-id="ec88a-207">Si vous voulez remplacer manuellement l’exemption pour un ordinateur, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="ec88a-207">If you want to manually override user exemption for a computer, follow these steps:</span></span>
 
1. <span data-ttu-id="ec88a-208">Définissez la valeur AllowUserExemption sur **0** sous la sous-clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="ec88a-208">Set the AllowUserExemption value to **0** under the following registry subkey:</span></span> <br />
**<span data-ttu-id="ec88a-209">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="ec88a-209">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

2. <span data-ttu-id="ec88a-210">Supprimez toutes les valeurs de Registre sous la sous-clé de Registre suivante, à l’exception de **AgentVersion**, **EncodedComputerName**et **installed**:</span><span class="sxs-lookup"><span data-stu-id="ec88a-210">Delete all the registry values under the following registry subkey except for **AgentVersion**, **EncodedComputerName**, and **Installed**:</span></span><br />
**<span data-ttu-id="ec88a-211">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM</span><span class="sxs-lookup"><span data-stu-id="ec88a-211">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM</span></span>**

    <span data-ttu-id="ec88a-212">**Remarques** Vous devez redémarrer l’agent MBAM pour que les modifications prennent effet.</span><span class="sxs-lookup"><span data-stu-id="ec88a-212">**Note** You must restart the MBAM agent for the changes to take effect.</span></span>

<span data-ttu-id="ec88a-213">Sachez qu’après avoir appliqué une stratégie de groupe à votre ordinateur, ces valeurs risquent de rétablir leurs paramètres d’origine.</span><span class="sxs-lookup"><span data-stu-id="ec88a-213">Be aware that after you apply Group Policy to the computer, these values may revert to their original settings.</span></span>

### <span data-ttu-id="ec88a-214">Problème WMI</span><span class="sxs-lookup"><span data-stu-id="ec88a-214">WMI issue</span></span>

<span data-ttu-id="ec88a-215">MBAM utilise les méthodes de la classe win32_encryptablevolume pour gérer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec88a-215">MBAM uses methods of the win32_encryptablevolume class to manage BitLocker.</span></span> <span data-ttu-id="ec88a-216">Si ce module n’est pas enregistré ou est endommagé, le client MBAM ne fonctionnera pas correctement et l’entrée d’événement suivante s’affichera dans le journal des événements d’administration MBAM:</span><span class="sxs-lookup"><span data-stu-id="ec88a-216">If this module is unregistered or corrupted, the MBAM client will not operate correctly, and you will see the following event entry in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

<span data-ttu-id="ec88a-217">Par ailleurs, il est possible que les stratégies de récupération et de matériel ne s’appliquent pas à l’aide du code d’erreur 0x8007007e.</span><span class="sxs-lookup"><span data-stu-id="ec88a-217">Additionally, you may notice that the Recovery and Hardware policies do not apply with Error Code 0x8007007e.</span></span> <span data-ttu-id="ec88a-218">Cela se traduit par «le module spécifié est introuvable».</span><span class="sxs-lookup"><span data-stu-id="ec88a-218">This translates to "The specified module could not be found."</span></span>

<span data-ttu-id="ec88a-219">Pour résoudre ce problème, vous devez réinscrire la classe **Win32_EncryptableVolume** à l’aide de la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="ec88a-219">To resolve this issue, you should reregister the **win32_encryptablevolume** class by using the following command:</span></span>

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <span data-ttu-id="ec88a-220">Résoudre les problèmes de communication avec l’agent MBAM</span><span class="sxs-lookup"><span data-stu-id="ec88a-220">Troubleshooting MBAM Agent communication issues</span></span>

<span data-ttu-id="ec88a-221">Cette section contient des informations de dépannage pour les problèmes suivants liés à la communication avec l’agent MBAM:</span><span class="sxs-lookup"><span data-stu-id="ec88a-221">This section contains troubleshooting information for the following issues that are related to MBAM agent communication:</span></span>

### <span data-ttu-id="ec88a-222">URL du service MBAM incorrecte</span><span class="sxs-lookup"><span data-stu-id="ec88a-222">Incorrect MBAM service URL</span></span>

<span data-ttu-id="ec88a-223">Si la valeur du service de vérification de conformité MBAM ou de récupération et de service matériel est incorrecte, une entrée d’événement semblable à la suivante apparaît dans le journal des événements d’administration MBAM sur l’ordinateur client:</span><span class="sxs-lookup"><span data-stu-id="ec88a-223">If the value of MBAM Compliance Status Service or Recovery and Hardware Service is incorrect, you'll see an event entry that resembles the following in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

<span data-ttu-id="ec88a-224">Vérifiez les valeurs de **KeyRecoveryServiceEndPoint** et **StatusReportingServiceEndpoint** sous la sous-clé de Registre suivante de l’ordinateur client:</span><span class="sxs-lookup"><span data-stu-id="ec88a-224">Verify the values of **KeyRecoveryServiceEndPoint** and **StatusReportingServiceEndpoint** under the following registry subkey on the client computer:</span></span> <br />
**<span data-ttu-id="ec88a-225">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="ec88a-225">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

<span data-ttu-id="ec88a-226">Par défaut, l’URL de KeyRecoveryServiceEndPoint (point de terminaison du service de récupération et de matériel MBAM) est au format suivant:</span><span class="sxs-lookup"><span data-stu-id="ec88a-226">By default, the URL for KeyRecoveryServiceEndPoint (MBAM Recovery and Hardware service endpoint) is in the following format:</span></span> <br />
**<span data-ttu-id="ec88a-227">http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="ec88a-227">http://\<servername\>:\<port\>/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>**

<span data-ttu-id="ec88a-228">Par défaut, l’URL de StatusReportingServiceEndpoint (point de terminaison du service de rapport d’État MBAM) est au format suivant:</span><span class="sxs-lookup"><span data-stu-id="ec88a-228">By default, the URL for StatusReportingServiceEndpoint (MBAM Status reporting service endpoint) is in the following format:</span></span><br />
**<span data-ttu-id="ec88a-229">http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="ec88a-229">http://\<servername\>:\<port\>/MBAMComplianceStatusService/StatusReportingService.svc</span></span>**

> [!Note]
> <span data-ttu-id="ec88a-230">L’URL ne doit contenir aucun espace.</span><span class="sxs-lookup"><span data-stu-id="ec88a-230">There should be no spaces in the URL.</span></span>

<span data-ttu-id="ec88a-231">Si l’URL du service est incorrecte, vous devez corriger l’URL du service dans le paramètre de stratégie de groupe suivant:</span><span class="sxs-lookup"><span data-stu-id="ec88a-231">If the service URL is incorrect, you should correct the service URL in the following Group Policy setting:</span></span>

<span data-ttu-id="ec88a-232">**Configuration ordinateur**  >  **Politiques**  >  **Modèles**  >  d’administration **Composants Windows**  >  **MDOP MBAM (gestion de BitLocker)**  >  **Gestion**  >  des clients **Configurer les services de MBAM**</span><span class="sxs-lookup"><span data-stu-id="ec88a-232">**Computer configuration** > **Policies** > **Administrative Templates** > **Windows Components** > **MDOP MBAM (BitLocker Management)** > **Client Management** > **Configure MBAM Services**</span></span>

### <span data-ttu-id="ec88a-233">Problème de connectivité affectant le serveur d’administration MBAM</span><span class="sxs-lookup"><span data-stu-id="ec88a-233">Connectivity issue that affects the MBAM administration server</span></span>

<span data-ttu-id="ec88a-234">L’agent MBAM ne sera pas en mesure de publier des mises à jour de la base de données s’il existe des problèmes de connectivité entre l’agent client et le serveur d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-234">The MBAM agent will be unable to post any updates to the database if connectivity issues exist between the client agent and the MBAM administration server.</span></span> <span data-ttu-id="ec88a-235">Dans le cas présent, vous remarquerez les entrées d’échec de connectivité dans le journal des événements d’administration MBAM sur l’ordinateur client:</span><span class="sxs-lookup"><span data-stu-id="ec88a-235">In this case, you will notice connectivity failure entries in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

<span data-ttu-id="ec88a-236">Vérifications de base:</span><span class="sxs-lookup"><span data-stu-id="ec88a-236">Basic checks:</span></span>

* <span data-ttu-id="ec88a-237">Vérifiez la connectivité de base en exécutant une commande ping sur le serveur d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-237">Verify basic connectivity by pinging the MBAM administration server by name and IP.</span></span> <span data-ttu-id="ec88a-238">Vérifiez si vous pouvez vous connecter au port de service ou de site Web d’administration MBAM à l’aide de Telnet ou Portqry.</span><span class="sxs-lookup"><span data-stu-id="ec88a-238">Check whether you can connect to the MBAM administration website or service port by using telnet or portqry.</span></span>

* <span data-ttu-id="ec88a-239">Vérifiez que le service IIS s’exécute sur le serveur d’administration et de surveillance MBAM et que le service Web MBAM écoute sur le même port que celui configuré sur l’ordinateur client MBAM ( `netstat –ano | find "portnumber"` ).</span><span class="sxs-lookup"><span data-stu-id="ec88a-239">Verify that the IIS service is running on the MBAM administration and monitoring server and that the MBAM web service is listening on the same port that is configured on the MBAM client computer (`netstat –ano | find "portnumber"`).</span></span>

* <span data-ttu-id="ec88a-240">Vérifiez que le numéro de port configuré pour le site Web MBAM utilise le gestionnaire des services Internet (inetmgr).</span><span class="sxs-lookup"><span data-stu-id="ec88a-240">Verify that the port number that is configured for the MBAM website is using IIS Manager (inetmgr).</span></span> <span data-ttu-id="ec88a-241">Assurez-vous que le numéro de port est identique au numéro de port sur lequel le client écoute.</span><span class="sxs-lookup"><span data-stu-id="ec88a-241">Make sure that the port number is the same as the port number on which the client is listening.</span></span> <span data-ttu-id="ec88a-242">Vérifiez que le numéro de port n’est pas partagé par une autre application.</span><span class="sxs-lookup"><span data-stu-id="ec88a-242">Make sure that the port number is not shared by another application.</span></span> <span data-ttu-id="ec88a-243">Par exemple, une autre application sur le serveur ne doit pas utiliser le même port.</span><span class="sxs-lookup"><span data-stu-id="ec88a-243">For example, another application on the server should not be using the same port.</span></span>

* <span data-ttu-id="ec88a-244">S’il y a un pare-feu, assurez-vous que le port est ouvert dans le pare-feu ou le serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="ec88a-244">If there is a firewall, make sure that the port is open in the firewall or proxy server.</span></span>

* <span data-ttu-id="ec88a-245">Si la communication entre le client et le serveur est sécurisée, vérifiez que vous utilisez un certificat SSL valide.</span><span class="sxs-lookup"><span data-stu-id="ec88a-245">If the communication between client and server is secure, make sure that you are using a valid SSL certificate.</span></span>

* <span data-ttu-id="ec88a-246">Vérifiez la connectivité réseau entre le serveur Web et le serveur de base de données sur lequel les données sont envoyées pour insertion.</span><span class="sxs-lookup"><span data-stu-id="ec88a-246">Verify network connectivity between the web server and the database server to which the data is sent for insertion.</span></span> <span data-ttu-id="ec88a-247">Vous pouvez vérifier la connectivité de base de données du serveur Web vers le serveur de base de données à l’aide de l’administrateur de sources de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="ec88a-247">You can check database connectivity from the web server to the database server by using ODBC Data Source Administrator.</span></span> <span data-ttu-id="ec88a-248">Des informations détaillées sur la résolution des problèmes de connexion au serveur SQL Server sont disponibles dans la [procédure de résolution des problèmes de connexion au moteur de base de données SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span><span class="sxs-lookup"><span data-stu-id="ec88a-248">Detailed SQL Server connection troubleshooting information is available in [How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span></span>

#### <span data-ttu-id="ec88a-249">Résoudre les problèmes de connectivité</span><span class="sxs-lookup"><span data-stu-id="ec88a-249">Troubleshooting the connectivity issue</span></span>

<span data-ttu-id="ec88a-250">Assurez-vous que l’URL du service configuré sur le client est correcte.</span><span class="sxs-lookup"><span data-stu-id="ec88a-250">Make sure that the service URL that is configured on the client is correct.</span></span> <span data-ttu-id="ec88a-251">Copiez la valeur de l’URL de KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) du Registre et ouvrez-la dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ec88a-251">Copy the value of the URL for KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) from the registry, and open it in Internet Explorer.</span></span>

<span data-ttu-id="ec88a-252">De même, copiez la valeur de l’URL pour StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**), puis ouvrez-la dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ec88a-252">Similarly, copy the value of the URL for StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**), and open it in Internet Explorer.</span></span>

> [!Note]
> <span data-ttu-id="ec88a-253">Si vous ne parvenez pas à accéder à l’URL à partir de l’ordinateur client, vous devez tester la connectivité réseau de base entre le client et le serveur exécutant IIS.</span><span class="sxs-lookup"><span data-stu-id="ec88a-253">If you cannot browse to the URL from the client computer, you should test basic network connectivity from the client to the server that is running IIS.</span></span> <span data-ttu-id="ec88a-254">Voir points 1, 2, 3 et 4 dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="ec88a-254">See points 1, 2, 3, and 4 in the previous section.</span></span>

<span data-ttu-id="ec88a-255">De plus, consultez les journaux d’application sur le serveur d’administration et de surveillance en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ec88a-255">Additionally, review the Application logs on the administration and monitoring server for any errors.</span></span>

<span data-ttu-id="ec88a-256">Vous pouvez effectuer une trace réseau concomitant entre le client et le serveur, puis examiner la trace pour déterminer la cause de l’échec de connexion entre l’agent client et le serveur d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-256">You can make a concurrent network trace between the client and the server, and review the trace to determine the cause of connection failure between the client agent and the MBAM administration server.</span></span>

> [!Note]
> <span data-ttu-id="ec88a-257">Si vous pouvez accéder aux URL du service à partir de l’ordinateur client et qu’il y a des entrées d’erreur de connectivité dans les journaux des événements d’administration MBAM, cela peut être dû à un échec de connectivité entre le serveur d’administration et le serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="ec88a-257">If you can browse to the service URLs from the client computer and there are connectivity error entries in the MBAM admin event logs, this might be because of a connectivity failure between the administration server and the database server.</span></span>

<span data-ttu-id="ec88a-258">Si vous parvenez à parcourir les deux URL de service, et qu’il existe une connectivité entre le client et le serveur en cours d’exécution, le service IIS fonctionne.</span><span class="sxs-lookup"><span data-stu-id="ec88a-258">If you can successfully browse to both service URLs, and there is connectivity between the client and the server that is running, IIS is working.</span></span> <span data-ttu-id="ec88a-259">Toutefois, il est possible qu’il y ait un problème de communication entre le serveur qui exécute les services Internet et le serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="ec88a-259">However, there may be a problem in communication between the server that is running IIS and the database server.</span></span>

<span data-ttu-id="ec88a-260">Les services MBAM peuvent ne pas être en mesure de se connecter au serveur de base de données en raison d’un problème de réseau ou d’un paramètre de chaîne de connexion de base de données incorrect.</span><span class="sxs-lookup"><span data-stu-id="ec88a-260">The MBAM services may be unable to connect to the database server because of a network issue or an incorrect database connection string setting.</span></span> <span data-ttu-id="ec88a-261">Passez en revue les journaux d’application sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="ec88a-261">Review the Application logs on the administration and monitoring server.</span></span> <span data-ttu-id="ec88a-262">Des entrées d’erreur ou des avertissements provenant de sources ASP.NET 2.0.50727.0 similaires à ceux de l’entrée de journal suivante peuvent s’afficher:</span><span class="sxs-lookup"><span data-stu-id="ec88a-262">You might see errors entries or warnings from source ASP.NET 2.0.50727.0 that resemble the following log entry:</span></span>

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <span data-ttu-id="ec88a-263">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="ec88a-263">Possible causes</span></span>

##### <span data-ttu-id="ec88a-264">Cause 1</span><span class="sxs-lookup"><span data-stu-id="ec88a-264">Cause 1</span></span>

<span data-ttu-id="ec88a-265">L’administrateur a pu spécifier un nom de l’instance de base de données ou un nom de base de données non valide lors de l’installation des composants serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="ec88a-265">The administrator may have specified an invalid database instance name/database name during installation of administration and monitoring server components.</span></span>

<span data-ttu-id="ec88a-266">Vous pouvez vérifier et corriger les chaînes de connexion de la base de données à l’aide de la console de gestion IIS.</span><span class="sxs-lookup"><span data-stu-id="ec88a-266">You can verify and correct the database connection strings by using the IIS Management console.</span></span> <span data-ttu-id="ec88a-267">Pour ce faire, ouvrez le gestionnaire des services Internet et naviguez jusqu’à l’administration et à la surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec88a-267">To do this, open IIS Manager, and browse to Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="ec88a-268">Pour chaque service figurant sur le côté gauche, procédez comme suit pour modifier les chaînes de connexion de base de données:</span><span class="sxs-lookup"><span data-stu-id="ec88a-268">For each service that is listed on the left side, follow these steps to change the database connection strings:</span></span>

1. <span data-ttu-id="ec88a-269">Dans l' **affichage fonctionnalités**, double-sélectionnez **chaînes de connexion**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-269">In **Features View**, double-select **Connection Strings**.</span></span>

2. <span data-ttu-id="ec88a-270">Dans la page **chaînes de connexion** , sélectionnez la chaîne de connexion que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="ec88a-270">On the **Connection Strings** page, select the connection string that you want to change.</span></span>

3. <span data-ttu-id="ec88a-271">Dans le volet **actions** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-271">In the **Actions** pane, select **Edit**.</span></span>

4. <span data-ttu-id="ec88a-272">Dans la boîte de dialogue **modifier la chaîne de connexion** , modifiez les propriétés que vous souhaitez modifier, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-272">In the **Edit Connection String** dialog box, change the properties that you want to change, and then select **OK**.</span></span>

##### <span data-ttu-id="ec88a-273">Cause 2</span><span class="sxs-lookup"><span data-stu-id="ec88a-273">Cause 2</span></span>

<span data-ttu-id="ec88a-274">Port SQL Server bloqué dans le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="ec88a-274">SQL Server port blocked in firewall.</span></span> <span data-ttu-id="ec88a-275">Vérifiez le numéro de port sur lequel SQL Server est configuré pour l’écoute et assurez-vous que le port est ouvert dans le pare-feu entre le serveur d’administration et le serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="ec88a-275">Verify the port number to which SQL Server is configured to listen, and make sure that the port is open in the firewall between the administration server and database server.</span></span>

##### <span data-ttu-id="ec88a-276">Cause 3</span><span class="sxs-lookup"><span data-stu-id="ec88a-276">Cause 3</span></span>

<span data-ttu-id="ec88a-277">Liaisons TCP/IP incorrectes SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ec88a-277">Incorrect SQL server TCP/IP bindings.</span></span> <span data-ttu-id="ec88a-278">Vérifiez les liaisons TCP/IP SQL dans le gestionnaire de configuration SQL Server sur le serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="ec88a-278">Verify SQL TCP/IP bindings in SQL Server Configuration Manager on the database server.</span></span> <span data-ttu-id="ec88a-279">MBAM doit être activé pour la connexion à la base de données par le biais de protocoles TCP/IP et de canaux nommés.</span><span class="sxs-lookup"><span data-stu-id="ec88a-279">MBAM requires that the TCP/IP and Named Pipes protocols are enabled to connect to the database.</span></span>

##### <span data-ttu-id="ec88a-280">Cause 4</span><span class="sxs-lookup"><span data-stu-id="ec88a-280">Cause 4</span></span>

<span data-ttu-id="ec88a-281">Le compte de service NT Nt\service ou le compte d’ordinateur du serveur d’administration MBAM ne disposent pas des autorisations nécessaires pour la connexion à la base de données SQL.</span><span class="sxs-lookup"><span data-stu-id="ec88a-281">The NT Authority\Network Service account or the MBAM Administration Server’s computer account doesn't have the required permissions to connect to the SQL database.</span></span>

<span data-ttu-id="ec88a-282">Lors de l’installation des composants de base de données sur le serveur de base de données, le programme d’installation crée deux groupes locaux: audit de la conformité MBAM et accès aux bases de données et de récupération MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-282">During the installation of database components on the database server, the installer creates two local groups: MBAM Compliance Auditing DB Access and MBAM Recovery and Hardware DB Access.</span></span>

<span data-ttu-id="ec88a-283">Le compte de service NT Authority\Network, le compte d’ordinateur du serveur d’administration MBAM et l’utilisateur qui installe les composants de base de données sont ajoutés automatiquement à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="ec88a-283">The NT Authority\Network Service account, the MBAM administration server’s computer account, and the user who installs the database components are automatically added to these groups.</span></span>

<span data-ttu-id="ec88a-284">Ces groupes disposent des autorisations requises sur la base de données au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="ec88a-284">These groups are granted the required permissions on the database during the installation.</span></span> <span data-ttu-id="ec88a-285">Tous les utilisateurs qui font partie de ce groupe reçoivent automatiquement les autorisations requises sur la base de données.</span><span class="sxs-lookup"><span data-stu-id="ec88a-285">All users who are part of this group automatically receive the required permissions on the database.</span></span>

<span data-ttu-id="ec88a-286">Le service Web n’est pas connecté au serveur de base de données en raison d’un problème d’autorisations si une ou plusieurs des conditions suivantes sont remplies:</span><span class="sxs-lookup"><span data-stu-id="ec88a-286">The web service may not connect to the database server because of a permissions issue if one or more of the following conditions are true:</span></span>

* <span data-ttu-id="ec88a-287">Les groupes mentionnés précédemment sont supprimés des groupes locaux sur le serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="ec88a-287">The groups that were mentioned earlier are removed from the local groups on the database server.</span></span>

* <span data-ttu-id="ec88a-288">Le compte de service NT Nt\service et le compte d’ordinateur du serveur d’administration MBAM ne sont pas membres de ces groupes.</span><span class="sxs-lookup"><span data-stu-id="ec88a-288">The NT Authority\Network Service account and the MBAM administration server’s computer account are not members of these groups.</span></span>

* <span data-ttu-id="ec88a-289">Ces groupes ne disposent pas des autorisations requises sur la base de données.</span><span class="sxs-lookup"><span data-stu-id="ec88a-289">These groups do not have the required permissions on the database.</span></span>

<span data-ttu-id="ec88a-290">Vous remarquerez les erreurs liées aux autorisations dans les journaux de l’application sur le serveur d’administration et de surveillance de MBAM si l’une des conditions précédentes est vraie.</span><span class="sxs-lookup"><span data-stu-id="ec88a-290">You will notice permissions-related errors in the Application logs on the MBAM administration and monitoring server if any of the previous conditions are true.</span></span> <span data-ttu-id="ec88a-291">Dans ce cas, vous devez ajouter manuellement le compte de service NT Nt\service et le compte d’ordinateur du serveur d’administration MBAM, et leur accorder un rôle public au niveau du serveur sur le serveur de base de données SQL qui utilise SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ec88a-291">In that case, you should manually add the NT Authority\Network Service account and MBAM administration server’s computer account and grant them a server-wide public role on the SQL database server that is using SQL Server Management Studio (https://msdn.microsoft.com/library/aa337562.aspx).</span></span>

#### <span data-ttu-id="ec88a-292">Examiner les journaux de service Web</span><span class="sxs-lookup"><span data-stu-id="ec88a-292">Review the web service logs</span></span>

<span data-ttu-id="ec88a-293">Si aucun événement n’est consigné dans les journaux d’application sur le serveur d’administration MBAM, il est temps de passer en revue les journaux de service Web (. svclog) du service Web MBAM hébergé sur le serveur d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-293">If no events are logged in the Application logs on the MBAM administration server, it’s time to review the web service logs (.svclog) of the MBAM web service that is hosted on the MBAM administration and monitoring server.</span></span> <span data-ttu-id="ec88a-294">Pour afficher le fichier journal, vous devez utiliser l’outil visionneuse de suivi de service (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx .</span><span class="sxs-lookup"><span data-stu-id="ec88a-294">You will have to use the Service Trace Viewer Tool (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx to view the log file.</span></span>

<span data-ttu-id="ec88a-295">Vous devez examiner essentiellement les journaux de suivi de service de RecoveryandHardwareService et ComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="ec88a-295">You should primarily investigate the service trace logs of RecoveryandHardwareService and ComplianceStatusService.</span></span> <span data-ttu-id="ec88a-296">Par défaut, les journaux de service Web se trouvent dans le dossier Solution\Logs de gestion de C:\inetpub\Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec88a-296">By default, web service logs are located in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span> <span data-ttu-id="ec88a-297">Là, chaque service écrit son fichier. svclog dans son propre dossier.</span><span class="sxs-lookup"><span data-stu-id="ec88a-297">There, each service writes its .svclog file under its own folder.</span></span>

<span data-ttu-id="ec88a-298">Examinez l’activité du journal de suivi des services pour toutes les entrées d’erreur ou d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="ec88a-298">Review the activity in the service trace log for any error or warning entries.</span></span> <span data-ttu-id="ec88a-299">Par défaut, les entrées d’erreur sont mises en surbrillance en rouge.</span><span class="sxs-lookup"><span data-stu-id="ec88a-299">By default, error entries are highlighted in red.</span></span> <span data-ttu-id="ec88a-300">Sélectionnez la description d’erreur dans le volet droit de la visionneuse de suivi pour afficher des informations détaillées sur l’entrée d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ec88a-300">Select the error description on the right pane of the trace viewer to view detailed information about the error entry.</span></span> <span data-ttu-id="ec88a-301">Voici un exemple d’entrée d’erreur du journal de suivi:</span><span class="sxs-lookup"><span data-stu-id="ec88a-301">The following is a sample error entry from the trace log:</span></span>

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <span data-ttu-id="ec88a-302">Nouvelle installation ou reconfiguration de l’infrastructure MBAM</span><span class="sxs-lookup"><span data-stu-id="ec88a-302">Re-installation or reconfiguration of MBAM infrastructure</span></span>

<span data-ttu-id="ec88a-303">Pour réinstaller ou reconfigurer l’infrastructure MBAM, vous devez connaître les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="ec88a-303">To re-install or reconfigure MBAM infrastructure, you must know the following things:</span></span>

* <span data-ttu-id="ec88a-304">Compte du pool d’applications</span><span class="sxs-lookup"><span data-stu-id="ec88a-304">Application Pool account</span></span>

* <span data-ttu-id="ec88a-305">Groupes MBAM (assistance technique avancée, groupe utilisateurs de rapports)</span><span class="sxs-lookup"><span data-stu-id="ec88a-305">MBAM Groups (Helpdesk, Advanced, Report Users Group)</span></span>

* <span data-ttu-id="ec88a-306">URL des rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="ec88a-306">MBAM Reports URL</span></span>

* <span data-ttu-id="ec88a-307">Nom SQL Server et noms de base de données</span><span class="sxs-lookup"><span data-stu-id="ec88a-307">SQL Server name and database names</span></span>

* <span data-ttu-id="ec88a-308">MBAM les comptes et les ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ec88a-308">MBAM ReadWrite and ReadOnly Accounts</span></span>

### <span data-ttu-id="ec88a-309">Compte du pool d’applications</span><span class="sxs-lookup"><span data-stu-id="ec88a-309">Application Pool account</span></span>

<span data-ttu-id="ec88a-310">Pour trouver le compte du pool d’applications, connectez-vous au serveur Web MBAM, ouvrez le **Gestionnaire des services Internet (IIS)**, puis sélectionnez **pools d’applications**:</span><span class="sxs-lookup"><span data-stu-id="ec88a-310">To find the Application Pool account, log on to the MBAM Web Server, open **Internet Information Services (IIS) Manager**, and then select **Application Pools**:</span></span>

![pools d’applications](images/troubleshooting-MBAM-installation-1.png)

<span data-ttu-id="ec88a-312">Le nom de principal de service (SPN) doit être défini dans ce compte.</span><span class="sxs-lookup"><span data-stu-id="ec88a-312">The Service Principal Name (SPN) must be set in this account.</span></span> <span data-ttu-id="ec88a-313">Ce paramètre est important pour la fonctionnalité de MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-313">This setting is very important to the functionality of MBAM.</span></span>

### <span data-ttu-id="ec88a-314">Groupes MBAM (support technique, avancé, groupe utilisateurs de rapports et URL des rapports)</span><span class="sxs-lookup"><span data-stu-id="ec88a-314">MBAM Groups (Helpdesk, Advanced, Report Users Group and Reports URL)</span></span>

![Groupes MBAM](images/troubleshooting-MBAM-installation-2.png)

<span data-ttu-id="ec88a-316">Cela fournit des informations telles que le groupe assistance, le groupe assistance avancée, le groupe utilisateurs de rapports et l’URL des rapports MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-316">This provides information such as Helpdesk Group, Advanced Helpdesk Group, Report Users group, and MBAM Reports URL.</span></span> <span data-ttu-id="ec88a-317">L’URL des rapports MBAM doit être fournie dans le programme d’installation d’MBAM et doit prendre la forme: http (s)://servername/ReportServer.</span><span class="sxs-lookup"><span data-stu-id="ec88a-317">The MBAM Reports URL must be provided in the MBAM setup and should read as: http(s)://servername/ReportServer.</span></span>

### <span data-ttu-id="ec88a-318">Noms de nom et de base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="ec88a-318">SQL Server name and database (DB) names</span></span>

<span data-ttu-id="ec88a-319">Pour savoir quels sont les noms et instances SQL Server hébergeant les DBs MBAM, connectez-vous au serveur Web MBAM (IIS) et naviguez jusqu’à la sous-clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="ec88a-319">To find the SQL Server names and instances hosting the MBAM DBs, log on to the MBAM Web (IIS) server and browse to the folowing registry subkey:</span></span>

**<span data-ttu-id="ec88a-320">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web</span><span class="sxs-lookup"><span data-stu-id="ec88a-320">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web</span></span>**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

<span data-ttu-id="ec88a-322">Les parties mises en surbrillance sont des chaînes de connexion.</span><span class="sxs-lookup"><span data-stu-id="ec88a-322">The highlighted portions are connection strings.</span></span> <span data-ttu-id="ec88a-323">Celles-ci doivent avoir le nom SQL Server, les noms de base de données et les instances (s’ils sont nommés).</span><span class="sxs-lookup"><span data-stu-id="ec88a-323">These should have the SQL Server name, database names, and instances (if named).</span></span>

### <span data-ttu-id="ec88a-324">MBAM les comptes et les ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ec88a-324">MBAM ReadWrite and ReadOnly accounts</span></span>

<span data-ttu-id="ec88a-325">Ces informations seront dans la base de données SQL Server, pour lesquelles nous avons déjà trouvé le nom du serveur Web.</span><span class="sxs-lookup"><span data-stu-id="ec88a-325">This information will be in the SQL Server database, for which we already found the name from the web server.</span></span>

#### <span data-ttu-id="ec88a-326">Compte ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ec88a-326">ReadWrite account</span></span>

1. <span data-ttu-id="ec88a-327">Connectez-vous à SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="ec88a-327">Log in to the SQL Management Studio.</span></span>

2. <span data-ttu-id="ec88a-328">Dans MBAM, cliquez avec le bouton droit sur **restauration et matériel**, sélectionnez **Propriétés**, puis sélectionnez **autorisations**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-328">Right-click **MBAM Recovery and Hardware**, select **Properties**, and then select **Permissions**.</span></span>

<span data-ttu-id="ec88a-329">Par exemple, le nom du compte laboratoire est **MBAMWrite**.</span><span class="sxs-lookup"><span data-stu-id="ec88a-329">For example, The the lab account name is **MBAMWrite**.</span></span> <span data-ttu-id="ec88a-330">Le pool d’applications et les comptes ReadWrite sont définis en tant que tels.</span><span class="sxs-lookup"><span data-stu-id="ec88a-330">The Application Pool and ReadWrite accounts are set to be the same.</span></span>

![SQL DB](images/troubleshooting-MBAM-installation-4.png)

![Propriétés de BDD](images/troubleshooting-MBAM-installation-5.png)

<span data-ttu-id="ec88a-333">Accédez à **sécurité** , puis **Connectez** -vous dans SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="ec88a-333">Browse to **Security** and then **Logins** in SQL Management Studio.</span></span> <span data-ttu-id="ec88a-334">Naviguez jusqu’au compte affiché dans la capture d’écran précédente.</span><span class="sxs-lookup"><span data-stu-id="ec88a-334">Browse to the account shown in the previous screenshot.</span></span>

![Sécurité SQL](images/troubleshooting-MBAM-installation-6.png)

<span data-ttu-id="ec88a-336">Cliquez avec le bouton droit sur les comptes, accédez à l’image **mappage des utilisateurs**et recherchez la base de données de récupération et de MBAM:</span><span class="sxs-lookup"><span data-stu-id="ec88a-336">Right-click the accounts, go to **Properties User Mapping**, and locate the MBAM Recovery and Hardware database:</span></span>

![Mappage utilisateur](images/troubleshooting-MBAM-installation-7.png)

#### <span data-ttu-id="ec88a-338">Compte ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ec88a-338">ReadOnly account</span></span>

<span data-ttu-id="ec88a-339">Ouvrez le gestionnaire de configuration SQL Server Reporting Services sur le serveur SSRS.</span><span class="sxs-lookup"><span data-stu-id="ec88a-339">Open SQL Server Reporting Services Configuration Manager on the SSRS Server.</span></span> <span data-ttu-id="ec88a-340">Sélectionnez **URL du gestionnaire de rapports**, puis parcourez les **URL**:</span><span class="sxs-lookup"><span data-stu-id="ec88a-340">Select **Report Manager URL**, and then browse the **URLs**:</span></span>

![Gestionnaire de rapports](images/troubleshooting-MBAM-installation-8.png)

<span data-ttu-id="ec88a-342">Sélectionnez **administration et surveillance de Microsoft BitLocker**:</span><span class="sxs-lookup"><span data-stu-id="ec88a-342">Select **Microsoft Bitlocker Administration and Monitoring**:</span></span>

![Administration et analyse de BitLocker](images/troubleshooting-MBAM-installation-9.png)

<span data-ttu-id="ec88a-344">Sélectionnez **MaltaDatasource**:</span><span class="sxs-lookup"><span data-stu-id="ec88a-344">Select **MaltaDatasource**:</span></span>

![Bases](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

<span data-ttu-id="ec88a-347">MaltaDataSource doit avoir le nom de compte ReadOnly et doit être utilisé dans la configuration MBAM.</span><span class="sxs-lookup"><span data-stu-id="ec88a-347">MaltaDataSource should have the ReadOnly Account name and should be used in MBAM setup.</span></span>

## <span data-ttu-id="ec88a-348">Référence</span><span class="sxs-lookup"><span data-stu-id="ec88a-348">Reference</span></span>

<span data-ttu-id="ec88a-349">Pour plus d’informations, consultez les articles suivants:</span><span class="sxs-lookup"><span data-stu-id="ec88a-349">For more information, see the following articles:</span></span>

[<span data-ttu-id="ec88a-350">Déploiement de MBAM 2,5 dans une configuration autonome</span><span class="sxs-lookup"><span data-stu-id="ec88a-350">Deploying MBAM 2.5 in a standalone configuration</span></span>](https://support.microsoft.com/help/3046555)

[<span data-ttu-id="ec88a-351">Microsoft BitLocker Administration and Monitoring2.5</span><span class="sxs-lookup"><span data-stu-id="ec88a-351">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)

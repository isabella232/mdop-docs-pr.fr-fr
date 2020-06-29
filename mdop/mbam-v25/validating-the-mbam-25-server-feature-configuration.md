---
title: Validation de la configuration des composants serveur de MBAM2.5
description: Validation de la configuration des composants serveur de MBAM2.5
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812143"
---
# <span data-ttu-id="b4194-103">Validation de la configuration des composants serveur de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b4194-103">Validating the MBAM 2.5 Server Feature Configuration</span></span>


<span data-ttu-id="b4194-104">Lorsque vous avez terminé le déploiement de la fonctionnalité serveur d’administration et de surveillance de BitLocker (MBAM 2,5), nous vous recommandons de valider le déploiement pour vous assurer que toutes les fonctionnalités ont bien été configurées.</span><span class="sxs-lookup"><span data-stu-id="b4194-104">When you finish the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server feature deployment, we recommend that you validate the deployment to ensure that all features have been successfully configured.</span></span> <span data-ttu-id="b4194-105">Utilisez la procédure qui correspond à la topologie (intégration autonome ou System Center Configuration Manager) que vous avez déployée.</span><span class="sxs-lookup"><span data-stu-id="b4194-105">Use the procedure that matches the topology (Stand-alone or System Center Configuration Manager Integration) that you deployed.</span></span>

## <span data-ttu-id="b4194-106">Validation du déploiement du serveur MBAM avec la topologie autonome</span><span class="sxs-lookup"><span data-stu-id="b4194-106">Validating the MBAM Server deployment with the Stand-alone topology</span></span>


<span data-ttu-id="b4194-107">Procédez comme suit pour valider votre déploiement MBAM Server avec la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="b4194-107">Use the following steps to validate your MBAM Server deployment with the Stand-alone topology.</span></span>

**<span data-ttu-id="b4194-108">Pour valider un déploiement de serveur MBAM autonome</span><span class="sxs-lookup"><span data-stu-id="b4194-108">To validate a Stand-alone MBAM Server deployment</span></span>**

1.  <span data-ttu-id="b4194-109">Sur chaque serveur sur lequel est déployée une fonctionnalité MBAM **Control Panel** , cliquez sur programmes &gt; **Programs** &gt; **et fonctionnalités**du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b4194-109">On each server where an MBAM feature is deployed, click **Control Panel** &gt; **Programs** &gt; **Programs and Features**.</span></span> <span data-ttu-id="b4194-110">Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="b4194-110">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

    **<span data-ttu-id="b4194-111">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4194-111">Note</span></span>**  
    <span data-ttu-id="b4194-112">Pour effectuer la validation, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="b4194-112">To do the validation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="b4194-113">Sur le serveur sur lequel est configuré la base de données de récupération, ouvrez SQL Server Management Studio, puis vérifiez que la base de données **MBAM et de récupération** de la base de données est configurée.</span><span class="sxs-lookup"><span data-stu-id="b4194-113">On the server where the Recovery Database is configured, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is configured.</span></span>

3.  <span data-ttu-id="b4194-114">Sur le serveur sur lequel la base de données d’audit et de conformité est configurée, ouvrez SQL Server Management Studio, puis vérifiez que la **base de données d’état de conformité MBAM** est configurée.</span><span class="sxs-lookup"><span data-stu-id="b4194-114">On the server where the Compliance and Audit Database is configured, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is configured.</span></span>

4.  <span data-ttu-id="b4194-115">Sur le serveur sur lequel la fonctionnalité de création de rapports est configurée, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’au site «Accueil» du site SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="b4194-115">On the server where the Reports feature is configured, open a web browser with administrative credentials and browse to the "Home" of the SQL Server Reporting Services site.</span></span>

    <span data-ttu-id="b4194-116">L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services est le suivant:</span><span class="sxs-lookup"><span data-stu-id="b4194-116">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

    <span data-ttu-id="b4194-117">http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *port* &gt; /reports.aspx</span><span class="sxs-lookup"><span data-stu-id="b4194-117">http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports.aspx</span></span>

    <span data-ttu-id="b4194-118">Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration Reporting Services et sélectionnez les instances que vous avez spécifiées lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="b4194-118">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that you specified during setup.</span></span>

5.  <span data-ttu-id="b4194-119">Confirmez qu’un dossier de rapports intitulé **Microsoft BitLocker administration et analyse** contient une source de données appelée **MaltaDataSource** ainsi que les dossiers de langue.</span><span class="sxs-lookup"><span data-stu-id="b4194-119">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** as well as the language folders.</span></span> <span data-ttu-id="b4194-120">La source de données contient des dossiers avec des noms qui représentent des langues (par exemple, en-US).</span><span class="sxs-lookup"><span data-stu-id="b4194-120">The data source contains folders with names that represent languages (for example, en-us).</span></span> <span data-ttu-id="b4194-121">Les rapports se trouvent dans les dossiers de langue.</span><span class="sxs-lookup"><span data-stu-id="b4194-121">The reports are in the language folders.</span></span>

    **<span data-ttu-id="b4194-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4194-122">Note</span></span>**  
    <span data-ttu-id="b4194-123">Si SQL Server Reporting Services (SSRS) a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *port* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;</span><span class="sxs-lookup"><span data-stu-id="b4194-123">If SQL Server Reporting Services (SSRS) was configured as a named instance, the URL should resemble the following: http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports\_&lt;*SSRSInstanceName*&gt;</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. <span data-ttu-id="b4194-124">Sur le serveur sur lequel la fonctionnalité de site Web Administration et contrôle est configurée, exécutez le **Gestionnaire de serveur**, accédez aux **rôles**, puis sélectionnez **serveur Web (IIS)** &gt; **Gestionnaire des services Internet (IIS**).</span><span class="sxs-lookup"><span data-stu-id="b4194-124">On the server where the Administration and Monitoring Website feature is configured, run **Server Manager**, browse to **Roles**, and then select **Web Server (IIS)** &gt; **Internet Information Services (IIS) Manager**.</span></span>

7. <span data-ttu-id="b4194-125">Dans **connexions**, accédez à \* &lt; nom &gt; \* de l’ordinateur et sélectionnez **sites** &gt; **administration et analyse de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="b4194-125">In **Connections**, browse to *&lt;computer name&gt;* and select **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="b4194-126">Vérifiez que les éléments suivants s’affichent:</span><span class="sxs-lookup"><span data-stu-id="b4194-126">Verify that the following are listed:</span></span>

   -   **<span data-ttu-id="b4194-127">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="b4194-127">MBAMAdministrationService</span></span>**

   -   **<span data-ttu-id="b4194-128">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="b4194-128">MBAMComplianceStatusService</span></span>**

   -   **<span data-ttu-id="b4194-129">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="b4194-129">MBAMRecoveryAndHardwareService</span></span>**

8. <span data-ttu-id="b4194-130">Sur le serveur sur lequel sont configurés le site Web d’administration et de surveillance et le portail libre-service, ouvrez un navigateur Web contenant les informations d’identification d’administration.</span><span class="sxs-lookup"><span data-stu-id="b4194-130">On the server where the Administration and Monitoring Website and Self-Service Portal are configured, open a web browser with administrative credentials.</span></span>

9. <span data-ttu-id="b4194-131">Naviguez jusqu’au site Web suivant pour vérifier qu’il se charge correctement:</span><span class="sxs-lookup"><span data-stu-id="b4194-131">Browse to the following websites to verify that they load successfully:</span></span>

   -   <span data-ttu-id="b4194-132">HTTPS (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /helpdesk/: confirmez chacun des liens pour la navigation et les rapports</span><span class="sxs-lookup"><span data-stu-id="b4194-132">https(s)://&lt;*MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/HelpDesk/ - confirm each of the links for navigation and reports</span></span>

   -   <span data-ttu-id="b4194-133">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /selfservice/</span><span class="sxs-lookup"><span data-stu-id="b4194-133">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/SelfService/</span></span>

   **<span data-ttu-id="b4194-134">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4194-134">Note</span></span>**  
   <span data-ttu-id="b4194-135">Il est supposé que vous avez configuré les fonctionnalités serveur sur le port par défaut sans chiffrement réseau.</span><span class="sxs-lookup"><span data-stu-id="b4194-135">It is assumed that you configured the server features on the default port without network encryption.</span></span> <span data-ttu-id="b4194-136">Si vous avez configuré les fonctionnalités du serveur sur un autre port ou répertoire virtuel, modifiez les URL pour inclure le port approprié, par exemple:</span><span class="sxs-lookup"><span data-stu-id="b4194-136">If you configured the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example:</span></span>

   <span data-ttu-id="b4194-137">http (s):// &lt; *nom d’hôte* &gt; : &lt; *port* &gt; /helpdesk/</span><span class="sxs-lookup"><span data-stu-id="b4194-137">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/HelpDesk/</span></span>

   <span data-ttu-id="b4194-138">http (s):// &lt; *nom d’hôte* &gt; : &lt; *port* &gt; / &lt; *VirtualDirectory*&gt;/</span><span class="sxs-lookup"><span data-stu-id="b4194-138">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/&lt;*virtualdirectory*&gt;/</span></span>

   <span data-ttu-id="b4194-139">Si les fonctionnalités du serveur étaient configurées avec le chiffrement réseau, modifiez http://sur https://.</span><span class="sxs-lookup"><span data-stu-id="b4194-139">If the server features were configured with network encryption, change http:// to https://.</span></span>



10. <span data-ttu-id="b4194-140">Accédez aux services Web suivants pour vérifier qu’ils se chargent correctement.</span><span class="sxs-lookup"><span data-stu-id="b4194-140">Browse to the following web services to verify that they load successfully.</span></span> <span data-ttu-id="b4194-141">Une page s’ouvre pour indiquer que le service est en cours d’exécution, mais que la page n’affiche aucune métadonnée.</span><span class="sxs-lookup"><span data-stu-id="b4194-141">A page opens to indicate that the service is running, but the page does not display any metadata.</span></span>

    -   <span data-ttu-id="b4194-142">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="b4194-142">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>

    -   <span data-ttu-id="b4194-143">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="b4194-143">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>

    -   <span data-ttu-id="b4194-144">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="b4194-144">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>

    -   <span data-ttu-id="b4194-145">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="b4194-145">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>

## <span data-ttu-id="b4194-146">Validation du déploiement du serveur MBAM avec la topologie d’intégration de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b4194-146">Validating the MBAM Server deployment with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="b4194-147">Procédez comme suit pour valider votre déploiement MBAM avec la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b4194-147">Use the following steps to validate your MBAM deployment with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="b4194-148">Suivez la procédure de validation qui correspond à la version de Configuration Manager que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="b4194-148">Complete the validation steps that match the version of Configuration Manager that you are using.</span></span>

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a><span data-ttu-id="b4194-149">Validation du déploiement du serveur MBAM avec System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b4194-149">Validating the MBAM Server deployment with System Center 2012 Configuration Manager</span></span>

<span data-ttu-id="b4194-150">Suivez ces étapes pour valider votre déploiement MBAM Server lorsque vous utilisez MBAM avec System Center 2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b4194-150">Use these steps to validate your MBAM Server deployment when you are using MBAM with System Center 2012 Configuration Manager.</span></span>

**<span data-ttu-id="b4194-151">Pour valider un déploiement d’intégration de Configuration Manager MBAM serveur – System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b4194-151">To validate a Configuration Manager Integration MBAM Server deployment – System Center 2012 Configuration Manager</span></span>**

1.  <span data-ttu-id="b4194-152">Sur le serveur sur lequel System Center 2012 Configuration Manager est déployé, ouvrez **programmes et fonctionnalités** dans **le panneau**de configuration, puis vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b4194-152">On the server where System Center 2012 Configuration Manager is deployed, open **Programs and Features** in **Control Panel**, and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="b4194-153">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4194-153">Note</span></span>**  
    <span data-ttu-id="b4194-154">Pour valider la configuration, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="b4194-154">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="b4194-155">Dans la console Configuration Manager, cliquez sur collections de périphériques **et** de l’espace de travail de gestion des éléments &gt; **Device Collections**et vérifiez qu’une nouvelle collection appelée **MBAM les ordinateurs pris en charge** est affichée.</span><span class="sxs-lookup"><span data-stu-id="b4194-155">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Device Collections**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="b4194-156">Dans la console Configuration Manager, cliquez sur **analyse** des rapports de rapports d’espace de travail de &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="b4194-156">In the Configuration Manager console, click the **Monitoring** workspace &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

4.  <span data-ttu-id="b4194-157">Vérifiez que le dossier **MBAM** contient des sous-dossiers avec des noms qui représentent différentes langues et que les rapports suivants apparaissent dans chaque sous-dossier de langue:</span><span class="sxs-lookup"><span data-stu-id="b4194-157">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="b4194-158">Compatibilité de l’ordinateur BitLocker</span><span class="sxs-lookup"><span data-stu-id="b4194-158">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="b4194-159">Tableau de bord de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="b4194-159">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="b4194-160">Détails de la conformité à l’entreprise BitLocker</span><span class="sxs-lookup"><span data-stu-id="b4194-160">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="b4194-161">Résumé de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="b4194-161">BitLocker Enterprise Compliance Summary</span></span>

5.  <span data-ttu-id="b4194-162">Dans la console Configuration Manager, cliquez sur éléments de base de la configuration des **ressources et** de la conformité &gt; **Compliance Settings** &gt; **Configuration Baselines**, puis vérifiez que la **protection BitLocker** de base de la configuration est répertoriée.</span><span class="sxs-lookup"><span data-stu-id="b4194-162">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

6.  <span data-ttu-id="b4194-163">Dans la console Configuration Manager, cliquez sur éléments de configuration de éléments **et de conformité** des espaces de travail et &gt; **Compliance Settings** &gt; **Configuration Items**Vérifiez que les nouveaux éléments de configuration suivants s’affichent:</span><span class="sxs-lookup"><span data-stu-id="b4194-163">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="b4194-164">Protection des lecteurs de données fixes BitLocker</span><span class="sxs-lookup"><span data-stu-id="b4194-164">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="b4194-165">Protection des lecteurs du système d’exploitation BitLocker</span><span class="sxs-lookup"><span data-stu-id="b4194-165">BitLocker Operating System Drive Protection</span></span>

### <span data-ttu-id="b4194-166">Validation du déploiement du serveur MBAM avec Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="b4194-166">Validating the MBAM Server deployment with Configuration Manager 2007</span></span>

<span data-ttu-id="b4194-167">Suivez ces étapes pour valider votre déploiement MBAM Server lorsque vous utilisez MBAM avec Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="b4194-167">Use these steps to validate your MBAM Server deployment when you are using MBAM with Configuration Manager 2007.</span></span>

**<span data-ttu-id="b4194-168">Pour valider un déploiement d’intégration de Configuration Manager MBAM serveur – Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="b4194-168">To validate a Configuration Manager Integration MBAM Server deployment – Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="b4194-169">Sur le serveur sur lequel Configuration Manager 2007 est déployé, ouvrez **programmes et fonctionnalités** dans le panneau de configuration, puis vérifiez que le **volet** **administration et analyse de BitLocker Microsoft** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b4194-169">On the server where Configuration Manager 2007 is deployed, open **Programs and Features** on **Control Panel** , and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="b4194-170">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4194-170">Note</span></span>**  
    <span data-ttu-id="b4194-171">Pour valider la configuration, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="b4194-171">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="b4194-172">Dans la console Configuration Manager, cliquez sur **base de données de site &lt; SiteCode &gt;  -  &lt; NomServeur &gt; , &lt; SiteName &gt; ), gestion de l’ordinateur**, puis vérifiez qu’une nouvelle collection appelée MBAM les **ordinateurs pris en charge** est affichée.</span><span class="sxs-lookup"><span data-stu-id="b4194-172">In the Configuration Manager console, click **Site Database &lt;SiteCode&gt; - &lt;ServerName&gt;, &lt;SiteName&gt;), Computer Management**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="b4194-173">Dans la console Configuration Manager **, cliquez sur** &gt; dossiers de **Reporting Services** &gt; rapport \*\* \\\\ &lt; ServerName &gt; \*\* Report services &gt; **Report Folders** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="b4194-173">In the Configuration Manager console, click **Reporting** &gt; **Reporting Services** &gt; **\\\\&lt;ServerName&gt;** &gt; **Report Folders** &gt; **MBAM**.</span></span>

    <span data-ttu-id="b4194-174">Vérifiez que le dossier **MBAM** contient des sous-dossiers avec des noms qui représentent différentes langues et que les rapports suivants apparaissent dans chaque sous-dossier de langue:</span><span class="sxs-lookup"><span data-stu-id="b4194-174">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="b4194-175">Compatibilité de l’ordinateur BitLocker</span><span class="sxs-lookup"><span data-stu-id="b4194-175">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="b4194-176">Tableau de bord de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="b4194-176">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="b4194-177">Détails de la conformité à l’entreprise BitLocker</span><span class="sxs-lookup"><span data-stu-id="b4194-177">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="b4194-178">Résumé de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="b4194-178">BitLocker Enterprise Compliance Summary</span></span>

4.  <span data-ttu-id="b4194-179">Dans la console Configuration Manager, cliquez sur configurations de configuration de la gestion de la **configuration souhaitées** &gt; **Configuration Baselines**, puis vérifiez que la **protection BitLocker** de base de la configuration est répertoriée.</span><span class="sxs-lookup"><span data-stu-id="b4194-179">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

5.  <span data-ttu-id="b4194-180">Dans la console Configuration Manager, cliquez sur éléments de configuration de la **gestion des configurations souhaités** &gt; **Configuration Items**, puis vérifiez que les éléments suivants sont affichés:</span><span class="sxs-lookup"><span data-stu-id="b4194-180">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="b4194-181">Protection des lecteurs de données fixes BitLocker</span><span class="sxs-lookup"><span data-stu-id="b4194-181">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="b4194-182">Protection des lecteurs du système d’exploitation BitLocker</span><span class="sxs-lookup"><span data-stu-id="b4194-182">BitLocker Operating System Drive Protection</span></span>



## <span data-ttu-id="b4194-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4194-183">Related topics</span></span>


[<span data-ttu-id="b4194-184">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b4194-184">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)


## <span data-ttu-id="b4194-185">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="b4194-185">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b4194-186">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="b4194-186">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b4194-187">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b4194-187">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>







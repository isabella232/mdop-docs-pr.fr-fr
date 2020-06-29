---
title: Évaluation de MBAM2.5 dans un environnement de test
description: Évaluation de MBAM2.5 dans un environnement de test
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809785"
---
# <span data-ttu-id="f6dd7-103">Évaluation de MBAM2.5 dans un environnement de test</span><span class="sxs-lookup"><span data-stu-id="f6dd7-103">Evaluating MBAM 2.5 in a Test Environment</span></span>


<span data-ttu-id="f6dd7-104">Cette rubrique décrit comment configurer un environnement de test pour évaluer l’administration et la surveillance de l’utilisation de Microsoft BitLocker (MBAM) 2,5 dans la topologie d’intégration autonome ou System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-104">This topic describes how you can set up a test environment to evaluate Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in the Stand-alone or System Center Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="f6dd7-105">Évaluation de MBAM 2,5 à l’aide de la topologie autonome</span><span class="sxs-lookup"><span data-stu-id="f6dd7-105">Evaluating MBAM 2.5 by using the Stand-alone topology</span></span>


<span data-ttu-id="f6dd7-106">Pour évaluer MBAM à l’aide de la topologie autonome, utilisez les informations du tableau suivant pour installer le logiciel serveur MBAM, puis configurez les fonctionnalités de MBAM Server dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-106">To evaluate MBAM by using the Stand-alone topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span>

**<span data-ttu-id="f6dd7-107">Pour évaluer MBAM 2,5 à l’aide de la topologie autonome</span><span class="sxs-lookup"><span data-stu-id="f6dd7-107">To evaluate MBAM 2.5 by using the Stand-alone topology</span></span>**

1. <span data-ttu-id="f6dd7-108">Avant l’installation d’MBAM, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-108">Before installing MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f6dd7-109">Tâche</span><span class="sxs-lookup"><span data-stu-id="f6dd7-109">Task</span></span></th>
   <th align="left"><span data-ttu-id="f6dd7-110">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="f6dd7-110">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-111">Vérifiez que vous avez installé tous les logiciels requis.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-111">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="f6dd7-112">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="f6dd7-112">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-113">Vérifiez le matériel, la RAM et d’autres spécifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-113">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="f6dd7-114">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-115">Passez en revue les conditions préalables à l’utilisation de Windows PowerShell Si vous envisagez d’utiliser les applets de contrôle pour configurer MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-115">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="f6dd7-116">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f6dd7-116">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f6dd7-117">Installez le logiciel serveur MBAM, puis configurez les fonctionnalités de votre choix.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-117">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f6dd7-118">Tâche</span><span class="sxs-lookup"><span data-stu-id="f6dd7-118">Task</span></span></th>
   <th align="left"><span data-ttu-id="f6dd7-119">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="f6dd7-119">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-120">Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous voulez configurer une fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-120">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="f6dd7-121">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-121">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-122">Configurez la base de données d’audit et de conformité avec la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-122">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="f6dd7-123">Comment configurer les bases de données MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-123">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-124">Configurer la fonctionnalité rapports.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-124">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="f6dd7-125">Configuration des rapports MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-125">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-126">Configurez les applications Web.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-126">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="f6dd7-127">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-127">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="f6dd7-128">Sur un ordinateur client, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-128">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="f6dd7-129">Installez le client MBAM sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-129">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="f6dd7-130">Appliquez les objets de stratégie de groupe MBAM à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-130">Apply the MBAM Group Policy Objects (GPOs) to the computer.</span></span>

   3.  <span data-ttu-id="f6dd7-131">Définissez les clés de Registre suivantes pour forcer le client MBAM à se réveiller plus rapidement et à intervalles réguliers:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-131">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="f6dd7-132">Remarque</span><span class="sxs-lookup"><span data-stu-id="f6dd7-132">Note</span></span>**  
       <span data-ttu-id="f6dd7-133">Comme ces clés réactivent le client MBAM toutes les minutes, nous vous recommandons d’utiliser les paramètres de clé de registre suivants uniquement dans un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-133">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="f6dd7-134">Redémarrez le **service client de gestion BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-134">Restart the **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="f6dd7-135">Évaluation de MBAM 2,5 à l’aide de la topologie d’intégration System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6dd7-135">Evaluating MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>


<span data-ttu-id="f6dd7-136">Pour évaluer MBAM à l’aide de la topologie d’intégration de Configuration Manager, utilisez les informations du tableau suivant pour installer le logiciel serveur MBAM, puis configurez les fonctionnalités de MBAM Server dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-136">To evaluate MBAM by using the Configuration Manager Integration topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span> <span data-ttu-id="f6dd7-137">Après avoir installé le client MBAM sur un ordinateur client, vous devez effectuer des étapes supplémentaires pour forcer le client MBAM à signaler l’état de l’ordinateur au MBAM plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-137">After installing the MBAM Client on a client computer, you will complete additional steps to force the MBAM Client to report the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="f6dd7-138">Pour évaluer MBAM 2,5 à l’aide de la topologie d’intégration System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6dd7-138">To evaluate MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>**

1. <span data-ttu-id="f6dd7-139">Avant d’installer MBAM, passez en revue la configuration logicielle requise et la configuration prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-139">Before installing MBAM, review the prerequisite software and supported configuration.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f6dd7-140">Tâche</span><span class="sxs-lookup"><span data-stu-id="f6dd7-140">Task</span></span></th>
   <th align="left"><span data-ttu-id="f6dd7-141">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="f6dd7-141">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-142">Vérifiez que vous avez installé tous les logiciels requis.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-142">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="f6dd7-143">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="f6dd7-143">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="f6dd7-144">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6dd7-144">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-145">Vérifiez le matériel, la RAM et d’autres spécifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-145">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="f6dd7-146">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-146">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-147">Passez en revue les conditions préalables à l’utilisation de Windows PowerShell Si vous envisagez d’utiliser les applets de contrôle pour configurer MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-147">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="f6dd7-148">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f6dd7-148">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-149">Créez ou modifiez des fichiers. mof.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-149">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="f6dd7-150">Modifier le fichier Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="f6dd7-150">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="f6dd7-151">Créer ou modifier le fichier Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="f6dd7-151">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f6dd7-152">Installez le logiciel serveur MBAM, puis configurez les fonctionnalités de votre choix.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-152">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f6dd7-153">Tâche</span><span class="sxs-lookup"><span data-stu-id="f6dd7-153">Task</span></span></th>
   <th align="left"><span data-ttu-id="f6dd7-154">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="f6dd7-154">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-155">Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous voulez configurer une fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-155">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f6dd7-156">Remarque</span><span class="sxs-lookup"><span data-stu-id="f6dd7-156">Note</span></span></strong><br/><p><span data-ttu-id="f6dd7-157">Vous pouvez installer les bases de données sur un ordinateur distant SQL Server à l’aide de Windows PowerShell ou d’un package d’application de couche de données (DAC) exporté.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-157">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="f6dd7-158">Pour plus d’informations sur les packages DAC, voir <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applications à couches de données </a> .</span><span class="sxs-lookup"><span data-stu-id="f6dd7-158">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="f6dd7-159">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-159">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-160">Configurez la base de données d’audit et de conformité avec la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-160">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="f6dd7-161">Comment configurer les bases de données MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-161">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-162">Configurer la fonctionnalité rapports.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-162">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="f6dd7-163">Configuration des rapports MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-163">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-164">Configurez les applications Web.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-164">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="f6dd7-165">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-165">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-166">Configurez System Center Configuration Manager pour installer les objets Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-166">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="f6dd7-167">Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6dd7-167">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="f6dd7-168">Sur un ordinateur client, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-168">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="f6dd7-169">Installez le client MBAM et le client Configuration Manager sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-169">Install the MBAM Client and the Configuration Manager Client on a client computer.</span></span>

   2.  <span data-ttu-id="f6dd7-170">Appliquez les objets de stratégie de groupe MBAM à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-170">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="f6dd7-171">Définissez les clés de Registre suivantes pour forcer le client MBAM à se réveiller plus rapidement et à intervalles réguliers:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-171">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="f6dd7-172">Remarque</span><span class="sxs-lookup"><span data-stu-id="f6dd7-172">Note</span></span>**  
       <span data-ttu-id="f6dd7-173">Comme ces clés réactivent le client MBAM toutes les minutes, nous vous recommandons d’utiliser les paramètres de clé de registre suivants uniquement dans un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-173">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="f6dd7-174">Redémarrez le **service client de gestion BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-174">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="f6dd7-175">Dans le panneau de configuration, ouvrez **Configuration Manager**, puis cliquez sur l’onglet **actions** .</span><span class="sxs-lookup"><span data-stu-id="f6dd7-175">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="f6dd7-176">Sélectionnez **cycle d’inventaire matériel**, puis cliquez sur **Exécuter maintenant**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-176">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="f6dd7-177">Cette étape exécute l’inventaire matériel en utilisant les nouvelles classes que vous avez importées dans vos fichiers. mof, puis envoie les données au serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-177">This step runs the hardware inventory by using the new classes that you imported to your .mof files, and then sends the data to the Configuration Manager server.</span></span>

   7.  <span data-ttu-id="f6dd7-178">Sélectionnez **récupération de la stratégie ordinateur & cycle d’évaluation**, puis cliquez sur **Exécuter maintenant** pour appliquer les objets de stratégie de groupe pertinents pour cet ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-178">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>



4. <span data-ttu-id="f6dd7-179">Dans la console Configuration Manager, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-179">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="f6dd7-180">Dans le volet de navigation, cliquez avec le bouton droit sur **MBAM prises en charge**, cliquez sur **mettre à jour l’appartenance**, puis sur **Oui** pour forcer l’ordinateur client à signaler son appartenance immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-180">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="f6dd7-181">Dans le volet de navigation, cliquez sur **MBAM systèmes pris en charge** pour vérifier que l’ordinateur client apparaît dans la collection.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-181">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="f6dd7-182">Sur l’ordinateur client, dans le panneau de configuration, rouvrez **Configuration Manager** , puis procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-182">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="f6dd7-183">Cliquez sur l’onglet **actions** , puis réexécutez l’extraction de la **stratégie ordinateur & cycle d’évaluation**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-183">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="f6dd7-184">Cliquez sur l’onglet **configurations** , sélectionnez le planning de référence BitLocker, puis cliquez sur **évaluer**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-184">Click the **Configurations** tab, select the BitLocker baseline, and then click **Evaluate**.</span></span>

6. <span data-ttu-id="f6dd7-185">Dans la console Configuration Manager, vérifiez que l’ordinateur client apparaît sur le rapport de conformité de l’entreprise: comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-185">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report: as follows:</span></span>

   1.  <span data-ttu-id="f6dd7-186">Dans le volet de navigation, sélectionnez l’espace de travail **analyse** .</span><span class="sxs-lookup"><span data-stu-id="f6dd7-186">In the navigation pane, select the **Monitoring** workspace.</span></span>

   2.  <span data-ttu-id="f6dd7-187">Dans l’arborescence de la console, développez **vue d’ensemble** des rapports de &gt; **rapport** &gt; **Reports** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-187">In the console tree, expand **Overview** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

   3.  <span data-ttu-id="f6dd7-188">Sélectionnez le dossier qui représente la langue dans laquelle vous souhaitez afficher les rapports, puis sélectionnez le rapport dans le volet résultats.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-188">Select the folder that represents the language in which you want to view reports, and then select the report in the results pane.</span></span>

## <span data-ttu-id="f6dd7-189">Évaluation de MBAM 2,5 à l’aide de System Center Configuration Manager 2007 Integration Topology</span><span class="sxs-lookup"><span data-stu-id="f6dd7-189">Evaluating MBAM 2.5 by using the System Center Configuration Manager 2007 Integration topology</span></span>


<span data-ttu-id="f6dd7-190">Pour évaluer MBAM à l’aide de la topologie d’intégration de Configuration Manager, procédez de la même façon pour installer et configurer MBAM dans votre environnement de test lorsque vous utilisez un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-190">To evaluate MBAM by using the Configuration Manager Integration topology, follow the same steps to install and configure MBAM in your test environment as you use in a production environment.</span></span> <span data-ttu-id="f6dd7-191">Après avoir installé le client MBAM sur un ordinateur client, suivez la procédure supplémentaire décrite dans cette rubrique pour permettre au client MBAM de commencer à signaler l’état de l’ordinateur pour MBAM plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-191">After installing the MBAM Client on a client computer, complete the additional steps in this topic to enable the MBAM Client to start reporting the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="f6dd7-192">Pour évaluer MBAM à l’aide de la topologie de l’intégration 2007 de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6dd7-192">To evaluate MBAM by using the Configuration Manager 2007 Integration topology</span></span>**

1. <span data-ttu-id="f6dd7-193">Avant l’installation d’MBAM, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-193">Before you install MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f6dd7-194">Tâche</span><span class="sxs-lookup"><span data-stu-id="f6dd7-194">Task</span></span></th>
   <th align="left"><span data-ttu-id="f6dd7-195">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="f6dd7-195">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-196">Vérifiez que vous avez installé tous les logiciels requis.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-196">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="f6dd7-197">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="f6dd7-197">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="f6dd7-198">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6dd7-198">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-199">Vérifiez le matériel, la RAM et d’autres spécifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-199">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="f6dd7-200">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-200">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-201">Créez ou modifiez des fichiers. mof.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-201">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="f6dd7-202">Modifier le fichier Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="f6dd7-202">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="f6dd7-203">Créer ou modifier le fichier Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="f6dd7-203">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f6dd7-204">Installez le logiciel serveur MBAM, puis configurez les fonctionnalités de votre choix.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-204">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f6dd7-205">Tâche</span><span class="sxs-lookup"><span data-stu-id="f6dd7-205">Task</span></span></th>
   <th align="left"><span data-ttu-id="f6dd7-206">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="f6dd7-206">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-207">Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous voulez configurer une fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-207">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f6dd7-208">Remarque</span><span class="sxs-lookup"><span data-stu-id="f6dd7-208">Note</span></span></strong><br/><p><span data-ttu-id="f6dd7-209">Vous pouvez installer les bases de données sur un ordinateur distant SQL Server à l’aide de Windows PowerShell ou d’un package d’application de couche de données (DAC) exporté.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-209">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="f6dd7-210">Pour plus d’informations sur les packages DAC, voir <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applications à couches de données </a> .</span><span class="sxs-lookup"><span data-stu-id="f6dd7-210">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="f6dd7-211">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-211">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-212">Configurez la base de données d’audit et de conformité avec la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-212">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="f6dd7-213">Comment configurer les bases de données MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-213">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-214">Configurer la fonctionnalité rapports.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-214">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="f6dd7-215">Configuration des rapports MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-215">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f6dd7-216">Configurez les applications Web.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-216">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="f6dd7-217">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-217">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f6dd7-218">Configurez System Center Configuration Manager pour installer les objets Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-218">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="f6dd7-219">Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6dd7-219">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="f6dd7-220">Sur un ordinateur client, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-220">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="f6dd7-221">Installez le client MBAM sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-221">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="f6dd7-222">Appliquez les objets de stratégie de groupe MBAM à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-222">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="f6dd7-223">Définissez les clés de Registre suivantes pour forcer le client MBAM à se réveiller plus rapidement et à des intervalles plus courts:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-223">Set the following registry keys to force the MBAM Client to wake up more quickly and at faster intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="f6dd7-224">Remarque</span><span class="sxs-lookup"><span data-stu-id="f6dd7-224">Note</span></span>**  
       <span data-ttu-id="f6dd7-225">Comme ces clés réactivent le client MBAM toutes les minutes, nous vous recommandons d’utiliser ces paramètres de clé de Registre uniquement dans un environnement d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-225">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in an evaluation environment.</span></span>



   4.  <span data-ttu-id="f6dd7-226">Redémarrez le **service client de gestion BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-226">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="f6dd7-227">Dans le panneau de configuration, ouvrez **Configuration Manager**, puis cliquez sur l’onglet **actions** .</span><span class="sxs-lookup"><span data-stu-id="f6dd7-227">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="f6dd7-228">Sélectionnez **récupération de la stratégie ordinateur & cycle d’évaluation**, puis cliquez sur **Exécuter maintenant** pour appliquer les objets de stratégie de groupe pertinents pour cet ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-228">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>

   7.  <span data-ttu-id="f6dd7-229">Sélectionnez **cycle d’inventaire matériel**, puis cliquez sur **Exécuter maintenant**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-229">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="f6dd7-230">Cette étape exécute l’inventaire matériel en utilisant les nouvelles classes que vous avez importées dans vos fichiers. mof, puis envoie les données au serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-230">This step runs the hardware inventory by using the new classes that you imported to your .mof files and then sends the data to the Configuration Manager server.</span></span>

4. <span data-ttu-id="f6dd7-231">Dans la console Configuration Manager, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-231">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="f6dd7-232">Dans le volet de navigation, cliquez avec le bouton droit sur **MBAM prises en charge**, cliquez sur **mettre à jour l’appartenance**, puis sur **Oui** pour forcer l’ordinateur client à signaler son appartenance immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-232">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="f6dd7-233">Dans le volet de navigation, cliquez sur **MBAM systèmes pris en charge** pour vérifier que l’ordinateur client apparaît dans la collection.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-233">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="f6dd7-234">Sur l’ordinateur client, dans le panneau de configuration, rouvrez **Configuration Manager** , puis procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f6dd7-234">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="f6dd7-235">Cliquez sur l’onglet **actions** , puis réexécutez l’extraction de la **stratégie ordinateur & cycle d’évaluation**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-235">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="f6dd7-236">Cliquez sur l’onglet **configurations** , sélectionnez le planning de référence BitLocker, puis cliquez sur **évaluer**.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-236">Click the **Configurations** tab, select the BitLocker baseline, and click **Evaluate**.</span></span>

6. <span data-ttu-id="f6dd7-237">Dans la console Configuration Manager, vérifiez que l’ordinateur client apparaît sur le rapport de conformité d’entreprise, comme suit.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-237">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report, as follows</span></span>

   1.  <span data-ttu-id="f6dd7-238">Dans le volet de navigation, développez **Computer Management** Reporting &gt; **Reporting** &gt; **services Reporting Services Reporting Services** &gt; \*\* &lt; nom du serveur &gt; MBAM\*\*.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-238">In the navigation pane, expand **Computer Management** &gt; **Reporting** &gt; **Reporting Services** &gt; **&lt;server name&gt;MBAM**.</span></span>

   2.  <span data-ttu-id="f6dd7-239">Dans le nœud **MBAM** , sélectionnez le dossier qui représente la langue dans laquelle vous souhaitez afficher les rapports, puis sélectionnez le rapport dans le volet résultats.</span><span class="sxs-lookup"><span data-stu-id="f6dd7-239">Within the **MBAM** node, select the folder that represents the language in which you want to view reports, and then select the report from the results pane.</span></span>


## <span data-ttu-id="f6dd7-240">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6dd7-240">Related topics</span></span>


[<span data-ttu-id="f6dd7-241">Prise en main de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f6dd7-241">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)


## <span data-ttu-id="f6dd7-242">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="f6dd7-242">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f6dd7-243">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="f6dd7-243">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="f6dd7-244">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f6dd7-244">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






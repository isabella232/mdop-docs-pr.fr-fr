---
title: Évaluation de MBAM1.0
description: Évaluation de MBAM1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811045"
---
# <span data-ttu-id="f868e-103">Évaluation de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-103">Evaluating MBAM 1.0</span></span>


<span data-ttu-id="f868e-104">Avant de déployer l’administration et la surveillance Microsoft BitLocker (MBAM) dans un environnement de production, vous devez l’évaluer dans un environnement de laboratoire.</span><span class="sxs-lookup"><span data-stu-id="f868e-104">Before you deploy Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a lab environment.</span></span> <span data-ttu-id="f868e-105">Vous pouvez utiliser les informations fournies dans cette rubrique pour configurer MBAM dans un seul environnement Lab serveur à des fins d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="f868e-105">You can use the information in this topic to set up MBAM in a single server lab environment for evaluation purposes only.</span></span>

<span data-ttu-id="f868e-106">Bien que les étapes du déploiement réel soient très similaires au scénario décrit dans [la rubrique Comment installer et configurer MBAM sur un seul serveur](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), cette rubrique contient des informations supplémentaires pour vous permettre de configurer un environnement d’évaluation MBAM dans le moins de temps.</span><span class="sxs-lookup"><span data-stu-id="f868e-106">While the actual deployment steps are very similar to the scenario that is described in [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), this topic contains additional information to enable you to set up an MBAM evaluation environment in the least amount of time.</span></span>

## <span data-ttu-id="f868e-107">Configurer l’environnement Lab</span><span class="sxs-lookup"><span data-stu-id="f868e-107">Set up the Lab Environment</span></span>


<span data-ttu-id="f868e-108">Même lorsque vous configurez une instance de MBAM qui n’est pas de production pour une évaluation dans un environnement Lab, vous devez toujours vérifier que vous avez satisfait aux conditions préalables de déploiement et à la configuration matérielle et logicielle requise.</span><span class="sxs-lookup"><span data-stu-id="f868e-108">Even when you set up a non-production instance of MBAM to evaluate in a lab environment, you should still verify that you have met the deployment prerequisites and the hardware and software requirements.</span></span> <span data-ttu-id="f868e-109">Pour plus d’informations, consultez la configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et les [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="f868e-109">For more information, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="f868e-110">Avant de commencer le déploiement d’évaluation d’MBAM, vous devez également consulter la [préparation de votre environnement pour MBAM 1,0](preparing-your-environment-for-mbam-10.md) .</span><span class="sxs-lookup"><span data-stu-id="f868e-110">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM evaluation deployment.</span></span>

### <span data-ttu-id="f868e-111">Planifier un déploiement d’une évaluation MBAM</span><span class="sxs-lookup"><span data-stu-id="f868e-111">Plan for an MBAM Evaluation Deployment</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="f868e-112">Tâche</span><span class="sxs-lookup"><span data-stu-id="f868e-112">Task</span></span></th>
<th align="left"><span data-ttu-id="f868e-113">Références</span><span class="sxs-lookup"><span data-stu-id="f868e-113">References</span></span></th>
<th align="left"><span data-ttu-id="f868e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f868e-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-115">Passez en revue les informations de prise en main sur MBAM pour obtenir une connaissance de base du produit avant de commencer la planification du déploiement.</span><span class="sxs-lookup"><span data-stu-id="f868e-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before you begin your deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)"><span data-ttu-id="f868e-116">Prise en main de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-116">Getting Started with MBAM 1.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p><span data-ttu-id="f868e-117">Préparez votre environnement informatique pour l’installation MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-117">Prepare your computing environment for the MBAM installation.</span></span> <span data-ttu-id="f868e-118">Pour ce faire, vous devez activer le chiffrement de données transparent (TDE) sur les instances SQL Server qui hébergeront des bases de données MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-118">To do so, you must enable the Transparent Data Encryption (TDE) on the SQL Server instances that will host MBAM databases.</span></span> <span data-ttu-id="f868e-119">Pour activer TDE dans votre environnement de laboratoire, vous pouvez créer un fichier. SQL à exécuter sur la base de données maître hébergée sur l’instance de SQL Server qu’MBAM utilisera.</span><span class="sxs-lookup"><span data-stu-id="f868e-119">To enable TDE in your lab environment, you can create a .sql file to run against the master database that is hosted on the instance of the SQL Server that MBAM will use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f868e-120">Remarque</span><span class="sxs-lookup"><span data-stu-id="f868e-120">Note</span></span></strong><br/><p><span data-ttu-id="f868e-121">L’exemple suivant permet de créer un fichier. SQL pour votre environnement Lab afin d’activer rapidement TDE sur l’instance SQL Server qui héberge les bases de données MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-121">You can use the following example to create a .sql file for your lab environment to quickly enable TDE on the SQL Server instance that will host the MBAM databases.</span></span> <span data-ttu-id="f868e-122">Les commandes SQL Server suivantes permettent à TDE à l’aide d’un certificat SQL Server signé en local.</span><span class="sxs-lookup"><span data-stu-id="f868e-122">These SQL Server commands will enable TDE by using a locally signed SQL Server certificate.</span></span> <span data-ttu-id="f868e-123">Assurez-vous de sauvegarder le certificat TDE et sa clé de chiffrement associée dans l’exemple de chemin de sauvegarde local de <em> C:\backup </em> .</span><span class="sxs-lookup"><span data-stu-id="f868e-123">Make sure to back up the TDE certificate and its associated encryption key to the example local backup path of <em>C:\Backup</em>.</span></span> <span data-ttu-id="f868e-124">Le certificat et la clé TDE sont requis lors de la récupération de la base de données ou du déplacement du certificat et de la clé vers un autre serveur sur lequel le chiffrement TDE est activé.</span><span class="sxs-lookup"><span data-stu-id="f868e-124">The TDE certificate and key are required when recover the database or move the certificate and key to another server that has TDE encryption in place.</span></span></p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)"><span data-ttu-id="f868e-125">Conditions préalables au déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-125">MBAM 1.0 Deployment Prerequisites</span></span></a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)"><span data-ttu-id="f868e-126">Chiffrement de base de données dans SQL Server 2008 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="f868e-126">Database Encryption in SQL Server 2008 Enterprise Edition</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-127">Planifiez et configurez les exigences de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-127">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)"><span data-ttu-id="f868e-128">Planification des exigences en matière de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-128">Planning for MBAM 1.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-129">Planifiez et créez les groupes de sécurité de services de domaine Active Directory nécessaires et planifiez les exigences d’appartenance au groupe de sécurité local MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-129">Plan for and create the necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="f868e-130">Planification des rôles administrateur de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-130">Planning for MBAM 1.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-131">Planifier le déploiement de fonctionnalités de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="f868e-131">Plan for MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)"><span data-ttu-id="f868e-132">Planification du déploiement de serveursMBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-132">Planning for MBAM 1.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-133">Planifier le déploiement du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-133">Plan for MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)"><span data-ttu-id="f868e-134">Planification du déploiement de clients MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-134">Planning for MBAM 1.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f868e-135">Effectuer un déploiement d’évaluation MBAM</span><span class="sxs-lookup"><span data-stu-id="f868e-135">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="f868e-136">Après avoir effectué les installations de planification et de pré-installation requises pour préparer votre environnement informatique pour une installation MBAM, vous pouvez commencer le déploiement d’évaluation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-136">After you complete the necessary planning and software prerequisite installations to prepare your computing environment for an MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-137">Passez en revue les informations de configurations prises en charge par MBAM pour vous assurer que les ordinateurs client et serveur sélectionnés sont pris en charge pour l’installation de la fonctionnalité MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-137">Review the MBAM supported configurations information to make sure that the selected client and server computers are supported for the MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="f868e-138">Configurations prises en charge par MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-138">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-139">Exécutez le programme d’installation de MBAM pour déployer les fonctionnalités serveur MBAM sur un serveur unique à des fins d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="f868e-139">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)"><span data-ttu-id="f868e-140">Installation et configuration de MBAM sur un seul serveur</span><span class="sxs-lookup"><span data-stu-id="f868e-140">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-141">Ajoutez les groupes de sécurité des services de domaine Active Directory (AD FS) que vous avez créés lors de la phase de planification aux groupes locaux du serveur MBAM local approprié sur le nouveau serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-141">Add the Active Directory Domain Services security groups that you created during the planning phase to the appropriate local MBAM Server feature local groups on the new MBAM server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="f868e-142">Planification des rôles d’administrateur MBAM 1,0 </a> et <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Comment gérer les rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="f868e-142">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-143">Créez et déployez les objets de stratégie de groupe MBAM requis.</span><span class="sxs-lookup"><span data-stu-id="f868e-143">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="f868e-144">Déploiement d'objets de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-144">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f868e-145">Déployez le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="f868e-145">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="f868e-146">Déploiement du client MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-146">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f868e-147">Configurer les ordinateurs de laboratoire pour l’évaluation de MBAM</span><span class="sxs-lookup"><span data-stu-id="f868e-147">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="f868e-148">Vous pouvez modifier les paramètres de fréquence des rapports d’État du client MBAM à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="f868e-148">You can change the frequency settings on the MBAM Client status reporting by using Registry Editor.</span></span> <span data-ttu-id="f868e-149">Toutefois, ces modifications doivent être utilisées uniquement à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="f868e-149">However, these modifications should be used for testing purposes only.</span></span>

**<span data-ttu-id="f868e-150">Warning</span><span class="sxs-lookup"><span data-stu-id="f868e-150">Warning</span></span>**  
<span data-ttu-id="f868e-151">Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="f868e-151">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="f868e-152">Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows.</span><span class="sxs-lookup"><span data-stu-id="f868e-152">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="f868e-153">Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre.</span><span class="sxs-lookup"><span data-stu-id="f868e-153">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="f868e-154">Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus.</span><span class="sxs-lookup"><span data-stu-id="f868e-154">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="f868e-155">Changez de Registre à vos propres risques.</span><span class="sxs-lookup"><span data-stu-id="f868e-155">Change the registry at your own risk.</span></span>



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a><span data-ttu-id="f868e-156">Modifier les paramètres de fréquence des rapports d’État du client MBAM</span><span class="sxs-lookup"><span data-stu-id="f868e-156">Modify the Frequency Settings on MBAM Client Status Reporting</span></span>

<span data-ttu-id="f868e-157">Les fréquences de rapport d’État et de réveil du client MBAM ont une valeur minimale de 90 minutes lorsqu’elles sont configurées pour utiliser une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f868e-157">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set to use Group Policy.</span></span> <span data-ttu-id="f868e-158">Vous pouvez modifier ces fréquences sur les ordinateurs clients MBAM en modifiant le Registre Windows sur valeurs inférieures, ce qui permet d’accélérer les tests.</span><span class="sxs-lookup"><span data-stu-id="f868e-158">You can change these frequencies on MBAM client computers by editing the Windows registry to lower values, which will help speed up the testing.</span></span> <span data-ttu-id="f868e-159">Pour modifier les paramètres de fréquence de création de rapports de l’état du client MBAM, utilisez un éditeur du Registre pour accéder à **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, modifiez les valeurs pour **ClientWakeupFrequency** et **StatusReportingFrequency** sur **1** comme valeur minimale prise en charge du client, puis redémarrez le service client de gestion BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f868e-159">To modify the frequency settings on MBAM Client status reporting, use a registry editor to navigate to **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client supported value, and then restart BitLocker Management Client Service.</span></span> <span data-ttu-id="f868e-160">Lorsque vous effectuez cette modification, le client MBAM rapporte chaque minute.</span><span class="sxs-lookup"><span data-stu-id="f868e-160">When you make this change, the MBAM Client will report every minute.</span></span> <span data-ttu-id="f868e-161">Vous pouvez définir des valeurs dont la valeur est faible uniquement lorsque vous effectuez cette opération manuellement dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f868e-161">You can set values this low only when you do so manually in the registry.</span></span>

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a><span data-ttu-id="f868e-162">Modifier le délai de démarrage sur le service client MBAM</span><span class="sxs-lookup"><span data-stu-id="f868e-162">Modify the Startup Delay on MBAM Client Service</span></span>

<span data-ttu-id="f868e-163">En plus des fréquences de création de rapports d’État et de réveil du client MBAM, il existe un délai aléatoire de maximum de 90 minutes lorsque le service d’agent client MBAM démarre sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="f868e-163">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="f868e-164">Si vous ne souhaitez pas utiliser le délai aléatoire, créez une valeur **DWORD** de **NoStartupDelay** sous **HKLM\\Software\\Microsoft\\MBAM**, définissez sa valeur sur **1**, puis redémarrez le service client de gestion BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f868e-164">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart BitLocker Management Client Service.</span></span>

## <span data-ttu-id="f868e-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f868e-165">Related topics</span></span>


[<span data-ttu-id="f868e-166">Prise en main de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f868e-166">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)










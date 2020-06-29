---
title: Évaluation de MBAM2.0
description: Évaluation de MBAM2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810734"
---
# <span data-ttu-id="491e0-103">Évaluation de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-103">Evaluating MBAM 2.0</span></span>


<span data-ttu-id="491e0-104">Avant de déployer l’administration et la surveillance de Microsoft BitLocker (MBAM) dans un environnement de production, vous devez l’évaluer dans un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="491e0-104">Before deploying Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a test environment.</span></span> <span data-ttu-id="491e0-105">Les informations contenues dans cette rubrique peuvent être utilisées pour configurer l’administration et la surveillance de Microsoft BitLocker à l’aide d’une topologie autonome dans un environnement de test serveur unique à des fins d’évaluation uniquement.</span><span class="sxs-lookup"><span data-stu-id="491e0-105">The information in this topic can be used to set up Microsoft BitLocker Administration and Monitoring with a Stand-alone topology in a single-server test environment for evaluation purposes only.</span></span> <span data-ttu-id="491e0-106">Une topologie sur un seul serveur n’est pas recommandée dans les environnements de production.</span><span class="sxs-lookup"><span data-stu-id="491e0-106">A single-server topology is not recommended for production environments.</span></span>

<span data-ttu-id="491e0-107">Pour obtenir des instructions sur le déploiement de MBAM dans un environnement de test, voir [Comment installer et configurer MBAM sur un seul serveur](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="491e0-107">For instructions on deploying MBAM in a test environment, see [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span></span>

## <span data-ttu-id="491e0-108">Configuration de l’environnement de test</span><span class="sxs-lookup"><span data-stu-id="491e0-108">Setting up the Test Environment</span></span>


<span data-ttu-id="491e0-109">Même si vous configurez une instance de MBAM qui n’est pas de production et qu’elle évalue dans un environnement de test, vous devez vérifier que vous remplissez bien les conditions préalables et matérielles et logicielles requises.</span><span class="sxs-lookup"><span data-stu-id="491e0-109">Even though you are setting up a non-production instance of MBAM to evaluate in a test environment, you should still verify that you have met the prerequisites and hardware and software requirements.</span></span> <span data-ttu-id="491e0-110">Avant de commencer l’installation, consultez la configuration requise pour le [déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md), les [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md)et [la préparation de votre environnement pour MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="491e0-110">Before you start the installation, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md), and [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md).</span></span>

### <span data-ttu-id="491e0-111">Planifier un déploiement d’une évaluation MBAM</span><span class="sxs-lookup"><span data-stu-id="491e0-111">Plan for an MBAM Evaluation Deployment</span></span>

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
<th align="left"><span data-ttu-id="491e0-112">Tâche</span><span class="sxs-lookup"><span data-stu-id="491e0-112">Task</span></span></th>
<th align="left"><span data-ttu-id="491e0-113">Références</span><span class="sxs-lookup"><span data-stu-id="491e0-113">References</span></span></th>
<th align="left"><span data-ttu-id="491e0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="491e0-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-115">Passez en revue les informations de prise en main de MBAM pour en savoir plus sur le produit avant de commencer la planification du déploiement.</span><span class="sxs-lookup"><span data-stu-id="491e0-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before beginning deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)"><span data-ttu-id="491e0-116">Prise en main de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-116">Getting Started with MBAM 2.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-117">Planifiez les prérequis de déploiement d’MBAM 2,0 et préparez votre environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="491e0-117">Plan for MBAM 2.0 Deployment Prerequisites and prepare your computing environment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)"><span data-ttu-id="491e0-118">Conditions préalables au déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-118">MBAM 2.0 Deployment Prerequisites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-119">Planifiez et configurez les exigences de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="491e0-119">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="491e0-120">Planification des exigences en matière de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-120">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-121">Planifiez et créez des groupes de sécurité ActiveDirectoryDomainServices nécessaires et planifiez les exigences d’appartenance au groupe de sécurité local MBAM.</span><span class="sxs-lookup"><span data-stu-id="491e0-121">Plan for and create necessary ActiveDirectoryDomainServices security groups, and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="491e0-122">Planification des rôles administrateur de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-122">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-123">Plan de déploiement de la fonctionnalité de déploiement de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="491e0-123">Plan for deploying MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)"><span data-ttu-id="491e0-124">Planification du déploiement de serveursMBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-124">Planning for MBAM 2.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-125">Plan de déploiement du déploiement du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="491e0-125">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="491e0-126">Planification du déploiement de clients MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-126">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="491e0-127">Effectuer un déploiement d’évaluation MBAM</span><span class="sxs-lookup"><span data-stu-id="491e0-127">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="491e0-128">Après avoir effectué les installations de planification et de configuration logicielles requises pour préparer votre environnement informatique pour l’installation d’MBAM, vous pouvez commencer le déploiement d’évaluation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="491e0-128">After completing the necessary planning and software prerequisite installations to prepare your computing environment for the MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

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
<td align="left"><p><span data-ttu-id="491e0-129">Passez en revue les informations de configurations prises en charge par MBAM pour vous assurer que les ordinateurs client et serveur sélectionnés sont pris en charge pour l’installation de la fonctionnalité MBAM.</span><span class="sxs-lookup"><span data-stu-id="491e0-129">Review the MBAM supported configurations information to make sure that selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="491e0-130">Configurations prises en charge par MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-130">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-131">Exécutez le programme d’installation de MBAM pour déployer les fonctionnalités serveur MBAM sur un serveur unique à des fins d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="491e0-131">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)"><span data-ttu-id="491e0-132">Installation et configuration de MBAM sur un seul serveur</span><span class="sxs-lookup"><span data-stu-id="491e0-132">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-133">Ajoutez des groupes de sécurité ActiveDirectoryDomainServices, que vous avez créés lors de la phase de planification, aux groupes locaux du serveur MBAM local appropriés sur le nouveau serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="491e0-133">Add ActiveDirectoryDomainServices security groups, that you created during the planning phase, to the appropriate local MBAM Server feature local groups on the new MBAM Server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="491e0-134">Planification des rôles d’administrateur MBAM 2,0 </a> et <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Comment gérer les rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="491e0-134">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-135">Créer et déployer des objets de stratégie de groupe MBAM requis.</span><span class="sxs-lookup"><span data-stu-id="491e0-135">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="491e0-136">Déploiement d'objets de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-136">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="491e0-137">Déployez le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="491e0-137">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="491e0-138">Déploiement du client MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-138">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="491e0-139">Configurer les ordinateurs de laboratoire pour l’évaluation de MBAM</span><span class="sxs-lookup"><span data-stu-id="491e0-139">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="491e0-140">Cette section contient des informations qui peuvent être utilisées pour accélérer la création de rapports d’État du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="491e0-140">This section contains information that can be used to speed up the MBAM Client status reporting.</span></span> <span data-ttu-id="491e0-141">Toutefois, ces modifications doivent être utilisées uniquement à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="491e0-141">However, these modifications should be used for testing purposes only.</span></span>

<span data-ttu-id="491e0-142">**Remarques**  Les informations de la section suivante décrivent comment modifier le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="491e0-142">**Note** The information in following section describes how to modify the Windows registry.</span></span> <span data-ttu-id="491e0-143">L’utilisation de l’éditeur du Registre peut être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows.</span><span class="sxs-lookup"><span data-stu-id="491e0-143">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="491e0-144">Microsoft ne peut pas garantir que les problèmes résultant de l’utilisation incorrecte de l’éditeur du Registre peuvent être résolus.</span><span class="sxs-lookup"><span data-stu-id="491e0-144">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="491e0-145">Utilisez l’éditeur du Registre à vos propres risques.</span><span class="sxs-lookup"><span data-stu-id="491e0-145">Use Registry Editor at your own risk.</span></span>

 

### <span data-ttu-id="491e0-146">Modifier les paramètres de fréquence des rapports d’État du client MBAM</span><span class="sxs-lookup"><span data-stu-id="491e0-146">Modify MBAM Client Status Reporting Frequency Settings</span></span>

<span data-ttu-id="491e0-147">Les fréquences de rapport d’État et de réveil du client MBAM ont une valeur minimale de 90 minutes lorsqu’elles sont définies à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="491e0-147">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set using Group Policy.</span></span> <span data-ttu-id="491e0-148">Vous pouvez utiliser le registre de Windows pour changer ces fréquences en une valeur inférieure sur les ordinateurs clients MBAM pour accélérer les tests.</span><span class="sxs-lookup"><span data-stu-id="491e0-148">You can use the Windows registry to change these frequencies to a lower value on MBAM client computers to help speed up testing.</span></span>

<span data-ttu-id="491e0-149">Pour modifier les paramètres de fréquence des rapports d’État du client MBAM:</span><span class="sxs-lookup"><span data-stu-id="491e0-149">To modify the MBAM Client status reporting frequency settings:</span></span>

1.  <span data-ttu-id="491e0-150">Utilisez un éditeur du Registre pour accéder à **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="491e0-150">Use a registry editor to navigate to **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span></span>

2.  <span data-ttu-id="491e0-151">Modifiez les valeurs de **ClientWakeupFrequency** et **StatusReportingFrequency** sur **1** comme valeur prise en charge par le client minimum.</span><span class="sxs-lookup"><span data-stu-id="491e0-151">Change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client-supported value.</span></span> <span data-ttu-id="491e0-152">Cette modification entraîne le rapport de chaque minute par le client MBAM.</span><span class="sxs-lookup"><span data-stu-id="491e0-152">This change causes the MBAM Client to report every minute.</span></span>

3.  <span data-ttu-id="491e0-153">Redémarrez le **service client de gestion BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="491e0-153">Restart **BitLocker Management Client Service**.</span></span>

<span data-ttu-id="491e0-154">**Remarques**  Pour définir des valeurs dont le niveau est faible, vous devez les définir manuellement dans le registre.</span><span class="sxs-lookup"><span data-stu-id="491e0-154">**Note** To set values that are this low, you must set them in the registry manually.</span></span>

 

### <span data-ttu-id="491e0-155">Modifier le délai de démarrage du service client MBAM</span><span class="sxs-lookup"><span data-stu-id="491e0-155">Modify MBAM Client Service Startup Delay</span></span>

<span data-ttu-id="491e0-156">En plus des fréquences de création de rapports d’État et de réveil du client MBAM, il existe un délai aléatoire de maximum de 90 minutes lorsque le service d’agent client MBAM démarre sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="491e0-156">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="491e0-157">Si vous ne souhaitez pas utiliser le délai aléatoire, créez une valeur **DWORD** de **NoStartupDelay** sous **HKLM\\Software\\Microsoft\\MBAM**, définissez sa valeur sur **1**, puis redémarrez le **service client de gestion BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="491e0-157">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="491e0-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="491e0-158">Related topics</span></span>


[<span data-ttu-id="491e0-159">Prise en main de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="491e0-159">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 






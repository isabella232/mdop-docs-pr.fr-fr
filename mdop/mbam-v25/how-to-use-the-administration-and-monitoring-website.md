---
title: Utilisation du site web d'administration et de surveillance
description: Utilisation du site web d'administration et de surveillance
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804681"
---
# <span data-ttu-id="b51ea-103">Utilisation du site web d'administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="b51ea-103">How to Use the Administration and Monitoring Website</span></span>


<span data-ttu-id="b51ea-104">Le site Web d’administration et de surveillance, également appelé support technique, est une interface d’administration pour le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b51ea-104">The Administration and Monitoring Website, also referred to as the Help Desk, is an administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="b51ea-105">Utilisez le site Web pour passer en revue les rapports, récupérer les lecteurs des utilisateurs finaux et gérer les TPMs des utilisateurs finaux, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b51ea-105">Use the website to review reports, recover end users’ drives, and manage end users’ TPMs, as described in the following sections.</span></span>

<span data-ttu-id="b51ea-106">**Remarques**  Si vous utilisez MBAM dans la topologie autonome, vous pouvez afficher tous les rapports à partir du site Web Administration et analyse.</span><span class="sxs-lookup"><span data-stu-id="b51ea-106">**Note** If you are using MBAM in the Stand-alone topology, you view all reports from the Administration and Monitoring Website.</span></span> <span data-ttu-id="b51ea-107">Si vous utilisez la topologie d’intégration Configuration Manager, vous pouvez afficher tous les rapports dans Configuration Manager, à l’exception du rapport d’audit de récupération, que vous continuez à consulter à partir du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="b51ea-107">If you are using the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit report, which you continue to view from the Administration and Monitoring Website.</span></span> <span data-ttu-id="b51ea-108">Pour plus d’informations sur les rapports, voir [surveillance et signalement de la conformité avec BitLocker avec MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="b51ea-108">For more information about reports, see [Monitoring and Reporting BitLocker Compliance with MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span></span>

 

## <span data-ttu-id="b51ea-109">Rôles requis pour l’utilisation du site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="b51ea-109">Required roles for using the Administration and Monitoring Website</span></span>


<span data-ttu-id="b51ea-110">Pour accéder à certaines zones du site Web d’administration et de surveillance, vous devez disposer de l’un des rôles suivants, qui sont des groupes que vous créez dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b51ea-110">To access specific areas of the Administration and Monitoring Website, you must have one of the following roles, which are groups that you create in Active Directory.</span></span> <span data-ttu-id="b51ea-111">Vous pouvez utiliser n’importe quel nom pour ces groupes.</span><span class="sxs-lookup"><span data-stu-id="b51ea-111">You can use any name for these groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b51ea-112">Compte</span><span class="sxs-lookup"><span data-stu-id="b51ea-112">Account</span></span></th>
<th align="left"><span data-ttu-id="b51ea-113">Description</span><span class="sxs-lookup"><span data-stu-id="b51ea-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b51ea-114">Utilisateurs du support technique avancée MBAM</span><span class="sxs-lookup"><span data-stu-id="b51ea-114">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-115">Permet d’accéder à toutes les zones du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="b51ea-115">Provides access to all areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="b51ea-116">Les utilisateurs qui ont ce rôle ne peuvent entrer que la clé de récupération, et non le domaine et le nom d’utilisateur de l’utilisateur final, pour aider les utilisateurs finaux à récupérer leurs lecteurs.</span><span class="sxs-lookup"><span data-stu-id="b51ea-116">Users who have this role enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="b51ea-117">Si un utilisateur est membre du groupe utilisateurs du support technique MBAM et du groupe utilisateurs du support technique avancé MBAM, les autorisations de groupe utilisateurs du support technique avancée MBAM sont prioritaires sur les autorisations du groupe utilisateurs du support technique MBAM.</span><span class="sxs-lookup"><span data-stu-id="b51ea-117">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b51ea-118">Utilisateurs du support technique MBAM</span><span class="sxs-lookup"><span data-stu-id="b51ea-118">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-119">Permet d’accéder aux zones gérer le module de plateforme sécurisée et de récupération des lecteurs du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="b51ea-119">Provides access to the Manage TPM and Drive Recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="b51ea-120">Les personnes qui ont ce rôle doivent remplir tous les champs, y compris le nom de domaine et le nom du compte de l’utilisateur final, lorsqu’ils utilisent l’une de ces zones.</span><span class="sxs-lookup"><span data-stu-id="b51ea-120">Individuals who have this role must fill in all fields, including the end-user’s domain and account name, when they use either area.</span></span></p>
<p><span data-ttu-id="b51ea-121">Si un utilisateur est membre du groupe utilisateurs du support technique MBAM et du groupe utilisateurs du support technique avancé MBAM, les autorisations de groupe utilisateurs du support technique avancée MBAM sont prioritaires sur les autorisations du groupe utilisateurs du support technique MBAM.</span><span class="sxs-lookup"><span data-stu-id="b51ea-121">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b51ea-122">Utilisateurs de rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="b51ea-122">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-123">Donne accès aux rapports figurant dans la <strong> </strong> zone rapports du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="b51ea-123">Provides access to the reports in the <strong>Reports</strong> area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b51ea-124">Tâches que vous pouvez effectuer sur le site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="b51ea-124">Tasks you can perform on the Administration and Monitoring Website</span></span>


<span data-ttu-id="b51ea-125">Le tableau suivant récapitule les tâches que vous pouvez effectuer sur le site Web d’administration et de contrôle, ainsi que des liens vers des informations supplémentaires sur chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="b51ea-125">The following table summarizes the tasks you can perform on the Administration and Monitoring Website and provides links to more information about each task.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b51ea-126">Tâche</span><span class="sxs-lookup"><span data-stu-id="b51ea-126">Task</span></span></th>
<th align="left"><span data-ttu-id="b51ea-127">Zone du site Web où vous accédez à la tâche</span><span class="sxs-lookup"><span data-stu-id="b51ea-127">Area of the Website where you access the task</span></span></th>
<th align="left"><span data-ttu-id="b51ea-128">Description</span><span class="sxs-lookup"><span data-stu-id="b51ea-128">Description</span></span></th>
<th align="left"><span data-ttu-id="b51ea-129">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b51ea-129">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b51ea-130">Affichage des rapports</span><span class="sxs-lookup"><span data-stu-id="b51ea-130">View reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-131">Rapports</span><span class="sxs-lookup"><span data-stu-id="b51ea-131">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-132">Vous permet d’exécuter des rapports pour surveiller l’activité d’utilisation, de conformité et de récupération de clés de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b51ea-132">Enables you to run reports to monitor BitLocker usage, compliance, and key recovery activity.</span></span> <span data-ttu-id="b51ea-133">Les rapports fournissent des données concernant la conformité d’entreprise, des ordinateurs individuels et la personne qui a demandé les clés de récupération ou le package OwnerAuth TPM pour un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="b51ea-133">Reports provide data about enterprise compliance, individual computers, and who requested recovery keys or the TPM OwnerAuth package for a specific computer.</span></span></p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)"><span data-ttu-id="b51ea-134">Affichage de rapports MBAM2.5 pour la topologie autonome</span><span class="sxs-lookup"><span data-stu-id="b51ea-134">Viewing MBAM 2.5 Reports for the Stand-alone Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b51ea-135">Déterminer l’état de chiffrement de BitLocker des ordinateurs perdus ou volés</span><span class="sxs-lookup"><span data-stu-id="b51ea-135">Determine the BitLocker encryption status of lost or stolen computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-136">Rapports</span><span class="sxs-lookup"><span data-stu-id="b51ea-136">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-137">Déterminer si un volume a été chiffré en cas de perte ou de vol de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b51ea-137">Determine if a volume was encrypted if the computer is lost or stolen.</span></span></p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)"><span data-ttu-id="b51ea-138">Détermination de l'état de chiffrement BitLocker des ordinateurs perdus</span><span class="sxs-lookup"><span data-stu-id="b51ea-138">How to Determine BitLocker Encryption State of Lost Computers</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b51ea-139">Récupérer des lecteurs perdus</span><span class="sxs-lookup"><span data-stu-id="b51ea-139">Recover lost drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-140">Récupération des lecteurs</span><span class="sxs-lookup"><span data-stu-id="b51ea-140">Drive Recovery</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-141">Récupérer des lecteurs:</span><span class="sxs-lookup"><span data-stu-id="b51ea-141">Recover drives that are:</span></span></p>
<ul>
<li><p><span data-ttu-id="b51ea-142">En mode récupération</span><span class="sxs-lookup"><span data-stu-id="b51ea-142">In recovery mode</span></span></p></li>
<li><p><span data-ttu-id="b51ea-143">Ont été déplacés</span><span class="sxs-lookup"><span data-stu-id="b51ea-143">Have been moved</span></span></p></li>
<li><p><span data-ttu-id="b51ea-144">Sont endommagés</span><span class="sxs-lookup"><span data-stu-id="b51ea-144">Are corrupted</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)"><span data-ttu-id="b51ea-145">Procédure de récupération d'un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="b51ea-145">How to Recover a Drive in Recovery Mode</span></span></a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)"><span data-ttu-id="b51ea-146">Récupération d'un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="b51ea-146">How to Recover a Moved Drive</span></span></a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)"><span data-ttu-id="b51ea-147">Récupération d'un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="b51ea-147">How to Recover a Corrupted Drive</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b51ea-148">Réinitialiser un verrouillage du TPM</span><span class="sxs-lookup"><span data-stu-id="b51ea-148">Reset a TPM lockout</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-149">Gérer le TPM</span><span class="sxs-lookup"><span data-stu-id="b51ea-149">Manage TPM</span></span></p></td>
<td align="left"><p><span data-ttu-id="b51ea-150">Donne accès aux données du TPM collectées par le client MBAM.</span><span class="sxs-lookup"><span data-stu-id="b51ea-150">Provides access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="b51ea-151">Dans un verrouillage de module de plateforme sécurisée, utilisez le site Web d’administration et de surveillance pour extraire le fichier de mot de passe nécessaire pour déverrouiller le TPM.</span><span class="sxs-lookup"><span data-stu-id="b51ea-151">In a TPM lockout, use the Administration and Monitoring Website to retrieve the necessary password file to unlock the TPM.</span></span></p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)"><span data-ttu-id="b51ea-152">Réinitialisation d'un verrouillage TPM</span><span class="sxs-lookup"><span data-stu-id="b51ea-152">How to Reset a TPM Lockout</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="b51ea-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b51ea-153">Related topics</span></span>


[<span data-ttu-id="b51ea-154">Gestion de BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b51ea-154">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="b51ea-155">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="b51ea-155">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b51ea-156">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="b51ea-156">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b51ea-157">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b51ea-157">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 






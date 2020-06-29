---
title: Présentation des rapports autonomes MBAM2.5
description: Présentation des rapports autonomes MBAM2.5
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804482"
---
# <span data-ttu-id="ddd4f-103">Présentation des rapports autonomes MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ddd4f-103">Understanding MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="ddd4f-104">Cette rubrique décrit les rapports disponibles lors de l’exécution de Microsoft BitLocker administration et de la surveillance (MBAM) dans la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-104">This topic describes the reports that are available when you are running Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology.</span></span>

**<span data-ttu-id="ddd4f-105">Remarque</span><span class="sxs-lookup"><span data-stu-id="ddd4f-105">Note</span></span>**  
<span data-ttu-id="ddd4f-106">Si vous exécutez MBAM avec la topologie d’intégration de Configuration Manager, vous générez des rapports à partir de Configuration Manager plutôt que d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-106">If you are running MBAM with the Configuration Manager Integration topology, you generate reports from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="ddd4f-107">Pour plus d’informations sur ces rapports, voir [afficher des rapports 2,5 MBAM pour la topologie d’intégration de Configuration Manager](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd4f-107">See [Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) for more information about these reports.</span></span>



## <span data-ttu-id="ddd4f-108">Présentation des rapports de topologie autonomes de MBAM</span><span class="sxs-lookup"><span data-stu-id="ddd4f-108">Understanding the MBAM Stand-alone topology reports</span></span>


<span data-ttu-id="ddd4f-109">MBAM fournit trois types de rapports que vous pouvez utiliser pour surveiller votre organisation pour la conformité avec BitLocker:</span><span class="sxs-lookup"><span data-stu-id="ddd4f-109">MBAM provides three report types that you can use to monitor your organization for BitLocker compliance:</span></span>

-   [<span data-ttu-id="ddd4f-110">Rapport de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="ddd4f-110">Enterprise Compliance Report</span></span>](#bkmk-enterprisecompliance)

-   [<span data-ttu-id="ddd4f-111">Rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-111">Computer Compliance Report</span></span>](#bkmk-compliance)

-   [<span data-ttu-id="ddd4f-112">Rapport d’audit de récupération</span><span class="sxs-lookup"><span data-stu-id="ddd4f-112">Recovery Audit Report</span></span>](#bkmk-recovery)

<span data-ttu-id="ddd4f-113">Pour accéder aux rapports MBAM lorsque vous exécutez MBAM dans la topologie autonome, ouvrez un navigateur Web, puis ouvrez le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-113">To access MBAM reports when you are running MBAM in the Stand-alone topology, open a web browser, and then open the Administration and Monitoring Website.</span></span> <span data-ttu-id="ddd4f-114">Dans la barre de menus de gauche, sélectionnez **rapports** .</span><span class="sxs-lookup"><span data-stu-id="ddd4f-114">Select **Reports** in the left menu bar.</span></span> <span data-ttu-id="ddd4f-115">Dans la barre de menus supérieure, sélectionnez le type de rapport que vous souhaitez générer.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-115">From the top menu bar, select the kind of report that you want to generate.</span></span> <span data-ttu-id="ddd4f-116">Pour plus d’informations sur la génération de ces rapports, voir [génération de rapports MBAM 2,5 autonomes](generating-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="ddd4f-116">For more information about generating these reports, see [Generating MBAM 2.5 Stand-alone Reports](generating-mbam-25-stand-alone-reports.md).</span></span>

### <a href="" id="bkmk-enterprisecompliance"></a><span data-ttu-id="ddd4f-117">Rapport de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="ddd4f-117">Enterprise Compliance Report</span></span>

<span data-ttu-id="ddd4f-118">Utilisez ce type de rapport pour collecter des informations sur la conformité de BitLocker globale dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-118">Use this report type to collect information about overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="ddd4f-119">Vous pouvez utiliser des filtres pour affiner vos résultats de recherche et en savoir plus sur l’état de conformité et l’état d’erreur des ordinateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-119">You can use filters to narrow your search results to learn more about the compliance state and error status of computers in your organization.</span></span>

**<span data-ttu-id="ddd4f-120">Présentation de la conformité entreprise</span><span class="sxs-lookup"><span data-stu-id="ddd4f-120">Enterprise Compliance Overview</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ddd4f-121">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="ddd4f-121">Column Name</span></span></th>
<th align="left"><span data-ttu-id="ddd4f-122">Description</span><span class="sxs-lookup"><span data-stu-id="ddd4f-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-123">Ordinateurs gérés</span><span class="sxs-lookup"><span data-stu-id="ddd4f-123">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-124">Nombre d’ordinateurs gérés par MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-124">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-125">Compatibilité%</span><span class="sxs-lookup"><span data-stu-id="ddd4f-125">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-126">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-126">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-127">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="ddd4f-127">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-128">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-128">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-129">Pourcentage d’exonération</span><span class="sxs-lookup"><span data-stu-id="ddd4f-129">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-130">Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-130">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-131">% Non exempté</span><span class="sxs-lookup"><span data-stu-id="ddd4f-131">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-132">Pourcentage d’ordinateurs non exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-132">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-133">Conformes</span><span class="sxs-lookup"><span data-stu-id="ddd4f-133">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-134">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-134">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-135">Non conforme</span><span class="sxs-lookup"><span data-stu-id="ddd4f-135">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-136">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-136">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-137">SIRET</span><span class="sxs-lookup"><span data-stu-id="ddd4f-137">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-138">Nombre total d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-138">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-139">Non exempté</span><span class="sxs-lookup"><span data-stu-id="ddd4f-139">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-140">Nombre total d’ordinateurs qui ne sont pas exemptés de l’exigence de chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-140">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ddd4f-141">Détails de l’ordinateur de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="ddd4f-141">Enterprise Compliance Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ddd4f-142">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="ddd4f-142">Column Name</span></span></th>
<th align="left"><span data-ttu-id="ddd4f-143">Description</span><span class="sxs-lookup"><span data-stu-id="ddd4f-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-144">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-144">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-145">Nom DNS spécifié par l’utilisateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-145">User-specified DNS name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-146">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="ddd4f-146">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-147">Nom de domaine complet sur lequel se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-147">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-148">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="ddd4f-148">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-149">État de la conformité de l’ordinateur, conformément à la stratégie spécifiée pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-149">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="ddd4f-150">Les États ne sont pas conformes et conformes.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-150">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="ddd4f-151">Pour plus d’informations sur l’interprétation des États de conformité, reportez-vous au tableau des États de conformité des rapports de conformité d’entreprise suivants.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-151">See the following Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-152">Question</span><span class="sxs-lookup"><span data-stu-id="ddd4f-152">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-153">État indiquant si cet ordinateur est exempté de la stratégie BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-153">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-154">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="ddd4f-154">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-155">Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-155">Error and status messages about the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-156">Dernier contact</span><span class="sxs-lookup"><span data-stu-id="ddd4f-156">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-157">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-157">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="ddd4f-158">La fréquence de contact est configurable.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-158">The contact frequency is configurable.</span></span> <span data-ttu-id="ddd4f-159">Pour plus d’informations, consultez les paramètres de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-159">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a><span data-ttu-id="ddd4f-160">Rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-160">Computer Compliance Report</span></span>

<span data-ttu-id="ddd4f-161">Utilisez ce type de rapport pour collecter des informations spécifiques à un ordinateur ou à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-161">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="ddd4f-162">Pour afficher ce rapport, cliquez sur le nom de l’ordinateur dans le rapport de conformité d’entreprise, ou tapez le nom de l’ordinateur dans le rapport de conformité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-162">View this report by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="ddd4f-163">Ce rapport affiche des informations de chiffrement détaillées sur chaque lecteur (système d’exploitation et lecteurs de données fixes) sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-163">This report shows detailed encryption information about each drive (operating system and fixed data drives) on a computer.</span></span> <span data-ttu-id="ddd4f-164">Il indique également la stratégie qui s’applique à chaque type de lecteur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-164">It also indicates the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="ddd4f-165">Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-165">To view the details of each drive, expand the Computer Name entry.</span></span>

**<span data-ttu-id="ddd4f-166">Remarque</span><span class="sxs-lookup"><span data-stu-id="ddd4f-166">Note</span></span>**  
<span data-ttu-id="ddd4f-167">Ce rapport ne montre aucun État de cryptage des volumes de données amovibles.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-167">Removable Data Volume encryption status is not shown in this report.</span></span>



**<span data-ttu-id="ddd4f-168">Champs du rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-168">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ddd4f-169">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="ddd4f-169">Column Name</span></span></th>
<th align="left"><span data-ttu-id="ddd4f-170">Description</span><span class="sxs-lookup"><span data-stu-id="ddd4f-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-171">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-171">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-172">Nom d’ordinateur DNS spécifié par l’utilisateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-172">User-specified DNS computer name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-173">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="ddd4f-173">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-174">Nom de domaine complet sur lequel se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-174">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-175">Type d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-175">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-176">Type d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-176">Type of computer.</span></span> <span data-ttu-id="ddd4f-177">Les types valides ne sont pas portables et portables.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-177">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-178">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="ddd4f-178">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-179">Type de système d’exploitation détecté sur l’ordinateur client géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-179">Operating system type found on the client computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-180">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="ddd4f-180">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-181">État de conformité global de l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-181">Overall compliance status of the computer that is managed by MBAM.</span></span> <span data-ttu-id="ddd4f-182">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-182">Valid states are Compliant and Noncompliant.</span></span></p>
<p><span data-ttu-id="ddd4f-183">Notez que l’état de la conformité par lecteur (voir le tableau ci-dessous) est susceptible d’indiquer les différents États de conformité.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-183">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="ddd4f-184">Toutefois, ce champ correspond à cet état de conformité, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-184">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-185">Niveau de cryptage de la stratégie</span><span class="sxs-lookup"><span data-stu-id="ddd4f-185">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-186">Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM (par exemple, 128-bits avec diffuseur).</span><span class="sxs-lookup"><span data-stu-id="ddd4f-186">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-187">Lecteur du système d’exploitation de la stratégie</span><span class="sxs-lookup"><span data-stu-id="ddd4f-187">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-188">Indique si le chiffrement est requis pour le système d’exploitation et le type de protecteur approprié.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-188">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-189">Politique-lecteur de données fixes</span><span class="sxs-lookup"><span data-stu-id="ddd4f-189">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-190">Indique si le chiffrement est requis pour le lecteur de données fixes.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-190">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-191">Lecteur de données amovibles pour une stratégie</span><span class="sxs-lookup"><span data-stu-id="ddd4f-191">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-192">Indique si le chiffrement est requis pour le lecteur amovible.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-192">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-193">Utilisateurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="ddd4f-193">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-194">Utilisateurs connus sur l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-194">Known users on the computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-195">Question</span><span class="sxs-lookup"><span data-stu-id="ddd4f-195">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-196">État indiquant si cet ordinateur est exempté de la stratégie BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-196">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-197">Fabricant</span><span class="sxs-lookup"><span data-stu-id="ddd4f-197">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-198">Nom de fabricant de l’ordinateur, tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-198">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-199">Modèle</span><span class="sxs-lookup"><span data-stu-id="ddd4f-199">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-200">Nom de modèle du fabricant d’ordinateurs, tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-200">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-201">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="ddd4f-201">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-202">Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-202">Error and status messages about the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-203">Dernier contact</span><span class="sxs-lookup"><span data-stu-id="ddd4f-203">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-204">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-204">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="ddd4f-205">La fréquence de contact est configurable.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-205">The contact frequency is configurable.</span></span> <span data-ttu-id="ddd4f-206">Pour plus d’informations, consultez les paramètres de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-206">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ddd4f-207">Champs du rapport de conformité informatique</span><span class="sxs-lookup"><span data-stu-id="ddd4f-207">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ddd4f-208">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="ddd4f-208">Column Name</span></span></th>
<th align="left"><span data-ttu-id="ddd4f-209">Description</span><span class="sxs-lookup"><span data-stu-id="ddd4f-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-210">Lettre du lecteur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-210">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-211">Lettre du lecteur de l’ordinateur qui a été affectée à l’utilisateur en particulier.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-211">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-212">Type de lecteur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-212">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-213">Type de lecteur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-213">Type of drive.</span></span> <span data-ttu-id="ddd4f-214">Les valeurs valides sont le lecteur du système d’exploitation et le lecteur de données fixes.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-214">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="ddd4f-215">Il s’agit de disques physiques plutôt que de volumes logiques.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-215">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-216">Niveau de cryptage</span><span class="sxs-lookup"><span data-stu-id="ddd4f-216">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-217">Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-217">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-218">Type de protecteur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-218">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-219">Type de protecteur sélectionné par le biais du paramètre de stratégie de groupe utilisé pour chiffrer un système d’exploitation ou un volume de données fixe.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-219">Type of protector selected through the Group Policy setting used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-220">État de protecteur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-220">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-221">Indique que l’ordinateur géré par MBAM a activé le type de protecteur qui est spécifié dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-221">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="ddd4f-222">Les États valides sont ACTIVÉs ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-222">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-223">État du chiffrement</span><span class="sxs-lookup"><span data-stu-id="ddd4f-223">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-224">État du chiffrement du lecteur.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-224">Encryption state of the drive.</span></span> <span data-ttu-id="ddd4f-225">Les États valides sont chiffrés, non chiffrés et chiffrés.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-225">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-226">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="ddd4f-226">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-227">État indiquant s’il est conforme à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-227">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="ddd4f-228">Les États ne sont pas conformes et conformes.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-228">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-229">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="ddd4f-229">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-230">Messages d’erreur et de statut de l’état de conformité de l’ordinateur, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-230">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-recovery"></a><span data-ttu-id="ddd4f-231">Rapport d’audit de récupération</span><span class="sxs-lookup"><span data-stu-id="ddd4f-231">Recovery Audit Report</span></span>

<span data-ttu-id="ddd4f-232">Utilisez ce type de rapport pour auditer les utilisateurs qui ont demandé l’accès aux clés de récupération BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-232">Use this report type to audit users who have requested access to BitLocker recovery keys.</span></span> <span data-ttu-id="ddd4f-233">Le rapport propose plusieurs filtres basés sur les critères de filtre souhaités.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-233">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="ddd4f-234">Vous pouvez filtrer sur un type spécifique d’utilisateur (un utilisateur du support technique ou un utilisateur final), si la demande a échoué ou a abouti, le type spécifique de clé demandée et une plage de dates pendant laquelle la récupération s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-234">You can filter on a specific type of user (a Help Desk user or an end user), whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span>

**<span data-ttu-id="ddd4f-235">Champs du rapport d’audit de récupération</span><span class="sxs-lookup"><span data-stu-id="ddd4f-235">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ddd4f-236">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="ddd4f-236">Column Name</span></span></th>
<th align="left"><span data-ttu-id="ddd4f-237">Description</span><span class="sxs-lookup"><span data-stu-id="ddd4f-237">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-238">Demander une date et une heure</span><span class="sxs-lookup"><span data-stu-id="ddd4f-238">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-239">Date et heure auxquelles une demande de récupération de clé a été effectuée par un utilisateur final ou un utilisateur du support technique.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-239">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-240">Source de requête d’audit</span><span class="sxs-lookup"><span data-stu-id="ddd4f-240">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-241">Site à partir duquel la demande a été lancée.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-241">The site from which the request was initiated.</span></span> <span data-ttu-id="ddd4f-242">Cette entrée aura une des deux valeurs suivantes: <strong> portail libre-service </strong> ou <strong> support technique </strong> .</span><span class="sxs-lookup"><span data-stu-id="ddd4f-242">This entry will have one of two values: <strong>Self-Service Portal</strong> or <strong>Helpdesk</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-243">État de la demande</span><span class="sxs-lookup"><span data-stu-id="ddd4f-243">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-244">État de la demande.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-244">Status of the request.</span></span> <span data-ttu-id="ddd4f-245">Les statuts valides sont réussis (la clé a été récupérée) ou FAILED (la clé n’a pas été récupérée).</span><span class="sxs-lookup"><span data-stu-id="ddd4f-245">Valid statuses are Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-246">Utilisateur du support technique</span><span class="sxs-lookup"><span data-stu-id="ddd4f-246">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-247">Utilisateur du support technique à l’origine de la demande de récupération de clé.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-247">Help Desk user who initiated the request for key retrieval.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ddd4f-248">Remarque</span><span class="sxs-lookup"><span data-stu-id="ddd4f-248">Note</span></span></strong><br/><p><span data-ttu-id="ddd4f-249">Si un utilisateur expérimenté du support technique récupère la clé sans spécifier d’utilisateur final, le <strong> champ d’utilisateur final </strong> sera vide.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-249">If an Advanced Helpdesk User recovers the key without specifying the end user, the <strong>End User</strong> field will be blank.</span></span> <span data-ttu-id="ddd4f-250">Un utilisateur du support technique standard doit spécifier l’utilisateur final, et cet utilisateur s’affichera dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-250">A standard Helpdesk User must specify the end user, and that user will appear in this field.</span></span></p>
<p><span data-ttu-id="ddd4f-251">Une récupération par le biais du portail en libre-service entraîne la liste de l’utilisateur à l’origine de la demande dans ce champ et dans le <strong> champ utilisateur final </strong> .</span><span class="sxs-lookup"><span data-stu-id="ddd4f-251">A recovery via the Self-Service Portal will list the requesting end user both in this field and in the <strong>End User</strong> field.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-252">Utilisateur final</span><span class="sxs-lookup"><span data-stu-id="ddd4f-252">End User</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-253">Utilisateur final à l’origine de la demande de récupération de la clé.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-253">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-254">Ordinateur</span><span class="sxs-lookup"><span data-stu-id="ddd4f-254">Computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-255">Nom de l’ordinateur qui a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-255">Computer name of the computer that was recovered.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ddd4f-256">Type de clé</span><span class="sxs-lookup"><span data-stu-id="ddd4f-256">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-257">Type de clé demandée par l’utilisateur du support technique ou par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-257">Type of key that was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="ddd4f-258">Les trois types de clés que MBAM recueille sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="ddd4f-258">The three types of keys that MBAM collects are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ddd4f-259">Mot de passe de clé de récupération (utilisé pour récupérer un ordinateur en mode de récupération)</span><span class="sxs-lookup"><span data-stu-id="ddd4f-259">Recovery Key Password (used to recover a computer in recovery mode)</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-260">ID de clé de récupération (utilisé pour récupérer un ordinateur en mode de récupération pour le compte d’un autre utilisateur)</span><span class="sxs-lookup"><span data-stu-id="ddd4f-260">Recovery Key ID (used to recover a computer in recovery mode on behalf of another user)</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-261">Hachage du mot de passe TPM (utilisé pour récupérer un ordinateur équipé d’un TPM verrouillé)</span><span class="sxs-lookup"><span data-stu-id="ddd4f-261">TPM Password Hash (used to recover a computer with a locked TPM)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ddd4f-262">Description de raison</span><span class="sxs-lookup"><span data-stu-id="ddd4f-262">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="ddd4f-263">Raison le type de clé spécifié a été requis par l’utilisateur du support technique ou par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-263">Reason the specified key type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="ddd4f-264">Les raisons sont indiquées dans les fonctionnalités de récupération des lecteurs et de gestion du TPM du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="ddd4f-264">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring Website.</span></span> <span data-ttu-id="ddd4f-265">Les entrées valides sont du texte entré par l’utilisateur ou l’un des codes de raison suivants:</span><span class="sxs-lookup"><span data-stu-id="ddd4f-265">The valid entries are user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="ddd4f-266">Ordre d’amorçage du système d’exploitation modifié</span><span class="sxs-lookup"><span data-stu-id="ddd4f-266">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-267">Modification du BIOS</span><span class="sxs-lookup"><span data-stu-id="ddd4f-267">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-268">Modification des fichiers du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ddd4f-268">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-269">Clé de démarrage perdue</span><span class="sxs-lookup"><span data-stu-id="ddd4f-269">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-270">Code confidentiel perdu</span><span class="sxs-lookup"><span data-stu-id="ddd4f-270">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-271">Réinitialisation du TPM</span><span class="sxs-lookup"><span data-stu-id="ddd4f-271">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-272">Phrase de passe perdue</span><span class="sxs-lookup"><span data-stu-id="ddd4f-272">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-273">Carte Smartcard perdue</span><span class="sxs-lookup"><span data-stu-id="ddd4f-273">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-274">Réinitialiser le verrouillage du code confidentiel</span><span class="sxs-lookup"><span data-stu-id="ddd4f-274">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-275">Activer le module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="ddd4f-275">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-276">Désactiver le module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="ddd4f-276">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-277">Changer le mot de passe du TPM</span><span class="sxs-lookup"><span data-stu-id="ddd4f-277">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="ddd4f-278">Vider le TPM</span><span class="sxs-lookup"><span data-stu-id="ddd4f-278">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ddd4f-279">Remarque</span><span class="sxs-lookup"><span data-stu-id="ddd4f-279">Note</span></span>**  
<span data-ttu-id="ddd4f-280">Vous pouvez enregistrer des résultats de rapport dans un fichier en cliquant sur le bouton **Exporter** dans la barre de menus **rapports** .</span><span class="sxs-lookup"><span data-stu-id="ddd4f-280">Report results can be saved to a file by clicking the **Export** button on the **Reports** menu bar.</span></span>




## <span data-ttu-id="ddd4f-281">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ddd4f-281">Related topics</span></span>


[<span data-ttu-id="ddd4f-282">Surveillance et création de rapports de la conformité BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ddd4f-282">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="ddd4f-283">Génération des rapports MBAM2.5 autonomes</span><span class="sxs-lookup"><span data-stu-id="ddd4f-283">Generating MBAM 2.5 Stand-alone Reports</span></span>](generating-mbam-25-stand-alone-reports.md)



## <span data-ttu-id="ddd4f-284">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="ddd4f-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ddd4f-285">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="ddd4f-285">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ddd4f-286">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ddd4f-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 






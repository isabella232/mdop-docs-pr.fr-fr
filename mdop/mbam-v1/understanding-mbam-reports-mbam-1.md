---
title: Compréhension des rapports MBAM
description: Compréhension des rapports MBAM
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809612"
---
# <span data-ttu-id="c9181-103">Compréhension des rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="c9181-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="c9181-104">Microsoft BitLocker administration et analyse (MBAM) génère divers rapports pour contrôler l’utilisation et la conformité de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c9181-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="c9181-105">Cette rubrique décrit les rapports MBAM à des fins de conformité d’entreprise, d’ordinateurs individuels, de compatibilité matérielle et d’activité de récupération de clés.</span><span class="sxs-lookup"><span data-stu-id="c9181-105">This topic describes the MBAM reports for enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span>

## <span data-ttu-id="c9181-106">Présentation des rapports</span><span class="sxs-lookup"><span data-stu-id="c9181-106">Understanding Reports</span></span>


<span data-ttu-id="c9181-107">Pour accéder à la fonctionnalité rapports d’MBAM, ouvrez le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-107">To access the Reports feature of MBAM, open the MBAM administration website.</span></span> <span data-ttu-id="c9181-108">Sélectionnez **rapports** dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="c9181-108">Select **Reports** in the navigation pane.</span></span> <span data-ttu-id="c9181-109">Ensuite, dans le volet contenu principal, cliquez sur l’onglet correspondant à votre type de rapport: **rapport de conformité d’entreprise**, rapport de conformité d' **ordinateur**, rapport **d’audit matériel**ou **rapport d’audit de récupération**.</span><span class="sxs-lookup"><span data-stu-id="c9181-109">Then, in the main content pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

### <span data-ttu-id="c9181-110">Rapport de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="c9181-110">Enterprise Compliance Report</span></span>

<span data-ttu-id="c9181-111">Un rapport de conformité d’entreprise fournit des informations sur la conformité de BitLocker globale au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c9181-111">An Enterprise Compliance Report provides information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="c9181-112">Les filtres disponibles pour ce rapport vous permettent d’affiner vos résultats de recherche en fonction de l’état de conformité et de l’état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c9181-112">The available filters for this report allow you to narrow your search results according to Compliance state and Error status.</span></span> <span data-ttu-id="c9181-113">Ce rapport s’exécute toutes les six heures.</span><span class="sxs-lookup"><span data-stu-id="c9181-113">This report runs every six hours.</span></span>

**<span data-ttu-id="c9181-114">Champs rapport de conformité entreprise</span><span class="sxs-lookup"><span data-stu-id="c9181-114">Enterprise Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9181-115">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c9181-115">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c9181-116">Description</span><span class="sxs-lookup"><span data-stu-id="c9181-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-117">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c9181-117">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-118">Nom DNS spécifié par l’utilisateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-118">The user-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-119">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="c9181-119">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-120">Nom de domaine complet sur lequel se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-120">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-121">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="c9181-121">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-122">État de la conformité de l’ordinateur, selon la stratégie spécifiée pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-122">The state of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="c9181-123">Les États possibles sont non conformes et conformes.</span><span class="sxs-lookup"><span data-stu-id="c9181-123">The possible states are Noncompliant and Compliant.</span></span> <span data-ttu-id="c9181-124">Pour plus d’informations, reportez-vous à la section État de conformité des rapports de conformité d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c9181-124">For more information, see Enterprise Compliance Report Compliance States in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-125">Question</span><span class="sxs-lookup"><span data-stu-id="c9181-125">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-126">État du matériel de l’ordinateur pour déterminer l’identification du type de matériel et si l’ordinateur est exempté d’une stratégie.</span><span class="sxs-lookup"><span data-stu-id="c9181-126">The state of the computer hardware for determining the identification of the hardware type and whether the computer is exempt from policy.</span></span> <span data-ttu-id="c9181-127">Il existe trois États possibles: matériel inconnu (le type de matériel n’a pas été identifié par MBAM), exonéré du matériel (le type de matériel a été identifié et marqué comme exempt de la stratégie de MBAM) et non exempté (le matériel a été identifié et n’est pas exempt de la stratégie).</span><span class="sxs-lookup"><span data-stu-id="c9181-127">There are three possible states: Hardware Unknown (the hardware type has not been identified by MBAM), Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy), and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-128">Utilisateurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="c9181-128">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-129">Utilisateurs connus sur l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-129">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-130">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="c9181-130">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-131">Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c9181-131">Error and status messages about the compliance state of the computer in accordance to the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-132">Dernier contact</span><span class="sxs-lookup"><span data-stu-id="c9181-132">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-133">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="c9181-133">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="c9181-134">Ce temps est configurable.</span><span class="sxs-lookup"><span data-stu-id="c9181-134">This time is configurable.</span></span> <span data-ttu-id="c9181-135">Voir paramètres de stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-135">See MBAM policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c9181-136">États de conformité des rapports de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="c9181-136">Enterprise Compliance Report Compliance states</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9181-137">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="c9181-137">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="c9181-138">Question</span><span class="sxs-lookup"><span data-stu-id="c9181-138">Exemption</span></span></th>
<th align="left"><span data-ttu-id="c9181-139">Description</span><span class="sxs-lookup"><span data-stu-id="c9181-139">Description</span></span></th>
<th align="left"><span data-ttu-id="c9181-140">Action de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c9181-140">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-141">Non conforme</span><span class="sxs-lookup"><span data-stu-id="c9181-141">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-142">Ne pas exempter</span><span class="sxs-lookup"><span data-stu-id="c9181-142">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-143">L’ordinateur n’est pas conforme conformément à la stratégie spécifiée, et le type de matériel n’a pas été indiqué comme exempt de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c9181-143">The computer is noncompliant according to the specified policy, and the hardware type has not been indicated as exempt from policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-144">Cliquez sur <strong> nom </strong> de l’ordinateur pour développer le rapport de conformité de l’ordinateur et déterminer si l’état de chaque lecteur répond à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c9181-144">Click <strong>Computer Name</strong> to expand the Computer Compliance Report and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="c9181-145">S’il s’agit d’un état de chiffrement indiquant que l’ordinateur n’est pas chiffré, il est possible que le chiffrement soit en cours de traitement ou qu’il y ait une erreur sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-145">If the encryption state indicates that the computer is not encrypted, encryption might still be in process, or there might be an error on the computer.</span></span> <span data-ttu-id="c9181-146">S’il n’y a aucune erreur, il est probable que l’ordinateur est toujours en train de se connecter ou de définir l’état de cryptage.</span><span class="sxs-lookup"><span data-stu-id="c9181-146">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="c9181-147">Revenez à l’étape précédente pour déterminer si l’état change.</span><span class="sxs-lookup"><span data-stu-id="c9181-147">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-148">Conformes</span><span class="sxs-lookup"><span data-stu-id="c9181-148">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-149">Ne pas exempter</span><span class="sxs-lookup"><span data-stu-id="c9181-149">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-150">L’ordinateur est conforme conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c9181-150">The computer is compliant in accordance with the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-151">Aucune action nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c9181-151">No Action needed.</span></span> <span data-ttu-id="c9181-152">Vous pouvez également afficher le rapport de conformité de l’ordinateur pour vérifier l’état de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-152">Optionally, you can view the Computer Compliance Report to confirm the state of the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-153">Conformes</span><span class="sxs-lookup"><span data-stu-id="c9181-153">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-154">Exemption matérielle</span><span class="sxs-lookup"><span data-stu-id="c9181-154">Hardware Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-155">Si le type de matériel est exonéré.</span><span class="sxs-lookup"><span data-stu-id="c9181-155">If the Hardware type is exempt.</span></span> <span data-ttu-id="c9181-156">Quelle que soit la façon dont la stratégie est définie ou du statut individuel de chaque disque dur, l’état global est considéré comme conforme.</span><span class="sxs-lookup"><span data-stu-id="c9181-156">Regardless of how the policy is set or the individual status of each hard-drive, the overall state is considered to be compliant.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-157">Aucune action nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c9181-157">No action needed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-158">Conformes</span><span class="sxs-lookup"><span data-stu-id="c9181-158">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-159">Matériel inconnu</span><span class="sxs-lookup"><span data-stu-id="c9181-159">Hardware Unknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-160">MBAM reconnaît le type de matériel, mais MBAM ne sait pas s’il est exempté ou n’est pas exempté.</span><span class="sxs-lookup"><span data-stu-id="c9181-160">MBAM recognizes the hardware type, but MBAM does not know whether it is exempt or not exempt.</span></span> <span data-ttu-id="c9181-161">Ce problème se produit si l’administrateur n’a pas défini l’État compatible du matériel.</span><span class="sxs-lookup"><span data-stu-id="c9181-161">This occurs if the administrator has not set the Compatible status for the hardware.</span></span> <span data-ttu-id="c9181-162">Par conséquent, MBAM rétablit l’État conforme par défaut.</span><span class="sxs-lookup"><span data-stu-id="c9181-162">Therefore, MBAM reverts to Compliant status by default.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-163">Il s’agit de l’état initial d’un nouveau client MBAM déployé.</span><span class="sxs-lookup"><span data-stu-id="c9181-163">This is the initial state of a newly deployed MBAM client.</span></span> <span data-ttu-id="c9181-164">Il s’agit généralement d’un état temporaire.</span><span class="sxs-lookup"><span data-stu-id="c9181-164">It is typically only a transient state.</span></span> <span data-ttu-id="c9181-165">Même si l’administrateur a marqué le matériel comme étant compatible, il est possible qu’il y ait un délai important ou un délai d’attente configuré pour signaler l’état de l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="c9181-165">Even if the administrator has marked the Hardware as Compatible, there can be a significant delay or configurable wait time before the client computer reports back in.</span></span> <span data-ttu-id="c9181-166">Prenez note de l’heure du dernier contact et recommencez après l’intervalle spécifié pour voir si l’État a changé.</span><span class="sxs-lookup"><span data-stu-id="c9181-166">Make note of the time of Last Contact, and check in again after the specified interval to see if the state has changed.</span></span> <span data-ttu-id="c9181-167">Si l’État n’a pas changé, il est possible qu’il y ait une erreur pour ce type d’ordinateur ou de matériel.</span><span class="sxs-lookup"><span data-stu-id="c9181-167">If the state has not changed, there may be an error for this computer or hardware type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c9181-168">Rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="c9181-168">Computer Compliance Report</span></span>

<span data-ttu-id="c9181-169">Le rapport de conformité informatique affiche des informations spécifiques à un ordinateur ou à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-169">The Computer Compliance Report displays information that is specific to a computer or user.</span></span>

<span data-ttu-id="c9181-170">Le rapport de conformité informatique fournit des informations de chiffrement détaillées et des stratégies applicables pour chaque lecteur sur un ordinateur, notamment les lecteurs de systèmes d’exploitation et les lecteurs de données fixes.</span><span class="sxs-lookup"><span data-stu-id="c9181-170">The Computer Compliance Report provides detailed encryption information and applicable policies for each drive on a computer, including operating system drives and fixed data drives.</span></span> <span data-ttu-id="c9181-171">Pour afficher ce type de rapport, cliquez sur le nom de l’ordinateur dans le rapport de conformité d’entreprise ou tapez le nom de l’ordinateur dans le rapport de conformité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-171">To view this report type, click the computer name in the Enterprise Compliance Report or type the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="c9181-172">Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-172">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="c9181-173">**Remarques**  Ce rapport ne fournit pas d’état de chiffrement pour les volumes de données amovibles.</span><span class="sxs-lookup"><span data-stu-id="c9181-173">**Note** This report does not provide encryption status for Removable Data Volumes.</span></span>

 

**<span data-ttu-id="c9181-174">Champs du rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="c9181-174">Computer Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9181-175">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c9181-175">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c9181-176">Description</span><span class="sxs-lookup"><span data-stu-id="c9181-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-177">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c9181-177">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-178">Nom de l’ordinateur DNS spécifié par l’utilisateur qui est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-178">The user-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-179">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="c9181-179">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-180">Nom de domaine complet sur lequel se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-180">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-181">Type d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c9181-181">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-182">Type de portabilité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-182">The portability type of computer.</span></span> <span data-ttu-id="c9181-183">Les types valides ne sont pas portables et portables.</span><span class="sxs-lookup"><span data-stu-id="c9181-183">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-184">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="c9181-184">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-185">Type de système d’exploitation installé sur l’ordinateur client géré MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-185">Operating System type installed on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-186">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="c9181-186">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-187">État de conformité global de l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-187">The overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="c9181-188">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="c9181-188">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="c9181-189">S’il est possible d’utiliser des lecteurs compatibles et non conformes sur le même ordinateur, ce champ indique la conformité globale de l’ordinateur par stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c9181-189">While it is possible to have Compliant and Noncompliant drives in the same computer, this field indicates the overall computer compliance per specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-190">Force de Cypher de stratégie</span><span class="sxs-lookup"><span data-stu-id="c9181-190">Policy Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-191">Le niveau de cryptage sélectionné par l’administrateur lors de la spécification de la stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-191">The Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="c9181-192">Par exemple, 128-bit avec diffuseur</span><span class="sxs-lookup"><span data-stu-id="c9181-192">For example, 128-bit with Diffuser</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-193">Lecteur du système d’exploitation de la stratégie</span><span class="sxs-lookup"><span data-stu-id="c9181-193">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-194">Indique si le chiffrement est requis pour les e/S et le type de protecteur applicable.</span><span class="sxs-lookup"><span data-stu-id="c9181-194">Indicates whether encryption is required for the O/S and the protector type as applicable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-195">Policy Data-Fixed Data</span><span class="sxs-lookup"><span data-stu-id="c9181-195">Policy Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-196">Indique si le chiffrement est requis pour le lecteur fixe.</span><span class="sxs-lookup"><span data-stu-id="c9181-196">Indicates whether encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-197">Lecteur de données amovibles pour une stratégie</span><span class="sxs-lookup"><span data-stu-id="c9181-197">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-198">Indique si le chiffrement est requis pour le lecteur amovible.</span><span class="sxs-lookup"><span data-stu-id="c9181-198">Indicates whether encryption is required for the Removable Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-199">Utilisateurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="c9181-199">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-200">Fournit l’identité des utilisateurs connus de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-200">Provides the identity of known users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-201">Question</span><span class="sxs-lookup"><span data-stu-id="c9181-201">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-202">Indique si le type de matériel de l’ordinateur est reconnu par MBAM et, si ce dernier a été signalé comme exempt de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c9181-202">Indicates whether the computer hardware type is recognized by MBAM and, if known, whether the computer has been indicated as exempt from policy.</span></span> <span data-ttu-id="c9181-203">Il existe trois États: matériel inconnu (le type de matériel n’a pas été identifié par MBAM); Exemption matérielle (le type de matériel a été identifié et est marqué comme exempt de la stratégie MBAM); et non exempté (le matériel a été identifié et n’est pas exempté de la stratégie).</span><span class="sxs-lookup"><span data-stu-id="c9181-203">There are three states: Hardware Unknown (the hardware type has not been identified by MBAM); Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy); and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-204">Fabricant</span><span class="sxs-lookup"><span data-stu-id="c9181-204">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-205">Le nom du fabricant de l’ordinateur tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-205">The computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-206">Modèle</span><span class="sxs-lookup"><span data-stu-id="c9181-206">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-207">Le nom du modèle de fabricant d’ordinateurs tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-207">The computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-208">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="c9181-208">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-209">Messages d’erreur et d’état de l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c9181-209">Error and status messages of the compliance state of the computer in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-210">Dernier contact</span><span class="sxs-lookup"><span data-stu-id="c9181-210">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-211">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="c9181-211">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="c9181-212">T</span><span class="sxs-lookup"><span data-stu-id="c9181-212">T</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c9181-213">Champs du rapport de conformité informatique</span><span class="sxs-lookup"><span data-stu-id="c9181-213">Computer Compliance Report Drive fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9181-214">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c9181-214">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c9181-215">Description</span><span class="sxs-lookup"><span data-stu-id="c9181-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-216">Lettre du lecteur</span><span class="sxs-lookup"><span data-stu-id="c9181-216">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-217">Lettre du lecteur de l’ordinateur qui a été affectée à ce lecteur particulier par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-217">Computer drive letter that was assigned to this particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-218">Type de lecteur</span><span class="sxs-lookup"><span data-stu-id="c9181-218">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-219">Type de lecteur.</span><span class="sxs-lookup"><span data-stu-id="c9181-219">Type of drive.</span></span> <span data-ttu-id="c9181-220">Les valeurs valides sont le lecteur du système d’exploitation et le lecteur de données fixes.</span><span class="sxs-lookup"><span data-stu-id="c9181-220">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="c9181-221">Il s’agit de disques physiques plutôt que de volumes logiques.</span><span class="sxs-lookup"><span data-stu-id="c9181-221">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-222">Cypher Strength</span><span class="sxs-lookup"><span data-stu-id="c9181-222">Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-223">Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-223">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-224">Type de protecteur</span><span class="sxs-lookup"><span data-stu-id="c9181-224">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-225">Type de protecteur sélectionné via une stratégie utilisée pour chiffrer un système d’exploitation ou un volume fixe.</span><span class="sxs-lookup"><span data-stu-id="c9181-225">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="c9181-226">Les types de protecteur valides sur un lecteur de système d’exploitation sont TPM ou TPM + NIP.</span><span class="sxs-lookup"><span data-stu-id="c9181-226">The valid protector types on an operating system drive are TPM or TPM+PIN.</span></span> <span data-ttu-id="c9181-227">Le seul type de protecteur valide pour un volume de données fixe est Password.</span><span class="sxs-lookup"><span data-stu-id="c9181-227">The only valid protector type for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-228">État de protecteur</span><span class="sxs-lookup"><span data-stu-id="c9181-228">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-229">Ce champ indique si l’ordinateur a activé le type de protecteur spécifié dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c9181-229">This field indicates whether the computer has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="c9181-230">Les États valides sont ACTIVÉs ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="c9181-230">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-231">État du chiffrement</span><span class="sxs-lookup"><span data-stu-id="c9181-231">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-232">Il s’agit de l’état de chiffrement actuel du lecteur.</span><span class="sxs-lookup"><span data-stu-id="c9181-232">This is the current encryption state of the drive.</span></span> <span data-ttu-id="c9181-233">Les États valides sont chiffrés, non chiffrés et chiffrés.</span><span class="sxs-lookup"><span data-stu-id="c9181-233">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-234">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="c9181-234">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-235">Indique si le lecteur est conforme à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c9181-235">Indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="c9181-236">Les États ne sont pas conformes et conformes.</span><span class="sxs-lookup"><span data-stu-id="c9181-236">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-237">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="c9181-237">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-238">Contient des messages d’erreur et de statut concernant l’état de conformité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c9181-238">Contains error and status messages regarding the compliance state of the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c9181-239">Rapport d’audit matériel</span><span class="sxs-lookup"><span data-stu-id="c9181-239">Hardware Audit Report</span></span>

<span data-ttu-id="c9181-240">Ce rapport peut vous aider à effectuer le suivi des modifications apportées à l’état de compatibilité matérielle de modèles et de modèles d’ordinateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c9181-240">This report can help you audit changes to the Hardware Compatibility status of specific computer makes and models.</span></span> <span data-ttu-id="c9181-241">Pour vous aider à affiner vos résultats de recherche, ce rapport inclut le filtrage sur des critères tels que le type de modification et l’heure d’apparition.</span><span class="sxs-lookup"><span data-stu-id="c9181-241">To help you narrow your search results, this report includes filtering on criteria such as type of change and time of occurrence.</span></span> <span data-ttu-id="c9181-242">Le suivi de chaque modification d’état dépend de l’utilisateur et de la date et de l’heure.</span><span class="sxs-lookup"><span data-stu-id="c9181-242">Each state change is tracked by user and date and time.</span></span> <span data-ttu-id="c9181-243">Le type de matériel est automatiquement rempli par l’agent MBAM qui s’exécute sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="c9181-243">The Hardware Type is automatically populated by the MBAM agent that runs on the client computer.</span></span> <span data-ttu-id="c9181-244">Ce rapport effectue le suivi des modifications apportées par l’utilisateur aux informations collectées directement depuis l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c9181-244">This report tracks user changes to the information collected directly from the MBAM managed computer.</span></span> <span data-ttu-id="c9181-245">Un changement d’administration classique consiste à changer de compatibilité en incompatibilité.</span><span class="sxs-lookup"><span data-stu-id="c9181-245">A typical administrative change is changing from Compatible to incompatible.</span></span> <span data-ttu-id="c9181-246">Toutefois, l’administrateur peut également modifier n’importe quel champ.</span><span class="sxs-lookup"><span data-stu-id="c9181-246">However, the administrator can also revise any field.</span></span>

**<span data-ttu-id="c9181-247">Champs du rapport d’audit matériel</span><span class="sxs-lookup"><span data-stu-id="c9181-247">Hardware Audit Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9181-248">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c9181-248">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c9181-249">Description</span><span class="sxs-lookup"><span data-stu-id="c9181-249">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-250">Date et heure</span><span class="sxs-lookup"><span data-stu-id="c9181-250">Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-251">Date et heure auxquelles une modification a été apportée au type de matériel.</span><span class="sxs-lookup"><span data-stu-id="c9181-251">Date and time that a change was made to the Hardware Type.</span></span> <span data-ttu-id="c9181-252">Notez que chaque type de matériel unique est affecté à au moins une entrée.</span><span class="sxs-lookup"><span data-stu-id="c9181-252">Note that every unique hardware type is assigned to at least one entry.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-253">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="c9181-253">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-254">Utilisateur administratif ayant modifié le changement pour l’entrée en particulier.</span><span class="sxs-lookup"><span data-stu-id="c9181-254">Administrative user that has made the change for the particular entry.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-255">Changer de type</span><span class="sxs-lookup"><span data-stu-id="c9181-255">Change Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-256">Type de modification apportée aux informations de type de matériel.</span><span class="sxs-lookup"><span data-stu-id="c9181-256">Type of change that was made to the hardware type information.</span></span> <span data-ttu-id="c9181-257">Les valeurs valides sont addition (nouvelle entrée), mise à jour (modifier une entrée existante) ou suppression (suppression d’entrée existante).</span><span class="sxs-lookup"><span data-stu-id="c9181-257">Valid values are Addition (new entry), Update (change existing entry), or Deletion (remove existing entry).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-258">Valeur d’origine</span><span class="sxs-lookup"><span data-stu-id="c9181-258">Original Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-259">Valeur de la spécification du type de matériel avant la modification.</span><span class="sxs-lookup"><span data-stu-id="c9181-259">Value of the hardware type specification before the change was made.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-260">Valeur actuelle</span><span class="sxs-lookup"><span data-stu-id="c9181-260">Current Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-261">Valeur de la spécification de type matérielle une fois la modification effectuée.</span><span class="sxs-lookup"><span data-stu-id="c9181-261">Value of the hardware type specification after the change was made.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c9181-262">Rapport d’audit de récupération</span><span class="sxs-lookup"><span data-stu-id="c9181-262">Recovery Audit Report</span></span>

<span data-ttu-id="c9181-263">Le rapport d’audit de récupération peut vous aider à contrôler les utilisateurs qui ont demandé l’accès aux clés de récupération.</span><span class="sxs-lookup"><span data-stu-id="c9181-263">The Recovery Audit Report can help you audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="c9181-264">Les critères de filtre pour ce rapport incluent le type d’utilisateur à l’origine de la demande, le type de clé demandée, l’heure d’apparition, la réussite ou l’échec, l’heure d’apparition et le type d’utilisateur demandant (support technique, utilisateur final).</span><span class="sxs-lookup"><span data-stu-id="c9181-264">The filter criteria for this report includes type of user making the request, type of key requested, time of occurrence, success or fail, time of occurrence, and type of user requesting (help desk, end user).</span></span> <span data-ttu-id="c9181-265">Ce rapport permet aux administrateurs de produire des rapports contextuels en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="c9181-265">This report enables administrators to produce contextual reports based on need.</span></span>

**<span data-ttu-id="c9181-266">Champs du rapport d’audit de récupération</span><span class="sxs-lookup"><span data-stu-id="c9181-266">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9181-267">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c9181-267">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c9181-268">Description</span><span class="sxs-lookup"><span data-stu-id="c9181-268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-269">Demander une date et une heure</span><span class="sxs-lookup"><span data-stu-id="c9181-269">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-270">Date et heure auxquelles une demande de récupération de clé a été effectuée par un utilisateur final ou un utilisateur du support technique.</span><span class="sxs-lookup"><span data-stu-id="c9181-270">The date and time that a key retrieval request was made by an end user or help desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-271">État de la demande</span><span class="sxs-lookup"><span data-stu-id="c9181-271">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-272">État de la demande.</span><span class="sxs-lookup"><span data-stu-id="c9181-272">Status of the request.</span></span> <span data-ttu-id="c9181-273">Les statuts valides sont réussis (la clé a été récupérée) ou FAILED (la clé n’est pas récupérée).</span><span class="sxs-lookup"><span data-stu-id="c9181-273">Valid statuses are either Successful (the key was retrieved) or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-274">Utilisateur du support technique</span><span class="sxs-lookup"><span data-stu-id="c9181-274">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-275">L’utilisateur du support technique ayant lancé la demande de récupération de la clé.</span><span class="sxs-lookup"><span data-stu-id="c9181-275">The help desk user who initiated the request for key retrieval.</span></span> <span data-ttu-id="c9181-276">Si l’utilisateur du support technique récupère la clé pour le compte d’un utilisateur final, le champ utilisateur final sera vide.</span><span class="sxs-lookup"><span data-stu-id="c9181-276">If the help desk user retrieves the key on behalf of an end user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-277">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="c9181-277">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-278">Utilisateur final à l’origine de la demande de récupération de la clé.</span><span class="sxs-lookup"><span data-stu-id="c9181-278">The end user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9181-279">Type de clé</span><span class="sxs-lookup"><span data-stu-id="c9181-279">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-280">Type de clé demandée.</span><span class="sxs-lookup"><span data-stu-id="c9181-280">The type of key that was requested.</span></span> <span data-ttu-id="c9181-281">MBAM collecte trois types de clé: mot de passe de clé de récupération (pour récupérer un ordinateur en mode de récupération); ID de la clé de récupération (pour récupérer un ordinateur en mode de récupération pour le compte d’un autre utilisateur); et le hachage du mot de passe du module de plateforme sécurisée (TPM) (pour récupérer un ordinateur avec un TPM verrouillé).</span><span class="sxs-lookup"><span data-stu-id="c9181-281">MBAM collects three key types: Recovery Key Password (to recovery a computer in recovery mode); Recovery Key ID (to recover a computer in recovery mode on behalf of another user); and Trusted Platform Module (TPM) Password Hash (to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9181-282">Description de raison</span><span class="sxs-lookup"><span data-stu-id="c9181-282">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9181-283">Raison d’une demande du type de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="c9181-283">The reason that the specified Key Type was requested.</span></span> <span data-ttu-id="c9181-284">Les raisons sont indiquées dans les fonctionnalités de récupération des lecteurs et de gestion du TPM du site Web d’administration.</span><span class="sxs-lookup"><span data-stu-id="c9181-284">The reasons are specified in the Drive Recovery and Manage TPM features of the Administrative web site.</span></span> <span data-ttu-id="c9181-285">Les entrées valides incluent le texte entré par l’utilisateur ou l’un des codes de raison suivants:</span><span class="sxs-lookup"><span data-stu-id="c9181-285">Valid entries include user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="c9181-286">Ordre d’amorçage du système d’exploitation modifié</span><span class="sxs-lookup"><span data-stu-id="c9181-286">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="c9181-287">Modification du BIOS</span><span class="sxs-lookup"><span data-stu-id="c9181-287">BIOS changed</span></span></p></li>
<li><p><span data-ttu-id="c9181-288">Modification des fichiers du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="c9181-288">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="c9181-289">Clé de démarrage perdue</span><span class="sxs-lookup"><span data-stu-id="c9181-289">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="c9181-290">Code confidentiel perdu</span><span class="sxs-lookup"><span data-stu-id="c9181-290">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="c9181-291">Réinitialisation du TPM</span><span class="sxs-lookup"><span data-stu-id="c9181-291">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="c9181-292">Phrase de passe perdue</span><span class="sxs-lookup"><span data-stu-id="c9181-292">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="c9181-293">Carte Smartcard perdue</span><span class="sxs-lookup"><span data-stu-id="c9181-293">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="c9181-294">Réinitialiser le verrouillage du code confidentiel</span><span class="sxs-lookup"><span data-stu-id="c9181-294">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="c9181-295">Activer le module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="c9181-295">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="c9181-296">Désactiver le module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="c9181-296">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="c9181-297">Changer le mot de passe du TPM</span><span class="sxs-lookup"><span data-stu-id="c9181-297">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="c9181-298">Vider le TPM</span><span class="sxs-lookup"><span data-stu-id="c9181-298">Clear TPM</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c9181-299">**Remarques**  Pour enregistrer les résultats d’un rapport dans un fichier, cliquez sur le bouton **Exporter** dans la barre de menus rapports.</span><span class="sxs-lookup"><span data-stu-id="c9181-299">**Note** To save report results to a file, click the **Export** button on the reports menu bar.</span></span>

 

## <span data-ttu-id="c9181-300">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9181-300">Related topics</span></span>


[<span data-ttu-id="c9181-301">Surveillance et création de rapports de la conformité BitLocker avec MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="c9181-301">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 






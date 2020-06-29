---
title: Compréhension des rapports MBAM
description: Compréhension des rapports MBAM
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810181"
---
# <span data-ttu-id="36b57-103">Compréhension des rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="36b57-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="36b57-104">Si vous avez choisi la topologie autonome lors de l’installation de Microsoft BitLocker administration et de la surveillance (MBAM), vous pouvez exécuter différents rapports dans MBAM pour contrôler l’utilisation et la conformité de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="36b57-104">If you chose the Stand-alone topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), you can run different reports in MBAM to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="36b57-105">MBAM indique la conformité et d’autres informations sur tous les ordinateurs et appareils qu’il gère.</span><span class="sxs-lookup"><span data-stu-id="36b57-105">MBAM reports compliance and other information about all of the computers and devices it manages.</span></span> <span data-ttu-id="36b57-106">Les informations contenues dans cette rubrique peuvent être utilisées pour vous aider à comprendre les rapports d’administration et de surveillance de BitLocker pour les entreprises et les rapports de compatibilité des ordinateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="36b57-106">The information in this topic can be used to help you understand the Microsoft BitLocker Administration and Monitoring reports for enterprise and individual computer compliance and for key recovery activity.</span></span>

<span data-ttu-id="36b57-107">**Remarques**  Si vous avez choisi la topologie Configuration Manager lors de l’installation de Microsoft BitLocker administration et de la surveillance (MBAM), les rapports sont générés à partir de Configuration Manager plutôt que d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="36b57-107">**Note** If you chose the Configuration Manager topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), reports are generated from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="36b57-108">Pour plus d’informations sur les rapports qui sont exécutés à partir de Configuration Manager, voir [Présentation des rapports MBAM dans Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="36b57-108">For more information about reports that are run from Configuration Manager, see [Understanding MBAM Reports in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span></span>

 

## <span data-ttu-id="36b57-109">Présentation des rapports</span><span class="sxs-lookup"><span data-stu-id="36b57-109">Understanding Reports</span></span>


<span data-ttu-id="36b57-110">Pour accéder à la fonctionnalité rapports d’administration et de contrôle Microsoft BitLocker, ouvrez un navigateur Web et ouvrez le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="36b57-110">To access the Reports feature of Microsoft BitLocker Administration and Monitoring, open a web browser and open the Administration and Monitoring website.</span></span> <span data-ttu-id="36b57-111">Dans la barre de menus de gauche, sélectionnez **rapports** , puis dans la barre de menus supérieure, sélectionnez le type de rapport que vous souhaitez générer.</span><span class="sxs-lookup"><span data-stu-id="36b57-111">Select **Reports** in the left menu bar and then select from the top menu bar the kind of report that you want to generate.</span></span>

### <span data-ttu-id="36b57-112">Rapport de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="36b57-112">Enterprise Compliance Report</span></span>

<span data-ttu-id="36b57-113">Utilisez ce type de rapport pour collecter des informations sur la conformité de BitLocker globale dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="36b57-113">Use this report type to collect information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="36b57-114">Vous pouvez utiliser des filtres différents pour affiner vos résultats de recherche en fonction de l’état de conformité et de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="36b57-114">You can use different filters to narrow your search results to Compliance state and Error status.</span></span> <span data-ttu-id="36b57-115">Les informations du rapport sont actualisées toutes les six heures.</span><span class="sxs-lookup"><span data-stu-id="36b57-115">The report information is updated every six hours.</span></span>

**<span data-ttu-id="36b57-116">Champs rapport de conformité entreprise</span><span class="sxs-lookup"><span data-stu-id="36b57-116">Enterprise Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="36b57-117">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="36b57-117">Column Name</span></span></th>
<th align="left"><span data-ttu-id="36b57-118">Description</span><span class="sxs-lookup"><span data-stu-id="36b57-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-119">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="36b57-119">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-120">Nom DNS spécifié par l’utilisateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="36b57-120">User-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-121">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="36b57-121">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-122">Nom de domaine complet sur lequel se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="36b57-122">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-123">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="36b57-123">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-124">État de la conformité de l’ordinateur, conformément à la stratégie spécifiée pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36b57-124">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="36b57-125">Les États ne sont pas conformes et conformes.</span><span class="sxs-lookup"><span data-stu-id="36b57-125">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="36b57-126">Pour plus d’informations sur l’interprétation des États de conformité, voir le tableau des États de conformité des rapports de conformité d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="36b57-126">See the Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-127">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="36b57-127">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-128">Messages d’erreur et d’état de l’état de conformité de l’ordinateur conformément à la politique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36b57-128">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-129">Dernier contact</span><span class="sxs-lookup"><span data-stu-id="36b57-129">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-130">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="36b57-130">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="36b57-131">La fréquence de contact est configurable (voir paramètres de la stratégie MBAM).</span><span class="sxs-lookup"><span data-stu-id="36b57-131">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="36b57-132">États de conformité des rapports de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="36b57-132">Enterprise Compliance Report Compliance States</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="36b57-133">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="36b57-133">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="36b57-134">Question</span><span class="sxs-lookup"><span data-stu-id="36b57-134">Exemption</span></span></th>
<th align="left"><span data-ttu-id="36b57-135">Description</span><span class="sxs-lookup"><span data-stu-id="36b57-135">Description</span></span></th>
<th align="left"><span data-ttu-id="36b57-136">Action de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="36b57-136">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-137">Non conforme</span><span class="sxs-lookup"><span data-stu-id="36b57-137">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-138">Ne pas exempter</span><span class="sxs-lookup"><span data-stu-id="36b57-138">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-139">L’ordinateur n’est pas conforme, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36b57-139">The computer is noncompliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-140">Développez les détails du rapport de conformité de l’ordinateur en cliquant sur <strong> nom </strong> de l’ordinateur et déterminez si l’état de chaque lecteur répond à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36b57-140">Expand the Computer Compliance Report details by clicking <strong>Computer Name</strong>, and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="36b57-141">S’il s’agit de l’état de chiffrement indiquant que l’ordinateur n’est pas chiffré, le chiffrement est peut-être en cours de traitement ou il y a une erreur sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36b57-141">If the encryption state indicates that the computer is not encrypted, encryption may be in process, or there is an error on the computer.</span></span> <span data-ttu-id="36b57-142">S’il n’y a aucune erreur, il est probable que l’ordinateur est toujours en train de se connecter ou de définir l’état de cryptage.</span><span class="sxs-lookup"><span data-stu-id="36b57-142">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="36b57-143">Revenez à l’étape précédente pour déterminer si l’état change.</span><span class="sxs-lookup"><span data-stu-id="36b57-143">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-144">Conformes</span><span class="sxs-lookup"><span data-stu-id="36b57-144">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-145">Ne pas exempter</span><span class="sxs-lookup"><span data-stu-id="36b57-145">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-146">Votre ordinateur est conforme, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36b57-146">The computer is compliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-147">Aucune action n’est nécessaire; l’état de l’ordinateur peut être confirmé en consultant le rapport de conformité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36b57-147">No action needed; the state of the computer can be confirmed by viewing the Computer Compliance Report.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="36b57-148">Rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="36b57-148">Computer Compliance Report</span></span>

<span data-ttu-id="36b57-149">Utilisez ce type de rapport pour collecter des informations spécifiques à un ordinateur ou à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="36b57-149">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="36b57-150">Ce rapport peut être affiché en cliquant sur le nom de l’ordinateur dans le rapport de conformité d’entreprise, ou en tapant le nom de l’ordinateur dans le rapport de conformité informatique.</span><span class="sxs-lookup"><span data-stu-id="36b57-150">This report can be viewed by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="36b57-151">Le rapport de conformité informatique fournit des informations de chiffrement détaillées sur chaque lecteur (système d’exploitation et lecteurs de données fixes) sur un ordinateur, ainsi que les indications de la stratégie appliquée à chaque type de lecteur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36b57-151">The Computer Compliance Report provides detailed encryption information about each drive (operating system and fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="36b57-152">Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36b57-152">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="36b57-153">**Remarques**  L’état de chiffrement des volumes de données amovibles ne s’affiche pas dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="36b57-153">**Note** Removable Data Volume encryption status will not be shown in the report.</span></span>

 

**<span data-ttu-id="36b57-154">Champs du rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="36b57-154">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="36b57-155">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="36b57-155">Column Name</span></span></th>
<th align="left"><span data-ttu-id="36b57-156">Description</span><span class="sxs-lookup"><span data-stu-id="36b57-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-157">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="36b57-157">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-158">Nom d’ordinateur DNS spécifié par l’utilisateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="36b57-158">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-159">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="36b57-159">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-160">Nom de domaine complet, où se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="36b57-160">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-161">Type d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="36b57-161">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-162">Type d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36b57-162">Type of computer.</span></span> <span data-ttu-id="36b57-163">Les types valides ne sont pas portables et portables.</span><span class="sxs-lookup"><span data-stu-id="36b57-163">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-164">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="36b57-164">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-165">Type de système d’exploitation détecté sur l’ordinateur client géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="36b57-165">Operating system type found on the MBAM-managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-166">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="36b57-166">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-167">État de conformité global de l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="36b57-167">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="36b57-168">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="36b57-168">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="36b57-169">Notez que l’état de la conformité par lecteur (voir le tableau ci-dessous) est susceptible d’indiquer les différents États de conformité.</span><span class="sxs-lookup"><span data-stu-id="36b57-169">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="36b57-170">Toutefois, ce champ correspond à cet état de conformité, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36b57-170">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-171">Niveau de cryptage de la stratégie</span><span class="sxs-lookup"><span data-stu-id="36b57-171">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-172">Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM (par exemple, 128-bits avec diffuseur).</span><span class="sxs-lookup"><span data-stu-id="36b57-172">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-173">Lecteur du système d’exploitation de la stratégie</span><span class="sxs-lookup"><span data-stu-id="36b57-173">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-174">Indique si le chiffrement est requis pour le système d’exploitation et le type de protecteur approprié.</span><span class="sxs-lookup"><span data-stu-id="36b57-174">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-175">Politique-lecteur de données fixes</span><span class="sxs-lookup"><span data-stu-id="36b57-175">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-176">Indique si le chiffrement est requis pour le lecteur de données fixes.</span><span class="sxs-lookup"><span data-stu-id="36b57-176">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-177">Lecteur de données amovibles pour une stratégie</span><span class="sxs-lookup"><span data-stu-id="36b57-177">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-178">Indique si le chiffrement est requis pour le lecteur amovible.</span><span class="sxs-lookup"><span data-stu-id="36b57-178">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-179">Utilisateurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="36b57-179">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-180">Utilisateurs connus sur l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="36b57-180">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-181">Fabricant</span><span class="sxs-lookup"><span data-stu-id="36b57-181">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-182">Nom de fabricant de l’ordinateur, tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36b57-182">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-183">Modèle</span><span class="sxs-lookup"><span data-stu-id="36b57-183">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-184">Nom de modèle du fabricant d’ordinateurs, tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36b57-184">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-185">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="36b57-185">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-186">Messages d’erreur et d’état de l’état de conformité de l’ordinateur, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36b57-186">Error and status messages of the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-187">Dernier contact</span><span class="sxs-lookup"><span data-stu-id="36b57-187">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-188">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="36b57-188">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="36b57-189">La fréquence de contact est configurable (voir paramètres de la stratégie MBAM).</span><span class="sxs-lookup"><span data-stu-id="36b57-189">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="36b57-190">Champs du rapport de conformité informatique</span><span class="sxs-lookup"><span data-stu-id="36b57-190">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="36b57-191">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="36b57-191">Column Name</span></span></th>
<th align="left"><span data-ttu-id="36b57-192">Description</span><span class="sxs-lookup"><span data-stu-id="36b57-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-193">Lettre du lecteur</span><span class="sxs-lookup"><span data-stu-id="36b57-193">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-194">Lettre du lecteur de l’ordinateur qui a été affectée à l’utilisateur en particulier.</span><span class="sxs-lookup"><span data-stu-id="36b57-194">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-195">Type de lecteur</span><span class="sxs-lookup"><span data-stu-id="36b57-195">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-196">Type de lecteur.</span><span class="sxs-lookup"><span data-stu-id="36b57-196">Type of drive.</span></span> <span data-ttu-id="36b57-197">Les valeurs valides sont le lecteur du système d’exploitation et le lecteur de données fixes.</span><span class="sxs-lookup"><span data-stu-id="36b57-197">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="36b57-198">Il s’agit de disques physiques plutôt que de volumes logiques.</span><span class="sxs-lookup"><span data-stu-id="36b57-198">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-199">Niveau de cryptage</span><span class="sxs-lookup"><span data-stu-id="36b57-199">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-200">Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="36b57-200">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-201">Type de protecteur</span><span class="sxs-lookup"><span data-stu-id="36b57-201">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-202">Type de protecteur sélectionné par le biais de la stratégie utilisée pour chiffrer un système d’exploitation ou un volume de données fixe.</span><span class="sxs-lookup"><span data-stu-id="36b57-202">Type of protector selected via the policy used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-203">État de protecteur</span><span class="sxs-lookup"><span data-stu-id="36b57-203">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-204">Indique que l’ordinateur géré par MBAM a activé le type de protecteur qui est spécifié dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="36b57-204">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="36b57-205">Les États valides sont ACTIVÉs ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="36b57-205">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-206">État du chiffrement</span><span class="sxs-lookup"><span data-stu-id="36b57-206">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-207">État du chiffrement du lecteur.</span><span class="sxs-lookup"><span data-stu-id="36b57-207">Encryption state of the drive.</span></span> <span data-ttu-id="36b57-208">Les États valides sont chiffrés, non chiffrés et chiffrés.</span><span class="sxs-lookup"><span data-stu-id="36b57-208">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-209">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="36b57-209">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-210">État indiquant s’il est conforme à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="36b57-210">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="36b57-211">Les États ne sont pas conformes et conformes.</span><span class="sxs-lookup"><span data-stu-id="36b57-211">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-212">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="36b57-212">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-213">Messages d’erreur et de statut de l’état de conformité de l’ordinateur, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36b57-213">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="36b57-214">Rapport d’audit de récupération</span><span class="sxs-lookup"><span data-stu-id="36b57-214">Recovery Audit Report</span></span>

<span data-ttu-id="36b57-215">Utilisez ce type de rapport pour auditer les utilisateurs qui ont demandé l’accès aux clés de récupération.</span><span class="sxs-lookup"><span data-stu-id="36b57-215">Use this report type to audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="36b57-216">Le rapport propose plusieurs filtres basés sur les critères de filtre souhaités.</span><span class="sxs-lookup"><span data-stu-id="36b57-216">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="36b57-217">Les utilisateurs peuvent filtrer sur un type spécifique d’utilisateur, à savoir un utilisateur du support technique ou un utilisateur final, si la demande a échoué ou a abouti, le type spécifique de clé demandée et une plage de dates pendant laquelle la récupération s’est produite.</span><span class="sxs-lookup"><span data-stu-id="36b57-217">Users can filter on a specific type of user, either a Help Desk user or an end user, whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span> <span data-ttu-id="36b57-218">L’administrateur peut générer des rapports contextuels en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="36b57-218">The administrator can produce contextual reports based on need.</span></span>

**<span data-ttu-id="36b57-219">Champs du rapport d’audit de récupération</span><span class="sxs-lookup"><span data-stu-id="36b57-219">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="36b57-220">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="36b57-220">Column Name</span></span></th>
<th align="left"><span data-ttu-id="36b57-221">Description</span><span class="sxs-lookup"><span data-stu-id="36b57-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-222">Demander une date et une heure</span><span class="sxs-lookup"><span data-stu-id="36b57-222">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-223">Date et heure auxquelles une demande de récupération de clé a été effectuée par un utilisateur final ou un utilisateur du support technique.</span><span class="sxs-lookup"><span data-stu-id="36b57-223">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-224">État de la demande</span><span class="sxs-lookup"><span data-stu-id="36b57-224">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-225">État de la demande.</span><span class="sxs-lookup"><span data-stu-id="36b57-225">Status of the request.</span></span> <span data-ttu-id="36b57-226">Les statuts valides sont réussis (la clé a été récupérée) ou FAILED (la clé n’a pas été récupérée).</span><span class="sxs-lookup"><span data-stu-id="36b57-226">Valid statuses are either Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-227">Utilisateur du support technique</span><span class="sxs-lookup"><span data-stu-id="36b57-227">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-228">Utilisateur de l’assistance technique ayant lancé la demande de récupération de la clé.</span><span class="sxs-lookup"><span data-stu-id="36b57-228">Help Desk user that initiated the request for key retrieval.</span></span> <span data-ttu-id="36b57-229">Remarque: si l’utilisateur du support technique récupère la clé de la part d’un utilisateur final, le champ d’utilisateur final sera vide.</span><span class="sxs-lookup"><span data-stu-id="36b57-229">Note: If the Help Desk user retrieves the key on behalf on an end-user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-230">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="36b57-230">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-231">Utilisateur final à l’origine de la demande de récupération de la clé.</span><span class="sxs-lookup"><span data-stu-id="36b57-231">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36b57-232">Type de clé</span><span class="sxs-lookup"><span data-stu-id="36b57-232">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-233">Type de clé demandée par l’utilisateur du support technique ou par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="36b57-233">Type of key that was requested by either the Help Desk user or the end user.</span></span> <span data-ttu-id="36b57-234">Les trois types de clés que MBAM recueille sont: mot de passe de la clé de récupération (utilisé pour la récupération d’un ordinateur en mode récupération), ID de la clé de récupération (utilisé pour récupérer un ordinateur en mode de récupération pour le compte d’un autre utilisateur)</span><span class="sxs-lookup"><span data-stu-id="36b57-234">The three types of keys that MBAM collects are: Recovery Key Password (used to recovery a computer in recovery mode), Recovery Key ID (used to recover a computer in recovery mode on behalf of another user), and TPM Password Hash (used to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36b57-235">Description de raison</span><span class="sxs-lookup"><span data-stu-id="36b57-235">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="36b57-236">Raison le type de clé spécifié a été requis par l’utilisateur du support technique ou par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="36b57-236">Reason the specified Key Type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="36b57-237">Les raisons sont indiquées dans les fonctionnalités de récupération des lecteurs et de gestion du TPM du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="36b57-237">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring website.</span></span> <span data-ttu-id="36b57-238">Le texte entré par l’utilisateur est le texte entré par l’utilisateur ou l’un des codes de raison suivants:</span><span class="sxs-lookup"><span data-stu-id="36b57-238">The valid entries are either user-entered text, or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="36b57-239">Ordre d’amorçage du système d’exploitation modifié</span><span class="sxs-lookup"><span data-stu-id="36b57-239">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="36b57-240">Modification du BIOS</span><span class="sxs-lookup"><span data-stu-id="36b57-240">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="36b57-241">Modification des fichiers du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="36b57-241">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="36b57-242">Clé de démarrage perdue</span><span class="sxs-lookup"><span data-stu-id="36b57-242">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="36b57-243">Code confidentiel perdu</span><span class="sxs-lookup"><span data-stu-id="36b57-243">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="36b57-244">Réinitialisation du TPM</span><span class="sxs-lookup"><span data-stu-id="36b57-244">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="36b57-245">Phrase de passe perdue</span><span class="sxs-lookup"><span data-stu-id="36b57-245">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="36b57-246">Carte Smartcard perdue</span><span class="sxs-lookup"><span data-stu-id="36b57-246">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="36b57-247">Réinitialiser le verrouillage du code confidentiel</span><span class="sxs-lookup"><span data-stu-id="36b57-247">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="36b57-248">Activer le module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="36b57-248">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="36b57-249">Désactiver le module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="36b57-249">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="36b57-250">Changer le mot de passe du TPM</span><span class="sxs-lookup"><span data-stu-id="36b57-250">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="36b57-251">Vider le TPM</span><span class="sxs-lookup"><span data-stu-id="36b57-251">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="36b57-252">**Remarques**  Vous pouvez enregistrer des résultats de rapport dans un fichier en cliquant sur le bouton **Exporter** dans la barre de menus rapports.</span><span class="sxs-lookup"><span data-stu-id="36b57-252">**Note** Report results can be saved to a file by clicking the **Export** button on the reports menu bar.</span></span> <span data-ttu-id="36b57-253">Pour plus d’informations sur l’exécution des rapports MBAM, voir [génération de rapports MBAM](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="36b57-253">For more information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

 

## <span data-ttu-id="36b57-254">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36b57-254">Related topics</span></span>


[<span data-ttu-id="36b57-255">Surveillance et création de rapports de la conformité BitLocker avec MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="36b57-255">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 






---
title: Présentation des rapports MBAM dans Configuration Manager
description: Présentation des rapports MBAM dans Configuration Manager
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810187"
---
# <span data-ttu-id="c51f7-103">Présentation des rapports MBAM dans Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c51f7-103">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="c51f7-104">Lorsque Microsoft BitLocker administration et la surveillance (MBAM) sont installés avec la topologie intégrée de Configuration Manager, les fonctionnalités de compatibilité matérielle et de création de rapports sont déplacées vers l’infrastructure de Configuration Manager et hors MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-104">When Microsoft BitLocker Administration and Monitoring (MBAM) is installed with the Configuration Manager Integrated topology, the hardware compliance and reporting features are moved into the Configuration Manager infrastructure and out of MBAM.</span></span> <span data-ttu-id="c51f7-105">Lorsque vous utilisez la topologie Configuration Manager, vous exécutez des rapports à partir de Configuration Manager plutôt que de MBAM, à l’exception du rapport d’audit de récupération, auquel vous pouvez toujours accéder à l’aide du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="c51f7-105">When you use the Configuration Manager topology, you run reports from Configuration Manager rather than from MBAM, except for the Recovery Audit Report, which you continue to access by using the Administration and Monitoring Website.</span></span>

<span data-ttu-id="c51f7-106">Les rapports pour la topologie intégrée de Configuration Manager présentent la conformité BitLocker pour l’entreprise et pour les ordinateurs et appareils individuels gérés par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-106">The reports for the Configuration Manager Integrated topology show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="c51f7-107">Les rapports fournissent des informations tabulaires et des graphiques, et vous permettent de filtrer des États pour afficher les données de différentes perspectives.</span><span class="sxs-lookup"><span data-stu-id="c51f7-107">The reports provide both tabular information and charts, and enable you to filter reports to view data from different perspectives.</span></span>

<span data-ttu-id="c51f7-108">Les informations fournies dans cette rubrique décrivent les rapports MBAM que vous exécutez à partir de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c51f7-108">The information in this topic describes the MBAM reports that you run from Configuration Manager.</span></span> <span data-ttu-id="c51f7-109">Pour plus d’informations sur les rapports MBAM pour la topologie autonome, voir [Présentation des rapports MBAM](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="c51f7-109">For information about MBAM reports for the Stand-alone topology, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

## <span data-ttu-id="c51f7-110">Accès aux rapports dans Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c51f7-110">Accessing Reports in Configuration Manager</span></span>


<span data-ttu-id="c51f7-111">Pour accéder à la fonctionnalité rapports dans Configuration Manager, ouvrez la **console Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="c51f7-111">To access the Reports feature in Configuration Manager, open the **Configuration Manager console**.</span></span> <span data-ttu-id="c51f7-112">Pour afficher la liste des rapports disponibles:</span><span class="sxs-lookup"><span data-stu-id="c51f7-112">To display the list of available reports:</span></span>

-   <span data-ttu-id="c51f7-113">Dans Configuration Manager 2007, développez le nœud gestion de l' **ordinateur** , puis développez le nœud **création de rapports** .</span><span class="sxs-lookup"><span data-stu-id="c51f7-113">In Configuration Manager 2007, expand the **Computer Management** node, and then expand the **Reporting** node.</span></span>

-   <span data-ttu-id="c51f7-114">Dans SystemCenter2012 ConfigurationManager, dans l’espace de travail analyse sous **vue d’ensemble**, développez le nœud **rapports** , puis cliquez sur **rapports**.</span><span class="sxs-lookup"><span data-stu-id="c51f7-114">In SystemCenter2012 ConfigurationManager, in the Monitoring workspace under **Overview**, expand the **Reporting** node and then click **Reports**.</span></span>

### <span data-ttu-id="c51f7-115">Tableau de bord de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="c51f7-115">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="c51f7-116">Le tableau de bord de conformité de BitLocker Enterprise fournit les graphiques suivants, qui indiquent l’état de conformité de BitLocker au sein de l’entreprise:</span><span class="sxs-lookup"><span data-stu-id="c51f7-116">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="c51f7-117">Distribution de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="c51f7-117">Compliance Status Distribution</span></span>

-   <span data-ttu-id="c51f7-118">Distribution d’erreurs non conformes</span><span class="sxs-lookup"><span data-stu-id="c51f7-118">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="c51f7-119">Répartition de l’état de conformité par type de lecteur</span><span class="sxs-lookup"><span data-stu-id="c51f7-119">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="c51f7-120">Distribution de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="c51f7-120">Compliance Status Distribution</span></span>**

<span data-ttu-id="c51f7-121">Ce graphique en secteurs affiche le statut de conformité de l’ordinateur au sein de l’entreprise et indique le pourcentage d’ordinateurs par rapport au nombre total d’ordinateurs de la collection sélectionnée qui présentent l’état de conformité.</span><span class="sxs-lookup"><span data-stu-id="c51f7-121">This pie chart shows computer compliance statuses within the enterprise, and shows the percentage of computers, compared to the total number of computers in the selected collection, that have that compliance status.</span></span> <span data-ttu-id="c51f7-122">Le nombre réel d’ordinateurs avec chaque statut est également affiché.</span><span class="sxs-lookup"><span data-stu-id="c51f7-122">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="c51f7-123">Le graphique en secteurs présente les États de conformité suivants:</span><span class="sxs-lookup"><span data-stu-id="c51f7-123">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="c51f7-124">Conformes</span><span class="sxs-lookup"><span data-stu-id="c51f7-124">Compliant</span></span>

-   <span data-ttu-id="c51f7-125">Non conforme</span><span class="sxs-lookup"><span data-stu-id="c51f7-125">Non Compliant</span></span>

-   <span data-ttu-id="c51f7-126">Exonéré d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c51f7-126">User Exempt</span></span>

-   <span data-ttu-id="c51f7-127">Exemption d’utilisateur temporaire</span><span class="sxs-lookup"><span data-stu-id="c51f7-127">Temporary User Exempt</span></span>

-   <span data-ttu-id="c51f7-128">Stratégie non appliquée</span><span class="sxs-lookup"><span data-stu-id="c51f7-128">Policy Not Enforced</span></span>

-   <span data-ttu-id="c51f7-129">Inconnu: il s’agit d’ordinateurs dont l’État a été signalé comme une erreur ou ceux qui font partie de la collection, mais qui n’ont jamais signalé leur état de conformité, par exemple, s’ils sont déconnectés de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="c51f7-129">Unknown -computers whose status was reported as an error, or devices that are part of the collection but have never reported their compliance status, for example, if they are disconnected from the organization</span></span>

**<span data-ttu-id="c51f7-130">Distribution d’erreurs non conformes</span><span class="sxs-lookup"><span data-stu-id="c51f7-130">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="c51f7-131">Ce graphique en secteurs présente les catégories d’ordinateurs de l’entreprise qui ne sont pas conformes à la stratégie de chiffrement de lecteur BitLocker et indique le nombre d’ordinateurs dans chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="c51f7-131">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker drive encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="c51f7-132">Chaque pourcentage de catégorie est calculé à partir du nombre total d’ordinateurs non conformes de la collection.</span><span class="sxs-lookup"><span data-stu-id="c51f7-132">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="c51f7-133">Chiffrement différé par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c51f7-133">User postponed encryption</span></span>

-   <span data-ttu-id="c51f7-134">Impossible de trouver le TPM compatible</span><span class="sxs-lookup"><span data-stu-id="c51f7-134">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="c51f7-135">Partition système non disponible ou trop grande</span><span class="sxs-lookup"><span data-stu-id="c51f7-135">System Partition not available or large enough</span></span>

-   <span data-ttu-id="c51f7-136">Conflit de stratégie</span><span class="sxs-lookup"><span data-stu-id="c51f7-136">Policy conflict</span></span>

-   <span data-ttu-id="c51f7-137">En attente de la mise en service automatique du module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="c51f7-137">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="c51f7-138">Une erreur inconnue s’est produite</span><span class="sxs-lookup"><span data-stu-id="c51f7-138">An unknown error has occurred</span></span>

-   <span data-ttu-id="c51f7-139">Aucune information – les ordinateurs sur lesquels le client MBAM n’est pas installé, ou qui ont installé le client MBAM mais qui ne sont pas activés, par exemple, le service ne fonctionne pas</span><span class="sxs-lookup"><span data-stu-id="c51f7-139">No information – computers that do not have the MBAM Client installed, or that have the MBAM Client installed but not activated, for example, the service is not working</span></span>

**<span data-ttu-id="c51f7-140">Répartition de l’état de conformité par type de lecteur</span><span class="sxs-lookup"><span data-stu-id="c51f7-140">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="c51f7-141">Ce graphique à barres affiche l’état de compatibilité BitLocker actuel par type de lecteur.</span><span class="sxs-lookup"><span data-stu-id="c51f7-141">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="c51f7-142">Les statuts sont «conformes» et «non conformes».</span><span class="sxs-lookup"><span data-stu-id="c51f7-142">The statuses are “Compliant” and “Non Compliant.”</span></span> <span data-ttu-id="c51f7-143">Des barres sont affichées pour les lecteurs de données fixes et les lecteurs de systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c51f7-143">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="c51f7-144">Les ordinateurs qui n’ont pas de lecteur de données fixe ne sont inclus et n’affichent aucune valeur dans la barre du lecteur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c51f7-144">Computers that do not have a fixed data drive are included and show a value only in the Operating System Drive bar.</span></span> <span data-ttu-id="c51f7-145">Le graphique n’inclut pas les utilisateurs qui ont reçu une exemption de la stratégie de chiffrement de lecteur BitLocker ou de la catégorie «aucune stratégie».</span><span class="sxs-lookup"><span data-stu-id="c51f7-145">The chart does not include users who have been granted an exemption from the BitLocker drive encryption policy or the “No Policy” category.</span></span>

### <span data-ttu-id="c51f7-146">Rapport Détails de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="c51f7-146">BitLocker Enterprise Compliance Details Report</span></span>

<span data-ttu-id="c51f7-147">Ce rapport affiche des informations sur la conformité de BitLocker globale dans votre entreprise pour la collection d’ordinateurs ciblés pour l’utilisation de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-147">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="c51f7-148">Champs du rapport Détails de conformité BitLocker entreprise</span><span class="sxs-lookup"><span data-stu-id="c51f7-148">BitLocker Enterprise Compliance Details Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c51f7-149">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c51f7-149">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c51f7-150">Description</span><span class="sxs-lookup"><span data-stu-id="c51f7-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-151">Ordinateurs gérés</span><span class="sxs-lookup"><span data-stu-id="c51f7-151">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-152">Nombre d’ordinateurs gérés par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-152">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-153">Compatibilité%</span><span class="sxs-lookup"><span data-stu-id="c51f7-153">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-154">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c51f7-154">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-155">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="c51f7-155">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-156">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c51f7-156">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-157">% De conformité inconnue</span><span class="sxs-lookup"><span data-stu-id="c51f7-157">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-158">Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="c51f7-158">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-159">Pourcentage d’exonération</span><span class="sxs-lookup"><span data-stu-id="c51f7-159">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-160">Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-160">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-161">% Non exempté</span><span class="sxs-lookup"><span data-stu-id="c51f7-161">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-162">Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-162">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-163">Conformes</span><span class="sxs-lookup"><span data-stu-id="c51f7-163">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-164">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c51f7-164">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-165">Non conforme</span><span class="sxs-lookup"><span data-stu-id="c51f7-165">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-166">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c51f7-166">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-167">Conformité inconnue</span><span class="sxs-lookup"><span data-stu-id="c51f7-167">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-168">Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="c51f7-168">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-169">SIRET</span><span class="sxs-lookup"><span data-stu-id="c51f7-169">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-170">Nombre total d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-170">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-171">Non exempté</span><span class="sxs-lookup"><span data-stu-id="c51f7-171">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-172">Nombre total d’ordinateurs qui ne sont pas exemptés de l’exigence de chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-172">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c51f7-173">Rapport des détails de conformité de BitLocker pour les entreprises-États de conformité</span><span class="sxs-lookup"><span data-stu-id="c51f7-173">BitLocker Enterprise Compliance Details Report - Compliance States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c51f7-174">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="c51f7-174">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="c51f7-175">Question</span><span class="sxs-lookup"><span data-stu-id="c51f7-175">Exemption</span></span></th>
<th align="left"><span data-ttu-id="c51f7-176">Description</span><span class="sxs-lookup"><span data-stu-id="c51f7-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-177">Non conforme</span><span class="sxs-lookup"><span data-stu-id="c51f7-177">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-178">Ne pas exempter</span><span class="sxs-lookup"><span data-stu-id="c51f7-178">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-179">L’ordinateur n’est pas conforme, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c51f7-179">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-180">Conformes</span><span class="sxs-lookup"><span data-stu-id="c51f7-180">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-181">Ne pas exempter</span><span class="sxs-lookup"><span data-stu-id="c51f7-181">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-182">L’ordinateur est conforme conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c51f7-182">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c51f7-183">Rapport synthèse de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="c51f7-183">BitLocker Enterprise Compliance Summary Report</span></span>

<span data-ttu-id="c51f7-184">Utilisez ce type de rapport pour afficher les informations relatives à la conformité de BitLocker globale dans votre entreprise et pour montrer la conformité d’ordinateurs individuels qui se trouvent dans la collection d’ordinateurs ciblés pour l’utilisation de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-184">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="c51f7-185">Champs du rapport de synthèse de conformité BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="c51f7-185">BitLocker Enterprise Compliance Summary Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c51f7-186">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c51f7-186">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c51f7-187">Description</span><span class="sxs-lookup"><span data-stu-id="c51f7-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-188">Ordinateurs gérés</span><span class="sxs-lookup"><span data-stu-id="c51f7-188">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-189">Nombre d’ordinateurs gérés par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-189">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-190">Compatibilité%</span><span class="sxs-lookup"><span data-stu-id="c51f7-190">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-191">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c51f7-191">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-192">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="c51f7-192">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-193">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c51f7-193">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-194">% De conformité inconnue</span><span class="sxs-lookup"><span data-stu-id="c51f7-194">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-195">Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="c51f7-195">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-196">Pourcentage d’exonération</span><span class="sxs-lookup"><span data-stu-id="c51f7-196">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-197">Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-197">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-198">% Non exempté</span><span class="sxs-lookup"><span data-stu-id="c51f7-198">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-199">Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-199">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-200">Conformes</span><span class="sxs-lookup"><span data-stu-id="c51f7-200">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-201">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c51f7-201">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-202">Non conforme</span><span class="sxs-lookup"><span data-stu-id="c51f7-202">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-203">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c51f7-203">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-204">Conformité inconnue</span><span class="sxs-lookup"><span data-stu-id="c51f7-204">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-205">Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="c51f7-205">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-206">SIRET</span><span class="sxs-lookup"><span data-stu-id="c51f7-206">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-207">Nombre total d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-207">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-208">Non exempté</span><span class="sxs-lookup"><span data-stu-id="c51f7-208">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-209">Nombre total d’ordinateurs qui ne sont pas exemptés de l’exigence de chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-209">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c51f7-210">Rapport de synthèse de conformité de BitLocker Enterprise-détails sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="c51f7-210">BitLocker Enterprise Compliance Summary Report - Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c51f7-211">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c51f7-211">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c51f7-212">Description</span><span class="sxs-lookup"><span data-stu-id="c51f7-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-213">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c51f7-213">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-214">Nom d’ordinateur DNS spécifié par l’utilisateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-214">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-215">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="c51f7-215">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-216">Nom de domaine complet, où se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-216">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-217">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="c51f7-217">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-218">État de conformité global de l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-218">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="c51f7-219">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="c51f7-219">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="c51f7-220">Notez que l’état de conformité par lecteur (voir le tableau ci-dessous) risque d’indiquer des États de conformité différents.</span><span class="sxs-lookup"><span data-stu-id="c51f7-220">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="c51f7-221">Toutefois, ce champ correspond à cet état de conformité, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c51f7-221">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-222">Question</span><span class="sxs-lookup"><span data-stu-id="c51f7-222">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-223">État qui indique si l’utilisateur est exempté ou non exempt de la stratégie BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-223">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-224">Utilisateurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="c51f7-224">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-225">Utilisateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c51f7-225">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-226">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="c51f7-226">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-227">Messages d’erreur et d’état de l’état de conformité de l’ordinateur conformément à la politique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c51f7-227">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-228">Dernier contact</span><span class="sxs-lookup"><span data-stu-id="c51f7-228">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-229">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="c51f7-229">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="c51f7-230">La fréquence de contact est configurable (voir paramètres de la stratégie MBAM).</span><span class="sxs-lookup"><span data-stu-id="c51f7-230">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c51f7-231">Rapport de conformité de l’ordinateur BitLocker</span><span class="sxs-lookup"><span data-stu-id="c51f7-231">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="c51f7-232">Utilisez ce type de rapport pour collecter des informations spécifiques à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c51f7-232">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="c51f7-233">Le rapport de conformité informatique fournit des informations de chiffrement détaillées sur chaque lecteur (système d’exploitation et lecteurs de données fixes) sur un ordinateur, ainsi que les indications de la stratégie appliquée à chaque type de lecteur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c51f7-233">The Computer Compliance Report provides detailed encryption information about each drive (Operating System and Fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="c51f7-234">Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c51f7-234">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="c51f7-235">**Remarques**  L’état du chiffrement du volume de données amovibles ne s’affiche pas dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="c51f7-235">**Note** Removable Data Volume encryption status is not shown in the report.</span></span>

 

**<span data-ttu-id="c51f7-236">Rapport de conformité de l’ordinateur BitLocker – champs détails de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c51f7-236">BitLocker Computer Compliance Report – Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c51f7-237">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c51f7-237">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c51f7-238">Description</span><span class="sxs-lookup"><span data-stu-id="c51f7-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-239">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c51f7-239">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-240">Nom d’ordinateur DNS spécifié par l’utilisateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-240">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-241">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="c51f7-241">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-242">Nom de domaine complet, où se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-242">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-243">Type d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c51f7-243">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-244">Type d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c51f7-244">Type of computer.</span></span> <span data-ttu-id="c51f7-245">Les types valides ne sont pas portables et portables.</span><span class="sxs-lookup"><span data-stu-id="c51f7-245">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-246">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="c51f7-246">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-247">Type de système d’exploitation détecté sur l’ordinateur client géré MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-247">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-248">Conformité globale</span><span class="sxs-lookup"><span data-stu-id="c51f7-248">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-249">État de conformité global de l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-249">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="c51f7-250">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="c51f7-250">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="c51f7-251">Notez que l’état de conformité par lecteur (voir le tableau ci-dessous) risque d’indiquer des États de conformité différents.</span><span class="sxs-lookup"><span data-stu-id="c51f7-251">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="c51f7-252">Toutefois, ce champ correspond à cet état de conformité, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c51f7-252">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-253">Compatibilité du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="c51f7-253">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-254">État de conformité du système d’exploitation géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-254">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="c51f7-255">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="c51f7-255">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-256">Compatibilité des lecteurs de données fixes</span><span class="sxs-lookup"><span data-stu-id="c51f7-256">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-257">État de la conformité du lecteur de données fixes géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-257">Compliance status of the Fixed Data Drive that is managed by MBAM.</span></span> <span data-ttu-id="c51f7-258">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="c51f7-258">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-259">Date de la dernière mise à jour</span><span class="sxs-lookup"><span data-stu-id="c51f7-259">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-260">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="c51f7-260">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="c51f7-261">La fréquence de contact est configurable (voir paramètres de la stratégie MBAM).</span><span class="sxs-lookup"><span data-stu-id="c51f7-261">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-262">Question</span><span class="sxs-lookup"><span data-stu-id="c51f7-262">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-263">État qui indique si l’utilisateur est exempté ou non exempt de la stratégie BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-263">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-264">Utilisateur exempté</span><span class="sxs-lookup"><span data-stu-id="c51f7-264">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-265">Utilisateur exempt de la stratégie BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c51f7-265">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-266">Date d’exemption</span><span class="sxs-lookup"><span data-stu-id="c51f7-266">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-267">Date à laquelle l’exemption a été accordée.</span><span class="sxs-lookup"><span data-stu-id="c51f7-267">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-268">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="c51f7-268">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-269">Messages d’erreur et d’état de l’état de conformité de l’ordinateur conformément à la politique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c51f7-269">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-270">Niveau de cryptage de la stratégie</span><span class="sxs-lookup"><span data-stu-id="c51f7-270">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-271">Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-271">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="c51f7-272">(par exemple, 128-bit avec diffuseur).</span><span class="sxs-lookup"><span data-stu-id="c51f7-272">(for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-273">Stratégie: lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="c51f7-273">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-274">Indique si le chiffrement est requis pour les e/S et le type de protecteur approprié.</span><span class="sxs-lookup"><span data-stu-id="c51f7-274">Indicates if encryption is required for the O/S and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-275">Stratégie: disque de données fixe</span><span class="sxs-lookup"><span data-stu-id="c51f7-275">Policy:Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-276">Indique si le chiffrement est requis pour le lecteur fixe.</span><span class="sxs-lookup"><span data-stu-id="c51f7-276">Indicates if encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-277">Fabricant</span><span class="sxs-lookup"><span data-stu-id="c51f7-277">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-278">Nom de fabricant de l’ordinateur tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c51f7-278">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-279">Modèle</span><span class="sxs-lookup"><span data-stu-id="c51f7-279">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-280">Nom de modèle du fabricant d’ordinateurs tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c51f7-280">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-281">Utilisateurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="c51f7-281">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-282">Utilisateurs connus sur l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-282">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c51f7-283">Rapport de conformité de l’ordinateur BitLocker – champs volume de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c51f7-283">BitLocker Computer Compliance Report – Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c51f7-284">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="c51f7-284">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c51f7-285">Description</span><span class="sxs-lookup"><span data-stu-id="c51f7-285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-286">Lettre du lecteur</span><span class="sxs-lookup"><span data-stu-id="c51f7-286">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-287">Lettre du lecteur de l’ordinateur qui a été affectée à l’utilisateur en particulier.</span><span class="sxs-lookup"><span data-stu-id="c51f7-287">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-288">Type de lecteur</span><span class="sxs-lookup"><span data-stu-id="c51f7-288">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-289">Type de lecteur.</span><span class="sxs-lookup"><span data-stu-id="c51f7-289">Type of drive.</span></span> <span data-ttu-id="c51f7-290">Les valeurs valides sont le lecteur du système d’exploitation et le lecteur de données fixes.</span><span class="sxs-lookup"><span data-stu-id="c51f7-290">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="c51f7-291">Il s’agit de disques physiques plutôt que de volumes logiques.</span><span class="sxs-lookup"><span data-stu-id="c51f7-291">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-292">Niveau de cryptage</span><span class="sxs-lookup"><span data-stu-id="c51f7-292">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-293">Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="c51f7-293">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-294">Types de protecteur</span><span class="sxs-lookup"><span data-stu-id="c51f7-294">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-295">Type de protecteur sélectionné via une stratégie utilisée pour chiffrer un système d’exploitation ou un volume fixe.</span><span class="sxs-lookup"><span data-stu-id="c51f7-295">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="c51f7-296">Les types de protecteur valides sur un système d’exploitation sont TPM ou TPM + NIP et un volume de données fixe est Password.</span><span class="sxs-lookup"><span data-stu-id="c51f7-296">The valid protector types on an operating system are TPM or TPM+PIN and for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51f7-297">État de protecteur</span><span class="sxs-lookup"><span data-stu-id="c51f7-297">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-298">Indique que l’ordinateur géré par MBAM a activé le type de protecteur spécifié dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c51f7-298">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="c51f7-299">Les États valides sont ACTIVÉs ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="c51f7-299">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51f7-300">État du chiffrement</span><span class="sxs-lookup"><span data-stu-id="c51f7-300">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51f7-301">État du chiffrement du lecteur.</span><span class="sxs-lookup"><span data-stu-id="c51f7-301">Encryption state of the drive.</span></span> <span data-ttu-id="c51f7-302">Les États valides sont chiffrés, non chiffrés et chiffrés.</span><span class="sxs-lookup"><span data-stu-id="c51f7-302">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c51f7-303">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c51f7-303">Related topics</span></span>


[<span data-ttu-id="c51f7-304">Utilisation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c51f7-304">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 






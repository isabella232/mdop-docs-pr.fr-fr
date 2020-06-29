---
title: Affichage de rapports MBAM2.5 pour la topologie Intégration Configuration Manager
description: Affichage de rapports MBAM2.5 pour la topologie Intégration Configuration Manager
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810319"
---
# <span data-ttu-id="f26a0-103">Affichage de rapports MBAM2.5 pour la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f26a0-103">Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="f26a0-104">Cette rubrique décrit les rapports disponibles lorsque vous configurez l’administration et la surveillance de Microsoft BitLocker (MBAM) avec la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f26a0-104">This topic describes the reports that are available when you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="f26a0-105">Les rapports indiquent la conformité de BitLocker pour l’entreprise et pour les ordinateurs et appareils individuels gérés par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-105">The reports show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="f26a0-106">Les rapports fournissent des informations tabulaires et des graphiques et disposent de filtres qui vous permettent d’afficher des données de différentes perspectives.</span><span class="sxs-lookup"><span data-stu-id="f26a0-106">The reports provide tabular information and charts, and they have filters that let you view data from different perspectives.</span></span>

<span data-ttu-id="f26a0-107">Dans la topologie d’intégration de Configuration Manager, vous affichez des rapports à partir de Configuration Manager plutôt qu’à partir du site Web Administration et analyse, à l’exception du **rapport d’audit de récupération**, que vous continuez à consulter à partir du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="f26a0-107">In the Configuration Manager Integration topology, you view reports from Configuration Manager rather than from the Administration and Monitoring Website, with the exception of the **Recovery Audit Report**, which you continue to view from the Administration and Monitoring Website.</span></span>

<span data-ttu-id="f26a0-108">Pour plus d’informations sur les rapports MBAM pour la topologie autonome, voir [affichage de MBAM rapports 2,5 pour la topologie autonome](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="f26a0-108">For information about MBAM reports for the Stand-alone topology, see [Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span></span>

## <span data-ttu-id="f26a0-109">Accès aux rapports dans Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f26a0-109">Accessing reports in Configuration Manager</span></span>


<span data-ttu-id="f26a0-110">Pour accéder à la fonctionnalité rapports dans Configuration Manager, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="f26a0-110">To access the Reports feature in Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f26a0-111">Version de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f26a0-111">Version of Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="f26a0-112">Afficher les rapports</span><span class="sxs-lookup"><span data-stu-id="f26a0-112">How to view the reports</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-113">SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="f26a0-113">SystemCenter2012 ConfigurationManager</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="f26a0-114">Dans le volet gauche, sélectionnez l' <strong> </strong> espace de travail analyse.</span><span class="sxs-lookup"><span data-stu-id="f26a0-114">In the left pane, select the <strong>Monitoring</strong> workspace.</span></span></p></li>
<li><p><span data-ttu-id="f26a0-115">Dans l’arborescence, développez <strong> vue d’ensemble des </strong> &gt; <strong> rapports de rapport </strong> &gt; <strong> </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="f26a0-115">In the tree, expand <strong>Overview</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reports</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f26a0-116">Sélectionnez le dossier qui représente la langue dans laquelle vous souhaitez afficher les rapports, puis sélectionnez le rapport dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="f26a0-116">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-117">Gestionnaire de configuration 2007</span><span class="sxs-lookup"><span data-stu-id="f26a0-117">Configuration Manager 2007</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="f26a0-118">Dans le volet gauche, développez Gestion de l’ordinateur création de rapports <strong> </strong> &gt; <strong> </strong> &gt; <strong> Reporting Services Reporting Services </strong> &gt; <strong> &lt; &gt; </strong> &gt; <strong> </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="f26a0-118">In the left pane, expand <strong>Computer Management</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reporting Services</strong> &gt; <strong>&lt;server name&gt;</strong> &gt; <strong>Report folders</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f26a0-119">Sélectionnez le dossier qui représente la langue dans laquelle vous souhaitez afficher les rapports, puis sélectionnez le rapport dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="f26a0-119">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f26a0-120">Description des rapports dans Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f26a0-120">Description of reports in Configuration Manager</span></span>


<span data-ttu-id="f26a0-121">Il existe quelques différences mineures dans les rapports pour la topologie d’intégration de Configuration Manager et la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="f26a0-121">There are a few minor differences in the reports for the Configuration Manager Integration topology and the Stand-alone topology.</span></span> <span data-ttu-id="f26a0-122">Les sections suivantes décrivent les données dans les rapports MBAM pour la topologie d’intégration de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="f26a0-122">The following sections describe the data in the MBAM reports for the Configuration Manager Integration topology:</span></span>

-   [<span data-ttu-id="f26a0-123">Tableau de bord de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f26a0-123">BitLocker Enterprise Compliance Dashboard</span></span>](#bkmk-dashboard)

-   [<span data-ttu-id="f26a0-124">Détails de la conformité à l’entreprise BitLocker</span><span class="sxs-lookup"><span data-stu-id="f26a0-124">BitLocker Enterprise Compliance Details</span></span>](#bkmk-compliancedetails)

-   [<span data-ttu-id="f26a0-125">Résumé de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f26a0-125">BitLocker Enterprise Compliance Summary</span></span>](#bkmk-compliancesummary)

-   [<span data-ttu-id="f26a0-126">Rapport de conformité de l’ordinateur BitLocker</span><span class="sxs-lookup"><span data-stu-id="f26a0-126">BitLocker Computer Compliance Report</span></span>](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a><span data-ttu-id="f26a0-127">Tableau de bord de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f26a0-127">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="f26a0-128">Le tableau de bord de conformité de BitLocker Enterprise fournit les graphiques suivants, qui indiquent l’état de conformité de BitLocker au sein de l’entreprise:</span><span class="sxs-lookup"><span data-stu-id="f26a0-128">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="f26a0-129">Distribution de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="f26a0-129">Compliance Status Distribution</span></span>

-   <span data-ttu-id="f26a0-130">Distribution d’erreurs non conformes</span><span class="sxs-lookup"><span data-stu-id="f26a0-130">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="f26a0-131">Répartition de l’état de conformité par type de lecteur</span><span class="sxs-lookup"><span data-stu-id="f26a0-131">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="f26a0-132">Distribution de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="f26a0-132">Compliance Status Distribution</span></span>**

<span data-ttu-id="f26a0-133">Ce graphique en secteurs montre l’état de la conformité pour les ordinateurs au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f26a0-133">This pie chart shows compliance status for computers within the enterprise.</span></span> <span data-ttu-id="f26a0-134">Il indique également le pourcentage d’ordinateurs par rapport au nombre total d’ordinateurs de la collection sélectionnée dont l’état de conformité est défini.</span><span class="sxs-lookup"><span data-stu-id="f26a0-134">It also shows the percentage of computers, compared to the total number of computers in the selected collection, that has that compliance status.</span></span> <span data-ttu-id="f26a0-135">Le nombre réel d’ordinateurs avec chaque statut est également affiché.</span><span class="sxs-lookup"><span data-stu-id="f26a0-135">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="f26a0-136">Le graphique en secteurs présente les États de conformité suivants:</span><span class="sxs-lookup"><span data-stu-id="f26a0-136">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="f26a0-137">Conformes</span><span class="sxs-lookup"><span data-stu-id="f26a0-137">Compliant</span></span>

-   <span data-ttu-id="f26a0-138">Non conforme</span><span class="sxs-lookup"><span data-stu-id="f26a0-138">Non Compliant</span></span>

-   <span data-ttu-id="f26a0-139">Exonéré d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f26a0-139">User Exempt</span></span>

-   <span data-ttu-id="f26a0-140">Exemption d’utilisateur temporaire</span><span class="sxs-lookup"><span data-stu-id="f26a0-140">Temporary User Exempt</span></span>

-   <span data-ttu-id="f26a0-141">Stratégie non appliquée</span><span class="sxs-lookup"><span data-stu-id="f26a0-141">Policy Not Enforced</span></span>

-   <span data-ttu-id="f26a0-142">Encore.</span><span class="sxs-lookup"><span data-stu-id="f26a0-142">Unknown.</span></span> <span data-ttu-id="f26a0-143">Ces ordinateurs ont signalé une erreur de statut ou font partie de la collection, mais n’ont jamais signalé leur état de conformité.</span><span class="sxs-lookup"><span data-stu-id="f26a0-143">These computers reported a status error, or they are part of the collection, but have never reported their compliance status.</span></span> <span data-ttu-id="f26a0-144">L’absence de statut de conformité peut se produire si l’ordinateur est déconnecté de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f26a0-144">The lack of a compliance status could occur if the computer is disconnected from the organization.</span></span>

**<span data-ttu-id="f26a0-145">Distribution d’erreurs non conformes</span><span class="sxs-lookup"><span data-stu-id="f26a0-145">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="f26a0-146">Ce graphique en secteurs présente les catégories d’ordinateurs de l’entreprise qui ne sont pas conformes à la stratégie de chiffrement de lecteur BitLocker et indique le nombre d’ordinateurs dans chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="f26a0-146">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker Drive Encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="f26a0-147">Chaque pourcentage de catégorie est calculé à partir du nombre total d’ordinateurs non conformes de la collection.</span><span class="sxs-lookup"><span data-stu-id="f26a0-147">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="f26a0-148">Chiffrement différé par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f26a0-148">User postponed encryption</span></span>

-   <span data-ttu-id="f26a0-149">Impossible de trouver le TPM compatible</span><span class="sxs-lookup"><span data-stu-id="f26a0-149">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="f26a0-150">Partition système non disponible ou trop grande</span><span class="sxs-lookup"><span data-stu-id="f26a0-150">System partition not available or large enough</span></span>

-   <span data-ttu-id="f26a0-151">Conflit de stratégie</span><span class="sxs-lookup"><span data-stu-id="f26a0-151">Policy conflict</span></span>

-   <span data-ttu-id="f26a0-152">En attente de la mise en service automatique du module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="f26a0-152">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="f26a0-153">Une erreur inconnue s’est produite</span><span class="sxs-lookup"><span data-stu-id="f26a0-153">An unknown error has occurred</span></span>

-   <span data-ttu-id="f26a0-154">Aucune information.</span><span class="sxs-lookup"><span data-stu-id="f26a0-154">No information.</span></span> <span data-ttu-id="f26a0-155">Sur ces ordinateurs, le client MBAM n’est pas installé ou le client MBAM est installé, mais n’est pas activé (par exemple, le service ne fonctionne pas).</span><span class="sxs-lookup"><span data-stu-id="f26a0-155">These computers do not have the MBAM Client installed, or they have the MBAM Client installed but not activated (for example, the service is not working).</span></span>

**<span data-ttu-id="f26a0-156">Répartition de l’état de conformité par type de lecteur</span><span class="sxs-lookup"><span data-stu-id="f26a0-156">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="f26a0-157">Ce graphique à barres affiche l’état de compatibilité BitLocker actuel par type de lecteur.</span><span class="sxs-lookup"><span data-stu-id="f26a0-157">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="f26a0-158">Les statuts sont **conformes** et **non conformes**.</span><span class="sxs-lookup"><span data-stu-id="f26a0-158">The statuses are **Compliant** and **Non Compliant**.</span></span> <span data-ttu-id="f26a0-159">Des barres sont affichées pour les lecteurs de données fixes et les lecteurs de systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f26a0-159">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="f26a0-160">Les ordinateurs qui n’ont pas de lecteur de données fixe ne sont inclus et n’affichent aucune valeur dans la barre du **lecteur du système d’exploitation** .</span><span class="sxs-lookup"><span data-stu-id="f26a0-160">Computers that do not have a fixed data drive are included and show a value only in the **Operating System Drive** bar.</span></span> <span data-ttu-id="f26a0-161">Le graphique n’inclut pas les utilisateurs qui ont reçu une exemption de la stratégie de chiffrement de lecteur BitLocker ou de la catégorie aucune stratégie.</span><span class="sxs-lookup"><span data-stu-id="f26a0-161">The chart does not include users who have been granted an exemption from the BitLocker Drive Encryption policy or the No Policy category.</span></span>

### <a href="" id="bkmk-compliancedetails"></a><span data-ttu-id="f26a0-162">Détails de la conformité à l’entreprise BitLocker</span><span class="sxs-lookup"><span data-stu-id="f26a0-162">BitLocker Enterprise Compliance Details</span></span>

<span data-ttu-id="f26a0-163">Ce rapport affiche des informations sur la conformité de BitLocker globale dans votre entreprise pour la collection d’ordinateurs ciblés pour l’utilisation de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-163">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="f26a0-164">Champs détails de la conformité d’entreprise BitLocker</span><span class="sxs-lookup"><span data-stu-id="f26a0-164">BitLocker Enterprise Compliance Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f26a0-165">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="f26a0-165">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f26a0-166">Description</span><span class="sxs-lookup"><span data-stu-id="f26a0-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-167">Ordinateurs gérés</span><span class="sxs-lookup"><span data-stu-id="f26a0-167">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-168">Nombre d’ordinateurs gérés par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-168">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-169">Compatibilité%</span><span class="sxs-lookup"><span data-stu-id="f26a0-169">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-170">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f26a0-170">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-171">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="f26a0-171">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-172">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f26a0-172">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-173">% De conformité inconnue</span><span class="sxs-lookup"><span data-stu-id="f26a0-173">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-174">Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="f26a0-174">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-175">Pourcentage d’exonération</span><span class="sxs-lookup"><span data-stu-id="f26a0-175">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-176">Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-176">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-177">% Non exempté</span><span class="sxs-lookup"><span data-stu-id="f26a0-177">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-178">Pourcentage d’ordinateurs non exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-178">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-179">Conformes</span><span class="sxs-lookup"><span data-stu-id="f26a0-179">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-180">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f26a0-180">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-181">Non conforme</span><span class="sxs-lookup"><span data-stu-id="f26a0-181">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-182">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f26a0-182">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-183">Conformité inconnue</span><span class="sxs-lookup"><span data-stu-id="f26a0-183">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-184">Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="f26a0-184">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-185">SIRET</span><span class="sxs-lookup"><span data-stu-id="f26a0-185">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-186">Nombre total d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-186">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-187">Non exempté</span><span class="sxs-lookup"><span data-stu-id="f26a0-187">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-188">Nombre total d’ordinateurs qui ne sont pas exemptés de l’exigence de chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-188">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f26a0-189">États des détails de la conformité d’entreprise BitLocker</span><span class="sxs-lookup"><span data-stu-id="f26a0-189">BitLocker Enterprise Compliance Details States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f26a0-190">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="f26a0-190">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="f26a0-191">Question</span><span class="sxs-lookup"><span data-stu-id="f26a0-191">Exemption</span></span></th>
<th align="left"><span data-ttu-id="f26a0-192">Description</span><span class="sxs-lookup"><span data-stu-id="f26a0-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-193">Non conforme</span><span class="sxs-lookup"><span data-stu-id="f26a0-193">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-194">Ne pas exempter</span><span class="sxs-lookup"><span data-stu-id="f26a0-194">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-195">L’ordinateur n’est pas conforme, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f26a0-195">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-196">Conformes</span><span class="sxs-lookup"><span data-stu-id="f26a0-196">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-197">Ne pas exempter</span><span class="sxs-lookup"><span data-stu-id="f26a0-197">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-198">L’ordinateur est conforme conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f26a0-198">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a><span data-ttu-id="f26a0-199">Résumé de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f26a0-199">BitLocker Enterprise Compliance Summary</span></span>

<span data-ttu-id="f26a0-200">Utilisez ce type de rapport pour afficher les informations relatives à la conformité de BitLocker globale dans votre entreprise et pour montrer la conformité d’ordinateurs individuels qui se trouvent dans la collection d’ordinateurs ciblés pour l’utilisation de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-200">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="f26a0-201">Champs de synthèse de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f26a0-201">BitLocker Enterprise Compliance Summary Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f26a0-202">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="f26a0-202">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f26a0-203">Description</span><span class="sxs-lookup"><span data-stu-id="f26a0-203">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-204">Ordinateurs gérés</span><span class="sxs-lookup"><span data-stu-id="f26a0-204">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-205">Nombre d’ordinateurs gérés par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-205">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-206">Compatibilité%</span><span class="sxs-lookup"><span data-stu-id="f26a0-206">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-207">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f26a0-207">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-208">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="f26a0-208">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-209">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f26a0-209">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-210">% De conformité inconnue</span><span class="sxs-lookup"><span data-stu-id="f26a0-210">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-211">Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="f26a0-211">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-212">Pourcentage d’exonération</span><span class="sxs-lookup"><span data-stu-id="f26a0-212">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-213">Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-213">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-214">% Non exempté</span><span class="sxs-lookup"><span data-stu-id="f26a0-214">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-215">Pourcentage d’ordinateurs non exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-215">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-216">Conformes</span><span class="sxs-lookup"><span data-stu-id="f26a0-216">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-217">Pourcentage d’ordinateurs conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f26a0-217">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-218">Non conforme</span><span class="sxs-lookup"><span data-stu-id="f26a0-218">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-219">Pourcentage d’ordinateurs non conformes dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f26a0-219">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-220">Conformité inconnue</span><span class="sxs-lookup"><span data-stu-id="f26a0-220">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-221">Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="f26a0-221">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-222">SIRET</span><span class="sxs-lookup"><span data-stu-id="f26a0-222">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-223">Nombre total d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-223">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-224">Non exempté</span><span class="sxs-lookup"><span data-stu-id="f26a0-224">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-225">Nombre total d’ordinateurs qui ne sont pas exemptés de l’exigence de chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-225">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f26a0-226">Détails de l’ordinateur de synthèse de BitLocker Enterprise Compliance</span><span class="sxs-lookup"><span data-stu-id="f26a0-226">BitLocker Enterprise Compliance Summary Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f26a0-227">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="f26a0-227">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f26a0-228">Description</span><span class="sxs-lookup"><span data-stu-id="f26a0-228">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-229">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="f26a0-229">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-230">Nom d’ordinateur DNS spécifié par l’utilisateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-230">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-231">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="f26a0-231">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-232">Nom de domaine complet, où se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-232">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-233">État de la conformité</span><span class="sxs-lookup"><span data-stu-id="f26a0-233">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-234">État de conformité global de l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-234">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="f26a0-235">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="f26a0-235">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="f26a0-236">Notez que l’état de conformité par lecteur (voir le tableau ci-dessous) risque d’indiquer des États de conformité différents.</span><span class="sxs-lookup"><span data-stu-id="f26a0-236">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="f26a0-237">Toutefois, ce champ correspond à cet état de conformité, conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f26a0-237">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-238">Question</span><span class="sxs-lookup"><span data-stu-id="f26a0-238">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-239">État qui indique si l’utilisateur est exempté ou non exempt de la stratégie BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-239">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-240">Utilisateurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="f26a0-240">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-241">Utilisateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f26a0-241">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-242">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="f26a0-242">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-243">Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f26a0-243">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-244">Dernier contact</span><span class="sxs-lookup"><span data-stu-id="f26a0-244">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-245">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="f26a0-245">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f26a0-246">La fréquence de contact est configurable par le biais des paramètres de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f26a0-246">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a><span data-ttu-id="f26a0-247">Rapport de conformité de l’ordinateur BitLocker</span><span class="sxs-lookup"><span data-stu-id="f26a0-247">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="f26a0-248">Utilisez ce type de rapport pour collecter des informations spécifiques à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f26a0-248">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="f26a0-249">Le rapport de conformité de l’ordinateur BitLocker fournit des informations de chiffrement détaillées sur chaque lecteur sur un ordinateur (système d’exploitation et lecteurs de données fixes).</span><span class="sxs-lookup"><span data-stu-id="f26a0-249">The BitLocker Computer Compliance Report provides detailed encryption information about each drive on a computer (operating system and fixed data drives).</span></span> <span data-ttu-id="f26a0-250">Il fournit également une indication de la stratégie qui s’applique à chaque type de lecteur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f26a0-250">It also provides an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="f26a0-251">Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f26a0-251">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="f26a0-252">**Remarques**  Le statut de chiffrement du volume de données amovibles ne s’affiche pas dans ce rapport.</span><span class="sxs-lookup"><span data-stu-id="f26a0-252">**Note** The Removable Data Volume encryption status is not shown in this report.</span></span>

 

**<span data-ttu-id="f26a0-253">Rapport de conformité de l’ordinateur BitLocker: champs détails de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="f26a0-253">BitLocker Computer Compliance Report: Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f26a0-254">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="f26a0-254">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f26a0-255">Description</span><span class="sxs-lookup"><span data-stu-id="f26a0-255">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-256">Nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="f26a0-256">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-257">Nom d’ordinateur DNS spécifié par l’utilisateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-257">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-258">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="f26a0-258">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-259">Nom de domaine complet, où se trouve l’ordinateur client et est géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-259">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-260">Type d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="f26a0-260">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-261">Type d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f26a0-261">Type of computer.</span></span> <span data-ttu-id="f26a0-262">Les types valides ne sont pas portables et portables.</span><span class="sxs-lookup"><span data-stu-id="f26a0-262">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-263">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="f26a0-263">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-264">Type de système d’exploitation détecté sur l’ordinateur client géré MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-264">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-265">Conformité globale</span><span class="sxs-lookup"><span data-stu-id="f26a0-265">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-266">État de conformité global de l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-266">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="f26a0-267">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="f26a0-267">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="f26a0-268">Notez que l’état de conformité par lecteur (voir le tableau ci-dessous) risque d’indiquer des États de conformité différents.</span><span class="sxs-lookup"><span data-stu-id="f26a0-268">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="f26a0-269">Toutefois, ce champ correspond à cet état de conformité conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f26a0-269">However, this field represents that compliance state in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-270">Compatibilité du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f26a0-270">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-271">État de conformité du système d’exploitation géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-271">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="f26a0-272">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="f26a0-272">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-273">Compatibilité des lecteurs de données fixes</span><span class="sxs-lookup"><span data-stu-id="f26a0-273">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-274">État de la conformité du lecteur de données fixes géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-274">Compliance status of the fixed data drive that is managed by MBAM.</span></span> <span data-ttu-id="f26a0-275">Les États valides sont conformes et non conformes.</span><span class="sxs-lookup"><span data-stu-id="f26a0-275">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-276">Date de la dernière mise à jour</span><span class="sxs-lookup"><span data-stu-id="f26a0-276">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-277">Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité.</span><span class="sxs-lookup"><span data-stu-id="f26a0-277">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f26a0-278">La fréquence de contact est configurable par le biais des paramètres de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f26a0-278">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-279">Question</span><span class="sxs-lookup"><span data-stu-id="f26a0-279">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-280">État qui indique si l’utilisateur est exempté ou non exempt de la stratégie BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-280">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-281">Utilisateur exempté</span><span class="sxs-lookup"><span data-stu-id="f26a0-281">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-282">Utilisateur exempt de la stratégie BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f26a0-282">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-283">Date d’exemption</span><span class="sxs-lookup"><span data-stu-id="f26a0-283">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-284">Date à laquelle l’exemption a été accordée.</span><span class="sxs-lookup"><span data-stu-id="f26a0-284">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-285">Détails de l’état de conformité</span><span class="sxs-lookup"><span data-stu-id="f26a0-285">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-286">Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f26a0-286">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-287">Niveau de cryptage de la stratégie</span><span class="sxs-lookup"><span data-stu-id="f26a0-287">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-288">Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM (par exemple, 128-bits avec diffuseur).</span><span class="sxs-lookup"><span data-stu-id="f26a0-288">Cipher strength selected by the Administrator during the MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-289">Stratégie: lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f26a0-289">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-290">Indique si le chiffrement est requis pour le système d’exploitation et le type de protecteur approprié.</span><span class="sxs-lookup"><span data-stu-id="f26a0-290">Indicates if encryption is required for the operating system and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-291">Stratégie: disque de données fixe</span><span class="sxs-lookup"><span data-stu-id="f26a0-291">Policy: Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-292">Indique si le chiffrement est requis pour le lecteur de données fixes.</span><span class="sxs-lookup"><span data-stu-id="f26a0-292">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-293">Fabricant</span><span class="sxs-lookup"><span data-stu-id="f26a0-293">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-294">Nom de fabricant de l’ordinateur tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f26a0-294">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-295">Modèle</span><span class="sxs-lookup"><span data-stu-id="f26a0-295">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-296">Nom de modèle du fabricant d’ordinateurs tel qu’il apparaît dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f26a0-296">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-297">Utilisateurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="f26a0-297">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-298">Utilisateurs connus sur l’ordinateur géré par MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-298">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f26a0-299">Rapport de conformité de l’ordinateur BitLocker: champs volume de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="f26a0-299">BitLocker Computer Compliance Report: Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f26a0-300">Nom de la colonne</span><span class="sxs-lookup"><span data-stu-id="f26a0-300">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f26a0-301">Description</span><span class="sxs-lookup"><span data-stu-id="f26a0-301">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-302">Lettre du lecteur</span><span class="sxs-lookup"><span data-stu-id="f26a0-302">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-303">Lettre du lecteur de l’ordinateur qui a été affectée à l’utilisateur en particulier.</span><span class="sxs-lookup"><span data-stu-id="f26a0-303">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-304">Type de lecteur</span><span class="sxs-lookup"><span data-stu-id="f26a0-304">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-305">Type de lecteur.</span><span class="sxs-lookup"><span data-stu-id="f26a0-305">Type of drive.</span></span> <span data-ttu-id="f26a0-306">Les valeurs valides sont le lecteur du système d’exploitation et le lecteur de données fixes.</span><span class="sxs-lookup"><span data-stu-id="f26a0-306">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="f26a0-307">Il s’agit de disques physiques plutôt que de volumes logiques.</span><span class="sxs-lookup"><span data-stu-id="f26a0-307">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-308">Niveau de cryptage</span><span class="sxs-lookup"><span data-stu-id="f26a0-308">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-309">Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="f26a0-309">Cipher strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-310">Types de protecteur</span><span class="sxs-lookup"><span data-stu-id="f26a0-310">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-311">Type de protecteur sélectionné par le biais de la stratégie utilisée pour chiffrer un système d’exploitation ou un lecteur de données fixe.</span><span class="sxs-lookup"><span data-stu-id="f26a0-311">Type of protector selected through the policy used to encrypt an operating system or fixed data drive.</span></span> <span data-ttu-id="f26a0-312">Les types de protecteur valides pour un système d’exploitation sont TPM ou TPM + NIP.</span><span class="sxs-lookup"><span data-stu-id="f26a0-312">The valid protector types for an operating system are TPM or TPM+PIN.</span></span> <span data-ttu-id="f26a0-313">Le type de protecteur valide pour un lecteur de données fixe est un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f26a0-313">The valid protector type for a fixed data drive is a password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f26a0-314">État de protecteur</span><span class="sxs-lookup"><span data-stu-id="f26a0-314">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-315">Indique que l’ordinateur géré par MBAM a activé le type de protecteur spécifié dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="f26a0-315">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="f26a0-316">Les États valides sont ACTIVÉs ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="f26a0-316">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f26a0-317">État du chiffrement</span><span class="sxs-lookup"><span data-stu-id="f26a0-317">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f26a0-318">État du chiffrement du lecteur.</span><span class="sxs-lookup"><span data-stu-id="f26a0-318">Encryption state of the drive.</span></span> <span data-ttu-id="f26a0-319">Les États valides sont chiffrés, non chiffrés et chiffrés.</span><span class="sxs-lookup"><span data-stu-id="f26a0-319">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f26a0-320">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f26a0-320">Related topics</span></span>


[<span data-ttu-id="f26a0-321">Surveillance et création de rapports de la conformité BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f26a0-321">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## <span data-ttu-id="f26a0-322">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="f26a0-322">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f26a0-323">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="f26a0-323">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f26a0-324">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f26a0-324">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 






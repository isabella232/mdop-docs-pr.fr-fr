---
title: Générer des rapports MBAM
description: Générer des rapports MBAM
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810608"
---
# <span data-ttu-id="4a69b-103">Générer des rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="4a69b-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="4a69b-104">Microsoft BitLocker administration et surveillance (MBAM) génère divers rapports pour contrôler l’utilisation et la conformité du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4a69b-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="4a69b-105">Cette rubrique décrit comment ouvrir le site Web d’administration MBAM et générer des rapports MBAM sur le respect de la conformité d’entreprise, des ordinateurs individuels, de la compatibilité matérielle et de la récupération de clés.</span><span class="sxs-lookup"><span data-stu-id="4a69b-105">This topic describes how to open the MBAM administration website and how to generate MBAM reports on enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span> <span data-ttu-id="4a69b-106">Pour plus d’informations sur les rapports MBAM, voir [Présentation des rapports MBAM](understanding-mbam-reports-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="4a69b-106">For more information about MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-1.md).</span></span>

<span data-ttu-id="4a69b-107">**Remarques**  Pour exécuter les rapports, vous devez être membre du rôle **utilisateurs du rapport** sur les ordinateurs sur lesquels vous avez installé les fonctionnalités d’administration et de surveillance de la base de données de serveur d’administration et de conformité, ainsi que des rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="4a69b-107">**Note** To run the reports, you must be a member of the **Report Users** role on the computers where you have installed the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports.</span></span>

 

**<span data-ttu-id="4a69b-108">Pour ouvrir le site Web d’administration MBAM</span><span class="sxs-lookup"><span data-stu-id="4a69b-108">To open the MBAM Administration website</span></span>**

1.  <span data-ttu-id="4a69b-109">Ouvrez un navigateur Web, puis accédez au site Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="4a69b-109">Open a web browser and navigate to the MBAM website.</span></span> <span data-ttu-id="4a69b-110">L’URL par défaut du site Web *est &lt; http:// &gt; nomordinateur* du serveur d’administration et de contrôle Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4a69b-110">The default URL for the website is *http://&lt;computername&gt;* of the Microsoft BitLocker Administration and Monitoring server.</span></span>

    <span data-ttu-id="4a69b-111">**Remarques**  Si le site Web MBAMadministration a été installé sur un autre port que le port 80, vous devez spécifier ce numéro de port dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="4a69b-111">**Note** If the MBAMadministration website was installed on a port other than port 80, you must specify that port number in the URL.</span></span> <span data-ttu-id="4a69b-112">Par exemple, \*http:// &lt; nomordinateur &gt; : &lt; port &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="4a69b-112">For example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="4a69b-113">Si vous spécifiez un nom d’hôte pour le site Web MBAMadministration lors de l’installation, l’URL serait \*http:// &lt; hostname &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="4a69b-113">If you specified a Host Name for the MBAMadministration website during the installation, the URL would be *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="4a69b-114">Dans le volet de navigation, cliquez sur **rapports**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-114">In the navigation pane, click **Reports**.</span></span> <span data-ttu-id="4a69b-115">Dans le volet principal, cliquez sur l’onglet de votre type de rapport: **rapport de conformité d’entreprise**, rapport de conformité des **ordinateurs**, rapport **d’audit matériel**ou **rapport d’audit de récupération**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-115">In the main pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

    <span data-ttu-id="4a69b-116">**Remarques**  Les données du client MBAM historique sont conservées dans la base de données de conformité.</span><span class="sxs-lookup"><span data-stu-id="4a69b-116">**Note** Historical MBAM Client data is retained in the compliance database.</span></span> <span data-ttu-id="4a69b-117">Ce risque de perte de données peut être requis en cas de perte ou de vol d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4a69b-117">This retained data may be needed in case a computer is lost or stolen.</span></span> <span data-ttu-id="4a69b-118">Lors de l’exécution de rapports d’entreprise, vous devez utiliser les dates de début et de fin appropriées pour limiter les délais pour les rapports de une à deux semaines afin d’améliorer la précision des données de rapport.</span><span class="sxs-lookup"><span data-stu-id="4a69b-118">When running enterprise reports, you should use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase the reporting data accuracy.</span></span>

     

**<span data-ttu-id="4a69b-119">Pour générer un rapport de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="4a69b-119">To generate an enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="4a69b-120">Sur le site Web MBAMadministration, cliquez sur **rapports** dans le volet de navigation, puis cliquez sur l’onglet **rapport de conformité d’entreprise** et sélectionnez les filtres appropriés pour votre rapport.</span><span class="sxs-lookup"><span data-stu-id="4a69b-120">On the MBAMadministration website, click **Reports** in the navigation pane, then click the **Enterprise Compliance Report** tab and select the appropriate filters for your report.</span></span> <span data-ttu-id="4a69b-121">Pour le rapport de conformité d’entreprise, vous pouvez définir les filtres suivants.</span><span class="sxs-lookup"><span data-stu-id="4a69b-121">For the Enterprise Compliance Report, you can set the following filters.</span></span>

    -   <span data-ttu-id="4a69b-122">**État de la conformité**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-122">**Compliance Status**.</span></span> <span data-ttu-id="4a69b-123">Utilisez ce filtre pour spécifier les types d’état de conformité (par exemple, conforme ou non conforme) à inclure dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="4a69b-123">Use this filter to specify the compliance status types (for example, Compliant or Noncompliant) to include in the report.</span></span>

    -   <span data-ttu-id="4a69b-124">**État d’erreur**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-124">**Error State**.</span></span> <span data-ttu-id="4a69b-125">Utilisez ce filtre pour spécifier les types d’état d’erreur (par exemple, aucune erreur ou erreur) à inclure dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="4a69b-125">Use this filter to specify the Error State types, such as No Error or Error, to include in the report.</span></span>

2.  <span data-ttu-id="4a69b-126">Cliquez sur **afficher le rapport** pour afficher le rapport spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a69b-126">Click **View Report** to display the specified report.</span></span>

    <span data-ttu-id="4a69b-127">Les résultats du rapport peuvent être enregistrés dans l’un des nombreux formats de fichier disponibles (par exemple, HTML, Microsoft Word et Microsoft Excel).</span><span class="sxs-lookup"><span data-stu-id="4a69b-127">The report results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="4a69b-128">**Remarques**  Le rapport de conformité d’entreprise est généré par un travail SQL qui s’exécute toutes les six heures.</span><span class="sxs-lookup"><span data-stu-id="4a69b-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="4a69b-129">Dès lors que vous essayez d’afficher le rapport pour la première fois, il est possible que certaines données soient manquantes.</span><span class="sxs-lookup"><span data-stu-id="4a69b-129">Therefore, the first time you try to view the report you may find that some data is missing.</span></span>

     

3.  <span data-ttu-id="4a69b-130">Pour afficher des informations sur un ordinateur figurant dans le rapport de conformité informatique, sélectionnez le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4a69b-130">To view information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="4a69b-131">Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4a69b-131">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="4a69b-132">Pour générer le rapport de conformité de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="4a69b-132">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="4a69b-133">Sur le site Web MBAMadministration, sélectionnez le nœud de **rapport** dans le volet de navigation, puis sélectionnez le **rapport de conformité**de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4a69b-133">In the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="4a69b-134">Utilisez le rapport de conformité de l’ordinateur pour rechercher le **nom d’utilisateur** ou le nom de l' **ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-134">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="4a69b-135">Cliquez sur **afficher le rapport** pour afficher le rapport sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4a69b-135">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="4a69b-136">Les résultats peuvent être enregistrés dans l’un des formats de fichier disponibles (par exemple, HTML, Microsoft Word et Microsoft Excel).</span><span class="sxs-lookup"><span data-stu-id="4a69b-136">Results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="4a69b-137">Pour afficher des informations supplémentaires sur un ordinateur dans le rapport de conformité informatique, sélectionnez le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4a69b-137">To display more information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="4a69b-138">Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4a69b-138">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="4a69b-139">**Remarques**  Un ordinateur client MBAM est considéré comme conforme si l’ordinateur répond aux exigences des paramètres de stratégie MBAM ou si le modèle matériel de l’ordinateur est défini sur incompatible.</span><span class="sxs-lookup"><span data-stu-id="4a69b-139">**Note** An MBAM Client computer is considered compliant if the computer matches the requirements of the MBAM policy settings or the computer’s hardware model is set to incompatible.</span></span> <span data-ttu-id="4a69b-140">Par conséquent, lorsque vous affichez des informations détaillées sur les volumes de disque associés à l’ordinateur, les ordinateurs exemptés du chiffrement BitLocker en raison de la compatibilité matérielle peuvent être affichés comme conformes, même si leur état de chiffrement de volume est affiché comme non conforme.</span><span class="sxs-lookup"><span data-stu-id="4a69b-140">Therefore, when you are viewing detailed information about the disk volumes associated with the computer, computers that are exempt from BitLocker encryption due to hardware compatibility can be displayed as compliant even though their drive volume encryption status is displayed as noncompliant.</span></span>

     

**<span data-ttu-id="4a69b-141">Pour générer le rapport d’audit de compatibilité matérielle</span><span class="sxs-lookup"><span data-stu-id="4a69b-141">To generate the Hardware Compatibility Audit Report</span></span>**

1.  <span data-ttu-id="4a69b-142">Sur le site Web MBAMadministration, sélectionnez le nœud de **rapport** dans le volet de navigation, puis sélectionnez le **rapport de vérification matérielle**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-142">From the MBAMadministration website, select the **Report** node from the navigation pane, and then select the **Hardware Audit Report**.</span></span> <span data-ttu-id="4a69b-143">Sélectionnez les filtres appropriés pour le rapport d’audit de votre matériel.</span><span class="sxs-lookup"><span data-stu-id="4a69b-143">Select the appropriate filters for your Hardware Audit report.</span></span> <span data-ttu-id="4a69b-144">Le rapport de vérification matérielle fournit les filtres suivants disponibles:</span><span class="sxs-lookup"><span data-stu-id="4a69b-144">The Hardware Audit report offers the following available filters:</span></span>

    -   <span data-ttu-id="4a69b-145">**Utilisateur (Domain\\User)**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-145">**User (Domain\\User)**.</span></span> <span data-ttu-id="4a69b-146">Spécifie le nom de l’utilisateur qui a apporté une modification.</span><span class="sxs-lookup"><span data-stu-id="4a69b-146">Specifies the name of the user who made a change.</span></span>

    -   <span data-ttu-id="4a69b-147">**Changer de type**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-147">**Change Type**.</span></span> <span data-ttu-id="4a69b-148">Spécifie le type de modification que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="4a69b-148">Specifies the type of changes you are looking for.</span></span>

    -   <span data-ttu-id="4a69b-149">**Date de début**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-149">**Start Date**.</span></span> <span data-ttu-id="4a69b-150">Spécifie la partie Date de début de la plage de dates dans laquelle vous souhaitez créer un rapport.</span><span class="sxs-lookup"><span data-stu-id="4a69b-150">Specifies the Start Date part of the date range that you want to report on.</span></span>

    -   <span data-ttu-id="4a69b-151">**Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-151">**End Date**.</span></span> <span data-ttu-id="4a69b-152">Spécifie la partie de la date de fin de la plage de dates dans laquelle vous souhaitez créer un rapport.</span><span class="sxs-lookup"><span data-stu-id="4a69b-152">Specifies the End Date part of the date range that you want to report on.</span></span>

2.  <span data-ttu-id="4a69b-153">Cliquez sur **afficher le rapport** pour afficher le rapport.</span><span class="sxs-lookup"><span data-stu-id="4a69b-153">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="4a69b-154">Vous pouvez enregistrer les résultats dans différents formats de fichier (par exemple, HTML, Microsoft Word et Microsoft Excel).</span><span class="sxs-lookup"><span data-stu-id="4a69b-154">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

**<span data-ttu-id="4a69b-155">Pour générer le rapport d’audit de clé de récupération</span><span class="sxs-lookup"><span data-stu-id="4a69b-155">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="4a69b-156">Sur le site Web de MBAMadministration, sélectionnez le nœud de **rapport** dans le volet de navigation, puis sélectionnez le **rapport d’audit de récupération**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-156">From the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="4a69b-157">Sélectionnez les filtres du rapport d’audit de la clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="4a69b-157">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="4a69b-158">Les filtres disponibles pour les audits de clé de récupération sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="4a69b-158">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="4a69b-159">**Demandeur**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-159">**Requestor**.</span></span> <span data-ttu-id="4a69b-160">Spécifie le nom d’utilisateur du demandeur.</span><span class="sxs-lookup"><span data-stu-id="4a69b-160">Specifies the user name of the requestor.</span></span> <span data-ttu-id="4a69b-161">Le demandeur est la personne du support technique qui a accédé à la clé pour le compte d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a69b-161">The requestor is the person in the help desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="4a69b-162">**Demandeur**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-162">**Requestee**.</span></span> <span data-ttu-id="4a69b-163">Spécifie le nom d’utilisateur de la requête.</span><span class="sxs-lookup"><span data-stu-id="4a69b-163">Specifies the user name of the requestee.</span></span> <span data-ttu-id="4a69b-164">La personne qui a appelé le support technique peut obtenir une clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="4a69b-164">The requestee is the person who called the help desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="4a69b-165">**Résultat** de la requête Spécifie les types de résultats de la requête, tels que: réussite ou échec.</span><span class="sxs-lookup"><span data-stu-id="4a69b-165">**Request Result** Specifies the request result types, such as: Success or Failed.</span></span> <span data-ttu-id="4a69b-166">Par exemple, il est possible que vous souhaitiez afficher les tentatives d’accès par clé en échec.</span><span class="sxs-lookup"><span data-stu-id="4a69b-166">For example, you may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="4a69b-167">**Type de clé**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-167">**Key Type**.</span></span> <span data-ttu-id="4a69b-168">Spécifie le type de clé, par exemple: mot de passe de clé de récupération ou hachage du mot de passe TPM.</span><span class="sxs-lookup"><span data-stu-id="4a69b-168">Specifies the Key Type, such as: Recovery Key Password or TPM Password Hash.</span></span>

    -   <span data-ttu-id="4a69b-169">**Date de début**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-169">**Start Date**.</span></span> <span data-ttu-id="4a69b-170">Spécifie la date de début dans la plage de dates.</span><span class="sxs-lookup"><span data-stu-id="4a69b-170">Specifies the Start Date part of the date range.</span></span>

    -   <span data-ttu-id="4a69b-171">**Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="4a69b-171">**End Date**.</span></span> <span data-ttu-id="4a69b-172">Spécifie la partie de la date de fin de la plage de dates.</span><span class="sxs-lookup"><span data-stu-id="4a69b-172">Specifies the End Date part of the date range.</span></span>

2.  <span data-ttu-id="4a69b-173">Cliquez sur **afficher le rapport** pour afficher le rapport.</span><span class="sxs-lookup"><span data-stu-id="4a69b-173">Click **View Report** to display the report.</span></span>

    <span data-ttu-id="4a69b-174">Vous pouvez enregistrer les résultats dans différents formats de fichier (par exemple, HTML, Microsoft Word et Microsoft Excel).</span><span class="sxs-lookup"><span data-stu-id="4a69b-174">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="4a69b-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a69b-175">Related topics</span></span>


[<span data-ttu-id="4a69b-176">Surveillance et création de rapports de la conformité BitLocker avec MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="4a69b-176">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 






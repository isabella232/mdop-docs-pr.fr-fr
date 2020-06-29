---
title: Génération des rapports MBAM2.5 autonomes
description: Génération des rapports MBAM2.5 autonomes
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809767"
---
# <span data-ttu-id="666b7-103">Génération des rapports MBAM2.5 autonomes</span><span class="sxs-lookup"><span data-stu-id="666b7-103">Generating MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="666b7-104">Lorsque vous configurez l’administration et la surveillance de Microsoft BitLocker (MBAM) avec la topologie autonome, vous pouvez générer des rapports pour contrôler l’utilisation et la conformité du chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="666b7-104">When you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate reports to monitor BitLocker drive encryption usage and compliance.</span></span> <span data-ttu-id="666b7-105">Cette rubrique contient les procédures suivantes:</span><span class="sxs-lookup"><span data-stu-id="666b7-105">This topic contains the following procedures:</span></span>

-   [<span data-ttu-id="666b7-106">Pour ouvrir le site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="666b7-106">To open the Administration and Monitoring Website</span></span>](#bkmk-openadmin)

-   [<span data-ttu-id="666b7-107">Pour générer un rapport de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="666b7-107">To generate an Enterprise Compliance Report</span></span>](#bkmk-enterprise)

-   [<span data-ttu-id="666b7-108">Pour générer un rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="666b7-108">To generate a Computer Compliance Report</span></span>](#bkmk-computercomp)

-   [<span data-ttu-id="666b7-109">Pour générer un rapport d’audit de clé de récupération</span><span class="sxs-lookup"><span data-stu-id="666b7-109">To generate a Recovery Key Audit Report</span></span>](#bkmk-recoverykey)

<span data-ttu-id="666b7-110">Pour obtenir une description des rapports autonomes, voir [Présentation des rapports MBAM 2,5 autonomes](understanding-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="666b7-110">For descriptions of the Stand-alone reports, see [Understanding MBAM 2.5 Stand-alone Reports](understanding-mbam-25-stand-alone-reports.md).</span></span>

<span data-ttu-id="666b7-111">**Remarques**  Pour exécuter les rapports, vous devez être membre du groupe **MBAM des utilisateurs du rapport** , que vous configurez dans les services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="666b7-111">**Note** To run the reports, you must be a member of the **MBAM Report Users** group, which you configure in Active Directory Domain Services.</span></span> <span data-ttu-id="666b7-112">Pour plus d’informations, reportez-vous [à planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="666b7-112">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

 

<a href="" id="bkmk-openadmin"></a>**<span data-ttu-id="666b7-113">Pour ouvrir le site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="666b7-113">To open the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="666b7-114">Ouvrez un navigateur Web, puis accédez au site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="666b7-114">Open a web browser and navigate to the Administration and Monitoring Website.</span></span> <span data-ttu-id="666b7-115">L’URL par défaut du site Web d’administration et de surveillance est la suivante:</span><span class="sxs-lookup"><span data-stu-id="666b7-115">The default URL for the Administration and Monitoring Website is:</span></span>

    *<span data-ttu-id="666b7-116">http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; port &gt; /helpdesk</span><span class="sxs-lookup"><span data-stu-id="666b7-116">http(s)://&lt;MBAMAdministrationServerName&gt;:&lt;port&gt;/Helpdesk</span></span>*

2.  <span data-ttu-id="666b7-117">Dans le volet de gauche, cliquez sur **rapports**.</span><span class="sxs-lookup"><span data-stu-id="666b7-117">In the left pane, click **Reports**.</span></span> <span data-ttu-id="666b7-118">Dans la barre de menus supérieure, sélectionnez le rapport que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="666b7-118">From the top menu bar, select the report you want to run.</span></span>

    <span data-ttu-id="666b7-119">Les données du client MBAM sont conservées dans la base de données d’audit et de conformité pour référence historique en cas de perte ou de vol d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="666b7-119">MBAM client data is retained in the Compliance and Audit Database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="666b7-120">Lors de l’exécution de rapports d’entreprise, nous vous recommandons d’utiliser les dates de début et de fin appropriées pour limiter les délais des rapports de une à deux semaines afin d’améliorer la précision des données de rapport.</span><span class="sxs-lookup"><span data-stu-id="666b7-120">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="666b7-121">Après avoir généré un rapport, vous pouvez enregistrer les résultats dans différents formats, tels que HTML, Microsoft Word et Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="666b7-121">After you generate a report, you can save the results in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="666b7-122">**Remarques**  Configurer SQL Server Reporting Services (SSRS) pour utiliser le protocole SSL (Secure Sockets Layer) avant de configurer le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="666b7-122">**Note** Configure SQL Server Reporting Services (SSRS) to use Secure Sockets Layer (SSL) before configuring the Administration and Monitoring Website.</span></span> <span data-ttu-id="666b7-123">Si, pour une raison quelconque, SSRS n’est pas configuré pour utiliser SSL, l’URL des rapports sera définie sur HTTP au lieu de HTTPs lorsque vous configurez le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="666b7-123">If, for any reason, SSRS is not configured to use SSL, the URL for the Reports will be set to HTTP instead of to HTTPS when you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="666b7-124">Si vous accédez au site Web Administration et surveillance et sélectionnez un rapport, le message suivant s’affiche: «seul le contenu sécurisé est affiché».</span><span class="sxs-lookup"><span data-stu-id="666b7-124">If you then go to the Administration and Monitoring Website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="666b7-125">Pour afficher l’État, cliquez sur **Afficher tout le contenu**.</span><span class="sxs-lookup"><span data-stu-id="666b7-125">To show the report, click **Show All Content**.</span></span>

     

<a href="" id="bkmk-enterprise"></a>**<span data-ttu-id="666b7-126">Pour générer un rapport de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="666b7-126">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="666b7-127">Sur le site Web d’administration et de surveillance, sélectionnez le nœud **rapports** dans le volet de navigation gauche, sélectionnez **rapport de conformité d’entreprise**, puis les filtres que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="666b7-127">From the Administration and Monitoring Website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="666b7-128">Les filtres disponibles pour le rapport de conformité d’entreprise sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="666b7-128">The available filters for the Enterprise Compliance Report are:</span></span>

    -   <span data-ttu-id="666b7-129">**État de la conformité**.</span><span class="sxs-lookup"><span data-stu-id="666b7-129">**Compliance Status**.</span></span> <span data-ttu-id="666b7-130">Utilisez ce filtre pour spécifier les types d’état de conformité du rapport (par exemple, conforme ou non conforme).</span><span class="sxs-lookup"><span data-stu-id="666b7-130">Use this filter to specify the compliance status types of the report (for example, Compliant or Noncompliant).</span></span>

    -   <span data-ttu-id="666b7-131">**État d’erreur**.</span><span class="sxs-lookup"><span data-stu-id="666b7-131">**Error State**.</span></span> <span data-ttu-id="666b7-132">Utilisez ce filtre pour spécifier les types d’état d’erreur du rapport (par exemple, aucune erreur ou erreur).</span><span class="sxs-lookup"><span data-stu-id="666b7-132">Use this filter to specify the error state types of the report (for example, No Error or Error).</span></span>

2.  <span data-ttu-id="666b7-133">Cliquez sur **afficher le rapport** pour afficher le rapport sélectionné.</span><span class="sxs-lookup"><span data-stu-id="666b7-133">Click **View Report** to display the selected report.</span></span>

3.  <span data-ttu-id="666b7-134">Sélectionnez le nom d’un ordinateur pour afficher des informations relatives à l’ordinateur figurant dans le rapport de compatibilité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="666b7-134">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="666b7-135">Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="666b7-135">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

<a href="" id="bkmk-computercomp"></a>**<span data-ttu-id="666b7-136">Pour générer un rapport de conformité ordinateur</span><span class="sxs-lookup"><span data-stu-id="666b7-136">To generate a Computer Compliance Report</span></span>**

1.  <span data-ttu-id="666b7-137">Sur le site Web d’administration et de surveillance, sélectionnez le nœud de **rapport** dans le volet de navigation gauche, puis cliquez sur **rapport de conformité d’ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="666b7-137">From the Administration and Monitoring Website, select the **Report** node from the left navigation pane, and then select **Computer Compliance Report**.</span></span> <span data-ttu-id="666b7-138">Utilisez le rapport de conformité de l’ordinateur pour rechercher le **nom d’utilisateur** ou le nom de l' **ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="666b7-138">Use the Computer Compliance Report to search for **User name** or **Computer name**.</span></span>

2.  <span data-ttu-id="666b7-139">Cliquez sur **afficher le rapport** pour afficher le rapport de conformité de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="666b7-139">Click **View Report** to view the Computer Compliance Report.</span></span>

3.  <span data-ttu-id="666b7-140">Sélectionnez le nom d’un ordinateur pour afficher des informations supplémentaires sur celui-ci dans le rapport de compatibilité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="666b7-140">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="666b7-141">Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="666b7-141">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="666b7-142">**Remarques**  Un ordinateur client MBAM est considéré comme conforme si l’ordinateur répond à la configuration requise des paramètres de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="666b7-142">**Note** An MBAM client computer is considered compliant if the computer matches or exceeds the requirements of the MBAM Group Policy settings.</span></span>

<a href="" id="bkmk-recoverykey"></a>**<span data-ttu-id="666b7-143">Pour générer un rapport d’audit de clé de récupération</span><span class="sxs-lookup"><span data-stu-id="666b7-143">To generate a Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="666b7-144">Sur le site Web d’administration et de surveillance, sélectionnez le nœud de **rapport** dans le volet de navigation gauche, puis cliquez sur **rapport d’audit de récupération**.</span><span class="sxs-lookup"><span data-stu-id="666b7-144">From the Administration and Monitoring Website, select the **Report** node in the left navigation pane, and then select **Recovery Audit Report**.</span></span> <span data-ttu-id="666b7-145">Sélectionnez les filtres du rapport d’audit de la clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="666b7-145">Select the filters for your Recovery Key Audit Report.</span></span> <span data-ttu-id="666b7-146">Les filtres disponibles pour les audits de clé de récupération sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="666b7-146">The available filters for recovery key audits are as follows:</span></span>

    -   <span data-ttu-id="666b7-147">**Utilisateur du support technique**.</span><span class="sxs-lookup"><span data-stu-id="666b7-147">**Helpdesk User**.</span></span> <span data-ttu-id="666b7-148">Ce filtre permet aux utilisateurs de spécifier le nom d’utilisateur du demandeur.</span><span class="sxs-lookup"><span data-stu-id="666b7-148">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="666b7-149">Le demandeur est la personne du support technique qui a accédé à la clé pour le compte d’un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="666b7-149">The requester is the person in the Help Desk who accessed the key on behalf of an end user.</span></span>

    -   <span data-ttu-id="666b7-150">**Utilisateur final**.</span><span class="sxs-lookup"><span data-stu-id="666b7-150">**End User**.</span></span> <span data-ttu-id="666b7-151">Ce filtre permet aux utilisateurs de spécifier le nom d’utilisateur de la requête.</span><span class="sxs-lookup"><span data-stu-id="666b7-151">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="666b7-152">La demande est l’utilisateur final ayant appelé le support technique pour obtenir une clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="666b7-152">The requestee is the end user who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="666b7-153">**Résultat**de la requête.</span><span class="sxs-lookup"><span data-stu-id="666b7-153">**Request Result**.</span></span> <span data-ttu-id="666b7-154">Ce filtre permet aux utilisateurs de spécifier les types de résultats de requête (par exemple, succès ou échec) sur lesquels ils veulent baser le rapport.</span><span class="sxs-lookup"><span data-stu-id="666b7-154">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="666b7-155">Par exemple, les utilisateurs peuvent souhaiter afficher les tentatives d’accès par clé en échec.</span><span class="sxs-lookup"><span data-stu-id="666b7-155">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="666b7-156">**Type de clé**.</span><span class="sxs-lookup"><span data-stu-id="666b7-156">**Key Type**.</span></span> <span data-ttu-id="666b7-157">Ce filtre permet aux utilisateurs de spécifier le type de clé (par exemple, un mot de passe pour la clé de récupération ou le hachage du mot de passe du TPM) sur lequel il souhaite baser le rapport.</span><span class="sxs-lookup"><span data-stu-id="666b7-157">This filter enables users to specify the key type (for example, Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="666b7-158">**Date de début**.</span><span class="sxs-lookup"><span data-stu-id="666b7-158">**Start Date**.</span></span> <span data-ttu-id="666b7-159">Ce filtre permet de définir la partie Date de début de la plage de dates à laquelle l’utilisateur souhaite rapporter.</span><span class="sxs-lookup"><span data-stu-id="666b7-159">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="666b7-160">**Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="666b7-160">**End Date**.</span></span> <span data-ttu-id="666b7-161">Ce filtre est utilisé pour définir la partie de la date de fin de la plage de dates à laquelle les utilisateurs veulent rapporter.</span><span class="sxs-lookup"><span data-stu-id="666b7-161">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="666b7-162">Cliquez sur **afficher le rapport** pour afficher le rapport.</span><span class="sxs-lookup"><span data-stu-id="666b7-162">Click **View Report** to view the report.</span></span>



## <span data-ttu-id="666b7-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="666b7-163">Related topics</span></span>


[<span data-ttu-id="666b7-164">Surveillance et création de rapports de la conformité BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="666b7-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="666b7-165">Présentation des rapports autonomes MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="666b7-165">Understanding MBAM 2.5 Stand-alone Reports</span></span>](understanding-mbam-25-stand-alone-reports.md)

 

## <span data-ttu-id="666b7-166">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="666b7-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="666b7-167">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="666b7-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="666b7-168">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="666b7-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 






---
title: Générer des rapports MBAM
description: Générer des rapports MBAM
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810349"
---
# <span data-ttu-id="70750-103">Générer des rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="70750-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="70750-104">Lorsque vous installez Microsoft BitLocker administration et surveillance (MBAM) avec la topologie autonome, vous pouvez générer différents rapports pour contrôler l’utilisation et la conformité du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="70750-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate different reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="70750-105">Les procédures décrites dans cette rubrique expliquent comment ouvrir le site Web d’administration et de contrôle, ainsi que les étapes nécessaires pour générer des rapports d’administration et de surveillance de BitLocker sur le respect de l’entreprise, sur les ordinateurs individuels et sur l’activité de récupération des clés.</span><span class="sxs-lookup"><span data-stu-id="70750-105">The procedures in this topic describe how to open the Administration and Monitoring website and the steps that are needed to generate Microsoft BitLocker Administration and Monitoring reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="70750-106">Pour plus d’informations sur les rapports MBAM, voir [Présentation des rapports MBAM](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="70750-106">For detailed information to help understand MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

<span data-ttu-id="70750-107">**Remarques**  Pour exécuter les rapports, vous devez être membre du rôle de l' **utilisateur du rapport** sur les ordinateurs sur lesquels sont installés les rapports d’administration et de surveillance des fonctionnalités du serveur, de la conformité et de l’audit.</span><span class="sxs-lookup"><span data-stu-id="70750-107">**Note** To run the reports, you must be a member of the **Report Users Role** on the computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

 

**<span data-ttu-id="70750-108">Pour ouvrir le site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="70750-108">To open the Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="70750-109">Ouvrez un navigateur Web, puis accédez au site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="70750-109">Open a web browser and navigate to the Administration and Monitoring website.</span></span> <span data-ttu-id="70750-110">L’URL par défaut du site Web d’administration et de surveillance est \*http:// &lt; nomordinateur &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="70750-110">The default URL for the Administration and Monitoring website is *http://&lt;computername&gt;*.</span></span>

    <span data-ttu-id="70750-111">**Remarques**  Si theAdministration et le site Web de surveillance ont été installés sur un autre port que 80, vous devez spécifier le port dans l’URL (par exemple, \*http:// &lt; nomordinateur &gt; : &lt; port &gt; \*).</span><span class="sxs-lookup"><span data-stu-id="70750-111">**Note** If theAdministration and Monitoring website was installed on a port other than 80, you have to specify the port in the URL (for example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="70750-112">Si vous avez spécifié un nom d’hôte pour theAdministration et qu’il est en cours d’installation, l’URL est \*http:// &lt; hostname &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="70750-112">If you specified a host name for theAdministration and Monitoring website during the installation, the URL is *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="70750-113">Dans le volet gauche, cliquez sur **rapports** , puis sélectionnez le rapport que vous souhaitez exécuter dans la barre de menus supérieure.</span><span class="sxs-lookup"><span data-stu-id="70750-113">In the left pane, click **Reports** and then select the report you want to run from the top menu bar.</span></span>

    <span data-ttu-id="70750-114">Les données du client MBAM historique sont conservées dans la base de données de conformité pour référence historique en cas de perte ou de vol d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="70750-114">Historical MBAM client data is retained in the compliance database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="70750-115">Lors de l’exécution de rapports d’entreprise, nous vous recommandons d’utiliser les dates de début et de fin appropriées pour limiter les délais des rapports de une à deux semaines afin d’améliorer la précision des données de rapport.</span><span class="sxs-lookup"><span data-stu-id="70750-115">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="70750-116">**Remarques**  Si SSRS n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL des rapports sera définie sur HTTP au lieu de HTTPs lors de l’installation du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="70750-116">**Note** If SSRS was not configured to use Secure Socket Layer, the URL for the reports will be set to HTTP instead of to HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="70750-117">Si vous accédez au portail du support technique et sélectionnez un rapport, le message suivant s’affiche: «seul le contenu sécurisé est affiché».</span><span class="sxs-lookup"><span data-stu-id="70750-117">If you then go to the Help Desk portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="70750-118">Pour afficher l’État, cliquez sur **Afficher tout le contenu**.</span><span class="sxs-lookup"><span data-stu-id="70750-118">To show the report, click **Show All Content**.</span></span>

     

**<span data-ttu-id="70750-119">Pour générer un rapport de conformité d’entreprise</span><span class="sxs-lookup"><span data-stu-id="70750-119">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="70750-120">Sur le site Web d’administration et de surveillance, sélectionnez le nœud **rapports** dans le volet de navigation gauche, sélectionnez **rapport de conformité d’entreprise**, puis les filtres que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="70750-120">From the Administration and Monitoring website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="70750-121">Les filtres disponibles pour le rapport de conformité d’entreprise sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="70750-121">The available filters for the Enterprise Compliance Report are the following:</span></span>

    -   <span data-ttu-id="70750-122">**État de la conformité**.</span><span class="sxs-lookup"><span data-stu-id="70750-122">**Compliance Status**.</span></span> <span data-ttu-id="70750-123">Utilisez ce filtre pour spécifier les types d’état de conformité (par exemple, conforme ou non conforme) du rapport.</span><span class="sxs-lookup"><span data-stu-id="70750-123">Use this filter to specify the compliance status types (for example, Compliant, or Noncompliant) of the report.</span></span>

    -   <span data-ttu-id="70750-124">**État d’erreur**.</span><span class="sxs-lookup"><span data-stu-id="70750-124">**Error State**.</span></span> <span data-ttu-id="70750-125">Utilisez ce filtre pour spécifier les types d’état d’erreur (par exemple, aucune erreur ou erreur) du rapport.</span><span class="sxs-lookup"><span data-stu-id="70750-125">Use this filter to specify the error state types (for example, No Error, or Error) of the report.</span></span>

2.  <span data-ttu-id="70750-126">Cliquez sur **afficher le rapport** pour afficher le rapport sélectionné.</span><span class="sxs-lookup"><span data-stu-id="70750-126">Click **View Report** to display the selected report.</span></span>

    <span data-ttu-id="70750-127">Les résultats peuvent être enregistrés dans différents formats, tels que HTML, Microsoft Word et Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="70750-127">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="70750-128">**Remarques**  Le rapport de conformité d’entreprise est généré par un travail SQL qui s’exécute toutes les six heures.</span><span class="sxs-lookup"><span data-stu-id="70750-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="70750-129">Par conséquent, lorsque vous affichez le rapport pour la première fois, il est possible que certaines données soient manquantes.</span><span class="sxs-lookup"><span data-stu-id="70750-129">Therefore, the first time you view the report, you may find that some data is missing.</span></span> <span data-ttu-id="70750-130">Vous pouvez générer manuellement des données de rapport mises à jour à l’aide de SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="70750-130">You can generate updated report data manually by using SQL Management Studio.</span></span> <span data-ttu-id="70750-131">Dans la fenêtre **Explorateur d’objets** , développez l' **agent SQL Server**, développez **travaux**, cliquez avec le bouton droit sur le travail **CreateCache** , puis sélectionnez **Démarrer la tâche à l’étape....**</span><span class="sxs-lookup"><span data-stu-id="70750-131">From the **Object Explorer** window, expand **SQL Server Agent**, expand **Jobs**, right-click the **CreateCache** job, and select **Start Job at Step….**</span></span>

     

3.  <span data-ttu-id="70750-132">Sélectionnez le nom d’un ordinateur pour afficher des informations relatives à l’ordinateur figurant dans le rapport de compatibilité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="70750-132">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="70750-133">Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="70750-133">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="70750-134">Pour générer le rapport de conformité de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="70750-134">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="70750-135">Sur le site Web d’administration et de surveillance, sélectionnez le nœud de **rapport** dans le volet de navigation gauche, puis sélectionnez le **rapport de conformité**de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="70750-135">In the Administration and Monitoring website, select the **Report** node from the left navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="70750-136">Utilisez le rapport de conformité de l’ordinateur pour rechercher le **nom d’utilisateur** ou le nom de l' **ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="70750-136">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="70750-137">Cliquez sur **afficher le rapport** pour afficher le rapport sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="70750-137">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="70750-138">Les résultats peuvent être enregistrés dans différents formats, tels que HTML, Microsoft Word et Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="70750-138">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="70750-139">Sélectionnez le nom d’un ordinateur pour afficher des informations supplémentaires sur celui-ci dans le rapport de compatibilité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="70750-139">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="70750-140">Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="70750-140">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="70750-141">**Remarques**  Un ordinateur client MBAM est considéré comme conforme si l’ordinateur répond aux exigences des paramètres de stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="70750-141">**Note** An MBAM client computer is considered compliant if the computer matches the requirements of the MBAM policy settings.</span></span>

     

**<span data-ttu-id="70750-142">Pour générer le rapport d’audit de clé de récupération</span><span class="sxs-lookup"><span data-stu-id="70750-142">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="70750-143">Sur le site Web d’administration et de surveillance, sélectionnez le nœud de **rapport** dans le volet de navigation gauche, puis sélectionnez le **rapport d’audit de récupération**.</span><span class="sxs-lookup"><span data-stu-id="70750-143">From the Administration and Monitoring website, select the **Report** node in the left navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="70750-144">Sélectionnez les filtres du rapport d’audit de la clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="70750-144">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="70750-145">Les filtres disponibles pour les audits de clé de récupération sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="70750-145">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="70750-146">**Demandeur**.</span><span class="sxs-lookup"><span data-stu-id="70750-146">**Requestor**.</span></span> <span data-ttu-id="70750-147">Ce filtre permet aux utilisateurs de spécifier le nom d’utilisateur du demandeur.</span><span class="sxs-lookup"><span data-stu-id="70750-147">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="70750-148">Le demandeur est la personne du support technique qui a accédé à la clé pour le compte d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="70750-148">The requester is the person in the Help Desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="70750-149">**Demandeur**.</span><span class="sxs-lookup"><span data-stu-id="70750-149">**Requestee**.</span></span> <span data-ttu-id="70750-150">Ce filtre permet aux utilisateurs de spécifier le nom d’utilisateur de la requête.</span><span class="sxs-lookup"><span data-stu-id="70750-150">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="70750-151">La personne qui a appelé le support technique peut obtenir une clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="70750-151">The requestee is the person who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="70750-152">**Résultat**de la requête.</span><span class="sxs-lookup"><span data-stu-id="70750-152">**Request Result**.</span></span> <span data-ttu-id="70750-153">Ce filtre permet aux utilisateurs de spécifier les types de résultats de requête (par exemple, succès ou échec) sur lesquels ils veulent baser le rapport.</span><span class="sxs-lookup"><span data-stu-id="70750-153">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="70750-154">Par exemple, les utilisateurs peuvent souhaiter afficher les tentatives d’accès par clé en échec.</span><span class="sxs-lookup"><span data-stu-id="70750-154">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="70750-155">**Type de clé**.</span><span class="sxs-lookup"><span data-stu-id="70750-155">**Key Type**.</span></span> <span data-ttu-id="70750-156">Ce filtre permet aux utilisateurs de spécifier le type de clé (par exemple: mot de passe pour la clé de récupération ou hachage du mot de passe TPM) sur lequel il souhaite baser le rapport.</span><span class="sxs-lookup"><span data-stu-id="70750-156">This filter enables users to specify the Key Type (for example: Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="70750-157">**Date de début**.</span><span class="sxs-lookup"><span data-stu-id="70750-157">**Start Date**.</span></span> <span data-ttu-id="70750-158">Ce filtre permet de définir la partie Date de début de la plage de dates à laquelle l’utilisateur souhaite rapporter.</span><span class="sxs-lookup"><span data-stu-id="70750-158">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="70750-159">**Date de fin**.</span><span class="sxs-lookup"><span data-stu-id="70750-159">**End Date**.</span></span> <span data-ttu-id="70750-160">Ce filtre est utilisé pour définir la partie de la date de fin de la plage de dates à laquelle les utilisateurs veulent rapporter.</span><span class="sxs-lookup"><span data-stu-id="70750-160">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="70750-161">Cliquez sur **afficher le rapport** pour afficher le rapport.</span><span class="sxs-lookup"><span data-stu-id="70750-161">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="70750-162">Les résultats peuvent être enregistrés dans différents formats, tels que HTML, Microsoft Word et Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="70750-162">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="70750-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="70750-163">Related topics</span></span>


[<span data-ttu-id="70750-164">Surveillance et création de rapports de la conformité BitLocker avec MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="70750-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 






---
title: À propos de MBAM2.0 SP1
description: À propos de MBAM2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810025"
---
# <span data-ttu-id="646cb-103">À propos de MBAM2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="646cb-103">About MBAM 2.0 SP1</span></span>

<span data-ttu-id="646cb-104">Cette rubrique décrit les modifications apportées à l’administration et à l’analyse de BitLocker (MBAM) 2,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="646cb-104">This topic describes the changes in Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="646cb-105">Pour obtenir une description générale de MBAM, reportez-vous à la rubrique [mise en route de MBAM 2,0](getting-started-with-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="646cb-105">For a general description of MBAM, see [Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md).</span></span>

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a><span data-ttu-id="646cb-106">Nouveautés de MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="646cb-106">What’s new in MBAM 2.0 SP1</span></span>

<span data-ttu-id="646cb-107">Cette version de MBAM offre les nouvelles fonctionnalités et fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="646cb-107">This version of MBAM provides the following new features and functionality.</span></span>

### <span data-ttu-id="646cb-108">Prise en charge de Windows 8,1, Windows Server 2012 R2 et System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="646cb-108">Support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager</span></span>

<span data-ttu-id="646cb-109">Microsoft BitLocker administration et analyse (MBAM) 2,0 Service Pack 1 (SP1) ajoute la prise en charge pour Windows 8,1, Windows Server 2012 R2 et System Center 2012 R2 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="646cb-109">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager.</span></span>

### <span data-ttu-id="646cb-110">Prise en charge de Microsoft SQL Server 2008 R2 SP2</span><span class="sxs-lookup"><span data-stu-id="646cb-110">Support for Microsoft SQL Server 2008 R2 SP2</span></span>

<span data-ttu-id="646cb-111">Microsoft BitLocker administration et analyse (MBAM) 2,0 Service Pack 1 (SP1) ajoute la prise en charge de Microsoft SQL Server 2008 R2 SP2.</span><span class="sxs-lookup"><span data-stu-id="646cb-111">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Microsoft SQL Server 2008 R2 SP2.</span></span> <span data-ttu-id="646cb-112">Vous devez utiliser Microsoft SQL Server 2008 R2 ou une version ultérieure si vous exécutez Microsoft System Center Configuration Manager 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="646cb-112">You must use Microsoft SQL Server 2008 R2 or higher if you are running Microsoft System Center Configuration Manager 2007 R2.</span></span>

### <span data-ttu-id="646cb-113">Report de commentaires client</span><span class="sxs-lookup"><span data-stu-id="646cb-113">Customer feedback rollup</span></span>

<span data-ttu-id="646cb-114">MBAM 2,0 SP1 inclut un ensemble de correctifs pour résoudre les problèmes détectés depuis la version d’administration et de surveillance de Microsoft BitLocker (MBAM) 2,0.</span><span class="sxs-lookup"><span data-stu-id="646cb-114">MBAM 2.0 SP1 includes a rollup of fixes to address issues that were found since the Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 release.</span></span> <span data-ttu-id="646cb-115">Dans le cadre de ces modifications, le champ nom de l’ordinateur apparaît désormais dans les rapports sur les détails de conformité de l’ordinateur et BitLocker Enterprise lors de l’exécution de MBAM avec Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="646cb-115">As part of these changes, the Computer Name field now appears in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007.</span></span>

### <span data-ttu-id="646cb-116">Une exception de pare-feu doit être définie sur les ports du portail libre-service et sur le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="646cb-116">Firewall exception must be set on ports for the Self-Service Portal and the Administration and Monitoring website</span></span>

<span data-ttu-id="646cb-117">Lorsque vous configurez le portail libre-service et le site Web d’administration et de surveillance, vous devez définir une exception de pare-feu pour autoriser les communications via les ports spécifiés.</span><span class="sxs-lookup"><span data-stu-id="646cb-117">When you configure the Self-Service Portal and the Administration and Monitoring website, you must set a firewall exception to enable communication through the specified ports.</span></span> <span data-ttu-id="646cb-118">Auparavant, l’installation MBAM Server a ouvert les ports automatiquement dans le pare-feu Windows.</span><span class="sxs-lookup"><span data-stu-id="646cb-118">Previously, the MBAM server installation opened the ports automatically in Windows Firewall.</span></span>

### <span data-ttu-id="646cb-119">L’emplacement des rapports MBAM a changé dans Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="646cb-119">Location of MBAM reports has changed in Configuration Manager</span></span>

<span data-ttu-id="646cb-120">MBAM-XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX MBAM.</span><span class="sxs-lookup"><span data-stu-id="646cb-120">MBAM reports for the Configuration Manager integrated topology are now available under subfolders within the MBAM node.</span></span> <span data-ttu-id="646cb-121">Les noms de sous-dossiers représentent la langue des rapports dans le sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="646cb-121">The subfolder names represent the language of the reports within the subfolder.</span></span>

### <span data-ttu-id="646cb-122">Possibilité d’installer MBAM sur un serveur de site principal lors de l’installation d’MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="646cb-122">Ability to install MBAM on a primary site server when you install MBAM with Configuration Manager</span></span>

<span data-ttu-id="646cb-123">Vous pouvez installer MBAM sur un serveur de site principal ou un serveur de site d’administration centrale lorsque vous installez MBAM avec la topologie intégrée de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="646cb-123">You can install MBAM on a primary site server or a central administration site server when you install MBAM with the Configuration Manager integrated topology.</span></span> <span data-ttu-id="646cb-124">Auparavant, vous étiez obligé d’installer MBAM sur un serveur de site d’administration centrale.</span><span class="sxs-lookup"><span data-stu-id="646cb-124">Previously, you were required to install MBAM on a central administration site server.</span></span>

**<span data-ttu-id="646cb-125">Important</span><span class="sxs-lookup"><span data-stu-id="646cb-125">Important</span></span>**  
<span data-ttu-id="646cb-126">Le serveur sur lequel vous installez MBAM doit être le serveur de niveau supérieur de votre hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="646cb-126">The server on which you install MBAM must be the top-tier server in your hierarchy.</span></span>



<span data-ttu-id="646cb-127">L’installation de MBAM fonctionne différemment pour Microsoft System Center Configuration Manager 2007 et Microsoft System Center 2012 Configuration Manager comme suit:</span><span class="sxs-lookup"><span data-stu-id="646cb-127">The MBAM installation works differently for Microsoft System Center Configuration Manager 2007 and Microsoft System Center 2012 Configuration Manager as follows:</span></span>

-   <span data-ttu-id="646cb-128">**Configuration manager 2007** : Si vous installez MBAM sur un serveur de site principal qui fait partie d’une hiérarchie de gestionnaires de configuration plus volumineux et possède un serveur parent de site central, MBAM résout le serveur parent du site central et effectue toutes les actions d’installation sur ce serveur parent.</span><span class="sxs-lookup"><span data-stu-id="646cb-128">**Configuration Manager 2007** : If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy and has a central site parent server, MBAM resolves the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="646cb-129">Les actions d’installation incluent la vérification des éléments requis et l’installation des objets et des rapports du gestionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="646cb-129">The installation actions include checking prerequisites and installing the Configuration Manager objects and reports.</span></span> <span data-ttu-id="646cb-130">Par exemple, si vous installez MBAM sur un serveur de site principal qui est un enfant d’un serveur parent de site central, MBAM installe tous les objets et rapports de configuration du serveur parent.</span><span class="sxs-lookup"><span data-stu-id="646cb-130">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="646cb-131">Si vous installez MBAM sur le serveur parent, MBAM effectue toutes les actions d’installation sur ce serveur parent.</span><span class="sxs-lookup"><span data-stu-id="646cb-131">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span>

-   <span data-ttu-id="646cb-132">**Gestionnaire de configuration de System Center 2012** : Si vous installez MBAM sur un serveur de site principal ou sur un serveur d’administration centrale, MBAM effectue toutes les actions d’installation sur ce serveur de site.</span><span class="sxs-lookup"><span data-stu-id="646cb-132">**System Center 2012 Configuration Manager** : If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span>

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> <span data-ttu-id="646cb-133">La console Configuration Manager doit être installée sur l’ordinateur sur lequel vous installez le serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="646cb-133">Configuration Manager Console must be installed on the computer on which you install the MBAM Server</span></span>

<span data-ttu-id="646cb-134">Lorsque vous installez MBAM avec la topologie intégrée de Configuration Manager, vous devez installer la console Configuration Manager sur le même ordinateur sur lequel MBAM sera installé.</span><span class="sxs-lookup"><span data-stu-id="646cb-134">When you install MBAM with the Configuration Manager integrated topology, you must install the Configuration Manager Console on the same computer on which MBAM will be installed.</span></span> <span data-ttu-id="646cb-135">Si vous utilisez l’architecture recommandée, décrite dans la rubrique [mise en route-utilisez MBAM avec Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), vous devez installer MBAM sur le serveur de site principal de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="646cb-135">If you use the recommended architecture, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), you would install MBAM on the Configuration Manager Primary Site Server.</span></span>

### <span data-ttu-id="646cb-136">Nouveaux paramètres de ligne de commande du programme d’installation pour la topologie intégrée de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="646cb-136">New setup command-line parameters for the Configuration Manager integrated topology</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="646cb-137">Paramètre de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="646cb-137">Command-Line Parameter</span></span></th>
<th align="left"><span data-ttu-id="646cb-138">Description</span><span class="sxs-lookup"><span data-stu-id="646cb-138">Description</span></span></th>
<th align="left"><span data-ttu-id="646cb-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="646cb-139">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="646cb-140">CM_SSRS_REMOTE_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="646cb-140">CM_SSRS_REMOTE_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="646cb-141">Vous permet d’installer les rapports du gestionnaire de configuration sur un serveur SQL Server Reporting Services (SSRS) distant qui fait partie du site de Configuration Manager sur lequel MBAM est installé.</span><span class="sxs-lookup"><span data-stu-id="646cb-141">Enables you to install the Configuration Manager reports on a remote SQL Server Reporting Services (SSRS) server that is part of the same Configuration Manager site to which MBAM is installed.</span></span> <span data-ttu-id="646cb-142">Vous pouvez définir la valeur sur le nom de domaine complet du serveur de rôles de point SSRS distant.</span><span class="sxs-lookup"><span data-stu-id="646cb-142">You can set the value to the fully qualified domain name of the remote SSRS point role server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="646cb-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</span><span class="sxs-lookup"><span data-stu-id="646cb-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME=ssrsServer.Contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="646cb-144">CM_REPORTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="646cb-144">CM_REPORTS_ONLY</span></span></p></td>
<td align="left"><p><span data-ttu-id="646cb-145">Vous permet d’installer uniquement les rapports du gestionnaire de configuration, sans autres objets de Configuration Manager, tels que les éléments de base, de collection et de configuration.</span><span class="sxs-lookup"><span data-stu-id="646cb-145">Enables you to install only the Configuration Manager reports, without other Configuration Manager objects, such as the baseline, collection, and configuration items.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="646cb-146">Remarque</span><span class="sxs-lookup"><span data-stu-id="646cb-146">Note</span></span></strong><br/><p><span data-ttu-id="646cb-147">Vous devez combiner ce paramètre avec le paramètre CM_REPORTS_COLLECTION_ID.</span><span class="sxs-lookup"><span data-stu-id="646cb-147">You must combine this parameter with the CM_REPORTS_COLLECTION_ID parameter.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="646cb-148">Valeurs de paramètre valides:</span><span class="sxs-lookup"><span data-stu-id="646cb-148">Valid parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="646cb-149">Vrai</span><span class="sxs-lookup"><span data-stu-id="646cb-149">True</span></span></p></li>
<li><p><span data-ttu-id="646cb-150">Faux</span><span class="sxs-lookup"><span data-stu-id="646cb-150">False</span></span></p></li>
</ul>
<p><span data-ttu-id="646cb-151">Vous pouvez combiner ce paramètre à l’aide du paramètre CM_SSRS_REMOTE_SERVER_NAME si vous voulez installer les rapports uniquement sur un serveur de rôles de point de contrôle distant.</span><span class="sxs-lookup"><span data-stu-id="646cb-151">You can combine this parameter with the CM_SSRS_REMOTE_SERVER_NAME parameter if you want to install the reports only to a remote SSRS point role server.</span></span></p>
<p><span data-ttu-id="646cb-152">Si vous ne définissez pas le paramètre ou si vous lui attribuez la valeur false, le programme d’installation de MBAM installe tous les objets du gestionnaire de configuration, y compris les rapports.</span><span class="sxs-lookup"><span data-stu-id="646cb-152">If you do not set the parameter or if you set it to False, MBAM Setup installs all of the Configuration Manager objects, including the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="646cb-153">MbamSetup.exe CM_REPORTS_ONLY = true</span><span class="sxs-lookup"><span data-stu-id="646cb-153">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="646cb-154">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="646cb-154">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="646cb-155">CM_REPORTS_COLLECTION_ID</span><span class="sxs-lookup"><span data-stu-id="646cb-155">CM_REPORTS_COLLECTION_ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="646cb-156">ID de collection existant qui identifie la collection pour laquelle les données de conformité de rapport seront affichées.</span><span class="sxs-lookup"><span data-stu-id="646cb-156">An existing collection ID that identifies the collection for which reporting compliance data will be displayed.</span></span> <span data-ttu-id="646cb-157">Vous pouvez spécifier n’importe quel ID de collection.</span><span class="sxs-lookup"><span data-stu-id="646cb-157">You can specify any collection ID.</span></span> <span data-ttu-id="646cb-158">Vous n’êtes pas tenu d’utiliser l’ID de collection «MBAM pris en charge».</span><span class="sxs-lookup"><span data-stu-id="646cb-158">You are not required to use the “MBAM Supported Computers” collection ID.</span></span></p></td>
<td align="left"><p><span data-ttu-id="646cb-159">MbamSetup.exe CM_REPORTS_ONLY = true</span><span class="sxs-lookup"><span data-stu-id="646cb-159">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="646cb-160">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="646cb-160">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="646cb-161">Possibilité d’activer ou de désactiver le texte d’avis de portail libre-service</span><span class="sxs-lookup"><span data-stu-id="646cb-161">Ability to turn Self-Service Portal notice text on or off</span></span>

<span data-ttu-id="646cb-162">MBAM 2,0 SP1 vous permet de désactiver le texte de la note sur le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="646cb-162">MBAM 2.0 SP1 enables you to turn off the notice text on the Self-Service Portal.</span></span> <span data-ttu-id="646cb-163">Auparavant, le texte d’avis affiché par défaut, et vous ne pouviez pas le désactiver.</span><span class="sxs-lookup"><span data-stu-id="646cb-163">Previously, the notice text displayed by default, and you could not turn it off.</span></span>

**<span data-ttu-id="646cb-164">Pour désactiver le texte de la note</span><span class="sxs-lookup"><span data-stu-id="646cb-164">To turn off the notice text</span></span>**

1.  <span data-ttu-id="646cb-165">Sur le serveur sur lequel vous avez installé le portail libre-service, ouvrez Internet Information Services (IIS) et naviguez jusqu’à **sites &gt; Microsoft BitLocker administration et analysez les paramètres de l' &gt; &gt; application selfservice**.</span><span class="sxs-lookup"><span data-stu-id="646cb-165">On the server where you installed the Self-Service Portal, open Internet Information Services (IIS) and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="646cb-166">Dans la colonne **nom** , sélectionnez **DisplayNotice**, puis attribuez la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="646cb-166">From the **Name** column, select **DisplayNotice**, and set the value to **false**.</span></span>

### <span data-ttu-id="646cb-167">Possibilité de localiser l’instruction HelpdeskText qui pointe les utilisateurs vers d’autres informations de portail libre-service</span><span class="sxs-lookup"><span data-stu-id="646cb-167">Ability to localize the HelpdeskText statement that points users to more Self-Service Portal information</span></span>

<span data-ttu-id="646cb-168">Vous pouvez configurer une version localisée de l’instruction «HelpdeskText» du portail libre-service, qui indique aux utilisateurs finaux comment obtenir de l’aide sur le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="646cb-168">You can configure a localized version of the Self-Service Portal “HelpdeskText” statement, which tells end users how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="646cb-169">Si vous configurez du texte localisé pour l’instruction, comme décrit dans les instructions ci-dessous, MBAM affiche la version localisée.</span><span class="sxs-lookup"><span data-stu-id="646cb-169">If you configure localized text for the statement, as described in the following instructions, MBAM will display the localized version.</span></span> <span data-ttu-id="646cb-170">Si MBAM ne trouve pas la version localisée, il affiche la valeur figurant dans le paramètre **HelpdeskText** .</span><span class="sxs-lookup"><span data-stu-id="646cb-170">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

**<span data-ttu-id="646cb-171">Pour afficher une version localisée de l’instruction HelpdeskText</span><span class="sxs-lookup"><span data-stu-id="646cb-171">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="646cb-172">Sur le serveur sur lequel vous avez installé le portail libre-service, ouvrez les services Internet (IIS) et naviguez jusqu’à **sites &gt; Microsoft BitLocker administration et contrôle des paramètres de l' &gt; &gt; application selfservice**.</span><span class="sxs-lookup"><span data-stu-id="646cb-172">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="646cb-173">Dans le volet **actions** , cliquez sur **Ajouter** pour ouvrir la boîte de dialogue Ajouter un **paramètre d’application** .</span><span class="sxs-lookup"><span data-stu-id="646cb-173">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="646cb-174">Dans le champ **nom** , tapez **HelpdeskText**\ _ &lt; *Language* &gt; , où &lt; *Language* &gt; correspond au code de langue approprié pour le texte.</span><span class="sxs-lookup"><span data-stu-id="646cb-174">In the **Name** field, type **HelpdeskText**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the text.</span></span> <span data-ttu-id="646cb-175">Par exemple, pour créer une instruction HelpdeskText localisée en espagnol, vous nommerez le paramètre HelpdeskText \ _es-es.</span><span class="sxs-lookup"><span data-stu-id="646cb-175">For example, to create a localized HelpdeskText statement in Spanish, you would name the parameter HelpdeskText\_es-es.</span></span> <span data-ttu-id="646cb-176">Pour obtenir la liste des codes de langue valides que vous pouvez utiliser, voir référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="646cb-176">For a list of the valid language codes that you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="646cb-177">Dans le champ **valeur** , tapez le texte localisé que vous souhaitez afficher aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="646cb-177">In the **Value** field, type the localized text that you want to display to end users.</span></span>

### <span data-ttu-id="646cb-178">Possibilité de localiser le portail libre-service HelpdeskURL</span><span class="sxs-lookup"><span data-stu-id="646cb-178">Ability to localize the Self-Service Portal HelpdeskURL</span></span>

<span data-ttu-id="646cb-179">Vous pouvez configurer une version localisée du portail libre-service HelpdeskURL pour l’afficher par défaut aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="646cb-179">You can configure a localized version of the Self-Service Portal HelpdeskURL to display to end users by default.</span></span> <span data-ttu-id="646cb-180">Si vous créez une version localisée, comme décrit dans les instructions ci-dessous, MBAM recherche et affiche la version localisée.</span><span class="sxs-lookup"><span data-stu-id="646cb-180">If you create a localized version, as described in the following instructions, MBAM finds and displays the localized version.</span></span> <span data-ttu-id="646cb-181">Si MBAM ne trouve pas de version localisée, il affiche l’URL configurée pour le paramètre HelpDeskURL.</span><span class="sxs-lookup"><span data-stu-id="646cb-181">If MBAM does not find a localized version, it displays the URL that is configured for the HelpDeskURL parameter.</span></span>

**<span data-ttu-id="646cb-182">Pour afficher un HelpdeskURL localisé</span><span class="sxs-lookup"><span data-stu-id="646cb-182">To display a localized HelpdeskURL</span></span>**

1.  <span data-ttu-id="646cb-183">Sur le serveur sur lequel vous avez installé le portail libre-service, ouvrez les services Internet (IIS) et naviguez jusqu’à **sites &gt; Microsoft BitLocker administration et contrôle des paramètres de l' &gt; &gt; application selfservice**.</span><span class="sxs-lookup"><span data-stu-id="646cb-183">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="646cb-184">Dans le volet **actions** , cliquez sur **Ajouter** pour ouvrir la boîte de dialogue Ajouter un **paramètre d’application** .</span><span class="sxs-lookup"><span data-stu-id="646cb-184">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="646cb-185">Dans le champ **nom** , tapez **HelpdeskURL**\ _ &lt; *Language* &gt; , où &lt; *Language* &gt; correspond au code de langue approprié pour l’URL.</span><span class="sxs-lookup"><span data-stu-id="646cb-185">In the **Name** field, type **HelpdeskURL**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the URL.</span></span> <span data-ttu-id="646cb-186">Par exemple, pour créer une HelpdeskURL localisée en espagnol, vous nommerez le paramètre HelpdeskURL \ _es-es.</span><span class="sxs-lookup"><span data-stu-id="646cb-186">For example, to create a localized HelpdeskURL in Spanish, you would name the parameter HelpdeskURL\_es-es.</span></span> <span data-ttu-id="646cb-187">Pour obtenir la liste des codes de langue valides que vous pouvez utiliser, voir référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="646cb-187">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="646cb-188">Dans le champ **valeur** , tapez le HelpdeskURL localisé que vous souhaitez afficher aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="646cb-188">In the **Value** field, type the localized HelpdeskURL that you want to display to end users.</span></span>

### <span data-ttu-id="646cb-189">Possibilité de localiser le texte d’avis du portail libre-service</span><span class="sxs-lookup"><span data-stu-id="646cb-189">Ability to localize the Self-Service Portal notice text</span></span>

<span data-ttu-id="646cb-190">Vous pouvez configurer le texte des notifications localisées pour qu’ils apparaissent par défaut aux utilisateurs finaux sur le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="646cb-190">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="646cb-191">Le fichier notice.txt, qui affiche le texte de l’avis, se trouve dans le répertoire racine suivant:</span><span class="sxs-lookup"><span data-stu-id="646cb-191">The notice.txt file, which displays the notice text, is located in the following root directory:</span></span>

<span data-ttu-id="646cb-192">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website</span><span class="sxs-lookup"><span data-stu-id="646cb-192">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="646cb-193">Pour afficher un texte d’avis localisé, vous devez créer un fichier notice.txt localisé et l’enregistrer sous un dossier de langue spécifique dans l’annuaire suivant:</span><span class="sxs-lookup"><span data-stu-id="646cb-193">To display localized notice text, you create a localized notice.txt file and save it under a specific language folder in the following directory:</span></span>

<span data-ttu-id="646cb-194">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website</span><span class="sxs-lookup"><span data-stu-id="646cb-194">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="646cb-195">MBAM affiche le texte de l’avis en fonction des règles suivantes:</span><span class="sxs-lookup"><span data-stu-id="646cb-195">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="646cb-196">Si vous créez un fichier notice.txt localisé dans le dossier de langue approprié, MBAM affiche le texte du message localisé.</span><span class="sxs-lookup"><span data-stu-id="646cb-196">If you create a localized notice.txt file in the appropriate language folder, MBAM displays the localized notice text.</span></span>

-   <span data-ttu-id="646cb-197">Si MBAM ne trouve pas de version localisée du fichier notice.txt, il affiche le texte dans le fichier de notice.txt par défaut.</span><span class="sxs-lookup"><span data-stu-id="646cb-197">If MBAM does not find a localized version of the notice.txt file, it displays the text in the default notice.txt file.</span></span>

-   <span data-ttu-id="646cb-198">Si MBAM ne trouve pas de fichier notice.txt par défaut, il affiche le texte par défaut dans le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="646cb-198">If MBAM does not find a default notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

**<span data-ttu-id="646cb-199">Remarque</span><span class="sxs-lookup"><span data-stu-id="646cb-199">Note</span></span>**  
<span data-ttu-id="646cb-200">Si le navigateur d’un utilisateur final est défini pour une langue qui ne possède pas de sous-dossier de langue correspondant ou notice.txt, le texte qui se trouve dans le fichier notice.txt dans le répertoire racine suivant s’affiche:</span><span class="sxs-lookup"><span data-stu-id="646cb-200">If an end user’s browser is set to a language that does not have a corresponding language subfolder or notice.txt, the text that is in the notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="646cb-201">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website</span><span class="sxs-lookup"><span data-stu-id="646cb-201">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\



**<span data-ttu-id="646cb-202">Pour créer un fichier notice.txt localisé</span><span class="sxs-lookup"><span data-stu-id="646cb-202">To create a localized notice.txt file</span></span>**

1.  <span data-ttu-id="646cb-203">Sur le serveur sur lequel vous avez installé le portail libre-service, créez un &lt; *language* &gt; dossier de langue dans l’annuaire suivant, où &lt; *Language* &gt; représente le nom de la langue localisée:</span><span class="sxs-lookup"><span data-stu-id="646cb-203">On the server where you installed the Self-Service Portal, create a &lt;*language*&gt; folder in the following directory, where &lt;*language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="646cb-204">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website</span><span class="sxs-lookup"><span data-stu-id="646cb-204">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

    **<span data-ttu-id="646cb-205">Remarque</span><span class="sxs-lookup"><span data-stu-id="646cb-205">Note</span></span>**  
    <span data-ttu-id="646cb-206">Certains dossiers de langue existent déjà et il n’est pas nécessaire d’en créer un.</span><span class="sxs-lookup"><span data-stu-id="646cb-206">Some language folders already exist, so you may not have to create one.</span></span> <span data-ttu-id="646cb-207">Si vous avez besoin de créer un dossier de langue, reportez-vous à la rubrique référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947) pour obtenir la liste des noms valides que vous pouvez utiliser pour le &lt; dossier *Language* &gt; .</span><span class="sxs-lookup"><span data-stu-id="646cb-207">If you do need to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*language*&gt; folder.</span></span>



2.  <span data-ttu-id="646cb-208">Créez un fichier notice.txt contenant le texte d’avis localisé.</span><span class="sxs-lookup"><span data-stu-id="646cb-208">Create a notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="646cb-209">Enregistrez le fichier notice.txt dans le &lt; dossier *Language* &gt; .</span><span class="sxs-lookup"><span data-stu-id="646cb-209">Save the notice.txt file in the &lt;*language*&gt; folder.</span></span> <span data-ttu-id="646cb-210">Par exemple, pour créer un fichier notice.txt localisé en espagnol, vous devez enregistrer le fichier notice.txt localisé dans le dossier suivant:</span><span class="sxs-lookup"><span data-stu-id="646cb-210">For example, to create a localized notice.txt file in Spanish, you would save the localized notice.txt file in the following folder:</span></span>

    <span data-ttu-id="646cb-211">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\es-es</span><span class="sxs-lookup"><span data-stu-id="646cb-211">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\es-es</span></span>

## <span data-ttu-id="646cb-212">Mise à niveau vers MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="646cb-212">Upgrading to MBAM 2.0 SP1</span></span>


<span data-ttu-id="646cb-213">Vous pouvez effectuer une mise à niveau vers MBAM 2,0 SP1 à partir de n’importe quelle version antérieure de MBAM.</span><span class="sxs-lookup"><span data-stu-id="646cb-213">You can upgrade to MBAM 2.0 SP1 from any previous version of MBAM.</span></span>

### <span data-ttu-id="646cb-214">Mise à niveau de l’infrastructure MBAM</span><span class="sxs-lookup"><span data-stu-id="646cb-214">Upgrading the MBAM infrastructure</span></span>

<span data-ttu-id="646cb-215">Vous pouvez mettre à niveau l’infrastructure du serveur MBAM vers MBAM 2,0 SP1 comme suit:</span><span class="sxs-lookup"><span data-stu-id="646cb-215">You can upgrade the MBAM Server infrastructure to MBAM 2.0 SP1 as follows:</span></span>

<span data-ttu-id="646cb-216">**Remplacement manuel du serveur sur place**: vous devez désinstaller manuellement l’infrastructure du serveur MBAM existante, puis installer l’infrastructure du serveur MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="646cb-216">**Manual in-place server replacement**: You must manually uninstall the existing MBAM Server infrastructure, and then install the MBAM 2.0 SP1 Server infrastructure.</span></span> <span data-ttu-id="646cb-217">Vous n’avez pas besoin de supprimer les bases de données pour procéder à la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="646cb-217">You do not have to remove the databases to do the upgrade.</span></span> <span data-ttu-id="646cb-218">Au lieu de cela, vous sélectionnez les bases de données existantes, lesquelles la version précédente de MBAM a été créée.</span><span class="sxs-lookup"><span data-stu-id="646cb-218">Instead, you select the existing databases, which the previous version of MBAM created.</span></span> <span data-ttu-id="646cb-219">Le programme d’installation de la mise à niveau MBAM 2,0 SP1 effectue une migration vers MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="646cb-219">The MBAM 2.0 SP1 upgrade installation then migrates the existing databases to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="646cb-220">**Mise à niveau du client distribué**: Si vous utilisez la topologie MBAM autonome, vous pouvez mettre à niveau les clients MBAM progressivement après l’installation de l’infrastructure de serveur MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="646cb-220">**Distributed client upgrade**: If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 SP1 Server infrastructure.</span></span>

<span data-ttu-id="646cb-221">Après avoir effectué la mise à niveau de l’infrastructure du serveur MBAM, les clients MBAM 1,0 ou 2,0 seront signalés au serveur MBAM 2,0 SP1 et stockeront les données de récupération, mais la conformité sera basée sur les stratégies disponibles pour la version du client MBAM actuellement installée.</span><span class="sxs-lookup"><span data-stu-id="646cb-221">After you upgrade the MBAM Server infrastructure, MBAM 1.0 or 2.0 Clients will report to the MBAM 2.0 SP1 Server successfully and will store the recovery data, but compliance will be based on the policies available for the MBAM Client version that is currently installed.</span></span> <span data-ttu-id="646cb-222">Pour activer la création de rapports sur les stratégies MBAM 2,0 SP1, vous devez mettre à niveau les ordinateurs clients vers MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="646cb-222">To enable reporting against MBAM 2.0 SP1 policies, you must upgrade client computers to MBAM 2.0 SP1.</span></span> <span data-ttu-id="646cb-223">Vous pouvez mettre à niveau les ordinateurs client vers le client MBAM 2,0 SP1 sans désinstaller le client précédent, et le client va commencer à s’appliquer et à signaler, selon les stratégies 2,0 SP1 MBAM.</span><span class="sxs-lookup"><span data-stu-id="646cb-223">You can upgrade the client computers to the MBAM 2.0 SP1 Client without uninstalling the previous Client, and the Client will start to apply and report, based on the MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="646cb-224">Pour plus d’informations sur la mise à niveau des serveurs MBAM, voir [mise à niveau à partir d’une version antérieure d’MBAM](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="646cb-224">For more information about upgrading the MBAM servers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

### <span data-ttu-id="646cb-225">Mise à niveau du client MBAM vers MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="646cb-225">Upgrading the MBAM Client to MBAM 2.0 SP1</span></span>

<span data-ttu-id="646cb-226">Pour mettre à niveau les ordinateurs des utilisateurs finaux vers le client MBAM 2,0 SP1, exécutez **MbamClientSetup.exe** sur chaque ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="646cb-226">To upgrade end-user computers to the MBAM 2.0 SP1 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="646cb-227">Le programme d’installation met automatiquement à jour le client vers le client MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="646cb-227">The installer automatically updates the Client to the MBAM 2.0 SP1 Client.</span></span> <span data-ttu-id="646cb-228">Après l’installation, les ordinateurs clients n’ont pas besoin d’être redémarrés et le client MBAM 2,0 SP1 commence à s’appliquer et à rapporter des stratégies MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="646cb-228">After the installation, client computers do not have to be rebooted, and the MBAM 2.0 SP1 Client starts to apply and report against MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="646cb-229">Si vous utilisez MBAM avec Configuration Manager, vous devez mettre à niveau les ordinateurs client MBAM vers MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="646cb-229">If you are using MBAM with Configuration Manager, you must upgrade the MBAM client computers to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="646cb-230">Pour plus d’informations sur la mise à niveau des ordinateurs clients MBAM, voir [mise à niveau à partir d’une version antérieure d’MBAM](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="646cb-230">For more information about upgrading the MBAM client computers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

## <span data-ttu-id="646cb-231">Installation ou mise à niveau vers MBAM 2,0 SP1 avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="646cb-231">Installing or upgrading to MBAM 2.0 SP1 with Configuration Manager</span></span>


<span data-ttu-id="646cb-232">Cette section décrit la configuration requise lors de l’installation d’MBAM 2,0 SP1 en tant que nouvelle installation ou en tant que mise à niveau vers une version antérieure de MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="646cb-232">This section describes the requirements when you are installing MBAM 2.0 SP1 as a new installation or as an upgrade to a previous MBAM 2.0 SP1 installation.</span></span>

### <span data-ttu-id="646cb-233">Fichiers nécessaires pour l’installation d’MBAM 2,0 SP1 si vous utilisez MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="646cb-233">Required files for installing MBAM 2.0 SP1 if you are using MBAM with Configuration Manager</span></span>

<span data-ttu-id="646cb-234">Si vous installez MBAM pour la première fois et que vous utilisez MBAM 2,0 SP1 avec System Center Configuration Manager, vous devez créer ou modifier des fichiers MOF pour permettre à MBAM de fonctionner correctement avec Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="646cb-234">If you are installing MBAM for the first time and you are using MBAM 2.0 SP1 with System Center Configuration Manager, you must create or edit mof files to enable MBAM to work correctly with Configuration Manager.</span></span>

-   **<span data-ttu-id="646cb-235">fichier Configuration. mof</span><span class="sxs-lookup"><span data-stu-id="646cb-235">configuration.mof file</span></span>**

    -   <span data-ttu-id="646cb-236">Si vous utilisez Configuration Manager 2007, vous devez modifier le fichier Configuration. mof en exécutant l’étape 3 à partir de la **mise à jour du fichier de configuration. mof si vous effectuez une mise à niveau vers MBAM 2,0 SP1 et que vous utilisez MBAM avec Configuration Manager 2007**, qui suit cet élément.</span><span class="sxs-lookup"><span data-stu-id="646cb-236">If you are using Configuration Manager 2007, you must edit the configuration.mof file by completing step 3 from the item **Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007**, which follows this item.</span></span>

    -   <span data-ttu-id="646cb-237">Si vous utilisez System Center 2012 Configuration Manager, vous pouvez modifier le fichier Configuration. mof en suivant les instructions dans [modifier le fichier Configuration. mof](edit-the-configurationmof-file.md).</span><span class="sxs-lookup"><span data-stu-id="646cb-237">If you are using System Center 2012 Configuration Manager, edit the configuration.mof file by following the instructions in [Edit the Configuration.mof File](edit-the-configurationmof-file.md).</span></span>

-   <span data-ttu-id="646cb-238">**fichier SMS \ _def. mof** : suivez les instructions de la procédure de [création ou de modification du fichier SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md).</span><span class="sxs-lookup"><span data-stu-id="646cb-238">**sms\_def.mof file** – follow the instructions in [Create or Edit the Sms\_def.mof File](create-or-edit-the-sms-defmof-file.md).</span></span>

### <span data-ttu-id="646cb-239">Mettez à jour le fichier Configuration. mof si vous effectuez une mise à niveau vers MBAM 2,0 SP1 et que vous utilisez MBAM avec Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="646cb-239">Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007</span></span>

<span data-ttu-id="646cb-240">Si vous effectuez une mise à niveau vers MBAM 2,0 SP1 et que vous utilisez MBAM avec Configuration Manager 2007, vous devez mettre à jour le fichier Configuration. mof pour vous assurer que MBAM 2,0 SP1 fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="646cb-240">If you are upgrading to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007, you must update the configuration.mof file to ensure that MBAM 2.0 SP1 works correctly.</span></span>

**<span data-ttu-id="646cb-241">Pour mettre à jour le fichier Configuration. mof:</span><span class="sxs-lookup"><span data-stu-id="646cb-241">To update the configuration.mof file:</span></span>**

1.  <span data-ttu-id="646cb-242">Sur le serveur Configuration Manager, naviguez jusqu’à l’emplacement du fichier Configuration. mof:</span><span class="sxs-lookup"><span data-stu-id="646cb-242">On the Configuration Manager Server, browse to the location of the Configuration.mof file:</span></span>

    <span data-ttu-id="646cb-243">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="646cb-243">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="646cb-244">Sur une installation par défaut, l’emplacement d’installation est%systemdrive%\\Program fichiers (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="646cb-244">On a default installation, the installation location is %systemdrive%\\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="646cb-245">Examinez le bloc de code que vous avez ajouté au fichier Configuration. mof et supprimez-le.</span><span class="sxs-lookup"><span data-stu-id="646cb-245">Review the block of code that you appended to the configuration.mof file, and delete it.</span></span> <span data-ttu-id="646cb-246">Le bloc de code est semblable à celui présenté dans l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="646cb-246">The block of code will be similar to the one shown in the following step.</span></span>

3.  <span data-ttu-id="646cb-247">Copiez le bloc de code suivant, puis ajoutez-le au fichier Configuration. mof pour ajouter les classes MBAM requises suivantes au fichier:</span><span class="sxs-lookup"><span data-stu-id="646cb-247">Copy the following block of code, and then append it to the configuration.mof file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### <span data-ttu-id="646cb-248">Traduction de MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="646cb-248">Translation of MBAM 2.0 SP1</span></span>

<span data-ttu-id="646cb-249">MBAM 2,0 SP1 est désormais disponible dans les langues suivantes:</span><span class="sxs-lookup"><span data-stu-id="646cb-249">MBAM 2.0 SP1 is now available in the following languages:</span></span>

-   <span data-ttu-id="646cb-250">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="646cb-250">English (United States) en-US</span></span>
-   <span data-ttu-id="646cb-251">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="646cb-251">French (France) fr-FR</span></span>
-   <span data-ttu-id="646cb-252">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="646cb-252">Italian (Italy) it-IT</span></span>
-   <span data-ttu-id="646cb-253">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="646cb-253">German (Germany) de-DE</span></span>
-   <span data-ttu-id="646cb-254">Espagnol, international (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="646cb-254">Spanish, International Sort (Spain) es-ES</span></span>
-   <span data-ttu-id="646cb-255">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="646cb-255">Korean (Korea) ko-KR</span></span>
-   <span data-ttu-id="646cb-256">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="646cb-256">Japanese (Japan) ja-JP</span></span>
-   <span data-ttu-id="646cb-257">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="646cb-257">Portuguese (Brazil) pt-BR</span></span>
-   <span data-ttu-id="646cb-258">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="646cb-258">Russian (Russia) ru-RU</span></span>
-   <span data-ttu-id="646cb-259">Chinois traditionnel zh-TW</span><span class="sxs-lookup"><span data-stu-id="646cb-259">Chinese Traditional zh-TW</span></span>
-   <span data-ttu-id="646cb-260">Chinois simplifié zh-NC</span><span class="sxs-lookup"><span data-stu-id="646cb-260">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="646cb-261">Obtention de technologies MDOP</span><span class="sxs-lookup"><span data-stu-id="646cb-261">How to Get MDOP Technologies</span></span>

<span data-ttu-id="646cb-262">MBAM 2,0 SP1 fait partie du pack d’optimisation du bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="646cb-262">MBAM 2.0 SP1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="646cb-263">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="646cb-263">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="646cb-264">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="646cb-264">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="646cb-265">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="646cb-265">Related topics</span></span>

[<span data-ttu-id="646cb-266">Notes de publication de MBAM2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="646cb-266">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)










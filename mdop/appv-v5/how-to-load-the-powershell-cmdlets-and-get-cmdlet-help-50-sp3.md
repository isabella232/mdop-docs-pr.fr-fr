---
title: Comment charger les applets de commande PowerShell et obtenir de l'aide sur ces derniers
description: Comment charger les applets de commande PowerShell et obtenir de l'aide sur ces derniers
author: dansimp
ms.assetid: 0624495b-943e-485b-9e54-b50e4ee6591c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 7692d3e36aabc4f3142f664e94d9d71b2cfc1bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805365"
---
# <span data-ttu-id="6f9ae-103">Comment charger les applets de commande PowerShell et obtenir de l'aide sur ces derniers</span><span class="sxs-lookup"><span data-stu-id="6f9ae-103">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span>


<span data-ttu-id="6f9ae-104">Contenu de cette rubrique:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-104">What this topic covers:</span></span>

-   [<span data-ttu-id="6f9ae-105">Configuration requise pour l’utilisation des cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-105">Requirements for using PowerShell cmdlets</span></span>](#bkmk-reqs-using-posh)

-   [<span data-ttu-id="6f9ae-106">Chargement des cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-106">Loading the PowerShell cmdlets</span></span>](#bkmk-load-cmdlets)

-   [<span data-ttu-id="6f9ae-107">Obtenir de l’aide pour les applets de applet PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-107">Getting help for the PowerShell cmdlets</span></span>](#bkmk-get-cmdlet-help)

-   [<span data-ttu-id="6f9ae-108">Affichage de l’aide pour une cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-108">Displaying the help for a PowerShell cmdlet</span></span>](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a><span data-ttu-id="6f9ae-109">Configuration requise pour l’utilisation des cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-109">Requirements for using PowerShell cmdlets</span></span>


<span data-ttu-id="6f9ae-110">Pour plus d’informations sur l’utilisation des applets de commande PowerShell App-V, consultez la configuration suivante:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-110">Review the following requirements for using the App-V PowerShell cmdlets:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6f9ae-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f9ae-111">Requirement</span></span></th>
<th align="left"><span data-ttu-id="6f9ae-112">Détails</span><span class="sxs-lookup"><span data-stu-id="6f9ae-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f9ae-113">Les utilisateurs ne peuvent exécuter des cmdlets App-V Server que si vous leur octroyez l’accès à l’aide de l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-113">Users can run App-V Server cmdlets only if you grant them access by using one of the following methods:</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="6f9ae-114">Lorsque vous déployez et configurez le serveur App-V </strong> :</span><span class="sxs-lookup"><span data-stu-id="6f9ae-114">When you are deploying and configuring the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="6f9ae-115">Spécifiez un groupe Active Directory ou un utilisateur qui dispose des autorisations pour gérer l’environnement App-V.</span><span class="sxs-lookup"><span data-stu-id="6f9ae-115">Specify an Active Directory group or individual user that has permissions to manage the App-V environment.</span></span> <span data-ttu-id="6f9ae-116">Découvrez <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> comment déployer le serveur App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="6f9ae-116">See <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
<li><p><strong><span data-ttu-id="6f9ae-117">Après avoir déployé le serveur App-V </strong> :</span><span class="sxs-lookup"><span data-stu-id="6f9ae-117">After you’ve deployed the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="6f9ae-118">Utilisez la console de gestion App-V pour ajouter un utilisateur ou un groupe Active Directory supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="6f9ae-118">Use the App-V Management console to add an additional Active Directory group or user.</span></span> <span data-ttu-id="6f9ae-119">Découvrez <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)"> comment ajouter ou supprimer un administrateur à l’aide de la console de gestion </a> .</span><span class="sxs-lookup"><span data-stu-id="6f9ae-119">See <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)">How to Add or Remove an Administrator by Using the Management Console</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f9ae-120">Applets de commande nécessitant une invite de commandes avec élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="6f9ae-120">Cmdlets that require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6f9ae-121">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6f9ae-121">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-122">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6f9ae-122">Remove-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-123">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f9ae-123">Set-AppvClientConfiguration</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-124">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="6f9ae-124">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-125">Remove-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="6f9ae-125">Remove-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-126">Add-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="6f9ae-126">Add-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-127">Remove-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="6f9ae-127">Remove-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-128">Send-AppvClientReport</span><span class="sxs-lookup"><span data-stu-id="6f9ae-128">Send-AppvClientReport</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-129">Set-AppvClientMode</span><span class="sxs-lookup"><span data-stu-id="6f9ae-129">Set-AppvClientMode</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-130">Set-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6f9ae-130">Set-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-131">Set-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="6f9ae-131">Set-AppvPublishingServer</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f9ae-132">Applets de commande que les utilisateurs finaux peuvent exécuter, sauf si vous les configurez pour exiger une invite de commandes avec élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="6f9ae-132">Cmdlets that end users can run, unless you configure them to require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6f9ae-133">Publisher-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6f9ae-133">Publish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-134">Annuler la publication-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6f9ae-134">Unpublish-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="6f9ae-135">Pour configurer ces applets de commande afin de nécessiter une invite de commandes avec élévation de privilèges, utilisez l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-135">To configure these cmdlets to require an elevated command prompt, use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6f9ae-136">Méthode</span><span class="sxs-lookup"><span data-stu-id="6f9ae-136">Method</span></span></th>
<th align="left"><span data-ttu-id="6f9ae-137">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="6f9ae-137">More resources</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f9ae-138">Exécutez l' <strong> applet de cmdlet Set-AppvClientConfiguration </strong> à l’aide du <strong> paramètre-RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="6f9ae-138">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>-RequirePublishAsAdmin</strong> parameter.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="6f9ae-139">Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-139">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="6f9ae-140">Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-140">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f9ae-141">Activez le paramètre de stratégie de groupe «exiger une publication en tant qu’administrateur» pour les clients App-V.</span><span class="sxs-lookup"><span data-stu-id="6f9ae-141">Enable the “Require publish as administrator” Group Policy setting for App-V Clients.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="6f9ae-142">Comment publier un package à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="6f9ae-142">How to Publish a Package by Using the Management Console</span></span></a> </p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a><span data-ttu-id="6f9ae-143">Chargement des cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-143">Loading the PowerShell cmdlets</span></span>
<span data-ttu-id="6f9ae-144">Pour charger les modules de cmdlet PowerShell:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-144">To load the PowerShell cmdlet modules:</span></span>

1.  <span data-ttu-id="6f9ae-145">Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.</span><span class="sxs-lookup"><span data-stu-id="6f9ae-145">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="6f9ae-146">Tapez l’une des commandes suivantes pour charger les applets de commande pour le module souhaité:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-146">Type one of the following commands to load the cmdlets for the module you want:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6f9ae-147">Composant App-V</span><span class="sxs-lookup"><span data-stu-id="6f9ae-147">App-V component</span></span></th>
<th align="left"><span data-ttu-id="6f9ae-148">Commande pour taper</span><span class="sxs-lookup"><span data-stu-id="6f9ae-148">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f9ae-149">App-V Server</span><span class="sxs-lookup"><span data-stu-id="6f9ae-149">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9ae-150">Importation-module AppvServer</span><span class="sxs-lookup"><span data-stu-id="6f9ae-150">Import-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f9ae-151">Séquenceur App-V</span><span class="sxs-lookup"><span data-stu-id="6f9ae-151">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9ae-152">Importation-module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="6f9ae-152">Import-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f9ae-153">Client App-V</span><span class="sxs-lookup"><span data-stu-id="6f9ae-153">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9ae-154">Importation-module AppvClient</span><span class="sxs-lookup"><span data-stu-id="6f9ae-154">Import-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="6f9ae-155">Obtenir de l’aide pour les applets de applet PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-155">Getting help for the PowerShell cmdlets</span></span>
<span data-ttu-id="6f9ae-156">À partir de App-V 5,0 SP3, l’aide de l’applet de cmdlet est disponible dans deux formats:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-156">Starting in App-V 5.0 SP3, cmdlet help is available in two formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6f9ae-157">Format</span><span class="sxs-lookup"><span data-stu-id="6f9ae-157">Format</span></span></th>
<th align="left"><span data-ttu-id="6f9ae-158">Description</span><span class="sxs-lookup"><span data-stu-id="6f9ae-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f9ae-159">Module téléchargeable</span><span class="sxs-lookup"><span data-stu-id="6f9ae-159">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9ae-160">Pour télécharger la dernière aide après le téléchargement du module de cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-160">To download the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="6f9ae-161">Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.</span><span class="sxs-lookup"><span data-stu-id="6f9ae-161">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="6f9ae-162">Tapez l’une des commandes suivantes pour charger les applets de commande pour le module souhaité:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-162">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6f9ae-163">Composant App-V</span><span class="sxs-lookup"><span data-stu-id="6f9ae-163">App-V component</span></span></th>
<th align="left"><span data-ttu-id="6f9ae-164">Commande pour taper</span><span class="sxs-lookup"><span data-stu-id="6f9ae-164">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f9ae-165">App-V Server</span><span class="sxs-lookup"><span data-stu-id="6f9ae-165">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9ae-166">Mise à jour-aide-module AppvServer</span><span class="sxs-lookup"><span data-stu-id="6f9ae-166">Update-Help -Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f9ae-167">Séquenceur App-V</span><span class="sxs-lookup"><span data-stu-id="6f9ae-167">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9ae-168">Mise à jour-aide-module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="6f9ae-168">Update-Help -Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f9ae-169">Client App-V</span><span class="sxs-lookup"><span data-stu-id="6f9ae-169">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9ae-170">Mise à jour-aide-module AppvClient</span><span class="sxs-lookup"><span data-stu-id="6f9ae-170">Update-Help -Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f9ae-171">Sur TechNet en tant que pages Web</span><span class="sxs-lookup"><span data-stu-id="6f9ae-171">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f9ae-172">Pour plus d’information, voir le nœud App-V sous l' <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Automation Microsoft Desktop Optimization with Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="6f9ae-172">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-display-help-cmdlet"></a><span data-ttu-id="6f9ae-173">Affichage de l’aide pour une cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9ae-173">Displaying the help for a PowerShell cmdlet</span></span>
<span data-ttu-id="6f9ae-174">Pour afficher de l’aide pour une cmdlet PowerShell spécifique:</span><span class="sxs-lookup"><span data-stu-id="6f9ae-174">To display help for a specific PowerShell cmdlet:</span></span>

1.  <span data-ttu-id="6f9ae-175">Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.</span><span class="sxs-lookup"><span data-stu-id="6f9ae-175">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="6f9ae-176">Tapez **Get-Help** &lt; *cmdlet* &gt; , par exemple, **Get-Help publishation-AppvClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="6f9ae-176">Type **Get-Help** &lt;*cmdlet*&gt;, for example, **Get-Help Publish-AppvClientPackage**.</span></span>

<span data-ttu-id="6f9ae-177">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="6f9ae-177">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6f9ae-178">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="6f9ae-178">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> <span data-ttu-id="6f9ae-179">Vous **avez un problème lié à l’application-V**?</span><span class="sxs-lookup"><span data-stu-id="6f9ae-179">**Got an App-V issue**?</span></span> <span data-ttu-id="6f9ae-180">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6f9ae-180">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 






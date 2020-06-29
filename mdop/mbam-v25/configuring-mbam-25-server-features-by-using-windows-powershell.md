---
title: Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell
description: Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809594"
---
# <span data-ttu-id="96fa3-103">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="96fa3-103">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>


<span data-ttu-id="96fa3-104">Après avoir installé le logiciel de serveur MBAM 2,5, vous pouvez utiliser les fonctionnalités de serveur MBAM 2,5 à l’aide d’applets de cmdlet Windows PowerShell ou de l’Assistant Configuration de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="96fa3-104">After you install the MBAM 2.5 Server software, you can use configure MBAM 2.5 Server features by using Windows PowerShell cmdlets or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="96fa3-105">Cette rubrique décrit comment configurer MBAM 2,5 à l’aide des cmdlets Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="96fa3-105">This topic describes how to configure MBAM 2.5 by using the Windows PowerShell cmdlets.</span></span> <span data-ttu-id="96fa3-106">Pour utiliser l’Assistant à la place, reportez-vous à [Configuration des fonctionnalités du serveur MBAM 2,5](configuring-the-mbam-25-server-features.md).</span><span class="sxs-lookup"><span data-stu-id="96fa3-106">To use the wizard instead, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md).</span></span>

## <span data-ttu-id="96fa3-107">Dans cette rubrique</span><span class="sxs-lookup"><span data-stu-id="96fa3-107">In this topic</span></span>


<span data-ttu-id="96fa3-108">Cette rubrique inclut les informations suivantes sur l’utilisation de Windows PowerShell pour configurer MBAM:</span><span class="sxs-lookup"><span data-stu-id="96fa3-108">This topic includes the following information about using Windows PowerShell to configure MBAM:</span></span>

-   [<span data-ttu-id="96fa3-109">Chargement de l’aide de Windows PowerShell pour MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="96fa3-109">How to load Windows PowerShell Help for MBAM 2.5</span></span>](#bkmk-load-posh-help)

-   [<span data-ttu-id="96fa3-110">Comment obtenir de l’aide sur une cmdlet Windows PowerShell MBAM</span><span class="sxs-lookup"><span data-stu-id="96fa3-110">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>](#bkmk-help-specific-cmdlet)

-   [<span data-ttu-id="96fa3-111">Configurations que vous pouvez effectuer uniquement avec Windows PowerShell, mais pas avec l’Assistant Configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="96fa3-111">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>](#bkmk-config-only-posh)

-   [<span data-ttu-id="96fa3-112">Conditions préalables et configuration requise pour l’utilisation de Windows PowerShell pour configurer les fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="96fa3-112">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>](#bkmk-prereqs-posh-mbamsvr)

-   [<span data-ttu-id="96fa3-113">Utilisation de Windows PowerShell pour configurer MBAM sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="96fa3-113">Using Windows PowerShell to configure MBAM on a remote computer</span></span>](#bkmk-remote-config)

-   [<span data-ttu-id="96fa3-114">Comptes requis et paramètres de cmdlet Windows PowerShell correspondants</span><span class="sxs-lookup"><span data-stu-id="96fa3-114">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>](#bkmk-reqd-posh-accts)

<span data-ttu-id="96fa3-115">Pour plus d’informations sur les applets de applet de passe **Get-MbamBitLockerRecoveryKey** et **Get-MbamTPMOwnerPassword** , qui sont utilisées pour gérer MBAM, voir [utilisation de Windows PowerShell pour gérer MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="96fa3-115">For information about the **Get-MbamBitLockerRecoveryKey** and **Get-MbamTPMOwnerPassword** Windows PowerShell cmdlets, which are used to administer MBAM, see [Using Windows PowerShell to Administer MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md).</span></span>

## <a href="" id="bkmk-load-posh-help"></a><span data-ttu-id="96fa3-116">Chargement de l’aide de Windows PowerShell pour MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="96fa3-116">How to load Windows PowerShell Help for MBAM 2.5</span></span>


<span data-ttu-id="96fa3-117">Pour obtenir la liste des cmdlets Windows PowerShell sur TechNet, voir [automatisation du pack d’optimisation du bureau Microsoft avec Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span><span class="sxs-lookup"><span data-stu-id="96fa3-117">For a list of the Windows PowerShell cmdlets on TechNet, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span></span>

**<span data-ttu-id="96fa3-118">Pour charger l’aide 2,5 de MBAM pour les applets de cmdlet Windows PowerShell après l’installation du logiciel serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="96fa3-118">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="96fa3-119">Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.</span><span class="sxs-lookup"><span data-stu-id="96fa3-119">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="96fa3-120">Tapez **Update-aide – module Microsoft. mbam**.</span><span class="sxs-lookup"><span data-stu-id="96fa3-120">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

## <a href="" id="bkmk-help-specific-cmdlet"></a><span data-ttu-id="96fa3-121">Comment obtenir de l’aide sur une cmdlet Windows PowerShell MBAM</span><span class="sxs-lookup"><span data-stu-id="96fa3-121">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>


<span data-ttu-id="96fa3-122">L’aide de Windows PowerShell pour MBAM est disponible dans les formats suivants:</span><span class="sxs-lookup"><span data-stu-id="96fa3-122">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="96fa3-123">Format d’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="96fa3-123">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="96fa3-124">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="96fa3-124">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-125">À l’invite de commandes Windows PowerShell, tapez <strong> get- </strong> &lt; <em> cmdlet cmdlet.</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="96fa3-125">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fa3-126">Pour télécharger les dernières cmdlets Windows PowerShell, suivez les instructions de la section précédente sur le chargement de l’aide de Windows PowerShell pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="96fa3-126">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fa3-127">Sur TechNet en tant que pages Web</span><span class="sxs-lookup"><span data-stu-id="96fa3-127">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-128">Dans le centre de téléchargement en tant que fichier Word. docx</span><span class="sxs-lookup"><span data-stu-id="96fa3-128">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fa3-129">Dans le centre de téléchargement sous forme de fichier. pdf</span><span class="sxs-lookup"><span data-stu-id="96fa3-129">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a><span data-ttu-id="96fa3-130">Configurations que vous pouvez effectuer uniquement avec Windows PowerShell, mais pas avec l’Assistant Configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="96fa3-130">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="96fa3-131">Configurations que vous pouvez effectuer uniquement à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="96fa3-131">Configurations that you can do only by using Windows PowerShell</span></span></th>
<th align="left"><span data-ttu-id="96fa3-132">Détails</span><span class="sxs-lookup"><span data-stu-id="96fa3-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-133">Installez les services Web sur un autre ordinateur à partir des applications Web.</span><span class="sxs-lookup"><span data-stu-id="96fa3-133">Install the web services on a separate computer from the web applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fa3-134">À l’aide de l’Assistant, vous devez installer les services Web et les applications Web sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="96fa3-134">Using the wizard, you must install the web services and web applications on the same computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fa3-135">Activez des rapports sur un point de services de Reporting autonome sans installer tous les objets de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="96fa3-135">Enable reports on a separate reporting services point without installing all of the Configuration Manager objects.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-136">Supprimez tous les objets de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="96fa3-136">Delete all of the objects from Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fa3-137">La suppression des objets entraîne la suppression de toutes les données de conformité de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="96fa3-137">Deleting the objects in turn deletes all of the compliance data from Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fa3-138">Entrez une chaîne de connexion personnalisée pour les bases de données.</span><span class="sxs-lookup"><span data-stu-id="96fa3-138">Enter a custom connection string for the databases.</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fa3-139">Exemple: pour configurer les applications Web de manière à utiliser la mise en miroir, vous devez utiliser l' <strong> </strong> applet de connexion Enable-MbamWebApplication pour spécifier la syntaxe de partenaire de basculement appropriée dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="96fa3-139">Example: To configure the web applications to work with mirroring, you must use the <strong>Enable-MbamWebApplication</strong> cmdlet to specify the appropriate failover partner syntax in the connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-140">Ignorez la validation et configurez une fonctionnalité même si la vérification préalable a échoué.</span><span class="sxs-lookup"><span data-stu-id="96fa3-140">Skip validation and configure a feature even though the prerequisite check failed.</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="96fa3-141">**Remarques**  Vous ne pouvez pas désactiver la base de données MBAM avec une applet de cmdlet Windows PowerShell ou l’Assistant Configuration de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="96fa3-141">**Note** You cannot disable the MBAM databases with a Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="96fa3-142">Pour éviter toute suppression accidentelle de vos données de conformité et d’audit, les administrateurs de base de données doivent supprimer manuellement des bases de données.</span><span class="sxs-lookup"><span data-stu-id="96fa3-142">To prevent the accidental removal of your compliance and audit data, database administrators must remove databases manually.</span></span>

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a><span data-ttu-id="96fa3-143">Conditions préalables et configuration requise pour l’utilisation de Windows PowerShell pour configurer les fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="96fa3-143">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>


<span data-ttu-id="96fa3-144">Avant de démarrer la configuration, remplissez les conditions préalables suivantes.</span><span class="sxs-lookup"><span data-stu-id="96fa3-144">Before starting the configuration, complete the following prerequisites.</span></span>

**<span data-ttu-id="96fa3-145">Prérequis liés au compte</span><span class="sxs-lookup"><span data-stu-id="96fa3-145">Account-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="96fa3-146">Prérequises</span><span class="sxs-lookup"><span data-stu-id="96fa3-146">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="96fa3-147">Détails ou informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="96fa3-147">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-148">Créez les comptes nécessaires.</span><span class="sxs-lookup"><span data-stu-id="96fa3-148">Create the required accounts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fa3-149"><strong> </strong> Pour plus d’plus d’rubriques, voir la section comptes requis et les paramètres de cmdlet Windows PowerShell correspondants.</span><span class="sxs-lookup"><span data-stu-id="96fa3-149">See section <strong>Required accounts and corresponding Windows PowerShell cmdlet parameters</strong> later in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fa3-150">Les comptes d’utilisateurs et les groupes que vous transmettez en tant que paramètres aux cmdlets Windows PowerShell doivent être des comptes valides dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="96fa3-150">User accounts and groups that you pass as parameters to the Windows PowerShell cmdlets must be valid accounts in the domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fa3-151">Vous ne pouvez pas utiliser les comptes locaux.</span><span class="sxs-lookup"><span data-stu-id="96fa3-151">You cannot use local accounts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-152">Spécifiez des comptes au format de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="96fa3-152">Specify accounts in the down-level format.</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fa3-153">Exemples:</span><span class="sxs-lookup"><span data-stu-id="96fa3-153">Examples:</span></span></p>
<p><span data-ttu-id="96fa3-154">domainNetBiosName\userdomainNetBiosName\group</span><span class="sxs-lookup"><span data-stu-id="96fa3-154">domainNetBiosName\userdomainNetBiosName\group</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="96fa3-155">Prérequis liés aux autorisations</span><span class="sxs-lookup"><span data-stu-id="96fa3-155">Permission-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="96fa3-156">Prérequises</span><span class="sxs-lookup"><span data-stu-id="96fa3-156">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="96fa3-157">Détails ou informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="96fa3-157">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-158">Vous devez être administrateur de l’ordinateur local sur lequel vous configurez la fonctionnalité MBAM.</span><span class="sxs-lookup"><span data-stu-id="96fa3-158">You must be an administrator on the local computer where you are configuring the MBAM feature.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fa3-159">Utilisez une invite de commandes Windows PowerShell avec élévation de privilèges pour exécuter toutes les applets de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="96fa3-159">Use an elevated Windows PowerShell command prompt to run all Windows PowerShell cmdlets.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-160">Pour l' <strong> applet de passe Enable-MbamDatabase </strong> uniquement:</span><span class="sxs-lookup"><span data-stu-id="96fa3-160">For the <strong>Enable-MbamDatabase</strong> cmdlet only:</span></span></p>
<p><span data-ttu-id="96fa3-161">Vous devez &quot; créer des autorisations de base de données &quot; sur l’instance de la base de données Microsoft SQL Server cible.</span><span class="sxs-lookup"><span data-stu-id="96fa3-161">You must have &quot;create any database&quot; permissions on the instance of the target Microsoft SQL Server database.</span></span></p>
<p><span data-ttu-id="96fa3-162">Ce compte d’utilisateur doit être membre du groupe Administrateurs local ou du groupe opérateurs de sauvegarde pour pouvoir inscrire le scripteur du service de cliché instantané de volume MBAM.</span><span class="sxs-lookup"><span data-stu-id="96fa3-162">This user account must be a part of the local administrators group or the Backup Operators group to register the MBAM Volume Shadow Copy Service (VSS) Writer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="96fa3-163">Par défaut, l’administrateur de base de données ou l’administrateur système dispose de l' &quot; autorisation de création de base de données requise &quot; .</span><span class="sxs-lookup"><span data-stu-id="96fa3-163">By default, the database administrator or system administrator has the required &quot;create any database&quot; permissions.</span></span></p>
<p></p>
<p><span data-ttu-id="96fa3-164">Pour plus d’informations sur le scripteur VSS, voir <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> service de cliché instantané de volume </a> .</span><span class="sxs-lookup"><span data-stu-id="96fa3-164">For more information about VSS Writer, see <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)">Volume Shadow Copy Service</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fa3-165">Pour la <strong> fonctionnalité d’intégration de System Center Configuration Manager </strong> uniquement:</span><span class="sxs-lookup"><span data-stu-id="96fa3-165">For the <strong>System Center Configuration Manager Integration</strong> feature only:</span></span></p>
<p><span data-ttu-id="96fa3-166">L’utilisateur qui a activé cette fonctionnalité doit avoir les autorisations suivantes dans Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="96fa3-166">The user who enables this feature must have these rights in Configuration Manager:</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="96fa3-167">Type de droits dans Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="96fa3-167">Type of rights in Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="96fa3-168">Droits requis</span><span class="sxs-lookup"><span data-stu-id="96fa3-168">Required rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-169">Droits de site Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="96fa3-169">Configuration Manager Site rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="96fa3-170">Read</span><span class="sxs-lookup"><span data-stu-id="96fa3-170">Read</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96fa3-171">Droits de collection de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="96fa3-171">Configuration Manager Collection rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="96fa3-172">Création-suppression-lecture-modification-déploiement des éléments de configuration</span><span class="sxs-lookup"><span data-stu-id="96fa3-172">Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96fa3-173">Droits des éléments de configuration du gestionnaire de configuration:</span><span class="sxs-lookup"><span data-stu-id="96fa3-173">Configuration Manager Configuration item rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="96fa3-174">Création-suppression-lecture</span><span class="sxs-lookup"><span data-stu-id="96fa3-174">Create- Delete- Read</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a><span data-ttu-id="96fa3-175">Utilisation de Windows PowerShell pour configurer MBAM sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="96fa3-175">Using Windows PowerShell to configure MBAM on a remote computer</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="96fa3-176">Quand utiliser cette fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="96fa3-176">When to use this capability</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="96fa3-177">Lorsque vous voulez configurer les fonctionnalités du serveur MBAM 2,5 sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="96fa3-177">When you want to configure the MBAM 2.5 Server features on a remote computer.</span></span> <span data-ttu-id="96fa3-178">Les applets de commande Windows PowerShell s’exécutent sur un ordinateur et vous configurez celles-ci sur un autre ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="96fa3-178">The Windows PowerShell cmdlets are running on one computer, and you are configuring the features on a different, remote computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="96fa3-179">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="96fa3-179">What you have to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="96fa3-180">Pour utiliser Windows PowerShell afin de configurer les fonctionnalités du serveur MBAM 2,5 sur un ordinateur distant, vous devez:</span><span class="sxs-lookup"><span data-stu-id="96fa3-180">To use Windows PowerShell to configure MBAM 2.5 Server features on a remote computer, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="96fa3-181">Assurez-vous que le logiciel serveur MBAM 2,5 est installé sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="96fa3-181">Ensure that the MBAM 2.5 Server software has been installed on the remote computer.</span></span></p></li>
<li><p><span data-ttu-id="96fa3-182">Utilisez le protocole CredSSP (Credential Security Support Provider) pour ouvrir la session Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="96fa3-182">Use the Credential Security Support Provider (CredSSP) Protocol to open the Windows PowerShell session.</span></span></p></li>
<li><p><span data-ttu-id="96fa3-183">Activez la gestion à distance de Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="96fa3-183">Enable Windows Remote Management (WinRM).</span></span> <span data-ttu-id="96fa3-184">Si vous ne parvenez pas à activer le service WinRM et à le configurer correctement, l' <strong> applet de commande New-PSSession </strong> décrite dans ce tableau affiche une erreur et explique comment résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="96fa3-184">If you fail to enable WinRM and to configure it correctly, the <strong>New-PSSession</strong> cmdlet that is described in this table displays an error and describes how to fix the issue.</span></span> <span data-ttu-id="96fa3-185">Pour plus d’informations sur WinRM, voir utilisation de la <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> gestion à distance de Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="96fa3-185">For more information about WinRM, see <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)">Using Windows Remote Management</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="96fa3-186">Raison pour laquelle vous devez le faire</span><span class="sxs-lookup"><span data-stu-id="96fa3-186">Why you have to do it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="96fa3-187">Ce protocole permet aux cmdlets Windows PowerShell de se connecter à des services de domaine Active Directory (AD FS) en utilisant les informations d’identification d’administrateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96fa3-187">This protocol enables the Windows PowerShell cmdlets to connect to Active Directory Domain Services by using the user’s administrative credentials.</span></span> <span data-ttu-id="96fa3-188">Il est possible que vous obteniez une erreur de validation si vous démarrez la session Windows PowerShell sans ce protocole.</span><span class="sxs-lookup"><span data-stu-id="96fa3-188">You might get a validation error if you start the Windows PowerShell session without this protocol.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="96fa3-189">Démarrer une session Windows PowerShell avec le protocole CredSSP</span><span class="sxs-lookup"><span data-stu-id="96fa3-189">How to start a Windows PowerShell session with the CredSSP protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="96fa3-190">Tapez le code suivant à l’invite Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="96fa3-190">Type the following code at the Windows PowerShell prompt:</span></span></p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p><span data-ttu-id="96fa3-191">Le code qui suit montre un exemple.</span><span class="sxs-lookup"><span data-stu-id="96fa3-191">The following code shows an example.</span></span></p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a><span data-ttu-id="96fa3-192">Comptes requis et paramètres de cmdlet Windows PowerShell correspondants</span><span class="sxs-lookup"><span data-stu-id="96fa3-192">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>


<span data-ttu-id="96fa3-193">Le tableau suivant décrit les comptes nécessaires à la configuration des fonctionnalités du serveur MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="96fa3-193">The following table describes the accounts that are required to configure MBAM 2.5 Server features.</span></span> <span data-ttu-id="96fa3-194">Il indique également la cmdlet et le paramètre Windows PowerShell correspondants pour lesquels vous devez spécifier le compte lors de la configuration.</span><span class="sxs-lookup"><span data-stu-id="96fa3-194">It also lists the corresponding Windows PowerShell cmdlet and parameter for which you have to specify the account during configuration.</span></span>

<span data-ttu-id="96fa3-195">Type de paramètre cmdlet (utilisateur ou groupe) Description-MBAMDatabase</span><span class="sxs-lookup"><span data-stu-id="96fa3-195">Cmdlet Parameter Type (User or Group) Description Enable-MBAMDatabase</span></span>

<span data-ttu-id="96fa3-196">AccessAccount</span><span class="sxs-lookup"><span data-stu-id="96fa3-196">AccessAccount</span></span>

<span data-ttu-id="96fa3-197">Utilisateur ou groupe</span><span class="sxs-lookup"><span data-stu-id="96fa3-197">User or Group</span></span>

<span data-ttu-id="96fa3-198">Spécifiez un utilisateur ou un groupe de domaine ayant une autorisation en lecture/écriture sur cette base de données pour permettre aux applications Web d’accéder aux données et aux rapports de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="96fa3-198">Specify a domain user or group that has read/write permission to this database to give the web applications access to data and reports in this database.</span></span> <span data-ttu-id="96fa3-199">Si la valeur est un utilisateur de domaine, le paramètre **WebServiceApplicationPoolCredential** qui est utilisé lors de l’exécution de l’applet de passe **Enable-MbamWebApplication** doit utiliser le même compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96fa3-199">If the value is a domain user, then the **WebServiceApplicationPoolCredential** parameter that is used when running the **Enable-MbamWebApplication** cmdlet must use the same user account.</span></span> <span data-ttu-id="96fa3-200">Si la valeur est un groupe d’utilisateurs du domaine, le compte de domaine utilisé par le paramètre **WebServiceApplicationPoolCredential** doit être membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="96fa3-200">If the value is a domain Users group, then the domain account that is used by the **WebServiceApplicationPoolCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="96fa3-201">ReportAccount</span><span class="sxs-lookup"><span data-stu-id="96fa3-201">ReportAccount</span></span>

<span data-ttu-id="96fa3-202">Utilisateur ou groupe</span><span class="sxs-lookup"><span data-stu-id="96fa3-202">User or Group</span></span>

<span data-ttu-id="96fa3-203">Spécifiez un groupe d’utilisateurs ou d’utilisateurs de domaine disposant de droits en lecture seule sur cette base de données pour indiquer à MBAM d’accéder aux données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="96fa3-203">Specify a domain user or Users group that has read-only permission to this database to provide the MBAM reports access to the compliance and audit data.</span></span> <span data-ttu-id="96fa3-204">Si la valeur est un utilisateur de domaine, le paramètre **ComplianceAndAuditDBCredential** de l’applet de passe **Enable-MbamReport** doit utiliser le même compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96fa3-204">If the value is a domain user, then the **ComplianceAndAuditDBCredential** parameter of the **Enable-MbamReport** cmdlet must use the same user account.</span></span> <span data-ttu-id="96fa3-205">Si la valeur est un groupe d’utilisateurs du domaine, le compte de domaine utilisé par le paramètre **ComplianceAndAuditDBCredential** doit être membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="96fa3-205">If the value is a domain Users group, then the domain account that is used by the **ComplianceAndAuditDBCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="96fa3-206">Enable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="96fa3-206">Enable-MbamReport</span></span>

<span data-ttu-id="96fa3-207">ComplianceAndAuditDBCredential</span><span class="sxs-lookup"><span data-stu-id="96fa3-207">ComplianceAndAuditDBCredential</span></span>

<span data-ttu-id="96fa3-208">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="96fa3-208">User</span></span>

<span data-ttu-id="96fa3-209">Spécifie les informations d’identification d’administration que l’instance SSRS locale utilise pour se connecter à la base de données de conformité et d’audit MBAM.</span><span class="sxs-lookup"><span data-stu-id="96fa3-209">Specifies the administrative credential that the local SSRS instance uses to connect to the MBAM Compliance and Audit Database.</span></span> <span data-ttu-id="96fa3-210">L’utilisateur de domaine dans les informations d’identification d’administration doit être le même que le compte d’utilisateur utilisé pour le paramètre **ReportAccount** , qui est utilisé lors de l’exécution de l’applet de connexion **Enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="96fa3-210">The domain user in the administrative credential must be the same as the user account that is used for the **ReportAccount** parameter, which is used while running the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="96fa3-211">Si un groupe d’utilisateurs de domaine a été utilisé avec le paramètre **ReportAccount** , ce compte doit être membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="96fa3-211">If a domain Users group was used with the **ReportAccount** parameter, this account should be a member of that group.</span></span>

<span data-ttu-id="96fa3-212">**Important**  Le compte spécifié dans les informations d’identification d’administration doit disposer de droits d’utilisateur limités pour renforcer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="96fa3-212">**Important** The account specified in the administrative credentials should have limited user rights for improved security.</span></span> <span data-ttu-id="96fa3-213">Par ailleurs, le mot de passe du compte doit être configuré pour ne pas arriver à expiration.</span><span class="sxs-lookup"><span data-stu-id="96fa3-213">Also, the password of the account should be set to not expire.</span></span>

 

<span data-ttu-id="96fa3-214">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="96fa3-214">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="96fa3-215">Groupe</span><span class="sxs-lookup"><span data-stu-id="96fa3-215">Group</span></span>

<span data-ttu-id="96fa3-216">Spécifie le groupe d’utilisateurs de domaine ayant des autorisations de lecture pour les rapports.</span><span class="sxs-lookup"><span data-stu-id="96fa3-216">Specifies the domain user group that has read permissions to the reports.</span></span> <span data-ttu-id="96fa3-217">Le groupe spécifié doit être le même que celui utilisé pour le paramètre **ReportsReadOnlyAccessGroup** dans l’applet de passe **Enable-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="96fa3-217">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamWebApplication** cmdlet.</span></span>

<span data-ttu-id="96fa3-218">Enable-MBAMWebApplication</span><span class="sxs-lookup"><span data-stu-id="96fa3-218">Enable-MBAMWebApplication</span></span>

<span data-ttu-id="96fa3-219">AdvancedHelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="96fa3-219">AdvancedHelpdeskAccessGroup</span></span>

<span data-ttu-id="96fa3-220">Groupe</span><span class="sxs-lookup"><span data-stu-id="96fa3-220">Group</span></span>

<span data-ttu-id="96fa3-221">Spécifie le groupe utilisateurs du domaine qui a accès à toutes les zones du site Web d’administration et de contrôle, à l’exception de la zone rapports.</span><span class="sxs-lookup"><span data-stu-id="96fa3-221">Specifies the domain Users group that has access to all areas of the Administration and Monitoring Website except the Reports area.</span></span>

<span data-ttu-id="96fa3-222">HelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="96fa3-222">HelpdeskAccessGroup</span></span>

<span data-ttu-id="96fa3-223">Groupe</span><span class="sxs-lookup"><span data-stu-id="96fa3-223">Group</span></span>

<span data-ttu-id="96fa3-224">Spécifie le groupe utilisateurs du domaine qui a accès aux zones **gérer le module de plateforme sécurisée** et de **récupération des lecteurs** du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="96fa3-224">Specifies the domain Users group that has access to the **Manage TPM** and **Drive Recovery** areas of the Administration and Monitoring Website.</span></span>

<span data-ttu-id="96fa3-225">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="96fa3-225">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="96fa3-226">Groupe</span><span class="sxs-lookup"><span data-stu-id="96fa3-226">Group</span></span>

<span data-ttu-id="96fa3-227">Spécifie le groupe utilisateurs du domaine disposant de droits d’accès en lecture à la zone **rapports** du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="96fa3-227">Specifies the domain Users group that has read permission to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="96fa3-228">Le groupe spécifié doit être le même que celui utilisé pour le paramètre **ReportsReadOnlyAccessGroup** dans l’applet de passe **Enable-MbamReport** .</span><span class="sxs-lookup"><span data-stu-id="96fa3-228">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamReport** cmdlet.</span></span>

<span data-ttu-id="96fa3-229">WebServiceApplicationPoolCredential</span><span class="sxs-lookup"><span data-stu-id="96fa3-229">WebServiceApplicationPoolCredential</span></span>

<span data-ttu-id="96fa3-230">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="96fa3-230">User</span></span>

<span data-ttu-id="96fa3-231">Spécifie l’utilisateur de domaine à utiliser par le pool d’applications pour les applications Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="96fa3-231">Specifies the domain user to be used by the application pool for the MBAM web applications.</span></span> <span data-ttu-id="96fa3-232">Ce compte d’utilisateur doit être le même que celui indiqué dans le paramètre **AccessAccount** de l’applet de passe **Enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="96fa3-232">It must be the same domain user account that is specified in the **AccessAccount** parameter of the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="96fa3-233">Si un groupe d’utilisateurs de domaine a été utilisé par le paramètre **AccessAccount** lors de l’exécution de l’applet de passe **Enable-MbamDatabase** , l’utilisateur de domaine spécifié ici doit être membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="96fa3-233">If a domain Users group was used by the **AccessAccount** parameter when running the **Enable-MbamDatabase** cmdlet, the domain user that is specified here must be a member of that group.</span></span> <span data-ttu-id="96fa3-234">Si vous ne spécifiez pas les informations d’identification d’administration, les informations d’identification d’administration spécifiées par une application Web précédemment activée sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="96fa3-234">If you do not specify the administrative credentials, the administrative credentials that were specified by any previously enabled web application are used.</span></span> <span data-ttu-id="96fa3-235">Toutes les applications Web utilisent la même identité de pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="96fa3-235">All of the web applications use the same application pool identity.</span></span> <span data-ttu-id="96fa3-236">S’il est spécifié plusieurs fois, la valeur la plus récemment spécifiée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="96fa3-236">If it is specified multiple times, the most recently specified value is used.</span></span>

<span data-ttu-id="96fa3-237">**Important**  Pour une sécurité accrue, configurez le compte spécifié dans les informations d’identification d’administration sur des droits d’utilisateur limités.</span><span class="sxs-lookup"><span data-stu-id="96fa3-237">**Important** For improved security, set the account that is specified in the administrative credentials to limited user rights.</span></span> <span data-ttu-id="96fa3-238">Définissez également le mot de passe du compte pour qu’il n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="96fa3-238">Also, set the password of the account to never expire.</span></span> <span data-ttu-id="96fa3-239">Assurez-vous que le compte intégré IIS \ _IUSRS ou le compte utilisé pour le paramètre **WebServiceApplicationPoolCredential** a été ajouté au paramètre d' **identité d’un client après l’authentification** .</span><span class="sxs-lookup"><span data-stu-id="96fa3-239">Ensure that either the built-in IIS\_IUSRS account or the account that is used for the **WebServiceApplicationPoolCredential** parameter has been added to the **Impersonate a client after authentication** local security setting.</span></span>

<span data-ttu-id="96fa3-240">Pour afficher le paramètre de sécurité local, ouvrez l' **éditeur de stratégie de sécurité local**, développez le nœud **stratégies locales** , sélectionnez le nœud d' **attribution de droits d’utilisateur** , puis double-cliquez sur l’option emprunter l’identité d' **un client après authentification** et **ouvrez une session en tant que** paramètres de la stratégie de groupe dans le volet Détails.</span><span class="sxs-lookup"><span data-stu-id="96fa3-240">To view the local security setting, open the **Local Security Policy editor**, expand the **Local Policies** node, select the **User Rights Assignment** node, and then double-click the **Impersonate a client after authentication** and **Log on as a batch job** Group Policy settings in the details pane.</span></span>

 

 




## <span data-ttu-id="96fa3-241">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96fa3-241">Related topics</span></span>


[<span data-ttu-id="96fa3-242">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="96fa3-242">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="96fa3-243">Validation de la configuration des composants serveur de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="96fa3-243">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)

[<span data-ttu-id="96fa3-244">Utilisation de Windows PowerShell pour administrer MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="96fa3-244">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)

 
## <span data-ttu-id="96fa3-245">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="96fa3-245">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="96fa3-246">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="96fa3-246">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="96fa3-247">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="96fa3-247">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 






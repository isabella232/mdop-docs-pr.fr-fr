---
title: Composants requis d'App-V5.0 SP3
description: Composants requis d'App-V5.0 SP3
author: dansimp
ms.assetid: fa8d5578-3a53-4e8a-95c7-e7a5f6e4a31c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e8318a71d2d3631b0ad47e3c3db3c569488790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806000"
---
# <span data-ttu-id="d1331-103">Composants requis d'App-V5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="d1331-103">App-V 5.0 SP3 Prerequisites</span></span>


<span data-ttu-id="d1331-104">Avant l’installation de Microsoft Application Virtualization (App-V) 5,0 SP3, assurez-vous d’avoir installé tous les logiciels requis suivants.</span><span class="sxs-lookup"><span data-stu-id="d1331-104">Before installing Microsoft Application Virtualization (App-V) 5.0 SP3, ensure that you have installed all of the following required prerequisite software.</span></span>

<span data-ttu-id="d1331-105">Pour obtenir la liste des systèmes d’exploitation pris en charge et la configuration matérielle requise pour le serveur App-V, le Sequencer et le client, voir [Configurations prises en charge par app-v 5,0 SP3](app-v-50-sp3-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="d1331-105">For a list of supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client, see [App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md).</span></span>

## <span data-ttu-id="d1331-106">Résumé de logiciels préinstallés sur chaque système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="d1331-106">Summary of software preinstalled on each operating system</span></span>


<span data-ttu-id="d1331-107">Le tableau suivant indique les logiciels déjà installés pour différents systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d1331-107">The following table indicates the software that is already installed for different operating systems.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-108">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="d1331-108">Operating system</span></span></th>
<th align="left"><span data-ttu-id="d1331-109">Description requise</span><span class="sxs-lookup"><span data-stu-id="d1331-109">Prerequisite description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-110">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d1331-110">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-111">Tous les logiciels requis sont déjà installés.</span><span class="sxs-lookup"><span data-stu-id="d1331-111">All of the prerequisite software is already installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-112">Windows8</span><span class="sxs-lookup"><span data-stu-id="d1331-112">Windows 8</span></span></p>
<p><span data-ttu-id="d1331-113">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="d1331-113">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-114">Les logiciels requis suivants sont déjà installés:</span><span class="sxs-lookup"><span data-stu-id="d1331-114">The following prerequisite software is already installed:</span></span></p>
<ul>
<li><p><span data-ttu-id="d1331-115">Microsoft .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="d1331-115">Microsoft .NET Framework 4.5</span></span></p></li>
<li><p><span data-ttu-id="d1331-116">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="d1331-116">Windows PowerShell 3.0</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d1331-117">Remarque</span><span class="sxs-lookup"><span data-stu-id="d1331-117">Note</span></span></strong><br/><p><span data-ttu-id="d1331-118">L’installation de PowerShell 3,0 nécessite un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="d1331-118">Installing PowerShell 3.0 requires a restart.</span></span></p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-119">Windows7</span><span class="sxs-lookup"><span data-stu-id="d1331-119">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-120">Le logiciel requis n’est pas déjà installé.</span><span class="sxs-lookup"><span data-stu-id="d1331-120">The prerequisite software is not already installed.</span></span> <span data-ttu-id="d1331-121">Pour pouvoir installer App-V, vous devez l’installer.</span><span class="sxs-lookup"><span data-stu-id="d1331-121">You must install it before you can install App-V.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d1331-122">Logiciels requis pour App-V Server</span><span class="sxs-lookup"><span data-stu-id="d1331-122">App-V Server prerequisite software</span></span>


<span data-ttu-id="d1331-123">Installez les logiciels prérequis requis pour les composants serveur App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="d1331-123">Install the required prerequisite software for the App-V 5.0 SP3 Server components.</span></span>

### <span data-ttu-id="d1331-124">Ce que vous devez savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d1331-124">What to know before you start</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-125">Compte pour l’installation de l’App-V Server</span><span class="sxs-lookup"><span data-stu-id="d1331-125">Account for installing the App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-126">Le compte que vous utilisez pour installer les composants du serveur App-V doit avoir:</span><span class="sxs-lookup"><span data-stu-id="d1331-126">The account that you use to install the App-V Server components must have:</span></span></p>
<ul>
<li><p><span data-ttu-id="d1331-127">Des droits d’administrateur sur l’ordinateur sur lequel vous installez les composants.</span><span class="sxs-lookup"><span data-stu-id="d1331-127">Administrative rights on the computer on which you are installing the components.</span></span></p></li>
<li><p><span data-ttu-id="d1331-128">La possibilité d’interroger les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d1331-128">The ability to query Active Directory Domain Services.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-129">Port et pare-feu</span><span class="sxs-lookup"><span data-stu-id="d1331-129">Port and firewall</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="d1331-130">Spécifiez un port sur lequel chaque composant sera hébergé.</span><span class="sxs-lookup"><span data-stu-id="d1331-130">Specify a port where each component will be hosted.</span></span></p></li>
<li><p><span data-ttu-id="d1331-131">Ajoutez les règles de pare-feu associées pour autoriser les demandes entrantes sur les ports spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d1331-131">Add the associated firewall rules to allow incoming requests to the specified ports.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-132">WebDAV (Web Distributed Authoring and Versioning)</span><span class="sxs-lookup"><span data-stu-id="d1331-132">Web Distributed Authoring and Versioning (WebDAV)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-133">WebDAV est automatiquement désactivé pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="d1331-133">WebDAV is automatically disabled for the Management Service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-134">Scénarios de déploiement pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1331-134">Supported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="d1331-135">Un déploiement autonome, dans lequel tous les composants sont déployés sur le même serveur.</span><span class="sxs-lookup"><span data-stu-id="d1331-135">A stand-alone deployment, where all components are deployed on the same server.</span></span></p></li>
<li><p><span data-ttu-id="d1331-136">Un déploiement distribué.</span><span class="sxs-lookup"><span data-stu-id="d1331-136">A distributed deployment.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-137">Scénarios de déploiement non pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1331-137">Unsupported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="d1331-138">Installation de l’App-V Server sur un ordinateur qui exécute une version ou un composant antérieur de App-V.</span><span class="sxs-lookup"><span data-stu-id="d1331-138">Installing the App-V Server on a computer that runs any previous version or component of App-V.</span></span></p></li>
<li><p><span data-ttu-id="d1331-139">Installation des composants App-V Server sur un ordinateur qui exécute le serveur principal ou le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="d1331-139">Installing the App-V server components on a computer that runs server core or domain controller.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="d1331-140">Logiciels requis par le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="d1331-140">Management server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-141">Conditions préalables et configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1331-141">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="d1331-142">Détails</span><span class="sxs-lookup"><span data-stu-id="d1331-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-143">Version prise en charge de SQL Server</span><span class="sxs-lookup"><span data-stu-id="d1331-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-144">Pour les versions prises en charge, voir <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> Configurations prises en charge par App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="d1331-144">For supported versions, see <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">App-V 5.0 SP3 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="d1331-145">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</span><span class="sxs-lookup"><span data-stu-id="d1331-145">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="d1331-146">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="d1331-146">Windows PowerShell 3.0</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d1331-147">L’installation de PowerShell 3,0 nécessite un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="d1331-147">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-148">Télécharger et installer <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</span><span class="sxs-lookup"><span data-stu-id="d1331-148">Download and install <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d1331-149">S’applique uniquement à Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d1331-149">Applies to Windows 7 only.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="d1331-150">Packages redistribuables Visual C++ pour Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="d1331-150">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-151">64 ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="d1331-151">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-152">Rôle du serveur Web Windows Server</span><span class="sxs-lookup"><span data-stu-id="d1331-152">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-153">Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="d1331-153">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-154">Outils de gestion du serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="d1331-154">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-155">Cliquez sur <strong> scripts et outils de gestion IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="d1331-155">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-156">Services de rôle de serveur Web</span><span class="sxs-lookup"><span data-stu-id="d1331-156">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d1331-157">Fonctionnalités HTTP communes:</span><span class="sxs-lookup"><span data-stu-id="d1331-157">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-158">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="d1331-158">Static Content</span></span></p></li>
<li><p><span data-ttu-id="d1331-159">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="d1331-159">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="d1331-160">Développement d’applications:</span><span class="sxs-lookup"><span data-stu-id="d1331-160">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-161">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="d1331-161">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="d1331-162">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="d1331-162">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="d1331-163">Extensions ISAPI</span><span class="sxs-lookup"><span data-stu-id="d1331-163">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="d1331-164">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="d1331-164">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="d1331-165">Sûreté</span><span class="sxs-lookup"><span data-stu-id="d1331-165">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-166">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="d1331-166">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="d1331-167">Filtrage de requête</span><span class="sxs-lookup"><span data-stu-id="d1331-167">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="d1331-168">Outils de gestion:</span><span class="sxs-lookup"><span data-stu-id="d1331-168">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-169">Console de gestion IIS</span><span class="sxs-lookup"><span data-stu-id="d1331-169">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-170">Emplacement d’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="d1331-170">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-171">Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</span><span class="sxs-lookup"><span data-stu-id="d1331-171">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-172">Emplacement de la base de données de gestion</span><span class="sxs-lookup"><span data-stu-id="d1331-172">Location of the Management database</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-173">Nom de la base de données SQL Server, nom de l’instance de base de données SQL Server et nom de la base de données.</span><span class="sxs-lookup"><span data-stu-id="d1331-173">SQL Server database name, SQL Server database instance name, and database name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-174">Autorisations de la console de gestion et de la base de données de gestion</span><span class="sxs-lookup"><span data-stu-id="d1331-174">Management console and Management database permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-175">Un utilisateur ou un groupe qui peut accéder à la console de gestion et à la base de données une fois le déploiement terminé.</span><span class="sxs-lookup"><span data-stu-id="d1331-175">A user or group that can access the Management console and database after the deployment is complete.</span></span> <span data-ttu-id="d1331-176">Seuls les utilisateurs ou les groupes peuvent accéder à la console de gestion et à la base de données, sauf si d’autres administrateurs sont ajoutés à l’aide de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="d1331-176">Only these users or groups will have access to the Management console and database unless additional administrators are added by using the Management console.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-177">Nom du site Web du service de gestion</span><span class="sxs-lookup"><span data-stu-id="d1331-177">Management service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-178">Nom du site Web de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="d1331-178">Name for the Management console website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-179">Liaison de port de service de gestion</span><span class="sxs-lookup"><span data-stu-id="d1331-179">Management service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-180">Numéro de port unique pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="d1331-180">Unique port number for the Management service.</span></span> <span data-ttu-id="d1331-181">Ce port ne peut pas être utilisé par un autre processus sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d1331-181">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-182">Microsoft Silverlight 5</span><span class="sxs-lookup"><span data-stu-id="d1331-182">Microsoft Silverlight 5</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-183">La console de gestion est disponible uniquement si Silverlight est installé.</span><span class="sxs-lookup"><span data-stu-id="d1331-183">The Management console is available only if Silverlight is installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="d1331-184">Logiciel requis pour la base de données du serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="d1331-184">Management server database prerequisite software</span></span>

<span data-ttu-id="d1331-185">La base de données de gestion est requise uniquement si vous utilisez le serveur de gestion App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="d1331-185">The Management database is required only if you are using the App-V 5.0 SP3 Management server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-186">Conditions préalables et configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1331-186">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="d1331-187">Détails</span><span class="sxs-lookup"><span data-stu-id="d1331-187">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="d1331-188">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</span><span class="sxs-lookup"><span data-stu-id="d1331-188">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="d1331-189">Packages redistribuables Visual C++ pour Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="d1331-189">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-190">Emplacement d’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="d1331-190">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-191">Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</span><span class="sxs-lookup"><span data-stu-id="d1331-191">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-192">Nom d’instance SQL Server personnalisé (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="d1331-192">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-193">Format à utiliser: <strong> InstanceName</span><span class="sxs-lookup"><span data-stu-id="d1331-193">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="d1331-194">Ce format repose sur l’hypothèse de l’installation sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d1331-194">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="d1331-195">Si vous spécifiez le nom avec le format <strong> SVR\INSTANCE </strong> , l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="d1331-195">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-196">Nom de la base de données personnalisée (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="d1331-196">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-197">Nom unique de la base de données.</span><span class="sxs-lookup"><span data-stu-id="d1331-197">Unique database name.</span></span></p>
<p><span data-ttu-id="d1331-198">Par défaut: AppVManagement</span><span class="sxs-lookup"><span data-stu-id="d1331-198">Default: AppVManagement</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-199">Emplacement du serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="d1331-199">Management server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-200">Compte d’ordinateur sur lequel est déployé le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="d1331-200">Machine account on which the Management server is deployed.</span></span></p>
<p><span data-ttu-id="d1331-201">Format à utiliser: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="d1331-201">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-202">Administrateur d’installation du serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="d1331-202">Management server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-203">Compte utilisé pour installer le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="d1331-203">Account used to install the Management server.</span></span></p>
<p><span data-ttu-id="d1331-204">Format à utiliser: Domain\AdministratorLoginName</span><span class="sxs-lookup"><span data-stu-id="d1331-204">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-205">Agent de service Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="d1331-205">Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-206">Configurez l’ordinateur de base de données de gestion de sorte que le service Microsoft SQL Server agent soit redémarré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d1331-206">Configure the Management database computer so that the Microsoft SQL Server Agent service is restarted automatically.</span></span> <span data-ttu-id="d1331-207">Pour obtenir des instructions, voir <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> configurer l’agent SQL Server pour redémarrer les services automatiquement </a> .</span><span class="sxs-lookup"><span data-stu-id="d1331-207">For instructions, see <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)">Configure SQL Server Agent to Restart Services Automatically</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="d1331-208">Logiciel requis par le serveur de publication</span><span class="sxs-lookup"><span data-stu-id="d1331-208">Publishing server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-209">Conditions préalables et configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1331-209">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="d1331-210">Détails</span><span class="sxs-lookup"><span data-stu-id="d1331-210">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="d1331-211">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</span><span class="sxs-lookup"><span data-stu-id="d1331-211">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="d1331-212">Packages redistribuables Visual C++ pour Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="d1331-212">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-213">64 ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="d1331-213">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-214">Rôle du serveur Web Windows Server</span><span class="sxs-lookup"><span data-stu-id="d1331-214">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-215">Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="d1331-215">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-216">Outils de gestion du serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="d1331-216">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-217">Cliquez sur <strong> scripts et outils de gestion IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="d1331-217">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-218">Services de rôle de serveur Web</span><span class="sxs-lookup"><span data-stu-id="d1331-218">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d1331-219">Fonctionnalités HTTP communes:</span><span class="sxs-lookup"><span data-stu-id="d1331-219">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-220">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="d1331-220">Static Content</span></span></p></li>
<li><p><span data-ttu-id="d1331-221">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="d1331-221">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="d1331-222">Développement d’applications:</span><span class="sxs-lookup"><span data-stu-id="d1331-222">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-223">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="d1331-223">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="d1331-224">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="d1331-224">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="d1331-225">Extensions ISAPI</span><span class="sxs-lookup"><span data-stu-id="d1331-225">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="d1331-226">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="d1331-226">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="d1331-227">Sûreté</span><span class="sxs-lookup"><span data-stu-id="d1331-227">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-228">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="d1331-228">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="d1331-229">Filtrage de requête</span><span class="sxs-lookup"><span data-stu-id="d1331-229">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="d1331-230">Outils de gestion:</span><span class="sxs-lookup"><span data-stu-id="d1331-230">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-231">Console de gestion IIS</span><span class="sxs-lookup"><span data-stu-id="d1331-231">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-232">Emplacement d’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="d1331-232">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-233">Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</span><span class="sxs-lookup"><span data-stu-id="d1331-233">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-234">URL du service de gestion</span><span class="sxs-lookup"><span data-stu-id="d1331-234">Management service URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-235">URL du service de gestion App-V.</span><span class="sxs-lookup"><span data-stu-id="d1331-235">URL of the App-V Management service.</span></span> <span data-ttu-id="d1331-236">Il s’agit du port sur lequel communiquer le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="d1331-236">This is the port with which the Publishing server communicates.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-237">Architecture d’installation</span><span class="sxs-lookup"><span data-stu-id="d1331-237">Installation architecture</span></span></th>
<th align="left"><span data-ttu-id="d1331-238">Format à utiliser pour l’URL</span><span class="sxs-lookup"><span data-stu-id="d1331-238">Format to use for the URL</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-239">Serveur de gestion et serveur de publication installés sur le même serveur</span><span class="sxs-lookup"><span data-stu-id="d1331-239">Management server and Publishing server are installed on the same server</span></span></p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-240">Serveur de gestion et serveur de publication installés sur différents serveurs</span><span class="sxs-lookup"><span data-stu-id="d1331-240">Management server and Publishing server are installed on different servers</span></span></p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-241">Nom du site Web du service de publication</span><span class="sxs-lookup"><span data-stu-id="d1331-241">Publishing service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-242">Nom du site Web de publication.</span><span class="sxs-lookup"><span data-stu-id="d1331-242">Name for the Publishing website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-243">Liaison de port de service de publication</span><span class="sxs-lookup"><span data-stu-id="d1331-243">Publishing service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-244">Numéro de port unique pour le service de publication.</span><span class="sxs-lookup"><span data-stu-id="d1331-244">Unique port number for the Publishing service.</span></span> <span data-ttu-id="d1331-245">Ce port ne peut pas être utilisé par un autre processus sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d1331-245">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="d1331-246">Logiciels requis par le serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="d1331-246">Reporting server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-247">Conditions préalables et configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1331-247">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="d1331-248">Détails</span><span class="sxs-lookup"><span data-stu-id="d1331-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-249">Version prise en charge de SQL Server</span><span class="sxs-lookup"><span data-stu-id="d1331-249">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-250">Pour les versions prises en charge, voir <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> Configurations prises en charge par App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="d1331-250">For supported versions, see <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">App-V 5.0 SP3 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="d1331-251">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</span><span class="sxs-lookup"><span data-stu-id="d1331-251">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="d1331-252">Packages redistribuables Visual C++ pour Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="d1331-252">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-253">64 ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="d1331-253">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-254">Rôle du serveur Web Windows Server</span><span class="sxs-lookup"><span data-stu-id="d1331-254">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-255">Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="d1331-255">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-256">Outils de gestion du serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="d1331-256">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-257">Cliquez sur <strong> scripts et outils de gestion IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="d1331-257">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-258">Services de rôle de serveur Web</span><span class="sxs-lookup"><span data-stu-id="d1331-258">Web Server Role Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-259">Pour réduire le risque de transfert de données indésirables ou malveillantes sur le serveur de création de rapports, vous devez limiter l’accès au service Web de création de rapports par votre stratégie de sécurité d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d1331-259">To reduce the risk of unwanted or malicious data being sent to the Reporting server, you should restrict access to the Reporting Web Service per your corporate security policy.</span></span></p>
<p><strong><span data-ttu-id="d1331-260">Fonctionnalités HTTP communes:</span><span class="sxs-lookup"><span data-stu-id="d1331-260">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-261">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="d1331-261">Static Content</span></span></p></li>
<li><p><span data-ttu-id="d1331-262">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="d1331-262">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="d1331-263">Développement d’applications:</span><span class="sxs-lookup"><span data-stu-id="d1331-263">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-264">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="d1331-264">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="d1331-265">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="d1331-265">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="d1331-266">Extensions ISAPI</span><span class="sxs-lookup"><span data-stu-id="d1331-266">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="d1331-267">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="d1331-267">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="d1331-268">Sûreté</span><span class="sxs-lookup"><span data-stu-id="d1331-268">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-269">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="d1331-269">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="d1331-270">Filtrage de requête</span><span class="sxs-lookup"><span data-stu-id="d1331-270">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="d1331-271">Outils de gestion:</span><span class="sxs-lookup"><span data-stu-id="d1331-271">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="d1331-272">Console de gestion IIS</span><span class="sxs-lookup"><span data-stu-id="d1331-272">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-273">Emplacement d’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="d1331-273">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-274">Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</span><span class="sxs-lookup"><span data-stu-id="d1331-274">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-275">Nom du site Web de service de création de rapports</span><span class="sxs-lookup"><span data-stu-id="d1331-275">Reporting service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-276">Nom du site Web de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="d1331-276">Name for the Reporting website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-277">Liaison de port de service de création de rapports</span><span class="sxs-lookup"><span data-stu-id="d1331-277">Reporting service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-278">Numéro de port unique pour le service de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="d1331-278">Unique port number for the Reporting service.</span></span> <span data-ttu-id="d1331-279">Ce port ne peut pas être utilisé par un autre processus sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d1331-279">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="d1331-280">Logiciel requis pour la création de rapports</span><span class="sxs-lookup"><span data-stu-id="d1331-280">Reporting database prerequisite software</span></span>

<span data-ttu-id="d1331-281">La base de données de création de rapports est requise uniquement si vous utilisez le serveur de création de rapports App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="d1331-281">The Reporting database is required only if you are using the App-V 5.0 SP3 Reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-282">Conditions préalables et configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1331-282">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="d1331-283">Détails</span><span class="sxs-lookup"><span data-stu-id="d1331-283">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="d1331-284">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</span><span class="sxs-lookup"><span data-stu-id="d1331-284">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="d1331-285">Packages redistribuables Visual C++ pour Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="d1331-285">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-286">Emplacement d’installation par défaut</span><span class="sxs-lookup"><span data-stu-id="d1331-286">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-287">Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</span><span class="sxs-lookup"><span data-stu-id="d1331-287">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-288">Nom d’instance SQL Server personnalisé (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="d1331-288">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-289">Format à utiliser: <strong> InstanceName</span><span class="sxs-lookup"><span data-stu-id="d1331-289">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="d1331-290">Ce format repose sur l’hypothèse de l’installation sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d1331-290">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="d1331-291">Si vous spécifiez le nom avec le format <strong> SVR\INSTANCE </strong> , l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="d1331-291">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-292">Nom de la base de données personnalisée (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="d1331-292">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-293">Nom unique de la base de données.</span><span class="sxs-lookup"><span data-stu-id="d1331-293">Unique database name.</span></span></p>
<p><span data-ttu-id="d1331-294">Par défaut: AppVReporting</span><span class="sxs-lookup"><span data-stu-id="d1331-294">Default: AppVReporting</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-295">Emplacement du serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="d1331-295">Reporting server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-296">Compte d’ordinateur sur lequel est déployé le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="d1331-296">Machine account on which the Reporting server is deployed.</span></span></p>
<p><span data-ttu-id="d1331-297">Format à utiliser: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="d1331-297">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1331-298">Administrateur d’installation du serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="d1331-298">Reporting server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-299">Compte utilisé pour installer le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="d1331-299">Account used to install the Reporting server.</span></span></p>
<p><span data-ttu-id="d1331-300">Format à utiliser: Domain\AdministratorLoginName</span><span class="sxs-lookup"><span data-stu-id="d1331-300">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d1331-301">Service Microsoft SQL Server et agent de service Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="d1331-301">Microsoft SQL Server Service and Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="d1331-302">Configurez ces services à associer aux comptes d’utilisateurs qui ont accès à la requête AD DS.</span><span class="sxs-lookup"><span data-stu-id="d1331-302">Configure these services to be associated with user accounts that have access to query AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d1331-303">Logiciel requis pour les clients App-V</span><span class="sxs-lookup"><span data-stu-id="d1331-303">App-V client prerequisite software</span></span>


<span data-ttu-id="d1331-304">Installez les logiciels requis suivants pour le client App-V.</span><span class="sxs-lookup"><span data-stu-id="d1331-304">Install the following prerequisite software for the App-V client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-305">Prérequises</span><span class="sxs-lookup"><span data-stu-id="d1331-305">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="d1331-306">Détails</span><span class="sxs-lookup"><span data-stu-id="d1331-306">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="d1331-307">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</span><span class="sxs-lookup"><span data-stu-id="d1331-307">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="d1331-308">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="d1331-308">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="d1331-309">L’installation de PowerShell 3,0 nécessite un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="d1331-309">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="d1331-310">KB2533623</span><span class="sxs-lookup"><span data-stu-id="d1331-310">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d1331-311">S’applique à Windows 7 uniquement: Télécharger et installer la Ko.</span><span class="sxs-lookup"><span data-stu-id="d1331-311">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="d1331-312">Packages redistribuables Visual C++ pour Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="d1331-312">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d1331-313">Logiciels requis du client de services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="d1331-313">Remote Desktop Services client prerequisite software</span></span>


<span data-ttu-id="d1331-314">Installez les logiciels requis suivants pour le client App-V Remote Desktop Services.</span><span class="sxs-lookup"><span data-stu-id="d1331-314">Install the following prerequisite software for the App-V Remote Desktop Services client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-315">Prérequises</span><span class="sxs-lookup"><span data-stu-id="d1331-315">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="d1331-316">Détails</span><span class="sxs-lookup"><span data-stu-id="d1331-316">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="d1331-317">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</span><span class="sxs-lookup"><span data-stu-id="d1331-317">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="d1331-318">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="d1331-318">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="d1331-319">L’installation de PowerShell 3,0 nécessite un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="d1331-319">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="d1331-320">KB2533623</span><span class="sxs-lookup"><span data-stu-id="d1331-320">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d1331-321">S’applique à Windows 7 uniquement: Télécharger et installer la Ko.</span><span class="sxs-lookup"><span data-stu-id="d1331-321">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="d1331-322">Packages redistribuables Visual C++ pour Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="d1331-322">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d1331-323">Logiciels requis par le Sequencer</span><span class="sxs-lookup"><span data-stu-id="d1331-323">Sequencer prerequisite software</span></span>


**<span data-ttu-id="d1331-324">Éléments à connaître avant d’installer la configuration requise:</span><span class="sxs-lookup"><span data-stu-id="d1331-324">What to know before installing the prerequisites:</span></span>**

-   <span data-ttu-id="d1331-325">Meilleure pratique: l’ordinateur qui exécute le Sequencer doit présenter les mêmes configurations matérielle et logicielle que les ordinateurs exécutant les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="d1331-325">Best practice: The computer that runs the Sequencer should have the same hardware and software configurations as the computers that will run the virtual applications.</span></span>

-   <span data-ttu-id="d1331-326">Le processus de séquençage est gourmand en ressources; il est donc important de veiller à ce que l’ordinateur qui exécute le Sequencer dispose de suffisamment de mémoire, d’un processeur rapide et d’un disque dur rapide.</span><span class="sxs-lookup"><span data-stu-id="d1331-326">The sequencing process is resource intensive, so make sure that the computer that runs the Sequencer has plenty of memory, a fast processor, and a fast hard drive.</span></span> <span data-ttu-id="d1331-327">La configuration requise pour les applications installées localement ne peut pas dépasser celle du Sequencer.</span><span class="sxs-lookup"><span data-stu-id="d1331-327">The system requirements of locally installed applications cannot exceed those of the Sequencer.</span></span> <span data-ttu-id="d1331-328">Pour plus d’informations, voir [configurations App-V 5,0 prises en charge](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="d1331-328">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1331-329">Prérequises</span><span class="sxs-lookup"><span data-stu-id="d1331-329">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="d1331-330">Détails</span><span class="sxs-lookup"><span data-stu-id="d1331-330">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="d1331-331">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</span><span class="sxs-lookup"><span data-stu-id="d1331-331">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="d1331-332">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="d1331-332">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="d1331-333">L’installation de PowerShell 3,0 nécessite un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="d1331-333">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="d1331-334">KB2533623</span><span class="sxs-lookup"><span data-stu-id="d1331-334">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d1331-335">S’applique à Windows 7 uniquement: Télécharger et installer la Ko.</span><span class="sxs-lookup"><span data-stu-id="d1331-335">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="d1331-336">Packages redistribuables Visual C++ pour Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="d1331-336">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="d1331-337">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1331-337">Related topics</span></span>


[<span data-ttu-id="d1331-338">Planification d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="d1331-338">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)

[<span data-ttu-id="d1331-339">Configurations prises en charge d'App-V5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="d1331-339">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)










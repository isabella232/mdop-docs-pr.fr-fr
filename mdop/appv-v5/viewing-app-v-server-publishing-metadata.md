---
title: Affichage des métadonnées de publication du serveur App-V
description: Affichage des métadonnées de publication du serveur App-V
author: dansimp
ms.assetid: 048dd42a-24d4-4cc4-81f6-7a919aadd9b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 304aa656de98a0c9d59f0a6166811ead911033ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804848"
---
# <span data-ttu-id="ca54b-103">Affichage des métadonnées de publication du serveur App-V</span><span class="sxs-lookup"><span data-stu-id="ca54b-103">Viewing App-V Server Publishing Metadata</span></span>


<span data-ttu-id="ca54b-104">Utilisez cette procédure pour afficher les métadonnées de publication, qui peuvent vous aider à résoudre les problèmes liés à la publication.</span><span class="sxs-lookup"><span data-stu-id="ca54b-104">Use this procedure to view publishing metadata, which can help you resolve publishing-related issues.</span></span> <span data-ttu-id="ca54b-105">Pour utiliser cette procédure, vous devez utiliser le serveur de gestion App-V.</span><span class="sxs-lookup"><span data-stu-id="ca54b-105">You must be using the App-V Management server to use this procedure.</span></span>

<span data-ttu-id="ca54b-106">Cet article contient les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ca54b-106">This article contains the following information:</span></span>

-   [<span data-ttu-id="ca54b-107">Configuration requise pour App-V 5,0 SP3 pour afficher les métadonnées de publication</span><span class="sxs-lookup"><span data-stu-id="ca54b-107">App-V 5.0 SP3 requirements for viewing publishing metadata</span></span>](#bkmk-50sp3-reqs-pub-meta)

-   [<span data-ttu-id="ca54b-108">Syntaxe à utiliser pour afficher les métadonnées de publication</span><span class="sxs-lookup"><span data-stu-id="ca54b-108">Syntax to use for viewing publishing metadata</span></span>](#bkmk-syntax-view-pub-meta)

-   [<span data-ttu-id="ca54b-109">Valeurs de requête pour le système d’exploitation client et version</span><span class="sxs-lookup"><span data-stu-id="ca54b-109">Query values for client operating system and version</span></span>](#bkmk-values-query-pub-meta)

-   [<span data-ttu-id="ca54b-110">Définition des métadonnées de publication</span><span class="sxs-lookup"><span data-stu-id="ca54b-110">Definition of publishing metadata</span></span>](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-50sp3-reqs-pub-meta"></a><span data-ttu-id="ca54b-111">Configuration requise pour App-V 5,0 SP3 pour afficher les métadonnées de publication</span><span class="sxs-lookup"><span data-stu-id="ca54b-111">App-V 5.0 SP3 requirements for viewing publishing metadata</span></span>


<span data-ttu-id="ca54b-112">Dans App-V 5,0 SP3, vous devez fournir les valeurs suivantes dans l’adresse lorsque vous interrogez le serveur de publication App-V pour les métadonnées:</span><span class="sxs-lookup"><span data-stu-id="ca54b-112">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ca54b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca54b-113">Value</span></span></th>
<th align="left"><span data-ttu-id="ca54b-114">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ca54b-114">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ca54b-115">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="ca54b-115">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ca54b-116">Si vous omettez le <strong> </strong> paramètre ClientVersion de la requête, les métadonnées excluent les nouvelles fonctionnalités d’App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="ca54b-116">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ca54b-117">Clientos</span><span class="sxs-lookup"><span data-stu-id="ca54b-117">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ca54b-118">Vous devez renseigner cette valeur uniquement si vous sélectionnez des systèmes d’exploitation de clients spécifiques lors du séquencé du package.</span><span class="sxs-lookup"><span data-stu-id="ca54b-118">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="ca54b-119">Si vous sélectionnez la valeur par défaut (tous les systèmes d’exploitation), ne spécifiez pas cette valeur dans la requête.</span><span class="sxs-lookup"><span data-stu-id="ca54b-119">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="ca54b-120">Si vous omettez le <strong> paramètre clientos </strong> dans la requête, seuls les packages qui ont été séquencés pour prendre en charge tout système d’exploitation apparaissent dans les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ca54b-120">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a><span data-ttu-id="ca54b-121">Syntaxe de requête pour afficher les métadonnées de publication</span><span class="sxs-lookup"><span data-stu-id="ca54b-121">Query syntax for viewing publishing metadata</span></span>


<span data-ttu-id="ca54b-122">Le tableau suivant répertorie les exemples de syntaxe et de requête.</span><span class="sxs-lookup"><span data-stu-id="ca54b-122">The following table provides the syntax and query examples.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ca54b-123">Version de App-V</span><span class="sxs-lookup"><span data-stu-id="ca54b-123">Version of App-V</span></span></th>
<th align="left"><span data-ttu-id="ca54b-124">Syntaxe de requête</span><span class="sxs-lookup"><span data-stu-id="ca54b-124">Query syntax</span></span></th>
<th align="left"><span data-ttu-id="ca54b-125">Descriptions des paramètres</span><span class="sxs-lookup"><span data-stu-id="ca54b-125">Parameter descriptions</span></span></th>
<th align="left"><span data-ttu-id="ca54b-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="ca54b-126">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca54b-127">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="ca54b-127">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ca54b-128">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ca54b-128">Parameter</span></span></th>
<th align="left"><span data-ttu-id="ca54b-129">Description</span><span class="sxs-lookup"><span data-stu-id="ca54b-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca54b-130">&lt;PubServer&gt;</span><span class="sxs-lookup"><span data-stu-id="ca54b-130">&lt;PubServer&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-131">Nom du serveur de publication App-V.</span><span class="sxs-lookup"><span data-stu-id="ca54b-131">Name of the App-V Publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca54b-132">&lt;Port de publication #&gt;</span><span class="sxs-lookup"><span data-stu-id="ca54b-132">&lt;Publishing Port#&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-133">Transférez le port vers le serveur de publication App-V que vous avez défini lors de la configuration du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="ca54b-133">Port to the App-V Publishing server, which you defined when you configured the Publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca54b-134">ClientVersion = &lt; AppvClientVersion&gt;</span><span class="sxs-lookup"><span data-stu-id="ca54b-134">ClientVersion=&lt;AppvClientVersion&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-135">Version du client App-V.</span><span class="sxs-lookup"><span data-stu-id="ca54b-135">Version of the App-V client.</span></span> <span data-ttu-id="ca54b-136">Pour obtenir la valeur correcte à utiliser, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ca54b-136">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca54b-137">Clientos = &lt; OSStringValue&gt;</span><span class="sxs-lookup"><span data-stu-id="ca54b-137">ClientOS=&lt;OSStringValue&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-138">Système d’exploitation de l’ordinateur qui exécute le client App-V.</span><span class="sxs-lookup"><span data-stu-id="ca54b-138">Operating system of the computer that is running the App-V client.</span></span> <span data-ttu-id="ca54b-139">Pour obtenir la valeur correcte à utiliser, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ca54b-139">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p><span data-ttu-id="ca54b-140">Pour obtenir le nom du serveur de publication et le numéro de port (http:// &lt; PubServer &gt; : port de &lt; publication # &gt; ) à partir du client App-V, observez la configuration d’URL de l’applet de passe <strong> PowerShell Get-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="ca54b-140">To get the name of the Publishing server and the port number (http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;) from the App-V Client, look at the URL configuration of the <strong>Get-AppvPublishingServer</strong> PowerShell cmdlet.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p><span data-ttu-id="ca54b-141">Dans l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="ca54b-141">In the example:</span></span></p>
<ul>
<li><p><span data-ttu-id="ca54b-142">Un Windows Server 2012 R2 nommé «pubsvr01» héberge le service de publication.</span><span class="sxs-lookup"><span data-stu-id="ca54b-142">A Windows Server 2012 R2 named “pubsvr01” hosts the Publishing service.</span></span></p></li>
<li><p><span data-ttu-id="ca54b-143">Le client Windows est Windows 8,1 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ca54b-143">The Windows client is Windows 8.1 64-bit.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca54b-144">App-V 5,0 via App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="ca54b-144">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong><span data-ttu-id="ca54b-145">Remarque</span><span class="sxs-lookup"><span data-stu-id="ca54b-145">Note</span></span></strong><br/><p><strong><span data-ttu-id="ca54b-146">ClientVersion </strong> et les <strong> clients </strong> y sont uniquement pris en charge dans App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="ca54b-146">ClientVersion</strong> and <strong>ClientOS</strong> are supported only in App-V 5.0 SP3.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="ca54b-147">Voir les informations pour App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="ca54b-147">See the information for App-V 5.0 SP3.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p><span data-ttu-id="ca54b-148">Dans l’exemple, un Windows Server 2012 R2 nommé «pubsvr01» héberge les services de gestion et de publication.</span><span class="sxs-lookup"><span data-stu-id="ca54b-148">In the example, A Windows Server 2012 R2 named “pubsvr01” hosts the Management and Publishing services.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a><span data-ttu-id="ca54b-149">Valeurs de requête pour le système d’exploitation client et version</span><span class="sxs-lookup"><span data-stu-id="ca54b-149">Query values for client operating system and version</span></span>


<span data-ttu-id="ca54b-150">Dans votre requête de métadonnées de publication, entrez les valeurs de chaîne correspondant au système d’exploitation du client et à la version que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="ca54b-150">In your publishing metadata query, enter the string values that correspond to the client operating system and version that you’re using.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ca54b-151">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ca54b-151">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ca54b-152">Architecture</span><span class="sxs-lookup"><span data-stu-id="ca54b-152">Architecture</span></span></th>
<th align="left"><span data-ttu-id="ca54b-153">Valeur de chaîne d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ca54b-153">Operating string string value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca54b-154">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ca54b-154">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-155">64 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-155">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-156">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="ca54b-156">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca54b-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ca54b-157">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-158">32 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-158">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-159">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="ca54b-159">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca54b-160">Windows8</span><span class="sxs-lookup"><span data-stu-id="ca54b-160">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-161">64 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-161">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-162">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="ca54b-162">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca54b-163">Windows8</span><span class="sxs-lookup"><span data-stu-id="ca54b-163">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-164">32 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-164">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-165">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="ca54b-165">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca54b-166">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="ca54b-166">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-167">64 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-167">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-168">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="ca54b-168">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca54b-169">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="ca54b-169">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-170">32 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-170">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-171">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="ca54b-171">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca54b-172">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="ca54b-172">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-173">64 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-173">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-174">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="ca54b-174">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca54b-175">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="ca54b-175">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-176">32 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-176">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-177">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="ca54b-177">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca54b-178">Windows7</span><span class="sxs-lookup"><span data-stu-id="ca54b-178">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-179">64 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-179">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-180">WindowsClient_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="ca54b-180">WindowsClient_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca54b-181">Windows7</span><span class="sxs-lookup"><span data-stu-id="ca54b-181">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-182">32 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-182">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-183">WindowsClient_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="ca54b-183">WindowsClient_6.1_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca54b-184">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="ca54b-184">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-185">64 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-185">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-186">WindowsServer_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="ca54b-186">WindowsServer_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca54b-187">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="ca54b-187">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-188">32 bits</span><span class="sxs-lookup"><span data-stu-id="ca54b-188">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca54b-189">WindowsServer_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="ca54b-189">WindowsServer_6.1_x86</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a><span data-ttu-id="ca54b-190">Définition des métadonnées de publication</span><span class="sxs-lookup"><span data-stu-id="ca54b-190">Definition of publishing metadata</span></span>


<span data-ttu-id="ca54b-191">Lors de la publication de packages sur un ordinateur exécutant le client App-V, des métadonnées sont envoyées à cet ordinateur pour indiquer les packages et groupes de connexion en cours de publication.</span><span class="sxs-lookup"><span data-stu-id="ca54b-191">When packages are published to a computer that is running the App-V client, metadata is sent to that computer indicating which packages and connection groups are being published.</span></span> <span data-ttu-id="ca54b-192">Le client App-V effectue deux requêtes distinctes pour ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="ca54b-192">The App-V Client makes two separate requests for the following:</span></span>

-   <span data-ttu-id="ca54b-193">Des packages et des groupes de connexion habilités à l’ordinateur client;</span><span class="sxs-lookup"><span data-stu-id="ca54b-193">Packages and connection groups that are entitled to the client computer.</span></span>

-   <span data-ttu-id="ca54b-194">Des packages et des groupes de connexion qui sont habilités à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="ca54b-194">Packages and connection groups that are entitled to the current user.</span></span>

<span data-ttu-id="ca54b-195">Le serveur de publication communique avec le serveur de gestion pour déterminer les packages et groupes de connexion disponibles pour le demandeur.</span><span class="sxs-lookup"><span data-stu-id="ca54b-195">The Publishing server communicates with the Management server to determine which packages and connection groups are available to the requester.</span></span> <span data-ttu-id="ca54b-196">Pour pouvoir générer les métadonnées, le serveur de publication doit être inscrit auprès du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="ca54b-196">The Publishing server must be registered with the Management server in order for the metadata to be generated.</span></span>

<span data-ttu-id="ca54b-197">Vous pouvez afficher les métadonnées de chaque requête dans un navigateur Internet à l’aide d’une requête qui se trouve dans le contexte de l’utilisateur ou de l’ordinateur en particulier.</span><span class="sxs-lookup"><span data-stu-id="ca54b-197">You can view the metadata for each request in an Internet browser by using a query that is in the context of the specific user or computer.</span></span>






## <span data-ttu-id="ca54b-198">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca54b-198">Related topics</span></span>


[<span data-ttu-id="ca54b-199">Référence technique pour App-V5.0</span><span class="sxs-lookup"><span data-stu-id="ca54b-199">Technical Reference for App-V 5.0</span></span>](technical-reference-for-app-v-50.md)










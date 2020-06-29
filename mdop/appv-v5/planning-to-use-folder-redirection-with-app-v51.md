---
title: Envisager l'utilisation de la redirection des dossiers avec App-V
description: Envisager l'utilisation de la redirection des dossiers avec App-V
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804938"
---
# <span data-ttu-id="f1415-103">Envisager l'utilisation de la redirection des dossiers avec App-V</span><span class="sxs-lookup"><span data-stu-id="f1415-103">Planning to Use Folder Redirection with App-V</span></span>


<span data-ttu-id="f1415-104">Microsoft Application Virtualization (App-V) 5,1 prend en charge l’utilisation de la redirection de dossiers, une fonctionnalité qui permet aux utilisateurs et aux administrateurs de rediriger le chemin d’accès d’un dossier vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="f1415-104">Microsoft Application Virtualization (App-V) 5.1 supports the use of folder redirection, a feature that enables users and administrators to redirect the path of a folder to a new location.</span></span>

<span data-ttu-id="f1415-105">Cette rubrique contient les sections suivantes:</span><span class="sxs-lookup"><span data-stu-id="f1415-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f1415-106">Configuration requise pour l’utilisation de la redirection de dossiers</span><span class="sxs-lookup"><span data-stu-id="f1415-106">Requirements for using folder redirection</span></span>](#bkmk-folder-redir-reqs)

-   [<span data-ttu-id="f1415-107">Configuration de la redirection de dossiers pour une utilisation avec App-V</span><span class="sxs-lookup"><span data-stu-id="f1415-107">How to configure folder redirection for use with App-V</span></span>](#bkmk-folder-redir-cfg)

-   [<span data-ttu-id="f1415-108">Fonctionnement de la redirection de dossiers avec App-V</span><span class="sxs-lookup"><span data-stu-id="f1415-108">How folder redirection works with App-V</span></span>](#bkmk-folder-redir-works)

-   [<span data-ttu-id="f1415-109">Présentation de la redirection de dossiers</span><span class="sxs-lookup"><span data-stu-id="f1415-109">Overview of folder redirection</span></span>](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a><span data-ttu-id="f1415-110">Configurations requises et scénarios non pris en charge pour l’utilisation de la redirection de dossiers</span><span class="sxs-lookup"><span data-stu-id="f1415-110">Requirements and unsupported scenarios for using folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1415-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1415-111">Requirements</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1415-112">Pour utiliser la redirection de dossiers% AppData%, vous devez effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="f1415-112">To use %AppData% folder redirection, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1415-113">Disposent d’un package App-V doté d’un dossier de système de fichiers virtuel AppData (VFS).</span><span class="sxs-lookup"><span data-stu-id="f1415-113">Have an App-V package that has an AppData virtual file system (VFS) folder.</span></span></p></li>
<li><p><span data-ttu-id="f1415-114">Activez la redirection de dossier et redirigez les dossiers des utilisateurs vers un dossier partagé, généralement un dossier réseau.</span><span class="sxs-lookup"><span data-stu-id="f1415-114">Enable folder redirection and redirect users’ folders to a shared folder, typically a network folder.</span></span></p></li>
<li><p><span data-ttu-id="f1415-115">Accédez à l’un ou l’autre des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="f1415-115">Roam both or neither of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1415-116">Fichiers sous%appdata%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="f1415-116">Files under %appdata%\Microsoft\AppV\Client\Catalog</span></span></p></li>
<li><p><span data-ttu-id="f1415-117">Paramètres du Registre sous HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</span><span class="sxs-lookup"><span data-stu-id="f1415-117">Registry settings under HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages</span></span></p>
<p><span data-ttu-id="f1415-118">Pour plus d’informations, consultez la rubrique <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> publication d’applications et interactions client </a> .</span><span class="sxs-lookup"><span data-stu-id="f1415-118">For more detail, see <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)">Application Publishing and Client Interaction</a>.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="f1415-119">Vérifiez que les dossiers suivants sont disponibles pour chaque utilisateur qui se connecte à l’ordinateur exécutant le client App-V 5,0 SP2 ou version ultérieure:</span><span class="sxs-lookup"><span data-stu-id="f1415-119">Ensure that the following folders are available to each user who logs into the computer that is running the App-V 5.0 SP2 or later client:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1415-120">% AppData% est configuré sur l’emplacement réseau souhaité (avec ou sans <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> prise en charge des fichiers hors connexion </a> ).</span><span class="sxs-lookup"><span data-stu-id="f1415-120">%AppData% is configured to the desired network location (with or without <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)">Offline Files</a> support).</span></span></p></li>
<li><p><span data-ttu-id="f1415-121">% LocalAppData% est configuré dans le dossier local souhaité.</span><span class="sxs-lookup"><span data-stu-id="f1415-121">%LocalAppData% is configured to the desired local folder.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1415-122">Scénarios non pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1415-122">Unsupported scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f1415-123">Configuration de% LocalAppData% en tant que lecteur réseau.</span><span class="sxs-lookup"><span data-stu-id="f1415-123">Configuring %LocalAppData% as a network drive.</span></span></p></li>
<li><p><span data-ttu-id="f1415-124">Redirection du menu Démarrer vers un dossier unique pour plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f1415-124">Redirecting the Start menu to a single folder for multiple users.</span></span></p></li>
<li><p><span data-ttu-id="f1415-125">En cas d’itinérance (% AppData%) est redirigé vers un partage réseau qui n’est pas disponible, les applications App-V ne peuvent pas se lancer comme suit:</span><span class="sxs-lookup"><span data-stu-id="f1415-125">If roaming AppData (%AppData%) is redirected to a network share that is not available, App-V applications will fail to launch as follows:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1415-126">Version App-V</span><span class="sxs-lookup"><span data-stu-id="f1415-126">App-V version</span></span></th>
<th align="left"><span data-ttu-id="f1415-127">Description du scénario</span><span class="sxs-lookup"><span data-stu-id="f1415-127">Scenario description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1415-128">Dans l’App-V 5,0 via App-V 5,0 SP2 plus de correctifs</span><span class="sxs-lookup"><span data-stu-id="f1415-128">In App-V 5.0 through App-V 5.0 SP2 plus hotfixes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1415-129">Ce problème survient, que l’activation des fichiers hors connexion soit activée ou non.</span><span class="sxs-lookup"><span data-stu-id="f1415-129">This failure will occur regardless of whether Offline Files is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1415-130">Dans l’App-V 5,0 SP3 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="f1415-130">In App-V 5.0 SP3 and later</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1415-131">Si le partage réseau non disponible a été activé pour les fichiers en mode hors connexion, l’application application-V s’exécutera correctement.</span><span class="sxs-lookup"><span data-stu-id="f1415-131">If the unavailable network share has been enabled for Offline Files, the App-V application will start successfully.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a><span data-ttu-id="f1415-132">Configuration de la redirection de dossiers pour une utilisation avec App-V</span><span class="sxs-lookup"><span data-stu-id="f1415-132">How to configure folder redirection for use with App-V</span></span>


<span data-ttu-id="f1415-133">La redirection de dossiers peut être appliquée à différents dossiers tels que le bureau, mes documents, mes images, etc. Toutefois, le seul dossier ayant un impact sur l’utilisation des applications App-V est le dossier AppData itinérance de l’utilisateur (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="f1415-133">Folder redirection can be applied to different folders, such as Desktop, My Documents, My Pictures, etc. However, the only folder that impacts the use of App-V applications is the user’s roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="f1415-134">Vous pouvez appliquer la redirection de dossiers à n’importe quel autre dossier pris en charge sans impact sur App-V.</span><span class="sxs-lookup"><span data-stu-id="f1415-134">You can apply folder redirection to any other supported folders without impacting App-V.</span></span>

## <a href="" id="bkmk-folder-redir-works"></a><span data-ttu-id="f1415-135">Fonctionnement de la redirection de dossiers avec App-V</span><span class="sxs-lookup"><span data-stu-id="f1415-135">How folder redirection works with App-V</span></span>


<span data-ttu-id="f1415-136">Le tableau suivant décrit le fonctionnement de la redirection de dossier lorsque% AppData% est redirigé vers un réseau et lorsque vous remplissez les conditions mentionnées plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="f1415-136">The following table describes how folder redirection works when %AppData% is redirected to a network and when you have met the requirements listed earlier in this article.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f1415-137">État de l’environnement virtuel</span><span class="sxs-lookup"><span data-stu-id="f1415-137">Virtual environment state</span></span></th>
<th align="left"><span data-ttu-id="f1415-138">Action qui se produit</span><span class="sxs-lookup"><span data-stu-id="f1415-138">Action that occurs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1415-139">Au démarrage de l’environnement virtuel</span><span class="sxs-lookup"><span data-stu-id="f1415-139">When the virtual environment starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1415-140">Le dossier de système de fichiers virtuel (VFS) est mappé au dossier AppData Local (% LocalAppData%) au lieu de se répartir sur le dossier AppData itinérance de l’utilisateur (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="f1415-140">The virtual file system (VFS) AppData folder is mapped to the local AppData folder (%LocalAppData%) instead of to the user’s roaming AppData folder (%AppData%).</span></span></p>
<ul>
<li><p><span data-ttu-id="f1415-141">LocalAppData contient un cache local du dossier AppData errant de l’utilisateur pour le package en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f1415-141">LocalAppData contains a local cache of the user’s roaming AppData folder for the package in use.</span></span> <span data-ttu-id="f1415-142">Le cache local se trouve sous les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="f1415-142">The local cache is located under:</span></span></p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p><span data-ttu-id="f1415-143">Les données les plus récentes du dossier d’itinérance de l’utilisateur sont copiées dans et remplacent les données actuellement présentes dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="f1415-143">The latest data from the user’s roaming AppData folder is copied to and replaces the data currently in the local cache.</span></span></p></li>
<li><p><span data-ttu-id="f1415-144">Lorsque l’environnement virtuel est en cours d’exécution, les données continuent d’être enregistrées dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="f1415-144">While the virtual environment is running, data continues to be saved to the local cache.</span></span> <span data-ttu-id="f1415-145">Les données ne sont fournies qu’à partir de% LocalAppData% et ne sont pas déplacées ou synchronisées avec% AppData% tant que l’utilisateur final n’a pas arrêté l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f1415-145">Data is served only out of %LocalAppData% and is not moved or synchronized with %AppData% until the end user shuts down the computer.</span></span></p></li>
<li><p><span data-ttu-id="f1415-146">Les entrées du dossier AppData sont créées à l’aide du contexte de l’utilisateur et non du contexte du système.</span><span class="sxs-lookup"><span data-stu-id="f1415-146">Entries to the AppData folder are made using the user context, not the system context.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="f1415-147">Remarque</span><span class="sxs-lookup"><span data-stu-id="f1415-147">Note</span></span></strong><br/><p><span data-ttu-id="f1415-148">La redirection de dossiers du client App-V ne peut pas déplacer les fichiers de% AppData% vers% LocalAppData%.</span><span class="sxs-lookup"><span data-stu-id="f1415-148">The App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%.</span></span> <span data-ttu-id="f1415-149">Consultez <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> les notes de publication pour App-V 5,0 SP2 </a> .</span><span class="sxs-lookup"><span data-stu-id="f1415-149">See <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)">Release Notes for App-V 5.0 SP2</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1415-150">Lorsque l’environnement virtuel s’arrête</span><span class="sxs-lookup"><span data-stu-id="f1415-150">When the virtual environment shuts down</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1415-151">Les données mises en cache locales dans AppData (itinérance) sont représentées et copiées dans le dossier AppData «Real» dans% AppData%.</span><span class="sxs-lookup"><span data-stu-id="f1415-151">The local cached data in AppData (roaming) is zipped up and copied to the “real” roaming AppData folder in %AppData%.</span></span> <span data-ttu-id="f1415-152">Un horodatage, qui indique le dernier chargement connu, est enregistré en même temps que la clé de Registre sous:</span><span class="sxs-lookup"><span data-stu-id="f1415-152">A time stamp, which indicates the last known upload, is simultaneously saved as a registry key under:</span></span></p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p><span data-ttu-id="f1415-153">Pour fournir la redondance, App-V conserve les trois copies les plus récentes des données comprimées sous% AppData%.</span><span class="sxs-lookup"><span data-stu-id="f1415-153">To provide redundancy, App-V keeps the three most recent copies of the compressed data under %AppData%.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a><span data-ttu-id="f1415-154">Présentation de la redirection de dossiers</span><span class="sxs-lookup"><span data-stu-id="f1415-154">Overview of folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1415-155">Objectif</span><span class="sxs-lookup"><span data-stu-id="f1415-155">Purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1415-156">Permet aux utilisateurs finaux de travailler avec des fichiers qui ont été redirigés vers un autre dossier, comme si les fichiers existaient déjà sur le lecteur local.</span><span class="sxs-lookup"><span data-stu-id="f1415-156">Enables end users to work with files, which have been redirected to another folder, as if the files still existed on the local drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1415-157">Description</span><span class="sxs-lookup"><span data-stu-id="f1415-157">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1415-158">La redirection de dossiers permet aux utilisateurs et aux administrateurs de rediriger le chemin d’accès d’un dossier vers un emplacement réseau.</span><span class="sxs-lookup"><span data-stu-id="f1415-158">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="f1415-159">Les documents figurant dans le dossier sont accessibles à l’utilisateur à partir de n’importe quel ordinateur du réseau.</span><span class="sxs-lookup"><span data-stu-id="f1415-159">The documents in the folder are available to the user from any computer on the network.</span></span></p>
<ul>
<li><p><span data-ttu-id="f1415-160">La redirection de dossiers permet aux utilisateurs et aux administrateurs de rediriger le chemin d’accès d’un dossier vers un emplacement réseau.</span><span class="sxs-lookup"><span data-stu-id="f1415-160">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="f1415-161">Les documents figurant dans le dossier sont accessibles à l’utilisateur à partir de n’importe quel ordinateur du réseau.</span><span class="sxs-lookup"><span data-stu-id="f1415-161">The documents in the folder are available to the user from any computer on the network.</span></span></p></li>
<li><p><span data-ttu-id="f1415-162">Le nouvel emplacement peut être un dossier sur l’ordinateur local ou un dossier sur un réseau partagé.</span><span class="sxs-lookup"><span data-stu-id="f1415-162">The new location can be a folder on the local computer or a folder on a shared network.</span></span></p></li>
<li><p><span data-ttu-id="f1415-163">La redirection de dossier met à jour les fichiers immédiatement, tandis que les données d’itinérance sont généralement synchronisées lorsque l’utilisateur se connecte ou se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="f1415-163">Folder redirection updates the files immediately, whereas roaming data is typically synchronized when the user logs in or logs off.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f1415-164">Exemple d’utilisation</span><span class="sxs-lookup"><span data-stu-id="f1415-164">Usage example</span></span></p></td>
<td align="left"><p><span data-ttu-id="f1415-165">Vous pouvez rediriger le dossier documents, qui est généralement stocké sur le disque dur local de l’ordinateur&#39;, à un emplacement réseau.</span><span class="sxs-lookup"><span data-stu-id="f1415-165">You can redirect the Documents folder, which is usually stored on the computer&#39;s local hard disk, to a network location.</span></span> <span data-ttu-id="f1415-166">L’utilisateur peut accéder aux documents du dossier à partir de n’importe quel ordinateur du réseau.</span><span class="sxs-lookup"><span data-stu-id="f1415-166">The user can access the documents in the folder from any computer on the network.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f1415-167">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="f1415-167">More resources</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)"><span data-ttu-id="f1415-168">Présentation de la redirection de dossiers</span><span class="sxs-lookup"><span data-stu-id="f1415-168">Folder redirection overview</span></span></a></p></td>
</tr>
</tbody>
</table>

















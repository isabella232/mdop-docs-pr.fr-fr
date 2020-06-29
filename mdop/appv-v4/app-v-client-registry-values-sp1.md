---
title: Valeurs de Registre d'App-V Client
description: Valeurs de Registre d'App-V Client
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808054"
---
# <span data-ttu-id="2af8d-103">Valeurs de Registre d'App-V Client</span><span class="sxs-lookup"><span data-stu-id="2af8d-103">App-V Client Registry Values</span></span>


<span data-ttu-id="2af8d-104">Le client Microsoft Application Virtualization (App-V) enregistre sa configuration dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2af8d-104">The Microsoft Application Virtualization (App-V) client stores its configuration in the registry.</span></span> <span data-ttu-id="2af8d-105">Vous pouvez recueillir des informations utiles sur le client si vous comprenez le format des données dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2af8d-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="2af8d-106">Vous pouvez également configurer de nombreuses actions client en modifiant des entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="2af8d-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="2af8d-107">Cette rubrique répertorie toutes les clés de Registre clientes Application Virtualization (App-V) et explique leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="2af8d-107">This topic lists all the Application Virtualization (App-V) client registry keys and explains their uses.</span></span>

**<span data-ttu-id="2af8d-108">Important</span><span class="sxs-lookup"><span data-stu-id="2af8d-108">Important</span></span>**  
<span data-ttu-id="2af8d-109">Sur un ordinateur exécutant un système d’exploitation 64 bits, les clés et les valeurs décrites dans les sections suivantes se trouvent sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="2af8d-109">On a computer running a 64-bit operating system, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>



## <span data-ttu-id="2af8d-110">Clé de configuration</span><span class="sxs-lookup"><span data-stu-id="2af8d-110">Configuration Key</span></span>


<span data-ttu-id="2af8d-111">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="2af8d-111">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2af8d-112">Nom</span><span class="sxs-lookup"><span data-stu-id="2af8d-112">Name</span></span></th>
<th align="left"><span data-ttu-id="2af8d-113">Type</span><span class="sxs-lookup"><span data-stu-id="2af8d-113">Type</span></span></th>
<th align="left"><span data-ttu-id="2af8d-114">Données (exemples)</span><span class="sxs-lookup"><span data-stu-id="2af8d-114">Data (Examples)</span></span></th>
<th align="left"><span data-ttu-id="2af8d-115">Description</span><span class="sxs-lookup"><span data-stu-id="2af8d-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-116">ProductName</span><span class="sxs-lookup"><span data-stu-id="2af8d-116">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-117">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-117">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-118">Client de bureau Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="2af8d-118">Microsoft Application Virtualization Desktop Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-119">Ne modifiez pas.</span><span class="sxs-lookup"><span data-stu-id="2af8d-119">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-120">Version</span><span class="sxs-lookup"><span data-stu-id="2af8d-120">Version</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-121">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-121">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-122">4.5.0.xxx</span><span class="sxs-lookup"><span data-stu-id="2af8d-122">4.5.0.xxx</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-123">Ne modifiez pas.</span><span class="sxs-lookup"><span data-stu-id="2af8d-123">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-124">Pilotes</span><span class="sxs-lookup"><span data-stu-id="2af8d-124">Drivers</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-125">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-125">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-126">Sftfs.sys</span><span class="sxs-lookup"><span data-stu-id="2af8d-126">Sftfs.sys</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-127">Si cette valeur de clé est présente, elle contient le nom du pilote à l’origine d’une erreur d’arrêt lors du dernier démarrage de la base.</span><span class="sxs-lookup"><span data-stu-id="2af8d-127">If this key value is present, it contains the name of the driver that caused a stop error the last time the core was starting.</span></span> <span data-ttu-id="2af8d-128">Après avoir résolu l’erreur d’arrêt, vous devez supprimer cette valeur de clé pour permettre à sftlist de démarrer.</span><span class="sxs-lookup"><span data-stu-id="2af8d-128">After you have fixed the stop error, you must delete this key value so that sftlist can start.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-129">InstallPath</span><span class="sxs-lookup"><span data-stu-id="2af8d-129">InstallPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-130">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-130">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-131">Par défaut = C:\Program Files\Microsoft Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="2af8d-131">Default=C:\Program Files\Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-132">L’emplacement de l’installation du client.</span><span class="sxs-lookup"><span data-stu-id="2af8d-132">The location where the client is installed.</span></span> <span data-ttu-id="2af8d-133">Ne modifiez pas.</span><span class="sxs-lookup"><span data-stu-id="2af8d-133">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-134">LogFileName</span><span class="sxs-lookup"><span data-stu-id="2af8d-134">LogFileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-135">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-135">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-136">Par défaut = CSIDL_COMMON_APPDATA virtualisation \Microsoft\Application Client\sftlog.txt</span><span class="sxs-lookup"><span data-stu-id="2af8d-136">Default=CSIDL_COMMON_APPDATA\Microsoft\Application Virtualization Client\sftlog.txt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-137">Le chemin d’accès et le nom du fichier journal du client.</span><span class="sxs-lookup"><span data-stu-id="2af8d-137">The path and name for the client log file.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2af8d-138">Remarque</span><span class="sxs-lookup"><span data-stu-id="2af8d-138">Note</span></span></strong><br/><p><span data-ttu-id="2af8d-139">Si vous exécutez une version antérieure à App-V 4,6, SP1 et que vous modifiez le nom ou l’emplacement du fichier journal, vous devez redémarrer le service sftlist pour que la modification soit prise en compte.</span><span class="sxs-lookup"><span data-stu-id="2af8d-139">If you are running an earlier version than App-V 4.6, SP1 and you modify the log file name or location, you must restart the sftlist service for the change to take effect.</span></span></p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-140">LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="2af8d-140">LogMinSeverity</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-141">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-141">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-142">Par défaut = 4, information</span><span class="sxs-lookup"><span data-stu-id="2af8d-142">Default=4, Informational</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-143">Détermine quels messages sont écrits dans le journal.</span><span class="sxs-lookup"><span data-stu-id="2af8d-143">Controls which messages are written to the log.</span></span> <span data-ttu-id="2af8d-144">La valeur indique un seuil de ce qui est enregistré, c’est-à-dire que tout est inférieur ou égal à cette valeur est consigné.</span><span class="sxs-lookup"><span data-stu-id="2af8d-144">The value indicates a threshold of what is logged—everything less than or equal to that value is logged.</span></span> <span data-ttu-id="2af8d-145">Par exemple, une valeur de 0x3 (avertissement) indique que les avertissements (0x3), les erreurs (0X2) et les erreurs critiques (0x1) sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="2af8d-145">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="2af8d-146">Plage de valeurs: 0x0 = aucune, 0x1 = Critical, 0X2 = erreur, 0x3 = Warning, 0x4 = informations (par défaut), 0x5 = Verbose.</span><span class="sxs-lookup"><span data-stu-id="2af8d-146">Value Range: 0x0 = None, 0x1 = Critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (Default), 0x5 = Verbose.</span></span></p>
<p><span data-ttu-id="2af8d-147">Le niveau du journal peut être configuré à partir de la console client Application Virtualization (App-V) et de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="2af8d-147">The log level is configurable from the Application Virtualization (App-V) client console and from the command prompt.</span></span> <span data-ttu-id="2af8d-148">À l’invite de commandes, la commande sftlist.exe/Verboselog augmentera le niveau du journal sur Verbose.</span><span class="sxs-lookup"><span data-stu-id="2af8d-148">At a command prompt, the command sftlist.exe /verboselog will increase the log level to verbose.</span></span> <span data-ttu-id="2af8d-149">Pour plus d’informations sur les détails de la ligne de commande, voir</span><span class="sxs-lookup"><span data-stu-id="2af8d-149">For more information on command-line details see</span></span></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p><span data-ttu-id="2af8d-150">.</span><span class="sxs-lookup"><span data-stu-id="2af8d-150">.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-151">LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="2af8d-151">LogRolloverCount</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-152">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-152">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-153">Par défaut = 4</span><span class="sxs-lookup"><span data-stu-id="2af8d-153">Default=4</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-154">Définit le nombre de copies de sauvegarde du fichier journal qui sont conservées lors de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="2af8d-154">Defines the number of backup copies of the log file that are kept when it is reset.</span></span> <span data-ttu-id="2af8d-155">La plage valide est égale à 0 – 9999.</span><span class="sxs-lookup"><span data-stu-id="2af8d-155">The valid range is 0–9999.</span></span> <span data-ttu-id="2af8d-156">La valeur par défaut est 4.</span><span class="sxs-lookup"><span data-stu-id="2af8d-156">The default is 4.</span></span> <span data-ttu-id="2af8d-157">La valeur 0 indique qu’il n’y a pas de copie.</span><span class="sxs-lookup"><span data-stu-id="2af8d-157">A value of 0 means no copies will be kept.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-158">LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="2af8d-158">LogMaxSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-160">Par défaut = 256</span><span class="sxs-lookup"><span data-stu-id="2af8d-160">Default=256</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-161">Définit la taille maximale en mégaoctets (Mo) que le fichier journal peut augmenter avant de procéder à la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="2af8d-161">Defines the maximum size in megabytes (MB) that the log file can grow before being reset.</span></span> <span data-ttu-id="2af8d-162">La taille par défaut est 256 Mo.</span><span class="sxs-lookup"><span data-stu-id="2af8d-162">The default size is 256 MB.</span></span> <span data-ttu-id="2af8d-163">Lorsque cette taille est atteinte, une réinitialisation du journal sera forcée lors de la tentative d’écriture suivante.</span><span class="sxs-lookup"><span data-stu-id="2af8d-163">When this size is reached, a log reset will be forced on the next write attempt.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-164">SystemEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="2af8d-164">SystemEventLogLevel</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-165">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-165">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-166">Par défaut = 0x4 (App-V 4,5)</span><span class="sxs-lookup"><span data-stu-id="2af8d-166">Default=0x4 (App-V 4.5)</span></span></p>
<p><span data-ttu-id="2af8d-167">Par défaut = 0x3 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="2af8d-167">Default=0x3 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-168">Indique le niveau de journalisation dans lequel les messages du journal sont écrits dans le journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="2af8d-168">Indicates the logging level at which log messages are written to the NT event log.</span></span> <span data-ttu-id="2af8d-169">La valeur indique un seuil de ce qui est enregistré, c’est-à-dire que tout est égal ou inférieur à cette valeur est consigné.</span><span class="sxs-lookup"><span data-stu-id="2af8d-169">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="2af8d-170">Par exemple, une valeur de 0x3 (avertissement) indique que les avertissements (0x3), les erreurs (0X2) et les erreurs critiques (0x1) sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="2af8d-170">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="2af8d-171">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="2af8d-171">Value Range</span></span></p>
<p><span data-ttu-id="2af8d-172">0x0 = aucun</span><span class="sxs-lookup"><span data-stu-id="2af8d-172">0x0 = None</span></span></p>
<p><span data-ttu-id="2af8d-173">0x1 = critique</span><span class="sxs-lookup"><span data-stu-id="2af8d-173">0x1 = Critical</span></span></p>
<p><span data-ttu-id="2af8d-174">0X2 = erreur</span><span class="sxs-lookup"><span data-stu-id="2af8d-174">0x2 = Error</span></span></p>
<p><span data-ttu-id="2af8d-175">0x3 = AVERTISSEMENT</span><span class="sxs-lookup"><span data-stu-id="2af8d-175">0x3 = Warning</span></span></p>
<p><span data-ttu-id="2af8d-176">0x4 = informations (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2af8d-176">0x4 = Information (Default)</span></span></p>
<p><span data-ttu-id="2af8d-177">0x5 = commentaires</span><span class="sxs-lookup"><span data-stu-id="2af8d-177">0x5 = Verbose</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-178">AllowIndependentFileStreaming</span><span class="sxs-lookup"><span data-stu-id="2af8d-178">AllowIndependentFileStreaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-179">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-179">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-180">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-180">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-181">Indique si la diffusion en continu à partir du fichier sera activée quelle que soit la façon dont le client a été configuré avec le paramètre APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="2af8d-181">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the APPLICATIONSOURCEROOT parameter.</span></span> <span data-ttu-id="2af8d-182">Si elle est définie sur FALSe, le transport n’active pas la diffusion en continu à partir de fichiers, même si le paramètre OSD HREF ou APPLICATIONSOURCEROOT contient un chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="2af8d-182">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the APPLICATIONSOURCEROOT parameter contains a file path.</span></span></p>
<p><span data-ttu-id="2af8d-183">0x0 = false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2af8d-183">0x0=False (default)</span></span></p>
<p><span data-ttu-id="2af8d-184">0x1 = vrai</span><span class="sxs-lookup"><span data-stu-id="2af8d-184">0x1=True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-185">ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="2af8d-185">ApplicationSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-186">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-186">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-187">rtsps://mainserver:322/prodapps</span><span class="sxs-lookup"><span data-stu-id="2af8d-187">rtsps://mainserver:322/prodapps</span></span></p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p><span data-ttu-id="2af8d-188">fichier://\uncserver\share\prodapps</span><span class="sxs-lookup"><span data-stu-id="2af8d-188">file://\uncserver\share\prodapps</span></span></p>
<p><span data-ttu-id="2af8d-189">fichier://\uncserver\share</span><span class="sxs-lookup"><span data-stu-id="2af8d-189">file://\uncserver\share</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-190">Permet à un administrateur ou à un système de distribution de logiciels électronique (ESD) de garantir le chargement des applications conformément au schéma de gestion de la topologie.</span><span class="sxs-lookup"><span data-stu-id="2af8d-190">Enables an administrator or electronic software distribution (ESD) system to ensure application loading is performed according to the topology management scheme.</span></span> <span data-ttu-id="2af8d-191">Utilisez cette valeur de clé pour remplacer le code base OSD pour l’élément HREF (par exemple, l’emplacement source) pour une application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-191">Use this key value to override the OSD CODEBASE for the HREF element (for example, the source location) for an application.</span></span> <span data-ttu-id="2af8d-192">La racine source de l’application prend en charge les URL et les formats de chemin UNC (Universal Naming Convention).</span><span class="sxs-lookup"><span data-stu-id="2af8d-192">Application Source Root supports URLs and Universal Naming Convention (UNC) path formats.</span></span></p>
<p><span data-ttu-id="2af8d-193">Le format correct pour le chemin d’accès URL est Protocol://servername: [port] [/path] [/], où le port et le chemin d’accès sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="2af8d-193">The correct format for the URL path is protocol://servername:[port][/path][/], where port and path are optional.</span></span> <span data-ttu-id="2af8d-194">Si un port n’est pas spécifié, le port par défaut du protocole est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2af8d-194">If a port is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="2af8d-195">Seule la partie protocole://Server: port de l’URL d’OSD est remplacée.</span><span class="sxs-lookup"><span data-stu-id="2af8d-195">Only the protocol://server:port portion of the OSD URL is replaced.</span></span> </p>
<p><span data-ttu-id="2af8d-196">Le format correct pour le chemin d’accès UNC est \computername\sharefolder [dossier] [], où le dossier est facultatif.</span><span class="sxs-lookup"><span data-stu-id="2af8d-196">The correct format for the UNC path is \computername\sharefolder[folder][], where folder is optional.</span></span> <span data-ttu-id="2af8d-197">Le nom de l’ordinateur peut être un nom de domaine complet (FQDN, Fully Qualified Domain Name) ou une adresse IP, et ShareFolder peut être une lettre d’unité.</span><span class="sxs-lookup"><span data-stu-id="2af8d-197">The computer name can be a fully qualified domain name (FQDN) or an IP address, and sharefolder can be a drive letter.</span></span> <span data-ttu-id="2af8d-198">Seule la partie \computername\sharefolder ou lettre de lecteur du chemin OSD est remplacée.</span><span class="sxs-lookup"><span data-stu-id="2af8d-198">Only the \computername\sharefolder or drive letter portion of the OSD path is replaced.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-199">OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="2af8d-199">OSDSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-200">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-200">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-201">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="2af8d-201">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="2af8d-202">\computername\content</span><span class="sxs-lookup"><span data-stu-id="2af8d-202">\computername\content</span></span></p>
<p><span data-ttu-id="2af8d-203">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="2af8d-203">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="2af8d-204">Permet à un administrateur de spécifier un emplacement source pour la récupération de fichier OSD pour un package d’application séquencé lors de la publication.</span><span class="sxs-lookup"><span data-stu-id="2af8d-204">Enables an administrator to specify a source location for OSD file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="2af8d-205">Les formats acceptables pour le OSDSourceRoot incluent les chemins d’accès UNC et les URL (http ou https).</span><span class="sxs-lookup"><span data-stu-id="2af8d-205">Acceptable formats for the OSDSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-206">IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="2af8d-206">IconSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-207">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-207">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-208">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="2af8d-208">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="2af8d-209">\computername\content</span><span class="sxs-lookup"><span data-stu-id="2af8d-209">\computername\content</span></span></p>
<p><span data-ttu-id="2af8d-210">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="2af8d-210">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="2af8d-211">Permet à un administrateur de spécifier un emplacement source pour la récupération du fichier d’icône pour un package d’application séquencé lors de la publication.</span><span class="sxs-lookup"><span data-stu-id="2af8d-211">Enables an administrator to specify a source location for icon file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="2af8d-212">Les formats acceptables pour le IconSourceRoot incluent les chemins d’accès UNC et les URL (http ou https).</span><span class="sxs-lookup"><span data-stu-id="2af8d-212">Acceptable formats for the IconSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-213">AutoLoadTriggers</span><span class="sxs-lookup"><span data-stu-id="2af8d-213">AutoLoadTriggers</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-214">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-214">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-215">Par défaut = 5</span><span class="sxs-lookup"><span data-stu-id="2af8d-215">Default=5</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-216">Autoload est un paramètre de configuration de la stratégie d’exécution du client qui permet d’afficher automatiquement le bloc de fonctionnalité secondaire d’une application virtualisée au client en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="2af8d-216">AutoLoad is a client runtime policy configuration parameter that enables the secondary feature block of a virtualized application to be streamed to the client automatically in the background.</span></span> <span data-ttu-id="2af8d-217">Les déclencheurs de chargement sont des indicateurs permettant d’indiquer des événements qui déclenchent le chargement automatique des applications.</span><span class="sxs-lookup"><span data-stu-id="2af8d-217">The AutoLoad triggers are flags to indicate events that initiate auto-loading of applications.</span></span> <span data-ttu-id="2af8d-218">Autoload utilise implicitement le streaming en arrière-plan pour permettre au chargement de l’application dans le cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-218">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span> <span data-ttu-id="2af8d-219">Le bloc de fonctionnalité principal est chargé en premier, et les blocs de fonctionnalités restants sont chargés en arrière-plan pour permettre aux opérations au premier plan, telles que l’interaction utilisateur avec les applications, d’avoir lieu et d’offrir des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="2af8d-219">The primary feature block will be loaded first, and the remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take place and provide optimal perceived performance.</span></span></p>
<p><span data-ttu-id="2af8d-220">Valeurs de masque de bits:</span><span class="sxs-lookup"><span data-stu-id="2af8d-220">Bit mask values:</span></span></p>
<p><span data-ttu-id="2af8d-221">(0) jamais: aucun bit n’est défini (valeur égale à 0), aucun chargement automatique ne sera effectué, car aucun déclencheur n’est défini.</span><span class="sxs-lookup"><span data-stu-id="2af8d-221">(0) Never: No bits are set (value is 0), no auto loading will be performed, because there are no triggers set.</span></span></p>
<p><span data-ttu-id="2af8d-222">(1) OnLaunch: le chargement s’exécute dès qu’un utilisateur démarre une application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-222">(1) OnLaunch: Loading starts when a user starts an application.</span></span></p>
<p><span data-ttu-id="2af8d-223">(2) OnRefresh: le chargement démarre lors de la publication de l’application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-223">(2) OnRefresh: Loading starts when the application is published.</span></span> <span data-ttu-id="2af8d-224">Ce problème survient chaque fois que l’enregistrement du package est ajouté ou mis à jour, par exemple, lors de l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="2af8d-224">This occurs whenever the package record is added or updated—for example, when a publishing refresh occurs.</span></span></p>
<p><span data-ttu-id="2af8d-225">(4) OnLogin: le chargement s’exécute dès qu’un utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="2af8d-225">(4) OnLogin: Loading starts when a user logs in.</span></span></p>
<p><span data-ttu-id="2af8d-226">(5) OnLaunch et OnLogin: par défaut.</span><span class="sxs-lookup"><span data-stu-id="2af8d-226">(5) OnLaunch and OnLogin: Default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-227">AutoLoadTarget</span><span class="sxs-lookup"><span data-stu-id="2af8d-227">AutoLoadTarget</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-228">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-229">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="2af8d-229">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-230">Indique ce qui sera chargé automatiquement lorsque des déclencheurs de chargement sont présents.</span><span class="sxs-lookup"><span data-stu-id="2af8d-230">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span> <span data-ttu-id="2af8d-231">Valeurs de masque de bits:</span><span class="sxs-lookup"><span data-stu-id="2af8d-231">Bit mask values:</span></span></p>
<p><span data-ttu-id="2af8d-232">(0) aucun: pas de chargement automatique, quels que soient les déclencheurs définis.</span><span class="sxs-lookup"><span data-stu-id="2af8d-232">(0) None: No auto-loading, regardless of what triggers may be set.</span></span></p>
<p><span data-ttu-id="2af8d-233">(1) PreviouslyUsed (par défaut): si aucun déclencheur de chargement automatique n’est activé, chargez uniquement les packages dans lesquels au moins une application dans le package a été précédemment utilisée (c’est-à-dire démarrée ou mise en cache).</span><span class="sxs-lookup"><span data-stu-id="2af8d-233">(1) PreviouslyUsed (default): If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used—that is, started or precached.</span></span></p>
<p><span data-ttu-id="2af8d-234">(2) All: si un déclencheur de chargement automatique est activé, toutes les applications du package (par package) ou tous les packages (définies pour le client) seront automatiquement chargées, qu’elles soient ou non démarrées.</span><span class="sxs-lookup"><span data-stu-id="2af8d-234">(2) All: If any AutoLoad trigger is enabled, all applications in the package (per package) or all packages (set for client) will be automatically loaded, whether or not they have ever been started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-235">RequireAuthorizationIfCached</span><span class="sxs-lookup"><span data-stu-id="2af8d-235">RequireAuthorizationIfCached</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-236">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-236">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-237">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="2af8d-237">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-238">Indique qu’une autorisation est toujours requise, qu’une application soit déjà en cache ou non.</span><span class="sxs-lookup"><span data-stu-id="2af8d-238">Indicates that authorization is always required, whether or not an application is already in cache.</span></span> <span data-ttu-id="2af8d-239">Valeurs possibles:</span><span class="sxs-lookup"><span data-stu-id="2af8d-239">Possible values:</span></span></p>
<p><span data-ttu-id="2af8d-240">0 = faux: Essayez toujours de vous connecter au serveur.</span><span class="sxs-lookup"><span data-stu-id="2af8d-240">0=False: Always try to connect to the server.</span></span> <span data-ttu-id="2af8d-241">Si une connexion au serveur ne peut pas être établie, le client permet toujours à l’utilisateur de lancer une application qui a déjà été chargée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-241">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p>
<p><span data-ttu-id="2af8d-242">1 = vrai (par défaut): l’application doit toujours être autorisée au démarrage.</span><span class="sxs-lookup"><span data-stu-id="2af8d-242">1=True (default): Application always must be authorized at startup.</span></span> <span data-ttu-id="2af8d-243">Pour les applications RTSP transmis, le jeton d’autorisation de l’utilisateur est envoyé au serveur pour autorisation.</span><span class="sxs-lookup"><span data-stu-id="2af8d-243">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="2af8d-244">Dans le cas des applications basées sur le fichier, les listes de contrôle d’accès de fichier déterminent si un utilisateur est susceptible d’y accéder.</span><span class="sxs-lookup"><span data-stu-id="2af8d-244">For file-based applications, file ACLs control whether a user may access the application.</span></span></p>
<p><span data-ttu-id="2af8d-245">Redémarrez le service sftlist pour que la modification soit prise en compte.</span><span class="sxs-lookup"><span data-stu-id="2af8d-245">Restart the sftlist service for the change to take effect.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-246">UserDataDirectory</span><span class="sxs-lookup"><span data-stu-id="2af8d-246">UserDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-247">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-247">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-248">AppData</span><span class="sxs-lookup"><span data-stu-id="2af8d-248">%APPDATA%</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-249">Emplacement de stockage des paramètres du cache d’icônes et de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2af8d-249">Location where the icon cache and user settings are stored.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-250">GlobalDataDirectory</span><span class="sxs-lookup"><span data-stu-id="2af8d-250">GlobalDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-251">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-251">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-252">C:\Users\Public\Documents</span><span class="sxs-lookup"><span data-stu-id="2af8d-252">C:\Users\Public\Documents</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-253">Directory à utiliser pour les données globales App-V, y compris les caches pour les fichiers OSD, les fichiers d’icônes, les informations de raccourci et les ressources SystemGuard telles que les fichiers. ini.</span><span class="sxs-lookup"><span data-stu-id="2af8d-253">Directory to use for global App-V data, including caches for OSD files, icon files, shortcut information, and SystemGuard resources such as .ini files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-254">AllowCrashes</span><span class="sxs-lookup"><span data-stu-id="2af8d-254">AllowCrashes</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-255">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-256">0 ou 1</span><span class="sxs-lookup"><span data-stu-id="2af8d-256">0 or 1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-257">Par défaut = 0: une valeur de 0 indique que le client tente d’intercepter les exceptions de programme interne pour permettre à d’autres applications utilisateur de se retrouver et de continuer en cas de blocage.</span><span class="sxs-lookup"><span data-stu-id="2af8d-257">Default=0: A value of 0 means that the client tries to catch internal program exceptions so that other user applications can recover and continue when a crash happens.</span></span> <span data-ttu-id="2af8d-258">La valeur 1 indique que le client autorise l’apparition des exceptions du programme interne afin qu’elles puissent être capturées dans un débogueur.</span><span class="sxs-lookup"><span data-stu-id="2af8d-258">A value of 1 means that the client allows the internal program exceptions to occur so that they can be captured in a debugger.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-259">CoreInternalTimeout</span><span class="sxs-lookup"><span data-stu-id="2af8d-259">CoreInternalTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-260">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-260">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-261">60</span><span class="sxs-lookup"><span data-stu-id="2af8d-261">60</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-262">Délai d’expiration en secondes pour les demandes de CPI internes entre le cœur et le front-end.</span><span class="sxs-lookup"><span data-stu-id="2af8d-262">Time-out in seconds for internal IPC requests between core and front-end.</span></span> <span data-ttu-id="2af8d-263">Ne modifiez pas.</span><span class="sxs-lookup"><span data-stu-id="2af8d-263">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-264">DefaultSuiteCombineTime</span><span class="sxs-lookup"><span data-stu-id="2af8d-264">DefaultSuiteCombineTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-265">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-266">0,10</span><span class="sxs-lookup"><span data-stu-id="2af8d-266">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-267">Cette valeur est utilisée pour indiquer le nombre de fois qu’un programme peut s’arrêter et ne générer aucun message d’erreur lorsqu’une autre application de la même suite est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2af8d-267">This value is used to indicate how soon after being started that a program can shut down and not generate any error messages when another application in the same suite is running.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-268">SerializedSuiteLaunchTimeout</span><span class="sxs-lookup"><span data-stu-id="2af8d-268">SerializedSuiteLaunchTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-269">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-269">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-270">Par défaut = 60000</span><span class="sxs-lookup"><span data-stu-id="2af8d-270">Default=60000</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-271">Définit la durée en millisecondes au sein de laquelle le client doit patienter pendant qu’il tente de sérialiser les programmes dans la même suite.</span><span class="sxs-lookup"><span data-stu-id="2af8d-271">Defines how long in milliseconds the client will wait as it tries to serialize program starts in the same suite.</span></span> <span data-ttu-id="2af8d-272">Si le client arrive à expiration, le démarrage du programme se poursuit mais il n’est pas sérialisé.</span><span class="sxs-lookup"><span data-stu-id="2af8d-272">If the client times out, the program start will continue but it will not be serialized.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-273">ScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="2af8d-273">ScriptTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-274">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-275">300</span><span class="sxs-lookup"><span data-stu-id="2af8d-275">300</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-276">Délai d’expiration par défaut (en secondes) pour les scripts du fichier OSD si attendez = TRUE.</span><span class="sxs-lookup"><span data-stu-id="2af8d-276">Default time-out in seconds for scripts in OSD file if WAIT=TRUE.</span></span> <span data-ttu-id="2af8d-277">Vous pouvez spécifier des délais d’expiration par script avec une temporisation au lieu d’attendre.</span><span class="sxs-lookup"><span data-stu-id="2af8d-277">You can specify per-script time-outs with TIMEOUT instead of WAIT.</span></span> <span data-ttu-id="2af8d-278">Une valeur de 0 signifie qu’il n’y A pas d’attente et 0xFFFFFFFF un délai d’exécution permanent.</span><span class="sxs-lookup"><span data-stu-id="2af8d-278">A value of 0 means no wait, and 0xFFFFFFFF means wait forever.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-279">LaunchRecordLogPath</span><span class="sxs-lookup"><span data-stu-id="2af8d-279">LaunchRecordLogPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-280">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-280">String</span></span> </p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2af8d-281">Si, dans le cadre de l’argument HKLM ou HKCU, cette valeur contient un chemin valide vers un fichier journal, SFTTray écrit dans ce journal lorsque les programmes démarrent, s’arrête, ne démarre pas, puis passe ou quittez le mode déconnecté.</span><span class="sxs-lookup"><span data-stu-id="2af8d-281">If, under either HKLM or HKCU, this value contains a valid path to a log file, SFTTray will write to this log when programs start, shut down, fail to launch, and enter or exit disconnected mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-282">LaunchRecordMask</span><span class="sxs-lookup"><span data-stu-id="2af8d-282">LaunchRecordMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-283">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-283">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-284">0x1A (26) consigner les erreurs de démarrage et les activités d’entrée et de sortie du mode déconnecté.</span><span class="sxs-lookup"><span data-stu-id="2af8d-284">0x1A (26) log launch errors and disconnected mode entry and exit activity.</span></span></p>
<p><span data-ttu-id="2af8d-285">0x1F (31) enregistre tout le contenu.</span><span class="sxs-lookup"><span data-stu-id="2af8d-285">0x1F (31) logs everything.</span></span></p>
<p><span data-ttu-id="2af8d-286">0x0 (0) n’enregistre aucune information.</span><span class="sxs-lookup"><span data-stu-id="2af8d-286">0x0 (0) logs nothing.</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-287">Spécifie lequel des cinq événements sont enregistrés (valeurs de masque de réaffichages):</span><span class="sxs-lookup"><span data-stu-id="2af8d-287">Specifies which of the five events are logged (bitmask values):</span></span></p>
<p><span data-ttu-id="2af8d-288">1 pour le démarrage du programme</span><span class="sxs-lookup"><span data-stu-id="2af8d-288">1 for program starts</span></span></p>
<p><span data-ttu-id="2af8d-289">2 pour les erreurs d’échec de lancement</span><span class="sxs-lookup"><span data-stu-id="2af8d-289">2 for launch failure errors</span></span></p>
<p><span data-ttu-id="2af8d-290">4 pour les arrêts</span><span class="sxs-lookup"><span data-stu-id="2af8d-290">4 for shutdowns</span></span></p>
<p><span data-ttu-id="2af8d-291">8 pour entrer en mode déconnecté</span><span class="sxs-lookup"><span data-stu-id="2af8d-291">8 for entering disconnected mode</span></span></p>
<p><span data-ttu-id="2af8d-292">16 pour quitter le mode déconnecté afin de vous reconnecter à un serveur</span><span class="sxs-lookup"><span data-stu-id="2af8d-292">16 for exiting disconnected mode to reconnect to a server</span></span></p>
<p><span data-ttu-id="2af8d-293">Ajoutez n’importe quelle combinaison de ces numéros pour activer les messages correspondants.</span><span class="sxs-lookup"><span data-stu-id="2af8d-293">Add any combination of those numbers to turn on the respective messages.</span></span> <span data-ttu-id="2af8d-294">Utilise par défaut la valeur 0x1F s’il ne se trouve pas dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2af8d-294">Defaults to 0x1F if not in registry.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-295">LaunchRecordWriteTimeout</span><span class="sxs-lookup"><span data-stu-id="2af8d-295">LaunchRecordWriteTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-296">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-296">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-297">Par défaut = 3000</span><span class="sxs-lookup"><span data-stu-id="2af8d-297">Default=3000</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-298">Spécifie en millisecondes le temps que la barre d’attente attend lors de la tentative d’écriture dans le journal d’enregistrement de lancement si un autre processus l’utilise.</span><span class="sxs-lookup"><span data-stu-id="2af8d-298">Specifies in milliseconds how long the tray will wait when trying to write to the launch record log if another process is using it.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-299">ImportSearchPath</span><span class="sxs-lookup"><span data-stu-id="2af8d-299">ImportSearchPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-300">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-300">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-301">d:\files; C:\Documents and settings\user1\SFTs</span><span class="sxs-lookup"><span data-stu-id="2af8d-301">d:\files;C:\documents and settings\user1\SFTs</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-302">Liste délimitée par des points-virgules de cinq annuaires pour lesquels rechercher des fichiers de la liste de choix mobiles avant d’inviter l’utilisateur à sélectionner un annuaire.</span><span class="sxs-lookup"><span data-stu-id="2af8d-302">A semicolon delimited list of up to five directories to search for portable SFT files before prompting the user to select a directory.</span></span> <span data-ttu-id="2af8d-303">Le caractère barre oblique inverse dans les chemins est facultatif.</span><span class="sxs-lookup"><span data-stu-id="2af8d-303">Trailing backslash in paths is optional.</span></span> <span data-ttu-id="2af8d-304">Cette valeur n’est pas présente par défaut et doit être définie manuellement.</span><span class="sxs-lookup"><span data-stu-id="2af8d-304">This value is not present by default and must be set manually.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-305">UserImportPath</span><span class="sxs-lookup"><span data-stu-id="2af8d-305">UserImportPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-306">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-306">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-307">D:\SFTs</span><span class="sxs-lookup"><span data-stu-id="2af8d-307">D:\SFTs</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="2af8d-308">Valide uniquement sous HKCU.</span><span class="sxs-lookup"><span data-stu-id="2af8d-308">Valid only under HKCU.</span></span> <span data-ttu-id="2af8d-309">Dernier emplacement sur lequel l’utilisateur a été consulté lors de la recherche d’un fichier SFT pour l’importation du package.</span><span class="sxs-lookup"><span data-stu-id="2af8d-309">The last location the user browsed to while finding a SFT file for package import.</span></span> <span data-ttu-id="2af8d-310">Configuré automatiquement si la valeur SFT est correctement trouvée.</span><span class="sxs-lookup"><span data-stu-id="2af8d-310">Set automatically if the SFT is found successfully.</span></span> <span data-ttu-id="2af8d-311">Il s’utilise sur les importations successives lorsque vous tentez de rechercher automatiquement des fichiers SFT.</span><span class="sxs-lookup"><span data-stu-id="2af8d-311">This is used on successive imports when trying to automatically locate SFT files.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2af8d-312">Clé partagée</span><span class="sxs-lookup"><span data-stu-id="2af8d-312">Shared Key</span></span>


<span data-ttu-id="2af8d-313">La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared contrôle les valeurs qui sont partagées entre les composants App-V.</span><span class="sxs-lookup"><span data-stu-id="2af8d-313">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared key controls values that are shared across App-V components.</span></span> <span data-ttu-id="2af8d-314">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé partagée.</span><span class="sxs-lookup"><span data-stu-id="2af8d-314">The following table provides information about the registry values associated with the Shared key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2af8d-315">Nom</span><span class="sxs-lookup"><span data-stu-id="2af8d-315">Name</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-316">Type</span><span class="sxs-lookup"><span data-stu-id="2af8d-316">Type</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-317">Données (exemples)</span><span class="sxs-lookup"><span data-stu-id="2af8d-317">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-318">Description</span><span class="sxs-lookup"><span data-stu-id="2af8d-318">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-319">DumpPath</span><span class="sxs-lookup"><span data-stu-id="2af8d-319">DumpPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-320">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-320">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-321">Par défaut = C:</span><span class="sxs-lookup"><span data-stu-id="2af8d-321">Default=C:</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="2af8d-322">Chemin par défaut pour créer des fichiers de vidage lors de la génération d’un minidump sur une exception.</span><span class="sxs-lookup"><span data-stu-id="2af8d-322">Default path to create dump files when generating a minidump on an exception.</span></span> <span data-ttu-id="2af8d-323">Par défaut, la valeur est C:\ en l’absence de spécification.</span><span class="sxs-lookup"><span data-stu-id="2af8d-323">This defaults to C:\ if not specified.</span></span> <span data-ttu-id="2af8d-324">Le programme d’installation du client définit cette clé sur le &lt; répertoire global Data \Dumps. Directory Data Virtualization. &gt;</span><span class="sxs-lookup"><span data-stu-id="2af8d-324">The Client installer sets this key to the &lt;App Virtualization global data directory&gt;\Dumps.</span></span> <span data-ttu-id="2af8d-325">Le programme d’installation de Sequencer définit cette clé sur le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="2af8d-325">The Sequencer installer sets this key to the installation directory.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-326">DumpPathSizeLimit</span><span class="sxs-lookup"><span data-stu-id="2af8d-326">DumpPathSizeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-327">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-327">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-328">1000</span><span class="sxs-lookup"><span data-stu-id="2af8d-328">1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-329">Spécifie la quantité totale d’espace disque en mégaoctets qui peut être utilisée pour stocker les minidumps.</span><span class="sxs-lookup"><span data-stu-id="2af8d-329">Specifies the maximum total amount of disk space in megabytes that can be used to store minidumps.</span></span> <span data-ttu-id="2af8d-330">Par défaut = 1000 Mo.</span><span class="sxs-lookup"><span data-stu-id="2af8d-330">Default = 1000 MB.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2af8d-331">Clé réseau</span><span class="sxs-lookup"><span data-stu-id="2af8d-331">Network Key</span></span>


<span data-ttu-id="2af8d-332">La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network contrôle divers paramètres liés au réseau.</span><span class="sxs-lookup"><span data-stu-id="2af8d-332">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network key controls a variety of network-related parameters.</span></span> <span data-ttu-id="2af8d-333">Cette clé est essentiellement utilisée par l’agent de transport réseau.</span><span class="sxs-lookup"><span data-stu-id="2af8d-333">This key is primarily used by the network transport agent.</span></span> <span data-ttu-id="2af8d-334">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé réseau.</span><span class="sxs-lookup"><span data-stu-id="2af8d-334">The following table provides information about the registry values associated with the Network key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2af8d-335">Nom</span><span class="sxs-lookup"><span data-stu-id="2af8d-335">Name</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-336">Type</span><span class="sxs-lookup"><span data-stu-id="2af8d-336">Type</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-337">Données (exemples)</span><span class="sxs-lookup"><span data-stu-id="2af8d-337">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-338">Description</span><span class="sxs-lookup"><span data-stu-id="2af8d-338">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-339">Online</span><span class="sxs-lookup"><span data-stu-id="2af8d-339">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-340">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-340">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-341">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="2af8d-341">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-342">Active ou désactive le mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2af8d-342">Enables or disables offline mode.</span></span> <span data-ttu-id="2af8d-343">Si la valeur est définie sur 0, le client ne va pas communiquer avec des serveurs de gestion ou des serveurs de publication App-V.</span><span class="sxs-lookup"><span data-stu-id="2af8d-343">If set to 0, the client will not communicate with App-V Management Servers or publishing servers.</span></span> <span data-ttu-id="2af8d-344">Dans les opérations déconnectées, le client peut démarrer une application chargée même lorsqu’elle n’est pas connectée à un serveur de gestion d’applications-V.</span><span class="sxs-lookup"><span data-stu-id="2af8d-344">In disconnected operations, the client can start a loaded application even when it is not connected to an App-V Management Server.</span></span> <span data-ttu-id="2af8d-345">En mode hors connexion, le client ne tente pas de se connecter à un serveur de gestion ou un serveur de publication App-V.</span><span class="sxs-lookup"><span data-stu-id="2af8d-345">In offline mode, the client does not attempt to connect to an App-V Management Server or publishing server.</span></span> <span data-ttu-id="2af8d-346">Vous devez autoriser les opérations déconnectées à travailler en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2af8d-346">You must allow disconnected operations to be able to work offline.</span></span> <span data-ttu-id="2af8d-347">La valeur par défaut est activée (en ligne) et 0 est désactivée (hors connexion).</span><span class="sxs-lookup"><span data-stu-id="2af8d-347">Default value is 1 enabled (online), and 0 is disabled (offline).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-348">AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="2af8d-348">AllowDisconnectedOperation</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-349">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-349">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-350">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="2af8d-350">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-351">Active ou désactive l’opération hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2af8d-351">Enables or disables disconnected operation.</span></span> <span data-ttu-id="2af8d-352">La valeur par défaut est activée et 0 est désactivé.</span><span class="sxs-lookup"><span data-stu-id="2af8d-352">Default value is 1 enabled, and 0 is disabled.</span></span> <span data-ttu-id="2af8d-353">Lorsque les opérations déconnectées sont activées, le client App-V peut démarrer une application chargée, même si elle n’est pas connectée à un serveur d’administration d’applications-V.</span><span class="sxs-lookup"><span data-stu-id="2af8d-353">When disconnected operations are enabled, the App-V client can start a loaded application even when it is not connected to an App-V Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-354">FastConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="2af8d-354">FastConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-356">Par défaut = 1 000</span><span class="sxs-lookup"><span data-stu-id="2af8d-356">Default=1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-357">Cette valeur spécifie le délai de connexion TCP en millisecondes pour déterminer quand passer en mode opérations déconnectées.</span><span class="sxs-lookup"><span data-stu-id="2af8d-357">This value specifies the TCP connect time-out in milliseconds to determine when to go into disconnected operations mode.</span></span> <span data-ttu-id="2af8d-358">Cette valeur peut être utilisée pour remplacer la valeur par défaut ConnectTimeout de 20 secondes (délai d’expiration de la connexion App-V pour les transactions réseau) ou le délai d’expiration TCP du système d’environ 25 secondes.</span><span class="sxs-lookup"><span data-stu-id="2af8d-358">This value can be used to override the default ConnectTimeout of 20 seconds (App-V connect time-out for network transactions) or the system’s TCP time-out of approximately 25 seconds.</span></span> <span data-ttu-id="2af8d-359">Cela amène le client en mode d’opérations déconnectées rapidement.</span><span class="sxs-lookup"><span data-stu-id="2af8d-359">This brings the client into disconnected operations mode quickly.</span></span> <span data-ttu-id="2af8d-360">Appliqué lors de la prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="2af8d-360">Applied on the next connect.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-361">LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="2af8d-361">LimitDisconnectedOperation</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-363">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="2af8d-363">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-364">Applicable uniquement si AllowDisconnectedOperation est activé.</span><span class="sxs-lookup"><span data-stu-id="2af8d-364">Applicable only if AllowDisconnectedOperation is 1, enabled.</span></span> <span data-ttu-id="2af8d-365">Cette valeur détermine s’il y a une limite de temps pour la durée pendant laquelle le client est autorisé à fonctionner dans les opérations déconnectées.</span><span class="sxs-lookup"><span data-stu-id="2af8d-365">This value determines whether there will be a time limit for how long the client will be allowed to operate in disconnected operations.</span></span> <span data-ttu-id="2af8d-366">1 = Limited.</span><span class="sxs-lookup"><span data-stu-id="2af8d-366">1=limited.</span></span> <span data-ttu-id="2af8d-367">0 = illimité.</span><span class="sxs-lookup"><span data-stu-id="2af8d-367">0=unlimited.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-368">DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="2af8d-368">DOTimeoutMinutes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-369">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-369">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-370">Par défaut = 129600</span><span class="sxs-lookup"><span data-stu-id="2af8d-370">Default=129,600</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-371">Indique le nombre de minutes d’utilisation d’une application en mode de fonctionnement déconnecté.</span><span class="sxs-lookup"><span data-stu-id="2af8d-371">Indicates how many minutes an application may be used in disconnected operation mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2af8d-372">Les valeurs valides sont comprises entre 1 et 999999 en jours exprimées en minutes (1 – 1439998560 minutes).</span><span class="sxs-lookup"><span data-stu-id="2af8d-372">The valid values are 1–999,999 in days expressed in minutes (1–1,439,998,560 minutes).</span></span> <span data-ttu-id="2af8d-373">La valeur par défaut est 90 jours ou 129 600 minutes.</span><span class="sxs-lookup"><span data-stu-id="2af8d-373">The default value is 90 days or 129,600 minutes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-374">Protocole</span><span class="sxs-lookup"><span data-stu-id="2af8d-374">Protocol</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-375">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-375">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-376">Par défaut = 8</span><span class="sxs-lookup"><span data-stu-id="2af8d-376">Default=8</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-377">Protocole par défaut à utiliser (TCP ou SSL).</span><span class="sxs-lookup"><span data-stu-id="2af8d-377">Default protocol to use (TCP vs SSL).</span></span> <span data-ttu-id="2af8d-378">Configurer dans la boîte de dialogue Options.</span><span class="sxs-lookup"><span data-stu-id="2af8d-378">Configure in Options Dialog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-379">ReadTimeout</span><span class="sxs-lookup"><span data-stu-id="2af8d-379">ReadTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-380">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-380">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-381">CX3-20</span><span class="sxs-lookup"><span data-stu-id="2af8d-381">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-382">Délai de lecture des transactions réseau, en secondes.</span><span class="sxs-lookup"><span data-stu-id="2af8d-382">Read time-out for network transactions, in seconds.</span></span> <span data-ttu-id="2af8d-383">Ne modifiez pas.</span><span class="sxs-lookup"><span data-stu-id="2af8d-383">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-384">WriteTimeout</span><span class="sxs-lookup"><span data-stu-id="2af8d-384">WriteTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-385">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-385">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-386">CX3-20</span><span class="sxs-lookup"><span data-stu-id="2af8d-386">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-387">Notez le délai d’expiration des transactions réseau, en quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="2af8d-387">Write time-out for network transactions, in seconds.</span></span> <span data-ttu-id="2af8d-388">Ne modifiez pas.</span><span class="sxs-lookup"><span data-stu-id="2af8d-388">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-389">ConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="2af8d-389">ConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-390">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-390">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-391">CX3-20</span><span class="sxs-lookup"><span data-stu-id="2af8d-391">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-392">Délai de connexion des transactions réseau, en secondes.</span><span class="sxs-lookup"><span data-stu-id="2af8d-392">Connect time-out for network transactions, in seconds.</span></span> <span data-ttu-id="2af8d-393">Ne modifiez pas.</span><span class="sxs-lookup"><span data-stu-id="2af8d-393">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-394">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="2af8d-394">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-396">3D</span><span class="sxs-lookup"><span data-stu-id="2af8d-396">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-397">Nombre d’occurrences d’une tentative de rétablissement d’une session interrompue.</span><span class="sxs-lookup"><span data-stu-id="2af8d-397">The number of times to try to reestablish a dropped session.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-398">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="2af8d-398">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-399">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-399">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-400">0,15</span><span class="sxs-lookup"><span data-stu-id="2af8d-400">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-401">Nombre de secondes d’attente entre les tentatives de rétablissement d’une session perdue.</span><span class="sxs-lookup"><span data-stu-id="2af8d-401">The number of seconds to wait between tries to reestablish a dropped session.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2af8d-402">Clé http</span><span class="sxs-lookup"><span data-stu-id="2af8d-402">Http Key</span></span>


<span data-ttu-id="2af8d-403">La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http contrôle les paramètres liés au streaming http.</span><span class="sxs-lookup"><span data-stu-id="2af8d-403">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http key controls the parameters that are related to Http streaming.</span></span> <span data-ttu-id="2af8d-404">Cette clé est essentiellement utilisée par l’agent de transport réseau.</span><span class="sxs-lookup"><span data-stu-id="2af8d-404">This key is used primarily by the network transport agent.</span></span> <span data-ttu-id="2af8d-405">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé http.</span><span class="sxs-lookup"><span data-stu-id="2af8d-405">The following table provides information about the registry values that are associated with the Http key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2af8d-406">Nom</span><span class="sxs-lookup"><span data-stu-id="2af8d-406">Name</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-407">Type</span><span class="sxs-lookup"><span data-stu-id="2af8d-407">Type</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-408">Données (exemples)</span><span class="sxs-lookup"><span data-stu-id="2af8d-408">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-409">Description</span><span class="sxs-lookup"><span data-stu-id="2af8d-409">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-410">LaunchIfNotFound</span><span class="sxs-lookup"><span data-stu-id="2af8d-410">LaunchIfNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-411">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-411">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-412">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-412">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-413">Contrôle le comportement de la diffusion HTTP en continu lorsqu’une connexion au serveur HTTP peut être établie et que le fichier de package n’existe plus sur le serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="2af8d-413">Controls the behavior of HTTP streaming when a connection to the HTTP server can be established and the package file no longer exists on the HTTP server.</span></span> <span data-ttu-id="2af8d-414">Si la valeur n’existe pas ou si elle n’est pas définie sur 1, le client App-V ne vous permet pas de lancer une application qui a déjà été chargée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-414">If the value does not exist or if it is not set to 1, the App-V client does not let you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2af8d-415">1</span><span class="sxs-lookup"><span data-stu-id="2af8d-415">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-416">Si cette valeur est définie sur 1, le client App-V vous permet de lancer une application qui a déjà été chargée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-416">If this value is set to 1, the App-V client lets you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2af8d-417">Clé de système de fichiers</span><span class="sxs-lookup"><span data-stu-id="2af8d-417">File System Key</span></span>


<span data-ttu-id="2af8d-418">Les valeurs contenues sous la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS contrôlent les paramètres du système de fichiers pour App-V.</span><span class="sxs-lookup"><span data-stu-id="2af8d-418">The values that are contained under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS key control the file system parameters for App-V.</span></span> <span data-ttu-id="2af8d-419">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé AppFS.</span><span class="sxs-lookup"><span data-stu-id="2af8d-419">The following table provides information about the registry values associated with the AppFS key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2af8d-420">Nom</span><span class="sxs-lookup"><span data-stu-id="2af8d-420">Name</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-421">Type</span><span class="sxs-lookup"><span data-stu-id="2af8d-421">Type</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-422">Données (exemples)</span><span class="sxs-lookup"><span data-stu-id="2af8d-422">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-423">Description</span><span class="sxs-lookup"><span data-stu-id="2af8d-423">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-424">FileSize</span><span class="sxs-lookup"><span data-stu-id="2af8d-424">FileSize</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-425">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-425">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-426">4096</span><span class="sxs-lookup"><span data-stu-id="2af8d-426">4096</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-427">Taille maximale en mégaoctets du fichier cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2af8d-427">Maximum size in megabytes of file system cache file.</span></span> <span data-ttu-id="2af8d-428">Si vous modifiez cette valeur dans le registre, vous devez définir l’État sur 0 et redémarrer.</span><span class="sxs-lookup"><span data-stu-id="2af8d-428">If you change this value in the registry, you must set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-429">FileName</span><span class="sxs-lookup"><span data-stu-id="2af8d-429">FileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-430">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-430">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="2af8d-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-432">Emplacement du fichier cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2af8d-432">Location of file system cache file.</span></span> <span data-ttu-id="2af8d-433">Si vous modifiez cette valeur dans le registre, vous devez laisser FileSize le même et redémarrer ou définir l’État sur 0 et redémarrer.</span><span class="sxs-lookup"><span data-stu-id="2af8d-433">If you change this value in the registry, you must either leave FileSize the same and reboot or set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-434">LettreLecteur</span><span class="sxs-lookup"><span data-stu-id="2af8d-434">DriveLetter</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-435">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-435">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-436">Q:</span><span class="sxs-lookup"><span data-stu-id="2af8d-436">Q:</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-437">Lecteur sur lequel le système de fichiers App-V sera monté, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="2af8d-437">Drive where App-V file system will be mounted, if it is available.</span></span> <span data-ttu-id="2af8d-438">Cette valeur est définie par l’écouteur ou le programme d’installation, et est lue par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2af8d-438">This value is set either by the listener or the installer, and it is read by the file system.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-439">État</span><span class="sxs-lookup"><span data-stu-id="2af8d-439">State</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-440">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-440">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-441">0x100</span><span class="sxs-lookup"><span data-stu-id="2af8d-441">0x100</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-442">État du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2af8d-442">State of file system.</span></span> <span data-ttu-id="2af8d-443">Définissez la valeur sur 0 et redémarrez pour effacer entièrement le cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2af8d-443">Set to 0 and reboot to completely clear the file system cache.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-444">FileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="2af8d-444">FileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-445">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-445">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-446">C:\Profiles\Joe\SG</span><span class="sxs-lookup"><span data-stu-id="2af8d-446">C:\Profiles\Joe\SG</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-447">Path pour symlinks, définie sous HKCU.</span><span class="sxs-lookup"><span data-stu-id="2af8d-447">Path for symlinks, set under HKCU.</span></span> <span data-ttu-id="2af8d-448">Ne pas modifier (utilisez le répertoire des données sous Configuration pour le modifier).</span><span class="sxs-lookup"><span data-stu-id="2af8d-448">Do not modify (use data directory under Configuration to change).</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-449">GlobalFileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="2af8d-449">GlobalFileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-450">String</span><span class="sxs-lookup"><span data-stu-id="2af8d-450">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-451">C:\Users\Public\Documents\SoftGrid Client\AppFS Storage</span><span class="sxs-lookup"><span data-stu-id="2af8d-451">C:\Users\Public\Documents\SoftGrid Client\AppFS Storage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-452">Chemin pour les données du système de fichiers global.</span><span class="sxs-lookup"><span data-stu-id="2af8d-452">Path for global file system data.</span></span> <span data-ttu-id="2af8d-453">Ne modifiez pas.</span><span class="sxs-lookup"><span data-stu-id="2af8d-453">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-454">MaxPercentToLockInCache</span><span class="sxs-lookup"><span data-stu-id="2af8d-454">MaxPercentToLockInCache</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-455">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-455">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-456">Valeur par défaut = 90</span><span class="sxs-lookup"><span data-stu-id="2af8d-456">Default=90</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-457">Spécifie le pourcentage maximal du fichier cache du système de fichiers qui peut être verrouillé.</span><span class="sxs-lookup"><span data-stu-id="2af8d-457">Specifies the maximum percentage of the file system cache file that can be locked.</span></span> <span data-ttu-id="2af8d-458">Ne modifiez pas.</span><span class="sxs-lookup"><span data-stu-id="2af8d-458">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-459">UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="2af8d-459">UnloadLeastRecentlyUsed</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-460">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-460">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-461">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="2af8d-461">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-462">La fonctionnalité de gestion de l’espace dans le système de fichiers utilise un algorithme de dernier recours (LRU) et est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="2af8d-462">The file system cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="2af8d-463">Si l’espace requis pour un nouveau package dépasse l’espace libre disponible dans le cache, le client App-V utilise cette fonctionnalité pour déterminer, le cas échéant, les packages existants qu’il peut supprimer du cache pour libérer de l’espace pour le nouveau package.</span><span class="sxs-lookup"><span data-stu-id="2af8d-463">If the space that is required for a new package would exceed the available free space in the cache, the App-V Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="2af8d-464">Le client supprime le package avec la dernière date à laquelle il est consulté le plus ancien s’il est antérieur à la valeur spécifiée dans la valeur de Registre MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="2af8d-464">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="2af8d-465">Les valeurs sont 0 (désactivées) et 1 (valeur par défaut activée).</span><span class="sxs-lookup"><span data-stu-id="2af8d-465">Values are 0 (disabled) and 1 (default, enabled).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-466">MinPackageAge</span><span class="sxs-lookup"><span data-stu-id="2af8d-466">MinPackageAge</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-467">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-467">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-468">1</span><span class="sxs-lookup"><span data-stu-id="2af8d-468">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-469">Pour déterminer à quel moment le package peut être sélectionné pour ignorer, définissez cette valeur de Registre sur égal au nombre minimal de jours que vous souhaitez voir s’écouler après le dernier accès au package.</span><span class="sxs-lookup"><span data-stu-id="2af8d-469">To determine when the package can be selected for discard, set this registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="2af8d-470">Les packages utilisés plus récemment ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="2af8d-470">Packages that have been used more recently are not discarded.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2af8d-471">Touche autorisations</span><span class="sxs-lookup"><span data-stu-id="2af8d-471">Permissions Key</span></span>


<span data-ttu-id="2af8d-472">Pour empêcher les utilisateurs d’effectuer des erreurs, les administrateurs peuvent utiliser la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions pour contrôler l’accès à certaines actions pour les utilisateurs non administrateurs, par exemple pour empêcher les utilisateurs de décharger accidentellement des programmes.</span><span class="sxs-lookup"><span data-stu-id="2af8d-472">To help to prevent users from making mistakes, administrators can use the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions key to control access to some actions for non-administrative users—for example, to prevent users from accidentally unloading programs.</span></span> <span data-ttu-id="2af8d-473">Les utilisateurs disposant de droits d’administration peuvent lui accorder une de ces autorisations.</span><span class="sxs-lookup"><span data-stu-id="2af8d-473">Users with administrative rights can give themselves any of these permissions.</span></span> <span data-ttu-id="2af8d-474">Sur les systèmes partagés, tels qu’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) (anciennement Terminal Server), veillez à accorder des autorisations supplémentaires aux utilisateurs, car certaines de ces autorisations permettent aux utilisateurs de contrôler les applications utilisées par tous les utilisateurs sur le système.</span><span class="sxs-lookup"><span data-stu-id="2af8d-474">On shared systems, such as a Remote Desktop Session Host (RD Session Host) server (formerly Terminal Server) system, be careful when granting additional permissions to users because some of these permissions would enable users to control the applications used by all users on the system.</span></span> <span data-ttu-id="2af8d-475">Les valeurs possibles de ces paramètres sont 1 (Allow) et 0 (Disallow).</span><span class="sxs-lookup"><span data-stu-id="2af8d-475">Possible values for these settings are 1 (allow) and 0 (disallow).</span></span>

<span data-ttu-id="2af8d-476">Les paramètres de touches autorisations contrôlent toutes les interfaces qui activent les actions nommées.</span><span class="sxs-lookup"><span data-stu-id="2af8d-476">The Permissions key settings control all interfaces that enable the named actions.</span></span> <span data-ttu-id="2af8d-477">Cela inclut la boîte de dialogue Options, SFTTray et SFTMime.</span><span class="sxs-lookup"><span data-stu-id="2af8d-477">This includes the Options Dialog, SFTTray, and SFTMime.</span></span> <span data-ttu-id="2af8d-478">Ces paramètres n’ont aucun impact sur les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="2af8d-478">These settings do not affect administrators.</span></span> <span data-ttu-id="2af8d-479">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé autorisations.</span><span class="sxs-lookup"><span data-stu-id="2af8d-479">The following table provides information about the registry values associated with the Permissions key.</span></span>

<span data-ttu-id="2af8d-480">Données de type de nom (exemples) Description ChangeFSDrive</span><span class="sxs-lookup"><span data-stu-id="2af8d-480">Name Type Data (Examples) Description ChangeFSDrive</span></span>

<span data-ttu-id="2af8d-481">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-481">DWORD</span></span>

<span data-ttu-id="2af8d-482">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-482">Default=0</span></span>

<span data-ttu-id="2af8d-483">La valeur 1 permet aux utilisateurs de sélectionner une autre lettre de lecteur à utiliser comme lecteur du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2af8d-483">A value of 1 allows users to pick a different drive letter to be used as the file system drive.</span></span>

<span data-ttu-id="2af8d-484">ChangeCacheSize</span><span class="sxs-lookup"><span data-stu-id="2af8d-484">ChangeCacheSize</span></span>

<span data-ttu-id="2af8d-485">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-485">DWORD</span></span>

<span data-ttu-id="2af8d-486">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-486">Default=0</span></span>

<span data-ttu-id="2af8d-487">La valeur 1 permet aux utilisateurs de modifier la taille du cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-487">A value of 1 allows users to change the cache size.</span></span>

<span data-ttu-id="2af8d-488">ChangeLogSettings</span><span class="sxs-lookup"><span data-stu-id="2af8d-488">ChangeLogSettings</span></span>

<span data-ttu-id="2af8d-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-489">DWORD</span></span>

<span data-ttu-id="2af8d-490">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-490">Default=0</span></span>

<span data-ttu-id="2af8d-491">La valeur 1 permet aux utilisateurs de modifier le niveau du journal, de modifier son emplacement et de le réinitialiser par le biais de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2af8d-491">A value of 1 allows users to modify the log level, change its location, and reset it through the user interface.</span></span>

<span data-ttu-id="2af8d-492">AddApp</span><span class="sxs-lookup"><span data-stu-id="2af8d-492">AddApp</span></span>

<span data-ttu-id="2af8d-493">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-493">DWORD</span></span>

<span data-ttu-id="2af8d-494">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-494">Default=0</span></span>

<span data-ttu-id="2af8d-495">La valeur 1 permet aux utilisateurs d’ajouter explicitement des applications.</span><span class="sxs-lookup"><span data-stu-id="2af8d-495">A value of 1 allows users to add applications explicitly.</span></span> <span data-ttu-id="2af8d-496">Cela n’affecte pas les applications ajoutées par le biais de la mise à jour de la publication, ou empêche les utilisateurs de démarrer (et donc d’ajouter implicitement) des applications qui n’ont pas encore été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="2af8d-496">This does not affect applications that are added through publishing refresh nor does it prevent users from starting (and thereby implicitly adding) applications that have not already been added.</span></span> <span data-ttu-id="2af8d-497">Les valeurs sont 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="2af8d-497">Values are 0 or 1.</span></span>

<span data-ttu-id="2af8d-498">LoadApp</span><span class="sxs-lookup"><span data-stu-id="2af8d-498">LoadApp</span></span> 

<span data-ttu-id="2af8d-499">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-499">DWORD</span></span> 

<span data-ttu-id="2af8d-500">0,4</span><span class="sxs-lookup"><span data-stu-id="2af8d-500">0</span></span>

<span data-ttu-id="2af8d-501">Ne permet pas à un utilisateur de charger une application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-501">Does not allow a user to load an application.</span></span> <span data-ttu-id="2af8d-502">Il s’agit de la valeur par défaut pour les hôtes de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2af8d-502">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="2af8d-503">Si vous êtes un utilisateur mobile, vous souhaiterez peut-être charger entièrement vos applications dans le cache pour les utiliser en mode hors connexion ou en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2af8d-503">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="2af8d-504">Pour diffuser des applications à partir du serveur de gestion App-V ou du serveur de streaming App-V, vous devez être connecté à un serveur pour charger des applications.</span><span class="sxs-lookup"><span data-stu-id="2af8d-504">To stream applications from the App-V Management Server or the App-V Streaming Server, you must be connected to a server to load applications.</span></span>

<span data-ttu-id="2af8d-505">1</span><span class="sxs-lookup"><span data-stu-id="2af8d-505">1</span></span>

<span data-ttu-id="2af8d-506">Permet à un utilisateur de charger une application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-506">Allows a user to load an application.</span></span> <span data-ttu-id="2af8d-507">Il s’agit de la valeur par défaut pour les ordinateurs de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="2af8d-507">This is the default for Windows desktops.</span></span> 

<span data-ttu-id="2af8d-508">UnloadApp</span><span class="sxs-lookup"><span data-stu-id="2af8d-508">UnloadApp</span></span> 

<span data-ttu-id="2af8d-509">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-509">DWORD</span></span> 

<span data-ttu-id="2af8d-510">0,4</span><span class="sxs-lookup"><span data-stu-id="2af8d-510">0</span></span>

<span data-ttu-id="2af8d-511">Ne permet pas à un utilisateur de décharger une application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-511">Does not allow a user to unload an application.</span></span> <span data-ttu-id="2af8d-512">Lorsque vous chargez ou déchargez un package, toutes les applications du package sont chargées ou supprimées du cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-512">When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span>

<span data-ttu-id="2af8d-513">1</span><span class="sxs-lookup"><span data-stu-id="2af8d-513">1</span></span>

<span data-ttu-id="2af8d-514">Permet à un utilisateur de décharger une application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-514">Allows a user to unload an application.</span></span> 

<span data-ttu-id="2af8d-515">LockApp</span><span class="sxs-lookup"><span data-stu-id="2af8d-515">LockApp</span></span> 

<span data-ttu-id="2af8d-516">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-516">DWORD</span></span> 

<span data-ttu-id="2af8d-517">0,4</span><span class="sxs-lookup"><span data-stu-id="2af8d-517">0</span></span>

<span data-ttu-id="2af8d-518">Ne permet pas à un utilisateur de verrouiller et de déverrouiller une application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-518">Does not allow a user to lock and unlock an application.</span></span> <span data-ttu-id="2af8d-519">Il s’agit de la valeur par défaut pour les hôtes de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2af8d-519">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="2af8d-520">Une application verrouillée ne peut pas être supprimée du cache pour libérer de l’espace pour les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="2af8d-520">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="2af8d-521">Pour supprimer une application verrouillée du Bureau App-V ou du client pour les services Bureau à distance (anciennement services Terminal Server), vous devez déverrouiller celle-ci.</span><span class="sxs-lookup"><span data-stu-id="2af8d-521">To remove a locked application from the App-V Desktop or Client for Remote Desktop Services (formerly Terminal Services) cache, you must unlock it.</span></span>

<span data-ttu-id="2af8d-522">1</span><span class="sxs-lookup"><span data-stu-id="2af8d-522">1</span></span>

<span data-ttu-id="2af8d-523">Permet à un utilisateur de verrouiller et de déverrouiller une application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-523">Allows a user to lock and unlock an application.</span></span> <span data-ttu-id="2af8d-524">Il s’agit de la valeur par défaut pour les ordinateurs de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="2af8d-524">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="2af8d-525">ManageTypes</span><span class="sxs-lookup"><span data-stu-id="2af8d-525">ManageTypes</span></span> 

<span data-ttu-id="2af8d-526">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-526">DWORD</span></span> 

<span data-ttu-id="2af8d-527">0,4</span><span class="sxs-lookup"><span data-stu-id="2af8d-527">0</span></span>

<span data-ttu-id="2af8d-528">Ne permet pas à un utilisateur d’ajouter, de modifier ou de supprimer des associations de types de fichiers uniquement pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2af8d-528">Does not allow a user to add, edit, or remove file type associations for that User alone.</span></span> <span data-ttu-id="2af8d-529">Il s’agit de la valeur par défaut pour les hôtes de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2af8d-529">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="2af8d-530">1</span><span class="sxs-lookup"><span data-stu-id="2af8d-530">1</span></span>

<span data-ttu-id="2af8d-531">Permet à un utilisateur d’ajouter, de modifier et de supprimer des associations de type de fichier uniquement pour cet utilisateur et pas globalement.</span><span class="sxs-lookup"><span data-stu-id="2af8d-531">Allows a user to add, edit, and remove file type associations for that user only and not globally.</span></span> <span data-ttu-id="2af8d-532">Il s’agit de la valeur par défaut pour les ordinateurs de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="2af8d-532">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="2af8d-533">RefreshServer</span><span class="sxs-lookup"><span data-stu-id="2af8d-533">RefreshServer</span></span> 

<span data-ttu-id="2af8d-534">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-534">DWORD</span></span> 

<span data-ttu-id="2af8d-535">0,4</span><span class="sxs-lookup"><span data-stu-id="2af8d-535">0</span></span>

<span data-ttu-id="2af8d-536">Ne permet pas à un utilisateur de déclencher une actualisation des paramètres MIME.</span><span class="sxs-lookup"><span data-stu-id="2af8d-536">Does not allow a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="2af8d-537">Il s’agit de la valeur par défaut pour les hôtes de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2af8d-537">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="2af8d-538">1</span><span class="sxs-lookup"><span data-stu-id="2af8d-538">1</span></span>

<span data-ttu-id="2af8d-539">Permet à un utilisateur de déclencher une actualisation des paramètres MIME.</span><span class="sxs-lookup"><span data-stu-id="2af8d-539">Enables a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="2af8d-540">Il s’agit de la valeur par défaut pour les ordinateurs de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="2af8d-540">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="2af8d-541">UpdateOSDFile</span><span class="sxs-lookup"><span data-stu-id="2af8d-541">UpdateOSDFile</span></span>

<span data-ttu-id="2af8d-542">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-542">DWORD</span></span>

<span data-ttu-id="2af8d-543">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-543">Default= 0</span></span>

<span data-ttu-id="2af8d-544">La valeur 1 permet à un utilisateur d’utiliser un fichier OSD modifié.</span><span class="sxs-lookup"><span data-stu-id="2af8d-544">A value of 1 enables a user to use a modified OSD file.</span></span>

<span data-ttu-id="2af8d-545">ImportApp</span><span class="sxs-lookup"><span data-stu-id="2af8d-545">ImportApp</span></span> 

<span data-ttu-id="2af8d-546">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-546">DWORD</span></span> 

<span data-ttu-id="2af8d-547">0,4</span><span class="sxs-lookup"><span data-stu-id="2af8d-547">0</span></span>

<span data-ttu-id="2af8d-548">Ne permet pas à un utilisateur d’importer des applications dans le cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-548">Does not allow a user to import applications into cache.</span></span> <span data-ttu-id="2af8d-549">La différence entre Load et Import réside dans le fait que le client obtient le package à partir de l’emplacement actuellement configuré contenu dans l’URL d’OSD, ASR ou override.</span><span class="sxs-lookup"><span data-stu-id="2af8d-549">The difference between Load and Import is that when a Load is triggered, the client gets the package from the currently configured location contained in the OSD, ASR, or Override URL.</span></span> <span data-ttu-id="2af8d-550">Lors de l’utilisation de l’importation, un emplacement à partir duquel obtenir le package doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="2af8d-550">When using Import, a location to get the package from must be specified.</span></span> 

<span data-ttu-id="2af8d-551">1</span><span class="sxs-lookup"><span data-stu-id="2af8d-551">1</span></span>

<span data-ttu-id="2af8d-552">Permet à un utilisateur d’importer des applications dans le cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-552">Allows a user to import applications into cache.</span></span> 

<span data-ttu-id="2af8d-553">ChangeRefreshSettings</span><span class="sxs-lookup"><span data-stu-id="2af8d-553">ChangeRefreshSettings</span></span>

<span data-ttu-id="2af8d-554">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-554">DWORD</span></span>

<span data-ttu-id="2af8d-555">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-555">Default=0</span></span>

<span data-ttu-id="2af8d-556">La valeur 1 permet aux utilisateurs de modifier les paramètres d’actualisation des serveurs (actualisation à la connexion et actualisation périodique).</span><span class="sxs-lookup"><span data-stu-id="2af8d-556">A value of 1 allows users to modify the refresh settings for servers (refresh on login and periodic refresh).</span></span> <span data-ttu-id="2af8d-557">Cela ne signifie pas que l’utilisateur peut modifier les autres paramètres du serveur (chemin d’accès, hôte, etc.).</span><span class="sxs-lookup"><span data-stu-id="2af8d-557">This does not imply that the user can modify other server settings (path, host, and so on).</span></span>

<span data-ttu-id="2af8d-558">ManageServers</span><span class="sxs-lookup"><span data-stu-id="2af8d-558">ManageServers</span></span>

<span data-ttu-id="2af8d-559">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-559">DWORD</span></span>

<span data-ttu-id="2af8d-560">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-560">Default=0</span></span>

<span data-ttu-id="2af8d-561">La valeur 1 permet à l’utilisateur d’ajouter, de modifier et de supprimer des serveurs, à l’exception de la modification des paramètres d’actualisation, qui est contrôlée par l’autorisation ChangeRefreshSettings.</span><span class="sxs-lookup"><span data-stu-id="2af8d-561">A value of 1 allows the user to add, edit, and remove servers, except for editing the refresh settings, which is controlled by the ChangeRefreshSettings permission.</span></span>

<span data-ttu-id="2af8d-562">PublishShortcut</span><span class="sxs-lookup"><span data-stu-id="2af8d-562">PublishShortcut</span></span>

<span data-ttu-id="2af8d-563">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-563">DWORD</span></span>

<span data-ttu-id="2af8d-564">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-564">Default=0</span></span>

<span data-ttu-id="2af8d-565">La valeur 1 permet aux utilisateurs de publier des raccourcis par le biais de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2af8d-565">A value of 1 allows users to publish shortcuts through the user interface.</span></span> <span data-ttu-id="2af8d-566">Cela n’affecte pas les raccourcis publiés lors de l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="2af8d-566">This does not affect shortcuts that are published during a publishing refresh.</span></span>

<span data-ttu-id="2af8d-567">ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="2af8d-567">ViewAllApplications</span></span>

<span data-ttu-id="2af8d-568">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-568">DWORD</span></span>

<span data-ttu-id="2af8d-569">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-569">Default=0</span></span>

<span data-ttu-id="2af8d-570">La valeur 1 affiche toutes les applications par le biais de l’interface utilisateur; dans le cas contraire, seules les applications de l’utilisateur sont affichées.</span><span class="sxs-lookup"><span data-stu-id="2af8d-570">A value of 1 displays all applications through the user interface; otherwise, only the user’s applications are displayed.</span></span>

<span data-ttu-id="2af8d-571">RepairApp</span><span class="sxs-lookup"><span data-stu-id="2af8d-571">RepairApp</span></span>

<span data-ttu-id="2af8d-572">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-572">DWORD</span></span>

<span data-ttu-id="2af8d-573">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="2af8d-573">Default=1</span></span>

<span data-ttu-id="2af8d-574">La valeur 1 permet à l’utilisateur d’utiliser l’action de réparation sur les applications dans SFTMime ou la console de gestion du client.</span><span class="sxs-lookup"><span data-stu-id="2af8d-574">A value of 1 allows the user to use the Repair action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="2af8d-575">Lorsque vous réparez une application, vous supprimez les paramètres utilisateur personnalisés et restaurez les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="2af8d-575">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="2af8d-576">Cette action ne modifie pas ou ne supprime aucun raccourci ou association de type de fichier, et ne supprime pas l’application du cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-576">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

<span data-ttu-id="2af8d-577">ClearApp</span><span class="sxs-lookup"><span data-stu-id="2af8d-577">ClearApp</span></span>

<span data-ttu-id="2af8d-578">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-578">DWORD</span></span>

<span data-ttu-id="2af8d-579">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="2af8d-579">Default=1</span></span>

<span data-ttu-id="2af8d-580">La valeur 1 permet à l’utilisateur d’utiliser l’action Effacer sur les applications dans SFTMime ou la console de gestion du client.</span><span class="sxs-lookup"><span data-stu-id="2af8d-580">A value of 1 allows the user to use the Clear action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="2af8d-581">Lorsque vous effacez une application de la console, vous ne pouvez plus utiliser cette application.</span><span class="sxs-lookup"><span data-stu-id="2af8d-581">When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="2af8d-582">Toutefois, l’application reste en cache et reste disponible pour les autres utilisateurs du même système.</span><span class="sxs-lookup"><span data-stu-id="2af8d-582">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="2af8d-583">Après une actualisation de publication, les applications effacées seront de nouveau accessibles.</span><span class="sxs-lookup"><span data-stu-id="2af8d-583">After a publishing refresh, the cleared applications will again become available to you.</span></span>

<span data-ttu-id="2af8d-584">DeleteApp</span><span class="sxs-lookup"><span data-stu-id="2af8d-584">DeleteApp</span></span>

<span data-ttu-id="2af8d-585">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-585">DWORD</span></span>

<span data-ttu-id="2af8d-586">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-586">Default=0</span></span>

<span data-ttu-id="2af8d-587">La valeur 1 permet à l’utilisateur d’utiliser l’action de suppression sur les applications dans SFTMime ou la console de gestion du client.</span><span class="sxs-lookup"><span data-stu-id="2af8d-587">A value of 1 allows the user to use the Delete action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="2af8d-588">Lorsque vous supprimez une application, l’application sélectionnée ne sera plus disponible pour les utilisateurs de ce client.</span><span class="sxs-lookup"><span data-stu-id="2af8d-588">When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="2af8d-589">Les raccourcis et les associations de types de fichiers sont supprimés et l’application est supprimée du cache.</span><span class="sxs-lookup"><span data-stu-id="2af8d-589">Shortcuts and file type associations are deleted and the application is deleted from cache.</span></span> <span data-ttu-id="2af8d-590">Toutefois, si une autre application fait référence à des données dans le cache du système de fichiers ou des données de paramètres pour l’application sélectionnée, ces éléments ne seront pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="2af8d-590">However, if another application refers to data in the file system cache or settings data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="2af8d-591">Après une actualisation de publication, les applications supprimées vous sont à nouveau accessibles.</span><span class="sxs-lookup"><span data-stu-id="2af8d-591">After a publishing refresh, the deleted applications will again become available to you.</span></span>

<span data-ttu-id="2af8d-592">ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="2af8d-592">ToggleOfflineMode</span></span>

<span data-ttu-id="2af8d-593">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-593">DWORD</span></span>

<span data-ttu-id="2af8d-594">La valeur 1 permet aux utilisateurs de sélectionner l’exécution du client en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2af8d-594">A value of 1 allows the users to select to run the client in Offline Mode.</span></span> <span data-ttu-id="2af8d-595">En mode hors connexion, le client de virtualisation des applications peut démarrer une application chargée même lorsqu’elle n’est pas connectée à un serveur de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="2af8d-595">In Offline Mode, the Application Virtualization client can start a loaded application even when it is not connected to an Application Virtualization Server.</span></span>



## <span data-ttu-id="2af8d-596">Paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="2af8d-596">Custom Settings</span></span>


<span data-ttu-id="2af8d-597">La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings contient des valeurs spécifiques aux composants frontaux.</span><span class="sxs-lookup"><span data-stu-id="2af8d-597">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings key contains values specific to front-end components.</span></span> <span data-ttu-id="2af8d-598">Tous les paramètres personnalisés sont stockés en tant que chaînes.</span><span class="sxs-lookup"><span data-stu-id="2af8d-598">All custom settings are stored as strings.</span></span> <span data-ttu-id="2af8d-599">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé CustomSettings.</span><span class="sxs-lookup"><span data-stu-id="2af8d-599">The following table provides information about the registry values associated with the CustomSettings key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2af8d-600">Nom</span><span class="sxs-lookup"><span data-stu-id="2af8d-600">Name</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-601">Type</span><span class="sxs-lookup"><span data-stu-id="2af8d-601">Type</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-602">Données (exemples)</span><span class="sxs-lookup"><span data-stu-id="2af8d-602">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-603">Description</span><span class="sxs-lookup"><span data-stu-id="2af8d-603">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-604">TrayErrorDelay</span><span class="sxs-lookup"><span data-stu-id="2af8d-604">TrayErrorDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-605">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-605">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-606">Par défaut = 30</span><span class="sxs-lookup"><span data-stu-id="2af8d-606">Default=30</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-607">Durée en secondes pendant laquelle la zone de notification de virtualisation des applications affiche des messages d’erreur tels que le &quot; lancement a échoué &quot; .</span><span class="sxs-lookup"><span data-stu-id="2af8d-607">Time in seconds that the Application Virtualization notification area will display error messages like &quot;Launch failed&quot;.</span></span> <span data-ttu-id="2af8d-608">Valeur minimale de 1.</span><span class="sxs-lookup"><span data-stu-id="2af8d-608">Minimum value of 1.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-609">TraySuccessDelay</span><span class="sxs-lookup"><span data-stu-id="2af8d-609">TraySuccessDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-610">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-610">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-611">Par défaut = 10</span><span class="sxs-lookup"><span data-stu-id="2af8d-611">Default=10</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2af8d-612">Durée en secondes pendant laquelle la zone de notification appvmed affiche des messages de réussite tels que &quot; Word lancé &quot; ou &quot; Excel s’arrête &quot; .</span><span class="sxs-lookup"><span data-stu-id="2af8d-612">Time in seconds that the appvmed notification area will display success messages like &quot;Word launched&quot; or &quot;Excel shut down&quot;.</span></span> <span data-ttu-id="2af8d-613">Si la valeur est 0, ces messages seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="2af8d-613">If 0, those messages will be suppressed.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-614">TrayVisibility</span><span class="sxs-lookup"><span data-stu-id="2af8d-614">TrayVisibility</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-615">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-616">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="2af8d-616">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-617">0 = afficher la barre d’État lorsque les applications virtualisées sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="2af8d-617">0=Show Tray when virtualized applications are in use.</span></span></p>
<p><span data-ttu-id="2af8d-618">1 = afficher la barre d’État toujours.</span><span class="sxs-lookup"><span data-stu-id="2af8d-618">1=Show Tray always.</span></span></p>
<p><span data-ttu-id="2af8d-619">2 = ne jamais afficher la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="2af8d-619">2=Never show Tray.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-620">TrayShowRefresh</span><span class="sxs-lookup"><span data-stu-id="2af8d-620">TrayShowRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-621">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-621">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2af8d-622">Lorsque la valeur est définie et définie sur 1, permet d’afficher les applications d’actualisation des éléments de menu dans le menu de la barre d’état système et est accessible à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2af8d-622">When present and set to a value of 1, allows menu item Refresh Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-623">TrayShowLoad</span><span class="sxs-lookup"><span data-stu-id="2af8d-623">TrayShowLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-624">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-624">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2af8d-625">Lorsque la valeur est définie et définie sur 1, permet à l’élément de menu de charger les applications affichées dans le menu de la barre d’état système et est accessible à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2af8d-625">When present and set to a value of 1, allows menu item Load Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2af8d-626">Paramètres de création de rapports</span><span class="sxs-lookup"><span data-stu-id="2af8d-626">Reporting Settings</span></span>


<span data-ttu-id="2af8d-627">La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting contient des valeurs propres à la création de rapports sur un serveur de gestion d’applications-V.</span><span class="sxs-lookup"><span data-stu-id="2af8d-627">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting key contains values specific to reporting to an App-V Management Server.</span></span> <span data-ttu-id="2af8d-628">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="2af8d-628">The following table provides information about the registry values associated with the Reporting key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2af8d-629">Nom</span><span class="sxs-lookup"><span data-stu-id="2af8d-629">Name</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-630">Type</span><span class="sxs-lookup"><span data-stu-id="2af8d-630">Type</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-631">Données (exemples)</span><span class="sxs-lookup"><span data-stu-id="2af8d-631">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="2af8d-632">Description</span><span class="sxs-lookup"><span data-stu-id="2af8d-632">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af8d-633">DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="2af8d-633">DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-634">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-634">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-635">Par défaut = 20</span><span class="sxs-lookup"><span data-stu-id="2af8d-635">Default=20</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-636">Cette valeur spécifie la taille maximale en mégaoctets (Mo) du cache XML pour le stockage des informations de rapport.</span><span class="sxs-lookup"><span data-stu-id="2af8d-636">This value specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="2af8d-637">La taille s’applique au cache en mémoire.</span><span class="sxs-lookup"><span data-stu-id="2af8d-637">The size applies to the cache in memory.</span></span> <span data-ttu-id="2af8d-638">Lorsque la limite est atteinte, le fichier journal est restauré.</span><span class="sxs-lookup"><span data-stu-id="2af8d-638">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="2af8d-639">Lors de l’ajout d’un nouvel enregistrement (en bas de la liste), un ou plusieurs des enregistrements les plus anciens (haut de la liste) seront supprimés pour pouvoir libérer de l’espace.</span><span class="sxs-lookup"><span data-stu-id="2af8d-639">When a new record is added (bottom of the list), one or more of the oldest records (top of the list) will be deleted to make room.</span></span> <span data-ttu-id="2af8d-640">Un message d’avertissement sera consigné dans le journal du client et dans le journal des événements la première fois que cela se produit, et il ne sera pas enregistré de nouveau tant qu’il n’a pas été correctement vidé lors de la transmission et que le journal aura été rempli de nouveau.</span><span class="sxs-lookup"><span data-stu-id="2af8d-640">A warning will be logged to the Client log and the event log the first time this occurs, and it will not be logged again until after the cache has been successfully cleared on transmission and the log has filled up again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af8d-641">DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="2af8d-641">DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-642">DWORD</span><span class="sxs-lookup"><span data-stu-id="2af8d-642">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-643">Par défaut = 65536</span><span class="sxs-lookup"><span data-stu-id="2af8d-643">Default=65536</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af8d-644">Cette valeur spécifie la taille maximale en octets à transmettre au serveur en même temps lors de l’actualisation de la publication, afin d’éviter les échecs de transmission permanents lorsque le journal atteint une taille significative.</span><span class="sxs-lookup"><span data-stu-id="2af8d-644">This value specifies the maximum size in bytes to transmit to the server at once on publishing refresh, to avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="2af8d-645">La valeur par défaut est 65536.</span><span class="sxs-lookup"><span data-stu-id="2af8d-645">The default value is 65536.</span></span> <span data-ttu-id="2af8d-646">Lorsque vous transmettez des données de rapport au serveur, un bloc d’enregistrements d’application (inférieur ou égal à la taille du bloc en octets dans les données XML) est supprimé du cache et envoyé au serveur.</span><span class="sxs-lookup"><span data-stu-id="2af8d-646">When transmitting report data to the server, one block of application records—less than or equal to the block size in bytes of XML data—will be removed from the cache and sent to the server.</span></span> <span data-ttu-id="2af8d-647">Chaque bloc disposera des données générales du client et de la liste des packages globaux, et ces derniers ne seront pas pris en facteur dans les calculs de la taille du bloc. Il existe un potentiel pour une liste de packages extrêmement volumineux, qui engendre des échecs de transmission via des connexions à faible bande passante ou peu fiable.</span><span class="sxs-lookup"><span data-stu-id="2af8d-647">Each block will have the general Client data and global package list data prepended, and these will not factor into the block size calculations; the potential exists for an extremely large package list to result in transmission failures over low bandwidth or unreliable connections.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2af8d-648">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2af8d-648">Related topics</span></span>


[<span data-ttu-id="2af8d-649">Référence d'Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="2af8d-649">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)










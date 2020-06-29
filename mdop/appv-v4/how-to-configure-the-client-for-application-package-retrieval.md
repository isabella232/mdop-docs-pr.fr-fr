---
title: Procédure pour configurer le client afin d'extraire le package d'application
description: Procédure pour configurer le client afin d'extraire le package d'application
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807262"
---
# <span data-ttu-id="9f3b9-103">Procédure pour configurer le client afin d'extraire le package d'application</span><span class="sxs-lookup"><span data-stu-id="9f3b9-103">How to Configure the Client for Application Package Retrieval</span></span>


<span data-ttu-id="9f3b9-104">Lorsque le client est configuré à l’aide d’un serveur de gestion des applications (App-V) en tant que serveur de publication, par défaut lors du prochain cycle d’actualisation de la publication, le client récupère à partir du serveur les fichiers du manifeste de l’OSD (Open Software Descriptor) et du manifeste de package pour chaque package que l’utilisateur est autorisé à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-104">When the client is configured with an Application Virtualization (App-V) Management Server as its publishing server, by default at the next publishing refresh cycle, the client retrieves from the server the Open Software Descriptor (OSD) and package manifest files for each package that the user is authorized to use.</span></span> <span data-ttu-id="9f3b9-105">Le client utilise les informations de source de package définies dans ces fichiers pour déterminer où trouver le contenu, les icônes et les associations de types de fichiers du package.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-105">The client uses the package source information that is defined in these files to determine where to find the package content, icons, and file type associations.</span></span>

<span data-ttu-id="9f3b9-106">Si vous voulez que le client obtienne le contenu du package (fichier SFT) à partir d’un serveur de streaming App-V local ou d’une autre source, telle qu’un serveur Web ou un serveur de fichiers, au lieu du serveur d’administration App-V, vous pouvez configurer la valeur de clé de registre ApplicationSourceRoot sur l’ordinateur de manière à ce qu’elle pointe vers le partage de contenu local sur</span><span class="sxs-lookup"><span data-stu-id="9f3b9-106">If you want the client to obtain the package content (SFT file) from a local App-V Streaming Server or other alternate source such as a Web server or file server, instead of from the App-V Management Server, you can configure the ApplicationSourceRoot registry key value on the computer to point to the local content share on the other server.</span></span> <span data-ttu-id="9f3b9-107">Le fichier OSD définit quand même le chemin source d’origine pour le contenu du package.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-107">The OSD file still defines the original source path for the package content.</span></span> <span data-ttu-id="9f3b9-108">Toutefois, le client utilise la valeur du paramètre ApplicationSourceRoot à la place du serveur et du partage spécifiés dans le chemin d’accès du contenu du fichier OSD.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-108">However the client uses the value of the ApplicationSourceRoot setting in place of the server and share that are specified in the content path in the OSD file.</span></span> <span data-ttu-id="9f3b9-109">Cette opération permet de rediriger le client pour récupérer le contenu à partir de l’autre serveur.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-109">This redirects the client to retrieve the content from the other server.</span></span>

<span data-ttu-id="9f3b9-110">Vous pouvez également configurer les valeurs de clé de Registre OSDSourceRoot et IconSourceRoot si vous souhaitez remplacer ces paramètres dans le fichier manifeste du package ou dans les chemins d’accès envoyés par un serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-110">You can also configure the OSDSourceRoot and IconSourceRoot registry key values if you want to override those settings in the package manifest file or in the paths sent by a publishing server.</span></span> <span data-ttu-id="9f3b9-111">OSDSourceRoot spécifie un emplacement source pour la récupération de fichier OSD pour un package d’application au cours de la publication.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-111">The OSDSourceRoot specifies a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="9f3b9-112">IconSourceRoot spécifie un emplacement source pour la récupération d’icône pour un package d’application lors de la publication.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-112">The IconSourceRoot specifies a source location for icon retrieval for an application package during publication.</span></span>

**<span data-ttu-id="9f3b9-113">Remarque</span><span class="sxs-lookup"><span data-stu-id="9f3b9-113">Note</span></span>**  
-   <span data-ttu-id="9f3b9-114">Les paramètres IconSourceRoot et OSDSourceRoot remplacent les valeurs figurant dans le fichier manifeste du package, de sorte que si vous tentez de déployer un package à l’aide de la méthode de fichier Windows Installer (. msi), il remplacera également les valeurs du fichier manifeste de package contenu dans ce fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-114">The IconSourceRoot and OSDSourceRoot settings override the values in the package manifest file, so if you try to deploy a package by using the Windows Installer (.msi) file method, it will also override the values in the package manifest file that is contained within that .msi file.</span></span>

-   <span data-ttu-id="9f3b9-115">Au cours des opérations de diffusion en continu de publication et HTTP (S), les clients App-V 4,5 SP1 utilisent les paramètres du serveur proxy configurés dans Internet Explorer sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-115">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>



**<span data-ttu-id="9f3b9-116">Pour configurer la valeur de clé de registre ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="9f3b9-116">To configure the ApplicationSourceRoot registry key value</span></span>**

-   <span data-ttu-id="9f3b9-117">Dans la valeur de clé de Registre suivante, configurez le ApplicationSourceRoot à l’aide d’un chemin UNC ou d’une URL:</span><span class="sxs-lookup"><span data-stu-id="9f3b9-117">Configure the ApplicationSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="9f3b9-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="9f3b9-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span></span>

    <span data-ttu-id="9f3b9-119">Le format correct pour le chemin d’accès UNC (Universal Naming Convention) est **\\\\computername\\sharefolder\\\ [dossier \] \ [\ \ \]**, où le **dossier** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-119">The correct format for the Universal Naming Convention (UNC) path is **\\\\computername\\sharefolder\\\[folder\]\[\\\]**, where **folder** is optional.</span></span> <span data-ttu-id="9f3b9-120">**Nomordinateur** peut être un nom de domaine complet (FQDN, Fully Qualified Domain Name) ou une adresse IP, et **ShareFolder** peut être une lettre d’unité.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-120">The **computername** can be a Fully Qualified Domain Name (FQDN) or an IP address, and **sharefolder** can be a drive letter.</span></span> <span data-ttu-id="9f3b9-121">Seule la partie **\\\\computername\\sharedfolder** ou lettre de lecteur du chemin OSD est remplacée.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-121">Only the **\\\\computername\\sharedfolder** or drive letter portion of the OSD path is replaced.</span></span>

    <span data-ttu-id="9f3b9-122">Le format correct pour le chemin d’accès URL est **Protocol://servername: \ [port \] \ [/path\] \ [/\]**, où le **port** et le **chemin d’accès** sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-122">The correct format for the URL path is **protocol://servername:\[port\]\[/path\]\[/\]**, where **port** and **path** are optional.</span></span> <span data-ttu-id="9f3b9-123">Si **port** n’est pas spécifié, le port par défaut du protocole est utilisé.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-123">If **port** is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="9f3b9-124">Seule la partie **protocole://Server: port** de l’URL d’OSD est remplacée.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-124">Only the **protocol://server:port** portion of the OSD URL is replaced.</span></span>

    **<span data-ttu-id="9f3b9-125">Important</span><span class="sxs-lookup"><span data-stu-id="9f3b9-125">Important</span></span>**  
    <span data-ttu-id="9f3b9-126">Les variables d’environnement ne sont pas prises en charge dans la définition de ApplicationSourceRoot.</span><span class="sxs-lookup"><span data-stu-id="9f3b9-126">Environment variables are not supported in the ApplicationSourceRoot definition.</span></span>



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**<span data-ttu-id="9f3b9-127">Pour configurer la valeur OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="9f3b9-127">To configure the OSDSourceRoot value</span></span>**

-   <span data-ttu-id="9f3b9-128">Dans la valeur de clé de Registre suivante, configurez le OSDSourceRoot à l’aide d’un chemin UNC ou d’une URL:</span><span class="sxs-lookup"><span data-stu-id="9f3b9-128">Configure the OSDSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="9f3b9-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="9f3b9-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span></span>

    <span data-ttu-id="9f3b9-130">Les formats acceptables pour le OSDSourceRoot incluent des chemins d’accès UNC et des URL, comme dans l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="9f3b9-130">Acceptable formats for the OSDSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="9f3b9-131">**\\\\computername\\sharefolder\\resource** ou **\\\\computername\\content** ou \*\* &lt; Drive &gt; : \\FolderName\*\*</span><span class="sxs-lookup"><span data-stu-id="9f3b9-131">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="9f3b9-132">**http://computername/productivity/** ou**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="9f3b9-132">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

**<span data-ttu-id="9f3b9-133">Pour configurer la valeur IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="9f3b9-133">To configure the IconSourceRoot value</span></span>**

-   <span data-ttu-id="9f3b9-134">Dans la valeur de clé de Registre suivante, configurez le IconSourceRoot à l’aide d’un chemin UNC ou d’une URL:</span><span class="sxs-lookup"><span data-stu-id="9f3b9-134">Configure the IconSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="9f3b9-135">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="9f3b9-135">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span></span>

    <span data-ttu-id="9f3b9-136">Les formats acceptables pour le IconSourceRoot incluent des chemins d’accès UNC et des URL, comme dans l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="9f3b9-136">Acceptable formats for the IconSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="9f3b9-137">**\\\\computername\\sharefolder\\resource** ou **\\\\computername\\content** ou \*\* &lt; Drive &gt; : \\FolderName\*\*</span><span class="sxs-lookup"><span data-stu-id="9f3b9-137">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="9f3b9-138">**http://computername/productivity/** ou**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="9f3b9-138">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

## <span data-ttu-id="9f3b9-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9f3b9-139">Related topics</span></span>


[<span data-ttu-id="9f3b9-140">Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="9f3b9-140">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)










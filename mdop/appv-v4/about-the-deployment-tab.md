---
title: À propos de l'onglet Déploiement
description: À propos de l'onglet Déploiement
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808117"
---
# <span data-ttu-id="12c01-103">À propos de l'onglet Déploiement</span><span class="sxs-lookup"><span data-stu-id="12c01-103">About the Deployment Tab</span></span>


<span data-ttu-id="12c01-104">Pour modifier les informations relatives à une application que vous allez mettre en ordre, utilisez l’onglet **déploiement** de la console</span><span class="sxs-lookup"><span data-stu-id="12c01-104">Use the **Deployment** tab in the Application Virtualization Sequencer Console to change the information for an application you are about to sequence.</span></span> <span data-ttu-id="12c01-105">Cet onglet contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="12c01-105">This tab contains the following elements.</span></span>

## <span data-ttu-id="12c01-106">URL du serveur</span><span class="sxs-lookup"><span data-stu-id="12c01-106">Server URL</span></span>


<span data-ttu-id="12c01-107">Utilisez les contrôles d' **URL du serveur** pour spécifier les paramètres de configuration du serveur d’applications virtuel.</span><span class="sxs-lookup"><span data-stu-id="12c01-107">Use the **Server URL** controls to specify the virtual application server configuration settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12c01-108">Contrôle</span><span class="sxs-lookup"><span data-stu-id="12c01-108">Control</span></span></th>
<th align="left"><span data-ttu-id="12c01-109">Description</span><span class="sxs-lookup"><span data-stu-id="12c01-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12c01-110">Protocole</span><span class="sxs-lookup"><span data-stu-id="12c01-110">Protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12c01-111">Vous permet de sélectionner le protocole qui diffusera en continu le package d’application séquencé d’un serveur d’application virtuel vers un client de bureau de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="12c01-111">Enables you to select the protocol that will stream the sequenced application package from a virtual application server to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="12c01-112">Les protocoles suivants sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="12c01-112">The following protocols are available:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="12c01-113">RTSP </strong> : le protocole par défaut spécifie que le protocole de diffusion en continu en temps réel contrôle l’échange d’applications compatibles avec la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="12c01-113">RTSP</strong>—The default, it specifies that the Real-Time Streaming Protocol controls the exchange of virtualization-enabled applications.</span></span></p></li>
<li><p><strong><span data-ttu-id="12c01-114">RTSP </strong> : spécifie que le protocole de diffusion en continu en temps réel avec la sécurité au niveau de transport contrôle l’échange d’un package d’application séquencé.</span><span class="sxs-lookup"><span data-stu-id="12c01-114">RTSPS</strong>—Specifies that the Real-Time Streaming Protocol with Transport Layer Security controls the exchange of a sequenced application package.</span></span></p></li>
<li><p><strong><span data-ttu-id="12c01-115">Fichier </strong> — spécifie que l’application séquencée sera diffusée à partir d’un partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="12c01-115">File</strong>—Specifies that the sequenced application will be streamed from a file share.</span></span></p></li>
<li><p><strong><span data-ttu-id="12c01-116">HTTPs </strong> : indique que le protocole SSL (Secure Hypertext Transport Protocol) contrôle l’échange d’un package.</span><span class="sxs-lookup"><span data-stu-id="12c01-116">HTTPS</strong>—Specifies that Secure Hypertext Transport Protocol controls the exchange of a package.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="12c01-117">Nom</span><span class="sxs-lookup"><span data-stu-id="12c01-117">Hostname</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12c01-118">Vous permet de sélectionner le serveur d’applications virtuelles ou l’équilibrage de charge dans le premier plan d’un groupe de serveurs d’applications virtuelles qui diffusera le package logiciel sur un client de bureau de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="12c01-118">Enables you to select the virtual application server or the load balancer in front of a group of virtual application servers that will stream the software package to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="12c01-119">Vous devez renseigner cet élément pour créer un package d’application séquencé, mais vous pouvez passer de la variable d’environnement% SFT_SOFTGRIDSERVER% par défaut au nom d’hôte ou à l’adresse IP réelle d’un serveur d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="12c01-119">You must complete this item to create a sequenced application package, but you can change from the default %SFT_SOFTGRIDSERVER% environment variable to the actual hostname or IP address of a virtual application server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="12c01-120">Remarque</span><span class="sxs-lookup"><span data-stu-id="12c01-120">Note</span></span></strong><br/><p><span data-ttu-id="12c01-121">Si vous choisissez de ne pas spécifier de nom d’hôte ou d’adresse IP statique, vous devez configurer une variable d’environnement appelée SFT_SOFTGRIDSERVER dans chaque client de bureau.</span><span class="sxs-lookup"><span data-stu-id="12c01-121">If you choose not to specify a static hostname or IP address, on each Application Virtualization Desktop Client you must set up an environment variable called SFT_SOFTGRIDSERVER.</span></span> <span data-ttu-id="12c01-122">Sa valeur doit correspondre au nom d’hôte ou à l’adresse IP du serveur d’applications virtuel ou de l’équilibrage de charge qui est le client&#39;source d’applications.</span><span class="sxs-lookup"><span data-stu-id="12c01-122">Its value must be the hostname or IP address of the virtual application server or load balancer that is this client&#39;s source of applications.</span></span> <span data-ttu-id="12c01-123">Cette variable d’environnement doit être une variable système plutôt qu’une variable utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12c01-123">You should make this environment variable a system variable rather than a user variable.</span></span> <span data-ttu-id="12c01-124">Toute session de client de bureau de virtualisation d’application en cours d’exécution sur cet ordinateur lors de votre affectation de cette variable doit être fermée, puis ouverte pour que la session de reprise puisse être consciente de sa nouvelle source d’application.</span><span class="sxs-lookup"><span data-stu-id="12c01-124">Any Application Virtualization Desktop Client session that is running on this computer during your assignment of this variable must be closed and then opened so that the resumed session will be aware of its new application source.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12c01-125">Port</span><span class="sxs-lookup"><span data-stu-id="12c01-125">Port</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12c01-126">Vous permet de spécifier le port sur lequel le serveur d’applications virtuelles ou le point d’équilibrage de charge écoutera un client de bureau de la virtualisation des applications&#39;demande du package.</span><span class="sxs-lookup"><span data-stu-id="12c01-126">Enables you to specify the port on which the virtual application server or the load balancer will listen for an Application Virtualization Desktop Client&#39;s request for the package.</span></span> <span data-ttu-id="12c01-127">Ces informations sont nécessaires pour créer un package, mais vous pouvez le modifier.</span><span class="sxs-lookup"><span data-stu-id="12c01-127">This information is required to create a package, but you can change it.</span></span> <span data-ttu-id="12c01-128">Le port par défaut est 554.</span><span class="sxs-lookup"><span data-stu-id="12c01-128">The default port is 554.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="12c01-129">Chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="12c01-129">Path</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12c01-130">Vous permet de spécifier le chemin d’accès relatif du serveur d’application virtuel sur lequel est stocké le package logiciel et celui à partir duquel il sera diffusé.</span><span class="sxs-lookup"><span data-stu-id="12c01-130">Enables you to specify the relative path on the virtual application server where the software package is stored and from which it will be streamed.</span></span> <span data-ttu-id="12c01-131">Ces informations sont nécessaires pour créer un package si le fichier SFT est stocké dans un sous-répertoire de contenu. dans le cas contraire, ces informations ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="12c01-131">This information is required to create a package if the SFT file will be stored in a subdirectory of CONTENT; otherwise, this information is not required.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="12c01-132">Systèmes d’exploitation</span><span class="sxs-lookup"><span data-stu-id="12c01-132">Operating Systems</span></span>


<span data-ttu-id="12c01-133">Utilisez les contrôles des **systèmes d’exploitation** pour spécifier la configuration requise pour le système d’exploitation de l’application.</span><span class="sxs-lookup"><span data-stu-id="12c01-133">Use the **Operating Systems** controls to specify the application's operating system requirements.</span></span> <span data-ttu-id="12c01-134">Si un client de bureau de virtualisation des applications ne peut pas prendre en charge les systèmes d’exploitation sélectionnés, l’application ne démarre pas.</span><span class="sxs-lookup"><span data-stu-id="12c01-134">If an Application Virtualization Desktop Client cannot support any of the selected operating systems, the application will not start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12c01-135">Contrôles</span><span class="sxs-lookup"><span data-stu-id="12c01-135">Controls</span></span></th>
<th align="left"><span data-ttu-id="12c01-136">Description</span><span class="sxs-lookup"><span data-stu-id="12c01-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12c01-137">Systèmes d’exploitation disponibles</span><span class="sxs-lookup"><span data-stu-id="12c01-137">Available Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12c01-138">Affiche la liste des systèmes d’exploitation qui peuvent prendre en charge les applications du package.</span><span class="sxs-lookup"><span data-stu-id="12c01-138">Displays a list of operating systems that can support the applications in the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="12c01-139">Systèmes d’exploitation sélectionnés</span><span class="sxs-lookup"><span data-stu-id="12c01-139">Selected Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12c01-140">Affiche la liste des systèmes d’exploitation sélectionnés qui prennent en charge les applications du package.</span><span class="sxs-lookup"><span data-stu-id="12c01-140">Displays a list of selected operating systems that support the applications in the package.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="12c01-141">Options de sortie</span><span class="sxs-lookup"><span data-stu-id="12c01-141">Output Options</span></span>


<span data-ttu-id="12c01-142">Utilisez les contrôles **options de sortie** pour spécifier les options de sortie que l’application doit installer.</span><span class="sxs-lookup"><span data-stu-id="12c01-142">Use the **Output Options** controls to specify the output options for the application to be installed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="12c01-143">Contrôle</span><span class="sxs-lookup"><span data-stu-id="12c01-143">Control</span></span></th>
<th align="left"><span data-ttu-id="12c01-144">Description</span><span class="sxs-lookup"><span data-stu-id="12c01-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12c01-145">Algorithme de compression</span><span class="sxs-lookup"><span data-stu-id="12c01-145">Compression Algorithm</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12c01-146">Permet de sélectionner la méthode permettant de compresser le fichier SFT pour la diffusion en continu sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="12c01-146">Use to select the method for compressing the SFT file for streaming across a network.</span></span> <span data-ttu-id="12c01-147">Sélectionnez l’une des méthodes de compression suivantes:</span><span class="sxs-lookup"><span data-stu-id="12c01-147">Select one of the following compression methods:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="12c01-148">Compressé </strong> : indique que le fichier SFT est compressé au <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> format zlib </a> .</span><span class="sxs-lookup"><span data-stu-id="12c01-148">Compressed</strong>—Specifies that the SFT file be compressed in the <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)">ZLIB</a> format.</span></span></p></li>
<li><p><strong><span data-ttu-id="12c01-149">Non compressé </strong> : la valeur par défaut spécifie que le fichier SFT ne doit pas être compressé.</span><span class="sxs-lookup"><span data-stu-id="12c01-149">Not Compressed</strong>—The default; specifies that the SFT file not be compressed.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="12c01-150">Mettre en place des descripteurs de sécurité</span><span class="sxs-lookup"><span data-stu-id="12c01-150">Enforce Security Descriptors</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12c01-151">Sélectionnez cette option pour appliquer les descripteurs de sécurité des applications du package après leur déploiement sur le client.</span><span class="sxs-lookup"><span data-stu-id="12c01-151">Select to enforce security descriptors of the applications in the package after it is deployed to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="12c01-152">Générer un package Microsoft Windows Installer (MSI)</span><span class="sxs-lookup"><span data-stu-id="12c01-152">Generate Microsoft Windows Installer (MSI) Package</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="12c01-153">Pour installer ou déployer un package d’application séquencé à l’aide du programme d’installation Windows.</span><span class="sxs-lookup"><span data-stu-id="12c01-153">Select to install or deploy a sequenced application package with the Windows Installer.</span></span> <span data-ttu-id="12c01-154">Si vous avez apporté des modifications à l’aide du Sequencer, les modifications ne sont pas incluses dans le fichier du programme d’installation Windows.</span><span class="sxs-lookup"><span data-stu-id="12c01-154">If you have made any changes using the sequencer the changes will not be included with the Windows Installer file.</span></span> <span data-ttu-id="12c01-155">Le fichier du programme d’installation Windows sera toujours créé à l’aide du fichier. SFT enregistré sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="12c01-155">The Windows Installer file will always be created using the .sft file saved on the hard disk.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="12c01-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12c01-156">Related topics</span></span>


[<span data-ttu-id="12c01-157">Procédure pour modifier les propriétés de déploiement</span><span class="sxs-lookup"><span data-stu-id="12c01-157">How to Change Deployment Properties</span></span>](how-to-change-deployment-properties.md)

[<span data-ttu-id="12c01-158">Console Sequencer</span><span class="sxs-lookup"><span data-stu-id="12c01-158">Sequencer Console</span></span>](sequencer-console.md)










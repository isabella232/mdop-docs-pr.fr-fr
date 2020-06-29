---
title: Choisir une méthode de publication
description: Choisir une méthode de publication
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808898"
---
# <span data-ttu-id="f36cc-103">Choisir une méthode de publication</span><span class="sxs-lookup"><span data-stu-id="f36cc-103">Determine Your Publishing Method</span></span>


<span data-ttu-id="f36cc-104">Après avoir séquencé une application à l’aide du séquence de virtualisation d’application, vous devez la *publier* pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f36cc-104">After you sequence an application by using the Application Virtualization Sequencer, you need to *publish* that application to your users.</span></span> <span data-ttu-id="f36cc-105">La publication de l’application consiste à fournir les icônes, les informations de définition de package et l’emplacement de la source de contenu sur les ordinateurs sur lesquels le client de virtualisation d’application a été installé.</span><span class="sxs-lookup"><span data-stu-id="f36cc-105">Publishing the application consists of delivering the icons, package definition information, and content source location to each computer where the Application Virtualization Client has been installed.</span></span> <span data-ttu-id="f36cc-106">Le tableau suivant décrit les méthodes de publication prises en charge lorsque vous déployez la virtualisation d’application à l’aide d’un système de distribution de logiciels électroniques.</span><span class="sxs-lookup"><span data-stu-id="f36cc-106">The following table describes publishing methods that are supported when you deploy Application Virtualization by using an electronic software distribution (ESD) system.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f36cc-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="f36cc-107">Method</span></span></th>
<th align="left"><span data-ttu-id="f36cc-108">Avantages</span><span class="sxs-lookup"><span data-stu-id="f36cc-108">Advantages</span></span></th>
<th align="left"><span data-ttu-id="f36cc-109">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="f36cc-109">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f36cc-110">Générer un fichier du programme d’installation Windows durant le séquençage, sous la forme d’une solution autonome.</span><span class="sxs-lookup"><span data-stu-id="f36cc-110">Generate a Windows Installer file during sequencing, as a stand-alone solution.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f36cc-111">Facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f36cc-111">Very simple to use.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-112">Package chargé dans le cache localement sur chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f36cc-112">Package loaded into cache locally on each computer.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-113">Icônes affichées pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f36cc-113">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-114">Similaire au déploiement de logiciels traditionnels.</span><span class="sxs-lookup"><span data-stu-id="f36cc-114">Similar to traditional software deployment.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-115">Il n’est pas nécessaire de utiliser des serveurs de streaming.</span><span class="sxs-lookup"><span data-stu-id="f36cc-115">No need for streaming servers.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f36cc-116">Il n’y a aucune souplesse quant à l’emplacement du contenu des packages sur les ordinateurs, même emplacement sur tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="f36cc-116">No flexibility in location of package contents on computers—same location on all computers.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-117">Ne doit utiliser que l’ajout/suppression de programmes ou msiexec pour supprimer des applications.</span><span class="sxs-lookup"><span data-stu-id="f36cc-117">Must use only Add/Remove Programs or msiexec to remove applications.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-118">Enlèvement et remplacement avec la nouvelle version requise pour la mise à jour du package.</span><span class="sxs-lookup"><span data-stu-id="f36cc-118">Removal and replacement with new version required for package updating.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f36cc-119">Générez un fichier du programme d’installation Windows pendant le séquençage, utilisé avec des propriétés de ligne de commande du MODE, de chargement et de OVERRIDEURL et le manifeste du package.</span><span class="sxs-lookup"><span data-stu-id="f36cc-119">Generate a Windows Installer file during sequencing, used with MODE, LOAD, and OVERRIDEURL command-line properties and the package manifest.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f36cc-120">Facile à utiliser mais avec une souplesse accrue.</span><span class="sxs-lookup"><span data-stu-id="f36cc-120">Simple to use but with added flexibility.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-121">Icônes affichées pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f36cc-121">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-122">Le fichier SFT contenant les applications peut être placé sur un emplacement de la source en continu, dont les clients sont configurés pour utiliser cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="f36cc-122">SFT file containing the applications can be placed on a streaming source location, with clients configured to use that location.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f36cc-123">Flexibilité limitée: seul l’emplacement du contenu du package peut être contrôlé au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f36cc-123">Limited flexibility—only the location of the package content can be controlled at run time.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-124">Ne devez utiliser que l’application Ajout/suppression de programmes ou msiexec pour supprimer l’application.</span><span class="sxs-lookup"><span data-stu-id="f36cc-124">Must use only Add/Remove Programs or msiexec to remove the application.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-125">Enlèvement et remplacement avec la nouvelle version requise pour la mise à jour du package, sauf si vous utilisez un serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="f36cc-125">Removal and replacement with new version required for package updating, unless using streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f36cc-126">Exécutez des commandes SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="f36cc-126">Run SFTMIME commands.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f36cc-127">Flexibilité totale: contrôle total de toutes les fonctions de gestion des packages.</span><span class="sxs-lookup"><span data-stu-id="f36cc-127">Complete flexibility—full control of all package management functions.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f36cc-128">Les commandes doivent être utilisées pour une utilisation avec le système ESD.</span><span class="sxs-lookup"><span data-stu-id="f36cc-128">Commands must be scripted for use with the ESD system.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-129">Les commandes doivent être exécutées sur chaque ordinateur avec une séquence correcte.</span><span class="sxs-lookup"><span data-stu-id="f36cc-129">Commands must be run on each computer in correct sequence.</span></span></p></li>
<li><p><span data-ttu-id="f36cc-130">Compréhension détaillée du langage de commande et de la planification soigneuse requise.</span><span class="sxs-lookup"><span data-stu-id="f36cc-130">Detailed understanding of command language and careful planning required.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f36cc-131">Pour plus d’informations sur l’utilisation de ces méthodes de publication, voir [Comment publier une application virtuelle sur le client](how-to-publish-a-virtual-application-on-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="f36cc-131">For more information about using these publishing methods, see [How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md).</span></span>

## <span data-ttu-id="f36cc-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f36cc-132">Related topics</span></span>


[<span data-ttu-id="f36cc-133">Choisir une méthode de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="f36cc-133">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="f36cc-134">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="f36cc-134">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="f36cc-135">Présentation du scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="f36cc-135">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="f36cc-136">Procédure pour publier une application virtuelle sur le client</span><span class="sxs-lookup"><span data-stu-id="f36cc-136">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="f36cc-137">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f36cc-137">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 






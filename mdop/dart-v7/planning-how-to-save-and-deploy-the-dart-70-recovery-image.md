---
title: Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT7.0
description: Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT7.0
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809570"
---
# <span data-ttu-id="5550f-103">Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="5550f-103">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="5550f-104">Utilisez les informations de cette section lorsque vous planifiez l’enregistrement et le déploiement de l’image de récupération du jeu d’outils de diagnostics et de récupération Microsoft (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="5550f-104">Use the information in this section when you plan for saving and deploying the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="5550f-105">Planification de l’enregistrement et du déploiement de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="5550f-105">Planning How to Save and Deploy the DaRT Recovery Image</span></span>


<span data-ttu-id="5550f-106">Vous pouvez enregistrer et déployer l’image de récupération DaRT en utilisant les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="5550f-106">You can save and deploy the DaRT recovery image by using the following methods.</span></span> <span data-ttu-id="5550f-107">Lorsque vous déterminez la méthode à utiliser, examinez les avantages et inconvénients de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="5550f-107">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="5550f-108">Par ailleurs, réfléchissez à la façon dont vous souhaitez utiliser DaRT au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="5550f-108">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="5550f-109">**Remarques**  Vous souhaiterez peut-être utiliser plusieurs méthodes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5550f-109">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="5550f-110">Par exemple, vous pouvez démarrer dans DaRT à partir d’une partition distante dans la plupart des cas, et disposer d’un lecteur flash USB dans le cas où l’ordinateur de l’utilisateur final ne peut pas se connecter au réseau.</span><span class="sxs-lookup"><span data-stu-id="5550f-110">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="5550f-111">Le tableau suivant présente quelques avantages et inconvénients de chaque méthode d’utilisation de DaRT au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5550f-111">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5550f-112">Méthode de démarrage dans DaRT</span><span class="sxs-lookup"><span data-stu-id="5550f-112">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="5550f-113">Avantages</span><span class="sxs-lookup"><span data-stu-id="5550f-113">Advantages</span></span></th>
<th align="left"><span data-ttu-id="5550f-114">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="5550f-114">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5550f-115">À partir d’un CD ou d’un DVD</span><span class="sxs-lookup"><span data-stu-id="5550f-115">From a CD or DVD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5550f-116">Prend en charge les scénarios dans lesquels l’enregistrement de démarrage principal (MBR) est endommagé et que vous ne pouvez pas accéder au disque dur.</span><span class="sxs-lookup"><span data-stu-id="5550f-116">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk.</span></span> <span data-ttu-id="5550f-117">Prend également en charge les cas où il n’y a pas de connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="5550f-117">Also supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="5550f-118">Les utilisateurs des versions antérieures de DaRT sont les plus familiers et un CD ou un DVD peut être gravé directement depuis l' <strong> Assistant image de récupération DART </strong> .</span><span class="sxs-lookup"><span data-stu-id="5550f-118">This is most familiar to users of earlier versions of DaRT, and a CD or DVD can be burned directly from the <strong>DaRT Recovery Image Wizard</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5550f-119">Nécessite que quelqu’un ayant accès au CD ou DVD soit physiquement sur l’ordinateur de l’utilisateur final pour démarrer sur DaRT.</span><span class="sxs-lookup"><span data-stu-id="5550f-119">Requires that someone with access to the CD or DVD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5550f-120">À partir d’un lecteur flash USB (UFD)</span><span class="sxs-lookup"><span data-stu-id="5550f-120">From a USB flash drive (UFD)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5550f-121">Offre les mêmes avantages que le démarrage à partir d’un CD ou d’un DVD, et fournit également une assistance technique pour les ordinateurs qui n’ont pas de lecteur de CD ou de DVD.</span><span class="sxs-lookup"><span data-stu-id="5550f-121">Provides same advantages as booting from a CD or DVD and also provides support to computers that have no CD or DVD drive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5550f-122">Vous devez mettre en forme l’UFD avant de pouvoir l’utiliser pour démarrer sur DaRT.</span><span class="sxs-lookup"><span data-stu-id="5550f-122">Requires you to format the UFD before you can use it to boot into DaRT.</span></span> <span data-ttu-id="5550f-123">Il est également nécessaire que quelqu’un ayant accès au lecteur UFD soit physiquement connecté à l’ordinateur de l’utilisateur final pour démarrer dans DaRT.</span><span class="sxs-lookup"><span data-stu-id="5550f-123">Also requires that someone with access to the UFD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5550f-124">À partir d’une partition distante (réseau)</span><span class="sxs-lookup"><span data-stu-id="5550f-124">From a remote (network) partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="5550f-125">Vous permet d’effectuer un démarrage dans DaRT sans avoir besoin d’un CD, d’un DVD ou d’un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="5550f-125">Lets you boot into DaRT without needing a CD, DVD, or UFD.</span></span> <span data-ttu-id="5550f-126">Il est également possible de mettre à jour des fichiers DaRT en toute simplicité, car il n’y a qu’un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="5550f-126">Also allows for easy upgrades of DaRT because there is only one file location to update.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5550f-127">Ne fonctionne pas si l’ordinateur de l’utilisateur final n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="5550f-127">Does not work if the end-user computer is not connected to the network.</span></span></p>
<p><span data-ttu-id="5550f-128">Disponible à grande échelle pour les utilisateurs finaux et peut nécessiter des considérations en matière de sécurité lors de la création de l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="5550f-128">Widely available to end users and might require additional security considerations when you are creating the recovery image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5550f-129">À partir d’une partition de récupération</span><span class="sxs-lookup"><span data-stu-id="5550f-129">From a recovery partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="5550f-130">Vous permet d’effectuer un démarrage dans DaRT sans avoir besoin d’un CD, d’un DVD ou d’un UFD incluant des instances dans lesquelles il n’y a pas de connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="5550f-130">Lets you boot into DaRT without needing a CD, DVD, or UFD that includes instances in which there is no network connectivity.</span></span></p>
<p><span data-ttu-id="5550f-131">Par ailleurs, il est possible d’implémenter et de gérer le processus d’image Windows standard à l’aide d’outils de distribution automatisés, tels que Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5550f-131">Also, can be implemented and managed as part of your standard Windows image process by using automated distribution tools, such as Microsoft Endpoint Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5550f-132">Lors de la mise à jour de DaRT, vous devez mettre à jour tous les ordinateurs de votre entreprise au lieu d’une seule partition (sur le réseau) ou de l’appareil (CD, DVD ou UFD).</span><span class="sxs-lookup"><span data-stu-id="5550f-132">When updating DaRT, requires you to update all computers in your enterprise instead of just one partition (on the network) or device (CD, DVD, or UFD).</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5550f-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5550f-133">Related topics</span></span>


[<span data-ttu-id="5550f-134">Planification du déploiement de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="5550f-134">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 






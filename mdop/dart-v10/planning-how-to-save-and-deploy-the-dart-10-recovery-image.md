---
title: Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT10
description: Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT10
author: dansimp
ms.assetid: 9a3e5413-2621-49ce-8bd2-992616691703
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbaa8c4160970de90561f5ff8cedcefd08ca1dd7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809684"
---
# <span data-ttu-id="4c2c9-103">Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT10</span><span class="sxs-lookup"><span data-stu-id="4c2c9-103">Planning How to Save and Deploy the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="4c2c9-104">Vous pouvez enregistrer et déployer l’image de récupération Microsoft Diagnostics et Recovery Tools (DaRT) 10 en utilisant les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-104">You can save and deploy the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image by using the following methods.</span></span> <span data-ttu-id="4c2c9-105">Lorsque vous déterminez la méthode à utiliser, examinez les avantages et inconvénients de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-105">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="4c2c9-106">Prenez également en considération votre infrastructure et votre équipe de support technique.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-106">You should also consider your infrastructure and support staff.</span></span> <span data-ttu-id="4c2c9-107">Si vous disposez d’une petite infrastructure, vous souhaiterez peut-être déployer DaRT 10 à l’aide d’un support amovible, car l’image de récupération sera toujours disponible si vous l’installez sur le disque dur local.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-107">If you have a small infrastructure, you might want to deploy DaRT 10 by using removable media, since the recovery image will always be available if you install it to the local hard drive.</span></span>

<span data-ttu-id="4c2c9-108">Si votre organisation utilise les services de domaine Active Directory (AD DS), il est possible que vous souhaitiez déployer des images de récupération en tant que service réseau en utilisant Windows DS.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-108">If your organization uses Active Directory Domain Services (AD DS), you may want to deploy recovery images as a network service by using Windows DS.</span></span> <span data-ttu-id="4c2c9-109">Les images de récupération sont toujours disponibles pour les ordinateurs connectés.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-109">Recovery images are always available to any connected computer.</span></span> <span data-ttu-id="4c2c9-110">Vous pouvez déployer plusieurs images à partir de Windows DS et les conserver toutes au même endroit.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-110">You can deploy multiple images from Windows DS and maintain them all in one place.</span></span>

<span data-ttu-id="4c2c9-111">**Remarques**  Il est possible que vous souhaitiez utiliser plusieurs méthodes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-111">**Note** You may want to use more than one method in your organization.</span></span> <span data-ttu-id="4c2c9-112">Par exemple, vous pouvez démarrer dans DaRT à partir d’une partition distante dans la plupart des cas, et disposer d’un lecteur flash USB dans le cas où l’ordinateur de l’utilisateur final ne peut pas se connecter au réseau.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-112">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="4c2c9-113">Le tableau suivant présente quelques avantages et inconvénients de chaque méthode d’utilisation de DaRT au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-113">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c2c9-114">Méthode de démarrage dans DaRT</span><span class="sxs-lookup"><span data-stu-id="4c2c9-114">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="4c2c9-115">Avantages</span><span class="sxs-lookup"><span data-stu-id="4c2c9-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="4c2c9-116">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="4c2c9-116">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c2c9-117">Support amovible</span><span class="sxs-lookup"><span data-stu-id="4c2c9-117">Removable Media</span></span></strong></p>
<p><span data-ttu-id="4c2c9-118">L’image de récupération est écrite sur un CD, un DVD ou un lecteur USB pour permettre au personnel de support d’adopter les outils de récupération pour l’ordinateur instable.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-118">The recovery image is written to a CD, DVD, or USB drive to enable support staff to take the recovery tools with them to the unstable computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c2c9-119">Prend en charge les scénarios dans lesquels l’enregistrement de démarrage principal (MBR) est endommagé et que vous ne pouvez pas accéder au disque dur et ne prend pas en charge les cas où il n’y a aucune connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-119">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk and supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="4c2c9-120">Vous permet de créer plusieurs images de récupération avec différents outils pour fournir différents niveaux de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-120">Enables you to create multiple recovery images with different tools to provide different levels of support.</span></span></p>
<p><span data-ttu-id="4c2c9-121">Fournit un outil intégré pour la gravure d’images de récupération sur un support amovible.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-121">Provides a built-in tool for burning recovery images to removable media.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c2c9-122">Nécessite que le personnel du support technique se trouve physiquement sur l’ordinateur de l’utilisateur final pour démarrer sur DaRT.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-122">Requires that support staff are physically at the end-user computer to boot into DaRT.</span></span></p>
<p><span data-ttu-id="4c2c9-123">Il est nécessaire de disposer du temps et de la maintenance pour créer plusieurs éléments multimédias avec des configurations différentes pour les ordinateurs 32 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-123">Requires time and maintenance to create multiple media with different configurations for 32-bit and 64-bit computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c2c9-124">À partir d’une partition distante (réseau)</span><span class="sxs-lookup"><span data-stu-id="4c2c9-124">From a remote (network) partition</span></span></strong></p>
<p><span data-ttu-id="4c2c9-125">L’image de récupération est hébergée sur un serveur de démarrage réseau tel que les services de déploiement Windows, qui permet aux utilisateurs ou au personnel de support de les diffuser sur des ordinateurs à la demande.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-125">The recovery image is hosted on a network boot server like Windows Deployment Services (Windows DS), which allows users or support staff to stream it to computers on demand.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c2c9-126">Disponible pour tous les ordinateurs ayant accès au serveur d’amorçage réseau.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-126">Available to all computers that have access to the network boot server.</span></span></p>
<p><span data-ttu-id="4c2c9-127">Les images de récupération sont hébergées sur un serveur central, qui permet des mises à jour centralisées.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-127">Recovery images are hosted on a central server, which enables centralized updates.</span></span></p>
<p><span data-ttu-id="4c2c9-128">Le personnel de support centralisé peut fournir des réparations via une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-128">Centralized help desk staff can provide repairs by using remote connectivity.</span></span></p>
<p><span data-ttu-id="4c2c9-129">Aucun espace de stockage local requis pour les clients.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-129">No local storage requirement on the clients.</span></span></p>
<p><span data-ttu-id="4c2c9-130">Possibilité de créer plusieurs images de récupération avec différents outils pour des niveaux de support spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-130">Ability to create multiple recovery images with different tools for specific support levels.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c2c9-131">Le besoin de sécuriser l’infrastructure Windows DS pour s’assurer que les utilisateurs normaux peuvent démarrer uniquement l’image de récupération DaRT et non le processus complet d’imagerie du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-131">The need to secure Windows DS infrastructure to ensure that regular users can start only the DaRT recovery image and not the full operating system imaging process.</span></span></p>
<p></p>
<p></p>
<p><span data-ttu-id="4c2c9-132">Nécessite que l’ordinateur de l’utilisateur final est connecté au réseau lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-132">Requires that the end-user computer is connected to the network at runtime.</span></span></p>
<p><span data-ttu-id="4c2c9-133">Nécessite que l’image de récupération soit placée sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-133">Requires that the recovery image is brought across the network.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c2c9-134">À partir d’une partition de récupération sur le disque dur local</span><span class="sxs-lookup"><span data-stu-id="4c2c9-134">From a recovery partition on the local hard drive</span></span></strong></p>
<p><span data-ttu-id="4c2c9-135">L’image de récupération est installée sur un disque dur local manuellement ou à l’aide de systèmes de distribution de logiciels électroniques tels que System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-135">The recovery image is installed on a local hard drive either manually or by using electronic software distribution systems like System Center Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c2c9-136">L’image de récupération est toujours disponible, car elle est prédéfinie sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-136">The recovery image is always available because it is pre-staged on the computer.</span></span></p>
<p><span data-ttu-id="4c2c9-137">Le personnel de support centralisé peut fournir une assistance via une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-137">Centralized help desk staff can provide support by using Remote Connection.</span></span></p>
<p><span data-ttu-id="4c2c9-138">L’image de récupération est gérée de manière centralisée et déployée.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-138">The recovery image is centrally managed and deployed.</span></span></p>
<p><span data-ttu-id="4c2c9-139">Des demandes de clé de récupération supplémentaires sur des ordinateurs qui sont protégés par le chiffrement de lecteur BitLocker Windows sont éliminées.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-139">Additional recovery key requests on computers that are protected by Windows BitLocker drive encryption are eliminated.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c2c9-140">Le stockage local est requis.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-140">Local storage is required.</span></span></p>
<p><span data-ttu-id="4c2c9-141">Il est recommandé de limiter les risques liés à une partition de démarrage qui est dédiée et non chiffrée.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-141">A dedicated, unencrypted partition for recovery image placement is recommended to reduce the risk of a failed boot partition.</span></span></p>
<p><span data-ttu-id="4c2c9-142">Lors de la mise à jour de DaRT, vous devez mettre à jour tous les ordinateurs de votre entreprise au lieu d’une seule partition (sur le réseau) ou d’un appareil amovible.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-142">When updating DaRT, you must update all computers in your enterprise instead of just one partition (on the network) or removable device.</span></span></p>
<p><span data-ttu-id="4c2c9-143">Des considérations supplémentaires sont nécessaires si vous déployez l’image de récupération après activation de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4c2c9-143">Additional consideration is required if you deploy the recovery image after BitLocker has been enabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4c2c9-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c2c9-144">Related topics</span></span>


[<span data-ttu-id="4c2c9-145">Planification du déploiement de DaRT10</span><span class="sxs-lookup"><span data-stu-id="4c2c9-145">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 






---
title: Déploiement de packages App-V5.0 à l'aide d'une solution de distribution électronique de logiciels
description: Déploiement de packages App-V5.0 à l'aide d'une solution de distribution électronique de logiciels
author: dansimp
ms.assetid: 08e5e05b-dbb8-4be7-b2d8-721ef627da81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 33af02c5e9fad7408f9719ecd1a7fa90eacfeb29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805539"
---
# <span data-ttu-id="8300a-103">Déploiement de packages App-V5.0 à l'aide d'une solution de distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="8300a-103">How to deploy App-V 5.0 Packages Using Electronic Software Distribution</span></span>


<span data-ttu-id="8300a-104">Vous pouvez utiliser un système de distribution de logiciels électronique (ESD) pour déployer des applications virtuelles App-V 5,0 pour les clients App-V.</span><span class="sxs-lookup"><span data-stu-id="8300a-104">You can use an electronic software distribution (ESD) system to deploy App-V 5.0 virtual applications to App-V clients.</span></span> <span data-ttu-id="8300a-105">Pour plus d’informations, consultez la documentation disponible avec la fonction ESD que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="8300a-105">For details, see the documentation available with the ESD you are using.</span></span>

<span data-ttu-id="8300a-106">Pour connaître la configuration requise et les options d’utilisation d’une application ESD pour déployer des packages App-V, voir [planification du déploiement de App-v 5,0 avec un système de distribution de logiciels électronique](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="8300a-106">For component requirements and options for using an ESD to deploy App-V packages, see [Planning to Deploy App-V 5.0 with an Electronic Software Distribution System](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md).</span></span>

<span data-ttu-id="8300a-107">Appliquez l’une des méthodes suivantes pour publier des packages sur les ordinateurs clients App-V avec une application ESD:</span><span class="sxs-lookup"><span data-stu-id="8300a-107">Use one of the following methods to publish packages to App-V client computers with an ESD:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8300a-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="8300a-108">Method</span></span></th>
<th align="left"><span data-ttu-id="8300a-109">Description</span><span class="sxs-lookup"><span data-stu-id="8300a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8300a-110">Fonctionnalités fournies par un tiers ESD</span><span class="sxs-lookup"><span data-stu-id="8300a-110">Functionality provided by a third-party ESD</span></span></p></td>
<td align="left"><p><span data-ttu-id="8300a-111">Utilisez les fonctionnalités d’un fournisseur de ESD tiers.</span><span class="sxs-lookup"><span data-stu-id="8300a-111">Use the functionality in a third-party ESD.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8300a-112">Programme d’installation Windows autonome</span><span class="sxs-lookup"><span data-stu-id="8300a-112">Stand-alone Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="8300a-113">Installez l’application sur l’ordinateur client cible à l’aide du fichier Windows Installer (. msi) associé qui est créé lors de la séquence initiale d’une application.</span><span class="sxs-lookup"><span data-stu-id="8300a-113">Install the application on the target client computer by using the associated Windows Installer (.msi) file that is created when you initially sequence an application.</span></span> <span data-ttu-id="8300a-114">Le fichier d’installation Windows contient les informations du fichier de package App-V 5,0 utilisées pour configurer un package et copie les fichiers de package requis sur le client.</span><span class="sxs-lookup"><span data-stu-id="8300a-114">The Windows Installer file contains the associated App-V 5.0 package file information used to configure a package and copies the required package files to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8300a-115">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8300a-115">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="8300a-116">Utilisez les cmdlets PowerShell pour déployer des applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="8300a-116">Use PowerShell cmdlets to deploy virtualized applications.</span></span> <span data-ttu-id="8300a-117">Pour plus d’informations sur l’utilisation des applications PowerShell et App-V 5,0, voir <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)"> administration de l’application-v à l’aide de PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="8300a-117">For more information about using PowerShell and App-V 5.0, see <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)">Administering App-V by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="8300a-118">Pour déployer des packages App-V 5,0 en utilisant une ESD</span><span class="sxs-lookup"><span data-stu-id="8300a-118">To deploy App-V 5.0 packages by using an ESD</span></span>**

1.  <span data-ttu-id="8300a-119">Installez le Sequencer App-V 5,0 sur un ordinateur de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8300a-119">Install the App-V 5.0 Sequencer on a computer in your environment.</span></span> <span data-ttu-id="8300a-120">Pour plus d’informations sur l’installation de Sequencer, voir [Comment installer le Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="8300a-120">For more information about installing the sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="8300a-121">Utilisez le Sequencer App-V 5,0 pour créer une application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="8300a-121">Use the App-V 5.0 Sequencer to create virtual application.</span></span> <span data-ttu-id="8300a-122">Pour plus d’informations sur la création d’une application virtuelle, voir [création et gestion des applications virtuelles App-V 5,0](creating-and-managing-app-v-50-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8300a-122">For information about creating a virtual application, see [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

3.  <span data-ttu-id="8300a-123">Une fois que vous avez créé l’application virtuelle, déployez le package à l’aide de votre solution ESD.</span><span class="sxs-lookup"><span data-stu-id="8300a-123">After you create the virtual application, deploy the package by using your ESD solution.</span></span>

    <span data-ttu-id="8300a-124">Pour plus d’informations sur l’utilisation de System Center Configuration Manager, voir présentation de la [gestion des applications dans Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) pour plus d’informations sur l’utilisation d’App-V 5,0 et de System Center2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8300a-124">If you are using System Center Configuration Manager, start by reviewing [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) for information about using App-V 5.0 and System Center2012 Configuration Manager.</span></span>

    <span data-ttu-id="8300a-125">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="8300a-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="8300a-126">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="8300a-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="8300a-127">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="8300a-127">Got an App-V issue?</span></span>** <span data-ttu-id="8300a-128">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="8300a-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="8300a-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8300a-129">Related topics</span></span>


[<span data-ttu-id="8300a-130">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="8300a-130">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 






---
title: Notes de publication pour MED-V1.0 SP1 et SP2
description: Notes de publication pour MED-V1.0 SP1 et SP2
author: dansimp
ms.assetid: 0fde8732-8ad2-483c-b094-7996ed9f2766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e90b85068faa277cd03e31963c4cad5b5a37f7a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811850"
---
# <span data-ttu-id="34f96-103">Notes de publication pour MED-V1.0 SP1 et SP2</span><span class="sxs-lookup"><span data-stu-id="34f96-103">MED-V 1.0 SP1 and SP2 Release Notes</span></span>


<span data-ttu-id="34f96-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="34f96-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="34f96-105">**Remarques**  Lisez attentivement ces notes de publication avant d’installer la plate-forme Microsoft Enterprise Desktop Virtualization (MED-V).</span><span class="sxs-lookup"><span data-stu-id="34f96-105">**Note** Read these Release Notes thoroughly before you install the Microsoft Enterprise Desktop Virtualization (MED-V) platform.</span></span> <span data-ttu-id="34f96-106">Ces notes de publication contiennent des informations dont vous avez besoin pour installer correctement la plateforme MED-V.</span><span class="sxs-lookup"><span data-stu-id="34f96-106">These Release Notes contain information that you must have to successfully install the MED-V platform.</span></span> <span data-ttu-id="34f96-107">Ce document contient des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="34f96-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="34f96-108">S’il existe une différence entre ces notes de publication et d’autres documents de la plateforme MED-V, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="34f96-108">If there is a discrepancy between these Release Notes and other MED-V platform documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="34f96-109">Ces notes de publication remplacent le contenu fourni avec ce produit.</span><span class="sxs-lookup"><span data-stu-id="34f96-109">These Release Notes supersede the content included with this product.</span></span>

 

## <span data-ttu-id="34f96-110">À propos de la documentation relative aux produits</span><span class="sxs-lookup"><span data-stu-id="34f96-110">About the Product Documentation</span></span>


<span data-ttu-id="34f96-111">La documentation complète de la plateforme Microsoft Enterprise Desktop Virtualization (MED-V) est disponible.</span><span class="sxs-lookup"><span data-stu-id="34f96-111">Comprehensive documentation for Microsoft Enterprise Desktop Virtualization (MED-V) platform is available.</span></span> <span data-ttu-id="34f96-112">Reportez-vous au Guide de planification, de déploiement et d’opérations de Microsoft Enterprise Desktop Virtualization.</span><span class="sxs-lookup"><span data-stu-id="34f96-112">Refer to the Microsoft Enterprise Desktop Virtualization Planning, Deployment, and Operations Guide.</span></span>

## <span data-ttu-id="34f96-113">Se protéger contre les failles de sécurité et les virus</span><span class="sxs-lookup"><span data-stu-id="34f96-113">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="34f96-114">Pour vous aider à vous protéger contre les failles de sécurité et les virus, installez les mises à jour de sécurité disponibles pour les nouveaux logiciels que vous installez.</span><span class="sxs-lookup"><span data-stu-id="34f96-114">To help protect against security vulnerabilities and viruses, you should install the latest available security updates for any new software that you are installing.</span></span> <span data-ttu-id="34f96-115">Pour plus d’informations, consultez le site Web de sécurité Microsoft à l’adresse <https://go.microsoft.com/fwlink/?LinkId=3482> .</span><span class="sxs-lookup"><span data-stu-id="34f96-115">For more information, see the Microsoft Security website at <https://go.microsoft.com/fwlink/?LinkId=3482>.</span></span>

## <a href="" id="what-s-new-in-med-v-1-0-sp2"></a><span data-ttu-id="34f96-116">Nouveautés de la version 1,0 du SP2 MED-V</span><span class="sxs-lookup"><span data-stu-id="34f96-116">What’s New in MED-V 1.0 SP2</span></span>


<span data-ttu-id="34f96-117">MED-V 1.0 SP2 inclut les mises à jour suivantes des fonctionnalités et fonctionnalités de MED-V 1.0 SP1:</span><span class="sxs-lookup"><span data-stu-id="34f96-117">MED-V1.0SP2 includes the following updates to the MED-V1.0SP1 features and functionality:</span></span>

-   <span data-ttu-id="34f96-118">Prise en charge de l’utilisation de MED-V sur une station de travail simplifiée chinois classique ou chinois.</span><span class="sxs-lookup"><span data-stu-id="34f96-118">Support for running MED-V on a Chinese traditional or Chinese simplified workstation.</span></span>

-   <span data-ttu-id="34f96-119">La prise en charge du client MED-V 1.0 SP2 s’exécute sur Windows 7 SP1.</span><span class="sxs-lookup"><span data-stu-id="34f96-119">Support for the MED-V1.0SP2 client to run on Windows 7 SP1.</span></span>

-   <span data-ttu-id="34f96-120">Performances améliorées pour les applications qui s’exécutent dans l’espace de travail MED-V lorsque les trames MED-V qui entourent les applications publiées sont activées.</span><span class="sxs-lookup"><span data-stu-id="34f96-120">Improved performance for the applications that are running in the MED-V workspace when MED-V frames around the published applications are turned-on.</span></span> <span data-ttu-id="34f96-121">Auparavant, dans certains cas, les images MED-V devaient être désactivées pour que les applications s’exécutent correctement.</span><span class="sxs-lookup"><span data-stu-id="34f96-121">Previously, under some instances the MED-V frames had to be turned-off for the applications to run correctly.</span></span>

## <span data-ttu-id="34f96-122">Problèmes connus avec MED-V 1.0 SP1 et MED-V 1,0 SP2</span><span class="sxs-lookup"><span data-stu-id="34f96-122">Known Issues with MED-V1.0 SP1 and MED-V 1.0 SP2</span></span>


<span data-ttu-id="34f96-123">Cette section fournit des informations mises à jour sur les problèmes liés à la plateforme Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="34f96-123">This section provides the most up-to-date information about issues with the Microsoft Enterprise Desktop Virtualization (MED-V)1.0 SP1 platform.</span></span> <span data-ttu-id="34f96-124">Ces problèmes n’apparaissent pas dans la documentation du produit et dans certains cas, il est possible que la documentation sur le produit soit contradictoire.</span><span class="sxs-lookup"><span data-stu-id="34f96-124">These issues do not appear in the product documentation and in some cases may contradict existing product documentation.</span></span> <span data-ttu-id="34f96-125">Dans la mesure du possible, ces problèmes sont résolus dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="34f96-125">Whenever possible, these issues are addressed in later releases.</span></span>

### <span data-ttu-id="34f96-126">MED-V ne fournit pas de prise en charge avancée de l’utilisation de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="34f96-126">MED-V does not provide Windows7 advanced user experience support</span></span>

<span data-ttu-id="34f96-127">MED-V 1.0 SP1 ne fournit pas de prise en charge avancée de l’utilisation de l’utilisateur, comme suit:</span><span class="sxs-lookup"><span data-stu-id="34f96-127">MED-V1.0 SP1 does not provide Windows7 advanced user experience support, such as the following:</span></span>

<span data-ttu-id="34f96-128">L’ancrage des fenêtres en haut, à gauche ou à droite n’est pas appliqué aux fenêtres d’application publiées.</span><span class="sxs-lookup"><span data-stu-id="34f96-128">Docking windows to the top, left, or right is not applied to published application windows.</span></span>

<span data-ttu-id="34f96-129">La version d’évaluation de la barre des tâches de la barre des tâches n’affiche pas le contenu d’application publié.</span><span class="sxs-lookup"><span data-stu-id="34f96-129">The Windows7 taskbar preview does not display the published application content.</span></span>

## <span data-ttu-id="34f96-130">Informations de copyright des notes de publication</span><span class="sxs-lookup"><span data-stu-id="34f96-130">Release Notes Copyright Information</span></span>


<span data-ttu-id="34f96-131">Les informations contenues dans ce document, y compris les URL et les autres références de site Web Internet, peuvent faire l’objet de modifications sans préavis et sont fournies à titre informatif uniquement.</span><span class="sxs-lookup"><span data-stu-id="34f96-131">Information in this document, including URL and other Internet website references, is subject to change without notice, and is provided for informational purposes only.</span></span> <span data-ttu-id="34f96-132">L’ensemble des risques liés à l’utilisation ou aux résultats de l’utilisation de ce document par le biais de l’utilisateur et Microsoft Corporation ne garantit aucune garantie, expresse ou implicite.</span><span class="sxs-lookup"><span data-stu-id="34f96-132">The entire risk of the use or results of the use of this document remains with the user, and Microsoft Corporation makes no warranties, either express or implied.</span></span> <span data-ttu-id="34f96-133">Les exemples de sociétés, d’organisations, de produits, de personnes et d’événements décrits dans les présentes sont fictifs.</span><span class="sxs-lookup"><span data-stu-id="34f96-133">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="34f96-134">Il n’est pas possible d’associer une entreprise, une organisation, un produit, une personne ou un événement réel.</span><span class="sxs-lookup"><span data-stu-id="34f96-134">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span> <span data-ttu-id="34f96-135">Conformément à toutes les lois applicables en matière de copyright, il incombe à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="34f96-135">Complying with all applicable copyright laws is the responsibility of the user.</span></span> <span data-ttu-id="34f96-136">Sans limiter les droits découlant du droit d’auteur, aucune partie de ce document ne pourra être reproduite, stockée ou introduite dans un système de récupération, ni transmise à l’aide d’un moyen quelconque (électronique, mécanique, photocopie, enregistrement ou autre), ou à d’autres fins, sans l’autorisation écrite rapide de Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="34f96-136">Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.</span></span>

<span data-ttu-id="34f96-137">Microsoft peut être doté d’un brevet, d’une demande de brevet, de marques commerciales, de droits d’auteur ou d’autres droits de propriété intellectuelle concernant le sujet figurant dans ce document.</span><span class="sxs-lookup"><span data-stu-id="34f96-137">Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document.</span></span> <span data-ttu-id="34f96-138">À l’exception de ce que prévoit expressément un contrat de licence écrit de la part de Microsoft, la fourniture de ce document ne vous donne aucune licence pour ces brevets, marques commerciales, droits d’auteur ou toute autre propriété intellectuelle.</span><span class="sxs-lookup"><span data-stu-id="34f96-138">Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.</span></span>



<span data-ttu-id="34f96-139">Microsoft, Microsoft Enterprise Desktop Virtualization, MS-DOS, Windows, windowsserver2003, Windows Vista, Active Directory et ActiveSync sont des marques commerciales déposées ou des marques commerciales de MicrosoftCorporation aux États-Unis et/ou dans d’autres pays.</span><span class="sxs-lookup"><span data-stu-id="34f96-139">Microsoft, Microsoft Enterprise Desktop Virtualization, MS-DOS, Windows, WindowsServer, Windows Vista, Active Directory, and ActiveSync are either registered trademarks or trademarks of MicrosoftCorporation in the U.S.A. and/or other countries.</span></span>

<span data-ttu-id="34f96-140">Les noms des sociétés et produits réels mentionnés dans le présent document pourront être des marques de leurs propriétaires respectifs.</span><span class="sxs-lookup"><span data-stu-id="34f96-140">The names of actual companies and products mentioned herein may be the trademarks of their respective owners.</span></span>

 

 






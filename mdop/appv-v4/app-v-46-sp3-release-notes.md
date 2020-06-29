---
title: Notes de publication d'App-V4.6 SP3
description: Notes de publication d'App-V4.6 SP3
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808049"
---
# <span data-ttu-id="c3e19-103">Notes de publication d'App-V4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="c3e19-103">App-V 4.6 SP3 Release Notes</span></span>


<span data-ttu-id="c3e19-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="c3e19-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="c3e19-105">Lisez attentivement ces notes de publication avant d’installer le système de gestion Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="c3e19-105">Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="c3e19-106">Ces notes de publication contiennent des informations qui vous permettent d’installer correctement Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="c3e19-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP3.</span></span> <span data-ttu-id="c3e19-107">Ce document contient des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="c3e19-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="c3e19-108">S’il existe une différence entre ces notes de publication et d’autres documents App-V, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="c3e19-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="c3e19-109">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="c3e19-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="c3e19-110">Se protéger contre les failles de sécurité et les virus</span><span class="sxs-lookup"><span data-stu-id="c3e19-110">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="c3e19-111">Pour vous aider à vous protéger contre les failles de sécurité et les virus, il est important d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé.</span><span class="sxs-lookup"><span data-stu-id="c3e19-111">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="c3e19-112">Pour plus d’informations, consultez le [site Web de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) sur la sécurité ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="c3e19-112">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="c3e19-113">Problèmes connus liés à la virtualisation des applications 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="c3e19-113">Known Issues with Application Virtualization4.6 SP3</span></span>


<span data-ttu-id="c3e19-114">Cette section fournit les informations les plus récentes sur les problèmes liés à Microsoft Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="c3e19-114">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6SP3.</span></span> <span data-ttu-id="c3e19-115">Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire.</span><span class="sxs-lookup"><span data-stu-id="c3e19-115">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="c3e19-116">Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3e19-116">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="c3e19-117">Impossible d’ouvrir des liens hypertexte à l’aide d’Internet Explorer11 sur Microsoft Windows 8,1 au sein de l’environnement virtuel</span><span class="sxs-lookup"><span data-stu-id="c3e19-117">Unable to open hyperlinks using Internet Explorer11 on Microsoft Windows 8.1 within the Virtual Environment</span></span>

<span data-ttu-id="c3e19-118">Toute tentative d’ouverture des liens hypertexte à partir d’un environnement virtuel échoue sur Windows 8,1 à l’aide d’Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="c3e19-118">Attempting to open hyperlinks from within a virtual environment will fail on Windows 8.1 using Internet Explorer 11.</span></span> <span data-ttu-id="c3e19-119">En effet, Internet Explorer 11 est désormais fourni avec le mode de protection améliorée (EPM) activé par défaut, et l’application-V ne peut pas accéder aux clés de Registre, aux fichiers et aux objets de port de communication requis.</span><span class="sxs-lookup"><span data-stu-id="c3e19-119">This is because Internet Explorer 11 now ships with the Enhanced Protection Mode (EPM) enabled by default and this causes App-V to be unable to access required registry keys, files and communication port objects.</span></span>

<span data-ttu-id="c3e19-120">Solution de contournement: désactivez EPM dans Internet Explorer11 avant d’ouvrir un package App-V.</span><span class="sxs-lookup"><span data-stu-id="c3e19-120">WORKAROUND: Disable EPM in Internet Explorer11 before opening an App-V package.</span></span> <span data-ttu-id="c3e19-121">Cela vous permettra d’ouvrir Internet Explorer à partir de l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="c3e19-121">This will allow you to open Internet Explorer from within the virtual environment.</span></span>

## <span data-ttu-id="c3e19-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3e19-122">Related topics</span></span>


[<span data-ttu-id="c3e19-123">À propos de Microsoft Application Virtualization4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="c3e19-123">About Microsoft Application Virtualization 4.6 SP3</span></span>](about-microsoft-application-virtualization-46-sp3.md)

 

 






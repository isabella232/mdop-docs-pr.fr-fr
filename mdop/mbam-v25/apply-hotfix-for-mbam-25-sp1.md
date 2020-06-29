---
title: Application de correctifs sur MBAM2.5SP1
description: Application de correctifs sur MBAM2.5SP1
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810404"
---
# <span data-ttu-id="f16ae-103">Application de correctifs sur MBAM2.5SP1</span><span class="sxs-lookup"><span data-stu-id="f16ae-103">Applying hotfixes on MBAM 2.5 SP1</span></span>
<span data-ttu-id="f16ae-104">Cette rubrique décrit la procédure d’application des correctifs pour l’administration et la surveillance de Microsoft BitLocker (MBAM) Server 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="f16ae-104">This topic describes the process for applying the hotfixes for Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>

### <span data-ttu-id="f16ae-105">Avant de commencer, téléchargez la dernière version du correctif de l’administration et de la surveillance de BitLocker (MBAM) Server 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="f16ae-105">Before you begin, download the latest hotfix of Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>
[<span data-ttu-id="f16ae-106">Pack d’optimisation de bureau</span><span class="sxs-lookup"><span data-stu-id="f16ae-106">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> <span data-ttu-id="f16ae-107">Pour plus d’informations sur les versions d’Hotfix, voir le [graphique de version MBAM](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span><span class="sxs-lookup"><span data-stu-id="f16ae-107">For more information about the hotfix releases, see the [MBAM version chart](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span></span>

#### <span data-ttu-id="f16ae-108">Procédure de mise à jour du serveur MBAM pour l’environnement MBAM existant</span><span class="sxs-lookup"><span data-stu-id="f16ae-108">Steps to update the MBAM Server for existing MBAM environment</span></span> 
1. <span data-ttu-id="f16ae-109">Supprimez la fonctionnalité du serveur MBAM (pour ce faire, ouvrez l’outil Configuration de MBAM Server, puis sélectionnez Supprimer des fonctionnalités).</span><span class="sxs-lookup"><span data-stu-id="f16ae-109">Remove MBAM server feature (do this by opening the MBAM Server Configuration Tool, then selecting Remove Features).</span></span>
2. <span data-ttu-id="f16ae-110">Supprimez MDOP MBAM du panneau de configuration | Programmes et fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="f16ae-110">Remove MDOP MBAM from Control Panel | Programs and Features.</span></span>
3. <span data-ttu-id="f16ae-111">Installez les composants serveur MBAM 2,5 SP1 RTM.</span><span class="sxs-lookup"><span data-stu-id="f16ae-111">Install MBAM 2.5 SP1 RTM server components.</span></span>
4. <span data-ttu-id="f16ae-112">Installez le dernier correctif cumulatif MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="f16ae-112">Install lastest MBAM 2.5 SP1 hotfix rollup.</span></span>
5. <span data-ttu-id="f16ae-113">Configurer les fonctionnalités d’MBAM à l’aide de MBAM Server Configurator.</span><span class="sxs-lookup"><span data-stu-id="f16ae-113">Configure MBAM features using MBAM Server Configurator.</span></span>

#### <span data-ttu-id="f16ae-114">Procédures d’installation du nouveau correctif MBAM 2,5 SP1 pour le serveur</span><span class="sxs-lookup"><span data-stu-id="f16ae-114">Steps to install the new MBAM 2.5 SP1 server hotfix</span></span>
<span data-ttu-id="f16ae-115">Reportez-vous au document pour l' [installation d’un nouveau serveur](deploying-the-mbam-25-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="f16ae-115">Refer to the document for [new server installation](deploying-the-mbam-25-server-infrastructure.md).</span></span>

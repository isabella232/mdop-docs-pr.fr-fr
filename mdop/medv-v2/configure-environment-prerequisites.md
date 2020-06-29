---
title: Configurer la configuration requise de l'environnement
description: Configurer la configuration requise de l'environnement
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811760"
---
# <span data-ttu-id="b1d11-103">Configurer la configuration requise de l'environnement</span><span class="sxs-lookup"><span data-stu-id="b1d11-103">Configure Environment Prerequisites</span></span>


<span data-ttu-id="b1d11-104">Avant de déployer et d’exécuter Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, vous devez vous assurer que votre environnement répond aux conditions minimales requises suivantes.</span><span class="sxs-lookup"><span data-stu-id="b1d11-104">Before you can deploy and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you must ensure that your environment meets the following minimum prerequisites.</span></span>

**<span data-ttu-id="b1d11-105">Windows7</span><span class="sxs-lookup"><span data-stu-id="b1d11-105">Windows 7</span></span>**

<span data-ttu-id="b1d11-106">L’agent hôte MED-V et le module de création de package de l’espace de travail MED-V sont uniquement pris en charge dans Windows 7 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b1d11-106">The MED-V Host Agent and the MED-V Workspace Packager are only supported in Windows 7 or newer.</span></span>

**<span data-ttu-id="b1d11-107">Windows XP SP3</span><span class="sxs-lookup"><span data-stu-id="b1d11-107">Windows XP SP3</span></span>**

<span data-ttu-id="b1d11-108">L’agent d’invité MED-V est uniquement pris en charge par Windows XP SP3.</span><span class="sxs-lookup"><span data-stu-id="b1d11-108">The MED-V Guest Agent is only supported in Windows XP SP3.</span></span>

**<span data-ttu-id="b1d11-109">.NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="b1d11-109">.NET Framework 3.5 SP1</span></span>**

<span data-ttu-id="b1d11-110">Les agents d’accueil et les agents invités de MED-V et le package de l’espace de travail MED-V nécessitent Microsoft .NET Framework 3,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="b1d11-110">The MED-V Host and Guest agents and the MED-V Workspace Packager require the Microsoft .NET Framework 3.5 SP1.</span></span>

<span data-ttu-id="b1d11-111">**Important**  Vous devez également installer la mise à jour [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) qui répond aux problèmes de compatibilité des applications connus.</span><span class="sxs-lookup"><span data-stu-id="b1d11-111">**Important** You must also install the update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950), which addresses several known application compatibility issues.</span></span>

 

<span data-ttu-id="b1d11-112">**Remarques**  Vous devez installer manuellement .NET Framework 3,5 SP1 et la mise à jour KB959209 dans l’image du PC virtuel Windows que vous préparez pour une utilisation avec MED-V.</span><span class="sxs-lookup"><span data-stu-id="b1d11-112">**Note** You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="b1d11-113">Toutefois, par défaut, Microsoft .NET Framework 3,5 SP1 et la mise à jour sont inclus lorsque vous installez Windows 7 sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="b1d11-113">However, by default, the Microsoft .NET Framework 3.5 SP1 and the update are included when you install Windows 7 on the host computer.</span></span>

 

**<span data-ttu-id="b1d11-114">Une infrastructure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b1d11-114">An Active Directory Infrastructure</span></span>**

<span data-ttu-id="b1d11-115">La stratégie de groupe fournit la gestion et la configuration centralisées des systèmes d’exploitation, des applications et des paramètres des utilisateurs dans un environnement Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1d11-115">Group Policy provides the centralized management and configuration of operating systems, applications, and users' settings in an Active Directory environment.</span></span>

## <span data-ttu-id="b1d11-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1d11-116">Related topics</span></span>


[<span data-ttu-id="b1d11-117">Configurer les composants requis pour l'installation</span><span class="sxs-lookup"><span data-stu-id="b1d11-117">Configure Installation Prerequisites</span></span>](configure-installation-prerequisites.md)

[<span data-ttu-id="b1d11-118">Architecture de haut niveau</span><span class="sxs-lookup"><span data-stu-id="b1d11-118">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="b1d11-119">Configurations prises en charge par MED-V2.0</span><span class="sxs-lookup"><span data-stu-id="b1d11-119">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 






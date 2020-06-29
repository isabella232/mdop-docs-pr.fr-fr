---
title: Mise à jour de MED-V2.0
description: Mise à jour de MED-V2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810133"
---
# <span data-ttu-id="eeb4a-103">Mise à jour de MED-V2.0</span><span class="sxs-lookup"><span data-stu-id="eeb4a-103">Updating MED-V 2.0</span></span>


<span data-ttu-id="eeb4a-104">Contribuez à sécuriser votre système en appliquant les mises à jour de sécurité appropriées pour Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-104">Help secure your system by applying the appropriate security updates for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="eeb4a-105">Mise à jour de MED-V</span><span class="sxs-lookup"><span data-stu-id="eeb4a-105">Updating MED-V</span></span>


<span data-ttu-id="eeb4a-106">Vous pouvez mettre à jour MED-V de manière interactive, par l’utilisateur final ou en silence à l’aide d’un système de distribution de logiciels électronique.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-106">You can update MED-V interactively, by the end user, or silently by using an electronic software distribution system.</span></span> <span data-ttu-id="eeb4a-107">L’installation de l’agent hôte MED-V met à niveau l’agent hôte MED-V, puis met à jour l’espace de travail MED-V si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-107">Installation of the MED-V Host Agent upgrades the MED-V Host Agent and then updates the MED-V workspace if required.</span></span> <span data-ttu-id="eeb4a-108">L’agent d’hébergement MED-V et l’agent invité se synchronisent. Si des applications sont exécutées à partir de l’espace de travail MED-V alors que l’agent hôte MED-V est en cours de mise à jour, le redémarrage de l’ordinateur hôte est requis pour achever la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-108">The MED-V Host Agent and Guest Agent keep in sync. If applications are running from the MED-V workspace while the MED-V Host Agent is being updated, a restart of the host computer is required to complete the update.</span></span> <span data-ttu-id="eeb4a-109">Si aucune application n’est en cours d’exécution, MED-V est redémarré automatiquement et la mise à niveau est terminée sans redémarrage de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-109">If no applications are running, MED-V is restarted automatically and the upgrade is completed without a restart of the host computer.</span></span>

<span data-ttu-id="eeb4a-110">Si vous effectuez une mise à jour de MED-V à l’aide d’un système de distribution de logiciels électronique, vous pouvez contrôler le comportement de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-110">If you are updating MED-V by using an electronic software distribution system, you can control the restart behavior.</span></span> <span data-ttu-id="eeb4a-111">Pour cela, supprimez le redémarrage en tapant **REBOOT = «ReallySuppress»** à l’invite de commandes lors de l’installation d' MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-111">To do this, suppress the restart by typing **REBOOT=”ReallySuppress”** at the command prompt when installing MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="eeb4a-112">Ensuite, configurez le système de distribution de logiciels électronique pour capturer le code de retour 3010 (qui indique qu’un redémarrage est requis) et exécutez le comportement de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="eeb4a-112">Then, configure the electronic software distribution system to capture the 3010 return code (which signals that a restart is required) and perform the set restart behavior.</span></span>

## <span data-ttu-id="eeb4a-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eeb4a-113">Related topics</span></span>


[<span data-ttu-id="eeb4a-114">Informations techniques de référence pour MED-V</span><span class="sxs-lookup"><span data-stu-id="eeb4a-114">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 






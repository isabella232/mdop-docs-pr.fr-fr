---
title: Résolution des problèmes de déploiement
description: Résolution des problèmes de déploiement
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809630"
---
# <span data-ttu-id="793bd-103">Résolution des problèmes de déploiement</span><span class="sxs-lookup"><span data-stu-id="793bd-103">Deployment Troubleshooting</span></span>


<span data-ttu-id="793bd-104">Cette rubrique contient des informations pour vous aider à résoudre les problèmes de déploiement dans Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="793bd-104">This topic includes information to help you troubleshoot deployment issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="793bd-105">Résoudre les problèmes de déploiement MED-V</span><span class="sxs-lookup"><span data-stu-id="793bd-105">Troubleshooting Issues in MED-V Deployment</span></span>


<span data-ttu-id="793bd-106">Le problème suivant peut se produire lorsque vous déployez MED-V.</span><span class="sxs-lookup"><span data-stu-id="793bd-106">The following issue might occur when you deploy MED-V.</span></span> <span data-ttu-id="793bd-107">La solution aide à résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="793bd-107">The solution helps troubleshoot this issue.</span></span>

**<span data-ttu-id="793bd-108">Des problèmes se produisent lors de l’installation de MED-V pour l’utilisateur actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="793bd-108">Problems Occur if Installing MED-V for Current User Only.</span></span>** <span data-ttu-id="793bd-109">MED-V ne prend en charge que l’installation du gestionnaire de package d’espace de travail MED-V, de l’agent hôte MED-V et de l’espace de travail MED-V pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="793bd-109">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="793bd-110">L’installation pour l’utilisateur actuel cause uniquement les échecs de l’installation des composants et de l’installation de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="793bd-110">Installing for the current user only causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>

**<span data-ttu-id="793bd-111">Solution</span><span class="sxs-lookup"><span data-stu-id="793bd-111">Solution</span></span>**

<span data-ttu-id="793bd-112">N’utilisez jamais l’option **ALLUSERS = ""** lors de l’installation des composants MED-V.</span><span class="sxs-lookup"><span data-stu-id="793bd-112">Never use the option **ALLUSERS=””** when installing the MED-V components.</span></span>

**<span data-ttu-id="793bd-113">MED-V nécessite une utilisation exclusive de la pile de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="793bd-113">MED-V Requires Exclusive Use of the Virtualization Stack.</span></span>** <span data-ttu-id="793bd-114">Seule une pile de virtualisation peut être exécutée à la fois sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="793bd-114">Only one virtualization stack can be run at a time on a computer.</span></span> <span data-ttu-id="793bd-115">Le PC virtuel Windows doit utiliser la pile virtuelle et MED-V dépend du PC virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="793bd-115">Windows Virtual PC must use the virtual stack, and MED-V depends on Windows Virtual PC.</span></span> <span data-ttu-id="793bd-116">Par conséquent, si vous essayez de déployer ou d’utiliser MED-V lorsque d’autres applications utilisent la pile virtuelle, MED-V ne peut pas s’exécuter ou être installé correctement.</span><span class="sxs-lookup"><span data-stu-id="793bd-116">Therefore, if you try to deploy or use MED-V when other applications are running that use the virtual stack, MED-V cannot run or be successfully installed.</span></span>

**<span data-ttu-id="793bd-117">Solution</span><span class="sxs-lookup"><span data-stu-id="793bd-117">Solution</span></span>**

<span data-ttu-id="793bd-118">Fermez toute application en cours d’exécution qui utilise la pile de virtualisation avant d’installer ou d’exécuter MED-V.</span><span class="sxs-lookup"><span data-stu-id="793bd-118">Close any application that is running that uses the virtualization stack before you install or run MED-V.</span></span>

**<span data-ttu-id="793bd-119">Les raccourcis restent après la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="793bd-119">Shortcuts Remain after Uninstall.</span></span>** <span data-ttu-id="793bd-120">Par défaut, lorsque vous désinstallez MED-V, les raccourcis du menu **Démarrer** de l’utilisateur final sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="793bd-120">By default, when you uninstall MED-V, shortcuts in the end user’s **Start** menu are removed.</span></span> <span data-ttu-id="793bd-121">Toutefois, dans certains cas, par exemple pour les utilisateurs finaux qui exécutent des profils itinérants, le raccourci vers les applications publiées MED-V reste dans le menu **Démarrer** de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="793bd-121">However, in certain situations, such as for end users who are running roaming profiles, shortcuts to MED-V published applications remain in the end user’s **Start** menu.</span></span>

**<span data-ttu-id="793bd-122">Solution</span><span class="sxs-lookup"><span data-stu-id="793bd-122">Solution</span></span>**

<span data-ttu-id="793bd-123">Pour supprimer manuellement les raccourcis restant dans le menu **Démarrer** , cliquez avec le bouton droit sur les raccourcis, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="793bd-123">To manually delete the remaining shortcuts on the **Start** menu, right-click the shortcuts, and then click **Remove**.</span></span>

**<span data-ttu-id="793bd-124">Désactivez le paramètre de stratégie de groupe message d’ouverture de session dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="793bd-124">Disable Logon Message Group Policy Setting in the MED-V Workspace.</span></span>** <span data-ttu-id="793bd-125">Si le message d’ouverture de session Windows XP est activé dans l’espace de travail MED-V, l’utilisateur final doit se connecter chaque fois qu’il souhaite ouvrir une application virtuelle MED-V.</span><span class="sxs-lookup"><span data-stu-id="793bd-125">If the Windows XP logon message is enabled in the MED-V workspace, the end user must log on every time they want to open a MED-V virtual application.</span></span> <span data-ttu-id="793bd-126">Cela crée une mauvaise utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="793bd-126">This creates a poor user experience.</span></span>

**<span data-ttu-id="793bd-127">Solution</span><span class="sxs-lookup"><span data-stu-id="793bd-127">Solution</span></span>**

<span data-ttu-id="793bd-128">Désactivez les paramètres de stratégie de groupe suivants dans l’ordinateur virtuel MED-V:</span><span class="sxs-lookup"><span data-stu-id="793bd-128">Disable the following Group Policy settings in the MED-V virtual machine:</span></span>

**<span data-ttu-id="793bd-129">Ouverture de session interactive: contenu du message pour les utilisateurs essayant de se connecter</span><span class="sxs-lookup"><span data-stu-id="793bd-129">Interactive logon: Message text for users attempting to log on</span></span>**

**<span data-ttu-id="793bd-130">Ouverture de session interactive: titre du message pour les utilisateurs essayant de se connecter</span><span class="sxs-lookup"><span data-stu-id="793bd-130">Interactive logon: Message title for users attempting to log on</span></span>**

## <span data-ttu-id="793bd-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="793bd-131">Related topics</span></span>


[<span data-ttu-id="793bd-132">Résolution des problèmes d'opérations</span><span class="sxs-lookup"><span data-stu-id="793bd-132">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

 

 






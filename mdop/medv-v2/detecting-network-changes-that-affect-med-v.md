---
title: Détection des modifications réseau qui affectent MED-V
description: Détection des modifications réseau qui affectent MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809917"
---
# <span data-ttu-id="97cc5-103">Détection des modifications réseau qui affectent MED-V</span><span class="sxs-lookup"><span data-stu-id="97cc5-103">Detecting Network Changes that Affect MED-V</span></span>


<span data-ttu-id="97cc5-104">La solution 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V) vous permet de configurer votre environnement pour détecter certaines modifications réseau qui peuvent se produire après le déploiement des espaces de travail MED-v et qui peut affecter MED-V.</span><span class="sxs-lookup"><span data-stu-id="97cc5-104">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution lets you configure your environment to detect certain network changes that might occur after MED-V workspaces are deployed and that can affect MED-V.</span></span>

<span data-ttu-id="97cc5-105">Cette fonctionnalité inclut un composant s’exécutant dans le système d’exploitation invité, qui est averti de la modification de la configuration réseau de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="97cc5-105">The feature includes a component running in the guest operating system that is notified of network configuration changes on the host computer.</span></span> <span data-ttu-id="97cc5-106">Il permet à une application non-Microsoft ou d’une autre application en cours d’exécution dans l’invité de résoudre les points de terminaison réseau pour lesquels l’application ESD ou l’application est résolue.</span><span class="sxs-lookup"><span data-stu-id="97cc5-106">It allows a non-Microsoft ESD or other application that is running in the guest to resolve to the same network endpoints that the host ESD or application resolves to.</span></span>

<span data-ttu-id="97cc5-107">**Remarques**  Cette fonctionnalité n’est disponible que si l’ordinateur virtuel est configuré pour le mode traduction d’adresses réseau (NAT).</span><span class="sxs-lookup"><span data-stu-id="97cc5-107">**Note** This feature is only available if the virtual machine is configured for network address translation (NAT) mode.</span></span> <span data-ttu-id="97cc5-108">S’il s’agit d’un ordinateur virtuel configuré pour le mode pont, aucune indication de modification n’est générée.</span><span class="sxs-lookup"><span data-stu-id="97cc5-108">If the virtual machine is configured for BRIDGED mode, no change indications are generated.</span></span>

 

<span data-ttu-id="97cc5-109">Cette section fournit des informations et des instructions pour vous aider à surveiller les changements de réseau qui peuvent affecter MED-V.</span><span class="sxs-lookup"><span data-stu-id="97cc5-109">This section provides information and instruction to assist you in monitoring those network changes that can affect MED-V.</span></span>

## <span data-ttu-id="97cc5-110">Pour détecter les changements de réseau pour MED-V</span><span class="sxs-lookup"><span data-stu-id="97cc5-110">To detect network changes for MED-V</span></span>


<span data-ttu-id="97cc5-111">Après avoir déployé vos espaces de travail MED-V, vous pouvez surveiller les modifications apportées à certaines configurations réseau en préformant les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="97cc5-111">After you have deployed your MED-V workspaces, you can monitor changes to certain network configurations by preforming the following tasks:</span></span>

1. <span data-ttu-id="97cc5-112">Créez un fichier MOF (Managed Object Format) qui cherchera les modifications de configuration réseau que vous souhaitez surveiller.</span><span class="sxs-lookup"><span data-stu-id="97cc5-112">Create a Managed Object Format (MOF) file that will look for the network configuration changes that you want to monitor.</span></span> <span data-ttu-id="97cc5-113">Le code suivant montre un exemple du fichier MOF que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="97cc5-113">The following code shows an example of the MOF file that you can create.</span></span>

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. <span data-ttu-id="97cc5-114">Compilez le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="97cc5-114">Compile the MOF file.</span></span>

3. <span data-ttu-id="97cc5-115">Installez le fichier MOF dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="97cc5-115">Install the MOF file in the guest.</span></span>

<span data-ttu-id="97cc5-116">Une fois que vous avez installé le fichier MOF, vous pouvez créer un abonnement Event qui s’abonne aux événements de création, de modification ou de suppression WMI pour la classe **CCM \ _NetworkAdapters** .</span><span class="sxs-lookup"><span data-stu-id="97cc5-116">After you have installed the MOF file, you can create an event subscription that subscribes to Windows Management Instrumentation (WMI) creation, modification, or deletion events for the **CCM\_NetworkAdapters** class.</span></span> <span data-ttu-id="97cc5-117">Les modifications suivantes sont détectées sur l’hôte:</span><span class="sxs-lookup"><span data-stu-id="97cc5-117">This detects the following changes to the host:</span></span>

<span data-ttu-id="97cc5-118">Quelles sont les modifications apportées à la configuration du réseau, par exemple les modifications apportées à l’adresse IP ou à la carte réseau?</span><span class="sxs-lookup"><span data-stu-id="97cc5-118">Are there any configuration changes to the network, such as changes to the IP address or network adapter?</span></span>

<span data-ttu-id="97cc5-119">Le réseau est-il disponible ou indisponible?</span><span class="sxs-lookup"><span data-stu-id="97cc5-119">Is the network available or unavailable?</span></span>

<span data-ttu-id="97cc5-120">Le programme d’installation du réseau a-t-il été passé du mode pont au mode NAT?</span><span class="sxs-lookup"><span data-stu-id="97cc5-120">Was the network setup changed from BRIDGED mode to NAT mode?</span></span>

<span data-ttu-id="97cc5-121">Le programme d’installation du réseau a-t-il été passé du mode NAT au mode relié?</span><span class="sxs-lookup"><span data-stu-id="97cc5-121">Was the network setup changed from NAT mode to BRIDGED mode?</span></span>

<span data-ttu-id="97cc5-122">Un composant MED-V sur l’hôte surveille le réseau de ces modifications, puis signale l’invité du changement.</span><span class="sxs-lookup"><span data-stu-id="97cc5-122">A MED-V component on the host monitors the network for these changes and then signals the guest of the change.</span></span> <span data-ttu-id="97cc5-123">Un composant de l’invité crée une instance WMI permettant de surveiller l’espace de travail MED-V pour ces modifications.</span><span class="sxs-lookup"><span data-stu-id="97cc5-123">A component in the guest creates a WMI instance to monitor the MED-V workspace for these changes.</span></span>

<span data-ttu-id="97cc5-124">L’abonnement d’événements que vous avez créé avertit par le système WMI lorsque l’un ou plusieurs de ces changements de réseau (création, modification ou suppression) se produisent.</span><span class="sxs-lookup"><span data-stu-id="97cc5-124">The event subscription you created provides notification through the WMI system when one or more of these network changes – creation, modification, or deletion – occurs.</span></span>

## <span data-ttu-id="97cc5-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97cc5-125">Related topics</span></span>


[<span data-ttu-id="97cc5-126">Surveiller des espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="97cc5-126">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="97cc5-127">Gérer les paramètres de l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="97cc5-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 






---
title: Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server
description: Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806438"
---
# <span data-ttu-id="f6070-103">Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="f6070-103">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>


<span data-ttu-id="f6070-104">Dans le déploiement d’un serveur de virtualisation des applications, les packages d’application virtuels qui ont été séquencés, testés et détectés déployés sont copiés sur le partage de contenu principal à utiliser par le serveur de gestion de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="f6070-104">In an Application Virtualization Server-based deployment, virtual application packages that have been sequenced, tested, and found deployable are copied to the main CONTENT share to be used by the Application Virtualization Management Server.</span></span> <span data-ttu-id="f6070-105">Une fois les packages importés sur le serveur de gestion de la virtualisation des applications, ils peuvent être publiés aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="f6070-105">After the packages are imported on the Application Virtualization Management Server, they can be published to the end users.</span></span>

<span data-ttu-id="f6070-106">**Remarques**  Le partage de contenu doit se trouver sur le stockage de disque connecté du serveur.</span><span class="sxs-lookup"><span data-stu-id="f6070-106">**Note** The CONTENT share should be located on the server’s attached disk storage.</span></span> <span data-ttu-id="f6070-107">L’utilisation d’un périphérique de stockage réseau, tel qu’un réseau SAN ou un partage DFS, doit être considérée soigneusement en raison de l’impact sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="f6070-107">Using a network storage device such as a SAN or a DFS share should be considered carefully because of the network impact.</span></span>

 

<span data-ttu-id="f6070-108">Les applications sont configurées pour les groupes Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f6070-108">Applications are provisioned to Active Directory groups.</span></span> <span data-ttu-id="f6070-109">En règle générale, l’administrateur de virtualisation des applications va créer des groupes Active Directory pour chaque application virtuelle à publier, puis ajouter les utilisateurs appropriés à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="f6070-109">Typically, the Application Virtualization administrator will create Active Directory groups for each virtual application to be published and then add the appropriate users to those groups.</span></span> <span data-ttu-id="f6070-110">Lorsque les utilisateurs se connectent à leur station de travail, le client de virtualisation des applications effectue par défaut une actualisation de publication en utilisant les informations d’identification de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="f6070-110">When the users log on to their workstations, the Application Virtualization Client, by default, performs a publishing refresh using the credentials of the logged on user.</span></span> <span data-ttu-id="f6070-111">L’utilisateur peut alors lancer des applications à partir de n’importe quel emplacement.</span><span class="sxs-lookup"><span data-stu-id="f6070-111">The user can then start applications from wherever the shortcuts have been placed.</span></span> <span data-ttu-id="f6070-112">L’administrateur de virtualisation des applications détermine l’emplacement et le nombre de raccourcis situés sur le système client lors du séquençage de l’application.</span><span class="sxs-lookup"><span data-stu-id="f6070-112">The Application Virtualization administrator determines where and how many shortcuts are located on the client system during the sequencing of the application.</span></span>

<span data-ttu-id="f6070-113">**Remarques**  Une *actualisation* de la publication est un appel du serveur de virtualisation des applications qui est défini sur le client de virtualisation des applications, qui permet de déterminer quels raccourcis d’application virtuelle sont envoyés au client pour une utilisation par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="f6070-113">**Note** A *publishing refresh* is a call to the Application Virtualization Server that is defined on the Application Virtualization Client, to determine which virtual application shortcuts are sent to the client for use by the end user.</span></span>

 

## <span data-ttu-id="f6070-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6070-114">Related topics</span></span>


[<span data-ttu-id="f6070-115">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="f6070-115">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="f6070-116">Procédure pour publier une application virtuelle sur le client</span><span class="sxs-lookup"><span data-stu-id="f6070-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="f6070-117">Présentation des composants du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f6070-117">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="f6070-118">Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="f6070-118">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 






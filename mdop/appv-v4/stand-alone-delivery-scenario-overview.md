---
title: Présentation du scénario de distribution autonome
description: Présentation du scénario de distribution autonome
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806254"
---
# <span data-ttu-id="c04b0-103">Présentation du scénario de distribution autonome</span><span class="sxs-lookup"><span data-stu-id="c04b0-103">Stand-Alone Delivery Scenario Overview</span></span>


<span data-ttu-id="c04b0-104">Le scénario de remise autonome est une solution idéale pour les environnements dans lesquels une connectivité à faible bande passante ou aucune connectivité ne limite la capacité du client de bureau de virtualisation des applications à diffuser des applications à partir de serveurs centralisés.</span><span class="sxs-lookup"><span data-stu-id="c04b0-104">The stand-alone delivery scenario is an ideal application virtualization solution for environments where either low bandwidth connectivity or no connectivity limits the ability of the Application Virtualization Desktop Client to stream applications from centralized servers.</span></span> <span data-ttu-id="c04b0-105">Dans ces environnements, les utilisateurs travaillent souvent à distance et les propriétaires d’appareils peuvent installer des applications à l’aide des fichiers du programme d’installation Windows.</span><span class="sxs-lookup"><span data-stu-id="c04b0-105">In these environments, users often work remotely and device owners install applications by using Windows Installer files.</span></span>

<span data-ttu-id="c04b0-106">Vous pouvez utiliser le Sequencer Application Virtualization pour créer des applications séquencées incluant des fichiers Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c04b0-106">You can use the Application Virtualization Sequencer to create sequenced applications that include Windows Installer files.</span></span> <span data-ttu-id="c04b0-107">Ces packages incluent les applications virtualisées, les informations de composition et les routines de programme d’installation nécessaires pour l’installation des packages sur les systèmes clients.</span><span class="sxs-lookup"><span data-stu-id="c04b0-107">These packages include the virtualized applications, publication information, and the necessary installer routines for installing the packages on the client systems.</span></span> <span data-ttu-id="c04b0-108">Le programme d’installation ajoute le package d’application virtuel au client de bureau Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="c04b0-108">The installer adds the virtual application package to the Microsoft Application Virtualization Desktop Client.</span></span> <span data-ttu-id="c04b0-109">Les informations de composition sont configurées pour charger des applications à partir d’un emplacement local plutôt que de les diffuser sur un réseau étendu.</span><span class="sxs-lookup"><span data-stu-id="c04b0-109">The publication information is configured to load applications from a local location rather than stream them across a WAN.</span></span> <span data-ttu-id="c04b0-110">Les utilisateurs peuvent se connecter temporairement à un réseau pour récupérer les fichiers Windows Installer ou les exécuter à partir d’un DVD.</span><span class="sxs-lookup"><span data-stu-id="c04b0-110">Users can temporarily connect to a network to retrieve the Windows Installer files or can run them from a DVD.</span></span>

<span data-ttu-id="c04b0-111">Le scénario de remise autonome fournit aux utilisateurs les avantages suivants:</span><span class="sxs-lookup"><span data-stu-id="c04b0-111">The stand-alone delivery scenario provides users the following benefits:</span></span>

-   <span data-ttu-id="c04b0-112">Opération de déploiement simple.</span><span class="sxs-lookup"><span data-stu-id="c04b0-112">Simple deployment operation.</span></span>

-   <span data-ttu-id="c04b0-113">Réseau et serveurs non nécessaires à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c04b0-113">Network and servers not needed at runtime.</span></span>

-   <span data-ttu-id="c04b0-114">Applications déjà mises en cache et disponibles pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c04b0-114">Applications pre-cached and available to all users.</span></span>

<span data-ttu-id="c04b0-115">Le scénario de remise autonome comporte les limitations suivantes:</span><span class="sxs-lookup"><span data-stu-id="c04b0-115">The stand-alone delivery scenario has the following limitations:</span></span>

-   <span data-ttu-id="c04b0-116">Les rapports automatisés intégrés ne sont pas disponibles; les rapports doivent être générés à l’aide d’outils de création de rapports externes.</span><span class="sxs-lookup"><span data-stu-id="c04b0-116">Built-in, automated reporting is unavailable; reports must be generated with external reporting tools.</span></span>

-   <span data-ttu-id="c04b0-117">Les applications doivent être transmises au client manuellement, comme les fichiers Windows Installer d’origine.</span><span class="sxs-lookup"><span data-stu-id="c04b0-117">Applications must be delivered to the client manually like the original Windows Installer files.</span></span>

## <span data-ttu-id="c04b0-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c04b0-118">Related topics</span></span>


[<span data-ttu-id="c04b0-119">Procédure pour installer manuellement Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="c04b0-119">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="c04b0-120">Procédure pour publier une application virtuelle sur le client</span><span class="sxs-lookup"><span data-stu-id="c04b0-120">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 






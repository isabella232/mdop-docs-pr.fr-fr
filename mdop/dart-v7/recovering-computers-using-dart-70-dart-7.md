---
title: Récupération des ordinateurs à l'aide de DaRT7.0
description: Récupération des ordinateurs à l'aide de DaRT7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809552"
---
# <span data-ttu-id="3eab6-103">Récupération des ordinateurs à l'aide de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="3eab6-103">Recovering Computers Using DaRT 7.0</span></span>


<span data-ttu-id="3eab6-104">Deux méthodes sont disponibles pour récupérer des ordinateurs à l’aide de Microsoft Diagnostics and Recovery Tools (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="3eab6-104">There are two methods available to recover computers using Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span> <span data-ttu-id="3eab6-105">Vous pouvez exécuter l’image de récupération DaRT7 localement ou utiliser la fonctionnalité de connexion à distance disponible dans DaRT7 pour récupérer un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="3eab6-105">You can either run the DaRT7 recovery image locally or use The Remote Connection feature available in DaRT7 to recover a remote computer.</span></span> <span data-ttu-id="3eab6-106">Les deux méthodes sont décrites plus en détail dans cette section.</span><span class="sxs-lookup"><span data-stu-id="3eab6-106">Both methods are described in more detail in this section.</span></span>

## <span data-ttu-id="3eab6-107">Récupérer des ordinateurs locaux en utilisant l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="3eab6-107">Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="3eab6-108">Pour récupérer un ordinateur local à l’aide de DaRT7, vous devez avoir une présentation physique de l’ordinateur de l’utilisateur final rencontrant des problèmes qui nécessitent DaRT.</span><span class="sxs-lookup"><span data-stu-id="3eab6-108">To recover a local computer by using DaRT7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

<span data-ttu-id="3eab6-109">Vous avez le choix entre différentes méthodes pour démarrer DaRT, en fonction du déploiement de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="3eab6-109">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="3eab6-110">Insérez un CD, un DVD ou un lecteur flash USB dans l’ordinateur défectueux, puis utilisez-le pour démarrer l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3eab6-110">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="3eab6-111">Démarrez dans DaRT à partir d’une partition de récupération sur l’ordinateur qui pose problème.</span><span class="sxs-lookup"><span data-stu-id="3eab6-111">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="3eab6-112">Démarrez dans DaRT à partir d’une partition distante sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="3eab6-112">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="3eab6-113">Pour plus d’informations sur les avantages et inconvénients de chaque méthode, voir [planification de l’enregistrement et du déploiement de l’image de récupération 7,0 de DART](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="3eab6-113">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

<span data-ttu-id="3eab6-114">Quelle que soit la méthode que vous utilisez pour démarrer dans DaRT, vous devez activer le périphérique de démarrage dans le BIOS pour l’option de démarrage ou les options que vous voulez mettre à disposition de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="3eab6-114">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="3eab6-115">**Remarques**  La configuration du BIOS est unique, en fonction du type de disque dur, de cartes réseau et d’autres éléments utilisés au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3eab6-115">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

[<span data-ttu-id="3eab6-116">Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="3eab6-116">How to Recover Local Computers Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="3eab6-117">Récupérer des ordinateurs distants à l’aide de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="3eab6-117">Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="3eab6-118">Grâce à la fonctionnalité de connexion à distance de DaRT, un administrateur informatique exécute les outils DaRT à distance sur un ordinateur d’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="3eab6-118">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="3eab6-119">Lorsque certaines informations sont fournies par l’utilisateur final (ou par un professionnel du support technique travaillant sur l’ordinateur de l’utilisateur final), l’administrateur informatique ou l’agent de support technique peut prendre le contrôle de l’ordinateur de l’utilisateur final et exécuter les outils DaRT nécessaires à distance.</span><span class="sxs-lookup"><span data-stu-id="3eab6-119">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="3eab6-120">**Important**  Les deux ordinateurs qui établissent une connexion à distance doivent faire partie du même réseau.</span><span class="sxs-lookup"><span data-stu-id="3eab6-120">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="3eab6-121">La fenêtre du **jeu d’outils de diagnostics et de récupération** inclut la possibilité d’exécuter le DART sur un ordinateur d’utilisateur final à distance à partir d’un ordinateur d’administration.</span><span class="sxs-lookup"><span data-stu-id="3eab6-121">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="3eab6-122">L’utilisateur final ouvre les outils DaRT sur le problème et démarre la session à distance en cliquant sur **connexion à distance**.</span><span class="sxs-lookup"><span data-stu-id="3eab6-122">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="3eab6-123">La fonctionnalité de connexion à distance sur l’ordinateur de l’utilisateur final crée les informations de connexion suivantes: un numéro de ticket, un port et une liste de toutes les adresses IP disponibles.</span><span class="sxs-lookup"><span data-stu-id="3eab6-123">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="3eab6-124">Le numéro de ticket et le port sont générés de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="3eab6-124">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="3eab6-125">L’administrateur informatique ou l’agent de support technique entre ces informations dans la **visionneuse de connexion à distance DART** pour établir la connexion aux services Terminal Server à l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="3eab6-125">The IT administrator or helpdesk agent enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="3eab6-126">La connexion de services Terminal Server établie permet à un administrateur informatique d’interagir à distance avec les outils DaRT sur l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="3eab6-126">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="3eab6-127">L’ordinateur de l’utilisateur final traite alors les informations de connexion, partage son écran et répond aux instructions de l’ordinateur de l’administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="3eab6-127">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="3eab6-128">Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="3eab6-128">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="3eab6-129">Autres ressources pour récupérer des ordinateurs à l’aide de DaRT7</span><span class="sxs-lookup"><span data-stu-id="3eab6-129">Other resources for recovering computers using DaRT7</span></span>


[<span data-ttu-id="3eab6-130">Opérations de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="3eab6-130">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 






---
title: Récupération des ordinateurs à l'aide de DaRT10
description: Récupération des ordinateurs à l'aide de DaRT10
author: dansimp
ms.assetid: 2ad7fab0-c22d-4171-8b5a-b2b7d7c0ad2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2031d55427e24638e41dfc6ed7b0ef437922e9c4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809666"
---
# <span data-ttu-id="9063d-103">Récupération des ordinateurs à l'aide de DaRT10</span><span class="sxs-lookup"><span data-stu-id="9063d-103">Recovering Computers Using DaRT 10</span></span>


<span data-ttu-id="9063d-104">Après le déploiement de l’image de récupération Microsoft Diagnostics and Recovery Tools (DaRT) 10, vous pouvez utiliser DaRT 10 pour récupérer des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="9063d-104">After deploying the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image, you can use DaRT 10 to recover computers.</span></span> <span data-ttu-id="9063d-105">Les informations contenues dans cette section décrivent les tâches de récupération que vous pouvez effectuer.</span><span class="sxs-lookup"><span data-stu-id="9063d-105">The information in this section describes the recovery tasks that you can perform.</span></span>

<span data-ttu-id="9063d-106">Vous avez le choix entre différentes méthodes pour démarrer DaRT, en fonction du déploiement de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="9063d-106">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="9063d-107">Insérez un CD, un DVD ou un lecteur flash USB dans l’ordinateur défectueux, puis utilisez-le pour démarrer l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9063d-107">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="9063d-108">Démarrez dans DaRT à partir d’une partition de récupération sur l’ordinateur qui pose problème.</span><span class="sxs-lookup"><span data-stu-id="9063d-108">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="9063d-109">Démarrez dans DaRT à partir d’une partition distante sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="9063d-109">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="9063d-110">Pour plus d’informations sur les avantages et inconvénients de chaque méthode, voir [planification de l’enregistrement et du déploiement de l’image de récupération DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="9063d-110">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="9063d-111">Quelle que soit la méthode que vous utilisez pour démarrer dans DaRT, vous devez activer le périphérique de démarrage dans le BIOS pour l’option de démarrage ou les options que vous voulez mettre à disposition de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="9063d-111">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="9063d-112">**Remarques**  La configuration du BIOS est unique, en fonction du type de disque dur, de cartes réseau et d’autres éléments utilisés au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9063d-112">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

## <span data-ttu-id="9063d-113">Récupérer un ordinateur local à l’aide de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="9063d-113">Recover a local computer by using the DaRT recovery image</span></span>


<span data-ttu-id="9063d-114">Pour récupérer un ordinateur local à l’aide de DaRT, vous devez avoir une présentation physique de l’ordinateur de l’utilisateur final rencontrant des problèmes qui nécessitent DaRT.</span><span class="sxs-lookup"><span data-stu-id="9063d-114">To recover a local computer by using DaRT, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

[<span data-ttu-id="9063d-115">Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="9063d-115">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md)

## <span data-ttu-id="9063d-116">Récupérer un ordinateur distant à l’aide de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="9063d-116">Recover a remote computer by using the DaRT recovery image</span></span>


<span data-ttu-id="9063d-117">Grâce à la fonctionnalité de connexion à distance de DaRT, un administrateur informatique exécute les outils DaRT à distance sur un ordinateur d’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="9063d-117">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="9063d-118">Lorsque certaines informations sont fournies par l’utilisateur final (ou par un professionnel du support technique travaillant sur l’ordinateur de l’utilisateur final), l’administrateur informatique ou le service de support technique peut prendre le contrôle de l’ordinateur de l’utilisateur final et exécuter les outils DaRT nécessaires à distance.</span><span class="sxs-lookup"><span data-stu-id="9063d-118">After certain information is provided by the end user (or by a help desk professional working on the end-user computer), the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="9063d-119">**Important**  Les deux ordinateurs qui établissent une connexion à distance doivent faire partie du même réseau.</span><span class="sxs-lookup"><span data-stu-id="9063d-119">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="9063d-120">La fenêtre du **jeu d’outils de diagnostics et de récupération** inclut la possibilité d’exécuter le DART sur un ordinateur d’utilisateur final à distance à partir d’un ordinateur d’administration.</span><span class="sxs-lookup"><span data-stu-id="9063d-120">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="9063d-121">L’utilisateur final ouvre les outils DaRT sur le problème et démarre la session à distance en cliquant sur **connexion à distance**.</span><span class="sxs-lookup"><span data-stu-id="9063d-121">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="9063d-122">La fonctionnalité de connexion à distance sur l’ordinateur de l’utilisateur final crée les informations de connexion suivantes: un numéro de ticket, un port et une liste de toutes les adresses IP disponibles.</span><span class="sxs-lookup"><span data-stu-id="9063d-122">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="9063d-123">Le numéro de ticket et le port sont générés de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="9063d-123">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="9063d-124">L’administrateur informatique ou le service de support technique entre les informations dans la **visionneuse de connexion à distance DART** pour établir la connexion aux services Terminal Server à l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="9063d-124">The IT administrator or help desk worker enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="9063d-125">La connexion de services Terminal Server établie permet à un administrateur informatique d’interagir à distance avec les outils DaRT sur l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="9063d-125">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="9063d-126">L’ordinateur de l’utilisateur final traite alors les informations de connexion, partage son écran et répond aux instructions de l’ordinateur de l’administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="9063d-126">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="9063d-127">Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="9063d-127">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md)

## <span data-ttu-id="9063d-128">Autres ressources pour récupérer des ordinateurs avec DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9063d-128">Other resources for recovering computers using DaRT 10</span></span>


[<span data-ttu-id="9063d-129">Opérations de DaRT10</span><span class="sxs-lookup"><span data-stu-id="9063d-129">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

 

 






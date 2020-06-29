---
title: Comment installer l'agent hôte MED-V manuellement
description: Comment installer l'agent hôte MED-V manuellement
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804572"
---
# <span data-ttu-id="f17a6-103">Comment installer l'agent hôte MED-V manuellement</span><span class="sxs-lookup"><span data-stu-id="f17a6-103">How to Manually Install the MED-V Host Agent</span></span>


<span data-ttu-id="f17a6-104">Il existe deux composants distincts mais liés à la solution 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V): agent d’hébergement et agent invité MED-V.</span><span class="sxs-lookup"><span data-stu-id="f17a6-104">There are two separate but related components to the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="f17a6-105">L’agent hôte réside sur l’ordinateur hôte (l’ordinateur de l’utilisateur exécutant Windows 7) et fournit un canal permettant de communiquer avec l’invité MED-V (l’ordinateur virtuel MED-V qui s’exécute sur l’ordinateur hôte).</span><span class="sxs-lookup"><span data-stu-id="f17a6-105">The Host Agent resides on the host computer (a user’s computer that is running Windows 7) and provides a channel to communicate with the MED-V guest (the MED-V virtual machine running in the host computer).</span></span> <span data-ttu-id="f17a6-106">Il fournit également certaines fonctionnalités associées à MED-V, comme la publication d’applications.</span><span class="sxs-lookup"><span data-stu-id="f17a6-106">It also provides certain MED-V related functionality, such as application publishing.</span></span>

<span data-ttu-id="f17a6-107">En règle générale, vous déployez et installez l’agent d’hébergement MED-V en utilisant la méthode de mise en service préférée de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="f17a6-107">Typically, you deploy and install the MED-V Host Agent by using your company’s preferred method of provisioning software.</span></span> <span data-ttu-id="f17a6-108">Néanmoins, avant de déployer MED-V au sein de votre entreprise, vous préférerez peut-être installer l’agent hôte localement pour le test.</span><span class="sxs-lookup"><span data-stu-id="f17a6-108">However, before deploying MED-V across your enterprise, you might prefer to install the Host Agent locally for testing.</span></span> <span data-ttu-id="f17a6-109">Cette section fournit des instructions pas à pas pour l’installation manuelle de l’agent hôte MED-V.</span><span class="sxs-lookup"><span data-stu-id="f17a6-109">This section provides step-by-step instructions for manually installing the MED-V Host Agent.</span></span>

<span data-ttu-id="f17a6-110">**Remarques**  L’agent d’invité MED-V est automatiquement installé lors de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="f17a6-110">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<span data-ttu-id="f17a6-111">**Important**  Fermez Internet Explorer avant d’installer l’agent d’hébergement MED-V, sinon des conflits peuvent se produire plus tard avec la redirection d’URL.</span><span class="sxs-lookup"><span data-stu-id="f17a6-111">**Important** Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="f17a6-112">Vous pouvez également le faire en spécifiant un redémarrage de l’ordinateur lors d’une distribution.</span><span class="sxs-lookup"><span data-stu-id="f17a6-112">You can also do this by specifying a computer restart during a distribution.</span></span>

 

**<span data-ttu-id="f17a6-113">Pour installer l’agent hôte MED-V</span><span class="sxs-lookup"><span data-stu-id="f17a6-113">To install the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="f17a6-114">Recherchez les fichiers d’installation de MED-V que vous avez reçus dans le cadre de votre téléchargement de logiciels.</span><span class="sxs-lookup"><span data-stu-id="f17a6-114">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="f17a6-115">Double-cliquez sur le fichier d’installation MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="f17a6-115">Double-click the MED-V\_HostAgent\_Setup installation file.</span></span>

    <span data-ttu-id="f17a6-116">L’Assistant de configuration de l' **agent d’hébergement MED-V de Microsoft Enterprise Desktop Virtualization** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f17a6-116">The **Microsoft Enterprise Desktop Virtualization (MED-V) Host Agent Setup** wizard opens.</span></span> <span data-ttu-id="f17a6-117">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="f17a6-117">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="f17a6-118">Acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="f17a6-118">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="f17a6-119">Sélectionnez le dossier de destination pour l’installation de l’agent hôte MED-V.</span><span class="sxs-lookup"><span data-stu-id="f17a6-119">Select the destination folder for installing the MED-V Host Agent.</span></span> <span data-ttu-id="f17a6-120">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f17a6-120">Click **Next**.</span></span>

5.  <span data-ttu-id="f17a6-121">Pour commencer l’installation de l’agent hôte, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="f17a6-121">To begin the Host Agent installation, click **Install**.</span></span>

6.  <span data-ttu-id="f17a6-122">Une fois l’installation terminée, cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="f17a6-122">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="f17a6-123">Pour vérifier que l’installation de l’agent hôte a réussi, cliquez sur **Démarrer**, sur **tous les programmes**, sur **virtualisation du bureau Microsoft entreprise**, puis sur **agent hôte MED-V**.</span><span class="sxs-lookup"><span data-stu-id="f17a6-123">To verify that the installation of the Host Agent was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="f17a6-124">**Remarques**  Tant qu’un espace de travail MED-V n’est pas installé, l’agent hôte MED-V peut être démarré et exécuté, mais ne fournit aucune fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f17a6-124">**Note** Until a MED-V workspace is installed, the MED-V Host Agent can be started and runs, but provides no functionality.</span></span>

 

## <span data-ttu-id="f17a6-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f17a6-125">Related topics</span></span>


[<span data-ttu-id="f17a6-126">Déploiement des composants de MED-V via un système de distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="f17a6-126">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="f17a6-127">Comment installer le Gestionnaire de package de l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="f17a6-127">How to Install the MED-V Workspace Packager</span></span>](how-to-install-the-med-v-workspace-packager.md)

[<span data-ttu-id="f17a6-128">Comment désinstaller les composants de MED-V</span><span class="sxs-lookup"><span data-stu-id="f17a6-128">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 






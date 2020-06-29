---
title: Comment créer un environnement de test
description: Comment créer un environnement de test
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812264"
---
# <span data-ttu-id="d6d0f-103">Comment créer un environnement de test</span><span class="sxs-lookup"><span data-stu-id="d6d0f-103">How to Create a Test Environment</span></span>


<span data-ttu-id="d6d0f-104">Vous trouverez ci-dessous des étapes et des instructions pour vous aider à créer un environnement de test que vous pouvez utiliser pour tester votre package d’espace de travail MED-V en local avant de le déployer dans l’ensemble de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-104">The following are some steps and instructions to help you create a test environment that you can use to test your MED-V workspace package locally before deploying it throughout your enterprise.</span></span> <span data-ttu-id="d6d0f-105">Cette section fournit des recommandations sur la création d’un environnement de test, que ce soit manuellement ou à l’aide d’un système de distribution de logiciels électronique.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-105">This section provides guidance about how to create a test environment, either manually or by using an electronic software distribution system.</span></span>

**<span data-ttu-id="d6d0f-106">Pour créer un environnement de test en utilisant une ESD</span><span class="sxs-lookup"><span data-stu-id="d6d0f-106">To create a test environment by using an ESD</span></span>**

1.  <span data-ttu-id="d6d0f-107">Utilisez la méthode de déploiement de logiciels au sein de votre entreprise pour déployer les composants nécessaires suivants sur un ordinateur de test.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-107">Use your company’s method of deploying software throughout the enterprise to deploy the following necessary components to a test computer.</span></span> <span data-ttu-id="d6d0f-108">Installez-les dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="d6d0f-108">Install them in the following order:</span></span>

    -   <span data-ttu-id="d6d0f-109">**PC virtuel Windows** , s’il n’est pas déjà installé.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-109">**Windows Virtual PC** – if not already installed.</span></span> <span data-ttu-id="d6d0f-110">Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d6d0f-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="d6d0f-111">**Ajouts et mises à jour pour PC virtuel**, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-111">**Windows Virtual PC Additions and Updates**– if not already installed.</span></span> <span data-ttu-id="d6d0f-112">Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d6d0f-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="d6d0f-113">**Fichier d’installation de l’agent hôte MED-v** : installation de l’agent hôte (med-v \ _HostAgent _setup fichier d’installation).</span><span class="sxs-lookup"><span data-stu-id="d6d0f-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="d6d0f-114">Pour plus d’informations, reportez-vous à la rubrique [installation manuelle de l’agent hôte MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="d6d0f-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    -   <span data-ttu-id="d6d0f-115">**Exécutable du programme d’espace de travail MED-v, VHD et de l’installation,** créé dans le **Gestionnaire de package med-v**</span><span class="sxs-lookup"><span data-stu-id="d6d0f-115">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="d6d0f-116">Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="d6d0f-116">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        <span data-ttu-id="d6d0f-117">**Important**  Le fichier de disque dur virtuel et de configuration doit se trouver dans le même dossier que le programme d’installation de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-117">**Important** The VHD and Setup executable program must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="d6d0f-118">Ensuite, installez le programme d’installation de l’espace de travail MED-V en exécutant setup.exe.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-118">Then, install the MED-V workspace installer by running setup.exe.</span></span>

         

2.  <span data-ttu-id="d6d0f-119">Une fois tous les composants installés sur l’ordinateur de test, exécutez l’agent d’hébergement MED-V pour commencer la première configuration.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-119">After all of the components are installed on the test computer, run the MED-V Host Agent to start first time setup.</span></span>

    <span data-ttu-id="d6d0f-120">Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **ordinateur de bureau Microsoft**, puis sur agent d' **hébergement MED-V**.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-120">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

    <span data-ttu-id="d6d0f-121">**Remarques**  Si vous ne pouvez pas exécuter physiquement l’agent hôte MED-V sur l’ordinateur de test, la première fois que le programme d’installation s’exécute automatiquement au prochain redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-121">**Note** If you cannot physically run the MED-V Host Agent on the test computer, first time setup starts automatically the next time that the computer restarts.</span></span>

     

<span data-ttu-id="d6d0f-122">Le premier démarrage du programme d’installation et peut prendre 10 minutes ou plus pour terminer.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-122">First time setup starts and can take ten minutes or more to finish.</span></span>

<span data-ttu-id="d6d0f-123">Pour plus d’informations sur le test de vos paramètres de configuration lors de la première exécution du programme d’installation, voir vérifier les paramètres de configuration de la [première fois](how-to-verify-first-time-setup-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d6d0f-123">For information about testing your configuration settings when first time setup is running, see [How to Verify First Time Setup Settings](how-to-verify-first-time-setup-settings.md).</span></span>

**<span data-ttu-id="d6d0f-124">Pour créer un environnement de test manuellement</span><span class="sxs-lookup"><span data-stu-id="d6d0f-124">To create a test environment manually</span></span>**

1.  <span data-ttu-id="d6d0f-125">Installez l’agent d’hébergement MED-V dans un environnement de test local incluant des éléments requis pour la fonction MED-V, tels que le PC virtuel Windows, avec des ajouts et des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-125">Install the MED-V Host Agent in a local test environment that includes MED-V prerequisites, such as Windows Virtual PC with additions and updates.</span></span> <span data-ttu-id="d6d0f-126">Pour plus d’informations, reportez-vous à la rubrique [installation manuelle de l’agent hôte MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="d6d0f-126">For information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

2.  <span data-ttu-id="d6d0f-127">Copiez les fichiers de l’espace de travail MED-V dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-127">Copy the MED-V workspace files to your test environment.</span></span> <span data-ttu-id="d6d0f-128">Les fichiers d’espace de travail MED-V se trouvent dans le dossier de destination que vous avez spécifié dans le package de création de package de l' **espace de travail MED-v**.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-128">The MED-V workspace files are located in the destination folder that you specified in the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="d6d0f-129">**Important**  Le fichier de disque dur virtuel et de configuration doit se trouver dans le même dossier de votre environnement de test que le programme d’installation de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-129">**Important** The VHD and Setup executable program must be in the same folder on your test environment as the MED-V workspace installer.</span></span>

     

3.  <span data-ttu-id="d6d0f-130">Installez l’espace de travail MED-V en exécutant setup.exe.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-130">Install the MED-V workspace by running setup.exe.</span></span>

4.  <span data-ttu-id="d6d0f-131">Commencez par configurer pour la première fois en exécutant l’agent hôte MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-131">Start first time setup by running the MED-V Host Agent.</span></span>

    <span data-ttu-id="d6d0f-132">Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **ordinateur de bureau Microsoft**, puis sur agent d' **hébergement MED-V**.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-132">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="d6d0f-133">Le premier démarrage du programme d’installation et peut prendre plusieurs minutes en fonction de la taille du VHD spécifié.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-133">First time setup starts and might take several minutes to complete, depending on the size of the VHD specified.</span></span>

<span data-ttu-id="d6d0f-134">Vous êtes maintenant prêt à tester les différents paramètres de configuration, de publication d’application et de redirection d’URL que vous avez spécifiés pour votre espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-134">You are now ready to test the different settings for configuration, application publishing, and URL redirection that you specified for your MED-V workspace.</span></span>

<span data-ttu-id="d6d0f-135">**Remarques**  Par défaut, MED-V remplace la stratégie de verrouillage de l’écran dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-135">**Note** By default, MED-V overrides the screen lock policy in the guest.</span></span> <span data-ttu-id="d6d0f-136">Toutefois, cela ne pose pas de problème de sécurité, car l’ordinateur hôte continue à respecter la stratégie de verrouillage de l’écran.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-136">However, this does not pose a security problem because the host computer still honors the screen lock policy.</span></span>

 

## <span data-ttu-id="d6d0f-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6d0f-137">Related topics</span></span>


[<span data-ttu-id="d6d0f-138">Comment vérifier les paramètres de première installation</span><span class="sxs-lookup"><span data-stu-id="d6d0f-138">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="d6d0f-139">Comment tester la publication d'applications</span><span class="sxs-lookup"><span data-stu-id="d6d0f-139">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="d6d0f-140">Comment tester la redirection d'URL</span><span class="sxs-lookup"><span data-stu-id="d6d0f-140">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

 

 






---
title: Comment déployer un espace de travail MED-V manuellement
description: Comment déployer un espace de travail MED-V manuellement
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812258"
---
# <span data-ttu-id="8ab80-103">Comment déployer un espace de travail MED-V manuellement</span><span class="sxs-lookup"><span data-stu-id="8ab80-103">How to Deploy a MED-V Workspace Manually</span></span>


<span data-ttu-id="8ab80-104">Dans certains cas, vous voudrez peut-être déployer votre espace de travail MED-V manuellement, par exemple, si votre entreprise n’utilise pas de système électronique de distribution de logiciels pour déployer des applications.</span><span class="sxs-lookup"><span data-stu-id="8ab80-104">In some instances, you might want to deploy your MED-V workspace manually, for example, if your company does not use an electronic software distribution system to deploy applications.</span></span>

<span data-ttu-id="8ab80-105">Cette section fournit des instructions sur le déploiement manuel d’un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="8ab80-105">This section provides instruction about how to manually deploy a MED-V workspace.</span></span>

**<span data-ttu-id="8ab80-106">Pour déploiement manuel d’un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="8ab80-106">To deploy a MED-V workspace manually</span></span>**

1.  <span data-ttu-id="8ab80-107">Copiez toutes les applications prérequises et les fichiers de package d’espace de travail MED-V sur un lecteur partagé ou sur un DVD.</span><span class="sxs-lookup"><span data-stu-id="8ab80-107">Copy all prerequisite applications and the MED-V workspace package files to a shared drive or to a DVD.</span></span> <span data-ttu-id="8ab80-108">Voici la liste des applications et fichiers nécessaires.</span><span class="sxs-lookup"><span data-stu-id="8ab80-108">The following is a list of the required applications and files.</span></span>

    -   <span data-ttu-id="8ab80-109">**PC virtuel Windows**.</span><span class="sxs-lookup"><span data-stu-id="8ab80-109">**Windows Virtual PC**.</span></span> <span data-ttu-id="8ab80-110">Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="8ab80-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="8ab80-111">**Ajouts et mises à jour de l’ordinateur virtuel Windows**.</span><span class="sxs-lookup"><span data-stu-id="8ab80-111">**Windows Virtual PC Additions and Updates**.</span></span> <span data-ttu-id="8ab80-112">Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="8ab80-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="8ab80-113">**Fichier d’installation de l’agent hôte MED-v** : installation de l’agent hôte (med-v \ _HostAgent _setup fichier d’installation).</span><span class="sxs-lookup"><span data-stu-id="8ab80-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span>

        **<span data-ttu-id="8ab80-114">Warning</span><span class="sxs-lookup"><span data-stu-id="8ab80-114">Warning</span></span>**  
        <span data-ttu-id="8ab80-115">Fermez Internet Explorer avant d’installer l’agent d’hébergement MED-V, sinon des conflits peuvent se produire plus tard avec la redirection d’URL.</span><span class="sxs-lookup"><span data-stu-id="8ab80-115">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="8ab80-116">Vous pouvez également le faire en spécifiant un redémarrage de l’ordinateur lors d’une distribution.</span><span class="sxs-lookup"><span data-stu-id="8ab80-116">You can also do this by specifying a computer restart during a distribution.</span></span>



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. <span data-ttu-id="8ab80-117">Installez les éléments suivants dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="8ab80-117">Install the following in the order listed.</span></span> <span data-ttu-id="8ab80-118">L’utilisateur final peut exécuter cette tâche manuellement ou vous pouvez créer un script pour installer les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="8ab80-118">The end user can perform this task manually or you can create a script to install the following:</span></span>

   -   <span data-ttu-id="8ab80-119">Le PC virtuel Windows et les mises à jour et ajouts de PC virtuelles.</span><span class="sxs-lookup"><span data-stu-id="8ab80-119">Windows Virtual PC and the Windows Virtual PC additions and updates.</span></span> <span data-ttu-id="8ab80-120">Un redémarrage de l’ordinateur est requis.</span><span class="sxs-lookup"><span data-stu-id="8ab80-120">A computer restart is required.</span></span>

   -   <span data-ttu-id="8ab80-121">Agent hôte MED-V.</span><span class="sxs-lookup"><span data-stu-id="8ab80-121">The MED-V Host Agent.</span></span>

       **<span data-ttu-id="8ab80-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="8ab80-122">Note</span></span>**  
       <span data-ttu-id="8ab80-123">S’il est en cours d’exécution, Internet Explorer doit être redémarré pour pouvoir terminer l’installation de l’agent hôte MED-V.</span><span class="sxs-lookup"><span data-stu-id="8ab80-123">If it is running, Internet Explorer must be restarted before the installation of the MED-V Host Agent can finish.</span></span>



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. <span data-ttu-id="8ab80-124">Pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="8ab80-124">Complete first time setup.</span></span>

   <span data-ttu-id="8ab80-125">Après l’installation de l’espace de travail MED-V, vous avez la possibilité de démarrer MED-V.</span><span class="sxs-lookup"><span data-stu-id="8ab80-125">After the MED-V workspace is installed, you have the option of starting MED-V.</span></span> <span data-ttu-id="8ab80-126">L’agent hôte MED-V est alors démarré.</span><span class="sxs-lookup"><span data-stu-id="8ab80-126">This starts the MED-V Host Agent.</span></span> <span data-ttu-id="8ab80-127">Vous pouvez démarrer MED-V à ce moment ou démarrer l’agent hôte MED-V plus tard pour terminer la première configuration.</span><span class="sxs-lookup"><span data-stu-id="8ab80-127">You can either start MED-V at that time, or start the MED-V Host Agent later to complete first time setup.</span></span>

   <span data-ttu-id="8ab80-128">Pour démarrer l’agent hôte MED-V, cliquez sur **Démarrer**, sur **tous les programmes**, sur **virtualisation de bureau de Microsoft**, puis sur agent d' **hébergement med-v**.</span><span class="sxs-lookup"><span data-stu-id="8ab80-128">To start the MED-V Host Agent, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

## <span data-ttu-id="8ab80-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ab80-129">Related topics</span></span>


[<span data-ttu-id="8ab80-130">Déploiement d'un espace de travail MED-V via un système de distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="8ab80-130">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="8ab80-131">Comment déployer un espace de travail MED-V dans une image Windows7</span><span class="sxs-lookup"><span data-stu-id="8ab80-131">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[<span data-ttu-id="8ab80-132">Déploiement du package d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="8ab80-132">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)










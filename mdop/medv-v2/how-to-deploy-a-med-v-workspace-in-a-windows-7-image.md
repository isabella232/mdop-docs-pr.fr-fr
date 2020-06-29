---
title: Comment déployer un espace de travail MED-V dans une image Windows7
description: Comment déployer un espace de travail MED-V dans une image Windows7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812263"
---
# <span data-ttu-id="de334-103">Comment déployer un espace de travail MED-V dans une image Windows7</span><span class="sxs-lookup"><span data-stu-id="de334-103">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>


<span data-ttu-id="de334-104">Vous pouvez installer tous les composants MED-V dans une image Windows 7 que vous distribuez au sein de votre entreprise tout comme vous le feriez pour toute nouvelle installation de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="de334-104">You can install all the MED-V components into a Windows 7 image that you distribute throughout your enterprise just as you would any new installation of Windows 7.</span></span> <span data-ttu-id="de334-105">L’utilisateur final termine ensuite l’installation de l’espace de travail MED-V en cliquant sur le raccourci du menu **Démarrer** que vous avez configuré pour démarrer med-v.</span><span class="sxs-lookup"><span data-stu-id="de334-105">The end user then finishes the installation of the MED-V workspace by clicking a **Start** menu shortcut that you configure to start MED-V.</span></span> <span data-ttu-id="de334-106">Le premier démarrage du programme d’installation et l’utilisateur final suivent les instructions pour terminer la configuration.</span><span class="sxs-lookup"><span data-stu-id="de334-106">First time setup starts and the end user follows the instructions to complete the configuration.</span></span>

<span data-ttu-id="de334-107">La section suivante fournit des informations et des instructions pour vous aider à déployer l’espace de travail MED-V au sein de votre entreprise à l’aide d’une image Windows 7.</span><span class="sxs-lookup"><span data-stu-id="de334-107">The following section provides information and instructions to help you deploy the MED-V workspace throughout your enterprise by using a Windows 7 image.</span></span>

**<span data-ttu-id="de334-108">Pour déployer un espace de travail MED-V dans une image Windows 7</span><span class="sxs-lookup"><span data-stu-id="de334-108">To deploy a MED-V workspace in a Windows 7 image</span></span>**

1.  <span data-ttu-id="de334-109">Créer une image standard de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="de334-109">Create a standard image of Windows 7.</span></span> <span data-ttu-id="de334-110">Pour plus d’informations, reportez-vous à [la rubrique Création d’une image standard de Windows 7: Guide détaillé](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .</span><span class="sxs-lookup"><span data-stu-id="de334-110">For more information, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=204843) (https://go.microsoft.com/fwlink/?LinkId=204843).</span></span>

2.  <span data-ttu-id="de334-111">Dans l’image Windows 7, installez le PC virtuel Windows et les mises à jour de PC virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="de334-111">In the Windows 7 image, install Windows Virtual PC and the Windows Virtual PC updates.</span></span> <span data-ttu-id="de334-112">Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="de334-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

3.  <span data-ttu-id="de334-113">Installez l’agent hôte MED-V en utilisant le fichier d’installation MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="de334-113">Install the MED-V Host Agent by using the MED-V\_HostAgent\_Setup installation file.</span></span> <span data-ttu-id="de334-114">Pour plus d’informations, reportez-vous à la rubrique [installation manuelle de l’agent hôte MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="de334-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    <span data-ttu-id="de334-115">**Avertissement**  Internet Explorer doit être fermé avant l’installation de l’agent d’hébergement MED-V, sinon des conflits peuvent se produire plus tard avec la redirection d’URL.</span><span class="sxs-lookup"><span data-stu-id="de334-115">**Warning** Internet Explorer must be closed before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="de334-116">Vous pouvez également le faire en spécifiant un redémarrage de l’ordinateur lors d’une distribution.</span><span class="sxs-lookup"><span data-stu-id="de334-116">You can also do this by specifying a computer restart during a distribution.</span></span>

     

4.  <span data-ttu-id="de334-117">Copiez les fichiers du package d’espace de travail MED-V dans l’image Windows 7.</span><span class="sxs-lookup"><span data-stu-id="de334-117">Copy the MED-V workspace package files to the Windows 7 image.</span></span> <span data-ttu-id="de334-118">Les fichiers de package d’espace de travail MED-V sont le programme d’installation de l’espace de travail MED-V, le fichier. medv et le fichier setup.exe que vous avez créé à l’aide du **Gestionnaire de package med-v**.</span><span class="sxs-lookup"><span data-stu-id="de334-118">The MED-V workspace package files are the MED-V workspace installer, .medv file, and setup.exe file that you created by using the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="de334-119">**Important**  Le fichier. medv et setup.exe doit se trouver dans le même dossier que le programme d’installation de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="de334-119">**Important** The .medv and setup.exe file must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="de334-120">Installez ensuite l’espace de travail MED-V en exécutant setup.exe.</span><span class="sxs-lookup"><span data-stu-id="de334-120">Then, install the MED-V workspace by running setup.exe.</span></span>

     

5.  <span data-ttu-id="de334-121">Configurez un raccourci dans le menu **Démarrer** pour ouvrir l’installation du package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="de334-121">Configure a shortcut on the **Start** menu to open the MED-V workspace package installation.</span></span>

    <span data-ttu-id="de334-122">Créez un raccourci du menu **Démarrer** dans le fichier setup.exe pour permettre à l’utilisateur final de démarrer une installation MED-V selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="de334-122">Create a **Start** menu shortcut to the setup.exe file that lets the end user start a MED-V installation as required.</span></span>

6.  <span data-ttu-id="de334-123">En utilisant le processus de déploiement d’images standard de votre entreprise, vous pouvez distribuer l’image Windows 7 sur les ordinateurs de votre entreprise qui nécessitent MED-V.</span><span class="sxs-lookup"><span data-stu-id="de334-123">By using your company’s standard image deployment process, distribute the Windows 7 image to computers in your enterprise that require MED-V.</span></span>

<span data-ttu-id="de334-124">Lorsque l’utilisateur final doit accéder à une application publiée dans l’espace de travail MED-V, il peut cliquer sur le raccourci du menu **Démarrer** pour installer l’espace de travail MED-v.</span><span class="sxs-lookup"><span data-stu-id="de334-124">When the end user has to access an application published in the MED-V workspace, they can click the **Start** menu shortcut to install the MED-V workspace.</span></span> <span data-ttu-id="de334-125">Ce paramètre démarre automatiquement la première fois et termine la configuration de MED-V.</span><span class="sxs-lookup"><span data-stu-id="de334-125">This automatically starts first time setup and completes the configuration of MED-V.</span></span> <span data-ttu-id="de334-126">Une fois l’installation terminée, l’utilisateur final peut accéder aux applications MED-V dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="de334-126">After first time setup is complete, the end user can access the MED-V applications on the **Start** menu.</span></span>

## <span data-ttu-id="de334-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de334-127">Related topics</span></span>


[<span data-ttu-id="de334-128">Vue d'ensemble du déploiement de MED-V2.0</span><span class="sxs-lookup"><span data-stu-id="de334-128">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="de334-129">Déploiement d'un espace de travail MED-V via un système de distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="de334-129">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 






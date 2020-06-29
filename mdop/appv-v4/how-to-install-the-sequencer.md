---
title: Installation de Sequencer
description: Installation de Sequencer
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807038"
---
# <span data-ttu-id="a0527-103">Installation de Sequencer</span><span class="sxs-lookup"><span data-stu-id="a0527-103">How to Install the Sequencer</span></span>


<span data-ttu-id="a0527-104">Le Sequencer Microsoft Application Virtualization (App-V) vérifie et enregistre le processus d’installation et de configuration pour les applications, afin que l’application puisse être exécutée en tant qu’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a0527-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="a0527-105">Vous devriez installer le Sequencer sur un ordinateur sur lequel seul le système d’exploitation est installé.</span><span class="sxs-lookup"><span data-stu-id="a0527-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="a0527-106">Vous pouvez également installer le Sequencer sur un ordinateur exécutant un environnement virtuel (par exemple, Microsoft Virtual PC).</span><span class="sxs-lookup"><span data-stu-id="a0527-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="a0527-107">Cette méthode est utile, car il est plus facile de mettre à jour un environnement d’séquençage net qui peut être réutilisé avec une configuration supplémentaire minimum.</span><span class="sxs-lookup"><span data-stu-id="a0527-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="a0527-108">Vous devez disposer des droits d’administrateur sur l’ordinateur que vous utilisez pour séquencer l’application et l’ordinateur doit être connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="a0527-108">You must have administrative rights on the computer you are using to sequence the application and the computer must be connected to the network.</span></span> <span data-ttu-id="a0527-109">Il n’est pas nécessaire d’exécuter une version quelconque du client Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="a0527-109">The computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="a0527-110">La création d’une application virtuelle à l’aide du Sequencer est gourmande en ressources; c’est pourquoi il est important d’installer le Sequencer sur un ordinateur qui répond ou dépasse la configuration recommandée.</span><span class="sxs-lookup"><span data-stu-id="a0527-110">Creating a virtual application using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="a0527-111">Pour plus d’informations sur la configuration système requise, voir [Configuration matérielle et logicielle requise](sequencer-hardware-and-software-requirements.md)pour le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a0527-111">For more information about the system requirements, see [Sequencer Hardware and Software Requirements](sequencer-hardware-and-software-requirements.md)..</span></span>

**<span data-ttu-id="a0527-112">Pour installer le Sequencer Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="a0527-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="a0527-113">Copiez les fichiers d’installation de Microsoft Application Virtualization Sequencer sur l’ordinateur sur lequel vous voulez l’installer.</span><span class="sxs-lookup"><span data-stu-id="a0527-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="a0527-114">Pour démarrer l’Assistant Installation de Microsoft Application Virtualization Sequencer, sélectionnez **setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="a0527-114">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="a0527-115">Si le **package redistribuable Microsoft Visual C++ SP1 (x86)** n’est pas détecté avant l’installation, **setup.exe** l’installera.</span><span class="sxs-lookup"><span data-stu-id="a0527-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="a0527-116">Dans la page **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a0527-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="a0527-117">Dans la page **contrat de licence** , pour accepter les conditions du contrat de licence, cliquez sur **J’accepte les conditions du contrat**de licence.</span><span class="sxs-lookup"><span data-stu-id="a0527-117">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="a0527-118">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a0527-118">Click **Next**.</span></span>

5.  <span data-ttu-id="a0527-119">Dans la page **dossier de destination** , pour accepter le dossier d’installation par défaut, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a0527-119">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="a0527-120">Pour spécifier un autre dossier de destination, cliquez sur **modifier** , puis spécifiez le dossier d’installation qui sera utilisé pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="a0527-120">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="a0527-121">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a0527-121">Click **Next**.</span></span>

6.  <span data-ttu-id="a0527-122">Dans la page **êtes-vous prêt à installer le programme** , cliquez sur **installer**pour lancer l’installation.</span><span class="sxs-lookup"><span data-stu-id="a0527-122">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="a0527-123">Dans la page **Assistant InstallShield terminé** , pour fermer l’Assistant Installation et ouvrir le Sequencer, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a0527-123">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="a0527-124">Pour fermer l’Assistant Installation sans ouvrir le Sequencer, désactivez **l’option lancer le programme** , puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a0527-124">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="a0527-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0527-125">Related topics</span></span>


[<span data-ttu-id="a0527-126">Configuration de Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="a0527-126">Configuring the Application Virtualization Sequencer</span></span>](configuring-the-application-virtualization-sequencer.md)

 

 






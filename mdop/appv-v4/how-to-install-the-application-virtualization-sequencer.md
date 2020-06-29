---
title: Procédure pour installer Application Virtualization Sequencer
description: Procédure pour installer Application Virtualization Sequencer
author: dansimp
ms.assetid: 89cdf60d-18b0-4204-aa9f-b402610f8f0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a6fe03f2149504b6c34c70b2b82ce2ba0b55ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807054"
---
# <span data-ttu-id="2a03d-103">Procédure pour installer Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2a03d-103">How to Install the Application Virtualization Sequencer</span></span>


<span data-ttu-id="2a03d-104">Le Sequencer Microsoft Application Virtualization vérifie et enregistre le processus d’installation et de configuration pour les applications, afin que l’application puisse être exécutée en tant qu’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2a03d-104">The Microsoft Application Virtualization Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="2a03d-105">Vous devriez installer le Sequencer sur un ordinateur sur lequel seul le système d’exploitation est installé.</span><span class="sxs-lookup"><span data-stu-id="2a03d-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="2a03d-106">Vous pouvez également installer le Sequencer sur un ordinateur exécutant un environnement virtuel (par exemple, Microsoft Virtual PC).</span><span class="sxs-lookup"><span data-stu-id="2a03d-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="2a03d-107">Cette méthode est utile, car il est plus facile de mettre à jour un environnement d’séquençage net qui peut être réutilisé avec une configuration supplémentaire minimum.</span><span class="sxs-lookup"><span data-stu-id="2a03d-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="2a03d-108">Vous devez disposer des droits d’administrateur sur l’ordinateur que vous utilisez pour séquencer l’application, et l’ordinateur ne doit pas exécuter de version du client App-V.</span><span class="sxs-lookup"><span data-stu-id="2a03d-108">You must have administrative rights on the computer you are using to sequence the application and the computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="2a03d-109">La création d’une application virtuelle à l’aide du Sequencer est gourmande en ressources; c’est pourquoi il est important d’installer le Sequencer sur un ordinateur qui répond ou dépasse la configuration recommandée.</span><span class="sxs-lookup"><span data-stu-id="2a03d-109">Creating a virtual application by using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="2a03d-110">L’exécution du Sequencer App-V en mode sans échec n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2a03d-110">Running the App-V sequencer in Safe Mode is not supported.</span></span> <span data-ttu-id="2a03d-111">Pour plus d’informations sur la configuration système requise, voir [Configuration requise pour le système de virtualisation des applications](application-virtualization-system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2a03d-111">For more information about the system requirements, see [Application Virtualization System Requirements](application-virtualization-system-requirements.md).</span></span>

<span data-ttu-id="2a03d-112">**Important**  Après avoir séquencé une application, vous devez réinstaller le système d’exploitation et le Sequencer de l’ordinateur que vous utilisez pour séquencer les applications avant de procéder à une nouvelle application.</span><span class="sxs-lookup"><span data-stu-id="2a03d-112">**Important** After you have sequenced an application, before you can properly sequence a new application you must reinstall the operating system and the Sequencer on the computer you are using to sequence applications.</span></span>

 

**<span data-ttu-id="2a03d-113">Pour installer le Sequencer Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="2a03d-113">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="2a03d-114">Copiez les fichiers d’installation de Microsoft Application Virtualization Sequencer sur l’ordinateur sur lequel vous voulez l’installer.</span><span class="sxs-lookup"><span data-stu-id="2a03d-114">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="2a03d-115">Pour démarrer l’Assistant Installation de Microsoft Application Virtualization Sequencer, sélectionnez **setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="2a03d-115">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="2a03d-116">Si le **package redistribuable Microsoft Visual C++ SP1 (x86)** n’est pas détecté avant l’installation, **setup.exe** l’installera.</span><span class="sxs-lookup"><span data-stu-id="2a03d-116">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="2a03d-117">Dans la page **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="2a03d-117">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="2a03d-118">Dans la page **contrat de licence** , pour accepter les conditions du contrat de licence, cliquez sur **J’accepte les conditions du contrat**de licence.</span><span class="sxs-lookup"><span data-stu-id="2a03d-118">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="2a03d-119">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2a03d-119">Click **Next**.</span></span>

5.  <span data-ttu-id="2a03d-120">Dans la page **dossier de destination** , pour accepter le dossier d’installation par défaut, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="2a03d-120">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="2a03d-121">Pour spécifier un autre dossier de destination, cliquez sur **modifier** , puis spécifiez le dossier d’installation qui sera utilisé pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="2a03d-121">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="2a03d-122">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2a03d-122">Click **Next**.</span></span>

6.  <span data-ttu-id="2a03d-123">Dans la page **êtes-vous prêt à installer le programme** , cliquez sur **installer**pour lancer l’installation.</span><span class="sxs-lookup"><span data-stu-id="2a03d-123">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="2a03d-124">Dans la page **Assistant InstallShield terminé** , pour fermer l’Assistant Installation et ouvrir le Sequencer, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="2a03d-124">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="2a03d-125">Pour fermer l’Assistant Installation sans ouvrir le Sequencer, désactivez **l’option lancer le programme** , puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="2a03d-125">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="2a03d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a03d-126">Related topics</span></span>


[<span data-ttu-id="2a03d-127">Procédure pour mettre à niveau Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2a03d-127">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

[<span data-ttu-id="2a03d-128">Configuration requise pour le déploiement d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="2a03d-128">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

 

 






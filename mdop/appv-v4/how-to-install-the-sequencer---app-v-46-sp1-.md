---
title: Comment installer le Sequencer (App-V 4,6 SP1)
description: Comment installer le Sequencer (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807041"
---
# <span data-ttu-id="ff1bc-103">Comment installer le Sequencer (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="ff1bc-103">How to Install the Sequencer (App-V 4.6 SP1)</span></span>


<span data-ttu-id="ff1bc-104">Le Sequencer Microsoft Application Virtualization (App-V) vérifie et enregistre le processus d’installation et de configuration pour les applications, afin que l’application puisse être exécutée en tant qu’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="ff1bc-105">Vous devriez installer le Sequencer App-V sur un ordinateur sur lequel seul le système d’exploitation est installé.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-105">You should install the App-V Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="ff1bc-106">Vous pouvez également installer le Sequencer sur un ordinateur exécutant un environnement virtuel (par exemple, un ordinateur virtuel).</span><span class="sxs-lookup"><span data-stu-id="ff1bc-106">Alternatively, you can install the Sequencer on a computer running in a virtual environment, for example, a virtual computer.</span></span> <span data-ttu-id="ff1bc-107">Cette méthode est utile, car il est plus facile de conserver un environnement de séquençage net que vous pouvez réutiliser avec une configuration supplémentaire minimum.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-107">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span>

<span data-ttu-id="ff1bc-108">Vous devez disposer d’informations d’identification d’administrateur sur l’ordinateur que vous utilisez pour séquencer l’application, et l’ordinateur ne doit pas exécuter de version du client App-V.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-108">You must have administrative credentials on the computer you are using to sequence the application, and the computer must not be running any version of App-V client.</span></span> <span data-ttu-id="ff1bc-109">La création d’une application virtuelle à l’aide du Sequencer App-V nécessite plusieurs opérations, donc il est important que vous installiez le Sequencer sur un ordinateur qui répond ou dépasse la [configuration logicielle requise pour la configuration matérielle et logicielle requise](application-virtualization-sequencer-hardware-and-software-requirements.md)pour le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-109">Creating a virtual application by using the App-V Sequencer requires multiple operations, so it is important that you install the Sequencer on a computer that meets or exceeds the [Application Virtualization Sequencer Hardware and Software Requirements](application-virtualization-sequencer-hardware-and-software-requirements.md).</span></span>

**<span data-ttu-id="ff1bc-110">Remarque</span><span class="sxs-lookup"><span data-stu-id="ff1bc-110">Note</span></span>**  
<span data-ttu-id="ff1bc-111">L’exécution du Sequencer App-V en mode sans échec n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-111">Running the App-V sequencer in Safe Mode is not supported.</span></span>



**<span data-ttu-id="ff1bc-112">Pour installer le Sequencer Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ff1bc-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="ff1bc-113">Copiez les fichiers d’installation de Microsoft Application Virtualization Sequencer sur l’ordinateur sur lequel vous voulez l’installer.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer on which you want to install it.</span></span>

2.  <span data-ttu-id="ff1bc-114">Pour démarrer l’Assistant Installation de Microsoft Application Virtualization Sequencer, double-cliquez sur **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-114">To start the Microsoft Application Virtualization Sequencer installation wizard, double-click **Setup.exe**.</span></span> <span data-ttu-id="ff1bc-115">Si le **package redistribuable Microsoft Visual C++ SP1 (x86)** n’est pas détecté avant l’installation, cliquez sur **installer** pour installer la prérequis requise.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, click **Install** to install the required prerequisite.</span></span>

3.  <span data-ttu-id="ff1bc-116">Dans la page **Bienvenue** , cliquez sur **suivant**pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-116">To continue the installation, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="ff1bc-117">Dans la page **contrat de licence** , pour accepter les conditions du contrat de licence, cliquez sur **J’accepte les termes du contrat**de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-117">On the **License Agreement** page, to accept the terms of the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

5.  <span data-ttu-id="ff1bc-118">Dans la page **dossier de destination** , pour accepter le dossier d’installation par défaut, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-118">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="ff1bc-119">Pour spécifier un autre dossier de destination, cliquez sur **modifier** , puis spécifiez le dossier d’installation qui sera utilisé pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-119">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="ff1bc-120">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-120">Click **Next**.</span></span>

6.  <span data-ttu-id="ff1bc-121">Sur la page **lecteur virtuel** , pour configurer le lecteur par défaut de la virtualisation d’application **Q:\\** (par défaut) le lecteur d’exécution des applications séquencées, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-121">On the **Virtual Drive** page, to configure the Application Virtualization default drive **Q:\\** (default) as the drive that all sequenced applications will run from, click **Next**.</span></span> <span data-ttu-id="ff1bc-122">Si vous voulez spécifier une autre lettre de lecteur, sélectionnez la lettre de lecteur de votre choix dans la liste, puis cliquez sur **Next (suivant**).</span><span class="sxs-lookup"><span data-stu-id="ff1bc-122">If you want to specify a different drive letter, use the list and select the drive letter that you want to use by selecting the appropriate drive letter, and then click **Next**.</span></span>

    **<span data-ttu-id="ff1bc-123">Important</span><span class="sxs-lookup"><span data-stu-id="ff1bc-123">Important</span></span>**  
    <span data-ttu-id="ff1bc-124">La lettre du lecteur de virtualisation des applications spécifiée avec cette étape est la lettre du lecteur à partir de laquelle les applications virtuelles seront exécutées sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-124">The Application Virtualization drive letter specified with this step is the drive letter that virtual applications will be run from on target computers.</span></span> <span data-ttu-id="ff1bc-125">La lettre de lecteur spécifiée doit être disponible et non actuellement utilisée sur les ordinateurs exécutant le client App-V.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-125">The drive letter specified must be available, and not currently in use on the computers running the App-V client.</span></span> <span data-ttu-id="ff1bc-126">Si le lecteur spécifié est déjà utilisé, l’application virtuelle échoue sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-126">If the specified drive is already in use, the virtual application fails on the target computer.</span></span>



7.  <span data-ttu-id="ff1bc-127">Dans la page **êtes-vous prêt à installer le programme** , cliquez sur **installer**pour lancer l’installation.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-127">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

8.  <span data-ttu-id="ff1bc-128">Dans la page **Assistant InstallShield terminé** , pour fermer l’Assistant Installation et ouvrir le Sequencer App-V, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-128">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the App-V Sequencer, click **Finish**.</span></span> <span data-ttu-id="ff1bc-129">Pour fermer l’Assistant Installation sans ouvrir le Sequencer, désactivez **lancer le programme**, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-129">To close the installation wizard without opening the Sequencer, clear **Launch the program**, and then click **Finish**.</span></span>

    **<span data-ttu-id="ff1bc-130">Remarque</span><span class="sxs-lookup"><span data-stu-id="ff1bc-130">Note</span></span>**  
    <span data-ttu-id="ff1bc-131">Si vous avez installé le Sequencer App-V sur un ordinateur exécutant un environnement virtuel (par exemple, une machine virtuelle), vous devez prendre une photo.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-131">If you installed the App-V Sequencer on a computer running a virtual environment, for example a virtual machine, you must now take a snapshot.</span></span> <span data-ttu-id="ff1bc-132">Après avoir séquencé une application, vous pouvez revenir à cette image pour effectuer une séquence de l’application suivante.</span><span class="sxs-lookup"><span data-stu-id="ff1bc-132">After you sequence an application, you can revert to this image, so you can sequence the next application.</span></span>



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## <span data-ttu-id="ff1bc-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff1bc-133">Related topics</span></span>


[<span data-ttu-id="ff1bc-134">Configuration d'Application Virtualization Sequencer (App-V4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="ff1bc-134">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)










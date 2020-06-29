---
title: Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT
description: Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810151"
---
# <span data-ttu-id="c11a6-103">Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="c11a6-103">How to Recover Local Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="c11a6-104">Pour récupérer un ordinateur local à l’aide de Microsoft Diagnostics et Recovery Tools Tools (DaRT) 7, vous devez avoir une présentation physique de l’ordinateur de l’utilisateur final rencontrant des problèmes qui nécessitent DaRT.</span><span class="sxs-lookup"><span data-stu-id="c11a6-104">To recover a local computer by using Microsoft Diagnostics and Recovery Toolset (DaRT) 7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span> <span data-ttu-id="c11a6-105">Vous pouvez également exécuter DaRT à distance en suivant les instructions de la [procédure de récupération d’ordinateurs distants à l’aide de l’image de récupération DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="c11a6-105">You can also run DaRT remotely by following the instructions at [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

**<span data-ttu-id="c11a6-106">Pour récupérer un ordinateur local à l’aide de DaRT</span><span class="sxs-lookup"><span data-stu-id="c11a6-106">To recover a local computer by using DaRT</span></span>**

1.  <span data-ttu-id="c11a6-107">Au démarrage de l’ordinateur dans l’image de récupération DaRT, la boîte de dialogue **netstart** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c11a6-107">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="c11a6-108">Vous êtes invité à indiquer si vous souhaitez initialiser les services réseau.</span><span class="sxs-lookup"><span data-stu-id="c11a6-108">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="c11a6-109">Si vous cliquez sur **Oui**, on suppose qu’un serveur DHCP est présent sur le réseau et qu’une tentative d’obtention d’une adresse IP du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c11a6-109">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="c11a6-110">Si le réseau utilise des adresses IP statiques au lieu de DHCP, vous pouvez utiliser l’outil de **configuration TCP/IP** dans DART pour spécifier une adresse IP statique.</span><span class="sxs-lookup"><span data-stu-id="c11a6-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="c11a6-111">Pour ignorer le processus d’initialisation du réseau, cliquez sur **non**.</span><span class="sxs-lookup"><span data-stu-id="c11a6-111">To skip the network initialization process, click **No**.</span></span>

2.  <span data-ttu-id="c11a6-112">Après la boîte de dialogue initialisation du réseau, vous êtes invité à indiquer si vous souhaitez remapper les lettres de lecteur.</span><span class="sxs-lookup"><span data-stu-id="c11a6-112">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="c11a6-113">Lorsque vous exécutez Windows en ligne, le volume système est généralement mappé au lecteur C. Toutefois, lorsque vous exécutez Windows Offline sous WinRE, le volume système d’origine peut être mappé sur un autre lecteur, ce qui peut entraîner une confusion.</span><span class="sxs-lookup"><span data-stu-id="c11a6-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="c11a6-114">Si vous décidez de remapper, DaRT tente de mapper les lettres du lecteur hors ligne pour correspondre aux lettres de lecteur en ligne.</span><span class="sxs-lookup"><span data-stu-id="c11a6-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="c11a6-115">Le remappage est effectué uniquement si un système d’exploitation hors connexion est sélectionné plus tard dans le processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="c11a6-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

3.  <span data-ttu-id="c11a6-116">Après la boîte de dialogue remappage, une boîte de dialogue **options de récupération du système** s’affiche et vous invite à sélectionner une disposition de clavier.</span><span class="sxs-lookup"><span data-stu-id="c11a6-116">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="c11a6-117">Il affiche ensuite le répertoire racine du système, le type de système d’exploitation installé et la taille de partition.</span><span class="sxs-lookup"><span data-stu-id="c11a6-117">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="c11a6-118">Si vous ne voyez pas votre système d’exploitation et que vous suspectez qu’il n’y a pas de problème, cliquez sur **charger des pilotes** pour charger les pilotes suspects.</span><span class="sxs-lookup"><span data-stu-id="c11a6-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="c11a6-119">Vous êtes alors invité à insérer le média d’installation pour l’appareil et à sélectionner le pilote.</span><span class="sxs-lookup"><span data-stu-id="c11a6-119">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="c11a6-120">Sélectionnez l’installation que vous voulez réparer ou diagnostiquer, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c11a6-120">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="c11a6-121">Remarque</span><span class="sxs-lookup"><span data-stu-id="c11a6-121">Note</span></span>**  
    <span data-ttu-id="c11a6-122">Si l’environnement de récupération Windows (WinRE) détecte ou suspecte que Windows 7 ne démarrait pas correctement la dernière fois qu’il a été essayé, la **réparation du démarrage** peut commencer à s’exécuter automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c11a6-122">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. <span data-ttu-id="c11a6-123">Dans la fenêtre **options de récupération du système** , cliquez sur outils de **Diagnostics et de récupération Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="c11a6-123">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="c11a6-124">La fenêtre du **jeu d’outils de diagnostics et de récupération** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="c11a6-124">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="c11a6-125">Vous pouvez désormais exécuter tous les outils ou assistants proposés lors de la création de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="c11a6-125">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="c11a6-126">Vous pouvez cliquer sur **aide** dans la fenêtre **jeu d’outils de diagnostics et de récupération** pour ouvrir le fichier d’aide du client qui fournit des instructions détaillées et des informations nécessaires à l’exécution des outils DART individuels.</span><span class="sxs-lookup"><span data-stu-id="c11a6-126">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="c11a6-127">Vous pouvez également cliquer sur l' **Assistant solution** dans la fenêtre **jeu d’outils de diagnostics et de récupération** pour choisir l’outil le plus approprié pour la situation, en fonction d’un bref entretien que l’Assistant fournit.</span><span class="sxs-lookup"><span data-stu-id="c11a6-127">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="c11a6-128">Pour obtenir des informations générales sur l’un des outils DaRT, voir [vue d’ensemble des outils dans DaRT 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="c11a6-128">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

**<span data-ttu-id="c11a6-129">Pour exécuter DaRT à l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="c11a6-129">To run DaRT at the command prompt</span></span>**

1. <span data-ttu-id="c11a6-130">Vous pouvez exécuter DaRT à l’invite de commandes en spécifiant la commande **netstart.exe** et en utilisant l’un des paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c11a6-130">You can run DaRT at the command prompt by specifying the **netstart.exe** command and by using any of the following parameters:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="c11a6-131">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c11a6-131">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="c11a6-132">Description</span><span class="sxs-lookup"><span data-stu-id="c11a6-132">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="c11a6-133">-réseau</span><span class="sxs-lookup"><span data-stu-id="c11a6-133">-network</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c11a6-134">Initialise les services réseau.</span><span class="sxs-lookup"><span data-stu-id="c11a6-134">Initializes the network services.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="c11a6-135">-remonter</span><span class="sxs-lookup"><span data-stu-id="c11a6-135">-remount</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c11a6-136">Remappez les lettres de lecteur.</span><span class="sxs-lookup"><span data-stu-id="c11a6-136">Remaps the drive letters.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="c11a6-137">-invite</span><span class="sxs-lookup"><span data-stu-id="c11a6-137">-prompt</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c11a6-138">Affiche des messages demandant à l’utilisateur final de spécifier si le réseau doit être initialisé et remapper les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="c11a6-138">Displays messages asking the end user to specify whether to initialize the network and remap the drives.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="c11a6-139">Important</span><span class="sxs-lookup"><span data-stu-id="c11a6-139">Important</span></span></strong><br/><p><span data-ttu-id="c11a6-140">La réponse de l’utilisateur final aux invites remplace les commutateurs-réseau et-remontage.</span><span class="sxs-lookup"><span data-stu-id="c11a6-140">The end user’s response to the prompts overrides the -network and -remount switches.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="c11a6-141">Vous pouvez personnaliser DaRT de telle sorte qu’un ordinateur qui démarre sur DaRT ouvre automatiquement l’outil de **connexion à distance** qui est utilisé pour établir une connexion à distance avec l’assistance.</span><span class="sxs-lookup"><span data-stu-id="c11a6-141">You can customize DaRT so that a computer that boots into DaRT automatically opens the **Remote Connection** tool that is used to establish a remote connection with the help desk.</span></span>

## <span data-ttu-id="c11a6-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c11a6-142">Related topics</span></span>


[<span data-ttu-id="c11a6-143">Récupération des ordinateurs à l'aide de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="c11a6-143">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)










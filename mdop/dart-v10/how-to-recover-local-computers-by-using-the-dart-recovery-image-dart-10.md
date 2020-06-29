---
title: Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT
description: Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT
author: dansimp
ms.assetid: a6adc717-827c-45e8-b9c3-06d0e919e0bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06e8ad82f869568c9fa25fcbb16825b2abff06f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809444"
---
# <span data-ttu-id="9954d-103">Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="9954d-103">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="9954d-104">Utilisez ces instructions pour récupérer un ordinateur en cours de présentation physique sur l’ordinateur de l’utilisateur final qui rencontre des problèmes.</span><span class="sxs-lookup"><span data-stu-id="9954d-104">Use these instructions to recover a computer when you are physically present at the end-user computer that is experiencing problems.</span></span>

**<span data-ttu-id="9954d-105">Récupération d’un ordinateur local à l’aide de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="9954d-105">How to recover a local computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="9954d-106">Démarrez l’ordinateur de l’utilisateur final à l’aide de l’image de récupération Microsoft Diagnostics and Recovery Tools (DaRT) 10.</span><span class="sxs-lookup"><span data-stu-id="9954d-106">Boot the end-user computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

    <span data-ttu-id="9954d-107">Au démarrage de l’ordinateur dans l’image de récupération de DaRT 10, la boîte de dialogue de **démarrage** automatique s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9954d-107">As the computer is booting into the DaRT 10 recovery image, the **NetStart** dialog box appears.</span></span>

2.  <span data-ttu-id="9954d-108">Lorsque le système vous demande si vous souhaitez initialiser les services réseau, sélectionnez l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="9954d-108">When you are asked whether you want to initialize network services, select one of the following:</span></span>

    <span data-ttu-id="9954d-109">**Oui** -il est supposé qu’un serveur DHCP est présent sur le réseau et une tentative d’obtention d’une adresse IP du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="9954d-109">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="9954d-110">Si le réseau utilise des adresses IP statiques au lieu de DHCP, vous pouvez utiliser l’outil de **configuration TCP/IP** dans DART pour spécifier une adresse IP statique.</span><span class="sxs-lookup"><span data-stu-id="9954d-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="9954d-111">**Non** -ignorer le processus d’initialisation du réseau.</span><span class="sxs-lookup"><span data-stu-id="9954d-111">**No** - skip the network initialization process.</span></span>

3.  <span data-ttu-id="9954d-112">Indiquez si vous souhaitez remapper les lettres de lecteur.</span><span class="sxs-lookup"><span data-stu-id="9954d-112">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="9954d-113">Lorsque vous exécutez Windows en ligne, le volume système est généralement mappé au lecteur C. Toutefois, lorsque vous exécutez Windows Offline sous WinRE, le volume système d’origine peut être mappé sur un autre lecteur, ce qui peut entraîner une confusion.</span><span class="sxs-lookup"><span data-stu-id="9954d-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="9954d-114">Si vous décidez de remapper, DaRT tente de mapper les lettres du lecteur hors ligne pour correspondre aux lettres de lecteur en ligne.</span><span class="sxs-lookup"><span data-stu-id="9954d-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="9954d-115">Le remappage est effectué uniquement si un système d’exploitation hors connexion est sélectionné plus tard dans le processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="9954d-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="9954d-116">Dans la boîte de dialogue **options de récupération du système** , sélectionnez une disposition de clavier.</span><span class="sxs-lookup"><span data-stu-id="9954d-116">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5.  <span data-ttu-id="9954d-117">Vérifiez le répertoire racine du système affiché, le type de système d’exploitation installé et la taille de partition.</span><span class="sxs-lookup"><span data-stu-id="9954d-117">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="9954d-118">Si vous ne voyez pas votre système d’exploitation et suspectez l’absence de pilotes dans le cas contraire, cliquez sur **charger les pilotes** pour charger les pilotes suspects, puis insérez le support d’installation de l’appareil et sélectionnez le pilote.</span><span class="sxs-lookup"><span data-stu-id="9954d-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6.  <span data-ttu-id="9954d-119">Sélectionnez l’installation que vous voulez réparer ou diagnostiquer, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9954d-119">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="9954d-120">Remarque</span><span class="sxs-lookup"><span data-stu-id="9954d-120">Note</span></span>**  
    <span data-ttu-id="9954d-121">Si l’environnement de récupération Windows (WinRE) détecte un problème ou s’il suspect qu’il n’a pas démarré correctement le dernier **démarrage** de Windows 10, il est possible qu’il s’exécute automatiquement.</span><span class="sxs-lookup"><span data-stu-id="9954d-121">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="9954d-122">Dans la fenêtre **options de récupération du système** , cliquez sur outils de **Diagnostics et de récupération Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="9954d-122">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="9954d-123">La fenêtre du **jeu d’outils de diagnostics et de récupération** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="9954d-123">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="9954d-124">Vous pouvez désormais exécuter tous les outils ou assistants proposés lors de la création de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="9954d-124">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="9954d-125">Vous pouvez cliquer sur **aide** dans la fenêtre **jeu d’outils de diagnostics et de récupération** pour ouvrir le fichier d’aide du client qui fournit des instructions détaillées et des informations nécessaires à l’exécution des outils DART individuels.</span><span class="sxs-lookup"><span data-stu-id="9954d-125">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="9954d-126">Vous pouvez également cliquer sur l' **Assistant solution** dans la fenêtre **jeu d’outils de diagnostics et de récupération** pour choisir l’outil le plus approprié pour la situation, en fonction d’un bref entretien que l’Assistant fournit.</span><span class="sxs-lookup"><span data-stu-id="9954d-126">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="9954d-127">Pour obtenir des informations générales sur l’un des outils DaRT, voir [vue d’ensemble des outils dans DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="9954d-127">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

**<span data-ttu-id="9954d-128">Exécution de DaRT à l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="9954d-128">How to run DaRT at the command prompt</span></span>**

- <span data-ttu-id="9954d-129">Pour exécuter DaRT à l’invite de commandes, spécifiez la commande **netstart.exe** puis utilisez l’un des paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="9954d-129">To run DaRT at the command prompt, specify the **netstart.exe** command then use any of the following parameters:</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong><span data-ttu-id="9954d-130">Paramètre</span><span class="sxs-lookup"><span data-stu-id="9954d-130">Parameter</span></span></strong></p></td>
  <td align="left"><p><strong><span data-ttu-id="9954d-131">Description</span><span class="sxs-lookup"><span data-stu-id="9954d-131">Description</span></span></strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="9954d-132">-réseau</span><span class="sxs-lookup"><span data-stu-id="9954d-132">-network</span></span></p></td>
  <td align="left"><p><span data-ttu-id="9954d-133">Initialise les services réseau.</span><span class="sxs-lookup"><span data-stu-id="9954d-133">Initializes the network services.</span></span></p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="9954d-134">-remonter</span><span class="sxs-lookup"><span data-stu-id="9954d-134">-remount</span></span></p></td>
  <td align="left"><p><span data-ttu-id="9954d-135">Remappez les lettres de lecteur.</span><span class="sxs-lookup"><span data-stu-id="9954d-135">Remaps the drive letters.</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="9954d-136">-invite</span><span class="sxs-lookup"><span data-stu-id="9954d-136">-prompt</span></span></p></td>
  <td align="left"><p><span data-ttu-id="9954d-137">Affiche des messages demandant à l’utilisateur final de spécifier si le réseau doit être initialisé et remapper les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="9954d-137">Displays messages that ask the end user to specify whether to initialize the network and remap the drives.</span></span></p>
  <div class="alert">
  <strong><span data-ttu-id="9954d-138">Warning</span><span class="sxs-lookup"><span data-stu-id="9954d-138">Warning</span></span></strong><br/><p><span data-ttu-id="9954d-139">La réponse de l’utilisateur final à l’invite a pour effet de remplacer les commutateurs-Network et – remount.</span><span class="sxs-lookup"><span data-stu-id="9954d-139">The end user’s response to the prompt overrides the –network and –remount switches.</span></span></p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## <span data-ttu-id="9954d-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9954d-140">Related topics</span></span>


[<span data-ttu-id="9954d-141">Opérations de DaRT10</span><span class="sxs-lookup"><span data-stu-id="9954d-141">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="9954d-142">Récupération des ordinateurs à l'aide de DaRT10</span><span class="sxs-lookup"><span data-stu-id="9954d-142">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)










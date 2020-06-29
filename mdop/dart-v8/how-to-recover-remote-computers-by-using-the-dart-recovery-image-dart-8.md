---
title: Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT
description: Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT
author: dansimp
ms.assetid: 363ccd48-6820-4b5b-a43a-323c0b208a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b3e3155dbea8da18338b8a167d22f73b1c8e4bb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810530"
---
# <span data-ttu-id="04042-103">Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="04042-103">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="04042-104">Utilisez la fonctionnalité de connexion à distance dans Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 pour exécuter les outils DaRT à distance sur un ordinateur d’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="04042-104">Use the Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 to run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="04042-105">Lorsque l’utilisateur final fournit à l’administrateur ou au service de support technique des informations spécifiques, l’administrateur informatique ou le service de support technique peut prendre le contrôle de l’ordinateur de l’utilisateur final et exécuter les outils DaRT nécessaires à distance.</span><span class="sxs-lookup"><span data-stu-id="04042-105">After the end user provides the administrator or help desk worker with certain information, the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="04042-106">Si vous avez désactivé les outils DaRT lors de la création de l’image de récupération, vous avez toujours accès à tous les outils.</span><span class="sxs-lookup"><span data-stu-id="04042-106">If you disabled the DaRT tools when you created the recovery image, you still have access to all of the tools.</span></span> <span data-ttu-id="04042-107">L’ensemble des outils, à l’exception de la connexion à distance, ne sont pas disponibles pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="04042-107">All of the tools, except Remote Connection, are unavailable to end users.</span></span>

**<span data-ttu-id="04042-108">Pour récupérer un ordinateur distant à l’aide de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="04042-108">To recover a remote computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="04042-109">Démarrez un ordinateur utilisateur final en utilisant l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="04042-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="04042-110">En règle générale, vous devez utiliser l’une des méthodes suivantes pour démarrer dans DaRT afin de récupérer un ordinateur distant, selon la manière dont vous déployez l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="04042-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="04042-111">Pour plus d’informations sur le déploiement de l’image de récupération DaRT, voir [déploiement de dart 8,0](deploying-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="04042-111">For more information about deploying the DaRT recovery image, see [Deploying DaRT 8.0](deploying-dart-80-dart-8.md).</span></span>

    -   <span data-ttu-id="04042-112">Démarrez dans DaRT à partir d’une partition de récupération sur l’ordinateur qui pose problème.</span><span class="sxs-lookup"><span data-stu-id="04042-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="04042-113">Démarrez dans DaRT à partir d’une partition distante sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="04042-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="04042-114">Pour plus d’informations sur les avantages et inconvénients de chaque méthode, voir [planification de l’enregistrement et du déploiement de l’image de récupération 8,0 de DART](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="04042-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

    <span data-ttu-id="04042-115">Quelle que soit la méthode que vous utilisez pour démarrer dans DaRT, vous devez activer le périphérique de démarrage dans le BIOS pour l’option de démarrage ou les options que vous voulez mettre à disposition de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="04042-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="04042-116">Remarque</span><span class="sxs-lookup"><span data-stu-id="04042-116">Note</span></span>**  
    <span data-ttu-id="04042-117">La configuration du BIOS est unique, en fonction du type de disque dur, de cartes réseau et d’autres éléments utilisés au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="04042-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. <span data-ttu-id="04042-118">Lorsque le système vous demande si vous souhaitez initialiser les services réseau, sélectionnez l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="04042-118">When you are asked whether you want to initialize network services, select one of the following:</span></span>

   <span data-ttu-id="04042-119">**Oui** -il est supposé qu’un serveur DHCP est présent sur le réseau et une tentative d’obtention d’une adresse IP du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="04042-119">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="04042-120">Si le réseau utilise des adresses IP statiques au lieu de DHCP, vous pouvez utiliser l’outil de **configuration TCP/IP** dans DART pour spécifier une adresse IP statique.</span><span class="sxs-lookup"><span data-stu-id="04042-120">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

   <span data-ttu-id="04042-121">**Non** -ignorer le processus d’initialisation du réseau.</span><span class="sxs-lookup"><span data-stu-id="04042-121">**No** - skip the network initialization process.</span></span>

3. <span data-ttu-id="04042-122">Indiquez si vous souhaitez remapper les lettres de lecteur.</span><span class="sxs-lookup"><span data-stu-id="04042-122">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="04042-123">Lorsque vous exécutez Windows en ligne, le volume système est généralement mappé au lecteur C. Toutefois, lorsque vous exécutez Windows Offline sous WinRE, le volume système d’origine peut être mappé sur un autre lecteur, ce qui peut entraîner une confusion.</span><span class="sxs-lookup"><span data-stu-id="04042-123">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="04042-124">Si vous décidez de remapper, DaRT tente de mapper les lettres du lecteur hors ligne pour correspondre aux lettres de lecteur en ligne.</span><span class="sxs-lookup"><span data-stu-id="04042-124">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="04042-125">Le remappage est effectué uniquement si un système d’exploitation hors connexion est sélectionné plus tard dans le processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="04042-125">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4. <span data-ttu-id="04042-126">Dans la boîte de dialogue **options de récupération du système** , sélectionnez une disposition de clavier.</span><span class="sxs-lookup"><span data-stu-id="04042-126">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5. <span data-ttu-id="04042-127">Vérifiez le répertoire racine du système affiché, le type de système d’exploitation installé et la taille de partition.</span><span class="sxs-lookup"><span data-stu-id="04042-127">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="04042-128">Si vous ne voyez pas votre système d’exploitation et suspectez l’absence de pilotes dans le cas contraire, cliquez sur **charger les pilotes** pour charger les pilotes suspects, puis insérez le support d’installation de l’appareil et sélectionnez le pilote.</span><span class="sxs-lookup"><span data-stu-id="04042-128">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6. <span data-ttu-id="04042-129">Sélectionnez l’installation que vous voulez réparer ou diagnostiquer, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="04042-129">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

   **<span data-ttu-id="04042-130">Remarque</span><span class="sxs-lookup"><span data-stu-id="04042-130">Note</span></span>**  
   <span data-ttu-id="04042-131">Si l’environnement de récupération Windows (WinRE) détecte un problème ou s’il suspect que Windows 8 ne démarrait pas correctement la dernière fois qu’il a été essayé, l' **outil de réparation du démarrage** peut commencer à s’exécuter automatiquement.</span><span class="sxs-lookup"><span data-stu-id="04042-131">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 8 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="04042-132">Pour plus d’informations sur la façon de résoudre ce problème, reportez-vous à la rubrique [résolution des problèmes DaRT 8,0](troubleshooting-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="04042-132">For information about how to resolve this issue, see [Troubleshooting DaRT 8.0](troubleshooting-dart-80-dart-8.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="04042-133">Dans la fenêtre **options de récupération du système** , cliquez sur outils de **Diagnostics et de récupération Microsoft** pour ouvrir les **outils de diagnostics et de récupération**.</span><span class="sxs-lookup"><span data-stu-id="04042-133">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset**.</span></span>

8. <span data-ttu-id="04042-134">Dans la fenêtre **jeu d’outils de diagnostics et de récupération** , cliquez sur **connexion à distance** pour ouvrir la fenêtre de **connexion à distance DART** .</span><span class="sxs-lookup"><span data-stu-id="04042-134">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="04042-135">Si vous êtes invité à fournir l’accès distant au support technique, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="04042-135">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="04042-136">La fenêtre de connexion à distance DaRT s’ouvre et affiche un numéro de ticket, une adresse IP et des informations de port.</span><span class="sxs-lookup"><span data-stu-id="04042-136">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

9. <span data-ttu-id="04042-137">Sur l’ordinateur du support technique, ouvrez la **visionneuse de connexion à distance DART**.</span><span class="sxs-lookup"><span data-stu-id="04042-137">On the help desk computer, open the **DaRT Remote Connection Viewer**.</span></span>

10. <span data-ttu-id="04042-138">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft DART 8,0**, puis sur **visionneuse de connexions à distance DART**.</span><span class="sxs-lookup"><span data-stu-id="04042-138">Click **Start**, click **All Programs**, click **Microsoft DaRT 8.0**, and then click **DaRT Remote Connection Viewer**.</span></span>

11. <span data-ttu-id="04042-139">Dans la fenêtre de **connexion à distance de DART** , entrez les informations requises sur le ticket, l’adresse IP et le port.</span><span class="sxs-lookup"><span data-stu-id="04042-139">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="04042-140">Remarque</span><span class="sxs-lookup"><span data-stu-id="04042-140">Note</span></span>**  
   <span data-ttu-id="04042-141">Ces informations sont créées sur l’ordinateur de l’utilisateur final et doivent être fournies par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="04042-141">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="04042-142">Plusieurs adresses IP peuvent être proposées, en fonction du nombre de personnes disponibles sur l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="04042-142">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



12. <span data-ttu-id="04042-143">Cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="04042-143">Click **Connect**.</span></span>

<span data-ttu-id="04042-144">L’administrateur informatique suppose désormais le contrôle de l’ordinateur de l’utilisateur final et peut exécuter les outils DaRT à distance.</span><span class="sxs-lookup"><span data-stu-id="04042-144">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="04042-145">Remarque</span><span class="sxs-lookup"><span data-stu-id="04042-145">Note</span></span>**  
<span data-ttu-id="04042-146">Un fichier nommé inv32.xml contient des informations de connexion distantes, telles que le numéro de port et l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="04042-146">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="04042-147">Par défaut, le fichier se trouve généralement sur%windir%\\system32.</span><span class="sxs-lookup"><span data-stu-id="04042-147">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="04042-148">Pour personnaliser le processus de connexion à distance</span><span class="sxs-lookup"><span data-stu-id="04042-148">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="04042-149">Vous pouvez personnaliser le processus de connexion à distance en modifiant le fichier winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="04042-149">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="04042-150">Pour plus d’informations sur la modification du fichier winpeshl.ini, voir [Winpeshl.ini de fichiers](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="04042-150">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="04042-151">Spécifiez les commandes et les paramètres suivants pour personnaliser l’établissement d’une connexion distante avec un ordinateur d’utilisateur final:</span><span class="sxs-lookup"><span data-stu-id="04042-151">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="04042-152">Commande</span><span class="sxs-lookup"><span data-stu-id="04042-152">Command</span></span></th>
   <th align="left"><span data-ttu-id="04042-153">Paramètre</span><span class="sxs-lookup"><span data-stu-id="04042-153">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="04042-154">Description</span><span class="sxs-lookup"><span data-stu-id="04042-154">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="04042-155">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="04042-155">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="04042-156">-nomessage</span><span class="sxs-lookup"><span data-stu-id="04042-156">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="04042-157">Spécifie que l’invite de confirmation ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="04042-157">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="04042-158">La connexion à distance </strong> continue comme si l’utilisateur final avait répondu &quot; Oui &quot; à l’invite de confirmation.</span><span class="sxs-lookup"><span data-stu-id="04042-158">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="04042-159">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="04042-159">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="04042-160">aucune</span><span class="sxs-lookup"><span data-stu-id="04042-160">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="04042-161">Empêche la poursuite d’un script personnalisé tant que <strong> la connexion à distance n' </strong> est pas en cours d’exécution ou qu’une connexion valide est établie avec l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="04042-161">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="04042-162">Important</span><span class="sxs-lookup"><span data-stu-id="04042-162">Important</span></span></strong><br/><p><span data-ttu-id="04042-163">Cette commande n’utilise aucune fonction si elle est spécifiée de manière indépendante.</span><span class="sxs-lookup"><span data-stu-id="04042-163">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="04042-164">Il doit être spécifié dans un script pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="04042-164">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="04042-165">Voici un exemple de fichier winpeshl.ini personnalisé pour ouvrir l’outil de **connexion à distance** dès qu’une tentative de démarrage dans DART est lancée:</span><span class="sxs-lookup"><span data-stu-id="04042-165">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

<span data-ttu-id="04042-166">Lorsque DaRT démarre, il crée le fichier inv32.xml dans \\Windows\\System32\\ sur le disque RAM.</span><span class="sxs-lookup"><span data-stu-id="04042-166">When DaRT starts, it creates the file inv32.xml in \\Windows\\System32\\ on the RAM disk.</span></span> <span data-ttu-id="04042-167">Ce fichier contient des informations de connexion: adresse IP, port et numéro de ticket.</span><span class="sxs-lookup"><span data-stu-id="04042-167">This file contains connection information: IP address, port, and ticket number.</span></span> <span data-ttu-id="04042-168">Vous pouvez copier ce fichier sur un partage réseau pour déclencher un flux de travail de support technique.</span><span class="sxs-lookup"><span data-stu-id="04042-168">You can copy this file to a network share to trigger a Help desk workflow.</span></span> <span data-ttu-id="04042-169">Par exemple, un programme personnalisé peut vérifier le partage réseau pour les fichiers de connexion, puis créer un ticket de support ou envoyer des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="04042-169">For example, a custom program can check the network share for connection files, and then create a support ticket or send email notifications.</span></span>

**<span data-ttu-id="04042-170">Pour exécuter la visionneuse de connexions à distance à l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="04042-170">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="04042-171">Pour exécuter la **visionneuse de connexions à distance DART** à l’invite de commandes, spécifiez la commande **DartRemoteViewer.exe** et utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="04042-171">To run the **DaRT Remote Connection Viewer** at the command prompt, specify the **DartRemoteViewer.exe** command and use the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="04042-172">Paramètre</span><span class="sxs-lookup"><span data-stu-id="04042-172">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="04042-173">Description</span><span class="sxs-lookup"><span data-stu-id="04042-173">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="04042-174">-ticket = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="04042-174">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="04042-175">Où &lt; <em> ticketnumber </em> &gt; correspond au numéro de ticket, y compris aux tirets, qui est généré par la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="04042-175">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="04042-176">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="04042-176">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="04042-177">Où &lt; <em> IPAddress </em> &gt; est l’adresse IP générée par la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="04042-177">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="04042-178">-port = &lt; <em> port</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="04042-178">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="04042-179">Où &lt; <em> port </em> &gt; correspond au port qui correspond à l’adresse IP spécifiée.</span><span class="sxs-lookup"><span data-stu-id="04042-179">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="04042-180">Si les trois paramètres sont spécifiés et que les données sont valides, une connexion est effectuée immédiatement au démarrage du programme.</span><span class="sxs-lookup"><span data-stu-id="04042-180">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="04042-181">Si un paramètre n’est pas valide, le programme démarre comme s’il n’y a aucun paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="04042-181">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="04042-182">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04042-182">Related topics</span></span>


[<span data-ttu-id="04042-183">Opérations de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="04042-183">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

[<span data-ttu-id="04042-184">Récupération des ordinateurs à l'aide de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="04042-184">Recovering Computers Using DaRT 8.0</span></span>](recovering-computers-using-dart-80-dart-8.md)










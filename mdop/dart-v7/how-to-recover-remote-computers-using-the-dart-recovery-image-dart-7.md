---
title: Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT
description: Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809569"
---
# <span data-ttu-id="a502d-103">Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="a502d-103">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="a502d-104">Les fonctionnalités de connexion à distance de Microsoft Diagnostics and Recovery Tools (DaRT) 7 permettent à un administrateur informatique d’exécuter les outils DaRT à distance sur un ordinateur d’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a502d-104">The Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="a502d-105">Lorsque certaines informations sont fournies par l’utilisateur final (ou par un professionnel du support technique travaillant sur l’ordinateur de l’utilisateur final), l’administrateur informatique ou l’agent de support technique peut prendre le contrôle de l’ordinateur de l’utilisateur final et exécuter les outils DaRT nécessaires à distance.</span><span class="sxs-lookup"><span data-stu-id="a502d-105">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

**<span data-ttu-id="a502d-106">Important</span><span class="sxs-lookup"><span data-stu-id="a502d-106">Important</span></span>**  
<span data-ttu-id="a502d-107">Les deux ordinateurs qui établissent une connexion à distance doivent faire partie du même réseau.</span><span class="sxs-lookup"><span data-stu-id="a502d-107">The two computers establishing a remote connection must be part of the same network.</span></span>



**<span data-ttu-id="a502d-108">Pour récupérer un ordinateur distant à l’aide de DaRT</span><span class="sxs-lookup"><span data-stu-id="a502d-108">To recover a remote computer by using DaRT</span></span>**

1.  <span data-ttu-id="a502d-109">Démarrez un ordinateur utilisateur final en utilisant l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="a502d-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="a502d-110">En règle générale, vous devez utiliser l’une des méthodes suivantes pour démarrer dans DaRT afin de récupérer un ordinateur distant, selon la manière dont vous déployez l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="a502d-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="a502d-111">Pour plus d’informations sur le déploiement de l’image de récupération DaRT, voir [déploiement de l’image de récupération 7,0 de DART](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="a502d-111">For more information about deploying the DaRT recovery image, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

    -   <span data-ttu-id="a502d-112">Démarrez dans DaRT à partir d’une partition de récupération sur l’ordinateur qui pose problème.</span><span class="sxs-lookup"><span data-stu-id="a502d-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="a502d-113">Démarrez dans DaRT à partir d’une partition distante sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="a502d-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="a502d-114">Pour plus d’informations sur les avantages et inconvénients de chaque méthode, voir [planification de l’enregistrement et du déploiement de l’image de récupération 7,0 de DART](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="a502d-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

    <span data-ttu-id="a502d-115">Quelle que soit la méthode que vous utilisez pour démarrer dans DaRT, vous devez activer le périphérique de démarrage dans le BIOS pour l’option de démarrage ou les options que vous voulez mettre à disposition de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a502d-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="a502d-116">Remarque</span><span class="sxs-lookup"><span data-stu-id="a502d-116">Note</span></span>**  
    <span data-ttu-id="a502d-117">La configuration du BIOS est unique, en fonction du type de disque dur, de cartes réseau et d’autres éléments utilisés au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a502d-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



2.  <span data-ttu-id="a502d-118">Au démarrage de l’ordinateur dans l’image de récupération DaRT, la boîte de dialogue **netstart** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a502d-118">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="a502d-119">Vous êtes invité à indiquer si vous souhaitez initialiser les services réseau.</span><span class="sxs-lookup"><span data-stu-id="a502d-119">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="a502d-120">Si vous cliquez sur **Oui**, on suppose qu’un serveur DHCP est présent sur le réseau et qu’une tentative d’obtention d’une adresse IP du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="a502d-120">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="a502d-121">Si le réseau utilise des adresses IP statiques au lieu de DHCP, vous pouvez utiliser l’outil de **configuration TCP/IP** dans DART pour spécifier une adresse IP statique.</span><span class="sxs-lookup"><span data-stu-id="a502d-121">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="a502d-122">Pour ignorer le processus d’initialisation du réseau, cliquez sur **non**.</span><span class="sxs-lookup"><span data-stu-id="a502d-122">To skip the network initialization process, click **No**.</span></span>

3.  <span data-ttu-id="a502d-123">Après la boîte de dialogue initialisation du réseau, vous êtes invité à indiquer si vous souhaitez remapper les lettres de lecteur.</span><span class="sxs-lookup"><span data-stu-id="a502d-123">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="a502d-124">Lorsque vous exécutez Windows en ligne, le volume système est généralement mappé au lecteur C. Toutefois, lorsque vous exécutez Windows Offline sous WinRE, le volume système d’origine peut être mappé sur un autre lecteur, ce qui peut entraîner une confusion.</span><span class="sxs-lookup"><span data-stu-id="a502d-124">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="a502d-125">Si vous décidez de remapper, DaRT tente de mapper les lettres du lecteur hors ligne pour correspondre aux lettres de lecteur en ligne.</span><span class="sxs-lookup"><span data-stu-id="a502d-125">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="a502d-126">Le remappage est effectué uniquement si un système d’exploitation hors connexion est sélectionné plus tard dans le processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="a502d-126">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="a502d-127">Après la boîte de dialogue remappage, une boîte de dialogue **options de récupération du système** s’affiche et vous invite à sélectionner une disposition de clavier.</span><span class="sxs-lookup"><span data-stu-id="a502d-127">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="a502d-128">Il affiche ensuite le répertoire racine du système, le type de système d’exploitation installé et la taille de partition.</span><span class="sxs-lookup"><span data-stu-id="a502d-128">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="a502d-129">Si vous ne voyez pas votre système d’exploitation et que vous suspectez qu’il n’y a pas de problème, cliquez sur **charger des pilotes** pour charger les pilotes suspects.</span><span class="sxs-lookup"><span data-stu-id="a502d-129">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="a502d-130">Vous êtes alors invité à insérer le média d’installation pour l’appareil et à sélectionner le pilote.</span><span class="sxs-lookup"><span data-stu-id="a502d-130">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="a502d-131">Sélectionnez l’installation que vous voulez réparer ou diagnostiquer, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a502d-131">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="a502d-132">Remarque</span><span class="sxs-lookup"><span data-stu-id="a502d-132">Note</span></span>**  
    <span data-ttu-id="a502d-133">Si l’environnement de récupération Windows (WinRE) détecte ou suspecte que Windows 7 ne démarrait pas correctement la dernière fois qu’il a été essayé, la **réparation du démarrage** peut commencer à s’exécuter automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a502d-133">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="a502d-134">Pour plus d’informations sur la façon de résoudre ce problème, reportez-vous à la rubrique [résolution des problèmes DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="a502d-134">For information about this situation including how to resolve it, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. <span data-ttu-id="a502d-135">Dans la fenêtre des **options de récupération du système** , sélectionnez **Microsoft Diagnostics and Recovery Tools** pour ouvrir la fenêtre de **Diagnostics et d’outils de récupération** .</span><span class="sxs-lookup"><span data-stu-id="a502d-135">On the **System Recovery Options** window, select **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset** window.</span></span>

6. <span data-ttu-id="a502d-136">Dans la fenêtre **jeu d’outils de diagnostics et de récupération** , cliquez sur **connexion à distance** pour ouvrir la fenêtre de **connexion à distance DART** .</span><span class="sxs-lookup"><span data-stu-id="a502d-136">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="a502d-137">Si vous êtes invité à fournir l’accès distant au support technique, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a502d-137">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="a502d-138">La fenêtre de connexion à distance DaRT s’ouvre et affiche un numéro de ticket, une adresse IP et des informations de port.</span><span class="sxs-lookup"><span data-stu-id="a502d-138">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

7. <span data-ttu-id="a502d-139">Sur l’ordinateur de l’agent de support technique, ouvrez la **visionneuse de connexion à distance DART**.</span><span class="sxs-lookup"><span data-stu-id="a502d-139">On the helpdesk agent computer, open the **DaRT Remote Connection Viewer**.</span></span>

   <span data-ttu-id="a502d-140">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft DART 7**, puis sur **visionneuse de connexions à distance DART**.</span><span class="sxs-lookup"><span data-stu-id="a502d-140">Click **Start**, click **All Programs**, click **Microsoft DaRT 7**, and then click **DaRT Remote Connection Viewer**.</span></span>

8. <span data-ttu-id="a502d-141">Dans la fenêtre de **connexion à distance de DART** , entrez les informations requises sur le ticket, l’adresse IP et le port.</span><span class="sxs-lookup"><span data-stu-id="a502d-141">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="a502d-142">Remarque</span><span class="sxs-lookup"><span data-stu-id="a502d-142">Note</span></span>**  
   <span data-ttu-id="a502d-143">Ces informations sont créées sur l’ordinateur de l’utilisateur final et doivent être fournies par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a502d-143">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="a502d-144">Plusieurs adresses IP peuvent être proposées, en fonction du nombre de personnes disponibles sur l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a502d-144">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



9. <span data-ttu-id="a502d-145">Cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="a502d-145">Click **Connect**.</span></span>

<span data-ttu-id="a502d-146">L’administrateur informatique suppose désormais le contrôle de l’ordinateur de l’utilisateur final et peut exécuter les outils DaRT à distance.</span><span class="sxs-lookup"><span data-stu-id="a502d-146">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="a502d-147">Remarque</span><span class="sxs-lookup"><span data-stu-id="a502d-147">Note</span></span>**  
<span data-ttu-id="a502d-148">Un fichier nommé inv32.xml contient des informations de connexion distantes, telles que le numéro de port et l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="a502d-148">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="a502d-149">Par défaut, le fichier se trouve généralement sur%windir%\\system32.</span><span class="sxs-lookup"><span data-stu-id="a502d-149">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="a502d-150">Pour personnaliser le processus de connexion à distance</span><span class="sxs-lookup"><span data-stu-id="a502d-150">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="a502d-151">Vous pouvez personnaliser le processus de connexion à distance en modifiant le fichier winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="a502d-151">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="a502d-152">Pour plus d’informations sur la modification du fichier winpeshl.ini, voir [Winpeshl.ini de fichiers](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="a502d-152">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="a502d-153">Spécifiez les commandes et les paramètres suivants pour personnaliser l’établissement d’une connexion distante avec un ordinateur d’utilisateur final:</span><span class="sxs-lookup"><span data-stu-id="a502d-153">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a502d-154">Commande</span><span class="sxs-lookup"><span data-stu-id="a502d-154">Command</span></span></th>
   <th align="left"><span data-ttu-id="a502d-155">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a502d-155">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="a502d-156">Description</span><span class="sxs-lookup"><span data-stu-id="a502d-156">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a502d-157">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="a502d-157">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a502d-158">-nomessage</span><span class="sxs-lookup"><span data-stu-id="a502d-158">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a502d-159">Spécifie que l’invite de confirmation ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="a502d-159">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="a502d-160">La connexion à distance </strong> continue comme si l’utilisateur final avait répondu &quot; Oui &quot; à l’invite de confirmation.</span><span class="sxs-lookup"><span data-stu-id="a502d-160">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a502d-161">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="a502d-161">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a502d-162">aucune</span><span class="sxs-lookup"><span data-stu-id="a502d-162">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a502d-163">Empêche la poursuite d’un script personnalisé tant que <strong> la connexion à distance n' </strong> est pas en cours d’exécution ou qu’une connexion valide est établie avec l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a502d-163">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a502d-164">Important</span><span class="sxs-lookup"><span data-stu-id="a502d-164">Important</span></span></strong><br/><p><span data-ttu-id="a502d-165">Cette commande n’utilise aucune fonction si elle est spécifiée de manière indépendante.</span><span class="sxs-lookup"><span data-stu-id="a502d-165">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="a502d-166">Il doit être spécifié dans un script pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="a502d-166">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="a502d-167">Voici un exemple de fichier winpeshl.ini personnalisé pour ouvrir l’outil de **connexion à distance** dès qu’une tentative de démarrage dans DART est lancée:</span><span class="sxs-lookup"><span data-stu-id="a502d-167">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

**<span data-ttu-id="a502d-168">Pour exécuter la visionneuse de connexions à distance à l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="a502d-168">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="a502d-169">Vous pouvez exécuter la **visionneuse de connexions à distance DART** à l’invite de commandes en spécifiant la commande **DartRemoteViewer.exe** et en utilisant les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="a502d-169">You can run the **DaRT Remote Connection Viewer** at the command prompt by specifying the **DartRemoteViewer.exe** command and by using the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a502d-170">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a502d-170">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="a502d-171">Description</span><span class="sxs-lookup"><span data-stu-id="a502d-171">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a502d-172">-ticket = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a502d-172">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a502d-173">Où &lt; <em> ticketnumber </em> &gt; correspond au numéro de ticket, y compris aux tirets, qui est généré par la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="a502d-173">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a502d-174">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a502d-174">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a502d-175">Où &lt; <em> IPAddress </em> &gt; est l’adresse IP générée par la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="a502d-175">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a502d-176">-port = &lt; <em> port</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a502d-176">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a502d-177">Où &lt; <em> port </em> &gt; correspond au port qui correspond à l’adresse IP spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a502d-177">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="a502d-178">Si les trois paramètres sont spécifiés et que les données sont valides, une connexion est effectuée immédiatement au démarrage du programme.</span><span class="sxs-lookup"><span data-stu-id="a502d-178">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="a502d-179">Si un paramètre n’est pas valide, le programme démarre comme s’il n’y a aucun paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="a502d-179">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="a502d-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a502d-180">Related topics</span></span>


[<span data-ttu-id="a502d-181">Récupération des ordinateurs à l'aide de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="a502d-181">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)










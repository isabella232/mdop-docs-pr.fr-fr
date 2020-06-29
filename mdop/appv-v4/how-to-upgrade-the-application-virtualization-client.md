---
title: Procédure pour mettre à niveau Application Virtualization Client
description: Procédure pour mettre à niveau Application Virtualization Client
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806713"
---
# <span data-ttu-id="79191-103">Procédure pour mettre à niveau Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="79191-103">How to Upgrade the Application Virtualization Client</span></span>


<span data-ttu-id="79191-104">Vous pouvez utiliser les procédures suivantes pour mettre à niveau le client de bureau App-V) ou le client App-V pour les services Bureau à distance (auparavant services Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="79191-104">You can use the following procedures to upgrade the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="79191-105">Pour effectuer une mise à niveau du client, installez une nouvelle version sur la version antérieure déjà installée.</span><span class="sxs-lookup"><span data-stu-id="79191-105">You upgrade the client by installing a new version over the previously installed older version.</span></span> <span data-ttu-id="79191-106">Lorsque vous procédez à la mise à niveau des clients, le logiciel d’installation conserve automatiquement et migre les paramètres de l’utilisateur pour les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="79191-106">When you upgrade the clients, the installer software automatically preserves and migrates the user’s settings for virtual applications.</span></span> <span data-ttu-id="79191-107">Des droits d’administration sont nécessaires pour exécuter le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="79191-107">Administrative rights are required to run the setup program.</span></span>

<span data-ttu-id="79191-108">**Remarques**  Lors de la mise à niveau vers Application Virtualization (App-V) 4.5 ou versions ultérieures, les autorisations d’accès à la clé de Registre HKCU sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="79191-108">**Note** During the upgrade to Application Virtualization (App-V)4.5 or later versions, the permissions to the HKCU registry key are changed.</span></span> <span data-ttu-id="79191-109">Pour cette raison, les utilisateurs perdent des configurations utilisateur qui ont été définies auparavant, par exemple, des paramètres du mode déconnecté configurés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="79191-109">Because of this, users will lose user configurations that were set previously, such as user-configured Disconnected Mode settings.</span></span> <span data-ttu-id="79191-110">Si l’utilisateur n’est pas activement empêché de configurer le comportement de l’interface utilisateur du client par le biais d’un verrouillage des autorisations, l’utilisateur peut réinitialiser ces préférences après une actualisation de publication.</span><span class="sxs-lookup"><span data-stu-id="79191-110">If the user is not actively restricted from configuring client user interface behavior through a permission lockdown, the user can reset these preferences after a publishing refresh.</span></span>

 

<span data-ttu-id="79191-111">**Important**  Lorsque vous procédez à la mise à niveau vers la version 4.6 ou une version ultérieure du client App-V, vous devez utiliser le programme d’installation approprié pour le système d’exploitation de l’ordinateur, 32-bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="79191-111">**Important** When upgrading to version4.6 or a later version of the App-V Client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="79191-112">L’installation échoue et un message d’erreur s’affiche si vous utilisez le mauvais programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="79191-112">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

 

**<span data-ttu-id="79191-113">Pour mettre à niveau le client de bureau de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="79191-113">To upgrade the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="79191-114">Fermez toutes les applications virtuelles, cliquez avec le bouton droit sur l’icône du client de bureau App-V affichée dans la zone de notification du bureau Windows, puis sélectionnez **quitter** pour arrêter le client existant.</span><span class="sxs-lookup"><span data-stu-id="79191-114">Shut down all virtual applications, right-click the App-V Desktop Client icon displayed in the Windows desktop notification area, and select **Exit** to shut down the existing client.</span></span>

2.  <span data-ttu-id="79191-115">Lorsque vous avez obtenu le fichier d’archive du programme d’installation approprié et que vous l’avez enregistré sur votre ordinateur, double-cliquez dessus pour développer l’archive.</span><span class="sxs-lookup"><span data-stu-id="79191-115">After you have obtained the correct installer archive file and saved it to your computer, double-click it to expand the archive.</span></span>

3.  <span data-ttu-id="79191-116">Recherchez le fichier setup.exe, puis double-cliquez sur setup.exe pour démarrer l’installation.</span><span class="sxs-lookup"><span data-stu-id="79191-116">Browse to find the setup.exe file, and double-click setup.exe to start the installation.</span></span>

4.  <span data-ttu-id="79191-117">L’Assistant vérifie le système pour s’assurer que tous les logiciels requis sont installés et vous invite à installer l’une des opérations suivantes, le cas échéant:</span><span class="sxs-lookup"><span data-stu-id="79191-117">The wizard checks the system to ensure that all prerequisite software is installed and will prompt you to install any of the following, if missing:</span></span>

    -   <span data-ttu-id="79191-118">Package redistribuable Microsoft VisualC + + 2005SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="79191-118">Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>

    -   <span data-ttu-id="79191-119">Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="79191-119">Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

    -   <span data-ttu-id="79191-120">Rapport d’erreurs d’application Microsoft</span><span class="sxs-lookup"><span data-stu-id="79191-120">Microsoft Application Error Reporting</span></span>

    <span data-ttu-id="79191-121">**Remarques**  Pour la version 4.6 ou une version ultérieure, l’Assistant installe également la configuration logicielle requise suivante:</span><span class="sxs-lookup"><span data-stu-id="79191-121">**Note** For version4.6 and higher, the wizard will also install the following software prerequisite:</span></span>

    -   <span data-ttu-id="79191-122">Package redistribuable Microsoft VisualC + + 2008SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="79191-122">Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

     

5.  <span data-ttu-id="79191-123">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="79191-123">Click **Install**.</span></span> <span data-ttu-id="79191-124">La progression de l’installation s’affiche, et l’état passe de **en attente** à **l’installation**.</span><span class="sxs-lookup"><span data-stu-id="79191-124">Installation progress is displayed, and the status changes from **Pending** to **Installing**.</span></span> <span data-ttu-id="79191-125">L' **État d’installation passe à succès dès** que chaque étape est terminée.</span><span class="sxs-lookup"><span data-stu-id="79191-125">Installation status changes to **Succeeded** as each step is completed successfully.</span></span>

6.  <span data-ttu-id="79191-126">Lorsque la boîte de dialogue **client de bureau de virtualisation des applications** apparaît et affiche un message indiquant qu’une version plus ancienne du client est disponible sur l’ordinateur, cliquez sur en **regard** de mettre à niveau vers la nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="79191-126">When the **Application Virtualization Desktop Client** dialog appears and displays a message stating that an older version of the client has been found on the computer, click **Next** to upgrade to the new version.</span></span>

7.  <span data-ttu-id="79191-127">Lorsque l’écran du **contrat de licence** s’affiche, lisez le contrat de licence et, si vous êtes d’accord, cliquez sur **J’accepte les conditions du contrat de licence**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="79191-127">When the **License Agreement** screen is displayed, read the license agreement, and if you agree, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

8.  <span data-ttu-id="79191-128">Lorsque l’Assistant InstallShield affiche la boîte **de dialogue préparer la mise à niveau de l’application** , cliquez sur **mettre** à niveau pour commencer la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="79191-128">When the InstallShield Wizard displays the **Ready to Upgrade the Program** dialog screen, click **Upgrade** to begin the upgrade.</span></span> <span data-ttu-id="79191-129">L’écran suivant indique que le client est en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="79191-129">The next screen indicates that the client is being installed.</span></span>

    <span data-ttu-id="79191-130">**Avertissement**  Si vous n’avez pas arrêté le programme client à l’étape 1, un message d’avertissement relatif **à l’utilisation du fichier** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="79191-130">**Warning** If you did not shut down the client program in step 1, you might see a **Files In Use** warning displayed.</span></span> <span data-ttu-id="79191-131">Si tel est le cas, cliquez avec le bouton droit sur l’icône du client App-V affichée dans la zone de notification du bureau et sélectionnez **quitter** pour arrêter le client existant.</span><span class="sxs-lookup"><span data-stu-id="79191-131">If this happens, right-click the App-V Client icon displayed in the desktop notification area and select **Exit** to shut down the existing client.</span></span> <span data-ttu-id="79191-132">Cliquez ensuite sur **Réessayer** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="79191-132">Then click **Retry** to continue.</span></span>

     

9.  <span data-ttu-id="79191-133">Lorsque l’installation est terminée, vous êtes invité à redémarrer votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="79191-133">When the installation completes successfully, you will be prompted to restart the computer.</span></span> <span data-ttu-id="79191-134">Vous devez redémarrer l’ordinateur pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="79191-134">You need to restart the computer to complete the installation.</span></span>

    <span data-ttu-id="79191-135">**Attention**  Si la mise à niveau échoue pour une raison quelconque, vous devez redémarrer votre ordinateur avant de réessayer la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="79191-135">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

**<span data-ttu-id="79191-136">Pour mettre à niveau le client de virtualisation des applications à l’aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="79191-136">To upgrade the Application Virtualization Client by Using the Command Line</span></span>**

1.  <span data-ttu-id="79191-137">Si vous procédez à la mise à niveau du client App-V à l’aide du programme setup.msi, assurez-vous que tous les logiciels requis requis sont installés.</span><span class="sxs-lookup"><span data-stu-id="79191-137">If upgrading the App-V client using the setup.msi program, ensure that any necessary prerequisite software has been installed.</span></span>

    **<span data-ttu-id="79191-138">Important</span><span class="sxs-lookup"><span data-stu-id="79191-138">Important</span></span>**  
    -   <span data-ttu-id="79191-139">Pour la version 4.6 et une version ultérieure du client App-V, le programme de setup.msi vérifie le système et ne fonctionne pas avec un message d’erreur indiquant que l’installation ne peut pas continuer si le logiciel requis n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="79191-139">For version4.6 and later of the App-V client, the setup.msi program checks the system and will fail with an error message indicating that installation cannot continue if prerequisite software is not installed.</span></span>

    -   <span data-ttu-id="79191-140">Pour App-V version 4.6, les paramètres de ligne de commande ne peuvent pas être utilisés lors d’une mise à niveau et seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="79191-140">For App-V version4.6, command-line parameters cannot be used during an upgrade and will be ignored.</span></span>

     

2.  <span data-ttu-id="79191-141">L’exemple de ligne de commande suivant utilise le fichier setup.msi pour mettre à niveau le client App-V.</span><span class="sxs-lookup"><span data-stu-id="79191-141">The following command-line example uses the setup.msi file to upgrade the App-V Client.</span></span> <span data-ttu-id="79191-142">Vous devez utiliser le programme d’installation client approprié, selon que vous effectuez une mise à niveau du client de bureau App-V ou du client App-V pour les services Bureau à distance (anciennement services Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="79191-142">You will need to use the correct client installer program depending on whether you are upgrading the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span>

    **<span data-ttu-id="79191-143">msiexec.exe/i "setup.msi"</span><span class="sxs-lookup"><span data-stu-id="79191-143">msiexec.exe /i "setup.msi"</span></span>**

    <span data-ttu-id="79191-144">**Important**  Les guillemets sont requis uniquement lorsque la valeur contient un espace.</span><span class="sxs-lookup"><span data-stu-id="79191-144">**Important** The quotation marks are required only when the value contains a space.</span></span> <span data-ttu-id="79191-145">Par souci de cohérence, toutes les instances de l’exemple précédent sont indiquées par des guillemets.</span><span class="sxs-lookup"><span data-stu-id="79191-145">For consistency, all instances in the preceding example are shown as having quotation marks.</span></span>

     

**<span data-ttu-id="79191-146">Pour mettre à niveau le client de virtualisation des applications pour les services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="79191-146">To upgrade the Application Virtualization Client for Remote Desktop Services</span></span>**

1.  <span data-ttu-id="79191-147">Suivez les stratégies standard de votre organisation relatives à l’installation ou à la mise à niveau d’applications sur le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="79191-147">Follow your organization’s standard policies for installing or upgrading applications on the Remote Desktop Session Host (RDSession Host) server.</span></span> <span data-ttu-id="79191-148">Si le système fait partie d’une batterie de serveurs, supprimez l’hôte RDSession de la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="79191-148">If the system is part of a farm, remove the RDSession Host from the server farm.</span></span>

2.  <span data-ttu-id="79191-149">Pour mettre à niveau le client App-V pour les services Bureau à distance (auparavant services Terminal Server), vous devez utiliser la ligne de commande car vous ne pouvez pas mettre à niveau le client manuellement sur l’hôte RDSession.</span><span class="sxs-lookup"><span data-stu-id="79191-149">To upgrade the App-V Client for Remote Desktop Services (formerly Terminal Services), you must use the command line because you cannot upgrade the client manually on the RDSession Host.</span></span>

    <span data-ttu-id="79191-150">**Remarques**  Dans l’App-V version 4,6 et les versions ultérieures, en plus de l’utilisation de la ligne de commande pour mettre à niveau le client, vous pouvez également utiliser une session de bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="79191-150">**Note** In App-V version 4.6 and later, in addition to using the command line to upgrade the client, you can also use a Remote Desktop session.</span></span> <span data-ttu-id="79191-151">Aucun paramètre spécial n’est requis pour démarrer la session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="79191-151">No special parameters are required to start the Remote Desktop session.</span></span>

     

3.  <span data-ttu-id="79191-152">Après l’exécution de la mise à niveau du client pour les services Bureau à distance, redémarrez et connectez-vous à l’hôte RDSession.</span><span class="sxs-lookup"><span data-stu-id="79191-152">After the Client for Remote Desktop Services upgrade is complete, restart and log in to the RDSession Host.</span></span>

4.  <span data-ttu-id="79191-153">Après le redémarrage du système, ajoutez le serveur à la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="79191-153">After the system is restarted, add the server to the server farm.</span></span>

    <span data-ttu-id="79191-154">**Attention**  Si la mise à niveau échoue pour une raison quelconque, vous devez redémarrer votre ordinateur avant de réessayer la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="79191-154">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

## <span data-ttu-id="79191-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79191-155">Related topics</span></span>


[<span data-ttu-id="79191-156">Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="79191-156">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 






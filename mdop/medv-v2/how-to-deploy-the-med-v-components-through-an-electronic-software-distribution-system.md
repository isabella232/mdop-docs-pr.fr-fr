---
title: Déploiement des composants de MED-V via un système de distribution électronique de logiciels
description: Déploiement des composants de MED-V via un système de distribution électronique de logiciels
author: dansimp
ms.assetid: 8a800bdf-6fa4-47b4-b417-df053289d4e8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d772702c770340796fe770273146bd0308617a69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810805"
---
# <span data-ttu-id="c2a0c-103">Déploiement des composants de MED-V via un système de distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="c2a0c-103">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>


<span data-ttu-id="c2a0c-104">Un système de distribution de logiciels électronique peut vous aider à déplacer efficacement des logiciels vers de nombreux ordinateurs par le biais de connexion réseau lente ou rapide.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-104">An electronic software distribution system can help you efficiently move software to many computers over slow or fast network connections.</span></span> <span data-ttu-id="c2a0c-105">La section suivante fournit des informations et des instructions pour vous aider à déployer les composants 2,0 de la virtualisation de bureau Microsoft Enterprise (MED-V) au sein de votre entreprise à l’aide d’un système de distribution de logiciels.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-105">The following section provides information and instructions to help you deploy the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components throughout your enterprise by using a software distribution system.</span></span>

**<span data-ttu-id="c2a0c-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="c2a0c-106">Note</span></span>**  
<span data-ttu-id="c2a0c-107">Quelle que soit la solution de distribution de logiciels que vous utilisez, vous devez être familiarisé avec la configuration requise pour votre solution particulière.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-107">Whichever software distribution solution that you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="c2a0c-108">Si vous utilisez System Center Configuration Manager 2007 R2 ou une version ultérieure, voir la [bibliothèque de documentation du gestionnaire de configuration](https://go.microsoft.com/fwlink/?LinkId=66999) dans la bibliothèque technique Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .</span><span class="sxs-lookup"><span data-stu-id="c2a0c-108">If you are using System Center Configuration Manager 2007 R2 or a later version, see the [Configuration Manager Documentation Library](https://go.microsoft.com/fwlink/?LinkId=66999) in the Microsoft Technical Library (https://go.microsoft.com/fwlink/?LinkId=66999).</span></span>



**<span data-ttu-id="c2a0c-109">Important</span><span class="sxs-lookup"><span data-stu-id="c2a0c-109">Important</span></span>**  
<span data-ttu-id="c2a0c-110">Si vous utilisez System Center Configuration Manager 2007 SP2 et que vos espaces de travail MED-V sont configurés pour fonctionner en mode **NAT** , les machines virtuelles sont classées comme des clients Internet et ne peuvent pas trouver les points de distribution les plus proches pour le téléchargement du contenu.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-110">If you are using System Center Configuration Manager 2007 SP2 and your MED-V workspaces are configured to operate in **NAT** mode, the virtual machines are classified as Internet-based clients and cannot find the closest distribution points from which to download content.</span></span>

<span data-ttu-id="c2a0c-111">Le [correctif pour améliorer la fonctionnalité pour les ordinateurs virtuels gérés par Med-v](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) ajoute de nouvelles fonctionnalités aux machines virtuelles gérées par Med-v et configurées pour fonctionner en mode **NAT** .</span><span class="sxs-lookup"><span data-stu-id="c2a0c-111">The [hotfix to improve the functionality for VMs that are managed by MED-V](https://go.microsoft.com/fwlink/?LinkId=201088) (https://go.microsoft.com/fwlink/?LinkId=201088) adds new functionality to virtual machines that are managed by MED-V and that are configured to operate in **NAT** mode.</span></span> <span data-ttu-id="c2a0c-112">La nouvelle fonctionnalité permet aux machines virtuelles d’accéder aux points de distribution les plus proches.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-112">The new functionality lets virtual machines access the closest distribution points.</span></span> <span data-ttu-id="c2a0c-113">Par conséquent, l’administrateur peut gérer l’ordinateur virtuel et l’ordinateur hôte de la même manière.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-113">Therefore, the administrator can manage the virtual machine and the host computer in the same manner.</span></span> <span data-ttu-id="c2a0c-114">Ce correctif doit d’abord être installé sur le serveur de site, puis sur le client.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-114">This hotfix must be installed first on the site server and then on the client.</span></span>

<span data-ttu-id="c2a0c-115">La mise à jour est publiquement disponible.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-115">The update is publicly available.</span></span> <span data-ttu-id="c2a0c-116">Toutefois, vous pouvez être invité à accepter un contrat pour les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-116">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="c2a0c-117">Suivez les invites sur les pages Web successives pour récupérer ce correctif.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-117">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>



**<span data-ttu-id="c2a0c-118">Remarque</span><span class="sxs-lookup"><span data-stu-id="c2a0c-118">Note</span></span>**  
<span data-ttu-id="c2a0c-119">Pour pouvoir déployer les composants MED-v de votre système de distribution de logiciels, vous devez installer le gestionnaire de package d’espace de travail MED-V et générer vos espaces de travail MED-v.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-119">You must install the MED-V workspace packager and build your MED-V workspaces before you can deploy the MED-V components through your software distribution system.</span></span> <span data-ttu-id="c2a0c-120">Pour plus d’informations sur la préparation d’une image et sur la création de vos espaces de travail MED-V, voir [opérations pour med-v](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-120">For more information about how to prepare an image and to build your MED-V workspaces, see [Operations for MED-V](operations-for-med-v.md).</span></span>



**<span data-ttu-id="c2a0c-121">Pour déployer les composants MED-V à l’aide d’un système de distribution de logiciels</span><span class="sxs-lookup"><span data-stu-id="c2a0c-121">To deploy the MED-V components by using a software distribution system</span></span>**

1.  <span data-ttu-id="c2a0c-122">Définissez un groupe d’ordinateurs et d’utilisateurs dans le système de distribution de logiciels électroniques en tant qu’ensemble cible d’ordinateurs/utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-122">Define a group of computers and users in the electronic software distribution system as the target set of computers/users.</span></span>

2.  <span data-ttu-id="c2a0c-123">Créez des packages pour chaque fichier d’installation Microsoft devant être distribué.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-123">Create packages for each Microsoft installation file that needs to be distributed.</span></span> <span data-ttu-id="c2a0c-124">Vous trouverez ci-après les fichiers requis et l’ordre dans lequel ils doivent être installés:</span><span class="sxs-lookup"><span data-stu-id="c2a0c-124">The following are the required files and the order in which they must be installed:</span></span>

    1.  <span data-ttu-id="c2a0c-125">**PC virtuel Windows** , si ce n’est pas déjà fait (un redémarrage de l’ordinateur est requis).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-125">**Windows Virtual PC** – if not already installed (a computer restart is required).</span></span> <span data-ttu-id="c2a0c-126">Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-126">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    2.  <span data-ttu-id="c2a0c-127">**Ajouts et mises à jour pour PC virtuel** , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-127">**Windows Virtual PC Additions and Updates** – if not already installed.</span></span> <span data-ttu-id="c2a0c-128">Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-128">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    3.  <span data-ttu-id="c2a0c-129">**Fichier d’installation de l’agent hôte MED-v** : installation de l’agent hôte (med-v \ _HostAgent _setup fichier d’installation).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-129">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="c2a0c-130">Pour plus d’informations, reportez-vous à la rubrique [installation manuelle de l’agent hôte MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-130">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

        **<span data-ttu-id="c2a0c-131">Warning</span><span class="sxs-lookup"><span data-stu-id="c2a0c-131">Warning</span></span>**  
        <span data-ttu-id="c2a0c-132">Fermez Internet Explorer avant d’installer l’agent d’hébergement MED-V, sinon des conflits peuvent se produire plus tard avec la redirection d’URL.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-132">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="c2a0c-133">Vous pouvez également le faire en spécifiant un redémarrage de l’ordinateur lors d’une distribution.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-133">You can also do this by specifying a computer restart during a distribution.</span></span>   

    4.  <span data-ttu-id="c2a0c-134">**Exécutable du programme d’espace de travail MED-v, VHD et de l’installation,** créé dans le **Gestionnaire de package med-v**</span><span class="sxs-lookup"><span data-stu-id="c2a0c-134">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="c2a0c-135">Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-135">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        **<span data-ttu-id="c2a0c-136">Important</span><span class="sxs-lookup"><span data-stu-id="c2a0c-136">Important</span></span>**  
        <span data-ttu-id="c2a0c-137">Le fichier de disque dur virtuel compressé (. medv) et le programme exécutable du programme d’installation (setup.exe) doivent figurer dans le même dossier que le programme d’installation de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-137">The compressed virtual hard disk file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="c2a0c-138">Ensuite, installez le programme d’installation de l’espace de travail MED-V en exécutant setup.exe.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-138">Then, install the MED-V workspace installer by running setup.exe.</span></span>

        **<span data-ttu-id="c2a0c-139">Astuce</span><span class="sxs-lookup"><span data-stu-id="c2a0c-139">Tip</span></span>**  
        <span data-ttu-id="c2a0c-140">Dans la mesure où des problèmes peuvent se produire lorsque vous installez MED-V à partir d’un emplacement réseau, il est recommandé de copier les fichiers de configuration de l’espace de travail MED-V localement, puis d’exécuter setup.exe.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-140">Because problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>       

3.  <span data-ttu-id="c2a0c-141">Configurez les packages pour qu’ils s’exécutent en mode silencieux (aucune interaction utilisateur n’est requise).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-141">Configure the packages to run in silent mode (no user interaction is required).</span></span>

    <span data-ttu-id="c2a0c-142">L’exécution en mode silencieux élimine l’invite de fermeture d’Internet Explorer s’il est en cours d’exécution et l’invite de démarrage de l’agent hôte MED-V.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-142">Running in silent mode eliminates the prompt to close Internet Explorer if it is running and the prompt to start the MED-V Host Agent.</span></span> <span data-ttu-id="c2a0c-143">Les deux actions sont effectuées au redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-143">Both actions are performed when the computer is restarted.</span></span>

    **<span data-ttu-id="c2a0c-144">Remarque</span><span class="sxs-lookup"><span data-stu-id="c2a0c-144">Note</span></span>**  
    <span data-ttu-id="c2a0c-145">Le redémarrage de l’ordinateur virtuel Windows nécessite que vous redémarriez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-145">Installation of Windows Virtual PC requires you to restart the computer.</span></span> <span data-ttu-id="c2a0c-146">Vous pouvez créer un processus d’installation unique et installer tous les composants en même temps si vous supprimez le redémarrage et ignorez les conditions préalables nécessaires à l’installation de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-146">You can create a single installation process and install all the components at the same time if you suppress the restart and ignore the prerequisites necessary for MED-V to install.</span></span> <span data-ttu-id="c2a0c-147">Vous pouvez également effectuer cette opération à l’aide d’arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-147">You can also do this by using command-line arguments.</span></span> <span data-ttu-id="c2a0c-148">Pour obtenir un exemple de ces arguments, voir [pour installer les composants MED-V à l’aide d’un fichier de commandes](#bkmk-batch).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-148">For an example of these arguments, see [To install the MED-V components by using a batch file](#bkmk-batch).</span></span> <span data-ttu-id="c2a0c-149">MED-V démarre automatiquement au redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-149">MED-V automatically starts when the computer is restarted.</span></span>

4.  <span data-ttu-id="c2a0c-150">Installation de MED-V et de ses composants avant d’installer Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-150">Install MED-V and its components before installing Windows Virtual PC.</span></span> <span data-ttu-id="c2a0c-151">Consultez l’exemple de fichier de commandes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-151">See the example batch file later in this topic.</span></span>

    **<span data-ttu-id="c2a0c-152">Important</span><span class="sxs-lookup"><span data-stu-id="c2a0c-152">Important</span></span>**  
    <span data-ttu-id="c2a0c-153">Sélectionnez l’option **Ignorer \ _PREREQUISITES** comme illustré dans l’exemple de fichier de commandes pour que les composants MED-V puissent être installés avant les composants VPC requis.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-153">Select the **IGNORE\_PREREQUISITES** option as shown in the example batch file so that the MED-V components can be installed prior to the required VPC components.</span></span> <span data-ttu-id="c2a0c-154">Installez les composants MED-V de façon à ce qu’ils permettent le redémarrage unique.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-154">Install the MED-V components in this order to allow for the single restart.</span></span>

5.  <span data-ttu-id="c2a0c-155">Identifiez les autres exigences nécessaires pour l’installation et pour votre système de distribution de logiciels, tels que les plateformes cibles et l’espace libre sur le disque.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-155">Identify any other requirements necessary for the installation and for your software distribution system, such as target platforms and the free disk space.</span></span>

6.  <span data-ttu-id="c2a0c-156">Affectez les packages à l’ensemble cible d’ordinateurs/utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-156">Assign the packages to the target set of computers/users.</span></span>

    <span data-ttu-id="c2a0c-157">Au fur et à mesure que des ordinateurs sont exécutés, le client système de distribution de logiciels reconnaît que de nouveaux packages sont disponibles et commence à installer les packages conformément à la définition et aux exigences.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-157">As computers are running, the software distribution system client recognizes that new packages are available and begins to install the packages per the definition and requirements.</span></span> <span data-ttu-id="c2a0c-158">Les installations doivent s’exécuter de façon séquentielle en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-158">The installations should run sequentially in silent mode.</span></span> <span data-ttu-id="c2a0c-159">Nous vous recommandons de procéder comme processus unique, qui ne nécessite pas de redémarrage tant que tous les packages ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-159">We recommend that this is performed as a single process that does not require a restart until all the packages are installed.</span></span>

7.  <span data-ttu-id="c2a0c-160">Une fois l’installation terminée, redémarrez l’ordinateur mis à jour.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-160">After the installations are complete, restart the updated computers.</span></span>

    <span data-ttu-id="c2a0c-161">En fonction du système de distribution de logiciels, vous pouvez planifier un redémarrage de l’ordinateur ou les utilisateurs finaux peuvent redémarrer les ordinateurs manuellement pendant leurs tâches normales.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-161">Depending on the software distribution system, you can schedule a restart of the computer or the end users can restart the computers manually during their regular work.</span></span> <span data-ttu-id="c2a0c-162">Après le redémarrage de l’ordinateur, MED-V démarre automatiquement dès qu’un utilisateur final se connecte.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-162">After the computer is restarted, MED-V automatically starts after an end user logs on.</span></span> <span data-ttu-id="c2a0c-163">Lorsque MED-V démarre pour la première fois, il exécute la première fois.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-163">When MED-V starts for the first time, it runs first time setup.</span></span>

<span data-ttu-id="c2a0c-164">Le premier démarrage du programme d’installation et peut prendre quelques minutes en fonction de la taille du disque dur virtuel que vous avez spécifié et du nombre de stratégies appliqués à l’espace de travail MED-V au démarrage.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-164">First time setup starts and might take several minutes to finish, depending on the size of the virtual hard disk that you specified and the number of policies applied to the MED-V workspace on startup.</span></span> <span data-ttu-id="c2a0c-165">L’utilisateur final peut suivre la progression en regardant l’icône MED-V dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-165">The end user can track the progress by watching the MED-V icon in the notification area.</span></span> <span data-ttu-id="c2a0c-166">Pour plus d’informations sur le programme d’installation pour la première fois, voir [vue d’ensemble du déploiement de MED-V 2,0](med-v-20-deployment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c2a0c-166">For more information about first time setup, see [MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md).</span></span>

<a href="" id="bkmk-batch"></a>**<span data-ttu-id="c2a0c-167">Pour installer les composants MED-V à l’aide d’un fichier de commandes</span><span class="sxs-lookup"><span data-stu-id="c2a0c-167">To install the MED-V components by using a batch file</span></span>**

1.  <span data-ttu-id="c2a0c-168">Lancez l’installation à partir d’une invite de commandes avec les informations d’identification d’administration.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-168">Run the installation at a command prompt with administrative credentials.</span></span>

2.  <span data-ttu-id="c2a0c-169">Déployez chaque composant dans un répertoire unique.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-169">Deploy each component to a single directory.</span></span> <span data-ttu-id="c2a0c-170">Si elle est exécutée à partir d’un partage réseau, un délai plus long est requis pour décompresser le fichier. medv.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-170">If run from a network share, a longer time is required to decompress the .medv file.</span></span>

3.  <span data-ttu-id="c2a0c-171">Nous vous conseillons de spécifier le déploiement de PC virtuel Windows et de package Windows Virtual PC après l’installation de l’agent hôte MED-V et des fichiers de package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-171">As a best practice, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="c2a0c-172">Cela signifie que Windows Update n’entraîne aucune interférence avec le processus d’installation en nécessitant un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-172">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

4.  <span data-ttu-id="c2a0c-173">Redémarrez l’ordinateur une fois le fichier de commandes terminé.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-173">Restart the computer after the batch file is finished.</span></span>

<span data-ttu-id="c2a0c-174">Après le redémarrage, l’utilisateur est invité à exécuter la première fois et à terminer la configuration de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-174">After the restart, the user is prompted to run first time setup and complete the configuration of MED-V.</span></span>

<span data-ttu-id="c2a0c-175">Dans l’exemple suivant, avec les arguments spécifiés, vous pouvez installer les composants MED-V 64 d’un processus unique:</span><span class="sxs-lookup"><span data-stu-id="c2a0c-175">The following example, with the specified arguments, shows how to install 64-bit MED-V components in a single process:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2a0c-176">Argument</span><span class="sxs-lookup"><span data-stu-id="c2a0c-176">Argument</span></span></th>
<th align="left"><span data-ttu-id="c2a0c-177">Description</span><span class="sxs-lookup"><span data-stu-id="c2a0c-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2a0c-178">/norestart</span><span class="sxs-lookup"><span data-stu-id="c2a0c-178">/norestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2a0c-179">Empêche l’installation de Windows Virtual PC et de la mise à jour du PC virtuel Windows pour le redémarrage de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-179">Prevents the installation of Windows Virtual PC and the Windows Virtual PC update from restarting the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2a0c-180">/quiet</span><span class="sxs-lookup"><span data-stu-id="c2a0c-180">/quiet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2a0c-181">Installe les composants MED-V en mode quiet sans aucune interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-181">Installs the MED-V components in quiet mode without user interaction.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2a0c-182">/qn</span><span class="sxs-lookup"><span data-stu-id="c2a0c-182">/qn</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2a0c-183">Installe les composants MED-V sans interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-183">Installs the MED-V components without a user interface.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2a0c-184">IGNORE_PREREQUISITES</span><span class="sxs-lookup"><span data-stu-id="c2a0c-184">IGNORE_PREREQUISITES</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2a0c-185">Installations sans vérification de l’ordinateur virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-185">Installs without checking for Windows Virtual PC.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c2a0c-186">Remarque</span><span class="sxs-lookup"><span data-stu-id="c2a0c-186">Note</span></span></strong><br/><p><span data-ttu-id="c2a0c-187">Spécifiez cet argument uniquement si vous installez Windows Virtual PC dans le cadre de cette installation.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-187">Only specify this argument if you are installing Windows Virtual PC as part of this installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2a0c-188">OVERWRITEVHD</span><span class="sxs-lookup"><span data-stu-id="c2a0c-188">OVERWRITEVHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2a0c-189">Force l’installation de l’espace de travail MED-V et empêche les invites qu’il peut générer.</span><span class="sxs-lookup"><span data-stu-id="c2a0c-189">Forces the installation of the MED-V workspace and prevents any prompts that it might generate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c2a0c-190">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2a0c-190">Example</span></span>


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## <span data-ttu-id="c2a0c-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2a0c-191">Related topics</span></span>


[<span data-ttu-id="c2a0c-192">Vue d'ensemble du déploiement de MED-V2.0</span><span class="sxs-lookup"><span data-stu-id="c2a0c-192">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="c2a0c-193">Déployer les composants MED-V</span><span class="sxs-lookup"><span data-stu-id="c2a0c-193">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)










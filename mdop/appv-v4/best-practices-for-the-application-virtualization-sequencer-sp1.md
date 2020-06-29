---
title: Meilleures pratiques pour Application Virtualization Sequencer
description: Meilleures pratiques pour Application Virtualization Sequencer
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809090"
---
# <span data-ttu-id="fb911-103">Meilleures pratiques pour Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="fb911-103">Best Practices for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="fb911-104">Cette rubrique décrit les meilleures pratiques pour exécuter le Sequencer Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="fb911-104">This topic provides best practices for running the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="fb911-105">Examinez et prenez en compte les recommandations suivantes lors de la planification et de l’utilisation du Sequencer dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="fb911-105">Review and consider the following recommendations when planning and using the Sequencer in your environment.</span></span>

## <span data-ttu-id="fb911-106">Pratiques recommandées pour la configuration de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="fb911-106">Sequencing Computer Configuration Best Practices</span></span>


<span data-ttu-id="fb911-107">Pour configurer l’ordinateur exécutant le Sequencer App-V, les meilleures pratiques suivantes doivent être prises en compte:</span><span class="sxs-lookup"><span data-stu-id="fb911-107">The following best practices should be considered when configuring the computer running the App-V Sequencer:</span></span>

-   **<span data-ttu-id="fb911-108">Séquence sur un ordinateur ayant une configuration similaire et exécutant une version antérieure du système d’exploitation que les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="fb911-108">Sequence on a computer that has a similar configuration and that is running an earlier version of the operating system than the target computers.</span></span>**

    <span data-ttu-id="fb911-109">Assurez-vous que l’ordinateur exécutant le Sequencer exécute une version antérieure du système d’exploitation que les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="fb911-109">Ensure that the computer that is running the Sequencer is running an earlier version of the operating system than the target computers.</span></span> <span data-ttu-id="fb911-110">Cela inclut les versions du Service Pack et de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fb911-110">This includes the service pack and update versions.</span></span> <span data-ttu-id="fb911-111">Par exemple, si les ordinateurs cibles exécutent Vista et WindowsXP, il est préférable de séquencer les applications sur un ordinateur exécutant WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="fb911-111">For example, if the target computers are running WindowsVista and WindowsXP, you should sequence applications on a computer that is running WindowsXP.</span></span> <span data-ttu-id="fb911-112">La possibilité de séquencer sur un système d’exploitation et d’exécuter l’application virtualisée sur un autre système d’exploitation n’est pas garantie et dépend de l’application et du système d’exploitation spécifiques.</span><span class="sxs-lookup"><span data-stu-id="fb911-112">The ability to sequence on one operating system and run the virtualized application on a different operating system is not guaranteed, and depends on the particular application and operating system.</span></span> <span data-ttu-id="fb911-113">Si vous rencontrez des problèmes, il est possible que vous deviez effectuer une séquence sur le même environnement de système d’exploitation que celui sur lequel le client App-V est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fb911-113">If you encounter issues, you may be required to sequence on the same operating system environment as the one on which the App-V client is running.</span></span>

-   **<span data-ttu-id="fb911-114">Configurer l’ordinateur exécutant le Sequencer avec plusieurs partitions.</span><span class="sxs-lookup"><span data-stu-id="fb911-114">Configure the computer running the Sequencer with multiple partitions.</span></span>**

    <span data-ttu-id="fb911-115">Vous devez configurer l’ordinateur exécutant le Sequencer avec au moins deux partitions principales.</span><span class="sxs-lookup"><span data-stu-id="fb911-115">You should configure the computer running the Sequencer with at least two primary partitions.</span></span> <span data-ttu-id="fb911-116">La première partition (**C:**) doit contenir le système d’exploitation et elle doit être mise en forme à l’aide du système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="fb911-116">The first partition (**C:**) should contain the operating system, and it should be formatted using the NTFS file system.</span></span> <span data-ttu-id="fb911-117">La deuxième partition (**Q:**) est utilisée en tant que chemin de destination de l’installation de l’application virtuelle et doit également être mise en forme à l’aide du système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="fb911-117">The second partition (**Q:**) is used as the destination path for the virtual application installation and should also be formatted using the NTFS file system.</span></span>

-   **<span data-ttu-id="fb911-118">Configurez le répertoire temporaire avec suffisamment d’espace libre sur le disque.</span><span class="sxs-lookup"><span data-stu-id="fb911-118">Configure the temp directory with enough free disk space.</span></span>**

    <span data-ttu-id="fb911-119">Le Sequencer utilise le répertoire **% tmp%** ou **% temp%** , ainsi que le répertoire de **travail** pour le stockage des fichiers temporaires lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="fb911-119">The Sequencer uses the **%TMP%** or **%TEMP%** directory and the **Scratch** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="fb911-120">Vous devez configurer ces répertoires sur l’ordinateur exécutant le Sequencer dont l’espace disque disponible correspond à la configuration estimée requise pour l’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="fb911-120">You should configure these directories on the computer running the Sequencer with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="fb911-121">Pour vérifier l’emplacement du répertoire de **travail** , vous pouvez ouvrir la console de Sequencer et sélectionner des **Outils**, des **options**, puis sélectionner l’onglet **chemins d’accès** . la configuration des répertoires TEMP et du répertoire de **travail** sur différentes partitions de disque dur peut améliorer les performances lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="fb911-121">You can verify the location of the **Scratch** directory by opening the Sequencer console and selecting **Tools**, **Options**, and then selecting the **Paths** tab. Configuring the temp directories and the **Scratch** directory on different hard drive partitions can improve performance during sequencing.</span></span>

-   **<span data-ttu-id="fb911-122">Séquencez des applications à l’aide de Microsoft VirtualPC.</span><span class="sxs-lookup"><span data-stu-id="fb911-122">Sequence applications by using Microsoft VirtualPC.</span></span>**

    <span data-ttu-id="fb911-123">Vous allez séquentiellement la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="fb911-123">You will sequence most applications more than once.</span></span> <span data-ttu-id="fb911-124">Pour faciliter cela, vous devez envisager le séquençage sur un ordinateur exécutant un environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="fb911-124">To help facilitate this, you should consider sequencing on a computer running in a virtual environment.</span></span> <span data-ttu-id="fb911-125">Cela vous permettra de séquencer une application et de revenir à un état propre, avec une reconfiguration minimale, sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fb911-125">This will allow you to sequence an application and revert to a clean state, with minimal reconfiguration, on the computer that is running the Sequencer.</span></span>

    <span data-ttu-id="fb911-126">Si vous exécutez Microsoft Hyper-V dans votre environnement, le Sequencer App-V sera exécuté lorsque l’ordinateur virtuel Hyper-V sur lequel il s’exécute est:</span><span class="sxs-lookup"><span data-stu-id="fb911-126">If you are running Microsoft Hyper-V in your environment the App-V sequencer will run when the Hyper-V virtual computer it is running on is:</span></span>

    -   <span data-ttu-id="fb911-127">en pause et en reprise.</span><span class="sxs-lookup"><span data-stu-id="fb911-127">paused and resumed.</span></span>

    -   <span data-ttu-id="fb911-128">a son état enregistré et restauré.</span><span class="sxs-lookup"><span data-stu-id="fb911-128">has its state saved and restored.</span></span>

    -   <span data-ttu-id="fb911-129">enregistré en tant qu’instantané et est restauré.</span><span class="sxs-lookup"><span data-stu-id="fb911-129">saved as a snapshot and is restored.</span></span>

    -   <span data-ttu-id="fb911-130">migration vers un autre matériel dans le cadre d’une migration dynamique.</span><span class="sxs-lookup"><span data-stu-id="fb911-130">migrated to different hardware as part of a live migration.</span></span>

-   **<span data-ttu-id="fb911-131">Avant de séquencer une nouvelle application, arrêtez les autres programmes en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fb911-131">Before you sequence a new application, shut down other running programs.</span></span>**

    <span data-ttu-id="fb911-132">Les processus et tâches planifiées qui s’exécutent normalement sur l’ordinateur de séquençage peuvent ralentir le processus de séquençage et provoquer la collecte de données inappropriées lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="fb911-132">Processes and scheduled tasks that normally run on the sequencing computer can slow down the sequencing process and cause irrelevant data to be gathered during sequencing.</span></span> <span data-ttu-id="fb911-133">Toutes les applications et tous les programmes inutiles doivent être fermés avant de commencer à effectuer le séquençage.</span><span class="sxs-lookup"><span data-stu-id="fb911-133">All unnecessary applications and programs should be shut down before you begin sequencing.</span></span>

-   **<span data-ttu-id="fb911-134">Séquence sur un ordinateur exécutant un service Terminal Server</span><span class="sxs-lookup"><span data-stu-id="fb911-134">Sequence on a computer that is running Terminal Services</span></span>**

    <span data-ttu-id="fb911-135">Vous ne devez pas configurer le mode installation sur un ordinateur exécutant les services Terminal Server avant d’installer le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fb911-135">You should not configure the install mode on a computer that is running Terminal Services before you install the sequencer.</span></span>

## <span data-ttu-id="fb911-136">Recommandations en matière de séquençage</span><span class="sxs-lookup"><span data-stu-id="fb911-136">Sequencing Best Practices</span></span>


<span data-ttu-id="fb911-137">Les meilleures pratiques suivantes doivent être envisagées lors du séquençage d’une nouvelle application:</span><span class="sxs-lookup"><span data-stu-id="fb911-137">The following best practices should be considered when sequencing a new application:</span></span>

-   

    <span data-ttu-id="fb911-138">**Remarques**  Si vous exécutez App-V 4,6 SP1, vous n’avez pas besoin d’effectuer de séquence vers un répertoire qui suit la Convention de nommage 8,3.</span><span class="sxs-lookup"><span data-stu-id="fb911-138">**Note** If you are running App-V 4.6 SP1 you do not need to sequence to a directory that follows the 8.3 naming convention.</span></span>

     

-   **<span data-ttu-id="fb911-139">Séquence vers un répertoire unique qui suit la Convention d’affectation de noms 8,3.</span><span class="sxs-lookup"><span data-stu-id="fb911-139">Sequence to a unique directory that follows the 8.3 naming convention.</span></span>**

    <span data-ttu-id="fb911-140">Vous devez effectuer une séquence de toutes les applications dans un répertoire qui suit la Convention d’affectation de noms 8,3.</span><span class="sxs-lookup"><span data-stu-id="fb911-140">You should sequence all applications to a directory that follows the 8.3 naming convention.</span></span> <span data-ttu-id="fb911-141">Le nom du répertoire spécifié ne peut pas contenir plus de huit caractères, suivi d’une extension de nom de fichier à trois caractères (par exemple, **Q:\\MYAPP. ABC**.</span><span class="sxs-lookup"><span data-stu-id="fb911-141">The specified directory name cannot contain more than eight characters, followed by a three-character file name extension—for example, **Q:\\MYAPP.ABC**.</span></span>

-   **<span data-ttu-id="fb911-142">Séquence vers un dossier de destination à la racine du lecteur, et non vers un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="fb911-142">Sequence to a destination folder on the root of the drive, not to a subdirectory.</span></span>**

    <span data-ttu-id="fb911-143">Si la suite d’applications est composée de plusieurs parties, installez chaque application dans un sous-répertoire du répertoire principal.</span><span class="sxs-lookup"><span data-stu-id="fb911-143">If the application suite has multiple parts, install each application to a subdirectory of the main directory.</span></span> <span data-ttu-id="fb911-144">Par exemple, si un package contient une application conjointement avec un client, utilisez **Q:\\AppSuite** en tant qu’annuaire principal, puis séquencez l’application principale sur **Q:\\AppSuite\\Main**, puis séquencez le client sur **Q:\\AppSuite\\Client**.</span><span class="sxs-lookup"><span data-stu-id="fb911-144">For example, if a package contains an application along with a client, use **Q:\\AppSuite** as the main directory and sequence the main application to **Q:\\AppSuite\\Main**, and sequence the client to **Q:\\AppSuite\\Client**.</span></span>

-   **<span data-ttu-id="fb911-145">Configurez et testez l’application lors de la phase d’installation.</span><span class="sxs-lookup"><span data-stu-id="fb911-145">Configure and test the application during the installation phase.</span></span>**

    <span data-ttu-id="fb911-146">L’exécution de l’installation d’une application implique souvent d’effectuer plusieurs étapes manuelles qui ne font pas partie du processus d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="fb911-146">Completing the installation of an application often requires performing several manual steps that are not part of the application installation process.</span></span> <span data-ttu-id="fb911-147">Cette procédure peut impliquer la configuration d’une connexion à une base de données ou la copie des fichiers mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fb911-147">These steps can involve configuring a connection to a database or copying updated files.</span></span> <span data-ttu-id="fb911-148">Vous devez effectuer ces configurations lors de la phase d’installation, puis exécuter l’application pour vérifier qu’elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="fb911-148">You should perform these configurations during the installation phase and then run the application to make sure it works.</span></span>

-   **<span data-ttu-id="fb911-149">Exécutez l’application autant de fois que nécessaire, jusqu’à ce que le programme soit stable.</span><span class="sxs-lookup"><span data-stu-id="fb911-149">Run the application, multiple times if necessary, until the program is stable.</span></span>**

    <span data-ttu-id="fb911-150">Vous devez exécuter l’application plusieurs fois pendant l’installation pour garantir que toutes les configurations d’inscription et de boîte de dialogue associées aient été effectuées.</span><span class="sxs-lookup"><span data-stu-id="fb911-150">You should run the application multiple times during the installation to ensure all associated registration and dialog box configurations have been completed.</span></span> <span data-ttu-id="fb911-151">L’ouverture de l’application à plusieurs reprises lors de l’installation permet de garantir que seules les fonctionnalités d’application pertinentes sont chargées dans le **bloc de fonctionnalités principal**.</span><span class="sxs-lookup"><span data-stu-id="fb911-151">Opening the application multiple times during installation will ensure that only the relevant application features are loaded into the **primary feature block**.</span></span>

-   **<span data-ttu-id="fb911-152">Désactiver toutes les fonctionnalités de mise à jour automatique associées à l’application.</span><span class="sxs-lookup"><span data-stu-id="fb911-152">Disable all automatic update features associated with the application.</span></span>**

    <span data-ttu-id="fb911-153">Certaines applications peuvent vérifier automatiquement les mises à jour les plus récentes lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="fb911-153">Some applications have the ability to check for the latest updates automatically during installation.</span></span> <span data-ttu-id="fb911-154">Pour vous aider à effectuer le contrôle de version des packages d’application virtuelle, vous devez désactiver cette fonctionnalité lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="fb911-154">To assist with versioning of virtual application packages, you should disable this feature during sequencing.</span></span> <span data-ttu-id="fb911-155">S’il existe des mises à jour requises, vous devez effectuer une nouvelle création de package d’application virtuelle avec les mises à jour associées installées.</span><span class="sxs-lookup"><span data-stu-id="fb911-155">If there are required updates, you should sequence a new virtual application package with the associated updates installed.</span></span>

## <span data-ttu-id="fb911-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb911-156">Related topics</span></span>


[<span data-ttu-id="fb911-157">Planification du déploiement du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="fb911-157">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 






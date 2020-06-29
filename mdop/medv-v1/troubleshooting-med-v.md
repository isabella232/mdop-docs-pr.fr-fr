---
title: Résolution des problèmes liés à MED-V
description: Résolution des problèmes liés à MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811411"
---
# <span data-ttu-id="18c86-103">Résolution des problèmes liés à MED-V</span><span class="sxs-lookup"><span data-stu-id="18c86-103">Troubleshooting MED-V</span></span>


<span data-ttu-id="18c86-104">Cette section fournit des informations pour vous aider à résoudre les problèmes généraux liés à la virtualisation de bureau de Microsoft entreprise (MED-V).</span><span class="sxs-lookup"><span data-stu-id="18c86-104">This section provides information to help troubleshoot general issues with Microsoft Enterprise Desktop Virtualization (MED-V).</span></span>

## <span data-ttu-id="18c86-105">La modification de la résolution de l’hôte puis l’agrandissement de l’espace de travail MED-V entraîne l’affichage du bureau noir.</span><span class="sxs-lookup"><span data-stu-id="18c86-105">Changing the host resolution and then maximizing the MED-V workspace causes the desktop to appear black</span></span>


<span data-ttu-id="18c86-106">Lorsque vous travaillez en mode Bureau complet, si vous modifiez la résolution de l’hôte, puis agrandissez la fenêtre d’espace de travail MED-V, le Bureau s’affiche en noir et l’espace de travail MED-V ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="18c86-106">When working in full desktop mode, if you change the host resolution and then maximize the MED-V workspace window, the desktop appears black and the MED-V workspace might not respond.</span></span>

### <span data-ttu-id="18c86-107">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-107">Solution</span></span>

<span data-ttu-id="18c86-108">Arrêtez et démarrez l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="18c86-108">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="18c86-109">Démarrage d’un espace de travail MED-V avec un adaptateur réseau désactivé, puis l’activation ultérieure de l’adaptateur ne restaure pas la connectivité réseau</span><span class="sxs-lookup"><span data-stu-id="18c86-109">Starting a MED-V workspace with a network adapter disabled and then later enabling the adapter does not restore network connectivity</span></span>


<span data-ttu-id="18c86-110">Si vous configurez un espace de travail MED-V en mode pont et démarrez l’espace de travail MED-V alors qu’une carte réseau est désactivée, la connectivité réseau par le biais de cet adaptateur ne sera pas restaurée.</span><span class="sxs-lookup"><span data-stu-id="18c86-110">If you configure a MED-V workspace in bridge mode and then start the MED-V workspace while a network adapter is disabled, if the adapter is later enabled, the network connectivity through that adapter is not restored.</span></span>

### <span data-ttu-id="18c86-111">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-111">Solution</span></span>

<span data-ttu-id="18c86-112">Arrêtez et démarrez l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="18c86-112">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="18c86-113">Une image ne peut être utilisée que par un seul utilisateur Windows par ordinateur</span><span class="sxs-lookup"><span data-stu-id="18c86-113">An image can be used by only one Windows user per computer</span></span>


<span data-ttu-id="18c86-114">Une image d’espace de travail MED-V ne peut être utilisée que par l’utilisateur Windows qui a téléchargé ou importé l’image.</span><span class="sxs-lookup"><span data-stu-id="18c86-114">A MED-V workspace image can be used only by the Windows user who downloaded or imported the image.</span></span> <span data-ttu-id="18c86-115">Cet utilisateur est le seul à ne pas utiliser d’administrateurs disposant d’autorisations sur le dossier dans lequel se trouvent les images téléchargées.</span><span class="sxs-lookup"><span data-stu-id="18c86-115">This user is the only user aside from administrators who have permissions to the folder where the downloaded images are located.</span></span>

### <span data-ttu-id="18c86-116">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-116">Solution</span></span>

<span data-ttu-id="18c86-117">Changez manuellement la liste de contrôle d’accès (ACL) sur le magasin d’images.</span><span class="sxs-lookup"><span data-stu-id="18c86-117">Manually change the access control list (ACL) on the image store.</span></span>

## <span data-ttu-id="18c86-118">Lors de l’installation de MED-V à l’aide de Configuration Manager avec des droits d’utilisateur activés, la désinstallation échoue</span><span class="sxs-lookup"><span data-stu-id="18c86-118">When installing MED-V by using Configuration Manager with users rights enabled, uninstall fails</span></span>


<span data-ttu-id="18c86-119">Si MED-V est installé à l’aide de Microsoft System Center Configuration Manager et que le mode exécution du package a pour valeur utilisateurs, la désinstallation échoue avec un message d’erreur indiquant que seuls les utilisateurs administratifs peuvent désinstaller MED-V.</span><span class="sxs-lookup"><span data-stu-id="18c86-119">If MED-V is installed by using Microsoft System Center Configuration Manager and the run mode of the package is set to users rights, uninstall fails with an error message that says that only administrative users can uninstall MED-V.</span></span>

### <span data-ttu-id="18c86-120">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-120">Solution</span></span>

<span data-ttu-id="18c86-121">Lors de la création d’un package de gestionnaire de configuration pour MED-V, définissez le mode d’exécution sur droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="18c86-121">When creating a Configuration Manager package for MED-V, set the run mode to administrative rights.</span></span>

## <span data-ttu-id="18c86-122">Lors de l’installation de MED-V à l’aide d’un système de déploiement d’entreprise, où l’installation est configurée pour exécuter le client après l’installation, vous ne pouvez pas exécuter le client.</span><span class="sxs-lookup"><span data-stu-id="18c86-122">When installing MED-V by using a corporate deployment system, where the installation is configured to run the client following installation, you cannot run the client</span></span>


<span data-ttu-id="18c86-123">Si MED-V est installé à l’aide d’un système de déploiement d’entreprise et que le package d’installation est configuré pour exécuter un client MED-V après l’installation, une fois le client exécuté sous le compte système, vous ne pouvez pas voir que le client s’exécute (sauf dans la zone de notification) et que vous ne pouvez pas interagir avec ce dernier.</span><span class="sxs-lookup"><span data-stu-id="18c86-123">If MED-V is installed by using a corporate deployment system and the installation package is configured to run MED-V client following the installation, after the client is running under the system account, you cannot see that the client is running (except in the notification area), and you cannot interact with it.</span></span>

### <span data-ttu-id="18c86-124">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-124">Solution</span></span>

<span data-ttu-id="18c86-125">Lors de l’installation de MED-V à l’aide d’un système de déploiement d’entreprise, utilisez le paramètre *Start \ _MEDV = 0* . msi.</span><span class="sxs-lookup"><span data-stu-id="18c86-125">When installing MED-V by using a corporate deployment system, use the *START\_MEDV=0* .msi parameter.</span></span>

## <span data-ttu-id="18c86-126">Échec du démarrage de l’image de test MED-V</span><span class="sxs-lookup"><span data-stu-id="18c86-126">MED-V test image fails to start</span></span>


<span data-ttu-id="18c86-127">Si une image de test MED-V ne démarre pas, elle ne sera jamais récupérée et tous les démarrages futurs échoueront avec un message d’erreur «Impossible de charger GINA».</span><span class="sxs-lookup"><span data-stu-id="18c86-127">If a MED-V test image fails to start, it will never recover and all future startups will fail with a “GINA fail to load” error message.</span></span>

### <span data-ttu-id="18c86-128">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-128">Solution</span></span>

<span data-ttu-id="18c86-129">Supprimez l’image de test existante, puis recréez-la.</span><span class="sxs-lookup"><span data-stu-id="18c86-129">Delete the existing test image and then re-create it.</span></span>

## <span data-ttu-id="18c86-130">Après avoir essayé de rejoindre un domaine avec des informations d’identification incorrectes, l’image ne fonctionne jamais dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="18c86-130">After attempting to join a domain with the wrong credentials, the image never succeeds in joining the domain</span></span>


<span data-ttu-id="18c86-131">S’il existe une erreur de configuration dans le bloc de construction de domaine de jointure, qui fait partie du script de configuration de l’ordinateur virtuel pour la première fois, l’espace de travail MED-V peut échouer lorsque vous essayez de rejoindre un domaine.</span><span class="sxs-lookup"><span data-stu-id="18c86-131">If there is a configuration error in the join domain building block, which is part of the virtual machine first-time setup script, it causes the MED-V workspace to fail when attempting to join a domain.</span></span> <span data-ttu-id="18c86-132">Une fois l’erreur de configuration réparée, l’image incluse dans l’espace de travail MED-V ne peut pas rejoindre le domaine.</span><span class="sxs-lookup"><span data-stu-id="18c86-132">After the configuration error is repaired, the image included in the MED-V workspace cannot join the domain.</span></span>

### <span data-ttu-id="18c86-133">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-133">Solution</span></span>

<span data-ttu-id="18c86-134">Si l’image a été déployée, redistribuez l’image.</span><span class="sxs-lookup"><span data-stu-id="18c86-134">If the image was deployed, redistribute the image.</span></span> <span data-ttu-id="18c86-135">Si l’image est une image de test, recréez l’image.</span><span class="sxs-lookup"><span data-stu-id="18c86-135">If the image was a test image, re-create the image.</span></span>

## <span data-ttu-id="18c86-136">MED-V ne prend pas en charge plusieurs moniteurs</span><span class="sxs-lookup"><span data-stu-id="18c86-136">MED-V does not support multiple monitors</span></span>


<span data-ttu-id="18c86-137">MED-V ne prend pas en charge l’affichage des applications publiées sur plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="18c86-137">MED-V does not support displaying published applications across multiple monitors.</span></span> <span data-ttu-id="18c86-138">Les applications et les applications clientes publiées peuvent s’afficher sur l’écran incorrect, et parfois après la déconnexion d’un écran, MED-V tente d’envoyer l’écran à l’écran de sorte que le moniteur connecté reste vide.</span><span class="sxs-lookup"><span data-stu-id="18c86-138">Published applications and other client windows may be displayed in the wrong screen, and sometimes after a screen is disconnected, MED-V attempts to send the screen to the monitor so that the connected monitor appears blank.</span></span>

### <span data-ttu-id="18c86-139">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-139">Solution</span></span>

<span data-ttu-id="18c86-140">Déconnectez l’écran supplémentaire, puis redémarrez le client.</span><span class="sxs-lookup"><span data-stu-id="18c86-140">Disconnect the additional screen, and restart the client.</span></span>

## <span data-ttu-id="18c86-141">Le démarrage de l’espace de travail MED-V peut échouer si l’hôte se bloque lors du démarrage d’un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="18c86-141">MED-V workspace might fail to start if the host crashes during MED-V workspace startup</span></span>


<span data-ttu-id="18c86-142">Si l’hôte se bloque pendant le processus de démarrage d’un espace de travail MED-V et qu’un message d’erreur s’affiche et indique «élément racine manquant», l’espace de travail MED-V peut ajouter des données à un fichier de configuration de machine virtuelle vide</span><span class="sxs-lookup"><span data-stu-id="18c86-142">If the host crashes during the MED-V workspace startup process and an error message appears that says “Root element is missing,” the MED-V workspace might add data to an empty virtual machine configuration (VMC) file, which will cause the startup process to fail.</span></span>

### <span data-ttu-id="18c86-143">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-143">Solution</span></span>

<span data-ttu-id="18c86-144">Remplacez le fichier VMC vide par un fichier VMC de l’image de base.</span><span class="sxs-lookup"><span data-stu-id="18c86-144">Replace the empty VMC file with a VMC file from the base image.</span></span>

## <span data-ttu-id="18c86-145">Le clavier ne répond pas dans les fenêtres d’application publiées</span><span class="sxs-lookup"><span data-stu-id="18c86-145">The keyboard does not respond in published application windows</span></span>


<span data-ttu-id="18c86-146">Dans un espace de travail MED-V, si vous appuyez sur la touche du logo Windows lorsque l’application publiée est activée, le clavier ne répond plus dans les fenêtres d’application publiées.</span><span class="sxs-lookup"><span data-stu-id="18c86-146">In a MED-V workspace, if you press the Windows logo key when a published application is in focus, the keyboard no longer responds in published application windows.</span></span>

### <span data-ttu-id="18c86-147">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-147">Solution</span></span>

<span data-ttu-id="18c86-148">Appuyez sur la touche du logo Windows alors qu’une application publiée a le focus.</span><span class="sxs-lookup"><span data-stu-id="18c86-148">Press the Windows logo key while a published application is in focus.</span></span>

## <span data-ttu-id="18c86-149">Un espace de travail MED-V de domaine ne met pas à jour les informations d’identification de domaine</span><span class="sxs-lookup"><span data-stu-id="18c86-149">A domain MED-V workspace does not update domain credentials</span></span>


<span data-ttu-id="18c86-150">Lors de l’utilisation d’un espace de travail MED-V persistant dans un environnement de domaine, si vous modifiez le mot de passe de votre domaine, le client MED-V ne met pas à jour les informations d’identification du domaine d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="18c86-150">When using a persistent MED-V workspace in a domain environment, if you change your domain password, the MED-V client does not update the MED-V workspace domain credentials.</span></span> <span data-ttu-id="18c86-151">Lorsqu’une application publiée tente d’accéder à une ressource réseau, vous recevez un message d’erreur vous informant que vos informations d’identification ont expiré.</span><span class="sxs-lookup"><span data-stu-id="18c86-151">When a published application attempts to access a network resource, you will receive an error message notifying you that your credentials expired.</span></span>

### <span data-ttu-id="18c86-152">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-152">Solution</span></span>

<span data-ttu-id="18c86-153">Redémarrez le système d’exploitation de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="18c86-153">Restart the MED-V workspace operating system.</span></span>

## <span data-ttu-id="18c86-154">Les fenêtres d’application publiées optimisées couvrent la barre des tâches hôte</span><span class="sxs-lookup"><span data-stu-id="18c86-154">Maximized published application windows cover the host taskbar</span></span>


<span data-ttu-id="18c86-155">Si vous agrandissez une fenêtre d’application publiée au mode plein écran, il est possible que la barre des tâches hôte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="18c86-155">If you maximize a published application window to full screen, it might cover the host taskbar.</span></span>

### <span data-ttu-id="18c86-156">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-156">Solution</span></span>

<span data-ttu-id="18c86-157">Effectuez l'une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="18c86-157">Do one of the following:</span></span>

<span data-ttu-id="18c86-158">Réduisez la fenêtre de l’application publiée pour accéder à la zone de notification, puis redémarrez l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="18c86-158">Minimize the published application window to gain access to the notification area, and restart the MED-V workspace.</span></span>

<span data-ttu-id="18c86-159">Réduisez la fenêtre de l’application publiée, puis restaurez la fenêtre à son état agrandi.</span><span class="sxs-lookup"><span data-stu-id="18c86-159">Minimize the published application window, and then restore the window to its maximized state.</span></span>

## <span data-ttu-id="18c86-160">L’ajout d’utilisateurs ou de groupes dans le gestionnaire de configuration du serveur MED-V ne fonctionne pas</span><span class="sxs-lookup"><span data-stu-id="18c86-160">Adding users or groups in the MED-V Server Configuration Manager does not work</span></span>


<span data-ttu-id="18c86-161">Lorsque vous ajoutez des utilisateurs ou des groupes dans la boîte de dialogue **Sélectionner des utilisateurs ou des groupes** , les utilisateurs ou groupes sélectionnés ne sont pas ajoutés à la liste de contrôle d’accès dans le gestionnaire de configuration de MED-V Server.</span><span class="sxs-lookup"><span data-stu-id="18c86-161">When adding users or groups in the **Select Users or Groups** dialog box, the selected users or groups are not added to the access control list in the MED-V Server Configuration Manager.</span></span>

### <span data-ttu-id="18c86-162">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-162">Solution</span></span>

<span data-ttu-id="18c86-163">Ajoutez des utilisateurs ou des groupes à l’aide de la boîte de dialogue **entrer un nom d’utilisateur ou de groupe** .</span><span class="sxs-lookup"><span data-stu-id="18c86-163">Add users or groups using the **Enter User or Group names** dialog box.</span></span> <span data-ttu-id="18c86-164">Pour en savoir plus, voir [Comment installer et configurer le composant serveur MED-V](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span><span class="sxs-lookup"><span data-stu-id="18c86-164">For detailed information, see [How to Install and Configure the MED-V Server Component](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span></span>

## <span data-ttu-id="18c86-165">MED-V ne fonctionne pas sur les ordinateurs sur lesquels Windows Virtual PC pour Windows 7 est installé</span><span class="sxs-lookup"><span data-stu-id="18c86-165">MED-V does not work on computers with Windows Virtual PC for Windows 7 installed</span></span>


<span data-ttu-id="18c86-166">MED-V nécessite Windows Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="18c86-166">MED-V requires Windows Virtual PC2007.</span></span> <span data-ttu-id="18c86-167">Le PC virtuel pour Windows et Virtual PC2007 SP1 ne peuvent pas être installés sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="18c86-167">Windows Virtual PC for Windows7 and Virtual PC2007 SP1 cannot be installed on the same computer.</span></span>

### <span data-ttu-id="18c86-168">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-168">Solution</span></span>

<span data-ttu-id="18c86-169">Désinstaller Virtual PC pour plus d’applications avant d’installer Virtual PC2007 SP1 et MED-V.</span><span class="sxs-lookup"><span data-stu-id="18c86-169">Uninstall Virtual PC for Windows7 before installing Virtual PC2007 SP1 and MED-V.</span></span>

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a><span data-ttu-id="18c86-170">MED-V ne prend pas en charge les images du mode PC virtuel et WindowsXP</span><span class="sxs-lookup"><span data-stu-id="18c86-170">MED-V does not support Virtual PC and WindowsXP Mode images</span></span>


<span data-ttu-id="18c86-171">MED-V 1.0 SP1 ne prend pas en charge les images créées par le PC virtuel Windows pour une application.</span><span class="sxs-lookup"><span data-stu-id="18c86-171">MED-V1.0 SP1 does not support images created by Windows Virtual PC for Windows7.</span></span> <span data-ttu-id="18c86-172">Si une image virtuelle pour une utilisation est utilisée, le client ne peut pas démarrer.</span><span class="sxs-lookup"><span data-stu-id="18c86-172">If a Virtual PC for Windows7 image is used, the client will fail during startup.</span></span>

### <span data-ttu-id="18c86-173">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-173">Solution</span></span>

<span data-ttu-id="18c86-174">Créer des images MED-V en utilisant Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="18c86-174">Create MED-V images by using Virtual PC2007 SP1.</span></span>

## <span data-ttu-id="18c86-175">Le pare-feu Windows bloque l’activité du réseau PC2007 SP1 virtuel</span><span class="sxs-lookup"><span data-stu-id="18c86-175">Windows firewall blocks Virtual PC2007 SP1 network activity</span></span>


<span data-ttu-id="18c86-176">Par défaut, le pare-feu Windows bloque l’activité du réseau PC2007 SP1 virtuel et, lorsque le service SP1 virtuel PC2007 s’exécute sur l’ordinateur client, il existe un message de pare-feu qui bloque la séquence de démarrage et l’accès au réseau.</span><span class="sxs-lookup"><span data-stu-id="18c86-176">By default, Windows firewall blocks Virtual PC2007 SP1 network activity, and when Virtual PC2007 SP1 initiates on the client computer, there is a firewall message that blocks its startup sequence and all network access.</span></span>

### <span data-ttu-id="18c86-177">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-177">Solution</span></span>

<span data-ttu-id="18c86-178">Mettez à jour l’exception de pare-feu à l’aide de la stratégie de groupe avant MED-V, qui est utilisée par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="18c86-178">Update the firewall exception by using Group Policy before MED-V is used by the end user.</span></span>

## <span data-ttu-id="18c86-179">Lors de la mise à niveau du client, un message d’erreur s’affiche</span><span class="sxs-lookup"><span data-stu-id="18c86-179">When upgrading the client an error message appears</span></span>


<span data-ttu-id="18c86-180">Lors de la mise à niveau du client de MED-V 1.0 vers MED-V 1.0 SP1, un message peut apparaître indiquant qu’aucun espace de travail MED-V n’est défini.</span><span class="sxs-lookup"><span data-stu-id="18c86-180">When upgrading the client from MED-V1.0 to MED-V1.0 SP1, a message may appear notifying you that no MED-V workspace is defined.</span></span>

### <span data-ttu-id="18c86-181">Solution</span><span class="sxs-lookup"><span data-stu-id="18c86-181">Solution</span></span>

<span data-ttu-id="18c86-182">Fermez le client et redémarrez-le.</span><span class="sxs-lookup"><span data-stu-id="18c86-182">Close the client and restart it.</span></span>

## <span data-ttu-id="18c86-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18c86-183">Related topics</span></span>


[<span data-ttu-id="18c86-184">Notes de publication pour MED-V1.0</span><span class="sxs-lookup"><span data-stu-id="18c86-184">MED-V 1.0 Release Notes</span></span>](med-v-10-release-notesmedv-10.md)

[<span data-ttu-id="18c86-185">Notes de publication pour MED-V1.0 SP1 et SP2</span><span class="sxs-lookup"><span data-stu-id="18c86-185">MED-V 1.0 SP1 and SP2 Release Notes</span></span>](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 






---
title: Déploiement d'App-V5.0 Sequencer et Client
description: Déploiement d'App-V5.0 Sequencer et Client
author: dansimp
ms.assetid: 84cc84bd-5bc0-41aa-9519-0ded2932c078
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 647ea12018bf966592b9e831d532c7c08093d367
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805845"
---
# <span data-ttu-id="240a8-103">Déploiement d'App-V5.0 Sequencer et Client</span><span class="sxs-lookup"><span data-stu-id="240a8-103">Deploying the App-V 5.0 Sequencer and Client</span></span>


<span data-ttu-id="240a8-104">Le client et le Sequencer App-V 5,0 permettent aux administrateurs de virtualiser et d’exécuter des applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="240a8-104">The App-V 5.0 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="240a8-105">Déployer le client</span><span class="sxs-lookup"><span data-stu-id="240a8-105">Deploy the client</span></span>


<span data-ttu-id="240a8-106">Le client App-V 5,0 est le composant qui exécute une application virtualisée sur un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="240a8-106">The App-V 5.0 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="240a8-107">Le client permet aux utilisateurs d’interagir avec des icônes et de double-cliquer sur les types de fichiers de sorte qu’ils puissent démarrer une application virtualisée.</span><span class="sxs-lookup"><span data-stu-id="240a8-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="240a8-108">Le client peut également obtenir le contenu de l’application virtuelle à partir du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="240a8-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="240a8-109">Comment déployer App-V Client</span><span class="sxs-lookup"><span data-stu-id="240a8-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)

[<span data-ttu-id="240a8-110">Procédure pour désinstaller App-V5.0 Client</span><span class="sxs-lookup"><span data-stu-id="240a8-110">How to Uninstall the App-V 5.0 Client</span></span>](how-to-uninstall-the-app-v-50-client.md)

[<span data-ttu-id="240a8-111">Déploiement de l’application-V 4,6 et du client App-V 5,0 sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="240a8-111">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## <span data-ttu-id="240a8-112">Paramètres de configuration du client</span><span class="sxs-lookup"><span data-stu-id="240a8-112">Client Configuration Settings</span></span>


<span data-ttu-id="240a8-113">Le client App-V 5,0 stocke sa configuration dans le registre.</span><span class="sxs-lookup"><span data-stu-id="240a8-113">The App-V 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="240a8-114">Vous pouvez recueillir des informations utiles sur le client si vous comprenez le format des données dans le registre.</span><span class="sxs-lookup"><span data-stu-id="240a8-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="240a8-115">Vous pouvez également configurer de nombreuses actions client en modifiant des entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="240a8-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="240a8-116">À propos des paramètres de configuration du client</span><span class="sxs-lookup"><span data-stu-id="240a8-116">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

## <span data-ttu-id="240a8-117">Configurer le client à l’aide du modèle ADMX et de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="240a8-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="240a8-118">Vous pouvez utiliser le modèle Microsoft ADMX pour configurer les paramètres du client de l’application-V 5,0 et du client de services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="240a8-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.0 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="240a8-119">Le modèle ADMX gère les configurations client courantes à l’aide d’une infrastructure de stratégie de groupe existante et comprend des paramètres pour la configuration du client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="240a8-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.0 client configuration.</span></span>

<span data-ttu-id="240a8-120">**Important**  Vous pouvez obtenir le modèle App-V 5,0 ADMX à partir du centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="240a8-120">**Important** You can obtain the App-V 5.0 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="240a8-121">Après avoir téléchargé et installé le modèle ADMX, vous devez effectuer les étapes suivantes sur l’ordinateur que vous utiliserez pour gérer la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="240a8-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="240a8-122">Il s’agit généralement du contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="240a8-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="240a8-123">Enregistrez le fichier **. admx** dans le répertoire suivant: **Windows \ \ PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="240a8-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="240a8-124">Enregistrez le fichier **. adml** dans le répertoire suivant: \*\*Windows \ \ PolicyDefinitions \ \ &lt; Language Directory &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="240a8-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="240a8-125">Après avoir effectué les étapes ci-dessus, vous pouvez gérer les paramètres de configuration du client App-V 5,0 avec la console de **gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="240a8-125">After you have completed the preceding steps, you can manage the App-V 5.0 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="240a8-126">Le client App-V 5,0 stocke également sa configuration dans le registre.</span><span class="sxs-lookup"><span data-stu-id="240a8-126">The App-V 5.0 client also stores its configuration in the registry.</span></span> <span data-ttu-id="240a8-127">Vous pouvez recueillir des informations utiles sur le client si vous comprenez le format des données dans le registre.</span><span class="sxs-lookup"><span data-stu-id="240a8-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="240a8-128">Vous pouvez également configurer de nombreuses actions client en modifiant des entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="240a8-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="240a8-129">Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="240a8-129">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="240a8-130">Déploiement du client à l’aide du mode magasin de contenu partagé</span><span class="sxs-lookup"><span data-stu-id="240a8-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="240a8-131">Le mode SCS (Data content Store) App-V 5,0 permet aux clients de l' 5,0 application SCS d’exécuter des applications virtuelles sans enregistrer les données de package associées localement.</span><span class="sxs-lookup"><span data-stu-id="240a8-131">The App-V 5.0 Shared Content Store (SCS) mode enables the SCS App-V 5.0 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="240a8-132">Toutes les données du package virtualisé requises sont transmises sur le réseau; par conséquent, vous devez utiliser le mode SCS uniquement dans les environnements dotés d’une connexion rapide.</span><span class="sxs-lookup"><span data-stu-id="240a8-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="240a8-133">Les services Bureau à distance et la version standard du client App-V 5,0 sont tous deux pris en charge en mode SCS.</span><span class="sxs-lookup"><span data-stu-id="240a8-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.0 client are supported with SCS mode.</span></span>

<span data-ttu-id="240a8-134">**Important**  Si le client App-V 5,0 est configuré pour s’exécuter en mode SCS, l’emplacement à partir duquel les packages App-V 5,0 doivent être diffusés doit être disponible; dans le cas contraire, le package virtuel ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="240a8-134">**Important** If the App-V 5.0 client is configured to run in the SCS mode, the location where the App-V 5.0 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="240a8-135">Par ailleurs, nous déconseillons le déploiement d’applications virtualisées sur les ordinateurs qui exécutent le client App-V 5,0 en mode SCS sur Internet.</span><span class="sxs-lookup"><span data-stu-id="240a8-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.0 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="240a8-136">Par ailleurs, le SCS n’est pas un emplacement physique contenant des packages virtualisés.</span><span class="sxs-lookup"><span data-stu-id="240a8-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="240a8-137">C’est un mode qui permet au client App-V 5,0 de diffuser les données du package virtualisé requis sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="240a8-137">It is a mode that allows the App-V 5.0 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="240a8-138">Le mode SCS est utile dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="240a8-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="240a8-139">Déploiements VDI (Virtual Desktop Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="240a8-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="240a8-140">Déploiements de services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="240a8-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="240a8-141">Pour utiliser SCS dans votre environnement, vous devez activer le client App-V 5,0 pour qu’il s’exécute en mode SCS.</span><span class="sxs-lookup"><span data-stu-id="240a8-141">To use SCS in your environment, you must enable the App-V 5.0 client to run in SCS mode.</span></span> <span data-ttu-id="240a8-142">Ce paramètre doit être spécifié lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="240a8-142">This setting should be specified during installation.</span></span> <span data-ttu-id="240a8-143">Par défaut, le client n’est pas configuré pour utiliser le mode SCS.</span><span class="sxs-lookup"><span data-stu-id="240a8-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="240a8-144">Vous devriez installer le client en suivant la procédure suggérée si vous envisagez d’utiliser SCS.</span><span class="sxs-lookup"><span data-stu-id="240a8-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="240a8-145">Toutefois, vous pouvez configurer un client App-V 5,0 existant pour qu’il s’exécute en mode SCS en entrant la commande PowerShell suivante sur l’ordinateur exécutant le client App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="240a8-145">However, you can configure an existing App-V 5.0 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.0 client:</span></span>

**<span data-ttu-id="240a8-146">Set-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="240a8-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="240a8-147">Il peut arriver que l’administrateur précharge certaines applications virtuelles sur l’ordinateur qui exécute le client App-V 5,0 en mode SCS.</span><span class="sxs-lookup"><span data-stu-id="240a8-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.0 client in SCS mode.</span></span> <span data-ttu-id="240a8-148">Pour ce faire, vous pouvez utiliser les commandes PowerShell pour ajouter, publier et monter le package.</span><span class="sxs-lookup"><span data-stu-id="240a8-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="240a8-149">Par exemple, si un package est préinstallé sur tous les ordinateurs, l’administrateur peut ajouter, publier et monter le package à l’aide de commandes PowerShell.</span><span class="sxs-lookup"><span data-stu-id="240a8-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="240a8-150">Le package n’est pas diffusé sur le réseau, car il est stocké localement.</span><span class="sxs-lookup"><span data-stu-id="240a8-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="240a8-151">Installation d'App-V5.0 Client pour le mode Magasin de contenu partagé</span><span class="sxs-lookup"><span data-stu-id="240a8-151">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)

## <span data-ttu-id="240a8-152">Déployer le Sequencer</span><span class="sxs-lookup"><span data-stu-id="240a8-152">Deploy the Sequencer</span></span>


<span data-ttu-id="240a8-153">Le Sequencer est un outil qui permet de convertir des applications standard en packages virtuels pour le déploiement sur des ordinateurs exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="240a8-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="240a8-154">Le Sequencer permet de fournir un processus de conversion simple et prévisible avec des modifications minimales apportées aux flux de travail de séquençage antérieur.</span><span class="sxs-lookup"><span data-stu-id="240a8-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="240a8-155">De plus, le Sequencer permet aux utilisateurs de configurer plus facilement des applications afin d’activer les connexions d’applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="240a8-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="240a8-156">Pour obtenir la liste des modifications apportées au Sequencer App-V 5,0, voir [Nouveautés de l’app-v 5,0](whats-new-in-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="240a8-156">For a list of changes in the App-V 5.0 Sequencer, see [What's New in App-V 5.0](whats-new-in-app-v-50.md).</span></span>

[<span data-ttu-id="240a8-157">Installation de Sequencer</span><span class="sxs-lookup"><span data-stu-id="240a8-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-client-and-sequencer-logs"></a> <span data-ttu-id="240a8-158">Journal des clients App-V 5,0 et Sequencer</span><span class="sxs-lookup"><span data-stu-id="240a8-158">App-V 5.0 Client and Sequencer logs</span></span>


<span data-ttu-id="240a8-159">Vous pouvez utiliser les informations du journal de Sequencer App-V 5,0 pour résoudre les problèmes liés à l’installation de Sequencer et aux événements opérationnels lors de l’utilisation d’App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="240a8-159">You can use the App-V 5.0 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="240a8-160">Les informations du journal relatives au Sequencer peuvent être examinées avec l' **Observateur d’événements**.</span><span class="sxs-lookup"><span data-stu-id="240a8-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="240a8-161">La ligne suivante affiche le chemin d’accès spécifique pour les événements liés au Sequencer:</span><span class="sxs-lookup"><span data-stu-id="240a8-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="240a8-162">**Journaux de l’observateur d’événements \ \ applications et services** Les événements liés au Sequencer sont précédés de **AppV \ _Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="240a8-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="240a8-163">Les événements liés au client sont précédés de **AppV \ _Client**.</span><span class="sxs-lookup"><span data-stu-id="240a8-163">Client-related events are prepended with **AppV\_Client**.</span></span>

<span data-ttu-id="240a8-164">Dans App-V 5,0 SP3, certains journaux ont été consolidés.</span><span class="sxs-lookup"><span data-stu-id="240a8-164">In App-V 5.0 SP3, some logs have been consolidated.</span></span> <span data-ttu-id="240a8-165">Voir [à propos de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="240a8-165">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <span data-ttu-id="240a8-166">Autres ressources pour le déploiement de Sequencer et de client</span><span class="sxs-lookup"><span data-stu-id="240a8-166">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="240a8-167">Déploiement d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="240a8-167">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="240a8-168">Planification d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="240a8-168">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)






 

 






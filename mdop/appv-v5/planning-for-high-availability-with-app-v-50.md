---
title: Planification de la haute disponibilité avec App-V5.0
description: Planification de la haute disponibilité avec App-V5.0
author: dansimp
ms.assetid: 6d9a6492-23f8-465c-82e5-49c863594156
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebf586de7cae19d40d76c9c0c845f93e7bd9021b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805017"
---
# <span data-ttu-id="68fa1-103">Planification de la haute disponibilité avec App-V5.0</span><span class="sxs-lookup"><span data-stu-id="68fa1-103">Planning for High Availability with App-V 5.0</span></span>


<span data-ttu-id="68fa1-104">Microsoft Application Virtualization 5,0 (App-V 5,0) les configurations système peuvent utiliser des options qui permettent de maintenir un niveau élevé de service disponible.</span><span class="sxs-lookup"><span data-stu-id="68fa1-104">Microsoft Application Virtualization 5.0 (App-V 5.0) system configurations can take advantage of options that maintain a high level of available service.</span></span>

<span data-ttu-id="68fa1-105">Utilisez les informations contenues dans les sections suivantes pour mieux comprendre les options de déploiement d’App-V 5,0 dans une configuration hautement disponible.</span><span class="sxs-lookup"><span data-stu-id="68fa1-105">Use the information in the following sections to help you understand the options to deploy App-V 5.0 in a highly available configuration.</span></span>

-   [<span data-ttu-id="68fa1-106">Prise en charge du regroupement Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="68fa1-106">Support for Microsoft SQL Server clustering</span></span>](#bkmk-sqlcluster)

-   [<span data-ttu-id="68fa1-107">Prise en charge de l’équilibrage de charge réseau IIS</span><span class="sxs-lookup"><span data-stu-id="68fa1-107">Support for IIS Network Load Balancing</span></span>](#bkmk-iisloadbal)

-   [<span data-ttu-id="68fa1-108">Prise en charge des serveurs de fichiers en cluster lors de l’exécution du mode SCS</span><span class="sxs-lookup"><span data-stu-id="68fa1-108">Support for clustered file servers when running (SCS) mode</span></span>](#bkmk-clusterscsmode)

-   [<span data-ttu-id="68fa1-109">Prise en charge de la mise en miroir Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="68fa1-109">Support for Microsoft SQL Server Mirroring</span></span>](#bkmk-sqlmirroring)

-   [<span data-ttu-id="68fa1-110">Prise en charge de Microsoft SQL Server toujours activé</span><span class="sxs-lookup"><span data-stu-id="68fa1-110">Support for Microsoft SQL Server Always On</span></span>](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a><span data-ttu-id="68fa1-111">Prise en charge du regroupement Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="68fa1-111">Support for Microsoft SQL Server clustering</span></span>


<span data-ttu-id="68fa1-112">Vous pouvez exécuter la base de données de gestion App-V et la base de données de création de rapports sur des ordinateurs exécutant des clusters Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="68fa1-112">You can run the App-V Management database and Reporting database on computers that are running Microsoft SQL Server clusters.</span></span> <span data-ttu-id="68fa1-113">Toutefois, vous devez les installer à l’aide de scripts.</span><span class="sxs-lookup"><span data-stu-id="68fa1-113">However, you must install the databases using scripts.</span></span>

<span data-ttu-id="68fa1-114">Pour obtenir des instructions, reportez-vous à la rubrique [déploiement de la base de données App-V à l’aide de scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="68fa1-114">For instructions, see [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span></span>

## <a href="" id="bkmk-iisloadbal"></a><span data-ttu-id="68fa1-115">Prise en charge de l’équilibrage de charge réseau IIS</span><span class="sxs-lookup"><span data-stu-id="68fa1-115">Support for IIS Network Load Balancing</span></span>


<span data-ttu-id="68fa1-116">Vous pouvez utiliser le service d’équilibrage de la charge réseau d’Internet Information Services (IIS) pour configurer un environnement hautement disponible pour les ordinateurs exécutant les services de gestion, de publication et de création de rapports de l’application-V 5. x.</span><span class="sxs-lookup"><span data-stu-id="68fa1-116">You can use Internet Information Services (IIS) Network Load Balancing to configure a highly available environment for computers running the App-V 5.x Management, Publishing, and Reporting services which are deployed through IIS.</span></span>

<span data-ttu-id="68fa1-117">Pour plus d’informations sur la configuration d’IIS et de l’équilibrage de charge réseau pour les ordinateurs exécutant les systèmes d’exploitation Windows Server, voir les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="68fa1-117">Review the following for more information about configuring IIS and Network Load Balancing for computers running Windows Server operating systems:</span></span>

-   <span data-ttu-id="68fa1-118">Fournit des informations sur la configuration d’Internet Information Services (IIS) 7,0.</span><span class="sxs-lookup"><span data-stu-id="68fa1-118">Provides information about configuring Internet Information Services (IIS) 7.0.</span></span>

    <span data-ttu-id="68fa1-119">Garantir [une disponibilité et une évolutivité élevées-ARR et NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span><span class="sxs-lookup"><span data-stu-id="68fa1-119">[Achieving High Availability and Scalability - ARR and NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span></span>

-   <span data-ttu-id="68fa1-120">Configuration de Microsoft Windows Server</span><span class="sxs-lookup"><span data-stu-id="68fa1-120">Configuring Microsoft Windows Server</span></span>

    <span data-ttu-id="68fa1-121">[Équilibrage de charge réseau](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .</span><span class="sxs-lookup"><span data-stu-id="68fa1-121">[Network Load Balancing](https://go.microsoft.com/fwlink/?LinkId=316370) (https://go.microsoft.com/fwlink/?LinkId=316370).</span></span>

    <span data-ttu-id="68fa1-122">Ces informations s’appliquent également aux clusters d’équilibrage de charge réseau IIS (NLB) dans Windows Server 2008, Windows Server2008R2 ou Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="68fa1-122">This information also applies to IIS Network Load Balancing (NLB) clusters in Windows Server2008, Windows Server2008R2, or Windows Server2012.</span></span>

    <span data-ttu-id="68fa1-123">**Remarques**  La fonctionnalité d’équilibrage de charge réseau IIS dans Windows Server2012 est généralement la même que dans Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="68fa1-123">**Note** The IIS Network Load Balancing functionality in Windows Server2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="68fa1-124">Toutefois, certains détails de la tâche sont modifiés dans Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="68fa1-124">However, some task details are changed in Windows Server2012.</span></span> <span data-ttu-id="68fa1-125">Pour plus d’informations sur les nouvelles manières de procéder, voir [tâches de gestion courantes et navigation dans Windows server 2012 R2 Preview et Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .</span><span class="sxs-lookup"><span data-stu-id="68fa1-125">For information on new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) (https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

     

## <a href="" id="bkmk-clusterscsmode"></a><span data-ttu-id="68fa1-126">Prise en charge des serveurs de fichiers en cluster lors de l’exécution du mode SCS</span><span class="sxs-lookup"><span data-stu-id="68fa1-126">Support for clustered file servers when running (SCS) mode</span></span>


<span data-ttu-id="68fa1-127">L’exécution de App-V 5,0 en mode de partage de contenu (SCS) avec des serveurs de fichiers groupés est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="68fa1-127">Running App-V 5.0 in Share Content Store (SCS) mode with clustered file servers is supported.</span></span>

<span data-ttu-id="68fa1-128">Les étapes suivantes peuvent être utilisées pour activer cette configuration:</span><span class="sxs-lookup"><span data-stu-id="68fa1-128">The following steps can be used to enable this configuration:</span></span>

-   <span data-ttu-id="68fa1-129">Configurez App-V 5,0 pour qu’il s’exécute en mode SCS du client.</span><span class="sxs-lookup"><span data-stu-id="68fa1-129">Configure App-V 5.0 to run in client SCS mode.</span></span> <span data-ttu-id="68fa1-130">Pour plus d’informations sur la configuration du mode SCS App-V 5,0, voir [Comment installer le client App-v 5,0 pour le mode magasin de contenu partagé](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md).</span><span class="sxs-lookup"><span data-stu-id="68fa1-130">For more information about configuring App-V 5.0 SCS mode, see [How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md).</span></span>

-   <span data-ttu-id="68fa1-131">Configurez le cluster de serveurs de fichiers configuré à la fois dans le mode de mise à l’échelle Microsoft Server2012 et le mode pre **2012** avec un réseau San virtuel.</span><span class="sxs-lookup"><span data-stu-id="68fa1-131">Configure the file server cluster configured in both the Microsoft Server2012 scale out mode and pre **2012** mode with a virtual SAN.</span></span>

<span data-ttu-id="68fa1-132">Les étapes suivantes peuvent être utilisées pour valider la configuration:</span><span class="sxs-lookup"><span data-stu-id="68fa1-132">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="68fa1-133">Ajoutez un package sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="68fa1-133">Add a package on the publishing server.</span></span> <span data-ttu-id="68fa1-134">Pour plus d’informations sur l’ajout d’un package, voir [comment ajouter ou mettre à niveau des packages à l’aide de la console de gestion](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="68fa1-134">For more information about adding a package, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="68fa1-135">Effectuez une actualisation de publication sur l’ordinateur exécutant le client App-V 5,0 et ouvrez une application.</span><span class="sxs-lookup"><span data-stu-id="68fa1-135">Perform a publishing refresh on the computer running the App-V 5.0 client and open an application.</span></span>

3.  <span data-ttu-id="68fa1-136">Basculer entre les nœuds de cluster pour la publication et l’actualisation des flux de travail pour garantir le fonctionnement correct du basculement.</span><span class="sxs-lookup"><span data-stu-id="68fa1-136">Switch cluster nodes mid-publishing refresh and mid-streaming to ensure fail-over works correctly.</span></span>

<span data-ttu-id="68fa1-137">Pour plus d’informations sur la configuration des clusters de basculement de Windows Server, voir les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="68fa1-137">Review the following for more information about configuring Windows Server Failover clusters:</span></span>

-   <span data-ttu-id="68fa1-138">[Liste de contrôle: créer un serveur de fichiers groupés](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .</span><span class="sxs-lookup"><span data-stu-id="68fa1-138">[Checklist: Create a Clustered File Server](https://go.microsoft.com/fwlink/?LinkId=316372) (https://go.microsoft.com/fwlink/?LinkId=316372).</span></span>

-   <span data-ttu-id="68fa1-139">[Utiliser des volumes partagés de cluster dans un cluster de basculement Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .</span><span class="sxs-lookup"><span data-stu-id="68fa1-139">[Use Cluster Shared Volumes in a Windows Server 2012 Failover Cluster](https://go.microsoft.com/fwlink/?LinkId=316373) (https://go.microsoft.com/fwlink/?LinkId=316373).</span></span>

## <a href="" id="bkmk-sqlmirroring"></a><span data-ttu-id="68fa1-140">Prise en charge de la mise en miroir Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="68fa1-140">Support for Microsoft SQL Server Mirroring</span></span>


<span data-ttu-id="68fa1-141">À l’aide de la mise en miroir de Microsoft SQL Server, où la base de données App-V 5,0 Management Server est mise en miroir à l’aide de deux instances SQL Server, les bases de données du serveur de gestion des applications-V 5,0 sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="68fa1-141">Using Microsoft SQL Server mirroring, where the App-V 5.0 management server database is mirrored utilizing two SQL Server instances, for App-V 5.0 management server databases is supported.</span></span>

<span data-ttu-id="68fa1-142">Pour plus d’informations sur la configuration de la mise en miroir de Microsoft SQL Server, voir les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="68fa1-142">Review the following for more information about configuring Microsoft SQL Server Mirroring:</span></span>

-   <span data-ttu-id="68fa1-143">[Procédure: préparation d’une base de données miroir pour la mise en miroir (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span><span class="sxs-lookup"><span data-stu-id="68fa1-143">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span></span>

-   <span data-ttu-id="68fa1-144">[Établir une session de mise en miroir de la base de données à l’aide de l’authentification Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span><span class="sxs-lookup"><span data-stu-id="68fa1-144">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span></span>

<span data-ttu-id="68fa1-145">Les étapes suivantes peuvent être utilisées pour valider la configuration:</span><span class="sxs-lookup"><span data-stu-id="68fa1-145">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="68fa1-146">Lancez une session de mise en miroir Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="68fa1-146">Initiate a Microsoft SQL Server Mirroring session.</span></span>

2.  <span data-ttu-id="68fa1-147">Sélectionnez **basculement** pour désigner une nouvelle instance principale de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="68fa1-147">Select **Failover** to designate a new master Microsoft SQL Server instance.</span></span>

3.  <span data-ttu-id="68fa1-148">Vérifiez que le serveur de gestion App-V 5,0 continue de fonctionner comme prévu après le basculement.</span><span class="sxs-lookup"><span data-stu-id="68fa1-148">Verify that the App-V 5.0 management server continues to function as expected after the failover.</span></span>

<span data-ttu-id="68fa1-149">Vous pouvez modifier la chaîne de connexion sur le serveur de gestion pour inclure le \*\*partenaire de basculement = &lt; Server2 &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="68fa1-149">The connection string on the management server can be modified to include **failover partner = &lt;server2&gt;**.</span></span> <span data-ttu-id="68fa1-150">Cette option n’est utile que lorsque le principal sur le miroir a basculé sur le secondaire et que l’ordinateur exécutant le client App-V 5,0 effectue une nouvelle connexion (par exemple, après un redémarrage).</span><span class="sxs-lookup"><span data-stu-id="68fa1-150">This will only help when the primary on the mirror has failed over to the secondary and the computer running the App-V 5.0 client is doing a fresh connection (say after reboot).</span></span>

<span data-ttu-id="68fa1-151">Procédez comme suit pour modifier la chaîne de connexion afin d’inclure le \*\*partenaire de basculement = &lt; Server2 &gt; \*\*:</span><span class="sxs-lookup"><span data-stu-id="68fa1-151">Use the following steps to modify the connection string to include **failover partner = &lt;server2&gt;**:</span></span>

<span data-ttu-id="68fa1-152">**Important**  Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="68fa1-152">**Important** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="68fa1-153">Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows.</span><span class="sxs-lookup"><span data-stu-id="68fa1-153">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="68fa1-154">Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre.</span><span class="sxs-lookup"><span data-stu-id="68fa1-154">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="68fa1-155">Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus.</span><span class="sxs-lookup"><span data-stu-id="68fa1-155">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="68fa1-156">Changez de Registre à vos propres risques.</span><span class="sxs-lookup"><span data-stu-id="68fa1-156">Change the registry at your own risk.</span></span>

 

1.  <span data-ttu-id="68fa1-157">Connectez-vous au serveur de gestion et ouvrez **regedit**.</span><span class="sxs-lookup"><span data-stu-id="68fa1-157">Login to the management server and open **regedit**.</span></span>

2.  <span data-ttu-id="68fa1-158">Accédez à **HKEY \ _LOCAL \ _MACHINE**  \\  **logiciel**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **ManagementService**.</span><span class="sxs-lookup"><span data-stu-id="68fa1-158">Navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Server** \\ **ManagementService**.</span></span>

3.  <span data-ttu-id="68fa1-159">Modifiez la valeur **gestion \ _SQL \ _CONNECTION \ _STRING** par le \*\*partenaire de basculement = &lt; Server2 &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="68fa1-159">Modify the **MANAGEMENT\_SQL\_CONNECTION\_STRING** value with the **failover partner = &lt;server2&gt;**.</span></span>

4.  <span data-ttu-id="68fa1-160">Redémarrez le service de gestion à l’aide de la console IIS.</span><span class="sxs-lookup"><span data-stu-id="68fa1-160">Restart management service using the IIS console.</span></span>

    <span data-ttu-id="68fa1-161">**Remarques**  La mise en miroir de la base de données se trouve sur la liste des fonctionnalités du moteur de base de données déconseillé pour Microsoft SQL Server2012 en raison de la fonctionnalité **AlwaysOn** disponible dans Microsoft sql Server 2012.</span><span class="sxs-lookup"><span data-stu-id="68fa1-161">**Note** Database Mirroring is on the list of Deprecated Database Engine Features for Microsoft SQL Server2012 due to the **AlwaysOn** feature available with Microsoft SQL Server 2012.</span></span>

     

<span data-ttu-id="68fa1-162">Pour plus d’informations, cliquez sur l’un des liens suivants:</span><span class="sxs-lookup"><span data-stu-id="68fa1-162">Click any of the following links for more information:</span></span>

-   <span data-ttu-id="68fa1-163">[Procédure: préparation d’une base de données miroir pour la mise en miroir (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .</span><span class="sxs-lookup"><span data-stu-id="68fa1-163">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) (https://go.microsoft.com/fwlink/?LinkId=394235).</span></span>

-   <span data-ttu-id="68fa1-164">[Procédure: configurer une session de mise en miroir de base de données (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .</span><span class="sxs-lookup"><span data-stu-id="68fa1-164">[How to: Configure a Database Mirroring Session (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) (https://go.microsoft.com/fwlink/?LinkId=394236).</span></span>

-   <span data-ttu-id="68fa1-165">[Etablissez une session de mise en miroir de la base de données à l’aide de l’authentification Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .</span><span class="sxs-lookup"><span data-stu-id="68fa1-165">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) (https://go.microsoft.com/fwlink/?LinkId=394237).</span></span>

-   <span data-ttu-id="68fa1-166">[Fonctionnalités du moteur de base de données déconseillées dans SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .</span><span class="sxs-lookup"><span data-stu-id="68fa1-166">[Deprecated Database Engine Features in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) (https://go.microsoft.com/fwlink/?LinkId=394238).</span></span>

## <a href="" id="bkmk-sqlalwayson"></a><span data-ttu-id="68fa1-167">Prise en charge de Microsoft SQL Server toujours sur la configuration</span><span class="sxs-lookup"><span data-stu-id="68fa1-167">Support for Microsoft SQL Server Always On configuration</span></span>


<span data-ttu-id="68fa1-168">La base de données du serveur de gestion de l’application-V 5,0 prend en charge les déploiements sur des ordinateurs exécutant Microsoft SQL Server avec la configuration **toujours active** .</span><span class="sxs-lookup"><span data-stu-id="68fa1-168">The App-V 5.0 management server database supports deployments to computers running Microsoft SQL Server with the **Always On** configuration.</span></span>

## <span data-ttu-id="68fa1-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68fa1-169">Related topics</span></span>


[<span data-ttu-id="68fa1-170">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="68fa1-170">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 






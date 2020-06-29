---
title: Configurer l'équilibrage de la charge réseau pour MBAM
description: Configurer l'équilibrage de la charge réseau pour MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811201"
---
# <span data-ttu-id="c585f-103">Configurer l'équilibrage de la charge réseau pour MBAM</span><span class="sxs-lookup"><span data-stu-id="c585f-103">How to Configure Network Load Balancing for MBAM</span></span>


<span data-ttu-id="c585f-104">Pour vérifier que vous remplissez les conditions préalables et que la configuration matérielle et logicielle requise pour l’installation de la fonctionnalité d’administration et de surveillance du serveur est satisfaites, consultez la configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et les [configurations MBAM 1,0 prises en charge](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c585f-104">To verify that you have met the prerequisites and hardware and software requirements to install the Administration and Monitoring Server feature, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="c585f-105">**Remarques**  Pour obtenir les fichiers journaux d’installation, vous devez installer Microsoft BitLocker administration et la surveillance (MBAM) à l’aide du package **msiexec** et de l’option **/l** &lt; emplacement &gt; .</span><span class="sxs-lookup"><span data-stu-id="c585f-105">**Note** To obtain the setup log files, you must install Microsoft BitLocker Administration and Monitoring (MBAM) by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="c585f-106">Les fichiers journaux sont créés à l’emplacement que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="c585f-106">The Log files are created in the location that you specify.</span></span>

<span data-ttu-id="c585f-107">D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% de l’utilisateur qui installe MBAM.</span><span class="sxs-lookup"><span data-stu-id="c585f-107">Additional setup log files are created in the %temp% folder of the user who installs MBAM.</span></span>

 

<span data-ttu-id="c585f-108">Les clusters de l’équilibrage de charge réseau (NLB) pour la fonctionnalité d’administration et de surveillance du serveur offrent une extensibilité dans MBAM et devraient prendre en charge plus de 55 000 ordinateurs client MBAM.</span><span class="sxs-lookup"><span data-stu-id="c585f-108">The Network Load Balancing (NLB) clusters for the Administration and Monitoring Server feature provides scalability in MBAM and it should support more than 55,000 MBAM client computers.</span></span>

<span data-ttu-id="c585f-109">**Remarques**  L’équilibrage de charge réseau de Windows Server répartit les demandes de clients sur un ensemble de serveurs configurés dans un seul cluster de serveur.</span><span class="sxs-lookup"><span data-stu-id="c585f-109">**Note** Windows Server Network Load Balancing distributes client requests across a set of servers that are configured into a single server cluster.</span></span> <span data-ttu-id="c585f-110">Lors de l’installation de l’équilibrage de charge réseau sur chacun des serveurs (hôtes) d’un cluster, le cluster présente une adresse IP virtuelle ou un nom de domaine complet (FQDN) aux demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="c585f-110">When Network Load Balancing is installed on each of the servers (hosts) in a cluster, the cluster presents a virtual IP address or fully qualified domain name (FQDN) to client requests.</span></span> <span data-ttu-id="c585f-111">Les requêtes du client initial sont dirigées vers tous les hôtes du cluster, mais un seul hôte accepte et gère la requête.</span><span class="sxs-lookup"><span data-stu-id="c585f-111">The initial client requests go to all the hosts in the cluster, but only one host accepts and handles the request.</span></span>

<span data-ttu-id="c585f-112">Tous les ordinateurs qui font partie d’un cluster NLB présentent les exigences suivantes:</span><span class="sxs-lookup"><span data-stu-id="c585f-112">All computers that will be part of a NLB cluster have the following requirements:</span></span>

-   <span data-ttu-id="c585f-113">Tous les ordinateurs du cluster NLB doivent se trouver dans le même domaine.</span><span class="sxs-lookup"><span data-stu-id="c585f-113">All computers in the NLB cluster must be in the same domain.</span></span>

-   <span data-ttu-id="c585f-114">Chaque ordinateur du cluster NLB doit utiliser une adresse IP statique.</span><span class="sxs-lookup"><span data-stu-id="c585f-114">Each computer in the NLB cluster must use a static IP address.</span></span>

-   <span data-ttu-id="c585f-115">L’équilibrage de charge réseau doit être activé sur chaque ordinateur du cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-115">Each computer in the NLB cluster must have Network Load Balancing enabled.</span></span>

-   <span data-ttu-id="c585f-116">Le cluster NLB nécessite une adresse IP statique, et un enregistrement hôte doit être créé manuellement dans le DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="c585f-116">The NLB cluster requires a static IP address, and a host record must be manually created in the domain name system (DNS).</span></span>

 

## <span data-ttu-id="c585f-117">Configuration de l’équilibrage de charge réseau pour les serveurs d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="c585f-117">Configuring Network Load Balancing for MBAM Administration and Monitoring Servers</span></span>


<span data-ttu-id="c585f-118">Les étapes suivantes expliquent comment configurer un nom virtuel de cluster NLB et une adresse IP pour deux serveurs d’administration et de surveillance de MBAM, et comment configurer des clients MBAM pour utiliser le cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-118">The following steps describe how to configure an NLB cluster virtual name and IP address for two MBAM Administration and Monitoring servers, and how to configure MBAM Clients to use the NLB Cluster.</span></span>

<span data-ttu-id="c585f-119">Avant de commencer les procédures décrites dans cette rubrique, vous devez disposer de la fonctionnalité de serveur d’administration et de surveillance de MBAM à l’aide de la même liaison de port IIS sur deux ordinateurs serveur distincts qui répondent à la configuration requise pour l’installation de la fonctionnalité MBAM Server et la configuration du cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-119">Before you begin the procedures described in this topic, you must have the MBAM Administration and Monitoring Server feature successfully installed by using the same IIS port binding on two separate server computers that meet the prerequisites for both MBAM Server feature installation and NLB Cluster configuration.</span></span>

<span data-ttu-id="c585f-120">**Remarques**  Cette rubrique décrit la procédure de base d’utilisation du gestionnaire de l’équilibrage de charge réseau pour créer un cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-120">**Note** This topic describes the basic process of using Network Load Balancing Manager to create an NLB Cluster.</span></span> <span data-ttu-id="c585f-121">Les étapes exactes de configuration d’un serveur Windows dans le cadre d’un cluster NLB dépendent de la version de Windows Server utilisée.</span><span class="sxs-lookup"><span data-stu-id="c585f-121">The exact steps to configure a Windows Server as part of an NLB cluster depend on the Windows Server version in use..</span></span> <span data-ttu-id="c585f-122">Pour plus d’informations sur la création d’NLBs sur WindowsServer2008, voir [création de clusters d’équilibrage de charge réseau](https://go.microsoft.com/fwlink/?LinkId=197176) dans la bibliothèque TechNet de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c585f-122">For more information about how to create NLBs on WindowsServer2008, see [Creating Network Load Balancing Clusters](https://go.microsoft.com/fwlink/?LinkId=197176) in the Windows Server2008 TechNet library.</span></span>

 

**<span data-ttu-id="c585f-123">Pour configurer le nom virtuel et l’adresse IP d’un cluster NLB pour deux serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="c585f-123">To configure an NLB Cluster Virtual Name and IP address for two MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="c585f-124">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Outils d’administration**, puis sur gestionnaire d’équilibrage de la **charge réseau**.</span><span class="sxs-lookup"><span data-stu-id="c585f-124">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Network Load Balancing Manager**.</span></span>

    <span data-ttu-id="c585f-125">**Remarques**  Si le gestionnaire de NLB n’est pas présent, vous pouvez l’installer en tant que fonctionnalité de WindowsServer2003.</span><span class="sxs-lookup"><span data-stu-id="c585f-125">**Note** If the NLB Manager is not present, you can install it as a WindowsServer feature.</span></span> <span data-ttu-id="c585f-126">Vous devez installer cette fonctionnalité sur les serveurs d’administration et de surveillance MBAM si vous souhaitez la configurer dans le cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-126">You must install this feature on both MBAM Administration and Monitoring servers if you want to configure it into the NLB cluster.</span></span>

     

2.  <span data-ttu-id="c585f-127">Dans la barre de menus, cliquez sur **cluster**, puis cliquez sur **nouveau** pour ouvrir la boîte de dialogue **paramètres du cluster** .</span><span class="sxs-lookup"><span data-stu-id="c585f-127">On the menu bar, click **Cluster**, and then click **New** to open the **Cluster Parameters** dialog box.</span></span>

3.  <span data-ttu-id="c585f-128">Dans la boîte de dialogue **paramètres du cluster** , entrez les informations relatives à la configuration IP du cluster NLB:</span><span class="sxs-lookup"><span data-stu-id="c585f-128">In the **Cluster Parameters** dialog box, enter the information for the NLB cluster IP configuration:</span></span>

    -   <span data-ttu-id="c585f-129">**Adresse IP:** Adresse IP du cluster NLB enregistrée dans DNS</span><span class="sxs-lookup"><span data-stu-id="c585f-129">**IP address:** NLB cluster IP address registered in DNS</span></span>

    -   <span data-ttu-id="c585f-130">**Masque de sous-réseau:** Masque de sous-réseau d’adresse IP du cluster NLB inscrit dans DNS</span><span class="sxs-lookup"><span data-stu-id="c585f-130">**Subnet mask:** NLB cluster IP address subnet mask registered in DNS</span></span>

    -   <span data-ttu-id="c585f-131">**Nom Internet complet:** Nom de domaine complet du nom de cluster NLB inscrit dans DNS</span><span class="sxs-lookup"><span data-stu-id="c585f-131">**Full Internet name:** FQDN of NLB cluster name registered in DNS</span></span>

4.  <span data-ttu-id="c585f-132">Assurez-vous que la case à **cocast** est activée en **mode de fonctionnement du cluster**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c585f-132">Ensure that **Unicast** is selected in **Cluster operation mode**, and then click **Next**.</span></span>

5.  <span data-ttu-id="c585f-133">Dans la page **adresses IP de cluster** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c585f-133">On the **Cluster IP Addresses** page, click **Next**.</span></span>

6.  <span data-ttu-id="c585f-134">Dans la page **règles de port** , cliquez sur **modifier** pour définir les ports auxquels le cluster NLB répondra et configurer les ports utilisés pour la communication du système client à site dès qu’ils sont définis pour le site, ou cliquez sur **suivant** pour activer l’adresse IP du cluster NLB pour répondre à tous les ports TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c585f-134">On the **Port Rules** page, click **Edit** to define the ports that the NLB cluster will respond to and configure the ports that are used for client-to-site system communication as they are defined for the site, or click **Next** to enable the NLB cluster IP address to respond to all TCP/IP ports.</span></span>

    <span data-ttu-id="c585f-135">**Remarques**  Assurez-vous que l' **affinité** est définie sur **Single**.</span><span class="sxs-lookup"><span data-stu-id="c585f-135">**Note** Ensure that **Affinity** is set to **Single**.</span></span>

     

7.  <span data-ttu-id="c585f-136">Dans la page **connexion** , entrez le nom d’hôte de l’instance du serveur d’administration MBAM et de surveillance qui fera partie du cluster NLB dans l' **hôte**, puis cliquez sur **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="c585f-136">On the **Connect** page, enter an MBAM Administration and Monitoring server instance host name that will be part of the NLB cluster in **Host**, and then click **Connect**.</span></span>

8.  <span data-ttu-id="c585f-137">Dans **interfaces disponibles pour la configuration d’un nouveau cluster**, sélectionnez l’interface réseau qui sera configurée pour répondre aux communications de cluster NLB, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c585f-137">In **Interfaces available for configuring a new cluster**, select the networking interface that will be configured to respond to NLB cluster communication, and then click **Next**.</span></span>

9.  <span data-ttu-id="c585f-138">Dans la page **paramètres d’hôte** , passez en revue les informations affichées pour vous assurer que les paramètres de **configuration IP dédiée** affichent la configuration IP d’hôte dédiée pour l’hôte de cluster NLB approprié, vérifiez que l' **État par défaut** de l’état d’accueil initial est **démarré**, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="c585f-138">On the **Host Parameters** page, review the information displayed to ensure that the **Dedicated IP configuration** settings display the dedicated host IP configuration for the correct NLB cluster host, check that the Initial host state **Default state:** is **Started**, and then click **Finish**.</span></span>

    <span data-ttu-id="c585f-139">**Remarques**  La page des **paramètres d’hôte** affiche également la priorité de l’hôte de cluster NLB, qui est de 1 à 32.</span><span class="sxs-lookup"><span data-stu-id="c585f-139">**Note** The **Host Parameters** page also displays the NLB cluster host priority, which is 1 through 32.</span></span> <span data-ttu-id="c585f-140">À mesure que de nouveaux hôtes sont ajoutés au cluster NLB, la priorité de l’hôte doit être différente de celle des hôtes précédemment ajoutés.</span><span class="sxs-lookup"><span data-stu-id="c585f-140">As new hosts are added to the NLB cluster, the host priority must differ from the previously added hosts.</span></span> <span data-ttu-id="c585f-141">La priorité est automatiquement incrémentée lorsque vous utilisez le gestionnaire d’équilibrage de la charge réseau.</span><span class="sxs-lookup"><span data-stu-id="c585f-141">The priority is automatically incremented when you use the Network Load Balancing Manager.</span></span>

     

10. <span data-ttu-id="c585f-142">Cliquez sur \*\* &lt; nom &gt; du cluster NLB\*\* et assurez-vous que l' **État** de l’interface du serveur NLB est **convergent** avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="c585f-142">Click **&lt;NLB cluster name&gt;** and ensure that the NLB host interface **Status** displays **Converged** before you continue.</span></span> <span data-ttu-id="c585f-143">Il est possible que vous n’ayez pas besoin d’actualiser l’affichage du cluster NLB en tant que configuration TCP/IP de l’hôte qui est modifiée par le gestionnaire NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-143">This step might require that you refresh the NLB cluster display as the host TCP/IP configuration that is being modified by the NLB Manager.</span></span>

11. <span data-ttu-id="c585f-144">Pour ajouter d’autres hôtes au cluster NLB, cliquez avec le bouton droit sur \*\* &lt; nom &gt; du cluster NLB\*\*, cliquez sur **Ajouter un hôte au cluster,** puis répétez les étapes 7 à 10 pour chaque système de site qui fera partie du cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-144">To add additional hosts to the NLB cluster, right-click **&lt;NLB cluster name&gt;**, click **Add Host to Cluster,** and then repeat steps 7 through 10 for each site system that will be part of the NLB cluster.</span></span>

12. <span data-ttu-id="c585f-145">Sur un ordinateur sur lequel le modèle de stratégie de groupe MBAM est installé, modifiez les paramètres de stratégie de groupe MBAM pour configurer les points de terminaison MBAM services de manière à utiliser le nom du cluster NLB et la liaison de port IIS appropriée pour accéder aux fonctionnalités d’administration et de contrôle du serveur MBAM qui sont installées sur les ordinateurs de cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-145">On a computer that has MBAM Group Policy template installed, modify the MBAM Group Policy settings to configure the MBAM services endpoints to use the NLB Cluster name and the appropriate IIS port binding to access the MBAM Administration and Monitoring Server features that are installed on the NLB Cluster computers.</span></span> <span data-ttu-id="c585f-146">Pour plus d’informations sur la modification des paramètres de l’objet de stratégie de MBAM, voir [Comment modifier les paramètres de l’objet de stratégie de groupe MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c585f-146">For more information about how to edit MBAM GPO settings, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span> <span data-ttu-id="c585f-147">Si les serveurs d’administration et de surveillance de MBAM sont nouveaux dans votre environnement, assurez-vous que les appartenances au groupe de sécurité local requises ont été configurées correctement.</span><span class="sxs-lookup"><span data-stu-id="c585f-147">If the MBAM Administration and Monitoring servers are new to your environment, ensure that the required local security group memberships have been properly configured.</span></span> <span data-ttu-id="c585f-148">Pour plus d’informations sur la configuration requise des groupes de sécurité, voir [planification de rôles d’administrateur MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="c585f-148">For more information about security group requirements, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

13. <span data-ttu-id="c585f-149">À la fin de la configuration du cluster NLB, il est recommandé de valider le fonctionnement de l’administration MBAM et de l’analyse du cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-149">When the NLB Cluster configuration is complete, we recommend that you validate that the MBAM Administration and Monitoring NLB Cluster is functional.</span></span> <span data-ttu-id="c585f-150">Pour ce faire, ouvrez un navigateur Web sur un ordinateur autre que celui qui est configuré dans le protocole NLB et assurez-vous que vous pouvez accéder au site Web d’administration et de surveillance de MBAM à l’aide du nom de domaine complet NLB.</span><span class="sxs-lookup"><span data-stu-id="c585f-150">To do this, open a web browser on a computer other than the servers that are configured in the NLB, and ensure that you can access the MBAM Administration and Monitoring web site by using the NLB FQDN.</span></span>

## <span data-ttu-id="c585f-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c585f-151">Related topics</span></span>


[<span data-ttu-id="c585f-152">Déploiement de l'infrastructure de serveur MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="c585f-152">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 






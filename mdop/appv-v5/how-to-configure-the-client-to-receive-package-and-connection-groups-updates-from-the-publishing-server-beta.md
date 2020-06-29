---
title: Comment configurer le client de manière à recevoir les mises à jour des groupes de connexion et des packages à partir du serveur de publication
description: Comment configurer le client de manière à recevoir les mises à jour des groupes de connexion et des packages à partir du serveur de publication
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805689"
---
# <span data-ttu-id="053d3-103">Comment configurer le client de manière à recevoir les mises à jour des groupes de connexion et des packages à partir du serveur de publication</span><span class="sxs-lookup"><span data-stu-id="053d3-103">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>


<span data-ttu-id="053d3-104">Le déploiement de packages et de groupes de connexion à l’aide du serveur de publication App-V 5,0 est utile, car il offre une gestion à un point et une extensibilité élevée.</span><span class="sxs-lookup"><span data-stu-id="053d3-104">Deploying packages and connection groups using the App-V 5.0 publishing server is helpful because it offers single-point management and high scalability.</span></span>

<span data-ttu-id="053d3-105">Procédez comme suit pour configurer le client App-V 5,0 pour recevoir des mises à jour du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="053d3-105">Use the following steps to configure the App-V 5.0 client to receive updates from the publishing server.</span></span>

<span data-ttu-id="053d3-106">**Remarques**  Pour les procédures suivantes, le serveur de gestion a été installé sur un ordinateur nommé **MyMgmtSrv**et le serveur de publication a été installé sur un ordinateur nommé **MyPubSrv**.</span><span class="sxs-lookup"><span data-stu-id="053d3-106">**Note** For the following procedures the management server was installed on a computer named **MyMgmtSrv**, and the publishing server was installed on a computer named **MyPubSrv**.</span></span>

 

**<span data-ttu-id="053d3-107">Pour configurer le client App-V 5,0 pour recevoir des mises à jour à partir du serveur de publication</span><span class="sxs-lookup"><span data-stu-id="053d3-107">To configure the App-V 5.0 client to receive updates from the publishing server</span></span>**

1.  <span data-ttu-id="053d3-108">Déployez les serveurs de publication et de gestion de l’application V 5,0, puis ajoutez les packages et groupes de connexion requis.</span><span class="sxs-lookup"><span data-stu-id="053d3-108">Deploy the App-V 5.0 management and publishing servers, and add the required packages and connection groups.</span></span> <span data-ttu-id="053d3-109">Pour plus d’informations sur l’ajout de packages et de groupes de connexions, voir [Ajouter ou mettre à niveau des packages à l’aide de la console de gestion](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) et [créer un groupe de connexion](how-to-create-a-connection-group.md).</span><span class="sxs-lookup"><span data-stu-id="053d3-109">For more information about adding packages and connection groups, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Create a Connection Group](how-to-create-a-connection-group.md).</span></span>

2.  <span data-ttu-id="053d3-110">Pour ouvrir la console de gestion, cliquez sur le lien suivant, ouvrez un navigateur et tapez les informations suivantes: http://MyMgmtSrv/AppvManagement/Console.html dans un navigateur Web, importez, publiez et activez tous les packages et groupes de connexion qui seront nécessaires pour un ensemble spécifique d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="053d3-110">To open the management console click the following link, open a browser and type the following: http://MyMgmtSrv/AppvManagement/Console.html in a web browser, and import, publish, and entitle all the packages and connection groups which will be necessary for a particular set of users.</span></span>

3.  <span data-ttu-id="053d3-111">Sur l’ordinateur exécutant le client App-V 5,0, ouvrez une invite de commandes PowerShell avec élévation de privilèges, exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="053d3-111">On the computer running the App-V 5.0 client, open an elevated PowerShell command prompt, run the following command:</span></span>

    **<span data-ttu-id="053d3-112">Add-AppvPublishingServer-nom ABC-URL http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="053d3-112">Add-AppvPublishingServer -Name ABC -URL http:// MyPubSrv/AppvPublishing</span></span>**

    <span data-ttu-id="053d3-113">Cette commande configure le serveur de publication spécifié.</span><span class="sxs-lookup"><span data-stu-id="053d3-113">This command will configure the specified publishing server.</span></span> <span data-ttu-id="053d3-114">La sortie doit apparaître comme suit:</span><span class="sxs-lookup"><span data-stu-id="053d3-114">You should see output similar to the following:</span></span>

    <span data-ttu-id="053d3-115">ID: 1</span><span class="sxs-lookup"><span data-stu-id="053d3-115">Id : 1</span></span>

    <span data-ttu-id="053d3-116">SetByGroupPolicy: false</span><span class="sxs-lookup"><span data-stu-id="053d3-116">SetByGroupPolicy : False</span></span>

    <span data-ttu-id="053d3-117">Nom: ABC</span><span class="sxs-lookup"><span data-stu-id="053d3-117">Name : ABC</span></span>

    <span data-ttu-id="053d3-118">URL: http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="053d3-118">URL : http:// MyPubSrv/AppvPublishing</span></span>

    <span data-ttu-id="053d3-119">GlobalRefreshEnabled: false</span><span class="sxs-lookup"><span data-stu-id="053d3-119">GlobalRefreshEnabled : False</span></span>

    <span data-ttu-id="053d3-120">GlobalRefreshOnLogon: false</span><span class="sxs-lookup"><span data-stu-id="053d3-120">GlobalRefreshOnLogon : False</span></span>

    <span data-ttu-id="053d3-121">GlobalRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="053d3-121">GlobalRefreshInterval : 0</span></span>

    <span data-ttu-id="053d3-122">GlobalRefreshIntervalUnit: jour</span><span class="sxs-lookup"><span data-stu-id="053d3-122">GlobalRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="053d3-123">UserRefreshEnabled: true</span><span class="sxs-lookup"><span data-stu-id="053d3-123">UserRefreshEnabled : True</span></span>

    <span data-ttu-id="053d3-124">UserRefreshOnLogon: true</span><span class="sxs-lookup"><span data-stu-id="053d3-124">UserRefreshOnLogon : True</span></span>

    <span data-ttu-id="053d3-125">UserRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="053d3-125">UserRefreshInterval : 0</span></span>

    <span data-ttu-id="053d3-126">UserRefreshIntervalUnit: jour</span><span class="sxs-lookup"><span data-stu-id="053d3-126">UserRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="053d3-127">ID renvoyé, dans le cas présent 1</span><span class="sxs-lookup"><span data-stu-id="053d3-127">The returned Id – in this case 1</span></span>

4.  <span data-ttu-id="053d3-128">Sur l’ordinateur exécutant le client App-V 5,0, ouvrez une invite de commandes PowerShell et tapez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="053d3-128">On the computer running the App-V 5.0 client, open a PowerShell command prompt, and type the following command:</span></span>

    **<span data-ttu-id="053d3-129">Synchronisation-AppvPublishingServer-ServerId 1</span><span class="sxs-lookup"><span data-stu-id="053d3-129">Sync-AppvPublishingServer -ServerId 1</span></span>**

    <span data-ttu-id="053d3-130">La commande interroge le serveur de publication pour les packages et groupes de connexion qui doivent être ajoutés ou supprimés pour ce client particulier en fonction des habilitations des packages et des groupes de connexion, comme configuré sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="053d3-130">The command will query the publishing server for the packages and connection groups that need to be added or removed for this particular client based on the entitlements for the packages and connection groups as configured on the management server.</span></span>

    <span data-ttu-id="053d3-131">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="053d3-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="053d3-132">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="053d3-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="053d3-133">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="053d3-133">Got an App-V issue?</span></span>** <span data-ttu-id="053d3-134">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="053d3-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="053d3-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="053d3-135">Related topics</span></span>


[<span data-ttu-id="053d3-136">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="053d3-136">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 






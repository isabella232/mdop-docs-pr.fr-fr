---
title: Comment installer le serveur de publication sur un ordinateur distant
description: Comment installer le serveur de publication sur un ordinateur distant
author: dansimp
ms.assetid: 1c903f78-0558-458d-a149-d5f6fb55aefb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a085d68305057538228599e35dd9500957342ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805383"
---
# <span data-ttu-id="de259-103">Comment installer le serveur de publication sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="de259-103">How to Install the Publishing Server on a Remote Computer</span></span>


<span data-ttu-id="de259-104">Utilisez la procédure suivante pour installer le serveur de publication sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="de259-104">Use the following procedure to install the publishing server on a separate computer.</span></span> <span data-ttu-id="de259-105">Avant d’effectuer la procédure suivante, assurez-vous que le serveur de base de données et de gestion est disponible.</span><span class="sxs-lookup"><span data-stu-id="de259-105">Before you perform the following procedure, ensure the database and management server are available.</span></span>

**<span data-ttu-id="de259-106">Pour installer le serveur de publication sur un autre ordinateur</span><span class="sxs-lookup"><span data-stu-id="de259-106">To install the publishing server on a separate computer</span></span>**

1. <span data-ttu-id="de259-107">Copiez les fichiers d’installation de App-V 5,1 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="de259-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="de259-108">Pour démarrer l’installation de l’application-V 5,1 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="de259-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="de259-109">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="de259-109">Click **Install**.</span></span>

2. <span data-ttu-id="de259-110">Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="de259-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="de259-111">Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).**</span><span class="sxs-lookup"><span data-stu-id="de259-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="de259-112">Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="de259-112">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="de259-113">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="de259-113">Click **Next**.</span></span>

4. <span data-ttu-id="de259-114">Dans la page de **sélection des fonctionnalités** , activez la case à cocher **serveur de publication** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="de259-114">On the **Feature Selection** page, select the **Publishing Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="de259-115">Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="de259-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="de259-116">Dans la page Configuration du **serveur de publication** , spécifiez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="de259-116">On the **Configure Publishing Server Configuration** page, specify the following items:</span></span>

   -   <span data-ttu-id="de259-117">URL du service de gestion auquel est connecté le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="de259-117">The URL for the management service that the publishing server will connect to.</span></span> <span data-ttu-id="de259-118">Par exemple, **http://ManagementServerName:12345** .</span><span class="sxs-lookup"><span data-stu-id="de259-118">For example, **http://ManagementServerName:12345**.</span></span>

   -   <span data-ttu-id="de259-119">Spécifiez le nom du site Web que vous voulez utiliser pour le service de publication.</span><span class="sxs-lookup"><span data-stu-id="de259-119">Specify the website name that you want to use for the publishing service.</span></span> <span data-ttu-id="de259-120">Acceptez la valeur par défaut si vous n’avez pas de nom personnalisé.</span><span class="sxs-lookup"><span data-stu-id="de259-120">Accept the default if you do not have a custom name.</span></span>

   -   <span data-ttu-id="de259-121">Pour la **liaison de port**, spécifiez un numéro de port unique qui sera utilisé par App-V 5,1, par exemple **54321**.</span><span class="sxs-lookup"><span data-stu-id="de259-121">For the **Port Binding**, specify a unique port number that will be used by App-V 5.1, for example **54321**.</span></span>

7. <span data-ttu-id="de259-122">Sur la page **prêt pour l’installation** , cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="de259-122">On the **Ready to Install** page, click **Install**.</span></span>

8. <span data-ttu-id="de259-123">Une fois l’installation terminée, le serveur de publication doit être enregistré auprès du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="de259-123">After the installation is complete, the publishing server must be registered with the management server.</span></span> <span data-ttu-id="de259-124">Dans la console de gestion App-V 5,1, procédez comme suit pour inscrire le serveur:</span><span class="sxs-lookup"><span data-stu-id="de259-124">In the App-V 5.1 management console, use the following steps to register the server:</span></span>

   1.  <span data-ttu-id="de259-125">Ouvrez la console App-V 5,1 Management Server.</span><span class="sxs-lookup"><span data-stu-id="de259-125">Open the App-V 5.1 management server console.</span></span>

   2.  <span data-ttu-id="de259-126">Dans le volet gauche, sélectionnez **serveurs**, puis sélectionnez **inscrire un nouveau serveur**.</span><span class="sxs-lookup"><span data-stu-id="de259-126">In the left pane, select **Servers**, and then select **Register New Server**.</span></span>

   3.  <span data-ttu-id="de259-127">Entrez le nom de ce serveur et une description (si nécessaire), puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="de259-127">Type the name of this server and a description (if required) and click **Add**.</span></span>

9. <span data-ttu-id="de259-128">Pour vérifier que le serveur de publication s’exécute correctement, importez un package sur le serveur de gestion, configurez le package dans un groupe d’annonces et publiez le package.</span><span class="sxs-lookup"><span data-stu-id="de259-128">To verify if the publishing server is running correctly, you should import a package to the management server, entitle the package to an AD group, and publish the package.</span></span> <span data-ttu-id="de259-129">À l’aide d’un navigateur Internet, ouvrez l’URL suivante: <strong> http://publishingserver:pubport </strong> .</span><span class="sxs-lookup"><span data-stu-id="de259-129">Using an internet browser, open the following URL: <strong>http://publishingserver:pubport</strong>.</span></span> <span data-ttu-id="de259-130">Si le serveur fonctionne correctement, des informations similaires à ce qui suit s’affichent:</span><span class="sxs-lookup"><span data-stu-id="de259-130">If the server is running correctly information similar to the following will be displayed:</span></span>

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   <span data-ttu-id="de259-131">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="de259-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="de259-132">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="de259-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="de259-133">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="de259-133">Got an App-V issue?</span></span>** <span data-ttu-id="de259-134">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="de259-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="de259-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de259-135">Related topics</span></span>


[<span data-ttu-id="de259-136">Déploiement d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="de259-136">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

 

 






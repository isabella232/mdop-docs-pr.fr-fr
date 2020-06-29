---
title: Comment installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données
description: Comment installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données
author: dansimp
ms.assetid: 95281287-cb56-4117-befd-854268ea147c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86f384e88b85101855287bb428e75376f7974219
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805419"
---
# <span data-ttu-id="6407d-103">Comment installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données</span><span class="sxs-lookup"><span data-stu-id="6407d-103">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="6407d-104">Utilisez la procédure suivante pour installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données.</span><span class="sxs-lookup"><span data-stu-id="6407d-104">Use the following procedure to install the management server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="6407d-105">Pour installer le serveur de gestion sur un ordinateur autonome en le connectant à la base de données</span><span class="sxs-lookup"><span data-stu-id="6407d-105">To install the management server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="6407d-106">Copiez les fichiers d’installation de App-V 5,0 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="6407d-106">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="6407d-107">Pour démarrer l’installation de l’application-V 5,0 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="6407d-107">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="6407d-108">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="6407d-108">Click **Install**.</span></span>

2.  <span data-ttu-id="6407d-109">Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="6407d-109">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="6407d-110">Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).**</span><span class="sxs-lookup"><span data-stu-id="6407d-110">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="6407d-111">Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="6407d-111">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="6407d-112">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6407d-112">Click **Next**.</span></span>

4.  <span data-ttu-id="6407d-113">Dans la page de **sélection des fonctionnalités** , activez la case à cocher **serveur de gestion** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="6407d-113">On the **Feature Selection** page, select the **Management Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="6407d-114">Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="6407d-114">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="6407d-115">Sur la page **configurer la base de données de gestion existante** , sélectionnez **utiliser un serveur SQL distant**, puis tapez le nom de l’ordinateur exécutant Microsoft SQL SQL (par exemple, **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="6407d-115">On the **Configure Existing Management Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL SQL, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="6407d-116">Remarque</span><span class="sxs-lookup"><span data-stu-id="6407d-116">Note</span></span>**  
    <span data-ttu-id="6407d-117">Si Microsoft SQL Server est déployé sur le même serveur, sélectionnez **use local SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="6407d-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. <span data-ttu-id="6407d-118">Dans la page Configuration du **serveur de gestion** , spécifiez le groupe d’annonces ou le compte qui sera connecté à la console de gestion à des fins d’administration, par exemple **MyDomain\\MyUser** ou **MyDomain\\AdminGroup**.</span><span class="sxs-lookup"><span data-stu-id="6407d-118">On the **Configure Management Server Configuration** page, specify the AD group or account that will connect to the management console for administrative purposes for example **MyDomain\\MyUser** or **MyDomain\\AdminGroup**.</span></span> <span data-ttu-id="6407d-119">Le compte ou le groupe d’annonces que vous spécifiez est activé pour gérer le serveur par le biais de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="6407d-119">The account or AD group you specify will be enabled to manage the server through the management console.</span></span> <span data-ttu-id="6407d-120">Vous pouvez ajouter des utilisateurs ou des groupes supplémentaires à l’aide de la console de gestion après l’installation.</span><span class="sxs-lookup"><span data-stu-id="6407d-120">You can add additional users or groups using the management console after installation</span></span>

   <span data-ttu-id="6407d-121">Spécifiez le **nom du site Web** que vous voulez utiliser pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="6407d-121">Specify the **Website Name** that you want to use for the management service.</span></span> <span data-ttu-id="6407d-122">Acceptez la valeur par défaut si vous n’avez pas de nom personnalisé.</span><span class="sxs-lookup"><span data-stu-id="6407d-122">Accept the default if you do not have a custom name.</span></span> <span data-ttu-id="6407d-123">Pour la **liaison de port**, spécifiez un numéro de port unique à utiliser (par exemple, **12345**).</span><span class="sxs-lookup"><span data-stu-id="6407d-123">For the **Port Binding**, specify a unique port number to be used, for example **12345**.</span></span>

8. <span data-ttu-id="6407d-124">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="6407d-124">Click **Install**.</span></span>

9. <span data-ttu-id="6407d-125">Pour vérifier que la configuration s’est déroulée correctement, ouvrez un navigateur Web, puis tapez l’URL suivante: http://managementserver:portnumber/Console.html si l’installation a réussi, vous devriez voir la **console de gestion Silverlight** sans message d’erreur ou avertissement affiché.</span><span class="sxs-lookup"><span data-stu-id="6407d-125">To confirm that the setup has completed successfully, open a web browser, and type the following URL: http://managementserver:portnumber/Console.html if the installation was successful you should see the **Silverlight Management Console** appear without any error messages or warnings being displayed.</span></span>

   <span data-ttu-id="6407d-126">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="6407d-126">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6407d-127">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="6407d-127">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="6407d-128">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="6407d-128">Got an App-V issue?</span></span>** <span data-ttu-id="6407d-129">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6407d-129">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="6407d-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6407d-130">Related topics</span></span>


[<span data-ttu-id="6407d-131">Déploiement d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="6407d-131">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)










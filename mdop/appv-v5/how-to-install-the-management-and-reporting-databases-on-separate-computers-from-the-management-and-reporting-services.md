---
title: Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports
description: Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805418"
---
# <span data-ttu-id="30d85-103">Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports</span><span class="sxs-lookup"><span data-stu-id="30d85-103">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>


<span data-ttu-id="30d85-104">Utilisez la procédure suivante pour installer le serveur de base de données et le serveur de gestion sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="30d85-104">Use the following procedure to install the database server and management server on different computers.</span></span> <span data-ttu-id="30d85-105">L’ordinateur sur lequel vous envisagez d’installer le serveur de base de données doit exécuter une version prise en charge de Microsoft SQL, ou l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="30d85-105">The computer you plan to install the database server on must be running a supported version of Microsoft SQL or the installation will fail.</span></span>

**<span data-ttu-id="30d85-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="30d85-106">Note</span></span>**  
<span data-ttu-id="30d85-107">À la fin du déploiement, le nom de l’instance, le nom de l' **instance** et le nom **de la base de données** **Microsoft SQL Server**sont requis par l’administrateur qui installe le service pour pouvoir se connecter à ces bases de données.</span><span class="sxs-lookup"><span data-stu-id="30d85-107">After you complete the deployment, the **Microsoft SQL Server name**, **instance name** and **database name** will be required by the administrator installing the service to be able to connect to these databases.</span></span>



**<span data-ttu-id="30d85-108">Pour installer la base de données de gestion et le serveur de gestion sur des ordinateurs séparés</span><span class="sxs-lookup"><span data-stu-id="30d85-108">To install the management database and the management server on separate computers</span></span>**

1.  <span data-ttu-id="30d85-109">Copiez les fichiers d’installation de App-V 5,0 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="30d85-109">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="30d85-110">Pour démarrer l’installation de l’application-V 5,0 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="30d85-110">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="30d85-111">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="30d85-111">Click **Install**.</span></span>

2.  <span data-ttu-id="30d85-112">Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-112">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="30d85-113">Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).**</span><span class="sxs-lookup"><span data-stu-id="30d85-113">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="30d85-114">Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="30d85-114">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="30d85-115">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-115">Click **Next**.</span></span>

4.  <span data-ttu-id="30d85-116">Dans la page de **sélection des fonctionnalités** , sélectionnez les composants que vous voulez installer en sélectionnant la case **de base de données du serveur de gestion** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-116">On the **Feature Selection** page, select the components you want to install by selecting the **Management Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="30d85-117">Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-117">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="30d85-118">Dans la **page créer un serveur de base de données**initial, acceptez les sélections par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-118">On the initial **Create New Management Server Database page**, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="30d85-119">Si vous utilisez une instance SQL Server personnalisée, sélectionnez **utiliser une instance personnalisée** et tapez le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="30d85-119">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="30d85-120">Si vous utilisez un nom de base de données personnalisé, sélectionnez **configuration personnalisée** , puis tapez le nom de la base de données.</span><span class="sxs-lookup"><span data-stu-id="30d85-120">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="30d85-121">Dans la page **créer une base de données de serveur de gestion** suivante, sélectionnez **utiliser un ordinateur distant**, puis entrez le compte d’ordinateur distant en utilisant le format suivant: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="30d85-121">On the next **Create New Management Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="30d85-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="30d85-122">Note</span></span>**  
    <span data-ttu-id="30d85-123">Si vous envisagez de déployer le serveur de gestion sur le même ordinateur, vous devez sélectionner **utiliser cet ordinateur local**.</span><span class="sxs-lookup"><span data-stu-id="30d85-123">If you plan to deploy the management server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="30d85-124">Pour démarrer l’installation, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="30d85-124">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="30d85-125">Pour installer la base de données de création de rapports et le serveur de rapports sur des ordinateurs distincts</span><span class="sxs-lookup"><span data-stu-id="30d85-125">To install the reporting database and the reporting server on separate computers</span></span>**

1.  <span data-ttu-id="30d85-126">Copiez les fichiers d’installation de App-V 5,0 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="30d85-126">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="30d85-127">Pour démarrer l’installation de l’application-V 5,0 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="30d85-127">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="30d85-128">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="30d85-128">Click **Install**.</span></span>

2.  <span data-ttu-id="30d85-129">Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-129">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="30d85-130">Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).**</span><span class="sxs-lookup"><span data-stu-id="30d85-130">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="30d85-131">Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="30d85-131">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="30d85-132">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-132">Click **Next**.</span></span>

4.  <span data-ttu-id="30d85-133">Dans la page de **sélection des fonctionnalités** , sélectionnez les composants que vous voulez installer en sélectionnant la case **de base de données du serveur de création de rapports** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-133">On the **Feature Selection** page, select the components you want to install by selecting the **Reporting Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="30d85-134">Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-134">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="30d85-135">Dans la page **de création de base de données initiale de création de rapports** , acceptez les sélections par défaut le cas échéant, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="30d85-135">On the initial **Create New Reporting Server Database** page, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="30d85-136">Si vous utilisez une instance SQL Server personnalisée, sélectionnez **utiliser une instance personnalisée** et tapez le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="30d85-136">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="30d85-137">Si vous utilisez un nom de base de données personnalisé, sélectionnez **configuration personnalisée** , puis tapez le nom de la base de données.</span><span class="sxs-lookup"><span data-stu-id="30d85-137">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="30d85-138">Dans la page **créer une base de données de serveur de** création de rapports, sélectionnez **utiliser un ordinateur distant**, puis entrez le compte d’ordinateur distant en utilisant le format suivant: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="30d85-138">On the next **Create New Reporting Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="30d85-139">Remarque</span><span class="sxs-lookup"><span data-stu-id="30d85-139">Note</span></span>**  
    <span data-ttu-id="30d85-140">Si vous envisagez de déployer le serveur de création de rapports sur le même ordinateur, vous devez sélectionner **utiliser cet ordinateur local**.</span><span class="sxs-lookup"><span data-stu-id="30d85-140">If you plan to deploy the reporting server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="30d85-141">Pour démarrer l’installation, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="30d85-141">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="30d85-142">Pour installer les bases de données de gestion et de création de rapports à l’aide de scripts de base de données App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="30d85-142">To install the management and reporting databases using App-V 5.0 database scripts</span></span>**

1.  <span data-ttu-id="30d85-143">Copiez les fichiers d’installation de App-V 5,0 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="30d85-143">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span>

2.  <span data-ttu-id="30d85-144">Pour extraire les scripts de base de données App-V 5,0, ouvrez une invite de commandes et spécifiez l’emplacement d’enregistrement des fichiers d’installation, puis exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="30d85-144">To extract the App-V 5.0 database scripts, open a command prompt and specify the location where the installation files are saved and run the following command:</span></span>

    <span data-ttu-id="30d85-145">**appv\_server\_setup.exe** **/Layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.</span><span class="sxs-lookup"><span data-stu-id="30d85-145">**appv\_server\_setup.exe** **/LAYOUT** **/LAYOUTDIR=”InstallationExtractionLocation”**.</span></span>

3.  <span data-ttu-id="30d85-146">Une fois l’extraction terminée, pour accéder au fichier Lisez-moi scripts et instructions de la base de données App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="30d85-146">After the extraction has been completed, to access the App-V 5.0 database scripts and instructions readme file:</span></span>

    -   <span data-ttu-id="30d85-147">Les scripts et instructions de la base de données de gestion App-V 5,0 se trouvent dans **InstallationExtractionLocation**le dossier suivant:  \\  base de données de gestion des**scripts de base de données**InstallationExtractionLocation  \\  **Management Database**.</span><span class="sxs-lookup"><span data-stu-id="30d85-147">The App-V 5.0 Management Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Management Database**.</span></span>

    -   <span data-ttu-id="30d85-148">Les scripts et instructions de la base de données de création de rapports App-V 5,0 se **InstallationExtractionLocation**trouvent dans le dossier suivant:  \\  **Database Scripts**  \\  **base de données de création de rapports**de la base de données InstallationExtractionLocation.</span><span class="sxs-lookup"><span data-stu-id="30d85-148">The App-V 5.0 Reporting Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Reporting Database**.</span></span>

4.  <span data-ttu-id="30d85-149">Pour chaque base de données, copiez les scripts dans un partage et modifiez-les en suivant les instructions dans le fichier Lisez-moi.</span><span class="sxs-lookup"><span data-stu-id="30d85-149">For each database, copy the scripts to a share and modify them following the instructions in the readme file.</span></span>

    **<span data-ttu-id="30d85-150">Remarque</span><span class="sxs-lookup"><span data-stu-id="30d85-150">Note</span></span>**  
    <span data-ttu-id="30d85-151">Pour plus d’informations sur la modification des SID requis contenus dans les scripts, voir [Comment installer les bases de données App-V et convertir les identificateurs de sécurité associés à l’aide de PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="30d85-151">For more information about modifying the required SIDs contained in the scripts see, [How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span></span>



5.  <span data-ttu-id="30d85-152">Exécutez les scripts sur l’ordinateur exécutant Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30d85-152">Run the scripts on the computer running Microsoft SQL Server.</span></span>

    <span data-ttu-id="30d85-153">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="30d85-153">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="30d85-154">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="30d85-154">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="30d85-155">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="30d85-155">Got an App-V issue?</span></span>** <span data-ttu-id="30d85-156">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="30d85-156">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="30d85-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30d85-157">Related topics</span></span>


[<span data-ttu-id="30d85-158">Déploiement d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="30d85-158">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)










---
title: Procédure pour installer le serveur Application Virtualization Management Server
description: Procédure pour installer le serveur Application Virtualization Management Server
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807077"
---
# <span data-ttu-id="31d26-103">Procédure pour installer le serveur Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="31d26-103">How to Install Application Virtualization Management Server</span></span>


<span data-ttu-id="31d26-104">Le serveur de gestion de la virtualisation des applications publie ses applications sur les clients.</span><span class="sxs-lookup"><span data-stu-id="31d26-104">The Application Virtualization Management Server publishes its applications to clients.</span></span> <span data-ttu-id="31d26-105">Dans un environnement qui est équilibré, il s’agit généralement de déploiements volumineux, tous les serveurs d’un groupe de serveurs doivent diffuser les mêmes applications.</span><span class="sxs-lookup"><span data-stu-id="31d26-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="31d26-106">Si les serveurs de gestion d’applications de la virtualisation doivent publier différentes applications, affectez-les à différents groupes de serveurs.</span><span class="sxs-lookup"><span data-stu-id="31d26-106">If Application Virtualization Management Servers are to publish different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="31d26-107">Dans ce cas, il se peut que vous deviez augmenter la capacité d’un groupe de serveurs.</span><span class="sxs-lookup"><span data-stu-id="31d26-107">In this case, you also might need to increase a server group's capacity.</span></span>

<span data-ttu-id="31d26-108">Si vous avez désigné un ordinateur cible sur le réseau et qu’un compte de connexion possède des privilèges d’administrateur local, vous pouvez utiliser la procédure suivante pour installer le serveur de gestion des applications et l’affecter au groupe de serveurs approprié.</span><span class="sxs-lookup"><span data-stu-id="31d26-108">If you have designated a target computer on the network, with a login account having local Administrator privileges, you can use the following procedure to install the Application Virtualization Management Server and assign it to the appropriate server group.</span></span>

**<span data-ttu-id="31d26-109">Remarque</span><span class="sxs-lookup"><span data-stu-id="31d26-109">Note</span></span>**  
<span data-ttu-id="31d26-110">L’Assistant installation peut créer un enregistrement de groupe de serveurs, s’il n’en existe pas, ainsi qu’un enregistrement de l’appartenance du serveur de gestion des applications à ce groupe.</span><span class="sxs-lookup"><span data-stu-id="31d26-110">The Installation Wizard can create a server group record, if one does not exist, as well as a record of the Application Virtualization Management Server's membership in this group.</span></span>



<span data-ttu-id="31d26-111">Lorsque vous avez terminé le processus d’installation, redémarrez le serveur.</span><span class="sxs-lookup"><span data-stu-id="31d26-111">After you complete the installation process, reboot the server.</span></span>

**<span data-ttu-id="31d26-112">Pour installer un serveur de gestion des applications virtuelles</span><span class="sxs-lookup"><span data-stu-id="31d26-112">To install an Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="31d26-113">Vérifiez et, si nécessaire, désinstallez les versions précédentes du serveur de gestion des applications qui sont installées sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="31d26-113">Verify and, if necessary, uninstall previous versions of the Application Virtualization Management Server that are installed on the target computer.</span></span>

2.  <span data-ttu-id="31d26-114">Pour ouvrir l’Assistant **installation de Microsoft Application Virtualization Server** , accédez à l’emplacement du système de virtualisation des applications **setup.exe** programme sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur le fichier **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="31d26-114">To open the **Microsoft Application Virtualization Management Server installation** wizard, navigate to the location of the Application Virtualization System **setup.exe** program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="31d26-115">Dans la page **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-115">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="31d26-116">Sur la page **contrat de licence** , lisez le contrat de licence et acceptez le contrat de licence, puis sélectionnez **J’accepte les termes du**contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="31d26-116">On the **License Agreement** page, read the license agreement and, to accept the license agreement, select **I accept the license terms and conditions**.</span></span> <span data-ttu-id="31d26-117">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-117">Click **Next**.</span></span>

5.  <span data-ttu-id="31d26-118">Dans la page **informations d’inscription** , vous devez entrer le nom d’utilisateur et l' **organisation**.</span><span class="sxs-lookup"><span data-stu-id="31d26-118">On the **Registering Information** page, you must enter the user name and the **Organization**.</span></span> <span data-ttu-id="31d26-119">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-119">Click **Next**.</span></span>

6.  <span data-ttu-id="31d26-120">Dans la page **type d’installation** , sélectionnez **personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="31d26-120">On the **Setup Type** page, select **Custom**.</span></span> <span data-ttu-id="31d26-121">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-121">Click **Next**.</span></span> <span data-ttu-id="31d26-122">Dans la page **configuration personnalisée** , désélectionnez tous les composants du système de virtualisation des applications, à l’exception du **serveur de virtualisation des applications**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-122">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    **<span data-ttu-id="31d26-123">Vigilance</span><span class="sxs-lookup"><span data-stu-id="31d26-123">Caution</span></span>**  
    <span data-ttu-id="31d26-124">Si un composant est déjà installé sur l’ordinateur, lorsque vous le désactivez dans la fenêtre **configuration personnalisée** , le composant est automatiquement désinstallé.</span><span class="sxs-lookup"><span data-stu-id="31d26-124">If a component is already installed on the computer, when you deselect it in the **Custom Setup** window, the component is automatically uninstalled.</span></span>



7.  <span data-ttu-id="31d26-125">Dans la page **de la base de données de configuration** , sélectionnez un serveur de base de données dans la liste des serveurs disponibles ou ajoutez un serveur en sélectionnant **utiliser le nom d’hôte suivant** et en spécifiant les données du **nom de serveur** et du numéro de **port** .</span><span class="sxs-lookup"><span data-stu-id="31d26-125">On the **Configuration Database** page, select a database server from the list of available servers or add a server by selecting **Use the following host name** and specifying the **Server Name** and **Port Number** data.</span></span> <span data-ttu-id="31d26-126">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-126">Click **Next**.</span></span>

    **<span data-ttu-id="31d26-127">Remarque</span><span class="sxs-lookup"><span data-stu-id="31d26-127">Note</span></span>**  
    <span data-ttu-id="31d26-128">Le serveur de gestion des applications virtuelles ne prend pas en charge le code SQL sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="31d26-128">The Application Virtualization Management Server does not support case sensitive SQL.</span></span>



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. <span data-ttu-id="31d26-129">Sur la page **mode de sécurité de connexion** , sélectionnez le certificat de votre choix dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="31d26-129">On the **Connection Security Mode** page, select the desired certificate from the drop-down list.</span></span> <span data-ttu-id="31d26-130">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-130">Click **Next**.</span></span>

   **<span data-ttu-id="31d26-131">Remarque</span><span class="sxs-lookup"><span data-stu-id="31d26-131">Note</span></span>**  
   <span data-ttu-id="31d26-132">Le paramètre **mode de connexion sécurisée** exige que le serveur ait configuré un certificat de serveur à partir d’une infrastructure à clé publique.</span><span class="sxs-lookup"><span data-stu-id="31d26-132">The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="31d26-133">Si un certificat de serveur n’est pas installé sur le serveur, cette option n’est pas disponible et ne peut pas être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="31d26-133">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="31d26-134">Vous devez accorder au compte de service réseau l’accès en lecture au certificat utilisé.</span><span class="sxs-lookup"><span data-stu-id="31d26-134">You must grant the Network Service account read access to the certificate being used.</span></span>



9. <span data-ttu-id="31d26-135">Dans la page **configuration de port TCP** , pour utiliser le port par défaut (554), sélectionnez **utiliser le port par défaut (554)**.</span><span class="sxs-lookup"><span data-stu-id="31d26-135">On the **TCP Port Configuration** page, to use the default port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="31d26-136">Pour spécifier un port personnalisé, sélectionnez **utiliser un port personnalisé** et spécifiez le numéro de port qui sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="31d26-136">To specify a custom port, select **Use custom port** and specify the port number that will be used.</span></span> <span data-ttu-id="31d26-137">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-137">Click **Next**.</span></span>

   **<span data-ttu-id="31d26-138">Remarque</span><span class="sxs-lookup"><span data-stu-id="31d26-138">Note</span></span>**  
   <span data-ttu-id="31d26-139">Lorsque vous installez le serveur dans un environnement non sécurisé, vous pouvez utiliser le port par défaut (554) ou vous pouvez définir un port personnalisé.</span><span class="sxs-lookup"><span data-stu-id="31d26-139">When you install the server in a nonsecure environment, you can use the default port (554) or you can define a custom port.</span></span>



10. <span data-ttu-id="31d26-140">Sur la page **groupe d’administrateurs** , spécifiez le nom du groupe de sécurité autorisé à gérer ce serveur dans nom du **groupe**.</span><span class="sxs-lookup"><span data-stu-id="31d26-140">On the **Administrator Group** page, specify the name of the security group authorized to manage this server in **Group Name**.</span></span> <span data-ttu-id="31d26-141">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-141">Click **Next**.</span></span> <span data-ttu-id="31d26-142">Confirmez le groupe spécifié, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-142">Confirm the group specified and click **Next**.</span></span>

11. <span data-ttu-id="31d26-143">Sur la page **groupe de fournisseurs par défaut** , spécifiez le nom du groupe de fournisseurs par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-143">On the **Default Provider Group** page, specify the name of the default provider group, and then click **Next**.</span></span>

12. <span data-ttu-id="31d26-144">Dans la page **chemin d’accès au contenu** , spécifiez l’emplacement de l’ordinateur cible sur lequel les fichiers SFT seront enregistrés, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-144">On the **Content Path** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

   **<span data-ttu-id="31d26-145">Remarque</span><span class="sxs-lookup"><span data-stu-id="31d26-145">Note</span></span>**  
   <span data-ttu-id="31d26-146">Si le port HTTP ou RTSP du serveur de gestion est déjà attribué, vous êtes invité à choisir un nouveau port.</span><span class="sxs-lookup"><span data-stu-id="31d26-146">If the HTTP or RTSP port for the Management Server is already allocated, you will be prompted to choose a new port.</span></span> <span data-ttu-id="31d26-147">Sélectionnez le port de votre choix, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="31d26-147">Select the desired port, and then click **Next**.</span></span>



13. <span data-ttu-id="31d26-148">Dans la page **êtes-vous prêt à installer le programme** , cliquez sur **installer**pour installer le serveur de gestion des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="31d26-148">On the **Ready to Install the Program** page, to install the Application Virtualization Management Server, click **Install**.</span></span>

   **<span data-ttu-id="31d26-149">Remarque</span><span class="sxs-lookup"><span data-stu-id="31d26-149">Note</span></span>**  
   <span data-ttu-id="31d26-150">Si l’erreur 25120 s’affiche lorsque vous essayez d’effectuer cette étape, vous devez activer **les scripts et les outils de gestion**IIS.</span><span class="sxs-lookup"><span data-stu-id="31d26-150">If error 25120 is displayed when you try to complete this step, you need to enable IIS **Management Scripts and Tools**.</span></span> <span data-ttu-id="31d26-151">Pour activer cette fonctionnalité Windows, ouvrez le panneau **de configuration programmes et fonctionnalités** , sélectionnez **activer ou désactiver des fonctionnalités Windows**, puis accédez à **Internet Information Services.**</span><span class="sxs-lookup"><span data-stu-id="31d26-151">To enable this Windows feature, open the **Programs and Features** control panel, select **Turn Windows features on or off**, and navigate to **Internet Information Services.**</span></span>

   <span data-ttu-id="31d26-152">Dans les **outils de gestion Web**, activez **les scripts et les outils de gestion IIS**.</span><span class="sxs-lookup"><span data-stu-id="31d26-152">Under **Web Management Tools**, enable **IIS Management Scripts and Tools**.</span></span>



14. <span data-ttu-id="31d26-153">Dans l’écran de l' **Assistant installation terminé** , cliquez sur **Terminer**pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="31d26-153">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

   **<span data-ttu-id="31d26-154">Important</span><span class="sxs-lookup"><span data-stu-id="31d26-154">Important</span></span>**  
   <span data-ttu-id="31d26-155">Le processus d’installation peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="31d26-155">The installation can take a few minutes to finish.</span></span> <span data-ttu-id="31d26-156">Un message de statut clignote au-dessus de la zone de notification du bureau Windows, indiquant que l’installation a réussi.</span><span class="sxs-lookup"><span data-stu-id="31d26-156">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

   <span data-ttu-id="31d26-157">Le redémarrage de l’ordinateur n’est pas nécessaire lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="31d26-157">It is not necessary to reboot the computer when prompted.</span></span> <span data-ttu-id="31d26-158">Toutefois, pour optimiser les performances du système, il est recommandé de redémarrer.</span><span class="sxs-lookup"><span data-stu-id="31d26-158">However, to optimize system performance, a reboot is recommended.</span></span>



## <span data-ttu-id="31d26-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31d26-159">Related topics</span></span>


[<span data-ttu-id="31d26-160">Procédure pour installer les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="31d26-160">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)










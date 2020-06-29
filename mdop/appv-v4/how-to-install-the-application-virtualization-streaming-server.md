---
title: Procédure pour installer le serveur Application Virtualization Streaming Server
description: Procédure pour installer le serveur Application Virtualization Streaming Server
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807062"
---
# <span data-ttu-id="ff794-103">Procédure pour installer le serveur Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="ff794-103">How to Install the Application Virtualization Streaming Server</span></span>


<span data-ttu-id="ff794-104">Le serveur de diffusion en continu d’applications publie ses applications sur les clients.</span><span class="sxs-lookup"><span data-stu-id="ff794-104">The Application Virtualization Streaming Server publishes its applications to clients.</span></span> <span data-ttu-id="ff794-105">Dans un environnement qui est équilibré, il s’agit généralement de déploiements volumineux, tous les serveurs d’un groupe de serveurs doivent diffuser les mêmes applications.</span><span class="sxs-lookup"><span data-stu-id="ff794-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="ff794-106">Si les serveurs de diffusion en continu de la virtualisation des applications doivent diffuser différentes applications, affectez-les à différents groupes de serveurs.</span><span class="sxs-lookup"><span data-stu-id="ff794-106">If Application Virtualization Streaming Servers are to stream different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="ff794-107">Dans ce cas, vous devrez peut-être également augmenter la capacité d’un groupe de serveurs.</span><span class="sxs-lookup"><span data-stu-id="ff794-107">In this case, you might also have to increase a server group's capacity.</span></span>

<span data-ttu-id="ff794-108">Si vous avez désigné un ordinateur cible sur le réseau et qu’un compte d’ouverture de session possède des privilèges d’administrateur local, vous pouvez utiliser la procédure suivante pour installer le serveur de diffusion en continu de l’application et l’affecter au groupe de serveurs approprié.</span><span class="sxs-lookup"><span data-stu-id="ff794-108">If you have designated a target computer on the network, with a logon account having local administrative privileges, you can use the following procedure to install the Application Virtualization Streaming Server and assign it to the appropriate server group.</span></span>

<span data-ttu-id="ff794-109">**Remarques**  L’Assistant installation peut créer un enregistrement de groupe de serveurs, s’il n’en existe pas, et un enregistrement du serveur de diffusion en continu d’applications de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="ff794-109">**Note** The Installation Wizard can create a server group record, if one does not exist, and a record of the Application Virtualization Streaming Server membership in this group.</span></span>

 

<span data-ttu-id="ff794-110">Lorsque vous avez terminé le processus d’installation, redémarrez le serveur.</span><span class="sxs-lookup"><span data-stu-id="ff794-110">After you complete the installation process, restart the server.</span></span>

**<span data-ttu-id="ff794-111">Pour installer un serveur de streaming de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="ff794-111">To install an Application Virtualization Streaming Server</span></span>**

1.  <span data-ttu-id="ff794-112">Vérifiez qu’aucune version antérieure du serveur de diffusion en continu d’applications n’est installée sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="ff794-112">Verify that no earlier versions of the Application Virtualization Streaming Server are installed on your target computer.</span></span>

    <span data-ttu-id="ff794-113">**Important**  Assurez-vous que le serveur de gestion de l’application-V n’est pas installé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ff794-113">**Important** Make sure that the App-V Management Server is not installed on this computer.</span></span> <span data-ttu-id="ff794-114">Les deux produits ne peuvent pas être installés sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ff794-114">The two products cannot be installed on the same computer.</span></span>

     

2.  <span data-ttu-id="ff794-115">Naviguez jusqu’à l’emplacement du programme d’installation du système de virtualisation des applications sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur le fichier **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="ff794-115">Navigate to the location of the Application Virtualization System Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="ff794-116">Dans la page **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff794-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="ff794-117">Dans la page **contrat de licence** , pour accepter les termes du contrat de licence, cliquez sur **J’accepte les conditions générales du**contrat de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff794-117">On the **License Agreement** page, to accept the license terms, select **I accept the licensing terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="ff794-118">Dans la page informations sur le **client** , spécifiez le **nom d’utilisateur** et l’organisation, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff794-118">On the **Customer Information** page, specify the **User name** and the organization, and then click **Next**.</span></span>

6.  <span data-ttu-id="ff794-119">Dans la page **chemin d’installation** , cliquez sur **Parcourir**, spécifiez l’emplacement où vous voulez installer le serveur de diffusion en continu, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff794-119">On the **Installation Path** page, click **Browse**, specify the location where you want to install the Streaming Server, and then click **Next**.</span></span>

7.  <span data-ttu-id="ff794-120">Sur la page **mode de sécurité de connexion** , sélectionnez le certificat de votre choix dans la liste déroulante, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff794-120">On the **Connection Security Mode** page, select the desired certificate from the drop-down list, and then click **Next**.</span></span>

    <span data-ttu-id="ff794-121">**Remarques**  Le paramètre **mode de connexion sécurisée** exige que le serveur ait configuré un certificat de serveur à partir d’une infrastructure à clé publique.</span><span class="sxs-lookup"><span data-stu-id="ff794-121">**Note** The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="ff794-122">Si un certificat de serveur n’est pas installé sur le serveur, cette option n’est pas disponible et ne peut pas être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ff794-122">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="ff794-123">Vous devez accorder au compte de service réseau l’accès en lecture au certificat utilisé.</span><span class="sxs-lookup"><span data-stu-id="ff794-123">You must grant the Network Service account read access to the certificate being used.</span></span>

     

8.  <span data-ttu-id="ff794-124">Dans la page **configuration de port TCP** , pour utiliser le port standard (554), sélectionnez **utiliser le port par défaut (554)**.</span><span class="sxs-lookup"><span data-stu-id="ff794-124">On the **TCP Port Configuration** page, to use the standard port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="ff794-125">Pour spécifier un port personnalisé, sélectionnez **utiliser un port personnalisé**, spécifiez le numéro de port dans le champ prévu à cet effet, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff794-125">To specify a custom port, select **Use custom port**, specify the port number in the field provided, and then click **Next**.</span></span>

    <span data-ttu-id="ff794-126">**Remarques**  Lorsque vous installez le serveur dans un scénario non sécurisé, vous pouvez utiliser le port par défaut (554), ou vous pouvez définir un port personnalisé.</span><span class="sxs-lookup"><span data-stu-id="ff794-126">**Note** When you install the server in a nonsecure scenario, you can use the default port (554), or you can define a custom port.</span></span>

     

9.  <span data-ttu-id="ff794-127">Dans la page **racine du contenu** , spécifiez l’emplacement de l’ordinateur cible sur lequel les fichiers SFT seront enregistrés, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff794-127">On the **Content Root** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

    <span data-ttu-id="ff794-128">**Remarques**  Si le port HTTP ou RTSP pour le serveur de streaming d’application virtuel est déjà attribué, vous serez invité à sélectionner un nouveau port.</span><span class="sxs-lookup"><span data-stu-id="ff794-128">**Note** If the HTTP or RTSP port for the Virtual Application Streaming Server is already allocated, you will be prompted to select a new port.</span></span> <span data-ttu-id="ff794-129">Spécifiez le port de votre choix, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ff794-129">Specify the desired port, and then click **Next**.</span></span>

     

10. <span data-ttu-id="ff794-130">Dans l’écran **Paramètres avancés** , entrez les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ff794-130">On the **Advanced Setting** screen, enter the following information:</span></span>

    1.  **<span data-ttu-id="ff794-131">Nombre maximal de connexions client</span><span class="sxs-lookup"><span data-stu-id="ff794-131">Max client connections</span></span>**

    2.  **<span data-ttu-id="ff794-132">Délai de connexion (s)</span><span class="sxs-lookup"><span data-stu-id="ff794-132">Connection timeout (sec)</span></span>**

    3.  **<span data-ttu-id="ff794-133">Taille du pool de threads RTSP</span><span class="sxs-lookup"><span data-stu-id="ff794-133">RTSP thread pool size</span></span>**

    4.  **<span data-ttu-id="ff794-134">Délai d’expiration RTSP (sec)</span><span class="sxs-lookup"><span data-stu-id="ff794-134">RTSP timeout (sec)</span></span>**

    5.  **<span data-ttu-id="ff794-135">Nombre de processus principaux</span><span class="sxs-lookup"><span data-stu-id="ff794-135">Number of core processes</span></span>**

    6.  **<span data-ttu-id="ff794-136">Délai d’expiration principal (s)</span><span class="sxs-lookup"><span data-stu-id="ff794-136">Core timeout (sec)</span></span>**

    7.  **<span data-ttu-id="ff794-137">Activer l’authentification des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ff794-137">Enable User authentication</span></span>**

    8.  **<span data-ttu-id="ff794-138">Activer l’autorisation de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="ff794-138">Enable User authorization</span></span>**

    9.  **<span data-ttu-id="ff794-139">Taille des blocs de cache (Ko)</span><span class="sxs-lookup"><span data-stu-id="ff794-139">Cache block size (KB)</span></span>**

    10. **<span data-ttu-id="ff794-140">Taille maximale du cache (Mo)</span><span class="sxs-lookup"><span data-stu-id="ff794-140">Maximum cache size (MB)</span></span>**

    <span data-ttu-id="ff794-141">**Remarques**  Le serveur de streaming App-V utilise les autorisations du système de fichiers NTFS pour contrôler l’accès aux applications sous le partage de contenu.</span><span class="sxs-lookup"><span data-stu-id="ff794-141">**Note** The App-V Streaming Server uses NTFS file system permissions to control access to the applications under the Content share.</span></span> <span data-ttu-id="ff794-142">Utiliser **activer l’authentification utilisateur** et **activer l’autorisation** de l’utilisateur pour contrôler si le serveur vérifie et applique les listes de contrôle d’accès (ACL) ou non.</span><span class="sxs-lookup"><span data-stu-id="ff794-142">Use **Enable User authentication** and **Enable User authorization** to control whether the server checks and enforces those access control lists (ACLs) or not.</span></span>

     

11. <span data-ttu-id="ff794-143">Dans la page **êtes-vous prêt à installer le programme** , cliquez sur **installer**pour lancer l’installation.</span><span class="sxs-lookup"><span data-stu-id="ff794-143">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

12. <span data-ttu-id="ff794-144">Dans l’écran de l' **Assistant installation terminé** , cliquez sur **Terminer**pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="ff794-144">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="ff794-145">**Important**  Le processus d’installation peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="ff794-145">**Important** The installation can take several minutes to finish.</span></span> <span data-ttu-id="ff794-146">Un message de statut clignote au-dessus de la zone de notification du bureau Windows, indiquant que l’installation a réussi.</span><span class="sxs-lookup"><span data-stu-id="ff794-146">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

    <span data-ttu-id="ff794-147">Il n’est pas nécessaire de redémarrer votre ordinateur lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="ff794-147">It is not required to restart the computer when you are prompted.</span></span> <span data-ttu-id="ff794-148">Toutefois, pour optimiser les performances du système, nous vous conseillons de redémarrer.</span><span class="sxs-lookup"><span data-stu-id="ff794-148">However, to optimize system performance, we recommend a restart.</span></span>

     

13. <span data-ttu-id="ff794-149">Répétez les étapes 1 à 12 pour chaque serveur d’application virtuel que vous devez installer.</span><span class="sxs-lookup"><span data-stu-id="ff794-149">Repeat Steps 1–12 for each Virtual Application Server that you have to install.</span></span>

## <span data-ttu-id="ff794-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff794-150">Related topics</span></span>


[<span data-ttu-id="ff794-151">Procédure pour installer les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="ff794-151">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 






---
title: Procédure pour installer et configurer l'application par défaut
description: Procédure pour installer et configurer l'application par défaut
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807078"
---
# <span data-ttu-id="cfd90-103">Procédure pour installer et configurer l'application par défaut</span><span class="sxs-lookup"><span data-stu-id="cfd90-103">How to Install and Configure the Default Application</span></span>


<span data-ttu-id="cfd90-104">L’application par défaut est fournie dans le cadre de l’installation et est automatiquement copiée dans le serveur de gestion Microsoft Application Virtualization (App-V) lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="cfd90-104">The default application is provided as part of the installation and is automatically copied to the Microsoft Application Virtualization (App-V) Management Server during installation.</span></span> <span data-ttu-id="cfd90-105">Il est utilisé pour vérifier que le serveur de gestion a été correctement installé et configuré, mais qu’il doit être publié sur le client Microsoft Application Virtualization (App-V), afin que l’utilisateur puisse y accéder.</span><span class="sxs-lookup"><span data-stu-id="cfd90-105">It is used to verify that the Management Server was installed and configured correctly, but it has to be published to the Microsoft Application Virtualization (App-V) Client so that the user can access it.</span></span>

<span data-ttu-id="cfd90-106">Utilisez les procédures suivantes pour publier l’application par défaut et la diffuser en continu.</span><span class="sxs-lookup"><span data-stu-id="cfd90-106">Use the following procedures to publish the default application and to stream it.</span></span>

**<span data-ttu-id="cfd90-107">Pour publier l’application par défaut</span><span class="sxs-lookup"><span data-stu-id="cfd90-107">To publish the default application</span></span>**

1.  <span data-ttu-id="cfd90-108">Ouvrez une session sur le serveur de gestion App-V à l’aide d’un compte membre du groupe d’administrateurs d’application-V spécifié lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="cfd90-108">Log on to the App-V Management Server by using an account that is a member of the App-V Administrators group specified during installation.</span></span>

2.  <span data-ttu-id="cfd90-109">Sur le serveur d’administration App-V, cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **console de gestion des applications**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-109">On the App-V Management Server, click **Start**, click **Administrative Tools**, and then click **Application Virtualization Management Console**.</span></span>

3.  <span data-ttu-id="cfd90-110">Dans la console de gestion App-V, cliquez sur **actions**, puis sur **se connecter au système de virtualisation des applications**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-110">In the App-V Management Console, click **Actions**, and then click **Connect to Application Virtualization System**.</span></span>

4.  <span data-ttu-id="cfd90-111">Dans la page Configuration de la **connexion** , décochez la case **utiliser une connexion sécurisée** .</span><span class="sxs-lookup"><span data-stu-id="cfd90-111">On the **Configure Connection** page, clear the **Use Secure Connection** check box.</span></span>

5.  <span data-ttu-id="cfd90-112">Dans la zone **nom d’hôte du service Web** , tapez le nom de domaine complet (FQDN) du serveur de gestion de l’application-V, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-112">In the **Web Service Host Name** box, type the fully qualified domain name (FQDN) of the App-V Management Server, and then click **OK**.</span></span>

    <span data-ttu-id="cfd90-113">**Remarques**  Vous pouvez également utiliser **localhost** pour le nom d’hôte du service Web s’il est installé sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="cfd90-113">**Note** You can also use **localhost** for the Web Service Host name if it is installed on the Management Server.</span></span>

     

6.  <span data-ttu-id="cfd90-114">Dans la console de gestion App-V, cliquez avec le bouton droit sur le nœud du **serveur** , puis cliquez sur **Options système**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-114">In the App-V Management Console, right-click the **Server** node, and click **System Options**.</span></span>

7.  <span data-ttu-id="cfd90-115">Dans l’onglet **général** , dans la zone **chemin d’accès par défaut** , entrez le chemin UNC (Universal Naming Convention) du dossier de contenu que vous avez créé sur le serveur lors de l’installation. par exemple, \ \ \ \ &lt; Server name &gt; \\Content, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-115">On the **General** tab, in the **Default Content Path** box, enter the Universal Naming Convention (UNC) path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and then click **OK**.</span></span>

    <span data-ttu-id="cfd90-116">**Important**  Utilisez le nom de domaine complet (FQDN) du nom du serveur pour permettre au client de résoudre correctement le nom.</span><span class="sxs-lookup"><span data-stu-id="cfd90-116">**Important** Use the FQDN for the server name so that the client can resolve the name correctly.</span></span>

     

8.  <span data-ttu-id="cfd90-117">Dans la console de gestion App-V, dans le volet de navigation, développez le nœud **serveur** , puis cliquez sur **applications**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-117">In the App-V Management Console, in the navigation pane, expand the **Server** node, and then click **Applications**.</span></span>

9.  <span data-ttu-id="cfd90-118">Dans le volet des rubriques, cliquez sur **application par défaut**, puis, dans le volet **actions** , cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-118">In the topic pane, click **Default Application**, and then, in the **Actions** pane, click **Properties**.</span></span>

10. <span data-ttu-id="cfd90-119">Dans la boîte de dialogue **Propriétés** , en regard de la zone **chemin d’accès** de l’OSD, cliquez sur **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-119">In the **Properties** dialog box, next to the **OSD Path** box, click **Browse**.</span></span>

11. <span data-ttu-id="cfd90-120">Dans la boîte de dialogue **ouvrir** , entrez le chemin d’accès UNC du dossier de contenu créé sur le serveur lors de l’installation. par exemple, \ \ \ \ &lt; Server name &gt; \\Content, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="cfd90-120">In the **Open** dialog box, enter the UNC path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and press ENTER.</span></span> <span data-ttu-id="cfd90-121">Vous devez utiliser le nom de serveur réel et ne pouvez pas utiliser **localhost** ici.</span><span class="sxs-lookup"><span data-stu-id="cfd90-121">You must use the actual server name and cannot use the **localhost** here.</span></span>

    <span data-ttu-id="cfd90-122">**Important**  Assurez-vous que les valeurs des zones **chemin d’accès** de l’OSD et **chemin d’accès** de l’icône sont au format UNC (par exemple, \ \ \ \ &lt; nom &gt; du serveur \\Content\\DefaultApp.ico), et pointez sur le dossier de contenu que vous avez créé lors de l’installation du serveur.</span><span class="sxs-lookup"><span data-stu-id="cfd90-122">**Important** Ensure that the values in both the **OSD Path** and **Icon Path** boxes are in UNC format (for example, \\\\&lt;Server Name&gt;\\Content\\DefaultApp.ico), and point to the Content folder you created when installing the server.</span></span> <span data-ttu-id="cfd90-123">Ne pas utiliser **localhost** ou un chemin d’accès de fichier contenant une lettre de lecteur telle que C:\\Program Files\\.. \\.. Teneur.</span><span class="sxs-lookup"><span data-stu-id="cfd90-123">Do not use **localhost** or a file path containing a drive letter such as C:\\Program Files\\..\\..\\Content.</span></span>

     

12. <span data-ttu-id="cfd90-124">Sélectionnez le fichier DefaultApp. OSD, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-124">Select the DefaultApp.osd file, and click **Open**.</span></span>

13. <span data-ttu-id="cfd90-125">Répétez les étapes précédentes pour configurer le chemin d’accès à l’icône.</span><span class="sxs-lookup"><span data-stu-id="cfd90-125">Repeat the previous steps to configure the icon path.</span></span>

14. <span data-ttu-id="cfd90-126">Cliquez sur l’onglet **autorisations d’accès** , puis vérifiez que le groupe utilisateurs d’App-V dispose d’autorisations d’accès à l’application.</span><span class="sxs-lookup"><span data-stu-id="cfd90-126">Click the **Access Permissions** tab, and confirm that the App-V Users group has access permissions to the application.</span></span>

15. <span data-ttu-id="cfd90-127">Cliquez sur l’onglet **raccourcis** , puis sur **publier sur le Bureau de l’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-127">Click the **Shortcuts** tab, and then click **Publish to User’s Desktop**.</span></span> <span data-ttu-id="cfd90-128">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfd90-128">Click **OK**.</span></span>

16. <span data-ttu-id="cfd90-129">Ouvrez l’Explorateur Windows et recherchez le répertoire de contenu.</span><span class="sxs-lookup"><span data-stu-id="cfd90-129">Open Windows Explorer, and locate the Content directory.</span></span>

17. <span data-ttu-id="cfd90-130">Double-cliquez sur le fichier DefaultApp. OSD et ouvrez-le avec le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="cfd90-130">Double-click the DefaultApp.osd file, and open it with Notepad.</span></span>

18. <span data-ttu-id="cfd90-131">Recherchez la ligne contenant la balise **href** et remplacez-la par le code suivant:</span><span class="sxs-lookup"><span data-stu-id="cfd90-131">Locate the line that contains the **HREF** tag, and change it to the following code:</span></span>

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    <span data-ttu-id="cfd90-132">Ou, si vous utilisez RTSP:</span><span class="sxs-lookup"><span data-stu-id="cfd90-132">Or, if you are using RTSPS:</span></span>

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. <span data-ttu-id="cfd90-133">Fermez le fichier DefaultApp. OSD et enregistrez les modifications.</span><span class="sxs-lookup"><span data-stu-id="cfd90-133">Close the DefaultApp.osd file, and save the changes.</span></span>

**<span data-ttu-id="cfd90-134">Pour diffuser en continu l’application par défaut</span><span class="sxs-lookup"><span data-stu-id="cfd90-134">To stream the default application</span></span>**

1.  <span data-ttu-id="cfd90-135">Sur l’ordinateur sur lequel est installé le client App-V, ouvrez une session en tant qu’utilisateur membre du groupe utilisateurs de virtualisation d’application spécifié lors de l’installation du serveur.</span><span class="sxs-lookup"><span data-stu-id="cfd90-135">On the computer that has the App-V Client installed, log on as a user who is a member of the Application Virtualization Users group specified during server installation.</span></span>

2.  <span data-ttu-id="cfd90-136">Sur le bureau, le raccourci de l' **application virtualisation d’application par défaut** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cfd90-136">On the desktop, the **Default Application Virtualization Application** shortcut appears.</span></span> <span data-ttu-id="cfd90-137">Double-cliquez sur le raccourci pour démarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="cfd90-137">Double-click the shortcut to start the application.</span></span>

3.  <span data-ttu-id="cfd90-138">Barre d’État, affichée au-dessus de la zone de notification Windows, qui indique que l’application a démarré.</span><span class="sxs-lookup"><span data-stu-id="cfd90-138">A status bar, displayed above the Windows notification area, reports that the application is starting.</span></span> <span data-ttu-id="cfd90-139">Si le démarrage de l’application réussit, l’écran de titre de l’application par défaut s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cfd90-139">If the application startup is successful, the title screen for the default application is displayed.</span></span> <span data-ttu-id="cfd90-140">Cliquez sur **OK** pour fermer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="cfd90-140">Click **OK** to close the dialog box.</span></span> <span data-ttu-id="cfd90-141">Vous avez vérifié que le système de l’application-V s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="cfd90-141">You have now confirmed that the App-V system is running correctly.</span></span>

## <span data-ttu-id="cfd90-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cfd90-142">Related topics</span></span>


[<span data-ttu-id="cfd90-143">Procédure pour configurer des serveurs pour un déploiement basé sur un serveur</span><span class="sxs-lookup"><span data-stu-id="cfd90-143">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 






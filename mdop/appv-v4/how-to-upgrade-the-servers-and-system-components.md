---
title: Procédure pour mettre à niveau les serveurs et les composants système
description: Procédure pour mettre à niveau les serveurs et les composants système
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806701"
---
# <span data-ttu-id="0d3a8-103">Procédure pour mettre à niveau les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="0d3a8-103">How to Upgrade the Servers and System Components</span></span>


<span data-ttu-id="0d3a8-104">Utilisez la procédure suivante pour mettre à niveau les composants logiciels installés sur tous les ordinateurs système de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-104">Use the following procedure to upgrade software components installed on all Application Virtualization System computers.</span></span> <span data-ttu-id="0d3a8-105">Le service système de virtualisation des applications sera redémarré automatiquement sur chaque ordinateur après la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-105">Application Virtualization System services will be restarted automatically on each computer after it has been upgraded.</span></span>

**<span data-ttu-id="0d3a8-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="0d3a8-106">Note</span></span>**  
-   <span data-ttu-id="0d3a8-107">Le processus de mise à niveau arrête tous les services du système de virtualisation des applications, ce qui a pour effet d’arrêter le service du système.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-107">The upgrade process stops all Application Virtualization System services, thereby taking the system out of service.</span></span> <span data-ttu-id="0d3a8-108">Les sessions utilisateur doivent être arrêtées avant de commencer le processus de mise à niveau, et vous devez arrêter l’ensemble des services serveur de virtualisation des applications dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-108">User sessions should be shut down before you begin the upgrade process, and you should stop all Application Virtualization Server services in your environment.</span></span>

-   <span data-ttu-id="0d3a8-109">Si vous disposez de plusieurs serveurs partageant l’accès à la base de données de virtualisation des applications, tous les serveurs doivent être déconnectés pendant la mise à niveau de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-109">If you have more than one server that is sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="0d3a8-110">Nous vous conseillons de suivre les pratiques normales de votre entreprise pour la mise à niveau de la base de données, mais il est recommandé de tester la mise à niveau de la base de données en utilisant d’abord une copie de sauvegarde de la base de données sur un serveur de test.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-110">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="0d3a8-111">Ensuite, vous devez sélectionner l’un des serveurs pour la première mise à niveau, qui mettra à niveau le schéma de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-111">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="0d3a8-112">Après avoir effectué la mise à niveau de la base de données de production, vous pouvez mettre à niveau les autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-112">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

-   <span data-ttu-id="0d3a8-113">Vous pouvez effectuer une mise à niveau vers Microsoft Application Virtualization (App-V) 4.5 uniquement à partir de Microsoft Application Virtualization (App-V) 4.1 ou 4.1 SP1.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-113">You can upgrade to Microsoft Application Virtualization (App-V)4.5 only from Microsoft Application Virtualization (App-V)4.1 or4.1 SP1.</span></span> <span data-ttu-id="0d3a8-114">Pour pouvoir procéder à la mise à niveau vers App-V 4.5, vous devez désinstaller ou mettre à niveau App-V 4.0 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-114">App-V4.0 and earlier must be uninstalled or upgraded to4.1 or4.1 SP1 before upgrading to App-V4.5.</span></span>

 

**<span data-ttu-id="0d3a8-115">Pour mettre à niveau les composants logiciels sur les ordinateurs système de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="0d3a8-115">To upgrade software components on Application Virtualization System computers</span></span>**

1.  <span data-ttu-id="0d3a8-116">Naviguez jusqu’à l’emplacement du programme d’installation sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur le fichier Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-116">Navigate to the location of the Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the Setup.exe file.</span></span>

2.  <span data-ttu-id="0d3a8-117">Dans la page **Bienvenue** de l’Assistant Installation, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-117">On the **Welcome** page of the Installation Wizard, click **Next**.</span></span>

3.  <span data-ttu-id="0d3a8-118">Sur la page **contrat de licence** , lisez le contrat de licence, activez la case à cocher **accepter les termes du contrat de licence**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-118">On the **License Agreement** page, read the license agreement, check **I accept the terms in the license agreement**, and click **Next**.</span></span>

4.  <span data-ttu-id="0d3a8-119">Lorsque la page **logiciel installé** s’ouvre et affiche la liste des composants du système de virtualisation des applications installés et la version de chaque composant, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-119">When the **Installed Software** page opens and displays a list of the installed Application Virtualization System components and the version of each component, click **Next**.</span></span>

5.  <span data-ttu-id="0d3a8-120">Dans la page **avertissement de perte de session** , lisez le message affiché, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-120">On the **Session Loss Warning** page, read the displayed message and click **Next**.</span></span>

6.  <span data-ttu-id="0d3a8-121">Dans la page **connexion à la base de données de configuration** , examinez le contenu de la page, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-121">On the **Connect to Configuration Database** page, review the content on the page and click **Next**.</span></span>

7.  <span data-ttu-id="0d3a8-122">Si la page **obligatoire mise à niveau de la base de données** est affichée, une mise à niveau de la base de données est requise.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-122">If the **Database Upgrade Required** page is displayed, a database upgrade is required.</span></span> <span data-ttu-id="0d3a8-123">Entrez les informations d’identification d’administration de la base de données, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-123">Enter the database administrative credentials, and then click **Next**.</span></span> <span data-ttu-id="0d3a8-124">Si cette page n’est pas affichée, passez à l’étape 9.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-124">If this page is not displayed, skip to Step 9.</span></span>

8.  <span data-ttu-id="0d3a8-125">Dans la page **de la base de données de configuration de sauvegarde** , activez les cases à cocher appropriées pour effectuer la sauvegarde et exporter celle-ci vers un emplacement existant, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-125">On the **Backup Configuration Database** page, check the appropriate boxes to perform the backup and export it to an existing location, and then click **Next**.</span></span>

    <span data-ttu-id="0d3a8-126">**Important**  Si vous voulez être en mesure de revenir à la version précédente en cas d’échec de la mise à niveau, veillez à activer la case à cocher **effectuer une sauvegarde de la base de données de configuration** ou vous allez perdre les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-126">**Important** If you want to be able to roll back to the previous version in the event of an upgrade failure, make sure you check the **Perform a backup of the configuration database** box, or you will lose the configuration data.</span></span>

    <span data-ttu-id="0d3a8-127">Lorsque vous voulez restaurer une base de données avec le service VSS, vous devez d’abord arrêter le service App-V Server sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-127">When you want to restore a database with VSS, you must first stop the App-V Server Service on the Management Server.</span></span> <span data-ttu-id="0d3a8-128">Vous devez effectuer cette opération sur chaque serveur de gestion s’il existe plusieurs serveurs connectés à la même base de données.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-128">This should be done on every Management server if there is more than one server connected to the same database.</span></span>

     

9.  <span data-ttu-id="0d3a8-129">Sur la première page de **validation du package** , lisez le contenu, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-129">On the first **Package Validation** page, read the content and then click **Next**.</span></span>

10. <span data-ttu-id="0d3a8-130">Sur la deuxième page de **validation du package** , vous avez la possibilité d’afficher les détails de la validation du package dans une fenêtre bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-130">On the second **Package Validation** page, you have the option of displaying the details of the package validation in a Notepad window.</span></span> <span data-ttu-id="0d3a8-131">Pour afficher les détails, cliquez sur **Détails**. dans le cas contraire, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-131">To see the details, click **Details**; otherwise, click **Next**.</span></span>

11. <span data-ttu-id="0d3a8-132">Dans la page **prêt pour la mise à niveau du programme** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-132">On the **Ready to Upgrade the Program** page, click **Next**.</span></span>

12. <span data-ttu-id="0d3a8-133">Dans la page terminé de l' **Assistant Installation** , cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-133">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

13. <span data-ttu-id="0d3a8-134">Répétez les étapes 1 à 12 sur tous les autres ordinateurs sur lesquels vous avez installé la console de gestion des applications ou le composant logiciel serveur Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-134">Repeat steps 1–12 on all other computers where you installed the Application Virtualization Management Console or the Application Virtualization Server software component.</span></span>

    <span data-ttu-id="0d3a8-135">Après avoir effectué la mise à niveau du magasin de données, vous pouvez reprendre le fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="0d3a8-135">After upgrading the data store, you can resume normal operation.</span></span> <span data-ttu-id="0d3a8-136">(Le magasin de données est mis à niveau lors de la mise à niveau d’un serveur ou du service Web de gestion des applications.)</span><span class="sxs-lookup"><span data-stu-id="0d3a8-136">(The data store is upgraded when you upgrade any server or the App-V Management Web Service.)</span></span>

## <span data-ttu-id="0d3a8-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d3a8-137">Related topics</span></span>


[<span data-ttu-id="0d3a8-138">Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0d3a8-138">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 






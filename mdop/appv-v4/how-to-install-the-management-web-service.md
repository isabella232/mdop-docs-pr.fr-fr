---
title: Procédure pour installer le service de gestion Web
description: Procédure pour installer le service de gestion Web
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807042"
---
# <span data-ttu-id="ddae0-103">Procédure pour installer le service de gestion Web</span><span class="sxs-lookup"><span data-stu-id="ddae0-103">How to Install the Management Web Service</span></span>


<span data-ttu-id="ddae0-104">Suivez la procédure ci-dessous pour installer le service Web Application Virtualization Management sur un ordinateur cible sur le réseau, avec un compte de connexion doté de privilèges d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="ddae0-104">Use the following procedure to install the Application Virtualization Management Web Service on a target computer on the network, with a logon account having local administrative privileges.</span></span> <span data-ttu-id="ddae0-105">Même si ce n’est pas le cas, nous vous recommandons d’installer ce composant sur votre serveur Web.</span><span class="sxs-lookup"><span data-stu-id="ddae0-105">Although it is not required, we recommended that you install this component on your Web server.</span></span>

**<span data-ttu-id="ddae0-106">Pour installer le service Web de gestion</span><span class="sxs-lookup"><span data-stu-id="ddae0-106">To install the Management Web Service</span></span>**

1.  <span data-ttu-id="ddae0-107">Vérifiez qu’aucune version antérieure du service Web Application Virtualization n’est installée sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="ddae0-107">Verify that no previous versions of the Application Virtualization Web Service are installed on your target computer.</span></span>

2.  <span data-ttu-id="ddae0-108">Naviguez jusqu’à l’emplacement du programme d’installation du système de virtualisation des applications sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-108">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="ddae0-109">Après l’ouverture de l’Assistant Installation, dans la page **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-109">After the Installation Wizard opens, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="ddae0-110">Dans la page **contrat de licence** , pour accepter le contrat de licence, cliquez sur **J’accepte les termes du**contrat de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-110">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="ddae0-111">Dans la page **informations d’inscription** , spécifiez le **nom d’utilisateur** et les informations de l’organisation, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-111">On the **Registration Information** page, specify the **User Name** and organization information, and then click **Next**.</span></span>

6.  <span data-ttu-id="ddae0-112">Dans la page **type d’installation** , cliquez sur **personnalisé**, puis sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-112">On the **Setup Type** page, click **Custom**, and then click **Next**.</span></span>

    <span data-ttu-id="ddae0-113">**Remarques**  S’il ne s’agit pas du premier composant que vous avez installé sur votre ordinateur, la page **maintenance du programme** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ddae0-113">**Note** If this is not the first component you installed on this computer, the **Program Maintenance** page is displayed.</span></span> <span data-ttu-id="ddae0-114">Dans la page **maintenance du programme** , cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-114">On the **Program Maintenance** page, click **Modify**.</span></span>

     

7.  <span data-ttu-id="ddae0-115">Dans la page **configuration personnalisée** , effacez tous les composants du système de virtualisation des applications, à l’exception de **App Virt Management Service**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-115">On the **Custom Setup** page, clear all Application Virtualization System components except **App Virt Management Service**, and then click **Next**.</span></span>

    <span data-ttu-id="ddae0-116">**Remarques**  Si un composant est déjà installé sur l’ordinateur, vous devez le supprimer de la page de **configuration personnalisée** pour le désinstaller automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ddae0-116">**Note** If a component is already installed on the computer, by clearing it on the **Custom Setup** page, you will automatically uninstall it.</span></span>

     

8.  <span data-ttu-id="ddae0-117">Dans la page **serveur de base de données** , cliquez sur **se connecter à une base de données disponible**, puis sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-117">On the **Database Server** page, click **Connect to available database**, and then click **Next**.</span></span>

    <span data-ttu-id="ddae0-118">**Remarques**  Dans un environnement de production, Microsoft part du principe que vous êtes connecté à une base de données existante.</span><span class="sxs-lookup"><span data-stu-id="ddae0-118">**Note** In a production environment, Microsoft assumes that you will connect to an existing database.</span></span> <span data-ttu-id="ddae0-119">Pour installer une base de données, reportez-vous [à la rubrique installation d’une base de données](how-to-install-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="ddae0-119">If you want to install a database, see [How to Install a Database](how-to-install-a-database.md).</span></span> <span data-ttu-id="ddae0-120">Après l’installation de la base de données, passez à l’étape 13.</span><span class="sxs-lookup"><span data-stu-id="ddae0-120">After installing the database, continue with step 13.</span></span>

     

9.  <span data-ttu-id="ddae0-121">Dans la page **type du serveur de base de données** , sélectionnez un type de base de données dans la liste, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-121">On the **Database Server Type** page, select a database type from the list, and then click **Next**.</span></span>

10. <span data-ttu-id="ddae0-122">Sur la **page emplacement du serveur de base de données** , sélectionnez un serveur de base de données dans la liste des serveurs disponibles ou ajouter un serveur en activant la case à cocher **utiliser le nom d’hôte suivant** et en entrant les informations dans les zones **nom du serveur** et numéro de **port** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-122">On the **Database Server Location** page, select a database server from the list of available servers or add a server by selecting the **Use the following host name** check box and entering information in the **Server Name** and **Port Number** boxes, and then click **Next**.</span></span>

11. <span data-ttu-id="ddae0-123">Dans la page **Sélectionner une base de données** , sélectionnez la base de données souhaitée, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-123">On the **Select Database** page, select the database you want, and then click **Next**.</span></span>

12. <span data-ttu-id="ddae0-124">Dans la page **Configuration utilisateur de la base de données** , entrez les informations d’identification que le service Web de gestion doit utiliser pour accéder au magasin de données, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-124">On the **Database User Configuration** page, enter the credentials that the Management Web Service will use to access the data store, and then click **Next**.</span></span>

13. <span data-ttu-id="ddae0-125">Dans la page **êtes-vous prêt à modifier le programme** , cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-125">On the **Ready to Modify the Program** page, click **Install**.</span></span>

    <span data-ttu-id="ddae0-126">**Remarques**  S’il s’agit du premier composant que vous installez, la page **prêt à installer le programme** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ddae0-126">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="ddae0-127">Dans la page, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-127">On the page, click **Install**.</span></span>

     

14. <span data-ttu-id="ddae0-128">Dans la page terminé de l' **Assistant Installation** , cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ddae0-128">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

## <span data-ttu-id="ddae0-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ddae0-129">Related topics</span></span>


[<span data-ttu-id="ddae0-130">Procédure pour installer les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="ddae0-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 






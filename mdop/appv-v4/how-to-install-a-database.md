---
title: Procédure pour installer une base de données
description: Procédure pour installer une base de données
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807082"
---
# <span data-ttu-id="c8327-103">Procédure pour installer une base de données</span><span class="sxs-lookup"><span data-stu-id="c8327-103">How to Install a Database</span></span>


<span data-ttu-id="c8327-104">Vous pouvez utiliser la procédure suivante pour installer une base de données pour le déploiement de la virtualisation de l’application sur serveur si une base de données n’est pas encore disponible.</span><span class="sxs-lookup"><span data-stu-id="c8327-104">You can use the following procedure to install a database for your server-based deployment of Application Virtualization if a database is not already available.</span></span> <span data-ttu-id="c8327-105">En règle générale, dans un environnement de production, vous devez vous connecter à une base de données existante.</span><span class="sxs-lookup"><span data-stu-id="c8327-105">Typically, in a production environment, you will connect to an existing database.</span></span>

<span data-ttu-id="c8327-106">**Important**  Pour installer la base de données, vous devez utiliser un compte réseau doté des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="c8327-106">**Important** To install the database, you must use a network account with the appropriate permissions.</span></span> <span data-ttu-id="c8327-107">Si votre organisation exige que seuls les administrateurs de base de données soient autorisés à créer et à effectuer des mises à jour de la base de données, des scripts permettent d’effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="c8327-107">If your organization requires that only database administrators are allowed to create and conduct database upgrades, scripts are available that allow this task to be performed.</span></span>

 

**<span data-ttu-id="c8327-108">Pour installer une base de données</span><span class="sxs-lookup"><span data-stu-id="c8327-108">To install a database</span></span>**

1.  <span data-ttu-id="c8327-109">Naviguez jusqu’à l’emplacement du programme d’installation du système de virtualisation des applications sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="c8327-109">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

2.  <span data-ttu-id="c8327-110">Dans la **page Bienvenue**, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-110">On the **Welcome Page**, click **Next**.</span></span>

3.  <span data-ttu-id="c8327-111">Dans la page **contrat de licence** , pour accepter le contrat de licence, cliquez sur **J’accepte les termes du**contrat de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-111">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and click **Next**.</span></span>

4.  <span data-ttu-id="c8327-112">Dans la page **informations d’inscription** , spécifiez le nom d' **utilisateur** et les informations de l' **organisation** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-112">On the **Registering Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

5.  <span data-ttu-id="c8327-113">Dans la page **type d’installation** , sélectionnez **personnalisé** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-113">On the **Setup Type** page, select **Custom** and then click **Next**.</span></span>

6.  <span data-ttu-id="c8327-114">Dans la page **configuration personnalisée** , désélectionnez tous les composants du système de virtualisation des applications, à l’exception du **serveur de virtualisation des applications**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-114">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    <span data-ttu-id="c8327-115">**Remarques**  Si un composant est déjà installé sur l’ordinateur, vous devez le désélectionner sur l’écran de **configuration personnalisé** pour le désinstaller automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c8327-115">**Note** If a component is already installed on the computer, by deselecting it on the **Custom Setup** screen it will automatically be uninstalled.</span></span>

     

7.  <span data-ttu-id="c8327-116">Dans la page **serveur de base de données** , tapez les mots de passe, attribuez un chemin d’installation, enregistrez les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-116">On the **Database Server** page, type the passwords, assign an installation path, save the information, and click **Next**.</span></span>

8.  <span data-ttu-id="c8327-117">Sélectionnez un nom pour la base de données, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-117">Select a name for the database, and then click **Next**.</span></span>

    <span data-ttu-id="c8327-118">**Remarques**  Si l’erreur 25109 s’affiche lorsque vous essayez d’effectuer cette étape, vous avez configuré incorrectement les autorisations nécessaires pour l’installation de la base de données.</span><span class="sxs-lookup"><span data-stu-id="c8327-118">**Note** If error 25109 is displayed when you try to complete this step, you have incorrectly set up the permissions necessary to install the database.</span></span> <span data-ttu-id="c8327-119">Pour plus d’informations sur la configuration des autorisations SQL nécessaires, voir <https://go.microsoft.com/fwlink/?LinkId=132144> .</span><span class="sxs-lookup"><span data-stu-id="c8327-119">For details on setting up the necessary SQL permissions, please see <https://go.microsoft.com/fwlink/?LinkId=132144>.</span></span>

     

9.  <span data-ttu-id="c8327-120">Dans l’écran **serveur d’annuaire** , entrez le nom de domaine et les informations d’identification que les serveurs de virtualisation des applications et le service Web de gestion doivent utiliser pour accéder à votre contrôleur de domaine, enregistrer ces informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-120">On the **Directory Server** screen, enter a domain name and credentials that Application Virtualization Servers and the Management Web Service will use to access your domain controller, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="c8327-121">**Remarques**  L’installation est par défaut celle du domaine de l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c8327-121">**Note** The installation will default to the domain of the current computer.</span></span>

     

10. <span data-ttu-id="c8327-122">Sur la page **groupe administrateur** , entrez le nom d’un groupe qui disposera des privilèges d’administrateur, enregistrez les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-122">On the **Administrator Group** page, enter the name of a group that will have Administrator privileges, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="c8327-123">**Remarques**  Vous pouvez également entrer les premiers caractères du nom d’un groupe disposant de privilèges d’administration, cliquez sur **suivant**, puis, dans l’écran **Sélectionner un groupe d’administrateurs** , sélectionnez le groupe dans la liste résultante.</span><span class="sxs-lookup"><span data-stu-id="c8327-123">**Note** You can also enter the first few characters of the name of a group that will have Administration privileges, click **Next**, and on the **Select Administrator Group** screen, select the group from the resulting list.</span></span> <span data-ttu-id="c8327-124">Enregistrez ces informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-124">Then save this information and click **Next**.</span></span>

     

11. <span data-ttu-id="c8327-125">Sur la page **groupe de fournisseurs par défaut** , entrez le nom complet d’un groupe qui contrôlera l’accès aux applications, enregistrez les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-125">On the **Default Provider Group** page, enter the complete name of a group that will control access to applications, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="c8327-126">**Remarques**  Vous pouvez également entrer les premiers caractères du nom d’un groupe qui contrôleront l’accès aux applications, cliquez sur **suivant**, puis, dans l’écran **Sélectionner le groupe du fournisseur par défaut** , sélectionnez le groupe dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c8327-126">**Note** You can also enter the first few characters of the name of a group that will control access to applications, click **Next**, and on the **Select Default Provider Group** screen, select the group in the list.</span></span> <span data-ttu-id="c8327-127">Enregistrez ces informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c8327-127">Then save this information and click **Next**.</span></span>

     

12. <span data-ttu-id="c8327-128">Dans la page terminé de l' **Assistant Installation** , cliquez sur **Terminer**pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="c8327-128">On the **Installation Wizard Completed** page, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="c8327-129">**Important**  Le processus d’installation peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="c8327-129">**Important** The installation can take a few minutes to finish.</span></span> <span data-ttu-id="c8327-130">Un message de statut clignote au-dessus de la zone de notification du bureau Windows, indiquant si l’installation a réussi.</span><span class="sxs-lookup"><span data-stu-id="c8327-130">A status message will flash above the Windows desktop notification area, indicating whether the installation succeeded.</span></span>

     

## <span data-ttu-id="c8327-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8327-131">Related topics</span></span>


[<span data-ttu-id="c8327-132">Procédure pour installer les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="c8327-132">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 






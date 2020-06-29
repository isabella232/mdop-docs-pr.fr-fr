---
title: Procédure pour installer la console de gestion
description: Procédure pour installer la console de gestion
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807053"
---
# <span data-ttu-id="292c0-103">Procédure pour installer la console de gestion</span><span class="sxs-lookup"><span data-stu-id="292c0-103">How to Install the Management Console</span></span>


<span data-ttu-id="292c0-104">Vous pouvez utiliser la procédure suivante pour installer la console de gestion des applications de virtualisation sur un ordinateur cible sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="292c0-104">You can use the following procedure to install the Application Virtualization Management Console on a target computer on the network.</span></span> <span data-ttu-id="292c0-105">Vous devez utiliser un compte réseau qui dispose de privilèges d’administrateur sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="292c0-105">You must use a network account that has administrator privileges on the target computer.</span></span> <span data-ttu-id="292c0-106">Vous pouvez utiliser la console pour configurer et gérer la plateforme de système de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="292c0-106">You can use the console to configure and manage the Application Virtualization System Platform.</span></span>

<span data-ttu-id="292c0-107">Pour pouvoir effectuer cette procédure, vous devez installer le service Web Application Virtualization Management sur cet ordinateur ou sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="292c0-107">Before you can complete this procedure, you must install the Application Virtualization Management Web Service on this or a different computer.</span></span> <span data-ttu-id="292c0-108">Le service Web de gestion vous permet d’accéder au magasin de données et au contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="292c0-108">The Management Web Service allows you to access the data store and the domain controller.</span></span> <span data-ttu-id="292c0-109">Pour plus d’informations sur l’installation du service Web, voir [Comment installer le service Web de gestion](how-to-install-the-management-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="292c0-109">For more information about installing the Web service, see [How to Install the Management Web Service](how-to-install-the-management-web-service.md).</span></span>

**<span data-ttu-id="292c0-110">Pour installer la console de gestion</span><span class="sxs-lookup"><span data-stu-id="292c0-110">To install the Management Console</span></span>**

1.  <span data-ttu-id="292c0-111">Vérifiez qu’aucune version antérieure de la console de gestion n’est installée sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="292c0-111">Verify that no previous versions of the Management Console are installed on the target computer.</span></span>

2.  <span data-ttu-id="292c0-112">Naviguez jusqu’à l’emplacement du programme d’installation du système de virtualisation des applications sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="292c0-112">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="292c0-113">Dans la **page Bienvenue**, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="292c0-113">On the **Welcome Page**, click **Next**.</span></span>

4.  <span data-ttu-id="292c0-114">Dans la page **contrat de licence** , pour accepter le contrat de licence, cliquez sur **J’accepte les termes du**contrat de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="292c0-114">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="292c0-115">Dans la page **informations d’inscription** , spécifiez le **nom d’utilisateur** et les informations de l' **organisation** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="292c0-115">On the **Registration Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

6.  <span data-ttu-id="292c0-116">Dans la page **type d’installation** , cliquez sur **personnalisé** , puis sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="292c0-116">On the **Setup Type** page, click **Custom** and then click **Next**.</span></span>

7.  <span data-ttu-id="292c0-117">Dans la page **configuration personnalisée** , désélectionnez tous les composants du système de virtualisation des applications, à l’exception de la **console de gestion**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="292c0-117">On the **Custom Setup** page, deselect all Application Virtualization System components except **Management Console**, and then click **Next**.</span></span>

    <span data-ttu-id="292c0-118">**Remarques**  Si un composant est déjà installé sur l’ordinateur, vous devez le désélectionner sur l’écran de configuration personnalisé pour le désinstaller automatiquement.</span><span class="sxs-lookup"><span data-stu-id="292c0-118">**Note** If a component is already installed on the computer, by deselecting it on the Custom Setup screen, it will automatically be uninstalled.</span></span>

     

8.  <span data-ttu-id="292c0-119">Dans l’écran êtes-vous **prêt à modifier l’application** , cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="292c0-119">On the **Ready to Modify the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="292c0-120">**Remarques**  S’il s’agit du premier composant que vous installez, la page **prêt à installer le programme** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="292c0-120">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="292c0-121">Pour démarrer l’installation, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="292c0-121">To start the installation, click **Install**.</span></span>

     

9.  <span data-ttu-id="292c0-122">Dans l’écran de l' **Assistant installation terminé** , cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="292c0-122">On the **Installation Wizard Completed** screen, click **Finish**.</span></span> <span data-ttu-id="292c0-123">Cliquez sur **OK** pour redémarrer l’ordinateur et terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="292c0-123">Click **Okay** to restart the computer and complete the installation.</span></span>

10. <span data-ttu-id="292c0-124">Dans le panneau de configuration Windows, double-cliquez sur **Outils d’administration** , puis cliquez sur **console de gestion des applications** pour afficher la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="292c0-124">In the Windows Control Panel, double-click **Administrative Tools** and then click **Application Virtualization Management Console** to display the Management Console.</span></span>

11. <span data-ttu-id="292c0-125">Cliquez sur l’icône de **connexion** ou cliquez avec le bouton droit sur le conteneur **Application Virtualization Systems** , puis cliquez sur **se connecter au système de virtualisation des applications**.</span><span class="sxs-lookup"><span data-stu-id="292c0-125">Click the **Connect** icon, or right-click the **Application Virtualization Systems** container, and then click **Connect to Application Virtualization System**.</span></span>

12. <span data-ttu-id="292c0-126">Dans l’écran **connexion au système de virtualisation des applications** , entrez le nom d’hôte et le port de l’ordinateur de service Web de gestion, modifiez les informations de sécurité et les informations d’identification d’ouverture de session si nécessaire, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="292c0-126">On the **Connect to Application Virtualization System** screen, enter the host name and port of the Management Web Service computer, change the security information and login credentials if necessary, and then click **OK**.</span></span>

13. <span data-ttu-id="292c0-127">Après vous être connecté à l’ordinateur de service Web de gestion, cliquez sur **fichier** dans le menu de la **console** , puis cliquez sur **quitter**.</span><span class="sxs-lookup"><span data-stu-id="292c0-127">After connecting to the Management Web Service computer, click **File** on the **Console** menu, and then click **Exit**.</span></span> <span data-ttu-id="292c0-128">Cliquez sur **Oui** pour enregistrer les paramètres de la console.</span><span class="sxs-lookup"><span data-stu-id="292c0-128">Click **Yes** to save console settings.</span></span>

## <span data-ttu-id="292c0-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="292c0-129">Related topics</span></span>


[<span data-ttu-id="292c0-130">Procédure pour installer les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="292c0-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 






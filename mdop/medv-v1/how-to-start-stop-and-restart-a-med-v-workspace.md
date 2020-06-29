---
title: Comment démarrer, arrêter et redémarrer un espace de travail MED-V
description: Comment démarrer, arrêter et redémarrer un espace de travail MED-V
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811327"
---
# <span data-ttu-id="98faa-103">Comment démarrer, arrêter et redémarrer un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="98faa-103">How to Start, Stop, and Restart a MED-V Workspace</span></span>


**<span data-ttu-id="98faa-104">Pour créer un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="98faa-104">To start a MED-V workspace</span></span>**

1.  <span data-ttu-id="98faa-105">Dans la zone de notification, cliquez avec le bouton droit sur l’icône MED-V.</span><span class="sxs-lookup"><span data-stu-id="98faa-105">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="98faa-106">Dans le sous-menu, cliquez sur **Démarrer l’espace de travail**.</span><span class="sxs-lookup"><span data-stu-id="98faa-106">On the submenu, click **Start Workspace**.</span></span>

    -   <span data-ttu-id="98faa-107">S’il existe plusieurs espaces de travail MED-V en cours d’exécution sur l’ordinateur, la fenêtre **de sélection de l’espace de travail** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="98faa-107">If there are multiple MED-V workspaces running on the computer, the **Workspace Selection** window appears.</span></span>

        1.  <span data-ttu-id="98faa-108">Sélectionnez un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="98faa-108">Select a MED-V workspace.</span></span>

        2.  <span data-ttu-id="98faa-109">Activez la case à cocher **Démarrer l’espace de travail sélectionné sans m’avertir** pour ignorer cette fenêtre la prochaine fois que le client est démarré et l’ouverture automatique de l’espace de travail MED-V sélectionné.</span><span class="sxs-lookup"><span data-stu-id="98faa-109">Select the **Start the selected Workspace without asking me** check box to skip this window the next time the client is started and to automatically open the selected MED-V workspace.</span></span>

        3.  <span data-ttu-id="98faa-110">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="98faa-110">Click **OK**.</span></span>

    <span data-ttu-id="98faa-111">La fenêtre **Démarrer l’authentification de l’espace de travail** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="98faa-111">The **Start Workspace Authentication** window appears.</span></span>

    -   <span data-ttu-id="98faa-112">S’il existe plusieurs espaces de travail MED-V sur l’ordinateur et que vous avez choisi d’utiliser un espace de travail MED-V, la fenêtre affichée dans la figure ci-dessous s’affiche.</span><span class="sxs-lookup"><span data-stu-id="98faa-112">If there are several MED-V workspaces on the computer and you have opted to use a specified MED-V workspace, the window shown in the following figure appears.</span></span>

        ![](images/medv-logon.gif)

    -   <span data-ttu-id="98faa-113">S’il n’y a qu’un seul espace de travail MED-V sur l’ordinateur, l’option «démarrer le dernier espace de travail utilisé» n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="98faa-113">If there is only one MED-V workspace on the computer, the “Start last used Workspace” option is unavailable.</span></span>

3.  <span data-ttu-id="98faa-114">Entrez les informations d’identification de l’utilisateur de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="98faa-114">Type in your domain user credentials.</span></span>

    <span data-ttu-id="98faa-115">**Remarques**  Lors du premier démarrage d’un espace de travail MED-V, le nom d’utilisateur doit présenter le format suivant: nom de &lt; domaine nom d' &gt; \\ &lt; utilisateur &gt; .</span><span class="sxs-lookup"><span data-stu-id="98faa-115">**Note** The first time a MED-V workspace is started, the user name should be in the following format: &lt;domain name&gt;\\&lt;user name&gt;.</span></span>

     

4.  <span data-ttu-id="98faa-116">Sélectionnez **enregistrer mon mot** de passe pour enregistrer votre mot de passe entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="98faa-116">Select **Save my password** to save your password between sessions.</span></span>

    <span data-ttu-id="98faa-117">**Remarques**  Pour activer la fonctionnalité enregistrer le mot de passe, l’attribut EnableSavePassword doit être défini sur true dans le fichier ClientSettings.xml.</span><span class="sxs-lookup"><span data-stu-id="98faa-117">**Note** To enable the save password feature, the EnableSavePassword attribute must be set to True in the ClientSettings.xml file.</span></span> <span data-ttu-id="98faa-118">Le fichier se trouve dans le dossier *Servers\\Configuration Server\\* .</span><span class="sxs-lookup"><span data-stu-id="98faa-118">The file can be found in the *Servers\\Configuration Server\\* folder.</span></span>

     

5.  <span data-ttu-id="98faa-119">Décochez la case **Démarrer le dernier espace de travail utilisé** pour choisir un autre espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="98faa-119">Clear the **Start last used workspace** check box to choose a different MED-V workspace.</span></span>

6.  <span data-ttu-id="98faa-120">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="98faa-120">Click **OK**.</span></span>

    <span data-ttu-id="98faa-121">Plusieurs écrans de statut apparaissent en fonction de la configuration de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="98faa-121">Several status screens appear depending on the MED-V workspace configuration.</span></span>

    <span data-ttu-id="98faa-122">L’écran **de démarrage** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="98faa-122">The **Starting Workspace** screen appears.</span></span>

**<span data-ttu-id="98faa-123">Pour redémarrer une version d’un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="98faa-123">To restart a MED-V workspace</span></span>**

1.  <span data-ttu-id="98faa-124">Lorsque le client est en cours d’exécution, dans la zone de notification, cliquez avec le bouton droit sur l’icône MED-V.</span><span class="sxs-lookup"><span data-stu-id="98faa-124">When the client is running, in the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="98faa-125">Dans le sous-menu, cliquez sur **redémarrer l’espace de travail**.</span><span class="sxs-lookup"><span data-stu-id="98faa-125">On the submenu, click **Restart Workspace**.</span></span>

    <span data-ttu-id="98faa-126">L’espace de travail MED-V est redémarré.</span><span class="sxs-lookup"><span data-stu-id="98faa-126">The MED-V workspace is restarted.</span></span>

    -   <span data-ttu-id="98faa-127">Dans un espace de travail MED-V permanent, l’ordinateur virtuel est arrêté, puis redémarré.</span><span class="sxs-lookup"><span data-stu-id="98faa-127">In a persistent MED-V workspace, the virtual machine is shut down and then restarted.</span></span>

    -   <span data-ttu-id="98faa-128">Dans un espace de travail MED-V revertible, l’ordinateur virtuel ne s’arrête pas réellement; au lieu de cela, il revient à son état d’origine.</span><span class="sxs-lookup"><span data-stu-id="98faa-128">In a revertible MED-V workspace, the virtual machine does not actually shut down; instead, it returns to its original state.</span></span>

**<span data-ttu-id="98faa-129">Pour mettre fin à un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="98faa-129">To stop a MED-V workspace</span></span>**

1.  <span data-ttu-id="98faa-130">Dans la zone de notification, cliquez avec le bouton droit sur l’icône MED-V.</span><span class="sxs-lookup"><span data-stu-id="98faa-130">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="98faa-131">Dans le sous-menu, cliquez sur **arrêter l’espace de travail**.</span><span class="sxs-lookup"><span data-stu-id="98faa-131">On the submenu, click **Stop Workspace**.</span></span>

    <span data-ttu-id="98faa-132">L’espace de travail MED-V est arrêté.</span><span class="sxs-lookup"><span data-stu-id="98faa-132">The MED-V workspace is stopped.</span></span>

## <span data-ttu-id="98faa-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="98faa-133">Related topics</span></span>


[<span data-ttu-id="98faa-134">Comment démarrer et quitter le client MED-V</span><span class="sxs-lookup"><span data-stu-id="98faa-134">How to Start and Exit the MED-V Client</span></span>](how-to-start-and-exit-the-med-v-client.md)

 

 






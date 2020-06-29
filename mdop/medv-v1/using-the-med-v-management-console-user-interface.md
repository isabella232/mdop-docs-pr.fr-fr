---
title: Utilisation de l'interface utilisateur de la console de gestion MED-V
description: Utilisation de l'interface utilisateur de la console de gestion MED-V
author: dansimp
ms.assetid: f42714d7-6f0c-4995-ab31-d4ef0845a22c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22fc98c3edbea48847e1a00369bea21a470e66b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811400"
---
# <span data-ttu-id="a3bac-103">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="a3bac-103">Using the MED-V Management Console User Interface</span></span>


<span data-ttu-id="a3bac-104">L’interface utilisateur de la console est divisée en sections suivantes:</span><span class="sxs-lookup"><span data-stu-id="a3bac-104">The console user interface is divided into the following sections:</span></span>

-   <span data-ttu-id="a3bac-105">Les **boutons d’administration de MED-V**suivants qui correspondent aux trois modules:</span><span class="sxs-lookup"><span data-stu-id="a3bac-105">The following **MED-V management buttons**, which correspond to the three modules:</span></span>

    -   <span data-ttu-id="a3bac-106">**Stratégie**: le module de **stratégie** permet de définir les espaces de travail MED-V et leurs paramètres et autorisations associés.</span><span class="sxs-lookup"><span data-stu-id="a3bac-106">**Policy**—The **Policy** module is used to define the MED-V workspaces and their related settings and permissions.</span></span>

    -   <span data-ttu-id="a3bac-107">**Images**: le module **images** permet de gérer les images d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="a3bac-107">**Images**—The **Images** module is used to manage MED-V workspace images.</span></span>

    -   <span data-ttu-id="a3bac-108">**Rapports**: le module **rapports** est utilisé pour générer et afficher des rapports d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="a3bac-108">**Reports**—The **Reports** module is used for generating and viewing MED-V workspace reports.</span></span>

-   <span data-ttu-id="a3bac-109">La **barre d’outils** affiche des raccourcis relatifs au bouton sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a3bac-109">The **toolbar** displays shortcuts relevant to the button selected.</span></span>

-   <span data-ttu-id="a3bac-110">Le **volet d’affichage** affiche un module correspondant au bouton sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a3bac-110">The **display pane** displays a module corresponding to the button that is selected.</span></span>

![](images/medv-ui-console-general.gif)

## <span data-ttu-id="a3bac-111">Se connecter à la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="a3bac-111">How to Log In to the MED-V Management Console</span></span>


**<span data-ttu-id="a3bac-112">Pour ouvrir la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="a3bac-112">To open the MED-V management console</span></span>**

-   <span data-ttu-id="a3bac-113">Dans le menu **Démarrer** de Windows, sélectionnez \*\*tous les programmes &gt; gestion &gt; \*\*med-v de med-v ou sur le bureau, double-cliquez sur l’icône gestion Med-v.</span><span class="sxs-lookup"><span data-stu-id="a3bac-113">On the Windows **Start** menu, select **All Programs &gt; MED-V &gt; MED-V Management**, or on the desktop, double-click the MED-V Management icon.</span></span>

    <span data-ttu-id="a3bac-114">La fenêtre de **connexion gestion MED-V** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a3bac-114">The **MED-V Management Login** window appears.</span></span>

<span data-ttu-id="a3bac-115">**Remarques**  Pour des raisons de sécurité, le premier utilisateur à se connecter à la console de gestion MED-V devient le seul utilisateur de cet ordinateur autorisé à accéder à la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="a3bac-115">**Note** For security reasons, the first user to log in to the MED-V management console will become the only user on that computer allowed to access the management console.</span></span>

 

**<span data-ttu-id="a3bac-116">Pour vous connecter</span><span class="sxs-lookup"><span data-stu-id="a3bac-116">To log in</span></span>**

1.  <span data-ttu-id="a3bac-117">Entrez les informations d’identification de l’utilisateur de votre domaine au format suivant:</span><span class="sxs-lookup"><span data-stu-id="a3bac-117">Type in your domain user credentials in the following format:</span></span>

    <span data-ttu-id="a3bac-118">"Domain \ _name \\user\ _name", "password"</span><span class="sxs-lookup"><span data-stu-id="a3bac-118">"domain\_name\\user\_name", "password"</span></span>

    <span data-ttu-id="a3bac-119">**Remarques**  Lors de la configuration du serveur, les utilisateurs disposant d’un accès complet ainsi que des utilisateurs dotés d’un accès en lecture seule sont définis.</span><span class="sxs-lookup"><span data-stu-id="a3bac-119">**Note** When configuring the server, users with full access as well as users with read-only access are defined.</span></span> <span data-ttu-id="a3bac-120">Tous les utilisateurs doivent être utilisateurs de domaines.</span><span class="sxs-lookup"><span data-stu-id="a3bac-120">All users must be domain users.</span></span> <span data-ttu-id="a3bac-121">Le nom d’utilisateur et le mot de passe du domaine sont utilisés pour la connexion de gestion MED-V.</span><span class="sxs-lookup"><span data-stu-id="a3bac-121">The domain user name and password is used for MED-V management login.</span></span>

     

2.  <span data-ttu-id="a3bac-122">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3bac-122">Click **OK**.</span></span>

    <span data-ttu-id="a3bac-123">La console de **gestion MED-V** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a3bac-123">The **MED-V Management** console appears.</span></span>

## <span data-ttu-id="a3bac-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3bac-124">Related topics</span></span>


[<span data-ttu-id="a3bac-125">Comment installer le client MED-V et la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="a3bac-125">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

 

 






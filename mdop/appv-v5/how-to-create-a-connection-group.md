---
title: Comment créer un groupe de connexion
description: Comment créer un groupe de connexion
author: dansimp
ms.assetid: 9d272052-2d28-4e41-989c-89610482a0ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 816fc3b37be056ed54a88c394ef64fa1edaf47ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805653"
---
# <span data-ttu-id="7d1bd-103">Comment créer un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="7d1bd-103">How to Create a Connection Group</span></span>


<span data-ttu-id="7d1bd-104">Suivez ces étapes pour créer un groupe de connexion à l’aide de la console de gestion App-V.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="7d1bd-105">Pour utiliser PowerShell afin de créer des groupes de connexion, reportez-vous [à la rubrique Comment gérer les groupes de connexion sur un ordinateur autonome à l’aide de PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="7d1bd-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span></span>

<span data-ttu-id="7d1bd-106">Lorsque vous placez des packages dans un groupe de connexions, leurs chemins d’accès racines de package sont fusionnés.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="7d1bd-107">Si vous supprimez des packages, seuls les packages restants maintiennent la racine fusionnée.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="7d1bd-108">Pour créer un groupe de connexions</span><span class="sxs-lookup"><span data-stu-id="7d1bd-108">To create a connection group</span></span>**

1.  <span data-ttu-id="7d1bd-109">Dans la console de gestion App-V 5,0, sélectionnez **packages**.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-109">In the App-V 5.0 Management Console, select **Packages**.</span></span>

2.  <span data-ttu-id="7d1bd-110">Sélectionnez **groupes de connexion** pour afficher la bibliothèque de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-110">Select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

3.  <span data-ttu-id="7d1bd-111">Pour créer un groupe de connexion, sélectionnez **Ajouter un groupe de connexion** .</span><span class="sxs-lookup"><span data-stu-id="7d1bd-111">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

4.  <span data-ttu-id="7d1bd-112">Dans le volet **nouveau groupe de connexions** , tapez une description pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-112">In the **New Connection Group** pane, type a description for the group.</span></span>

5.  <span data-ttu-id="7d1bd-113">Cliquez sur **modifier** dans le volet **packages connectés** pour ajouter une nouvelle application au groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-113">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

6.  <span data-ttu-id="7d1bd-114">Dans le volet **bibliothèque entière** , sélectionnez l’application que vous voulez ajouter, puis cliquez sur la flèche pour ajouter l’application.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-114">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="7d1bd-115">Pour supprimer une application, sélectionnez l’application à supprimer dans le volet **packages dans** , puis cliquez sur la flèche.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-115">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="7d1bd-116">Pour redéfinir la priorité des applications de votre groupe de connexion, utilisez les flèches du volet **packages dans** .</span><span class="sxs-lookup"><span data-stu-id="7d1bd-116">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="7d1bd-117">**Important**  Par défaut, les configurations d’accès aux services de domaine Active Directory associées à une application spécifique ne sont pas ajoutées au groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-117">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="7d1bd-118">Pour transférer la configuration de l’accès Active Directory, sélectionnez **Ajouter l’accès au package à l’accès au groupe**, qui se trouve dans le volet **packages dans** .</span><span class="sxs-lookup"><span data-stu-id="7d1bd-118">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

7.  <span data-ttu-id="7d1bd-119">Après avoir ajouté toutes les applications et configuré l’accès Active Directory, cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="7d1bd-119">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="7d1bd-120">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="7d1bd-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="7d1bd-121">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="7d1bd-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="7d1bd-122">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="7d1bd-122">Got an App-V issue?</span></span>** <span data-ttu-id="7d1bd-123">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="7d1bd-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="7d1bd-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d1bd-124">Related topics</span></span>


[<span data-ttu-id="7d1bd-125">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="7d1bd-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="7d1bd-126">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="7d1bd-126">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 






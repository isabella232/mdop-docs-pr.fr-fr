---
title: Procédure pour ajouter manuellement une application
description: Procédure pour ajouter manuellement une application
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806970"
---
# <span data-ttu-id="723f2-103">Procédure pour ajouter manuellement une application</span><span class="sxs-lookup"><span data-stu-id="723f2-103">How to Manually Add an Application</span></span>


<span data-ttu-id="723f2-104">Lors de l’ajout d’une application au serveur de gestion de la virtualisation des applications, il est recommandé de l’importer.</span><span class="sxs-lookup"><span data-stu-id="723f2-104">When adding an application to the Application Virtualization Management Server, it is recommended that you import it.</span></span> <span data-ttu-id="723f2-105">Vous pouvez ajouter une application manuellement, mais vous devez fournir des informations précises et détaillées sur l’application appelée dans cette section.</span><span class="sxs-lookup"><span data-stu-id="723f2-105">You can add an application manually, but you must provide the precise, detailed information about the application called for in this section.</span></span>

**<span data-ttu-id="723f2-106">Pour ajouter manuellement une nouvelle application</span><span class="sxs-lookup"><span data-stu-id="723f2-106">To manually add a new application</span></span>**

1.  <span data-ttu-id="723f2-107">Dans le volet gauche, cliquez avec le bouton droit sur le nœud **applications** et sélectionnez **nouvelle application**.</span><span class="sxs-lookup"><span data-stu-id="723f2-107">In the left pane, right-click the **Applications** node and choose **New Application**.</span></span>

2.  <span data-ttu-id="723f2-108">Dans l' **Assistant Nouvelle application**, complétez la boîte de dialogue **informations générales** :</span><span class="sxs-lookup"><span data-stu-id="723f2-108">In the **New Application Wizard**, complete the **General Information** dialog box:</span></span>

    1.  <span data-ttu-id="723f2-109">**Nom**de l’application: tapez le nom que vous voulez que les utilisateurs voient.</span><span class="sxs-lookup"><span data-stu-id="723f2-109">**Application Name**—Type the name you want the users to see.</span></span>

    2.  <span data-ttu-id="723f2-110">**Version**: tapez la version de l’application.</span><span class="sxs-lookup"><span data-stu-id="723f2-110">**Version**—Type the application version.</span></span>

    3.  <span data-ttu-id="723f2-111">**Activée**: cette case doit être cochée pour diffuser l’application en continu après sa création.</span><span class="sxs-lookup"><span data-stu-id="723f2-111">**Enabled**—This box must be selected to stream the application after you create it.</span></span>

    4.  <span data-ttu-id="723f2-112">**Description**: tapez éventuellement une description pour une utilisation administrative.</span><span class="sxs-lookup"><span data-stu-id="723f2-112">**Description**—Type an optional description for administrative use.</span></span>

    5.  <span data-ttu-id="723f2-113">**Chemin d’accès**de l’OSD: Naviguez sur le réseau jusqu’au fichier Open Software Descriptor (OSD) de l’application.</span><span class="sxs-lookup"><span data-stu-id="723f2-113">**OSD Path**—Browse the network to the application's Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="723f2-114">Ce fichier doit se trouver dans un dossier réseau partagé.</span><span class="sxs-lookup"><span data-stu-id="723f2-114">This file must be in a shared network folder.</span></span>

    6.  <span data-ttu-id="723f2-115">**Path d’icône**: Naviguez jusqu’au fichier. ico de l’application.</span><span class="sxs-lookup"><span data-stu-id="723f2-115">**Icon Path**—Browse to the application's ICO file.</span></span>

    7.  <span data-ttu-id="723f2-116">**Groupe de licences d’application**: Si vous avez configuré des groupes de licences, vous pouvez les affecter à un en le sélectionnant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="723f2-116">**Application License Group**—If you have set up license groups, you can assign the application to one by selecting it in the pull-down list.</span></span>

    8.  <span data-ttu-id="723f2-117">**Groupe de serveurs**: Si vous disposez de plusieurs serveurs de virtualisation des applications, vous pouvez leur affecter une en le sélectionnant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="723f2-117">**Server Group**—If you have multiple Application Virtualization Servers, you can assign the application to one by selecting it in the pull-down list.</span></span>

3.  <span data-ttu-id="723f2-118">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="723f2-118">Click **Next**.</span></span>

4.  <span data-ttu-id="723f2-119">Dans la boîte de dialogue **Sélectionner un package** , sélectionnez le package associé, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="723f2-119">In the **Select Package** dialog box, select the related package and click **Next**.</span></span>

5.  <span data-ttu-id="723f2-120">Dans l’écran **raccourcis clavier publiés** , activez les cases à cocher des emplacements dans lesquels vous souhaitez que les raccourcis des applications apparaissent sur les ordinateurs clients, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="723f2-120">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers and click **Next**.</span></span>

6.  <span data-ttu-id="723f2-121">Dans l’écran **associations de fichiers** , vous pouvez ajouter de nouvelles associations de fichiers de type à cette application.</span><span class="sxs-lookup"><span data-stu-id="723f2-121">In the **File Associations** screen, you can add new type file associations to this application.</span></span> <span data-ttu-id="723f2-122">Pour cela, cliquez sur **Ajouter**, entrez l’extension (sans point précédent), entrez une description, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="723f2-122">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

7.  <span data-ttu-id="723f2-123">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="723f2-123">Click **Next**.</span></span>

8.  <span data-ttu-id="723f2-124">Dans la boîte de dialogue **autorisations d’accès** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="723f2-124">In the **Access Permissions** dialog box, click **Add**.</span></span>

9.  <span data-ttu-id="723f2-125">Dans la boîte de dialogue **Ajouter/modifier un groupe d’utilisateurs** , accédez au groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="723f2-125">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="723f2-126">Vous pouvez également entrer le domaine et le groupe en entrant les informations dans les champs correspondants.</span><span class="sxs-lookup"><span data-stu-id="723f2-126">You can also enter the domain and group by typing the information in the respective fields.</span></span> <span data-ttu-id="723f2-127">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="723f2-127">When you finish, click **OK**.</span></span> <span data-ttu-id="723f2-128">Vous pouvez ajouter d’autres groupes aux mêmes pages.</span><span class="sxs-lookup"><span data-stu-id="723f2-128">You can add other groups with the same pages.</span></span>

10. <span data-ttu-id="723f2-129">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="723f2-129">Click **Next**.</span></span>

11. <span data-ttu-id="723f2-130">Dans l’écran **Résumé** , vous pouvez consulter les paramètres d’importation.</span><span class="sxs-lookup"><span data-stu-id="723f2-130">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="723f2-131">Cliquez sur **Terminer** pour ajouter l’application, cliquez sur **précédent** pour modifier les informations ou cliquez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="723f2-131">Click **Finish** to add the application, click **Back** to change the information, or click **Cancel**.</span></span>

## <span data-ttu-id="723f2-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="723f2-132">Related topics</span></span>


[<span data-ttu-id="723f2-133">Procédure pour gérer des applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="723f2-133">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 






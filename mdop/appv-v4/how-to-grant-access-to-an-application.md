---
title: Procédure pour accorder l'accès à une application
description: Procédure pour accorder l'accès à une application
author: dansimp
ms.assetid: e54d9e84-21f5-488f-b040-25f374d9289f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9cd3dfe4661f09bb7e7d3514a397955cb892be81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807105"
---
# <span data-ttu-id="a03d7-103">Procédure pour accorder l'accès à une application</span><span class="sxs-lookup"><span data-stu-id="a03d7-103">How to Grant Access to an Application</span></span>


<span data-ttu-id="a03d7-104">En tant qu’administrateur, vous pouvez utiliser la console de gestion du serveur Application Virtualization pour déterminer les utilisateurs qui peuvent accéder aux applications.</span><span class="sxs-lookup"><span data-stu-id="a03d7-104">As the administrator, you can use the Application Virtualization Server Management Console to determine which users can access which applications.</span></span> <span data-ttu-id="a03d7-105">Vous pouvez effectuer cette opération lorsque vous importez le fichier de séquence (SPRJ) ou le fichier d’ouverture de la boîte de dialogue, ou à tout moment dans la boîte de dialogue des **Propriétés** de l’application.</span><span class="sxs-lookup"><span data-stu-id="a03d7-105">You can do this when you import the Sequencer Project (SPRJ) or Open Software Descriptor (OSD) file or at anytime using the application's **Properties** dialog box.</span></span> <span data-ttu-id="a03d7-106">À l’aide des deux méthodes, utilisez les options d' **autorisation d’accès** pour ajouter des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a03d7-106">With both methods, use the **Access Permissions** options to add users.</span></span>

**<span data-ttu-id="a03d7-107">Pour accorder l’accès à une application</span><span class="sxs-lookup"><span data-stu-id="a03d7-107">To grant access to an application</span></span>**

1.  <span data-ttu-id="a03d7-108">Pour une application existante, cliquez sur le nœud **applications** dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="a03d7-108">For an existing application, click the **Applications** node in the left pane.</span></span> <span data-ttu-id="a03d7-109">Cliquez avec le bouton droit sur une application dans le volet droit, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a03d7-109">Right-click an application in the right pane, and choose **Properties**.</span></span>

2.  <span data-ttu-id="a03d7-110">Sélectionnez l’onglet **autorisations d’accès** .</span><span class="sxs-lookup"><span data-stu-id="a03d7-110">Select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="a03d7-111">Pour ajouter des groupes d’utilisateurs, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a03d7-111">To add user groups, click **Add**.</span></span>

4.  <span data-ttu-id="a03d7-112">Dans la boîte de dialogue **Ajouter/modifier un groupe d’utilisateurs** , accédez au groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a03d7-112">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="a03d7-113">Vous pouvez également entrer le domaine et le groupe en entrant les informations dans les champs correspondants.</span><span class="sxs-lookup"><span data-stu-id="a03d7-113">You can also enter the domain and group by typing the information in the respective fields.</span></span>

5.  <span data-ttu-id="a03d7-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a03d7-114">Click **OK**.</span></span> <span data-ttu-id="a03d7-115">Vous pouvez ajouter d’autres groupes aux mêmes pages.</span><span class="sxs-lookup"><span data-stu-id="a03d7-115">You can add other groups with the same pages.</span></span>

6.  <span data-ttu-id="a03d7-116">Lorsque l’Assistant réapparaît, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a03d7-116">When the wizard reappears, click **OK**.</span></span>

    <span data-ttu-id="a03d7-117">**Remarques**  Pour pouvoir accorder l’accès aux applications, vous devez configurer vos groupes dans les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a03d7-117">**Note** You must set up your groups in Active Directory Domain Services before you attempt to grant access to applications.</span></span>

     

## <span data-ttu-id="a03d7-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a03d7-118">Related topics</span></span>


[<span data-ttu-id="a03d7-119">Procédure pour refuser l'accès à une application</span><span class="sxs-lookup"><span data-stu-id="a03d7-119">How to Deny Access to an Application</span></span>](how-to-deny-access-to-an-application.md)

[<span data-ttu-id="a03d7-120">Procédure pour gérer des groupes d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="a03d7-120">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="a03d7-121">Procédure pour gérer des licences d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="a03d7-121">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="a03d7-122">Procédure pour ajouter manuellement une application</span><span class="sxs-lookup"><span data-stu-id="a03d7-122">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 






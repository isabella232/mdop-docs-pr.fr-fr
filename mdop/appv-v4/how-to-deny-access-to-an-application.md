---
title: Procédure pour refuser l'accès à une application
description: Procédure pour refuser l'accès à une application
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807138"
---
# <span data-ttu-id="dd893-103">Procédure pour refuser l'accès à une application</span><span class="sxs-lookup"><span data-stu-id="dd893-103">How to Deny Access to an Application</span></span>


<span data-ttu-id="dd893-104">Les utilisateurs doivent figurer dans la liste des **autorisations d’accès** d’une application pour charger et utiliser l’application.</span><span class="sxs-lookup"><span data-stu-id="dd893-104">Users must be in an application's **Access Permissions** list to load and use the application.</span></span> <span data-ttu-id="dd893-105">Bien que la console de gestion du serveur d’applications ne prenne pas en charge explicitement le refus d’accès à une application par un groupe d’utilisateurs, vous pouvez supprimer les groupes d’utilisateurs des propriétés d’une application pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="dd893-105">Although the Application Virtualization Server Management Console does not support explicitly denying a user group access to an application, you can remove the user groups from an application’s properties to achieve this.</span></span>

**<span data-ttu-id="dd893-106">Pour refuser l’accès à une application</span><span class="sxs-lookup"><span data-stu-id="dd893-106">To deny access to an application</span></span>**

1.  <span data-ttu-id="dd893-107">Pour une application existante, cliquez sur le nœud **applications** dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="dd893-107">For an existing application, click the **Applications** node in the left pane.</span></span>

2.  <span data-ttu-id="dd893-108">Cliquez avec le bouton droit sur une application dans le volet droit, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="dd893-108">Right-click an application in the right pane, and choose **Properties**.</span></span> <span data-ttu-id="dd893-109">Puis sélectionnez l’onglet **autorisations d’accès** .</span><span class="sxs-lookup"><span data-stu-id="dd893-109">Then select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="dd893-110">Pour supprimer l’accès d’un groupe d’utilisateurs, sélectionnez le groupe d’utilisateurs et cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="dd893-110">To remove access for a user group, highlight the user group and click **Remove**.</span></span>

4.  <span data-ttu-id="dd893-111">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd893-111">Click **OK**.</span></span>

    <span data-ttu-id="dd893-112">**Remarques**  Pour contrôler l’accès aux applications, vous pouvez également limiter les licences d’application.</span><span class="sxs-lookup"><span data-stu-id="dd893-112">**Note** To control access to applications, you can also limit the application licenses.</span></span> <span data-ttu-id="dd893-113">La configuration des groupes d’utilisateurs appropriés dans les services de domaine Active Directory (AD FS) constitue le moyen le plus facile d’octroyer et de refuser l’accès à des groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="dd893-113">Setting up the proper user groups in Active Directory Domain Services provides the easiest way to grant and deny access to specific sets of users.</span></span>

     

## <span data-ttu-id="dd893-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd893-114">Related topics</span></span>


[<span data-ttu-id="dd893-115">Procédure pour accorder l'accès à une application</span><span class="sxs-lookup"><span data-stu-id="dd893-115">How to Grant Access to an Application</span></span>](how-to-grant-access-to-an-application.md)

[<span data-ttu-id="dd893-116">Procédure pour gérer des licences d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="dd893-116">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="dd893-117">Procédure pour gérer des applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="dd893-117">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 






---
title: Procédure pour gérer des licences d'applications dans Server Management Console
description: Procédure pour gérer des licences d'applications dans Server Management Console
author: dansimp
ms.assetid: 48503b04-0de7-48de-98ee-4623a712a341
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ca9ab54c8b4cee06e0b17d8b5dee3d3ca7ce69c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807021"
---
# <span data-ttu-id="dfbda-103">Procédure pour gérer des licences d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="dfbda-103">How to Manage Application Licenses in the Server Management Console</span></span>


<span data-ttu-id="dfbda-104">La console de gestion du serveur applicatif est l’interface utilisée pour gérer la plateforme de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="dfbda-104">The Application Virtualization Server Management Console is the interface you use to manage the Application Virtualization platform.</span></span> <span data-ttu-id="dfbda-105">À partir de là, vous pouvez ajouter, supprimer, configurer et contrôler des groupes de licences d’application.</span><span class="sxs-lookup"><span data-stu-id="dfbda-105">From it, you can add, remove, configure, and control application license groups.</span></span>

<span data-ttu-id="dfbda-106">**Important**  Si le paramètre de source d’application cliente (ASR) App-V est configuré de manière à utiliser n’importe quel type de source de flux continu autre que le serveur de gestion, par exemple un serveur en flux continu, un serveur IIS ou un serveur de fichiers, le serveur de gestion ne peut pas appliquer sa stratégie de licence.</span><span class="sxs-lookup"><span data-stu-id="dfbda-106">**Important** If the App-V client Application Source Root (ASR) setting is configured to use any type of streaming source other than the Management Server, for example a Streaming Server, an IIS server, or a File server, then the Management Server is unable to enforce its licensing policy.</span></span>

 

## <span data-ttu-id="dfbda-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="dfbda-107">In This Section</span></span>


<a href="" id="how-to-create-an-application-license-group"></a>[<span data-ttu-id="dfbda-108">Procédure pour créer un groupe de licences d'applications</span><span class="sxs-lookup"><span data-stu-id="dfbda-108">How to Create an Application License Group</span></span>](how-to-create-an-application-license-group.md)  
<span data-ttu-id="dfbda-109">Fournit une procédure de création d’une nouvelle application dans un groupe de licences.</span><span class="sxs-lookup"><span data-stu-id="dfbda-109">Provides a procedure for creating a new application in a license group.</span></span>

<a href="" id="how-to-associate-an-application-with-a-license-group"></a>[<span data-ttu-id="dfbda-110">Procédure pour associer une application avec un groupe de licences</span><span class="sxs-lookup"><span data-stu-id="dfbda-110">How to Associate an Application with a License Group</span></span>](how-to-associate-an-application-with-a-license-group.md)  
<span data-ttu-id="dfbda-111">Fournit une procédure permettant d’ajouter une application à un groupe de licences.</span><span class="sxs-lookup"><span data-stu-id="dfbda-111">Provides a procedure for adding an application to a license group.</span></span>

<a href="" id="how-to-remove-an-application-from-a-license-group"></a>[<span data-ttu-id="dfbda-112">Procédure pour supprimer une application d'un groupe de licences</span><span class="sxs-lookup"><span data-stu-id="dfbda-112">How to Remove an Application from a License Group</span></span>](how-to-remove-an-application-from-a-license-group.md)  
<span data-ttu-id="dfbda-113">Fournit une procédure pour supprimer une application d’un groupe de licences.</span><span class="sxs-lookup"><span data-stu-id="dfbda-113">Provides a procedure for removing an application from a license group.</span></span>

<a href="" id="how-to-remove-an-application-license-group"></a>[<span data-ttu-id="dfbda-114">Procédure pour supprimer un groupe de licences d'applications</span><span class="sxs-lookup"><span data-stu-id="dfbda-114">How to Remove an Application License Group</span></span>](how-to-remove-an-application-license-group.md)  
<span data-ttu-id="dfbda-115">Cette section présente les étapes nécessaires à la suppression d’un groupe de licences d’application.</span><span class="sxs-lookup"><span data-stu-id="dfbda-115">This section includes the steps necessary to delete an application license group.</span></span>

<a href="" id="how-to-set-up-an-unlimited-license-group"></a>[<span data-ttu-id="dfbda-116">Procédure pour configurer un groupe de licences illimitées</span><span class="sxs-lookup"><span data-stu-id="dfbda-116">How to Set Up an Unlimited License Group</span></span>](how-to-set-up-an-unlimited-license-group.md)  
<span data-ttu-id="dfbda-117">Fournit une procédure de création d’un nouveau groupe de licences illimité permettant à un nombre illimité d’utilisateurs d’accéder aux applications du groupe.</span><span class="sxs-lookup"><span data-stu-id="dfbda-117">Provides a procedure for creating a new unlimited license group, allowing an unlimited number of users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-concurrent-license-group"></a>[<span data-ttu-id="dfbda-118">Procédure pour configurer un groupe de licences simultanées</span><span class="sxs-lookup"><span data-stu-id="dfbda-118">How to Set Up a Concurrent License Group</span></span>](how-to-set-up-a-concurrent-license-group.md)  
<span data-ttu-id="dfbda-119">Fournit une procédure de création d’un nouveau groupe de licences simultanées permettant à un nombre spécifique d’utilisateurs simultanés d’accéder aux applications du groupe.</span><span class="sxs-lookup"><span data-stu-id="dfbda-119">Provides a procedure for creating a new concurrent license group, allowing a specific number of concurrent users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-named-license-group"></a>[<span data-ttu-id="dfbda-120">Procédure pour configurer un groupe de licences nommées</span><span class="sxs-lookup"><span data-stu-id="dfbda-120">How to Set Up a Named License Group</span></span>](how-to-set-up-a-named-license-group.md)  
<span data-ttu-id="dfbda-121">Fournit une procédure de création d’un nouveau groupe de licences illimité, permettant aux utilisateurs spécifiques d’accéder aux applications du groupe.</span><span class="sxs-lookup"><span data-stu-id="dfbda-121">Provides a procedure for creating a new unlimited license group, allowing specific users to access the applications in the group.</span></span>

## <span data-ttu-id="dfbda-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfbda-122">Related topics</span></span>


[<span data-ttu-id="dfbda-123">Procédure pour effectuer des tâches d'administration dans Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="dfbda-123">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 






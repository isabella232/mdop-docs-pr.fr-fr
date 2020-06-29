---
title: Procédure pour charger des applications virtuelles depuis la zone de notification du Bureau
description: Procédure pour charger des applications virtuelles depuis la zone de notification du Bureau
author: dansimp
ms.assetid: f52758eb-8b81-4b3c-9bc3-adcf7c00c238
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7004f9e0031dfeeedc8b6a916e2f3488f1d31e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807018"
---
# <span data-ttu-id="41fb6-103">Procédure pour charger des applications virtuelles depuis la zone de notification du Bureau</span><span class="sxs-lookup"><span data-stu-id="41fb6-103">How to Load Virtual Applications from the Desktop Notification Area</span></span>


<span data-ttu-id="41fb6-104">Si vous êtes un utilisateur mobile, vous souhaiterez peut-être charger entièrement vos applications dans le cache pour les utiliser en mode hors connexion ou en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="41fb6-104">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="41fb6-105">Pour diffuser des applications à partir du serveur de virtualisation des applications (App-V) Server ou du serveur de diffusion en continu application (App-V), vous devez être connecté à un serveur pour charger des applications.</span><span class="sxs-lookup"><span data-stu-id="41fb6-105">To stream applications from the Application Virtualization (App-V) Server or the Application Virtualization (App-V) Streaming Server, you must be connected to a server to load applications.</span></span> <span data-ttu-id="41fb6-106">Si vous n’êtes pas connecté au serveur lorsque vous tentez de télécharger des applications, votre système génère alors un message d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="41fb6-106">If you are not connected to the server when you attempt to load applications, your system will generate an appropriate error message.</span></span> <span data-ttu-id="41fb6-107">Vous pouvez également diffuser des applications sur le client à partir d’un fichier ou d’un disque.</span><span class="sxs-lookup"><span data-stu-id="41fb6-107">You can also stream applications to the client from a file or disk.</span></span>

<span data-ttu-id="41fb6-108">Les applications sont chargées une application à la fois.</span><span class="sxs-lookup"><span data-stu-id="41fb6-108">The applications are loaded one application at a time.</span></span> <span data-ttu-id="41fb6-109">La barre de progression indique le nom de l’application, le pourcentage d’application chargé et le nombre d’applications déjà traitées par rapport au nombre total d’applications mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="41fb6-109">The progress bar shows you the application name, the percentage of application loaded, and the number of applications already processed compared to the total number of the applications queued.</span></span> <span data-ttu-id="41fb6-110">Vous pouvez ignorer l’application en cours avant qu’elle ne soit 100% chargée.</span><span class="sxs-lookup"><span data-stu-id="41fb6-110">You can skip any application in progress before it is 100% loaded.</span></span> <span data-ttu-id="41fb6-111">Vous pouvez également ignorer le chargement de toutes les applications restantes.</span><span class="sxs-lookup"><span data-stu-id="41fb6-111">You can skip the loading of all remaining applications as well.</span></span>

<span data-ttu-id="41fb6-112">**Remarques**  Si votre système rencontre une erreur lors du chargement d’une application, il vous signale l’erreur.</span><span class="sxs-lookup"><span data-stu-id="41fb6-112">**Note** If your system encounters an error while loading an application, it reports the error to you.</span></span> <span data-ttu-id="41fb6-113">Vous devez ignorer la boîte de dialogue d’erreur avant de charger l’application suivante.</span><span class="sxs-lookup"><span data-stu-id="41fb6-113">You must dismiss the error dialog before it will load the next application.</span></span>

 

**<span data-ttu-id="41fb6-114">Pour charger toutes les applications</span><span class="sxs-lookup"><span data-stu-id="41fb6-114">To load all applications</span></span>**

1.  <span data-ttu-id="41fb6-115">Cliquez avec le bouton droit sur l’icône système de virtualisation des applications dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="41fb6-115">Right-click the Application Virtualization System icon in the notification area.</span></span>

2.  <span data-ttu-id="41fb6-116">Dans le menu contextuel, sélectionnez **charger des applications** .</span><span class="sxs-lookup"><span data-stu-id="41fb6-116">Select **Load Applications** from the pop-up menu.</span></span>

**<span data-ttu-id="41fb6-117">Pour ignorer des applications</span><span class="sxs-lookup"><span data-stu-id="41fb6-117">To skip applications</span></span>**

1.  <span data-ttu-id="41fb6-118">Cliquez sur la barre de progression pour afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="41fb6-118">Click the progress bar to display the dialog box.</span></span>

2.  <span data-ttu-id="41fb6-119">Pour obtenir les résultats souhaités, sélectionnez l’un des boutons suivants:</span><span class="sxs-lookup"><span data-stu-id="41fb6-119">Select one of the following buttons to achieve the desired results:</span></span>

    1.  <span data-ttu-id="41fb6-120">**Ignorer**: pour ignorer l’application actuellement en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="41fb6-120">**Skip**—To skip the currently loading application.</span></span>

    2.  <span data-ttu-id="41fb6-121">**Ignorer tout**: pour ignorer toutes les applications restantes.</span><span class="sxs-lookup"><span data-stu-id="41fb6-121">**Skip All**—To skip all remaining applications.</span></span>

    3.  <span data-ttu-id="41fb6-122">**Continuer**: pour annuler la boîte de dialogue et poursuivre le chargement des applications.</span><span class="sxs-lookup"><span data-stu-id="41fb6-122">**Continue**—To cancel the dialog box and continue loading applications.</span></span>

## <span data-ttu-id="41fb6-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41fb6-123">Related topics</span></span>


[<span data-ttu-id="41fb6-124">Procédure d'utilisation de la zone de notification du Bureau pour Application Virtualization Client Management</span><span class="sxs-lookup"><span data-stu-id="41fb6-124">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 






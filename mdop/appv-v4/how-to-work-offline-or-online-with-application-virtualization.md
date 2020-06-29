---
title: Procédure pour travailler hors connexion ou en ligne avec Application Virtualization
description: Procédure pour travailler hors connexion ou en ligne avec Application Virtualization
author: dansimp
ms.assetid: aa532b37-8a00-4db4-9b51-e1e8354b2495
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0dfdd315fe607156135247c4a34d0248ef8fbdd9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806682"
---
# <span data-ttu-id="0ef3a-103">Procédure pour travailler hors connexion ou en ligne avec Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0ef3a-103">How to Work Offline or Online with Application Virtualization</span></span>


<span data-ttu-id="0ef3a-104">Si vous envisagez de vous déconnecter du réseau pour une période prolongée, vous pouvez travailler en mode hors connexion pour éliminer les retards possibles lorsque le client de virtualisation d’application tente de communiquer avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-104">If you plan to be disconnected from the network for an extended period of time, you can work in offline mode to eliminate possible delays when the Application Virtualization client attempts to communicate with the server.</span></span> <span data-ttu-id="0ef3a-105">En mode hors connexion, le client de virtualisation des applications ne tente pas de communiquer avec le serveur de publication; les applications doivent donc être entièrement mises en cache avant d’activer le mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-105">In offline mode, the Application Virtualization client will not attempt to communicate with the publishing server, so applications must be fully cached before enabling offline mode.</span></span> <span data-ttu-id="0ef3a-106">Les applications ne seront pas récupérées à partir du partage de contenu, même si elles se trouvent sur le disque local de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-106">Applications will not be retrieved from the content share even if they are on the local disk on the computer.</span></span> <span data-ttu-id="0ef3a-107">Pour basculer entre le travail en mode hors connexion et en ligne, vous pouvez utiliser la procédure suivante du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-107">You can use the following Application Virtualization Client procedure to toggle between working offline and online.</span></span>

<span data-ttu-id="0ef3a-108">**Remarques**  Par défaut, l’option **travailler en mode hors connexion** est désactivée pour le client pour les services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-108">**Note** By default, **Work Offline** is disabled for the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="0ef3a-109">Votre administrateur système doit modifier vos autorisations d’utilisateur pour vous permettre d’utiliser ce paramètre sur un client pour les services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-109">Your system administrator must change your user permissions to allow you to use this setting on a Client for Remote Desktop Services.</span></span>

 

**<span data-ttu-id="0ef3a-110">Pour travailler en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="0ef3a-110">To work offline</span></span>**

-   <span data-ttu-id="0ef3a-111">Cliquez avec le bouton droit dans la zone de notification, puis sélectionnez **travailler hors connexion** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-111">Right-click the Application Virtualization System icon in the notification area, and select **Work Offline** from the pop-up menu.</span></span>

**<span data-ttu-id="0ef3a-112">Pour travailler en ligne</span><span class="sxs-lookup"><span data-stu-id="0ef3a-112">To work online</span></span>**

-   <span data-ttu-id="0ef3a-113">Cliquez avec le bouton droit sur l’icône système de virtualisation des applications dans la zone de notification, puis sélectionnez **travailler en ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-113">Right-click the Application Virtualization System icon in the notification area, and select **Work Online** from the pop-up menu.</span></span>

## <span data-ttu-id="0ef3a-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ef3a-114">Related topics</span></span>


[<span data-ttu-id="0ef3a-115">Procédure d'utilisation de la zone de notification du Bureau pour Application Virtualization Client Management</span><span class="sxs-lookup"><span data-stu-id="0ef3a-115">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 






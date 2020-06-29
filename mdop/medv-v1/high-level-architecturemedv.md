---
title: Architecture de haut niveau
description: Architecture de haut niveau
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811615"
---
# <span data-ttu-id="32c63-103">Architecture de haut niveau</span><span class="sxs-lookup"><span data-stu-id="32c63-103">High-Level Architecture</span></span>


<span data-ttu-id="32c63-104">La solution MED-V comprend les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="32c63-104">The MED-V solution comprises the following elements:</span></span>

-   <span data-ttu-id="32c63-105">**Machine virtuelle définie par l’administrateur**, qui encapsule un environnement de bureau complet, y compris un système d’exploitation, des applications, ainsi que des outils de gestion et de sécurité facultatifs.</span><span class="sxs-lookup"><span data-stu-id="32c63-105">**Administrator-defined virtual machine**—Encapsulates a full desktop environment, including an operating system, applications, and optional management and security tools.</span></span>

-   <span data-ttu-id="32c63-106">**Référentiel d’images**: stocke toutes les images virtuelles sur un serveur IIS standard et permet la gestion des versions d’images virtuelles, la récupération d’image authentifiée par le client et le téléchargement efficace (d’une nouvelle image ou mise à jour) via la technologie de transfert de découpage.</span><span class="sxs-lookup"><span data-stu-id="32c63-106">**Image repository**—Stores all virtual images on a standard IIS server and enables virtual images version management, client-authenticated image retrieval, and efficient download (of a new image or updates) via Trim Transfer technology.</span></span>

-   <span data-ttu-id="32c63-107">**Serveur de gestion**: associe les images virtuelles du référentiel d’images et les stratégies d’utilisation de l’administrateur à Active Directory® utilisateurs ou groupes.</span><span class="sxs-lookup"><span data-stu-id="32c63-107">**Management server**—Associates virtual images from the image repository along with administrator usage policies to Active Directory® users or groups.</span></span> <span data-ttu-id="32c63-108">Le serveur de gestion agrège également les événements des clients et les stocke dans une base de données externe (Microsoft SQL Server®) à des fins de surveillance et de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="32c63-108">The management server also aggregates clients' events and stores them in an external database (Microsoft SQL Server®) for monitoring and reporting purposes.</span></span>

-   <span data-ttu-id="32c63-109">**Console de gestion**: permet aux administrateurs de contrôler le serveur de gestion et le référentiel d’images.</span><span class="sxs-lookup"><span data-stu-id="32c63-109">**Management console**—Enables administrators to control the management server and the image repository.</span></span>

-   **<span data-ttu-id="32c63-110">Client de l’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="32c63-110">End-user client</span></span>**

    1.  <span data-ttu-id="32c63-111">Cycle de vie d’image virtuelle: authentification, récupération d’image, application de stratégies d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="32c63-111">Virtual image life-cycle—Authentication, image retrieval, enforcement of usage policies.</span></span>

    2.  <span data-ttu-id="32c63-112">Gestion de session de machine virtuelle: démarrez, arrêtez et verrouillez l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="32c63-112">Virtual machine session management—Start, stop, lock the virtual machine.</span></span>

    3.  <span data-ttu-id="32c63-113">Expérience de bureau unique: les applications installées sur l’ordinateur virtuel sont accessibles en toute transparence par le biais du menu de démarrage standard du bureau et intégrées à d’autres applications sur le Bureau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32c63-113">Single desktop experience—Applications installed in the virtual machine seamlessly available through the standard desktop Start menu and integrated with other applications on the user desktop.</span></span>

<span data-ttu-id="32c63-114">Toutes les communications entre le client et les serveurs (serveur de gestion et référentiel d’images) sont effectuées en haut d’un canal HTTP ou HTTPs standard.</span><span class="sxs-lookup"><span data-stu-id="32c63-114">All communication between the client and the servers (management server and image repository) is carried on top of a standard HTTP or HTTPS channel.</span></span>

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 






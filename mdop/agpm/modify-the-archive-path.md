---
title: Modifier le chemin d'accès de l'archive
description: Modifier le chemin d'accès de l'archive
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808329"
---
# <span data-ttu-id="ab265-103">Modifier le chemin d'accès de l'archive</span><span class="sxs-lookup"><span data-stu-id="ab265-103">Modify the Archive Path</span></span>


<span data-ttu-id="ab265-104">Le chemin d’accès d’archive est l’emplacement de l’archivage relatif au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab265-104">The archive path is the location of the archive relative to the AGPM Server.</span></span> <span data-ttu-id="ab265-105">Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou sur un autre serveur dans la même forêt.</span><span class="sxs-lookup"><span data-stu-id="ab265-105">The archive path can point to a folder on the AGPM Server or on another server in the same forest.</span></span>

<span data-ttu-id="ab265-106">Le chemin d’accès d’archive et le compte de service AGPM sont configurés lors de l’installation d’AGPM Server et peuvent être modifiés par la suite via **Ajouter ou supprimer des programmes** sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab265-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="ab265-107">Un compte d’utilisateur membre du groupe administrateurs de domaine et ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le serveur de gestion de la stratégie de groupe Microsoft Advanced) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="ab265-107">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="ab265-108">Pour modifier le chemin d’accès de l’archive</span><span class="sxs-lookup"><span data-stu-id="ab265-108">To modify the archive path</span></span>**

1.  <span data-ttu-id="ab265-109">Sur l’ordinateur sur lequel est installé Microsoft Advanced Group Policy Management-serveur, cliquez sur **Démarrer**, puis sur **panneau de configuration**, cliquez sur **Ajouter ou supprimer des programmes**.</span><span class="sxs-lookup"><span data-stu-id="ab265-109">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="ab265-110">Cliquez sur **gestion de la stratégie de groupe Microsoft avancée-serveur**, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="ab265-110">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="ab265-111">Cliquez sur **suivant**, puis sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="ab265-111">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="ab265-112">Suivez les instructions à l’écran pour configurer les paramètres du service AGPM:</span><span class="sxs-lookup"><span data-stu-id="ab265-112">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="ab265-113">Pour le chemin d’accès de l’archive, entrez le nouvel emplacement de l’archivage relatif au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab265-113">For the archive path, enter a new location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="ab265-114">Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou un autre emplacement, mais l’espace disponible doit être suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab265-114">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="ab265-115">Entrez les informations d’identification du compte de service AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab265-115">Enter credentials for the AGPM Service Account.</span></span>

        <span data-ttu-id="ab265-116">**Important**  La modification de l’installation efface les informations d’identification du compte de service AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab265-116">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="ab265-117">Vous devez entrer de nouveau les informations d’identification, mais elles ne sont pas obligées de correspondre aux informations d’identification utilisées lors de l’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="ab265-117">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="ab265-118">Le compte de service AGPM doit disposer d’un accès complet aux objets GPO qu’il doit gérer.</span><span class="sxs-lookup"><span data-stu-id="ab265-118">The AGPM Service Account must have full access to the GPOs that it will manage.</span></span> <span data-ttu-id="ab265-119">S’il s’agit de gérer les objets de stratégie de groupe sur un domaine unique, vous pouvez créer le compte système local pour le contrôleur de domaine principal du compte de service AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab265-119">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="ab265-120">S’il s’agit de gérer des objets de stratégie de groupe sur plusieurs domaines ou si un serveur membre sera le serveur AGPM, vous devez configurer un autre compte en tant que compte de service AGPM, car le compte système local d’un contrôleur de domaine ne peut pas accéder aux objets de stratégie de groupe sur d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="ab265-120">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="ab265-121">Pour le propriétaire de l’archive, entrez les informations d’identification d’un administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="ab265-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="ab265-122">Cliquez sur **modifier**, et une fois l’installation terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ab265-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="ab265-123">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ab265-123">Additional references</span></span>

-   [<span data-ttu-id="ab265-124">Gestion du service AGPM</span><span class="sxs-lookup"><span data-stu-id="ab265-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 






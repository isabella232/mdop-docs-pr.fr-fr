---
title: Modifier le compte du service AGPM
description: Modifier le compte du service AGPM
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808341"
---
# <span data-ttu-id="adcbd-103">Modifier le compte du service AGPM</span><span class="sxs-lookup"><span data-stu-id="adcbd-103">Modify the AGPM Service Account</span></span>


<span data-ttu-id="adcbd-104">Le service AGPM est un service Windows agissant en tant que proxy de sécurité, gérant l’accès client aux objets de stratégie de groupe (GPO) dans l’environnement d’archivage et de production.</span><span class="sxs-lookup"><span data-stu-id="adcbd-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="adcbd-105">Si ce service est arrêté ou désactivé, les clients AGPM ne peuvent pas effectuer d’opérations via le serveur.</span><span class="sxs-lookup"><span data-stu-id="adcbd-105">If this service is stopped or disabled, AGPM clients cannot perform operations through the server.</span></span>

<span data-ttu-id="adcbd-106">Le chemin d’accès d’archive et le compte de service AGPM sont configurés lors de l’installation d’AGPM Server et peuvent être modifiés par la suite via **Ajouter ou supprimer des programmes** sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="adcbd-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="adcbd-107">**Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="adcbd-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="adcbd-108">Cela peut empêcher le démarrage du service AGPM.</span><span class="sxs-lookup"><span data-stu-id="adcbd-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="adcbd-109">Un compte d’utilisateur membre du groupe administrateurs de domaine et ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le serveur de gestion de la stratégie de groupe Microsoft Advanced) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="adcbd-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

<span data-ttu-id="adcbd-110">**Important**  Le compte de service AGPM doit disposer d’un accès complet aux objets de stratégie de groupe qu’il doit gérer et bénéficier d’une autorisation **de connexion en tant que service** .</span><span class="sxs-lookup"><span data-stu-id="adcbd-110">**Important** The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="adcbd-111">S’il s’agit de gérer les objets de stratégie de groupe sur un domaine unique, vous pouvez créer le compte système local pour le contrôleur de domaine principal du compte de service AGPM.</span><span class="sxs-lookup"><span data-stu-id="adcbd-111">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

<span data-ttu-id="adcbd-112">S’il s’agit de gérer des objets de stratégie de groupe sur plusieurs domaines ou si un serveur membre sera le serveur AGPM, vous devez configurer un autre compte en tant que compte de service AGPM, car le compte système local d’un contrôleur de domaine ne peut pas accéder aux objets de stratégie de groupe sur d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="adcbd-112">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

 

**<span data-ttu-id="adcbd-113">Pour modifier le compte de service AGPM</span><span class="sxs-lookup"><span data-stu-id="adcbd-113">To modify the AGPM Service Account</span></span>**

1.  <span data-ttu-id="adcbd-114">Sur l’ordinateur sur lequel est installé Microsoft Advanced Group Policy Management-serveur, cliquez sur **Démarrer**, puis sur **panneau de configuration**, cliquez sur **Ajouter ou supprimer des programmes**.</span><span class="sxs-lookup"><span data-stu-id="adcbd-114">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="adcbd-115">Cliquez sur **gestion de la stratégie de groupe Microsoft avancée-serveur**, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="adcbd-115">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="adcbd-116">Cliquez sur **suivant**, puis sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="adcbd-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="adcbd-117">Suivez les instructions à l’écran pour configurer les paramètres du service AGPM:</span><span class="sxs-lookup"><span data-stu-id="adcbd-117">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="adcbd-118">Pour le chemin d’accès de l’archive, confirmez ou modifiez l’emplacement de l’archivage par rapport au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="adcbd-118">For the archive path, confirm or change the location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="adcbd-119">Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou un autre emplacement, mais l’espace disponible doit être suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="adcbd-119">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="adcbd-120">Entrez les nouvelles informations d’identification pour le compte de service AGPM.</span><span class="sxs-lookup"><span data-stu-id="adcbd-120">Enter new credentials for the AGPM Service Account.</span></span>

    3.  <span data-ttu-id="adcbd-121">Pour le propriétaire de l’archive, entrez les informations d’identification d’un administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="adcbd-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="adcbd-122">Cliquez sur **modifier**, et une fois l’installation terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="adcbd-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="adcbd-123">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="adcbd-123">Additional references</span></span>

-   [<span data-ttu-id="adcbd-124">Gestion du service AGPM</span><span class="sxs-lookup"><span data-stu-id="adcbd-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 






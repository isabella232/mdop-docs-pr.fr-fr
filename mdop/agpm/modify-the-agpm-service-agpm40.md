---
title: Modifier le service AGPM
description: Modifier le service AGPM
author: dansimp
ms.assetid: 3239d088-bb86-4ec4-bc56-dbe8f1c710f5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: be39b170ef4cdc14c0f447bb6bd09a4ea92c82fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808330"
---
# <span data-ttu-id="ddd9c-103">Modifier le service AGPM</span><span class="sxs-lookup"><span data-stu-id="ddd9c-103">Modify the AGPM Service</span></span>


<span data-ttu-id="ddd9c-104">Le service AGPM est un service Windows agissant en tant que proxy de sécurité, gérant l’accès client aux objets de stratégie de groupe (GPO) dans l’environnement d’archivage et de production du domaine.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment of the domain.</span></span> <span data-ttu-id="ddd9c-105">Si ce service est arrêté ou désactivé, les clients AGPM ne peuvent pas effectuer d’opérations via le serveur.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-105">If this service is stopped or disabled, AGPM Clients cannot perform operations through the server.</span></span> <span data-ttu-id="ddd9c-106">Vous pouvez modifier le chemin d’archive, le compte de service AGPM et le port sur lequel le service AGPM écoute.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-106">You can modify the archive path, the AGPM Service Account, and the port on which the AGPM Service listens.</span></span>

<span data-ttu-id="ddd9c-107">**Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="ddd9c-108">Cela peut empêcher le démarrage du service AGPM.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="ddd9c-109">Un compte d’utilisateur membre du groupe administrateurs de domaine et ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le serveur de gestion de la stratégie de groupe Microsoft Advanced) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span> <span data-ttu-id="ddd9c-110">Par ailleurs, vous devez fournir les informations d’identification du compte de service AGPM pour pouvoir exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-110">Additionally, you must provide credentials for the AGPM Service Account to complete this procedure.</span></span>

**<span data-ttu-id="ddd9c-111">Pour modifier le service AGPM</span><span class="sxs-lookup"><span data-stu-id="ddd9c-111">To modify the AGPM Service</span></span>**

1.  <span data-ttu-id="ddd9c-112">Sur l’ordinateur sur lequel est installé Microsoft Advanced Group Policy Management-Server, cliquez sur **Démarrer**, **panneau de configuration**, **programmes**et **programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-112">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, **Control Panel**, **Programs**, and **Programs and Features**.</span></span>

2.  <span data-ttu-id="ddd9c-113">Cliquez avec le bouton droit sur **gestion de stratégie de groupe avancée Microsoft-serveur**, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-113">Right-click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="ddd9c-114">Cliquez sur **suivant**, puis sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-114">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="ddd9c-115">Suivez les instructions pour configurer le service AGPM:</span><span class="sxs-lookup"><span data-stu-id="ddd9c-115">Follow the instructions to configure the AGPM Service:</span></span>

    1.  <span data-ttu-id="ddd9c-116">Dans la boîte de dialogue **path Archive** , entrez le nouvel emplacement de l’archivage relatif au serveur AGPM ou confirmez le chemin d’accès actuel de l’archivage, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-116">In the **Archive Path** dialog box, enter a new location for the archive relative to the AGPM Server, or confirm the current archive path, and then click **Next**.</span></span>

        <span data-ttu-id="ddd9c-117">**Important**  Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou un autre emplacement, mais l’espace disponible doit être suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-117">**Important** The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

         

    2.  <span data-ttu-id="ddd9c-118">Dans la boîte de dialogue **compte de service AGPM** , entrez les informations d’identification d’un compte de service sous lequel le service AGPM sera exécuté, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-118">In the **AGPM Service Account** dialog box, enter credentials for a service account under which the AGPM Service will run, and click **Next**.</span></span>

        <span data-ttu-id="ddd9c-119">**Important**  La modification de l’installation efface les informations d’identification du compte de service AGPM.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-119">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="ddd9c-120">Vous devez entrer de nouveau les informations d’identification, mais elles ne sont pas obligées de correspondre aux informations d’identification utilisées lors de l’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-120">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="ddd9c-121">Le compte de service AGPM doit disposer d’un accès complet aux objets de stratégie de groupe qu’il doit gérer et bénéficier d’une autorisation **de connexion en tant que service** .</span><span class="sxs-lookup"><span data-stu-id="ddd9c-121">The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="ddd9c-122">S’il s’agit de gérer les objets de stratégie de groupe sur un domaine unique, vous pouvez créer le compte système local pour le contrôleur de domaine principal du compte de service AGPM.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-122">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="ddd9c-123">S’il s’agit de gérer des objets de stratégie de groupe sur plusieurs domaines ou si un serveur membre sera le serveur AGPM, vous devez configurer un autre compte en tant que compte de service AGPM, car le compte système local d’un contrôleur de domaine ne peut pas accéder aux objets de stratégie de groupe sur d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-123">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="ddd9c-124">Dans la boîte de dialogue **Archiver le propriétaire** , entrez le nom d’utilisateur d’un administrateur AGPM (contrôle total) ou d’un groupe d’administrateurs AGPM, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-124">In the **Archive Owner** dialog box, enter the user name of an AGPM Administrator (Full Control) or group of AGPM Administrators, and click **Next**.</span></span>

        <span data-ttu-id="ddd9c-125">**Remarques**  La modification de l’installation efface les informations d’identification pour le propriétaire de l’archivage.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-125">**Note** Modifying the installation clears the credentials for the Archive Owner.</span></span> <span data-ttu-id="ddd9c-126">Vous devez entrer de nouveau les informations d’identification, mais elles ne sont pas obligées de correspondre aux informations d’identification utilisées lors de l’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-126">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

         

    4.  <span data-ttu-id="ddd9c-127">Dans la boîte de dialogue **configuration du port** , tapez un nouveau port sur lequel le service AGPM écoute ou confirme le port actuellement sélectionné, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-127">In the **Port Configuration** dialog box, type a new port on which the AGPM Service should listen or confirm the port currently selected, and click **Next**.</span></span>

        <span data-ttu-id="ddd9c-128">**Remarques**  Par défaut, le service AGPM écoute sur le port 4600.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-128">**Note** By default, the AGPM Service listens on port 4600.</span></span>

        <span data-ttu-id="ddd9c-129">Si vous configurez manuellement les exceptions de port ou que les règles configurent les exceptions de port, vous pouvez désactiver la case à cocher **Ajouter une exception de Port au pare-feu** .</span><span class="sxs-lookup"><span data-stu-id="ddd9c-129">If you manually configure port exceptions or have rules configuring port exceptions, you can clear the **Add port exception to firewall** check box.</span></span>

         

5.  <span data-ttu-id="ddd9c-130">Cliquez sur **modifier**, et une fois l’installation terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-130">Click **Change**, and when the installation is complete click **Finish**.</span></span>

6.  <span data-ttu-id="ddd9c-131">Si vous avez modifié le port sur lequel écoute le service AGPM, modifiez le port dans la connexion de serveur AGPM pour chaque administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-131">If you have changed the port on which the AGPM Service listens, modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="ddd9c-132">(Pour plus d’informations, voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="ddd9c-132">(For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).)</span></span>

7.  <span data-ttu-id="ddd9c-133">Répétez cette opération pour chaque serveur AGPM sur lequel les modifications de configuration doivent être appliquées.</span><span class="sxs-lookup"><span data-stu-id="ddd9c-133">Repeat for each AGPM Server to which the configuration changes should be applied.</span></span>

### <span data-ttu-id="ddd9c-134">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ddd9c-134">Additional references</span></span>

-   [<span data-ttu-id="ddd9c-135">Gestion du service AGPM</span><span class="sxs-lookup"><span data-stu-id="ddd9c-135">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm40.md)

 

 






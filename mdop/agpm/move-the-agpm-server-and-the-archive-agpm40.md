---
title: Déplacer le serveur AGPM et l'archive
description: Déplacer le serveur AGPM et l'archive
author: dansimp
ms.assetid: 9ec48d3a-c293-45f0-8939-32ccdc062303
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 61ad2eb6e0ea46eef89379894a99469254e0fd5e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809413"
---
# <span data-ttu-id="a5460-103">Déplacer le serveur AGPM et l'archive</span><span class="sxs-lookup"><span data-stu-id="a5460-103">Move the AGPM Server and the Archive</span></span>


<span data-ttu-id="a5460-104">Si vous remplacez le serveur AGPM et le serveur sur lequel l’archive est hébergée, vous devez déplacer le service AGPM et l’archive.</span><span class="sxs-lookup"><span data-stu-id="a5460-104">If you are replacing the AGPM Server and the server on which the archive is hosted, you must move the AGPM Service and the archive.</span></span> <span data-ttu-id="a5460-105">Si vous le souhaitez, vous pouvez déplacer le service AGPM et l’archive séparément.</span><span class="sxs-lookup"><span data-stu-id="a5460-105">If you prefer, you can move the AGPM Service and the archive separately.</span></span>

**<span data-ttu-id="a5460-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="a5460-106">Note</span></span>**  
-   <span data-ttu-id="a5460-107">Le serveur AGPM est l’ordinateur qui héberge le service AGPM et l’ordinateur sur lequel est installée la gestion de stratégie de groupe avancée Microsoft – serveur.</span><span class="sxs-lookup"><span data-stu-id="a5460-107">The AGPM Server is the computer that hosts the AGPM Service and the computer on which Microsoft Advanced Group Policy Management – Server is installed.</span></span>

-   <span data-ttu-id="a5460-108">Par défaut, l’archive est hébergée sur le serveur AGPM, mais vous pouvez spécifier un chemin d’accès d’archive pour l’héberger sur un autre serveur à la place.</span><span class="sxs-lookup"><span data-stu-id="a5460-108">By default, the archive is hosted on the AGPM Server, but you can specify an archive path to host it on another server instead.</span></span>

 

<span data-ttu-id="a5460-109">Un compte d’utilisateur membre du groupe administrateurs de domaine et ayant accès à l’ancien et au nouveau serveur AGPM est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a5460-109">A user account that is a member of the Domain Admins group and has access to the previous and new AGPM Servers is required to complete this procedure.</span></span> <span data-ttu-id="a5460-110">Par ailleurs, vous devez fournir des informations d’identification pour le compte de service AGPM que le nouveau serveur AGPM doit utiliser pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a5460-110">Additionally, you must provide credentials for the AGPM Service Account to be used by the new AGPM Server to complete this procedure.</span></span>

**<span data-ttu-id="a5460-111">Pour déplacer le service AGPM et l’archivage vers un ou plusieurs serveurs</span><span class="sxs-lookup"><span data-stu-id="a5460-111">To move the AGPM Service and the archive to a different server or servers</span></span>**

1.  <span data-ttu-id="a5460-112">Sauvegardez l’archive.</span><span class="sxs-lookup"><span data-stu-id="a5460-112">Back up the archive.</span></span> <span data-ttu-id="a5460-113">Pour plus d’informations, voir [sauvegarder l’archive](back-up-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="a5460-113">For more information, see [Back Up the Archive](back-up-the-archive-agpm40.md).</span></span>

2.  <span data-ttu-id="a5460-114">Déplacer le service AGPM:</span><span class="sxs-lookup"><span data-stu-id="a5460-114">Move the AGPM Service:</span></span>

    1.  <span data-ttu-id="a5460-115">Arrêtez le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="a5460-115">Stop the AGPM Service.</span></span> <span data-ttu-id="a5460-116">Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="a5460-116">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="a5460-117">Installez la gestion de la stratégie de groupe avancée Microsoft-serveur sur le nouveau serveur qui héberge le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="a5460-117">Install Microsoft Advanced Group Policy Management - Server on the new server that will host the AGPM Service.</span></span> <span data-ttu-id="a5460-118">Au cours de ce processus, vous spécifiez le chemin d’accès à la nouvelle archive, l’emplacement de l’Archive par rapport au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="a5460-118">During this process, you specify the new archive path, the location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="a5460-119">Pour plus d’informations, reportez-vous au [Guide étape par étape de la gestion de la 4,0 stratégie de groupe Microsoft Advanced](https://go.microsoft.com/fwlink/?LinkId=153505) https://go.microsoft.com/fwlink/?LinkId=153505) [Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) https://go.microsoft.com/fwlink/?LinkId=156883)</span><span class="sxs-lookup"><span data-stu-id="a5460-119">For more information, see [Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505) and [Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883).</span></span>

    3.  <span data-ttu-id="a5460-120">Par le biais d’un administrateur d’AGPM (contrôle total), vous devez configurer la connexion à un serveur AGPM pour tous les administrateurs de stratégie de groupe qui utiliseront le nouveau serveur AGPM et supprimer la connexion de l’ancien serveur AGPM, ou tous les administrateurs de stratégie de groupe doivent configurer manuellement la nouvelle connexion AGPM Server et supprimer l’ancienne connexion à un serveur AGPM pour le composant logiciel AGPM.</span><span class="sxs-lookup"><span data-stu-id="a5460-120">Either an AGPM Administrator (Full Control) must configure the AGPM Server connection for all Group Policy administrators who will use the new AGPM Server and remove the connection for the old AGPM Server, or else each Group Policy administrator must manually configure the new AGPM Server connection and remove the old AGPM Server connection for the AGPM snap-in on their computer.</span></span> <span data-ttu-id="a5460-121">Pour plus d’informations, voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="a5460-121">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

        <span data-ttu-id="a5460-122">**Remarques**  Il est recommandé de désinstaller l’application gestion de la stratégie de groupe avancée Microsoft – serveur du serveur AGPM précédent.</span><span class="sxs-lookup"><span data-stu-id="a5460-122">**Note** As a best practice, you should uninstall Microsoft Advanced Group Policy Management – Server from the previous AGPM Server.</span></span> <span data-ttu-id="a5460-123">Cela permet de garantir que le service AGPM ne peut pas être redémarré involontairement sur ce serveur et risque de provoquer une confusion en cas de connexion à un serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="a5460-123">This will ensure that the AGPM Service cannot be unintentionally restarted on that server and potentially cause confusion if any AGPM Server connections to it remain.</span></span>

         

3.  <span data-ttu-id="a5460-124">Copiez l’archive de la sauvegarde sur le nouveau serveur qui héberge l’archive.</span><span class="sxs-lookup"><span data-stu-id="a5460-124">Copy the archive from the backup to the new server that will host the archive.</span></span> <span data-ttu-id="a5460-125">Pour plus d’informations, voir [restaurer l’archive à partir d’une sauvegarde](restore-the-archive-from-a-backup-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="a5460-125">For more information, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

    <span data-ttu-id="a5460-126">**Important**  Si vous avez déplacé l’archive sans déplacer le service AGPM en même temps:</span><span class="sxs-lookup"><span data-stu-id="a5460-126">**Important** If you moved the archive without moving the AGPM Service at the same time:</span></span>

    1.  <span data-ttu-id="a5460-127">Vous devez modifier la trajectoire d’archive de sorte qu’elle pointe vers le nouvel emplacement de l’Archive par rapport au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="a5460-127">You must change the archive path to point to the new location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="a5460-128">Pour plus d’informations, voir [modifier le service AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="a5460-128">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="a5460-129">Vous devez entrer à nouveau le mot de passe et le confirmer sous l’onglet **délégation de domaine** . Pour plus d’informations, voir [configurer une notification par courrier électronique](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="a5460-129">You must re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

     

### <span data-ttu-id="a5460-130">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="a5460-130">Additional references</span></span>

-   [<span data-ttu-id="a5460-131">Sauvegarder l'archive</span><span class="sxs-lookup"><span data-stu-id="a5460-131">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="a5460-132">Restaurer l'archive à partir d'une sauvegarde</span><span class="sxs-lookup"><span data-stu-id="a5460-132">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="a5460-133">Configurer les connexions du serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="a5460-133">Configure AGPM Server Connections</span></span>](configure-agpm-server-connections-agpm40.md)

-   [<span data-ttu-id="a5460-134">Modifier le service AGPM</span><span class="sxs-lookup"><span data-stu-id="a5460-134">Modify the AGPM Service</span></span>](modify-the-agpm-service-agpm40.md)

-   <span data-ttu-id="a5460-135">[Guide pas à pas pour la gestion avancée de la stratégie de groupe Microsoft 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span><span class="sxs-lookup"><span data-stu-id="a5460-135">[Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span></span>

-   <span data-ttu-id="a5460-136">[Guide de planification de Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span><span class="sxs-lookup"><span data-stu-id="a5460-136">[Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span></span>

-   [<span data-ttu-id="a5460-137">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="a5460-137">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 






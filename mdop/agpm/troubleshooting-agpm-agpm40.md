---
title: Résolution des problèmes d'AGPM
description: Résolution des problèmes d'AGPM
author: dansimp
ms.assetid: bedcd817-beb2-47bf-aebd-e3923c4fd06f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b44612cb9e3737a8d8f3109f76b0c9325d183383
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808193"
---
# <span data-ttu-id="80645-103">Résolution des problèmes d'AGPM</span><span class="sxs-lookup"><span data-stu-id="80645-103">Troubleshooting AGPM</span></span>


<span data-ttu-id="80645-104">Cette section répertorie les problèmes courants que vous pouvez rencontrer lors de l’utilisation de la gestion de la stratégie de groupe avancée (AGPM) pour gérer les objets de stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="80645-104">This section lists common issues that you may encounter when you use Advanced Group Policy Management (AGPM) to manage Group Policy Objects (GPOs).</span></span> <span data-ttu-id="80645-105">Pour diagnostiquer des problèmes qui ne sont pas répertoriés ici, il est possible que l’Administrateur AGPM (contrôle total) utilise la journalisation et le suivi.</span><span class="sxs-lookup"><span data-stu-id="80645-105">To diagnose issues not listed here, it may be helpful for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="80645-106">Pour plus d’informations, voir [configurer la journalisation et le suivi](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

**<span data-ttu-id="80645-107">Remarque</span><span class="sxs-lookup"><span data-stu-id="80645-107">Note</span></span>**  
-   <span data-ttu-id="80645-108">Pour plus d’informations sur la restauration d’une version antérieure d’un objet de stratégie de groupe en cas de problème, reportez-vous [à la rubrique revenir à une version antérieure d’un objet de stratégie de groupe](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-108">For information about rolling back to an earlier version of a GPO if there are problems, see [Roll Back to an Earlier Version of a GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span></span>

-   <span data-ttu-id="80645-109">Pour plus d’informations sur la récupération d’un sinistre en restaurant l’archive complète à partir d’une sauvegarde, voir [restaurer l’archive à partir d’une sauvegarde](restore-the-archive-from-a-backup-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-109">For information about how to recover from a disaster by restoring the complete archive from a backup, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

 

## <span data-ttu-id="80645-110">Quels problèmes rencontrez-vous?</span><span class="sxs-lookup"><span data-stu-id="80645-110">What problems are you having?</span></span>


-   [<span data-ttu-id="80645-111">Je ne peux pas accéder à une archive</span><span class="sxs-lookup"><span data-stu-id="80645-111">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="80645-112">L’état de l’objet de stratégie de groupe varie selon les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="80645-112">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="80645-113">Je ne parviens pas à modifier la connexion à un serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="80645-113">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="80645-114">Je ne parviens pas à changer le modèle par défaut ou à afficher, créer, modifier, renommer, déployer ou supprimer des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="80645-114">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="80645-115">Je ne peux pas utiliser un nom d’objet GPO particulier</span><span class="sxs-lookup"><span data-stu-id="80645-115">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="80645-116">Je ne reçois pas de notifications par courrier électronique AGPM</span><span class="sxs-lookup"><span data-stu-id="80645-116">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="80645-117">Je ne peux pas utiliser le port 4600 pour le service AGPM</span><span class="sxs-lookup"><span data-stu-id="80645-117">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="80645-118">Le service AGPM ne démarre pas</span><span class="sxs-lookup"><span data-stu-id="80645-118">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="80645-119">Échec de l’installation de logiciels de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="80645-119">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

-   [<span data-ttu-id="80645-120">Une erreur s’est produite lors de la restauration de l’archivage sur un nouveau serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="80645-120">An error occurred when I restored the archive to a new AGPM Server</span></span>](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="80645-121">Je ne peux pas accéder à une archive</span><span class="sxs-lookup"><span data-stu-id="80645-121">I am unable to access an archive</span></span>

-   <span data-ttu-id="80645-122">**Cause**: vous n’avez pas sélectionné le serveur et le port appropriés pour l’archive.</span><span class="sxs-lookup"><span data-stu-id="80645-122">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="80645-123">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="80645-123">**Solution**:</span></span>

    -   <span data-ttu-id="80645-124">Si vous êtes un administrateur AGPM: voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-124">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="80645-125">Si vous n’êtes pas un administrateur AGPM: Demandez les détails de connexion du serveur AGPM auprès d’un administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="80645-125">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="80645-126">Voir [configurer une connexion de serveur AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-126">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

-   <span data-ttu-id="80645-127">**Raison**: le service AGPM n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="80645-127">**Cause**: The AGPM Service is not running.</span></span>

-   <span data-ttu-id="80645-128">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="80645-128">**Solution**:</span></span>

    -   <span data-ttu-id="80645-129">Si vous êtes un administrateur AGPM: démarrez le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="80645-129">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="80645-130">Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-130">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    -   <span data-ttu-id="80645-131">Si vous n’êtes pas un administrateur AGPM: contactez un administrateur AGPM pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="80645-131">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="80645-132">L’état de l’objet de stratégie de groupe varie selon les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="80645-132">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="80645-133">**Raison**: d’autres administrateurs de stratégie de groupe ont sélectionné différents serveurs AGPM pour la même archive.</span><span class="sxs-lookup"><span data-stu-id="80645-133">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="80645-134">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="80645-134">**Solution**:</span></span>

    -   <span data-ttu-id="80645-135">Si vous êtes un administrateur AGPM: voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-135">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="80645-136">Si vous n’êtes pas un administrateur AGPM: Demandez les détails de connexion du serveur AGPM auprès d’un administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="80645-136">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="80645-137">Voir [configurer une connexion de serveur AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-137">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="80645-138">Je ne parviens pas à modifier la connexion à un serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="80645-138">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="80645-139">**Raison**: si les paramètres sous l’onglet **serveur AGPM** ne sont pas disponibles, le serveur AGPM a été configuré de manière centralisée à l’aide d’un modèle d’administration.</span><span class="sxs-lookup"><span data-stu-id="80645-139">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="80645-140">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="80645-140">**Solution**:</span></span>

    -   <span data-ttu-id="80645-141">Si vous êtes un administrateur AGPM: si les paramètres sous l’onglet **serveur AGPM** ne sont pas disponibles, voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-141">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

    -   <span data-ttu-id="80645-142">Si vous n’êtes pas un administrateur AGPM: si les paramètres sous l’onglet **serveur AGPM** ne sont pas disponibles, vous n’êtes pas obligé de modifier le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="80645-142">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="80645-143">Je ne parviens pas à changer le modèle par défaut ou à afficher, créer, modifier, renommer, déployer ou supprimer des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="80645-143">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="80645-144">**Cause**: vous n’avez pas reçu de rôle avec les autorisations requises pour effectuer les tâches ou tâches.</span><span class="sxs-lookup"><span data-stu-id="80645-144">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="80645-145">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="80645-145">**Solution**:</span></span>

    -   <span data-ttu-id="80645-146">Si vous êtes un administrateur d’AGPM: voir [déléguer l’accès au niveau du domaine à l’archive et l'](delegate-domain-level-access-to-the-archive-agpm40.md) [accès délégué à un objet GPO individuel dans l’archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-146">If you are an AGPM Administrator: See [Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm40.md) and [Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md).</span></span> <span data-ttu-id="80645-147">Les autorisations AGPM seront mises en cascade à partir du domaine vers tous les objets de stratégie de groupe actuellement présents dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="80645-147">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="80645-148">Pour plus d’informations sur les rôles pouvant exécuter une tâche et les autorisations nécessaires à l’exécution d’une tâche, voir l’aide de cette tâche.</span><span class="sxs-lookup"><span data-stu-id="80645-148">For details about which roles can perform a task and which permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="80645-149">Si vous n’êtes pas un administrateur AGPM et que vous avez besoin d’autorisations ou de rôles supplémentaires: contactez un administrateur AGPM pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="80645-149">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="80645-150">Sachez que si vous êtes un éditeur, vous pouvez commencer le processus de création d’un objet de stratégie de groupe, de déploiement d’un objet de stratégie de groupe ou de suppression d’un objet de stratégie de groupe à partir de l’environnement de production du domaine, mais un approbateur ou un administrateur AGPM doit approuver votre demande.</span><span class="sxs-lookup"><span data-stu-id="80645-150">Be aware that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment of the domain, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="80645-151">Je ne peux pas utiliser un nom d’objet GPO particulier</span><span class="sxs-lookup"><span data-stu-id="80645-151">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="80645-152">**Cause**: le nom de l’objet de stratégie de groupe est déjà utilisé ou vous ne disposez pas des autorisations nécessaires pour le répertorier.</span><span class="sxs-lookup"><span data-stu-id="80645-152">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="80645-153">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="80645-153">**Solution**:</span></span>

    -   <span data-ttu-id="80645-154">Si le nom de l’objet de stratégie de groupe s’affiche sous l’onglet **contrôlé**, non **contrôlé**ou **en attente** , sélectionnez un autre nom.</span><span class="sxs-lookup"><span data-stu-id="80645-154">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="80645-155">Si un objet de stratégie de groupe qui a été déployé est renommé mais qu’il n’a pas encore été redéployé, il sera affiché sous son ancien nom dans l’environnement de production du domaine.</span><span class="sxs-lookup"><span data-stu-id="80645-155">If a GPO that was deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment of the domain.</span></span> <span data-ttu-id="80645-156">Par conséquent, l’ancien nom est toujours utilisé.</span><span class="sxs-lookup"><span data-stu-id="80645-156">Therefore, the old name is still being used.</span></span> <span data-ttu-id="80645-157">Redéploiement de l’objet de stratégie de groupe pour mettre à jour son nom dans l’environnement de production et libérer ce nom pour une utilisation par un autre objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="80645-157">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="80645-158">Si le nom de l’objet GPO n’apparaît pas dans l’onglet **contrôlé**, non **contrôlé**ou **en attente** , il est possible que vous ne disposiez pas des autorisations nécessaires pour afficher l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="80645-158">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="80645-159">Pour demander une autorisation, contactez un administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="80645-159">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="80645-160">Je ne reçois pas de notifications par courrier électronique AGPM</span><span class="sxs-lookup"><span data-stu-id="80645-160">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="80645-161">**Raison**: un serveur de courrier électronique SMTP et une adresse de messagerie valides n’ont pas été fournis ou aucune action ne a été effectuée pour générer une notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="80645-161">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="80645-162">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="80645-162">**Solution**:</span></span>

    -   <span data-ttu-id="80645-163">Si vous êtes un administrateur d’AGPM: pour les notifications par courrier électronique concernant les actions en attente envoyées par AGPM, un administrateur AGPM doit fournir un serveur de messagerie SMTP et des adresses de messagerie valides pour les approbateurs dans l’onglet **délégation de domaine** . Pour plus d’informations, voir [configurer une notification par courrier électronique](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-163">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

    -   <span data-ttu-id="80645-164">Les notifications par courrier électronique sont générées uniquement lorsque l’éditeur, le réviseur ou un autre administrateur de stratégie de groupe qui ne dispose pas de l’autorisation nécessaire pour créer, déployer ou supprimer un objet GPO envoie une demande pour l’une de ces actions.</span><span class="sxs-lookup"><span data-stu-id="80645-164">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="80645-165">Il n’y a aucune notification automatique d’approbation ou de rejet d’une demande.</span><span class="sxs-lookup"><span data-stu-id="80645-165">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="80645-166">Je ne peux pas utiliser le port 4600 pour le service AGPM</span><span class="sxs-lookup"><span data-stu-id="80645-166">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="80645-167">**Raison**: par défaut, le port sur lequel le service AGPM écoute est le port 4600.</span><span class="sxs-lookup"><span data-stu-id="80645-167">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="80645-168">**Solution**: si le port 4600 n’est pas disponible pour le service AGPM, modifiez la configuration de port sur le serveur AGPM pour utiliser un autre port, puis mettez à jour le port dans la connexion de serveur AGPM pour les clients AGPM.</span><span class="sxs-lookup"><span data-stu-id="80645-168">**Solution**: If port 4600 is not available for the AGPM Service, modify the port configuration on the AGPM Server to use another port and then update the port in the AGPM Server connection for AGPM Clients.</span></span> <span data-ttu-id="80645-169">Pour plus d’informations, voir [modifier le service AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-169">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="80645-170">Le service AGPM ne démarre pas</span><span class="sxs-lookup"><span data-stu-id="80645-170">The AGPM Service will not start</span></span>

-   <span data-ttu-id="80645-171">**Raison**: vous avez modifié les paramètres du service AGPM dans le système d’exploitation sous outils et **services** **d’administration** .</span><span class="sxs-lookup"><span data-stu-id="80645-171">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="80645-172">**Solution**: modifiez les paramètres de la **gestion de stratégie de groupe avancée Microsoft-serveur** sous **programmes et fonctionnalités** dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="80645-172">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Programs and Features** in Control Panel.</span></span> <span data-ttu-id="80645-173">Pour plus d’informations, voir [modifier le service AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-173">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="80645-174">Échec de l’installation de logiciels de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="80645-174">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="80645-175">**Raison**: AGPM conserve l’intégrité des packages d’installation de logiciels de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="80645-175">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="80645-176">Bien que les objets de stratégie de groupe soient modifiés hors connexion, les liens entre les packages en plus des informations client mises en cache sont conservés.</span><span class="sxs-lookup"><span data-stu-id="80645-176">Although GPOs are edited offline, links between packages in addition to cached client information are preserved.</span></span> <span data-ttu-id="80645-177">Cela est normal.</span><span class="sxs-lookup"><span data-stu-id="80645-177">This is by design.</span></span>

-   <span data-ttu-id="80645-178">**Solution**: lorsque vous modifiez un objet de stratégie de groupe hors connexion avec AGPM, configurez la mise à niveau de l’installation de logiciels de stratégie de groupe d’un package dans un autre objet de stratégie de groupe pour référencer l’objet de stratégie de groupe déployé et non la copie</span><span class="sxs-lookup"><span data-stu-id="80645-178">**Solution**: When you edit a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="80645-179">L’éditeur doit disposer d’une autorisation de **lecture** pour l’objet GPO déployé.</span><span class="sxs-lookup"><span data-stu-id="80645-179">The Editor must have **Read** permission for the deployed GPO.</span></span>

### <a href="" id="bkmk-error-on-restore"></a><span data-ttu-id="80645-180">Une erreur s’est produite lors de la restauration de l’archivage sur un nouveau serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="80645-180">An error occurred when I restored the archive to a new AGPM Server</span></span>

-   <span data-ttu-id="80645-181">**Raison**: pour des raisons de sécurité, le chiffrement qui protège le mot de passe entré sous l’onglet **délégation de domaine** entraîne l’échec du mot de passe si l’archive est déplacée vers un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="80645-181">**Cause**: For security reasons, the encryption protecting the password entered on the **Domain Delegation** tab causes the password to fail if the archive is moved to another computer.</span></span>

-   <span data-ttu-id="80645-182">**Solution**: entrez à nouveau et confirmez le mot de passe dans l’onglet **délégation de domaine** . Pour plus d’informations, voir [configurer une notification par courrier électronique](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="80645-182">**Solution**: Re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

 

 






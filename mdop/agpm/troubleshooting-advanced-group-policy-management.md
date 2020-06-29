---
title: Résolution des problèmes de la Gestion avancée des stratégies de groupe
description: Résolution des problèmes de la Gestion avancée des stratégies de groupe
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807433"
---
# <span data-ttu-id="a81e6-103">Résolution des problèmes de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="a81e6-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="a81e6-104">Cette section répertorie les problèmes courants que vous pouvez rencontrer lors de l’utilisation de la gestion de stratégie de groupe avancée (AGPM) pour gérer les objets de stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="a81e6-104">This section lists a few common issues you may encounter when using Advanced Group Policy Management (AGPM) to manage Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="a81e6-105">Quels problèmes rencontrez-vous?</span><span class="sxs-lookup"><span data-stu-id="a81e6-105">What problems are you having?</span></span>


-   [<span data-ttu-id="a81e6-106">Je ne peux pas accéder à une archive</span><span class="sxs-lookup"><span data-stu-id="a81e6-106">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="a81e6-107">L’état de l’objet de stratégie de groupe varie selon les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a81e6-107">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="a81e6-108">Je ne parviens pas à modifier la connexion à un serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="a81e6-108">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="a81e6-109">Je ne parviens pas à changer le modèle par défaut ou à afficher, créer, modifier, renommer, déployer ou supprimer des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a81e6-109">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="a81e6-110">Je ne peux pas utiliser un nom d’objet GPO particulier</span><span class="sxs-lookup"><span data-stu-id="a81e6-110">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="a81e6-111">Je ne reçois pas de notifications par courrier électronique AGPM</span><span class="sxs-lookup"><span data-stu-id="a81e6-111">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="a81e6-112">Je ne peux pas utiliser le port 4600 pour le service AGPM</span><span class="sxs-lookup"><span data-stu-id="a81e6-112">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="a81e6-113">Le service AGPM ne démarre pas</span><span class="sxs-lookup"><span data-stu-id="a81e6-113">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="a81e6-114">Échec de l’installation de logiciels de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a81e6-114">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="a81e6-115">Je ne peux pas accéder à une archive</span><span class="sxs-lookup"><span data-stu-id="a81e6-115">I am unable to access an archive</span></span>

-   <span data-ttu-id="a81e6-116">**Cause**: vous n’avez pas sélectionné le serveur et le port appropriés pour l’archive.</span><span class="sxs-lookup"><span data-stu-id="a81e6-116">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="a81e6-117">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="a81e6-117">**Solution**:</span></span>

    -   <span data-ttu-id="a81e6-118">Si vous êtes un administrateur AGPM, voir [configurer la connexion à un serveur AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-118">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="a81e6-119">Si vous n’êtes pas un administrateur AGPM: Demandez les détails de connexion du serveur AGPM auprès d’un administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="a81e6-119">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="a81e6-120">Voir [configurer la connexion à un serveur AGPM](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-120">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

-   <span data-ttu-id="a81e6-121">**Raison**: ce service n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a81e6-121">**Cause**: The Advanced Group Policy Management Service is not running.</span></span>

-   <span data-ttu-id="a81e6-122">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="a81e6-122">**Solution**:</span></span>

    -   <span data-ttu-id="a81e6-123">Si vous êtes un administrateur AGPM: démarrez le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="a81e6-123">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="a81e6-124">Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-124">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).</span></span>

    -   <span data-ttu-id="a81e6-125">Si vous n’êtes pas un administrateur AGPM: contactez un administrateur AGPM pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="a81e6-125">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="a81e6-126">L’état de l’objet de stratégie de groupe varie selon les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a81e6-126">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="a81e6-127">**Raison**: d’autres administrateurs de stratégie de groupe ont sélectionné différents serveurs AGPM pour la même archive.</span><span class="sxs-lookup"><span data-stu-id="a81e6-127">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="a81e6-128">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="a81e6-128">**Solution**:</span></span>

    -   <span data-ttu-id="a81e6-129">Si vous êtes un administrateur AGPM, voir [configurer la connexion à un serveur AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-129">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="a81e6-130">Si vous n’êtes pas un administrateur AGPM: Demandez les détails de connexion du serveur AGPM auprès d’un administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="a81e6-130">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="a81e6-131">Voir [configurer la connexion à un serveur AGPM](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-131">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="a81e6-132">Je ne parviens pas à modifier la connexion à un serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="a81e6-132">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="a81e6-133">**Raison**: si les paramètres sous l’onglet **serveur AGPM** ne sont pas disponibles, le serveur AGPM a été configuré de manière centralisée à l’aide d’un modèle d’administration.</span><span class="sxs-lookup"><span data-stu-id="a81e6-133">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="a81e6-134">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="a81e6-134">**Solution**:</span></span>

    -   <span data-ttu-id="a81e6-135">Si vous êtes un administrateur AGPM: si les paramètres sous l’onglet **serveur AGPM** ne sont pas disponibles, voir [configurer la connexion au serveur AGPM](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-135">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="a81e6-136">Si vous n’êtes pas un administrateur AGPM: si les paramètres sous l’onglet **serveur AGPM** ne sont pas disponibles, vous n’êtes pas obligé de modifier le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="a81e6-136">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="a81e6-137">Je ne parviens pas à changer le modèle par défaut ou à afficher, créer, modifier, renommer, déployer ou supprimer des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a81e6-137">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="a81e6-138">**Cause**: vous n’avez pas reçu de rôle avec les autorisations requises pour effectuer les tâches ou tâches.</span><span class="sxs-lookup"><span data-stu-id="a81e6-138">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="a81e6-139">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="a81e6-139">**Solution**:</span></span>

    -   <span data-ttu-id="a81e6-140">Si vous êtes un administrateur AGPM, voir [déléguer l’accès au niveau du domaine](delegate-domain-level-access.md) et [déléguer l’accès à un objet GPO individuel](delegate-access-to-an-individual-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-140">If you are an AGPM Administrator: See [Delegate Domain-Level Access](delegate-domain-level-access.md) and [Delegate Access to an Individual GPO](delegate-access-to-an-individual-gpo.md).</span></span> <span data-ttu-id="a81e6-141">Les autorisations AGPM seront mises en cascade à partir du domaine vers tous les objets de stratégie de groupe actuellement présents dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="a81e6-141">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="a81e6-142">Comme les administrateurs de stratégie de groupe sont ajoutés au niveau du domaine, leurs autorisations doivent être définies pour être appliquées à **cet objet et aux objets imbriqués**.</span><span class="sxs-lookup"><span data-stu-id="a81e6-142">As new Group Policy administrators are added at the domain level, their permissions must be set to apply to **This object and nested objects**.</span></span> <span data-ttu-id="a81e6-143">Pour plus d’informations sur les rôles pouvant exécuter une tâche et les autorisations nécessaires pour effectuer une tâche, voir l’aide de cette tâche.</span><span class="sxs-lookup"><span data-stu-id="a81e6-143">For details about which roles can perform a task and what permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="a81e6-144">Si vous n’êtes pas un administrateur AGPM et que vous avez besoin d’autorisations ou de rôles supplémentaires: contactez un administrateur AGPM pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="a81e6-144">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="a81e6-145">Notez que si vous êtes un éditeur, vous pouvez commencer le processus de création d’un objet de stratégie de groupe, de déploiement d’un objet de stratégie de groupe ou de suppression d’un objet de stratégie de groupe à partir de l’environnement de production, mais un approbateur ou un administrateur AGPM doit approuver votre demande.</span><span class="sxs-lookup"><span data-stu-id="a81e6-145">Note that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="a81e6-146">Je ne peux pas utiliser un nom d’objet GPO particulier</span><span class="sxs-lookup"><span data-stu-id="a81e6-146">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="a81e6-147">**Cause**: le nom de l’objet de stratégie de groupe est déjà utilisé ou vous ne disposez pas des autorisations nécessaires pour le répertorier.</span><span class="sxs-lookup"><span data-stu-id="a81e6-147">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="a81e6-148">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="a81e6-148">**Solution**:</span></span>

    -   <span data-ttu-id="a81e6-149">Si le nom de l’objet de stratégie de groupe s’affiche sous l’onglet **contrôlé**, non **contrôlé**ou **en attente** , sélectionnez un autre nom.</span><span class="sxs-lookup"><span data-stu-id="a81e6-149">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="a81e6-150">Si un objet de stratégie de groupe qui a été déployé est renommé mais qu’il n’a pas encore été redéployé, il sera affiché sous son ancien nom dans l’environnement de production; par conséquent, l’ancien nom est toujours utilisé.</span><span class="sxs-lookup"><span data-stu-id="a81e6-150">If a GPO that has been deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment—therefore, the old name is still in use.</span></span> <span data-ttu-id="a81e6-151">Redéploiement de l’objet de stratégie de groupe pour mettre à jour son nom dans l’environnement de production et libérer ce nom pour une utilisation par un autre objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a81e6-151">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="a81e6-152">Si le nom de l’objet GPO n’apparaît pas dans l’onglet **contrôlé**, non **contrôlé**ou **en attente** , il est possible que vous ne disposiez pas des autorisations nécessaires pour afficher l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="a81e6-152">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="a81e6-153">Pour demander une autorisation, contactez un administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="a81e6-153">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="a81e6-154">Je ne reçois pas de notifications par courrier électronique AGPM</span><span class="sxs-lookup"><span data-stu-id="a81e6-154">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="a81e6-155">**Raison**: un serveur de courrier électronique SMTP et une adresse de messagerie valides n’ont pas été fournis ou aucune action ne a été effectuée pour générer une notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a81e6-155">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="a81e6-156">**Solution**:</span><span class="sxs-lookup"><span data-stu-id="a81e6-156">**Solution**:</span></span>

    -   <span data-ttu-id="a81e6-157">Si vous êtes un administrateur d’AGPM: pour les notifications par courrier électronique concernant les actions en attente envoyées par AGPM, un administrateur AGPM doit fournir un serveur de messagerie SMTP et des adresses de messagerie valides pour les approbateurs dans l’onglet **délégation de domaine** . Pour plus d’informations, voir [configurer une notification par courrier électronique](configure-e-mail-notification.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-157">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification.md).</span></span>

    -   <span data-ttu-id="a81e6-158">Les notifications par courrier électronique sont générées uniquement lorsque l’éditeur, le réviseur ou un autre administrateur de stratégie de groupe qui ne dispose pas de l’autorisation nécessaire pour créer, déployer ou supprimer un objet GPO envoie une demande pour l’une de ces actions.</span><span class="sxs-lookup"><span data-stu-id="a81e6-158">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="a81e6-159">Il n’y a aucune notification automatique d’approbation ou de rejet d’une demande.</span><span class="sxs-lookup"><span data-stu-id="a81e6-159">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="a81e6-160">Je ne peux pas utiliser le port 4600 pour le service AGPM</span><span class="sxs-lookup"><span data-stu-id="a81e6-160">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="a81e6-161">**Raison**: par défaut, le port sur lequel le service AGPM écoute est le port 4600.</span><span class="sxs-lookup"><span data-stu-id="a81e6-161">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="a81e6-162">**Solution**: si le port 4600 n’est pas disponible pour le service AGPM, modifiez chaque fichier d’index d’archive pour utiliser un autre port, puis mettez à jour le serveur AGPM pour tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a81e6-162">**Solution**: If port 4600 is not available for the AGPM Service, modify each archive index file to use another port and then update the AGPM Server for all Group Policy administrators.</span></span> <span data-ttu-id="a81e6-163">Pour plus d’informations, voir [modifier le port sur lequel écoute le service AGPM](modify-the-port-on-which-the-agpm-service-listens.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-163">For more information, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="a81e6-164">Le service AGPM ne démarre pas</span><span class="sxs-lookup"><span data-stu-id="a81e6-164">The AGPM Service will not start</span></span>

-   <span data-ttu-id="a81e6-165">**Raison**: vous avez modifié les paramètres du service AGPM dans le système d’exploitation sous outils et **services** **d’administration** .</span><span class="sxs-lookup"><span data-stu-id="a81e6-165">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="a81e6-166">**Solution**: modifiez les paramètres de la **gestion de stratégie de groupe avancée Microsoft-serveur** sous **Ajouter ou supprimer des programmes**.</span><span class="sxs-lookup"><span data-stu-id="a81e6-166">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Add or Remove Programs**.</span></span> <span data-ttu-id="a81e6-167">Pour plus d’informations, voir [modifier le compte de service AGPM](modify-the-agpm-service-account.md).</span><span class="sxs-lookup"><span data-stu-id="a81e6-167">For more information, see [Modify the AGPM Service Account](modify-the-agpm-service-account.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="a81e6-168">Échec de l’installation de logiciels de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a81e6-168">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="a81e6-169">**Raison**: AGPM conserve l’intégrité des packages d’installation de logiciels de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a81e6-169">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="a81e6-170">Bien que les objets de stratégie de groupe soient modifiés hors connexion, les liens entre les packages et les informations client mises en cache sont conservés.</span><span class="sxs-lookup"><span data-stu-id="a81e6-170">Although GPOs are edited offline, links between packages as well as cached client information are preserved.</span></span> <span data-ttu-id="a81e6-171">Cela est normal.</span><span class="sxs-lookup"><span data-stu-id="a81e6-171">This is by design.</span></span>

-   <span data-ttu-id="a81e6-172">**Solution**: lors de la modification d’un objet de stratégie de groupe hors connexion avec AGPM, configurez la mise à niveau de l’installation de logiciels de stratégie de groupe d’un package dans un autre objet de stratégie de groupe pour faire référence à l’objet de stratégie de groupe déployé</span><span class="sxs-lookup"><span data-stu-id="a81e6-172">**Solution**: When editing a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="a81e6-173">L’éditeur doit disposer d’une autorisation de **lecture** pour l’objet GPO déployé.</span><span class="sxs-lookup"><span data-stu-id="a81e6-173">The Editor must have **Read** permission for the deployed GPO.</span></span>

 

 






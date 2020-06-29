---
title: Notes de publication de MBAM1.0
description: Notes de publication de MBAM1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811508"
---
# <span data-ttu-id="725f4-103">Notes de publication de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="725f4-103">Release Notes for MBAM 1.0</span></span>


**<span data-ttu-id="725f4-104">Pour rechercher un problème spécifique dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="725f4-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="725f4-105">Lisez attentivement ces notes de publication avant d’installer Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="725f4-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

<span data-ttu-id="725f4-106">Ces notes de publication contiennent des informations requises pour l’installation réussie de MBAM.</span><span class="sxs-lookup"><span data-stu-id="725f4-106">These release notes contain information that is required to successfully install MBAM.</span></span> <span data-ttu-id="725f4-107">Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="725f4-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="725f4-108">S’il existe une différence entre ces notes de publication et d’autres documents de MBAM, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="725f4-108">If there is a difference between these release notes and other MBAM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="725f4-109">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="725f4-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="725f4-110">À propos de la documentation relative aux produits</span><span class="sxs-lookup"><span data-stu-id="725f4-110">About the Product Documentation</span></span>


<span data-ttu-id="725f4-111">Pour plus d’informations sur la documentation MBAM, voir la page d’accueil MBAM sur Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="725f4-111">For information about MBAM documentation, see the MBAM home page on Microsoft TechNet.</span></span>

<span data-ttu-id="725f4-112">Pour obtenir la version téléchargeable de la documentation MBAM, voir <https://go.microsoft.com/fwlink/p/?LinkId=225356> sur le centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="725f4-112">To obtain a downloadable copy of the MBAM documentation, see <https://go.microsoft.com/fwlink/p/?LinkId=225356> on the Microsoft Download Center.</span></span>

## <span data-ttu-id="725f4-113">Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="725f4-113">Provide Feedback</span></span>


<span data-ttu-id="725f4-114">Vos commentaires vous intéressent sur MBAM.</span><span class="sxs-lookup"><span data-stu-id="725f4-114">We are interested in your feedback on MBAM.</span></span> <span data-ttu-id="725f4-115">Vous pouvez envoyer vos commentaires à <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="725f4-115">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="725f4-116">**Remarques**  Cette adresse de messagerie n’est pas un canal de support, mais vos commentaires nous aideront à planifier des changements ultérieurs dans la documentation et les versions de nos produits.</span><span class="sxs-lookup"><span data-stu-id="725f4-116">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="725f4-117">Pour obtenir les informations les plus récentes sur MDOP et les ressources de formation supplémentaires, voir la page d' [utilisation de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="725f4-117">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="725f4-118">Pour en savoir plus sur les nouvelles mises à jour ou pour nous faire part de vos commentaires, suivez-nous sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="725f4-118">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="725f4-119">Problèmes connus avec MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="725f4-119">Known Issues with MBAM 1.0</span></span>


<span data-ttu-id="725f4-120">Cette section contient des notes de publication relatives aux problèmes connus liés à la configuration et à l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="725f4-120">This section contains release notes about the known issues with MBAM setup and installation.</span></span>

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a><span data-ttu-id="725f4-121">Si vous sélectionnez l’option «utiliser un certificat pour chiffrer les communications réseau» lors de l’installation, les connexions de base de données et les applications dépendantes existantes peuvent cesser de fonctionner</span><span class="sxs-lookup"><span data-stu-id="725f4-121">If you select the “Use a certificate to encrypt the network communication” option during Setup, existing database connections and dependent applications can stop functioning</span></span>

<span data-ttu-id="725f4-122">Vous pouvez configurer MBAM pour la **communication réseau chiffrée** après l’installation de la base de données de récupération et du matériel ou des fonctionnalités de la base de données d’état de conformité.</span><span class="sxs-lookup"><span data-stu-id="725f4-122">You can configure MBAM for **Encrypted network communication** after you install either the Recovery and Hardware Database or the Compliance Status Database features.</span></span> <span data-ttu-id="725f4-123">Si vous choisissez de configurer MBAM pour la communication réseau chiffrée, MBAM programme d’installation configure l’instance du moteur de base de données SQL Server de façon à utiliser SSL (Secure Sockets Layer) pour la communication entre la base de données en vigueur et les fonctionnalités du serveur d’administration et de surveillance ainsi que les fonctionnalités du serveur rapport de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="725f4-123">If you choose to configure MBAM for Encrypted network communication, MBAM Setup configures the instance of the SQL Server Database Engine to use Secure Sockets Layer (SSL) for communication between the applicable database and both the Administration and Monitoring Server and the Compliance and Audit Report Server features.</span></span>

-   <span data-ttu-id="725f4-124">Si l’instance du moteur de base de données SQL Server n’est pas déjà configurée pour utiliser SSL, le programme d’installation de MBAM la configure pour le faire.</span><span class="sxs-lookup"><span data-stu-id="725f4-124">If the instance of the SQL Server Database Engine is not already configured to use SSL, MBAM Setup configures it to do so.</span></span> <span data-ttu-id="725f4-125">Cela peut empêcher les applications qui essaient d’utiliser des bases de données non MBAM sur l’instance du moteur de base de données SQL Server de communiquer avec leurs bases de données.</span><span class="sxs-lookup"><span data-stu-id="725f4-125">This can prevent applications that try to use non-MBAM databases on the instance of the SQL Server Database Engine from communicating with their databases.</span></span>

-   <span data-ttu-id="725f4-126">Si l’instance du moteur de base de données SQL Server est déjà configurée pour utiliser SSL, il est configuré de manière à utiliser le certificat que l’utilisateur a sélectionné lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="725f4-126">If the instance of the SQL Server Database Engine is already configured to use SSL, it is configured to use the certificate that the user selected during setup.</span></span> <span data-ttu-id="725f4-127">Si ce certificat est différent de celui déjà utilisé, il peut empêcher l’exécution des applications qui utilisent les bases de données SQL Server sur l’instance du moteur de base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="725f4-127">If this certificate differs from the one that was already in use, it can prevent applications that use SQL Server databases on the instance of the SQL Server Database Engine from running.</span></span>

<span data-ttu-id="725f4-128">**Solution de contournement:** Néant</span><span class="sxs-lookup"><span data-stu-id="725f4-128">**WORKAROUND:** None</span></span>

### <span data-ttu-id="725f4-129">Échec de la configuration de MBAM lors de l’installation lorsque vous utilisez un compte d’administrateur local</span><span class="sxs-lookup"><span data-stu-id="725f4-129">MBAM Setup fails during installation when you use a local Administrator account</span></span>

<span data-ttu-id="725f4-130">Échec de l’installation d’MBAM lorsque vous utilisez un compte d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="725f4-130">MBAM Setup fails when you use a local Administrator account.</span></span> <span data-ttu-id="725f4-131">Le fichier journal contient les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="725f4-131">The log file contains the following information:</span></span>

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

<span data-ttu-id="725f4-132">**Solution de contournement:** Utilisez un compte de domaine avec des informations d’identification d’administrateur sur l’ordinateur serveur lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="725f4-132">**WORKAROUND:** Use a domain account with administrative credentials on the server computer when you install MBAM.</span></span>

### <span data-ttu-id="725f4-133">MBAM-XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX</span><span class="sxs-lookup"><span data-stu-id="725f4-133">MBAM Setup reconfigures the instance of the SQL Server Database Engine to not use SSL if you select “Do not encrypt network communication”</span></span>

<span data-ttu-id="725f4-134">Lorsque vous installez la base de données de récupération et de matériel ou la base de données de statut de conformité, vous pouvez utiliser le programme d’installation pour configurer MBAM en sélectionnant **communication réseau chiffrée**.</span><span class="sxs-lookup"><span data-stu-id="725f4-134">When you install either the Recovery and Hardware Database or the Compliance Status Database, you can use Setup to configure MBAM by selecting **Encrypted network communication**.</span></span> <span data-ttu-id="725f4-135">Si vous décidez de ne pas chiffrer la communication réseau, le programme d’installation de MBAM reconfigure l’instance du moteur de base de données SQL Server de sorte qu’elle n’utilise pas SSL.</span><span class="sxs-lookup"><span data-stu-id="725f4-135">If you decide not to encrypt the network communication, MBAM Setup reconfigures the instance of the SQL Server Database Engine so that it does not use SSL.</span></span>

-   <span data-ttu-id="725f4-136">Si l’instance du moteur de base de données SQL Server est déjà configurée pour utiliser SSL, le programme d’installation d’MBAM désactive SSL sur l’instance du moteur de base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="725f4-136">If the instance of the SQL Server Database Engine is already configured to use SSL, MBAM Setup disables SSL on the instance of the SQL Server Database Engine.</span></span> <span data-ttu-id="725f4-137">Cette opération modifie la sécurité des communications entre les applications qui utilisent des bases de données qui ne sont pas liées à des bases de données MBAM sur l’instance du moteur de base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="725f4-137">This changes the communication security between the applications that use databases that are not related to MBAM databases on the instance of the SQL Server Database Engine.</span></span>

<span data-ttu-id="725f4-138">**Solution de contournement:** Néant</span><span class="sxs-lookup"><span data-stu-id="725f4-138">**WORKAROUND:** None</span></span>

### <span data-ttu-id="725f4-139">Conditions préalables manquantes pour les scripts de gestion d’Internet Information Services (IIS) et la fonctionnalité serveur Web outils</span><span class="sxs-lookup"><span data-stu-id="725f4-139">Missing prerequisite for the Internet Information Services (IIS) Management Scripts and Tools web server feature</span></span>

<span data-ttu-id="725f4-140">La configuration de MBAM dépend des scripts de gestion IIS et de la fonctionnalité serveur Web outils, mais elle n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="725f4-140">MBAM Setup is dependent on the IIS Management Scripts and Tools web server feature, but it is not an enforced prerequisite.</span></span> <span data-ttu-id="725f4-141">Le programme d’installation du serveur vous permet d’installer MBAM lorsque cette fonctionnalité n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="725f4-141">Server setup lets you install MBAM when this feature is missing.</span></span> <span data-ttu-id="725f4-142">Toutefois, cela a pour effet que le rédacteur du service de sauvegarde MBAM le démarrage puis s’arrête, car il ne parvient pas à trouver les informations WMI (Windows Management Instrumentation) et les fournisseurs de services Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="725f4-142">However, this will cause the backup service MBAM VSS Writer to start and then stop, because it cannot locate the Windows Management Instrumentation (WMI) and the Internet Information Services (IIS) provider.</span></span> <span data-ttu-id="725f4-143">Aucun message d’erreur ne s’affiche pour cette condition, sauf dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="725f4-143">There is no error message for this condition, except that which occurs in the event log.</span></span> <span data-ttu-id="725f4-144">L’installation d’MBAM sans les scripts et les outils de gestion IIS entraîne l’exécution des opérations de sauvegarde pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="725f4-144">Installation of MBAM without IIS Management Scripts and Tools causes the backup operations not to run for MBAM.</span></span>

<span data-ttu-id="725f4-145">**Solution de contournement:** Assurez-vous que les scripts de gestion IIS et la fonctionnalité serveur Web Tools sont installés avant de lancer la configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="725f4-145">**WORKAROUND:** Ensure that the IIS Management Scripts and Tools web server feature is installed before you start the MBAM Setup.</span></span>

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a><span data-ttu-id="725f4-146">Le programme d’installation d’MBAM cesse de répondre lors de la phase d’installation des fonctionnalités sélectionnées lorsque le programme d’installation est configuré pour utiliser un certificat</span><span class="sxs-lookup"><span data-stu-id="725f4-146">MBAM Setup stops responding during the “Installing selected features” phase when setup is configured to use a certificate</span></span>

<span data-ttu-id="725f4-147">Le programme d’installation d’MBAM cesse de répondre lors de l' **installation de fonctionnalités sélectionnées** du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="725f4-147">MBAM Setup stops responding during the **Installing selected features** phase of setup.</span></span> <span data-ttu-id="725f4-148">Cette situation se produit lors de l’installation de la base de données de récupération et de matériel ou de la base de données d’état de conformité, après avoir sélectionné l’option **utiliser un certificat pour chiffrer les communications réseau** .</span><span class="sxs-lookup"><span data-stu-id="725f4-148">This occurs during the installation of the Recovery and Hardware Database or the Compliance Status Database, after you select the **Use a certificate to encrypt the network communication** option.</span></span> <span data-ttu-id="725f4-149">Par ailleurs, la configuration d’MBAM cesse de répondre si l’instance du moteur de base de données SQL Server ne peut pas accéder au certificat qui a été spécifié lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="725f4-149">Furthermore, the MBAM Setup stops responding if the instance of the SQL Server Database Engine cannot access the certificate that was specified during setup.</span></span>

<span data-ttu-id="725f4-150">**Solution de contournement:** Mettez à jour les autorisations sur le certificat, afin que le service Windows pour l’instance correspondante du moteur de base de données SQL Server puisse accéder au certificat.</span><span class="sxs-lookup"><span data-stu-id="725f4-150">**WORKAROUND:** Update the permissions on the certificate, so that the Windows service for the applicable instance of the SQL Server Database Engine can access the certificate.</span></span> <span data-ttu-id="725f4-151">Vous pouvez également modifier le compte sous lequel l’instance du moteur de base de données SQL Server s’exécute, afin que le moteur de base de données utilise le certificat.</span><span class="sxs-lookup"><span data-stu-id="725f4-151">You can also change the account under which the instance of the SQL Server Database Engine runs, for the database engine to use the certificate.</span></span> <span data-ttu-id="725f4-152">Pour déterminer les autorisations du certificat, tapez la commande suivante à l’invite de commandes: **certutil-v-Store My**</span><span class="sxs-lookup"><span data-stu-id="725f4-152">To determine the permissions for the certificate, type the following command at the command prompt: **certutil -v -store MY**</span></span>

### <span data-ttu-id="725f4-153">La configuration de MBAM est interrompue lors de l’installation de SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="725f4-153">MBAM Setup pauses when you install SQL Server Reporting Services</span></span>

<span data-ttu-id="725f4-154">Lors de l’installation d’MBAM, lorsque vous sélectionnez une instance de SQL Server Reporting Services (SSRS) et qu’elle n’est pas disponible, ou qu’elle est configurée de manière incorrecte, le programme d’installation de MBAM risque de suspendre pendant une minute tout en essayant de communiquer avec l’instance SSRS.</span><span class="sxs-lookup"><span data-stu-id="725f4-154">During MBAM installation, when you select an instance of SQL Server Reporting Services (SSRS) and SSRS instance is not available or it is configured incorrectly, the MBAM Setup might pause for up to one minute while it attempts to communicate with the SSRS instance.</span></span>

<span data-ttu-id="725f4-155">**Solution de contournement:** Attendez au moins une minute pour la reprise de l’installation d’MBAM alors que le programme d’installation tente de contacter l’instance de SSRS.</span><span class="sxs-lookup"><span data-stu-id="725f4-155">**WORKAROUND:** Wait for at least one minute for MBAM Setup to resume while the Setup program attempts to contact the instance of SSRS.</span></span>

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a><span data-ttu-id="725f4-156">Le serveur d’administration et de surveillance ne s’exécute pas après l’installation</span><span class="sxs-lookup"><span data-stu-id="725f4-156">Administration and Monitoring Server does not run after setup</span></span>

<span data-ttu-id="725f4-157">Après l’installation réussie de la fonctionnalité d’administration et de surveillance du serveur par MBAM, MBAM affiche des messages d’erreur lorsque vous essayez d’accéder au site Web de l’administrateur MBAM.</span><span class="sxs-lookup"><span data-stu-id="725f4-157">After MBAM Setup successfully installs the Administration and Monitoring Server feature, MBAM displays error messages when you try to access the MBAM administrator website.</span></span> <span data-ttu-id="725f4-158">Ce problème survient pour l’une des raisons suivantes:</span><span class="sxs-lookup"><span data-stu-id="725f4-158">This issue occurs for one of the following reasons:</span></span>

-   <span data-ttu-id="725f4-159">Une ou plusieurs conditions préalables sur le serveur d’administration et de surveillance ont été supprimées après l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="725f4-159">One or more prerequisites on the Administration and Monitoring Server were removed after the MBAM installation.</span></span>

-   <span data-ttu-id="725f4-160">Une ou plusieurs conditions préalables ont été installées sur le serveur et ont été supprimées après l’exécution de la configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="725f4-160">One or more prerequisites were installed on the server and later they were removed before running the MBAM Setup.</span></span>

<span data-ttu-id="725f4-161">**Solution de contournement:** Passez en revue la documentation MBAM et vérifiez que tous les éléments requis MBAM sont installés.</span><span class="sxs-lookup"><span data-stu-id="725f4-161">**WORKAROUND:** Review the MBAM documentation and confirm that all MBAM prerequisites are installed.</span></span>

### <span data-ttu-id="725f4-162">Un clic sur les liens de documentation lors de l’installation entraîne l’exécution d’une erreur d’application après la fin de l’installation</span><span class="sxs-lookup"><span data-stu-id="725f4-162">Clicking documentation links during Setup results in an application error after Setup is finished</span></span>

<span data-ttu-id="725f4-163">Lorsque vous cliquez sur un lien de la documentation lors de l’installation, puis fermez le programme d’installation en cliquant sur **Annuler** ou **Terminer** une fois l’installation terminée, un message d’erreur d’application s’affiche.</span><span class="sxs-lookup"><span data-stu-id="725f4-163">When you click a documentation link during setup and then close the Setup program by clicking **Cancel** or **Finish** after Setup has successfully finished, an application error message appears..</span></span> <span data-ttu-id="725f4-164">Le problème est dû à une erreur de violation d’accès dans le planificateur de tâches Windows.</span><span class="sxs-lookup"><span data-stu-id="725f4-164">The problem is caused by an access violation error in the Windows Task Scheduler.</span></span>

<span data-ttu-id="725f4-165">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="725f4-165">**WORKAROUND:** None.</span></span> <span data-ttu-id="725f4-166">Vous pouvez ignorer cette erreur.</span><span class="sxs-lookup"><span data-stu-id="725f4-166">You can ignore this error.</span></span>

### <span data-ttu-id="725f4-167">Échec de l’installation d’MBAM ne supprime pas les nouvelles bases de données</span><span class="sxs-lookup"><span data-stu-id="725f4-167">Failed MBAM Setup does not remove new databases</span></span>

<span data-ttu-id="725f4-168">En cas d’échec de la configuration de MBAM, il est possible que le programme d’installation ne supprime pas les bases de données nouvellement créées.</span><span class="sxs-lookup"><span data-stu-id="725f4-168">If the MBAM Setup fails, Setup might not remove the newly created databases.</span></span> <span data-ttu-id="725f4-169">Cela peut provoquer des échecs lors des installations suivantes.</span><span class="sxs-lookup"><span data-stu-id="725f4-169">This can cause failures during subsequent installations.</span></span>

<span data-ttu-id="725f4-170">**Solution de contournement:** Sélectionnez un autre nom pour l’instance de base de données au cours de l’installation suivante.</span><span class="sxs-lookup"><span data-stu-id="725f4-170">**WORKAROUND:** Choose a different name for the database instance during the subsequent installation.</span></span>

### <span data-ttu-id="725f4-171">Le programme d’installation d’MBAM ne reconnaît pas les certificats valides de cluster d’équilibrage de charge réseau</span><span class="sxs-lookup"><span data-stu-id="725f4-171">MBAM Setup does not recognize valid network load-balancing cluster certificates</span></span>

<span data-ttu-id="725f4-172">Lors de l’installation du serveur d’administration et de surveillance d’MBAM, l’option de chiffrement réseau sélectionnée ne correspond pas au certificat valide.</span><span class="sxs-lookup"><span data-stu-id="725f4-172">During the MBAM Administration and Monitoring Server installation, with the network encryption option selected, the cluster certificate is not recognized as a valid certificate.</span></span> <span data-ttu-id="725f4-173">Il est reconnu comme valide lorsque le certificat de communication avec la base de données est installé, mais qu’il est rejeté pour la communication par le cluster d’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="725f4-173">It is recognized as valid when the certificate for communication with the database is installed, but it is rejected for communication by the load-balancing cluster.</span></span>

<span data-ttu-id="725f4-174">**Solution de contournement:** Vérifiez que la liste de révocation de certificats associée au certificat est accessible, ou utilisez un certificat qui ne nécessite pas une validation à l’aide de la liste de révocation.</span><span class="sxs-lookup"><span data-stu-id="725f4-174">**WORKAROUND:** Confirm that the certificate revocation list (CRL) associated with the certificate is accessible, or use a certificate that does not require validation by using the CRL.</span></span>

## <span data-ttu-id="725f4-175">Informations de copyright des notes de publication</span><span class="sxs-lookup"><span data-stu-id="725f4-175">Release Notes Copyright Information</span></span>


<span data-ttu-id="725f4-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="725f4-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="725f4-177">Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="725f4-177">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="725f4-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="725f4-178">Related topics</span></span>


[<span data-ttu-id="725f4-179">À propos de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="725f4-179">About MBAM 1.0</span></span>](about-mbam-10.md)

 

 






---
title: Notes de publication pour App-V5.1
description: Notes de publication pour App-V5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804879"
---
# <span data-ttu-id="491dc-103">Notes de publication pour App-V5.1</span><span class="sxs-lookup"><span data-stu-id="491dc-103">Release Notes for App-V 5.1</span></span>


<span data-ttu-id="491dc-104">Vous trouverez ci-après des problèmes connus dans Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="491dc-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.1.</span></span>

## <span data-ttu-id="491dc-105">Une erreur se produit lors de l’actualisation de la publication entre le serveur de gestion App-V 5,0 SP3 et le client App-V 5,1 sur Windows 10</span><span class="sxs-lookup"><span data-stu-id="491dc-105">Error occurs during publishing refresh between App-V 5.0 SP3 Management Server and App-V 5.1 Client on Windows 10</span></span>


<span data-ttu-id="491dc-106">Une erreur est générée lors de l’actualisation de la publication lors de la synchronisation des packages du serveur de gestion App-V 5,0 SP3 vers un client App-V 5,1 sur Windows 10.</span><span class="sxs-lookup"><span data-stu-id="491dc-106">An error is generated during publishing refresh when synchronizing packages from the App-V 5.0 SP3 management server to an App-V 5.1 client on Windows 10 .</span></span> <span data-ttu-id="491dc-107">Cette erreur se produit car le serveur App-V 5,0 SP3 ne comprend pas le système d’exploitation Windows 10 qui est spécifié dans l’URL de publication.</span><span class="sxs-lookup"><span data-stu-id="491dc-107">This error occurs because the App-V 5.0 SP3 server does not understand the Windows 10 operating system that is specified in the publishing URL.</span></span> <span data-ttu-id="491dc-108">Ce problème a été résolu pour le serveur de publication 5,1 App-V, mais n’est pas transféré vers des versions de App-V 5,0 SP3 ou antérieure.</span><span class="sxs-lookup"><span data-stu-id="491dc-108">The issue is fixed for App-V 5.1 publishing server, but is not backported to versions of App-V 5.0 SP3 or earlier.</span></span>

<span data-ttu-id="491dc-109">**Solution de contournement**: mettez à niveau le serveur de gestion App-v 5,0 vers le serveur de gestion App-v 5,1 pour les clients Windows 10.</span><span class="sxs-lookup"><span data-stu-id="491dc-109">**Workaround**: Upgrade the App-V 5.0 Management server to the App-V 5.1 Management server for Windows 10 Clients.</span></span>

## <span data-ttu-id="491dc-110">Les configurations personnalisées ne sont pas appliquées pour les packages qui seront publiés globalement s’ils sont définis à l’aide du serveur App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="491dc-110">Custom configurations do not get applied for packages that will be published globally if they are set using the App-V 5.1 Server</span></span>


<span data-ttu-id="491dc-111">Si vous affectez un package à un groupe d’annonces qui contient des comptes d’ordinateur et appliquez une configuration personnalisée à ce groupe à l’aide du serveur App-V, la configuration personnalisée ne sera pas appliquée à ces machines.</span><span class="sxs-lookup"><span data-stu-id="491dc-111">If you assign a package to an AD group that contains machine accounts and apply a custom configuration to that group using the App-V Server, the custom configuration will not be applied to those machines.</span></span> <span data-ttu-id="491dc-112">Le client App-V 5,1 publie des packages attribués à un compte d’ordinateur de manière globale.</span><span class="sxs-lookup"><span data-stu-id="491dc-112">The App-V 5.1 Client will publish packages assigned to a machine account globally.</span></span> <span data-ttu-id="491dc-113">Toutefois, il stocke les fichiers de configuration personnalisés par utilisateur dans le profil de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="491dc-113">However, it stores custom configuration files per user in each user’s profile.</span></span> <span data-ttu-id="491dc-114">Les packages publiés globalement n’ont pas accès à cette configuration personnalisée.</span><span class="sxs-lookup"><span data-stu-id="491dc-114">Globally published packages will not have access to this custom configuration.</span></span>

<span data-ttu-id="491dc-115">**Solution de contournement**: effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="491dc-115">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="491dc-116">Attribuez le package à des groupes contenant uniquement des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="491dc-116">Assign the package to groups containing only user accounts.</span></span> <span data-ttu-id="491dc-117">Cela permet de s’assurer que la configuration personnalisée du package sera stockée dans le profil de chaque utilisateur et sera appliquée correctement.</span><span class="sxs-lookup"><span data-stu-id="491dc-117">This will ensure that the package’s custom configuration will be stored in each user’s profile and will be applied correctly.</span></span>

-   <span data-ttu-id="491dc-118">Créez un fichier de configuration de déploiement personnalisé et appliquez-le au package sur le client à l’aide de l’applet de demande Add-AppvClientPackage avec le paramètre – DynamicDeploymentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="491dc-118">Create a custom deployment configuration file and apply it to the package on the client using the Add-AppvClientPackage cmdlet with the –DynamicDeploymentConfiguration parameter.</span></span> <span data-ttu-id="491dc-119">Pour plus d’informations, voir [à propos de la configuration dynamique de App-V 5,1](about-app-v-51-dynamic-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="491dc-119">See [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md) for more information.</span></span>

-   <span data-ttu-id="491dc-120">Créez un package avec la configuration personnalisée à l’aide du séquenceur App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="491dc-120">Create a new package with the custom configuration using the App-V 5.1 Sequencer.</span></span>

## <span data-ttu-id="491dc-121">Fichiers du serveur non supprimés après l’installation de New App-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="491dc-121">Server files not deleted after new App-V 5.1 Server installation</span></span>


<span data-ttu-id="491dc-122">Si vous désinstallez le serveur App-V 5,0 SP1, puis installez le serveur App-V 5,1, l’installation échoue, la mauvaise version du serveur de gestion est installée et un message d’erreur est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="491dc-122">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.1 Server, the installation fails, the wrong version of the Management server is installed, and an error message is returned.</span></span> <span data-ttu-id="491dc-123">Le problème se produit parce que les fichiers serveur ne sont pas supprimés lorsque vous désinstallez App-V 5,0 SP1, de sorte que le processus d’installation effectue une mise à niveau au lieu d’une nouvelle installation.</span><span class="sxs-lookup"><span data-stu-id="491dc-123">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the installation process does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="491dc-124">**Solution de contournement**: supprimez cette clé de Registre avant de commencer à installer App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="491dc-124">**Workaround**: Delete this registry key before you start installing App-V 5.1:</span></span>

<span data-ttu-id="491dc-125">Sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, recherchez et supprimez la clé du GUID d’installation contenant la valeur DWORD «DisplayName» avec les données de valeur «Microsoft Application Virtualization (App-V) Server».</span><span class="sxs-lookup"><span data-stu-id="491dc-125">Under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, locate and delete the installation GUID key that contains the DWORD value "DisplayName" with value data "Microsoft Application Virtualization (App-V) Server".</span></span> <span data-ttu-id="491dc-126">Il s’agit de la seule touche qui doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="491dc-126">This is the only key that should be deleted.</span></span>

## <span data-ttu-id="491dc-127">Les associations de types de fichiers ajoutées manuellement ne sont pas enregistrées correctement</span><span class="sxs-lookup"><span data-stu-id="491dc-127">File type associations added manually are not saved correctly</span></span>


<span data-ttu-id="491dc-128">Les associations de types de fichiers ajoutées à un package d’application manuellement à l’aide de l’onglet raccourcis et FTAs à la fin de l’Assistant Mise à niveau de l’application ne sont pas enregistrées correctement.</span><span class="sxs-lookup"><span data-stu-id="491dc-128">File type associations added to an application package manually using the Shortcuts and FTAs tab at the end of the application upgrade wizard are not saved correctly.</span></span> <span data-ttu-id="491dc-129">Ils ne seront pas disponibles pour le client App-V ou pour le Sequencer lors de la mise à jour du package enregistré.</span><span class="sxs-lookup"><span data-stu-id="491dc-129">They will not be available to the App-V Client or to the Sequencer when updating the saved package again.</span></span>

<span data-ttu-id="491dc-130">**Solution de contournement**: pour ajouter une association de type de fichier, ouvrez le package à des fins de modification, puis exécutez l’Assistant Mise à jour.</span><span class="sxs-lookup"><span data-stu-id="491dc-130">**Workaround**: To add a file type association, open the package for modification and run the update wizard.</span></span> <span data-ttu-id="491dc-131">Lors de l’étape d’installation, ajoutez la nouvelle association de type de fichier par le biais du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="491dc-131">During the Installation step, add the new file type association through the operating system.</span></span> <span data-ttu-id="491dc-132">Le Sequencer détecte la nouvelle association dans le registre système et l’ajoute au registre virtuel du package, là où il sera disponible pour le client.</span><span class="sxs-lookup"><span data-stu-id="491dc-132">The sequencer will detect the new association in the system registry and add it to the package’s virtual registry, where it will be available to the client.</span></span>

## <span data-ttu-id="491dc-133">Lorsque vous diffusez des packages en continu en mode de stockage de contenu partagé dans un client géré par AppLocker, des données supplémentaires sont écrites sur le disque local.</span><span class="sxs-lookup"><span data-stu-id="491dc-133">When streaming packages in Shared Content Store (SCS) mode to a client that is also managed with AppLocker, additional data is written to the local disk.</span></span>


<span data-ttu-id="491dc-134">Pour réduire la quantité de données écrites sur le disque local du client, vous pouvez activer le mode SCS sur le client App-V 5,1 pour diffuser le contenu d’un package à la demande.</span><span class="sxs-lookup"><span data-stu-id="491dc-134">To decrease the amount of data written to a client’s local disk, you can enable SCS mode on the App-V 5.1 Client to stream the contents of a package on demand.</span></span> <span data-ttu-id="491dc-135">Toutefois, si AppLocker gère une application au sein du package, il est possible que certaines données soient écrites sur le disque local du client qui ne serait pas écrit autrement.</span><span class="sxs-lookup"><span data-stu-id="491dc-135">However, if AppLocker manages an application within the package, some data might be written to the client’s local disk that would not otherwise be written.</span></span>

<span data-ttu-id="491dc-136">**Solution de contournement**: aucune</span><span class="sxs-lookup"><span data-stu-id="491dc-136">**Workaround**: None</span></span>

## <span data-ttu-id="491dc-137">Dans la boîte de dialogue Ajouter un package de la console de gestion, le bouton Parcourir n’est pas disponible lorsque vous utilisez Chrome ou Firefox</span><span class="sxs-lookup"><span data-stu-id="491dc-137">In the Management Console Add Package dialog box, the Browse button is not available when using Chrome or Firefox</span></span>


<span data-ttu-id="491dc-138">Sur la page packages de la console de gestion, si vous cliquez sur **Ajouter ou mettre à niveau** dans le coin inférieur droit, la boîte de dialogue **Ajouter un package** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="491dc-138">On the Packages page of the Management Console, if you click **Add or Upgrade** in the lower-right corner, the **Add Package** dialog box appears.</span></span> <span data-ttu-id="491dc-139">Si vous accédez à la console de gestion en utilisant chrome ou Firefox comme navigateur, vous ne pourrez pas accéder à l’emplacement du package.</span><span class="sxs-lookup"><span data-stu-id="491dc-139">If you are accessing the Management Console using Chrome or Firefox as your browser, you will not be able to browse to the location of the package.</span></span>

<span data-ttu-id="491dc-140">**Solution de contournement**: tapez ou copiez-collez le chemin d’accès du package dans le champ d’entrée **Ajouter le package** .</span><span class="sxs-lookup"><span data-stu-id="491dc-140">**Workaround**: Type or copy and paste the path to the package into the **Add Package** input field.</span></span> <span data-ttu-id="491dc-141">Si la console de gestion a accès à ce chemin d’accès, vous serez en mesure d’ajouter le package.</span><span class="sxs-lookup"><span data-stu-id="491dc-141">If the Management Console has access to this path, you will be able to add the package.</span></span> <span data-ttu-id="491dc-142">Si le package se trouve sur un partage réseau, vous pouvez accéder à l’emplacement à l’aide de l’Explorateur de fichiers en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="491dc-142">If the package is on a network share, you can browse to the location using File Explorer by doing these steps:</span></span>

1.  <span data-ttu-id="491dc-143">En appuyant sur **MAJ**, cliquez avec le bouton droit sur le fichier de package.</span><span class="sxs-lookup"><span data-stu-id="491dc-143">While pressing **Shift**, right-click on the package file</span></span>

2.  <span data-ttu-id="491dc-144">Sélectionnez **Copy As Path**</span><span class="sxs-lookup"><span data-stu-id="491dc-144">Select **Copy as path**</span></span>

3.  <span data-ttu-id="491dc-145">Collez le chemin d’accès dans le champ de saisie de la boîte de dialogue **Ajouter un package** .</span><span class="sxs-lookup"><span data-stu-id="491dc-145">Paste the path into the **Add Package** dialog box input field</span></span>

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a><span data-ttu-id="491dc-146">La mise à niveau d’App-V Management Server vers 5,1 échoue parfois avec le message «une erreur de base de données s’est produite»</span><span class="sxs-lookup"><span data-stu-id="491dc-146">Upgrading App-V Management Server to 5.1 sometimes fails with the message “A database error occurred”</span></span>


<span data-ttu-id="491dc-147">Si vous installez le serveur de gestion App-V 5,0 SP1 et que vous essayez d’effectuer une mise à niveau vers la version Server App-V 5,1 lorsque plusieurs groupes de connexion sont configurés et activés, l’erreur suivante s’affiche: «une erreur de base de données s’est produite.</span><span class="sxs-lookup"><span data-stu-id="491dc-147">If you install the App-V 5.0 SP1 Management Server, and then try to upgrade to App-V 5.1 Server when multiple connection groups are configured and enabled, the following error is displayed: “A database error occurred.</span></span> <span data-ttu-id="491dc-148">Raison: «nom de colonne non valide» «PackageOptional».</span><span class="sxs-lookup"><span data-stu-id="491dc-148">Reason: 'Invalid column name 'PackageOptional'.</span></span> <span data-ttu-id="491dc-149">Nom de colonne non valide «VersionOptional».</span><span class="sxs-lookup"><span data-stu-id="491dc-149">Invalid column name 'VersionOptional'.”</span></span>

<span data-ttu-id="491dc-150">**Solution**: exécutez la commande suivante sur votre base de données SQL:</span><span class="sxs-lookup"><span data-stu-id="491dc-150">**Workaround**: Run this command on your SQL database:</span></span>

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

<span data-ttu-id="491dc-151">où «AppVManagement» est le nom de la base de données.</span><span class="sxs-lookup"><span data-stu-id="491dc-151">where “AppVManagement” is the name of the database.</span></span>

## <span data-ttu-id="491dc-152">Les utilisateurs ne peuvent pas ouvrir un package dans un groupe de connexions publié par un utilisateur si vous ajoutez ou supprimez un package facultatif</span><span class="sxs-lookup"><span data-stu-id="491dc-152">Users cannot open a package in a user-published connection group if you add or remove an optional package</span></span>


<span data-ttu-id="491dc-153">Dans les environnements qui exécutent le client RDS ou qui ont plusieurs utilisateurs simultanés par ordinateur, les utilisateurs connectés ne peuvent pas ouvrir les applications dans les packages d’un groupe de connexion publié par l’utilisateur si un package facultatif est ajouté ou supprimé du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="491dc-153">In environments that are running the RDS Client or that have multiple concurrent users per computer, logged-in users cannot open applications in packages that are in a user-published connection group if an optional package is added to or removed from the connection group.</span></span>

<span data-ttu-id="491dc-154">**Solution**: Demandez aux utilisateurs de se déconnecter, puis de vous reconnecter.</span><span class="sxs-lookup"><span data-stu-id="491dc-154">**Workaround**: Have users log out and then log back in.</span></span>

## <span data-ttu-id="491dc-155">Le message d’erreur s’affiche par erreur lorsque le groupe de connexions est uniquement publié pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="491dc-155">Error message is erroneously displayed when the connection group is published only to the user</span></span>


<span data-ttu-id="491dc-156">Lorsque vous exécutez l’outil de réparation-AppvClientConnectionGroup, l’erreur suivante s’affiche, même lorsque le groupe de connexions est publié uniquement à l’utilisateur: «erreur d’intégration d’application interne-V: package non intégré pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="491dc-156">When you run Repair-AppvClientConnectionGroup, the following error is displayed, even when the connection group is published only to the user: “Internal App-V Integration error: Package not integrated for the user.</span></span> <span data-ttu-id="491dc-157">Vérifiez que le package est ajouté à l’ordinateur et publié sur l’utilisateur.»</span><span class="sxs-lookup"><span data-stu-id="491dc-157">Please ensure that the package is added to the machine and published to the user.”</span></span>

<span data-ttu-id="491dc-158">**Solution de contournement**: effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="491dc-158">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="491dc-159">Publiez tous les packages d’un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="491dc-159">Publish all packages in a connection group.</span></span>

    <span data-ttu-id="491dc-160">Ce problème survient lorsque le groupe de connexion en cours de réparation comporte des packages qui sont manquants ou ne sont pas disponibles pour l’utilisateur (autrement dit, non publié globalement ou pour l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="491dc-160">The problem arises when the connection group being repaired has packages that are missing or not available to the user (that is, not published globally or to the user).</span></span> <span data-ttu-id="491dc-161">Toutefois, la réparation fonctionnera si tous les packages du groupe de connexions sont disponibles, vérifiez donc que tous les packages sont publiés.</span><span class="sxs-lookup"><span data-stu-id="491dc-161">However, the repair will work if all of the connection group’s packages are available, so ensure that all packages are published.</span></span>

-   <span data-ttu-id="491dc-162">Réparez les packages individuellement à l’aide de la commande réparer-AppvClientPackage plutôt que de la commande réparer-AppvClientConnectionGroup.</span><span class="sxs-lookup"><span data-stu-id="491dc-162">Repair packages individually using the Repair-AppvClientPackage command rather than the Repair-AppvClientConnectionGroup command.</span></span>

    <span data-ttu-id="491dc-163">Déterminez les packages disponibles pour les utilisateurs, puis exécutez la commande réparer-AppvClientPackage une fois pour chaque package.</span><span class="sxs-lookup"><span data-stu-id="491dc-163">Determine which packages are available to users and then run the Repair-AppvClientPackage command once for each package.</span></span> <span data-ttu-id="491dc-164">Utilisez les cmdlets PowerShell pour effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="491dc-164">Use PowerShell cmdlets to do the following:</span></span>

    1.  <span data-ttu-id="491dc-165">Obtenez tous les packages d’un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="491dc-165">Get all the packages in a connection group.</span></span>

    2.  <span data-ttu-id="491dc-166">Vérifiez si chaque package est actuellement publié.</span><span class="sxs-lookup"><span data-stu-id="491dc-166">Check to see if each package is currently published.</span></span>

    3.  <span data-ttu-id="491dc-167">Si le package est actuellement publié, exécutez réparation-AppvClientPackage sur ce package.</span><span class="sxs-lookup"><span data-stu-id="491dc-167">If the package is currently published, run Repair-AppvClientPackage on that package.</span></span>

## <span data-ttu-id="491dc-168">Les icônes ne s’affichent pas correctement dans le Sequencer</span><span class="sxs-lookup"><span data-stu-id="491dc-168">Icons not displayed properly in Sequencer</span></span>


<span data-ttu-id="491dc-169">Les icônes de l’onglet raccourcis et des types de fichiers ne s’affichent pas correctement lors de la modification d’un package dans le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="491dc-169">Icons in the Shortcuts and File Type Associations tab are not displayed correctly when modifying a package in the App-V Sequencer.</span></span> <span data-ttu-id="491dc-170">Ce problème survient lorsque la taille des icônes n’est pas 16x16 ou 32x32.</span><span class="sxs-lookup"><span data-stu-id="491dc-170">This problem occurs when the size of the icons are not 16x16 or 32x32.</span></span>

<span data-ttu-id="491dc-171">**Solution**: Utilisez uniquement des icônes de 16x16 ou 32x32.</span><span class="sxs-lookup"><span data-stu-id="491dc-171">**Workaround**: Only use icons that are 16x16 or 32x32.</span></span>

## <span data-ttu-id="491dc-172">Le script InsertVersionInfo. SQL n’est plus requis pour la base de données de gestion</span><span class="sxs-lookup"><span data-stu-id="491dc-172">InsertVersionInfo.sql script no longer required for the Management Database</span></span>


<span data-ttu-id="491dc-173">Le script InsertVersionInfo. SQL n’est pas requis pour les versions de la base de données de gestion App-V ultérieure à l’application-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="491dc-173">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="491dc-174">Le script Permissions. SQL doit être mis à jour en suivant l' **étape 2** de [l’article 3031340](https://support.microsoft.com/kb/3031340)de la base de connaissances.</span><span class="sxs-lookup"><span data-stu-id="491dc-174">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span>

<span data-ttu-id="491dc-175">**Important** 
 L' **étape 1** n’est pas requise pour les versions de App-v ultérieures à l’application-v 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="491dc-175">**Important**
**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

 

## <span data-ttu-id="491dc-176">Microsoft Visual Studio 2012 non pris en charge</span><span class="sxs-lookup"><span data-stu-id="491dc-176">Microsoft Visual Studio 2012 not supported</span></span>


<span data-ttu-id="491dc-177">App-V 5,1 ne prend pas en charge Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="491dc-177">App-V 5.1 does not support Visual Studio 2012.</span></span>

<span data-ttu-id="491dc-178">**Solution de contournement**: aucune</span><span class="sxs-lookup"><span data-stu-id="491dc-178">**Workaround**: None</span></span>

## <span data-ttu-id="491dc-179">Restrictions de nom de fichier d’application pour le Sequencer App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="491dc-179">Application filename restrictions for App-V 5.x Sequencer</span></span>


<span data-ttu-id="491dc-180">Le Sequencer App-V 5. x ne peut pas séquencer des applications avec des noms de fichier correspondant à «CO_ &lt; x &gt; », où x est une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="491dc-180">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="491dc-181">Le 0x8007139F d’erreur est généré.</span><span class="sxs-lookup"><span data-stu-id="491dc-181">Error 0x8007139F will be generated.</span></span>

<span data-ttu-id="491dc-182">**Solution**: utilisez un autre nom de fichier</span><span class="sxs-lookup"><span data-stu-id="491dc-182">**Workaround**: Use a different filename</span></span>

## <span data-ttu-id="491dc-183">Erreur «fichier introuvable» intermittente lors du montage d’un package</span><span class="sxs-lookup"><span data-stu-id="491dc-183">Intermittent "File Not Found" error when Mounting a Package</span></span>


<span data-ttu-id="491dc-184">Occasionnellement lors du montage d’un package, une erreur «fichier introuvable» (0x80070002) est générée.</span><span class="sxs-lookup"><span data-stu-id="491dc-184">Occasionally when mounting a package, a "File Not Found" (0x80070002) error is generated.</span></span> <span data-ttu-id="491dc-185">En règle générale, ce problème se produit lorsqu’un dossier d’un package App-V contient un grand nombre de fichiers (c’est-à-dire 20 Ko ou plus).</span><span class="sxs-lookup"><span data-stu-id="491dc-185">Typically, this occurs when a folder in an App-V package contains many files ( i.e. 20K or more).</span></span> <span data-ttu-id="491dc-186">Cela peut entraîner un délai de diffusion plus long que prévu et un délai d’expiration qui génère l’erreur «fichier introuvable».</span><span class="sxs-lookup"><span data-stu-id="491dc-186">This can cause streaming to take longer than expected and to time out which generates the "File Not Found" error.</span></span>

<span data-ttu-id="491dc-187">**Solution de contournement**: à partir de HF06, une nouvelle clé de registre a été ajoutée pour permettre l’extension de ce délai.</span><span class="sxs-lookup"><span data-stu-id="491dc-187">**Workaround**: Starting with HF06, a new registry key has been introduced to enable extending this time-out period.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left"><span data-ttu-id="491dc-188">Chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="491dc-188">Path</span></span></td>
<td align="left"><span data-ttu-id="491dc-189">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</span><span class="sxs-lookup"><span data-stu-id="491dc-189">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Streaming</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="491dc-190">Paramètre</span><span class="sxs-lookup"><span data-stu-id="491dc-190">Setting</span></span></td>
<td align="left"><span data-ttu-id="491dc-191">StreamResponseWaitTimeout</span><span class="sxs-lookup"><span data-stu-id="491dc-191">StreamResponseWaitTimeout</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="491dc-192">Smalldatetime</span><span class="sxs-lookup"><span data-stu-id="491dc-192">DataType</span></span></td>
<td align="left"><span data-ttu-id="491dc-193">DWORD</span><span class="sxs-lookup"><span data-stu-id="491dc-193">DWORD</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="491dc-194">UnitsIn</span><span class="sxs-lookup"><span data-stu-id="491dc-194">Units</span></span></td>
<td align="left"><span data-ttu-id="491dc-195">Lesquelles</span><span class="sxs-lookup"><span data-stu-id="491dc-195">Seconds</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="491dc-196">Par défaut</span><span class="sxs-lookup"><span data-stu-id="491dc-196">Default</span></span></td>
<td align="left"><span data-ttu-id="491dc-197">n°5</span><span class="sxs-lookup"><span data-stu-id="491dc-197">5</span></span><br />
<strong><span data-ttu-id="491dc-198">Remarque </strong> : cette valeur est la valeur par défaut si la clé de Registre n’est pas définie ou si une valeur &lt; = 5 est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="491dc-198">Note</strong>: this value is the default if the registry key is not defined or a value &lt;=5 is specified.</span></span>
</td>
</tr>
</tbody>
</table>






## <span data-ttu-id="491dc-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="491dc-199">Related topics</span></span>


[<span data-ttu-id="491dc-200">À propos d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="491dc-200">About App-V 5.1</span></span>](about-app-v-51.md)

 

 






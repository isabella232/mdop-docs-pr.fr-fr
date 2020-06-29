---
title: Notes de publication pour App-V5.0 SP2
description: Notes de publication pour App-V5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804896"
---
# <span data-ttu-id="0adae-103">Notes de publication pour App-V5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="0adae-103">Release Notes for App-V 5.0 SP2</span></span>


**<span data-ttu-id="0adae-104">Pour rechercher un problème spécifique dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="0adae-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="0adae-105">Lisez soigneusement ces notes de publication avant d’installer App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="0adae-105">Read these release notes thoroughly before you install App-V 5.0 SP2.</span></span>

<span data-ttu-id="0adae-106">Ces notes de publication contiennent des informations nécessaires pour l’installation de l’application-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="0adae-106">These release notes contain information that is required to successfully install App-V 5.0 SP2.</span></span> <span data-ttu-id="0adae-107">Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="0adae-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="0adae-108">S’il existe des différences entre ces notes de publication et d’autres documents App-V 5,0, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="0adae-108">If there are differences between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="0adae-109">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="0adae-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="0adae-110">À propos de la documentation relative aux produits</span><span class="sxs-lookup"><span data-stu-id="0adae-110">About the Product Documentation</span></span>


<span data-ttu-id="0adae-111">Pour plus d’informations sur la documentation App-V 5,0, consultez la page d’accueil App-V 5,0 sur Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="0adae-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="0adae-112">Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="0adae-112">Provide Feedback</span></span>


<span data-ttu-id="0adae-113">Vos commentaires vous intéressent sur App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0adae-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="0adae-114">Vous pouvez envoyer vos commentaires à <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="0adae-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="0adae-115">**Remarques**  Cette adresse de messagerie n’est pas un canal de support, mais vos commentaires nous aideront à planifier des changements ultérieurs dans la documentation et les versions de nos produits.</span><span class="sxs-lookup"><span data-stu-id="0adae-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="0adae-116">Pour obtenir les informations les plus récentes sur MDOP et les ressources de formation supplémentaires, voir la page d' [utilisation de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="0adae-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="0adae-117">Pour en savoir plus sur les nouvelles mises à jour ou pour nous faire part de vos commentaires, suivez-nous sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="0adae-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="0adae-118">Problèmes connus avec le correctif logiciel 4 pour la virtualisation des applications 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0adae-118">Known Issues with Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>


### <span data-ttu-id="0adae-119">Les packages cessent de fonctionner après la désinstallation du package Hotfix 4 pour l’application virtualisation 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0adae-119">Packages stop working after you uninstall Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>

<span data-ttu-id="0adae-120">Packages publiés lorsque le correctif logiciel 4 pour l’application virtualisation du SP2 pour applications 5,0 SP2 ne fonctionne plus lorsque le correctif logiciel 4 pour l’application virtualisation 5,0 SP2 est supprimé.</span><span class="sxs-lookup"><span data-stu-id="0adae-120">Packages published when Hotfix Package 4 for Application Virtualization 5.0 SP2 is applied stop working when Hotfix Package 4 for Application Virtualization 5.0 SP2 is removed.</span></span>

<span data-ttu-id="0adae-121">MOYENS</span><span class="sxs-lookup"><span data-stu-id="0adae-121">WORKAROUND:</span></span>

<span data-ttu-id="0adae-122">Si le dossier suivant existe, vous devez le supprimer:</span><span class="sxs-lookup"><span data-stu-id="0adae-122">If the following folder exists, then you must delete it:</span></span>

<span data-ttu-id="0adae-123">**% LocalAppData%**  \\  **Microsoft**  \\  **AppV**  \\  **Client**  \\  **VFS**  \\  \*\* &lt; ID &gt; de package\*\* de chaque package publié.</span><span class="sxs-lookup"><span data-stu-id="0adae-123">**%localappdata%** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **VFS** \\ **&lt;package ID&gt;** for each package that was published.</span></span>

<span data-ttu-id="0adae-124">**Remarques**  Vous devez disposer de privilèges élevés pour supprimer ce dossier.</span><span class="sxs-lookup"><span data-stu-id="0adae-124">**Note** You must have elevated privileges to delete this folder.</span></span>

 

<span data-ttu-id="0adae-125">Pour utiliser un script, pour chaque compte d’utilisateur sur l’ordinateur et pour chaque ID de package publié après l’installation du package de correctif 4 pour l’application virtualisation de l’application 5,0 SP2:</span><span class="sxs-lookup"><span data-stu-id="0adae-125">To use a script, for each user account on the computer and for each package id that was published after installing Hotfix Package 4 for Application Virtualization 5.0 SP2:</span></span>

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   <span data-ttu-id="0adae-126">Le raccourci reste avec les sessions utilisateur même après la suppression du dossier du répertoire de la section précédente, de sorte que vous pouvez cliquer sur le raccourci pour exécuter de nouveau l’application.</span><span class="sxs-lookup"><span data-stu-id="0adae-126">The shortcuts will remain with the user sessions even after deleting the folder from the directory in the previous section, so you can click on the shortcut to run the application again.</span></span> <span data-ttu-id="0adae-127">Il n’est pas nécessaire de republier l’application.</span><span class="sxs-lookup"><span data-stu-id="0adae-127">There is no need to re-publish the application.</span></span>

-   <span data-ttu-id="0adae-128">Ce problème survient pour l’utilisateur ayant publié des packages empaquetés et publiés globalement par exemple, Microsoft Centre.</span><span class="sxs-lookup"><span data-stu-id="0adae-128">This issue happens for both user published packaged and globally published packages for example, Microsoft Office2013.</span></span> <span data-ttu-id="0adae-129">Le dossier doit être supprimé pour les deux types de packages.</span><span class="sxs-lookup"><span data-stu-id="0adae-129">The folder must be deleted for both types of packages.</span></span>

-   <span data-ttu-id="0adae-130">Vous n’avez pas besoin de supprimer le dossier VFS dans les données d’application itinérantes (**% AppData%**).</span><span class="sxs-lookup"><span data-stu-id="0adae-130">You do not need to delete the VFS folder in the Roaming app data (**%appdata%**).</span></span> <span data-ttu-id="0adae-131">Seule la **% LocalAppData%** doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="0adae-131">Only the **%localappdata%** must be deleted.</span></span>

### <span data-ttu-id="0adae-132">Emplacement du système de fichiers Microsoft Office incorrect</span><span class="sxs-lookup"><span data-stu-id="0adae-132">Microsoft Office integration points to wrong file system location</span></span>

<span data-ttu-id="0adae-133">Les points d’intégration de Microsoft Office au mauvais emplacement du système de fichiers (Groove.exe message d’erreur).</span><span class="sxs-lookup"><span data-stu-id="0adae-133">Microsoft Office integration points to wrong file system location (Groove.exe error message).</span></span>

<span data-ttu-id="0adae-134">MOYENS</span><span class="sxs-lookup"><span data-stu-id="0adae-134">WORKAROUND:</span></span>

<span data-ttu-id="0adae-135">Appliquez l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="0adae-135">Use one of the following methods:</span></span>

1.  <span data-ttu-id="0adae-136">Supprimez le raccourci dans le dossier démarrage après la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="0adae-136">Delete the shortcut in the start-up folder after upgrade.</span></span>

2.  <span data-ttu-id="0adae-137">Modifiez le raccourci dans le dossier de démarrage à l’aide d’un script.</span><span class="sxs-lookup"><span data-stu-id="0adae-137">Change the shortcut in the start-up folder using a script.</span></span>

3.  <span data-ttu-id="0adae-138">Utilisez le fichier de configuration de déploiement pour spécifier le raccourci cible à la racine d’intégration.</span><span class="sxs-lookup"><span data-stu-id="0adae-138">Use the deployment configuration file to specify the shortcut target to the integration root.</span></span>

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> <span data-ttu-id="0adae-139">Le correctif logiciel 4 pour l’application virtualisation du programme d’installation de l’application 5,0 SP2 peut prendre un certain temps</span><span class="sxs-lookup"><span data-stu-id="0adae-139">Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can take a long time</span></span>

<span data-ttu-id="0adae-140">Le correctif logiciel 4 pour l’application virtualisation du programme d’installation de l’application 5,0 SP2 peut prendre un certain temps en fonction du nombre de fichiers stockés dans le cache de package existant.</span><span class="sxs-lookup"><span data-stu-id="0adae-140">The Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can potentially take a long time depending on how many files are stored in the existing package cache.</span></span>

<span data-ttu-id="0adae-141">La mise à jour des descripteurs de sécurité du package associés lors de l’installation du correctif logiciel 4 pour l’installation d’application de la virtualisation du SP2 5,0 a un impact significatif sur le temps nécessaire à l’installation.</span><span class="sxs-lookup"><span data-stu-id="0adae-141">Updating associated package security descriptors during the Hotfix Package 4 for Application Virtualization 5.0 SP2 installation has a significant impact on how long it takes the installation will take.</span></span> <span data-ttu-id="0adae-142">Auparavant, l’installation était standard dans la durée.</span><span class="sxs-lookup"><span data-stu-id="0adae-142">Previously, the installation install was standard in duration.</span></span> <span data-ttu-id="0adae-143">Toutefois, elle dépend désormais du nombre de fichiers que vous avez intermédiaires dans le cache du package.</span><span class="sxs-lookup"><span data-stu-id="0adae-143">However, it now depends on how many files you have staged in the package cache.</span></span>

<span data-ttu-id="0adae-144">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="0adae-144">WORKAROUND: None</span></span>

### <span data-ttu-id="0adae-145">La désinstallation du package de correctif 4 pour l’application virtualisation du SP2 5,0 échoue si le package JIT-V est en cours d’utilisation</span><span class="sxs-lookup"><span data-stu-id="0adae-145">Uninstalling Hotfix Package 4 for Application Virtualization 5.0 SP2 fails if JIT-V package is in use</span></span>

<span data-ttu-id="0adae-146">Si vous installez le package de correctif logiciel 4 pour la virtualisation des applications 5,0 SP2 et que vous essayez de désinstaller le correctif lorsque la virtualisation juste-à-V est utilisée, l’opération échoue si toutes les conditions suivantes sont remplies:</span><span class="sxs-lookup"><span data-stu-id="0adae-146">If you install Hotfix Package 4 for Application Virtualization 5.0 SP2 and then try to uninstall the hotfix when just-in-time virtualization (JIT-V) is being used, the operation will fail if all of the following conditions are true:</span></span>

-   <span data-ttu-id="0adae-147">Vous avez installé l’application à l’aide d’un fichier Windows Installer (. msi), puis vous appliquez les mises à jour à l’aide d’un fichier de correctif Microsoft Installer (. msp).</span><span class="sxs-lookup"><span data-stu-id="0adae-147">You installed by using a Windows Installer file (.msi), and then you apply updates by using a Microsoft Installer Patch File (.msp).</span></span>

-   <span data-ttu-id="0adae-148">Vous essayez de désinstaller une mise à jour à l’aide de l’option Ajout/suppression de programmes du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="0adae-148">You try to uninstall an update by using the Add or Remove Programs item in Control Panel.</span></span>

-   <span data-ttu-id="0adae-149">Un package prenant en charge la fonction JIT est en cours d’exécution sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0adae-149">A JIT-V-enabled package is running on the computer.</span></span>

<span data-ttu-id="0adae-150">Solution de contournement: procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="0adae-150">WORKAROUND: Complete the following steps:</span></span>

1.  <span data-ttu-id="0adae-151">Ouvrez Windows PowerShell et exécutez les commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="0adae-151">Open Windows PowerShell and run the following commands:</span></span>

    -   **<span data-ttu-id="0adae-152">Importation-module appvclient</span><span class="sxs-lookup"><span data-stu-id="0adae-152">Import-module appvclient</span></span>**

    -   **<span data-ttu-id="0adae-153">Get-AppvClientPackage | Stop-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="0adae-153">Get-AppvClientPackage | Stop-AppvClientPackage</span></span>**

2.  <span data-ttu-id="0adae-154">Désinstaller la mise à jour à l’aide d’ajout/suppression de programmes.</span><span class="sxs-lookup"><span data-stu-id="0adae-154">Uninstall the update using Add or Remove Programs.</span></span>

## <span data-ttu-id="0adae-155">Problèmes connus avec App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0adae-155">Known Issues with App-V 5.0 SP2</span></span>


### <a href="" id="bkmk-folderredirection"></a><span data-ttu-id="0adae-156">La redirection de dossiers d’applications-V ne peut pas déplacer les fichiers de% AppData% vers% LocalAppData%</span><span class="sxs-lookup"><span data-stu-id="0adae-156">App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%</span></span>

<span data-ttu-id="0adae-157">Lorsque% AppData% est un dossier réseau partagé que vous avez configuré pour la redirection de dossiers, les modifications que les utilisateurs finaux effectuent sur AppData (itinérance) peuvent être perdues lors du changement d’ordinateur ou de l’effacement de leur AppData Local lors de la déconnexion, puis de connexion.</span><span class="sxs-lookup"><span data-stu-id="0adae-157">When %AppData% is a shared network folder that you have configured for folder redirection, the changes that end users make to AppData (Roaming) can be lost when they switch computers or when their local AppData is cleared when they log off and then log back on.</span></span> <span data-ttu-id="0adae-158">Cette erreur se produit, car la clé de Registre (AppDataTime), qui indique le dernier chargement connu, est hors de la synchronisation avec le AppData mis en cache local.</span><span class="sxs-lookup"><span data-stu-id="0adae-158">This error occurs because the registry key (AppDataTime), which indicates the last known upload, gets out of synchronization with the local cached AppData.</span></span>

<span data-ttu-id="0adae-159">Solution de contournement: supprimez manuellement la clé de Registre suivante pour chaque package approprié lors de la connexion ou de la déconnexion d’un utilisateur final:</span><span class="sxs-lookup"><span data-stu-id="0adae-159">WORKAROUND: Manually delete the following registry key for each relevant package when an end user logs on or off:</span></span>

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

<span data-ttu-id="0adae-160">La première fois que les utilisateurs finaux démarrent une application dans le package après s’être connecté, App-V force le téléchargement de l’enregistrement% AppData%, même si% LocalAppData% est déjà à jour.</span><span class="sxs-lookup"><span data-stu-id="0adae-160">The first time that end users start an application in the package after they log in, App-V forces a download of the zipped %AppData%, even if %LocalAppData% is already up to date.</span></span>

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> <span data-ttu-id="0adae-161">App-V 5,0 Service Pack 2 (App-V 5,0 SP2) n’inclut pas de nouvelle version du serveur App-V</span><span class="sxs-lookup"><span data-stu-id="0adae-161">App-V 5.0 Service Pack 2 (App-V 5.0 SP2) does not include a new version of the App-V Server</span></span>

<span data-ttu-id="0adae-162">App-V 5.0 SP2 n’inclut pas de nouvelle version du serveur App-V.</span><span class="sxs-lookup"><span data-stu-id="0adae-162">App-V 5.0SP2 does not include a new version of the App-V Server.</span></span> <span data-ttu-id="0adae-163">Si vous déployez des clients App-V 5,0 SP2 exécutant Windows 8,1 dans votre environnement et que vous envisagez de gérer les clients à l’aide de l’infrastructure App-V, vous devez installer le [package Hotfix 2 pour Microsoft application virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634).</span><span class="sxs-lookup"><span data-stu-id="0adae-163">If you deploy App-V 5.0 SP2 clients running Windows 8.1 in your environment and plan to manage the clients using the App-V infrastructure, you must install [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634).</span></span> <span data-ttu-id="0adae-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span><span class="sxs-lookup"><span data-stu-id="0adae-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span></span>

<span data-ttu-id="0adae-165">Si vous exécutez et gérez des clients App-V 5,0 SP2 en utilisant l’une des méthodes suivantes, aucune mise à jour de client n’est requise:</span><span class="sxs-lookup"><span data-stu-id="0adae-165">If you are running and managing App-V 5.0 SP2 clients using any of the following methods no client update is required:</span></span>

-   <span data-ttu-id="0adae-166">Mode autonome.</span><span class="sxs-lookup"><span data-stu-id="0adae-166">Standalone mode.</span></span>

-   <span data-ttu-id="0adae-167">Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0adae-167">Configuration Manager.</span></span>

-   <span data-ttu-id="0adae-168">Des ESD tiers.</span><span class="sxs-lookup"><span data-stu-id="0adae-168">Third party ESD.</span></span>

<span data-ttu-id="0adae-169">Le client App-V 5,0 SP2 est entièrement compatible avec Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="0adae-169">The App-V 5.0 SP2 client is fully compatible with Windows 8.1</span></span>

<span data-ttu-id="0adae-170">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="0adae-170">WORKAROUND: None.</span></span>

## <span data-ttu-id="0adae-171">Informations de copyright des notes de publication</span><span class="sxs-lookup"><span data-stu-id="0adae-171">Release Notes Copyright Information</span></span>


<span data-ttu-id="0adae-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0adae-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="0adae-173">Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="0adae-173">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="0adae-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0adae-174">Related topics</span></span>


[<span data-ttu-id="0adae-175">À propos d'App-V5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="0adae-175">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

 

 






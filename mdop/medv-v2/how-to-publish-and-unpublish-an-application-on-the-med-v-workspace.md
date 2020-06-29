---
title: Comment publier et annuler la publication d'une application sur l'espace de travail MED-V
description: Comment publier et annuler la publication d'une application sur l'espace de travail MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812047"
---
# <span data-ttu-id="c8fc9-103">Comment publier et annuler la publication d'une application sur l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="c8fc9-103">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>


<span data-ttu-id="c8fc9-104">Même si une application est installée dans un espace de travail MED-V, vous devrez peut-être également publier l’application avant qu’elle ne soit disponible pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-104">Even though an application is installed in a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="c8fc9-105">Par défaut, la plupart des applications sont publiées au moment où elles sont installées et des raccourcis sont créés et activés.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-105">By default, most applications are published at the time that they are installed and shortcuts are created and enabled.</span></span>

<span data-ttu-id="c8fc9-106">Dans certains cas, vous souhaiterez peut-être installer des applications sur l’espace de travail MED-V sans les mettre à la disposition de l’utilisateur final, par exemple, un logiciel d’analyse antivirus.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-106">In some cases, you might want to install applications on the MED-V workspace without making them available to the end user, for example, virus-scanning software.</span></span> <span data-ttu-id="c8fc9-107">De même, il peut arriver que vous souhaitiez publier une application installée sur l’espace de travail MED-V qui n’est pas disponible pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-107">Similarly, there are occasions in which you want to publish an application that is installed on the MED-V workspace that was previously unavailable to the end user.</span></span> <span data-ttu-id="c8fc9-108">Par exemple, il se peut que vous deviez publier une application installée si l’installation n’a pas créé automatiquement de raccourci dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="c8fc9-108">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span>

<span data-ttu-id="c8fc9-109">**Important**  Si vous publiez une application qui ne prend pas en charge les chemins UNC, nous vous conseillons de mapper l’application sur un lecteur.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-109">**Important** If you publish an application that does not support UNC paths, we recommend that you map the application to a drive.</span></span>

 

<span data-ttu-id="c8fc9-110">Vous pouvez publier ou annuler la publication d’applications dans un espace de travail MED-V en effectuant l’une des tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="c8fc9-110">You can publish or unpublish applications to a deployed MED-V workspace by performing one of the following tasks:</span></span>

**<span data-ttu-id="c8fc9-111">Pour publier ou annuler la publication d’une application installée</span><span class="sxs-lookup"><span data-stu-id="c8fc9-111">To publish or unpublish an installed application</span></span>**

1.  <span data-ttu-id="c8fc9-112">Pour publier une application sur un espace de travail MED-V, copiez le raccourci de l’application dans le dossier suivant de l’ordinateur virtuel:</span><span class="sxs-lookup"><span data-stu-id="c8fc9-112">To publish an application on a deployed MED-V workspace, copy a shortcut for that application to the following folder on the virtual machine:</span></span>

    <span data-ttu-id="c8fc9-113">C:\\Documents et Settings\\All Users\\Start</span><span class="sxs-lookup"><span data-stu-id="c8fc9-113">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="c8fc9-114">Si nécessaire, utilisez une stratégie de groupe ou un système de ESD pour déployer un script qui copie le raccourci de l’application dans le dossier du menu tous les Users\\Start.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-114">If it is necessary, use Group Policy or an ESD system to deploy a script that copies the shortcut for that application to the All Users\\Start Menu folder.</span></span>

2.  <span data-ttu-id="c8fc9-115">Pour annuler la publication d’une application sur un espace de travail MED-V, supprimez le raccourci de l’application dans le dossier suivant de l’ordinateur virtuel:</span><span class="sxs-lookup"><span data-stu-id="c8fc9-115">To unpublish an application on a deployed MED-V workspace, delete the shortcut for that application from the following folder on the virtual machine:</span></span>

    <span data-ttu-id="c8fc9-116">C:\\Documents et Settings\\All Users\\Start</span><span class="sxs-lookup"><span data-stu-id="c8fc9-116">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="c8fc9-117">Si nécessaire, utilisez une stratégie de groupe ou un système ESD pour déployer un script qui supprime le raccourci de l’application dans le dossier du menu tous les Users\\Start.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-117">If it is necessary, use Group Policy or an ESD system to deploy a script that deletes the shortcut for that application from the All Users\\Start Menu folder.</span></span>

    <span data-ttu-id="c8fc9-118">**Remarques**  Souvent, le raccourci est automatiquement supprimé du menu **Démarrer** de l’ordinateur hôte lorsque vous désinstallez l’application.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-118">**Note** Frequently, the shortcut is automatically deleted from the host computer **Start** menu when you uninstall the application.</span></span> <span data-ttu-id="c8fc9-119">Toutefois, dans certains cas, par exemple pour un espace de travail MED-V configuré pour tous les utilisateurs d’un ordinateur partagé, vous devrez peut-être supprimer manuellement le raccourci dans le menu **Démarrer** après la désinstallation de l’application.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-119">However, in some cases, such as for a MED-V workspace that is configured for all users of a shared computer, you might have to manually delete the shortcut on the **Start** menu after the application is uninstalled.</span></span> <span data-ttu-id="c8fc9-120">Pour cela, il suffit de cliquer avec le bouton droit sur le raccourci et de sélectionner **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-120">The end-user can do this by right-clicking the shortcut and selecting **Delete**.</span></span>

     

<span data-ttu-id="c8fc9-121">Pour vérifier que l’application a été publiée ou annulée, vérifiez sur l’espace de travail MED-V si le raccourci correspondant est disponible ou non.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-121">To test that the application was published or unpublished, verify on the MED-V workspace whether the corresponding shortcut is available or not.</span></span>

<span data-ttu-id="c8fc9-122">**Remarques**  Les applications incluses dans Windows XP SP3 et situées dans le dossier du menu Démarrer de l’ordinateur virtuel ne sont pas automatiquement publiées sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-122">**Note** Applications that are included in Windows XP SP3 and are located in the virtual machine Start Menu folder are not automatically published to the host.</span></span> <span data-ttu-id="c8fc9-123">Ils sont contrôlés par des paramètres de Registre qui bloquent la publication automatique.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-123">They are controlled by registry settings that block automatic publishing.</span></span> <span data-ttu-id="c8fc9-124">Pour plus d’informations, voir liste d’exclusion de l' [application Windows Virtual PC](windows-virtual-pc-application-exclude-list.md).</span><span class="sxs-lookup"><span data-stu-id="c8fc9-124">For more information, see [Windows Virtual PC Application Exclude List](windows-virtual-pc-application-exclude-list.md).</span></span>

 

**<span data-ttu-id="c8fc9-125">Pour publier des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="c8fc9-125">To publish Control Panel items</span></span>**

1.  <span data-ttu-id="c8fc9-126">Créer un raccourci sur l’ordinateur virtuel où la cible est le nom de l’élément, par exemple, C:\\WINDOWS\\system32\\appwiz.cpl.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-126">Create a shortcut on the virtual machine where the target is the name of the item, such as C:\\WINDOWS\\system32\\appwiz.cpl.</span></span>

    <span data-ttu-id="c8fc9-127">Le raccourci doit être créé ou déplacé vers le dossier «%ALLUSERSPROFILE%\\Start Menu\\» ou l’un de ses sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-127">The shortcut must be either created in or moved to the "%ALLUSERSPROFILE%\\Start Menu\\" folder or one of its subfolders.</span></span>

    <span data-ttu-id="c8fc9-128">L’élément sera publié sur l’ordinateur hôte à l’emplacement correspondant dans le dossier du menu Démarrer de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-128">The item will be published to the host computer in the corresponding location in the host Start Menu folder.</span></span>

2.  <span data-ttu-id="c8fc9-129">Démarrez le raccourci de l’élément dans l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-129">Start the shortcut for the item in the host.</span></span>

<span data-ttu-id="c8fc9-130">**Attention**  Lorsque vous créez le raccourci, ne spécifiez pas% SystemRoot% \\control.exe.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-130">**Caution** When you create the shortcut, do not specify %SystemRoot%\\control.exe.</span></span> <span data-ttu-id="c8fc9-131">Cette application ne sera pas publiée, car elle figure dans les paramètres de Registre qui bloquent la publication automatique.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-131">This application will not be published because it is contained in the registry settings that block automatic publishing.</span></span>

 

**<span data-ttu-id="c8fc9-132">Comment MED-V gère la publication automatique d’applications</span><span class="sxs-lookup"><span data-stu-id="c8fc9-132">How MED-V handles automatic application publishing</span></span>**

1.  <span data-ttu-id="c8fc9-133">Lors de la publication d’applications, MED-V copie les raccourcis depuis l’ordinateur virtuel invité vers l’ordinateur hôte en essayant de faire correspondre la hiérarchie de dossiers qui existe dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-133">During application publishing, MED-V copies the shortcuts from the guest virtual machine to the host computer by trying to match the folder hierarchy that exists in the guest.</span></span> <span data-ttu-id="c8fc9-134">En procédant ainsi, MED-V copie le raccourci de l’invité vers l’hôte en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="c8fc9-134">By doing this, MED-V copies shortcuts from the guest to the host by following these steps:</span></span>

    1.  <span data-ttu-id="c8fc9-135">MED-V essaie de rechercher un dossier sous Démarrer Menu\\Programs sur l’ordinateur hôte portant le même nom que le dossier de l’invité sur lequel réside le raccourci.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-135">MED-V tries to locate a folder under Start Menu\\Programs in the host computer that is named the same as the folder in the guest where the shortcut resides.</span></span>

    2.  <span data-ttu-id="c8fc9-136">S’il n’y a pas de dossier correspondant, MED-V tente d’accéder à un dossier dans le dossier du menu Démarrer de l’hôte portant le même nom que le dossier de l’invité dans lequel réside le raccourci.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-136">If there is no matching folder, MED-V then tries to locate a folder in the host Start Menu folder that is named the same as the folder in the guest where the shortcut resides.</span></span>

    3.  <span data-ttu-id="c8fc9-137">S’il n’y a aucun dossier correspondant, MED-V copie le raccourci vers le dossier par défaut sur l’hôte, le dossier Menu\\Programs de démarrage.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-137">If there is no matching folder, MED-V copies the shortcut to the default folder on the host, the Start Menu\\Programs folder.</span></span>

2.  <span data-ttu-id="c8fc9-138">Exemple de processus de publication d’application:</span><span class="sxs-lookup"><span data-stu-id="c8fc9-138">Example of application publishing process:</span></span>

    1.  <span data-ttu-id="c8fc9-139">Si le raccourci d’une application est publié dans le dossier Start Menu\\Programs\\AppShortcuts de l’invité, l’application MED-V recherche un dossier de démarrage Menu\\Programs\\ AppShortcuts et, le cas échéant, copie le raccourci vers ce dossier.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-139">If an application shortcut is published to the Start Menu\\Programs\\AppShortcuts folder in the guest, then MED-V looks in the host computer for a Start Menu\\Programs\\ AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    2.  <span data-ttu-id="c8fc9-140">Si le dossier est introuvable, l’action MED-V recherche un dossier de démarrage dans l’ordinateur hôte et, le cas échéant, copie le raccourci vers ce dossier.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-140">If the folder is not found, then MED-V looks in the host computer for a Start Menu\\AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    3.  <span data-ttu-id="c8fc9-141">Si le dossier n’est pas trouvé, MED-V copie le raccourci dans le dossier de démarrage Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-141">If the folder is not found, then MED-V copies the shortcut to the Start Menu\\Programs folder.</span></span>

<span data-ttu-id="c8fc9-142">**Remarques**  Un dossier doit déjà exister dans le dossier du menu Démarrer de l’ordinateur hôte pour MED-V pour y copier le raccourci.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-142">**Note** A folder must already exist in the host computer Start Menu folder for MED-V to copy the shortcut there.</span></span> <span data-ttu-id="c8fc9-143">MED-V ne crée pas le dossier s’il n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="c8fc9-143">MED-V does not create the folder if it does not already exist.</span></span>

 

## <span data-ttu-id="c8fc9-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8fc9-144">Related topics</span></span>


[<span data-ttu-id="c8fc9-145">Installation et suppression d'une application sur l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="c8fc9-145">Installing and Removing an Application on the MED-V Workspace</span></span>](installing-and-removing-an-application-on-the-med-v-workspace.md)

[<span data-ttu-id="c8fc9-146">Gestion des mises à jour de logiciels pour les espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="c8fc9-146">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

[<span data-ttu-id="c8fc9-147">Liste d'exclusion d'applications de WindowsVirtualPC</span><span class="sxs-lookup"><span data-stu-id="c8fc9-147">Windows Virtual PC Application Exclude List</span></span>](windows-virtual-pc-application-exclude-list.md)

 

 






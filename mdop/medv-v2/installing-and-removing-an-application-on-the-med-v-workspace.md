---
title: Installation et suppression d'une application sur l'espace de travail MED-V
description: Installation et suppression d'une application sur l'espace de travail MED-V
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812222"
---
# <span data-ttu-id="91ecd-103">Installation et suppression d'une application sur l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="91ecd-103">Installing and Removing an Application on the MED-V Workspace</span></span>


<span data-ttu-id="91ecd-104">Les applications qui ne sont pas compatibles avec le système d’exploitation hôte peuvent être exécutées dans l’espace de travail MED-V et être ouvertes dans l’espace de travail MED-V de la même manière que dans l’ordinateur hôte, dans le menu **Démarrer** ou à l’aide d’un raccourci localhost.</span><span class="sxs-lookup"><span data-stu-id="91ecd-104">Applications that are incompatible with the host operating system can be run in the MED-V workspace and opened in the MED-V workspace in the same manner in which they are opened from the host computer, on the **Start** menu or by using a localhost shortcut.</span></span>

<span data-ttu-id="91ecd-105">Après avoir déployé un espace de travail MED-V, vous avez accès à différentes options pour l’installation et la suppression d’applications dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="91ecd-105">After you have deployed a MED-V workspace, you have several different options available to you for installing and removing applications in the MED-V workspace.</span></span> <span data-ttu-id="91ecd-106">Les options suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="91ecd-106">These options include the following:</span></span>

-   [<span data-ttu-id="91ecd-107">Utilisation d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="91ecd-107">Using Group Policy</span></span>](#bkmk-grouppolicy)

-   [<span data-ttu-id="91ecd-108">Utilisation d’un système de distribution de logiciels électronique</span><span class="sxs-lookup"><span data-stu-id="91ecd-108">Using an Electronic Software Distribution System</span></span>](#bkmk-esd)

-   [<span data-ttu-id="91ecd-109">Utilisation de la virtualisation des applications (APP-V)</span><span class="sxs-lookup"><span data-stu-id="91ecd-109">Using Application Virtualization (APP-V)</span></span>](#bkmk-appv)

-   [<span data-ttu-id="91ecd-110">Mise à jour de l’image principale</span><span class="sxs-lookup"><span data-stu-id="91ecd-110">Updating the Core Image</span></span>](#bkmk-coreimage)

<span data-ttu-id="91ecd-111">**Important**  Pour vous assurer qu’une application installée est automatiquement publiée sur l’hôte, installez l’application sur l’ordinateur virtuel pour **tous les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="91ecd-111">**Important** To make sure that an installed application is automatically published to the host, install the application on the virtual machine for **All Users**.</span></span> <span data-ttu-id="91ecd-112">Pour plus d’informations sur la publication d’applications, voir [publication et annulation de la publication d’une application dans l’espace de travail MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="91ecd-112">For more information about application publishing, see [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span>

 

<span data-ttu-id="91ecd-113">**Astuce**  MED-V ne prend pas en charge la redirection d’invité à hôte pour la gestion de contenu, par exemple en double-cliquant sur un document Microsoft Word dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="91ecd-113">**Tip** MED-V does not support guest-to-host redirection for content handling, such as double-clicking a Microsoft Word document in Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="91ecd-114">Par conséquent, les applications requises, comme Microsoft Word, doivent être installées dans l’espace de travail MED-V pour fournir la fonctionnalité de gestion de contenu par défaut qu’un utilisateur final peut attendre.</span><span class="sxs-lookup"><span data-stu-id="91ecd-114">Therefore, the required applications, such as Microsoft Word, must be installed in MED-V workspace to provide the default content handling functionality that an end user might expect.</span></span>

 

## <a href="" id="bkmk-grouppolicy"></a> <span data-ttu-id="91ecd-115">Ajout et suppression d’applications à l’aide d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="91ecd-115">Adding and Removing Applications by Using Group Policy</span></span>


<span data-ttu-id="91ecd-116">Vous pouvez utiliser une stratégie de groupe et des objets de stratégie de groupe pour attribuer ou publier des applications dans l’ensemble des espaces de travail MED-V de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="91ecd-116">You can use Group Policy and Group Policy objects to assign or publish applications to all or some MED-V workspaces in your enterprise.</span></span> <span data-ttu-id="91ecd-117">S’il s’agit d’une application attribuée, l’application s’affiche dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="91ecd-117">For assigned applications, when an end user logs on to their computer, the application appears on the **Start** menu.</span></span> <span data-ttu-id="91ecd-118">Lorsqu’ils sélectionnent la nouvelle application pour la première fois, l’application s’installe et est prête à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="91ecd-118">When they select the new application for the first time, the application installs and is ready for use.</span></span> <span data-ttu-id="91ecd-119">Pour les applications publiées, l’application n’apparaît pas dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="91ecd-119">For published applications, the application does not appear on the **Start** menu.</span></span> <span data-ttu-id="91ecd-120">Il est disponible uniquement pour l’utilisateur final pour l’installation à l’aide de l’application **Ajout/suppression de programmes** du **panneau de configuration** ou en ouvrant un fichier associé à l’application.</span><span class="sxs-lookup"><span data-stu-id="91ecd-120">It is only available for the end user to install by using **Add or Remove Programs** in **Control Panel** or by opening a file that is associated with the application.</span></span>

<span data-ttu-id="91ecd-121">Vous pouvez également utiliser les objets de stratégie de groupe et de stratégie de groupe de la même manière pour supprimer des applications de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="91ecd-121">You can also use Group Policy and Group Policy objects in the same manner to remove applications from the MED-V workspace.</span></span>

<span data-ttu-id="91ecd-122">Pour plus d’informations sur la façon d’ajouter et de supprimer des applications à l’aide d’une stratégie de groupe, voir [installation de logiciels de stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="91ecd-122">For more information about how to add and remove applications by using Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

## <a href="" id="bkmk-esd"></a> <span data-ttu-id="91ecd-123">Ajout et suppression d’applications à l’aide d’un système ESD</span><span class="sxs-lookup"><span data-stu-id="91ecd-123">Adding and Removing Applications by Using an ESD System</span></span>


<span data-ttu-id="91ecd-124">Un système de distribution de logiciels électronique (ESD) est conçu pour déployer efficacement des logiciels et d’autres informations sur de nombreux ordinateurs sur des connexions réseau.</span><span class="sxs-lookup"><span data-stu-id="91ecd-124">An electronic software distribution (ESD) system is designed to efficiently deploy software and other information to many different computers over network connections.</span></span> <span data-ttu-id="91ecd-125">Si votre organisation utilise un système de maintenance ESD pour déployer le logiciel, vous pouvez l’utiliser pour ajouter et supprimer des applications dans les espaces de travail MED-V, de la même façon que vous ajoutez et supprimez des applications sur des ordinateurs physiques.</span><span class="sxs-lookup"><span data-stu-id="91ecd-125">If your organization uses an ESD system to deploy software, you can use it to add and remove applications on MED-V workspaces just as you add and remove applications on physical computers.</span></span>

## <a href="" id="bkmk-appv"></a> <span data-ttu-id="91ecd-126">Ajout et suppression d’applications à l’aide de APP-V</span><span class="sxs-lookup"><span data-stu-id="91ecd-126">Adding and Removing Applications by Using APP-V</span></span>


<span data-ttu-id="91ecd-127">Microsoft Application Virtualization (App-V) fournit la capacité d’administration de rendre les applications accessibles aux ordinateurs des utilisateurs finaux sans avoir à installer les applications directement sur ces ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="91ecd-127">Microsoft Application Virtualization (App-V) provides the administrative capability to make applications available to end-user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="91ecd-128">Vous souhaiterez peut-être utiliser MED-V et App-V conjointement si, par exemple, votre organisation a des applications que vous avez séquencées avec l’application-V dans Windows XP, et que le réséquençage retarderait votre migration vers Windows 7.</span><span class="sxs-lookup"><span data-stu-id="91ecd-128">You might want to use MED-V and App-V together if, for example, your organization has applications that you sequenced with App-V in Windows XP, and re-sequencing them would delay your migration to Windows 7.</span></span>

<span data-ttu-id="91ecd-129">Vous pouvez utiliser MED-V conjointement avec App-V pour ajouter et supprimer des applications virtuelles sur un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="91ecd-129">You can use MED-V together with App-V to add and remove virtual applications on a deployed MED-V workspace.</span></span> <span data-ttu-id="91ecd-130">Pour gérer les applications de cette manière, vous devez d’abord installer l’agent App-V sur le système d’exploitation invité MED-V.</span><span class="sxs-lookup"><span data-stu-id="91ecd-130">To manage applications in this manner, you must first install the App-V agent on the MED-V guest operating system.</span></span> <span data-ttu-id="91ecd-131">Vous pouvez ensuite utiliser App-V dans l’espace de travail MED-V pour ajouter et supprimer les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="91ecd-131">You can then use App-V in the MED-V workspace to add and remove the virtual applications.</span></span>

<span data-ttu-id="91ecd-132">Pour plus d’informations sur la façon d’installer et d’utiliser App-V, voir [virtualisation des applications](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="91ecd-132">For information about how to install and use App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

<span data-ttu-id="91ecd-133">**Important**  Les applications App-V que vous publiez sur l’espace de travail MED-V possèdent des associations de types de fichiers qui ne peuvent pas être redirigées de l’ordinateur hôte vers l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="91ecd-133">**Important** App-V applications that you publish to the MED-V workspace have file-type associations that cannot redirect from the host computer to the guest virtual machine.</span></span> <span data-ttu-id="91ecd-134">Toutefois, l’utilisateur final peut toujours accéder à ces types de fichiers en cliquant sur **fichier**, puis en cliquant sur **ouvrir** dans l’application publiée-V.</span><span class="sxs-lookup"><span data-stu-id="91ecd-134">However, the end user can still access these file types by clicking **File**, and then by clicking **Open** on the published App-V application.</span></span>

<span data-ttu-id="91ecd-135">Pour forcer la redirection de ces associations de type de fichier, interroger l’application-V pour les associations de types de fichiers mappées en tapant le code suivant à une invite de commandes dans l’ordinateur virtuel invité: **SFTMIME/Query obj: type**.</span><span class="sxs-lookup"><span data-stu-id="91ecd-135">To force redirection of those file-type associations, query App-V for mapped file type associations by typing the following at a command prompt in the guest virtual machine: **sftmime /QUERY OBJ:TYPE**.</span></span> <span data-ttu-id="91ecd-136">Puis mappez les associations de types de fichiers dans l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="91ecd-136">Then, map those file type associations in the host computer.</span></span>

 

## <a href="" id="bkmk-coreimage"></a> <span data-ttu-id="91ecd-137">Ajout et suppression d’applications sur l’image principale</span><span class="sxs-lookup"><span data-stu-id="91ecd-137">Adding and Removing Applications on the Core Image</span></span>


<span data-ttu-id="91ecd-138">Même si vous n’avez pas envisagé de meilleures pratiques MED-V, vous pouvez ajouter et supprimer des applications directement sur l’image principale.</span><span class="sxs-lookup"><span data-stu-id="91ecd-138">Although not considered a MED-V best practice, you can add and remove applications directly on the core image.</span></span> <span data-ttu-id="91ecd-139">Après avoir ajouté ou supprimé une application, vous pouvez redéployer l’espace de travail MED-V vers votre entreprise tout comme vous l’avez déployé à l’origine.</span><span class="sxs-lookup"><span data-stu-id="91ecd-139">After you have added or removed an application, you can redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

<span data-ttu-id="91ecd-140">Pour plus d’informations sur l’ajout ou la suppression d’applications sur l’image principale, voir [l’installation d’applications sur une image de PC virtuel Windows](installing-applications-on-a-windows-virtual-pc-image.md).</span><span class="sxs-lookup"><span data-stu-id="91ecd-140">For more information about how to add or remove applications on the core image, see [Installing Applications on a Windows Virtual PC Image](installing-applications-on-a-windows-virtual-pc-image.md).</span></span>

<span data-ttu-id="91ecd-141">**Important**  Nous déconseillons cette méthode de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="91ecd-141">**Important** We do not recommend this method of managing applications.</span></span> <span data-ttu-id="91ecd-142">Si vous ajoutez ou supprimez des applications sur l’image principale, puis redéployez l’espace de travail MED-V vers votre entreprise, la première fois que vous devez réexécuter le programme d’installation, la première fois que vous devez réexécuter le programme d’installation, les données enregistrées sur l’ordinateur virtuel sont perdues</span><span class="sxs-lookup"><span data-stu-id="91ecd-142">If you add or remove applications on the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved on the virtual machine is lost.</span></span>

 

<span data-ttu-id="91ecd-143">**Remarques**  Même si une application est installée dans un espace de travail MED-V, vous devrez peut-être également publier l’application avant qu’elle ne soit disponible pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="91ecd-143">**Note** Even though an application is installed into a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="91ecd-144">Par exemple, il se peut que vous deviez publier une application installée si l’installation n’a pas créé automatiquement de raccourci dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="91ecd-144">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span> <span data-ttu-id="91ecd-145">De même, pour annuler la publication d’une application, vous devrez peut-être supprimer manuellement un raccourci du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="91ecd-145">Likewise, to unpublish an application, you might have to manually remove a shortcut from the **Start** menu.</span></span>

<span data-ttu-id="91ecd-146">Par défaut, la plupart des applications sont publiées au moment où elles sont installées, lors de la création et de l’activation automatiques de raccourcis.</span><span class="sxs-lookup"><span data-stu-id="91ecd-146">By default, most applications are published at the time that they are installed, when shortcuts are automatically created and enabled.</span></span>

 

## <span data-ttu-id="91ecd-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91ecd-147">Related topics</span></span>


[<span data-ttu-id="91ecd-148">Comment tester la publication d'applications</span><span class="sxs-lookup"><span data-stu-id="91ecd-148">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="91ecd-149">Comment publier et annuler la publication d'une application sur l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="91ecd-149">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 






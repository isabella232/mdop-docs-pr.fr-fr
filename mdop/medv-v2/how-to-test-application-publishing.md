---
title: Comment tester la publication d'applications
description: Comment tester la publication d'applications
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812041"
---
# <span data-ttu-id="4ba8c-103">Comment tester la publication d'applications</span><span class="sxs-lookup"><span data-stu-id="4ba8c-103">How to Test Application Publishing</span></span>


<span data-ttu-id="4ba8c-104">Suite à l’exécution de votre test de configuration pour la première fois, vous pouvez vérifier que la fonctionnalité de publication des applications fonctionne normalement en effectuant les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-104">After your test of first time setup finishes, you can verify that the application publishing functionality is working as expected by performing the following tasks.</span></span>

<a href="" id="bkmk-apppub"></a>**<span data-ttu-id="4ba8c-105">Pour tester la publication d’applications</span><span class="sxs-lookup"><span data-stu-id="4ba8c-105">To test application publishing</span></span>**

1.  <span data-ttu-id="4ba8c-106">Vérifiez que les applications que vous avez spécifiées pour la publication sont visibles.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-106">Verify that the applications that you specified for publishing are visible.</span></span>

    <span data-ttu-id="4ba8c-107">Cliquez sur **Démarrer** , puis sur **tous les programmes** et recherchez les applications spécifiées.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-107">Click **Start** and then click **All Programs** and search for the specified applications.</span></span>

    <span data-ttu-id="4ba8c-108">Dans certains cas, vous pouvez avoir installé la même application deux fois, une fois sur l’ordinateur hôte et une fois sur l’invité.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-108">In some cases, you might have the same application installed two times, one time on the host computer and one time on the guest.</span></span> <span data-ttu-id="4ba8c-109">Si une application publiée qui porte le même nom est publiée au même emplacement dans le menu de **démarrage** de l’hôte, elle se distingue du raccourci de l’application hôte en ajoutant le nom de l’ordinateur virtuel au nom du raccourci.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-109">If a published application that has the same name is published to the same location on the host **Start** menu, it is distinguished from the host application shortcut by adding the virtual machine name to the shortcut name.</span></span> <span data-ttu-id="4ba8c-110">Par exemple, dans le cas d’un ordinateur virtuel appelé «MEDVHost1», une application hôte peut être «bloc-notes» et une application publiée peut être «bloc-notes (MEDVHost1)».</span><span class="sxs-lookup"><span data-stu-id="4ba8c-110">For example, for a virtual machine named “MEDVHost1”, a host application might be "Notepad" and a published application might be "Notepad (MEDVHost1)".</span></span>

2.  <span data-ttu-id="4ba8c-111">Vérifiez que les applications fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-111">Verify that the applications function as intended.</span></span>

    <span data-ttu-id="4ba8c-112">Sur l’ordinateur hôte, démarrez les applications que vous avez publiées et vérifiez qu’elles s’ouvrent dans Windows XP SP3 sur l’invité.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-112">On the host computer, start the applications that you published and verify that they open in Windows XP SP3 on the guest.</span></span> <span data-ttu-id="4ba8c-113">L’application doit s’afficher dans une fenêtre de style Windows XP sur le Bureau de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-113">The application must appear in a Windows XP-style window on the host computer desktop.</span></span>

3.  <span data-ttu-id="4ba8c-114">Le cas échéant, vérifiez que les fonctions de redirection de document comme prévu.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-114">If applicable, verify that document redirection functions as intended.</span></span>

    <span data-ttu-id="4ba8c-115">Si une application publiée sur l’invité doit ouvrir un dossier sur le lecteur du système hôte, assurez-vous qu’elle peut ouvrir le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-115">If a published application on the guest has to open a folder on the host system drive, ensure that it can open the specified folder.</span></span>

    <span data-ttu-id="4ba8c-116">**Important**  Comme le PC virtuel Windows ne prend pas en charge la création d’un partage à partir d’un dossier déjà partagé, la redirection ne se produit pas pour tous les documents qui s’ouvrent à partir d’un dossier partagé, tels que le dossier Mes documents qui se trouve sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-116">**Important** Because Windows Virtual PC does not support creating a share from a folder that is already shared, redirection does not occur for any documents that open from a shared folder, such as a My Documents folder that is located on the network.</span></span> <span data-ttu-id="4ba8c-117">Pour plus d’informations, reportez-vous à [résolution des problèmes d’opérations](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="4ba8c-117">For more information, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="4ba8c-118">Une fois que vous avez vérifié que les applications publiées sont installées et fonctionnent correctement, vous pouvez tester s’il est possible d’ajouter ou de supprimer des applications à partir de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-118">After you have verified that published applications are installed and functioning correctly, you can test whether applications can be added or removed from the MED-V workspace.</span></span>

**<span data-ttu-id="4ba8c-119">Pour vérifier qu’il est possible d’ajouter ou de supprimer une application</span><span class="sxs-lookup"><span data-stu-id="4ba8c-119">To test that an application can be added or removed</span></span>**

1.  <span data-ttu-id="4ba8c-120">Ajoutez ou supprimez une application de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-120">Add or remove an application from the MED-V workspace.</span></span>

    <span data-ttu-id="4ba8c-121">Pour plus d’informations sur la façon d’ajouter et de supprimer des applications d’un espace de travail MED-V, voir [gestion des applications déployées dans les espaces de travail MED-v](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="4ba8c-121">For information about how to add and remove applications from a MED-V workspace, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

2.  <span data-ttu-id="4ba8c-122">Si vous avez ajouté une application, répétez les étapes décrites dans la procédure [de test](#bkmk-apppub) de la publication d’applications pour vérifier que la nouvelle application fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-122">If you added an application, repeat the steps in [To Test Application Publishing](#bkmk-apppub) to verify that the new application functions as intended.</span></span>

3.  <span data-ttu-id="4ba8c-123">Si vous avez supprimé une application, cliquez sur **Démarrer** , puis sur **tous les programmes** et assurez-vous que les applications que vous avez supprimées ne sont plus répertoriées.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-123">If you removed an application, click **Start** and then click **All Programs** and verify that any applications that you removed are no longer listed.</span></span>

<span data-ttu-id="4ba8c-124">**Remarques**  Si vous rencontrez des problèmes lors de la vérification des paramètres de composition de votre application, voir [résolution des problèmes d’opérations](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="4ba8c-124">**Note** If you encounter any problems when verifying your application publication settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="4ba8c-125">Une fois que vous avez terminé le test de la publication d’une application, vous pouvez tester les autres configurations d’espace de travail MED-V pour vérifier qu’elles fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-125">After you have completed testing application publishing, you can test other MED-V workspace configurations to verify that they function as intended.</span></span>

<span data-ttu-id="4ba8c-126">Une fois que vous avez terminé de tester votre package d’espace de travail MED-V et que vous avez vérifié son fonctionnement, vous pouvez déployer l’espace de travail MED-V dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="4ba8c-126">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="4ba8c-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ba8c-127">Related topics</span></span>

[<span data-ttu-id="4ba8c-128">Comment tester la redirection d'URL</span><span class="sxs-lookup"><span data-stu-id="4ba8c-128">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="4ba8c-129">Comment vérifier les paramètres de première installation</span><span class="sxs-lookup"><span data-stu-id="4ba8c-129">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="4ba8c-130">Déploiement du package d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="4ba8c-130">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 






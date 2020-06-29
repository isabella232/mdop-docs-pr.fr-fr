---
title: Liste d'exclusion d'applications de WindowsVirtualPC
description: Liste d'exclusion d'applications de WindowsVirtualPC
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810109"
---
# <span data-ttu-id="be741-103">Liste d'exclusion d'applications de WindowsVirtualPC</span><span class="sxs-lookup"><span data-stu-id="be741-103">Windows Virtual PC Application Exclude List</span></span>


<span data-ttu-id="be741-104">Dans certains cas, il est possible que vous ne souhaitiez pas que les applications installées dans l’espace de travail MED-V soient publiées sur le menu **Démarrer** de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="be741-104">In some instances, you might not want applications that are installed in the MED-V workspace to be published to the host computer **Start** menu.</span></span> <span data-ttu-id="be741-105">Vous pouvez annuler la publication de ces applications en suivant les instructions de la [procédure de publication et d’annulation de la publication d’une application dans l’espace de travail MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="be741-105">You can unpublish these applications by following the instructions at [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span> <span data-ttu-id="be741-106">Toutefois, si le programme a déjà été automatiquement mis à jour, il peut également être republié automatiquement.</span><span class="sxs-lookup"><span data-stu-id="be741-106">However, if the program ever automatically updates, it might also be automatically republished.</span></span> <span data-ttu-id="be741-107">Ainsi, vous devrez annuler la publication de l’application.</span><span class="sxs-lookup"><span data-stu-id="be741-107">This causes you to have to unpublish the application again.</span></span>

<span data-ttu-id="be741-108">Windows Virtual PC inclut une fonctionnalité appelée «liste d’exclusion» qui vous permet de spécifier certaines applications installées que vous ne souhaitez pas publier dans le menu **Démarrer** de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="be741-108">Windows Virtual PC includes a feature known as the "Exclude List" that lets you specify certain installed applications that you do not want published to the host **Start** menu.</span></span> <span data-ttu-id="be741-109">La «liste d’exclusion» est située dans le registre invité dans la clé HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList et répertorie les applications qui ne sont pas publiées dans le menu **Démarrer** de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="be741-109">The "Exclude List" is located in the guest registry in the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList key and lists those applications that are not published to the host **Start** menu.</span></span> <span data-ttu-id="be741-110">Vous pouvez considérer la «liste d’exclusion» comme annuler définitivement la publication des applications spécifiées, car toutes les mises à jour automatiques des applications qui sont répertoriées n’entraînent pas leur republication automatique.</span><span class="sxs-lookup"><span data-stu-id="be741-110">You can think of the “Exclude List” as permanently unpublishing the specified applications because any automatic updates to the applications that are listed will not cause them to be automatically republished.</span></span>

## <span data-ttu-id="be741-111">Gestion des applications à l’aide de la liste d’exclusion dans le PC virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="be741-111">Managing Applications by Using the Exclude List in Windows Virtual PC</span></span>


****

1.  <span data-ttu-id="be741-112">Ouvrir l’espace de travail MED-V en plein écran.</span><span class="sxs-lookup"><span data-stu-id="be741-112">Open the MED-V workspace in full screen.</span></span>

    <span data-ttu-id="be741-113">Pour plus d’informations sur l’ouverture de l’espace de travail MED-V en mode plein écran à l’aide du kit de tâches d’administration de MED-v, voir [affichage des configurations d’espace de travail MED-v](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span><span class="sxs-lookup"><span data-stu-id="be741-113">For information about opening the MED-V workspace in full-screen mode by using the MED-V Administration Toolkit, see [Viewing MED-V Workspace Configurations](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span></span> <span data-ttu-id="be741-114">Ou vous pouvez l’ouvrir manuellement en mode plein écran en cliquant sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, sur **PC virtuel Windows**, puis en double-cliquant sur l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="be741-114">Or you can manually open it in full screen by clicking **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, and then double-click the MED-V workspace.</span></span>

2.  <span data-ttu-id="be741-115">Dans la fenêtre Windows Virtual PC de l’espace de travail MED-V, ouvrez l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="be741-115">In the MED-V workspace Windows Virtual PC window, open Registry Editor.</span></span>

    <span data-ttu-id="be741-116">Cliquez sur **Démarrer**, sur **exécuter**, puis tapez regedit.</span><span class="sxs-lookup"><span data-stu-id="be741-116">Click **Start**, click **Run**, and then type regedit.</span></span> <span data-ttu-id="be741-117">Cliquez ensuite sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="be741-117">Then click **OK**.</span></span>

3.  <span data-ttu-id="be741-118">Dans l’éditeur du Registre, recherchez la clé de Registre HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="be741-118">In Registry Editor, locate the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList registry key.</span></span>

4.  <span data-ttu-id="be741-119">Créez une nouvelle valeur de Registre pour l’application installée que vous ne souhaitez pas publier sur le menu **Démarrer** de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="be741-119">Create a new registry value for the installed application that you do not want published to the host computer **Start** menu.</span></span> <span data-ttu-id="be741-120">Par exemple, si vous voulez annuler la publication du programme publié automatiquement Microsoft Silverlight, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="be741-120">For example, if you want to unpublish the automatically published program Microsoft Silverlight, follow these steps:</span></span>

    1.  <span data-ttu-id="be741-121">Après avoir sélectionné la clé de Registre VPCVAppExcludeList, cliquez sur **modifier**, sur **nouveau**, puis sur **valeur de chaîne**.</span><span class="sxs-lookup"><span data-stu-id="be741-121">With the VPCVAppExcludeList registry key highlighted, click **Edit**, click **New**, and then click **String Value**.</span></span>

    2.  <span data-ttu-id="be741-122">Entrez le nom de la nouvelle valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="be741-122">Enter the name for the new registry value.</span></span> <span data-ttu-id="be741-123">Par exemple, pour Microsoft Silverlight, vous pouvez entrer sllauncher.exe.</span><span class="sxs-lookup"><span data-stu-id="be741-123">For example, for Microsoft Silverlight, you might enter sllauncher.exe.</span></span>

    3.  <span data-ttu-id="be741-124">Double-cliquez sur la nouvelle valeur du Registre et entrez les données de la valeur.</span><span class="sxs-lookup"><span data-stu-id="be741-124">Double-click the new registry value and enter the value data.</span></span>

        <span data-ttu-id="be741-125">Le champ données de la valeur correspond au chemin d’accès complet de la commande dont vous voulez annuler la publication.</span><span class="sxs-lookup"><span data-stu-id="be741-125">The value data is the full path for the command that you want to unpublish.</span></span> <span data-ttu-id="be741-126">Pour trouver le chemin d’accès complet, cliquez avec le bouton droit sur le raccourci du menu **Démarrer** de l’application que vous ne souhaitez pas publier, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="be741-126">You can find the full path by right-clicking on the shortcut on the **Start** menu for the application that you do not want published and then clicking **Properties**.</span></span> <span data-ttu-id="be741-127">Le chemin d’accès complet figure dans l’onglet **raccourci** de **target**.</span><span class="sxs-lookup"><span data-stu-id="be741-127">The full path is listed in the **Shortcut** tab under **Target**.</span></span>

        <span data-ttu-id="be741-128">Par exemple, pour le programme Microsoft Silverlight, le chemin d’accès complet peut être «C:\\Program Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe».</span><span class="sxs-lookup"><span data-stu-id="be741-128">For example, for the program Microsoft Silverlight, the full path might be "C:\\Program Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."</span></span>

        <span data-ttu-id="be741-129">**Important**  Le cas échéant, supprimez les guillemets du chemin d’accès complet lorsque vous entrez dans le champ données de la valeur.</span><span class="sxs-lookup"><span data-stu-id="be741-129">**Important** If applicable, remove the quotation marks from the full path when you enter it into the value data field.</span></span>

         

5.  <span data-ttu-id="be741-130">Fermez l’éditeur du Registre et redémarrez l’ordinateur virtuel de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="be741-130">Close Registry Editor and restart the MED-V workspace virtual machine.</span></span>

    <span data-ttu-id="be741-131">L’application est toujours installée sur l’espace de travail MED-V, mais elle est désormais supprimée du menu **Démarrer** de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="be741-131">The application is still installed in the MED-V workspace but is now removed from the host computer **Start** menu.</span></span>

<span data-ttu-id="be741-132">Vous pouvez également republier une application exclus dans le menu **Démarrer** de l’hôte en supprimant la valeur correspondante de la clé VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="be741-132">You can also republish an excluded application to the host **Start** menu by deleting the corresponding value from the VPCVAppExcludeList key.</span></span> <span data-ttu-id="be741-133">Par exemple, pour republier Microsoft Silverlight, cliquez avec le bouton droit sur la valeur du Registre sllauncher.exe puis sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="be741-133">For example, to republish Microsoft Silverlight, right-click the registry value sllauncher.exe and select **Delete**.</span></span>

## <span data-ttu-id="be741-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be741-134">Related topics</span></span>


[<span data-ttu-id="be741-135">Informations techniques de référence pour MED-V</span><span class="sxs-lookup"><span data-stu-id="be741-135">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

[<span data-ttu-id="be741-136">Comment publier et annuler la publication d'une application sur l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="be741-136">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 






---
title: Comment afficher et configurer des applications et des extensions de l’application virtuelle par défaut à l’aide de la console de gestion
description: Comment afficher et configurer des applications et des extensions de l’application virtuelle par défaut à l’aide de la console de gestion
author: dansimp
ms.assetid: c77e6662-7a18-4da1-8da8-b58068b65fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c5a8cd5c914d1ddd720ebfef318e3a094cdc6f0b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805113"
---
# <span data-ttu-id="51c08-103">Comment afficher et configurer des applications et des extensions de l’application virtuelle par défaut à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="51c08-103">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>


<span data-ttu-id="51c08-104">Utilisez la procédure suivante pour afficher et configurer les extensions de package par défaut.</span><span class="sxs-lookup"><span data-stu-id="51c08-104">Use the following procedure to view and configure default package extensions.</span></span>

**<span data-ttu-id="51c08-105">Pour afficher et configurer les extensions d’application virtuelles par défaut</span><span class="sxs-lookup"><span data-stu-id="51c08-105">To view and configure default virtual application extensions</span></span>**

1.  <span data-ttu-id="51c08-106">Pour afficher le package que vous voulez configurer, ouvrez la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="51c08-106">To view the package that you want to configure, open the App-V 5.0 Management Console.</span></span> <span data-ttu-id="51c08-107">Sélectionnez le package que vous voulez configurer, cliquez avec le bouton droit sur le nom du package, puis sélectionnez **modifier la configuration par défaut**.</span><span class="sxs-lookup"><span data-stu-id="51c08-107">Select the package that you want to configure, right-click the package name and select **edit default configuration**.</span></span>

2.  <span data-ttu-id="51c08-108">Pour afficher les applications contenues dans le package spécifié, dans le volet **configuration par défaut** , cliquez sur **applications**.</span><span class="sxs-lookup"><span data-stu-id="51c08-108">To view the applications contained in the specified package, in the **Default Configuration** pane, click **Applications**.</span></span> <span data-ttu-id="51c08-109">Pour afficher les raccourcis pour ce package, cliquez sur **raccourcis**.</span><span class="sxs-lookup"><span data-stu-id="51c08-109">To view the shortcuts for that package, click **Shortcuts**.</span></span> <span data-ttu-id="51c08-110">Pour afficher les associations de type de fichier pour ce package, cliquez sur **types de fichiers**.</span><span class="sxs-lookup"><span data-stu-id="51c08-110">To view the file type associations for that package, click **File Types**.</span></span>

3.  <span data-ttu-id="51c08-111">Pour activer les extensions d’application, sélectionnez **activer**.</span><span class="sxs-lookup"><span data-stu-id="51c08-111">To enable the application extensions, select **ENABLE**.</span></span>

    <span data-ttu-id="51c08-112">Pour activer les raccourcis, sélectionnez **activer les raccourcis**.</span><span class="sxs-lookup"><span data-stu-id="51c08-112">To enable shortcuts, select **ENABLE SHORTCUTS**.</span></span> <span data-ttu-id="51c08-113">Pour ajouter un nouveau raccourci pour l’application sélectionnée, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** et sélectionnez **Ajouter un nouveau raccourci**.</span><span class="sxs-lookup"><span data-stu-id="51c08-113">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane and select **Add new shortcut**.</span></span> <span data-ttu-id="51c08-114">Pour supprimer un raccourci, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** et sélectionnez **supprimer le raccourci**.</span><span class="sxs-lookup"><span data-stu-id="51c08-114">To remove a shortcut, right-click the application in the **SHORTCUTS** pane and select **Remove Shortcut**.</span></span> <span data-ttu-id="51c08-115">Pour modifier un raccourci existant, cliquez avec le bouton droit sur l’application, puis sélectionnez **modifier le raccourci**.</span><span class="sxs-lookup"><span data-stu-id="51c08-115">To edit an existing shortcut, right-click the application and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="51c08-116">Pour afficher d’autres extensions d’application, cliquez sur **avancé** , puis cliquez sur **Exporter la configuration**.</span><span class="sxs-lookup"><span data-stu-id="51c08-116">To view any other application extensions, click **Advanced** and click **Export Configuration**.</span></span> <span data-ttu-id="51c08-117">Tapez un nom de fichier, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="51c08-117">Type in a filename and click **Save**.</span></span> <span data-ttu-id="51c08-118">Vous pouvez afficher toutes les extensions d’application associées au package à l’aide du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="51c08-118">You can view all application extensions associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="51c08-119">Pour modifier les autres extensions de l’application, modifiez le fichier de configuration, puis cliquez sur **Importer et remplacez cette configuration**.</span><span class="sxs-lookup"><span data-stu-id="51c08-119">To edit other application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="51c08-120">Sélectionnez le fichier modifié, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="51c08-120">Select the modified file and click **Open**.</span></span> <span data-ttu-id="51c08-121">Dans la boîte de dialogue, cliquez sur **remplacer** pour terminer le processus.</span><span class="sxs-lookup"><span data-stu-id="51c08-121">In the dialog box, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="51c08-122">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="51c08-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="51c08-123">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="51c08-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="51c08-124">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="51c08-124">Got an App-V issue?</span></span>** <span data-ttu-id="51c08-125">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="51c08-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="51c08-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51c08-126">Related topics</span></span>


[<span data-ttu-id="51c08-127">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="51c08-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 






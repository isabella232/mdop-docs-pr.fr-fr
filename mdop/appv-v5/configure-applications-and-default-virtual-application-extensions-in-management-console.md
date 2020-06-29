---
title: Configurer les applications et les extensions d’application virtuelle par défaut dans la console de gestion
description: Comment afficher et configurer des applications et des extensions de l’application virtuelle par défaut à l’aide de la console de gestion
author: dansimp
ms.assetid: 1e1941d3-fb22-4077-8ec6-7a0cb80335d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2019
ms.openlocfilehash: 7c29ba0e40cf1adbc2b2297124cfb245a65a7ffe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805928"
---
#   <span data-ttu-id="d0e8d-103">Configurer les applications et les extensions d’application virtuelle par défaut dans la console de gestion</span><span class="sxs-lookup"><span data-stu-id="d0e8d-103">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>

<span data-ttu-id="d0e8d-104">Utilisez la procédure suivante pour *Afficher* et *configurer* les extensions de package par défaut.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-104">Use the following procedure to *view* and *configure* default package extensions.</span></span>

**<span data-ttu-id="d0e8d-105">Pour afficher et configurer les extensions d’application virtuelles par défaut</span><span class="sxs-lookup"><span data-stu-id="d0e8d-105">To view and configure default virtual application extensions</span></span>**

1.  <span data-ttu-id="d0e8d-106">Pour afficher le package que vous voulez configurer, ouvrez la console de gestion App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-106">To view the package that you want to configure, open the App-V 5.1 Management Console.</span></span> <span data-ttu-id="d0e8d-107">Sélectionnez le package que vous voulez configurer, cliquez avec le bouton droit sur le nom du package, puis sélectionnez **modifier la configuration par défaut**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-107">Select the package that you want to configure, right-click the package name and select **edit default configuration**.</span></span>

2.  <span data-ttu-id="d0e8d-108">Pour afficher les applications contenues dans le package spécifié, dans le volet **configuration par défaut** , cliquez sur **applications**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-108">To view the applications contained in the specified package, in the **Default Configuration** pane, click **Applications**.</span></span> <span data-ttu-id="d0e8d-109">Pour afficher les raccourcis pour ce package, cliquez sur **raccourcis**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-109">To view the shortcuts for that package, click **Shortcuts**.</span></span> <span data-ttu-id="d0e8d-110">Pour afficher les associations de type de fichier pour ce package, cliquez sur **types de fichiers**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-110">To view the file type associations for that package, click **File Types**.</span></span>

3.  <span data-ttu-id="d0e8d-111">Pour activer les extensions d’application, sélectionnez **activer**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-111">To enable the application extensions, select **ENABLE**.</span></span>

    <span data-ttu-id="d0e8d-112">Pour activer les raccourcis, sélectionnez **activer les raccourcis**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-112">To enable shortcuts, select **ENABLE SHORTCUTS**.</span></span> <span data-ttu-id="d0e8d-113">Pour ajouter un nouveau raccourci pour l’application sélectionnée, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** et sélectionnez **Ajouter un nouveau raccourci**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-113">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane and select **Add new shortcut**.</span></span> <span data-ttu-id="d0e8d-114">Pour supprimer un raccourci, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** et sélectionnez **supprimer le raccourci**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-114">To remove a shortcut, right-click the application in the **SHORTCUTS** pane and select **Remove Shortcut**.</span></span> <span data-ttu-id="d0e8d-115">Pour modifier un raccourci existant, cliquez avec le bouton droit sur l’application, puis sélectionnez **modifier le raccourci**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-115">To edit an existing shortcut, right-click the application and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="d0e8d-116">Pour afficher d’autres extensions d’application, cliquez sur **avancé** , puis cliquez sur **Exporter la configuration**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-116">To view any other application extensions, click **Advanced** and click **Export Configuration**.</span></span> <span data-ttu-id="d0e8d-117">Tapez un nom de fichier, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-117">Type in a filename and click **Save**.</span></span> <span data-ttu-id="d0e8d-118">Vous pouvez afficher toutes les extensions d’application associées au package à l’aide du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-118">You can view all application extensions associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="d0e8d-119">Pour modifier les autres extensions de l’application, modifiez le fichier de configuration, puis cliquez sur **Importer et remplacez cette configuration**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-119">To edit other application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="d0e8d-120">Sélectionnez le fichier modifié, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-120">Select the modified file and click **Open**.</span></span> <span data-ttu-id="d0e8d-121">Dans la boîte de dialogue, cliquez sur **remplacer** pour terminer le processus.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-121">In the dialog box, click **Overwrite** to complete the process.</span></span>

><span data-ttu-id="d0e8d-122">**Remarques** Si le téléchargement échoue et que la taille de votre fichier de configuration est supérieure à 4 Mo, vous devrez augmenter la taille de fichier maximale autorisée par le serveur.</span><span class="sxs-lookup"><span data-stu-id="d0e8d-122">**Note** If the upload fails and the size of your configuration file is above 4MB, you will need to increase the maximum file size allowed by the server.</span></span> <span data-ttu-id="d0e8d-123">Pour cela, il suffit d’ajouter l’attribut maxRequestLength avec une valeur supérieure à la taille de votre fichier de configuration (en Ko) pour l’élément httpRuntime de la ligne 26 `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config` .</span><span class="sxs-lookup"><span data-stu-id="d0e8d-123">This can be done by adding the maxRequestLength attribute with a value greater than the size of your configuration file (in KB) to the httpRuntime element on line 26 of `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config`.</span></span>  
<span data-ttu-id="d0e8d-124">Par exemple, si `<httpRuntime targetFramework="4.5"/>` vous modifiez la valeur sur pour `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` augmenter la taille maximale de 8 Mo</span><span class="sxs-lookup"><span data-stu-id="d0e8d-124">For example, changing `<httpRuntime targetFramework="4.5"/>` to `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` will increase the maximum size to 8MB</span></span>


<span data-ttu-id="d0e8d-125">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="d0e8d-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="d0e8d-126">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="d0e8d-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="d0e8d-127">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="d0e8d-127">Got an App-V issue?</span></span>** <span data-ttu-id="d0e8d-128">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="d0e8d-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d0e8d-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0e8d-129">Related topics</span></span>


[<span data-ttu-id="d0e8d-130">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="d0e8d-130">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 






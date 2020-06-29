---
title: Notes de publication d'App-V4.6SP2
description: Notes de publication d'App-V4.6SP2
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809299"
---
# <span data-ttu-id="f35c5-103">Notes de publication d'App-V4.6SP2</span><span class="sxs-lookup"><span data-stu-id="f35c5-103">App-V 4.6 SP2 Release Notes</span></span>


**<span data-ttu-id="f35c5-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="f35c5-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="f35c5-105">Lisez attentivement ces notes de publication avant de procéder à l’installation de Microsoft Application Virtualization (App-V) 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="f35c5-105">Read these release notes thoroughly before you install Microsoft Application Virtualization (App-V)4.6 SP2.</span></span>

<span data-ttu-id="f35c5-106">Ces notes de publication contiennent des informations nécessaires à l’installation réussie du SP2 pour l’application virtualisation des applications 4,6.</span><span class="sxs-lookup"><span data-stu-id="f35c5-106">These release notes contain information that is required to successfully install Application Virtualization 4.6 SP2.</span></span> <span data-ttu-id="f35c5-107">Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="f35c5-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="f35c5-108">S’il existe une différence entre ces notes de publication et la nouvelle documentation App-V 4.6 SP2, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="f35c5-108">If there is a difference between these release notes and other App-V4.6SP2 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="f35c5-109">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="f35c5-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="f35c5-110">À propos de la documentation relative aux produits</span><span class="sxs-lookup"><span data-stu-id="f35c5-110">About the Product Documentation</span></span>


<span data-ttu-id="f35c5-111">Pour plus d’informations sur la documentation pour App-V, voir la page [virtualisation d’application](https://go.microsoft.com/fwlink/?LinkID=232982) sur Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="f35c5-111">For more information about documentation for App-V, see the [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) page on Microsoft TechNet.</span></span>

## <span data-ttu-id="f35c5-112">Envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="f35c5-112">Providing feedback</span></span>


<span data-ttu-id="f35c5-113">Vos commentaires sur App-V 4.6 SP2 vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="f35c5-113">We are interested in your feedback on App-V4.6SP2.</span></span> <span data-ttu-id="f35c5-114">Vous pouvez envoyer vos commentaires à <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="f35c5-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="f35c5-115">**Remarques**  Cette adresse de messagerie n’est pas un canal de prise en charge, mais vos commentaires nous aideront à planifier des changements ultérieurs pour la documentation et les versions de nos produits.</span><span class="sxs-lookup"><span data-stu-id="f35c5-115">**Note** This email address is not a support channel, but your feedback will help us to plan future changes for our documentation and product releases.</span></span>

 

<span data-ttu-id="f35c5-116">Pour obtenir les informations les plus récentes sur MDOP et les ressources de formation supplémentaires, voir la page d' [utilisation de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="f35c5-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="f35c5-117">Pour en savoir plus sur les nouvelles mises à jour ou pour nous faire part de vos commentaires, suivez-nous sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="f35c5-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a><span data-ttu-id="f35c5-118">Problèmes connus liés à l’application-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="f35c5-118">Known Issues with App-V4.6SP2</span></span>


### <span data-ttu-id="f35c5-119">La prise en charge des noms de fichiers courts est désactivée pour les disques physiques non-systèmes lors de l’ordre</span><span class="sxs-lookup"><span data-stu-id="f35c5-119">Short file name support is disabled for non-system physical drives when you sequence</span></span>

<span data-ttu-id="f35c5-120">Lorsque vous séquencez sur Windows 8 ou Windows Server 2012, la prise en charge des noms de fichiers courts (8,3) est désactivée par défaut pour les lecteurs physiques non-système.</span><span class="sxs-lookup"><span data-stu-id="f35c5-120">When you sequence on Windows 8 or Windows Server 2012, support for short file names (8.3) is disabled by default for non-system physical drives.</span></span>

<span data-ttu-id="f35c5-121">Le disque physique sous-jacent associé au répertoire principal de l’application virtuelle (par exemple, «Q:\\appname») sur la station de séquençage doit fournir une prise en charge de nom de fichier court (8,3), afin que le Sequencer App-V 4.6 SP2 puisse générer des noms de fichiers courts lors de la création de packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="f35c5-121">The underlying physical drive associated with the primary virtual application directory (for example, “Q:\\appname”) on the sequencing station must provide short file name (8.3) support in order for the App-V4.6SP2 Sequencer to generate short file names when creating virtual application packages.</span></span> <span data-ttu-id="f35c5-122">La prise en charge des noms de fichiers courts (8,3) est désactivée par défaut pour les lecteurs physiques non-systèmes sur Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f35c5-122">Short file name (8.3) support is disabled by default for non-system physical drives on Windows 8 or Windows Server 2012.</span></span>

<span data-ttu-id="f35c5-123">**Solution de contournement:** Activer la prise en charge des noms de fichiers courts (8,3) sur les lecteurs physiques non-système.</span><span class="sxs-lookup"><span data-stu-id="f35c5-123">**Workaround:** Enable short file name (8.3) support on non-system physical drives.</span></span> <span data-ttu-id="f35c5-124">Vous pouvez utiliser la commande suivante pour activer la prise en charge des noms de fichiers courts sur Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f35c5-124">You can use the following command to enable short file name support on Windows 8 or Windows Server 2012.</span></span>

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

<span data-ttu-id="f35c5-125">Par exemple, utilisez la commande suivante si la lettre de lecteur est «Q:»:</span><span class="sxs-lookup"><span data-stu-id="f35c5-125">For example, use the following command if the drive letter is “Q:”:</span></span>

``` syntax
fsutil 8dot3name set Q: 0
```

<span data-ttu-id="f35c5-126">**Remarques**  Vous n’avez pas besoin de modifier ce paramètre sur le client App-V, car le système de fichiers App-V gère correctement les chemins d’accès courts sur Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f35c5-126">**Note** You do not need to change this setting on the App-V client because the App-V file system properly handles short paths on Windows 8 or Windows Server 2012.</span></span>

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> <span data-ttu-id="f35c5-127">App-V ne remplace pas le gestionnaire par défaut pour les associations de types de fichiers ou de protocoles sur Windows 8</span><span class="sxs-lookup"><span data-stu-id="f35c5-127">App-V does not override the default handler for file type or protocol associations on Windows 8</span></span>

<span data-ttu-id="f35c5-128">Si vous sélectionnez une application par défaut en utilisant les **programmes par défaut** du **panneau de configuration** dans Windows 8, l’application-V ne remplacera pas les associations de types de fichier associées pour cette application.</span><span class="sxs-lookup"><span data-stu-id="f35c5-128">If you select a default application by using **Default Programs** in **Control Panel** on Windows 8, App-V will not override the associated file type associations for that application.</span></span>

<span data-ttu-id="f35c5-129">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="f35c5-129">**Workaround:** None.</span></span>

### <span data-ttu-id="f35c5-130">La fonction de virtualisation d’Outlook 2010 n’est pas proposée comme option de liens sur Windows 8</span><span class="sxs-lookup"><span data-stu-id="f35c5-130">Virtualized Outlook 2010 is not offered as an option for mailto clickable links on Windows 8</span></span>

<span data-ttu-id="f35c5-131">L’extension d’interpréteur de formations mailto ne propose pas de services virtuels Outlook 2010 sur Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f35c5-131">The mailto shell extension does not offer virtualized Outlook 2010 on Windows 8.</span></span> <span data-ttu-id="f35c5-132">Par exemple, si vous cliquez sur un lien mailto: de Microsoft Outlook 2010 exécuté sur Windows 8, une nouvelle fenêtre de courrier n’est pas créée.</span><span class="sxs-lookup"><span data-stu-id="f35c5-132">For example, if you click a mailto: link from virtualized Outlook 2010 that is running on Windows 8, a new email window is not created.</span></span> <span data-ttu-id="f35c5-133">Cette option fonctionne correctement sur Windows 7 et les versions antérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="f35c5-133">This option works correctly on Windows 7 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="f35c5-134">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="f35c5-134">**Workaround:** None.</span></span>

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> <span data-ttu-id="f35c5-135">La mise à jour du SP2 Application Virtualization 4,6 n’est pas disponible sur les paramètres régionaux qui utilisent Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="f35c5-135">Application Virtualization 4.6 SP2 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="f35c5-136">Lorsque vous utilisez Microsoft Update, la mise à jour pour App-V 4.6 SP2 n’est pas disponible pour les paramètres régionaux de langue suivants:</span><span class="sxs-lookup"><span data-stu-id="f35c5-136">When you use Microsoft Update, the update for App-V4.6SP2 is not available for the following language locales:</span></span>

-   <span data-ttu-id="f35c5-137">Kazakh</span><span class="sxs-lookup"><span data-stu-id="f35c5-137">Kazakh</span></span>

-   <span data-ttu-id="f35c5-138">Hindi</span><span class="sxs-lookup"><span data-stu-id="f35c5-138">Hindi</span></span>

-   <span data-ttu-id="f35c5-139">Serbe-cyrillique</span><span class="sxs-lookup"><span data-stu-id="f35c5-139">Serbian-Cyrillic</span></span>

<span data-ttu-id="f35c5-140">**Solution de contournement:** Si vous utilisez Microsoft Windows Server Update Services (WSUS), utilisez la version anglaise de la mise à jour ou téléchargez la mise à jour à partir du catalogue Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="f35c5-140">**Workaround:** If you are using Microsoft Windows Server Update Services (WSUS), use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

## <span data-ttu-id="f35c5-141">Informations de copyright des notes de publication</span><span class="sxs-lookup"><span data-stu-id="f35c5-141">Release Notes Copyright Information</span></span>


<span data-ttu-id="f35c5-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f35c5-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="f35c5-143">Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="f35c5-143">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="f35c5-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f35c5-144">Related topics</span></span>


[<span data-ttu-id="f35c5-145">À propos de Microsoft Application Virtualization4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="f35c5-145">About Microsoft Application Virtualization 4.6 SP2</span></span>](about-microsoft-application-virtualization-46-sp2.md)

 

 






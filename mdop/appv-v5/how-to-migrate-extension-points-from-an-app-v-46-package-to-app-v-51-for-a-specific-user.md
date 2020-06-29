---
title: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique
description: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805299"
---
# <span data-ttu-id="f7b24-103">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f7b24-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>


<span data-ttu-id="f7b24-104">Utilisez la procédure suivante pour migrer des packages créés avec App-V à l’aide du fichier de configuration utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f7b24-104">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

<span data-ttu-id="f7b24-105">**Remarques**  Cette procédure suppose que vous utilisez la dernière version de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="f7b24-105">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>

**<span data-ttu-id="f7b24-106">Pour convertir un package</span><span class="sxs-lookup"><span data-stu-id="f7b24-106">To convert a package</span></span>**

1. <span data-ttu-id="f7b24-107">Recherchez le fichier de configuration utilisateur pour le package que vous voulez convertir.</span><span class="sxs-lookup"><span data-stu-id="f7b24-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="f7b24-108">Pour définir la stratégie, effectuez les mises à jour suivantes dans la section **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; du package**.</span><span class="sxs-lookup"><span data-stu-id="f7b24-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="f7b24-109">Voici un exemple de fichier de configuration utilisateur:</span><span class="sxs-lookup"><span data-stu-id="f7b24-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="f7b24-110">&lt;? XML version = "1.0"&gt;</span><span class="sxs-lookup"><span data-stu-id="f7b24-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="f7b24-111">&lt;UserConfiguration PackageId = &lt; ID &gt; de package DisplayName = &lt; nom du package&gt;</span><span class="sxs-lookup"><span data-stu-id="f7b24-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="f7b24-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="f7b24-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="f7b24-113">PackageName = &lt; ID de package&gt;</span><span class="sxs-lookup"><span data-stu-id="f7b24-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="f7b24-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="f7b24-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="f7b24-115">Pour ajouter le package App-V 5,1, tapez les informations suivantes dans la fenêtre d’invite de commandes PowerShell avec élévation de privilèges:</span><span class="sxs-lookup"><span data-stu-id="f7b24-115">To add the App-V 5.1 package, type the following in an elevated PowerShell command prompt window:</span></span>

   <span data-ttu-id="f7b24-116">PS &gt; **$pkg = Add-AppvClientPackage-** Path &lt; pour l’emplacement du package&gt;</span><span class="sxs-lookup"><span data-stu-id="f7b24-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="f7b24-117">&gt;**Publication PS-AppVClientPackage $pkg-chemin DynamicUserConfiguration** &lt; du fichier de configuration de l’utilisateur&gt;</span><span class="sxs-lookup"><span data-stu-id="f7b24-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="f7b24-118">Ouvrez l’application à l’aide de FTAs ou raccourcis.</span><span class="sxs-lookup"><span data-stu-id="f7b24-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="f7b24-119">L’application doit s’ouvrir à l’aide de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f7b24-119">The application should open using App-V 5.1.</span></span>

   <span data-ttu-id="f7b24-120">Le package App-V 4,6 et le package App-V 5,1 convertis sont publiés pour l’utilisateur, mais les FTAs et raccourcis des applications ont été supposés par le package App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f7b24-120">The App-V 4.6 package and the converted App-V 5.1 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.1 package.</span></span>

   <span data-ttu-id="f7b24-121">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="f7b24-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f7b24-122">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="f7b24-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f7b24-123">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="f7b24-123">Got an App-V issue?</span></span>** <span data-ttu-id="f7b24-124">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f7b24-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f7b24-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7b24-125">Related topics</span></span>


[<span data-ttu-id="f7b24-126">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="f7b24-126">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="f7b24-127">Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f7b24-127">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 






---
title: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique
description: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805305"
---
# <span data-ttu-id="0aa52-103">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="0aa52-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>

<span data-ttu-id="0aa52-104">*Remarque:*\* App-V 4,6 a quitté la version standard du support technique.</span><span class="sxs-lookup"><span data-stu-id="0aa52-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="0aa52-105">Utilisez la procédure suivante pour migrer des packages créés avec App-V à l’aide du fichier de configuration utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0aa52-105">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

**<span data-ttu-id="0aa52-106">Pour convertir un package</span><span class="sxs-lookup"><span data-stu-id="0aa52-106">To convert a package</span></span>**

1. <span data-ttu-id="0aa52-107">Recherchez le fichier de configuration utilisateur pour le package que vous voulez convertir.</span><span class="sxs-lookup"><span data-stu-id="0aa52-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="0aa52-108">Pour définir la stratégie, effectuez les mises à jour suivantes dans la section **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; du package**.</span><span class="sxs-lookup"><span data-stu-id="0aa52-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="0aa52-109">Voici un exemple de fichier de configuration utilisateur:</span><span class="sxs-lookup"><span data-stu-id="0aa52-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="0aa52-110">&lt;? XML version = "1.0"&gt;</span><span class="sxs-lookup"><span data-stu-id="0aa52-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="0aa52-111">&lt;UserConfiguration PackageId = &lt; ID &gt; de package DisplayName = &lt; nom du package&gt;</span><span class="sxs-lookup"><span data-stu-id="0aa52-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="0aa52-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="0aa52-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="0aa52-113">PackageName = &lt; ID de package&gt;</span><span class="sxs-lookup"><span data-stu-id="0aa52-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="0aa52-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="0aa52-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="0aa52-115">Pour ajouter le package App-V 5,0, tapez ce qui suit dans une invite de commandes PowerShell avec élévation de privilèges:</span><span class="sxs-lookup"><span data-stu-id="0aa52-115">To add the App-V 5.0 package type the following in an elevated PowerShell command prompt:</span></span>

   <span data-ttu-id="0aa52-116">PS &gt; **$pkg = Add-AppvClientPackage-** Path &lt; pour l’emplacement du package&gt;</span><span class="sxs-lookup"><span data-stu-id="0aa52-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="0aa52-117">&gt;**Publication PS-AppVClientPackage $pkg-chemin DynamicUserConfiguration** &lt; du fichier de configuration de l’utilisateur&gt;</span><span class="sxs-lookup"><span data-stu-id="0aa52-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="0aa52-118">Ouvrez l’application à l’aide de FTAs ou raccourcis.</span><span class="sxs-lookup"><span data-stu-id="0aa52-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="0aa52-119">L’application doit s’ouvrir à l’aide de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0aa52-119">The application should open using App-V 5.0.</span></span>

   <span data-ttu-id="0aa52-120">Le package App-V SP2 et le package App-V 5,0 converti sont publiés pour l’utilisateur, mais les FTAs et raccourcis des applications ont été supposés par le package App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0aa52-120">The App-V SP2 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="0aa52-121">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="0aa52-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="0aa52-122">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="0aa52-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="0aa52-123">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="0aa52-123">Got an App-V issue?</span></span>** <span data-ttu-id="0aa52-124">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="0aa52-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="0aa52-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0aa52-125">Related topics</span></span>


[<span data-ttu-id="0aa52-126">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="0aa52-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 






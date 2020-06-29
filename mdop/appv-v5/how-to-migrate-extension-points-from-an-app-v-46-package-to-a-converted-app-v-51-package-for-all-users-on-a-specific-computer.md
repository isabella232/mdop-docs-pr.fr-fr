---
title: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique
description: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique
author: dansimp
ms.assetid: 4ef823a5-3106-44c5-aecc-29edf69c2fbb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 7bac244804b46309a0e0a75cb3742dfe22e92e8f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805310"
---
# <span data-ttu-id="f01ba-103">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f01ba-103">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>


<span data-ttu-id="f01ba-104">Utilisez la procédure suivante pour migrer des points d’extension d’un package App-V 4.6 vers un package App-V 5,1 à l’aide du fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="f01ba-104">Use the following procedure to migrate extension points from an App-V4.6 package to a App-V 5.1 package using the deployment configuration file.</span></span>

<span data-ttu-id="f01ba-105">**Remarques**  Cette procédure suppose que vous utilisez la dernière version de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="f01ba-105">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>  
<span data-ttu-id="f01ba-106">La procédure suivante ne nécessite pas de serveur de gestion 5,1 App-V.</span><span class="sxs-lookup"><span data-stu-id="f01ba-106">The following procedure does not require an App-V 5.1 management server.</span></span>

 

**<span data-ttu-id="f01ba-107">Pour migrer des points d’extension d’un package d’un package App-V 4.6 vers un package App-V 5,1 converti à l’aide du fichier de configuration de déploiement</span><span class="sxs-lookup"><span data-stu-id="f01ba-107">To migrate extension points from a package from an App-V4.6 package to a converted App-V 5.1 package using the deployment configuration file</span></span>**

1. <span data-ttu-id="f01ba-108">Recherchez le répertoire contenant le fichier de configuration de déploiement pour le package que vous voulez migrer.</span><span class="sxs-lookup"><span data-stu-id="f01ba-108">Locate the directory that contains the deployment configuration file for the package you want to migrate.</span></span> <span data-ttu-id="f01ba-109">Pour définir la stratégie, effectuez la mise à jour suivante vers la section **userConfiguration** :</span><span class="sxs-lookup"><span data-stu-id="f01ba-109">To set the policy, make the following update to the **userConfiguration** section:</span></span>

   **<span data-ttu-id="f01ba-110">ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID de package&gt;</span><span class="sxs-lookup"><span data-stu-id="f01ba-110">ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;</span></span>**

   <span data-ttu-id="f01ba-111">Voici un exemple de contenu d’un fichier de configuration de déploiement:</span><span class="sxs-lookup"><span data-stu-id="f01ba-111">The following is an example of content from a deployment configuration file:</span></span>

   <span data-ttu-id="f01ba-112">&lt;? XML version = "1.0"&gt;</span><span class="sxs-lookup"><span data-stu-id="f01ba-112">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="f01ba-113">&lt;DeploymentConfiguration</span><span class="sxs-lookup"><span data-stu-id="f01ba-113">&lt;DeploymentConfiguration</span></span>

   <span data-ttu-id="f01ba-114">xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageId = &lt; ID de package &gt; DisplayName = &lt; nom d’affichage&gt;</span><span class="sxs-lookup"><span data-stu-id="f01ba-114">xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration>" PackageId=&lt;Package ID&gt; DisplayName=&lt;Display Name&gt;</span></span>

   <span data-ttu-id="f01ba-115">&lt;MachineConfiguration/&gt;</span><span class="sxs-lookup"><span data-stu-id="f01ba-115">&lt;MachineConfiguration/&gt;</span></span>

   <span data-ttu-id="f01ba-116">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="f01ba-116">&lt;UserConfiguration&gt;</span></span>

   <span data-ttu-id="f01ba-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="f01ba-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="f01ba-118">PackageName = &lt; ID de package&gt;</span><span class="sxs-lookup"><span data-stu-id="f01ba-118">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="f01ba-119">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="f01ba-119">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="f01ba-120">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="f01ba-120">&lt;/DeploymentConfiguration&gt;</span></span>

2. <span data-ttu-id="f01ba-121">Pour ajouter le package App-V 5,1, dans une invite de commandes PowerShell avec élévation de privilèges, tapez:</span><span class="sxs-lookup"><span data-stu-id="f01ba-121">To add the App-V 5.1 package, in an elevated PowerShell command prompt type:</span></span>

   <span data-ttu-id="f01ba-122">PS &gt; **$pkg = Add-AppvClientPackage** **-** Path &lt; pour l’emplacement du package &gt;  - **DynamicDeploymentConfiguration** chemin d’accès &lt; au fichier de configuration de déploiement&gt;</span><span class="sxs-lookup"><span data-stu-id="f01ba-122">PS&gt;**$pkg= Add-AppvClientPackage** **–Path** &lt;Path to package location&gt; -**DynamicDeploymentConfiguration** &lt;Path to the deployment configuration file&gt;</span></span>

   <span data-ttu-id="f01ba-123">&gt;**Publication PS-AppVClientPackage $pkg**</span><span class="sxs-lookup"><span data-stu-id="f01ba-123">PS&gt;**Publish-AppVClientPackage $pkg**</span></span>

3. <span data-ttu-id="f01ba-124">Pour tester la migration, ouvrez l’application virtuelle à l’aide de FTAs ou raccourcis associés.</span><span class="sxs-lookup"><span data-stu-id="f01ba-124">To test the migration, open the virtual application using associated FTAs or shortcuts.</span></span> <span data-ttu-id="f01ba-125">L’application s’ouvre avec App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f01ba-125">The application opens with App-V 5.1.</span></span> <span data-ttu-id="f01ba-126">À la fois, le package App-V 4,6 et le package App-V 5,1 convertis sont publiés pour l’utilisateur, mais les FTAs et raccourcis des applications ont été supposés par le package App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f01ba-126">Both, the App-V 4.6 package and the converted App-V 5.1 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.1 package.</span></span>

   <span data-ttu-id="f01ba-127">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="f01ba-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f01ba-128">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="f01ba-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f01ba-129">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="f01ba-129">Got an App-V issue?</span></span>** <span data-ttu-id="f01ba-130">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f01ba-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f01ba-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f01ba-131">Related topics</span></span>


[<span data-ttu-id="f01ba-132">Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f01ba-132">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="f01ba-133">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="f01ba-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 






---
title: Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique
description: Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique
author: dansimp
ms.assetid: 64640b8e-de6b-4006-a33e-353d285af15e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: ce8d5cc0e79be46fd9680a3bea0236bbeb93ea83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805191"
---
# <span data-ttu-id="60e24-103">Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="60e24-103">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>


<span data-ttu-id="60e24-104">Utilisez la procédure suivante pour rétablir les points d’extension d’un package App-V 5,1 au format de fichier App-V 4,6 à l’aide du fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="60e24-104">Use the following procedure to revert extension points from an App-V 5.1 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="60e24-105">Pour rétablir un package</span><span class="sxs-lookup"><span data-stu-id="60e24-105">To revert a package</span></span>**

1.  <span data-ttu-id="60e24-106">Assurez-vous que le package App-V 4,6 est publié pour les utilisateurs, mais que les FTAs et raccourcis ont été supposés par le package App-v 5,1 à l’aide de la méthode de migration suivante, [Comment migrer des points d’extension d’un package App-v 4,6 vers un package App-v 5,1 pour tous les utilisateurs sur un ordinateur en particulier](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="60e24-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="60e24-107">Dans la section **userConfiguration** du fichier de configuration de déploiement pour le package converti, pour définir la stratégie, effectuez la mise à jour suivante vers la section **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "FALSe" PackageName = &lt; &gt; ID de package**</span><span class="sxs-lookup"><span data-stu-id="60e24-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="60e24-108">À partir d’une invite de commandes avec élévation de privilèges, tapez:</span><span class="sxs-lookup"><span data-stu-id="60e24-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="60e24-109">PS &gt; **Set-AppvClientPackage $pkg – chemin DynamicDeploymentConfiguration** &lt; au fichier de configuration de déploiement&gt;</span><span class="sxs-lookup"><span data-stu-id="60e24-109">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="60e24-110">&gt;**Publication PS-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="60e24-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="60e24-111">Effectue une actualisation de publication ou attend la prochaine actualisation de publication planifiée pour le package App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="60e24-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 package.</span></span>

    <span data-ttu-id="60e24-112">Ouvrez l’application à l’aide de FTAs ou de raccourcis.</span><span class="sxs-lookup"><span data-stu-id="60e24-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="60e24-113">L’application doit maintenant s’ouvrir à l’aide de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="60e24-113">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="60e24-114">Remarque</span><span class="sxs-lookup"><span data-stu-id="60e24-114">Note</span></span>**  
    <span data-ttu-id="60e24-115">Si vous n’avez plus besoin du package App-V 5,1, vous pouvez annuler la publication du package App-V 5,1 et les points d’extension seront automatiquement rétablis sur App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="60e24-115">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="60e24-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60e24-116">Related topics</span></span>


[<span data-ttu-id="60e24-117">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="60e24-117">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)










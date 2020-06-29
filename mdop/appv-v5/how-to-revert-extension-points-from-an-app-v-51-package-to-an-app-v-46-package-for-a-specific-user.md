---
title: Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour un utilisateur spécifique
description: Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour un utilisateur spécifique
author: dansimp
ms.assetid: bd53c5d6-7fd2-4816-b03b-d59da0a35819
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a69d6fb5b180161f39aa89e03b52227f32ce4879
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805197"
---
# <span data-ttu-id="19e5d-103">Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="19e5d-103">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>


<span data-ttu-id="19e5d-104">Utilisez la procédure suivante pour rétablir le format de fichier App-V 5,1 dans le fichier de configuration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="19e5d-104">Use the following procedure to revert an App-V 5.1 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="19e5d-105">Pour rétablir un package</span><span class="sxs-lookup"><span data-stu-id="19e5d-105">To revert a package</span></span>**

1.  <span data-ttu-id="19e5d-106">Assurez-vous que le package App-V 4,6 est publié pour les utilisateurs, mais que les FTAs et raccourcis sont utilisés par le package App-v 5,1 à l’aide de la méthode de migration suivante, [Comment migrer des points d’extension d’un package App-v 4,6 vers App-v 5,1 pour un utilisateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="19e5d-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span></span>

    <span data-ttu-id="19e5d-107">Dans la section **userConfiguration** du fichier de configuration de déploiement pour le package converti, pour définir la stratégie, effectuez la mise à jour suivante vers la section **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "FALSe" PackageName = &lt; &gt; ID de package**</span><span class="sxs-lookup"><span data-stu-id="19e5d-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="19e5d-108">À partir d’une invite de commandes avec élévation de privilèges, tapez:</span><span class="sxs-lookup"><span data-stu-id="19e5d-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="19e5d-109">&gt;**Publication PS-AppVClientPackage $pkg – chemin DynamicUserConfigurationPath** &lt; au fichier de configuration utilisateur&gt;</span><span class="sxs-lookup"><span data-stu-id="19e5d-109">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="19e5d-110">Effectuez une actualisation de publication ou attendez la prochaine actualisation planifiée pour l’App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="19e5d-110">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="19e5d-111">Ouvrez l’application à l’aide de FTAs ou de raccourcis.</span><span class="sxs-lookup"><span data-stu-id="19e5d-111">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="19e5d-112">L’application doit maintenant s’ouvrir à l’aide de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="19e5d-112">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="19e5d-113">Remarque</span><span class="sxs-lookup"><span data-stu-id="19e5d-113">Note</span></span>**  
    <span data-ttu-id="19e5d-114">Si vous n’avez plus besoin du package App-V 5,1, vous pouvez annuler la publication du package App-V 5,1 et les points d’extension seront automatiquement rétablis sur App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="19e5d-114">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="19e5d-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19e5d-115">Related topics</span></span>


[<span data-ttu-id="19e5d-116">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="19e5d-116">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)










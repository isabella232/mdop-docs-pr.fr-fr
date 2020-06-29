---
title: Restauration de points d'extension d'un package App-V5.0 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique
description: Restauration de points d'extension d'un package App-V5.0 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805196"
---
# <span data-ttu-id="96410-103">Restauration de points d'extension d'un package App-V5.0 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="96410-103">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>

<span data-ttu-id="96410-104">*Remarque:*\* App-V 4,6 a quitté la version standard du support technique.</span><span class="sxs-lookup"><span data-stu-id="96410-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="96410-105">L’exemple suivant suppose que le client App-V 4,6 SP3 est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="96410-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="96410-106">Utilisez la procédure suivante pour rétablir les points d’extension d’un package App-V 5,0 au format de fichier App-V 4,6 à l’aide du fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="96410-106">Use the following procedure to revert extension points from an App-V 5.0 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="96410-107">Pour rétablir un package</span><span class="sxs-lookup"><span data-stu-id="96410-107">To revert a package</span></span>**

1.  <span data-ttu-id="96410-108">Assurez-vous que le package App-V 4,6 est publié pour les utilisateurs, mais que les FTAs et raccourcis ont été supposés par le package App-v 5,0 à l’aide de la méthode de migration suivante, [Comment migrer des points d’extension d’un package App-v 4,6 vers un package App-v 5,0 pour tous les utilisateurs sur un ordinateur en particulier](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="96410-108">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="96410-109">Dans la section **userConfiguration** du fichier de configuration de déploiement pour le package converti, pour définir la stratégie, effectuez la mise à jour suivante vers la section **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "FALSe" PackageName = &lt; &gt; ID de package**</span><span class="sxs-lookup"><span data-stu-id="96410-109">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="96410-110">À partir d’une invite de commandes avec élévation de privilèges, tapez:</span><span class="sxs-lookup"><span data-stu-id="96410-110">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="96410-111">PS &gt; **Set-AppvClientPackage $pkg – chemin DynamicDeploymentConfiguration** &lt; au fichier de configuration de déploiement&gt;</span><span class="sxs-lookup"><span data-stu-id="96410-111">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="96410-112">&gt;**Publication PS-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="96410-112">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="96410-113">Effectue une actualisation de publication ou attend la prochaine actualisation de publication planifiée pour le package App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="96410-113">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 SP2 package.</span></span>

    <span data-ttu-id="96410-114">Ouvrez l’application à l’aide de FTAs ou de raccourcis.</span><span class="sxs-lookup"><span data-stu-id="96410-114">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="96410-115">L’application doit maintenant s’ouvrir à l’aide de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="96410-115">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="96410-116">Remarque</span><span class="sxs-lookup"><span data-stu-id="96410-116">Note</span></span>**  
    <span data-ttu-id="96410-117">Si vous n’avez plus besoin du package App-V 5,0, vous pouvez annuler la publication du package App-V 5,0 et les points d’extension seront automatiquement rétablis sur App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="96410-117">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="96410-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96410-118">Related topics</span></span>


[<span data-ttu-id="96410-119">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="96410-119">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)










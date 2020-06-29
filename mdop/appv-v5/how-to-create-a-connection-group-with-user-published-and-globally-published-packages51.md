---
title: Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement
description: Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement
author: dansimp
ms.assetid: 851b8742-0283-4aa6-b3a3-f7f6289824c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 230e687360920c05a214624750eba54dc84b5731
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805671"
---
# <span data-ttu-id="34225-103">Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement</span><span class="sxs-lookup"><span data-stu-id="34225-103">How to Create a Connection Group with User-Published and Globally Published Packages</span></span>


<span data-ttu-id="34225-104">Vous pouvez créer des groupes de connexion habilités par l’utilisateur qui contiennent des packages publiés par l’utilisateur et globalement publiés, en utilisant l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="34225-104">You can create user-entitled connection groups that contain both user-published and globally published packages, using either of the following methods:</span></span>

-   [<span data-ttu-id="34225-105">Comment utiliser les applets de connexion PowerShell pour créer des groupes de connexion habilités par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="34225-105">How to use PowerShell cmdlets to create the user-entitled connection groups</span></span>](#bkmk-posh-userentitled-cg)

-   [<span data-ttu-id="34225-106">Utilisation du serveur App-V pour créer des groupes de connexion autorisés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="34225-106">How to use the App-V Server to create the user-entitled connection groups</span></span>](#bkmk-appvserver-userentitled-cg)

**<span data-ttu-id="34225-107">Ce que vous devez savoir avant de commencer:</span><span class="sxs-lookup"><span data-stu-id="34225-107">What to know before you start:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="34225-108">Scénarios non pris en charge et problèmes potentiels</span><span class="sxs-lookup"><span data-stu-id="34225-108">Unsupported scenarios and potential issues</span></span></th>
<th align="left"><span data-ttu-id="34225-109">Résultat</span><span class="sxs-lookup"><span data-stu-id="34225-109">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34225-110">Vous ne pouvez pas inclure de packages publiés par l’utilisateur dans les groupes de connexion globalement autorisés.</span><span class="sxs-lookup"><span data-stu-id="34225-110">You cannot include user-published packages in globally entitled connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="34225-111">Le groupe de connexion ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="34225-111">The connection group will fail.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34225-112">Si vous publiez un package dans le monde entier, puis créez un groupe de connexion publié par un utilisateur qui n’est pas facultatif, vous pouvez toujours exécuter <strong> unpublisher-AppvClientPackage &lt; package &gt; -global </strong> pour annuler la publication du package, même si ce package est utilisé dans un autre groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="34225-112">If you publish a package globally and then create a user-published connection group in which you’ve made that package non-optional, you can still run <strong>Unpublish-AppvClientPackage &lt;package&gt; -global</strong> to unpublish the package, even when that package is being used in another connection group.</span></span></p></td>
<td align="left"><p><span data-ttu-id="34225-113">S’il s’agit d’un autre groupe de connexion utilisant ce package, le package échouera dans ces groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="34225-113">If any other connection groups are using that package, the package will fail in those connection groups.</span></span></p>
<p><span data-ttu-id="34225-114">Pour éviter d’annuler accidentellement la publication d’un package non facultatif utilisé dans un autre groupe de connexion, nous vous recommandons d’effectuer le suivi des groupes de connexion dans lesquels vous avez utilisé un package non facultatif.</span><span class="sxs-lookup"><span data-stu-id="34225-114">To avoid inadvertently unpublishing a non-optional package that is being used in another connection group, we recommend that you track the connection groups in which you’ve used a non-optional package.</span></span></p></td>
</tr>
</tbody>
</table>

<a href="" id="bkmk-posh-userentitled-cg"></a>**<span data-ttu-id="34225-115">Comment utiliser les cmdlets PowerShell pour créer des groupes de connexion qui ont été autorisés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="34225-115">How to use PowerShell cmdlets to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="34225-116">Ajoutez des packages et publiez-les à l’aide des commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="34225-116">Add and publish packages by using the following commands:</span></span>

    **<span data-ttu-id="34225-117">Add-AppvClientPackage package1 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="34225-117">Add-AppvClientPackage Package1\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="34225-118">Add-AppvClientPackage package2 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="34225-118">Add-AppvClientPackage Package2\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="34225-119">Publisher-AppvClientPackage-PackageId package1 \ _ID-VersionId package1 \ _Version ID-global</span><span class="sxs-lookup"><span data-stu-id="34225-119">Publish-AppvClientPackage -PackageId Package1\_ID-VersionId Package1\_Version ID -Global</span></span>**

    **<span data-ttu-id="34225-120">Publisher-AppvClientPackage-PackageId package2 \ _ID-VersionIdPackage2 \ _ID</span><span class="sxs-lookup"><span data-stu-id="34225-120">Publish-AppvClientPackage -PackageId Package2\_ID -VersionIdPackage2\_ID</span></span>**

2.  <span data-ttu-id="34225-121">Créez le fichier XML de groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="34225-121">Create the connection group XML file.</span></span> <span data-ttu-id="34225-122">Pour plus d’informations, consultez [à propos du fichier de groupe de connexion](about-the-connection-group-file51.md).</span><span class="sxs-lookup"><span data-stu-id="34225-122">For more information, see [About the Connection Group File](about-the-connection-group-file51.md).</span></span>

3.  <span data-ttu-id="34225-123">Ajoutez et publiez le groupe de connexions en utilisant les commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="34225-123">Add and publish the connection group by using the following commands:</span></span>

    **<span data-ttu-id="34225-124">Connexion Add-AppvClientConnectionGroup \ _Group \ _XML \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="34225-124">Add-AppvClientConnectionGroup Connection\_Group\_XML\_file\_Path</span></span>**

    **<span data-ttu-id="34225-125">Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-CG CG \ _Version \ _ID</span><span class="sxs-lookup"><span data-stu-id="34225-125">Enable-AppvClientConnectionGroup -GroupId CG\_Group\_ID-VersionId CG\_Version\_ID</span></span>**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**<span data-ttu-id="34225-126">Utilisation du serveur App-V pour créer des groupes de connexion autorisés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="34225-126">How to use the App-V Server to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="34225-127">Ouvrez la console de gestion App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="34225-127">Open the App-V 5.1 Management Console.</span></span>

2.  <span data-ttu-id="34225-128">Suivez les instructions de la [procédure de publication d’un package à l’aide de la console de gestion](how-to-publish-a-package-by-using-the-management-console-51.md) pour publier des packages globalement et pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="34225-128">Follow the instructions in [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md) to publish packages globally and to the user.</span></span>

3.  <span data-ttu-id="34225-129">Suivez les instructions de la [procédure de création d’un groupe de connexion](how-to-create-a-connection-group51.md) pour créer le groupe de connexion et ajouter les packages publiés par l’utilisateur et publiés globalement.</span><span class="sxs-lookup"><span data-stu-id="34225-129">Follow the instructions in [How to Create a Connection Group](how-to-create-a-connection-group51.md) to create the connection group, and add the user-published and globally published packages.</span></span>

    <span data-ttu-id="34225-130">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="34225-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="34225-131">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="34225-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="34225-132">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="34225-132">Got an App-V issue?</span></span>** <span data-ttu-id="34225-133">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="34225-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="34225-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34225-134">Related topics</span></span>


[<span data-ttu-id="34225-135">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="34225-135">Managing Connection Groups</span></span>](managing-connection-groups51.md)

[<span data-ttu-id="34225-136">Comment utiliser des packages facultatifs dans les groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="34225-136">How to Use Optional Packages in Connection Groups</span></span>](how-to-use-optional-packages-in-connection-groups51.md)

 

 






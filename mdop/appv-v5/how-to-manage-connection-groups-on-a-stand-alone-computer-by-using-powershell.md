---
title: Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell
description: Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell
author: dansimp
ms.assetid: b73ae74d-8a6f-4bb3-b1f2-0067c7bd5212
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 32dd4f9c5ad1ba4ae9e25246d5ec52a6363ef303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805341"
---
# <span data-ttu-id="a74c9-103">Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a74c9-103">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span>


<span data-ttu-id="a74c9-104">Un groupe de connexion App-V vous permet d’exécuter toutes les applications virtuelles en tant qu’ensemble de packages définis dans un environnement virtuel unique.</span><span class="sxs-lookup"><span data-stu-id="a74c9-104">An App-V connection group allows you to run all the virtual applications as a defined set of packages in a single virtual environment.</span></span> <span data-ttu-id="a74c9-105">Par exemple, vous pouvez virtualiser une application et ses plug-ins en utilisant des packages distincts, mais les exécuter au sein d’un groupe de connexion unique.</span><span class="sxs-lookup"><span data-stu-id="a74c9-105">For example, you can virtualize an application and its plug-ins by using separate packages, but run them together in a single connection group.</span></span>

<span data-ttu-id="a74c9-106">Un fichier XML de groupe de connexion définit le groupe de connexion qui s’exécute sur l’ordinateur sur lequel vous avez installé le client App-V.</span><span class="sxs-lookup"><span data-stu-id="a74c9-106">A connection group XML file defines the connection group that runs on the computer where you’ve installed the App-V client.</span></span> <span data-ttu-id="a74c9-107">Pour plus d’informations sur le fichier XML du groupe de connexion et sur la manière de le configurer, voir [à propos du fichier de groupe de connexion](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="a74c9-107">For information about the connection group XML file and how to configure it, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

<span data-ttu-id="a74c9-108">Cette rubrique décrit les procédures suivantes:</span><span class="sxs-lookup"><span data-stu-id="a74c9-108">This topic explains the following procedures:</span></span>

-   [<span data-ttu-id="a74c9-109">Pour ajouter et publier les packages App-V dans le groupe de connexions</span><span class="sxs-lookup"><span data-stu-id="a74c9-109">To add and publish the App-V packages in the connection group</span></span>](#bkmk-add-pub-pkgs-in-cg)

-   [<span data-ttu-id="a74c9-110">Pour ajouter et activer le groupe de connexions sur le client App-V</span><span class="sxs-lookup"><span data-stu-id="a74c9-110">To add and enable the connection group on the App-V client</span></span>](#bkmk-add-enable-cg-on-clt)

-   [<span data-ttu-id="a74c9-111">Pour activer ou désactiver un groupe de connexions pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="a74c9-111">To enable or disable a connection group for a specific user</span></span>](#bkmk-enable-cg-for-user-poshtopic)

-   [<span data-ttu-id="a74c9-112">Pour autoriser seuls les administrateurs à activer les groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="a74c9-112">To allow only administrators to enable connection groups</span></span>](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>**<span data-ttu-id="a74c9-113">Pour ajouter et publier les packages App-V dans le groupe de connexions</span><span class="sxs-lookup"><span data-stu-id="a74c9-113">To add and publish the App-V packages in the connection group</span></span>**

1.  <span data-ttu-id="a74c9-114">Pour ajouter et publier les packages App-V 5,0 sur l’ordinateur exécutant le client App-V, tapez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="a74c9-114">To add and publish the App-V 5.0 packages to the computer running the App-V client, type the following command:</span></span>

    <span data-ttu-id="a74c9-115">Add-AppvClientPackage-path c:\\tmpstore\\quartfin.AppV | Publisher-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="a74c9-115">Add-AppvClientPackage –path c:\\tmpstore\\quartfin.appv | Publish-AppvClientPackage</span></span>

2.  <span data-ttu-id="a74c9-116">Répétez l' **étape 1** de cette procédure pour chaque package dans le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="a74c9-116">Repeat **step 1** of this procedure for each package in the connection group.</span></span>

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**<span data-ttu-id="a74c9-117">Pour ajouter et activer le groupe de connexions sur le client App-V</span><span class="sxs-lookup"><span data-stu-id="a74c9-117">To add and enable the connection group on the App-V client</span></span>**

1.  <span data-ttu-id="a74c9-118">Ajoutez le groupe de connexions en entrant la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="a74c9-118">Add the connection group by typing the following command:</span></span>

    <span data-ttu-id="a74c9-119">Add-AppvClientConnectionGroup-Path c:\\tmpstore\\financ.xml</span><span class="sxs-lookup"><span data-stu-id="a74c9-119">Add-AppvClientConnectionGroup –path c:\\tmpstore\\financ.xml</span></span>

2.  <span data-ttu-id="a74c9-120">Activez le groupe de connexions en entrant la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="a74c9-120">Enable the connection group by typing the following command:</span></span>

    <span data-ttu-id="a74c9-121">Enable-AppvClientConnectionGroup – nom «applications financières»</span><span class="sxs-lookup"><span data-stu-id="a74c9-121">Enable-AppvClientConnectionGroup –name “Financial Applications”</span></span>

    <span data-ttu-id="a74c9-122">Lorsque des applications virtuelles figurant dans les packages membres sont exécutées sur l’ordinateur cible, elles s’exécutent à l’intérieur de l’environnement virtuel du groupe de connexion et sont disponibles pour toutes les applications virtuelles dans les autres packages du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="a74c9-122">When any virtual applications that are in the member packages are run on the target computer, they will run inside the connection group’s virtual environment and will be available to all the virtual applications in the other packages in the connection group.</span></span>

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**<span data-ttu-id="a74c9-123">Pour activer ou désactiver un groupe de connexions pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="a74c9-123">To enable or disable a connection group for a specific user</span></span>**

1.  <span data-ttu-id="a74c9-124">Passez en revue la description du paramètre et la configuration requise:</span><span class="sxs-lookup"><span data-stu-id="a74c9-124">Review the parameter description and requirements:</span></span>

    -   <span data-ttu-id="a74c9-125">Ce paramètre permet à un administrateur d’activer ou de désactiver un groupe de connexion pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="a74c9-125">The parameter enables an administrator to enable or disable a connection group for a specific user.</span></span>

    -   <span data-ttu-id="a74c9-126">Pour utiliser ce paramètre, vous devez utiliser le correctif logiciel App-V 5,0 SP2 package 5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a74c9-126">You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

    -   <span data-ttu-id="a74c9-127">Vous pouvez exécuter cette cmdlet à partir de la session utilisateur ou administrateur.</span><span class="sxs-lookup"><span data-stu-id="a74c9-127">You can run this cmdlet from the user or administrator session.</span></span>

    -   <span data-ttu-id="a74c9-128">Vous devez être connecté avec des informations d’identification d’administrateur pour utiliser le paramètre.</span><span class="sxs-lookup"><span data-stu-id="a74c9-128">You must be logged in with administrative credentials to use the parameter.</span></span>

    -   <span data-ttu-id="a74c9-129">L’utilisateur final doit être connecté.</span><span class="sxs-lookup"><span data-stu-id="a74c9-129">The end user must be logged in.</span></span>

    -   <span data-ttu-id="a74c9-130">Vous devez indiquer l’identificateur de sécurité (SID) de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a74c9-130">You must provide the end user’s security identifier (SID).</span></span>

2.  <span data-ttu-id="a74c9-131">Utilisez les applets de commande suivantes, puis ajoutez le paramètre facultatif **-UserSid** **qui représente l’identificateur de sécurité** (SID) de l’utilisateur final:</span><span class="sxs-lookup"><span data-stu-id="a74c9-131">Use the following cmdlets, and add the optional **–UserSID** parameter, where **-UserSID** represents the end user’s security identifier (SID):</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a74c9-132">Applet de commande</span><span class="sxs-lookup"><span data-stu-id="a74c9-132">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="a74c9-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="a74c9-133">Examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a74c9-134">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="a74c9-134">Enable-AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a74c9-135">Enable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="a74c9-135">Enable-AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a74c9-136">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="a74c9-136">Disable -AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a74c9-137">Disable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="a74c9-137">Disable -AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**<span data-ttu-id="a74c9-138">Pour autoriser seuls les administrateurs à activer les groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="a74c9-138">To allow only administrators to enable connection groups</span></span>**

1.  <span data-ttu-id="a74c9-139">Passez en revue la description et la configuration requise pour l’utilisation de cette cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a74c9-139">Review the description and requirement for using this cmdlet:</span></span>

    -   <span data-ttu-id="a74c9-140">Utilisez cette cmdlet et ce paramètre pour configurer le client App-V de façon à ce que seuls les administrateurs (et non les utilisateurs finaux) puissent activer ou désactiver les groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="a74c9-140">Use this cmdlet and parameter to configure the App-V client to allow only administrators (not end users) to enable or disable connection groups.</span></span>

    -   <span data-ttu-id="a74c9-141">Vous devez utiliser au minimum App-V 5,0 SP3 pour pouvoir utiliser cette applet de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a74c9-141">You must be using at least App-V 5.0 SP3 to use this cmdlet.</span></span>

2.  <span data-ttu-id="a74c9-142">Exécutez l’applet de commande et le paramètre suivants:</span><span class="sxs-lookup"><span data-stu-id="a74c9-142">Run the following cmdlet and parameter:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a74c9-143">Applet de commande</span><span class="sxs-lookup"><span data-stu-id="a74c9-143">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="a74c9-144">Paramètre et valeurs</span><span class="sxs-lookup"><span data-stu-id="a74c9-144">Parameter and values</span></span></th>
    <th align="left"><span data-ttu-id="a74c9-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="a74c9-145">Example</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a74c9-146">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="a74c9-146">Set-AppvClientConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a74c9-147">–RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="a74c9-147">–RequirePublishAsAdmin</span></span></p>
    <ul>
    <li><p><span data-ttu-id="a74c9-148">0-faux</span><span class="sxs-lookup"><span data-stu-id="a74c9-148">0 - False</span></span></p></li>
    <li><p><span data-ttu-id="a74c9-149">1-vrai</span><span class="sxs-lookup"><span data-stu-id="a74c9-149">1 - True</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="a74c9-150">Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="a74c9-150">Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="a74c9-151">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="a74c9-151">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a74c9-152">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="a74c9-152">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a74c9-153">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="a74c9-153">Got an App-V issue?</span></span>** <span data-ttu-id="a74c9-154">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a74c9-154">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a74c9-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a74c9-155">Related topics</span></span>


[<span data-ttu-id="a74c9-156">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="a74c9-156">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="a74c9-157">Administration d'App-V à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a74c9-157">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 






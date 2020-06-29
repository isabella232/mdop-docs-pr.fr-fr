---
title: Utilisation de la console de gestion d'App-V5.1 Client
description: Utilisation de la console de gestion d'App-V5.1 Client
author: dansimp
ms.assetid: be6d4e35-5701-4f9a-ba8a-bede12662cf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63dd75395cdfef1aebae30b364f77465ba8a9882
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804842"
---
# <span data-ttu-id="d64b0-103">Utilisation de la console de gestion d'App-V5.1 Client</span><span class="sxs-lookup"><span data-stu-id="d64b0-103">Using the App-V 5.1 Client Management Console</span></span>


<span data-ttu-id="d64b0-104">Cette rubrique fournit des informations sur la manière de configurer et de gérer le client Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="d64b0-104">This topic provides information about how you can configure and manage the Microsoft Application Virtualization (App-V) 5.1 client.</span></span>

## <span data-ttu-id="d64b0-105">Modification de la configuration du client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="d64b0-105">Modify App-V 5.1 client configuration</span></span>


<span data-ttu-id="d64b0-106">Le client App-V 5,1 a des paramètres qui peuvent être configurés pour déterminer la façon dont le client s’exécutera dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="d64b0-106">The App-V 5.1 client has associated settings that can be configured to determine how the client will run in your environment.</span></span> <span data-ttu-id="d64b0-107">Vous pouvez gérer ces paramètres sur l’ordinateur qui exécute le client ou à l’aide de PowerShell ou d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d64b0-107">You can manage these settings on the computer that runs the client or by using PowerShell or Group Policy.</span></span> <span data-ttu-id="d64b0-108">Pour plus d’informations sur la modification du client à l’aide de PowerShell ou de la configuration de stratégie de groupe, reportez-vous [à la rubrique modification de la configuration du client à l’aide de PowerShell](how-to-modify-client-configuration-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="d64b0-108">For more information about how to modify the client using PowerShell or Group Policy configuration see, [How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell51.md).</span></span>

## <a href="" id="the-app-v-5-1-client-management-console-"></a><span data-ttu-id="d64b0-109">La console de gestion des clients App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="d64b0-109">The App-V 5.1 client management console</span></span>


<span data-ttu-id="d64b0-110">Vous pouvez obtenir des informations sur le client App-V 5,1 ou effectuer des tâches spécifiques en utilisant la console de gestion des clients App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="d64b0-110">You can obtain information about the App-V 5.1 client or perform specific tasks by using the App-V 5.1 client management console.</span></span> <span data-ttu-id="d64b0-111">Bon nombre de tâches que vous pouvez effectuer dans la console de gestion du client à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d64b0-111">Many of the tasks that you can perform in the client management console you can also perform by using PowerShell.</span></span> <span data-ttu-id="d64b0-112">Les applets de commande PowerShell associées à chaque action sont également affichées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d64b0-112">The associated PowerShell cmdlets for each action are also displayed in the following table.</span></span> <span data-ttu-id="d64b0-113">Pour plus d’informations sur l’utilisation de PowerShell, voir [administration d’App-V 5,1 à l’aide de PowerShell](administering-app-v-51-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="d64b0-113">For more information about how to use PowerShell, see [Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md).</span></span>

<span data-ttu-id="d64b0-114">La console de gestion du client contient les onglets principaux décrits ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d64b0-114">The client management console contains the following described main tabs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d64b0-115">Tabulation</span><span class="sxs-lookup"><span data-stu-id="d64b0-115">Tab</span></span></th>
<th align="left"><span data-ttu-id="d64b0-116">Description</span><span class="sxs-lookup"><span data-stu-id="d64b0-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d64b0-117">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="d64b0-117">Overview</span></span></p></td>
<td align="left"><p><span data-ttu-id="d64b0-118">L' <strong> onglet vue d’ensemble </strong> contient les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="d64b0-118">The <strong>Overview</strong> tab contains the following elements:</span></span></p>
<ul>
<li><p><span data-ttu-id="d64b0-119">Mise à jour: utilisez la <strong> vignette mettre à jour </strong> pour actualiser une application virtualisée ou pour recevoir un nouveau package virtualisé.</span><span class="sxs-lookup"><span data-stu-id="d64b0-119">Update – Use the <strong>Update</strong> tile to refresh a virtualized application or to receive a new virtualized package.</span></span></p>
<p><span data-ttu-id="d64b0-120">Le <strong> dernier rafraîchissement </strong> affiche la version actuelle du package virtualisé.</span><span class="sxs-lookup"><span data-stu-id="d64b0-120">The <strong>Last Refresh</strong> displays the current version of the virtualized package.</span></span></p></li>
<li><p><span data-ttu-id="d64b0-121">Télécharger toutes les applications virtuelles: utilisez la <strong> </strong> vignette Télécharger pour télécharger tous les packages approvisionnés par l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="d64b0-121">Download all virtual applications – Use the <strong>Download</strong> tile to download all of the packages provisioned to the current user.</span></span></p>
<p><span data-ttu-id="d64b0-122">(Cmdlet PowerShell associée: <strong> Mount-AppvClientPackage </strong> )</span><span class="sxs-lookup"><span data-stu-id="d64b0-122">(Associated PowerShell cmdlet: <strong>Mount-AppvClientPackage</strong>)</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="d64b0-123">Travailler hors connexion: utilisez cette vignette pour interdire toutes les mises à jour automatiques et manuelles des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="d64b0-123">Work Offline – Use this tile to disallow all automatic and manual virtual application updates.</span></span></p>
<p><span data-ttu-id="d64b0-124">(Cmdlet PowerShell associée: <strong> Set-AppvPublishServer – UserRefreshEnabled – GlobalRefreshEnabled </strong> )</span><span class="sxs-lookup"><span data-stu-id="d64b0-124">(Associated PowerShell cmdlet: <strong>Set-AppvPublishServer –UserRefreshEnabled –GlobalRefreshEnabled</strong>)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d64b0-125">Applications virtuelles</span><span class="sxs-lookup"><span data-stu-id="d64b0-125">Virtual Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="d64b0-126">L' <strong> onglet applications virtuelles </strong> affiche tous les packages qui ont été publiés pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d64b0-126">The <strong>VIRTUAL APPS</strong> tab displays all of the packages that have been published to the user.</span></span> <span data-ttu-id="d64b0-127">Vous pouvez également cliquer sur un package spécifique et afficher toutes les applications qui font partie de ce package.</span><span class="sxs-lookup"><span data-stu-id="d64b0-127">You can also click a specific package and see all of the applications that are part of that package.</span></span> <span data-ttu-id="d64b0-128">Cela permet d’afficher des informations sur les packages actuellement utilisés et la quantité de contenu de chaque package téléchargé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d64b0-128">This displays information about packages that are currently in use and how much of each package has been downloaded to the computer.</span></span> <span data-ttu-id="d64b0-129">Vous pouvez également démarrer et arrêter le téléchargement de packages.</span><span class="sxs-lookup"><span data-stu-id="d64b0-129">You can also start and stop package downloads.</span></span> <span data-ttu-id="d64b0-130">Par ailleurs, vous pouvez réparer l’état de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d64b0-130">Additionally, you can repair the user state.</span></span> <span data-ttu-id="d64b0-131">Une réparation entraîne la suppression de toutes les données utilisateur associées à un package.</span><span class="sxs-lookup"><span data-stu-id="d64b0-131">A repair will delete all user data that is associated with a package.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d64b0-132">Groupes de connexions d’application</span><span class="sxs-lookup"><span data-stu-id="d64b0-132">App Connection Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="d64b0-133">L' <strong> onglet groupes de connexion </strong> d’application affiche tous les groupes de connexions disponibles pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="d64b0-133">The <strong>APP CONNECTION GROUPS</strong> tab displays all of the connection groups that are available to the current user.</span></span> <span data-ttu-id="d64b0-134">Cliquez sur un groupe de connexion spécifique pour afficher tous les packages qui font partie du groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d64b0-134">Click a specific connection group to see all of the packages that are part of the selected group.</span></span> <span data-ttu-id="d64b0-135">Cela affiche des informations sur les groupes de connexion qui sont déjà utilisés et la quantité de contenu du groupe de connexions téléchargée sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d64b0-135">This displays information about connection groups that are already in use and how much of the connection group contents have been downloaded to the computer.</span></span> <span data-ttu-id="d64b0-136">Par ailleurs, vous pouvez démarrer et arrêter des téléchargements de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="d64b0-136">Additionally, you can start and stop connection group downloads.</span></span> <span data-ttu-id="d64b0-137">Vous pouvez utiliser cette section pour lancer une réparation.</span><span class="sxs-lookup"><span data-stu-id="d64b0-137">You can use this section to initiate a repair.</span></span> <span data-ttu-id="d64b0-138">Une réparation supprimera tout l’état utilisateur associé à un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="d64b0-138">A repair will remove all of the user state that is associated a connection group.</span></span></p>
<p><span data-ttu-id="d64b0-139">(Cmdlets PowerShell associées: Télécharger- <strong> Mount-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="d64b0-139">(Associated PowerShell cmdlets: Download - <strong>Mount-AppvClientConnectionGroup</strong>.</span></span> <span data-ttu-id="d64b0-140">Réparer- <strong> AppvClientConnectionGroup </strong> .)</span><span class="sxs-lookup"><span data-stu-id="d64b0-140">Repair -<strong>AppvClientConnectionGroup</strong>.)</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

[<span data-ttu-id="d64b0-141">Procédure d'accès à la console de gestion du client</span><span class="sxs-lookup"><span data-stu-id="d64b0-141">How to Access the Client Management Console</span></span>](how-to-access-the-client-management-console51.md)

[<span data-ttu-id="d64b0-142">Comment configurer le client de manière à recevoir les mises à jour des groupes de connexion et des packages à partir du serveur de publication</span><span class="sxs-lookup"><span data-stu-id="d64b0-142">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-51.md)






## <span data-ttu-id="d64b0-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d64b0-143">Related topics</span></span>


[<span data-ttu-id="d64b0-144">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="d64b0-144">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 






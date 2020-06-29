---
title: Surveillance des déploiements d'espace de travail MED-V
description: Surveillance des déploiements d'espace de travail MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812221"
---
# <span data-ttu-id="19a35-103">Surveillance des déploiements d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="19a35-103">Monitoring MED-V Workspace Deployments</span></span>


<span data-ttu-id="19a35-104">La fonctionnalité de contrôle de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 vous permet d’exécuter des requêtes sur des espaces de travail MED-V pour déterminer si la première configuration a été effectuée dans l’ensemble de votre entreprise après le déploiement des espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="19a35-104">The monitoring feature in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 lets you run queries on individual MED-V workspaces to determine whether first time setup succeeded throughout your enterprise after the MED-V workspaces are deployed.</span></span> <span data-ttu-id="19a35-105">Il est important de surveiller la réussite de l’installation pour la première fois, car MED-V n’est pas disponible tant qu’il n’a pas été correctement configuré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="19a35-105">Monitoring the success of first time setup is important because MED-V is not in a usable state until first time setup has been completed successfully.</span></span>

<span data-ttu-id="19a35-106">Cette section fournit des informations et des instructions pour vous aider à surveiller la réussite ou l’échec de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="19a35-106">This section provides information and instruction to assist you in monitoring the success or failure of first time setup.</span></span>

## <span data-ttu-id="19a35-107">Pour surveiller les déploiements d’espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="19a35-107">To monitor MED-V workspace deployments</span></span>


<span data-ttu-id="19a35-108">La fonctionnalité de surveillance est composée d’un fournisseur WMI (Windows Management Instrumentation) intégré qui vous permet de lancer une requête à l’aide du langage de requête WMI pour découvrir l’état de la première configuration de tous les utilisateurs finaux sur un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="19a35-108">The monitoring feature consists of a coupled in-process Windows Management Instrumentation (WMI) provider that you can query using WMI Query Language to discover the status of first time setup for all end users on a MED-V workspace.</span></span>

<span data-ttu-id="19a35-109">Le fournisseur WMI est implémenté à l’aide de l’infrastructure d’extension du fournisseur WMI à partir de Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="19a35-109">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span> <span data-ttu-id="19a35-110">Le fournisseur WMI s’exécute dans le contexte de LocalService et enregistre l’état de la première installation de façon sécurisée sous \\ProgramData.</span><span class="sxs-lookup"><span data-stu-id="19a35-110">The WMI provider executes in the context of LocalService and stores the first time setup state securely under \\ProgramData.</span></span>

<span data-ttu-id="19a35-111">Le fournisseur WMI est implémenté dans l’espace de noms **root\\microsoft\\medv** et implémente la classe **FTS \ _Status**, qui expose la méthode **SetFtsState**.</span><span class="sxs-lookup"><span data-stu-id="19a35-111">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **FTS\_Status**, which exposes the method **SetFtsState**.</span></span> <span data-ttu-id="19a35-112">MED-V utilise **SetFtsState** pour définir le premier État de l’installation.</span><span class="sxs-lookup"><span data-stu-id="19a35-112">MED-V uses **SetFtsState** to set the first time setup state.</span></span>

<span data-ttu-id="19a35-113">La classe contient les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="19a35-113">The class contains the following properties.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="19a35-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="19a35-114">Property</span></span></th>
<th align="left"><span data-ttu-id="19a35-115">Description</span><span class="sxs-lookup"><span data-stu-id="19a35-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="19a35-116">Ordinateur</span><span class="sxs-lookup"><span data-stu-id="19a35-116">Machine</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="19a35-117">Propriété en lecture seule </strong> qui contient le nom de l’ordinateur virtuel invité approvisionnée par le programme de configuration pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="19a35-117">Read Only</strong> property that contains the name of the guest virtual machine provisioned by first time setup.</span></span> <span data-ttu-id="19a35-118">Cette clé contient le nom que l’invité aurait eu lors du premier échec de la configuration.</span><span class="sxs-lookup"><span data-stu-id="19a35-118">This key contains the name that the guest would have had on first time setup failure.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="19a35-119">StatusCode</span><span class="sxs-lookup"><span data-stu-id="19a35-119">StatusCode</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="19a35-120">Propriété en lecture seule </strong> qui contient zéro si la première configuration a réussi.</span><span class="sxs-lookup"><span data-stu-id="19a35-120">Read Only</strong> property that contains zero if first time setup succeeded.</span></span> <span data-ttu-id="19a35-121">Toute autre valeur renvoyée est égale à l’ID d’événement de l’erreur qui est journalisée.</span><span class="sxs-lookup"><span data-stu-id="19a35-121">Any other value returned equals the event ID for the error that is logged.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="19a35-122">Heure</span><span class="sxs-lookup"><span data-stu-id="19a35-122">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19a35-123">Heure UTC de fin de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="19a35-123">The UTC time that first time setup completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="19a35-124">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="19a35-124">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19a35-125">Utilisateur pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="19a35-125">The user for which first time setup was run.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="19a35-126">Le code suivant montre le fichier MOF (Managed Object Format) qui définit la classe **FTS \ _Status** .</span><span class="sxs-lookup"><span data-stu-id="19a35-126">The following code shows the Managed Object Format (MOF) file that defines the **FTS\_Status** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

<span data-ttu-id="19a35-127">Dans la mesure où il est très probable que les espaces de travail MED-V pour lesquels le programme d’installation n’a pas été exécuté pour la première fois, vous pouvez écrire votre requête de telle sorte qu’elle ne se termine pas correctement, par exemple:</span><span class="sxs-lookup"><span data-stu-id="19a35-127">Because your main concern is most likely those MED-V workspaces for which first time setup was not completed successfully, you can write your query to only return those that failed first time setup, for example:</span></span>

``` syntax
Select * from FTS_Status where StatusCode != 0
```

<span data-ttu-id="19a35-128">Dans ce cas, la fonctionnalité de surveillance renvoie une liste des espaces de travail MED-V qui n’ont pas été configurés pour la première fois, que vous pouvez utiliser pour effectuer les actions appropriées à la résolution de l’échec.</span><span class="sxs-lookup"><span data-stu-id="19a35-128">In this case, the monitoring feature returns a list of those MED-V workspaces that failed first time setup, which you can use to take the appropriate actions to resolve the failure.</span></span>

## <span data-ttu-id="19a35-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19a35-129">Related topics</span></span>


[<span data-ttu-id="19a35-130">Surveiller des espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="19a35-130">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="19a35-131">Comment vérifier les paramètres de première installation</span><span class="sxs-lookup"><span data-stu-id="19a35-131">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

 

 






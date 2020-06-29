---
title: Comment autoriser uniquement les administrateurs à activer des groupes de connexion
description: Comment autoriser uniquement les administrateurs à activer des groupes de connexion
author: dansimp
ms.assetid: 60e62426-624f-4f26-851e-41cd78520883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53461d5c93bf246210c7427c95a8bbe8acca9cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805743"
---
# <span data-ttu-id="ad060-103">Comment autoriser uniquement les administrateurs à activer des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="ad060-103">How to Allow Only Administrators to Enable Connection Groups</span></span>


<span data-ttu-id="ad060-104">Vous pouvez configurer le client App-V de façon à ce que seuls les administrateurs (pas les utilisateurs finaux) puissent activer ou désactiver les groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="ad060-104">You can configure the App-V client so that only administrators (not end users) can enable or disable connection groups.</span></span> <span data-ttu-id="ad060-105">Dans les versions antérieures d’App-V, vous ne pouviez pas empêcher les utilisateurs finaux d’effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="ad060-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

<span data-ttu-id="ad060-106">**Remarques** 
 **Cette fonctionnalité est prise en charge à partir de l’App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="ad060-106">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="ad060-107">Appliquez l’une des méthodes suivantes pour autoriser uniquement les administrateurs à activer ou désactiver les groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="ad060-107">Use one of the following methods to allow only administrators to enable or disable connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad060-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="ad060-108">Method</span></span></th>
<th align="left"><span data-ttu-id="ad060-109">Étapes</span><span class="sxs-lookup"><span data-stu-id="ad060-109">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad060-110">Paramètre de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ad060-110">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad060-111">Activez le paramètre de stratégie de groupe «exiger une administration en tant qu’administrateur», qui se trouve dans le nœud d’objet de stratégie de groupe suivant:</span><span class="sxs-lookup"><span data-stu-id="ad060-111">Enable the “Require publish as administrator” Group Policy setting, which is located in the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="ad060-112">&gt;Stratégies de Configuration ordinateur &gt; modèles d’administration application pour la &gt; &gt; publication de l’application-V &gt;</span><span class="sxs-lookup"><span data-stu-id="ad060-112">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad060-113">Applet de commande PowerShell</span><span class="sxs-lookup"><span data-stu-id="ad060-113">PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad060-114">Exécutez l' <strong> applet de cmdlet Set-AppvClientConfiguration </strong> à l’aide du <strong> paramètre-RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="ad060-114">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>–RequirePublishAsAdmin</strong> parameter.</span></span></p>
<p><span data-ttu-id="ad060-115">Valeurs de paramètres:</span><span class="sxs-lookup"><span data-stu-id="ad060-115">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="ad060-116">0-faux</span><span class="sxs-lookup"><span data-stu-id="ad060-116">0 - False</span></span></p></li>
<li><p><span data-ttu-id="ad060-117">1-vrai</span><span class="sxs-lookup"><span data-stu-id="ad060-117">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="ad060-118">Exemple: </strong> : Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="ad060-118">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ad060-119">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="ad060-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ad060-120">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="ad060-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ad060-121">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="ad060-121">Got an App-V issue?</span></span>** <span data-ttu-id="ad060-122">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ad060-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ad060-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad060-123">Related topics</span></span>


[<span data-ttu-id="ad060-124">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="ad060-124">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 






---
title: Procédure pour effectuer des tâches DaRT à l'aide des commandes PowerShell
description: Procédure pour effectuer des tâches DaRT à l'aide des commandes PowerShell
author: dansimp
ms.assetid: f5a5c5f9-d667-4c85-9e82-7baf0b2aec6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fdf167ca81281da4e04dae10e34bad6122ec05aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809450"
---
# <span data-ttu-id="2b54f-103">Procédure pour effectuer des tâches DaRT à l'aide des commandes PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b54f-103">How to Perform DaRT Tasks by Using PowerShell Commands</span></span>


<span data-ttu-id="2b54f-104">Microsoft Diagnostics and Recovery Tools (DaRT) 10 fournit l’ensemble d’applets de commande Windows PowerShell suivant.</span><span class="sxs-lookup"><span data-stu-id="2b54f-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 10 provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="2b54f-105">Les administrateurs peuvent utiliser les applets de commande PowerShell suivants pour effectuer différentes tâches du serveur DaRT 10 à partir de l’invite de commandes plutôt que de l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="2b54f-105">Administrators can use these PowerShell cmdlets to perform various DaRT 10 server tasks from the command prompt rather than from the DaRT Recovery Image wizard.</span></span>

## <span data-ttu-id="2b54f-106">Pour administrer DaRT à l’aide de commandes PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b54f-106">To administer DaRT by using PowerShell commands</span></span>


<span data-ttu-id="2b54f-107">Utilisez les applets de commande PowerShell décrites ici pour gérer DaRT.</span><span class="sxs-lookup"><span data-stu-id="2b54f-107">Use the PowerShell cmdlets described here to administer DaRT.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2b54f-108">Nom</span><span class="sxs-lookup"><span data-stu-id="2b54f-108">Name</span></span></th>
<th align="left"><span data-ttu-id="2b54f-109">Description</span><span class="sxs-lookup"><span data-stu-id="2b54f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2b54f-110">Copy-DartImage</span><span class="sxs-lookup"><span data-stu-id="2b54f-110">Copy-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b54f-111">Brûlure d’une connexion ISO sur un CD, un DVD ou un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="2b54f-111">Burns an ISO to a CD, DVD, or USB drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2b54f-112">Export-DartImage</span><span class="sxs-lookup"><span data-stu-id="2b54f-112">Export-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b54f-113">Permet de convertir le fichier WIM source contenant une image DaRT en fichier ISO.</span><span class="sxs-lookup"><span data-stu-id="2b54f-113">Allows the source WIM file, which contains a DaRT image, to be converted into an ISO file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2b54f-114">Nouveau-DartConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b54f-114">New-DartConfiguration</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b54f-115">Crée un objet de configuration DaRT requis pour appliquer un ensemble d’outils DaRT à une image Windows.</span><span class="sxs-lookup"><span data-stu-id="2b54f-115">Creates a DaRT configuration object that is needed to apply a DaRT toolset to a Windows Image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2b54f-116">Set-DartImage</span><span class="sxs-lookup"><span data-stu-id="2b54f-116">Set-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="2b54f-117">Applique un objet DartConfiguration à une image Windows montée.</span><span class="sxs-lookup"><span data-stu-id="2b54f-117">Applies a DartConfiguration object to a mounted Windows Image.</span></span> <span data-ttu-id="2b54f-118">Cela inclut l’ajout de tous les fichiers, de la configuration et des dépendances du package.</span><span class="sxs-lookup"><span data-stu-id="2b54f-118">This includes adding all files, configuration, and package dependencies.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2b54f-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b54f-119">Related topics</span></span>


[<span data-ttu-id="2b54f-120">Administration de DaRT10 à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b54f-120">Administering DaRT 10 Using PowerShell</span></span>](administering-dart-10-using-powershell.md)

 

 






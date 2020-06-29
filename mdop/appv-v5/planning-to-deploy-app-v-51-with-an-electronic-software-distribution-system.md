---
title: Planification du déploiement d'App-V5.1 avec un système de distribution électronique de logiciels
description: Planification du déploiement d'App-V5.1 avec un système de distribution électronique de logiciels
author: dansimp
ms.assetid: c26602c2-5e8d-44e6-90df-adacc593607e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fde3f0ea4f1dec72b97143b4b27dd0b32a503b15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804950"
---
# <span data-ttu-id="8bfbe-103">Planification du déploiement d'App-V5.1 avec un système de distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="8bfbe-103">Planning to Deploy App-V 5.1 with an Electronic Software Distribution System</span></span>


<span data-ttu-id="8bfbe-104">Si vous utilisez un système de distribution de logiciels électronique pour déployer des packages App-V, consultez les considérations de planification suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bfbe-104">If you are using an electronic software distribution system to deploy App-V packages, review the following planning considerations.</span></span> <span data-ttu-id="8bfbe-105">Pour plus d’informations sur l’utilisation de System Center Configuration Manager pour déployer App-V, voir [Présentation de la gestion des applications dans Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span><span class="sxs-lookup"><span data-stu-id="8bfbe-105">For information about using System Center Configuration Manager to deploy App-V, see [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span></span>

<span data-ttu-id="8bfbe-106">Passez en revue les options suivantes relatives aux composants et à l’architecture qui s’appliquent lorsque vous utilisez un système de déploiement ESD pour déployer des packages App-V:</span><span class="sxs-lookup"><span data-stu-id="8bfbe-106">Review the following component and architecture requirements options that apply when you use an ESD to deploy App-V packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8bfbe-107">Option ou option de déploiement requise</span><span class="sxs-lookup"><span data-stu-id="8bfbe-107">Deployment requirement or option</span></span></th>
<th align="left"><span data-ttu-id="8bfbe-108">Description</span><span class="sxs-lookup"><span data-stu-id="8bfbe-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8bfbe-109">La base de données de gestion et le serveur de gestion App-V n’est pas requis.</span><span class="sxs-lookup"><span data-stu-id="8bfbe-109">The App-V Management server, Management database, and Publishing server are not required.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8bfbe-110">Ces fonctions sont gérées par la solution ESD implémentée.</span><span class="sxs-lookup"><span data-stu-id="8bfbe-110">These functions are handled by the implemented ESD solution.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8bfbe-111">Vous pouvez déployer le serveur de création de rapports d’application et de la base de données de création de rapports en parallèle avec la fonction ESD.</span><span class="sxs-lookup"><span data-stu-id="8bfbe-111">You can deploy the App-V Reporting server and Reporting database side by side with the ESD.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8bfbe-112">Le déploiement côte à côte vous permet de recueillir des données et de générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="8bfbe-112">The side-by-side deployment lets you to collect data and generate reports.</span></span></p>
<p><span data-ttu-id="8bfbe-113">Si vous activez le client App-V pour envoyer des informations de rapport et que vous n’utilisez pas le serveur de rapports d’applications-V, les données de rapport sont stockées dans les fichiers. XML associés.</span><span class="sxs-lookup"><span data-stu-id="8bfbe-113">If you enable the App-V client to send report information, and you are not using the App-V Reporting server, the reporting data is stored in associated .xml files.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="8bfbe-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bfbe-114">Related topics</span></span>


[<span data-ttu-id="8bfbe-115">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="8bfbe-115">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 






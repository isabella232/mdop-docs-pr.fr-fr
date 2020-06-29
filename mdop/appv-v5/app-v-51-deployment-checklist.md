---
title: Liste de contrôle pour le déploiement d'App-V5.1
description: Liste de contrôle pour le déploiement d'App-V5.1
author: dansimp
ms.assetid: 44bed85a-e4f5-49d7-a308-a2b681f76372
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0864335e505996a3ea379b09de6a1aaa7fbe1676
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805977"
---
# <span data-ttu-id="1f7d3-103">Liste de contrôle pour le déploiement d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="1f7d3-103">App-V 5.1 Deployment Checklist</span></span>


<span data-ttu-id="1f7d3-104">Cette liste de vérification peut être utilisée pour vous aider pendant le déploiement de Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="1f7d3-104">This checklist can be used to help you during Microsoft Application Virtualization (App-V) 5.1 deployment.</span></span>

**<span data-ttu-id="1f7d3-105">Remarque</span><span class="sxs-lookup"><span data-stu-id="1f7d3-105">Note</span></span>**  
<span data-ttu-id="1f7d3-106">Cette liste de vérification décrit les étapes recommandées et une liste générale des éléments à prendre en compte lors du déploiement des fonctionnalités d’application-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="1f7d3-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying App-V 5.1 features.</span></span> <span data-ttu-id="1f7d3-107">Il est recommandé de copier cette liste de vérification dans un tableur et de la personnaliser pour votre utilisation.</span><span class="sxs-lookup"><span data-stu-id="1f7d3-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="1f7d3-108">Tâche</span><span class="sxs-lookup"><span data-stu-id="1f7d3-108">Task</span></span></th>
<th align="left"><span data-ttu-id="1f7d3-109">Références</span><span class="sxs-lookup"><span data-stu-id="1f7d3-109">References</span></span></th>
<th align="left"><span data-ttu-id="1f7d3-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="1f7d3-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1f7d3-111">Achevez la phase de planification pour préparer l’environnement informatique pour le déploiement d’App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="1f7d3-111">Complete the planning phase to prepare the computing environment for App-V 5.1 deployment.</span></span></p></td>
<td align="left"><p><a href="app-v-51-planning-checklist.md" data-raw-source="[App-V 5.1 Planning Checklist](app-v-51-planning-checklist.md)"><span data-ttu-id="1f7d3-112">Liste de contrôle de la planification d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="1f7d3-112">App-V 5.1 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1f7d3-113">Passez en revue les informations de configurations prises en charge par App-V 5,1 pour vous assurer que les ordinateurs client et serveur sélectionnés sont pris en charge pour l’installation de la fonctionnalité App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="1f7d3-113">Review the App-V 5.1 supported configurations information to make sure selected client and server computers are supported for App-V 5.1 feature installation.</span></span></p></td>
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="1f7d3-114">Configurations prises en charge par App-V5.1</span><span class="sxs-lookup"><span data-stu-id="1f7d3-114">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1f7d3-115">Exécutez le programme d’installation d’App-V 5,1 pour déployer les fonctionnalités de l’application-V 5,1 requises pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="1f7d3-115">Run App-V 5.1 Setup to deploy the required App-V 5.1 features for your environment.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1f7d3-116">Remarque</span><span class="sxs-lookup"><span data-stu-id="1f7d3-116">Note</span></span></strong><br/><p><span data-ttu-id="1f7d3-117">Assurez le suivi des noms des serveurs et des URL associées créées lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="1f7d3-117">Keep track of the names of the servers and associated URL’s created during installation.</span></span> <span data-ttu-id="1f7d3-118">Ces informations seront utilisées tout au long du processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="1f7d3-118">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p></p>
<ul>
<li><p><a href="how-to-install-the-sequencer-51beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md)"><span data-ttu-id="1f7d3-119">Installation de Sequencer</span><span class="sxs-lookup"><span data-stu-id="1f7d3-119">How to Install the Sequencer</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="1f7d3-120">Comment déployer App-V Client</span><span class="sxs-lookup"><span data-stu-id="1f7d3-120">How to Deploy the App-V Client</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="1f7d3-121">Procédure de déploiement d'App-V5.1 Server</span><span class="sxs-lookup"><span data-stu-id="1f7d3-121">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="1f7d3-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f7d3-122">Related topics</span></span>


[<span data-ttu-id="1f7d3-123">Déploiement d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="1f7d3-123">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)










---
title: Architecture de haut niveau pour App-V5.1
description: Architecture de haut niveau pour App-V5.1
author: dansimp
ms.assetid: 90406361-55b8-40b7-85c0-449436789d4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8044c6ae9af4673ec12b47cf3b8fa73a134d9cca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805790"
---
# <span data-ttu-id="32582-103">Architecture de haut niveau pour App-V5.1</span><span class="sxs-lookup"><span data-stu-id="32582-103">High Level Architecture for App-V 5.1</span></span>


<span data-ttu-id="32582-104">Utilisez les informations suivantes pour vous simplifier le déploiement de Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="32582-104">Use the following information to help you simplify you Microsoft Application Virtualization (App-V) 5.1 deployment.</span></span>

## <span data-ttu-id="32582-105">Présentation de l’architecture</span><span class="sxs-lookup"><span data-stu-id="32582-105">Architecture Overview</span></span>


<span data-ttu-id="32582-106">Une implémentation standard d’App-V 5,1 se compose des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="32582-106">A typical App-V 5.1 implementation consists of the following elements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="32582-107">Élément</span><span class="sxs-lookup"><span data-stu-id="32582-107">Element</span></span></th>
<th align="left"><span data-ttu-id="32582-108">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="32582-108">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="32582-109">Serveur de gestion App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="32582-109">App-V 5.1 Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="32582-110">Le serveur de gestion App-V 5,1 fournit une fonctionnalité de gestion générale de l’infrastructure App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="32582-110">The App-V 5.1 Management server provides overall management functionality for the App-V 5.1 infrastructure.</span></span> <span data-ttu-id="32582-111">De plus, vous pouvez installer plusieurs instances du serveur de gestion dans votre environnement, qui offre les avantages suivants:</span><span class="sxs-lookup"><span data-stu-id="32582-111">Additionally, you can install more than one instance of the management server in your environment which provides the following benefits:</span></span></p>
<ul>
<li><p><span data-ttu-id="32582-112">Tolérance de panne et haute disponibilité: l’installation et la configuration du serveur de gestion App-V 5,1 sur deux ordinateurs séparés peuvent être utiles lorsque l’un des serveurs est indisponible ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="32582-112">Fault Tolerance and High Availability – Installing and configuring the App-V 5.1 Management server on two separate computers can help in situations when one of the servers is unavailable or offline.</span></span></p>
<p><span data-ttu-id="32582-113">Vous pouvez également améliorer la disponibilité de l’application-V 5,1 en installant le serveur de gestion sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="32582-113">You can also help increase App-V 5.1 availability by installing the Management server on multiple computers.</span></span> <span data-ttu-id="32582-114">Dans ce scénario, un équilibreur de charge réseau doit également être considéré de sorte que les requêtes serveur soient équilibrées.</span><span class="sxs-lookup"><span data-stu-id="32582-114">In this scenario, a network load balancer should also be considered so that server requests are balanced.</span></span></p></li>
<li><p><span data-ttu-id="32582-115">Extensibilité: vous pouvez ajouter d’autres serveurs de gestion nécessaires à la prise en charge d’une forte charge, par exemple pour installer plusieurs serveurs derrière un équilibreur de charge.</span><span class="sxs-lookup"><span data-stu-id="32582-115">Scalability – You can add additional management servers as necessary to support a high load, for example you can install multiple servers behind a load balancer.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="32582-116">Serveur de publication 5,1 App-V</span><span class="sxs-lookup"><span data-stu-id="32582-116">App-V 5.1 Publishing Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="32582-117">Le serveur de publication App-V 5,1 fournit des fonctionnalités pour l’hébergement et la diffusion en continu d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="32582-117">The App-V 5.1 publishing server provides functionality for virtual application hosting and streaming.</span></span> <span data-ttu-id="32582-118">Le serveur de publication ne nécessite pas de connexion de base de données et prend en charge les protocoles suivants:</span><span class="sxs-lookup"><span data-stu-id="32582-118">The publishing server does not require a database connection and supports the following protocols:</span></span></p>
<ul>
<li><p><span data-ttu-id="32582-119">HTTP et HTTPs</span><span class="sxs-lookup"><span data-stu-id="32582-119">HTTP, and HTTPS</span></span></p></li>
</ul>
<p><span data-ttu-id="32582-120">Vous pouvez également améliorer la disponibilité de l’application-V 5,1 en installant le serveur de publication sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="32582-120">You can also help increase App-V 5.1 availability by installing the Publishing server on multiple computers.</span></span> <span data-ttu-id="32582-121">Un équilibrage de charge réseau doit également être considéré de sorte que les requêtes serveur soient équilibrées.</span><span class="sxs-lookup"><span data-stu-id="32582-121">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="32582-122">Serveur de création de rapports App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="32582-122">App-V 5.1 Reporting Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="32582-123">Le serveur de création de rapports App-V 5,1 permet aux utilisateurs autorisés d’exécuter et d’afficher des rapports App-V 5,1 et des rapports ad hoc existants qui leur permettent de gérer l’infrastructure App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="32582-123">The App-V 5.1 Reporting server enables authorized users to run and view existing App-V 5.1 reports and ad hoc reports that can help them manage the App-V 5.1 infrastructure.</span></span> <span data-ttu-id="32582-124">Le serveur de création de rapports nécessite une connexion à la base de données de création de rapports App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="32582-124">The Reporting server requires a connection to the App-V 5.1 reporting database.</span></span> <span data-ttu-id="32582-125">Vous pouvez également améliorer la disponibilité de l’application-V 5,1 en installant le serveur de création de rapports sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="32582-125">You can also help increase App-V 5.1 availability by installing the Reporting server on multiple computers.</span></span> <span data-ttu-id="32582-126">Un équilibrage de charge réseau doit également être considéré de sorte que les requêtes serveur soient équilibrées.</span><span class="sxs-lookup"><span data-stu-id="32582-126">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="32582-127">Client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="32582-127">App-V 5.1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="32582-128">Le client App-V 5,1 permet aux packages créés à l’aide de App-V 5,1 de s’exécuter sur des ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="32582-128">The App-V 5.1 client enables packages created using App-V 5.1 to run on target computers.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="32582-129">**Remarques**  Si vous utilisez App-V 5,1 avec la distribution de logiciels électroniques (ESD), vous n’êtes pas tenu d’utiliser le serveur de gestion App-V 5,1, mais vous pouvez toujours utiliser la fonctionnalité de création de rapports et de streaming de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="32582-129">**Note** If you are using App-V 5.1 with Electronic Software Distribution (ESD) you are not required to use the App-V 5.1 Management server, however you can still utilize the reporting and streaming functionality of App-V 5.1.</span></span>

 






## <span data-ttu-id="32582-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32582-130">Related topics</span></span>


[<span data-ttu-id="32582-131">Prise en main de l'application App-V5.1</span><span class="sxs-lookup"><span data-stu-id="32582-131">Getting Started with App-V 5.1</span></span>](getting-started-with-app-v-51.md)

 

 






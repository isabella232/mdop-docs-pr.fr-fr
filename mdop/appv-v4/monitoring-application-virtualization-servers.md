---
title: Analyse des serveurs Application Virtualization Server
description: Analyse des serveurs Application Virtualization Server
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806589"
---
# <span data-ttu-id="d74ff-103">Analyse des serveurs Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="d74ff-103">Monitoring Application Virtualization Servers</span></span>


<span data-ttu-id="d74ff-104">Pour simplifier la gestion de serveur de la virtualisation des applications (App-V), vous pouvez utiliser le pack d’administration Manager2007 Operations Center.</span><span class="sxs-lookup"><span data-stu-id="d74ff-104">To simplify Application Virtualization (App-V) Server management, you can use the System Center Operations Manager2007 Management Pack.</span></span> <span data-ttu-id="d74ff-105">Ce module d’administration prend uniquement en charge les serveurs 4,5 de virtualisation des applications (App-V). elle ne prend pas en charge les versions antérieures du serveur.</span><span class="sxs-lookup"><span data-stu-id="d74ff-105">This Management Pack supports only Application Virtualization (App-V) 4.5 servers; it does not support previous server versions.</span></span> <span data-ttu-id="d74ff-106">Le pack d’administration maximise la disponibilité du serveur App-V pour gérer les demandes des clients App-V.</span><span class="sxs-lookup"><span data-stu-id="d74ff-106">The Management Pack maximizes App-V Server availability for handling App-V Client requests.</span></span>

## <span data-ttu-id="d74ff-107">Indicateurs d’État</span><span class="sxs-lookup"><span data-stu-id="d74ff-107">Status Indicators</span></span>


<span data-ttu-id="d74ff-108">Les indicateurs d’état d’intégrité du serveur App-V sont des codes de couleur.</span><span class="sxs-lookup"><span data-stu-id="d74ff-108">The App-V Server health status indicators are color-coded.</span></span> <span data-ttu-id="d74ff-109">Les couleurs représentent les valeurs d’État suivantes:</span><span class="sxs-lookup"><span data-stu-id="d74ff-109">The colors represent the following status values:</span></span>

-   <span data-ttu-id="d74ff-110">Aucune couleur indique que le serveur fonctionne sans erreur non récupérable.</span><span class="sxs-lookup"><span data-stu-id="d74ff-110">No color indicates that the server is running without non-recoverable errors.</span></span>

-   <span data-ttu-id="d74ff-111">Le jaune indique que l’un des composants ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="d74ff-111">Yellow indicates that one of the components is not functioning correctly.</span></span> <span data-ttu-id="d74ff-112">La fonctionnalité globale du serveur est détériorée, mais le serveur est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="d74ff-112">The overall functionality of the server is degraded, but the server is still available.</span></span>

-   <span data-ttu-id="d74ff-113">Rouge indique que le serveur n’est pas disponible et qu’il ne peut pas fournir de services clés ou communiquer avec des dépendances de service externe.</span><span class="sxs-lookup"><span data-stu-id="d74ff-113">Red indicates that the server is not available and that it cannot provide key services or communicate with external service dependencies.</span></span>

## <span data-ttu-id="d74ff-114">Critères d’analyse</span><span class="sxs-lookup"><span data-stu-id="d74ff-114">Monitoring Criteria</span></span>


<span data-ttu-id="d74ff-115">Le pack d’administration analyse les aspects suivants du fonctionnement du serveur:</span><span class="sxs-lookup"><span data-stu-id="d74ff-115">The Management Pack monitors the following aspects of server health:</span></span>

-   <span data-ttu-id="d74ff-116">État du serveur: analyse les événements du serveur pour vérifier que le serveur fournit ses services attendus.</span><span class="sxs-lookup"><span data-stu-id="d74ff-116">Server Status—monitors server events to validate that the server is providing its expected services.</span></span>

-   <span data-ttu-id="d74ff-117">Accès au magasin de données: permet de suivre la capacité d’un ou de plusieurs serveurs d’administration de l’application à accéder à la Banque de données App-V et à communiquer avec celle-ci.</span><span class="sxs-lookup"><span data-stu-id="d74ff-117">Data Store Access—tracks the ability of one or more of the App-V Management Servers to access and communicate with the App-V data store.</span></span>

-   <span data-ttu-id="d74ff-118">Accès aux données de contenu: contrôle l’accès au répertoire \\Content, qui peut être un répertoire local ou un partage réseau, et la possibilité de lire les fichiers demandés.</span><span class="sxs-lookup"><span data-stu-id="d74ff-118">Content Data Access—monitors access to the \\Content directory, which might be a local directory or a network share, and the ability to read the requested files.</span></span>

-   <span data-ttu-id="d74ff-119">Sécurité: signale les erreurs liées au certificat du serveur App-V et aux communications sécurisées.</span><span class="sxs-lookup"><span data-stu-id="d74ff-119">Security—reports errors with the App-V Server’s certificate and secure communications.</span></span>

-   <span data-ttu-id="d74ff-120">Gestion des demandes de clients: surveille la capacité d’un ou de plusieurs serveurs App-V à gérer et à répondre correctement aux demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="d74ff-120">Client Request Handling—monitors the ability of one or more of the App-V Servers to handle and correctly respond to client requests.</span></span> <span data-ttu-id="d74ff-121">Il s’agit notamment de publier des éléments tels que des demandes de configuration, des demandes de chargement de packages et des demandes hors séquence.</span><span class="sxs-lookup"><span data-stu-id="d74ff-121">These requests include publishing such items as configuration requests, package load requests, and out of sequence requests.</span></span>

-   <span data-ttu-id="d74ff-122">Configuration du serveur: vérifie les paramètres de configuration du serveur App-V.</span><span class="sxs-lookup"><span data-stu-id="d74ff-122">Server Configuration—checks the configuration settings of the App-V Server.</span></span> <span data-ttu-id="d74ff-123">Ces paramètres de configuration incluent les paramètres du Registre et du magasin de données App-V.</span><span class="sxs-lookup"><span data-stu-id="d74ff-123">These configuration settings include the settings in the registry and in the App-V data store.</span></span>

## <span data-ttu-id="d74ff-124">Différences de serveur</span><span class="sxs-lookup"><span data-stu-id="d74ff-124">Server Differences</span></span>


<span data-ttu-id="d74ff-125">Les principales différences entre le serveur de gestion App-V et le serveur de streaming d’applications-V sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="d74ff-125">The main differences between the App-V Management Server and the App-V Streaming Server are as follows:</span></span>

-   <span data-ttu-id="d74ff-126">Les serveurs de gestion App-V peuvent fournir des services de publication, de diffusion, de gestion et de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="d74ff-126">App-V Management Servers can provide publishing, streaming, management, and reporting services.</span></span> <span data-ttu-id="d74ff-127">Par conséquent, le pack d’administration peut gérer davantage de aspects du serveur de gestion d’application-V qu’il peut gérer sur le serveur de streaming App-V, qui fournit uniquement du streaming de package.</span><span class="sxs-lookup"><span data-stu-id="d74ff-127">Therefore, the Management Pack can manage more aspects of the App-V Management Server than it can manage on the App-V Streaming Server, which provides only package streaming.</span></span>

-   <span data-ttu-id="d74ff-128">Le serveur de streaming App-V n’ayant pas de magasin de données App-V, l’accès au magasin de données n’est pas surveillé.</span><span class="sxs-lookup"><span data-stu-id="d74ff-128">The App-V Streaming Server does not have an App-V data store, so data store access is not monitored.</span></span> <span data-ttu-id="d74ff-129">Les informations de configuration du serveur de streaming App-V sont gérées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="d74ff-129">The configuration information for the App-V Streaming Server is managed in the registry.</span></span>

-   <span data-ttu-id="d74ff-130">Le serveur de streaming App-V n’utilise pas l’interface de la console App-V Server Management. utiliser d’autres outils pour gérer la configuration.</span><span class="sxs-lookup"><span data-stu-id="d74ff-130">The App-V Streaming Server does not use the App-V Server Management Console interface; use other tools to manage the configuration.</span></span>

## <span data-ttu-id="d74ff-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d74ff-131">Related topics</span></span>


[<span data-ttu-id="d74ff-132">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="d74ff-132">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 






---
title: Présentation des composants du système Application Virtualization
description: Présentation des composants du système Application Virtualization
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806553"
---
# <span data-ttu-id="6773d-103">Présentation des composants du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6773d-103">Overview of the Application Virtualization System Components</span></span>


<span data-ttu-id="6773d-104">Le tableau suivant décrit les principaux composants du système de gestion de Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="6773d-104">The following table describes the primary components of the Microsoft Application Virtualization Management System.</span></span> <span data-ttu-id="6773d-105">Pour plus d’informations sur le déploiement de ces composants système, voir [scénario basé sur un serveur de virtualisation des applications](application-virtualization-server-based-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="6773d-105">For more information about deploying these system components, see [Application Virtualization Server-Based Scenario](application-virtualization-server-based-scenario.md).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6773d-106">Composant</span><span class="sxs-lookup"><span data-stu-id="6773d-106">Component</span></span></th>
<th align="left"><span data-ttu-id="6773d-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="6773d-107">Function</span></span></th>
<th align="left"><span data-ttu-id="6773d-108">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6773d-108">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6773d-109">Serveur de gestion de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6773d-109">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-110">Composant responsable de la diffusion du contenu du package et de la publication des raccourcis et des associations de types de fichiers sur le client de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="6773d-110">The component responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-111">Le serveur de gestion des applications virtuelles prend en charge la mise à niveau active, la gestion des licences et une base de données qui peut être utilisée pour la création de rapports.</span><span class="sxs-lookup"><span data-stu-id="6773d-111">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6773d-112">Dossier de contenu </strong></span><span class="sxs-lookup"><span data-stu-id="6773d-112">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-113">Emplacement des packages de virtualisation d’application pour la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="6773d-113">The location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-114">Ce dossier peut être localisé sur un serveur de gestion de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="6773d-114">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span> <span data-ttu-id="6773d-115">Le dossier peut également être placé sur un réseau de zone de stockage (SAN).</span><span class="sxs-lookup"><span data-stu-id="6773d-115">The folder can also be located on a Storage Area Network (SAN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6773d-116">Microsoft Application Virtualization Management Console</span><span class="sxs-lookup"><span data-stu-id="6773d-116">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-117">Utilitaire de gestion des composants enfichables 3,0 de MMC pour l’administration de serveur Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="6773d-117">An MMC 3.0 snap-in management utility for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-118">Ce composant peut être installé sur le serveur Microsoft Application Virtualization Server ou situé sur une station de travail distincte qui dispose de MMC 3.0 et. .NET 2.0 installé.</span><span class="sxs-lookup"><span data-stu-id="6773d-118">This component can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6773d-119">Service Web de gestion de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6773d-119">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-120">Composant responsable de la communication de toutes les demandes en lecture/écriture dans le magasin de données de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="6773d-120">The component responsible for communicating any read/write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-121">Ce composant peut être installé sur le serveur Microsoft Application Virtualization ou sur un autre ordinateur sur lequel IIS est installé.</span><span class="sxs-lookup"><span data-stu-id="6773d-121">This component can installed on the Microsoft Application Virtualization Server or on a separate computer with IIS installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6773d-122">Magasin de données de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6773d-122">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-123">Composant stocké dans la base de données SQL et responsable du stockage de toutes les informations liées à l’infrastructure de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="6773d-123">The component stored in the SQL database and responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-124">Ces informations incluent tous les enregistrements d’application, les affectations d’application et les groupes responsables de la gestion de l’environnement de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="6773d-124">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6773d-125">Serveur de diffusion de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6773d-125">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-126">Composant responsable de l’hébergement des packages de virtualisation d’application destinés à la diffusion en continu vers les clients d’une succursale, où le lien retour vers le serveur de gestion des applications est considéré comme un réseau étendu.</span><span class="sxs-lookup"><span data-stu-id="6773d-126">The component responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a WAN.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-127">Ce serveur est doté de la fonctionnalité de diffusion en continu uniquement et ne fournit ni la console de gestion des applications virtuelles, ni le service Web de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="6773d-127">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6773d-128">Sequencer Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6773d-128">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-129">Composant utilisé pour surveiller et capturer l’installation des applications afin de créer des packages d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6773d-129">The component used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-130">La sortie se compose des icônes de l’application, d’un fichier OSD contenant des informations de définition de package, d’un fichier de manifeste de package et du fichier SFT contenant les fichiers de contenu du programme d’application.</span><span class="sxs-lookup"><span data-stu-id="6773d-130">Output consists of the application’s icons, an OSD file containing package definition information, a package manifest file, and the SFT file containing the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6773d-131">Client Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6773d-131">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-132">Composants installés sur le client de bureau de virtualisation des applications ou sur le client de virtualisation d’application pour les services Bureau à distance (anciennement services Terminal Server) et qui fournit l’environnement virtuel pour les applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="6773d-132">The component installed on the Application Virtualization Desktop Client or on the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services) and that provides the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6773d-133">Le client de virtualisation d’applications Microsoft gère la diffusion du package dans le cache, l’actualisation de la publication, le transport et toute interaction avec les serveurs de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="6773d-133">The Microsoft Application Virtualization Client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization Servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6773d-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6773d-134">Related topics</span></span>


[<span data-ttu-id="6773d-135">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="6773d-135">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="6773d-136">Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="6773d-136">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[<span data-ttu-id="6773d-137">Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="6773d-137">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 






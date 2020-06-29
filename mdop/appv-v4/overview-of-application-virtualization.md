---
title: Vue d'ensemble d'Application Virtualization
description: Vue d'ensemble d'Application Virtualization
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806557"
---
# <span data-ttu-id="8fbab-103">Vue d'ensemble d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8fbab-103">Overview of Application Virtualization</span></span>


<span data-ttu-id="8fbab-104">Microsoft Application Virtualization (App-V) permet de rendre les applications accessibles aux utilisateurs finaux sans avoir à installer les applications directement sur ces ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="8fbab-104">Microsoft Application Virtualization (App-V) can make applications available to end user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="8fbab-105">C’est possible par le biais d’un processus connu sous le nom de *Sequencer de l’application*, qui permet à chaque application de s’exécuter dans son propre environnement virtuel autonome sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="8fbab-105">This is made possible through a process known as *sequencing the application*, which enables each application to run in its own self-contained virtual environment on the client computer.</span></span> <span data-ttu-id="8fbab-106">Les applications séquencées sont isolées les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="8fbab-106">The sequenced applications are isolated from each other.</span></span> <span data-ttu-id="8fbab-107">Cela élimine les conflits d’application, mais les applications peuvent quand même interagir avec l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="8fbab-107">This eliminates application conflicts, but the applications can still interact with the client computer.</span></span>

<span data-ttu-id="8fbab-108">Le client App-V est une fonctionnalité qui permet à l’utilisateur final d’interagir avec les applications une fois qu’elles ont été publiées sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8fbab-108">The App-V client is the feature that lets the end user interact with the applications after they have been published to the computer.</span></span> <span data-ttu-id="8fbab-109">Le client gère l’environnement virtuel dans lequel les applications virtuelles s’exécutent sur chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8fbab-109">The client manages the virtual environment in which the virtualized applications run on each computer.</span></span> <span data-ttu-id="8fbab-110">Après avoir installé le client sur un ordinateur, les applications doivent être mises à disposition de l’ordinateur par le biais d’un processus connu sous le nom de *publication*, qui permet à l’utilisateur final d’exécuter les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="8fbab-110">After the client has been installed on a computer, the applications must be made available to the computer through a process known as *publishing*, which enables the end user to run the virtual applications.</span></span> <span data-ttu-id="8fbab-111">Le processus de publication copie les icônes et raccourcis des applications virtuelles sur l’ordinateur, généralement sur le bureau Windows ou dans le menu **Démarrer** , et copie également les informations de définition de package et d’association de type de fichier sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8fbab-111">The publishing process copies the virtual application icons and shortcuts to the computer—typically on the Windows desktop or on the **Start** menu—and also copies the package definition and file type association information to the computer.</span></span> <span data-ttu-id="8fbab-112">La publication rend également le contenu du package d’application disponible pour l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="8fbab-112">Publishing also makes the application package content available to the end user’s computer.</span></span>

<span data-ttu-id="8fbab-113">Le contenu du package d’application virtuel peut être copié sur un ou plusieurs serveurs de virtualisation des applications de sorte qu’il puisse être diffusé aux clients à la demande et mis en cache localement.</span><span class="sxs-lookup"><span data-stu-id="8fbab-113">The virtual application package content can be copied onto one or more Application Virtualization servers so that it can be streamed down to the clients on demand and cached locally.</span></span> <span data-ttu-id="8fbab-114">Les serveurs de fichiers et les serveurs Web peuvent également être utilisés en tant que serveurs de diffusion en continu, ou être copiés directement sur l’ordinateur de l’utilisateur final, par exemple, si vous utilisez un système de distribution de logiciels électronique, tel que Microsoft Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="8fbab-114">File servers and Web servers can also be used as streaming servers, or the content can be copied directly to the end user’s computer—for example, if you are using an electronic software distribution system, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="8fbab-115">Dans une implémentation multiserveur, la mise à jour du contenu du package et sa mise à jour sur tous les serveurs de diffusion en continu nécessite une solution complète de gestion des packages.</span><span class="sxs-lookup"><span data-stu-id="8fbab-115">In a multi-server implementation, maintaining the package content and keeping it up to date on all the streaming servers requires a comprehensive package management solution.</span></span> <span data-ttu-id="8fbab-116">En fonction de la taille de votre organisation, il se peut que vous deviez disposer de nombreux applications virtuelles accessibles aux utilisateurs finaux dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="8fbab-116">Depending on the size of your organization, you might need to have many virtual applications available to end users located all over the world.</span></span> <span data-ttu-id="8fbab-117">Gestion des packages pour vous assurer que les applications appropriées sont disponibles pour tous les utilisateurs dans lesquels et quand ils ont besoin d’y accéder.</span><span class="sxs-lookup"><span data-stu-id="8fbab-117">Managing the packages to ensure that the appropriate applications are available to all users where and when they need access to them is therefore an important requirement.</span></span>

## <span data-ttu-id="8fbab-118">Fonctionnalités du système de virtualisation des applications Microsoft</span><span class="sxs-lookup"><span data-stu-id="8fbab-118">Microsoft Application Virtualization System Features</span></span>


<span data-ttu-id="8fbab-119">Le tableau suivant décrit les principales fonctionnalités du système de gestion de la virtualisation des applications Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8fbab-119">The following table describes the primary features of the Microsoft Application Virtualization Management System.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8fbab-120">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="8fbab-120">Feature</span></span></th>
<th align="left"><span data-ttu-id="8fbab-121">Fonction</span><span class="sxs-lookup"><span data-stu-id="8fbab-121">Function</span></span></th>
<th align="left"><span data-ttu-id="8fbab-122">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="8fbab-122">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fbab-123">Serveur de gestion de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8fbab-123">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-124">Responsable de la diffusion du contenu du package et de la publication des raccourcis et des associations de types de fichiers sur le client de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8fbab-124">Responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-125">Le serveur de gestion des applications virtuelles prend en charge la mise à niveau active, la gestion des licences et une base de données qui peut être utilisée pour la création de rapports.</span><span class="sxs-lookup"><span data-stu-id="8fbab-125">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8fbab-126">Dossier de contenu </strong></span><span class="sxs-lookup"><span data-stu-id="8fbab-126">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-127">Indique l’emplacement des packages de virtualisation d’application pour la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="8fbab-127">Indicates the location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-128">Ce dossier peut être localisé sur un serveur de gestion de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8fbab-128">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fbab-129">Microsoft Application Virtualization Management Console</span><span class="sxs-lookup"><span data-stu-id="8fbab-129">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-130">Cette console est un outil de gestion des composants enfichables 3,0 de MMC utilisé pour l’administration de serveur Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="8fbab-130">This console is an MMC 3.0 snap-in management tool used for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-131">Cet outil peut être installé sur le serveur Microsoft Application Virtualization ou situé sur une station de travail distincte qui comporte Microsoft Management Console (MMC) 3.0 et Microsoft. NETFramework 2,0 est installé.</span><span class="sxs-lookup"><span data-stu-id="8fbab-131">This tool can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has Microsoft Management Console (MMC)3.0 and Microsoft .NETFramework 2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fbab-132">Service Web de gestion de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8fbab-132">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-133">Responsable de la communication de toutes les demandes de lecture et d’écriture dans le magasin de données de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8fbab-133">Responsible for communicating any read and write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-134">Le service Web de gestion peut être installé sur le serveur de gestion Microsoft Application Virtualization ou sur un autre ordinateur sur lequel Microsoft Internet Information Services (IIS) est installé.</span><span class="sxs-lookup"><span data-stu-id="8fbab-134">The Management Web Service can be installed on the Microsoft Application Virtualization Management server or on a separate computer that has Microsoft Internet Information Services (IIS) installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fbab-135">Magasin de données de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8fbab-135">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-136">La base de données SQL Server App-V chargée du stockage de toutes les informations relatives à l’infrastructure de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8fbab-136">The App-V SQL Server database responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-137">Ces informations incluent tous les enregistrements d’application, les affectations d’application et les groupes responsables de la gestion de l’environnement de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8fbab-137">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fbab-138">Serveur de diffusion de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8fbab-138">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-139">Responsable de l’hébergement des packages de virtualisation d’application destinés à la diffusion en continu vers des clients dans une succursale, où le lien retour au serveur de gestion de l’application virtualisation est considéré comme une connexion de réseau de grande variété.</span><span class="sxs-lookup"><span data-stu-id="8fbab-139">Responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a wide area networks (WAN) connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-140">Ce serveur est doté de la fonctionnalité de diffusion en continu uniquement et ne fournit ni la console de gestion des applications virtuelles, ni le service Web de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="8fbab-140">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fbab-141">Sequencer Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8fbab-141">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-142">Le Sequencer est utilisé pour surveiller et capturer l’installation des applications afin de créer des packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="8fbab-142">The sequencer is used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-143">La sortie se compose d’icônes de l’application, d’un fichier. OSD contenant des informations de définition de package, d’un fichier manifeste de package et du fichier. SFT contenant les fichiers de contenu du programme d’application.</span><span class="sxs-lookup"><span data-stu-id="8fbab-143">The output consists of the application’s icons, an .osd file that contains package definition information, a package manifest file, and the .sft file that contains the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fbab-144">Client Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8fbab-144">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-145">Le client de bureau et le client de virtualisation des applications pour les services Bureau à distance fournissent et gèrent l’environnement virtuel pour les applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="8fbab-145">The Application Virtualization Desktop Client and the Application Virtualization Client for Remote Desktop Services provide and manage the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fbab-146">Le client de virtualisation d’applications Microsoft gère la diffusion du package dans le cache, l’actualisation de la publication, le transport et toute interaction avec les serveurs de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8fbab-146">The Microsoft Application Virtualization client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 






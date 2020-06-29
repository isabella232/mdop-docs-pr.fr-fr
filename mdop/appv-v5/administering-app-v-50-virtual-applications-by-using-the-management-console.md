---
title: Administration d'applications virtuelles App-V5.0 à l'aide de la console de gestion
description: Administration d'applications virtuelles App-V5.0 à l'aide de la console de gestion
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806049"
---
# <span data-ttu-id="8c1d9-103">Administration d'applications virtuelles App-V5.0 à l'aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-103">Administering App-V 5.0 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="8c1d9-104">Le serveur de gestion 5,0 de Microsoft Application Virtualization (App-V) vous permet de gérer les packages, groupes de connexion et accès aux packages dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-104">Use the Microsoft Application Virtualization (App-V) 5.0 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="8c1d9-105">Le serveur publie des icônes d’application, des raccourcis et des associations de types de fichiers sur des ordinateurs autorisés qui exécutent le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="8c1d9-106">Un ou plusieurs serveurs de gestion partagent généralement un magasin de données commun pour la configuration et les informations de package.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="8c1d9-107">Le serveur de gestion utilise les groupes AD DS (Active Directory Domain Services) pour gérer les autorisations de l’utilisateur et SQL Server doit être installé pour gérer la base de données et le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="8c1d9-108">Étant donné que les serveurs de gestion diffusent les applications aux utilisateurs finaux à la demande, ces serveurs sont idéalement adaptés aux configurations système qui disposent de réseaux locaux fiables et à bande passante élevée.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="8c1d9-109">Le serveur de gestion comprend les composants suivants:</span><span class="sxs-lookup"><span data-stu-id="8c1d9-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="8c1d9-110">Serveur de gestion: utilisez le serveur de gestion pour gérer des packages et des groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="8c1d9-111">Serveur de publication: utilisez le serveur de publication pour déployer des packages sur des ordinateurs qui exécutent le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.0 client.</span></span>

-   <span data-ttu-id="8c1d9-112">Base de données de gestion: utilisez la base de données de gestion pour gérer l’accès au package et publier la synchronisation du serveur avec le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="8c1d9-113">Tâches de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-113">Management Console tasks</span></span>


<span data-ttu-id="8c1d9-114">Les tâches les plus courantes que vous pouvez effectuer avec la console de gestion de l’application-V 5,0 sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="8c1d9-114">The most common tasks that you can perform with the App-V 5.0 Management console are:</span></span>

-   [<span data-ttu-id="8c1d9-115">Comment se connecter à la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-beta.md)

-   [<span data-ttu-id="8c1d9-116">Comment ajouter ou mettre à jour des packages à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [<span data-ttu-id="8c1d9-117">Comment configurer l’accès aux packages à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [<span data-ttu-id="8c1d9-118">Comment publier un package à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [<span data-ttu-id="8c1d9-119">Comment supprimer un package dans la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-beta.md)

-   [<span data-ttu-id="8c1d9-120">Comment ajouter ou supprimer un administrateur à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [<span data-ttu-id="8c1d9-121">Comment inscrire et désinscrire un serveur de publication à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [<span data-ttu-id="8c1d9-122">Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.0</span><span class="sxs-lookup"><span data-stu-id="8c1d9-122">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [<span data-ttu-id="8c1d9-123">Comment transférer l'accès et les configurations vers une autre version d'un package à l'aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [<span data-ttu-id="8c1d9-124">Comment personnaliser les extensions d’applications virtuelles d’un groupe AD spécifique à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [<span data-ttu-id="8c1d9-125">Configurer les applications et les extensions d’application virtuelle par défaut dans la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-125">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

<span data-ttu-id="8c1d9-126">Les principaux éléments de la console de gestion de l’application-V 5,0 sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="8c1d9-126">The main elements of the App-V 5.0 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1d9-127">Onglet de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8c1d9-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="8c1d9-128">Description</span><span class="sxs-lookup"><span data-stu-id="8c1d9-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1d9-129">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="8c1d9-129">Overview</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><strong><span data-ttu-id="8c1d9-130">App-V Sequencer </strong> - Sélectionnez cette option pour passer en revue des informations générales sur l’utilisation du séquenceur App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-130">App-V Sequencer</strong> - Select this option to review general information about using the App-V 5.0 sequencer.</span></span></p></li>
<li><p><strong><span data-ttu-id="8c1d9-131">Bibliothèque de packages </strong> d’applications: sélectionnez cette option pour ouvrir la <strong> </strong> page packages de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-131">Application Packages Library</strong> – Select this option to open the <strong>PACKAGES</strong> page of the Management Console.</span></span> <span data-ttu-id="8c1d9-132">Utilisez cette page pour réviser les packages qui ont été ajoutés au serveur.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-132">Use this page to review packages that have been added to the server.</span></span> <span data-ttu-id="8c1d9-133">Vous pouvez également gérer les groupes de connexion, et ajouter ou mettre à niveau des packages.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-133">You can also manage the connection groups, as well as add or upgrade packages.</span></span></p></li>
<li><p><strong><span data-ttu-id="8c1d9-134">SERVEURS </strong> : sélectionnez cette option pour ouvrir la <strong> </strong> page serveurs de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-134">SERVERS</strong> – Select this option to open the <strong>SERVERS</strong> page of the Management Console.</span></span> <span data-ttu-id="8c1d9-135">Utilisez cette page pour passer en revue la liste des serveurs enregistrés avec votre infrastructure App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-135">Use this page to review the list of servers that have been registered with your App-V 5.0 infrastructure.</span></span></p></li>
<li><p><strong><span data-ttu-id="8c1d9-136">CLIENTS </strong> : sélectionnez cette option pour consulter des informations générales sur les clients App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-136">CLIENTS</strong> – Select this option to review general information about App-V 5.0 clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1d9-137">Onglet packages</span><span class="sxs-lookup"><span data-stu-id="8c1d9-137">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1d9-138">Utilisez l' <strong> </strong> onglet packages pour ajouter ou mettre à niveau des packages.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-138">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span> <span data-ttu-id="8c1d9-139">Vous pouvez également gérer les groupes de connexions en cliquant sur <strong> groupes de connexion </strong> .</span><span class="sxs-lookup"><span data-stu-id="8c1d9-139">You can also manage connection groups by clicking <strong>CONNECTION GROUPS</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1d9-140">Onglet serveurs</span><span class="sxs-lookup"><span data-stu-id="8c1d9-140">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1d9-141">Utilisez l' <strong> </strong> onglet serveurs pour inscrire un nouveau serveur.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-141">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1d9-142">Onglet administrateurs</span><span class="sxs-lookup"><span data-stu-id="8c1d9-142">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1d9-143">Utilisez l' <strong> </strong> onglet administrateurs pour inscrire, ajouter ou supprimer des administrateurs dans votre environnement App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8c1d9-143">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.0 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a><span data-ttu-id="8c1d9-144">Autres ressources pour le déploiement de 5,0 App-V</span><span class="sxs-lookup"><span data-stu-id="8c1d9-144">Other resources for this App-V 5.0 deployment</span></span>


-   [<span data-ttu-id="8c1d9-145">Guide de l’administrateur de Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="8c1d9-145">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="8c1d9-146">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="8c1d9-146">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 






---
title: Administration d'applications virtuelles App-V5.1 à l'aide de la console de gestion
description: Administration d'applications virtuelles App-V5.1 à l'aide de la console de gestion
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806048"
---
# <span data-ttu-id="3f407-103">Administration d'applications virtuelles App-V5.1 à l'aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-103">Administering App-V 5.1 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="3f407-104">Le serveur de gestion 5,1 de Microsoft Application Virtualization (App-V) vous permet de gérer les packages, groupes de connexion et accès aux packages dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="3f407-104">Use the Microsoft Application Virtualization (App-V) 5.1 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="3f407-105">Le serveur publie des icônes d’application, des raccourcis et des associations de types de fichiers sur des ordinateurs autorisés qui exécutent le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3f407-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="3f407-106">Un ou plusieurs serveurs de gestion partagent généralement un magasin de données commun pour la configuration et les informations de package.</span><span class="sxs-lookup"><span data-stu-id="3f407-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="3f407-107">Le serveur de gestion utilise les groupes AD DS (Active Directory Domain Services) pour gérer les autorisations de l’utilisateur et SQL Server doit être installé pour gérer la base de données et le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="3f407-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="3f407-108">Étant donné que les serveurs de gestion diffusent les applications aux utilisateurs finaux à la demande, ces serveurs sont idéalement adaptés aux configurations système qui disposent de réseaux locaux fiables et à bande passante élevée.</span><span class="sxs-lookup"><span data-stu-id="3f407-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="3f407-109">Le serveur de gestion comprend les composants suivants:</span><span class="sxs-lookup"><span data-stu-id="3f407-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="3f407-110">Serveur de gestion: utilisez le serveur de gestion pour gérer des packages et des groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="3f407-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="3f407-111">Serveur de publication: utilisez le serveur de publication pour déployer des packages sur des ordinateurs qui exécutent le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3f407-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.1 client.</span></span>

-   <span data-ttu-id="3f407-112">Base de données de gestion: utilisez la base de données de gestion pour gérer l’accès au package et publier la synchronisation du serveur avec le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="3f407-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="3f407-113">Tâches de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-113">Management Console tasks</span></span>


<span data-ttu-id="3f407-114">Les tâches les plus courantes que vous pouvez effectuer avec la console de gestion de l’application-V 5,1 sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="3f407-114">The most common tasks that you can perform with the App-V 5.1 Management console are:</span></span>

-   [<span data-ttu-id="3f407-115">Comment se connecter à la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-51.md)

-   [<span data-ttu-id="3f407-116">Comment ajouter ou mettre à jour des packages à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [<span data-ttu-id="3f407-117">Comment configurer l’accès aux packages à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [<span data-ttu-id="3f407-118">Comment publier un package à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [<span data-ttu-id="3f407-119">Comment supprimer un package dans la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-51.md)

-   [<span data-ttu-id="3f407-120">Comment ajouter ou supprimer un administrateur à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [<span data-ttu-id="3f407-121">Comment inscrire et désinscrire un serveur de publication à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [<span data-ttu-id="3f407-122">Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.1</span><span class="sxs-lookup"><span data-stu-id="3f407-122">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [<span data-ttu-id="3f407-123">Comment transférer l'accès et les configurations vers une autre version d'un package à l'aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [<span data-ttu-id="3f407-124">Comment personnaliser les extensions d’applications virtuelles d’un groupe AD spécifique à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [<span data-ttu-id="3f407-125">Comment afficher et configurer des applications et des extensions de l’application virtuelle par défaut à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-125">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

<span data-ttu-id="3f407-126">Les principaux éléments de la console de gestion de l’application-V 5,1 sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="3f407-126">The main elements of the App-V 5.1 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3f407-127">Onglet de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="3f407-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="3f407-128">Description</span><span class="sxs-lookup"><span data-stu-id="3f407-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f407-129">Onglet packages</span><span class="sxs-lookup"><span data-stu-id="3f407-129">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f407-130">Utilisez l' <strong> </strong> onglet packages pour ajouter ou mettre à niveau des packages.</span><span class="sxs-lookup"><span data-stu-id="3f407-130">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3f407-131">Onglet groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="3f407-131">Connection Groups tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f407-132">Utilisez l' <strong> onglet groupes </strong> de connexions pour gérer les groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="3f407-132">Use the <strong>CONNECTION GROUPS</strong> tab to manage connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f407-133">Onglet serveurs</span><span class="sxs-lookup"><span data-stu-id="3f407-133">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f407-134">Utilisez l' <strong> </strong> onglet serveurs pour inscrire un nouveau serveur.</span><span class="sxs-lookup"><span data-stu-id="3f407-134">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3f407-135">Onglet administrateurs</span><span class="sxs-lookup"><span data-stu-id="3f407-135">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f407-136">Utilisez l' <strong> </strong> onglet administrateurs pour inscrire, ajouter ou supprimer des administrateurs dans votre environnement App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3f407-136">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.1 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3f407-137">**Important**  JavaScript doit être activé dans le navigateur qui ouvre la console de gestion Web.</span><span class="sxs-lookup"><span data-stu-id="3f407-137">**Important** JavaScript must be enabled on the browser that opens the Web Management Console.</span></span>

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a><span data-ttu-id="3f407-138">Autres ressources pour le déploiement de 5,1 App-V</span><span class="sxs-lookup"><span data-stu-id="3f407-138">Other resources for this App-V 5.1 deployment</span></span>


-   [<span data-ttu-id="3f407-139">Guide de l’administrateur de Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="3f407-139">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="3f407-140">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="3f407-140">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 






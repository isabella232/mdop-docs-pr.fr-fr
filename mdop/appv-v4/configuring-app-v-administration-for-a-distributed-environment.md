---
title: Configuration de l'administration d'App-V pour les environnements distribués
description: Configuration de l'administration d'App-V pour les environnements distribués
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809041"
---
# <span data-ttu-id="cd628-103">Configuration de l'administration d'App-V pour les environnements distribués</span><span class="sxs-lookup"><span data-stu-id="cd628-103">Configuring App-V Administration for a Distributed Environment</span></span>


<span data-ttu-id="cd628-104">Lors de la conception de l’infrastructure pour votre organisation spécifique, vous pouvez installer le service Web d’administration des applications sur un ordinateur autre que celui sur lequel vous installez le serveur de gestion des applications-V.</span><span class="sxs-lookup"><span data-stu-id="cd628-104">When designing the infrastructure for your specific organization, you can install the App-V Management Web Service on a computer other than the computer where you install the App-V Management Server.</span></span> <span data-ttu-id="cd628-105">Voici quelques raisons courantes de séparation de ces composants d’application-V:</span><span class="sxs-lookup"><span data-stu-id="cd628-105">Common reasons for separating these App-V components include the following:</span></span>

-   <span data-ttu-id="cd628-106">Niveau de performance</span><span class="sxs-lookup"><span data-stu-id="cd628-106">Performance</span></span>

-   <span data-ttu-id="cd628-107">Fiabilité</span><span class="sxs-lookup"><span data-stu-id="cd628-107">Reliability</span></span>

-   <span data-ttu-id="cd628-108">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="cd628-108">Availability</span></span>

-   <span data-ttu-id="cd628-109">Extensibilité</span><span class="sxs-lookup"><span data-stu-id="cd628-109">Scalability</span></span>

<span data-ttu-id="cd628-110">La séparation du serveur de gestion et du service Web de gestion nécessite une configuration supplémentaire pour que l’infrastructure fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="cd628-110">Separating the Management Server and Management Web Service requires additional configuration for the infrastructure to operate correctly.</span></span> <span data-ttu-id="cd628-111">Lorsque vous séparez ces deux fonctionnalités sans suivre les procédures décrites dans cette rubrique, la console de gestion se connecte au service Web de gestion mais ne peut pas s’authentifier correctement auprès du magasin de données.</span><span class="sxs-lookup"><span data-stu-id="cd628-111">When you separate these two features but do not complete the procedures described in this topic, the Management Console will connect to the Management Web Service but will not be able to properly authenticate with the data store.</span></span> <span data-ttu-id="cd628-112">La console de gestion ne se charge pas correctement et l’administrateur ne peut pas effectuer d’tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="cd628-112">The Management Console will not load properly, and the administrator will not be able to complete any administrative tasks.</span></span>

<span data-ttu-id="cd628-113">Ce comportement se produit parce que le service Web de gestion ne peut pas utiliser les informations d’identification qui lui sont transmises à partir de la console de gestion pour accéder au magasin de données.</span><span class="sxs-lookup"><span data-stu-id="cd628-113">This behavior occurs because the Management Web Service cannot use the credentials, passed to it from the Management Console, to access the data store.</span></span> <span data-ttu-id="cd628-114">La solution consiste à configurer le serveur de service Web de gestion pour être «approuvé pour la délégation».</span><span class="sxs-lookup"><span data-stu-id="cd628-114">The solution is to configure the Management Web Service server to be “Trusted for delegation.”</span></span>

## <span data-ttu-id="cd628-115">Configurer les services de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="cd628-115">Configuring Active Directory Domain Services</span></span>


<span data-ttu-id="cd628-116">Il est également nécessaire de configurer correctement les services de domaine Active Directory pour fonctionner dans un environnement distribué.</span><span class="sxs-lookup"><span data-stu-id="cd628-116">It is also necessary to configure Active Directory Domain Services properly to work in a distributed environment.</span></span> <span data-ttu-id="cd628-117">Cette section inclut les informations dont vous avez besoin pour configurer les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cd628-117">This section includes the information you need configure Active Directory Domain Services.</span></span>

### <span data-ttu-id="cd628-118">Lorsque le service SQL utilise le compte système local</span><span class="sxs-lookup"><span data-stu-id="cd628-118">When SQL Service Uses Local System account</span></span>

<span data-ttu-id="cd628-119">Pour configurer l’environnement dans lequel le service SQL utilise le compte système local, modifiez les propriétés du compte d’ordinateur du service Web de gestion pour qu’il soit approuvé pour la délégation.</span><span class="sxs-lookup"><span data-stu-id="cd628-119">To set up the environment where the SQL Service uses the local system account, change the properties of the machine account of the Management Web Service to be trusted for delegation.</span></span> <span data-ttu-id="cd628-120">Pour plus d’informations sur la façon de procéder, voir [Comment configurer le serveur pour être approuvé pour la délégation](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span><span class="sxs-lookup"><span data-stu-id="cd628-120">For detailed procedures about how to do this, see [How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span></span>

### <span data-ttu-id="cd628-121">Lorsque le service SQL utilise un compte basé sur un domaine</span><span class="sxs-lookup"><span data-stu-id="cd628-121">When SQL Service Uses Domain-Based Account</span></span>

<span data-ttu-id="cd628-122">Pour configurer l’environnement dans lequel les serveurs SQL utilisent des comptes de service basés sur le domaine, vous devez déterminer si un certain nombre de facteurs s’appliquent, y compris:</span><span class="sxs-lookup"><span data-stu-id="cd628-122">To set up the environment where SQL Servers use domain-based service accounts, you need to consider whether or not a variety of factors apply, including the following:</span></span>

-   <span data-ttu-id="cd628-123">Regroupement de SQL Server</span><span class="sxs-lookup"><span data-stu-id="cd628-123">Clustering of SQL Server</span></span>

-   <span data-ttu-id="cd628-124">Réplication</span><span class="sxs-lookup"><span data-stu-id="cd628-124">Replication</span></span>

-   <span data-ttu-id="cd628-125">Tâches automatisées</span><span class="sxs-lookup"><span data-stu-id="cd628-125">Automated tasks</span></span>

-   <span data-ttu-id="cd628-126">Serveurs liés</span><span class="sxs-lookup"><span data-stu-id="cd628-126">Linked servers</span></span>

<span data-ttu-id="cd628-127">Pour plus d’informations sur la configuration des services de domaine Active Directory lorsque le service SQL utilise un compte basé sur un domaine, reportez-vous à la rubrique <https://go.microsoft.com/fwlink/?LinkId=151968> .</span><span class="sxs-lookup"><span data-stu-id="cd628-127">For information about configuring Active Directory Domain Services when the SQL service uses a domain-based account, see <https://go.microsoft.com/fwlink/?LinkId=151968>.</span></span>

 

 






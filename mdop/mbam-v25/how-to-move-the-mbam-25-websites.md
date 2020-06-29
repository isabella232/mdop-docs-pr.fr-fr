---
title: Comment déplacer les sites Web MBAM2.5
description: Comment déplacer les sites Web MBAM2.5
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811340"
---
# <span data-ttu-id="8608f-103">Comment déplacer les sites Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8608f-103">How to Move the MBAM 2.5 Websites</span></span>


<span data-ttu-id="8608f-104">Utilisez ces procédures pour déplacer les sites Web MBAM suivants d’un ordinateur vers un autre, c’est-à-dire pour déplacer les fonctionnalités suivantes du serveur A vers le serveur B:</span><span class="sxs-lookup"><span data-stu-id="8608f-104">Use these procedures to move the following MBAM websites from one computer to another, that is, to move the following features from Server A to Server B:</span></span>

-   <span data-ttu-id="8608f-105">Site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="8608f-105">Administration and Monitoring Website</span></span>

-   <span data-ttu-id="8608f-106">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="8608f-106">Self-Service Portal</span></span>

<span data-ttu-id="8608f-107">**Important**  Lors de la configuration de ces deux sites Web, vous devez fournir la même chaîne de connexion, les URL de rapports, les comptes de groupe et le compte de domaine du pool d’applications de service Web que vous utilisez actuellement.</span><span class="sxs-lookup"><span data-stu-id="8608f-107">**Important** During the configuration of both websites, you must provide the same connection string, Reports URL, group accounts, and web service application pool domain account as the ones that you are currently using.</span></span> <span data-ttu-id="8608f-108">Si vous n’utilisez pas les mêmes valeurs, vous ne pouvez pas accéder à certains serveurs.</span><span class="sxs-lookup"><span data-stu-id="8608f-108">If you don’t use the same values, you cannot access some of the servers.</span></span> <span data-ttu-id="8608f-109">Pour obtenir les valeurs actuelles, utilisez la cmdlet Windows PowerShell **Get-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="8608f-109">To get the current values, use the **Get-MbamWebApplication** Windows PowerShell cmdlet.</span></span>

 

**<span data-ttu-id="8608f-110">Pour déplacer le site Web d’administration et de surveillance vers un autre serveur</span><span class="sxs-lookup"><span data-stu-id="8608f-110">To move the Administration and Monitoring Website to another server</span></span>**

1.  <span data-ttu-id="8608f-111">Sur le serveur B, installez le logiciel serveur MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="8608f-111">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="8608f-112">Pour obtenir des instructions, consultez [installer le logiciel serveur MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="8608f-112">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="8608f-113">Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonctionnalité de **site Web Administration et analyse** .</span><span class="sxs-lookup"><span data-stu-id="8608f-113">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Administration and Monitoring Website** feature.</span></span>

    <span data-ttu-id="8608f-114">Vous pouvez également utiliser l’applet de contrôle Windows PowerShell **Enable-MbamWebApplication** pour configurer le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="8608f-114">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="8608f-115">Pour obtenir des instructions sur la configuration du site Web d’administration et de surveillance, voir [Comment configurer les applications Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8608f-115">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

**<span data-ttu-id="8608f-116">Pour déplacer le portail libre-service vers un autre serveur</span><span class="sxs-lookup"><span data-stu-id="8608f-116">To move the Self-Service Portal to another server</span></span>**

1.  <span data-ttu-id="8608f-117">Sur le serveur B, installez le logiciel serveur MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="8608f-117">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="8608f-118">Pour obtenir des instructions, consultez [installer le logiciel serveur MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="8608f-118">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="8608f-119">Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonctionnalité de **portail libre-service** .</span><span class="sxs-lookup"><span data-stu-id="8608f-119">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Self-Service Portal** feature.</span></span>

    <span data-ttu-id="8608f-120">Vous pouvez également utiliser l’applet de cmdlet Windows PowerShell **Enable-MbamWebApplication** pour configurer le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="8608f-120">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Self-Service Portal.</span></span>

    <span data-ttu-id="8608f-121">Pour obtenir des instructions sur la configuration du site Web d’administration et de surveillance, voir [Comment configurer les applications Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8608f-121">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

3.  <span data-ttu-id="8608f-122">Si les ordinateurs clients de votre organisation n’ont pas accès au réseau de distribution de contenu Microsoft, vous devez également déplacer les fichiers JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8608f-122">If the client computers in your organization do not have access to the Microsoft Content Delivery Network, you also have to move the JavaScript files.</span></span> <span data-ttu-id="8608f-123">Pour plus d’informations, reportez-vous à la rubrique [configuration du portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) .</span><span class="sxs-lookup"><span data-stu-id="8608f-123">See [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) for more information.</span></span>

4.  <span data-ttu-id="8608f-124">Personnaliser le portail libre-service pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8608f-124">Customize the Self-Service Portal for your organization.</span></span> <span data-ttu-id="8608f-125">Utilisez les instructions de la section [Personnalisation du portail libre-service de votre organisation](customizing-the-self-service-portal-for-your-organization.md) pour vérifier vos personnalisations actuelles et configurer des paramètres personnalisés sur le portail libre serveur sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="8608f-125">Use the instructions in [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md) to review your current customizations and to configure custom settings on the Self-Server Portal on Server B.</span></span>



## <span data-ttu-id="8608f-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8608f-126">Related topics</span></span>


[<span data-ttu-id="8608f-127">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8608f-127">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="8608f-128">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8608f-128">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="8608f-129">Déplacement des composants MBAM2.5 vers un autre serveur</span><span class="sxs-lookup"><span data-stu-id="8608f-129">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 

## <span data-ttu-id="8608f-130">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="8608f-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8608f-131">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="8608f-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8608f-132">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8608f-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 






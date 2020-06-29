---
title: Procédure pour installer les serveurs et les composants système
description: Procédure pour installer les serveurs et les composants système
author: dansimp
ms.assetid: c6f5fef0-522a-4ef1-8585-05b292d0289b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ceb5b8376189aee7631229dca912140e454536b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807029"
---
# <span data-ttu-id="100f4-103">Procédure pour installer les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="100f4-103">How to Install the Servers and System Components</span></span>


<span data-ttu-id="100f4-104">Pour pouvoir livrer des applications aux utilisateurs, vous devez installer les composants de plateforme Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="100f4-104">Before you can deliver applications to users, you must install the Microsoft Application Virtualization Platform components.</span></span> <span data-ttu-id="100f4-105">Les rubriques de cette section fournissent les informations nécessaires à l’installation des serveurs de virtualisation des applications et des autres composants du système de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="100f4-105">The topics in this section provide the information required to install the Application Virtualization Servers and the other Application Virtualization System components.</span></span>

<span data-ttu-id="100f4-106">**Remarques**  Les procédures décrites dans cette section vous permettent d’effectuer une installation personnalisée, dans laquelle vous sélectionnez les composants à installer sur des ordinateurs séparés, comme recommandé dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="100f4-106">**Note** The procedures in this section take you through a customized installation, where you pick and choose components to install on separate computers, as recommended in a production environment.</span></span> <span data-ttu-id="100f4-107">Toutefois, vos procédures d’exploitation peuvent dicter une autre approche et, au cours du processus d’installation, vous pouvez regrouper les composants.</span><span class="sxs-lookup"><span data-stu-id="100f4-107">However, your operating procedures might dictate a different approach, and during the installation process you might want to group components together.</span></span> <span data-ttu-id="100f4-108">Quelle que soit l’endroit où vous installez les composants, vous pouvez les installer dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="100f4-108">Regardless of where you install the components, you can install them in any order.</span></span>

 

## <span data-ttu-id="100f4-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="100f4-109">In This Section</span></span>


<a href="" id="how-to-install-application-virtualization-management-server"></a>[<span data-ttu-id="100f4-110">Procédure pour installer le serveur Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="100f4-110">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)  
<span data-ttu-id="100f4-111">Fournit une procédure pas à pas pour l’installation du serveur de gestion des applications et son attribution au groupe de serveurs approprié.</span><span class="sxs-lookup"><span data-stu-id="100f4-111">Provides a step-by-step procedure for installing the Application Virtualization Management Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-application-virtualization-streaming-server"></a>[<span data-ttu-id="100f4-112">Procédure pour installer le serveur Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="100f4-112">How to Install the Application Virtualization Streaming Server</span></span>](how-to-install-the-application-virtualization-streaming-server.md)  
<span data-ttu-id="100f4-113">Fournit une procédure pas à pas pour l’installation du serveur de diffusion de la virtualisation des applications et son attribution au groupe de serveurs approprié.</span><span class="sxs-lookup"><span data-stu-id="100f4-113">Provides a step-by-step procedure for installing the Application Virtualization Streaming Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-management-web-service"></a>[<span data-ttu-id="100f4-114">Procédure pour installer le service de gestion Web</span><span class="sxs-lookup"><span data-stu-id="100f4-114">How to Install the Management Web Service</span></span>](how-to-install-the-management-web-service.md)  
<span data-ttu-id="100f4-115">Fournit une procédure pas à pas pour l’installation du service Web Application Virtualization sur un ordinateur cible sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="100f4-115">Provides a step-by-step procedure for installing the Application Virtualization Management Web Service on a target computer on your network.</span></span>

<a href="" id="how-to-install-the-management-console"></a>[<span data-ttu-id="100f4-116">Procédure pour installer la console de gestion</span><span class="sxs-lookup"><span data-stu-id="100f4-116">How to Install the Management Console</span></span>](how-to-install-the-management-console.md)  
<span data-ttu-id="100f4-117">Fournit une procédure pas à pas pour l’installation de la console de gestion des applications sur un ordinateur cible sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="100f4-117">Provides a step-by-step procedure for installing the Application Virtualization Management Console on a target computer on your network.</span></span>

<a href="" id="how-to-install-a-database"></a>[<span data-ttu-id="100f4-118">Procédure pour installer une base de données</span><span class="sxs-lookup"><span data-stu-id="100f4-118">How to Install a Database</span></span>](how-to-install-a-database.md)  
<span data-ttu-id="100f4-119">Fournit une procédure détaillée pour l’installation d’une base de données pour le déploiement de la virtualisation de l’application sur serveur, si une base de données n’est pas encore disponible.</span><span class="sxs-lookup"><span data-stu-id="100f4-119">Provides a step-by-step procedure for installing a database for your server-based deployment of Application Virtualization, if a database is not already available.</span></span>

<a href="" id="how-to-remove-the-application-virtualization-system-components"></a>[<span data-ttu-id="100f4-120">Procédure de suppression des composants du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="100f4-120">How to Remove the Application Virtualization System Components</span></span>](how-to-remove-the-application-virtualization-system-components.md)  
<span data-ttu-id="100f4-121">Fournit des procédures pas à pas pour supprimer tous les composants logiciels de virtualisation des applications ou ceux sélectionnés sur un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="100f4-121">Provides step-by-step procedures to remove all or selected Application Virtualization software components from a target computer.</span></span>

## <span data-ttu-id="100f4-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="100f4-122">Related topics</span></span>


[<span data-ttu-id="100f4-123">Présentation du scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="100f4-123">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="100f4-124">Procédure pour configurer des serveurs pour un déploiement basé sur un serveur</span><span class="sxs-lookup"><span data-stu-id="100f4-124">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="100f4-125">Procédure pour mettre à niveau les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="100f4-125">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)

 

 






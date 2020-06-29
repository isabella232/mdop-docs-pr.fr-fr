---
title: À propos de Microsoft Application Virtualization4.5
description: À propos de Microsoft Application Virtualization4.5
author: dansimp
ms.assetid: 39f45a6f-ac55-4fd7-8a83-865e1a7034f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 30f285680ab24e9c638ff8a200946925074bddf1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808142"
---
# <span data-ttu-id="1e1ea-103">À propos de Microsoft Application Virtualization4.5</span><span class="sxs-lookup"><span data-stu-id="1e1ea-103">About Microsoft Application Virtualization 4.5</span></span>


<span data-ttu-id="1e1ea-104">Auparavant appelé virtualisation des applications SoftGrid, Microsoft Application Virtualization (App-V) 4,5 est la première version de marque Microsoft du produit.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-104">Formerly known as SoftGrid Application Virtualization, Microsoft Application Virtualization (App-V) 4.5 is the first Microsoft-branded release of the product.</span></span> <span data-ttu-id="1e1ea-105">Il inclut de nouvelles fonctionnalités qui permettent aux organisations informatiques d’entreprise de prendre en charge les implémentations de virtualisation d’application globales à grande échelle.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-105">It includes new capabilities that make it easy for enterprise IT organizations to support large-scale, global application virtualization implementations.</span></span>

-   <span data-ttu-id="1e1ea-106">Virtualisation dynamique: App-V 4,5 offre la possibilité de contrôler l’interaction des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-106">Dynamic Virtualization: App-V 4.5 provides the flexibility to control virtual application interaction.</span></span> <span data-ttu-id="1e1ea-107">Les administrateurs désireux de consolider les environnements virtuels et de garantir une administration plus rapide et plus facile peuvent utiliser la composition de suite dynamique du produit, qui effectue et gère les packages pour les applications middleware séparément de l’application principale.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-107">Administrators who want to consolidate virtual environments and enable faster, easier administration, can use the product’s Dynamic Suite Composition, which sequences and manages packages for middleware applications separately from the main application.</span></span> <span data-ttu-id="1e1ea-108">Elle réduit la taille de package potentielle en éliminant l’emballage redondant d’un middleware.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-108">It shrinks potential package size by eliminating redundant packaging of middleware.</span></span> <span data-ttu-id="1e1ea-109">Cela permet à plusieurs applications Web de communiquer avec la même instance unique d’une application virtualisée, par exemple, Microsoft .NET Framework ou l’environnement Java Runtime Environment (JRE).</span><span class="sxs-lookup"><span data-stu-id="1e1ea-109">This lets multiple Web applications communicate with the same single instance of a virtualized application of, for example, Microsoft .NET Framework or Sun Java Runtime Environment (JRE).</span></span> <span data-ttu-id="1e1ea-110">Les mises à jour du middleware virtuel commun sont simplifiées et une application virtuelle est mise à jour au lieu de plusieurs.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-110">Updates for the common virtual middleware are simplified and one virtual application is updated instead of several.</span></span> <span data-ttu-id="1e1ea-111">Cette fonctionnalité «plusieurs-à-un» réduit considérablement le coût des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-111">This “many-to-one” capability greatly reduces the cost of updates.</span></span> <span data-ttu-id="1e1ea-112">Il facilite également le déploiement et la gestion des applications qui utilisent plusieurs composants enfichables et compléments, ainsi que la gestion de la distribution des plug-in avec différents groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-112">It also makes it easier to deploy and manage applications that use multiple plug-ins and add-ins, and improves management of plug-in distribution to different user groups.</span></span>

-   <span data-ttu-id="1e1ea-113">Extensibilité étendue: Choisissez parmi trois modes de déploiement flexibles:</span><span class="sxs-lookup"><span data-stu-id="1e1ea-113">Extended Scalability: Choose among three flexible deployment modes:</span></span>

    1.  <span data-ttu-id="1e1ea-114">Le serveur de gestion des applications virtuelles, qui est fourni avec le pack d’optimisation de la version de bureau de Microsoft et Microsoft Application Virtualization pour les packages de services Bureau à distance, permet un streaming dynamique incluant les mises à jour de package et actives, et nécessite Microsoft Active Directory Domain Services et Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-114">Application Virtualization Management Server, which ships as part of the Microsoft Desktop Optimization Pack and Microsoft Application Virtualization for Remote Desktop Services packages, enables dynamic streaming including package and active upgrades, and requires Microsoft Active Directory Domain Services and Microsoft SQL Server.</span></span>

    2.  <span data-ttu-id="1e1ea-115">Le serveur de diffusion de contenu de l’application, une version légère, qui est également fournie avec le pack d’optimisation de bureau de Microsoft et Microsoft Application Virtualization pour les packages de services Bureau à distance, propose une application en continu incluant des packages et des mises à niveau actives, sans les services de domaine Active Directory et de base de données, et permet aux administrateurs d’effectuer des déploiements sur des serveurs</span><span class="sxs-lookup"><span data-stu-id="1e1ea-115">Application Virtualization Streaming Server, a lightweight version which also ships as part of the Microsoft Desktop Optimization Pack and Microsoft Application Virtualization for Remote Desktop Services packages, offers application streaming including package and active upgrades without the Active Directory Domain Services and database overheads, and enables administrators to deploy to existing servers or add streaming to Electronic Software Delivery (ESD) systems.</span></span>

    3.  <span data-ttu-id="1e1ea-116">Le mode autonome permet aux applications virtuelles de s’exécuter sans diffusion en continu et est compatible avec Microsoft Endpoint Manager et systèmes ESD tiers.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-116">Standalone mode enables virtual applications to run without streaming and is interoperable with Microsoft Endpoint Configuration Manager and third-party ESD systems.</span></span>

-   <span data-ttu-id="1e1ea-117">Globalisation: le produit est localisé dans 11 langues, inclut la prise en charge des applications linguistiques étrangères qui utilisent des caractères spéciaux, et prend en charge l’activation de l’annuaire Active Directory et des serveurs et des paramètres régionaux d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-117">Globalization: The product is localized across 11 languages, includes support for foreign language applications that use special characters, and supports foreign language Active Directory and servers and runtime locale detection.</span></span>

-   <span data-ttu-id="1e1ea-118">Normes de sécurité Microsoft: Microsoft Application Virtualization (App-V) 4,5 est conforme aux normes de sécurité Microsoft, y compris à l’informatique digne de confiance, à l’initiative sécurisée et au cycle de développement de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-118">Microsoft Security Standards: Microsoft Application Virtualization (App-V) 4.5 complies with Microsoft security standards including Trustworthy Computing, Secure Windows Initiative and Security Development Lifecycle.</span></span> <span data-ttu-id="1e1ea-119">Il inclut la prise en charge des scénarios Internet et offre une configuration par défaut sécurisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-119">It includes support for Internet-facing scenarios and provides Secure by Default configuration out of the box.</span></span>

## <span data-ttu-id="1e1ea-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="1e1ea-120">In This Section</span></span>


<a href="" id="microsoft-application-virtualization-management-system-release-notes"></a>[<span data-ttu-id="1e1ea-121">Notes de publication sur le système de gestion des applications Microsoft application</span><span class="sxs-lookup"><span data-stu-id="1e1ea-121">Microsoft Application Virtualization Management System Release Notes</span></span>](microsoft-application-virtualization-management-system-release-notes.md)  
<span data-ttu-id="1e1ea-122">Fournit les informations les plus récentes sur les problèmes connus de Microsoft Application Virtualization (App-V) 4,5.</span><span class="sxs-lookup"><span data-stu-id="1e1ea-122">Provides the most up-to-date information about known issues with Microsoft Application Virtualization (App-V) 4.5.</span></span>

 

 






---
title: À propos de l'octroi de licence pour les applications
description: À propos de l'octroi de licence pour les applications
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808170"
---
# <span data-ttu-id="d20da-103">À propos de l'octroi de licence pour les applications</span><span class="sxs-lookup"><span data-stu-id="d20da-103">About Application Licensing</span></span>


<span data-ttu-id="d20da-104">Vous pouvez gérer les licences d’application directement à partir de la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="d20da-104">You can manage application licenses directly from the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="d20da-105">Types de licence</span><span class="sxs-lookup"><span data-stu-id="d20da-105">License Types</span></span>


<span data-ttu-id="d20da-106">Le système de virtualisation des applications System Center prend actuellement en charge les types de licence suivants:</span><span class="sxs-lookup"><span data-stu-id="d20da-106">The System Center Application Virtualization System currently supports the following license types:</span></span>

-   <span data-ttu-id="d20da-107">**Licence illimitée**: permet d’accéder à l’application par n’importe quel nombre d’utilisateurs simultanés.</span><span class="sxs-lookup"><span data-stu-id="d20da-107">**Unlimited License**—Allows access to the application by any number of simultaneous users.</span></span> <span data-ttu-id="d20da-108">Cette méthode de gestion des licences est appropriée lorsque vous voulez associer une licence à l’échelle de l’entreprise à une application.</span><span class="sxs-lookup"><span data-stu-id="d20da-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="d20da-109">**Licence simultanée**: permet de définir le nombre maximal d’utilisateurs simultanés autorisés à utiliser l’application.</span><span class="sxs-lookup"><span data-stu-id="d20da-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="d20da-110">**Licence nommée**: vous permet d’attribuer une licence à un utilisateur individuel.</span><span class="sxs-lookup"><span data-stu-id="d20da-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="d20da-111">Une licence nommée peut être utilisée pour s’assurer qu’un utilisateur particulier sera toujours en mesure d’exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="d20da-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="d20da-112">Vous pouvez combiner des licences concomitantes et nommées pour la même application.</span><span class="sxs-lookup"><span data-stu-id="d20da-112">You can combine concurrent and named licenses for the same application.</span></span>

<span data-ttu-id="d20da-113">La gestion des licences est désactivée par défaut, mais vous pouvez l’activer à partir de l’onglet **pipeline du fournisseur** de la boîte de dialogue **Propriétés du fournisseur** .</span><span class="sxs-lookup"><span data-stu-id="d20da-113">Licensing is disabled by default, but you can enable it from the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span> <span data-ttu-id="d20da-114">Pour plus d’informations sur l’activation et la désactivation de la gestion des licences, voir [Comment configurer ou désactiver la gestion des licences d’applications](how-to-set-up-or-disable-application-licensing.md).</span><span class="sxs-lookup"><span data-stu-id="d20da-114">For details about enabling and disabling licensing, see [How to Set Up or Disable Application Licensing](how-to-set-up-or-disable-application-licensing.md).</span></span>

## <span data-ttu-id="d20da-115">Stratégies du fournisseur</span><span class="sxs-lookup"><span data-stu-id="d20da-115">Provider Policies</span></span>


<span data-ttu-id="d20da-116">Des stratégies de fournisseur ont été développées pour le modèle de fournisseur de services d’application (ASP).</span><span class="sxs-lookup"><span data-stu-id="d20da-116">Provider policies were developed for the Application Service Provider (ASP) model.</span></span> <span data-ttu-id="d20da-117">Dans ce modèle, un seul ASP peut héberger un système de virtualisation d’application unique pour plusieurs clients, où chaque client doit rester isolé.</span><span class="sxs-lookup"><span data-stu-id="d20da-117">In this model, a single ASP can host a single Application Virtualization System for multiple clients, where each client needs to remain isolated.</span></span> <span data-ttu-id="d20da-118">Les clients peuvent avoir considérablement différentes exigences (par exemple, un client peut nécessiter une authentification alors qu’il n’en existe pas).</span><span class="sxs-lookup"><span data-stu-id="d20da-118">Clients might have dramatically different requirements—for example, one client might require authentication while another does not.</span></span> <span data-ttu-id="d20da-119">Vous pouvez utiliser des stratégies de fournisseur pour associer des autorisations aux clients de sorte que seuls les utilisateurs approuvés puissent accéder à chaque application virtuelle ou package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d20da-119">You can use provider policies to associate permissions with clients so that only the approved users can access each virtual application or virtual application package.</span></span>

<span data-ttu-id="d20da-120">Pour les clients d’entreprise, vous pouvez utiliser cette fonctionnalité lorsque vous avez strictement besoin des licences pour une ou plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="d20da-120">For the enterprise customer, you can use this feature when you have strict licensing requirements for one or more applications.</span></span> <span data-ttu-id="d20da-121">Dans cette situation, le composant gestion des licences est désactivé sous l’onglet **pipeline du fournisseur** de la boîte de dialogue **Propriétés du fournisseur** .</span><span class="sxs-lookup"><span data-stu-id="d20da-121">Under this situation, the licensing component is disabled on the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span>

<span data-ttu-id="d20da-122">L’onglet **pipeline du fournisseur** comporte également des cases à cocher pour activer l’authentification, l’autorisation (**appliquer les paramètres d’autorisation d’accès**) et la mesure (informations d'**utilisation du journal**).</span><span class="sxs-lookup"><span data-stu-id="d20da-122">The **Provider Pipeline** tab also has check boxes to enable authentication, authorization (**Enforce Access Permission Settings**), and metering (**Log Usage Information**).</span></span> <span data-ttu-id="d20da-123">Si votre configuration présente des exigences spéciales, vous pouvez écrire vos propres composants de pipeline et les ajouter au système en cliquant sur le bouton **avancé** .</span><span class="sxs-lookup"><span data-stu-id="d20da-123">If your configuration has special requirements, you can write your own pipeline components and add them to the system by clicking the **Advanced** button.</span></span>

## <span data-ttu-id="d20da-124">Autorités de compte</span><span class="sxs-lookup"><span data-stu-id="d20da-124">Account Authorities</span></span>


<span data-ttu-id="d20da-125">L’autorité de compte est le domaine dans lequel le serveur de virtualisation d’application est installé.</span><span class="sxs-lookup"><span data-stu-id="d20da-125">The account authority is the domain in which the Application Virtualization Server is installed.</span></span> <span data-ttu-id="d20da-126">Lorsque vous parcourez l’installation du serveur, vous êtes invité à fournir un nom de domaine; le domaine dans lequel l’ordinateur est installé est détecté et utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="d20da-126">As you proceed through the server installation, you are prompted to supply a domain name; the domain in which the computer is installed is detected and used by default.</span></span> <span data-ttu-id="d20da-127">Lorsque les utilisateurs essaient de se connecter au système, ils sont invités à entrer leurs informations d’identification avant de pouvoir accéder à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="d20da-127">When users attempt to log in to the system, they are prompted for their credentials before they can access that domain.</span></span>

<span data-ttu-id="d20da-128">Le système de virtualisation des applications prend en charge plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="d20da-128">The Application Virtualization System supports multiple domains.</span></span> <span data-ttu-id="d20da-129">Vous pouvez accorder l’accès à l’application aux groupes d’utilisateurs dans d’autres domaines si une relation d’approbation est établie entre les domaines.</span><span class="sxs-lookup"><span data-stu-id="d20da-129">You can grant application access to user groups in other domains if a trust relationship is established between domains.</span></span> <span data-ttu-id="d20da-130">Les utilisateurs doivent fournir des informations d’identification reconnues par chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="d20da-130">Users must supply credentials that are recognized by each domain.</span></span>

<span data-ttu-id="d20da-131">Dans la console de gestion du serveur d’applications, vous pouvez modifier le domaine principal (autorité de compte) et les informations d’identification qui sont utilisées pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="d20da-131">In the Application Virtualization Server Management Console, you can change the primary domain (account authority) and the credentials that are used to access it.</span></span>

## <span data-ttu-id="d20da-132">Authentification</span><span class="sxs-lookup"><span data-stu-id="d20da-132">Authentication</span></span>


<span data-ttu-id="d20da-133">L’authentification est le mécanisme utilisé pour confirmer l’identité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d20da-133">Authentication is the mechanism used to confirm a user's identity.</span></span> <span data-ttu-id="d20da-134">Tout utilisateur disposant d’un nom d’utilisateur et d’un mot de passe reconnus a accès.</span><span class="sxs-lookup"><span data-stu-id="d20da-134">Any user with a recognized user name and password has access.</span></span>

<span data-ttu-id="d20da-135">Dans le système de virtualisation des applications, vous pouvez activer ou désactiver l’authentification par le biais d’une case à cocher sous l’onglet **pipeline du fournisseur** . Par défaut, l’authentification Windows est activée.</span><span class="sxs-lookup"><span data-stu-id="d20da-135">In the Application Virtualization System, you can enable or disable authentication through a check box on the **Provider Pipeline** tab. By default, Windows Authentication is enabled.</span></span>

## <span data-ttu-id="d20da-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="d20da-136">Authorization</span></span>


<span data-ttu-id="d20da-137">Authorization est le processus utilisé pour confirmer l’identité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d20da-137">Authorization is the process used to confirm a user’s identity.</span></span> <span data-ttu-id="d20da-138">Après confirmation de l’identité de l’utilisateur, le système détermine s’il a accordé l’accès au système et aux applications auxquelles l’utilisateur a été autorisé à accéder.</span><span class="sxs-lookup"><span data-stu-id="d20da-138">After confirming the user's identity, the system determines whether the user was granted access to the system and to which applications the user was granted access.</span></span> <span data-ttu-id="d20da-139">La console de gestion du serveur d’applications est doté de la case à cocher **appliquer les paramètres d’autorisation d’accès** dans l’onglet **pipeline du fournisseur** pour activer ou désactiver l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="d20da-139">The Application Virtualization Server Management Console has an **Enforce Access Permission Settings** check box on the **Provider Pipeline** tab to enable or disable authorization.</span></span>

<span data-ttu-id="d20da-140">Dans le système de virtualisation des applications, Access est accordé uniquement à un groupe d’utilisateurs, et non à des utilisateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="d20da-140">In the Application Virtualization System, access is granted to a user group only, not to individual users.</span></span>

## <span data-ttu-id="d20da-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d20da-141">Related topics</span></span>


[<span data-ttu-id="d20da-142">Procédure pour gérer des licences d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="d20da-142">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="d20da-143">Procédure pour configurer ou désactiver l'octroi de licence pour les applications</span><span class="sxs-lookup"><span data-stu-id="d20da-143">How to Set Up or Disable Application Licensing</span></span>](how-to-set-up-or-disable-application-licensing.md)

[<span data-ttu-id="d20da-144">Server Management Console: nœud Stratégies du fournisseur</span><span class="sxs-lookup"><span data-stu-id="d20da-144">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 






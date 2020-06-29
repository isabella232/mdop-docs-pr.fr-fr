---
title: Prise en main de l'application App-V5.1
description: Prise en main de l'application App-V5.1
author: dansimp
ms.assetid: 49a20e1f-0566-4e53-a417-1521393fc974
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff10f12bc672a24f2837f50bfb1f0033ede3e46f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805809"
---
# <span data-ttu-id="e9b19-103">Prise en main de l'application App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-103">Getting Started with App-V 5.1</span></span>


<span data-ttu-id="e9b19-104">Microsoft Application Virtualization (App-V) 5,1 permet aux administrateurs de déployer, de mettre à jour et de prendre en charge des applications en temps réel, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="e9b19-104">Microsoft Application Virtualization (App-V) 5.1 enables administrators to deploy, update, and support applications as services in real time, on an as-needed basis.</span></span> <span data-ttu-id="e9b19-105">Les applications individuelles sont transformées à partir de produits installés en local en services gérés de manière centralisée et sont disponibles où vous le souhaitez, sans que vous ayez besoin de préconfigurer des ordinateurs ou de modifier les paramètres du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e9b19-105">Individual applications are transformed from locally installed products into centrally managed services and are available wherever you need, without the need to preconfigure computers or to change operating system settings.</span></span>

<span data-ttu-id="e9b19-106">App-V se compose des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="e9b19-106">App-V consists of the following elements:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e9b19-107">Élément</span><span class="sxs-lookup"><span data-stu-id="e9b19-107">Element</span></span></th>
<th align="left"><span data-ttu-id="e9b19-108">Description</span><span class="sxs-lookup"><span data-stu-id="e9b19-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e9b19-109">Serveur de gestion App-V</span><span class="sxs-lookup"><span data-stu-id="e9b19-109">App-V Management Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e9b19-110">Fournit un emplacement central pour la gestion de l’infrastructure App-V, qui offre des applications virtuelles au client de bureau App-V et au client de services Bureau à distance (anciennement services Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="e9b19-110">Provides a central location for managing the App-V infrastructure, which delivers virtual applications to both the App-V Desktop Client and the Remote Desktop Services (formerly Terminal Services) Client.</span></span></p></li>
<li><p><span data-ttu-id="e9b19-111">Utilise Microsoft SQL Server® pour le magasin de données, dans lequel un ou plusieurs serveurs d’administration d’applications-V peuvent partager un seul magasin de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9b19-111">Uses Microsoft SQL Server® for its data store, where one or more App-V Management servers can share a single SQL Server data store.</span></span></p></li>
<li><p><span data-ttu-id="e9b19-112">Authentifie les demandes et assure la sécurité, la mesure, la surveillance et la collecte des données.</span><span class="sxs-lookup"><span data-stu-id="e9b19-112">Authenticates requests and provides security, metering, monitoring, and data gathering.</span></span> <span data-ttu-id="e9b19-113">Le serveur utilise Active Directory et des outils de support pour gérer les utilisateurs et les applications.</span><span class="sxs-lookup"><span data-stu-id="e9b19-113">The server uses Active Directory and supporting tools to manage users and applications.</span></span></p></li>
<li><p><span data-ttu-id="e9b19-114">Dispose d’un site de gestion qui vous permet de configurer l’infrastructure App-V sur n’importe quel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e9b19-114">Has a management site that lets you configure the App-V infrastructure from any computer.</span></span> <span data-ttu-id="e9b19-115">Vous pouvez ajouter et supprimer des applications, manipuler des raccourcis, attribuer des autorisations d’accès à des utilisateurs et des groupes, et créer des groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="e9b19-115">You can add and remove applications, manipulate shortcuts, assign access permissions to users and groups, and create connection groups.</span></span></p></li>
<li><p><span data-ttu-id="e9b19-116">Autorise la communication entre la console de gestion Web App-V et le magasin de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9b19-116">Enables communication between the App-V Web Management Console and the SQL Server data store.</span></span> <span data-ttu-id="e9b19-117">Ces composants peuvent tous être installés sur un ordinateur serveur unique ou sur un ou plusieurs ordinateurs séparés, en fonction de l’architecture système requise.</span><span class="sxs-lookup"><span data-stu-id="e9b19-117">These components can all be installed on a single server computer, or on one or more separate computers, depending on the required system architecture.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e9b19-118">Serveur de publication App-V</span><span class="sxs-lookup"><span data-stu-id="e9b19-118">App-V Publishing Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e9b19-119">Fournit aux clients App-V des applications d’habilitation pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="e9b19-119">Provides App-V Clients with entitled applications for the specific user</span></span></p></li>
<li><p><span data-ttu-id="e9b19-120">Héberge le package d’application virtuel pour le streaming.</span><span class="sxs-lookup"><span data-stu-id="e9b19-120">Hosts the virtual application package for streaming.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e9b19-121">Client de bureau App-V</span><span class="sxs-lookup"><span data-stu-id="e9b19-121">App-V Desktop Client</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e9b19-122">Récupère les applications virtuelles</span><span class="sxs-lookup"><span data-stu-id="e9b19-122">Retrieves virtual applications</span></span></p></li>
<li><p><span data-ttu-id="e9b19-123">Publie les applications sur les clients.</span><span class="sxs-lookup"><span data-stu-id="e9b19-123">Publishes the applications on the clients</span></span></p></li>
<li><p><span data-ttu-id="e9b19-124">Configure et gère automatiquement les environnements virtuels lors de l’exécution sur les points de terminaison Windows.</span><span class="sxs-lookup"><span data-stu-id="e9b19-124">Automatically sets up and manages virtual environments at runtime on Windows endpoints.</span></span></p></li>
<li><p><span data-ttu-id="e9b19-125">Stocke des paramètres d’application virtuelle spécifiques à l’utilisateur, tels que des modifications de Registre et de fichier, dans chaque profil utilisateur&#39;s.</span><span class="sxs-lookup"><span data-stu-id="e9b19-125">Stores user-specific virtual application settings, such as registry and file changes, in each user&#39;s profile.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e9b19-126">Client App-V Remote Desktop Services (RDS)</span><span class="sxs-lookup"><span data-stu-id="e9b19-126">App-V Remote Desktop Services (RDS) Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="e9b19-127">Permet aux serveurs hôtes de session Bureau à distance d’utiliser les fonctionnalités du client de bureau App-V pour les sessions de bureau partagées.</span><span class="sxs-lookup"><span data-stu-id="e9b19-127">Enables Remote Desktop Session Host servers to use the capabilities of the App-V Desktop Client for shared desktop sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e9b19-128">Séquenceur App-V</span><span class="sxs-lookup"><span data-stu-id="e9b19-128">App-V Sequencer</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e9b19-129">Est un outil qui permet de transformer des applications traditionnelles en applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="e9b19-129">Is a wizard-based tool that you use to transform traditional applications into virtual applications.</span></span></p></li>
<li><p><span data-ttu-id="e9b19-130">Produit l’application «package», qui se compose des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="e9b19-130">Produces the application “package,” which consists of:</span></span></p>
<ol>
<li><p><span data-ttu-id="e9b19-131">fichier de l’application séquencé (APPV)</span><span class="sxs-lookup"><span data-stu-id="e9b19-131">a sequenced application (APPV) file</span></span></p></li>
<li><p><span data-ttu-id="e9b19-132">fichier Windows Installer (MSI) qui peut être déployé sur des clients configurés pour une opération autonome</span><span class="sxs-lookup"><span data-stu-id="e9b19-132">a Windows Installer file (MSI) that can be deployed to clients configured for stand-alone operation</span></span></p></li>
<li><p><span data-ttu-id="e9b19-133">Plusieurs fichiers XML, dont Report.XML, PackageName_DeploymentConfig.XML et PackageName_UserConfig.XML.</span><span class="sxs-lookup"><span data-stu-id="e9b19-133">Several XML files including Report.XML, PackageName_DeploymentConfig.XML, and PackageName_UserConfig.XML.</span></span> <span data-ttu-id="e9b19-134">Les fichiers XML UserConfig et DeploymentConfig permettent de configurer des modifications personnalisées du comportement par défaut du package.</span><span class="sxs-lookup"><span data-stu-id="e9b19-134">The UserConfig and DeploymentConfig XML files are used to configure custom changes to the default behavior of the package.</span></span></p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e9b19-135">Pour plus d’informations sur ces éléments, voir [architecture de haut niveau pour App-V 5,1](high-level-architecture-for-app-v-51.md).</span><span class="sxs-lookup"><span data-stu-id="e9b19-135">For more information about these elements, see [High Level Architecture for App-V 5.1](high-level-architecture-for-app-v-51.md).</span></span>

<span data-ttu-id="e9b19-136">Si vous débutez avec ce produit, nous vous conseillons de lire entièrement la documentation.</span><span class="sxs-lookup"><span data-stu-id="e9b19-136">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="e9b19-137">Avant de déployer celle-ci dans un environnement de production, nous vous conseillons également de valider votre plan de déploiement dans un environnement réseau de test.</span><span class="sxs-lookup"><span data-stu-id="e9b19-137">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="e9b19-138">Vous pouvez également envisager de prendre un cours sur les technologies pertinentes.</span><span class="sxs-lookup"><span data-stu-id="e9b19-138">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="e9b19-139">Pour plus d’informations sur les opportunités de formation Microsoft, voir la présentation de la formation Microsoft à l’adresse <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="e9b19-139">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="e9b19-140">**Remarques**  La version téléchargeable du Guide de l’administrateur n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="e9b19-140">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="e9b19-141">En revanche, vous pouvez en savoir plus sur un mode spécial de la bibliothèque TechNet qui vous permet de sélectionner des articles, de les regrouper dans une collection et de les imprimer ou de les exporter vers un fichier à partir de <https://go.microsoft.com/fwlink/?LinkId=272491> ( https://go.microsoft.com/fwlink/?LinkId=272491) .</span><span class="sxs-lookup"><span data-stu-id="e9b19-141">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272491> (https://go.microsoft.com/fwlink/?LinkId=272491).</span></span>

 

<span data-ttu-id="e9b19-142">Cette section du Guide de l’administrateur d’application-V 5,1 inclut des informations de haut niveau sur App-V 5,1 pour vous offrir une connaissance de base du produit avant de commencer la planification du déploiement.</span><span class="sxs-lookup"><span data-stu-id="e9b19-142">This section of the App-V 5.1 Administrator’s Guide includes high-level information about App-V 5.1 to provide you with a basic understanding of the product before you begin the deployment planning.</span></span>

## <span data-ttu-id="e9b19-143">Commencer à utiliser App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="e9b19-143">Getting started with App-V 5.1</span></span>


-   [<span data-ttu-id="e9b19-144">À propos d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-144">About App-V 5.1</span></span>](about-app-v-51.md)

    <span data-ttu-id="e9b19-145">Fournit une vue d’ensemble détaillée de App-V 5,1 et de la manière dont il peut être utilisé au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e9b19-145">Provides a high-level overview of App-V 5.1 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="e9b19-146">Évaluation d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-146">Evaluating App-V 5.1</span></span>](evaluating-app-v-51.md)

    <span data-ttu-id="e9b19-147">Fournit des informations sur la façon dont vous pouvez optimiser l’utilisation de App-V 5,1 au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e9b19-147">Provides information about how you can best evaluate App-V 5.1 for use in your organization.</span></span>

-   [<span data-ttu-id="e9b19-148">Architecture de haut niveau pour App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-148">High Level Architecture for App-V 5.1</span></span>](high-level-architecture-for-app-v-51.md)

    <span data-ttu-id="e9b19-149">Décrit les fonctionnalités de 5,1 App-V et la façon dont elles fonctionnent ensemble.</span><span class="sxs-lookup"><span data-stu-id="e9b19-149">Provides a description of the App-V 5.1 features and how they work together.</span></span>

-   [<span data-ttu-id="e9b19-150">Accessibilité d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-150">Accessibility for App-V 5.1</span></span>](accessibility-for-app-v-51.md)

    <span data-ttu-id="e9b19-151">Fournit des informations sur les fonctionnalités et les services qui rendent ce produit et sa documentation correspondante plus accessibles aux personnes atteintes de handicaps.</span><span class="sxs-lookup"><span data-stu-id="e9b19-151">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="e9b19-152">Autres ressources pour ce produit</span><span class="sxs-lookup"><span data-stu-id="e9b19-152">Other resources for this product</span></span>


-   [<span data-ttu-id="e9b19-153">Guide de l’administrateur de Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="e9b19-153">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="e9b19-154">Planification d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-154">Planning for App-V 5.1</span></span>](planning-for-app-v-51.md)

-   [<span data-ttu-id="e9b19-155">Déploiement d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-155">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

-   [<span data-ttu-id="e9b19-156">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-156">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

-   [<span data-ttu-id="e9b19-157">Résolution de problèmes d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-157">Troubleshooting App-V 5.1</span></span>](troubleshooting-app-v-51.md)

-   [<span data-ttu-id="e9b19-158">Référence technique pour App-V5.1</span><span class="sxs-lookup"><span data-stu-id="e9b19-158">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)






 

 






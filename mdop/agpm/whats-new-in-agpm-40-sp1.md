---
title: Nouveautés d'AGPM4.0SP1
description: Nouveautés d'AGPM4.0SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807393"
---
# <span data-ttu-id="b1101-103">Nouveautés d'AGPM4.0SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-103">What's New in AGPM 4.0 SP1</span></span>


<span data-ttu-id="b1101-104">Ce contenu «nouveautés» décrit les améliorations et les configurations prises en charge pour la gestion de la stratégie de groupe avancée Microsoft (AGPM) 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="b1101-104">This “What’s New” content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="b1101-105">S’il existe une différence entre ce contenu et toute autre documentation AGPM, ce contenu doit être considéré comme faisant autorité et doit remplacer le contenu inclus dans le produit.</span><span class="sxs-lookup"><span data-stu-id="b1101-105">If there is a difference between this content and other AGPM documentation, this content should be considered authoritative and should supersede the content included with this product.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="b1101-106">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="b1101-106">What’s new</span></span>


<span data-ttu-id="b1101-107">AGPM 4,0 SP1 prend en charge les améliorations suivantes:</span><span class="sxs-lookup"><span data-stu-id="b1101-107">AGPM 4.0 SP1 supports the following enhancements:</span></span>

### <span data-ttu-id="b1101-108">Extensions côté client nouvelles et modifiées</span><span class="sxs-lookup"><span data-stu-id="b1101-108">New and changed client-side extensions</span></span>

<span data-ttu-id="b1101-109">Les extensions côté client de la stratégie de groupe ont été ajoutées ou modifiées pour AGPM afin de prendre en charge les nouvelles stratégies de groupe dans Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b1101-109">Group Policy client-side extensions (CSEs) have been added or changed for AGPM to support new Group Policies in Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="b1101-110">Ces stratégies de groupe permettent aux administrateurs de stratégie de groupe de gérer et de suivre les paramètres de stratégie de groupe spécifiques de Windows 8 qui changent entre deux objets de stratégie de groupe ou modèles.</span><span class="sxs-lookup"><span data-stu-id="b1101-110">These group policies enable Group Policy administrators to manage and track Windows 8-specific Group Policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="b1101-111">Vous pouvez également créer des objets de stratégie de groupe personnalisés avec des paramètres spécifiques de Windows 8 et configurer et enregistrer les objets de stratégie de groupe en tant que modèle.</span><span class="sxs-lookup"><span data-stu-id="b1101-111">You can also create custom GPOs, with Windows 8-specific settings, and configure and save the GPOs as a template.</span></span> <span data-ttu-id="b1101-112">Pour afficher vos CSE, utilisez les paramètres et les rapports de différences disponibles dans le client AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="b1101-112">To view your CSEs, use the settings and difference reports that are available in the AGPM 4.0 SP1 client.</span></span>

<span data-ttu-id="b1101-113">Les extensions côté client nouvelles et modifiées sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="b1101-113">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="b1101-114">**Stratégie d’accès centralisé:** Permet aux administrateurs de stratégie de groupe de spécifier des stratégies d’accès centralisées sur des serveurs de stratégie de groupe, par exemple des serveurs de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b1101-114">**Central Access Policy:** Enables Group Policy administrators to specify Central Access Policies on Group Policy servers, for example, file servers.</span></span> <span data-ttu-id="b1101-115">La stratégie d’accès centralisé est une stratégie d’autorisation spécifiée par un élément d’objet de stratégie de groupe et appliquée aux cibles de stratégie pour faciliter l’accès centralisé et le contrôle des ressources.</span><span class="sxs-lookup"><span data-stu-id="b1101-115">Central Access Policy is an authorization policy that is specified by a GPO item and applied to policy targets to facilitate centralized access and control of resources.</span></span> <span data-ttu-id="b1101-116">Ces stratégies d’accès centralisé doivent être configurées sur un ordinateur client de stratégie de groupe à partir d’Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1101-116">These Central Access Policies must be configured on a Group Policy client computer from within Active Directory.</span></span> <span data-ttu-id="b1101-117">Une stratégie de groupe distribue les connaissances d’une stratégie d’accès centralisé applicable aux ordinateurs qui doivent l’appliquer.</span><span class="sxs-lookup"><span data-stu-id="b1101-117">A Group Policy distributes the knowledge of an applicable Central Access Policy to the computers that have to enforce it.</span></span>

-   <span data-ttu-id="b1101-118">**Modifications de la stratégie de résolution de nom:** Permet aux administrateurs de stratégie de groupe de configurer les paramètres pour la sécurité DNS et DirectAccess sur les ordinateurs clients DNS.</span><span class="sxs-lookup"><span data-stu-id="b1101-118">**Name Resolution Policy changes:** Enables Group Policy administrators to configure settings for DNS security and DirectAccess on DNS client computers.</span></span> <span data-ttu-id="b1101-119">De nouveaux onglets pour la configuration des paramètres du serveur DNS générique et des paramètres d’encodage ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="b1101-119">New tabs for configuring Generic DNS Server settings and Encoding settings have been added.</span></span>

-   <span data-ttu-id="b1101-120">**Modifications des préférences de stratégie de groupe:** Ajoute une prise en charge pour la configuration et la gestion des paramètres d’Internet Explorer 10 qui ont été ajoutés pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1101-120">**Group Policy Preference changes:** Adds support for the configuration and management of Internet Explorer 10 settings that were added for Windows 8.</span></span>

-   <span data-ttu-id="b1101-121">**Connexions d’application et de bureau distantes:** Permet aux administrateurs de stratégie de groupe de spécifier l’URL de connexion par défaut utilisée pour les connexions aux applications et au bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b1101-121">**Remote Application and Desktop Connections:** Lets Group Policy administrators specify the default connection URL that is used for Remote Application and Desktop Connections.</span></span>

-   <span data-ttu-id="b1101-122">**Options de démarrage de Windows to Go:** Permet aux administrateurs de stratégie de groupe de configurer le démarrage de l’ordinateur pour Windows sur Go si un appareil USB contenant un espace de travail Windows to Go est connecté.</span><span class="sxs-lookup"><span data-stu-id="b1101-122">**Windows To Go Startup Options:** Lets Group Policy administrators configure whether the computer will boot to Windows To Go if a USB device that contains a Windows To Go workspace is connected.</span></span>

-   <span data-ttu-id="b1101-123">**Options de mise en veille prolongée de Windows to Go:** Permet aux administrateurs de stratégie de groupe de configurer l’utilisation de l’état de veille de la mise en veille (S4) lors du démarrage de l’ordinateur à partir d’un espace de travail Windows to go.</span><span class="sxs-lookup"><span data-stu-id="b1101-123">**Windows To Go Hibernate Options:** Lets Group Policy administrators configure whether a computer can use the hibernation sleep state (S4) when the computer is started from a Windows To Go workspace.</span></span>

### <span data-ttu-id="b1101-124">Commentaires des clients et ROLLUP de HotFix</span><span class="sxs-lookup"><span data-stu-id="b1101-124">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="b1101-125">Le Service Pack d’AGPM 4,0 inclut un correctif cumulatif pour résoudre les problèmes détectés depuis la version d’AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="b1101-125">AGPM 4.0 SP1 includes a rollup of fixes to address issues found since the AGPM 4.0 release.</span></span> <span data-ttu-id="b1101-126">AGPM 4,0 SP1 contient les correctifs les plus récents pour la gestion de la stratégie de groupe Microsoft avancée 4,0 Hotfix 1.</span><span class="sxs-lookup"><span data-stu-id="b1101-126">AGPM 4.0 SP1 contains the latest fixes up to and including Microsoft Advanced Group Policy Management 4.0 Hotfix 1.</span></span>

### <span data-ttu-id="b1101-127">Les rapports et les différences indiquent les nouvelles extensions de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b1101-127">Settings and difference reports show new Group Policy extensions</span></span>

<span data-ttu-id="b1101-128">Les nouvelles extensions de stratégie de groupe ont été ajoutées aux rapports paramètres et différences.</span><span class="sxs-lookup"><span data-stu-id="b1101-128">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="b1101-129">Modifications et prise en charge du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="b1101-129">Installer changes and support</span></span>

<span data-ttu-id="b1101-130">Les modifications et la prise en charge du programme d’installation d’AGPM 4,0 SP1 sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="b1101-130">The changes and support for the AGPM 4.0 SP1 installer are:</span></span>

-   <span data-ttu-id="b1101-131">Si vous installez AGPM 4,0 SP1 sur Windows 8 ou Windows Server 2012, le programme d’installation d’AGPM vérifie que les logiciels prérequis requis (console de gestion des stratégies de groupe et .NET 3,5 Framework) sont installés.</span><span class="sxs-lookup"><span data-stu-id="b1101-131">If you install AGPM 4.0 SP1 on Windows 8 or Windows Server 2012, the AGPM installer verifies that the required prerequisite software (Group Policy Management Console and the .NET 3.5 Framework) is installed.</span></span> <span data-ttu-id="b1101-132">Si ces éléments requis ne sont pas installés, l’installation d’AGPM 4,0 SP1 est bloquée.</span><span class="sxs-lookup"><span data-stu-id="b1101-132">If these prerequisites are not installed, the AGPM 4.0 SP1 installation is blocked.</span></span>

-   <span data-ttu-id="b1101-133">Lors de l’installation d’AGPM 4,0 SP1, l’activation WCF, l’activation non HTTP et le service d’activation de processus Windows sont activés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b1101-133">When you install AGPM 4.0 SP1, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="b1101-134">Sur les systèmes d’exploitation Windows Vista, Windows 7 et Windows 8, téléchargez la version appropriée du kit de tâches d’administration du système distant pour votre système d’exploitation avant d’installer AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="b1101-134">On Windows Vista, Windows 7, and Windows 8 client operating systems, download the appropriate version of the Remote System Administration Toolkit for your operating system before you install AGPM 4.0 SP1.</span></span>

-   <span data-ttu-id="b1101-135">La compatibilité descendante avec les anciens systèmes d’exploitation pris en charge est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b1101-135">Backward compatibility with older supported operating systems is supported.</span></span>

### <span data-ttu-id="b1101-136">Possibilité d’effectuer la mise à niveau ou la mise à jour vers AGPM 4,0 SP1 sans entrer de nouveau les paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="b1101-136">Ability to upgrade or update to AGPM 4.0 SP1 without re-entering configuration parameters</span></span>

<span data-ttu-id="b1101-137">Vous pouvez mettre à niveau le client ou le serveur AGPM vers AGPM 4,0 SP1 uniquement d’AGPM 4,0 sans être invité à entrer de nouveau les paramètres de configuration (appelées «mise à niveau intelligente»), comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b1101-137">You can upgrade the AGPM client or server to AGPM 4.0 SP1 only from AGPM 4.0 without being prompted to re-enter configuration parameters (called “Smart Upgrade”), as shown in the following table.</span></span> <span data-ttu-id="b1101-138">Si vous effectuez une mise à niveau vers AGPM 4,0 SP1 à partir d’autres versions d’AGPM, comme indiqué dans le tableau ci-dessous, vous devez utiliser la «mise à niveau classique» qui nécessite d’entrer de nouveau les paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="b1101-138">If you are upgrading to AGPM 4.0 SP1 from other versions of AGPM, as shown in the table, you must use the “Classic Upgrade,” which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="b1101-139">Dans la mesure où chaque version d’AGPM est associée à un système d’exploitation spécifique, reportez-vous à la rubrique [choix de la version d’AGPM à installer](https://go.microsoft.com/fwlink/?LinkId=254350)et veillez à mettre à niveau votre système d’exploitation, le cas échéant, avant d’effectuer une mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="b1101-139">Since each version of AGPM is associated with a particular operating system, refer to [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350), and be sure to upgrade your operating system as appropriate before performing an upgrade.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b1101-140">Version d’AGPM à partir de laquelle vous pouvez effectuer la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="b1101-140">AGPM Version From Which You Can Upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b1101-141">2,5</span><span class="sxs-lookup"><span data-stu-id="b1101-141">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b1101-142">3,0</span><span class="sxs-lookup"><span data-stu-id="b1101-142">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b1101-143">4,0</span><span class="sxs-lookup"><span data-stu-id="b1101-143">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b1101-144">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-144">4.0 SP1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1101-145">2,5</span><span class="sxs-lookup"><span data-stu-id="b1101-145">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-146">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b1101-146">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-147">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="b1101-147">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-148">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="b1101-148">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-149">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="b1101-149">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1101-150">3,0</span><span class="sxs-lookup"><span data-stu-id="b1101-150">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-151">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b1101-151">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-152">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b1101-152">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-153">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="b1101-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-154">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="b1101-154">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1101-155">4,0</span><span class="sxs-lookup"><span data-stu-id="b1101-155">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-156">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b1101-156">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-157">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b1101-157">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-158">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b1101-158">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-159">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="b1101-159">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b1101-160">Configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="b1101-160">Supported configurations</span></span>


<span data-ttu-id="b1101-161">AGPM prend en charge les configurations du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b1101-161">AGPM supports the configurations in the following table.</span></span> <span data-ttu-id="b1101-162">Bien qu’AGPM prenne en charge des configurations mixtes, il est fortement recommandé d’exécuter le client et le serveur AGPM sur la même famille de systèmes d’exploitation (par exemple, Windows 8 et Windows Server 2012, Windows 7 avec Windows Server 2008 R2, etc.).</span><span class="sxs-lookup"><span data-stu-id="b1101-162">Although AGPM supports mixed configurations, it is strongly recommended that you run the AGPM client and server on the same operating system family, for example, Windows 8 with Windows Server 2012, Windows 7 with Windows Server 2008 R2, and so on.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b1101-163">Configurations prises en charge pour le serveur AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-163">Supported Configurations for AGPM 4.0 SP1 Server</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b1101-164">Configurations prises en charge pour le client AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-164">Supported Configurations for AGPM 4.0 SP1 Client</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b1101-165">Prise en charge d’AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-165">AGPM 4.0 SP1 Support</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1101-166">Windows 8 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1101-166">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-167">Windows 8 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1101-167">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-168">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1101-168">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1101-169">Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="b1101-169">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-170">Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="b1101-170">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-171">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="b1101-171">Supported, but cannot edit policy settings or preference items that exist only in Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1101-172">Windows Server 2008 R2 ou Windows 7, Windows 8 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1101-172">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-173">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-173">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-174">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server 2008 R2 ou Windows 7 ou Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1101-174">Supported, but cannot edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1101-175">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-175">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-176">Windows Server 2008 R2 ou Windows 7, Windows 8 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1101-176">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-177">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1101-177">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1101-178">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-178">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-179">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-179">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1101-180">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server 2008 R2 ou Windows 7 ou Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1101-180">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b1101-181">Conditions préalables à l’installation d’AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-181">Prerequisites for installing AGPM 4.0 SP1</span></span>


<span data-ttu-id="b1101-182">Le tableau suivant décrit le comportement de Windows 8 d’AGPM 4,0 SP1 et des programmes d’installation du serveur lorsque .NET 3,5 ou la console de gestion des stratégies de groupe dans les outils d’administration de serveur distant.</span><span class="sxs-lookup"><span data-stu-id="b1101-182">The following table describes the behavior on Windows 8 of AGPM 4.0 SP1 client and server installers when .NET 3.5 or the Group Policy Management Console in the Remote Server Administration Tools (RSAT) is missing.</span></span>

**<span data-ttu-id="b1101-183">Client AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-183">AGPM Client 4.0 SP1</span></span>**

**<span data-ttu-id="b1101-184">Serveur AGPM Server 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-184">AGPM Server 4.0 SP1</span></span>**

**<span data-ttu-id="b1101-185">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="b1101-185">Operating System</span></span>**

**<span data-ttu-id="b1101-186">.NET</span><span class="sxs-lookup"><span data-stu-id="b1101-186">.NET</span></span>**

**<span data-ttu-id="b1101-187">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="b1101-187">RSAT</span></span>**

**<span data-ttu-id="b1101-188">.NET</span><span class="sxs-lookup"><span data-stu-id="b1101-188">.NET</span></span>**

**<span data-ttu-id="b1101-189">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="b1101-189">RSAT</span></span>**

**<span data-ttu-id="b1101-190">Windows8</span><span class="sxs-lookup"><span data-stu-id="b1101-190">Windows 8</span></span>**

<span data-ttu-id="b1101-191">Si .NET 3,5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="b1101-191">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="b1101-192">Si la console de gestion des stratégies de messagerie n’est pas activée ou installée sur le système, le programme d’installation bloque celle-ci.</span><span class="sxs-lookup"><span data-stu-id="b1101-192">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

<span data-ttu-id="b1101-193">Si .NET 3,5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="b1101-193">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="b1101-194">Si la console de gestion des stratégies de messagerie n’est pas activée ou installée sur le système, le programme d’installation bloque celle-ci.</span><span class="sxs-lookup"><span data-stu-id="b1101-194">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

**<span data-ttu-id="b1101-195">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="b1101-195">Windows Server 2012</span></span>**

<span data-ttu-id="b1101-196">Si .NET 3,5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="b1101-196">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="b1101-197">Si la console de gestion des stratégies de messagerie n’est pas activée, le programme d’installation l’autorise lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="b1101-197">If GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="b1101-198">Si .NET 3,5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="b1101-198">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="b1101-199">Si la console de gestion des stratégies de messagerie n’est pas activée, le programme d’installation l’autorise lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="b1101-199">If GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="b1101-200">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1101-200">Related topics</span></span>


[<span data-ttu-id="b1101-201">Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="b1101-201">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="b1101-202">Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP1</span><span class="sxs-lookup"><span data-stu-id="b1101-202">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 






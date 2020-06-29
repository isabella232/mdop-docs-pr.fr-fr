---
title: Nouveautés d'AGPM4.0SP2
description: Nouveautés d'AGPM4.0SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807390"
---
# <span data-ttu-id="05c2a-103">Nouveautés d'AGPM4.0SP2</span><span class="sxs-lookup"><span data-stu-id="05c2a-103">What's New in AGPM 4.0 SP2</span></span>


<span data-ttu-id="05c2a-104">Ce contenu décrit les améliorations et les configurations prises en charge pour Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="05c2a-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="05c2a-105">S’il existe une différence entre ce contenu et une autre documentation AGPM, considérez ce contenu faisant autorité et supposez qu’il remplace l’autre documentation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="05c2a-106">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="05c2a-106">What’s new</span></span>


<span data-ttu-id="05c2a-107">AGPM 4.0 SP2 prend en charge les fonctionnalités et fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="05c2a-107">AGPM4.0 SP2 supports the following features and functionality.</span></span>

### <span data-ttu-id="05c2a-108">Prise en charge de Windows 8.1 et Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="05c2a-108">Support for Windows8.1 and Windows Server2012 R2</span></span>

<span data-ttu-id="05c2a-109">Le SP2 pour AGPM 4.0 ajoute une prise en charge pour les systèmes d’exploitation Windows 8.1 et Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="05c2a-109">AGPM4.0 SP2 adds support for the Windows8.1 and Windows Server2012 R2 operating systems.</span></span>

### <span data-ttu-id="05c2a-110">Extensions côté client nouvelles et modifiées</span><span class="sxs-lookup"><span data-stu-id="05c2a-110">New and changed client-side extensions</span></span>

<span data-ttu-id="05c2a-111">Les extensions côté client de la stratégie de groupe ont été ajoutées ou modifiées pour que AGPM prenne en charge les nouveaux paramètres de stratégie dans Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="05c2a-111">Group Policy client-side extensions have been added or changed for AGPM to support new policy settings in Windows8.1.</span></span> <span data-ttu-id="05c2a-112">Ces paramètres de stratégie permettent aux administrateurs de stratégie de groupe de gérer et de suivre les paramètres de stratégie spécifiques de Windows 8.1 qui changent entre deux objets de stratégie de groupe ou modèles.</span><span class="sxs-lookup"><span data-stu-id="05c2a-112">These policy settings enable Group Policy administrators to manage and track Windows8.1–specific policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="05c2a-113">Pour afficher vos extensions côté client, utilisez les paramètres et rapports de différences disponibles dans le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="05c2a-113">To view your client-side extensions, use the settings and difference reports that are available in the AGPM Client.</span></span>

<span data-ttu-id="05c2a-114">Les extensions côté client nouvelles et modifiées sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="05c2a-114">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="05c2a-115">**Spécifiez les paramètres des dossiers de tâches**.</span><span class="sxs-lookup"><span data-stu-id="05c2a-115">**Specify Work Folders settings**.</span></span> <span data-ttu-id="05c2a-116">Si vous activez ce paramètre de stratégie, l’administrateur informatique peut configurer la création automatique de dossiers de bureau.</span><span class="sxs-lookup"><span data-stu-id="05c2a-116">If you enable this policy setting, IT administrators can configure Work Folders to be created automatically.</span></span> <span data-ttu-id="05c2a-117">La fonctionnalité dossiers de travail permet aux utilisateurs finaux de synchroniser des fichiers à partir de leurs appareils de bureau Windows sur leurs autres appareils.</span><span class="sxs-lookup"><span data-stu-id="05c2a-117">The Work Folders feature enables end users to synchronize files from their Windows desktop devices to their other devices.</span></span> <span data-ttu-id="05c2a-118">Utilisez ce paramètre de stratégie pour créer une relation de synchronisation sur les appareils de l’utilisateur final et configurer l’identification du serveur de fichiers qui stocke les dossiers de tâches de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05c2a-118">Use this policy setting to create the synchronization relationship on an end user’s devices and to configure how to identify the file server that stores the user’s Work Folders.</span></span> <span data-ttu-id="05c2a-119">Si vous activez la case à cocher **synchronisation automatique** , le partenariat de synchronisation sera créé sans entrée utilisateur, et les données commenceront automatiquement à se synchroniser avec l’appareil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05c2a-119">If you select the **Auto provision synchronization** check box, the synchronization partnership will be created without user input, and data will automatically start synchronizing to the user’s device.</span></span> <span data-ttu-id="05c2a-120">Si vous n’activez pas la case à cocher **synchronisation automatique** , les utilisateurs doivent fournir des informations pour lancer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-120">If you do not select the **Auto provision synchronization** check box, users must provide input to start the synchronization.</span></span>

-   <span data-ttu-id="05c2a-121">**Forcez la configuration automatique pour tous les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="05c2a-121">**Force automatic setup for all users**.</span></span> <span data-ttu-id="05c2a-122">Si vous activez ce paramètre de stratégie, l’administrateur informatique peut déterminer s’il est possible de créer le partenariat dossiers de tâches automatiquement sur les appareils finaux sans entrée d’utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="05c2a-122">If you enable this policy setting, IT administrators can determine whether to create the Work Folders partnership automatically on end-user devices without input from end users.</span></span> <span data-ttu-id="05c2a-123">Si vous activez ce paramètre de stratégie, la synchronisation est configurée en fonction de la manière dont vous configurez le paramètre spécifier une stratégie de paramètre **dossiers de tâches** .</span><span class="sxs-lookup"><span data-stu-id="05c2a-123">If you enable this policy setting, the synchronization will be set up according to how you configure the **Specify Work Folders settings** policy setting.</span></span> <span data-ttu-id="05c2a-124">Si vous définissez le **paramètre forcer la configuration automatique pour tous les utilisateurs** sur **désactivé** ou **non configuré**, le partenariat dossiers de tâches sera configuré en fonction de la manière dont vous définissez l’option de **mise en service automatique** dans le paramètre spécifier une stratégie de **dossiers de tâches** .</span><span class="sxs-lookup"><span data-stu-id="05c2a-124">If you set the **Force automatic setup for all users** policy setting to **Disabled** or **Not configured**, the Work Folders partnership will be configured according to how you set the **Automatic Provisioning** option in the **Specify Work Folders settings** policy setting.</span></span>

<span data-ttu-id="05c2a-125">Pour plus d’informations sur la fonction dossiers de tâches, voir [vue d’ensemble des dossiers de tâches](https://go.microsoft.com/fwlink/?LinkId=330444).</span><span class="sxs-lookup"><span data-stu-id="05c2a-125">For more information about the Work Folders feature, see [Work Folders Overview](https://go.microsoft.com/fwlink/?LinkId=330444).</span></span>

### <span data-ttu-id="05c2a-126">Commentaires des clients et ROLLUP de HotFix</span><span class="sxs-lookup"><span data-stu-id="05c2a-126">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="05c2a-127">Le SP2 pour AGPM 4.0 inclut un correctif cumulatif des correctifs pour résoudre les problèmes rencontrés depuis la version d’AGPM 4.0 Service Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="05c2a-127">AGPM4.0 SP2 includes a rollup of hotfixes to address issues found since the AGPM4.0 Service Pack1 (SP1) release.</span></span> <span data-ttu-id="05c2a-128">Le SP2 pour AGPM 4.0 contient les derniers correctifs pour le Service Pack d’administration de la stratégie de groupe Microsoft Advanced Hotfix1.</span><span class="sxs-lookup"><span data-stu-id="05c2a-128">AGPM4.0 SP2 contains the latest fixes up to and including Microsoft Advanced Group Policy Management4.0 SP1 Hotfix1.</span></span> <span data-ttu-id="05c2a-129">Pour plus d’informations, voir l’article de la base de connaissances [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).</span><span class="sxs-lookup"><span data-stu-id="05c2a-129">For more information, see Knowledge Base article [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).</span></span>

### <span data-ttu-id="05c2a-130">Nouvelles extensions de stratégie de groupe dans les rapports et les différences</span><span class="sxs-lookup"><span data-stu-id="05c2a-130">New Group Policy extensions in settings and difference reports</span></span>

<span data-ttu-id="05c2a-131">Les nouvelles extensions de stratégie de groupe ont été ajoutées aux rapports paramètres et différences.</span><span class="sxs-lookup"><span data-stu-id="05c2a-131">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="05c2a-132">Modifications et prise en charge du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="05c2a-132">Installer changes and support</span></span>

<span data-ttu-id="05c2a-133">Les modifications et la prise en charge du programme d’installation d’AGPM 4.0 SP2 sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="05c2a-133">The changes and support for the AGPM4.0 SP2 installer are:</span></span>

-   <span data-ttu-id="05c2a-134">Si vous installez AGPM 4.0 SP2 sur le système d’exploitation Windows 8 ou Windows Server 2012 ou les systèmes d’exploitation plus récents, le programme d’installation d’AGPM vérifie que les logiciels requis préalablement requis (console de gestion des stratégies de groupe (GPMC) et Microsoft .NET Framework 3.5) sont installés.</span><span class="sxs-lookup"><span data-stu-id="05c2a-134">If you install AGPM4.0 SP2 on the Windows 8 or Windows Server 2012 operating system or later operating systems, the AGPM installer verifies that the required prerequisite software (the Group Policy Management Console (GPMC) and the Microsoft .NET Framework3.5) is installed.</span></span> <span data-ttu-id="05c2a-135">Si ce logiciel requis n’est pas installé, l’installation d’AGPM 4.0 SP2 est bloquée.</span><span class="sxs-lookup"><span data-stu-id="05c2a-135">If this prerequisite software is not installed, the AGPM4.0 SP2 installation is blocked.</span></span>

-   <span data-ttu-id="05c2a-136">Lorsque vous installez le serveur AGPM, l’activation WCF, l’activation non HTTP et le service d’activation de processus Windows sont activés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="05c2a-136">When you install the AGPM Server, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="05c2a-137">Sur le système d’exploitation du client Vista et les systèmes d’exploitation plus récents, téléchargez la version appropriée des outils d’administration du système distant pour votre système d’exploitation avant d’installer AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="05c2a-137">On the WindowsVista client operating system and later operating systems, download the appropriate version of the Remote System Administration Tools for your operating system before you install AGPM4.0 SP2.</span></span>

-   <span data-ttu-id="05c2a-138">Le SP2 pour AGPM 4.0 prend en charge la compatibilité descendante avec les anciens systèmes d’exploitation pris en charge.</span><span class="sxs-lookup"><span data-stu-id="05c2a-138">AGPM4.0 SP2 supports backward compatibility with older supported operating systems.</span></span>

### <span data-ttu-id="05c2a-139">Possibilité de procéder à la mise à niveau vers AGPM 4.0 SP2 sans avoir à entrer les paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="05c2a-139">Ability to upgrade to AGPM4.0 SP2 without reentering configuration parameters</span></span>

<span data-ttu-id="05c2a-140">Vous pouvez mettre à niveau le client AGPM ou le serveur AGPM vers AGPM 4.0 SP2 sans être invité à entrer de nouveau les paramètres de configuration (appelé mise à niveau intelligente) uniquement à partir d’AGPM 4.0, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="05c2a-140">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP2 without being prompted to reenter configuration parameters (called the Smart Upgrade) only from AGPM4.0 onward, as shown in the following table.</span></span> <span data-ttu-id="05c2a-141">Si vous effectuez une mise à niveau vers AGPM 4.0 SP2 à partir d’autres versions d’AGPM, comme indiqué dans le tableau ci-dessous, vous devez utiliser la mise à niveau classique, qui nécessite d’entrer de nouveau les paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="05c2a-141">If you are upgrading to AGPM4.0 SP2 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to reenter the configuration parameters.</span></span> <span data-ttu-id="05c2a-142">Étant donné que chaque version d’AGPM est associée à un système d’exploitation spécifique, voir [choisir la version d’AGPM à installer](https://go.microsoft.com/fwlink/?LinkId=254350) et vérifier que vous effectuez une mise à niveau de votre système d’exploitation le cas échéant avant de procéder à la mise à niveau d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="05c2a-142">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="05c2a-143">Mises à jour d’AGPM 4,0 SP2 prises en charge</span><span class="sxs-lookup"><span data-stu-id="05c2a-143">AGPM 4.0 SP2 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="05c2a-144">Version d’AGPM à partir de laquelle vous pouvez effectuer la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="05c2a-144">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="05c2a-145">2,5</span><span class="sxs-lookup"><span data-stu-id="05c2a-145">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="05c2a-146">3,0</span><span class="sxs-lookup"><span data-stu-id="05c2a-146">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="05c2a-147">4,0</span><span class="sxs-lookup"><span data-stu-id="05c2a-147">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="05c2a-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="05c2a-148">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="05c2a-149">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="05c2a-149">4.0 SP2</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05c2a-150">2,5</span><span class="sxs-lookup"><span data-stu-id="05c2a-150">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-151">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-152">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="05c2a-152">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-153">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="05c2a-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-154">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="05c2a-154">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-155">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="05c2a-155">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05c2a-156">3,0</span><span class="sxs-lookup"><span data-stu-id="05c2a-156">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-157">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-158">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-159">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="05c2a-159">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-160">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="05c2a-160">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-161">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="05c2a-161">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05c2a-162">4,0</span><span class="sxs-lookup"><span data-stu-id="05c2a-162">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-163">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-163">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-164">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-164">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-165">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-165">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-166">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="05c2a-166">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-167">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="05c2a-167">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05c2a-168">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="05c2a-168">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-169">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-169">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-170">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-170">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-171">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-171">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-172">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05c2a-172">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-173">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="05c2a-173">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="05c2a-174">Configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="05c2a-174">Supported configurations</span></span>


<span data-ttu-id="05c2a-175">Le SP2 pour AGPM 4.0 prend en charge les configurations du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="05c2a-175">AGPM4.0 SP2 supports the configurations in the following table.</span></span> <span data-ttu-id="05c2a-176">Bien qu’AGPM prenne en charge des configurations mixtes, nous vous recommandons vivement d’exécuter le client AGPM et le serveur AGPM sur la même ligne de système d’exploitation (par exemple, Windows 8.1 avec Windows Server2012 R2, Windows 8 avec Windows Server 2012, etc.).</span><span class="sxs-lookup"><span data-stu-id="05c2a-176">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows8.1 with Windows Server2012 R2, Windows 8 with Windows Server 2012, and so on.</span></span>

**<span data-ttu-id="05c2a-177">Systèmes d’exploitation et systèmes d’exploitation pris en charge par AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="05c2a-177">AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="05c2a-178">Configurations prises en charge pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="05c2a-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="05c2a-179">Configurations prises en charge pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="05c2a-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="05c2a-180">Prise en charge d’AGPM</span><span class="sxs-lookup"><span data-stu-id="05c2a-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05c2a-181">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="05c2a-181">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-182">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="05c2a-182">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-183">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="05c2a-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05c2a-184">Windows Server2012 R2, Windows Server 2012, Windows 8.1 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="05c2a-184">Windows Server2012 R2, Windows Server 2012, Windows8.1, or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-185">Windows Server 2012 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="05c2a-185">Windows Server 2012 or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-186">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="05c2a-186">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05c2a-187">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="05c2a-187">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-188">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="05c2a-188">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-189">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="05c2a-189">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1 or Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05c2a-190">Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="05c2a-190">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-191">Windows Server 2008 ou Vista avec Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="05c2a-191">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-192">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="05c2a-192">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05c2a-193">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="05c2a-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-194">Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="05c2a-194">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-195">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="05c2a-195">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05c2a-196">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="05c2a-196">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-197">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="05c2a-197">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05c2a-198">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="05c2a-198">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="05c2a-199">Conditions préalables à l’installation d’AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="05c2a-199">Prerequisites for installing AGPM4.0 SP2</span></span>


<span data-ttu-id="05c2a-200">Le tableau suivant décrit le comportement d’AGPM 4.0 SP2 et des programmes d’installation du serveur sur Windows 8.1 lorsque .NET Framework 3.5 ou la console GPMC dans les outils d’administration de serveur distant est manquant.</span><span class="sxs-lookup"><span data-stu-id="05c2a-200">The following table describes the behavior of AGPM4.0 SP2 Client and Server installers on Windows8.1 when the .NET Framework3.5 or the GPMC in the Remote Server Administration Tools is missing.</span></span>

**<span data-ttu-id="05c2a-201">Client AGPM</span><span class="sxs-lookup"><span data-stu-id="05c2a-201">AGPM Client</span></span>**

**<span data-ttu-id="05c2a-202">Serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="05c2a-202">AGPM Server</span></span>**

**<span data-ttu-id="05c2a-203">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="05c2a-203">Operating system</span></span>**

**<span data-ttu-id="05c2a-204">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="05c2a-204">.NET Framework</span></span>**

**<span data-ttu-id="05c2a-205">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="05c2a-205">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="05c2a-206">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="05c2a-206">.NET Framework</span></span>**

**<span data-ttu-id="05c2a-207">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="05c2a-207">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="05c2a-208">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="05c2a-208">Windows8.1</span></span>**

<span data-ttu-id="05c2a-209">Si .NET Framework 3.5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-209">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="05c2a-210">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-210">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="05c2a-211">Si .NET Framework 3.5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-211">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="05c2a-212">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

**<span data-ttu-id="05c2a-213">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="05c2a-213">Windows Server2012 R2</span></span>**

<span data-ttu-id="05c2a-214">Si .NET Framework 3.5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-214">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="05c2a-215">Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-215">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="05c2a-216">Si .NET Framework 3.5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-216">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="05c2a-217">Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="05c2a-217">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="05c2a-218">Obtention de technologies MDOP</span><span class="sxs-lookup"><span data-stu-id="05c2a-218">How to Get MDOP Technologies</span></span>


<span data-ttu-id="05c2a-219">AGPM 4,0 SP2 fait partie du pack d’optimisation de bureau de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="05c2a-219">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="05c2a-220">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="05c2a-220">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="05c2a-221">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="05c2a-221">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="05c2a-222">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05c2a-222">Related topics</span></span>


[<span data-ttu-id="05c2a-223">Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="05c2a-223">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="05c2a-224">Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP2</span><span class="sxs-lookup"><span data-stu-id="05c2a-224">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[<span data-ttu-id="05c2a-225">Choix de la version d'AGPM à installer</span><span class="sxs-lookup"><span data-stu-id="05c2a-225">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 






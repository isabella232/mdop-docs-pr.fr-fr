---
title: Déployer les fonctionnalités UE-V2.x requises
description: Déployer les fonctionnalités UE-V2.x requises
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810692"
---
# <span data-ttu-id="278e8-103">Déployer les fonctionnalités UE-V2.x requises</span><span class="sxs-lookup"><span data-stu-id="278e8-103">Deploy Required Features for UE-V 2.x</span></span>


<span data-ttu-id="278e8-104">L’ensemble des déploiements de Microsoft User performance (UE-V) 2,0, 2,1 et 2,1 SP1 nécessitent ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="278e8-104">All Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 deployments require these features</span></span>

-   <span data-ttu-id="278e8-105">[Déploiement d’un emplacement de stockage des paramètres](#ssl) accessible aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="278e8-105">[Deploy a Settings Storage Location](#ssl) that is accessible to end users.</span></span>

    <span data-ttu-id="278e8-106">Il s’agit d’un partage réseau standard qui stocke et récupère les paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="278e8-106">This is a standard network share that stores and retrieves user settings.</span></span>

-   [<span data-ttu-id="278e8-107">Choisir la méthode de configuration pour UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-107">Choose the Configuration Method for UE-V</span></span>](#config)

    <span data-ttu-id="278e8-108">UE-V peut être déployé et configuré à l’aide d’outils de gestion courants tels que la stratégie de groupe, le gestionnaire de configuration ou l’infrastructure de gestion Windows et PowerShell.</span><span class="sxs-lookup"><span data-stu-id="278e8-108">UE-V can be deployed and configured using common management tools including group policy, Configuration Manager, or Windows Management Infrastructure and Powershell.</span></span>

-   <span data-ttu-id="278e8-109">[Déployez un agent UE-V](#agent) pour qu’il soit installé sur tous les ordinateurs qui synchronisent les paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-109">[Deploy a UE-V Agent](#agent) to be installed on every computer that synchronizes settings.</span></span>

    <span data-ttu-id="278e8-110">Ce contrôle surveille les applications inscrites et le système d’exploitation en cas de modification des paramètres et synchronise ces paramètres entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="278e8-110">This monitors registered applications and the operating system for any settings changes and synchronizes those settings between computers.</span></span>

<span data-ttu-id="278e8-111">Les rubriques de cette section expliquent comment déployer ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="278e8-111">The topics in this section describe how to deploy these features.</span></span>

## <a href="" id="ssl"></a><span data-ttu-id="278e8-112">Déploiement d’un emplacement de stockage des paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-112">Deploy a UE-V Settings Storage Location</span></span>


<span data-ttu-id="278e8-113">UE-V nécessite un emplacement pour le stockage des paramètres utilisateur dans les fichiers du package de paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-113">UE-V requires a location in which to store user settings in settings package files.</span></span> <span data-ttu-id="278e8-114">Vous pouvez configurer cet emplacement de stockage des paramètres de l’une des manières suivantes:</span><span class="sxs-lookup"><span data-stu-id="278e8-114">You can configure this settings storage location in one of these ways:</span></span>

-   <span data-ttu-id="278e8-115">Créer votre propre emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="278e8-115">Create your own settings storage location</span></span>

-   <span data-ttu-id="278e8-116">Utiliser Active Directory existant pour l’emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="278e8-116">Use existing Active Directory for your settings storage location</span></span>

<span data-ttu-id="278e8-117">Si vous ne créez pas d’emplacement de stockage des paramètres, l’agent UE-V utilisera par défaut Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="278e8-117">If you don’t create a settings storage location, the UE-V Agent will use Active Directory (AD) by default.</span></span>

**<span data-ttu-id="278e8-118">Remarque</span><span class="sxs-lookup"><span data-stu-id="278e8-118">Note</span></span>**  
<span data-ttu-id="278e8-119">Dans le cadre des [performances et](https://technet.microsoft.com/library/dn458932.aspx#capacity) de la planification de la capacité et de réduire les problèmes liés à la latence du réseau, vous pouvez créer des emplacements de stockage des paramètres sur les mêmes réseaux locaux sur lesquels résident les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="278e8-119">As a matter of [performance and capacity planning](https://technet.microsoft.com/library/dn458932.aspx#capacity) and to reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="278e8-120">Nous vous recommandons d’utiliser 20 Mo d’espace disque par utilisateur pour l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-120">We recommend 20 MB of disk space per user for the settings storage location.</span></span>



### <span data-ttu-id="278e8-121">Créer un emplacement de stockage des paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-121">Create a UE-V Settings Storage Location</span></span>

<span data-ttu-id="278e8-122">Avant de définir l’emplacement de stockage des paramètres, vous devez créer un répertoire racine avec des autorisations en lecture/écriture pour les utilisateurs qui stockent des paramètres sur le partage.</span><span class="sxs-lookup"><span data-stu-id="278e8-122">Before you define the settings storage location, you must create a root directory with read/write permissions for users who store settings on the share.</span></span> <span data-ttu-id="278e8-123">L’agent UE-V crée des dossiers spécifiques à l’utilisateur sous cet annuaire racine.</span><span class="sxs-lookup"><span data-stu-id="278e8-123">The UE-V Agent creates user-specific folders under this root directory.</span></span>

<span data-ttu-id="278e8-124">L’emplacement de stockage des paramètres est défini en définissant l’option de configuration SettingsStoragePath, que vous pouvez configurer à l’aide de l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="278e8-124">The settings storage location is defined by setting the SettingsStoragePath configuration option, which you can configure by using one of these methods:</span></span>

-   <span data-ttu-id="278e8-125">Lorsque vous [déployez l’agent UE-V](#agent) par le biais d’un paramètre de ligne de commande ou d’un script de commandes</span><span class="sxs-lookup"><span data-stu-id="278e8-125">When you [Deploy the UE-V Agent](#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="278e8-126">Par le biais des paramètres de [stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="278e8-126">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="278e8-127">[Module System Center Configuration](https://technet.microsoft.com/library/dn458917.aspx) pour UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-127">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="278e8-128">Après l’installation de l’agent UE-V, à l’aide de [Windows PowerShell ou WMI (Windows Management Instrumentation)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="278e8-128">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>

<span data-ttu-id="278e8-129">Le chemin d’accès doit être dans un chemin UNC (Universal Naming Convention) du serveur et le partage.</span><span class="sxs-lookup"><span data-stu-id="278e8-129">The path must be in a universal naming convention (UNC) path of the server and share.</span></span> <span data-ttu-id="278e8-130">Par exemple, **\\\\Server\\Settingsshare\\**.</span><span class="sxs-lookup"><span data-stu-id="278e8-130">For example, **\\\\Server\\Settingsshare\\**.</span></span> <span data-ttu-id="278e8-131">Cette option de configuration prend en charge l’utilisation de variables pour activer des scénarios de synchronisation spécifiques.</span><span class="sxs-lookup"><span data-stu-id="278e8-131">This configuration option supports the use of variables to enable specific synchronization scenarios.</span></span> <span data-ttu-id="278e8-132">Par exemple, vous pouvez utiliser les `%username%\%computername%` variables pour conserver l’interface des paramètres utilisateur finaux dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="278e8-132">For example, you can use the `%username%\%computername%` variables to preserve the end user settings experience in these scenarios:</span></span>

-   <span data-ttu-id="278e8-133">Utilisateurs finaux qui utilisent plusieurs ordinateurs physiques dans votre entreprise</span><span class="sxs-lookup"><span data-stu-id="278e8-133">End users that use multiple physical computers in your enterprise</span></span>

-   <span data-ttu-id="278e8-134">Ordinateurs d’entreprise utilisés par plusieurs utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="278e8-134">Enterprise computers that are used by multiple end users</span></span>

<span data-ttu-id="278e8-135">L’agent UE-V crée de manière dynamique un chemin de stockage de paramètres spécifique à l’utilisateur, avec un dossier système caché nommé `SettingsPackages` en fonction du paramètre de configuration de **SettingsStoragePath**.</span><span class="sxs-lookup"><span data-stu-id="278e8-135">The UE-V Agent dynamically creates a user-specific settings storage path, with a hidden system folder named `SettingsPackages`, based on the configuration setting of **SettingsStoragePath**.</span></span> <span data-ttu-id="278e8-136">L’agent lit et écrit les paramètres dans cet emplacement, comme défini par les modèles d’emplacement des paramètres UE-V enregistrés.</span><span class="sxs-lookup"><span data-stu-id="278e8-136">The agent reads and writes settings to this location as defined by the registered UE-V settings location templates.</span></span>

<span data-ttu-id="278e8-137">**Les paramètres d’UE-V sont déterminés par une règle de dernier enregistrement WINS:** Si l’emplacement de stockage des paramètres est le même pour les utilisateurs disposant de plusieurs ordinateurs gérés, un agent UE-V lit et écrit à l’emplacement des paramètres indépendamment des agents qui s’exécutent sur d’autres ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="278e8-137">**UE-V settings are determined by a "Last write wins" rule:** If the settings storage location is the same for user with multiple managed computers, one UE-V Agent reads and writes to the settings location independently of agents running on other computers.</span></span> <span data-ttu-id="278e8-138">Les derniers paramètres et valeurs écrits sont ceux appliqués lorsque l’agent suivant lit à partir de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-138">The last written settings and values are the ones applied when the next agent reads from the settings storage location.</span></span>

<span data-ttu-id="278e8-139">**Déploiement de l’emplacement de stockage des paramètres:** Suivez ces étapes pour définir l’emplacement de stockage des paramètres plutôt que d’utiliser votre service Active Directory existant.</span><span class="sxs-lookup"><span data-stu-id="278e8-139">**Deploy the settings storage location:** Follow these steps to define the settings storage location rather than using your existing Active Directory service.</span></span> <span data-ttu-id="278e8-140">Vous devez limiter l’accès au partage de stockage de paramètres aux utilisateurs qui en ont besoin, comme indiqué dans les tableaux ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="278e8-140">You should limit access to the settings storage share to those users that require it, as shown in the tables below.</span></span>

**<span data-ttu-id="278e8-141">Pour déployer le partage réseau UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-141">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="278e8-142">Créer un groupe de sécurité pour les utilisateurs d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-142">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="278e8-143">Créez un dossier sur l’ordinateur central dans lequel sont stockés les packages de paramètres UE-V, puis accordez aux utilisateurs d’UE-V l’accès à un dossier.</span><span class="sxs-lookup"><span data-stu-id="278e8-143">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="278e8-144">L’administrateur qui prend en charge UE-V doit disposer de l’autorisation d’accès à ce dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="278e8-144">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="278e8-145">Définissez les autorisations de blocs de messages serveur au niveau du partage (SMB) suivantes pour le dossier emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-145">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="278e8-146">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="278e8-146">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="278e8-147">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="278e8-147">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="278e8-148">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="278e8-148">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="278e8-149">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="278e8-149">No permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="278e8-150">Groupe de sécurité des utilisateurs d’UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-150">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="278e8-151">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="278e8-151">Full control</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="278e8-152">Définissez les autorisations de système de fichiers NTFS suivantes pour le dossier emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-152">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="278e8-153">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="278e8-153">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="278e8-154">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="278e8-154">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="278e8-155">Folder</span><span class="sxs-lookup"><span data-stu-id="278e8-155">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="278e8-156">Créateur/propriétaire</span><span class="sxs-lookup"><span data-stu-id="278e8-156">Creator/owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="278e8-157">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="278e8-157">Full control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="278e8-158">Sous-dossiers et fichiers uniquement</span><span class="sxs-lookup"><span data-stu-id="278e8-158">Subfolders and files only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="278e8-159">Groupe de sécurité des utilisateurs d’UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-159">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="278e8-160">Afficher le dossier/lire les données, créer des dossiers/ajouter des données</span><span class="sxs-lookup"><span data-stu-id="278e8-160">List folder/read data, create folders/append data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="278e8-161">Ce dossier uniquement</span><span class="sxs-lookup"><span data-stu-id="278e8-161">This folder only</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="278e8-162">Dans cette configuration, l’agent UE-V crée et sécurise un dossier Settingspackage lorsqu’il s’exécute dans le contexte de l’utilisateur, et accorde à chaque utilisateur l’autorisation de créer des dossiers pour le stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-162">With this configuration, the UE-V Agent creates and secures a Settingspackage folder while it runs in the context of the user, and grants each user permission to create folders for settings storage.</span></span> <span data-ttu-id="278e8-163">Les utilisateurs reçoivent le contrôle total de leurs dossiers Settingspackage alors que d’autres utilisateurs ne peuvent pas y accéder.</span><span class="sxs-lookup"><span data-stu-id="278e8-163">Users receive full control to their Settingspackage folder while other users cannot access it.</span></span>

**<span data-ttu-id="278e8-164">Remarque</span><span class="sxs-lookup"><span data-stu-id="278e8-164">Note</span></span>**  
<span data-ttu-id="278e8-165">Si vous créez le partage de stockage de paramètres sur un ordinateur exécutant un système d’exploitation Windows Server, configurez UE-V pour vérifier que le groupe Administrateurs local ou l’utilisateur actuel est le propriétaire du dossier dans lequel les packages de paramètres sont stockés.</span><span class="sxs-lookup"><span data-stu-id="278e8-165">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="278e8-166">Pour activer cette sécurité supplémentaire, spécifiez ce paramètre dans l’éditeur du registre de Windows Server:</span><span class="sxs-lookup"><span data-stu-id="278e8-166">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="278e8-167">Ajoutez une clé de Registre **reg \ _DWORD** nommée **«RepositoryOwnerCheckEnabled»** dans **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="278e8-167">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="278e8-168">Définissez la valeur de la clé de Registre sur *1*.</span><span class="sxs-lookup"><span data-stu-id="278e8-168">Set the registry key value to *1*.</span></span>



### <span data-ttu-id="278e8-169">Utiliser Active Directory avec UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="278e8-169">Use Active Directory with UE-V 2.x</span></span>

<span data-ttu-id="278e8-170">Par défaut, l’agent UE-V utilise Active Directory (AD) si un emplacement de stockage des paramètres n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="278e8-170">The UE-V Agent uses Active Directory (AD) by default if a settings storage location is not otherwise defined.</span></span> <span data-ttu-id="278e8-171">Dans ces cas, l’agent UE-V crée dynamiquement le dossier de stockage des paramètres sous la racine du répertoire de base AD de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="278e8-171">In these cases, the UE-V Agent dynamically creates the settings storage folder under the root of the AD home directory of each user.</span></span> <span data-ttu-id="278e8-172">Toutefois, si un paramètre d’annuaire personnalisé est configuré dans AD, ce répertoire est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="278e8-172">But, if a custom directory setting is configured in AD, then that directory is used instead.</span></span>

## <a href="" id="config"></a><span data-ttu-id="278e8-173">Choisissez la méthode de configuration pour UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="278e8-173">Choose the Configuration Method for UE-V 2.x</span></span>


<span data-ttu-id="278e8-174">Vous voulez déterminer la méthode de configuration que vous utiliserez pour gérer UE-V après le déploiement, car il s’agit de la méthode de configuration que vous utilisez pour déployer l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-174">You want to figure out which configuration method you'll use to manage UE-V after deployment since this will be the configuration method you use to deploy the UE-V Agent.</span></span> <span data-ttu-id="278e8-175">En règle générale, il s’agit de la méthode de configuration que vous utilisez déjà dans votre environnement, telle que Windows PowerShell ou Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="278e8-175">Typically, this is the configuration method that you already use in your environment, such as Windows PowerShell or Configuration Manager.</span></span>

<span data-ttu-id="278e8-176">Vous pouvez configurer UE-V avant, pendant ou après l’installation d’UE-V agent, en fonction de la méthode de configuration que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="278e8-176">You can configure UE-V before, during, or after UE-V Agent installation, depending on the configuration method that you use.</span></span>

-   <span data-ttu-id="278e8-177">[Stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx)**:** vous pouvez utiliser votre infrastructure de stratégie de groupe existante pour configurer UE-v avant ou après le déploiement de l’agent UE-v.</span><span class="sxs-lookup"><span data-stu-id="278e8-177">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You can use your existing Group Policy infrastructure to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="278e8-178">Le modèle ADMX de stratégie de groupe UE-V autorise la gestion centralisée des options de configuration de l’agent UE-V communes et comprend des paramètres pour configurer la synchronisation d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-178">The UE-V Group Policy ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span>

    <span data-ttu-id="278e8-179">**Installation des modèles ADMX de stratégie de groupe UE-V:** Les modèles ADMX de stratégie de groupe pour UE-V configurent les paramètres de synchronisation pour l’agent UE-V et permettent la gestion centralisée des paramètres de configuration de l’agent UE-V communs en utilisant une infrastructure de stratégie de groupe existante.</span><span class="sxs-lookup"><span data-stu-id="278e8-179">**Installing the UE-V Group Policy ADMX Templates:** Group Policy ADMX templates for UE-V configure the synchronization settings for the UE-V Agent and enable the central management of common UE-V Agent configuration settings by using an existing Group Policy infrastructure.</span></span>

    <span data-ttu-id="278e8-180">Les systèmes d’exploitation pris en charge pour le contrôleur de domaine qui déploient les objets de stratégie de groupe sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="278e8-180">Supported operating systems for the domain controller that deploys the Group Policy Objects include the following:</span></span>

    <span data-ttu-id="278e8-181">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="278e8-181">Windows Server 2008 R2</span></span>

    <span data-ttu-id="278e8-182">Windows Server 2012 et Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="278e8-182">Windows Server 2012 and Windows Server 2012 R2</span></span>

-   <span data-ttu-id="278e8-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** le Pack de configuration d’UE-V vous permet d’utiliser la fonctionnalité paramètres de conformité de System Center Configuration Manager 2012 SP1 ou une version ultérieure pour appliquer des configurations cohérentes sur les sites sur lesquels UE-V et Configuration Manager sont installés.</span><span class="sxs-lookup"><span data-stu-id="278e8-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** The UE-V Configuration Pack lets you use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

-   <span data-ttu-id="278e8-184">[Windows PowerShell et WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** vous pouvez utiliser des commandes par script pour Windows PowerShell et Windows Management Instrumentation (WMI) pour modifier les configurations après l’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-184">[Windows PowerShell and WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** You can use scripted commands for Windows PowerShell and Windows Management Instrumentation (WMI) to modify configurations after you install the UE-V Agent.</span></span>

    **<span data-ttu-id="278e8-185">Remarque</span><span class="sxs-lookup"><span data-stu-id="278e8-185">Note</span></span>**  
    <span data-ttu-id="278e8-186">La modification du Registre peut occasionner une perte de données ou l’ordinateur ne répond plus.</span><span class="sxs-lookup"><span data-stu-id="278e8-186">Registry modification can result in data loss, or the computer becomes unresponsive.</span></span> <span data-ttu-id="278e8-187">Nous vous recommandons d’utiliser d’autres méthodes de configuration.</span><span class="sxs-lookup"><span data-stu-id="278e8-187">We recommend that you use other configuration methods.</span></span>



-   <span data-ttu-id="278e8-188">**Installation de la ligne de commande ou du script par lot:** Les paramètres utilisés lors [du déploiement de l’agent UE-v](#agent) configurent de nombreux paramètres UE-v.</span><span class="sxs-lookup"><span data-stu-id="278e8-188">**Command-line or Batch Script Installation:** Parameters that are used when you [Deploy the UE-V Agent](#agent) configure many UE-V settings.</span></span> <span data-ttu-id="278e8-189">Les systèmes de distribution de logiciels électroniques tels que System Center 2012 Configuration Manager, utilisent ces paramètres pour configurer leurs clients lorsqu’ils déploient et installent le logiciel d’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-189">Electronic software distribution systems, such as System Center 2012 Configuration Manager, use these parameters to configure their clients when they deploy and install the UE-V Agent software.</span></span>

## <a href="" id="agent"></a><span data-ttu-id="278e8-190">Déploiement de l’agent UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="278e8-190">Deploy the UE-V 2.x Agent</span></span>


<span data-ttu-id="278e8-191">UE-V agent est le cœur d’un déploiement UE-V et doit s’exécuter sur chaque ordinateur qui utilise UE-V pour synchroniser les paramètres de l’application et de Windows.</span><span class="sxs-lookup"><span data-stu-id="278e8-191">The UE-V Agent is the core of a UE-V deployment and must run on each computer that uses UE-V to synchronize application and Windows settings.</span></span>

<span data-ttu-id="278e8-192">**Fichiers d’installation d’agent UE-V:** Dans le cas d’un fichier d’installation unique, AgentSetup.exe, l’agent UE-V est installé sur les systèmes d’exploitation 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="278e8-192">**UE-V Agent Installation Files:** A single installation file, AgentSetup.exe, installs the UE-V Agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="278e8-193">De plus, AgentSetupx86.msi ou AgentSetupx64.msi des fichiers Windows Installer propres à l’architecture sont fournis, et étant donné qu’ils sont plus petits, ils peuvent rationaliser les déploiements des agents.</span><span class="sxs-lookup"><span data-stu-id="278e8-193">In addition, AgentSetupx86.msi or AgentSetupx64.msi architecture-specific Windows Installer files are provided, and since they are smaller, they might streamline the agent deployments.</span></span> <span data-ttu-id="278e8-194">Les [paramètres de ligne de commande du programme](#params) d’installation de AgentSetup.exe sont également pris en charge pour l’installation de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="278e8-194">The [command-line parameters for the AgentSetup.exe installer](#params) are supported for the Windows Installer installation as well.</span></span>

**<span data-ttu-id="278e8-195">Important</span><span class="sxs-lookup"><span data-stu-id="278e8-195">Important</span></span>**  
<span data-ttu-id="278e8-196">Lors de l’installation ou de la désinstallation d’UE-V agent, vous pouvez utiliser le fichier AgentSetup.exe ou le AgentSetup &lt; arch &gt; . msi, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="278e8-196">During UE-V Agent installation or uninstallation, you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="278e8-197">Le même fichier doit être utilisé pour désinstaller l’agent UE-V qui a été utilisé pour installer l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-197">The same file must be used to uninstall the UE-V Agent that was used to install the UE-V Agent.</span></span>



### <span data-ttu-id="278e8-198">Pour déployer l’agent UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-198">To Deploy the UE-V Agent</span></span>

<span data-ttu-id="278e8-199">Pour déployer l’agent UE-V, vous pouvez utiliser les méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="278e8-199">You can use the following methods to deploy the UE-V Agent:</span></span>

-   <span data-ttu-id="278e8-200">Un système de solution de distribution de logiciels électronique (ESD), tel que Configuration Manager, capable d’installer un fichier Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="278e8-200">An electronic software distribution (ESD) solution system, such as Configuration Manager, that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="278e8-201">Script d’installation qui fait référence au fichier Windows Installer (. msi) qui est stocké sur un partage centralisé.</span><span class="sxs-lookup"><span data-stu-id="278e8-201">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="278e8-202">Un programme d’installation que vous exécutez manuellement sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="278e8-202">An installation program that you run manually on the computer.</span></span>

<span data-ttu-id="278e8-203">Utilisez la procédure suivante pour déployer l’agent UE-V à partir d’un partage réseau.</span><span class="sxs-lookup"><span data-stu-id="278e8-203">Use the following procedure to deploy the UE-V Agent from a network share.</span></span>

**<span data-ttu-id="278e8-204">Pour installer et configurer l’agent UE-V à partir d’un partage réseau</span><span class="sxs-lookup"><span data-stu-id="278e8-204">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="278e8-205">Étape du fichier d’installation de l’agent UE-V AgentSetup.exe sur un partage réseau auquel les utilisateurs disposent d’une autorisation de lecture.</span><span class="sxs-lookup"><span data-stu-id="278e8-205">Stage the UE-V Agent installation file AgentSetup.exe on a network share to which users have Read permission.</span></span>

2.  <span data-ttu-id="278e8-206">Déploiement d’un script sur des ordinateurs utilisateurs qui installent l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-206">Deploy a script to user computers that installs the UE-V Agent.</span></span> <span data-ttu-id="278e8-207">Le script doit spécifier l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-207">The script should specify the settings storage location.</span></span>

<span data-ttu-id="278e8-208">**Options de déploiement:** Veillez à utiliser le format de variable approprié lors de l’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-208">**Deployment options:** Be sure to use the correct variable format when you install the UE-V Agent.</span></span> <span data-ttu-id="278e8-209">Le tableau suivant contient des exemples d’options de déploiement pour l’utilisation des fichiers AgentSetup.exe ou Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="278e8-209">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="278e8-210">Type de déploiement</span><span class="sxs-lookup"><span data-stu-id="278e8-210">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="278e8-211">Description du déploiement</span><span class="sxs-lookup"><span data-stu-id="278e8-211">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="278e8-212">Exemple</span><span class="sxs-lookup"><span data-stu-id="278e8-212">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-213">Invite de commandes</span><span class="sxs-lookup"><span data-stu-id="278e8-213">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-214">Lorsque vous installez l’agent UE-V à une invite de commandes, utilisez le <em> format de variable% ^ nom_utilisateur% </em> .</span><span class="sxs-lookup"><span data-stu-id="278e8-214">When you install the UE-V Agent at a command prompt, use the <em>%^username%</em> variable format.</span></span> <span data-ttu-id="278e8-215">S’il est nécessaire de disposer de guillemets en raison d’espaces dans le chemin de stockage des paramètres, utilisez un fichier de script de commandes pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="278e8-215">If quotation marks are required because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="278e8-216">Script de commande</span><span class="sxs-lookup"><span data-stu-id="278e8-216">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-217">Lorsque vous installez l’agent UE-V à partir d’un fichier de script de commandes, utilisez le <em> format de variable%% nom_utilisateur%% </em> .</span><span class="sxs-lookup"><span data-stu-id="278e8-217">When you install the UE-V Agent from a batch script file, use the <em>%%username%%</em> variable format.</span></span> <span data-ttu-id="278e8-218">Si vous utilisez cette méthode d’installation, vous devez ignorer la variable contenant les caractères%%.</span><span class="sxs-lookup"><span data-stu-id="278e8-218">If you use this installation method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="278e8-219">Sans ce caractère, le script développe la <em> variable username </em> au moment de l’installation, plutôt qu’au moment de l’exécution, ce qui amène UE-V à utiliser un emplacement de stockage des paramètres unique pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="278e8-219">Without this character, the script expands the <em>username</em> variable at installation time, rather than at run time, which causes UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-220">WindowsPowerShell</span><span class="sxs-lookup"><span data-stu-id="278e8-220">Windows PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-221">Lorsque vous installez l’agent UE-V à partir d’une invite Windows PowerShell ou d’un script Windows PowerShell, utilisez le <em> format de variable% nom_utilisateur% </em> .</span><span class="sxs-lookup"><span data-stu-id="278e8-221">When you install the UE-V Agent from a Windows PowerShell prompt or a Windows PowerShell script, use the <em>%username%</em> variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="278e8-222">Distribution de logiciel électronique, comme le déploiement du déploiement logiciel de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="278e8-222">Electronic software distribution, such as deployment of Configuration Manager Software Deployment</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-223">Lorsque vous installez l’agent UE-V à l’aide de Configuration Manager, utilisez le <em> format de variable ^% nom_utilisateur ^% </em> .</span><span class="sxs-lookup"><span data-stu-id="278e8-223">When you install the UE-V Agent by using Configuration Manager, use the <em>^%username^%</em> variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="278e8-224">Remarque</span><span class="sxs-lookup"><span data-stu-id="278e8-224">Note</span></span>**  
<span data-ttu-id="278e8-225">L’installation de l’agent UE-V nécessite des droits d’administrateur, et l’ordinateur doit être redémarré pour que l’agent UE-V puisse s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="278e8-225">The installation of the UE-V Agent requires administrator rights, and the computer requires a restart before the UE-V Agent can run.</span></span>



### <a href="" id="params"></a><span data-ttu-id="278e8-226">Paramètres de ligne de commande pour le déploiement d’agent UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-226">Command-line parameters for UE-V Agent deployment</span></span>

<span data-ttu-id="278e8-227">Les paramètres de ligne de commande de l’agent UE-V sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="278e8-227">The command-line parameters of the UE-V Agent are as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="278e8-228">Paramètre de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="278e8-228">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="278e8-229">Définition</span><span class="sxs-lookup"><span data-stu-id="278e8-229">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="278e8-230">Remarques</span><span class="sxs-lookup"><span data-stu-id="278e8-230">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-231">/Help ou/h ou/?</span><span class="sxs-lookup"><span data-stu-id="278e8-231">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-232">Affiche la boîte de dialogue utilisation de AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="278e8-232">Displays the AgentSetup.exe usage dialog box.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="278e8-233">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="278e8-233">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-234">Indique le chemin UNC (Universal Naming Convention) qui définit l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-234">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="278e8-235">Important</span><span class="sxs-lookup"><span data-stu-id="278e8-235">Important</span></span></strong><br/><p><span data-ttu-id="278e8-236">Vous devez spécifier un SettingsStoragePath dans UE-V 2,1 et UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="278e8-236">You must specify a SettingsStoragePath in UE-V 2.1 and UE-V 2.1 SP1.</span></span> <span data-ttu-id="278e8-237">Vous pouvez définir la chaîne AdHomePath pour spécifier que le chemin d’accès de l’utilisateur&#39;de la page d’accueil Active Directory est utilisé.</span><span class="sxs-lookup"><span data-stu-id="278e8-237">You can set the AdHomePath string to specify that the user&#39;s Active Directory home path is used.</span></span> <span data-ttu-id="278e8-238">Exemple : <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span><span class="sxs-lookup"><span data-stu-id="278e8-238">For example, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span></span></p>
<p><span data-ttu-id="278e8-239">Dans UE-V 2,0, vous pouvez laisser SettingsStoragePath vide pour utiliser le chemin d’accès à la page d’accueil Active Directory.</span><span class="sxs-lookup"><span data-stu-id="278e8-239">In UE-V 2.0, you can leave SettingsStoragePath blank to use the Active Directory home path instead.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="278e8-240">les variables d’environnement% nom d’utilisateur% ou% nom_ordinateur% sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="278e8-240">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="278e8-241">L’écriture de script peut nécessiter des variables d’échappement.</span><span class="sxs-lookup"><span data-stu-id="278e8-241">Scripting can require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="278e8-242">Par défaut </strong> : &lt; aucune&gt;</span><span class="sxs-lookup"><span data-stu-id="278e8-242">Default</strong>: &lt;none&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-243">SettingsStoragePathReg</span><span class="sxs-lookup"><span data-stu-id="278e8-243">SettingsStoragePathReg</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-244">Obtient la valeur SettingsStoragePath du registre lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="278e8-244">Gets the SettingsStoragePath value from the registry during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-245">À l’invite de commandes, tapez l’exemple suivant pour forcer UE-V à utiliser le chemin d’accès à la page d’accueil Active Directory au lieu d’un chemin UNC spécifique.</span><span class="sxs-lookup"><span data-stu-id="278e8-245">At the command prompt, type the following example to force UE-V to use the Active Directory home path instead of a specific UNC.</span></span></p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="278e8-246">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="278e8-246">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-247">Indique le chemin UNC (Universal Naming Convention) qui définit l’emplacement dans lequel les nouveaux modèles d’emplacement des paramètres sont consultés.</span><span class="sxs-lookup"><span data-stu-id="278e8-247">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-248">Requis uniquement pour les modèles d’emplacement des paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="278e8-248">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-249">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="278e8-249">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-250">Indique si les modèles Microsoft par défaut doivent être inscrits lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="278e8-250">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-251">True | Fals</span><span class="sxs-lookup"><span data-stu-id="278e8-251">True | False</span></span></p>
<p><strong><span data-ttu-id="278e8-252">Valeur par défaut </strong> : vrai</span><span class="sxs-lookup"><span data-stu-id="278e8-252">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="278e8-253">PowerSchool</span><span class="sxs-lookup"><span data-stu-id="278e8-253">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-254">Spécifie la méthode de synchronisation à utiliser.</span><span class="sxs-lookup"><span data-stu-id="278e8-254">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-255">SyncProvider | Néant</span><span class="sxs-lookup"><span data-stu-id="278e8-255">SyncProvider | None</span></span></p>
<p><strong><span data-ttu-id="278e8-256">Par défaut </strong> : SyncProvider</span><span class="sxs-lookup"><span data-stu-id="278e8-256">Default</strong>: SyncProvider</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-257">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="278e8-257">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-258">Spécifie le nombre de millisecondes pendant lesquelles l’ordinateur attend avant qu’il récupère les paramètres utilisateur à partir de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-258">Specifies the number of milliseconds that the computer waits before time-out when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="278e8-259">Par défaut </strong> : 2000 millisecondes</span><span class="sxs-lookup"><span data-stu-id="278e8-259">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="278e8-260">(attendez 2 secondes)</span><span class="sxs-lookup"><span data-stu-id="278e8-260">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="278e8-261">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="278e8-261">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-262">Indique si la synchronisation UE-V est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="278e8-262">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-263">True | Fals</span><span class="sxs-lookup"><span data-stu-id="278e8-263">True | False</span></span></p>
<p><strong><span data-ttu-id="278e8-264">Valeur par défaut </strong> : vrai</span><span class="sxs-lookup"><span data-stu-id="278e8-264">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-265">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="278e8-265">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-266">Spécifie la taille de fichier du package de paramètres en octets lorsque l’agent UE-V signale que les fichiers dépassent le seuil.</span><span class="sxs-lookup"><span data-stu-id="278e8-266">Specifies a settings package file size in bytes when the UE-V Agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-267">&lt;papier&gt;</span><span class="sxs-lookup"><span data-stu-id="278e8-267">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="278e8-268">Par défaut </strong> : aucun (aucun seuil d’avertissement)</span><span class="sxs-lookup"><span data-stu-id="278e8-268">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="278e8-269">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="278e8-269">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-270">Spécifie le paramètre de participation au programme d’amélioration du produit.</span><span class="sxs-lookup"><span data-stu-id="278e8-270">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="278e8-271">S' <strong> il est défini sur true </strong> , les informations du programme d’installation sont téléchargées sur le site du programme d’amélioration du produit de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="278e8-271">If set to <strong>True</strong>, installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="278e8-272">Si <strong> elle est définie sur false </strong> , aucune information n’est téléchargée.</span><span class="sxs-lookup"><span data-stu-id="278e8-272">If set to <strong>False</strong>, no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-273">True | Fals</span><span class="sxs-lookup"><span data-stu-id="278e8-273">True | False</span></span></p>
<p><strong><span data-ttu-id="278e8-274">Valeur par défaut </strong> : false</span><span class="sxs-lookup"><span data-stu-id="278e8-274">Default</strong>: False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-275">Restart</span><span class="sxs-lookup"><span data-stu-id="278e8-275">NoRestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-276">Prend en charge le report du redémarrage de l’ordinateur après l’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-276">Supports deferral of the restart of the computer after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="278e8-277">INSTALLFOLDER</span><span class="sxs-lookup"><span data-stu-id="278e8-277">INSTALLFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-278">Permet de définir un autre dossier d’installation pour l’agent UE-V ou le générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-278">Enables a different installation folder to be set for the UE-V Agent or UE-V Generator.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-279">MUENABLED</span><span class="sxs-lookup"><span data-stu-id="278e8-279">MUENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-280">Permet d’accepter l’option d’inclusion du programme Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="278e8-280">Enables Setup to accept the option to be included in the Microsoft Update program.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="278e8-281">ACCEPTLICENSETERMS</span><span class="sxs-lookup"><span data-stu-id="278e8-281">ACCEPTLICENSETERMS</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-282">Autorise l’installation de UE-V de manière silencieuse.</span><span class="sxs-lookup"><span data-stu-id="278e8-282">Lets UE-V be installed silently.</span></span> <span data-ttu-id="278e8-283">Cette valeur doit être définie sur <strong> true </strong> pour installer UE-v en silence, sans que l’utilisateur accepte les termes du contrat de licence UE-v.</span><span class="sxs-lookup"><span data-stu-id="278e8-283">This must be set to <strong>True</strong> to install UE-V silently and bypass the requirement that the user accepts the UE-V license terms.</span></span> <span data-ttu-id="278e8-284">S’il est défini sur <strong> false </strong> ou vide, l’utilisateur reçoit un message d’erreur et UE-V n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="278e8-284">If set to <strong>False</strong> or left empty, the user receives an error message and UE-V is not installed.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="278e8-285">Important</span><span class="sxs-lookup"><span data-stu-id="278e8-285">Important</span></span></strong><br/><p><span data-ttu-id="278e8-286">Ce paramètre est requis pour installer UE-V en silence.</span><span class="sxs-lookup"><span data-stu-id="278e8-286">This parameter is required to install UE-V silently.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="278e8-287">Restart</span><span class="sxs-lookup"><span data-stu-id="278e8-287">NORESTART</span></span></p></td>
<td align="left"><p><span data-ttu-id="278e8-288">Empêche un redémarrage obligatoire après l’installation d’UE-V agent.</span><span class="sxs-lookup"><span data-stu-id="278e8-288">Prevents a mandatory restart after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="278e8-289">Mettre à jour l’agent UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-289">Update the UE-V Agent</span></span>

<span data-ttu-id="278e8-290">Les mises à jour du logiciel de l’agent UE-V sont fournies par le biais de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="278e8-290">Updates for the UE-V Agent software are provided through Microsoft Update.</span></span> <span data-ttu-id="278e8-291">Vous pouvez déployer des mises à jour de l’agent UE-V à l’aide de systèmes d’infrastructure de distribution de logiciels d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="278e8-291">You can deploy UE-V Agent updates by using Enterprise Software Distribution (ESD) infrastructure systems.</span></span>

<span data-ttu-id="278e8-292">Lors d’une mise à niveau d’agent UE-V, le groupe par défaut des modèles d’emplacement des paramètres pour les applications Microsoft courantes et les paramètres Windows peut être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="278e8-292">During a UE-V Agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings can be updated.</span></span>

### <span data-ttu-id="278e8-293">Mettre à niveau l’agent UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="278e8-293">Upgrade the UE-V 2.x Agent</span></span>

<span data-ttu-id="278e8-294">L’agent UE-V 2. x introduit de nombreuses nouvelles fonctionnalités et modifie la façon dont l’agent charge le contenu sur le partage de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-294">The UE-V 2.x Agent introduces many new features and modifies how and when the agent uploads content to the settings storage share.</span></span> <span data-ttu-id="278e8-295">Le processus de mise à niveau automatise ces modifications.</span><span class="sxs-lookup"><span data-stu-id="278e8-295">The upgrade process automates these changes.</span></span> <span data-ttu-id="278e8-296">Pour mettre à niveau l’agent UE-V, exécutez le package d’installation de l’agent UE-V (AgentSetup.exe, AgentSetupx86.msi ou AgentSetupx64.msi) sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="278e8-296">To upgrade the UE-V Agent, run the UE-V Agent install package (AgentSetup.exe, AgentSetupx86.msi, or AgentSetupx64.msi) on users’ computers.</span></span>

**<span data-ttu-id="278e8-297">Remarque</span><span class="sxs-lookup"><span data-stu-id="278e8-297">Note</span></span>**  
<span data-ttu-id="278e8-298">Lorsque vous effectuez une mise à niveau de l’agent UE-V, vous devez utiliser le même type de programme d’installation (fichier. exe ou paquet. msi) qui a installé l’agent UE-V précédent.</span><span class="sxs-lookup"><span data-stu-id="278e8-298">When you upgrade the UE-V Agent, you must use the same installer type (.exe file or .msi packet) that installed the previous UE-V Agent.</span></span> <span data-ttu-id="278e8-299">Par exemple, utilisez le AgentSetup.exe UE-V 2 pour mettre à niveau les agents UE-V 1,0 installés à l’aide de AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="278e8-299">For example, use the UE-V 2 AgentSetup.exe to upgrade UE-V 1.0 Agents that were installed by using AgentSetup.exe.</span></span>



<span data-ttu-id="278e8-300">Les configurations suivantes sont conservées lors de l’exécution du programme d’installation de l’agent:</span><span class="sxs-lookup"><span data-stu-id="278e8-300">The following configurations are preserved when the Agent Setup program runs:</span></span>

-   <span data-ttu-id="278e8-301">Emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="278e8-301">Settings storage path</span></span>

-   <span data-ttu-id="278e8-302">Paramètres du Registre</span><span class="sxs-lookup"><span data-stu-id="278e8-302">Registry settings</span></span>

-   <span data-ttu-id="278e8-303">Tâches planifiées (les paramètres d’intervalle sont réinitialisés à leurs valeurs par défaut)</span><span class="sxs-lookup"><span data-stu-id="278e8-303">Scheduled tasks (Interval settings are reset to their defaults)</span></span>

**<span data-ttu-id="278e8-304">Remarque</span><span class="sxs-lookup"><span data-stu-id="278e8-304">Note</span></span>**  
<span data-ttu-id="278e8-305">Un ordinateur avec des modèles d’emplacement des paramètres d’UE-V 2. x qui sont inscrits dans le journal des événements UE-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="278e8-305">A computer with UE-V 2.x settings location templates that are registered in the UE-V 1.0 Agent register errors in the Windows Event Log.</span></span>



<span data-ttu-id="278e8-306">Vous pouvez utiliser Microsoft System Center 2012 Configuration Manager ou un autre outil de distribution de logiciels d’entreprise pour automatiser et distribuer la mise à niveau de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-306">You can use Microsoft System Center 2012 Configuration Manager or another enterprise software distribution tool to automate and distribute the UE-V Agent upgrade.</span></span>

<span data-ttu-id="278e8-307">**Recommandations:** Nous vous recommandons d’effectuer la mise à niveau de tous les agents UE-V 1,0 dans un environnement informatique, mais cela n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="278e8-307">**Recommendations:** We recommend that you upgrade all of the UE-V 1.0 Agents in a computing environment, but it is not required.</span></span> <span data-ttu-id="278e8-308">UE-V 2. x les modèles d’emplacement des paramètres peuvent interagir avec un agent UE-V 1,0, car ils partagent uniquement les paramètres à partir du chemin de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="278e8-308">UE-V 2.x settings location templates can interact with a UE-V 1.0 Agent because they only share the settings from the settings storage path.</span></span> <span data-ttu-id="278e8-309">Toutefois, nous vous recommandons de déplacer les déploiements vers une version d’agent unique pour simplifier la gestion et prendre en charge UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-309">We recommend, however, that you move the deployments to a single agent version to simplify management and to support UE-V.</span></span>

### <span data-ttu-id="278e8-310">Réparation d’UE-V agent après une mise à niveau infructueuse</span><span class="sxs-lookup"><span data-stu-id="278e8-310">Repair the UE-V Agent after an unsuccessful upgrade</span></span>

<span data-ttu-id="278e8-311">Vous risquez de rencontrer des erreurs après avoir essayé l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="278e8-311">You might experience errors after you attempt one of the following operations:</span></span>

-   <span data-ttu-id="278e8-312">Effectuer une mise à niveau d’UE-V 1,0 vers UE-V 2</span><span class="sxs-lookup"><span data-stu-id="278e8-312">Upgrade from UE-V 1.0 to UE-V 2</span></span>

-   <span data-ttu-id="278e8-313">Effectuez une mise à niveau vers une version plus récente de Windows, par exemple, de Windows 7 vers Windows 8 ou de Windows 8 vers Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="278e8-313">Upgrade to a newer version of Windows, for example, from Windows 7 to Windows 8 or from Windows 8 to Windows 8.1.</span></span>

-   <span data-ttu-id="278e8-314">Désinstaller l’agent après la mise à niveau de l’agent UE-V</span><span class="sxs-lookup"><span data-stu-id="278e8-314">Uninstall the agent after upgrading the UE-V Agent</span></span>

<span data-ttu-id="278e8-315">Pour résoudre les problèmes, essayez de réparer l’agent UE-V en entrant la commande suivante à l’invite de commandes sur l’ordinateur sur lequel l’agent est installé.</span><span class="sxs-lookup"><span data-stu-id="278e8-315">To resolve any issues, attempt to repair the UE-V Agent by entering this command at a command prompt on the computer where the agent is installed.</span></span>

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

<span data-ttu-id="278e8-316">Vous pouvez ensuite réessayer le processus de désinstallation ou procéder à la mise à niveau en installant la version la plus récente de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="278e8-316">You can then retry the uninstall process or upgrade by installing the newer version of the UE-V Agent.</span></span>






## <span data-ttu-id="278e8-317">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="278e8-317">Related topics</span></span>


[<span data-ttu-id="278e8-318">Préparer un déploiement UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="278e8-318">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="278e8-319">Déployer UE-V 2. x pour des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="278e8-319">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)










---
title: Déployer UE-V 2. x pour des applications personnalisées
description: Déployer UE-V 2. x pour des applications personnalisées
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810535"
---
# <span data-ttu-id="8cbe6-103">Déployer UE-V 2. x pour des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="8cbe6-103">Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="8cbe6-104">Microsoft User Interface Virtualization (UE-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-104">Microsoft User Experience Virtualization (UE-V) 2.0.</span></span> <span data-ttu-id="8cbe6-105">2,1 et 2,1 SP1 utilisent des fichiers XML appelés **modèles d’emplacement des paramètres** pour surveiller et synchroniser les paramètres des applications de bureau et les paramètres de bureau Windows entre les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-105">2.1, and 2.1 SP1 use XML files called **settings location templates** to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="8cbe6-106">Par défaut, certains modèles d’emplacement de paramètres sont inclus dans UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-106">By default, some settings location templates are included in UE-V.</span></span> <span data-ttu-id="8cbe6-107">Toutefois, si vous voulez synchroniser les paramètres des applications de bureau autres que celles incluses dans les modèles par défaut, vous pouvez créer vos propres modèles d’emplacement des paramètres personnalisés à l’aide du générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-107">But if you want to synchronize settings for desktop applications other than those included in the default templates, you can create your own custom settings location templates by using the UE-V Generator.</span></span>

<span data-ttu-id="8cbe6-108">Une fois que vous avez lu le document de planification dans [préparer un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md) et que vous avez décidé de synchroniser les paramètres pour des applications personnalisées (tierce partie, métier, etc.), vous déploierez les fonctionnalités d’UE-v comme décrit dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-108">Once you have read through the planning material in [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md) and have decided that you want to synchronize settings for custom applications (third-party, line-of-business, etc.), you will deploy the features of UE-V as described in this topic.</span></span> <span data-ttu-id="8cbe6-109">Pour commencer, Voici les principales étapes à suivre pour synchroniser les paramètres des applications personnalisées:</span><span class="sxs-lookup"><span data-stu-id="8cbe6-109">To start, here are the main steps required to synchronize settings for custom applications:</span></span>

-   [<span data-ttu-id="8cbe6-110">Installer le générateur de UEV</span><span class="sxs-lookup"><span data-stu-id="8cbe6-110">Install the UEV Generator</span></span>](#uevgen)

    <span data-ttu-id="8cbe6-111">Utilisez le générateur de UEV pour créer des modèles de localisation de paramètres XML personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-111">Use the UEV Generator to create custom XML settings location templates.</span></span>

-   [<span data-ttu-id="8cbe6-112">Configurer un catalogue de modèles de paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="8cbe6-112">Configure a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="8cbe6-113">Vous pouvez définir ce chemin d’accès à l’emplacement de stockage des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-113">You can define this path where custom settings location templates are stored.</span></span>

-   [<span data-ttu-id="8cbe6-114">Créer des modèles d’emplacement des paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="8cbe6-114">Create custom settings location templates</span></span>](#createcustomtemplates)

    <span data-ttu-id="8cbe6-115">Ces modèles personnalisés permettent aux utilisateurs de synchroniser les paramètres des applications personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-115">These custom templates let users sync settings for custom applications.</span></span>

-   [<span data-ttu-id="8cbe6-116">Déployer les modèles d’emplacement des paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="8cbe6-116">Deploy the custom settings location templates</span></span>](#deploycustomtemplates)

    <span data-ttu-id="8cbe6-117">Après avoir testé le modèle personnalisé pour vous assurer que les paramètres sont correctement synchronisés, vous pouvez déployer ces modèles de l’une des façons suivantes:</span><span class="sxs-lookup"><span data-stu-id="8cbe6-117">After you test the custom template to ensure that settings are synced correctly, you can deploy these templates in one of these ways:</span></span>

    -   <span data-ttu-id="8cbe6-118">Par le biais de votre infrastructure de déploiement existante, telle que Configuration Manager;</span><span class="sxs-lookup"><span data-stu-id="8cbe6-118">Through your existing deployment infrastructure, such as Configuration Manager</span></span>

    -   <span data-ttu-id="8cbe6-119">En utilisant les préférences de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8cbe6-119">By using Group Policy preferences</span></span>

    -   [<span data-ttu-id="8cbe6-120">Déployer un catalogue de modèles de paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="8cbe6-120">Deploy a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="8cbe6-121">**Remarques**  Les modèles déployés à l’aide d’un ESD ou d’une stratégie de groupe doivent être enregistrés auprès d’UE-V Windows Management Instrumentation (WMI) ou Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-121">**Note** Templates that are deployed by using ESD or Group Policy must be registered with UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span>

     

## <span data-ttu-id="8cbe6-122">Préparer le déploiement d’UE-V 2. x pour des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="8cbe6-122">Prepare to Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="8cbe6-123">Avant de commencer à déployer les fonctionnalités d’UE-V qui gèrent les applications personnalisées, vous avez quelques points à revoir.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-123">Before you start deploying the UE-V features that handle custom applications, there are just a couple things to review.</span></span>

### <span data-ttu-id="8cbe6-124">Générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="8cbe6-124">The UE-V Generator</span></span>

<span data-ttu-id="8cbe6-125">Le générateur UE-V analyse une application afin de détecter et de capturer les emplacements où l’application stocke ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-125">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="8cbe6-126">L’application surveillée doit être une application classique.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-126">The application that is monitored must be a traditional application.</span></span> <span data-ttu-id="8cbe6-127">Vous utilisez le générateur UE-V pour créer des modèles d’emplacement des paramètres, mais il ne peut pas créer de modèle d’emplacement de paramètres à partir des types d’applications suivants:</span><span class="sxs-lookup"><span data-stu-id="8cbe6-127">You use the UE-V Generator to create settings location templates, but it cannot create a settings location template from these application types:</span></span>

-   <span data-ttu-id="8cbe6-128">Applications virtualisées</span><span class="sxs-lookup"><span data-stu-id="8cbe6-128">Virtualized applications</span></span>

-   <span data-ttu-id="8cbe6-129">Applications proposées via les services Terminal Server</span><span class="sxs-lookup"><span data-stu-id="8cbe6-129">Applications that are offered through Terminal Services</span></span>

-   <span data-ttu-id="8cbe6-130">Applications Java</span><span class="sxs-lookup"><span data-stu-id="8cbe6-130">Java applications</span></span>

-   <span data-ttu-id="8cbe6-131">Applications Windows  </span><span class="sxs-lookup"><span data-stu-id="8cbe6-131">Windows apps</span></span>

<span data-ttu-id="8cbe6-132">**Remarques**  Les modèles d’emplacement des paramètres d’UE-V ne peuvent pas être créés à partir d’applications virtuelles ou d’applications de services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-132">**Note** UE-V settings location templates cannot be created from virtualized applications or Terminal Services applications.</span></span> <span data-ttu-id="8cbe6-133">Toutefois, les paramètres qui sont synchronisés à l’aide des modèles peuvent être appliqués à ces applications.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-133">However, settings that are synchronized by using the templates can be applied to those applications.</span></span> <span data-ttu-id="8cbe6-134">Pour créer des modèles qui prennent en charge les applications VDI (Virtual Desktop Infrastructure) et Terminal Services, ouvrez une version du package Windows Installer (. msi) de l’application à l’aide du générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-134">To create templates that support Virtual Desktop Infrastructure (VDI) and Terminal Services applications, open a version of the Windows Installer (.msi) package of the application by using the UE-V Generator.</span></span> <span data-ttu-id="8cbe6-135">Pour plus d’informations sur les paramètres de synchronisation des applications virtuelles, voir [utilisation de UE-V 2. x avec les applications de virtualisation des](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md)applications.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-135">For more information about synchronizing settings for virtual applications, see [Using UE-V 2.x with Application Virtualization Applications](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span></span>

 

<span data-ttu-id="8cbe6-136">**Emplacements exclus:** Le processus de découverte exclut les emplacements qui stockent fréquemment les fichiers de logiciels d’application qui ne synchronisent pas correctement les paramètres entre les ordinateurs des utilisateurs ou les environnements informatiques.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-136">**Excluded Locations:** The discovery process excludes locations that commonly store application software files that do not synchronize settings well between user computers or computing environments.</span></span> <span data-ttu-id="8cbe6-137">Par défaut, celles-ci sont exclues:</span><span class="sxs-lookup"><span data-stu-id="8cbe6-137">By default, these are excluded:</span></span>

-   <span data-ttu-id="8cbe6-138">HKEY \ _CURRENT \ _USER clés de Registre et les fichiers auxquels l’utilisateur connecté ne peut pas écrire de valeurs</span><span class="sxs-lookup"><span data-stu-id="8cbe6-138">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="8cbe6-139">HKEY \ _CURRENT \ _USER clés de Registre et fichiers associés à la fonctionnalité principale du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-139">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="8cbe6-140">Toutes les clés de Registre se trouvant dans la ruche du _MACHINE HKEY \ _LOCAL</span><span class="sxs-lookup"><span data-stu-id="8cbe6-140">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="8cbe6-141">Fichiers situés dans les répertoires de fichiers du programme</span><span class="sxs-lookup"><span data-stu-id="8cbe6-141">Files that are located in Program Files directories</span></span>

-   <span data-ttu-id="8cbe6-142">Fichiers situés dans les utilisateurs \ \ \ [nom d’utilisateur \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="8cbe6-142">Files that are located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="8cbe6-143">Fichiers du système d’exploitation Windows situés dans% SystemRoot%</span><span class="sxs-lookup"><span data-stu-id="8cbe6-143">Windows operating system files that are located in %Systemroot%</span></span>

<span data-ttu-id="8cbe6-144">Si les clés de Registre et les fichiers qui sont stockés dans des emplacements exclus sont requis pour synchroniser les paramètres d’application, vous pouvez ajouter manuellement les emplacements au modèle d’emplacement paramètres pendant le processus de création de modèle.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-144">If registry keys and files that are stored in excluded locations are required to synchronize application settings, you can manually add the locations to the settings location template during the template creation process.</span></span>
<span data-ttu-id="8cbe6-145">Toutefois, seules _CURRENT les modifications apportées à la ruche du _USER</span><span class="sxs-lookup"><span data-stu-id="8cbe6-145">However, only changes to the HKEY\_CURRENT\_USER hive will be sync-ed.</span></span>

### <span data-ttu-id="8cbe6-146">Remplacer les modèles Microsoft par défaut</span><span class="sxs-lookup"><span data-stu-id="8cbe6-146">Replace the default Microsoft templates</span></span>

<span data-ttu-id="8cbe6-147">L’agent UE-V installe un groupe par défaut de modèles d’emplacements de paramètres pour les applications Microsoft courantes et les paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-147">The UE-V Agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="8cbe6-148">Si vous personnalisez ces modèles ou créez des modèles d’emplacement des paramètres pour synchroniser les paramètres des applications personnalisées, l’agent UE-V peut être configuré de manière à utiliser un catalogue de modèles de paramètres pour stocker les modèles.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-148">If you customize these templates, or create settings location templates to synchronize settings for custom applications, the UE-V Agent can be configured to use a settings template catalog to store the templates.</span></span> <span data-ttu-id="8cbe6-149">Dans ce cas, vous devez inclure les modèles par défaut ainsi que les modèles personnalisés dans le catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-149">In this case, you will need to include the default templates along with the custom templates in the settings template catalog.</span></span>

<span data-ttu-id="8cbe6-150">Lorsque vous [déployez un agent UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent), vous pouvez utiliser le paramètre de ligne `RegisterMSTemplates` de commande pour désactiver l’inscription des modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-150">When you [Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent), you can use the command-line parameter `RegisterMSTemplates` to disable the registration of the default Microsoft templates.</span></span>

<span data-ttu-id="8cbe6-151">Lorsque vous utilisez une stratégie de groupe pour configurer le chemin du catalogue de modèles de paramètres, vous pouvez choisir de remplacer les modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-151">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="8cbe6-152">Si vous configurez les paramètres de stratégie pour remplacer les modèles Microsoft par défaut, tous les modèles Microsoft par défaut installés par l’agent UE-V sont supprimés et seuls les modèles figurant dans le catalogue de modèles paramètres sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-152">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V Agent are deleted and only the templates that are located in the settings template catalog are used.</span></span> <span data-ttu-id="8cbe6-153">Le paramètre de configuration de l’agent UE-V `RegisterMSTemplates` doit être défini sur *true* pour pouvoir remplacer le modèle Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-153">The UE-V Agent configuration setting parameter `RegisterMSTemplates` must be set to *true* in order to override the default Microsoft template.</span></span>

<span data-ttu-id="8cbe6-154">**Remarques**  Si vous désactivez ce paramètre de stratégie une fois qu’il est activé, l’agent UE-V ne restaure pas les modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-154">**Note** If you disable this policy setting after it has been enabled, the UE-V Agent does not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="8cbe6-155">S’il existe des modèles personnalisés dans le catalogue de modèles de paramètres qui utilisent le même IDENTIFIant que les modèles Microsoft par défaut, et que l’agent UE-V n’est pas configuré pour remplacer les modèles Microsoft par défaut, les modèles Microsoft ne sont pas pris en compte.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-155">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V Agent is not configured to replace the default Microsoft templates, the Microsoft templates are ignored.</span></span>

<span data-ttu-id="8cbe6-156">Vous pouvez également remplacer les modèles par défaut en utilisant les fonctionnalités de Windows PowerShell UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-156">You can also replace the default templates by using the UE-V Windows PowerShell features.</span></span> <span data-ttu-id="8cbe6-157">Pour remplacer le modèle Microsoft par défaut par Windows PowerShell, annulez l’enregistrement de tous les modèles Microsoft par défaut, puis enregistrez les modèles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-157">To replace the default Microsoft template with Windows PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="8cbe6-158">**Remarques**  Les packages d’anciens paramètres restent dans l’emplacement de stockage des paramètres même si vous déployez de nouveaux modèles d’emplacement pour une application.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-158">**Note** Old settings packages remain in the settings storage location even if you deploy new settings location templates for an application.</span></span> <span data-ttu-id="8cbe6-159">Ces packages ne sont pas lus par l’agent, mais aucun d’eux n’est automatiquement supprimé.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-159">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <a href="" id="uevgen"></a><span data-ttu-id="8cbe6-160">Installez le générateur UEV 2. x</span><span class="sxs-lookup"><span data-stu-id="8cbe6-160">Install the UEV 2.x Generator</span></span>


<span data-ttu-id="8cbe6-161">Pour créer un modèle d’emplacement des paramètres personnalisés, installez le générateur de 2,0 de Microsoft User Interface Virtualization (UE-V) sur un ordinateur que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-161">Install the Microsoft User Experience Virtualization (UE-V) 2.0 Generator on a computer that you can then use to create a custom settings location template.</span></span> <span data-ttu-id="8cbe6-162">Les applications doivent être installées sur l’ordinateur pour pouvoir générer les modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-162">This computer should have the applications installed for which custom settings location templates are to be generated.</span></span>

**<span data-ttu-id="8cbe6-163">Pour installer le générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="8cbe6-163">To install the UE-V Generator</span></span>**

1.  <span data-ttu-id="8cbe6-164">En tant qu’utilisateur disposant de droits d’administrateur local, recherchez le fichier d’installation du générateur UE-V **ToolSetup.exe** fourni avec le logiciel UE-v.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-164">As a user with local administrator rights, locate the UE-V Generator installation file **ToolSetup.exe** provided with the UE-V software.</span></span> <span data-ttu-id="8cbe6-165">Ou, si vous connaissez l’architecture de l’ordinateur, vous pouvez exécuter le fichier Windows Installer (. msi) approprié, **ToolsSetupx64.msi** ou **ToolsSetupx86.msi**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-165">Or, if you know the computer architecture, you can run the appropriate Windows Installer (.msi) file, **ToolsSetupx64.msi** or **ToolsSetupx86.msi**.</span></span>

2.  <span data-ttu-id="8cbe6-166">Double-cliquez sur le fichier d’installation.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-166">Double-click the installation file.</span></span> <span data-ttu-id="8cbe6-167">L’Assistant de configuration du générateur de la virtualisation de l’utilisation de l’utilisateur s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-167">The User Experience Virtualization Generator Setup wizard opens.</span></span> <span data-ttu-id="8cbe6-168">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-168">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="8cbe6-169">Acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-169">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="8cbe6-170">Cliquez sur les options pour les mises à jour Microsoft et le programme d’amélioration du produit.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-170">Click the options for Microsoft Updates and the Customer Experience Improvement Program.</span></span>

5.  <span data-ttu-id="8cbe6-171">Sélectionnez le dossier de destination dans lequel installer le générateur UE-V, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-171">Select the destination folder in which to install the UE-V Generator, and then click **Next**.</span></span>

6.  <span data-ttu-id="8cbe6-172">Cliquez sur **installer** pour lancer l’installation.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-172">Click **Install** to begin the installation.</span></span>

    <span data-ttu-id="8cbe6-173">**Remarques**  Une invite de **contrôle de compte d’utilisateur** apparaît avant l’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-173">**Note** A prompt for **User Account Control** appears before the application is installed.</span></span> <span data-ttu-id="8cbe6-174">Une autorisation est requise pour l’installation d’UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-174">Permission is required to install the UE-V Generator.</span></span>

     

7.  <span data-ttu-id="8cbe6-175">Cliquez sur **Terminer** pour fermer l’Assistant une fois l’installation terminée.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-175">Click **Finish** to close the wizard after the installation is finished.</span></span> <span data-ttu-id="8cbe6-176">Vous devez redémarrer votre ordinateur avant de pouvoir exécuter le générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-176">You must restart your computer before you can run the UE-V Generator.</span></span>

    <span data-ttu-id="8cbe6-177">Pour vérifier que l’installation a réussi, cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l’utilisation de l' **utilisateur Microsoft**, puis sur **Générateur de virtualisation Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-177">To verify that the installation was successful, click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

    <span data-ttu-id="8cbe6-178">**Remarques**  Le générateur UE-V 2 ne peut être utilisé que pour créer des modèles pour les agents UE-V 2.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-178">**Note** The UE-V 2 Generator can only be used to create templates for UE-V 2 Agents.</span></span> <span data-ttu-id="8cbe6-179">Dans le cas d’un déploiement mixte d’UE-V 1,0 agents et d’acteurs de l’UE-V 2, vous devez continuer à utiliser le générateur de complément UE-V 1,0 jusqu’à ce que vous ayez procédé à la mise à niveau de tous les agents UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-179">In a mixed deployment of UE-V 1.0 Agents and UE-V 2 Agents, you should continue to use the UE-V 1.0 Generator until you have upgraded all UE-V Agents.</span></span>

     

## <a href="" id="deploycatalogue"></a><span data-ttu-id="8cbe6-180">Déployer un catalogue de modèles de paramètres</span><span class="sxs-lookup"><span data-stu-id="8cbe6-180">Deploy a Settings Template Catalog</span></span>


<span data-ttu-id="8cbe6-181">Le catalogue de modèles de paramètres de virtualisation de l’utilisation de l’utilisateur est un chemin de dossier sur les ordinateurs UE-V ou un partage réseau SMB qui stocke tous les modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-181">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="8cbe6-182">Une tâche planifiée dans l’agent UE-V vérifie cet emplacement une fois par jour et met à jour son comportement de synchronisation, en fonction des modèles figurant dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-182">A scheduled task in the UE-V Agent checks this location one time each day and updates its synchronization behavior, based on the templates in this folder.</span></span>

<span data-ttu-id="8cbe6-183">L’agent UE-V inscrit les modèles qui ont été ajoutés ou mis à jour dans ce dossier après la dernière vérification du dossier et l’annulation de l’inscription de modèles qui ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-183">The UE-V Agent registers templates that were added or updated in this folder after the last time that the folder was checked and unregisters templates that are removed.</span></span> <span data-ttu-id="8cbe6-184">Par défaut, les modèles sont inscrits et annulés une fois par jour à 3:30 matin.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-184">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="8cbe6-185">heure locale par le planificateur de tâches et au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-185">local time by the Task Scheduler and at system startup.</span></span> <span data-ttu-id="8cbe6-186">Pour personnaliser la fréquence de cette tâche planifiée, reportez-vous à [la rubrique modification de la fréquence des tâches planifiées UE-V 2.](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)</span><span class="sxs-lookup"><span data-stu-id="8cbe6-186">To customize the frequency of this scheduled task, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="8cbe6-187">Vous pouvez configurer le chemin du catalogue de modèles de paramètres à l’aide des options de ligne de commande d’installation, de stratégie de groupe, de WMI ou de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-187">You can configure the settings template catalog path by using the installation command-line options, Group Policy, WMI, or Windows PowerShell.</span></span> <span data-ttu-id="8cbe6-188">Les modèles stockés dans le modèle de modèle paramètres sont automatiquement inscrits et désinscrits par une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-188">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span>

**<span data-ttu-id="8cbe6-189">Pour configurer le catalogue de modèles de paramètres pour UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="8cbe6-189">To configure the settings template catalog for UE-V 2.x</span></span>**

1.  <span data-ttu-id="8cbe6-190">Créez un dossier sur l’ordinateur sur lequel est stocké le catalogue de modèles de paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-190">Create a new folder on the computer that stores the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="8cbe6-191">Définissez les autorisations de niveau de partage (SMB) suivantes pour le dossier du catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-191">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="8cbe6-192">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="8cbe6-192">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="8cbe6-193">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="8cbe6-193">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8cbe6-194">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="8cbe6-194">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-195">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="8cbe6-195">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8cbe6-196">Ordinateurs de domaine</span><span class="sxs-lookup"><span data-stu-id="8cbe6-196">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-197">Lire les niveaux d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8cbe6-197">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8cbe6-198">Administrateurs</span><span class="sxs-lookup"><span data-stu-id="8cbe6-198">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-199">Niveaux d’autorisation en lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8cbe6-199">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="8cbe6-200">Définissez les autorisations de système de fichiers NTFS suivantes pour le dossier du catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-200">Set the following NTFS file system permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="8cbe6-201">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="8cbe6-201">User account</span></span></th>
    <th align="left"><span data-ttu-id="8cbe6-202">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="8cbe6-202">Recommended permissions</span></span></th>
    <th align="left"><span data-ttu-id="8cbe6-203">Appliquer à</span><span class="sxs-lookup"><span data-stu-id="8cbe6-203">Apply to</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8cbe6-204">Créateur/propriétaire</span><span class="sxs-lookup"><span data-stu-id="8cbe6-204">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-205">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="8cbe6-205">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-206">Ce dossier, les sous-dossiers et les fichiers</span><span class="sxs-lookup"><span data-stu-id="8cbe6-206">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8cbe6-207">Ordinateurs de domaine</span><span class="sxs-lookup"><span data-stu-id="8cbe6-207">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-208">Afficher le contenu du dossier et lire</span><span class="sxs-lookup"><span data-stu-id="8cbe6-208">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-209">Ce dossier, les sous-dossiers et les fichiers</span><span class="sxs-lookup"><span data-stu-id="8cbe6-209">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8cbe6-210">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="8cbe6-210">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-211">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="8cbe6-211">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-212">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="8cbe6-212">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8cbe6-213">Administrateurs</span><span class="sxs-lookup"><span data-stu-id="8cbe6-213">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-214">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="8cbe6-214">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8cbe6-215">Ce dossier, les sous-dossiers et les fichiers</span><span class="sxs-lookup"><span data-stu-id="8cbe6-215">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="8cbe6-216">Cliquez sur **OK** pour fermer les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-216">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="8cbe6-217">Au minimum, le partage réseau doit accorder des autorisations pour le groupe ordinateurs du domaine.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-217">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="8cbe6-218">Par ailleurs, accordez des autorisations d’accès au dossier de partage réseau aux administrateurs qui doivent gérer les modèles stockés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-218">In addition, grant access permissions for the network share folder to administrators who are to manage the stored templates.</span></span>

## <a href="" id="createcustomtemplates"></a><span data-ttu-id="8cbe6-219">Créer des modèles d’emplacement des paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="8cbe6-219">Create Custom Settings Location Templates</span></span>


<span data-ttu-id="8cbe6-220">Utilisez le générateur UE-V pour créer des modèles d’emplacement des paramètres pour les applications métier ou d’autres applications personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-220">Use the UE-V Generator to create settings location templates for line-of-business applications or other custom applications.</span></span> <span data-ttu-id="8cbe6-221">Une fois que le modèle d’application est créé, vous pouvez le déployer sur des ordinateurs de sorte que les paramètres soient synchronisés pour cette application.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-221">After the template for an application is created, you can deploy it to computers so that settings are synchronized for that application.</span></span>

**<span data-ttu-id="8cbe6-222">Pour créer un modèle d’emplacement des paramètres UE-V avec le générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="8cbe6-222">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="8cbe6-223">Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **utilisation de Microsoft**, puis sur générateur de **virtualisation Microsoft User Interface**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-223">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="8cbe6-224">Cliquez sur **créer un modèle d’emplacement des paramètres**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-224">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="8cbe6-225">Spécifiez l’application.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-225">Specify the application.</span></span> <span data-ttu-id="8cbe6-226">Naviguez jusqu’au chemin d’accès de l’application (. exe) ou du raccourci de l’application (. lnk) pour lequel vous voulez créer un modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-226">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="8cbe6-227">Spécifiez les arguments de ligne de commande, le cas échéant, et le répertoire de travail, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-227">Specify the command-line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="8cbe6-228">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-228">Click **Next** to continue.</span></span>

    <span data-ttu-id="8cbe6-229">**Remarques**  Avant le démarrage de l’application, le système affiche une invite de **contrôle de compte d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-229">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="8cbe6-230">Une autorisation est requise pour contrôler les emplacements du Registre et des fichiers utilisés par l’application pour le stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-230">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="8cbe6-231">Après le démarrage de l’application, fermez l’application.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-231">After the application starts, close the application.</span></span> <span data-ttu-id="8cbe6-232">Le générateur UE-V enregistre les emplacements où l’application stocke ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-232">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="8cbe6-233">Une fois le processus terminé, cliquez sur **suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-233">After the process is completed, click **Next** to continue.</span></span>

6.  <span data-ttu-id="8cbe6-234">Passez en revue et activez les cases à cocher situées en regard des emplacements de paramètres de Registre et des emplacements de fichier de paramètres appropriés à synchroniser pour cette application.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-234">Review and select the check boxes that are next to the appropriate registry settings locations and settings file locations to synchronize for this application.</span></span> <span data-ttu-id="8cbe6-235">La liste inclut les deux catégories suivantes pour les emplacements de paramètres:</span><span class="sxs-lookup"><span data-stu-id="8cbe6-235">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="8cbe6-236">**Standard**: les paramètres de l’application qui sont stockés dans le Registre sous les clés HKEY \ _CURRENT \ _USER ou dans les dossiers de fichiers sous \ \ **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **itinérance**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-236">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="8cbe6-237">UE-V Generator inclut ces paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-237">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="8cbe6-238">Non **standard**: les paramètres d’application stockés en dehors des emplacements sont spécifiés dans les recommandations en matière de stockage des données de paramètres (facultatif).</span><span class="sxs-lookup"><span data-stu-id="8cbe6-238">**Nonstandard**: Application settings that are stored outside the locations are specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="8cbe6-239">Il s’agit des fichiers et dossiers sous **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-239">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="8cbe6-240">Passez en revue ces emplacements pour déterminer s’ils doivent figurer dans le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-240">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="8cbe6-241">Activez les cases à cocher emplacements pour les inclure.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-241">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="8cbe6-242">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-242">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="8cbe6-243">Examinez et modifiez les **Propriétés**, emplacements **du Registre** et emplacements des **fichiers** pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-243">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="8cbe6-244">Modifiez les propriétés suivantes sous l’onglet **Propriétés** :</span><span class="sxs-lookup"><span data-stu-id="8cbe6-244">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="8cbe6-245">**Nom**de l’application: nom de l’application qui est écrite dans la description des propriétés du programme files.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-245">**Application Name**: The application name that is written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="8cbe6-246">**Nom du programme**: nom du programme provenant des propriétés du fichier programme.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-246">**Program name**: The name of the program that is taken from the program file properties.</span></span> <span data-ttu-id="8cbe6-247">Ce nom est généralement l’extension de nom de fichier. exe.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-247">This name usually has the .exe file name extension.</span></span>

        -   <span data-ttu-id="8cbe6-248">**Version du produit**: numéro de version du fichier. exe de l’application.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-248">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="8cbe6-249">En conjonction avec la version du **fichier**, cette propriété permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-249">This property, in conjunction with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="8cbe6-250">Cette propriété accepte un numéro de version principal.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-250">This property accepts a major version number.</span></span> <span data-ttu-id="8cbe6-251">Si cette propriété est vide, le modèle d’emplacement des paramètres s’applique à toutes les versions du produit.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-251">If this property is empty, the settings location template applies to all versions of the product.</span></span>

        -   <span data-ttu-id="8cbe6-252">**Version du fichier**: numéro de version du fichier. exe de l’application.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-252">**File version**: The file version number of the .exe file of the application.</span></span> <span data-ttu-id="8cbe6-253">Combinée à la **version du produit**, cette propriété permet d’identifier les applications ciblées par le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-253">This property, in conjunction with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="8cbe6-254">Cette propriété accepte un numéro de version principal.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-254">This property accepts a major version number.</span></span> <span data-ttu-id="8cbe6-255">Si cette propriété est vide, le modèle d’emplacement des paramètres s’applique à toutes les versions du programme.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-255">If this property is empty, the settings location template applies to all versions of the program.</span></span>

        -   <span data-ttu-id="8cbe6-256">**Nom** de l’auteur du modèle (facultatif): nom de l’auteur du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-256">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="8cbe6-257">**Courrier de création de modèles** (facultatif): adresse de messagerie de l’auteur du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-257">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="8cbe6-258">L’onglet **Registre** recense la **clé** et l' **étendue** des emplacements du Registre inclus dans le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-258">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="8cbe6-259">Modifiez les emplacements du Registre à l’aide du menu déroulant **tâches** .</span><span class="sxs-lookup"><span data-stu-id="8cbe6-259">Edit the registry locations by using the **Tasks** drop-down menu.</span></span> <span data-ttu-id="8cbe6-260">Les tâches vous permettent d’ajouter de nouvelles clés, de modifier le nom ou l’étendue des clés existantes, de supprimer des clés et de parcourir le registre où se trouvent les clés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-260">Tasks enable you to add new keys, edit the name or scope of existing keys, delete keys, and browse the registry where the keys are located.</span></span> <span data-ttu-id="8cbe6-261">Utilisez l’étendue **all settings** pour inclure tous les paramètres de Registre sous la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-261">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="8cbe6-262">Utilisez les **paramètres et** sous-clés pour inclure tous les paramètres de Registre sous les paramètres de clé, de sous-clé et de sous-clé spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-262">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="8cbe6-263">L’onglet **fichiers** recense le chemin d’accès au fichier et le masque des fichiers des emplacements de fichier inclus dans le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-263">The **Files** tab lists the file path and file mask of the file locations that are included in the settings location template.</span></span> <span data-ttu-id="8cbe6-264">Modifiez les emplacements des fichiers à l’aide du menu déroulant **tâches** .</span><span class="sxs-lookup"><span data-stu-id="8cbe6-264">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="8cbe6-265">Les tâches d’emplacement des fichiers vous permettent d’ajouter de nouveaux fichiers ou dossiers, de modifier l’étendue des fichiers ou dossiers existants, de supprimer des fichiers ou des dossiers, et d’ouvrir l’emplacement sélectionné dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-265">Tasks for file locations enable you to add new files or folder locations, edit the scope of existing files or folders, delete files or folders, and open the selected location in Windows Explorer.</span></span> <span data-ttu-id="8cbe6-266">Laissez le masque de fichiers vide pour inclure tous les fichiers dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-266">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="8cbe6-267">Cliquez sur **créer**, puis cliquez sur **Enregistrer** pour enregistrer le modèle d’emplacement des paramètres sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-267">Click **Create**, and then click **Save** to save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="8cbe6-268">Cliquez sur **Fermer** pour fermer l’Assistant modèle de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-268">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="8cbe6-269">Quittez l’application de générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-269">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="8cbe6-270">Après avoir créé le modèle d’emplacement des paramètres pour une application, vous devez tester le modèle.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-270">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="8cbe6-271">Déployez le modèle dans un environnement de laboratoire avant de le mettre en production dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-271">Deploy the template in a lab environment before you put it into production in the enterprise.</span></span>

<span data-ttu-id="8cbe6-272">[Référence du schéma de modèle d’application pour UE-V](https://technet.microsoft.com/library/dn763947.aspx) détails de la structure XML du modèle d’emplacement des paramètres d’UE-v et fournit des instructions pour la modification de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-272">[Application Template Schema Reference for UE-V](https://technet.microsoft.com/library/dn763947.aspx) details the XML structure of the UE-V settings location template and provides guidance for editing these files.</span></span>

## <a href="" id="deploycustomtemplates"></a><span data-ttu-id="8cbe6-273">Déployer les modèles d’emplacement des paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="8cbe6-273">Deploy the Custom Settings Location Templates</span></span>


<span data-ttu-id="8cbe6-274">Après avoir créé un modèle d’emplacement des paramètres auprès du générateur UE-V, vous devez le tester pour vous assurer que les paramètres de l’application sont correctement synchronisés.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-274">After you create a settings location template with the UE-V Generator, you should test it to ensure that the application settings are synchronized correctly.</span></span> <span data-ttu-id="8cbe6-275">Vous pouvez ensuite déployer en toute sécurité le modèle d’emplacement des paramètres sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-275">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="8cbe6-276">Les modèles d’emplacement des paramètres peuvent être déployés en utilisant l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="8cbe6-276">Settings location templates can be deployed by using one of these methods:</span></span>

-   <span data-ttu-id="8cbe6-277">Système de distribution de logiciels d’entreprise (ESD) tel que System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8cbe6-277">An enterprise software distribution (ESD) system such as System Center Configuration Manager</span></span>

-   <span data-ttu-id="8cbe6-278">Stratégie de groupe Préférences</span><span class="sxs-lookup"><span data-stu-id="8cbe6-278">Group Policy preferences</span></span>

-   <span data-ttu-id="8cbe6-279">Catalogue de modèles de paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="8cbe6-279">A UE-V settings template catalog</span></span>

<span data-ttu-id="8cbe6-280">Les modèles déployés à l’aide d’un système ESD ou d’objets de stratégie de groupe doivent être inscrits via le service WMI (Windows Management Instrumentation) ou Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-280">Templates that are deployed by using an ESD system or Group Policy Objects must be registered through UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span> <span data-ttu-id="8cbe6-281">Les modèles stockés dans l’emplacement du catalogue de modèles de paramètres sont automatiquement inscrits par l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-281">Templates that are stored in the settings template catalog location are automatically registered by the UE-V Agent.</span></span>

**<span data-ttu-id="8cbe6-282">Pour utiliser le chemin de catalogue du modèle de paramètres pour déployer les modèles d’emplacement des paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="8cbe6-282">To use the settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="8cbe6-283">Naviguez jusqu’au dossier de partage réseau défini comme catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-283">Browse to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="8cbe6-284">Ajoutez, supprimez ou mettez à jour les modèles d’emplacement des paramètres dans le catalogue de modèles de paramètres pour refléter la configuration de modèle d’agent UE-V que vous voulez pour les ordinateurs UE-V.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-284">Add, remove, or update settings location templates in the settings template catalog to reflect the UE-V Agent template configuration that you want for UE-V computers.</span></span>

    <span data-ttu-id="8cbe6-285">**Remarques**  Les modèles sur les ordinateurs sont mis à jour quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-285">**Note** Templates on computers are updated daily.</span></span> <span data-ttu-id="8cbe6-286">La mise à jour dépend des modifications apportées au catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-286">The update is based on changes to the settings template catalog.</span></span>

     

3.  <span data-ttu-id="8cbe6-287">Pour mettre à jour manuellement des modèles sur un ordinateur qui exécute l’agent UE-V, ouvrez une invite de commandes avec élévation de privilèges et naviguez jusqu’à \*\*% programme Files%\\Microsoft de l’utilisation de l’utilisateur \ \ agent \ \ &lt; x86 ou x64 &gt; \*\*, puis exécutez **ApplySettingsTemplateCatalog.exe**.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-287">To manually update templates on a computer that runs the UE-V Agent, open an elevated command prompt, and browse to **%Program Files%\\Microsoft User Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe**.</span></span>

    <span data-ttu-id="8cbe6-288">**Remarques**  Ce programme s’exécute automatiquement au démarrage de l’ordinateur et à tous les jours à 3:30 A. M.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-288">**Note** This program runs automatically during computer startup and daily at 3:30 A. M.</span></span> <span data-ttu-id="8cbe6-289">pour recueillir les nouveaux modèles récemment ajoutés au catalogue.</span><span class="sxs-lookup"><span data-stu-id="8cbe6-289">to gather any new templates that were recently added to the catalog.</span></span>

     






## <span data-ttu-id="8cbe6-290">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8cbe6-290">Related topics</span></span>


[<span data-ttu-id="8cbe6-291">Préparer un déploiement UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="8cbe6-291">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="8cbe6-292">Déployer les fonctionnalités UE-V2.x requises</span><span class="sxs-lookup"><span data-stu-id="8cbe6-292">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 






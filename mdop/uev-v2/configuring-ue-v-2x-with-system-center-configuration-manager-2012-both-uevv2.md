---
title: Configuration d’UE-V 2. x avec System Center Configuration Manager 2012
description: Configuration d’UE-V 2. x avec System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810536"
---
# <span data-ttu-id="7ce45-103">Configuration d’UE-V 2. x avec System Center Configuration Manager 2012</span><span class="sxs-lookup"><span data-stu-id="7ce45-103">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>


<span data-ttu-id="7ce45-104">Après l’installation de Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1 et leurs fonctionnalités requises, UE-V doit être configurée.</span><span class="sxs-lookup"><span data-stu-id="7ce45-104">After you install Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 and their required features, UE-V must be configured.</span></span> <span data-ttu-id="7ce45-105">Le Pack de configuration UE-V permet aux administrateurs d’utiliser la fonctionnalité paramètres de conformité de System Center Configuration Manager 2012 SP1 ou une version ultérieure pour appliquer des configurations cohérentes sur les sites dans lesquels UE-V et Configuration Manager sont installés.</span><span class="sxs-lookup"><span data-stu-id="7ce45-105">The UE-V Configuration Pack provides a way for administrators to use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

## <span data-ttu-id="7ce45-106">Fonctionnalités prises en charge dans UE-V configuration Pack</span><span class="sxs-lookup"><span data-stu-id="7ce45-106">UE-V Configuration Pack supported features</span></span>


<span data-ttu-id="7ce45-107">Le Pack de configuration d’UE-V inclut des outils qui permettent d’effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="7ce45-107">The UE-V Configuration Pack includes tools to perform the following tasks:</span></span>

-   <span data-ttu-id="7ce45-108">Créer ou mettre à jour les paramètres de distribution de modèles d’emplacement des paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="7ce45-108">Create or update UE-V settings location template distribution baselines.</span></span>

    -   <span data-ttu-id="7ce45-109">Définir des modèles UE-V pour être inscrits ou désinscrits</span><span class="sxs-lookup"><span data-stu-id="7ce45-109">Define UE-V templates to be registered or unregistered</span></span>

    -   <span data-ttu-id="7ce45-110">Mise à jour des éléments de configuration de modèle UE-V et des plannings de référence en tant que modèles ajoutés ou mis à jour</span><span class="sxs-lookup"><span data-stu-id="7ce45-110">Update UE-V template configuration items and baselines as templates are added or updated</span></span>

    -   <span data-ttu-id="7ce45-111">Distribuer et enregistrer des modèles UE-V à l’aide de la correction standard des éléments de configuration</span><span class="sxs-lookup"><span data-stu-id="7ce45-111">Distribute and register UE-V templates using standard Configuration Item remediation</span></span>

-   <span data-ttu-id="7ce45-112">Créez ou mettez à jour un élément de configuration de la stratégie d’agent UE-V pour définir ou effacer ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="7ce45-112">Create or update a UE-V Agent policy configuration item to set or clear these settings.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7ce45-113">Taille maximale du package</span><span class="sxs-lookup"><span data-stu-id="7ce45-113">Max package size</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-114">Activer/désactiver la synchronisation des applications Windows</span><span class="sxs-lookup"><span data-stu-id="7ce45-114">Enable/disable Windows app sync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-115">Attendez la fin de la synchronisation lors du démarrage de l’application</span><span class="sxs-lookup"><span data-stu-id="7ce45-115">Wait for sync on application start</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7ce45-116">Définir le délai d’importation</span><span class="sxs-lookup"><span data-stu-id="7ce45-116">Setting import delay</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-117">Synchroniser les applications Windows non répertoriées</span><span class="sxs-lookup"><span data-stu-id="7ce45-117">Sync unlisted Windows apps</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-118">Attendez la fin de la synchronisation lors de l’ouverture de session</span><span class="sxs-lookup"><span data-stu-id="7ce45-118">Wait for sync on logon</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7ce45-119">Notification d’importation de paramètres</span><span class="sxs-lookup"><span data-stu-id="7ce45-119">Settings import notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-120">URL du contact</span><span class="sxs-lookup"><span data-stu-id="7ce45-120">IT contact URL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-121">Attendre le délai de synchronisation</span><span class="sxs-lookup"><span data-stu-id="7ce45-121">Wait for sync timeout</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7ce45-122">Emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="7ce45-122">Settings storage path</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-123">IL contacte un texte descriptif</span><span class="sxs-lookup"><span data-stu-id="7ce45-123">IT contact descriptive text</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-124">Chemin du catalogue de modèles de paramètres</span><span class="sxs-lookup"><span data-stu-id="7ce45-124">Settings template catalog path</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7ce45-125">Activation de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="7ce45-125">Sync enablement</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-126">Icône de barre d’État activée</span><span class="sxs-lookup"><span data-stu-id="7ce45-126">Tray icon enabled</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-127">Démarrer/arrêter le service d’agent UE-V</span><span class="sxs-lookup"><span data-stu-id="7ce45-127">Start/Stop UE-V agent service</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7ce45-128">Méthode de synchronisation</span><span class="sxs-lookup"><span data-stu-id="7ce45-128">Sync method</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-129">Notification d’utilisation initiale</span><span class="sxs-lookup"><span data-stu-id="7ce45-129">First use notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ce45-130">Définir les applications Windows qui feront l’itinérance des paramètres</span><span class="sxs-lookup"><span data-stu-id="7ce45-130">Define which Windows apps will roam settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7ce45-131">Délai de synchronisation</span><span class="sxs-lookup"><span data-stu-id="7ce45-131">Sync timeout</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="7ce45-132">Vérifier la conformité en confirmant que UE-V est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7ce45-132">Verify compliance by confirming that UE-V is running.</span></span>

## <span data-ttu-id="7ce45-133">Générer un élément de configuration de la stratégie d’agent UE-V</span><span class="sxs-lookup"><span data-stu-id="7ce45-133">Generate a UE-V Agent Policy Configuration Item</span></span>


<span data-ttu-id="7ce45-134">Toutes les stratégies et configuration de l’agent UE-V sont distribuées à l’aide d’un élément de configuration unique généré à l’aide de l’outil UevAgentPolicyGenerator.exe.</span><span class="sxs-lookup"><span data-stu-id="7ce45-134">All UE-V Agent policy and configuration is distributed through a single configuration item that is generated using the UevAgentPolicyGenerator.exe tool.</span></span> <span data-ttu-id="7ce45-135">Cet outil lit la configuration souhaitée à partir d’un fichier de configuration XML et crée un CI contenant les paramètres de découverte et de correction nécessaires à la mise en conformité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7ce45-135">This tool reads the desired configuration from an XML configuration file and creates a CI containing the discovery and remediation settings needed to bring the machine into compliance.</span></span>

<span data-ttu-id="7ce45-136">Le fichier CAB de configuration de la stratégie d’agent UE-V est créé à l’aide de l’outil de ligne de commande UevTemplateBaselineGenerator.exe, qui comporte les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="7ce45-136">The UE-V Agent policy configuration item CAB file is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="7ce45-137">Code du site de site &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="7ce45-137">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="7ce45-138">Nom de l' &lt; &gt; argument PolicyName facultatif: est défini par défaut sur «UE-V Policy agent» en cas de non-présentation</span><span class="sxs-lookup"><span data-stu-id="7ce45-138">PolicyName &lt;name&gt; Optional: Defaults to “UE-V Agent Policy” if not present</span></span>

-   <span data-ttu-id="7ce45-139">&lt;Description &gt; de PolicyDescription facultatif: une description est fournie en cas de non-présentation</span><span class="sxs-lookup"><span data-stu-id="7ce45-139">PolicyDescription &lt;description&gt; Optional: A description is provided if not present</span></span>

-   <span data-ttu-id="7ce45-140">CabFilePath &lt; chemin d’accès complet de l’élément de configuration. Fichier CAB&gt;</span><span class="sxs-lookup"><span data-stu-id="7ce45-140">CabFilePath &lt;full path to configuration item .CAB file&gt;</span></span>

-   <span data-ttu-id="7ce45-141">ConfigurationFile &lt; chemin complet du fichier XML de configuration de l’agent&gt;</span><span class="sxs-lookup"><span data-stu-id="7ce45-141">ConfigurationFile &lt;full path to agent configuration XML file&gt;</span></span>

<span data-ttu-id="7ce45-142">**Remarques**  Il peut être nécessaire de modifier la stratégie d’exécution PowerShell pour autoriser l’exécution de ces scripts dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="7ce45-142">**Note** It might be necessary to change the PowerShell execution policy to allow these scripts to run in your environment.</span></span> <span data-ttu-id="7ce45-143">Procédez comme suit dans la console Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="7ce45-143">Perform these steps in the Configuration Manager console:</span></span>

1.  <span data-ttu-id="7ce45-144">Sélectionner **les &gt; &gt; Propriétés de paramètres du client d’administration**</span><span class="sxs-lookup"><span data-stu-id="7ce45-144">Select **Administration &gt; Client Settings &gt; Properties**</span></span>

2.  <span data-ttu-id="7ce45-145">Dans l’onglet **agent utilisateur** , définissez la **stratégie d’exécution PowerShell** sur **outrepasser**</span><span class="sxs-lookup"><span data-stu-id="7ce45-145">In the **User Agent** tab, set the **PowerShell Execution Policy** to **Bypass**</span></span>

<a href="" id="create"></a>**<span data-ttu-id="7ce45-146">Créer le premier élément de configuration de stratégie UE-V</span><span class="sxs-lookup"><span data-stu-id="7ce45-146">Create the First UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="7ce45-147">Copiez le fichier de configuration des paramètres par défaut à partir du répertoire d’installation d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="7ce45-147">Copy the default settings configuration file from the UE-V Config Pack installation directory to a location visible to your ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    <span data-ttu-id="7ce45-148">Le fichier de configuration par défaut comporte cinq sections:</span><span class="sxs-lookup"><span data-stu-id="7ce45-148">The default configuration file contains five sections:</span></span>

    <a href="" id="computer-policy"></a>**<span data-ttu-id="7ce45-149">Stratégie d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="7ce45-149">Computer Policy</span></span>**  
    <span data-ttu-id="7ce45-150">Tous les paramètres au niveau d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="7ce45-150">All UE-V machine level settings.</span></span> <span data-ttu-id="7ce45-151">L’attribut DesiredState peut être</span><span class="sxs-lookup"><span data-stu-id="7ce45-151">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="7ce45-152">**Définir** la valeur sur le registre</span><span class="sxs-lookup"><span data-stu-id="7ce45-152">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="7ce45-153">**Effacer** pour supprimer le paramètre</span><span class="sxs-lookup"><span data-stu-id="7ce45-153">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="7ce45-154">**Non géré** pour que l’élément de configuration reste à l’état actuel</span><span class="sxs-lookup"><span data-stu-id="7ce45-154">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="7ce45-155">Ne pas supprimer les lignes de cette section.</span><span class="sxs-lookup"><span data-stu-id="7ce45-155">Do not remove lines from this section.</span></span> <span data-ttu-id="7ce45-156">Définissez plutôt le DesiredState sur «non géré» si vous ne souhaitez pas que Configuration Manager modifie les valeurs actuelles ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ce45-156">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="currentcomputeruserpolicy"></a>**<span data-ttu-id="7ce45-157">CurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce45-157">CurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="7ce45-158">Tout le niveau des utilisateurs d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="7ce45-158">All UE-V user level settings.</span></span> <span data-ttu-id="7ce45-159">Ces entrées remplacent les paramètres de l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ce45-159">These entries override the machine settings for a user.</span></span> <span data-ttu-id="7ce45-160">L’attribut DesiredState peut être</span><span class="sxs-lookup"><span data-stu-id="7ce45-160">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="7ce45-161">**Définir** la valeur sur le registre</span><span class="sxs-lookup"><span data-stu-id="7ce45-161">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="7ce45-162">**Effacer** pour supprimer le paramètre</span><span class="sxs-lookup"><span data-stu-id="7ce45-162">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="7ce45-163">**Non géré** pour que l’élément de configuration reste à l’état actuel</span><span class="sxs-lookup"><span data-stu-id="7ce45-163">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="7ce45-164">Ne pas supprimer les lignes de cette section.</span><span class="sxs-lookup"><span data-stu-id="7ce45-164">Do not remove lines from this section.</span></span> <span data-ttu-id="7ce45-165">Définissez plutôt le DesiredState sur «non géré» si vous ne souhaitez pas que Configuration Manager modifie les valeurs actuelles ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ce45-165">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="services"></a>**<span data-ttu-id="7ce45-166">Services</span><span class="sxs-lookup"><span data-stu-id="7ce45-166">Services</span></span>**  
    <span data-ttu-id="7ce45-167">Entrées de cette opération de service de contrôle de section.</span><span class="sxs-lookup"><span data-stu-id="7ce45-167">Entries in this section control service operation.</span></span> <span data-ttu-id="7ce45-168">Le fichier de configuration par défaut contient une entrée unique pour le UevAgentService.</span><span class="sxs-lookup"><span data-stu-id="7ce45-168">The default configuration file contains a single entry for the UevAgentService.</span></span> <span data-ttu-id="7ce45-169">L’attribut DesiredState peut être défini sur **en cours d’exécution** ou **arrêté**.</span><span class="sxs-lookup"><span data-stu-id="7ce45-169">The DesiredState attribute can be set to **Running** or **Stopped**.</span></span>

    <a href="" id="windows8appscomputerpolicy"></a>**<span data-ttu-id="7ce45-170">Windows8AppsComputerPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce45-170">Windows8AppsComputerPolicy</span></span>**  
    <span data-ttu-id="7ce45-171">Tous les paramètres de synchronisation des applications Windows au niveau machine.</span><span class="sxs-lookup"><span data-stu-id="7ce45-171">All machine level Windows app synchronization settings.</span></span> <span data-ttu-id="7ce45-172">Chaque propriété packagefamilyname répertorié dans cette section peut être affectée à un DesiredState de</span><span class="sxs-lookup"><span data-stu-id="7ce45-172">Each PackageFamilyName listed in this section can be assigned a DesiredState of</span></span>

    -   <span data-ttu-id="7ce45-173">**Activation** de l’itinérance des paramètres</span><span class="sxs-lookup"><span data-stu-id="7ce45-173">**Enabled** to have settings roam</span></span>

    -   <span data-ttu-id="7ce45-174">**Désactivé** pour empêcher les paramètres d’être en itinérance</span><span class="sxs-lookup"><span data-stu-id="7ce45-174">**Disabled** to prevent settings from roaming</span></span>

    -   <span data-ttu-id="7ce45-175">**Compensé** pour que l’entrée ne soit pas supprimée du contrôle UE-V</span><span class="sxs-lookup"><span data-stu-id="7ce45-175">**Cleared** to have the entry removed from UE-V control</span></span>

    <span data-ttu-id="7ce45-176">Des lignes supplémentaires peuvent être ajoutées à cette section en fonction de la liste des applications Windows installées qui peuvent être consultées à l’aide de la cmdlet PowerShell GetAppxPackage.</span><span class="sxs-lookup"><span data-stu-id="7ce45-176">Additional lines can be added to this section based on the list of installed Windows apps that can be viewed using the PowerShell cmdlet GetAppxPackage.</span></span>

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**<span data-ttu-id="7ce45-177">Windows8AppsCurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce45-177">Windows8AppsCurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="7ce45-178">Identique à Windows8AppsComputerPolicy avec des paramètres qui remplacent les paramètres de l’ordinateur d’un utilisateur individuel.</span><span class="sxs-lookup"><span data-stu-id="7ce45-178">Identical to the Windows8AppsComputerPolicy with settings that override machine settings for an individual user.</span></span>

2.  <span data-ttu-id="7ce45-179">Modifiez le fichier de configuration en modifiant les champs état souhaité et valeur.</span><span class="sxs-lookup"><span data-stu-id="7ce45-179">Edit the configuration file by changing the desired state and value fields.</span></span>

3.  <span data-ttu-id="7ce45-180">Exécutez la commande suivante sur un ordinateur exécutant la console d’administration de ConfigMgr:</span><span class="sxs-lookup"><span data-stu-id="7ce45-180">Run this command on a machine running the ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  <span data-ttu-id="7ce45-181">Importer le fichier CAB en utilisant la console ConfigMgr ou l’importation PowerShell-CMConfigurationItem</span><span class="sxs-lookup"><span data-stu-id="7ce45-181">Import the CAB file using ConfigMgr console or PowerShell Import-CMConfigurationItem</span></span>

**<span data-ttu-id="7ce45-182">Mettre à jour un élément de configuration de stratégie UE-V</span><span class="sxs-lookup"><span data-stu-id="7ce45-182">Update a UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="7ce45-183">Modifiez le fichier de configuration en modifiant les champs état souhaité et valeur.</span><span class="sxs-lookup"><span data-stu-id="7ce45-183">Edit the configuration file by changing the desired state and value fields.</span></span>

2.  <span data-ttu-id="7ce45-184">Exécutez la commande à partir de l’étape 3 de [la rubrique créer le premier élément de configuration de stratégie UE-V](#create).</span><span class="sxs-lookup"><span data-stu-id="7ce45-184">Run the command from Step 3 in [Create the First UE-V Policy Configuration Item](#create).</span></span> <span data-ttu-id="7ce45-185">Si vous avez modifié le nom avec le paramètre PolicyName, assurez-vous d’entrer le même nom.</span><span class="sxs-lookup"><span data-stu-id="7ce45-185">If you changed the name with the PolicyName parameter, make sure you enter the same name.</span></span>

3.  <span data-ttu-id="7ce45-186">Réimportez le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="7ce45-186">Reimport the CAB file.</span></span> <span data-ttu-id="7ce45-187">La version de ConfigMgr sera mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7ce45-187">The version in ConfigMgr will be updated.</span></span>

## <span data-ttu-id="7ce45-188">Générer une référence de modèle UE-V</span><span class="sxs-lookup"><span data-stu-id="7ce45-188">Generate a UE-V Template Baseline</span></span>
<span data-ttu-id="7ce45-189">Les modèles UE-V sont distribués à l’aide d’un planning de référence contenant plusieurs éléments de configuration.</span><span class="sxs-lookup"><span data-stu-id="7ce45-189">UE-V templates are distributed using a baseline containing multiple configuration items.</span></span> <span data-ttu-id="7ce45-190">Chaque élément de configuration contient les scripts de découverte et de correction nécessaires à l’installation d’un modèle UE-V.</span><span class="sxs-lookup"><span data-stu-id="7ce45-190">Each configuration item contains the discovery and remediation scripts needed to install one UE-V template.</span></span> <span data-ttu-id="7ce45-191">Le modèle UE-V réel est incorporé dans le script de correction pour la distribution à l’aide de la fonctionnalité standard des éléments de configuration.</span><span class="sxs-lookup"><span data-stu-id="7ce45-191">The actual UE-V template is embedded within the remediation script for distribution using standard Configuration Item functionality.</span></span>

<span data-ttu-id="7ce45-192">Le planning de référence de modèle UE-V est créé à l’aide de l’outil de ligne de commande UevTemplateBaselineGenerator.exe, qui comporte les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="7ce45-192">The UE-V template baseline is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="7ce45-193">Code du site de site &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="7ce45-193">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="7ce45-194">Nom de BaselineName &lt; &gt; (facultatif: par défaut sur «UE-V» planning de référence, le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="7ce45-194">BaselineName &lt;name&gt; (Optional: defaults to “UE-V Template Distribution Baseline” if not present)</span></span>

-   <span data-ttu-id="7ce45-195">&lt;Description &gt; de BaselineDescription (facultatif: une description est fournie en cas de non-présentation)</span><span class="sxs-lookup"><span data-stu-id="7ce45-195">BaselineDescription &lt;description&gt; (Optional: a description is provided if not present)</span></span>

-   <span data-ttu-id="7ce45-196">&lt;Dossier de modèles TemplateFolder UE-V&gt;</span><span class="sxs-lookup"><span data-stu-id="7ce45-196">TemplateFolder &lt;UE-V template folder&gt;</span></span>

-   <span data-ttu-id="7ce45-197">Enregistrer la &lt; liste de fichiers de modèles séparés par des virgules&gt;</span><span class="sxs-lookup"><span data-stu-id="7ce45-197">Register &lt;comma separated template file list&gt;</span></span>

-   <span data-ttu-id="7ce45-198">Annuler l’inscription de la &lt; liste des modèles séparés par des virgules&gt;</span><span class="sxs-lookup"><span data-stu-id="7ce45-198">Unregister &lt;comma separated template list&gt;</span></span>

-   <span data-ttu-id="7ce45-199">CabFilePath &lt; chemin complet du fichier CAB de référence pour générer&gt;</span><span class="sxs-lookup"><span data-stu-id="7ce45-199">CabFilePath &lt;Full path to baseline CAB file to generate&gt;</span></span>

<span data-ttu-id="7ce45-200">Le résultat est un fichier CAB de référence qui est prêt à être importé dans Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7ce45-200">The result is a baseline CAB file that is ready for import into Configuration Manager.</span></span> <span data-ttu-id="7ce45-201">S’il s’agit d’une date ultérieure, vous pouvez mettre à jour ou ajouter un modèle, vous pouvez relancer la commande en utilisant le même nom de référence.</span><span class="sxs-lookup"><span data-stu-id="7ce45-201">If at a future date, you update or add a template, you can rerun the command using the same baseline name.</span></span> <span data-ttu-id="7ce45-202">L’importation des résultats du fichier CAB dans les mises à jour de la version CI sur les modèles modifiés.</span><span class="sxs-lookup"><span data-stu-id="7ce45-202">Importing the CAB results in CI version updates on the changed templates.</span></span>

### <a href="" id="create2"></a><span data-ttu-id="7ce45-203">Créer la première référence de modèle UE-V</span><span class="sxs-lookup"><span data-stu-id="7ce45-203">Create the First UE-V Template Baseline</span></span>

1.  <span data-ttu-id="7ce45-204">Créez un ensemble «maître» de modèles UE-V dans un emplacement de dossier stable visible pour l’ordinateur exécutant votre console d’administration ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="7ce45-204">Create a “master” set of UE-V templates in a stable folder location visible to the machine running your ConfigMgr Admin Console.</span></span> <span data-ttu-id="7ce45-205">À mesure que les modèles sont ajoutés ou mis à jour, il s’agit de ceux qui sont extraits pour distribution.</span><span class="sxs-lookup"><span data-stu-id="7ce45-205">As templates are added or updated, this folder is where they are pulled for distribution.</span></span> <span data-ttu-id="7ce45-206">La liste initiale des modèles peut être copiée à partir d’un ordinateur sur lequel est installé UE-V.</span><span class="sxs-lookup"><span data-stu-id="7ce45-206">The initial list of templates can be copied from a machine with UE-V installed.</span></span> <span data-ttu-id="7ce45-207">L’emplacement du modèle par défaut est C:\\Program Files\\Microsoft user interface Virtualization\\Templates.</span><span class="sxs-lookup"><span data-stu-id="7ce45-207">The default template location is C:\\Program Files\\Microsoft User Experience Virtualization\\Templates.</span></span>

2.  <span data-ttu-id="7ce45-208">Créez un fichier text.bat dans lequel vous pouvez ajouter la commande de générateur de modèles.</span><span class="sxs-lookup"><span data-stu-id="7ce45-208">Create a text.bat file where you can add the template generator command.</span></span> <span data-ttu-id="7ce45-209">Ce paramètre est facultatif, mais il est plus simple à régénérer si vous enregistrez les paramètres de commande.</span><span class="sxs-lookup"><span data-stu-id="7ce45-209">This is optional, but will make regeneration simpler if you save the command parameters.</span></span>

3.  <span data-ttu-id="7ce45-210">Ajoutez la commande et des paramètres au fichier. bat qui générera le planning de référence.</span><span class="sxs-lookup"><span data-stu-id="7ce45-210">Add the command and parameters to the .bat file that will generate the baseline.</span></span> <span data-ttu-id="7ce45-211">L’exemple suivant crée un planning de référence qui répartit le bloc-notes et la calculatrice:</span><span class="sxs-lookup"><span data-stu-id="7ce45-211">The following example creates a baseline that distributes Notepad and Calculator:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  <span data-ttu-id="7ce45-212">Exécutez le fichier. bat pour créer UevTemplateBaseline.cab prêtes à être importées dans Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7ce45-212">Run the .bat file to create UevTemplateBaseline.cab ready for import into Configuration Manager.</span></span>

### <span data-ttu-id="7ce45-213">Mise à jour d’une référence de modèle UE-V</span><span class="sxs-lookup"><span data-stu-id="7ce45-213">Update a UE-V Template Baseline</span></span>

<span data-ttu-id="7ce45-214">Le générateur de modèles utilise la version du modèle pour déterminer si un modèle doit être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7ce45-214">The template generator uses the template version to determine if a template should be updated.</span></span> <span data-ttu-id="7ce45-215">Si vous effectuez un changement de modèle et mettez à jour la version, le générateur de ligne de base compare le modèle dans votre dossier principal avec le modèle contenu dans l’article CI du serveur ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="7ce45-215">If you make a template change and update the version, the baseline generator compares the template in your master folder with the template contained in the CI on the ConfigMgr server.</span></span> <span data-ttu-id="7ce45-216">S’il existe une différence, les versions de référence CI de base et de la base de référence générées sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7ce45-216">If a difference is found, the generated baseline and modified CI versions are updated.</span></span>

<span data-ttu-id="7ce45-217">Pour distribuer un nouveau modèle de bloc-notes, vous devez effectuer les étapes suivantes:</span><span class="sxs-lookup"><span data-stu-id="7ce45-217">To distribute a new Notepad template, you would perform these steps:</span></span>

1.  <span data-ttu-id="7ce45-218">Mettez à jour le modèle et la version du modèle figurant dans l' &lt; &gt; élément version du modèle.</span><span class="sxs-lookup"><span data-stu-id="7ce45-218">Update the template and template version located in the &lt;Version&gt; element of the template.</span></span>

2.  <span data-ttu-id="7ce45-219">Copiez le modèle dans votre répertoire de modèle maître.</span><span class="sxs-lookup"><span data-stu-id="7ce45-219">Copy the template to your master template directory.</span></span>

3.  <span data-ttu-id="7ce45-220">Exécutez la commande dans le fichier. bat que vous avez créé à l’étape 3 de [la rubrique créer le premier Planning UE-V de modèle](#create2).</span><span class="sxs-lookup"><span data-stu-id="7ce45-220">Run the command in the .bat file that you created in Step 3 in [Create the First UE-V Template Baseline](#create2).</span></span>

4.  <span data-ttu-id="7ce45-221">Importez le fichier CAB généré dans ConfigMgr à l’aide de la console ou de PowerShell Import-CMBaseline.</span><span class="sxs-lookup"><span data-stu-id="7ce45-221">Import the generated CAB file into ConfigMgr using the console or PowerShell Import-CMBaseline.</span></span>

## <span data-ttu-id="7ce45-222">Télécharger le Pack de configuration pour UE-V</span><span class="sxs-lookup"><span data-stu-id="7ce45-222">Get the UE-V Configuration Pack</span></span>


<span data-ttu-id="7ce45-223">Le module de configuration d’UE-V pour configurations Manager 2012 SP1 ou version ultérieure peut être téléchargé [ici](https://go.microsoft.com/fwlink/?LinkId=317263).</span><span class="sxs-lookup"><span data-stu-id="7ce45-223">The UE-V Configuration Pack for Configuration Manager 2012 SP1 or later can be downloaded [here](https://go.microsoft.com/fwlink/?LinkId=317263).</span></span>






## <span data-ttu-id="7ce45-224">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ce45-224">Related topics</span></span>


[<span data-ttu-id="7ce45-225">Gérer les configurations pour UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="7ce45-225">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 






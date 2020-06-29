---
title: Modification de la fréquence des tâches planifiées UE-V 2. x
description: Modification de la fréquence des tâches planifiées UE-V 2. x
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810548"
---
# <span data-ttu-id="a82c5-103">Modification de la fréquence des tâches planifiées UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="a82c5-103">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>


<span data-ttu-id="a82c5-104">Le programme d’installation de Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1 agent, AgentSetup.exe, crée les tâches planifiées suivantes lors de l’installation d’UE-V agent:</span><span class="sxs-lookup"><span data-stu-id="a82c5-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 Agent installer, AgentSetup.exe, creates the following scheduled tasks during the UE-V Agent installation:</span></span>

-   **<span data-ttu-id="a82c5-105">Surveiller les paramètres de l’application</span><span class="sxs-lookup"><span data-stu-id="a82c5-105">Monitor Application Settings</span></span>**

-   **<span data-ttu-id="a82c5-106">Application de contrôleur de synchronisation</span><span class="sxs-lookup"><span data-stu-id="a82c5-106">Sync Controller Application</span></span>**

-   **<span data-ttu-id="a82c5-107">Synchroniser les paramètres lors de la fermeture de session</span><span class="sxs-lookup"><span data-stu-id="a82c5-107">Synchronize Settings at Logoff</span></span>**

-   **<span data-ttu-id="a82c5-108">Mise à jour automatique de modèle</span><span class="sxs-lookup"><span data-stu-id="a82c5-108">Template Auto Update</span></span>**

-   **<span data-ttu-id="a82c5-109">Collecter les données du programme d’amélioration du produit</span><span class="sxs-lookup"><span data-stu-id="a82c5-109">Collect CEIP data</span></span>**

-   **<span data-ttu-id="a82c5-110">Télécharger les données du programme d’amélioration du produit</span><span class="sxs-lookup"><span data-stu-id="a82c5-110">Upload CEIP Data</span></span>**

<span data-ttu-id="a82c5-111">**Remarques**  À l’exception de la collecte des données du programme d’amélioration du produit, les tâches suivantes doivent rester activées car UE-V ne peut pas fonctionner sans eux.</span><span class="sxs-lookup"><span data-stu-id="a82c5-111">**Note** With the exception of Collect CEIP Data, these tasks must remain enabled as UE-V cannot function without them.</span></span>

 

<span data-ttu-id="a82c5-112">Ces tâches planifiées ne peuvent pas être configurées avec les outils UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-112">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="a82c5-113">Les administrateurs désireux de modifier la tâche planifiée pour ces éléments peuvent créer un script qui utilise les options de la ligne de commande Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="a82c5-113">Administrators who want to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="a82c5-114">Pour plus d’informations sur les Schtasks.exe, voir [utilisation de schtasks, exe pour planifier des tâches dans Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="a82c5-114">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

<span data-ttu-id="a82c5-115">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="a82c5-115">For more information about</span></span>

## <span data-ttu-id="a82c5-116">Tâches planifiées UE-V</span><span class="sxs-lookup"><span data-stu-id="a82c5-116">UE-V Scheduled Tasks</span></span>


<span data-ttu-id="a82c5-117">Les tâches planifiées suivantes sont incluses dans UE-V 2 avec des exemples de commandes de configuration de tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="a82c5-117">The following scheduled tasks are included in UE-V 2 with sample scheduled task configuration commands.</span></span>

### <span data-ttu-id="a82c5-118">Collecter les données du programme d’amélioration du produit</span><span class="sxs-lookup"><span data-stu-id="a82c5-118">Collect CEIP Data</span></span>

<span data-ttu-id="a82c5-119">Si, à l’issue de l’installation, l’utilisateur ou l’administrateur a choisi de participer au programme d’amélioration du produit (CEIP), UE-V collecte des données afin d’améliorer le produit dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a82c5-119">If upon installation the user or administrator choses to participate in the Customer Experience Improvement Program (CEIP), UE-V collects data to help improve the product in future releases.</span></span> <span data-ttu-id="a82c5-120">Cette tâche planifiée ne s’exécute qu’à l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="a82c5-120">This scheduled task only runs at logon.</span></span> <span data-ttu-id="a82c5-121">La tâche recueillir les données du programme d' **amélioration du produit** exécute le UevSqmSession.exe figurant dans le répertoire d’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-121">The **Collect CEIP Data** task runs the UevSqmSession.exe, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a82c5-122">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="a82c5-122">Task name</span></span></th>
<th align="left"><span data-ttu-id="a82c5-123">Événement par défaut</span><span class="sxs-lookup"><span data-stu-id="a82c5-123">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a82c5-124">\Microsoft\UE-V\Collect les données du programme d’amélioration du produit</span><span class="sxs-lookup"><span data-stu-id="a82c5-124">\Microsoft\UE-V\Collect CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-125">Accès</span><span class="sxs-lookup"><span data-stu-id="a82c5-125">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a82c5-126">Surveiller les paramètres de l’application</span><span class="sxs-lookup"><span data-stu-id="a82c5-126">Monitor Application Settings</span></span>

<span data-ttu-id="a82c5-127">La tâche **surveiller les paramètres d’application** permet de synchroniser les paramètres des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="a82c5-127">The **Monitor Application Settings** task is used to synchronize settings for Windows apps.</span></span> <span data-ttu-id="a82c5-128">Elle est exécutée lors de la connexion, mais elle est retardée de 30 secondes sans répercussions sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="a82c5-128">It is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span> <span data-ttu-id="a82c5-129">La tâche surveiller l’état de l’application exécute le fichier UevAppMonitor.exe qui se trouve dans le répertoire d’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-129">The Monitor Application Status task runs the UevAppMonitor.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a82c5-130">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="a82c5-130">Task name</span></span></th>
<th align="left"><span data-ttu-id="a82c5-131">Événement par défaut</span><span class="sxs-lookup"><span data-stu-id="a82c5-131">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a82c5-132">État de l’application \Microsoft\UE-V\Monitor</span><span class="sxs-lookup"><span data-stu-id="a82c5-132">\Microsoft\UE-V\Monitor Application Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-133">Accès</span><span class="sxs-lookup"><span data-stu-id="a82c5-133">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a82c5-134">Application de contrôleur de synchronisation</span><span class="sxs-lookup"><span data-stu-id="a82c5-134">Sync Controller Application</span></span>

<span data-ttu-id="a82c5-135">La tâche de l' **application du contrôleur de synchronisation** est utilisée pour démarrer le contrôleur de synchronisation afin de synchroniser les paramètres de l’ordinateur vers l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="a82c5-135">The **Sync Controller Application** task is used to start the Sync Controller to synchronize settings from the computer to the settings storage location.</span></span> <span data-ttu-id="a82c5-136">Par défaut, la tâche est exécutée toutes les 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="a82c5-136">By default, the task runs every 30 minutes.</span></span> <span data-ttu-id="a82c5-137">À ce moment, les paramètres locaux sont synchronisés avec l’emplacement de stockage des paramètres, et les paramètres mis à jour à l’emplacement de stockage des paramètres sont synchronisés avec l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a82c5-137">At that time, local settings are synchronized to the settings storage location, and updated settings on the settings storage location are synchronized to the computer.</span></span> <span data-ttu-id="a82c5-138">L’application de contrôleur de synchronisation exécute le Microsoft.Uev.SyncController.exe qui se trouve dans le répertoire d’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-138">The Sync Controller application runs the Microsoft.Uev.SyncController.exe, which is located in the UE-V Agent installation directory.</span></span>
<span data-ttu-id="a82c5-139">**Remarque:** Comme pour la tâche **surveiller les paramètres** de l’application, cette tâche est exécutée lors de la connexion, mais elle est retardée de 30 secondes sans affecter la connexion.</span><span class="sxs-lookup"><span data-stu-id="a82c5-139">**Note:** As per the **Monitor Application Settings** task, this task is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a82c5-140">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="a82c5-140">Task name</span></span></th>
<th align="left"><span data-ttu-id="a82c5-141">Événement par défaut</span><span class="sxs-lookup"><span data-stu-id="a82c5-141">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a82c5-142">Application de contrôleur \Microsoft\UE-V\Sync</span><span class="sxs-lookup"><span data-stu-id="a82c5-142">\Microsoft\UE-V\Sync Controller Application</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-143">Connexion et toutes les 30 minutes</span><span class="sxs-lookup"><span data-stu-id="a82c5-143">Logon, and every 30 minutes thereafter</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a82c5-144">Par exemple, la commande suivante configure l’agent pour synchroniser les paramètres toutes les 15 minutes au lieu des 30 minutes par défaut.</span><span class="sxs-lookup"><span data-stu-id="a82c5-144">For example, the following command configures the agent to synchronize settings every 15 minutes instead of the default 30 minutes.</span></span>

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### <span data-ttu-id="a82c5-145">Synchroniser les paramètres lors de la fermeture de session</span><span class="sxs-lookup"><span data-stu-id="a82c5-145">Synchronize Settings at Logoff</span></span>

<span data-ttu-id="a82c5-146">La tâche **synchroniser les paramètres lors de la déconnexion** est utilisée pour démarrer une application lors de l’ouverture de session qui contrôle la synchronisation des applications lors de la fermeture de session pour UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-146">The **Synchronize Settings at Logoff** task is used to start an application at logon that controls the synchronization of applications at logoff for UE-V.</span></span> <span data-ttu-id="a82c5-147">La tâche synchroniser les paramètres lors de la déconnexion exécute le fichier Microsoft.Uev.SyncController.exe situé dans le répertoire d’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-147">The Synchronize Settings at Logoff task runs the Microsoft.Uev.SyncController.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a82c5-148">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="a82c5-148">Task name</span></span></th>
<th align="left"><span data-ttu-id="a82c5-149">Événement par défaut</span><span class="sxs-lookup"><span data-stu-id="a82c5-149">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a82c5-150">Paramètres \Microsoft\UE-V\Synchronize à la fermeture de session</span><span class="sxs-lookup"><span data-stu-id="a82c5-150">\Microsoft\UE-V\Synchronize Settings at Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-151">Accès</span><span class="sxs-lookup"><span data-stu-id="a82c5-151">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a82c5-152">Mise à jour automatique de modèle</span><span class="sxs-lookup"><span data-stu-id="a82c5-152">Template Auto Update</span></span>

<span data-ttu-id="a82c5-153">La tâche de **mise à jour automatique de modèle** vérifie dans le catalogue de modèles de paramètres les modèles nouveaux, mis à jour ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="a82c5-153">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="a82c5-154">Cette tâche s’exécute uniquement si la SettingsTemplateCatalog est configurée.</span><span class="sxs-lookup"><span data-stu-id="a82c5-154">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="a82c5-155">La tâche de **mise à jour automatique du modèle** exécute le fichier ApplySettingsCatalog.exe situé dans le répertoire d’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-155">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a82c5-156">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="a82c5-156">Task name</span></span></th>
<th align="left"><span data-ttu-id="a82c5-157">Événement par défaut</span><span class="sxs-lookup"><span data-stu-id="a82c5-157">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a82c5-158">Mise à jour automatique \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="a82c5-158">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-159">Démarrage système et à 3:30 AM tous les jours, à une heure aléatoire au sein d’une fenêtre d’une heure</span><span class="sxs-lookup"><span data-stu-id="a82c5-159">System startup and at 3:30 AM every day, at a random time within a 1-hour window</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a82c5-160">**Par exemple:** La commande suivante configure l’agent UE-V pour vérifier le magasin de catalogues de modèles de paramètres chaque heure.</span><span class="sxs-lookup"><span data-stu-id="a82c5-160">**Example:** The following command configures the UE-V Agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### <span data-ttu-id="a82c5-161">Télécharger les données du programme d’amélioration du produit</span><span class="sxs-lookup"><span data-stu-id="a82c5-161">Upload CEIP Data</span></span>

<span data-ttu-id="a82c5-162">La tâche **Télécharger les données** du programme d’amélioration du produit s’exécute pendant l’installation si l’utilisateur ou l’administrateur a choisi de participer au programme d’amélioration du produit (CEIP).</span><span class="sxs-lookup"><span data-stu-id="a82c5-162">The **Upload CEIP Data** task runs during the installation if the user or the administrator chose to participate in the Customer Experience Improvement Program (CEIP).</span></span> <span data-ttu-id="a82c5-163">Cette tâche télécharge les données sur les serveurs du programme d’amélioration du produit dans lesquels les données sont utilisées pour améliorer le produit des futures versions d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-163">This task uploads the data to the CEIP servers where the data is used to help improve the product for future releases of UE-V.</span></span> <span data-ttu-id="a82c5-164">Cette tâche planifiée s’exécute à l’ouverture de session et toutes les 4 heures par la suite.</span><span class="sxs-lookup"><span data-stu-id="a82c5-164">This scheduled task runs at logon and every 4 hours afterwards.</span></span> <span data-ttu-id="a82c5-165">La tâche Télécharger les données du programme d' **amélioration du produit** exécute le fichier UevSqmUploader.exe situé dans le répertoire d’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-165">The **Upload CEIP data** task runs the UevSqmUploader.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a82c5-166">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="a82c5-166">Task name</span></span></th>
<th align="left"><span data-ttu-id="a82c5-167">Événement par défaut</span><span class="sxs-lookup"><span data-stu-id="a82c5-167">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a82c5-168">\Microsoft\UE-V\Upload les données du programme d’amélioration du produit</span><span class="sxs-lookup"><span data-stu-id="a82c5-168">\Microsoft\UE-V\Upload CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-169">Lors de l’ouverture de session et toutes les 4 heures</span><span class="sxs-lookup"><span data-stu-id="a82c5-169">At logon and every 4 hours</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a82c5-170">UE-V 2-détails de la tâche planifiée</span><span class="sxs-lookup"><span data-stu-id="a82c5-170">UE-V 2 Scheduled Task Details</span></span>


<span data-ttu-id="a82c5-171">Le tableau suivant fournit des informations supplémentaires sur les tâches planifiées pour UE-V 2:</span><span class="sxs-lookup"><span data-stu-id="a82c5-171">The following chart provides additional information about scheduled tasks for UE-V 2:</span></span>

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
<td align="left"><p><strong><span data-ttu-id="a82c5-172">Nom de la tâche </strong> (nom du fichier)</span><span class="sxs-lookup"><span data-stu-id="a82c5-172">Task Name</strong> (file name)</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a82c5-173">Fréquence par défaut</span><span class="sxs-lookup"><span data-stu-id="a82c5-173">Default Frequency</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a82c5-174">Bascule d’alimentation</span><span class="sxs-lookup"><span data-stu-id="a82c5-174">Power Toggle</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a82c5-175">Inactif uniquement</span><span class="sxs-lookup"><span data-stu-id="a82c5-175">Idle Only</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a82c5-176">Connexion réseau</span><span class="sxs-lookup"><span data-stu-id="a82c5-176">Network Connection</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a82c5-177">Description</span><span class="sxs-lookup"><span data-stu-id="a82c5-177">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a82c5-178">Surveiller les paramètres </strong> de l’application (UevAppMonitor.exe)</span><span class="sxs-lookup"><span data-stu-id="a82c5-178">Monitor Application Settings</strong> (UevAppMonitor.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-179">Démarre 30 secondes après l’ouverture de session et continue jusqu’à la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="a82c5-179">Starts 30 seconds after logon and continues until logoff.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-180">Non</span><span class="sxs-lookup"><span data-stu-id="a82c5-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-181">Oui</span><span class="sxs-lookup"><span data-stu-id="a82c5-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-182">N/A</span><span class="sxs-lookup"><span data-stu-id="a82c5-182">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-183">Synchronise les paramètres des applications Windows (AppX).</span><span class="sxs-lookup"><span data-stu-id="a82c5-183">Synchronizes settings for Windows (AppX) apps.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a82c5-184">Application de contrôleur </strong> de synchronisation (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="a82c5-184">Sync Controller Application</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-185">À l’ouverture de session et toutes les 30 minutes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a82c5-185">At logon and every 30 min thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-186">Oui</span><span class="sxs-lookup"><span data-stu-id="a82c5-186">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-187">Oui</span><span class="sxs-lookup"><span data-stu-id="a82c5-187">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-188">Uniquement si le réseau est connecté</span><span class="sxs-lookup"><span data-stu-id="a82c5-188">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-189">Démarre le contrôleur de synchronisation qui synchronise les paramètres locaux avec l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="a82c5-189">Starts the Sync Controller which synchronizes local settings with the settings storage location.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a82c5-190">Synchroniser les paramètres lors de la fermeture </strong> de session (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="a82c5-190">Synchronize Settings at Logoff</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-191">S’exécute à l’ouverture de session, puis attend la fin de la synchronisation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="a82c5-191">Runs at logon and then waits for Logoff to Synchronize settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-192">Non</span><span class="sxs-lookup"><span data-stu-id="a82c5-192">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-193">Oui</span><span class="sxs-lookup"><span data-stu-id="a82c5-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-194">N/A</span><span class="sxs-lookup"><span data-stu-id="a82c5-194">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-195">Démarrez une application lors de l’ouverture de session qui contrôle la synchronisation des applications lors de la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="a82c5-195">Start an application at logon that controls the synchronization of applications at logoff.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a82c5-196">Mise à jour automatique </strong> de modèle (ApplySettingsCatalog.exe)</span><span class="sxs-lookup"><span data-stu-id="a82c5-196">Template Auto Update</strong> (ApplySettingsCatalog.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-197">S’exécute à l’ouverture de session initiale et à 3:30 AM par jour.</span><span class="sxs-lookup"><span data-stu-id="a82c5-197">Runs at initial logon and at 3:30 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-198">Oui</span><span class="sxs-lookup"><span data-stu-id="a82c5-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-199">Non</span><span class="sxs-lookup"><span data-stu-id="a82c5-199">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-200">N/A</span><span class="sxs-lookup"><span data-stu-id="a82c5-200">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-201">Vérifie si le catalogue de modèles est nouveau, mis à jour ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="a82c5-201">Checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="a82c5-202">Cette tâche s’exécute uniquement si SettingsTemplateCatalog est configuré.</span><span class="sxs-lookup"><span data-stu-id="a82c5-202">This task only runs if SettingsTemplateCatalog is configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a82c5-203">Collecter les données du programme d’amélioration du produit </strong> (UevSqmSession.exe)</span><span class="sxs-lookup"><span data-stu-id="a82c5-203">Collect CEIP data</strong> (UevSqmSession.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-204">Service de lancement d’ouverture de session</span><span class="sxs-lookup"><span data-stu-id="a82c5-204">At logon launches service</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-205">Non</span><span class="sxs-lookup"><span data-stu-id="a82c5-205">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-206">Oui</span><span class="sxs-lookup"><span data-stu-id="a82c5-206">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-207">N/A</span><span class="sxs-lookup"><span data-stu-id="a82c5-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-208">Si l’utilisateur ou l’administrateur décide du programme d’amélioration du produit (CEIP), cette tâche collecte des données qui permettent d’améliorer les versions ultérieures d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="a82c5-208">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task collects data that helps improve UE-V future releases.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a82c5-209">Télécharger les données du programme d’amélioration du produit </strong> (UevSqmUploader.exe)</span><span class="sxs-lookup"><span data-stu-id="a82c5-209">Upload CEIP Data</strong> (UevSqmUploader.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-210">S’exécute à l’ouverture de session et à 4:00 AM par jour.</span><span class="sxs-lookup"><span data-stu-id="a82c5-210">Runs at logon and at 4:00 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-211">Non</span><span class="sxs-lookup"><span data-stu-id="a82c5-211">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-212">Oui</span><span class="sxs-lookup"><span data-stu-id="a82c5-212">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-213">Uniquement si le réseau est connecté</span><span class="sxs-lookup"><span data-stu-id="a82c5-213">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="a82c5-214">Si l’utilisateur ou l’administrateur décide du programme d’amélioration du produit (CEIP), cette tâche télécharge les données vers les serveurs CEIP.</span><span class="sxs-lookup"><span data-stu-id="a82c5-214">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task uploads the data to the CEIP servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="a82c5-215">Légende</span><span class="sxs-lookup"><span data-stu-id="a82c5-215">Legend</span></span>**

-   <span data-ttu-id="a82c5-216">**Bascule d’alimentation** – le planificateur de tâches optimise la consommation d’énergie quand il n’est pas connecté à une alimentation ca.</span><span class="sxs-lookup"><span data-stu-id="a82c5-216">**Power Toggle** – Task Scheduler will optimize power consumption when not connected to AC power.</span></span> <span data-ttu-id="a82c5-217">L’exécution de la tâche risque de ne pas fonctionner si l’ordinateur bascule sur batterie.</span><span class="sxs-lookup"><span data-stu-id="a82c5-217">The task might stop running if the computer switches to battery power.</span></span>

-   <span data-ttu-id="a82c5-218">**Inactif uniquement** : la tâche ne s’exécute pas si l’ordinateur cesse d’être inactif.</span><span class="sxs-lookup"><span data-stu-id="a82c5-218">**Idle Only** – The task will stop running if the computer ceases to be idle.</span></span> <span data-ttu-id="a82c5-219">Par défaut, la tâche ne redémarrera pas lorsque l’ordinateur sera inactif de nouveau.</span><span class="sxs-lookup"><span data-stu-id="a82c5-219">By default the task will not restart when the computer is idle again.</span></span> <span data-ttu-id="a82c5-220">Au lieu de cela, la tâche redémarrera sur le déclencheur de tâche suivant.</span><span class="sxs-lookup"><span data-stu-id="a82c5-220">Instead the task will begin again on the next task trigger.</span></span>

-   <span data-ttu-id="a82c5-221">**Connexion réseau** : les tâches marquées sur «Oui» s’exécutent uniquement si une connexion réseau est disponible sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a82c5-221">**Network Connection** – Tasks marked “Yes” only run if the computer has a network connection available.</span></span> <span data-ttu-id="a82c5-222">Les tâches marquées «N/A» s’exécutent indépendamment de la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="a82c5-222">Tasks marked “N/A” run regardless of network connectivity.</span></span>

### <span data-ttu-id="a82c5-223">Comment gérer les tâches planifiées</span><span class="sxs-lookup"><span data-stu-id="a82c5-223">How to Manage Scheduled Tasks</span></span>

<span data-ttu-id="a82c5-224">Pour rechercher des tâches planifiées, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="a82c5-224">To find Scheduled Tasks, perform the following:</span></span>

1.  <span data-ttu-id="a82c5-225">Ouvrez «planifier les tâches» sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a82c5-225">Open “Schedule Tasks” on the user computer.</span></span>

2.  <span data-ttu-id="a82c5-226">Naviguez jusqu’à: planificateur de tâches- &gt; bibliothèque du planificateur de tâches- &gt; Microsoft- &gt; UE-V</span><span class="sxs-lookup"><span data-stu-id="a82c5-226">Navigate to: Task Scheduler -&gt; Task Scheduler Library -&gt; Microsoft -&gt; UE-V</span></span>

3.  <span data-ttu-id="a82c5-227">Sélectionnez la tâche planifiée que vous voulez gérer et configurer dans le volet Détails.</span><span class="sxs-lookup"><span data-stu-id="a82c5-227">Select the scheduled task you wish to manage and configure in the details pane.</span></span>

### <span data-ttu-id="a82c5-228">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="a82c5-228">Additional information</span></span>

<span data-ttu-id="a82c5-229">Les informations supplémentaires suivantes s’appliquent aux tâches planifiées UE-V:</span><span class="sxs-lookup"><span data-stu-id="a82c5-229">The following additional information applies to UE-V scheduled tasks:</span></span>

-   <span data-ttu-id="a82c5-230">les programmes de séquence de tâches se trouvent dans le dossier d’installation de l’agent UE-V, par `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` défaut.</span><span class="sxs-lookup"><span data-stu-id="a82c5-230">ll task sequence programs are located in the UE-V Agent installation folder, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\`, by default.</span></span>

-   <span data-ttu-id="a82c5-231">La tâche planifiée de l’application du contrôleur de synchronisation est le composant essentiel lorsque UE-V PowerSchool est défini sur "SyncProvider" (UE-V 2 Configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="a82c5-231">The Sync Controller Application Scheduled task is the crucial component when the UE-V SyncMethod is set to “SyncProvider” (UE-V 2 default configuration).</span></span> <span data-ttu-id="a82c5-232">Cette tâche planifiée conserve les SettingsSToragePath synchronisés avec les versions mises en cache localement des fichiers du package de paramètres.</span><span class="sxs-lookup"><span data-stu-id="a82c5-232">This scheduled task keeps the SettingsSToragePath synchronized with the locally cached versions of the settings package files.</span></span> <span data-ttu-id="a82c5-233">Si les utilisateurs se plaignent que les paramètres ne sont pas synchronisés assez souvent, vous pouvez réduire le paramètre de tâche planifiée à 1 minute.</span><span class="sxs-lookup"><span data-stu-id="a82c5-233">If users complain that settings do not synchronize often enough, then you can reduce the scheduled task setting to as little as 1 minute.</span></span><span data-ttu-id="a82c5-234">Vous pouvez également augmenter la valeur par défaut de 30 minutes, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a82c5-234"> You can also increase the 30 min default to a higher amount if necessary.</span></span> <span data-ttu-id="a82c5-235">Si les utilisateurs se plaignent que les paramètres ne sont pas synchronisés assez rapidement lors de l’ouverture de session, vous pouvez supprimer le paramètre de délai pour la tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="a82c5-235">If users complain that settings do not synchronize fast enough on logon, then you can remove the delay setting for the scheduled task.</span></span> <span data-ttu-id="a82c5-236">(Vous pouvez trouver le paramètre de délai dans la boîte de dialogue **modifier le déclencheur** )</span><span class="sxs-lookup"><span data-stu-id="a82c5-236">(You can find the delay setting in the **Edit Trigger** dialogue box)</span></span>

-   <span data-ttu-id="a82c5-237">Vous n’avez pas besoin de désactiver la tâche planifiée de mise à jour automatique de modèle si vous utilisez une autre méthode pour synchroniser les modèles des clients (c’est-à-dire les plannings de référence de la stratégie de groupe ou du gestionnaire de configuration).</span><span class="sxs-lookup"><span data-stu-id="a82c5-237">You do not need to disable the Template Auto Update scheduled task if you use another method to keep the clients’ templates in sync (i.e. Group Policy or Configuration Manager Baselines).</span></span> <span data-ttu-id="a82c5-238">Si la valeur de la propriété SettingsTemplateCatalog n’est pas spécifiée, vous ne parvient pas à UE-V pour vérifier les modèles personnalisés dans le catalogue des paramètres.</span><span class="sxs-lookup"><span data-stu-id="a82c5-238">Leaving the SettingsTemplateCatalog property value blank prevents UE-V from checking the settings catalog for custom templates.</span></span> <span data-ttu-id="a82c5-239">Cette tâche planifiée exécute ApplySettingsCatalog.exe et renverra essentiellement immédiatement.</span><span class="sxs-lookup"><span data-stu-id="a82c5-239">This scheduled task runs ApplySettingsCatalog.exe and will essentially return immediately.</span></span>

-   <span data-ttu-id="a82c5-240">La tâche planifiée des paramètres d’application vous permet de mettre à jour les paramètres de l’application Windows (AppX) en temps réel, en fonction des déclencheurs de paramètres du programme d’application Windows intégrés dans chaque application.</span><span class="sxs-lookup"><span data-stu-id="a82c5-240">The Monitor Application Settings scheduled task will update Windows app (AppX) settings in real time, based on Windows app program setting triggers built into each app.</span></span>






## <span data-ttu-id="a82c5-241">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a82c5-241">Related topics</span></span>


[<span data-ttu-id="a82c5-242">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="a82c5-242">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="a82c5-243">Déployer UE-V 2. x pour des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="a82c5-243">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 






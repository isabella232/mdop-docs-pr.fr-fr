---
title: Modification de la fréquence des tâches planifiées UE-V
description: Modification de la fréquence des tâches planifiées UE-V
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809504"
---
# <span data-ttu-id="80a21-103">Modification de la fréquence des tâches planifiées UE-V</span><span class="sxs-lookup"><span data-stu-id="80a21-103">Changing the Frequency of UE-V Scheduled Tasks</span></span>


<span data-ttu-id="80a21-104">Le programme d’installation de l’agent Microsoft User Interface Virtualization (UE-V), AgentSetup.exe, crée deux tâches planifiées au cours de l’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="80a21-104">The Microsoft User Experience Virtualization (UE-V) Agent installer, AgentSetup.exe, creates two scheduled tasks during the UE-V Agent installation.</span></span> <span data-ttu-id="80a21-105">Les deux tâches sont la tâche de **mise à jour automatique de modèle** et la tâche définir l’état de l' **emplacement de stockage** .</span><span class="sxs-lookup"><span data-stu-id="80a21-105">The two tasks are the **Template Auto Update** task and the **Setting Storage Location Status** task.</span></span> <span data-ttu-id="80a21-106">Ces tâches planifiées ne peuvent pas être configurées avec les outils UE-V.</span><span class="sxs-lookup"><span data-stu-id="80a21-106">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="80a21-107">Les administrateurs désireux de modifier la tâche planifiée pour ces éléments peuvent créer un script qui utilise les options de la ligne de commande Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="80a21-107">Administrators who wish to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="80a21-108">Pour plus d’informations sur les Schtasks.exe, voir [utilisation de schtasks, exe pour planifier des tâches dans Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="80a21-108">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

## <span data-ttu-id="80a21-109">Mise à jour automatique de modèle</span><span class="sxs-lookup"><span data-stu-id="80a21-109">Template Auto-Update</span></span>


<span data-ttu-id="80a21-110">La tâche de **mise à jour automatique de modèle** vérifie dans le catalogue de modèles de paramètres les modèles nouveaux, mis à jour ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="80a21-110">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="80a21-111">Cette tâche s’exécute uniquement si la SettingsTemplateCatalog est configurée.</span><span class="sxs-lookup"><span data-stu-id="80a21-111">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="80a21-112">La tâche de **mise à jour automatique du modèle** exécute le fichier ApplySettingsCatalog.exe situé dans le répertoire d’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="80a21-112">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent install directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80a21-113">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="80a21-113">Task name</span></span></th>
<th align="left"><span data-ttu-id="80a21-114">Déclencheur par défaut</span><span class="sxs-lookup"><span data-stu-id="80a21-114">Default trigger</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80a21-115">Mise à jour automatique \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="80a21-115">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="80a21-116">3:30 AM tous les jours</span><span class="sxs-lookup"><span data-stu-id="80a21-116">3:30 AM every day</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="80a21-117">**Par exemple:** La commande suivante configure l’agent pour vérifier dans le magasin de catalogues de modèles les paramètres chaque heure.</span><span class="sxs-lookup"><span data-stu-id="80a21-117">**Example:** The following command configures the agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## <span data-ttu-id="80a21-118">État de l’emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="80a21-118">Settings Storage Location Status</span></span>


<span data-ttu-id="80a21-119">La tâche définir l’état de l' **emplacement de stockage** effectue les actions suivantes:</span><span class="sxs-lookup"><span data-stu-id="80a21-119">The **Setting Storage Location Status** task performs the following actions:</span></span>

1.  <span data-ttu-id="80a21-120">Vérifie que les dossiers UE-V sont toujours épinglés ou enregistrés à l’aide de la fonctionnalité fichiers en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="80a21-120">Checks to make sure the UE-V folders are still pinned or registered with the offline files feature.</span></span>

2.  <span data-ttu-id="80a21-121">Vérifie si l’emplacement de stockage des paramètres est hors connexion ou en ligne.</span><span class="sxs-lookup"><span data-stu-id="80a21-121">Checks whether the settings storage location is offline or online.</span></span>

3.  <span data-ttu-id="80a21-122">Force une synchronisation à l’intervalle spécifié au lieu de l’intervalle par défaut des fichiers en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="80a21-122">Forces a synchronization on the specified interval instead of the default interval for offline files.</span></span>

4.  <span data-ttu-id="80a21-123">Synchronise les packages de paramètres qui sont configurés pour être prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="80a21-123">Synchronizes any settings packages that are configured to be pre-fetched.</span></span>

5.  <span data-ttu-id="80a21-124">Vérifie si le chemin d’accès du répertoire de base Active Directory a changé.</span><span class="sxs-lookup"><span data-stu-id="80a21-124">Checks if the Active Directory home directory path has changed.</span></span>

6.  <span data-ttu-id="80a21-125">Écrit la configuration de stockage des paramètres actuelle sous l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="80a21-125">Writes the current settings storage configuration under the following location</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="80a21-126">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="80a21-126">Task name</span></span></th>
    <th align="left"><span data-ttu-id="80a21-127">Déclencheur par défaut</span><span class="sxs-lookup"><span data-stu-id="80a21-127">Default trigger</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="80a21-128">État de l’emplacement de stockage \Microsoft\UE-V\Settings</span><span class="sxs-lookup"><span data-stu-id="80a21-128">\Microsoft\UE-V\Settings Storage Location Status</span></span></p></td>
    <td align="left"><p><span data-ttu-id="80a21-129">Lors de la connexion de tout utilisateur, après un déclenchement répété, répéter toutes les 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="80a21-129">At logon of any user – After triggered, repeat every 30 minutes indefinitely.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="80a21-130">**Par exemple:** La commande suivante configure l’agent pour qu’il exécute l’action située au-dessus toutes les heures.</span><span class="sxs-lookup"><span data-stu-id="80a21-130">**Example:** The following command configures the agent to run the action above every hour.</span></span>

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## <span data-ttu-id="80a21-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80a21-131">Related topics</span></span>


[<span data-ttu-id="80a21-132">Administration d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="80a21-132">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="80a21-133">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="80a21-133">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 






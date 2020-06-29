---
title: Gérer la sauvegarde et la restauration d’administration dans UE-V 2. x
description: Gérer la sauvegarde et la restauration d’administration dans UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812324"
---
# <span data-ttu-id="e40d7-103">Gérer la sauvegarde et la restauration d’administration dans UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e40d7-103">Manage Administrative Backup and Restore in UE-V 2.x</span></span>


<span data-ttu-id="e40d7-104">En tant qu’administrateur de Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, vous pouvez restaurer les paramètres d’application et de fenêtre à l’état d’origine.</span><span class="sxs-lookup"><span data-stu-id="e40d7-104">As an administrator of Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you can restore application and Windows settings to their original state.</span></span> <span data-ttu-id="e40d7-105">Dans le cadre de l’ajout d’un nouvel appareil dans UE-V 2,1, vous pouvez également restaurer des paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e40d7-105">And new in UE-V 2.1, you can also restore additional settings when a user adopts a new device.</span></span>

## <span data-ttu-id="e40d7-106">Restaurer les paramètres dans UE-V 2,1 ou UE-V 2,1 SP1 lorsqu’un utilisateur adopte un nouvel appareil</span><span class="sxs-lookup"><span data-stu-id="e40d7-106">Restore Settings in UE-V 2.1 or UE-V 2.1 SP1 when a User Adopts a New Device</span></span>


<span data-ttu-id="e40d7-107">Pour restaurer les paramètres lors de la mise en place d’un nouvel appareil par un utilisateur, vous pouvez placer un modèle d’emplacement des paramètres dans le profil de **sauvegarde** ou d' **itinérance (par défaut)** à l’aide de l’applet de connexion Set-UevTemplateProfile PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e40d7-107">To restore settings when a user adopts a new device, you can put a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="e40d7-108">Cela permet aux paramètres de l’ordinateur de se synchroniser avec le nouvel ordinateur, en plus des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e40d7-108">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="e40d7-109">Les modèles attribués au profil de sauvegarde sont sauvegardés pour cet appareil et configurés sur une base par appareil.</span><span class="sxs-lookup"><span data-stu-id="e40d7-109">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="e40d7-110">Pour sauvegarder les paramètres d’un modèle, utilisez l’applet de commande suivante dans Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e40d7-110">To backup settings for a template, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   <span data-ttu-id="e40d7-111">&lt;TemplateID &gt; est l’ID du modèle UE-V.</span><span class="sxs-lookup"><span data-stu-id="e40d7-111">&lt;TemplateID&gt; is the UE-V Template ID</span></span>

-   <span data-ttu-id="e40d7-112">&lt;la sauvegarde &gt; peut être de type sauvegarde ou itinérance.</span><span class="sxs-lookup"><span data-stu-id="e40d7-112">&lt;backup&gt; can either be Backup or Roaming</span></span>

<span data-ttu-id="e40d7-113">Lorsque vous remplacez l’appareil d’un utilisateur-V, les paramètres sont restaurés automatiquement si le domaine, le nom d’utilisateur et le nom de l’appareil de l’utilisateur correspondent.</span><span class="sxs-lookup"><span data-stu-id="e40d7-113">When replacing a user’s device UE-V automatically restores settings if the user’s domain, username, and device name all match.</span></span> <span data-ttu-id="e40d7-114">Toutes les données synchronisées et toutes les données de sauvegarde sont automatiquement restaurées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e40d7-114">All synchronized and any backup data is restored on the device automatically.</span></span>

<span data-ttu-id="e40d7-115">Vous pouvez également utiliser la nouvelle cmdlet PowerShell, Restore-UevBackup, pour restaurer les paramètres d’un autre appareil.</span><span class="sxs-lookup"><span data-stu-id="e40d7-115">You can also use the new PowerShell cmdlet, Restore-UevBackup, to restore settings from a different device.</span></span> <span data-ttu-id="e40d7-116">Pour cloner les packages de paramètres pour le nouvel appareil, utilisez l’applet de commande suivante dans Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e40d7-116">To clone the settings packages for the new device, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Restore-UevBackup –Machine <MachineName>
```

<span data-ttu-id="e40d7-117">où &lt; nomordinateur &gt; correspond au nom d’ordinateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e40d7-117">where &lt;MachineName&gt; is the computer name of the device.</span></span>

<span data-ttu-id="e40d7-118">Les modèles tels que le modèle Office 2013 qui incluent de nombreuses applications peuvent tous être inclus dans le profil itinérant (par défaut) ou sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="e40d7-118">Templates such as the Office 2013 template that include many applications can either all be included in the roamed (default) or backed up profile.</span></span> <span data-ttu-id="e40d7-119">Chaque application individuelle d’une suite de modèles suit le groupe.</span><span class="sxs-lookup"><span data-stu-id="e40d7-119">Individual apps in a template suite follow the group.</span></span> <span data-ttu-id="e40d7-120">Les modèles de zone de boîte de votre entreprise 2013 incluent des paramètres d’itinérance et de sauvegarde uniquement.</span><span class="sxs-lookup"><span data-stu-id="e40d7-120">Office 2013 in-box templates include both roaming and backup-only settings.</span></span> <span data-ttu-id="e40d7-121">Les paramètres de sauvegarde ne peuvent pas être inclus dans un profil itinérant.</span><span class="sxs-lookup"><span data-stu-id="e40d7-121">Backup-only settings cannot be included in a roaming profile.</span></span>

<span data-ttu-id="e40d7-122">Dans le cadre de la fonctionnalité de sauvegarde/restauration, UE-V a ajouté le **dernier fonctionnement connu (LKG)** aux options permettant de restaurer les paramètres.</span><span class="sxs-lookup"><span data-stu-id="e40d7-122">As part of the Backup/Restore feature, UE-V added **last known good (LKG)** to the options for rolling back to settings.</span></span> <span data-ttu-id="e40d7-123">Dans cette version, vous pouvez restaurer les paramètres d’origine ou les paramètres LKG.</span><span class="sxs-lookup"><span data-stu-id="e40d7-123">In this release, you can roll back to either the original settings or LKG settings.</span></span> <span data-ttu-id="e40d7-124">Les paramètres LKG permettent aux utilisateurs de revenir à un point intermédiaire et stable avant l’État pre-UE-V des paramètres.</span><span class="sxs-lookup"><span data-stu-id="e40d7-124">The LKG settings let users roll back to an intermediate and stable point ahead of the pre-UE-V state of the settings.</span></span>

### <span data-ttu-id="e40d7-125">Sauvegarder et restaurer des modèles avec UE-V</span><span class="sxs-lookup"><span data-stu-id="e40d7-125">How to Backup/Restore Templates with UE-V</span></span>

<span data-ttu-id="e40d7-126">Voici les composants clés de sauvegarde et de restauration de UE-V:</span><span class="sxs-lookup"><span data-stu-id="e40d7-126">These are the key backup and restore components of UE-V:</span></span>

-   <span data-ttu-id="e40d7-127">Profils de modèles</span><span class="sxs-lookup"><span data-stu-id="e40d7-127">Template profiles</span></span>

-   <span data-ttu-id="e40d7-128">Emplacement des packages de paramètres dans le modèle d’emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="e40d7-128">Settings packages location within the Settings Storage Location template</span></span>

-   <span data-ttu-id="e40d7-129">Déclencheur de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="e40d7-129">Backup trigger</span></span>

-   <span data-ttu-id="e40d7-130">Restauration des paramètres</span><span class="sxs-lookup"><span data-stu-id="e40d7-130">How settings are restored</span></span>

**<span data-ttu-id="e40d7-131">Profils de modèles</span><span class="sxs-lookup"><span data-stu-id="e40d7-131">Template Profiles</span></span>**

<span data-ttu-id="e40d7-132">Un profil de modèle UE-V est défini lorsque le modèle est enregistré sur l’appareil ou après l’inscription via l’utilitaire de configuration PowerShell/WMI.</span><span class="sxs-lookup"><span data-stu-id="e40d7-132">A UE-V template profile is defined when the template is registered on the device or post registration through the PowerShell/WMI configuration utility.</span></span> <span data-ttu-id="e40d7-133">Les types de profils sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="e40d7-133">The profile types include:</span></span>

-   <span data-ttu-id="e40d7-134">Itinérance (par défaut)</span><span class="sxs-lookup"><span data-stu-id="e40d7-134">Roaming (default)</span></span>

-   <span data-ttu-id="e40d7-135">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="e40d7-135">Backup</span></span>

-   <span data-ttu-id="e40d7-136">En un coup de passe</span><span class="sxs-lookup"><span data-stu-id="e40d7-136">BackupOnly</span></span>

<span data-ttu-id="e40d7-137">Tous les modèles sont inclus dans le profil d’itinérance s’ils sont enregistrés sauf spécification contraire.</span><span class="sxs-lookup"><span data-stu-id="e40d7-137">All templates are included in the roaming profile when registered unless otherwise specified.</span></span> <span data-ttu-id="e40d7-138">Les modèles suivants permettent de synchroniser les paramètres avec tous les appareils sur lesquels le modèle correspondant a été activé.</span><span class="sxs-lookup"><span data-stu-id="e40d7-138">These templates synchronize settings to all UE-V enabled devices with the corresponding template enabled.</span></span>

<span data-ttu-id="e40d7-139">Les modèles peuvent être ajoutés au profil de sauvegarde avec PowerShell ou WMI à l’aide de l’applet de applet Set-UevTemplateProfile.</span><span class="sxs-lookup"><span data-stu-id="e40d7-139">Templates can be added to the Backup Profile with PowerShell or WMI using the Set-UevTemplateProfile cmdlet.</span></span> <span data-ttu-id="e40d7-140">Les modèles dans le profil de sauvegarde enregistrent ces paramètres vers l’emplacement de stockage des paramètres dans un répertoire de noms d’appareils spécial.</span><span class="sxs-lookup"><span data-stu-id="e40d7-140">Templates in the Backup Profile back up these settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="e40d7-141">Les paramètres spécifiés sont sauvegardés à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="e40d7-141">Specified settings are backed up to this location.</span></span>

<span data-ttu-id="e40d7-142">Les modèles désignés en dernier incluent des paramètres spécifiques à cet appareil qui ne doivent pas être synchronisés, sauf s’ils sont explicitement restaurés.</span><span class="sxs-lookup"><span data-stu-id="e40d7-142">Templates designated BackupOnly include settings specific to that device that should not be synchronized unless explicitly restored.</span></span> <span data-ttu-id="e40d7-143">Ces paramètres sont stockés dans l’emplacement du package de paramètres spécifique à l’appareil, à l’emplacement de stockage des paramètres comme paramètres Backedup.</span><span class="sxs-lookup"><span data-stu-id="e40d7-143">These settings are stored in the same device-specific settings package location on the settings storage location as the Backedup Settings.</span></span> <span data-ttu-id="e40d7-144">Ces modèles ont un identificateur spécial incorporé dans le modèle qui spécifie qu’ils doivent faire partie de ce profil.</span><span class="sxs-lookup"><span data-stu-id="e40d7-144">These templates have a special identifier embedded in the template that specifies they should be part of this profile.</span></span>

**<span data-ttu-id="e40d7-145">Emplacement des packages de paramètres dans le modèle d’emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="e40d7-145">Settings packages location within the Settings Storage Location template</span></span>**

<span data-ttu-id="e40d7-146">Les paramètres de profil itinérant sont stockés dans l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="e40d7-146">Roaming Profile settings are stored on the settings storage location.</span></span> <span data-ttu-id="e40d7-147">Les modèles attribués au registre de sauvegarde ou à l’enregistrement par le biais stockent leurs paramètres dans l’emplacement de stockage des paramètres dans un répertoire de noms d’appareils spécial.</span><span class="sxs-lookup"><span data-stu-id="e40d7-147">Templates assigned to the Backup or the BackupOnly profile store their settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="e40d7-148">Chaque appareil doté de modèles dans ces profils possède son nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e40d7-148">Each device with templates in these profiles has its own device name.</span></span> <span data-ttu-id="e40d7-149">UE-V ne nettoie pas ces annuaires.</span><span class="sxs-lookup"><span data-stu-id="e40d7-149">UE-V does not clean up these directories.</span></span>

**<span data-ttu-id="e40d7-150">Déclencheur de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="e40d7-150">Backup trigger</span></span>**

<span data-ttu-id="e40d7-151">La sauvegarde est déclenchée par les mêmes événements déclenchant une synchronisation UE-V.</span><span class="sxs-lookup"><span data-stu-id="e40d7-151">Backup is triggered by the same events that trigger a UE-V synchronization.</span></span>

**<span data-ttu-id="e40d7-152">Restauration des paramètres</span><span class="sxs-lookup"><span data-stu-id="e40d7-152">How settings are restored</span></span>**

<span data-ttu-id="e40d7-153">La restauration de l’appareil d’un utilisateur restaure les paramètres du modèle actuellement inscrits à partir du dossier de sauvegarde d’un autre appareil, ainsi que tous les paramètres synchronisés vers l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="e40d7-153">Restoring a user’s device restores the currently registered Template’s settings from another device’s backup folder and all synchronized settings to the current machine.</span></span> <span data-ttu-id="e40d7-154">Les paramètres sont restaurés de deux manières:</span><span class="sxs-lookup"><span data-stu-id="e40d7-154">Settings are restored in these two ways:</span></span>

-   **<span data-ttu-id="e40d7-155">Restauration automatique</span><span class="sxs-lookup"><span data-stu-id="e40d7-155">Automatic restore</span></span>**

    <span data-ttu-id="e40d7-156">Si le chemin d’accès, le domaine et le nom de l’ordinateur de l’utilisateur correspondent à l’utilisateur actuel, tous les paramètres de cet utilisateur sont synchronisés, avec uniquement les derniers paramètres appliqués.</span><span class="sxs-lookup"><span data-stu-id="e40d7-156">If the user’s UE-V settings storage path, domain, and Computer name match the current user then all of the settings for that user are synchronized, with only the latest settings applied.</span></span> <span data-ttu-id="e40d7-157">Si un utilisateur ouvre une session sur un nouvel appareil pour la première fois et que ces critères sont remplis, les données de paramètres sont appliquées à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="e40d7-157">If a user logs on to a new device for the first time and these criteria are met, the settings data is applied to that device.</span></span>

    **<span data-ttu-id="e40d7-158">Remarque</span><span class="sxs-lookup"><span data-stu-id="e40d7-158">Note</span></span>**  
    <span data-ttu-id="e40d7-159">Les paramètres d’accessibilité et de bureau Windows requièrent que l’utilisateur se connecte à nouveau pour qu’il s’applique.</span><span class="sxs-lookup"><span data-stu-id="e40d7-159">Accessibility and Windows Desktop settings require the user to re-logon to Windows to be applied.</span></span>



-   **<span data-ttu-id="e40d7-160">Restauration manuelle</span><span class="sxs-lookup"><span data-stu-id="e40d7-160">Manual Restore</span></span>**

    <span data-ttu-id="e40d7-161">Si vous souhaitez aider les utilisateurs en restaurant un appareil lors d’une actualisation, vous pouvez choisir d’utiliser l’applet de passe Restore-UevBackup.</span><span class="sxs-lookup"><span data-stu-id="e40d7-161">If you want to assist users by restoring a device during a refresh, you can choose to use the Restore-UevBackup cmdlet.</span></span> <span data-ttu-id="e40d7-162">Cette commande entraîne le téléchargement des paramètres de l’utilisateur à partir de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="e40d7-162">This command causes the user’s settings to be downloaded from the Settings Storage Location.</span></span>

## <span data-ttu-id="e40d7-163">Rétablir l’état d’origine des paramètres d’application et de fenêtre</span><span class="sxs-lookup"><span data-stu-id="e40d7-163">Restore Application and Windows Settings to Original State</span></span>


<span data-ttu-id="e40d7-164">Les commandes WMI et Windows PowerShell vous permettent de restaurer les paramètres d’application et de Windows aux valeurs de paramètres qui se trouvaient sur l’ordinateur lors du premier démarrage de l’application après l’installation d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="e40d7-164">WMI and Windows PowerShell commands let you restore application and Windows settings to the settings values that were on the computer the first time that the application started after the UE-V Agent was installed.</span></span> <span data-ttu-id="e40d7-165">Cette action de restauration est effectuée en fonction des paramètres par application ou Windows.</span><span class="sxs-lookup"><span data-stu-id="e40d7-165">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="e40d7-166">Les paramètres sont restaurés lors de la prochaine exécution de l’application, ou les paramètres sont restaurés dès que l’utilisateur ouvre une session sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e40d7-166">The settings are restored the next time that the application runs, or the settings are restored when the user logs on to the operating system.</span></span>

**<span data-ttu-id="e40d7-167">Pour restaurer les paramètres d’application et les paramètres Windows avec Windows PowerShell pour UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e40d7-167">To restore application settings and Windows settings with Windows PowerShell for UE-V 2.x</span></span>**

1.  <span data-ttu-id="e40d7-168">Ouvrez la fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e40d7-168">Open the Windows PowerShell window.</span></span>

2.  <span data-ttu-id="e40d7-169">Entrez l’applet de commande Windows PowerShell suivante pour restaurer les paramètres de l’application et les paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="e40d7-169">Enter the following Windows PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="e40d7-170">Cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e40d7-170">Windows PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="e40d7-171">Description</span><span class="sxs-lookup"><span data-stu-id="e40d7-171">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="e40d7-172">Restaure les paramètres utilisateur pour une application ou rétablit un groupe de paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="e40d7-172">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="e40d7-173">Pour restaurer les paramètres d’application et les paramètres Windows avec WMI</span><span class="sxs-lookup"><span data-stu-id="e40d7-173">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="e40d7-174">Ouvrez une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e40d7-174">Open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="e40d7-175">Entrez la commande WMI suivante pour restaurer les paramètres de l’application et les paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="e40d7-175">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="e40d7-176">Commande WMI</span><span class="sxs-lookup"><span data-stu-id="e40d7-176">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="e40d7-177">Description</span><span class="sxs-lookup"><span data-stu-id="e40d7-177">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="e40d7-178">Restaure les paramètres utilisateur pour une application ou rétablit un groupe de paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="e40d7-178">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## <span data-ttu-id="e40d7-179">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e40d7-179">Related topics</span></span>


[<span data-ttu-id="e40d7-180">Administration d’UE-V 2. x avec Windows PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="e40d7-180">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="e40d7-181">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e40d7-181">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)










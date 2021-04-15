---
title: Configuration d'UE-V 2.x avec des objets de stratégie de groupe
description: Configuration d'UE-V 2.x avec des objets de stratégie de groupe
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494059"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a><span data-ttu-id="7cffa-103">Configuration d'UE-V 2.x avec des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7cffa-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="7cffa-104">Certains paramètres de stratégie de groupe Microsoft User Experience Virtualization (UE-V) 2.0, 2.1 et 2.1 SP1 peuvent être définis pour les ordinateurs, et d'autres paramètres de stratégie de groupe pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7cffa-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="7cffa-105">Pour plus d'informations sur l'installation des fichiers ADMX de stratégie de groupe UE-V, voir l'installation des modèles ADMX de stratégie de groupe [UE-V 2.](https://technet.microsoft.com/library/dn458891.aspx#admx)</span><span class="sxs-lookup"><span data-stu-id="7cffa-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="7cffa-106">Les paramètres de stratégie suivants peuvent être configurés pour UE-V.</span><span class="sxs-lookup"><span data-stu-id="7cffa-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="7cffa-107">Paramètres de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7cffa-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7cffa-108">Nom du paramètre de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7cffa-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="7cffa-109">Target</span><span class="sxs-lookup"><span data-stu-id="7cffa-109">Target</span></span></th>
<th align="left"><span data-ttu-id="7cffa-110">Description des paramètres de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7cffa-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="7cffa-111">Options de configuration</span><span class="sxs-lookup"><span data-stu-id="7cffa-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-112">Configurer la méthode sync</span><span class="sxs-lookup"><span data-stu-id="7cffa-112">Configure Sync Method</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-113">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-114">À l'aide de ce paramètre de stratégie de groupe, vous pouvez configurer si User Experience Virtualization (UE-V) utilise la fonctionnalité de fournisseur de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="7cffa-114">By using this Group Policy setting, you can configure whether User Experience Virtualization (UE-V) uses the sync provider feature.</span></span> <span data-ttu-id="7cffa-115">Ce paramètre de stratégie vous permet également d'activer l'apparition d'une notification lorsque l'importation des paramètres utilisateur est retardée.</span><span class="sxs-lookup"><span data-stu-id="7cffa-115">This policy setting also lets you enable a notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-116">Activez ce paramètre pour configurer l'agent UE-V afin de ne pas utiliser le fournisseur de synchronisation ou le moteur de synchronisation externe.</span><span class="sxs-lookup"><span data-stu-id="7cffa-116">Enable this setting to configure the UE-V agent not to use the sync provider, or to use the external synchronization engine.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7cffa-117">Contact IT Link Text</span><span class="sxs-lookup"><span data-stu-id="7cffa-117">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-118">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="7cffa-118">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-119">Ce paramètre de stratégie de groupe spécifie le texte du lien hypertexte de l'URL du contact it dans le Centre de paramètres de l'entreprise.</span><span class="sxs-lookup"><span data-stu-id="7cffa-119">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-120">Si vous activez ce paramètre de stratégie de groupe, le Centre de paramètres d'entreprise affiche le texte spécifié dans le lien vers l'URL du contact it.</span><span class="sxs-lookup"><span data-stu-id="7cffa-120">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-121">Contact IT URL</span><span class="sxs-lookup"><span data-stu-id="7cffa-121">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-122">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="7cffa-122">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-123">Ce paramètre de stratégie de groupe spécifie l'URL du lien Contact IT dans le Centre de paramètres de l'entreprise.</span><span class="sxs-lookup"><span data-stu-id="7cffa-123">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-124">Si vous activez ce paramètre, le Centre de paramètres d’entreprise contacte le texte it vers l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7cffa-124">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="7cffa-125">Le lien peut être de n’importe quel protocole standard, tel que HTTP ou mailto.</span><span class="sxs-lookup"><span data-stu-id="7cffa-125">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7cffa-126">Notification de première utilisation</span><span class="sxs-lookup"><span data-stu-id="7cffa-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-127">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="7cffa-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-128">Ce paramètre de stratégie de groupe active une notification dans la zone de notification qui s’affiche lorsque l’UE-V</span><span class="sxs-lookup"><span data-stu-id="7cffa-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="7cffa-129">s’exécute pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="7cffa-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-130">La valeur par défaut est activée.</span><span class="sxs-lookup"><span data-stu-id="7cffa-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-131">Ping sur l’emplacement de stockage des paramètres avant synchronisation</span><span class="sxs-lookup"><span data-stu-id="7cffa-131">Ping the settings storage location before sync</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-132">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-133">Ce paramètre de stratégie permet à la configuration du fournisseur de synchronisation UE-V d’envoyer un ping sur le chemin de stockage des paramètres avant de tenter de synchroniser les paramètres afin de vérifier la connexion.</span><span class="sxs-lookup"><span data-stu-id="7cffa-133">This policy setting allows configuration of the UE-V sync provider to ping the settings storage path before attempting to sync settings in order to verify the connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-134">Activez ou désactivez ce paramètre de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7cffa-134">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7cffa-135">Seuil d’avertissement de taille de package Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cffa-135">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-136">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-136">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-137">Ce paramètre de stratégie de groupe vous permet de configurer l’agent UE-V pour signaler quand la taille d’un fichier de package de paramètres atteint un seuil défini.</span><span class="sxs-lookup"><span data-stu-id="7cffa-137">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-138">Spécifiez le seuil préféré pour les tailles de package de paramètres en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="7cffa-138">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="7cffa-139">Par défaut, l’agent UE-V n’a pas de seuil de taille de fichier de package.</span><span class="sxs-lookup"><span data-stu-id="7cffa-139">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-140">Chemin de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="7cffa-140">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-141">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-141">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-142">Ce paramètre de stratégie de groupe configure l’endroit où les paramètres utilisateur doivent être stockés.</span><span class="sxs-lookup"><span data-stu-id="7cffa-142">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-143">Entrez un chemin d’accès UNC (Universal Naming Convention) et des variables telles que \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="7cffa-143">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7cffa-144">Chemin d’accès du catalogue de modèles de paramètres</span><span class="sxs-lookup"><span data-stu-id="7cffa-144">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-145">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="7cffa-145">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-146">Ce paramètre de stratégie de groupe configure l’emplacement des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="7cffa-146">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="7cffa-147">Ce paramètre de stratégie configure également si le catalogue doit être utilisé pour remplacer les modèles Microsoft par défaut installés avec l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="7cffa-147">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-148">Entrez un chemin d’accès UNC (Universal Naming Convention) tel que \Server\TemplateShare ou un emplacement de dossier sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7cffa-148">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="7cffa-149">Cochez la case pour remplacer les modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="7cffa-149">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-150">Paramètres de synchronisation sur les connexions à connexions avec des compteurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-150">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-151">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-151">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-152">Ce paramètre de stratégie de groupe définit si UE-V synchronise les paramètres sur les connexions à connexions avec jauge.</span><span class="sxs-lookup"><span data-stu-id="7cffa-152">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-153">Par défaut, l’agent UE-V ne synchronise pas les paramètres sur une connexion à connexion sécurisée.</span><span class="sxs-lookup"><span data-stu-id="7cffa-153">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7cffa-154">Synchroniser les paramètres sur les connexions avec des compteurs, même en itinérance</span><span class="sxs-lookup"><span data-stu-id="7cffa-154">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-155">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-155">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-156">Ce paramètre de stratégie de groupe définit si UE-V synchronise les paramètres sur les connexions à connexions avec des compteurs en dehors du réseau du fournisseur d’accueil, par exemple, lorsque la connexion de données est en mode d’itinérance.</span><span class="sxs-lookup"><span data-stu-id="7cffa-156">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-157">Par défaut, UE-V ne synchronise pas les paramètres sur une connexion avec mesure lorsqu’il est en mode d’itinérance.</span><span class="sxs-lookup"><span data-stu-id="7cffa-157">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-158">Délai d’délai de synchronisation</span><span class="sxs-lookup"><span data-stu-id="7cffa-158">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-159">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-159">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-160">Ce paramètre de stratégie de groupe configure le nombre de millisecondes que l’ordinateur attend avant un délai d’attente lorsqu’il récupère les paramètres utilisateur à partir de l’emplacement des paramètres distants.</span><span class="sxs-lookup"><span data-stu-id="7cffa-160">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="7cffa-161">Si l’emplacement de stockage distant n’est pas disponible et que l’utilisateur n’utilise pas le fournisseur de synchronisation, le démarrage de l’application est retardé de ce nombre de millisecondes.</span><span class="sxs-lookup"><span data-stu-id="7cffa-161">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-162">Spécifiez le délai d’délai de synchronisation préféré en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="7cffa-162">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="7cffa-163">La valeur par défaut est 2 000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="7cffa-163">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7cffa-164">Synchroniser les paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="7cffa-164">Synchronize Windows settings</span></span> </p></td>
<td align="left"><p><span data-ttu-id="7cffa-165">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-165">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-166">Ce paramètre de stratégie de groupe configure la synchronisation des paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="7cffa-166">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-167">Sélectionnez les paramètres Windows synchronisés entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="7cffa-167">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="7cffa-168">Par défaut, les thèmes Windows, les paramètres de bureau et les paramètres d’accessibilité synchronisent les paramètres entre les ordinateurs de la même version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7cffa-168">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-169">Icône Tray</span><span class="sxs-lookup"><span data-stu-id="7cffa-169">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-170">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="7cffa-170">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-171">Ce paramètre de stratégie de groupe active l’icône de bac UE-V.</span><span class="sxs-lookup"><span data-stu-id="7cffa-171">This Group Policy setting enables the UE-V tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-172">La valeur par défaut est activée.</span><span class="sxs-lookup"><span data-stu-id="7cffa-172">The default is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7cffa-173">Utiliser User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="7cffa-173">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-174">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-174">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-175">Ce paramètre de stratégie de groupe vous permet d’activer ou de désactiver UE-V.</span><span class="sxs-lookup"><span data-stu-id="7cffa-175">This Group Policy setting lets you enable or disable UE-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-176">Activez ou désactivez ce paramètre de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7cffa-176">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-177">VDI Configuration</span><span class="sxs-lookup"><span data-stu-id="7cffa-177">VDI Configuration</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-178">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-178">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-179">Ce paramètre de stratégie configure la synchronisation des informations de récupération UE-V pour les ordinateurs qui s’exécutent dans un environnement VDI en pool.</span><span class="sxs-lookup"><span data-stu-id="7cffa-179">This policy setting configures the synchronization of UE-V rollback information for computers running in a pooled VDI environment.</span></span> <span data-ttu-id="7cffa-180">Si cette stratégie est activée, l’état de restauration UE-V est copié sur l’emplacement de stockage des paramètres lors de la connexion et restauré lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="7cffa-180">If this policy is enabled, the UE-V rollback state is copied to the settings storage location on logout and restored on login.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-181">Activez ou désactivez ce paramètre de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7cffa-181">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="7cffa-182">Remarque</span><span class="sxs-lookup"><span data-stu-id="7cffa-182">Note</span></span>**  
<span data-ttu-id="7cffa-183">En outre, les paramètres de stratégie de groupe sont disponibles pour de nombreuses applications de bureau et applications Windows.</span><span class="sxs-lookup"><span data-stu-id="7cffa-183">In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="7cffa-184">Vous pouvez utiliser ces paramètres pour activer ou désactiver la synchronisation des paramètres pour des applications spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7cffa-184">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="7cffa-185">Paramètres de stratégie de groupe Des applications Windows</span><span class="sxs-lookup"><span data-stu-id="7cffa-185">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7cffa-186">Nom du paramètre de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7cffa-186">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="7cffa-187">Target</span><span class="sxs-lookup"><span data-stu-id="7cffa-187">Target</span></span></th>
<th align="left"><span data-ttu-id="7cffa-188">Description des paramètres de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7cffa-188">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="7cffa-189">Options de configuration</span><span class="sxs-lookup"><span data-stu-id="7cffa-189">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-190">Ne pas synchroniser les applications Windows</span><span class="sxs-lookup"><span data-stu-id="7cffa-190">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-191">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7cffa-191">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-192">Ce paramètre de stratégie de groupe définit si l'agent UE-V synchronise les paramètres des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="7cffa-192">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-193">La valeur par défaut consiste à synchroniser les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="7cffa-193">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7cffa-194">Liste des applications Windows</span><span class="sxs-lookup"><span data-stu-id="7cffa-194">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-195">Ordinateur et utilisateur</span><span class="sxs-lookup"><span data-stu-id="7cffa-195">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-196">Ce paramètre répertorie les noms de package de famille des applications Windows et indique expressément si UE-V synchronise les paramètres de cette application.</span><span class="sxs-lookup"><span data-stu-id="7cffa-196">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-197">Vous pouvez utiliser ce paramètre pour spécifier que les paramètres d'une application ne sont jamais synchronisés par UE-V, même si les paramètres de toutes les autres applications Windows sont synchronisés.</span><span class="sxs-lookup"><span data-stu-id="7cffa-197">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7cffa-198">Synchroniser les applications Windows non listées</span><span class="sxs-lookup"><span data-stu-id="7cffa-198">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-199">Ordinateur et utilisateur</span><span class="sxs-lookup"><span data-stu-id="7cffa-199">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-200">Ce paramètre de stratégie de groupe définit le comportement de synchronisation des paramètres par défaut de l'agent UE-V pour les applications Windows qui ne sont pas explicitement répertoriées dans la liste des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="7cffa-200">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7cffa-201">Par défaut, l'agent UE-V synchronise uniquement les paramètres des applications Windows incluses dans la liste des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="7cffa-201">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7cffa-202">Pour plus d'informations sur la synchronisation des applications Windows, voir [Liste des applications Windows.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)</span><span class="sxs-lookup"><span data-stu-id="7cffa-202">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="7cffa-203">Pour configurer les paramètres de stratégie de groupe ciblés par l'ordinateur</span><span class="sxs-lookup"><span data-stu-id="7cffa-203">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="7cffa-204">Utilisez la Console de gestion des stratégies de groupe (GPMC) ou la Gestion avancée des stratégies de groupe (AGPM) sur l'ordinateur qui agit en tant que contrôleur de domaine pour gérer les paramètres de stratégie de groupe pour les ordinateurs UE-V.</span><span class="sxs-lookup"><span data-stu-id="7cffa-204">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="7cffa-205">Accédez **à Configuration ordinateur,** sélectionnez **Stratégies,** sélectionnez Modèles d'administration, cliquez sur **Composants Windows,** puis sélectionnez **Microsoft User Experience Virtualization**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7cffa-205">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="7cffa-206">Sélectionnez le paramètre de stratégie de groupe à modifier.</span><span class="sxs-lookup"><span data-stu-id="7cffa-206">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="7cffa-207">Pour configurer les paramètres de stratégie de groupe ciblés par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="7cffa-207">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="7cffa-208">Utilisez la Console de gestion des stratégies de groupe (GPMC) ou l'outil Gestion avancée des stratégies de groupe (AGPM) dans Microsoft Desktop Optimization Pack (MDOP) sur l'ordinateur du contrôleur de domaine pour gérer les paramètres de stratégie de groupe pour UE-V.</span><span class="sxs-lookup"><span data-stu-id="7cffa-208">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="7cffa-209">Accédez **à configuration utilisateur,** sélectionnez **Stratégies,** sélectionnez Modèles d'administration, cliquez sur **Composants Windows,** puis sélectionnez **Microsoft User Experience Virtualization**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7cffa-209">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="7cffa-210">Sélectionnez le paramètre de stratégie de groupe modifié.</span><span class="sxs-lookup"><span data-stu-id="7cffa-210">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="7cffa-211">L'agent UE-V utilise l'ordre de priorité suivant pour déterminer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="7cffa-211">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="7cffa-212">Ordre de priorité pour les paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="7cffa-212">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="7cffa-213">Paramètres ciblés par l'utilisateur gérés par les paramètres de stratégie de groupe : ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe sous `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="7cffa-213">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="7cffa-214">Paramètres ciblés par l'ordinateur gérés par les paramètres de stratégie de groupe : ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe sous `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="7cffa-214">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="7cffa-215">Paramètres de configuration définis par l'utilisateur actuel à l'aide de Windows PowerShell ou windows management Instrumentation (WMI) : ces paramètres de configuration sont stockés par l'agent UE-V sous cet emplacement de Registre : `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`</span><span class="sxs-lookup"><span data-stu-id="7cffa-215">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="7cffa-216">Paramètres de configuration définis pour l'ordinateur à l'aide de Windows PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="7cffa-216">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="7cffa-217">Ces paramètres de configuration sont stockés par l'agent UE-V sous cet emplacement de Registre `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` :</span><span class="sxs-lookup"><span data-stu-id="7cffa-217">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="7cffa-218">**Vous avez une suggestion pour UE-V**?</span><span class="sxs-lookup"><span data-stu-id="7cffa-218">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="7cffa-219">Ajoutez ou votez sur les suggestions [ici.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)</span><span class="sxs-lookup"><span data-stu-id="7cffa-219">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="7cffa-220">**Vous avez un problème UE-V**?</span><span class="sxs-lookup"><span data-stu-id="7cffa-220">**Got a UE-V issue**?</span></span> <span data-ttu-id="7cffa-221">Utilisez le [forum TechNet UE-V.](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)</span><span class="sxs-lookup"><span data-stu-id="7cffa-221">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cffa-222">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7cffa-222">Related topics</span></span>


[<span data-ttu-id="7cffa-223">Administration d'UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="7cffa-223">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="7cffa-224">Gérer les configurations pour UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="7cffa-224">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 

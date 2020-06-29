---
title: Configuration d’UE-V 2. x avec des objets de stratégie de groupe
description: Configuration d’UE-V 2. x avec des objets de stratégie de groupe
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
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810547"
---
# <span data-ttu-id="8c1cc-103">Configuration d’UE-V 2. x avec des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8c1cc-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="8c1cc-104">Certains paramètres de la stratégie de groupe Microsoft User performance (UE-V) 2,0, 2,1 et 2,1 SP1 peuvent être définis pour les ordinateurs, et les autres paramètres de stratégie de groupe pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="8c1cc-105">Pour plus d’informations sur l’installation des fichiers ADMX de stratégie de groupe UE-v, voir [installation des modèles ADMX de stratégie de groupe UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="8c1cc-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="8c1cc-106">Les paramètres de stratégie suivants peuvent être configurés pour UE-V.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="8c1cc-107">Paramètres de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8c1cc-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1cc-108">Nom du paramètre de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8c1cc-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="8c1cc-109">Target</span><span class="sxs-lookup"><span data-stu-id="8c1cc-109">Target</span></span></th>
<th align="left"><span data-ttu-id="8c1cc-110">Description du paramètre de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8c1cc-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="8c1cc-111">Options de configuration</span><span class="sxs-lookup"><span data-stu-id="8c1cc-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1cc-112">Texte du lien Contactez-le</span><span class="sxs-lookup"><span data-stu-id="8c1cc-112">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-113">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="8c1cc-113">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-114">Ce paramètre de stratégie de groupe spécifie le texte du lien hypertexte d’URL de contact dans le centre de paramètres de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-114">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-115">Si vous activez ce paramètre de stratégie de groupe, le centre de paramètres de la société affiche le texte spécifié dans le lien vers l’URL du contact.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-115">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1cc-116">URL de contact</span><span class="sxs-lookup"><span data-stu-id="8c1cc-116">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-117">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="8c1cc-117">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-118">Ce paramètre de stratégie de groupe spécifie l’URL du lien de contact dans le centre de paramètres de la société.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-118">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-119">Si vous activez ce paramètre, le centre de paramètres de la société adresse le lien vers l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-119">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="8c1cc-120">Le lien peut être de n’importe quel protocole standard, tel que HTTP ou mailto.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-120">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1cc-121">Ne pas utiliser le fournisseur de synchronisation</span><span class="sxs-lookup"><span data-stu-id="8c1cc-121">Do not use the sync provider</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-122">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8c1cc-122">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-123">En utilisant ce paramètre de stratégie de groupe, vous pouvez configurer le fait que UE-V utilise la fonctionnalité du fournisseur de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-123">By using this Group Policy setting, you can configure whether UE-V uses the sync provider feature.</span></span> <span data-ttu-id="8c1cc-124">Ce paramètre de stratégie vous permet également d’activer la notification lorsque l’importation des paramètres utilisateur est retardée.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-124">This policy setting also lets you enable notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-125">Activez ce paramètre pour configurer l’agent UE-V de façon à ce qu’il ne fasse pas appel au fournisseur de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-125">Enable this setting to configure the UE-V Agent not to use the sync provider.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1cc-126">Notification d’utilisation initiale</span><span class="sxs-lookup"><span data-stu-id="8c1cc-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-127">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="8c1cc-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-128">Ce paramètre de stratégie de groupe permet de notifier dans la zone de notification qui s’affiche lorsque UE-V</span><span class="sxs-lookup"><span data-stu-id="8c1cc-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="8c1cc-129">l’agent s’exécute pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-130">La valeur par défaut est activée.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1cc-131">Paramètres des fenêtres itinérantes</span><span class="sxs-lookup"><span data-stu-id="8c1cc-131">Roam Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-132">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8c1cc-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-133">Ce paramètre de stratégie de groupe configure la synchronisation des paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-133">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-134">Sélectionnez les paramètres Windows à synchroniser entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-134">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="8c1cc-135">Par défaut, les thèmes Windows, les paramètres de bureau et les options d’ergonomie synchronisent les paramètres entre les ordinateurs de la même version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-135">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1cc-136">Seuil d’avertissement de taille de package paramètres</span><span class="sxs-lookup"><span data-stu-id="8c1cc-136">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-137">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8c1cc-137">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-138">Ce paramètre de stratégie de groupe vous permet de configurer l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-138">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-139">Spécifiez le seuil préféré pour les tailles de packages de paramètres en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="8c1cc-139">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="8c1cc-140">Par défaut, l’agent UE-V n’a pas de seuil de taille de fichier de package.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-140">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1cc-141">Emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="8c1cc-141">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-142">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8c1cc-142">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-143">Ce paramètre de stratégie de groupe permet de configurer l’emplacement de stockage des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-143">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-144">Entrez le chemin d’accès UNC (Universal Naming Convention) et les variables comme \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-144">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1cc-145">Chemin du catalogue de modèles de paramètres</span><span class="sxs-lookup"><span data-stu-id="8c1cc-145">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-146">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="8c1cc-146">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-147">Ce paramètre de stratégie de groupe permet de configurer l’emplacement de stockage des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-147">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="8c1cc-148">Ce paramètre de stratégie définit également si le catalogue doit être utilisé pour remplacer les modèles Microsoft par défaut installés avec l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-148">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-149">Entrez un chemin d’accès UNC (Universal Naming Convention) tel que \Server\TemplateShare ou un dossier sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-149">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="8c1cc-150">Activez la case à cocher pour remplacer les modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-150">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1cc-151">Paramètres de synchronisation sur les connexions limitées</span><span class="sxs-lookup"><span data-stu-id="8c1cc-151">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-152">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8c1cc-152">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-153">Ce paramètre de stratégie de groupe définit si UE-V synchronise les paramètres de connexions limitées.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-153">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-154">Par défaut, l’agent UE-V ne synchronise pas les paramètres sur une connexion limitée.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-154">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1cc-155">Paramètres de synchronisation sur les connexions limitées, même en cas d’itinérance</span><span class="sxs-lookup"><span data-stu-id="8c1cc-155">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-156">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8c1cc-156">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-157">Ce paramètre de stratégie de groupe définit si UE-V synchronise les paramètres de connexions limitées en dehors du réseau des fournisseurs de réseaux domestiques, par exemple lorsque la connexion de données est en mode itinérant.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-157">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-158">Par défaut, UE-V ne synchronise pas les paramètres sur une connexion limitée lorsqu’il est en mode itinérant.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-158">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1cc-159">Délai d’expiration de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="8c1cc-159">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-160">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8c1cc-160">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-161">Ce paramètre de stratégie de groupe configure le nombre de millisecondes avant qu’il n’expire lors de la récupération des paramètres utilisateur à partir de l’emplacement des paramètres distants.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-161">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="8c1cc-162">Si l’emplacement de stockage à distance n’est pas disponible et que l’utilisateur n’utilise pas le fournisseur de synchronisation, le démarrage de l’application est retardée de ce nombre de millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-162">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-163">Spécifiez le délai d’expiration de la synchronisation par défaut en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-163">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="8c1cc-164">La valeur par défaut est 2000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-164">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1cc-165">Icône de la barre d’état système</span><span class="sxs-lookup"><span data-stu-id="8c1cc-165">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-166">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="8c1cc-166">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-167">Ce paramètre de stratégie de groupe permet de l’icône de la barre d’état utilisateur de la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-167">This Group Policy setting enables the User Experience Virtualization (UE-V) tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-168">La valeur par défaut est activée.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-168">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1cc-169">Utiliser la virtualisation de l’utilisation de l’utilisateur (UE-V)</span><span class="sxs-lookup"><span data-stu-id="8c1cc-169">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-170">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8c1cc-170">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-171">Ce paramètre de stratégie de groupe vous permet d’activer ou de désactiver la virtualisation de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-171">This Group Policy setting lets you enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-172">Activez ou désactivez ce paramètre de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-172">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8c1cc-173">**Remarques**  De plus, les paramètres de stratégie de groupe sont disponibles pour de nombreuses applications de bureau et applications Windows.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-173">**Note** In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="8c1cc-174">Vous pouvez utiliser ces paramètres pour activer ou désactiver la synchronisation des paramètres pour des applications spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-174">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="8c1cc-175">Paramètres de stratégie de groupe des applications Windows</span><span class="sxs-lookup"><span data-stu-id="8c1cc-175">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1cc-176">Nom du paramètre de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8c1cc-176">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="8c1cc-177">Target</span><span class="sxs-lookup"><span data-stu-id="8c1cc-177">Target</span></span></th>
<th align="left"><span data-ttu-id="8c1cc-178">Description du paramètre de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8c1cc-178">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="8c1cc-179">Options de configuration</span><span class="sxs-lookup"><span data-stu-id="8c1cc-179">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1cc-180">Ne pas synchroniser les applications Windows</span><span class="sxs-lookup"><span data-stu-id="8c1cc-180">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-181">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8c1cc-181">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-182">Ce paramètre de stratégie de groupe définit si UE-V agent synchronise les paramètres des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-182">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-183">La valeur par défaut consiste à synchroniser les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-183">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1cc-184">Liste des applications Windows</span><span class="sxs-lookup"><span data-stu-id="8c1cc-184">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-185">Ordinateur et utilisateur</span><span class="sxs-lookup"><span data-stu-id="8c1cc-185">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-186">Ce paramètre dresse la liste des noms de famille de packages des applications Windows et indique expressément si UE-V synchronise les paramètres de l’application.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-186">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-187">Vous pouvez utiliser ce paramètre pour spécifier que les paramètres d’une application ne sont jamais synchronisés par UE-V, même si les paramètres de toutes les autres applications Windows sont synchronisés.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-187">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1cc-188">Synchroniser les applications Windows non répertoriées</span><span class="sxs-lookup"><span data-stu-id="8c1cc-188">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-189">Ordinateur et utilisateur</span><span class="sxs-lookup"><span data-stu-id="8c1cc-189">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-190">Ce paramètre de stratégie de groupe définit le comportement de synchronisation des paramètres par défaut de l’agent UE-V pour les applications Windows qui ne figurent pas explicitement dans la liste des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-190">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1cc-191">Par défaut, l’agent UE-V synchronise uniquement les paramètres des applications Windows qui sont incluses dans la liste des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-191">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8c1cc-192">Pour plus d’informations sur la synchronisation des applications Windows, voir [liste des applications Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="8c1cc-192">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="8c1cc-193">Pour configurer les paramètres de stratégie de groupe ciblés par l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="8c1cc-193">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="8c1cc-194">Utilisez la console de gestion des stratégies de groupe (GPMC) ou la gestion avancée des stratégies de groupe (AGPM) sur l’ordinateur qui sert de contrôleur de domaine pour gérer les paramètres de stratégie de groupe pour les ordinateurs UE-V.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-194">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="8c1cc-195">Accédez à **Configuration ordinateur**, sélectionnez **stratégies**, **modèles d’administration**, cliquez sur **composants Windows**, puis sélectionnez **virtualisation**de l’utilisation de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-195">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="8c1cc-196">Sélectionnez le paramètre de stratégie de groupe que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-196">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="8c1cc-197">Pour configurer les paramètres de stratégie de groupe ciblés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="8c1cc-197">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="8c1cc-198">Utilisez la console de gestion des stratégies de groupe (GPMC) ou l’outil de gestion des stratégies de groupe (AGPM) dans Microsoft Desktop Optimization Pack (MDOP) sur l’ordinateur contrôleur de domaine pour gérer les paramètres de stratégie de groupe pour UE-V.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-198">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="8c1cc-199">Accédez à **Configuration utilisateur**, sélectionnez **stratégies**, sélectionnez **modèles d’administration**, cliquez sur **composants Windows**, puis sélectionnez virtualisation de l' **utilisation de Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-199">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="8c1cc-200">Sélectionnez le paramètre de stratégie de groupe modifié.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-200">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="8c1cc-201">L’agent UE-V utilise l’ordre de priorité suivant pour déterminer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-201">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="8c1cc-202">Ordre de priorité pour les paramètres d’UE-V</span><span class="sxs-lookup"><span data-stu-id="8c1cc-202">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="8c1cc-203">Paramètres ciblés par l’utilisateur, gérés par des paramètres de stratégie de groupe, ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="8c1cc-203">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="8c1cc-204">Paramètres ciblés par ordinateur gérés par des paramètres de stratégie de groupe: ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="8c1cc-204">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="8c1cc-205">Paramètres de configuration définis par l’utilisateur actuel à l’aide de Windows PowerShell ou de Windows Management Instrumentation (WMI)-ces paramètres de configuration sont stockés par l’agent UE-V sous cet emplacement du Registre: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="8c1cc-205">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="8c1cc-206">Paramètres de configuration définis pour l’ordinateur à l’aide de Windows PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="8c1cc-206">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="8c1cc-207">Ces paramètres de configuration sont stockés par l’agent UE-V sous cet emplacement du Registre: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="8c1cc-207">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="8c1cc-208">Vous **avez une suggestion pour UE-V**?</span><span class="sxs-lookup"><span data-stu-id="8c1cc-208">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="8c1cc-209">Ajoutez ou Votez en fonction [de suggestions.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)</span><span class="sxs-lookup"><span data-stu-id="8c1cc-209">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="8c1cc-210">Vous **avez un problème UE-V**?</span><span class="sxs-lookup"><span data-stu-id="8c1cc-210">**Got a UE-V issue**?</span></span> <span data-ttu-id="8c1cc-211">Utiliser le [Forum de TechNet UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="8c1cc-211">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="8c1cc-212">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c1cc-212">Related topics</span></span>


[<span data-ttu-id="8c1cc-213">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="8c1cc-213">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="8c1cc-214">Gérer les configurations pour UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="8c1cc-214">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 






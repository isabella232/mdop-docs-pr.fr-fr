---
title: Configuration d’UE-V avec les objets de stratégie de groupe
description: Configuration d’UE-V avec les objets de stratégie de groupe
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811910"
---
# <span data-ttu-id="a3e10-103">Configuration d’UE-V avec les objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a3e10-103">Configuring UE-V with Group Policy Objects</span></span>


<span data-ttu-id="a3e10-104">Certains paramètres de stratégie de groupe de Microsoft User performance (UE-V) peuvent être définis pour les ordinateurs et d’autres pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a3e10-104">Some Microsoft User Experience Virtualization (UE-V) Group Policy settings can be defined for computers and others can be defined for users.</span></span> <span data-ttu-id="a3e10-105">UE-V les paramètres de stratégie de configuration de l’agent peuvent être définis pour des ordinateurs ou des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a3e10-105">UE-V agent configuration policy settings can be defined for computers or users.</span></span> <span data-ttu-id="a3e10-106">Pour plus d’informations sur l’installation des fichiers ADMX de stratégie de groupe UE-V, voir [installation des modèles ADMX de stratégie de groupe UE-v](installing-the-ue-v-group-policy-admx-templates.md).</span><span class="sxs-lookup"><span data-stu-id="a3e10-106">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V Group Policy ADMX Templates](installing-the-ue-v-group-policy-admx-templates.md).</span></span>

<span data-ttu-id="a3e10-107">Les paramètres de stratégie suivants peuvent être configurés pour UE-V:</span><span class="sxs-lookup"><span data-stu-id="a3e10-107">The following policy settings can be configured for UE-V:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a3e10-108">Nom du paramètre de stratégie</span><span class="sxs-lookup"><span data-stu-id="a3e10-108">Policy setting name</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a3e10-109">Target</span><span class="sxs-lookup"><span data-stu-id="a3e10-109">Target</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a3e10-110">Description du paramètre de stratégie</span><span class="sxs-lookup"><span data-stu-id="a3e10-110">Policy setting description</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a3e10-111">Options de configuration</span><span class="sxs-lookup"><span data-stu-id="a3e10-111">Configuration options</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3e10-112">Utiliser la virtualisation de l’utilisation de l’utilisateur (UE-V)</span><span class="sxs-lookup"><span data-stu-id="a3e10-112">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-113">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a3e10-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-114">Ce paramètre de stratégie vous permet d’activer ou de désactiver la virtualisation de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3e10-114">This policy setting allows you to enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-115">Activez ou désactivez ce paramètre de stratégie.</span><span class="sxs-lookup"><span data-stu-id="a3e10-115">Enable or disable this policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3e10-116">Emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="a3e10-116">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-117">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a3e10-117">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-118">Ce paramètre de stratégie permet de configurer l’emplacement de stockage des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3e10-118">This policy setting configures where the user settings will be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-119">Spécifiez un chemin d’accès UNC (Universal Naming Convention) et des variables (par exemple, \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="a3e10-119">Provide a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3e10-120">Chemin du catalogue de modèles de paramètres</span><span class="sxs-lookup"><span data-stu-id="a3e10-120">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-121">Ordinateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="a3e10-121">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-122">Ce paramètre de stratégie configure l’emplacement de stockage des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="a3e10-122">This policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="a3e10-123">Ce paramètre de stratégie configure également si le catalogue est utilisé pour remplacer les modèles Microsoft par défaut installés avec l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3e10-123">This policy setting also configures whether the catalog will be used to replace the default Microsoft templates that are installed with the UE-V agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-124">Fournissez un chemin UNC (Universal Naming Convention) tel que \Server\TemplateShare ou un dossier sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a3e10-124">Provide a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p></p>
<p><span data-ttu-id="a3e10-125">Activez la case à cocher pour remplacer les modèles Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="a3e10-125">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3e10-126">Ne pas utiliser de fichiers hors connexion</span><span class="sxs-lookup"><span data-stu-id="a3e10-126">Do not use Offline Files</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-127">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a3e10-127">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-128">Ce paramètre de stratégie vous permet de configurer l’utilisation de la fonctionnalité fichiers en mode hors connexion de Windows pour UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3e10-128">This policy setting allows you to configure whether UE-V will use the Windows Offline Files feature.</span></span> <span data-ttu-id="a3e10-129">Ce paramètre de stratégie vous permet également d’activer la notification lorsque l’importation des paramètres utilisateur est retardée.</span><span class="sxs-lookup"><span data-stu-id="a3e10-129">This policy setting also allows you to enable notification to occur when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-130">Pour configurer l’agent UE-V de façon à ne pas utiliser de fichiers hors connexion, activez ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="a3e10-130">To configure the UE-V Agent to not use offline files, enable this setting.</span></span></p>
<p></p>
<p><span data-ttu-id="a3e10-131">Spécifiez si les notifications doivent être fournies lorsque l’importation des paramètres est retardée.</span><span class="sxs-lookup"><span data-stu-id="a3e10-131">Specify if notifications should be given when settings import is delayed.</span></span></p>
<p></p>
<p><span data-ttu-id="a3e10-132">Spécifiez la durée en secondes d’attente avant l’affichage de la notification.</span><span class="sxs-lookup"><span data-stu-id="a3e10-132">Specify the length of time in seconds to wait before the notification appears.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3e10-133">Délai d’expiration de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="a3e10-133">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-134">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a3e10-134">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-135">Ce paramètre de stratégie configure le nombre de millisecondes que l’ordinateur attend avant un délai d’expiration lors de la récupération des paramètres utilisateur à partir de l’emplacement des paramètres distants.</span><span class="sxs-lookup"><span data-stu-id="a3e10-135">This policy setting configures the number of milliseconds that the computer waits before a timeout when retrieving user settings from the remote settings location.</span></span> <span data-ttu-id="a3e10-136">Si l’emplacement de stockage à distance n’est pas disponible, le lancement de l’application est retardée de ce nombre de millisecondes.</span><span class="sxs-lookup"><span data-stu-id="a3e10-136">If the remote storage location is unavailable, the application launch is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-137">Spécifiez le délai d’expiration de la synchronisation préféré, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="a3e10-137">Specify the preferred synchronization timeout in milliseconds.</span></span> <span data-ttu-id="a3e10-138">Valeur par défaut de 2000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="a3e10-138">The default value of 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3e10-139">Seuil d’avertissement de taille de package</span><span class="sxs-lookup"><span data-stu-id="a3e10-139">Package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-140">Ordinateurs et utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a3e10-140">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-141">Ce paramètre de stratégie vous permet de configurer l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres.</span><span class="sxs-lookup"><span data-stu-id="a3e10-141">This policy setting allows you to configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-142">Spécifié le seuil préféré pour les tailles de packages de paramètres en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="a3e10-142">Specified the preferred threshold for settings package sizes in kilobytes.</span></span></p>
<p><span data-ttu-id="a3e10-143">Par défaut, l’agent UE-V n’a pas de seuil de taille de fichier de package.</span><span class="sxs-lookup"><span data-stu-id="a3e10-143">By default, the UE-V agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3e10-144">Paramètres d’application itinérante</span><span class="sxs-lookup"><span data-stu-id="a3e10-144">Roaming Application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-145">Utilisateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="a3e10-145">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-146">Ce paramètre de stratégie configure l’itinérance des paramètres utilisateur des applications.</span><span class="sxs-lookup"><span data-stu-id="a3e10-146">This policy setting configures the roaming of user settings of applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-147">Sélectionnez les paramètres Windows qui seront itinérants entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="a3e10-147">Select which Windows settings will roam between computers.</span></span></p>
<p><span data-ttu-id="a3e10-148">Par défaut, les paramètres utilisateur des applications avec le modèle de paramètres fourni par UE-V sont itinérants entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="a3e10-148">By default, the user settings of applications with settings template provided by UE-V are roamed between computers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3e10-149">Paramètres de Windows en itinérance</span><span class="sxs-lookup"><span data-stu-id="a3e10-149">Roaming Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-150">Utilisateurs uniquement</span><span class="sxs-lookup"><span data-stu-id="a3e10-150">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-151">Ce paramètre de stratégie configure l’itinérance des paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="a3e10-151">This policy setting configures the roaming of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3e10-152">Sélectionner les applications qui peuvent être déplacées entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="a3e10-152">Select which applications will roam between computers.</span></span></p>
<p><span data-ttu-id="a3e10-153">Par défaut, les thèmes Windows sont itinérants entre les ordinateurs de la même version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a3e10-153">By default, Windows themes are roamed between computers of the same operating system version.</span></span> <span data-ttu-id="a3e10-154">Les paramètres de bureau Windows et les options d’ergonomie ne sont pas itinérants.</span><span class="sxs-lookup"><span data-stu-id="a3e10-154">Windows desktop settings and Ease of Access settings are not roamed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="a3e10-155">Pour configurer des stratégies ciblées par l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="a3e10-155">To configure computer-targeted policies</span></span>**

1.  <span data-ttu-id="a3e10-156">Utilisez la console de gestion des stratégies de groupe (GPMC) ou la gestion avancée des stratégies de groupe (AGPM) sur l’ordinateur contrôleur de domaine qui gère la stratégie de groupe pour les ordinateurs UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3e10-156">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the domain controller computer that manages Group Policy for UE-V computers.</span></span> <span data-ttu-id="a3e10-157">Accédez à **Configuration ordinateur**, sélectionnez **stratégies**, **modèles d’administration**, cliquez sur **composants Windows**, puis sélectionnez **virtualisation**de l’utilisation de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3e10-157">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="a3e10-158">Sélectionnez le paramètre de stratégie à modifier.</span><span class="sxs-lookup"><span data-stu-id="a3e10-158">Select the policy setting to be edited.</span></span>

**<span data-ttu-id="a3e10-159">Pour configurer des stratégies ciblées par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a3e10-159">To configure user-targeted policies</span></span>**

1.  <span data-ttu-id="a3e10-160">Servez-vous de la console de gestion des stratégies de groupe (GPMC) ou de l’outil de gestion des stratégies de groupe (AGPM) dans Microsoft Desktop Optimization Pack</span><span class="sxs-lookup"><span data-stu-id="a3e10-160">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer that manages Group Policy for UE-V.</span></span> <span data-ttu-id="a3e10-161">Accédez à **Configuration utilisateur**, sélectionnez **stratégies**, sélectionnez **modèles d’administration**, cliquez sur **composants Windows**, puis sélectionnez virtualisation de l' **utilisation de Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="a3e10-161">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="a3e10-162">Sélectionnez le paramètre de stratégie modifié.</span><span class="sxs-lookup"><span data-stu-id="a3e10-162">Select the policy setting edited.</span></span>

<span data-ttu-id="a3e10-163">L’agent UE-V utilise l’ordre de priorité suivant pour déterminer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="a3e10-163">The UE-V agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="a3e10-164">Ordre de priorité pour les paramètres d’UE-V</span><span class="sxs-lookup"><span data-stu-id="a3e10-164">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="a3e10-165">Paramètres ciblés par l’utilisateur gérés par une stratégie de groupe: ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="a3e10-165">User-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="a3e10-166">Paramètres de l’ordinateur gérés par une stratégie de groupe: ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="a3e10-166">Computer-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="a3e10-167">Paramètres de configuration définis par l’utilisateur actuel à l’aide de PowerShell ou WMI; ces paramètres de configuration sont stockés par l’agent UE-V sous cet emplacement du Registre: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="a3e10-167">Configuration settings defined by the current user using PowerShell or WMI - These configuration settings are stored by the UE-V agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="a3e10-168">Paramètres de configuration définis pour l’ordinateur utilisant PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="a3e10-168">Configuration settings defined for the computer using PowerShell or WMI.</span></span> <span data-ttu-id="a3e10-169">Ces paramètres de configuration sont stockés par l’agent UE-V sous le `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="a3e10-169">These configuration settings are stored by the UE-V agent under the `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration`.</span></span>

## <span data-ttu-id="a3e10-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3e10-170">Related topics</span></span>


[<span data-ttu-id="a3e10-171">Administration d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="a3e10-171">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="a3e10-172">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="a3e10-172">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 






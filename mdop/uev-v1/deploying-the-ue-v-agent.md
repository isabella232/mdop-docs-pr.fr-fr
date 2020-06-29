---
title: Déploiement de l'agent UE-V
description: Déploiement de l'agent UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812203"
---
# <span data-ttu-id="0875f-103">Déploiement de l'agent UE-V</span><span class="sxs-lookup"><span data-stu-id="0875f-103">Deploying the UE-V Agent</span></span>


<span data-ttu-id="0875f-104">L’agent Microsoft User Interface Virtualization (UE-V) doit s’exécuter sur chaque ordinateur qui utilise UE-V pour rendre itinérants les paramètres d’application et de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0875f-104">The Microsoft User Experience Virtualization (UE-V) agent must run on each computer that uses UE-V to roam application and Windows settings.</span></span> <span data-ttu-id="0875f-105">Dans le cas d’un fichier d’installation unique, AgentSetup.exe, l’agent UE-V est installé sur les systèmes d’exploitation 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0875f-105">A single installer file, AgentSetup.exe, installs the UE-V agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="0875f-106">Les paramètres de ligne de commande de l’agent UE-V sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="0875f-106">The command-line parameters of the UE-V Agent are the following:</span></span>

**<span data-ttu-id="0875f-107">AgentSetup.exe des paramètres de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="0875f-107">AgentSetup.exe command-line parameters</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="0875f-108">Paramètre de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="0875f-108">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0875f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="0875f-109">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0875f-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="0875f-110">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0875f-111">/Help ou/h ou/?</span><span class="sxs-lookup"><span data-stu-id="0875f-111">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-112">Affiche la boîte de dialogue d’utilisation de AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="0875f-112">Displays the AgentSetup.exe usage dialog.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0875f-113">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="0875f-113">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-114">Indique le chemin UNC (Universal Naming Convention) qui définit l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="0875f-114">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-115">les variables d’environnement% nom d’utilisateur% ou% nom_ordinateur% sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="0875f-115">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="0875f-116">Les scripts peuvent nécessiter des variables d’échappement.</span><span class="sxs-lookup"><span data-stu-id="0875f-116">Scripting may require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="0875f-117">Par défaut </strong> : &lt; aucun &gt; (accueil de l’utilisateur Active Directory)</span><span class="sxs-lookup"><span data-stu-id="0875f-117">Default</strong>: &lt;none&gt; (Active Directory user home)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0875f-118">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="0875f-118">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-119">Indique le chemin UNC (Universal Naming Convention) qui définit l’emplacement dans lequel les nouveaux modèles d’emplacement des paramètres sont consultés.</span><span class="sxs-lookup"><span data-stu-id="0875f-119">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-120">Requis uniquement pour les modèles d’emplacement des paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="0875f-120">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0875f-121">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="0875f-121">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-122">Indique si les modèles Microsoft par défaut doivent être inscrits lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="0875f-122">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-123">True | Fals</span><span class="sxs-lookup"><span data-stu-id="0875f-123">True | False</span></span></p>
<p><strong><span data-ttu-id="0875f-124">Valeur par défaut </strong> : vrai</span><span class="sxs-lookup"><span data-stu-id="0875f-124">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0875f-125">PowerSchool</span><span class="sxs-lookup"><span data-stu-id="0875f-125">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-126">Spécifie la méthode de synchronisation à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0875f-126">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-127">OfflineFiles | Néant</span><span class="sxs-lookup"><span data-stu-id="0875f-127">OfflineFiles | None</span></span></p>
<p><strong><span data-ttu-id="0875f-128">Par défaut </strong> : OFFLINEFILES</span><span class="sxs-lookup"><span data-stu-id="0875f-128">Default</strong>: OfflineFiles</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0875f-129">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="0875f-129">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-130">Spécifie le nombre de millisecondes avant dépassement du délai d’attente lors de la récupération des paramètres utilisateur à partir de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="0875f-130">Specifies the number of milliseconds that the computer waits before timeout when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="0875f-131">Par défaut </strong> : 2000 millisecondes</span><span class="sxs-lookup"><span data-stu-id="0875f-131">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="0875f-132">(attendez 2 secondes)</span><span class="sxs-lookup"><span data-stu-id="0875f-132">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0875f-133">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="0875f-133">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-134">Indique si la synchronisation UE-V est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="0875f-134">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-135">True | Fals</span><span class="sxs-lookup"><span data-stu-id="0875f-135">True | False</span></span></p>
<p><strong><span data-ttu-id="0875f-136">Valeur par défaut </strong> : vrai</span><span class="sxs-lookup"><span data-stu-id="0875f-136">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0875f-137">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="0875f-137">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-138">Spécifie la taille de fichier du package de paramètres en octets lorsque l’agent UE-V signale que les fichiers dépassent le seuil.</span><span class="sxs-lookup"><span data-stu-id="0875f-138">Specifies a settings package file size in bytes when the UE-V agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-139">&lt;papier&gt;</span><span class="sxs-lookup"><span data-stu-id="0875f-139">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="0875f-140">Par défaut </strong> : aucun (aucun seuil d’avertissement)</span><span class="sxs-lookup"><span data-stu-id="0875f-140">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0875f-141">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="0875f-141">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-142">Spécifie le paramètre de participation au programme d’amélioration du produit.</span><span class="sxs-lookup"><span data-stu-id="0875f-142">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="0875f-143">S’il est défini sur true, les informations du programme d’installation sont téléchargées sur le site du programme d’amélioration du produit de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0875f-143">If set to true, then installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="0875f-144">Si elle a la valeur false, aucune information n’est téléchargée.</span><span class="sxs-lookup"><span data-stu-id="0875f-144">If set to false, then no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-145">True | Fals</span><span class="sxs-lookup"><span data-stu-id="0875f-145">True | False</span></span></p>
<p><strong><span data-ttu-id="0875f-146">Valeur par défaut </strong> : false</span><span class="sxs-lookup"><span data-stu-id="0875f-146">Default</strong>: False</span></span></p>
<p><strong><span data-ttu-id="0875f-147">Sur Windows 7 </strong> : vrai</span><span class="sxs-lookup"><span data-stu-id="0875f-147">On Windows 7</strong>: True</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0875f-148">Lors de l’installation, le paramètre de ligne de commande SettingsStoragePath spécifie l’emplacement de stockage des paramètres pour les valeurs de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0875f-148">During installation, the SettingsStoragePath command-line parameter specifies the settings storage location for the settings values.</span></span> <span data-ttu-id="0875f-149">Un emplacement de stockage des paramètres peut être défini avant le déploiement de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="0875f-149">A settings storage location can be defined before deploying the UE-V Agent.</span></span> <span data-ttu-id="0875f-150">Si aucun emplacement de stockage des paramètres n’est défini, UE-V utilise le répertoire de base de l’utilisateur Active Directory comme emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="0875f-150">If no settings storage location is defined, then UE-V uses the Active Directory user Home Directory as the settings storage location.</span></span> <span data-ttu-id="0875f-151">Lorsque vous spécifiez la configuration SettingsStoragePath lors de l’installation et que vous utilisez le% nom_utilisateur% dans le cadre de la valeur, vous pouvez utiliser les mêmes paramètres utilisateur sur tous les ordinateurs ou sessions dans lesquels l’utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="0875f-151">When you specify the SettingsStoragePath configuration during setup and use the %username% as part of the value, this will roam the same user settings experience on all computers or sessions that a user logs into.</span></span> <span data-ttu-id="0875f-152">Si vous spécifiez les variables%username%\\%ComputerName% dans le cadre de la valeur SettingsStoragePath, cela préserve l’interface des paramètres pour chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0875f-152">If you specify the %username%\\%computername% variables as part of the SettingsStoragePath value, this will preserve the settings experience for each computer.</span></span>

<span data-ttu-id="0875f-153">Les fichiers Windows Installer (. msi) spécifiques à l’architecture sont fournis pour l’installation de l’agent UE-V, en plus du programme d’installation 32 bits et 64 bits combinés.</span><span class="sxs-lookup"><span data-stu-id="0875f-153">Architecture-specific Windows Installer (.msi) files are provided for the UE-V agent installation in addition to the combined 32-bit and 64-bit installer.</span></span> <span data-ttu-id="0875f-154">Les fichiers AgentSetupx86.msi ou AgentSetupx64.msi d’installation sont plus petits que le fichier AgentSetup.exe et peuvent rationaliser les déploiements des agents.</span><span class="sxs-lookup"><span data-stu-id="0875f-154">The AgentSetupx86.msi or AgentSetupx64.msi install files are smaller than the AgentSetup.exe file and might streamline the agent deployments.</span></span> <span data-ttu-id="0875f-155">Les paramètres de ligne de commande du programme d’installation de AgentSetup.exe sont pris en charge pour l’installation de Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="0875f-155">The command-line parameters for the AgentSetup.exe installer are supported for the Windows Installer (.msi) installation.</span></span>

<span data-ttu-id="0875f-156">**Remarques**  Lors de l’installation ou de la désinstallation d’UE-V agent, vous pouvez utiliser le fichier AgentSetup.exe ou le AgentSetup &lt; arch &gt; . msi, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="0875f-156">**Note** During UE-V agent installation or uninstallation you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="0875f-157">Le même fichier doit être utilisé pour désinstaller l’agent UE-V tel qu’il a été utilisé pour installer l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="0875f-157">The same file must be used to uninstall the UE-V Agent as it was used to install the UE-V Agent.</span></span>

 

<span data-ttu-id="0875f-158">Veillez à utiliser le format de variable approprié lors de l’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="0875f-158">Be sure to use the correct variable format when you install the UE-V agent.</span></span> <span data-ttu-id="0875f-159">Le tableau suivant contient des exemples d’options de déploiement pour l’utilisation des fichiers d’installation de AgentSetup.exe ou Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="0875f-159">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) installation files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="0875f-160">Type de déploiement</span><span class="sxs-lookup"><span data-stu-id="0875f-160">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0875f-161">Description du déploiement</span><span class="sxs-lookup"><span data-stu-id="0875f-161">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0875f-162">Exemple</span><span class="sxs-lookup"><span data-stu-id="0875f-162">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0875f-163">Invite de commandes</span><span class="sxs-lookup"><span data-stu-id="0875f-163">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-164">Lorsque vous installez l’agent UE-V à partir d’une invite de commandes, utilisez le format de variable% ^ nom_utilisateur%.</span><span class="sxs-lookup"><span data-stu-id="0875f-164">When you install the UE-V agent from a command prompt, use the %^username% variable format.</span></span> <span data-ttu-id="0875f-165">Si des guillemets sont nécessaires en raison d’espaces dans le chemin de stockage des paramètres, utilisez un fichier de script de commandes pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="0875f-165">If quotation marks are needed because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0875f-166">Script de commande</span><span class="sxs-lookup"><span data-stu-id="0875f-166">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-167">Lorsque vous installez l’agent UE-V à partir d’un fichier de script de commandes, utilisez le format de variable%% nom_utilisateur%%.</span><span class="sxs-lookup"><span data-stu-id="0875f-167">When you install the UE-V Agent from a batch script file, use the %%username%% variable format.</span></span> <span data-ttu-id="0875f-168">Si vous utilisez cette méthode d’installation, vous devez ignorer la variable contenant les caractères%%.</span><span class="sxs-lookup"><span data-stu-id="0875f-168">If you use this install method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="0875f-169">Sans ce caractère, le script développe la variable nom d’utilisateur au moment de l’installation, plutôt qu’au moment de l’exécution, provoquant l’utilisation d’un emplacement de stockage des paramètres unique pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0875f-169">Without this character, the script expands the username variable at install time, rather than at run time, causing UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0875f-170">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0875f-170">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-171">Lorsque vous installez l’agent UE-V à partir d’une invite PowerShell ou d’un script PowerShell, utilisez le format de variable% nom_utilisateur%.</span><span class="sxs-lookup"><span data-stu-id="0875f-171">When you install the UE-V agent from a PowerShell prompt or PowerShell script, use the %username% variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0875f-172">Distribution de logiciel électronique, comme le déploiement du déploiement logiciel de Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="0875f-172">Electronic software distribution, such as deployment of Configuration Manager Software Deployment)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0875f-173">Lorsque vous installez l’agent UE-V avec Configuration Manager, utilisez le format de variable ^% nom_utilisateur ^%.</span><span class="sxs-lookup"><span data-stu-id="0875f-173">When you install the UE-V Agent with Configuration Manager, use the ^%username^% variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0875f-174">**Remarques**  L’installation de l’agent U-EV nécessite des droits d’administrateur et l’ordinateur exige un redémarrage pour que l’agent UE-V puisse s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="0875f-174">**Note** The installation of the U-EV Agent requires Administrator rights and the computer will require a restart before the UE-V agent can run.</span></span>

 

## <span data-ttu-id="0875f-175">Méthodes de déploiement d’agent UE-V à partir d’un partage réseau</span><span class="sxs-lookup"><span data-stu-id="0875f-175">UE-V Agent deployment methods from a network share</span></span>


<span data-ttu-id="0875f-176">Pour déployer l’agent UE-V, vous pouvez utiliser les méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="0875f-176">You can use the following methods to deploy the UE-V agent:</span></span>

-   <span data-ttu-id="0875f-177">Une solution de distribution de logiciels électronique (ESD) qui peut installer un fichier Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="0875f-177">An electronic software distribution (ESD) solution that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="0875f-178">Script d’installation qui fait référence au fichier Windows Installer (. msi) qui est stocké sur un partage centralisé.</span><span class="sxs-lookup"><span data-stu-id="0875f-178">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="0875f-179">Exécution manuelle du programme d’installation sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0875f-179">Manually running the installation program on the computer.</span></span>

<span data-ttu-id="0875f-180">Pour déployer l’agent UE-V à partir d’un partage réseau, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="0875f-180">To deploy the UE-V agent from a network share, use the following steps:</span></span>

**<span data-ttu-id="0875f-181">Pour installer et configurer l’agent UE-V à partir d’un partage réseau</span><span class="sxs-lookup"><span data-stu-id="0875f-181">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="0875f-182">Copiez le fichier d’installation de l’agent UE-V (AgentSetup.exe) sur un partage réseau auquel les utilisateurs disposent d’une autorisation de lecture.</span><span class="sxs-lookup"><span data-stu-id="0875f-182">Stage the UE-V agent installation file (AgentSetup.exe) on a network share to which users have “read” permission.</span></span>

2.  <span data-ttu-id="0875f-183">Déploiement d’un script sur des ordinateurs utilisateurs qui installent l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="0875f-183">Deploy a script to user computers that installs the UE-V agent.</span></span> <span data-ttu-id="0875f-184">Le script doit spécifier l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="0875f-184">The script should specify the settings storage location.</span></span>

**<span data-ttu-id="0875f-185">Mettre à jour l’agent UE-V</span><span class="sxs-lookup"><span data-stu-id="0875f-185">Update the UE-V Agent</span></span>**

<span data-ttu-id="0875f-186">Les mises à jour du logiciel d’agent UE-V seront fournies par le biais de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="0875f-186">Updates for the UE-V agent software will be provided through Microsoft Update.</span></span> <span data-ttu-id="0875f-187">Lors d’une mise à niveau d’un agent UE-V, le groupe par défaut des modèles d’emplacement des paramètres pour les applications Microsoft courantes et les paramètres Windows est susceptible d’être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="0875f-187">During a UE-V agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings may be updated.</span></span> <span data-ttu-id="0875f-188">UE-V les mises à jour de l’agent peuvent être déployées à l’aide de l’infrastructure de distribution de logiciels d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="0875f-188">UE-V agent updates can be deployed by using Enterprise Software Distribution (ESD) infrastructure.</span></span>

## <span data-ttu-id="0875f-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0875f-189">Related topics</span></span>


[<span data-ttu-id="0875f-190">Déploiement d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="0875f-190">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="0875f-191">Configurations prises en charge pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="0875f-191">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

[<span data-ttu-id="0875f-192">Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="0875f-192">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

[<span data-ttu-id="0875f-193">Installation du Générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="0875f-193">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="0875f-194">Déploiement de l’agent de virtualisation de l’utilisation de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0875f-194">Deploy the User Experience Virtualization Agent</span></span>
 

 






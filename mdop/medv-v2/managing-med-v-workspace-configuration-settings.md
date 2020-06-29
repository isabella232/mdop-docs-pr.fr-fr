---
title: Gestion des paramètres de configuration d'espace de travail MED-V
description: Gestion des paramètres de configuration d'espace de travail MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811586"
---
# <span data-ttu-id="fcb08-103">Gestion des paramètres de configuration d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="fcb08-103">Managing MED-V Workspace Configuration Settings</span></span>


<span data-ttu-id="fcb08-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 enregistre ses paramètres de configuration dans le registre.</span><span class="sxs-lookup"><span data-stu-id="fcb08-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 stores its configuration settings in the registry.</span></span> <span data-ttu-id="fcb08-105">Les informations que nous inclurons ici pour le registre peuvent vous aider à mieux gérer vos services MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb08-105">The information we include here about the registry may help you better manage your MED-V services.</span></span>

<span data-ttu-id="fcb08-106">MED-V utilise le chemin de recherche suivant pour rechercher les valeurs des paramètres résultants:</span><span class="sxs-lookup"><span data-stu-id="fcb08-106">MED-V uses the following search path when looking for the resultant settings values:</span></span>

<span data-ttu-id="fcb08-107">MED-V examine d’abord la stratégie de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fcb08-107">MED-V first looks in the machine policy.</span></span>

<span data-ttu-id="fcb08-108">Si la valeur est introuvable, MED-V effectue une recherche dans la stratégie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fcb08-108">If the value is not found, MED-V looks in the user policy.</span></span>

<span data-ttu-id="fcb08-109">Si la valeur est introuvable, MED-V effectue une recherche dans la ruche HKEY \ _LOCAL \ _MACHINE \\System.</span><span class="sxs-lookup"><span data-stu-id="fcb08-109">If the value is not found, MED-V looks in the HKEY\_LOCAL\_MACHINE\\System hive.</span></span>

<span data-ttu-id="fcb08-110">Si la valeur est introuvable, MED-V effectue une recherche dans la ruche du registre de l’utilisateur HKEY \ _CURRENT.</span><span class="sxs-lookup"><span data-stu-id="fcb08-110">If the value is not found, MED-V looks in the HKEY\_CURRENT USER registry hive.</span></span>

<span data-ttu-id="fcb08-111">Si la valeur est toujours introuvable, MED-V utilise la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="fcb08-111">If the value is still not found, MED-V uses the default.</span></span>

<span data-ttu-id="fcb08-112">Nous vous conseillons de définir la valeur dans la ruche HKEY \ _LOCAL \ _MACHINE \\System ou la stratégie de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fcb08-112">A general best practice is to set the value in the HKEY\_LOCAL\_MACHINE\\System hive or in the machine policy.</span></span> <span data-ttu-id="fcb08-113">Toutefois, si vous voulez que l’utilisateur final puisse configurer un paramètre particulier, vous devez le laisser.</span><span class="sxs-lookup"><span data-stu-id="fcb08-113">But if you want the end user to be able to configure a particular setting, then you should leave it out.</span></span>

**<span data-ttu-id="fcb08-114">Remarque</span><span class="sxs-lookup"><span data-stu-id="fcb08-114">Note</span></span>**  
<span data-ttu-id="fcb08-115">Avant de déployer vos espaces de travail MED-V, vous pouvez utiliser un éditeur de script pour modifier le script Windows PowerShell (fichier. ps1) créé par le gestionnaire de package MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb08-115">Before you deploy your MED-V workspaces, you can use a script editor to change the Windows PowerShell script (.ps1 file) that the MED-V workspace packager created.</span></span> <span data-ttu-id="fcb08-116">Pour plus d’informations, reportez-vous à [Configuration des paramètres avancés à l’aide de Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="fcb08-116">For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span></span>

<span data-ttu-id="fcb08-117">Après avoir déployé vos espaces de travail MED-V, vous pouvez modifier certains paramètres de configuration de MED-V en modifiant les entrées du Registre.</span><span class="sxs-lookup"><span data-stu-id="fcb08-117">After you have deployed your MED-V workspaces, you can change certain MED-V configuration settings by editing the registry entries.</span></span>



<span data-ttu-id="fcb08-118">Cette section répertorie toutes les clés de Registre MED-V configurables et explique leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="fcb08-118">This section lists all the configurable MED-V registry keys and explains their uses.</span></span>

## <span data-ttu-id="fcb08-119">Clé de diagnostic</span><span class="sxs-lookup"><span data-stu-id="fcb08-119">Diagnostics Key</span></span>


<span data-ttu-id="fcb08-120">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="fcb08-120">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fcb08-121">Nom</span><span class="sxs-lookup"><span data-stu-id="fcb08-121">Name</span></span> </th>
<th align="left"><span data-ttu-id="fcb08-122">Type</span><span class="sxs-lookup"><span data-stu-id="fcb08-122">Type</span></span> </th>
<th align="left"><span data-ttu-id="fcb08-123">Données/par défaut</span><span class="sxs-lookup"><span data-stu-id="fcb08-123">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="fcb08-124">Description</span><span class="sxs-lookup"><span data-stu-id="fcb08-124">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-125">EventLogLevel</span><span class="sxs-lookup"><span data-stu-id="fcb08-125">EventLogLevel</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-126">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-127">Par défaut = 3</span><span class="sxs-lookup"><span data-stu-id="fcb08-127">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-128">Type d’informations enregistrées dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="fcb08-128">The type of information that is logged in the event log.</span></span> <span data-ttu-id="fcb08-129">Les niveaux incluent les éléments suivants: 0 (aucun), 1 (erreur), 2 (avertissement), 3 (information), 4 (débogage).</span><span class="sxs-lookup"><span data-stu-id="fcb08-129">Levels include the following: 0 (None), 1 (Error), 2 (Warning), 3 (Information), 4 (Debug).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fcb08-130">Clé FTS</span><span class="sxs-lookup"><span data-stu-id="fcb08-130">Fts Key</span></span>


<span data-ttu-id="fcb08-131">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.</span><span class="sxs-lookup"><span data-stu-id="fcb08-131">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Fts key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fcb08-132">Nom</span><span class="sxs-lookup"><span data-stu-id="fcb08-132">Name</span></span></th>
<th align="left"><span data-ttu-id="fcb08-133">Type</span><span class="sxs-lookup"><span data-stu-id="fcb08-133">Type</span></span></th>
<th align="left"><span data-ttu-id="fcb08-134">Données/par défaut</span><span class="sxs-lookup"><span data-stu-id="fcb08-134">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="fcb08-135">Description</span><span class="sxs-lookup"><span data-stu-id="fcb08-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-136">AddUserToAdminGroupEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-136">AddUserToAdminGroupEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-137">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-137">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-138">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="fcb08-138">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-139">Configure la première fois que le programme d’installation ajoute automatiquement l’utilisateur final au groupe&#39;s administrateur.</span><span class="sxs-lookup"><span data-stu-id="fcb08-139">Configures whether first time setup automatically adds the end user to the administrator&#39;s group.</span></span> <span data-ttu-id="fcb08-140">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-140">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-141">0 = faux: le programme d’installation pour la première fois n’ajoute pas automatiquement l’utilisateur final au groupe&#39;les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="fcb08-141">0 = false: First time setup does not automatically add the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-142">1 = vrai: le programme d’installation ajoute automatiquement l’utilisateur final au groupe&#39;s administrateur.</span><span class="sxs-lookup"><span data-stu-id="fcb08-142">1 = true: First time setup automatically adds the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-143">ComputerNameMask</span><span class="sxs-lookup"><span data-stu-id="fcb08-143">ComputerNameMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-144">SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-144">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-145">MEDV\*</span><span class="sxs-lookup"><span data-stu-id="fcb08-145">MEDV\*</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-146">Le masque du nom de l’ordinateur utilisé pour créer l’ordinateur virtuel invité&#39;le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fcb08-146">The computer name mask that is used to create the guest virtual machine&#39;s computer name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-147">Le masque peut contenir une balise% username% pour insérer le nom d’utilisateur dans le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fcb08-147">The mask can contain a %username% tag to insert the username as part of the computer name.</span></span> <span data-ttu-id="fcb08-148">De même, la balise% hostname% insère le nom de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-148">Likewise, the %hostname% tag inserts the name of the host computer.</span></span></p>
<p><span data-ttu-id="fcb08-149">Chaque &quot; # &quot; caractère du masque est remplacé par un chiffre aléatoire.</span><span class="sxs-lookup"><span data-stu-id="fcb08-149">Every &quot;#&quot; character in the mask is replaced by a random digit.</span></span> <span data-ttu-id="fcb08-150">Le caractère astérisque (\*) à la fin du masque est remplacé par un caractère alphanumérique aléatoire.</span><span class="sxs-lookup"><span data-stu-id="fcb08-150">An asterisk (\*) character at the end of the mask is replaced by random alphanumeric characters.</span></span></p>
<p><span data-ttu-id="fcb08-151">Un nombre déterminé de caractères du nom d’utilisateur% et du nom d’utilisateur% peut être capturé à l’aide de crochets.</span><span class="sxs-lookup"><span data-stu-id="fcb08-151">A specific number of characters from %hostname% and %username% can be captured by using square brackets.</span></span> <span data-ttu-id="fcb08-152">Par exemple, &quot; % nom_utilisateur% [3] &quot; utilisera les trois premiers caractères du nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fcb08-152">For example, &quot;%username%[3]&quot; would use the first three characters of the username.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-153">DeleteVMStateTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-153">DeleteVMStateTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-154">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-154">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-155">Valeur par défaut = 90</span><span class="sxs-lookup"><span data-stu-id="fcb08-155">Default=90</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-156">Valeur du délai d’expiration, en secondes, lors de la première tentative de configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fcb08-156">The time-out value, in seconds, when first time setup tries to delete the virtual machine.</span></span> <span data-ttu-id="fcb08-157">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-157">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-158">DetachVfdTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-158">DetachVfdTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-160">Par défaut = 120</span><span class="sxs-lookup"><span data-stu-id="fcb08-160">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-161">La valeur du délai d’expiration en secondes, lors de la première tentative de configuration de la disquette virtuelle de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fcb08-161">The time-out value, in seconds, when first time setup tries to detach the virtual floppy disk from the virtual machine.</span></span> <span data-ttu-id="fcb08-162">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-162">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-163">DialogUrl</span><span class="sxs-lookup"><span data-stu-id="fcb08-163">DialogUrl</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-164">SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-164">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-165">URL personnalisable qui s’associe à la page Web interne et qui s’affiche lorsque vous affichez un message de boîte de dialogue pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="fcb08-165">Customizable URL that links to internal webpage and is displayed by first time setup dialog messages.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-166">ExplorerTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-166">ExplorerTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-167">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-167">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-168">Par défaut = 900</span><span class="sxs-lookup"><span data-stu-id="fcb08-168">Default=900</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-169">Valeur du délai d’attente, en secondes, que le programme d’installation attend pour la première fois pour l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="fcb08-169">The time-out value, in seconds, that first time setup waits for Windows Explorer.</span></span> <span data-ttu-id="fcb08-170">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-170">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-171">FailureDialogMsg</span><span class="sxs-lookup"><span data-stu-id="fcb08-171">FailureDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-172">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-172">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-173">Le message est disponible dans le fichier de ressources</span><span class="sxs-lookup"><span data-stu-id="fcb08-173">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-174">Message personnalisable qui s’affiche à l’utilisateur final lorsque le programme ne peut pas être exécuté pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="fcb08-174">Customizable message that is displayed to the end user when first time setup cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-175">GiveUserGroupRightsMaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="fcb08-175">GiveUserGroupRightsMaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-176">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-176">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-177">Par défaut = 3</span><span class="sxs-lookup"><span data-stu-id="fcb08-177">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-178">Le nombre maximal de fois que MED-V tente de lui accorder des droits de groupe d’utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="fcb08-178">The maximum number of times that MED-V tries to give an end user group rights.</span></span> <span data-ttu-id="fcb08-179">Le dépassement de la valeur de réessayer spécifiée sans être en mesure de donner aux droits de groupe d’utilisateurs finaux entraîne un échec de préparation d’ordinateur virtuel, qui est ensuite soumis à la valeur MaxRetryCount.</span><span class="sxs-lookup"><span data-stu-id="fcb08-179">Exceeding the specified retry value without being able to successfully give an end user group rights most likely causes a virtual machine preparation failure that is then subject to the MaxRetryCount value.</span></span> <span data-ttu-id="fcb08-180">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-180">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-181">GiveUserGroupRightsTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-181">GiveUserGroupRightsTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-182">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-182">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-183">Par défaut = 300</span><span class="sxs-lookup"><span data-stu-id="fcb08-183">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-184">Valeur du délai d’expiration, en secondes, lors de la fourniture de droits de groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="fcb08-184">The time-out value, in seconds, when giving a user group rights.</span></span> <span data-ttu-id="fcb08-185">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-185">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-186">LogFilePaths</span><span class="sxs-lookup"><span data-stu-id="fcb08-186">LogFilePaths</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-187">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-187">MULTI_SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-188">Liste des chemins d’accès aux fichiers journaux collectés par MED-V lors de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="fcb08-188">A list of the log file paths that MED-V collects during first time setup.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-189">MaxPostponeTime</span><span class="sxs-lookup"><span data-stu-id="fcb08-189">MaxPostponeTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-190">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-190">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-191">Par défaut = 120</span><span class="sxs-lookup"><span data-stu-id="fcb08-191">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-192">Le nombre maximal d’heures qui peuvent être reportées par l’utilisateur final pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="fcb08-192">The maximum number of hours that first time setup can be postponed by the end user.</span></span> <span data-ttu-id="fcb08-193">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-193">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-194">MaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="fcb08-194">MaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-195">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-195">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-196">Par défaut = 3</span><span class="sxs-lookup"><span data-stu-id="fcb08-196">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-197">Le nombre maximal de fois que MED-V tente de préparer une machine virtuelle si chaque tentative se termine par un échec autre qu’une erreur logicielle.</span><span class="sxs-lookup"><span data-stu-id="fcb08-197">The maximum number of times that MED-V tries to prepare a virtual machine if each attempt ends in a failure other than a software error.</span></span> <span data-ttu-id="fcb08-198">En cas d’échec de la préparation de l’ordinateur virtuel et du nombre de tentatives de configuration pour la première fois, MED-V informe l’utilisateur final de l’échec et ne donne pas la possibilité de réessayer.</span><span class="sxs-lookup"><span data-stu-id="fcb08-198">When virtual machine preparation fails and the number of first time setup retries is exceeded, then MED-V informs the end user about the failure and does not give the option to retry.</span></span> <span data-ttu-id="fcb08-199">Le nombre est remis à zéro chaque fois que MED-V est démarré.</span><span class="sxs-lookup"><span data-stu-id="fcb08-199">The count is re-set every time that MED-V is started.</span></span> <span data-ttu-id="fcb08-200">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-200">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-201">Mode</span><span class="sxs-lookup"><span data-stu-id="fcb08-201">Mode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-202">SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-202">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-203">Par défaut = sans assistance</span><span class="sxs-lookup"><span data-stu-id="fcb08-203">Default=Unattended</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-204">Configure le mode d’interaction de l’utilisateur pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="fcb08-204">Configures how first time setup interacts with the user.</span></span> <span data-ttu-id="fcb08-205">Les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="fcb08-205">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fcb08-206">Surveillance.</span><span class="sxs-lookup"><span data-stu-id="fcb08-206">Attended.</span></span></strong> <span data-ttu-id="fcb08-207">L’utilisateur final doit entrer des informations lors de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="fcb08-207">The end user must enter information during first time setup.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fcb08-208">Remarque</span><span class="sxs-lookup"><span data-stu-id="fcb08-208">Note</span></span></strong><br/><p><span data-ttu-id="fcb08-209">Si vous avez créé le fichier Sysprep. inf de manière à ce que la mini-installation nécessite l’entrée de l’utilisateur, vous devez sélectionner le <strong> </strong> mode assisté ou des problèmes peuvent se produire lors de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="fcb08-209">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, then you must select <strong>Attended</strong> mode or problems might occur during first time setup.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fcb08-210">Sans assistance </strong> .</span><span class="sxs-lookup"><span data-stu-id="fcb08-210">Unattended</strong>.</span></span> <span data-ttu-id="fcb08-211">Lors de la première installation, la machine virtuelle n’est pas visible pour l’utilisateur final, mais l’utilisateur final est invité avant le premier démarrage de l’installation.</span><span class="sxs-lookup"><span data-stu-id="fcb08-211">The virtual machine is not shown to the end user during first time setup, but the end user is prompted before first time setup starts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fcb08-212">Silent </strong> .</span><span class="sxs-lookup"><span data-stu-id="fcb08-212">Silent</strong>.</span></span> <span data-ttu-id="fcb08-213">Lors de la première installation, la machine virtuelle n’est pas visible pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="fcb08-213">The virtual machine is not shown to the end user at all during first time setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-214">NonInteractiveRetryTimeoutInc</span><span class="sxs-lookup"><span data-stu-id="fcb08-214">NonInteractiveRetryTimeoutInc</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-215">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-215">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-216">Par défaut = 15</span><span class="sxs-lookup"><span data-stu-id="fcb08-216">Default=15</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-217">La valeur du délai d’expiration, en minutes, lors de la première configuration du mode interactif de configuration pour la première fois lors de la nouvelle tentative d’installation.</span><span class="sxs-lookup"><span data-stu-id="fcb08-217">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode when re-attempting setup.</span></span> <span data-ttu-id="fcb08-218">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-218">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-219">NonInteractiveTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-219">NonInteractiveTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-220">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-220">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-221">Par défaut = 45</span><span class="sxs-lookup"><span data-stu-id="fcb08-221">Default=45</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-222">La valeur du délai d’expiration, en minutes, lors de la première configuration du mode interactif de configuration pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="fcb08-222">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode.</span></span> <span data-ttu-id="fcb08-223">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-223">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-224">PostponeUtcDateTimeLimit</span><span class="sxs-lookup"><span data-stu-id="fcb08-224">PostponeUtcDateTimeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-225">SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-225">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-226">La date et l’heure au format DateTime UTC, qui peut être ajourné pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="fcb08-226">The date and time, in UTC DateTime format, that first time setup can be postponed.</span></span> <span data-ttu-id="fcb08-227">Entrez au format &quot; aaaa-mm-jj hh: mm &quot; avec les heures spécifiées à l’aide de la norme d’horloge de 24 heures.</span><span class="sxs-lookup"><span data-stu-id="fcb08-227">Enter in the format &quot;yyyy-MM-dd hh:mm&quot; with hours specified by using the 24-hour clock standard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-228">RetryDialogMsg</span><span class="sxs-lookup"><span data-stu-id="fcb08-228">RetryDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-229">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-229">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-230">Le message est disponible dans le fichier de ressources</span><span class="sxs-lookup"><span data-stu-id="fcb08-230">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-231">Message personnalisable qui s’affiche à l’utilisateur final lors du premier démarrage de l’installation.</span><span class="sxs-lookup"><span data-stu-id="fcb08-231">Customizable message that is displayed to the end user when first time setup must re-attempt setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-232">SetComputerNameEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-232">SetComputerNameEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-233">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-233">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-234">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="fcb08-234">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-235">La configuration de l’entrée NomOrdinateur dans la section [UserData] du fichier Sysprep. inf dans l’invité doit être mise à jour en fonction du ComputerNameMask spécifié.</span><span class="sxs-lookup"><span data-stu-id="fcb08-235">Configures whether the ComputerName entry under the [UserData] section of the Sysprep.inf file in the guest should be updated according to the specified ComputerNameMask.</span></span>   <span data-ttu-id="fcb08-236">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-236">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-237">0 = false: l’entrée NomOrdinateur dans le fichier Sysprep. inf n’est pas mise à jour en fonction de ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="fcb08-237">0 = false: The ComputerName entry in the Sysprep.inf file is not updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-238">1 = vrai: l’entrée NomOrdinateur dans le fichier Sysprep. inf est mise à jour en fonction de ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="fcb08-238">1 = true: The ComputerName entry in the Sysprep.inf file is updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-239">SetJoinDomainEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-239">SetJoinDomainEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-240">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-240">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-241">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="fcb08-241">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-242">Configure si le paramètre JoinDomain sous la section [identification] du fichier Sysprep. inf dans l’invité doit être mis à jour de façon à correspondre aux paramètres de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-242">Configures whether the JoinDomain setting under the [Identification] section of the Sysprep.inf file in the guest should be updated to match the settings on the host.</span></span>  <span data-ttu-id="fcb08-243">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-243">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-244">0 = false: le paramètre JoinDomain dans le fichier Sysprep. inf n’est pas mis à jour pour correspondre aux paramètres de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-244">0 = false: The JoinDomain setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-245">1 = vrai: le paramètre JoinDomain dans le fichier Sysprep. inf est mis à jour de façon à correspondre aux paramètres de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-245">1 = true: The JoinDomain setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-246">SetMachineObjectOUEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-246">SetMachineObjectOUEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-247">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-247">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-248">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="fcb08-248">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-249">Configure si le paramètre MachineObjectOU sous la section [identification] du fichier Sysprep. inf de l’invité est mis à jour de façon à correspondre à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-249">Configures whether the MachineObjectOU setting under the [Identification] section of the Sysprep.inf file in the guest is updated to match the host.</span></span>  <span data-ttu-id="fcb08-250">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-250">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-251">0 = false: le paramètre MachineObjectOU dans le fichier Sysprep. inf n’est pas mis à jour pour correspondre aux paramètres de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-251">0 = false: The MachineObjectOU setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-252">1 = vrai: le paramètre MachineObjectOU dans le fichier Sysprep. inf est mis à jour de façon à correspondre aux paramètres de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-252">1 = true: The MachineObjectOU setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-253">SetRegionalSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-253">SetRegionalSettingsEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-254">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-254">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-255">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="fcb08-255">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-256">Configure le mode de mise à jour des paramètres de la section [RegionalSettings] du fichier Sysprep. inf dans l’invité pour correspondre à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-256">Configures whether the settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span>  <span data-ttu-id="fcb08-257">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-257">0 = false; 1 = true.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fcb08-258">Remarque</span><span class="sxs-lookup"><span data-stu-id="fcb08-258">Note</span></span></strong><br/><p><span data-ttu-id="fcb08-259">Par défaut, le paramètre TimeZone dans l’invité est toujours synchronisé avec le paramètre TimeZone de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-259">By default, the setting for TimeZone in the guest is always synchronized with the TimeZone setting in the host.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-260">0 = false: les paramètres de la section [RegionalSettings] du fichier Sysprep. inf dans l’invité ne sont pas mis à jour pour correspondre à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-260">0 = false: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are not updated to match the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-261">1 = vrai: les paramètres de la section [RegionalSettings] du fichier Sysprep. inf de l’invité sont mis à jour de façon à correspondre à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-261">1 = true: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-262">SetUserDataEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-262">SetUserDataEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-263">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-263">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-264">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="fcb08-264">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-265">Indique si les paramètres FullName et OrgName figurant sous la section [UserData] du fichier Sysprep. inf de l’invité sont mis à jour de façon à correspondre aux paramètres de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-265">Configures whether the FullName and the OrgName settings under the [UserData] section of the Sysprep.inf file in the guest are updated to match the settings on the host.</span></span>  <span data-ttu-id="fcb08-266">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-266">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-267">0 = false: les paramètres NomComplet et OrgName du fichier Sysprep. inf ne sont pas mis à jour pour correspondre aux paramètres de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-267">0 = false: The FullName and OrgName settings in the Sysprep.inf file are not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-268">1 = vrai: les paramètres NomComplet et OrgName du fichier Sysprep. inf sont mis à jour de façon à correspondre aux paramètres de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-268">1 = true: The FullName and OrgName settings in the Sysprep.inf file are updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-269">StartDialogMsg</span><span class="sxs-lookup"><span data-stu-id="fcb08-269">StartDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-270">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-270">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-271">Le message est disponible dans le fichier de ressources</span><span class="sxs-lookup"><span data-stu-id="fcb08-271">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-272">Message personnalisable qui s’affiche à l’utilisateur final lors du premier démarrage de l’installation.</span><span class="sxs-lookup"><span data-stu-id="fcb08-272">Customizable message that is displayed to the end user when first time setup is ready to start.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-273">TaskCancelTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-273">TaskCancelTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-274">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-275">Par défaut = 30</span><span class="sxs-lookup"><span data-stu-id="fcb08-275">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-276">La valeur du délai d’expiration, en secondes, lors de la première installation, le programme d’installation attend une réponse de l’ordinateur virtuel pour une opération d’annulation.</span><span class="sxs-lookup"><span data-stu-id="fcb08-276">The time-out value, in seconds, that first time setup waits for a response from the virtual machine for a Cancel operation.</span></span> <span data-ttu-id="fcb08-277">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-277">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-278">TaskVMTurnOffTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-278">TaskVMTurnOffTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-279">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-279">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-280">Par défaut = 60</span><span class="sxs-lookup"><span data-stu-id="fcb08-280">Default=60</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-281">La valeur du délai d’expiration, en secondes, lors de la première installation, le programme d’installation attend que l’ordinateur virtuel s’arrête.</span><span class="sxs-lookup"><span data-stu-id="fcb08-281">The time-out value, in seconds, that first time setup waits for the virtual machine to shut down.</span></span> <span data-ttu-id="fcb08-282">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-282">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-283">UpgradeTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-283">UpgradeTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-284">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-284">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-285">Par défaut = 600</span><span class="sxs-lookup"><span data-stu-id="fcb08-285">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-286">Durée, en secondes, avant la mise à niveau du logiciel de l’agent invité MED-V. Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-286">The time, in seconds, before an attempted upgrade of the MED-V Guest Agent software times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fcb08-287">Clé UserExperience</span><span class="sxs-lookup"><span data-stu-id="fcb08-287">UserExperience Key</span></span>


<span data-ttu-id="fcb08-288">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience et à la clé HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.</span><span class="sxs-lookup"><span data-stu-id="fcb08-288">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\UserExperience key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fcb08-289">Nom</span><span class="sxs-lookup"><span data-stu-id="fcb08-289">Name</span></span></th>
<th align="left"><span data-ttu-id="fcb08-290">Type</span><span class="sxs-lookup"><span data-stu-id="fcb08-290">Type</span></span></th>
<th align="left"><span data-ttu-id="fcb08-291">Données/par défaut</span><span class="sxs-lookup"><span data-stu-id="fcb08-291">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="fcb08-292">Description</span><span class="sxs-lookup"><span data-stu-id="fcb08-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-293">AppPublishingEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-293">AppPublishingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-294">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-294">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-295">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="fcb08-295">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-296">Configure le mode d’activation de la publication d’application de l’invité vers l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-296">Configures whether application publication from the guest to the host is enabled.</span></span>  <span data-ttu-id="fcb08-297">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-297">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-298">0 = false: désactive la publication d’applications de l’invité auprès de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-298">0 = false: Disables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-299">1 = true: permet la publication d’applications de l’invité auprès de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-299">1 = true: Enables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-300">AudioSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-300">AudioSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-301">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-302">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="fcb08-302">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-303">Indique si le partage de l’appareil d’e/s audio entre l’invité et l’hôte est activé.</span><span class="sxs-lookup"><span data-stu-id="fcb08-303">Configures whether the sharing of the audio I/O device between the guest and the host is enabled.</span></span>  <span data-ttu-id="fcb08-304">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-304">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-305">0 = false: désactive le partage du périphérique d’e/s audio entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-305">0 = false: Disables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-306">1 = true: active le partage de l’appareil d’e/s audio entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-306">1 = true: Enables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-307">ClipboardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-307">ClipboardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-308">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-308">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-309">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="fcb08-309">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-310">Indique si le partage du presse-papiers entre l’invité et l’hôte est activé.</span><span class="sxs-lookup"><span data-stu-id="fcb08-310">Configures whether the sharing of the Clipboard between the guest and the host is enabled.</span></span>  <span data-ttu-id="fcb08-311">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-311">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-312">0 = false: désactive le partage du presse-papiers entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-312">0 = false: Disables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-313">1 = true: active le partage du presse-papiers entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-313">1 = true: Enables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-314">DialogTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-314">DialogTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-315">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-315">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-316">Par défaut = 300</span><span class="sxs-lookup"><span data-stu-id="fcb08-316">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-317">Durée, en secondes, avant le délai de démarrage de la première boîte de dialogue de démarrage de l’installation. Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-317">The time, in seconds, before the first time setup Start Dialog times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-318">HideVmTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-318">HideVmTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-319">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-319">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-320">Par défaut = 30</span><span class="sxs-lookup"><span data-stu-id="fcb08-320">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-321">Valeur du délai d’expiration (en minutes) à laquelle la fenêtre de l’ordinateur virtuel en plein écran est cachée lors d’une longue tentative d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="fcb08-321">The time-out value, in minutes, that the full-screen virtual machine window is hidden from the end user during a long logon attempt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-322">LogonStartEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-322">LogonStartEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-323">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-323">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-324">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="fcb08-324">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-325">Indique si l’invité doit être démarré lorsque l’utilisateur final se connecte à l’ordinateur de bureau ou lorsque la première application invité est démarrée.</span><span class="sxs-lookup"><span data-stu-id="fcb08-325">Configures whether the guest should be started when the end user logs on to the desktop or when the first guest application is started.</span></span>  <span data-ttu-id="fcb08-326">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-326">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-327">0 = false: l’invité est démarré lorsque la première application invité est démarrée.</span><span class="sxs-lookup"><span data-stu-id="fcb08-327">0 = false: The guest is started when the first guest application is started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-328">1 = vrai: l’invité est démarré lorsque l’utilisateur final se connecte à l’ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="fcb08-328">1 = true: The guest is started when the end user logs on to the desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-329">PrinterSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-329">PrinterSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-330">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-330">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-331">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="fcb08-331">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-332">Indique si le partage d’imprimantes entre l’invité et l’hôte est activé.</span><span class="sxs-lookup"><span data-stu-id="fcb08-332">Configures whether the sharing of printers between the guest and the host is enabled.</span></span>  <span data-ttu-id="fcb08-333">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-333">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-334">0 = false: désactive le partage d’imprimantes entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-334">0 = false: Disables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-335">1 = true: permet le partage d’imprimantes entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-335">1 = true: Enables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-336">RebootAbsoluteDelayTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-336">RebootAbsoluteDelayTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-337">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-337">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-338">Par défaut = 1440</span><span class="sxs-lookup"><span data-stu-id="fcb08-338">Default=1440</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-339">Valeur du délai d’expiration, en minutes, lors du premier démarrage de l’installation.</span><span class="sxs-lookup"><span data-stu-id="fcb08-339">The time-out value, in minutes, that first time setup waits for a restart.</span></span> <span data-ttu-id="fcb08-340">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-340">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-341">RedirectUrls</span><span class="sxs-lookup"><span data-stu-id="fcb08-341">RedirectUrls</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-342">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-342">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-343">Liste d’URL spécifiée</span><span class="sxs-lookup"><span data-stu-id="fcb08-343">Specified URL list</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-344">Spécifie une liste d’URL à rediriger de l’hôte vers l’invité.</span><span class="sxs-lookup"><span data-stu-id="fcb08-344">Specifies a list of URLs to be redirected from the host to the guest.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-345">SmartCardLogonEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-345">SmartCardLogonEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-346">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-346">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-347">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="fcb08-347">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-348">Permet de configurer l’utilisation des cartes à puce pour l’authentification des utilisateurs dans MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb08-348">Configures whether smart cards can be used to authenticate users to MED-V.</span></span> <span data-ttu-id="fcb08-349">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-349">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-350">0 = faux: ne permet pas aux cartes à puce d’authentifier les utilisateurs finaux sur MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb08-350">0 = false: Does not let Smart Cards authenticate end users to MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-351">1 = vrai: permet aux cartes à puce d’authentifier les utilisateurs finaux sur MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb08-351">1 = true: Lets Smart Cards authenticate end users to MED-V.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fcb08-352">Important</span><span class="sxs-lookup"><span data-stu-id="fcb08-352">Important</span></span></strong><br/><p><span data-ttu-id="fcb08-353">Si SmartCardLogonEnabled et CredentialCacheEnabled sont activés, SmartCardLogonEnabled substitutions CredentialCacheEnabled.</span><span class="sxs-lookup"><span data-stu-id="fcb08-353">If SmartCardLogonEnabled and CredentialCacheEnabled are both enabled, SmartCardLogonEnabled overrides CredentialCacheEnabled.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-354">SmartCardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-354">SmartCardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-356">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="fcb08-356">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-357">Configure le partage des cartes à puce entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-357">Configures whether the sharing of Smart Cards between the guest and the host is enabled.</span></span>  <span data-ttu-id="fcb08-358">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-358">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-359">0 = false: désactive le partage des cartes à puce entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-359">0 = false: Disables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-360">1 = true: permet le partage de cartes à puce entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-360">1 = true: Enables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-361">USBDeviceSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-361">USBDeviceSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-363">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="fcb08-363">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-364">Configure le partage des périphériques USB entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-364">Configures whether the sharing of USB devices between the guest and the host is enabled.</span></span>  <span data-ttu-id="fcb08-365">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-365">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-366">0 = false: désactive le partage des périphériques USB entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-366">0 = false: Disables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-367">1 = true: permet le partage d’appareils USB entre l’invité et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-367">1 = true: Enables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fcb08-368">Clé VM</span><span class="sxs-lookup"><span data-stu-id="fcb08-368">VM Key</span></span>


<span data-ttu-id="fcb08-369">Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM et à la clé HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="fcb08-369">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\VM key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\VM key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fcb08-370">Nom</span><span class="sxs-lookup"><span data-stu-id="fcb08-370">Name</span></span></th>
<th align="left"><span data-ttu-id="fcb08-371">Type</span><span class="sxs-lookup"><span data-stu-id="fcb08-371">Type</span></span></th>
<th align="left"><span data-ttu-id="fcb08-372">Données/par défaut</span><span class="sxs-lookup"><span data-stu-id="fcb08-372">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="fcb08-373">Description</span><span class="sxs-lookup"><span data-stu-id="fcb08-373">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-374">CloseAction</span><span class="sxs-lookup"><span data-stu-id="fcb08-374">CloseAction</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-375">SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-375">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-376">Par défaut = mise en veille prolongée</span><span class="sxs-lookup"><span data-stu-id="fcb08-376">Default=HIBERNATE</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-377">L’action exécutée par l’ordinateur virtuel après la dernière application en cours d’exécution est fermée.</span><span class="sxs-lookup"><span data-stu-id="fcb08-377">The action that the virtual machine performs after the last application that is running is closed.</span></span> <span data-ttu-id="fcb08-378">Ce paramètre est ignoré si la valeur LogonStartEnabled est activée.</span><span class="sxs-lookup"><span data-stu-id="fcb08-378">This setting is ignored if the LogonStartEnabled value is enabled.</span></span> <span data-ttu-id="fcb08-379">Les options disponibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="fcb08-379">Possible options are as follows:</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fcb08-380">Mise en veille prolongée </strong> .</span><span class="sxs-lookup"><span data-stu-id="fcb08-380">HIBERNATE</strong> .</span></span> <span data-ttu-id="fcb08-381">Cette option libère toutes les ressources physiques utilisées par l’ordinateur virtuel, comme la mémoire et le processeur, et enregistre l’état de toutes les applications et opérations en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fcb08-381">This option releases all physical resources that the virtual machine is using, such as memory and CPU, and saves the state of all running applications and operations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fcb08-382">ARRÊT </strong> .</span><span class="sxs-lookup"><span data-stu-id="fcb08-382">SHUTDOWN</strong> .</span></span> <span data-ttu-id="fcb08-383">Cette option arrête le système d’exploitation invité de manière sécurisée, puis libère toutes les ressources physiques utilisées par l’ordinateur virtuel, comme la mémoire et l’UC.</span><span class="sxs-lookup"><span data-stu-id="fcb08-383">This option shuts down the guest operating system safely and then releases all physical resources that the virtual machine is using, such as memory and CPU.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fcb08-384">DÉSACTIVER </strong> .</span><span class="sxs-lookup"><span data-stu-id="fcb08-384">TURN-OFF</strong>.</span></span> <span data-ttu-id="fcb08-385">Cette option peut entraîner une perte de données, car elle est identique à la désactivation du bouton d’alimentation ou du retrait du cordon d’alimentation sur un ordinateur physique.</span><span class="sxs-lookup"><span data-stu-id="fcb08-385">This option can cause data loss because it is the same as turning off the power button or pulling out the power cord on a physical computer.</span></span> <span data-ttu-id="fcb08-386">Utilisez cette option uniquement si vous ne pouvez pas utiliser l’une des deux autres options.</span><span class="sxs-lookup"><span data-stu-id="fcb08-386">Use this option only if you cannot use one of the other two options.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-387">GuestMemFromHostMem</span><span class="sxs-lookup"><span data-stu-id="fcb08-387">GuestMemFromHostMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-388">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-388">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-389">378, 512, 1024, 1536, 2048</span><span class="sxs-lookup"><span data-stu-id="fcb08-389">378, 512, 1024, 1536, 2048</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-390">Liste de valeurs de mémoire (Mo) pour l’invité.</span><span class="sxs-lookup"><span data-stu-id="fcb08-390">A list of memory (MB) values for the guest.</span></span> <span data-ttu-id="fcb08-391">Cette valeur est utilisée pour déterminer la quantité de RAM disponible pour l’invité.</span><span class="sxs-lookup"><span data-stu-id="fcb08-391">This value is used to determine how much RAM is available to the guest.</span></span> <span data-ttu-id="fcb08-392">Combinée à HostMemToGuestMem, une table de recherche est créée pour déterminer la quantité de mémoire RAM à allouer sur l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="fcb08-392">Combined with HostMemToGuestMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="fcb08-393">Les valeurs possibles peuvent être comprises entre 128 et 3712.</span><span class="sxs-lookup"><span data-stu-id="fcb08-393">Possible values can be from 128 to 3712.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-394">GuestUpdateDuration</span><span class="sxs-lookup"><span data-stu-id="fcb08-394">GuestUpdateDuration</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-396">Par défaut = 240</span><span class="sxs-lookup"><span data-stu-id="fcb08-396">Default=240</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-397">Le nombre de minutes écoulées par MED-V pour la mise à jour automatique de l’invité, en commençant à l’heure spécifiée dans la valeur GuestUpdateTime.</span><span class="sxs-lookup"><span data-stu-id="fcb08-397">The number of minutes that MED-V should keep the guest awake for automatic updating, starting at the time specified in the GuestUpdateTime value.</span></span> <span data-ttu-id="fcb08-398">Plage = 0 à 1440.</span><span class="sxs-lookup"><span data-stu-id="fcb08-398">Range = 0 to 1440.</span></span> <span data-ttu-id="fcb08-399">Si vous définissez cette valeur sur zéro (0), la fonction de correction invité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="fcb08-399">Setting this value to zero (0) disables the guest patching functionality.</span></span></p>
<p><span data-ttu-id="fcb08-400">Pour plus d’informations sur la mise à jour automatique des invités, voir <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gestion des mises à jour automatiques pour les espaces de travail MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="fcb08-400">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-401">GuestUpdateTime</span><span class="sxs-lookup"><span data-stu-id="fcb08-401">GuestUpdateTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-402">SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-402">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-403">Par défaut = 00:00</span><span class="sxs-lookup"><span data-stu-id="fcb08-403">Default=00:00</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-404">Les heures et les minutes chaque jour lorsque MED-V doit réveiller l’invité pour la mise à jour automatique, en utilisant la norme d’horloge de 24 heures.</span><span class="sxs-lookup"><span data-stu-id="fcb08-404">The hour and minute each day when MED-V should wake up the guest for automatic updating, by using the 24-hour clock standard.</span></span> <span data-ttu-id="fcb08-405">Spécifiez l’heure au format HH: MM.</span><span class="sxs-lookup"><span data-stu-id="fcb08-405">Specify the time in the format HH:MM</span></span>  </p>
<p><span data-ttu-id="fcb08-406">Pour plus d’informations sur la mise à jour automatique des invités, voir <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gestion des mises à jour automatiques pour les espaces de travail MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="fcb08-406">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-407">HostMemToGuestMem</span><span class="sxs-lookup"><span data-stu-id="fcb08-407">HostMemToGuestMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-408">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-408">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-409">1024, 2048, 4096, 8192, 16384</span><span class="sxs-lookup"><span data-stu-id="fcb08-409">1024, 2048, 4096, 8192, 16384</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-410">Liste de valeurs de mémoire (Mo) pour l’invité, définies par la mémoire RAM disponible sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-410">A list of memory (MB) values for the guest, determined by the RAM available on the host.</span></span> <span data-ttu-id="fcb08-411">Combinée à GuestMemFromHostMem, une table de recherche est créée pour déterminer la quantité de mémoire RAM à allouer sur l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="fcb08-411">Combined with GuestMemFromHostMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="fcb08-412">Les valeurs possibles peuvent être comprises entre 1024 et 16384.</span><span class="sxs-lookup"><span data-stu-id="fcb08-412">Possible values can be from 1024 to 16384.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-413">HostMemToGuestMemCalcEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-413">HostMemToGuestMemCalcEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-414">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-414">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-415">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="fcb08-415">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-416">Configure si la mémoire allouée pour l’invité est calculée à partir de la mémoire présente sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-416">Configures whether the memory allocated for the guest is calculated from the memory present on the host.</span></span>  <span data-ttu-id="fcb08-417">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-417">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-418">0 = false: la mémoire allouée pour l’invité n’est pas calculée à partir de la mémoire présente sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-418">0 = false: The memory allocated for the guest is not calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-419">1 = vrai: la mémoire allouée pour l’invité est calculée à partir de la mémoire présente sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fcb08-419">1 = true: The memory allocated for the guest is calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-420">Mémoire</span><span class="sxs-lookup"><span data-stu-id="fcb08-420">Memory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-421">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-421">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-422">Par défaut = 512</span><span class="sxs-lookup"><span data-stu-id="fcb08-422">Default=512</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-423">RAM (Mo) qui doit être allouée pour l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="fcb08-423">The RAM (MB) that should be allocated for the guest virtual machine.</span></span> <span data-ttu-id="fcb08-424">Ce paramètre est ignoré si le paramètre HostMemToGuestMemEnabled est activé.</span><span class="sxs-lookup"><span data-stu-id="fcb08-424">This setting is ignored if the HostMemToGuestMemEnabled setting is enabled.</span></span> <span data-ttu-id="fcb08-425">Plage = 128 à 2048.</span><span class="sxs-lookup"><span data-stu-id="fcb08-425">Range=128 to 2048.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-426">MultiUserEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb08-426">MultiUserEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-427">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-427">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-428">Par défaut = 0</span><span class="sxs-lookup"><span data-stu-id="fcb08-428">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-429">Configure si plusieurs utilisateurs partagent le même espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb08-429">Configures whether multiple users share the same MED-V workspace.</span></span>  <span data-ttu-id="fcb08-430">0 = faux; 1 = vrai.</span><span class="sxs-lookup"><span data-stu-id="fcb08-430">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-431">0 = faux: plusieurs utilisateurs ne partagent pas le même espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb08-431">0 = false: Multiple users do not share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-432">1 = vrai: plusieurs utilisateurs partagent le même espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb08-432">1 = true: Multiple users share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fcb08-433">NetworkingMode</span><span class="sxs-lookup"><span data-stu-id="fcb08-433">NetworkingMode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-434">SZ</span><span class="sxs-lookup"><span data-stu-id="fcb08-434">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-435">Par défaut = NAT</span><span class="sxs-lookup"><span data-stu-id="fcb08-435">Default=NAT</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-436">Type de connexion réseau utilisée sur l’invité.</span><span class="sxs-lookup"><span data-stu-id="fcb08-436">The kind of network connection used on the guest.</span></span> <span data-ttu-id="fcb08-437">Les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="fcb08-437">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fcb08-438">Bridged </strong> .</span><span class="sxs-lookup"><span data-stu-id="fcb08-438">Bridged</strong>.</span></span> <span data-ttu-id="fcb08-439">MED-V dispose de sa propre adresse réseau, généralement obtenue par le biais du protocole DHCP.</span><span class="sxs-lookup"><span data-stu-id="fcb08-439">MED-V has its own network address, typically obtained through DHCP.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="fcb08-440">TAR </strong> .</span><span class="sxs-lookup"><span data-stu-id="fcb08-440">NAT</strong>.</span></span> <span data-ttu-id="fcb08-441">MED-V utilise la traduction d’adresses réseau (NAT) pour partager l’adresse IP de l’hôte&#39;s pour le trafic sortant.</span><span class="sxs-lookup"><span data-stu-id="fcb08-441">MED-V uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-442">TaskTimeout</span><span class="sxs-lookup"><span data-stu-id="fcb08-442">TaskTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-443">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-443">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-444">Par défaut = 600</span><span class="sxs-lookup"><span data-stu-id="fcb08-444">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-445">Valeur de délai d’expiration générale, en secondes, que MED-V attend qu’une tâche se termine, par exemple, redémarrage et arrêt.</span><span class="sxs-lookup"><span data-stu-id="fcb08-445">A general time-out value, in seconds, that MED-V waits for a task to be completed, such as restarting and shutting down.</span></span> <span data-ttu-id="fcb08-446">Plage = 0 à 2147483647.</span><span class="sxs-lookup"><span data-stu-id="fcb08-446">Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fcb08-447">Paramètres du Registre invité</span><span class="sxs-lookup"><span data-stu-id="fcb08-447">Guest Registry Settings</span></span>


<span data-ttu-id="fcb08-448">Cette section répertorie les clés de registre d’invité MED-V configurables et explique leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="fcb08-448">This section lists the configurable MED-V guest registry keys and explains their uses.</span></span>

### <span data-ttu-id="fcb08-449">v2</span><span class="sxs-lookup"><span data-stu-id="fcb08-449">v2</span></span>

<span data-ttu-id="fcb08-450">Le tableau suivant fournit des informations sur la valeur du Registre invité associée à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.</span><span class="sxs-lookup"><span data-stu-id="fcb08-450">The following table provides information about the guest registry value associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\ key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fcb08-451">Nom</span><span class="sxs-lookup"><span data-stu-id="fcb08-451">Name</span></span> </th>
<th align="left"><span data-ttu-id="fcb08-452">Type</span><span class="sxs-lookup"><span data-stu-id="fcb08-452">Type</span></span> </th>
<th align="left"><span data-ttu-id="fcb08-453">Données/par défaut</span><span class="sxs-lookup"><span data-stu-id="fcb08-453">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="fcb08-454">Description</span><span class="sxs-lookup"><span data-stu-id="fcb08-454">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fcb08-455">EnableGPWorkarounds</span><span class="sxs-lookup"><span data-stu-id="fcb08-455">EnableGPWorkarounds</span></span></p></td>
<td align="left"><p><span data-ttu-id="fcb08-456">DWORD</span><span class="sxs-lookup"><span data-stu-id="fcb08-456">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-457">Par défaut = 1</span><span class="sxs-lookup"><span data-stu-id="fcb08-457">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="fcb08-458">Configure la façon dont MED-V gère les clés BufferPolicyReads et GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="fcb08-458">Configures how MED-V handles the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="fcb08-459">Par défaut, MED-V définit ces clés comme suit:</span><span class="sxs-lookup"><span data-stu-id="fcb08-459">By default, MED-V sets these keys as follows:</span></span></p>
<p><span data-ttu-id="fcb08-460">BufferPolicyReads = 1 et GroupPolicyMinTransferRate = 0.</span><span class="sxs-lookup"><span data-stu-id="fcb08-460">BufferPolicyReads=1 and GroupPolicyMinTransferRate=0.</span></span></p>
<p><span data-ttu-id="fcb08-461">Créez la clé EnableGPWorkarounds, si nécessaire, puis affectez la valeur zéro à la clé si vous ne souhaitez pas que MED-V modifie les paramètres par défaut de BufferPolicyReads et GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="fcb08-461">Create the EnableGPWorkarounds  key, if it is necessary, and set the key to zero if you do not want MED-V to change the default settings of BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fcb08-462">Remarque</span><span class="sxs-lookup"><span data-stu-id="fcb08-462">Note</span></span></strong><br/><p><span data-ttu-id="fcb08-463">Si votre espace de travail MED-V s’exécute en mode NAT, EnableGPWorkarounds affecte les clés de Registre BufferPolicyReads et GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="fcb08-463">If your MED-V workspace is running in NAT mode, EnableGPWorkarounds affects the registry keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span> <span data-ttu-id="fcb08-464">Si votre espace de travail MED-V s’exécute en mode BRIDGEd, EnableGPWorkarounds affecte uniquement la clé de Registre BufferPolicyReads.</span><span class="sxs-lookup"><span data-stu-id="fcb08-464">If your MED-V workspace is running in BRIDGED mode, EnableGPWorkarounds only affects the registry key BufferPolicyReads.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="fcb08-465">1 = vrai: MED-V définit les touches BufferPolicyReads = 1 et GroupPolicyMinTransferRate = 0 (en cas d’exécution en mode NAT) ou simplement BufferPolicyReads = 1 (en mode pont).</span><span class="sxs-lookup"><span data-stu-id="fcb08-465">1=true: MED-V sets the keys BufferPolicyReads=1 and GroupPolicyMinTransferRate=0 (if running in NAT mode) or just BufferPolicyReads=1 (if running in BRIDGED mode).</span></span></p>
<p><span data-ttu-id="fcb08-466">0 = faux: MED-V n’apporte aucune modification aux clés BufferPolicyReads et GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="fcb08-466">0=false: MED-V does not make any changes to the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fcb08-467">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcb08-467">Related topics</span></span>


[<span data-ttu-id="fcb08-468">Gérer les applications de l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="fcb08-468">Manage MED-V Workspace Applications</span></span>](manage-med-v-workspace-applications.md)

[<span data-ttu-id="fcb08-469">Gérer la redirection d'URL MED-V</span><span class="sxs-lookup"><span data-stu-id="fcb08-469">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)

[<span data-ttu-id="fcb08-470">Gérer les paramètres de l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="fcb08-470">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)










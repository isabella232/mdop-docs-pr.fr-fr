---
title: Autorisations d'accès utilisateur dans Application Virtualization Client
description: Autorisations d'accès utilisateur dans Application Virtualization Client
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806178"
---
# <span data-ttu-id="c5fa7-103">Autorisations d'accès utilisateur dans Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="c5fa7-103">User Access Permissions in Application Virtualization Client</span></span>


<span data-ttu-id="c5fa7-104">Dans l’onglet **autorisations** de la boîte de dialogue **Propriétés** , accessible en cliquant avec le bouton droit sur le nœud **virtualisation** de l’application dans la console de gestion du client de virtualisation des applications, les administrateurs peuvent accorder des autorisations aux utilisateurs pour utiliser les diverses fonctions client.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-104">On the **Permissions** tab on the **Properties** dialog box, accessible by right-clicking the **Application Virtualization** node in the Application Virtualization Client Management Console, administrators can grant users permissions to use the various client functions.</span></span>

<span data-ttu-id="c5fa7-105">**Remarques**  Avant de modifier les autorisations des utilisateurs, assurez-vous que les modifications apportées aux autorisations sont conformes aux instructions de l’Organisation concernant l’octroi d’autorisations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-105">**Note** Before changing users permissions, ensure that any permissions changes are consistent with the organization's guidelines for granting user permissions.</span></span>

 

<span data-ttu-id="c5fa7-106">Le tableau suivant répertorie et décrit les autorisations qui peuvent être accordées aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-106">The following table lists and describes the permissions that can be granted to users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c5fa7-107">Nom de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="c5fa7-107">Permission Name</span></span></th>
<th align="left"><span data-ttu-id="c5fa7-108">Description</span><span class="sxs-lookup"><span data-stu-id="c5fa7-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-109">Ajouter des applications</span><span class="sxs-lookup"><span data-stu-id="c5fa7-109">Add applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-110">Enregistrez de nouvelles applications en passant un nouveau fichier OSD au client à l’aide du sfttray.exe, sftmime.exe ou la console MMC.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-110">Register new applications by passing a new OSD file to the client by using sfttray.exe, sftmime.exe or the MMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5fa7-111">Changer la taille de cache du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="c5fa7-111">Change file system cache size</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-112">Augmenter la taille du cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-112">Increase the size of the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-113">Changer de lecteur système de fichiers</span><span class="sxs-lookup"><span data-stu-id="c5fa7-113">Change file system drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-114">Sélectionnez une autre lettre de lecteur préférée pour le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-114">Select a different preferred drive letter for the file system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5fa7-115">Modifier les paramètres du journal</span><span class="sxs-lookup"><span data-stu-id="c5fa7-115">Change log settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-116">Modifiez le niveau du journal ou le chemin d’accès du journal du fichier journal du client.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-116">Change the log level or the log path for the client log file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-117">Changer de fichier OSD</span><span class="sxs-lookup"><span data-stu-id="c5fa7-117">Change OSD files</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-118">Modifiez les fichiers OSD pour les applications enregistrées et transmettez-les au client.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-118">Modify OSD files for registered applications and pass them into the client.</span></span> <span data-ttu-id="c5fa7-119">Cela n’affecte pas l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-119">This does not affect publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5fa7-120">Effacer les paramètres de l’application</span><span class="sxs-lookup"><span data-stu-id="c5fa7-120">Clear application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-121">Supprimez des types de fichiers, des raccourcis et des configurations pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-121">Delete file types, shortcuts and any configurations for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-122">Supprimer des applications</span><span class="sxs-lookup"><span data-stu-id="c5fa7-122">Delete applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-123">Supprimez toutes les références à une application du système de fichiers et du cache OSD pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-123">Remove all references to an application from the file system and OSD cache for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5fa7-124">Importer des applications dans le cache</span><span class="sxs-lookup"><span data-stu-id="c5fa7-124">Import applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-125">Chargez les données d’application directement à partir d’un fichier SFT spécifié dans le cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-125">Load application data directly from a specified SFT file into the file system cache.</span></span> <span data-ttu-id="c5fa7-126">Ce problème affecte tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-126">This affects all users.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-127">Charger des applications dans le cache</span><span class="sxs-lookup"><span data-stu-id="c5fa7-127">Load applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-128">Démarrez un chargement du fichier SFT pour une application à partir de la source configurée, par exemple un serveur de streaming App-V.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-128">Start a load of the SFT file for an application from the configured source, such as an App-V Streaming Server.</span></span> <span data-ttu-id="c5fa7-129">Cette opération charge l’application pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-129">This loads the application for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5fa7-130">Verrouillage et déverrouillage d’applications dans le cache</span><span class="sxs-lookup"><span data-stu-id="c5fa7-130">Lock and unlock applications in the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-131">Interdisez ou autorisez les applications d’être déchargées à partir du cache du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-131">Prevent or allow applications from being unloaded from the file system cache.</span></span> <span data-ttu-id="c5fa7-132">Ce problème affecte tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-132">This affects all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-133">Gestion des associations de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="c5fa7-133">Manage file type associations</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-134">Ajoutez, modifiez ou supprimez des associations de types de fichiers pour l’utilisateur actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-134">Add, modify, or delete file type associations for the current user only.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5fa7-135">Gérer les paramètres d’actualisation de publication</span><span class="sxs-lookup"><span data-stu-id="c5fa7-135">Manage publishing refresh settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-136">Modifiez les paramètres qui contrôlent le minutage des mises à jour de publication de tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-136">Change settings that control the timing of publishing refreshes for all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-137">Gérer les serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="c5fa7-137">Manage publishing servers</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-138">Ajoutez, modifiez ou supprimez des serveurs de publication pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-138">Add, modify, or delete publishing servers for all users on the computer.</span></span> <span data-ttu-id="c5fa7-139">Cette autorisation inclut implicitement l’autorisation de gérer les paramètres d’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-139">This permission implicitly includes permission to manage publishing refresh settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5fa7-140">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="c5fa7-140">Publish shortcuts</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-141">Créer de nouveaux raccourcis vers des applications enregistrées.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-141">Create new shortcuts to registered applications.</span></span> <span data-ttu-id="c5fa7-142">L’utilisateur doit également disposer de l’autorisation de créer des fichiers dans le système de fichiers local.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-142">The user must also have permission to create files in the local file system.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-143">Réparer des applications</span><span class="sxs-lookup"><span data-stu-id="c5fa7-143">Repair applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-144">Supprimer des configurations spécifiques aux applications pour l’utilisateur actuel, sans supprimer les raccourcis ou les types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-144">Remove application specific configurations for the current user without removing shortcuts or file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5fa7-145">Démarrer une actualisation de publication</span><span class="sxs-lookup"><span data-stu-id="c5fa7-145">Start a publishing refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-146">Démarrer une actualisation de publication non planifiée pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-146">Start an unscheduled publishing refresh for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-147">Basculer en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="c5fa7-147">Toggle offline mode</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-148">Changer le client entier en mode hors connexion pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-148">Change the entire client from online to offline mode for all users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5fa7-149">Décharger les applications du cache</span><span class="sxs-lookup"><span data-stu-id="c5fa7-149">Unload applications from the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-150">Effacez les données d’application du cache du système de fichiers pour tous les utilisateurs sans supprimer les paramètres spécifiques à l’utilisateur, les raccourcis ou les associations de types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-150">Clear application data from the file system cache for all users without removing user-specific settings, shortcuts, or file type associations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5fa7-151">Afficher toutes les applications</span><span class="sxs-lookup"><span data-stu-id="c5fa7-151">View all applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5fa7-152">Permettre à l’utilisateur de voir les applications virtuelles pour tous les utilisateurs enregistrés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5fa7-152">Allow the user to see the virtual applications for all users registered on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c5fa7-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5fa7-153">Related topics</span></span>


[<span data-ttu-id="c5fa7-154">Procédure pour modifier les autorisations d'accès utilisateur</span><span class="sxs-lookup"><span data-stu-id="c5fa7-154">How to Change User Access Permissions</span></span>](how-to-change-user-access-permissions.md)

 

 






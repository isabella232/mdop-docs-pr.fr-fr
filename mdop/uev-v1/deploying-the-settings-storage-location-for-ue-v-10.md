---
title: Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0
description: Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811874"
---
# <span data-ttu-id="346f5-103">Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="346f5-103">Deploying the Settings Storage Location for UE-V 1.0</span></span>


<span data-ttu-id="346f5-104">Le déploiement de Microsoft User Interface Virtualization (UE-V) nécessite un emplacement de stockage des paramètres où les paramètres utilisateur sont stockés dans un fichier de package de paramètres.</span><span class="sxs-lookup"><span data-stu-id="346f5-104">Microsoft User Experience Virtualization (UE-V) deployment requires a settings storage location where the user settings are stored in a settings package file.</span></span> <span data-ttu-id="346f5-105">Vous pouvez configurer l’emplacement de stockage des paramètres de l’une des deux manières suivantes:</span><span class="sxs-lookup"><span data-stu-id="346f5-105">The settings storage location can be configured in one of the following two ways:</span></span>

-   <span data-ttu-id="346f5-106">**Répertoire de base Active Directory** : si un répertoire de base est défini pour l’utilisateur dans Active Directory, l’agent UE-V utilisera cet emplacement pour stocker les packages d’emplacements des paramètres.</span><span class="sxs-lookup"><span data-stu-id="346f5-106">**Active Directory home directory** – if a home directory is defined for the user in Active Directory, the UE-V agent will use this location to store settings location packages.</span></span> <span data-ttu-id="346f5-107">L’agent UE-V crée dynamiquement le dossier de stockage propre à l’utilisateur sous la racine de l’annuaire de base.</span><span class="sxs-lookup"><span data-stu-id="346f5-107">The UE-V agent dynamically creates the user-specific storage folder below the root of the home directory.</span></span> <span data-ttu-id="346f5-108">L’agent utilise uniquement le répertoire de base de l’Active Directory si aucun emplacement de stockage des paramètres n’est défini.</span><span class="sxs-lookup"><span data-stu-id="346f5-108">The agent only uses the home directory of the Active Directory if a settings storage location is not defined.</span></span>

-   <span data-ttu-id="346f5-109">**Créer un partage de stockage de paramètres** : le partage de stockage de paramètres est un partage réseau standard accessible aux utilisateurs d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="346f5-109">**Create a settings storage share** – the settings storage share is a standard network share that is accessible by UE-V users.</span></span>

## <span data-ttu-id="346f5-110">Déployer un partage de stockage de paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="346f5-110">Deploy a UE-V settings storage share</span></span>


<span data-ttu-id="346f5-111">Lorsque vous créez le partage de stockage des paramètres, vous devez limiter l’accès aux seuls utilisateurs qui ont besoin d’y accéder.</span><span class="sxs-lookup"><span data-stu-id="346f5-111">When you create the settings storage share, you should limit access only to users that need access.</span></span> <span data-ttu-id="346f5-112">Les autorisations nécessaires sont indiquées dans les tableaux ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="346f5-112">The necessary permissions are shown in the tables below.</span></span>

**<span data-ttu-id="346f5-113">Pour déployer le partage réseau UE-V</span><span class="sxs-lookup"><span data-stu-id="346f5-113">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="346f5-114">Créer un groupe de sécurité pour les utilisateurs d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="346f5-114">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="346f5-115">Créez un dossier sur l’ordinateur central qui stockera les packages de paramètres UE-V, puis accordez aux utilisateurs d’UE-V des autorisations de groupe sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="346f5-115">Create a new folder on the centrally located computer that will store the UE-V settings packages, and then grant the UE-V users with group permissions to the folder.</span></span> <span data-ttu-id="346f5-116">L’administrateur prenant en charge UE-V aura besoin d’autorisations sur ce dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="346f5-116">The administrator supporting UE-V will need permissions to this shared folder.</span></span>

3.  <span data-ttu-id="346f5-117">Définissez les autorisations de niveau de partage (SMB) suivantes pour le dossier Setting Storage Location:</span><span class="sxs-lookup"><span data-stu-id="346f5-117">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="346f5-118">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="346f5-118">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="346f5-119">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="346f5-119">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="346f5-120">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="346f5-120">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="346f5-121">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="346f5-121">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="346f5-122">Groupe de sécurité des utilisateurs d’UE-V</span><span class="sxs-lookup"><span data-stu-id="346f5-122">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="346f5-123">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="346f5-123">Full Control</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="346f5-124">Définissez les autorisations NTFS suivantes pour le dossier emplacement de stockage des paramètres:</span><span class="sxs-lookup"><span data-stu-id="346f5-124">Set the following NTFS permissions for the settings storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="346f5-125">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="346f5-125">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="346f5-126">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="346f5-126">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="346f5-127">Folder</span><span class="sxs-lookup"><span data-stu-id="346f5-127">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="346f5-128">Créateur/propriétaire</span><span class="sxs-lookup"><span data-stu-id="346f5-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="346f5-129">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="346f5-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="346f5-130">Sous-dossiers et fichiers uniquement</span><span class="sxs-lookup"><span data-stu-id="346f5-130">Subfolders and Files Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="346f5-131">Groupe de sécurité des utilisateurs d’UE-V</span><span class="sxs-lookup"><span data-stu-id="346f5-131">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="346f5-132">Afficher le dossier/lire les données, créer des dossiers/ajouter des données</span><span class="sxs-lookup"><span data-stu-id="346f5-132">List Folder/Read Data, Create Folders/Append Data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="346f5-133">Ce dossier uniquement</span><span class="sxs-lookup"><span data-stu-id="346f5-133">This Folder Only</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

5.  <span data-ttu-id="346f5-134">Cliquez sur **OK** pour fermer les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="346f5-134">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="346f5-135">Cette configuration d’autorisation permet aux utilisateurs de créer des dossiers pour le stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="346f5-135">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="346f5-136">UE-V agent crée et sécurise un `settingspackage` dossier en cas d’exécution dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="346f5-136">The UE-V agent creates and secures a `settingspackage` folder while running in the context of the user.</span></span> <span data-ttu-id="346f5-137">L’utilisateur reçoit le contrôle total de son `settingspackage` dossier.</span><span class="sxs-lookup"><span data-stu-id="346f5-137">The user receives full control to their `settingspackage` folder.</span></span> <span data-ttu-id="346f5-138">Les autres utilisateurs n’héritent pas de l’accès à ce dossier.</span><span class="sxs-lookup"><span data-stu-id="346f5-138">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="346f5-139">Vous n’avez pas besoin de créer et de sécuriser des répertoires utilisateur individuels, car cela s’effectue automatiquement par l’agent qui s’exécute dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="346f5-139">You do not need to create and secure individual user directories, because this will be done automatically by the agent that runs in the context of the user.</span></span>

<span data-ttu-id="346f5-140">**Remarques**  Une sécurité supplémentaire peut être configurée quand un serveur Windows est utilisé pour le partage de stockage de paramètres.</span><span class="sxs-lookup"><span data-stu-id="346f5-140">**Note** Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="346f5-141">UE-V peut être configuré pour vérifier que le groupe de l’administrateur local ou l’utilisateur actuel est le propriétaire du dossier dans lequel les packages de paramètres sont stockés.</span><span class="sxs-lookup"><span data-stu-id="346f5-141">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="346f5-142">Pour activer une sécurité supplémentaire, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="346f5-142">To enable additional security complete the following:</span></span>

1.  <span data-ttu-id="346f5-143">Ajoutez une clé de Registre **reg \ _DWORD** nommée «RepositoryOwnerCheckEnabled» dans **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**</span><span class="sxs-lookup"><span data-stu-id="346f5-143">Add a **REG\_DWORD** registry key named "RepositoryOwnerCheckEnabled" to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration.**</span></span>

2.  <span data-ttu-id="346f5-144">Définissez la valeur de clé de Registre sur 1.</span><span class="sxs-lookup"><span data-stu-id="346f5-144">Set registry key value to 1.</span></span>

 

## <span data-ttu-id="346f5-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="346f5-145">Related topics</span></span>


[<span data-ttu-id="346f5-146">Déploiement d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="346f5-146">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="346f5-147">Configurations prises en charge pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="346f5-147">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

<span data-ttu-id="346f5-148">Déploiement de l’espace de stockage central pour l’utilisation de l’interface utilisateur les modèles et packages de paramètres d' [installation du générateur UE-V](installing-the-ue-v-generator.md)</span><span class="sxs-lookup"><span data-stu-id="346f5-148">Deploy the Central Storage for User Experience Virtualization Settings Templates and Settings Packages [Installing the UE-V Generator](installing-the-ue-v-generator.md)</span></span>

[<span data-ttu-id="346f5-149">Déploiement de l'agent UE-V</span><span class="sxs-lookup"><span data-stu-id="346f5-149">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

 

 






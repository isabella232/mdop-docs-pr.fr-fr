---
title: Déploiement du catalogue de modèles de paramètres pour UE-V1.0
description: Déploiement du catalogue de modèles de paramètres pour UE-V1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811873"
---
# <span data-ttu-id="fa0fd-103">Déploiement du catalogue de modèles de paramètres pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="fa0fd-103">Deploying the Settings Template Catalog for UE-V 1.0</span></span>


<span data-ttu-id="fa0fd-104">Les modèles d’emplacement des paramètres personnalisés peuvent être stockés sur le chemin d’accès d’un dossier sur les ordinateurs Microsoft User Interface Virtualization (UE-V) ou sur un partage réseau SMB.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-104">Custom settings location templates can be stored on a folder path on Microsoft User Experience Virtualization (UE-V) computers or on a Server Message Block (SMB) network share.</span></span> <span data-ttu-id="fa0fd-105">Une tâche planifiée sur l’ordinateur vérifie la recherche de modèles nouveaux ou mis à jour à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-105">A scheduled task on the computer checks for new or updated templates from this location.</span></span> <span data-ttu-id="fa0fd-106">La tâche vérifie cet emplacement une fois par jour et met à jour son comportement de synchronisation en fonction des modèles figurant dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-106">The task checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="fa0fd-107">Les modèles ajoutés ou mis à jour dans ce dossier depuis la dernière vérification sont inscrits par l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-107">Templates that are added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="fa0fd-108">UE-V agent annule les modèles supprimés de ce dossier.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-108">The UE-V agent deregisters templates that were removed from this folder.</span></span> <span data-ttu-id="fa0fd-109">La tâche planifiée s’exécute en tant que système.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-109">The scheduled task runs as SYSTEM.</span></span> <span data-ttu-id="fa0fd-110">Au minimum, le partage réseau doit accorder des autorisations pour le groupe ordinateurs du domaine.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-110">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="fa0fd-111">Par ailleurs, accordez des autorisations d’accès au dossier de partage réseau aux administrateurs qui géreront les modèles stockés.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-111">In addition, grant access permissions for the network share folder to administrators who will manage the stored templates.</span></span> <span data-ttu-id="fa0fd-112">Pour plus d’informations sur les modèles d’emplacement des paramètres personnalisés, voir [planification du déploiement de modèles personnalisés pour UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="fa0fd-112">For more information about custom setting location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

**<span data-ttu-id="fa0fd-113">Pour configurer le catalogue de modèles de paramètres pour UE-V</span><span class="sxs-lookup"><span data-stu-id="fa0fd-113">To configure the settings template catalog for UE-V</span></span>**

1.  <span data-ttu-id="fa0fd-114">Créez un dossier sur l’ordinateur qui stockera le catalogue de modèles de paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-114">Create a new folder on the computer that will store the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="fa0fd-115">Définissez les autorisations de niveau de partage (SMB) suivantes pour le dossier du catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-115">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="fa0fd-116">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fa0fd-116">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="fa0fd-117">Recommander des autorisations</span><span class="sxs-lookup"><span data-stu-id="fa0fd-117">Recommend permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fa0fd-118">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="fa0fd-118">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-119">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="fa0fd-119">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fa0fd-120">Ordinateurs de domaine</span><span class="sxs-lookup"><span data-stu-id="fa0fd-120">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-121">Lire les niveaux d’autorisation</span><span class="sxs-lookup"><span data-stu-id="fa0fd-121">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fa0fd-122">Administrateurs</span><span class="sxs-lookup"><span data-stu-id="fa0fd-122">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-123">Niveaux d’autorisation en lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa0fd-123">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="fa0fd-124">Définissez les autorisations NTFS suivantes pour le dossier du catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-124">Set the following NTFS permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="fa0fd-125">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fa0fd-125">User Account</span></span></th>
    <th align="left"><span data-ttu-id="fa0fd-126">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="fa0fd-126">Recommended Permissions</span></span></th>
    <th align="left"><span data-ttu-id="fa0fd-127">Appliquer à</span><span class="sxs-lookup"><span data-stu-id="fa0fd-127">Apply To</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fa0fd-128">Créateur/propriétaire</span><span class="sxs-lookup"><span data-stu-id="fa0fd-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-129">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="fa0fd-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-130">Ce dossier, les sous-dossiers et les fichiers</span><span class="sxs-lookup"><span data-stu-id="fa0fd-130">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fa0fd-131">Ordinateurs de domaine</span><span class="sxs-lookup"><span data-stu-id="fa0fd-131">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-132">Afficher le contenu du dossier et lire</span><span class="sxs-lookup"><span data-stu-id="fa0fd-132">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-133">Ce dossier, les sous-dossiers et les fichiers</span><span class="sxs-lookup"><span data-stu-id="fa0fd-133">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fa0fd-134">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="fa0fd-134">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-135">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="fa0fd-135">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-136">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="fa0fd-136">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fa0fd-137">Administrateurs</span><span class="sxs-lookup"><span data-stu-id="fa0fd-137">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-138">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="fa0fd-138">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa0fd-139">Ce dossier, les sous-dossiers et les fichiers</span><span class="sxs-lookup"><span data-stu-id="fa0fd-139">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="fa0fd-140">Cliquez sur **OK** pour fermer les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fa0fd-140">Click **OK** to close the dialog boxes.</span></span>

## <span data-ttu-id="fa0fd-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa0fd-141">Related topics</span></span>


[<span data-ttu-id="fa0fd-142">Déploiement d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="fa0fd-142">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="fa0fd-143">Planification du déploiement de modèle personnalisé d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="fa0fd-143">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 






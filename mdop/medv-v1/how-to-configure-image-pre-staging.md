---
title: Comment configurer la prédéfinition d'une image
description: Comment configurer la prédéfinition d'une image
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811736"
---
# <span data-ttu-id="165c2-103">Comment configurer la prédéfinition d'une image</span><span class="sxs-lookup"><span data-stu-id="165c2-103">How to Configure Image Pre-staging</span></span>


<span data-ttu-id="165c2-104">**Remarques**  Le préstaging d’image est uniquement utile pour le téléchargement d’image initial.</span><span class="sxs-lookup"><span data-stu-id="165c2-104">**Note** Image pre-staging is useful only for the initial image download.</span></span> <span data-ttu-id="165c2-105">Il n’est pas pris en charge pour la mise à jour des images.</span><span class="sxs-lookup"><span data-stu-id="165c2-105">It is not supported for image update.</span></span>

 

## <span data-ttu-id="165c2-106">Comment configurer la prédéfinition d'une image</span><span class="sxs-lookup"><span data-stu-id="165c2-106">How to Configure Image Pre-staging</span></span>


**<span data-ttu-id="165c2-107">Pour configurer le prédéploiement d’une image</span><span class="sxs-lookup"><span data-stu-id="165c2-107">To configure image pre-staging</span></span>**

1.  <span data-ttu-id="165c2-108">Sur l’ordinateur client, sous le répertoire du magasin d’images, créez un dossier pour l’image de pré-intermédiaire et nommez-la *images MED-V*.</span><span class="sxs-lookup"><span data-stu-id="165c2-108">On the client computer, under the image store directory, create a folder for the pre-staging image, and name it *MED-V Images*.</span></span>

    <span data-ttu-id="165c2-109">**Remarques**  Ce dossier doit être appelé *images MED-V*.</span><span class="sxs-lookup"><span data-stu-id="165c2-109">**Note** This folder must be called *MED-V Images*.</span></span>

     

2.  <span data-ttu-id="165c2-110">Dans le dossier images MED-V, créez un sous-dossier et nommez-le *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="165c2-110">Inside the MED-V Images folder, create a subfolder and name it *PrestagedImages*.</span></span>

    <span data-ttu-id="165c2-111">**Remarques**  Ce dossier doit être appelé *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="165c2-111">**Note** This folder must be called *PrestagedImages*.</span></span>

     

3.  <span data-ttu-id="165c2-112">Pour appliquer la sécurité des listes de contrôle d’accès (ACL) au dossier *images MED-V* , définissez la liste de contrôle d’accès suivante:</span><span class="sxs-lookup"><span data-stu-id="165c2-112">To apply Access Control Lists (ACL) security to the *MED-V Images* folder, set the following ACL:</span></span>

    **<span data-ttu-id="165c2-113">Utilisateurs de AUTHORITY\\Authenticated NT: (OI) (CI) (CI) (accès spécial:)</span><span class="sxs-lookup"><span data-stu-id="165c2-113">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 <span data-ttu-id="165c2-114">FICHIER \ _APPEND \ _DATA</span><span class="sxs-lookup"><span data-stu-id="165c2-114">FILE\_APPEND\_DATA</span></span>**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **<span data-ttu-id="165c2-115">AUTORITE AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="165c2-115">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="165c2-116">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="165c2-116">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="165c2-117">**Remarques**  Nous vous recommandons d’appliquer la sécurité d’ACL au dossier *images MED-V* .</span><span class="sxs-lookup"><span data-stu-id="165c2-117">**Note** It is recommended to apply ACL security to the *MED-V Images* folder.</span></span>

     

4.  <span data-ttu-id="165c2-118">Pour appliquer la sécurité d’ACL au dossier *PrestagedImages* , définissez la liste de contrôle d’accès suivante:</span><span class="sxs-lookup"><span data-stu-id="165c2-118">To apply ACL security to the *PrestagedImages* folder, set the following ACL:</span></span>

    **<span data-ttu-id="165c2-119">Utilisateurs de AUTHORITY\\Authenticated NT: (OI) (CI) (CI) (accès spécial:)</span><span class="sxs-lookup"><span data-stu-id="165c2-119">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

    **<span data-ttu-id="165c2-120">LIRE \ _CONTROL</span><span class="sxs-lookup"><span data-stu-id="165c2-120">READ\_CONTROL</span></span>**

    **<span data-ttu-id="165c2-121">LEURS</span><span class="sxs-lookup"><span data-stu-id="165c2-121">SYNCHRONIZE</span></span>**

    **<span data-ttu-id="165c2-122">FICHIER \ _GENERIC \ _READ</span><span class="sxs-lookup"><span data-stu-id="165c2-122">FILE\_GENERIC\_READ</span></span>**

    **<span data-ttu-id="165c2-123">FICHIER \ _READ \ _DATA</span><span class="sxs-lookup"><span data-stu-id="165c2-123">FILE\_READ\_DATA</span></span>**

    **<span data-ttu-id="165c2-124">FICHIER \ _READ \ _EA</span><span class="sxs-lookup"><span data-stu-id="165c2-124">FILE\_READ\_EA</span></span>**

    **<span data-ttu-id="165c2-125">FICHIER \ _READ \ _ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="165c2-125">FILE\_READ\_ATTRIBUTES</span></span>**

    **<span data-ttu-id="165c2-126">AUTORITE AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="165c2-126">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="165c2-127">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="165c2-127">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="165c2-128">**Remarques**  Nous vous recommandons d’appliquer la sécurité d’ACL au dossier *PrestagedImages*</span><span class="sxs-lookup"><span data-stu-id="165c2-128">**Note** It is recommended to apply ACL security to the *PrestagedImages* folder.</span></span>

     

5.  <span data-ttu-id="165c2-129">Envoyez les fichiers image (CKM et INDEX) dans le dossier *PrestagedImages* .</span><span class="sxs-lookup"><span data-stu-id="165c2-129">Push the image files (CKM and INDEX files) to the *PrestagedImages* folder.</span></span>

    <span data-ttu-id="165c2-130">**Remarques**  Une fois les fichiers image transférés dans le dossier préinstallation, il est recommandé d’exécuter une vérification de l’intégrité des données et de marquer les fichiers en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="165c2-130">**Note** After the image files have been pushed to the pre-stage folder, it is recommended to run a data integrity check and to mark the files as read-only.</span></span>

     

6.  <span data-ttu-id="165c2-131">Incluez le paramètre suivant dans l’installation du client MED-V: *Client.MSI VMSFOLDER = «C:\\MED-V images»*.</span><span class="sxs-lookup"><span data-stu-id="165c2-131">Include the following parameter in the MED-V client installation: *Client.MSI VMSFOLDER=”C:\\MED-V Images”*.</span></span>

## <span data-ttu-id="165c2-132">Comment mettre à jour le lieu de préinstallation</span><span class="sxs-lookup"><span data-stu-id="165c2-132">How to Update the Pre-stage Location</span></span>


**<span data-ttu-id="165c2-133">Pour mettre à jour l’emplacement antérieur</span><span class="sxs-lookup"><span data-stu-id="165c2-133">To update the pre-stage location</span></span>**

1.  <span data-ttu-id="165c2-134">La clé de Registre *PrestagedImagesPath*, qui pointe vers l’emplacement d’image par défaut.</span><span class="sxs-lookup"><span data-stu-id="165c2-134">The registry key, *PrestagedImagesPath*, points to the default image location.</span></span> <span data-ttu-id="165c2-135">Il se trouve dans le répertoire suivant:</span><span class="sxs-lookup"><span data-stu-id="165c2-135">It is located in the following directory:</span></span>

    -   <span data-ttu-id="165c2-136">Sur un ordinateur x86-</span><span class="sxs-lookup"><span data-stu-id="165c2-136">On an x86 -</span></span> `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   <span data-ttu-id="165c2-137">Sur un x64-</span><span class="sxs-lookup"><span data-stu-id="165c2-137">On an x64 -</span></span> `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  <span data-ttu-id="165c2-138">Si l’image se trouve dans un autre emplacement, modifiez le chemin.</span><span class="sxs-lookup"><span data-stu-id="165c2-138">If the image is in a different location, change the path.</span></span>

 

 






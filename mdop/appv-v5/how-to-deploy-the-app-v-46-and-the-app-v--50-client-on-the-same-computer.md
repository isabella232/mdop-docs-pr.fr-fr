---
title: Déploiement de l’application-V 4,6 et du client App-V 5,0 sur le même ordinateur
description: Déploiement de l’application-V 4,6 et du client App-V 5,0 sur le même ordinateur
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805533"
---
# <span data-ttu-id="38092-103">Déploiement de l’application-V 4,6 et du client App-V 5,0 sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="38092-103">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>

<span data-ttu-id="38092-104">**Remarque:** App-V 4,6 a quitté le support technique standard.</span><span class="sxs-lookup"><span data-stu-id="38092-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="38092-105">L’exemple suivant suppose que le client App-V 4,6 SP3 est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="38092-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="38092-106">Utilisez les informations suivantes pour installer le client App-V 5,0 (de préférence, avec les derniers Service Packs et correctifs) et le client App-V 4.6 SP3 sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="38092-106">Use the following information to install the App-V 5.0 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP3 client on the same computer.</span></span> <span data-ttu-id="38092-107">Pour plus d’informations sur les versions prises en charge, les configurations requises et d’autres informations de planification, voir [planification de la migration à partir d’une version antérieure d’App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="38092-107">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span></span>

**<span data-ttu-id="38092-108">Pour déployer le client App-V 5,0 et le client App-V 4,6 sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="38092-108">To deploy the App-V 5.0 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="38092-109">Installez le client App-V 5,0 SP3 sur l’ordinateur exécutant la version App-V 4,6 du client.</span><span class="sxs-lookup"><span data-stu-id="38092-109">Install the App-V 5.0 SP3 client on the computer that is running the App-V 4.6 version of the client.</span></span> <span data-ttu-id="38092-110">Pour obtenir de meilleurs résultats, nous vous recommandons d’installer toutes les mises à jour disponibles sur le client App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="38092-110">For best results, we recommend that you install all available updates to the App-V 5.0 SP3 client.</span></span>

2.  <span data-ttu-id="38092-111">Convertissez ou réexécutez progressivement les packages.</span><span class="sxs-lookup"><span data-stu-id="38092-111">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="38092-112">Pour convertir les packages, utilisez le convertisseur de package App-V 5,0, puis convertissez les packages requis au format App-V 5,0 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="38092-112">To convert the packages, use the App-V 5.0 package converter and convert the required packages to the App-V 5.0 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="38092-113">Pour réorganiser les packages, envisagez d’utiliser la dernière version du Sequencer pour obtenir de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="38092-113">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="38092-114">Pour plus d’informations sur les packages de publication, voir [Comment publier un package à l’aide de la console de gestion](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="38092-114">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

3.  <span data-ttu-id="38092-115">Déploiement de packages sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="38092-115">Deploy packages to the client computers.</span></span>

4.  <span data-ttu-id="38092-116">Convertissez les points d’extension selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="38092-116">Convert extension points, as needed.</span></span> <span data-ttu-id="38092-117">Pour plus d’informations, voir les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="38092-117">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="38092-118">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 converti pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="38092-118">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="38092-119">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="38092-119">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [<span data-ttu-id="38092-120">Comment convertir un package créé dans une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="38092-120">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  <span data-ttu-id="38092-121">Testez la réussite de vos packages App-V 5,0, puis supprimez les packages 4,6.</span><span class="sxs-lookup"><span data-stu-id="38092-121">Test that your App-V 5.0 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="38092-122">Pour vérifier l’état de l’utilisateur sur vos ordinateurs clients, nous vous recommandons d’utiliser [la virtualisation de l’interface utilisateur](https://technet.microsoft.com/library/dn458947.aspx) ou un autre outil de gestion de l’environnement des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="38092-122">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="38092-123">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="38092-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="38092-124">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="38092-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="38092-125">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="38092-125">Got an App-V issue?</span></span>** <span data-ttu-id="38092-126">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="38092-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="38092-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38092-127">Related topics</span></span>


[<span data-ttu-id="38092-128">Planification d'une migration à partir d'une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="38092-128">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v.md)

[<span data-ttu-id="38092-129">Déploiement d'App-V5.0 Sequencer et Client</span><span class="sxs-lookup"><span data-stu-id="38092-129">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 






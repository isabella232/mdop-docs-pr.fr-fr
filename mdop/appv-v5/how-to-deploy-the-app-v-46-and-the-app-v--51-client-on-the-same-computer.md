---
title: Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur
description: Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805527"
---
# <span data-ttu-id="f7b40-103">Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="f7b40-103">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>

<span data-ttu-id="f7b40-104">**Remarque:** App-V 4,6 a quitté le support technique standard.</span><span class="sxs-lookup"><span data-stu-id="f7b40-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="f7b40-105">Utilisez les informations ci-dessous pour installer le client Microsoft Application Virtualization (App-V) 5,1 (de préférence avec les derniers Service Packs et correctifs) et le client App-V 4.6 SP2 ou le client App-V 4.6 S3 sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f7b40-105">Use the following information to install the Microsoft Application Virtualization (App-V) 5.1 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP2 client or the App-V 4.6S3 client on the same computer.</span></span> <span data-ttu-id="f7b40-106">Pour plus d’informations sur les versions prises en charge, les configurations requises et d’autres informations de planification, voir [planification de la migration à partir d’une version antérieure d’App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="f7b40-106">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span></span>

**<span data-ttu-id="f7b40-107">Pour déployer le client App-V 5,1 et le client App-V 4,6 sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="f7b40-107">To deploy the App-V 5.1 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="f7b40-108">Installez la version suivante du client App-V sur l’ordinateur exécutant App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="f7b40-108">Install the following version of the App-V client on the computer that is running App-V 4.6.</span></span>

    -   [<span data-ttu-id="f7b40-109">Microsoft Application Virtualization 4,6 Service Pack 3</span><span class="sxs-lookup"><span data-stu-id="f7b40-109">Microsoft Application Virtualization 4.6 Service Pack 3</span></span>](https://www.microsoft.com/download/details.aspx?id=41187)

2.  <span data-ttu-id="f7b40-110">Installez le client App-V 5,1 sur l’ordinateur exécutant la version App-V 4,6 SP3 du client.</span><span class="sxs-lookup"><span data-stu-id="f7b40-110">Install the App-V 5.1 client on the computer that is running the App-V 4.6 SP3 version of the client.</span></span> <span data-ttu-id="f7b40-111">Pour obtenir de meilleurs résultats, nous vous recommandons d’installer toutes les mises à jour disponibles sur le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f7b40-111">For best results, we recommend that you install all available updates to the App-V 5.1 client.</span></span>

3.  <span data-ttu-id="f7b40-112">Convertissez ou réexécutez progressivement les packages.</span><span class="sxs-lookup"><span data-stu-id="f7b40-112">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="f7b40-113">Pour convertir les packages, utilisez le convertisseur de package App-V 5,1, puis convertissez les packages requis au format App-V 5,1 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="f7b40-113">To convert the packages, use the App-V 5.1 package converter and convert the required packages to the App-V 5.1 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="f7b40-114">Pour réorganiser les packages, envisagez d’utiliser la dernière version du Sequencer pour obtenir de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="f7b40-114">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="f7b40-115">Pour plus d’informations sur les packages de publication, voir [Comment publier un package à l’aide de la console de gestion](how-to-publish-a-package-by-using-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="f7b40-115">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md).</span></span>

4.  <span data-ttu-id="f7b40-116">Déploiement de packages sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="f7b40-116">Deploy packages to the client computers.</span></span>

5.  <span data-ttu-id="f7b40-117">Convertissez les points d’extension selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="f7b40-117">Convert extension points, as needed.</span></span> <span data-ttu-id="f7b40-118">Pour plus d’informations, voir les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7b40-118">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="f7b40-119">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f7b40-119">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="f7b40-120">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f7b40-120">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [<span data-ttu-id="f7b40-121">Comment convertir un package créé dans une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="f7b40-121">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  <span data-ttu-id="f7b40-122">Testez la réussite de vos packages App-V 5,1, puis supprimez les packages 4,6.</span><span class="sxs-lookup"><span data-stu-id="f7b40-122">Test that your App-V 5.1 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="f7b40-123">Pour vérifier l’état de l’utilisateur sur vos ordinateurs clients, nous vous recommandons d’utiliser [la virtualisation de l’interface utilisateur](https://technet.microsoft.com/library/dn458947.aspx) ou un autre outil de gestion de l’environnement des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f7b40-123">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="f7b40-124">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="f7b40-124">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f7b40-125">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="f7b40-125">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f7b40-126">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="f7b40-126">Got an App-V issue?</span></span>** <span data-ttu-id="f7b40-127">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f7b40-127">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f7b40-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7b40-128">Related topics</span></span>


[<span data-ttu-id="f7b40-129">Planification d'une migration à partir d'une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="f7b40-129">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[<span data-ttu-id="f7b40-130">Planification du déploiement d'App-V5.1 Sequencer et Client</span><span class="sxs-lookup"><span data-stu-id="f7b40-130">Deploying the App-V 5.1 Sequencer and Client</span></span>](deploying-the-app-v-51-sequencer-and-client.md)

 

 






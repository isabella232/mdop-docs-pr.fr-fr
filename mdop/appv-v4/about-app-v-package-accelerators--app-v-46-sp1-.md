---
title: À propos des accélérateurs de package App-V (App-V4.6 SP1)
description: À propos des accélérateurs de package App-V (App-V4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808169"
---
# <span data-ttu-id="c5ee6-103">À propos des accélérateurs de package App-V (App-V4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="c5ee6-103">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="c5ee6-104">Vous pouvez utiliser les accélérateurs de package App-V pour effectuer une séquence automatique de grandes applications complexes.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-104">You can use App-V Package Accelerators to automatically sequence large, complex applications.</span></span> <span data-ttu-id="c5ee6-105">Par ailleurs, lorsque vous appliquez un accélérateur de package App-V, il n’est pas toujours nécessaire d’installer manuellement une application pour créer le package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-105">Additionally, when you apply an App-V Package Accelerator, you are not always required to manually install an application to create the virtual application package.</span></span>

<span data-ttu-id="c5ee6-106">**Remarques**  Dans certains cas, vous êtes invité à installer une application localement sur l’ordinateur exécutant le Sequencer App-V avant de pouvoir utiliser l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-106">**Note** In some cases, you are prompted to install an application locally to the computer running the App-V Sequencer before you can use the Package Accelerator.</span></span> <span data-ttu-id="c5ee6-107">Si vous devez installer une application, vous devez installer l’application à l’emplacement par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-107">If you have to install an application, you must install the application to the application’s default location.</span></span> <span data-ttu-id="c5ee6-108">Cette installation n’est pas gérée par le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-108">This installation is not monitored by App-V Sequencer.</span></span> <span data-ttu-id="c5ee6-109">Lorsque l’accélérateur de package App-V est créé, l’auteur de l’accélérateur de package détermine s’il est nécessaire d’installer une application localement.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-109">When the App-V Package Accelerator is created, the author of the Package Accelerator determines whether to install an application locally is required.</span></span>

 

<span data-ttu-id="c5ee6-110">Le Sequencer App-V extrait les fichiers requis de l’accélérateur de package App-V et du support d’installation associé pour créer un package virtuel sans avoir à surveiller l’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-110">App-V Sequencer extracts the required files from the App-V Package Accelerator and associated installation media to create a virtual package without having to monitor the installation of the application.</span></span>

<span data-ttu-id="c5ee6-111">**Important**  Exclusion de responsabilité: le Sequencer Microsoft Application Virtualization ne vous donne aucun droit de licence pour l’application logicielle que vous utilisez pour créer un accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-111">**Important** Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="c5ee6-112">Vous devez respecter les conditions générales du contrat de licence utilisateur final pour une telle application.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-112">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="c5ee6-113">Il est de votre responsabilité de veiller à ce que les termes du contrat de licence de l’application logicielle vous permettent de créer un accélérateur de package à l’aide du Sequencer de la virtualisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-113">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>

 

<span data-ttu-id="c5ee6-114">Les accélérateurs et les modèles de projet App-V diffèrent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-114">App-V Package Accelerators and project templates differ from each other.</span></span> <span data-ttu-id="c5ee6-115">Les accélérateurs de package sont propres à l’application.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-115">Package Accelerators are application-specific.</span></span> <span data-ttu-id="c5ee6-116">Les modèles Project permettent aux utilisateurs d’enregistrer les paramètres fréquemment utilisés spécifiques à une organisation et de les appliquer à plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-116">Project templates enable users to save commonly used settings specific to an organization and apply them to multiple applications.</span></span> <span data-ttu-id="c5ee6-117">Vous pouvez également créer des modèles de projet à l’invite de commandes, en revanche, vous devez utiliser la console de Sequencer App-V pour créer des accélérateurs de package.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-117">You can also create project templates at the command prompt, while in contrast, you must use the App-V Sequencer console to create Package Accelerators.</span></span> <span data-ttu-id="c5ee6-118">En outre, la création d’un package à l’aide d’un accélérateur de package et l’application d’un modèle de projet ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-118">Additionally, creating a package by using a Package Accelerator and applying a project template is not supported.</span></span>

## <span data-ttu-id="c5ee6-119">Partage d’application-V package Accelerators</span><span class="sxs-lookup"><span data-stu-id="c5ee6-119">Sharing App-V Package Accelerators</span></span>


<span data-ttu-id="c5ee6-120">Cette section fournit des informations pratiques recommandées sur le partage des accélérateurs de package.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-120">This section provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="c5ee6-121">Si vous envisagez de partager des accélérateurs de package, des informations telles que les noms d’ordinateur, les informations de compte d’utilisateur et les informations relatives aux applications associées peuvent être incluses dans les accélérateurs de package. la liste suivante décrit les méthodes que vous devez prendre en compte lors de la création d’accélérateurs de package:</span><span class="sxs-lookup"><span data-stu-id="c5ee6-121">If you plan to share Package Accelerators, information such as computer names, user account information, and information about the associated applications might be included in the Package Accelerators.The following list describes methods you should consider when creating Package Accelerators:</span></span>

-   <span data-ttu-id="c5ee6-122">**Nom d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-122">**User name**.</span></span> <span data-ttu-id="c5ee6-123">Lorsque vous ouvrez une session sur l’ordinateur exécutant le Sequencer App-V, vous devez utiliser un compte utilisateur générique, tel que le compte d' **administrateur** intégré pour l’administration de l’ordinateur/domaine.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-123">When you log on to the computer running App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account for administering the computer / domain.</span></span> <span data-ttu-id="c5ee6-124">Vous ne devez pas utiliser un compte basé sur un nom d’utilisateur existant.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-124">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="c5ee6-125">**Nom**de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-125">**Computer Name**.</span></span> <span data-ttu-id="c5ee6-126">Spécifiez un nom général et non identifiant de l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-126">Specify a general, non-identifying name for the computer running the Sequencer.</span></span>

-   <span data-ttu-id="c5ee6-127">**URL du serveur**.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-127">**Server URL**.</span></span> <span data-ttu-id="c5ee6-128">Dans l’onglet **déploiement** de la console de Sequencer, utilisez les paramètres par défaut pour les informations sur la configuration de l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-128">In the Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="c5ee6-129">**Applications**.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-129">**Applications**.</span></span> <span data-ttu-id="c5ee6-130">Si vous ne voulez pas partager la liste des applications installées sur l’ordinateur exécutant le Sequencer lors de la création de l’accélérateur de package, vous devez supprimer le fichier **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="c5ee6-130">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="c5ee6-131">Ce fichier se trouve dans le répertoire racine du package du package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-131">This file is located in the package root directory of the virtual application package.</span></span>

<span data-ttu-id="c5ee6-132">Vous devez également consulter les paramètres ou les fichiers de configuration associés au package d’application virtuelle pour vous assurer que les applications ne contiennent aucune information personnelle.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-132">You should also review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.</span></span>

## <span data-ttu-id="c5ee6-133">Sécurisation des accélérateurs de package App-V</span><span class="sxs-lookup"><span data-stu-id="c5ee6-133">Securing App-V Package Accelerators</span></span>


<span data-ttu-id="c5ee6-134">Enregistrez toujours les accélérateurs de packages App-V et tout support d’installation associé à un emplacement sécurisé sur le réseau pour protéger les accélérateurs d’application et les fichiers d’installation contre la falsification ou la corruption.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-134">Always save App-V Package Accelerators and any associated installation media in a secure location on the network to protect the App-V Package Accelerators and the installation files from being tampered with or becoming corrupted.</span></span> <span data-ttu-id="c5ee6-135">Étant donné que les accélérateurs de package peuvent également contenir des informations relatives au mot de passe et à l’utilisateur, vous devez enregistrer les accélérateurs d’applications-V dans un emplacement sécurisé, et vous devez signer numériquement l’accélérateur de package après l’avoir créé, afin que l’éditeur puisse être vérifié lorsque l’accélérateur de package est appliqué.</span><span class="sxs-lookup"><span data-stu-id="c5ee6-135">Because Package Accelerators can also contain password and user-specific information, you must save App-V Package Accelerators in a secure location, and you must digitally sign the Package Accelerator after you create it so that the publisher can be verified when the Package Accelerator is applied.</span></span> <span data-ttu-id="c5ee6-136">Pour plus d’informations sur les signatures numériques, voir [recommandations en matière de signature numérique pour la sécurité des critères communs](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .</span><span class="sxs-lookup"><span data-stu-id="c5ee6-136">For more information about digital signatures, see [Application Guidelines on Digital Signature Practices for Common Criteria Security](https://go.microsoft.com/fwlink/?LinkId=204705) (https://go.microsoft.com/fwlink/?LinkId=204705).</span></span>

## <span data-ttu-id="c5ee6-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5ee6-137">Related topics</span></span>


[<span data-ttu-id="c5ee6-138">Procédure pour créer des accélérateurs de package App-V (App-V4.6SP1)</span><span class="sxs-lookup"><span data-stu-id="c5ee6-138">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[<span data-ttu-id="c5ee6-139">Comment appliquer un accélérateur de package pour créer un package d’application virtuelle (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="c5ee6-139">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 






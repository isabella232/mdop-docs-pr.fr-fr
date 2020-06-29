---
title: Page À propos du partage d'accélérateurs de package
description: Page À propos du partage d'accélérateurs de package
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808129"
---
# <span data-ttu-id="b83e9-103">Page À propos du partage d'accélérateurs de package</span><span class="sxs-lookup"><span data-stu-id="b83e9-103">About Sharing Package Accelerators Page</span></span>


<span data-ttu-id="b83e9-104">Les informations suivantes fournissent des informations pratiques recommandées sur le partage des accélérateurs de package.</span><span class="sxs-lookup"><span data-stu-id="b83e9-104">This following information provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="b83e9-105">Si vous envisagez de partager des fichiers accélérateurs de package, des informations telles que les noms d’ordinateur, les informations de compte d’utilisateur et les informations relatives aux applications incluses dans les transformations peuvent être incluses dans le fichier accélérateurs de package.</span><span class="sxs-lookup"><span data-stu-id="b83e9-105">If you plan to share Package Accelerators files, information such as computer names, user account information, and information about applications included in the transforms might be included in the Package Accelerators file.</span></span> <span data-ttu-id="b83e9-106">Vous devez examiner les paramètres ou les fichiers de configuration associés au package d’application virtuelle pour vous assurer que les applications ne contiennent aucune information personnelle. Cette page contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="b83e9-106">You should review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.This page contains the following elements.</span></span>

-   <span data-ttu-id="b83e9-107">**Nom d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="b83e9-107">**Username**.</span></span> <span data-ttu-id="b83e9-108">Lorsque vous ouvrez une session sur l’ordinateur exécutant le Sequencer Microsoft App-V, vous devez utiliser un compte utilisateur générique, tel que le compte d' **administrateur** intégré.</span><span class="sxs-lookup"><span data-stu-id="b83e9-108">When you log on to the computer running the Microsoft App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account.</span></span> <span data-ttu-id="b83e9-109">Vous ne devez pas utiliser un compte basé sur un nom d’utilisateur existant.</span><span class="sxs-lookup"><span data-stu-id="b83e9-109">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="b83e9-110">**Nom**de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b83e9-110">**Computer Name**.</span></span> <span data-ttu-id="b83e9-111">Spécifiez un nom général et non identifiant de l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="b83e9-111">Specify a general, non-identifying name of the computer running the Sequencer.</span></span>

-   <span data-ttu-id="b83e9-112">**URL du serveur**.</span><span class="sxs-lookup"><span data-stu-id="b83e9-112">**Server URL**.</span></span> <span data-ttu-id="b83e9-113">Dans la console App-V Sequencer, dans l’onglet **déploiement** , utilisez les paramètres par défaut pour les informations sur la configuration de l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="b83e9-113">In the App-V Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="b83e9-114">**Applications**.</span><span class="sxs-lookup"><span data-stu-id="b83e9-114">**Applications**.</span></span> <span data-ttu-id="b83e9-115">Si vous ne voulez pas partager la liste des applications installées sur l’ordinateur exécutant le Sequencer lors de la création de l’accélérateur de package, vous devez supprimer le fichier **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="b83e9-115">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="b83e9-116">Ce fichier se trouve dans le répertoire racine du package du package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="b83e9-116">This file is located in the package root directory of the virtual application package.</span></span>

## <span data-ttu-id="b83e9-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b83e9-117">Related topics</span></span>


[<span data-ttu-id="b83e9-118">Assistant Créer un accélérateur de package (AppV4.6SP1)</span><span class="sxs-lookup"><span data-stu-id="b83e9-118">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

[<span data-ttu-id="b83e9-119">À propos des accélérateurs de package App-V (App-V4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="b83e9-119">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 






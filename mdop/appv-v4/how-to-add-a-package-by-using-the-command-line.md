---
title: Procédure d'ajout d'un package à l'aide de la ligne de commande
description: Procédure d'ajout d'un package à l'aide de la ligne de commande
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808736"
---
# <span data-ttu-id="017a5-103">Procédure d'ajout d'un package à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="017a5-103">How to Add a Package by Using the Command Line</span></span>


<span data-ttu-id="017a5-104">Les procédures suivantes répertorient les étapes nécessaires à l’ajout d’un package d’application virtuel au client Application Virtualization (App-V) sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="017a5-104">The following procedures list the steps that are necessary to add a virtual application package to the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="017a5-105">Pour ajouter un package d’application virtuel pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="017a5-105">To add a virtual application package for a specific user</span></span>**

-   <span data-ttu-id="017a5-106">Exécutez la commande suivante sous le compte d’utilisateur de la personne qui doit obtenir le package.</span><span class="sxs-lookup"><span data-stu-id="017a5-106">Run the following command under the user account of the person who is to get the package.</span></span> <span data-ttu-id="017a5-107">La commande ajoute et publie le package pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="017a5-107">The command adds and publishes the package for that user.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**<span data-ttu-id="017a5-108">Pour ajouter un package d’application virtuel pour tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="017a5-108">To add a virtual application package for all users</span></span>**

-   <span data-ttu-id="017a5-109">Exécutez la commande suivante sous un compte disposant de droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="017a5-109">Run the following command under an account that has administrator rights.</span></span> <span data-ttu-id="017a5-110">Le package est ajouté et publié pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="017a5-110">The package is added and published for all users on the computer.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**<span data-ttu-id="017a5-111">Pour ajouter un package à l’aide d’un système de distribution de logiciels électronique</span><span class="sxs-lookup"><span data-stu-id="017a5-111">To add a package using an electronic software distribution system</span></span>**

1.  <span data-ttu-id="017a5-112">Si vous utilisez un système de distribution de logiciels électronique qui exécute les commandes sous le compte **système** de l’ordinateur, le package est publié uniquement pour ce compte, sauf si vous utilisez le commutateur/global.</span><span class="sxs-lookup"><span data-stu-id="017a5-112">If you are using an electronic software distribution system that runs the commands under the computer’s **SYSTEM** account, the package is published for that account only, unless you use the /GLOBAL switch.</span></span> <span data-ttu-id="017a5-113">Exécutez la commande suivante pour ajouter et publier le package pour tous les utilisateurs sur l’ordinateur:</span><span class="sxs-lookup"><span data-stu-id="017a5-113">Run the following command to add and publish the package for all users on the computer:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    <span data-ttu-id="017a5-114">Si vous souhaitez ajouter le package uniquement pour des utilisateurs spécifiques, exécutez la commande **Ajouter un package** , puis publiez explicitement le package pour chaque utilisateur en exécutant la commande de publication de **package** suivante sous le compte d’utilisateur de chaque personne:</span><span class="sxs-lookup"><span data-stu-id="017a5-114">If you want to add the package for specific users only, run the **ADD PACKAGE** command, and then explicitly publish the package for each user by running the following **PUBLISH PACKAGE** command under each person’s user account:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    <span data-ttu-id="017a5-115">La publication du package sans le paramètre GLOBAL autorise l’accès de l’utilisateur aux applications du package et publie les types de fichiers et les raccourcis répertoriés dans le manifeste dans le profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="017a5-115">Publishing the package without the GLOBAL parameter grants the user access to the applications in the package and publishes the file types and shortcuts that are listed in the manifest to the user’s profile.</span></span> <span data-ttu-id="017a5-116">Les autorisations requises sont «gérer les associations de types de fichiers» (**ManageTypes**) et «publier des raccourcis» (**PublishShortcut**).</span><span class="sxs-lookup"><span data-stu-id="017a5-116">Permissions required are “Manage file type associations” (**ManageTypes**) and “Publish shortcuts” (**PublishShortcut**).</span></span>

## <span data-ttu-id="017a5-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="017a5-117">Related topics</span></span>


[<span data-ttu-id="017a5-118">Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="017a5-118">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[<span data-ttu-id="017a5-119">Procédure de suppression d'un package à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="017a5-119">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 






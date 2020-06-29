---
title: Procédure de suppression d'un package à l'aide de la ligne de commande
description: Procédure de suppression d'un package à l'aide de la ligne de commande
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806861"
---
# <span data-ttu-id="28bd8-103">Procédure de suppression d'un package à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="28bd8-103">How to Remove a Package by Using the Command Line</span></span>


<span data-ttu-id="28bd8-104">Vous pouvez utiliser les procédures de ligne de commande suivantes pour supprimer un package d’application virtuel du client Application Virtualization (App-V) sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="28bd8-104">You can use the following command-line procedures to delete a virtual application package from the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="28bd8-105">Pour supprimer un package d’application virtuel pour tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="28bd8-105">To delete a virtual application package for all users</span></span>**

-   <span data-ttu-id="28bd8-106">Si le package a été précédemment ajouté pour tous les utilisateurs à l’aide du commutateur/GLOBAL, utilisez la commande suivante pour supprimer le package ainsi que les types de fichiers et raccourcis globaux.</span><span class="sxs-lookup"><span data-stu-id="28bd8-106">If the package was previously added for all users by using the /GLOBAL switch, use the following command to delete the package and the global file types and shortcuts.</span></span> <span data-ttu-id="28bd8-107">Vous devez disposer des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="28bd8-107">Administrator rights are required.</span></span> <span data-ttu-id="28bd8-108">Le commutateur/GLOBAL n’est pas nécessaire dans ce cas, car la commande effectue toujours une suppression globale du package.</span><span class="sxs-lookup"><span data-stu-id="28bd8-108">The /GLOBAL switch is not needed in this case because the command always performs a global deletion of the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

**<span data-ttu-id="28bd8-109">Pour supprimer un package déjà ajouté pour des utilisateurs individuels</span><span class="sxs-lookup"><span data-stu-id="28bd8-109">To delete a package previously added for individual users</span></span>**

1.  <span data-ttu-id="28bd8-110">Si le package a déjà été ajouté pour des utilisateurs individuels, plusieurs options s’offrent à vous.</span><span class="sxs-lookup"><span data-stu-id="28bd8-110">If the package was previously added for individual users, you have several options.</span></span>

    <span data-ttu-id="28bd8-111">Exécutez la commande suivante une fois sous le compte d’utilisateur de chaque personne à laquelle le package a été publié.</span><span class="sxs-lookup"><span data-stu-id="28bd8-111">Run the following command once under the user account of each person the package was published to.</span></span> <span data-ttu-id="28bd8-112">Ainsi, l’utilisateur n’a pas accès aux applications s’il effectue une itinérance sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="28bd8-112">This denies the user access to the applications if they roam to another computer.</span></span> <span data-ttu-id="28bd8-113">Il supprime les paramètres de l’utilisateur, les raccourcis et les types de fichiers spécifiques du profil, et arrête les chargements en arrière-plan dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="28bd8-113">It deletes the specific user’s settings, shortcuts, and file types from the profile, and it stops background loads under the user’s context.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  <span data-ttu-id="28bd8-114">Vous pouvez également exécuter la commande suivante sous le compte d’utilisateur de chaque personne à laquelle le package a été publié.</span><span class="sxs-lookup"><span data-stu-id="28bd8-114">Alternatively, run the following command under the user account of each person the package was published to.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    <span data-ttu-id="28bd8-115">Ensuite, exécutez cette commande pour le package.</span><span class="sxs-lookup"><span data-stu-id="28bd8-115">Then run this command for the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

    <span data-ttu-id="28bd8-116">Le package est alors entièrement supprimé et les paramètres de l’utilisateur, les raccourcis et les types de fichiers sont supprimés de leur profil.</span><span class="sxs-lookup"><span data-stu-id="28bd8-116">This completely removes the package, and it deletes all user settings, shortcuts, and file types from their profiles.</span></span> <span data-ttu-id="28bd8-117">Si le package est ensuite rajouté, les utilisateurs devront spécifier de nouveau leurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="28bd8-117">If the package is subsequently re-added, the users will have to specify their settings again.</span></span> <span data-ttu-id="28bd8-118">Seule l’autorisation «Delete applications» (**DeleteApp**) est nécessaire pour exécuter cette commande.</span><span class="sxs-lookup"><span data-stu-id="28bd8-118">Only “Delete applications” (**DeleteApp**) permission is needed to run this command.</span></span>

3.  <span data-ttu-id="28bd8-119">À la place, vous pouvez simplement exécuter la commande **supprimer le package** sans utiliser la commande annuler la **publication du package** .</span><span class="sxs-lookup"><span data-stu-id="28bd8-119">As a third alternative, you can simply run the **DELETE PACKAGE** command without using the **UNPUBLISH PACKAGE** command.</span></span> <span data-ttu-id="28bd8-120">Dans ce cas, les types de fichiers et les raccourcis pour chaque utilisateur sont masqués plutôt que supprimés, et les paramètres de l’utilisateur sont conservés.</span><span class="sxs-lookup"><span data-stu-id="28bd8-120">In this case, file types and shortcuts for each user are hidden rather than deleted, and the user settings are retained.</span></span> <span data-ttu-id="28bd8-121">Cela signifie que si le package est ensuite rajouté pour l’utilisateur, les types de fichiers et les raccourcis sont restaurés et les paramètres de l’utilisateur sont réappliqués.</span><span class="sxs-lookup"><span data-stu-id="28bd8-121">This means that if the package is subsequently re-added for the user, the file types and shortcuts are restored, and the user settings are reapplied.</span></span>

## <span data-ttu-id="28bd8-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28bd8-122">Related topics</span></span>


[<span data-ttu-id="28bd8-123">Procédure d'ajout d'un package à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="28bd8-123">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="28bd8-124">Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="28bd8-124">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 






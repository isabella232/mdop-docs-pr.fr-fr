---
title: Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande
description: Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807146"
---
# <span data-ttu-id="76a2d-103">Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="76a2d-103">How to Delete All Virtual Applications by Using the Command Line</span></span>


<span data-ttu-id="76a2d-104">Vous pouvez utiliser la procédure suivante pour supprimer toutes les applications virtuelles d’un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="76a2d-104">You can use the following procedure to delete all virtual applications from a specific computer.</span></span>

<span data-ttu-id="76a2d-105">**Remarques**  Lorsque toutes les applications sont supprimées d’un package, le client Application Virtualization (App-V) supprime également le package.</span><span class="sxs-lookup"><span data-stu-id="76a2d-105">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

 

**<span data-ttu-id="76a2d-106">Pour supprimer toutes les applications</span><span class="sxs-lookup"><span data-stu-id="76a2d-106">To delete all applications</span></span>**

-   <span data-ttu-id="76a2d-107">Exécutez la commande suivante pour supprimer toutes les applications du compte d’utilisateur sous lequel la commande est exécutée.</span><span class="sxs-lookup"><span data-stu-id="76a2d-107">Run the following command to delete all applications for the user account under which the command is run.</span></span> <span data-ttu-id="76a2d-108">Si vous exécutez la commande avec le commutateur/GLOBAL facultatif, en utilisant un compte disposant de droits d’administration, toutes les applications sont supprimées pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="76a2d-108">If you run the command with the optional /GLOBAL switch, using an account with administrative rights, all applications are deleted for all users.</span></span>

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    <span data-ttu-id="76a2d-109">**Remarques**  Lorsque toutes les applications sont supprimées d’un package, le client Application Virtualization (App-V) supprime également le package.</span><span class="sxs-lookup"><span data-stu-id="76a2d-109">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

     

## <span data-ttu-id="76a2d-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76a2d-110">Related topics</span></span>


[<span data-ttu-id="76a2d-111">Procédure d'ajout d'un package à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="76a2d-111">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="76a2d-112">Procédure de suppression d'un package à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="76a2d-112">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 






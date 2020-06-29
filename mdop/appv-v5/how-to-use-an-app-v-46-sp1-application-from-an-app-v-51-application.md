---
title: Utiliser une application application-V 4,6 à partir d’une application App-V 5,1
description: Utiliser une application application-V 4,6 à partir d’une application App-V 5,1
author: dansimp
ms.assetid: 909b4391-762b-4988-b0cf-32b67f1fcf0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: c0d308dcae33b02c089c101ffcd5041b2e665f59
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805125"
---
# <span data-ttu-id="f4479-103">Utiliser une application application-V 4,6 à partir d’une application App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="f4479-103">How to Use an App-V 4.6 Application From an App-V 5.1 Application</span></span>

<span data-ttu-id="f4479-104">*Remarque:*\* App-V 4,6 a quitté la version standard du support technique.</span><span class="sxs-lookup"><span data-stu-id="f4479-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="f4479-105">Les éléments suivants s’appliquent à un package App-V 4,6 SP3.</span><span class="sxs-lookup"><span data-stu-id="f4479-105">The following applies to an App-V 4.6 SP3 package.</span></span>

<span data-ttu-id="f4479-106">Utilisez la procédure suivante pour exécuter une application App-V 4.6 avec des applications App-V 5,1 sur un client autonome.</span><span class="sxs-lookup"><span data-stu-id="f4479-106">Use the following procedure to run an App-V4.6 application with App-V 5.1 applications on a standalone client.</span></span>

<span data-ttu-id="f4479-107">**Remarques**  Cette procédure suppose que vous utilisez la dernière version de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="f4479-107">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>

**<span data-ttu-id="f4479-108">Pour exécuter des applications sur un client autonome</span><span class="sxs-lookup"><span data-stu-id="f4479-108">To run applications on a standalone client</span></span>**

1.  <span data-ttu-id="f4479-109">Sélectionnez deux applications dans votre environnement qui peuvent être ouvertes les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="f4479-109">Select two applications in your environment that can be opened from one another.</span></span> <span data-ttu-id="f4479-110">Par exemple, Microsoft Outlook et Adobe Acrobat Reader.</span><span class="sxs-lookup"><span data-stu-id="f4479-110">For example, Microsoft Outlook and Adobe Acrobat Reader.</span></span> <span data-ttu-id="f4479-111">Vous pouvez accéder à une pièce jointe de message électronique créée à l’aide d’Adobe Acrobat.</span><span class="sxs-lookup"><span data-stu-id="f4479-111">You can access an email attachment created using Adobe Acrobat.</span></span>

2.  <span data-ttu-id="f4479-112">Convertir les packages, ou créer un package pour l’une de ces applications à l’aide du format App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f4479-112">Convert the packages, or create a new package for either of the applications using the App-V 5.1 format.</span></span> <span data-ttu-id="f4479-113">Pour plus d’informations sur la conversion des packages, voir [Comment migrer des points d’extension d’un package App-v 4,6 vers un package App-v 5,1 pour tous les utilisateurs sur un ordinateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md) ou [Comment migrer des points d’extension d’un package app-v 4,6 vers app-v 5,1 pour un utilisateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="f4479-113">For more information about converting packages see, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md) or [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span></span>

3.  <span data-ttu-id="f4479-114">Ajoutez et mettez en service le package à l’aide de la console de gestion App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f4479-114">Add and provision the package using the App-V 5.1 management console.</span></span> <span data-ttu-id="f4479-115">Pour plus d’informations sur l’ajout et la mise à jour des packages, voir [Ajout ou mise à niveau](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) de packages à l’aide de la console de gestion et configuration de l' [accès aux packages à l’aide de la console de gestion](how-to-configure-access-to-packages-by-using-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="f4479-115">For more information adding and provisioning packages see, [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) and [How to Configure Access to Packages by Using the Management Console](how-to-configure-access-to-packages-by-using-the-management-console-51.md).</span></span>

4.  <span data-ttu-id="f4479-116">L’application convertie s’exécute désormais avec App-V 5,1, et vous pouvez ouvrir une application à partir de l’autre.</span><span class="sxs-lookup"><span data-stu-id="f4479-116">The converted application now runs using App-V 5.1 and you can open one application from the other.</span></span> <span data-ttu-id="f4479-117">Par exemple, si vous avez converti un package Microsoft Office en un package App-V 5,1 et qu’Adobe Acrobat s’exécute toujours en tant que package App-V 4.6, vous pouvez ouvrir une pièce jointe Adobe Acrobat Reader à l’aide de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="f4479-117">For example, if you converted a Microsoft Office package to an App-V 5.1 package and Adobe Acrobat is still running as an App-V4.6 package, you can open an Adobe Acrobat Reader attachment using Microsoft Outlook.</span></span>

    <span data-ttu-id="f4479-118">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="f4479-118">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f4479-119">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="f4479-119">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f4479-120">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="f4479-120">Got an App-V issue?</span></span>** <span data-ttu-id="f4479-121">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f4479-121">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f4479-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4479-122">Related topics</span></span>


[<span data-ttu-id="f4479-123">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="f4479-123">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 






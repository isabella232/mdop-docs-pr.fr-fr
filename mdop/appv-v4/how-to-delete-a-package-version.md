---
title: Procédure pour supprimer une version de package
description: Procédure pour supprimer une version de package
author: dansimp
ms.assetid: a55adb9d-ffa6-4df3-a2d1-5e0c73c35e1b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc77e60ac9745033ae8f074ae71db0cb8517a202
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807157"
---
# <span data-ttu-id="5f770-103">Procédure pour supprimer une version de package</span><span class="sxs-lookup"><span data-stu-id="5f770-103">How to Delete a Package Version</span></span>


<span data-ttu-id="5f770-104">À partir de la console de gestion du serveur d’applications, vous pouvez utiliser la procédure suivante pour supprimer une ou plusieurs versions et continuer à diffuser les versions restantes du package.</span><span class="sxs-lookup"><span data-stu-id="5f770-104">From the Application Virtualization Server Management Console, for a package that has multiple versions, you can use the following procedure to delete one or more versions and still stream the remaining versions of the package.</span></span> <span data-ttu-id="5f770-105">Vous pouvez effectuer cette opération pour gérer plus efficacement les fichiers sur le serveur ou pour supprimer une version obsolète.</span><span class="sxs-lookup"><span data-stu-id="5f770-105">You might do this to more effectively manage files on the server or to remove an obsolete version.</span></span>

<span data-ttu-id="5f770-106">**Remarques**  Lorsque vous choisissez de supprimer une version, une boîte de confirmation vous rappelle qu’il est possible que les ordinateurs clients l’utilisent toujours.</span><span class="sxs-lookup"><span data-stu-id="5f770-106">**Note** When you choose to delete a version, a confirmation box reminds you that client computers might still be using it.</span></span> <span data-ttu-id="5f770-107">Conseillez aux utilisateurs de quitter et de décharger toutes les applications avant de supprimer une version utilisée.</span><span class="sxs-lookup"><span data-stu-id="5f770-107">You should advise users to exit and unload any applications before you remove a version that is in use.</span></span>

 

**<span data-ttu-id="5f770-108">Pour supprimer une version de package</span><span class="sxs-lookup"><span data-stu-id="5f770-108">To delete a package version</span></span>**

1.  <span data-ttu-id="5f770-109">Dans le volet gauche de la console de gestion du serveur d’applications, développez **packages**.</span><span class="sxs-lookup"><span data-stu-id="5f770-109">In the left panel of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

2.  <span data-ttu-id="5f770-110">Cliquez sur le package qui contient la version que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="5f770-110">Click the package that contains the version you want to delete.</span></span>

3.  <span data-ttu-id="5f770-111">Dans le volet central, cliquez avec le bouton droit sur la version du package que vous voulez supprimer, puis sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="5f770-111">In the center pane, right-click the version of the package you want to delete and choose **Delete**.</span></span>

4.  <span data-ttu-id="5f770-112">Lisez la fenêtre de confirmation, puis cliquez sur **Oui** pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5f770-112">Read the confirmation window, and click **Yes** to complete the action.</span></span>

    <span data-ttu-id="5f770-113">**Remarques**  Si vous avez des utilisateurs en opération de déconnexion, leurs applications seront remplacées par les nouvelles versions lors de leur connexion suivante aux serveurs.</span><span class="sxs-lookup"><span data-stu-id="5f770-113">**Note** If you have users in disconnected operation, their applications will be replaced with the new versions the next time they connect to the servers.</span></span> <span data-ttu-id="5f770-114">Lorsque vous êtes certain que tous les utilisateurs disposent d’applications mises à jour, vous pouvez supprimer les anciennes versions.</span><span class="sxs-lookup"><span data-stu-id="5f770-114">After you are sure all users have updated applications, you can delete old versions.</span></span>

     

## <span data-ttu-id="5f770-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f770-115">Related topics</span></span>


[<span data-ttu-id="5f770-116">Procédure pour supprimer un package</span><span class="sxs-lookup"><span data-stu-id="5f770-116">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="5f770-117">Procédure pour gérer les packages dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="5f770-117">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 






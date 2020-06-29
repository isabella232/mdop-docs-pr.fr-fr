---
title: Procédure pour ajouter un package
description: Procédure pour ajouter un package
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808730"
---
# <span data-ttu-id="d2994-103">Procédure pour ajouter un package</span><span class="sxs-lookup"><span data-stu-id="d2994-103">How to Add a Package</span></span>


<span data-ttu-id="d2994-104">Vous pouvez ajouter un package à partir de la console de gestion du serveur d’applications, de la manière suivante:</span><span class="sxs-lookup"><span data-stu-id="d2994-104">You can add a package from the Application Virtualization Server Management Console in the following ways:</span></span>

-   <span data-ttu-id="d2994-105">Importer une application, qui crée le package automatiquement dans le processus.</span><span class="sxs-lookup"><span data-stu-id="d2994-105">Import an application, which creates the package automatically in the process.</span></span>

-   <span data-ttu-id="d2994-106">Ajoutez un package manuellement.</span><span class="sxs-lookup"><span data-stu-id="d2994-106">Add a package manually.</span></span>

<span data-ttu-id="d2994-107">Il est recommandé d’importer des applications au lieu de les ajouter manuellement.</span><span class="sxs-lookup"><span data-stu-id="d2994-107">It is recommended that you import applications instead of adding them manually.</span></span> <span data-ttu-id="d2994-108">Pour plus d’informations sur l’importation d’applications, voir [Comment importer une application](how-to-import-an-applicationserver.md).</span><span class="sxs-lookup"><span data-stu-id="d2994-108">For more information about importing applications, see [How to Import an Application](how-to-import-an-applicationserver.md).</span></span>

**<span data-ttu-id="d2994-109">Pour ajouter manuellement un package</span><span class="sxs-lookup"><span data-stu-id="d2994-109">To add a package manually</span></span>**

1.  <span data-ttu-id="d2994-110">Dans la console de gestion de l’application virtualisation du serveur, cliquez avec le bouton droit sur le nœud **packages** dans le volet gauche, puis sélectionnez **nouveau package**.</span><span class="sxs-lookup"><span data-stu-id="d2994-110">In the Application Virtualization Server Management Console, right-click the **Packages** node in the left pane and choose **New Package**.</span></span>

2.  <span data-ttu-id="d2994-111">Dans la boîte de dialogue **nouveau package** , tapez un nom dans le champ **nom du package** .</span><span class="sxs-lookup"><span data-stu-id="d2994-111">In the **New Package** dialog box, type a name in the **Package Name** field.</span></span>

3.  <span data-ttu-id="d2994-112">Recherchez ou tapez un nom de chemin d’accès dans le champ chemin d’accès **complet du fichier de package** .</span><span class="sxs-lookup"><span data-stu-id="d2994-112">Browse for or type a path name in the **Full path for package file** field.</span></span> <span data-ttu-id="d2994-113">Il doit s’agir d’un fichier SFT.</span><span class="sxs-lookup"><span data-stu-id="d2994-113">This must be an SFT file.</span></span>

    <span data-ttu-id="d2994-114">**Remarques**  Si vous naviguez jusqu’au fichier SFT, remplacez le chemin d’accès local (par exemple, C:\\Program Files\\User\ _Apps \\Virtual\ _App \ _Server \\Content) par le nom d’hôte statique ou l’adresse IP du serveur.</span><span class="sxs-lookup"><span data-stu-id="d2994-114">**Note** If you browse to the SFT file, replace the local path (such as C:\\Program Files\\User\_Apps\\Virtual\_App\_Server\\content) with the server's static host name or IP address.</span></span> <span data-ttu-id="d2994-115">L’utilisation de la variable *% SFT \ _SOFTGRIDSERVER%* nécessite une configuration d’ordinateur par client.</span><span class="sxs-lookup"><span data-stu-id="d2994-115">Using the variable *%SFT\_SOFTGRIDSERVER%* requires per-client computer configuration.</span></span>

    <span data-ttu-id="d2994-116">Dans les boîtes de dialogue qui font référence aux serveurs d’applications virtuelles, vous devez utiliser un emplacement réseau, tel que le nom d’hôte statique ou l’adresse IP du serveur auquel vos utilisateurs peuvent accéder.</span><span class="sxs-lookup"><span data-stu-id="d2994-116">In dialog boxes that refer to Virtual Application Servers, you must use a network location, such as the server's static host name or IP address, that your users can access.</span></span> <span data-ttu-id="d2994-117">Le fichier OSD (Open Software Descriptor) de l’application peut remplacer la variable d’espace réservé *% SFT \ _SOFTGRIDSERER%* par le nom d’hôte statique ou l’adresse IP du serveur.</span><span class="sxs-lookup"><span data-stu-id="d2994-117">The application's Open Software Descriptor (OSD) file can replace the placeholder variable *%SFT\_SOFTGRIDSERER%* with the server's static host name or IP address.</span></span> <span data-ttu-id="d2994-118">Si vous laissez la variable PlaceHolder, vous devez définir cette variable sur chaque ordinateur client qui accédera à ce serveur.</span><span class="sxs-lookup"><span data-stu-id="d2994-118">If you leave the placeholder variable, you must set this variable on each client computer that will access that server.</span></span> <span data-ttu-id="d2994-119">Définissez une variable utilisateur ou système sur chaque ordinateur pour la fonction SFT \ _SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="d2994-119">Set a User or System variable on each computer for SFT\_SOFTGRIDSERVER.</span></span> <span data-ttu-id="d2994-120">La valeur de la variable doit correspondre au nom d’hôte statique ou à l’adresse IP du serveur.</span><span class="sxs-lookup"><span data-stu-id="d2994-120">The variable value must be the server's static host name or IP address.</span></span> <span data-ttu-id="d2994-121">Si vous définissez une variable, quittez la session du client, déconnectez-vous et reconnectez-vous à Microsoft Windows, puis redémarrez la session sur chaque ordinateur sur lequel une session est en cours d’exécution et où la variable a été définie.</span><span class="sxs-lookup"><span data-stu-id="d2994-121">If you set a variable, exit the Client session, log out of and back into Microsoft Windows, and then restart the session on each computer that had a session running and had the variable set.</span></span>

     

4.  <span data-ttu-id="d2994-122">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2994-122">Click **Next**.</span></span>

5.  <span data-ttu-id="d2994-123">La boîte de dialogue **récapitulative** indique l’emplacement du fichier et vous invite à copier le fichier dans l’emplacement si vous ne l’avez pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="d2994-123">The **Summary** dialog box shows the file location and prompts you to copy the file to the location if you have not already done so.</span></span> <span data-ttu-id="d2994-124">Cliquez sur **Terminer** une fois que vous avez vérifié les informations.</span><span class="sxs-lookup"><span data-stu-id="d2994-124">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="d2994-125">**Remarques**  Si vous gérez des applications sur un serveur distant, dans la boîte de dialogue suivante, tapez uniquement le chemin d’accès du fichier relatif à la racine de contenu du serveur.</span><span class="sxs-lookup"><span data-stu-id="d2994-125">**Note** If you are managing applications on a remote server, in the next dialog box, type only the path of the file relative to the server's content root.</span></span>

     

## <span data-ttu-id="d2994-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2994-126">Related topics</span></span>


[<span data-ttu-id="d2994-127">Procédure pour importer une application</span><span class="sxs-lookup"><span data-stu-id="d2994-127">How to Import an Application</span></span>](how-to-import-an-applicationserver.md)

[<span data-ttu-id="d2994-128">Procédure pour gérer les packages dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="d2994-128">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 






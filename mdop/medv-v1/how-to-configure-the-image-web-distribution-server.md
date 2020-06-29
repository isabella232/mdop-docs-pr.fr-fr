---
title: Comment configurer le serveur de distribution Web d'images
description: Comment configurer le serveur de distribution Web d'images
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810986"
---
# <span data-ttu-id="df3cd-103">Comment configurer le serveur de distribution Web d'images</span><span class="sxs-lookup"><span data-stu-id="df3cd-103">How to Configure the Image Web Distribution Server</span></span>


<span data-ttu-id="df3cd-104">Un référentiel d’image est un serveur facultatif utilisé pour la distribution d’images (qui permet aux administrateurs de télécharger de nouvelles images et d’autres ordinateurs clients de vérifier le serveur toutes les 15 minutes et de mettre à jour leur image s’il est disponible).</span><span class="sxs-lookup"><span data-stu-id="df3cd-104">An image repository is an optional server that is used for image distribution (where administrators upload new images and client computers check the server every 15 minutes and update their image if a new one is available).</span></span>

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


<span data-ttu-id="df3cd-105">Pour un serveur de distribution d’images, vous devez disposer des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="df3cd-105">An image distribution server requires the following:</span></span>

-   <span data-ttu-id="df3cd-106">Internet Information Services (IIS) — pour plus d’informations, voir [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).</span><span class="sxs-lookup"><span data-stu-id="df3cd-106">Internet Information Services (IIS)—For information, see [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).</span></span>

    <span data-ttu-id="df3cd-107">Pendant l’installation d’IIS, lors de l’ajout de services de rôle, sélectionnez les méthodes d’authentification prises en charge suivantes:</span><span class="sxs-lookup"><span data-stu-id="df3cd-107">During the IIS installation, when adding role services, select the following supported authentication methods:</span></span>

    -   **<span data-ttu-id="df3cd-108">Authentification de base</span><span class="sxs-lookup"><span data-stu-id="df3cd-108">Basic Authentication</span></span>**

    -   **<span data-ttu-id="df3cd-109">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="df3cd-109">Windows Authentication</span></span>**

    -   **<span data-ttu-id="df3cd-110">Authentification du mappage de certificat client</span><span class="sxs-lookup"><span data-stu-id="df3cd-110">Client Certificate Mapping Authentication</span></span>**

    <span data-ttu-id="df3cd-111">Lorsque vous configurez IIS, incluez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="df3cd-111">When configuring IIS, include the following:</span></span>

    -   <span data-ttu-id="df3cd-112">Ajoutez un répertoire virtuel avec l’alias nommé **MEDVImages**.</span><span class="sxs-lookup"><span data-stu-id="df3cd-112">Add a virtual directory, with the alias named **MEDVImages**.</span></span> <span data-ttu-id="df3cd-113">Le chemin d’accès physique doit pointer vers l’emplacement des images.</span><span class="sxs-lookup"><span data-stu-id="df3cd-113">The physical path should point to the location of the images.</span></span>

    -   <span data-ttu-id="df3cd-114">Activez BITS.</span><span class="sxs-lookup"><span data-stu-id="df3cd-114">Enable BITS.</span></span>

    -   <span data-ttu-id="df3cd-115">Ajoutez les types MIME suivants:</span><span class="sxs-lookup"><span data-stu-id="df3cd-115">Add the following MIME types:</span></span>

        -   **<span data-ttu-id="df3cd-116">. CKM (application/octet-stream)</span><span class="sxs-lookup"><span data-stu-id="df3cd-116">.ckm (application/octet-stream)</span></span>**

        -   <span data-ttu-id="df3cd-117">**. index (application/octet-stream**)</span><span class="sxs-lookup"><span data-stu-id="df3cd-117">**.index (application/octet-stream**)</span></span>

    -   <span data-ttu-id="df3cd-118">Sur le site MED-V, ajoutez des autorisations de lecture à **tout le monde**.</span><span class="sxs-lookup"><span data-stu-id="df3cd-118">On the MED-V site, add read permissions to **Everyone**.</span></span>

    -   <span data-ttu-id="df3cd-119">Redémarrez IIS.</span><span class="sxs-lookup"><span data-stu-id="df3cd-119">Restart IIS.</span></span>

-   <span data-ttu-id="df3cd-120">Extensions du serveur BITS pour IIS: pour plus d’informations, voir [installer des extensions de serveur bits](https://go.microsoft.com/fwlink/?LinkId=142996).</span><span class="sxs-lookup"><span data-stu-id="df3cd-120">BITS Server Extensions for IIS—For information, see [Install BITS Server Extensions](https://go.microsoft.com/fwlink/?LinkId=142996).</span></span>

## <span data-ttu-id="df3cd-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df3cd-121">Related topics</span></span>


[<span data-ttu-id="df3cd-122">Configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="df3cd-122">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="df3cd-123">Concevoir les référentiel d'images MED-V</span><span class="sxs-lookup"><span data-stu-id="df3cd-123">Design the MED-V Image Repositories</span></span>](design-the-med-v-image-repositories.md)

 

 






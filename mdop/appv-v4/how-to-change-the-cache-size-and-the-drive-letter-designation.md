---
title: Procédure pour modifier la taille de cache et la désignation de lettre de lecteur
description: Procédure pour modifier la taille de cache et la désignation de lettre de lecteur
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807346"
---
# <span data-ttu-id="0d65d-103">Procédure pour modifier la taille de cache et la désignation de lettre de lecteur</span><span class="sxs-lookup"><span data-stu-id="0d65d-103">How to Change the Cache Size and the Drive Letter Designation</span></span>


<span data-ttu-id="0d65d-104">Vous pouvez modifier la taille du cache et la désignation de la lettre du lecteur directement à partir du nœud **virtualisation** des applications de la console de gestion du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="0d65d-104">You can change the cache size and drive letter designation directly from the **Application Virtualization** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="0d65d-105">Remarque</span><span class="sxs-lookup"><span data-stu-id="0d65d-105">Note</span></span>**  
<span data-ttu-id="0d65d-106">Une fois la taille de cache définie, elle ne peut pas être réduite.</span><span class="sxs-lookup"><span data-stu-id="0d65d-106">After the cache size has been set, it cannot be made smaller.</span></span>



**<span data-ttu-id="0d65d-107">Pour modifier la taille du cache</span><span class="sxs-lookup"><span data-stu-id="0d65d-107">To change the cache size</span></span>**

1.  <span data-ttu-id="0d65d-108">Cliquez avec le bouton droit sur le nœud **Application Virtualization** , puis sélectionnez **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="0d65d-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="0d65d-109">Dans la boîte de dialogue **Propriétés** , sélectionnez l’onglet **système de fichiers** .</span><span class="sxs-lookup"><span data-stu-id="0d65d-109">Select the **File System** tab on the **Properties** dialog box.</span></span> <span data-ttu-id="0d65d-110">Dans la section **paramètres de configuration du cache du client** , cliquez sur l’une des cases d’option suivantes pour choisir le mode de gestion de l’espace de cache:</span><span class="sxs-lookup"><span data-stu-id="0d65d-110">In the **Client Cache Configuration Settings** section, click one of the following radio buttons to choose how to manage the cache space:</span></span>

    **<span data-ttu-id="0d65d-111">Important</span><span class="sxs-lookup"><span data-stu-id="0d65d-111">Important</span></span>**  
    <span data-ttu-id="0d65d-112">Si vous activez le paramètre **utiliser le seuil d’espace disque disponible** , la valeur que vous entrez définit la taille de cache sur la taille de disque totale moins le nombre de seuils d’espace disque libre que vous avez entré.</span><span class="sxs-lookup"><span data-stu-id="0d65d-112">If you select the **Use free disk space threshold** setting, the value you enter will set the cache size to the total disk size minus the free disk space threshold number you entered.</span></span> <span data-ttu-id="0d65d-113">Si vous souhaitez revenir à l’utilisation du paramètre **utiliser la taille maximale du cache** , vous devez spécifier un nombre plus grand que la taille de cache actuelle.</span><span class="sxs-lookup"><span data-stu-id="0d65d-113">If you then want revert to using the **Use maximum cache size** setting, you must specify a larger number than the existing cache size.</span></span> <span data-ttu-id="0d65d-114">Dans le cas contraire, l’erreur «une nouvelle taille doit être supérieure à la taille de cache existante» s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0d65d-114">Otherwise, the error “New size must be larger than the existing cache size” will appear.</span></span>



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. <span data-ttu-id="0d65d-115">Cliquez sur **OK** ou sur **appliquer** pour modifier le paramètre.</span><span class="sxs-lookup"><span data-stu-id="0d65d-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="0d65d-116">Pour modifier la désignation de lettre de lecteur</span><span class="sxs-lookup"><span data-stu-id="0d65d-116">To change the drive letter designation</span></span>**

1.  <span data-ttu-id="0d65d-117">Cliquez avec le bouton droit sur le nœud **Application Virtualization** , puis sélectionnez **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="0d65d-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="0d65d-118">Dans l’onglet **système de fichiers** de la boîte de dialogue **Propriétés** , dans le champ **lecteur à utiliser** , sélectionnez la lettre de lecteur de votre choix dans la liste déroulante des lettres de lecteur disponibles.</span><span class="sxs-lookup"><span data-stu-id="0d65d-118">On the **File System** tab in the **Properties** dialog box, in the **Drive to use** field, select the desired drive letter from the drop-down list of available drive letters.</span></span> <span data-ttu-id="0d65d-119">Ce paramètre est en vigueur au redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0d65d-119">This setting becomes effective when the computer is rebooted.</span></span>

3.  <span data-ttu-id="0d65d-120">Cliquez sur **OK** ou sur **appliquer** pour modifier le paramètre.</span><span class="sxs-lookup"><span data-stu-id="0d65d-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="0d65d-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d65d-121">Related topics</span></span>


[<span data-ttu-id="0d65d-122">Procédure pour configurer le client dans Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="0d65d-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)










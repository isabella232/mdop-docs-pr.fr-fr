---
title: Procédure pour réinitialiser le cache de FileSystem
description: Procédure pour réinitialiser le cache de FileSystem
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806817"
---
# <span data-ttu-id="2226b-103">Procédure pour réinitialiser le cache de FileSystem</span><span class="sxs-lookup"><span data-stu-id="2226b-103">How to Reset the FileSystem Cache</span></span>


<span data-ttu-id="2226b-104">La réinitialisation du cache de systèmes de fichiers n’est pas un facteur qui devrait généralement être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2226b-104">Resetting the FileSystem cache is not something that should usually be necessary.</span></span> <span data-ttu-id="2226b-105">Néanmoins, si vous avez besoin de réinitialiser entièrement le cache de systèmes de fichiers, peut-être à des fins de dépannage, vous pouvez utiliser la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="2226b-105">However if you need to completely reset the FileSystem cache, perhaps for troubleshooting purposes, you can use the following procedure.</span></span> <span data-ttu-id="2226b-106">Des droits d’administration sont requis pour effectuer cette action.</span><span class="sxs-lookup"><span data-stu-id="2226b-106">Administrative rights are required to perform this action.</span></span>

**<span data-ttu-id="2226b-107">Pour réinitialiser le cache de systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="2226b-107">To reset the FileSystem cache</span></span>**

1.  <span data-ttu-id="2226b-108">Définissez la valeur de Registre suivante sur 0 (zéro):</span><span class="sxs-lookup"><span data-stu-id="2226b-108">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="2226b-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="2226b-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="2226b-110">Redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2226b-110">Restart the computer.</span></span>

## <span data-ttu-id="2226b-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2226b-111">Related topics</span></span>


[<span data-ttu-id="2226b-112">Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="2226b-112">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 






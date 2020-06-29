---
title: Procédure pour modifier la taille du cache de FileSystem
description: Procédure pour modifier la taille du cache de FileSystem
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807333"
---
# <span data-ttu-id="8fd54-103">Procédure pour modifier la taille du cache de FileSystem</span><span class="sxs-lookup"><span data-stu-id="8fd54-103">How to Change the Size of the FileSystem Cache</span></span>


<span data-ttu-id="8fd54-104">Vous pouvez modifier la taille du cache de systèmes de fichiers à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8fd54-104">You can change the size of the FileSystem cache by using the command line.</span></span> <span data-ttu-id="8fd54-105">Cette action nécessite une réinitialisation complète du cache et nécessite des droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="8fd54-105">This action requires a complete reset of the cache, and it requires administrative rights.</span></span>

**<span data-ttu-id="8fd54-106">Pour modifier la taille du cache de systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="8fd54-106">To change the size of the FileSystem cache</span></span>**

1.  <span data-ttu-id="8fd54-107">Définissez la valeur de Registre suivante sur 0 (zéro):</span><span class="sxs-lookup"><span data-stu-id="8fd54-107">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="8fd54-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="8fd54-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="8fd54-109">Définissez la valeur de Registre suivante à la taille maximale du cache, en Mo, nécessaire pour contenir les packages, par exemple 8192 Mo:</span><span class="sxs-lookup"><span data-stu-id="8fd54-109">Set the following registry value to the maximum cache size, in MB, that is necessary to hold the packages—for example, 8192 MB:</span></span>

    <span data-ttu-id="8fd54-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span><span class="sxs-lookup"><span data-stu-id="8fd54-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span></span>

3.  <span data-ttu-id="8fd54-111">Redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8fd54-111">Restart the computer.</span></span>

## <span data-ttu-id="8fd54-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8fd54-112">Related topics</span></span>


[<span data-ttu-id="8fd54-113">Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="8fd54-113">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 






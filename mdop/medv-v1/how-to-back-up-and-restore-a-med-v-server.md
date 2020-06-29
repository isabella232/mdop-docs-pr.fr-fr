---
title: Procédure de sauvegarde et de restauration d'un serveur MED-V
description: Procédure de sauvegarde et de restauration d'un serveur MED-V
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809744"
---
# <span data-ttu-id="87553-103">Procédure de sauvegarde et de restauration d'un serveur MED-V</span><span class="sxs-lookup"><span data-stu-id="87553-103">How to Back Up and Restore a MED-V Server</span></span>


<span data-ttu-id="87553-104">Les fichiers XML situés sur le serveur peuvent être sauvegardés, puis restaurés en cas de perte de données sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="87553-104">XML files located on the server can be backed up and then restored in case of loss of data on the server.</span></span>

**<span data-ttu-id="87553-105">Pour sauvegarder un serveur MED-V</span><span class="sxs-lookup"><span data-stu-id="87553-105">To back up a MED-V server</span></span>**

-   <span data-ttu-id="87553-106">Sauvegardez les fichiers suivants situés dans \* &lt; INSTALLDIR &gt; \\Servers\\ConfigurationServer\*:</span><span class="sxs-lookup"><span data-stu-id="87553-106">Back up the following files, located in *&lt;InstallDir&gt;\\Servers\\ConfigurationServer*:</span></span>

    <span data-ttu-id="87553-107">**Remarques**  Si la configuration a été modifiée par défaut, les fichiers peuvent être stockés à un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="87553-107">**Note** If the configuration has been changed from the default, the files might be stored in a different location.</span></span>

     

    -   <span data-ttu-id="87553-108">ClientPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="87553-108">ClientPolicy.xml</span></span>

    -   <span data-ttu-id="87553-109">ClientSettings.xml</span><span class="sxs-lookup"><span data-stu-id="87553-109">ClientSettings.xml</span></span>

    -   <span data-ttu-id="87553-110">ConfigurationFiles.xml</span><span class="sxs-lookup"><span data-stu-id="87553-110">ConfigurationFiles.xml</span></span>

    -   <span data-ttu-id="87553-111">OrganizationPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="87553-111">OrganizationPolicy.xml</span></span>

    -   <span data-ttu-id="87553-112">WorkspaceKeys.xml</span><span class="sxs-lookup"><span data-stu-id="87553-112">WorkspaceKeys.xml</span></span>

    <span data-ttu-id="87553-113">**Remarques**  Le fichier ServerSettings.xml peut également être sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="87553-113">**Note** The ServerSettings.xml file can be backed up as well.</span></span> <span data-ttu-id="87553-114">Toutefois, si une configuration spécifique a été modifiée (par exemple, sur le serveur d’origine, le répertoire des VM pour MED-V se trouve dans «*C:\\Vms*» et ce type d’annuaire n’existe pas sur le nouveau serveur), il est possible qu’elle génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="87553-114">However, if a specific configuration has been changed (for example, on the original server, the MED-V VMS directory is located in "*C:\\Vms*" and such a directory does not exist on the new server), it can cause an error.</span></span>

     

**<span data-ttu-id="87553-115">Pour restaurer un serveur MED-V</span><span class="sxs-lookup"><span data-stu-id="87553-115">To restore a MED-V server</span></span>**

1.  <span data-ttu-id="87553-116">Installez un nouveau serveur MED-V.</span><span class="sxs-lookup"><span data-stu-id="87553-116">Install a new MED-V server.</span></span>

2.  <span data-ttu-id="87553-117">Copiez les fichiers de sauvegarde dans le répertoire suivant:</span><span class="sxs-lookup"><span data-stu-id="87553-117">Copy the backup files to the following directory:</span></span>

    *<span data-ttu-id="87553-118">&lt;InstallDir &gt; \\Servers\\ConfigurationServer</span><span class="sxs-lookup"><span data-stu-id="87553-118">&lt;InstallDir&gt;\\Servers\\ConfigurationServer</span></span>*

3.  <span data-ttu-id="87553-119">Redémarrez le service MED-V.</span><span class="sxs-lookup"><span data-stu-id="87553-119">Restart the MED-V service.</span></span>

 

 






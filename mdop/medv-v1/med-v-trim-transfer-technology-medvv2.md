---
title: Technologie de transfert de découpage MED-V
description: Technologie de transfert de découpage MED-V
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811604"
---
# <span data-ttu-id="3f222-103">Technologie de transfert de découpage MED-V</span><span class="sxs-lookup"><span data-stu-id="3f222-103">MED-V Trim Transfer Technology</span></span>


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


<span data-ttu-id="3f222-104">La technologie de déduplication avancée de MED-V accélère le téléchargement d’images virtuelles d’machines virtuelles sur le réseau local (LAN) ou sur réseau étendu (WAN), ce qui permet de réduire la bande passante réseau nécessaire au transfert d’une machine virtuelle d’espace de travail MED-V vers plusieurs utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="3f222-104">The MED-V advanced Trim Transfer de-duplication technology accelerates the download of initial and updated virtual machine images over the LAN or WAN, thereby reducing the network bandwidth needed to transport a MED-V workspace virtual machine to multiple end users.</span></span>

<span data-ttu-id="3f222-105">Cette technologie avancée utilise des données locales existantes pour générer l’image de l’ordinateur virtuel, en tirant parti du fait que, dans de nombreux cas, la majeure partie de l’ordinateur virtuel (par exemple, les fichiers système et d’application) existe déjà sur le disque de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="3f222-105">This breakthrough technology uses existing local data to build the virtual machine image, leveraging the fact that in many cases, much of the virtual machine (for example, system and application files) already exists on the end user's disk.</span></span> <span data-ttu-id="3f222-106">Par exemple, si un ordinateur virtuel contenant WindowsXP est remis à un client exécutant une copie locale de WindowsXP, MED-V supprime automatiquement les éléments WindowsXP redondants du transfert.</span><span class="sxs-lookup"><span data-stu-id="3f222-106">For example, if a virtual machine containing WindowsXP is delivered to a client running a local copy of WindowsXP, MED-V will automatically remove the redundant WindowsXP elements from the transfer.</span></span> <span data-ttu-id="3f222-107">Pour garantir un espace de travail valide et fonctionnel, le client MED-V vérifie l’intégrité des données locales avant qu’elle ne soit utilisée, ce qui permet de garantir que les blocs de données locaux constituent une version de bit absolument identique à celle de l’image de l’ordinateur virtuel souhaité.</span><span class="sxs-lookup"><span data-stu-id="3f222-107">To ensure a valid and functional workspace, the MED-V client cryptographically verifies the integrity of local data before it is utilized, guaranteeing that the local blocks of data are absolutely bit-by-bit identical to those in the desired virtual machine image.</span></span> <span data-ttu-id="3f222-108">Les blocs qui ne correspondent pas sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="3f222-108">Blocks that do not match are not used.</span></span>

<span data-ttu-id="3f222-109">Le processus est économe en bande passante et transparente, et les transferts s’exécutent en arrière-plan, à l’aide de ressources réseau et processeur inutilisées.</span><span class="sxs-lookup"><span data-stu-id="3f222-109">The process is bandwidth-efficient and transparent, and transfers run in the background, utilizing unused network and CPU resources.</span></span>

<span data-ttu-id="3f222-110">Lors de la mise à jour vers une nouvelle version d’image (par exemple, lorsque les administrateurs souhaitent distribuer une nouvelle application ou un nouveau correctif), seuls les éléments qui ont changé («Delta») sont téléchargés, et non la totalité de l’ordinateur virtuel, réduisant considérablement le temps de bande passante et de remise réseau requis.</span><span class="sxs-lookup"><span data-stu-id="3f222-110">When updating to a new image version (for example, when administrators want to distribute a new application or patch), only the elements that have changed ("deltas") are downloaded, and not the entire virtual machine, significantly reducing the required network bandwidth and delivery time.</span></span>

<span data-ttu-id="3f222-111">Vous pouvez configurer les dossiers indexés sur l’hôte dans le cadre du protocole de transfert de découpage, en fonction du système d’exploitation hôte.</span><span class="sxs-lookup"><span data-stu-id="3f222-111">You can configure which folders are indexed on the host as part of the Trim Transfer protocol, based on the host operating system.</span></span> <span data-ttu-id="3f222-112">Ces paramètres sont configurés dans le fichier *ClientSettings.xml* , qui se trouve dans le dossier **Servers\\Configuration Server\\** .</span><span class="sxs-lookup"><span data-stu-id="3f222-112">These settings are configured in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="3f222-113">Le service doit être redémarré lors de l’application de nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="3f222-113">When applying new settings, the service must be restarted.</span></span>

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 






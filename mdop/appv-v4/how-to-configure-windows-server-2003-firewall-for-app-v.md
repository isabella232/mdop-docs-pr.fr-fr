---
title: Procédure pour configurer le Pare-feu Windows Server2003 pour App-V
description: Procédure pour configurer le Pare-feu Windows Server2003 pour App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807222"
---
# <span data-ttu-id="7f76f-103">Procédure pour configurer le Pare-feu Windows Server2003 pour App-V</span><span class="sxs-lookup"><span data-stu-id="7f76f-103">How to Configure Windows Server 2003 Firewall for App-V</span></span>


<span data-ttu-id="7f76f-104">Suivez la procédure ci-dessous pour configurer le pare-feu windowsserver2003 2003 pour App-V.</span><span class="sxs-lookup"><span data-stu-id="7f76f-104">Use the following procedure to configure the WindowsServer 2003 firewall for App-V.</span></span>

**<span data-ttu-id="7f76f-105">Pour configurer le pare-feu de windowsserver2003 2003 pour App-V</span><span class="sxs-lookup"><span data-stu-id="7f76f-105">To configure WindowsServer 2003 firewall for App-V</span></span>**

1.  <span data-ttu-id="7f76f-106">Dans le **panneau de configuration**, ouvrez le **pare-feu Windows**.</span><span class="sxs-lookup"><span data-stu-id="7f76f-106">In **Control Panel**, open the **Windows Firewall**.</span></span>

    <span data-ttu-id="7f76f-107">**Remarques**  Si le serveur n’a pas été configuré pour exécuter le service de pare-feu avant cette étape, vous serez invité à démarrer le service de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="7f76f-107">**Note** If the server has not been configured to run the firewall service before this step, you will be prompted to start the firewall service.</span></span>

     

2.  <span data-ttu-id="7f76f-108">Si les fichiers ICO et OSD sont publiés via SMB, assurez-vous que le **partage de fichiers et d’imprimantes** est activé sous l’onglet **exceptions** .</span><span class="sxs-lookup"><span data-stu-id="7f76f-108">If ICO and OSD files are published through SMB, ensure that **File and Printer Sharing** is enabled on the **Exceptions** tab.</span></span>

    <span data-ttu-id="7f76f-109">**Remarques**  Si des fichiers. ICO et OSD sont publiés par le biais du protocole HTTP/HTTPs sur le serveur de gestion, vous devrez peut-être ajouter une exception pour HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="7f76f-109">**Note** If ICO and OSD files are published through HTTP/HTTPS on the Management Server, you might need to add an exception for HTTP or HTTPS.</span></span> <span data-ttu-id="7f76f-110">Si le serveur IIS hébergeant les fichiers ICO et OSD est hébergé sur un ordinateur distinct du serveur de gestion, vous devez ajouter l’exception à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f76f-110">If the IIS server hosting the ICO and OSD files is hosted on a computer separate from the Management Server, you need to add the exception to that computer.</span></span> <span data-ttu-id="7f76f-111">Pour optimiser les performances, nous vous recommandons d’héberger les fichiers ICO et OSD sur un serveur distinct à partir du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="7f76f-111">To maximize performance, it is recommended that you host the ICO and OSD files on a separate server from the Management Server.</span></span>

     

3.  <span data-ttu-id="7f76f-112">Ajoutez une exception de programme pour `sghwdsptr.exe` , qui est le fichier exécutable du service du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="7f76f-112">Add a program exception for `sghwdsptr.exe`, which is the Management Server service executable.</span></span> <span data-ttu-id="7f76f-113">Le chemin d’accès par défaut à cet exécutable est `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="7f76f-113">The default path to this executable is `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

    <span data-ttu-id="7f76f-114">**Remarques**  Si le serveur de gestion utilise RTSP pour la communication, vous devez également ajouter une exception de programme pour `sghwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="7f76f-114">**Note** If the Management Server uses RTSP for communication, you must also add a program exception for `sghwsvr.exe`.</span></span>

    <span data-ttu-id="7f76f-115">Le serveur de streaming App-V nécessite une exception `sglwdsptr.exe` de programme pour la communication RTSP.</span><span class="sxs-lookup"><span data-stu-id="7f76f-115">The App-V Streaming Server requires a program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="7f76f-116">Le serveur de streaming App-V qui utilise RTSP pour la communication nécessite également une exception de programme pour `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="7f76f-116">The App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

     

4.  <span data-ttu-id="7f76f-117">Assurez-vous que l’étendue correcte est configurée pour chaque exception.</span><span class="sxs-lookup"><span data-stu-id="7f76f-117">Ensure that the proper scope is configured for each exception.</span></span> <span data-ttu-id="7f76f-118">Pour réduire les risques, supprimez tous les ordinateurs et limitez strictement les adresses IP auxquelles le serveur répond.</span><span class="sxs-lookup"><span data-stu-id="7f76f-118">To reduce risk, remove any computer and strictly limit the IP addresses to which the server will respond.</span></span>

## <span data-ttu-id="7f76f-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f76f-119">Related topics</span></span>


[<span data-ttu-id="7f76f-120">Procédure pour configurer le Pare-feu Windows Server2008 pour App-V</span><span class="sxs-lookup"><span data-stu-id="7f76f-120">How to Configure Windows Server 2008 Firewall for App-V</span></span>](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 






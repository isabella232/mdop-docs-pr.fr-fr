---
title: Configuration du pare-feu pour les serveurs App-V Server
description: Configuration du pare-feu pour les serveurs App-V Server
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808982"
---
# <span data-ttu-id="1836d-103">Configuration du pare-feu pour les serveurs App-V Server</span><span class="sxs-lookup"><span data-stu-id="1836d-103">Configuring the Firewall for the App-V Servers</span></span>


<span data-ttu-id="1836d-104">Après l’installation de Microsoft Application Virtualization (App-V) Server Management Server ou de Streaming Server et de sa configuration pour utiliser le protocole RTSP ou RTSP, vous devez créer des exceptions de pare-feu pour les programmes App-V.</span><span class="sxs-lookup"><span data-stu-id="1836d-104">After you install the Microsoft Application Virtualization (App-V) Management Server or Streaming Server and configure it to use the RTSP or RTSPS protocol, you must create firewall exceptions for the App-V programs.</span></span>

## <span data-ttu-id="1836d-105">Configuration des exceptions de pare-feu pour le serveur de gestion de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="1836d-105">Configuring Firewall Exceptions for Application Virtualization Management Server</span></span>


<span data-ttu-id="1836d-106">Créez une exception de pare-feu pour **sghwdsptr.exe** et **sghwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="1836d-106">Create a firewall exception for **sghwdsptr.exe** and **sghwsvr.exe**.</span></span> <span data-ttu-id="1836d-107">Ces programmes se trouvent dans le dossier C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin sur un système d’exploitation 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1836d-107">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="1836d-108">Si vous utilisez une version de système d’exploitation 64 bits, le dossier se trouve sous C:\\Program Files (x86) \\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="1836d-108">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.</span></span>

## <span data-ttu-id="1836d-109">Configuration des exceptions de pare-feu pour le serveur de diffusion de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="1836d-109">Configuring Firewall Exceptions for Application Virtualization Streaming Server</span></span>


<span data-ttu-id="1836d-110">Créez une exception de pare-feu pour **sglwdsptr.exe** et **sglwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="1836d-110">Create a firewall exception for **sglwdsptr.exe** and **sglwsvr.exe**.</span></span> <span data-ttu-id="1836d-111">Ces programmes se trouvent dans le dossier C:\\Program Files\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin sur un système d’exploitation 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1836d-111">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="1836d-112">Si vous utilisez une version de système d’exploitation 64 bits, le dossier se trouve sous C:\\Program Files (x86) \\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="1836d-112">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.</span></span>

## <span data-ttu-id="1836d-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1836d-113">Related topics</span></span>


[<span data-ttu-id="1836d-114">Procédure pour configurer des serveurs pour un déploiement basé sur un serveur</span><span class="sxs-lookup"><span data-stu-id="1836d-114">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="1836d-115">Procédure pour installer et configurer l'application par défaut</span><span class="sxs-lookup"><span data-stu-id="1836d-115">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)

 

 






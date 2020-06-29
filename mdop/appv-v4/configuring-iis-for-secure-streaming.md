---
title: Configuration d'IIS pour la diffusion en continu sécurisé
description: Configuration d'IIS pour la diffusion en continu sécurisé
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809023"
---
# <span data-ttu-id="c1697-103">Configuration d'IIS pour la diffusion en continu sécurisé</span><span class="sxs-lookup"><span data-stu-id="c1697-103">Configuring IIS for Secure Streaming</span></span>


<span data-ttu-id="c1697-104">Avec la version 4,5 de Microsoft Application Virtualization (App-V), vous pouvez utiliser HTTP et HTTPs en tant que protocoles pour la diffusion de packages d’application en continu vers les clients App-V.</span><span class="sxs-lookup"><span data-stu-id="c1697-104">With the release of Microsoft Application Virtualization (App-V) version 4.5, you can use HTTP and HTTPS as protocols for streaming application packages to the App-V clients.</span></span> <span data-ttu-id="c1697-105">Cette option permet aux organisations d’exploiter l’évolutivité supplémentaire proposée par les services Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="c1697-105">This option enables organizations to leverage the additional scalability that IIS typically offers.</span></span> <span data-ttu-id="c1697-106">Lorsque vous utilisez IIS en tant que serveur de diffusion en continu, vous pouvez sécuriser les communications entre le client et le serveur en utilisant HTTPs au lieu de HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1697-106">When you use IIS as a streaming server, you can help secure the communications between the client and server by using HTTPS instead of HTTP.</span></span>

<span data-ttu-id="c1697-107">**Remarques**  Si vous voulez diffuser des applications à partir d’un serveur de fichiers, vous devez améliorer la sécurité des communications vers les packages d’application.</span><span class="sxs-lookup"><span data-stu-id="c1697-107">**Note** If you want to stream applications from a file server, you should enhance the security of the communications to the application packages.</span></span> <span data-ttu-id="c1697-108">Pour cela, vous pouvez utiliser le protocole IPsec.</span><span class="sxs-lookup"><span data-stu-id="c1697-108">This can be achieved using IPsec.</span></span> <span data-ttu-id="c1697-109">Pour plus d’informations, reportez-vous aux rubriques suivantes dans la bibliothèque TechNet:</span><span class="sxs-lookup"><span data-stu-id="c1697-109">For more information see the following topics in the TechNet Library:</span></span>

-   <span data-ttu-id="c1697-110">Pour Windows Server2003,</span><span class="sxs-lookup"><span data-stu-id="c1697-110">For Windows Server2003,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133226>

-   <span data-ttu-id="c1697-111">Pour Windows Server 2008,</span><span class="sxs-lookup"><span data-stu-id="c1697-111">For Windows Server 2008,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## <span data-ttu-id="c1697-112">Types MIME</span><span class="sxs-lookup"><span data-stu-id="c1697-112">MIME Types</span></span>


<span data-ttu-id="c1697-113">Lorsque vous utilisez IIS pour diffuser des applications virtuelles à l’aide de HTTP ou HTTPs, pour prendre en charge l’application-V, vous devez ajouter les types MIME suivants au serveur IIS:</span><span class="sxs-lookup"><span data-stu-id="c1697-113">When you use IIS to stream virtual applications with HTTP or HTTPS, to support App-V, the following MIME types must be added to the IIS server:</span></span>

-   <span data-ttu-id="c1697-114">. OSD = TXT</span><span class="sxs-lookup"><span data-stu-id="c1697-114">.OSD=TXT</span></span>

-   <span data-ttu-id="c1697-115">. SFT = binaire</span><span class="sxs-lookup"><span data-stu-id="c1697-115">.SFT=Binary</span></span>

<span data-ttu-id="c1697-116">Pour plus d’informations sur l’ajout de types MIME, utilisez les Articles de la base de connaissances suivants:</span><span class="sxs-lookup"><span data-stu-id="c1697-116">Use the following KB articles as guidance for adding MIME types:</span></span>

<span data-ttu-id="c1697-117">6,0 IIS:</span><span class="sxs-lookup"><span data-stu-id="c1697-117">IIS 6.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151973>

<span data-ttu-id="c1697-118">7,0 IIS:</span><span class="sxs-lookup"><span data-stu-id="c1697-118">IIS 7.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151977>

## <span data-ttu-id="c1697-119">Authentification Kerberos</span><span class="sxs-lookup"><span data-stu-id="c1697-119">Kerberos Authentication</span></span>


<span data-ttu-id="c1697-120">Lorsque vous utilisez l’authentification HTTP ou HTTPs et Kerberos pour diffuser des fichiers. ICO, OSD ou SFT, vous renforcez la sécurité de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="c1697-120">When you use HTTP or HTTPS and Kerberos authentication to stream ICO, OSD, or SFT files, you are enhancing the security of your environment.</span></span> <span data-ttu-id="c1697-121">Toutefois, pour qu’IIS prenne en charge l’authentification Kerberos, vous devez configurer un nom de principal de service approprié (SPN).</span><span class="sxs-lookup"><span data-stu-id="c1697-121">However, for IIS to support Kerberos authentication, you must configure a proper Service Principal Name (SPN).</span></span> <span data-ttu-id="c1697-122">L' `setspn.exe` outil est disponible pour Windows Server2003 à partir des outils de support sur le CD d’installation et est intégré à Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c1697-122">The `setspn.exe` tool is available for Windows Server2003 from the Support Tools on the installation CD and is built-in to Windows Server2008.</span></span>

<span data-ttu-id="c1697-123">Pour créer un SPN, exécutez `setspn.exe` à partir d’une invite de commandes lorsque vous êtes connecté en tant que membre du groupe administrateurs de domaine (par exemple,) `setspn.exe –A HTTP/FQDN of Server ServerName` .</span><span class="sxs-lookup"><span data-stu-id="c1697-123">To create an SPN, run `setspn.exe` from a command prompt while logged in as a member of Domain Administrators—for example, `setspn.exe –A HTTP/FQDN of Server ServerName`.</span></span>

## <span data-ttu-id="c1697-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1697-124">Related topics</span></span>


[<span data-ttu-id="c1697-125">Configuration de Management ou Streaming Server pour sécuriser les communications post-installation</span><span class="sxs-lookup"><span data-stu-id="c1697-125">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 






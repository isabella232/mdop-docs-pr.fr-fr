---
title: Configuration de MED-V pour les réseaux distants
description: Configuration de MED-V pour les réseaux distants
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811927"
---
# <span data-ttu-id="25308-103">Configuration de MED-V pour les réseaux distants</span><span class="sxs-lookup"><span data-stu-id="25308-103">Configuring MED-V for Remote Networks</span></span>


<span data-ttu-id="25308-104">Vous pouvez configurer MED-V de façon à ce qu’il fonctionne à l’intérieur d’un réseau, à distance ou les deux à l’intérieur du réseau et à distance.</span><span class="sxs-lookup"><span data-stu-id="25308-104">You can configure MED-V to work from inside a network, remotely, or both from inside the network and remotely.</span></span>

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**<span data-ttu-id="25308-105">Pour configurer MED-V de façon à ce qu’il fonctionne à l’intérieur d’un réseau</span><span class="sxs-lookup"><span data-stu-id="25308-105">To configure MED-V to work from inside a network</span></span>**

-   <span data-ttu-id="25308-106">Configurer un serveur MED-V et une distribution d’image à l’intérieur du réseau.</span><span class="sxs-lookup"><span data-stu-id="25308-106">Configure a MED-V server and image distribution inside the network.</span></span>

**<span data-ttu-id="25308-107">Pour configurer MED-V de façon à ce qu’il fonctionne à distance</span><span class="sxs-lookup"><span data-stu-id="25308-107">To configure MED-V to work remotely</span></span>**

1.  <span data-ttu-id="25308-108">Configurer un serveur MED-V et un serveur de distribution d’images accessibles à partir d’Internet.</span><span class="sxs-lookup"><span data-stu-id="25308-108">Configure a MED-V server and an image distribution server that are accessible from the Internet.</span></span>

2.  <span data-ttu-id="25308-109">Le cas échéant, configurez un proxy inverse (également appelé DMZ).</span><span class="sxs-lookup"><span data-stu-id="25308-109">If needed, configure a perimeter network (also called a DMZ) reverse proxy.</span></span>

3.  <span data-ttu-id="25308-110">Définissez la méthode d’authentification dans le fichier *ClientSettings.xml* , qui se trouve dans le dossier **Servers\\Configuration Server\\** .</span><span class="sxs-lookup"><span data-stu-id="25308-110">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

**<span data-ttu-id="25308-111">Pour configurer MED-V de façon à ce qu’il fonctionne à la fois à partir d’un réseau et à distance</span><span class="sxs-lookup"><span data-stu-id="25308-111">To configure MED-V to work both from inside a network and remotely</span></span>**

1.  <span data-ttu-id="25308-112">Configurer un serveur et un serveur de distribution d’image MED-V à l’intérieur du réseau.</span><span class="sxs-lookup"><span data-stu-id="25308-112">Configure a MED-V server and image distribution server inside the network.</span></span>

2.  <span data-ttu-id="25308-113">Assurez-vous que les serveurs sont accessibles à partir d’Internet.</span><span class="sxs-lookup"><span data-stu-id="25308-113">Ensure that the servers are accessible from the Internet.</span></span>

3.  <span data-ttu-id="25308-114">Configuration de la résolution DNS de telle sorte que lorsque le client tente de se connecter à un serveur, il se connecte automatiquement au serveur approprié (au sein du réseau ou via Internet) en fonction de l’emplacement du client.</span><span class="sxs-lookup"><span data-stu-id="25308-114">Configure the DNS resolution so that when the client attempts to connect to a server, it automatically connects to the correct server (within the network or over the Internet) based on the client location.</span></span>

4.  <span data-ttu-id="25308-115">Le cas échéant, configurez un proxy inverse de réseau de périmètre.</span><span class="sxs-lookup"><span data-stu-id="25308-115">If needed, configure a perimeter network reverse proxy.</span></span>

5.  <span data-ttu-id="25308-116">Définissez la méthode d’authentification dans le fichier *ClientSettings.xml* , qui se trouve dans le dossier **Servers\\Configuration Server\\** .</span><span class="sxs-lookup"><span data-stu-id="25308-116">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="25308-117">**Remarques**  Le service doit être redémarré lors de l’application de nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="25308-117">**Note** When applying new settings, the service must be restarted.</span></span>

 

-   <span data-ttu-id="25308-118">Vous pouvez remplacer le schéma d’authentification IIS par l’une des valeurs suivantes: BASIC, DIGEST, NTLM ou NEGOTIATE.</span><span class="sxs-lookup"><span data-stu-id="25308-118">You can change the IIS authentication scheme to one of the following: BASIC, DIGEST, NTLM, or NEGOTIATE.</span></span> <span data-ttu-id="25308-119">La valeur par défaut est NEGOTIATE et utilise l’entrée suivante:</span><span class="sxs-lookup"><span data-stu-id="25308-119">The default is NEGOTIATE and uses the following entry:</span></span>

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## <span data-ttu-id="25308-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="25308-120">Related topics</span></span>


[<span data-ttu-id="25308-121">Conception et planification de l'infrastructure de MED-V</span><span class="sxs-lookup"><span data-stu-id="25308-121">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 






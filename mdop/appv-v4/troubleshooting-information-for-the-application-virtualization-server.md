---
title: Informations pour résoudre les problèmes liés au serveur Application Virtualization Server
description: Informations pour résoudre les problèmes liés au serveur Application Virtualization Server
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806206"
---
# <span data-ttu-id="fe1b7-103">Informations pour résoudre les problèmes liés au serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="fe1b7-103">Troubleshooting Information for the Application Virtualization Server</span></span>


<span data-ttu-id="fe1b7-104">Cette rubrique contient des informations que vous pouvez utiliser pour résoudre divers problèmes sur les serveurs de virtualisation des applications (App-V).</span><span class="sxs-lookup"><span data-stu-id="fe1b7-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Servers.</span></span>

## <span data-ttu-id="fe1b7-105">Message d’avertissement 25017 dans le journal d’installation après l’installation du serveur</span><span class="sxs-lookup"><span data-stu-id="fe1b7-105">Warning Message 25017 in Setup Log After Installing the Server</span></span>


<span data-ttu-id="fe1b7-106">Le message suivant peut apparaître dans le journal de configuration du serveur après l’installation.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-106">You might find the following message in the server setup log after installation.</span></span>

*<span data-ttu-id="fe1b7-107">Avertissement 25017.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-107">Warning 25017.</span></span> <span data-ttu-id="fe1b7-108">Le programme d’installation n’a pas pu créer l’objet marqueur Active Directory pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-108">The installation Program could not create the Active Directory marker object for the server.</span></span> <span data-ttu-id="fe1b7-109">Le compte utilisé pour l’installation ne disposait pas des droits suffisants pour écrire dans Active Directory ou Active Directory n’était pas disponible.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-109">The account used to install did not have the sufficient rights to write to Active Directory or Active Directory was unavailable.</span></span>*

<span data-ttu-id="fe1b7-110">Le programme d’installation de l’application-V ou du programme d’installation de serveur en continu crée une entrée de point de connexion de service sous l’objet ordinateur dans les services de domaine Active Directory (AD DS) qui correspond à l’ordinateur sur lequel le serveur est installé, si le compte utilisé pour exécuter le programme d’installation dispose des droits appropriés.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-110">The App-V Management or Streaming Server installer creates a Service Connection Point entry under the Computer object in Active Directory Domain Services (ADDS) that corresponds to the computer on which the server is installed if the account used to run the installer has the appropriate rights.</span></span> <span data-ttu-id="fe1b7-111">L’impossibilité de créer cette entrée n’entraînera pas l’échec de l’installation, sans conséquence du fonctionnement du produit.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-111">Failure to create this entry will not cause the install to fail and this should not otherwise affect the functioning of the product.</span></span> <span data-ttu-id="fe1b7-112">La cause probable de tout échec réside dans le fait que le compte d’utilisateur utilisé pour exécuter l’installation ne dispose pas des droits suffisants pour écrire dans ADDS.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-112">The likely cause of any failure is that the user account used to run the install did not have sufficient rights to write to ADDS.</span></span> <span data-ttu-id="fe1b7-113">Même si l’inscription du serveur App-V dans ADDS est facultative, l’un des avantages d’une telle action est d’activer les outils de gestion centralisés pour localiser le serveur App-V à des fins d’inventaire et de gestion.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-113">Although registering the App-V server in ADDS is optional, one benefit of doing so enables centralized management tools to locate the App-V server for inventory and management purposes.</span></span>

## <span data-ttu-id="fe1b7-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe1b7-114">Related topics</span></span>


[<span data-ttu-id="fe1b7-115">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="fe1b7-115">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 






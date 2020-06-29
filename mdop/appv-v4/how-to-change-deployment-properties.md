---
title: Procédure pour modifier les propriétés de déploiement
description: Procédure pour modifier les propriétés de déploiement
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807357"
---
# <span data-ttu-id="57ce0-103">Procédure pour modifier les propriétés de déploiement</span><span class="sxs-lookup"><span data-stu-id="57ce0-103">How to Change Deployment Properties</span></span>


<span data-ttu-id="57ce0-104">Vous pouvez utiliser les procédures suivantes pour modifier les informations de l’onglet **déploiement** d’une application que vous séquençage, y compris l’URL du serveur virtualisation des applications, les systèmes d’exploitation requis par les applications virtualisées et les options de sortie de l’application virtuelle à installer.</span><span class="sxs-lookup"><span data-stu-id="57ce0-104">You can use the following procedures to change the **Deployment** tab information for an application you are sequencing, including the Application Virtualization server URL, the operating systems required by the virtualized applications, and the output options for the virtual application to be installed.</span></span>

**<span data-ttu-id="57ce0-105">Pour modifier l’URL du serveur</span><span class="sxs-lookup"><span data-stu-id="57ce0-105">To change the server URL</span></span>**

1.  <span data-ttu-id="57ce0-106">Dans la zone de liste déroulante, sélectionnez le protocole de diffusion.</span><span class="sxs-lookup"><span data-stu-id="57ce0-106">Select the streaming protocol from the drop-down list box.</span></span>

2.  <span data-ttu-id="57ce0-107">Entrez le nom d’hôte du serveur d’applications virtuel ou du solde de charge du groupe de serveurs.</span><span class="sxs-lookup"><span data-stu-id="57ce0-107">Enter the host name of the virtual application server or the server group's load balancer.</span></span> <span data-ttu-id="57ce0-108">Vous pouvez utiliser le nom d’hôte réel ou l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="57ce0-108">You can use the actual host name or IP address.</span></span>

3.  <span data-ttu-id="57ce0-109">Spécifiez le numéro de port sur lequel le serveur d’applications virtuelles ou l’équilibrage de charge doit écouter une demande de client de bureau de virtualisation d’application pour l’application en flux.</span><span class="sxs-lookup"><span data-stu-id="57ce0-109">Specify the port number on which the virtual application server or load balancer will listen for an Application Virtualization Desktop Client request for the streamed application.</span></span>

4.  <span data-ttu-id="57ce0-110">Spécifiez le chemin d’accès relatif du serveur d’applications virtuel sur lequel est stocké le package logiciel.</span><span class="sxs-lookup"><span data-stu-id="57ce0-110">Specify the relative path on the virtual application server where the software package is stored.</span></span>

**<span data-ttu-id="57ce0-111">Pour modifier la configuration requise pour les systèmes d’exploitation des applications</span><span class="sxs-lookup"><span data-stu-id="57ce0-111">To change the application operating systems requirements</span></span>**

1.  <span data-ttu-id="57ce0-112">Pour ajouter le ou les systèmes d’exploitation requis, sélectionnez-le dans la liste **disponible** et cliquez sur la flèche pointant sur le contrôle de liste systèmes d’exploitation **sélectionnés** .</span><span class="sxs-lookup"><span data-stu-id="57ce0-112">To add the required operating system(s), select it in the **Available** list and click the arrow button pointing to the **Selected** operating systems list control.</span></span>

2.  <span data-ttu-id="57ce0-113">Pour supprimer un système d’exploitation, sélectionnez-le dans le contrôle de liste **sélectionné** , puis cliquez sur la flèche pointant sur le contrôle de liste systèmes d’exploitation **disponibles** .</span><span class="sxs-lookup"><span data-stu-id="57ce0-113">To remove an operating system, select it in the **Selected** list control, and click the arrow button pointing to the **Available** operating systems list control.</span></span>

**<span data-ttu-id="57ce0-114">Pour modifier les options de sortie de l’application</span><span class="sxs-lookup"><span data-stu-id="57ce0-114">To change the application output options</span></span>**

1.  <span data-ttu-id="57ce0-115">Dans la liste déroulante **algorithme de compression** , sélectionnez la méthode de compression à utiliser lors de la diffusion de l’application.</span><span class="sxs-lookup"><span data-stu-id="57ce0-115">From the **Compression Algorithm** drop-down list, select the compression method to use when streaming the application.</span></span>

2.  <span data-ttu-id="57ce0-116">Cochez la case **appliquer les descripteurs de sécurité** pour vérifier que les descripteurs de sécurité des applications empaquetées sont appliqués lors du déploiement.</span><span class="sxs-lookup"><span data-stu-id="57ce0-116">Select the **Enforce Security Descriptors** check box to ensure security descriptors of the packaged applications are enforced when deployed.</span></span>

3.  <span data-ttu-id="57ce0-117">Sélectionnez **générer un fichier de différences** pour générer un fichier de différences pour l’application à partir de la version séquencée précédente.</span><span class="sxs-lookup"><span data-stu-id="57ce0-117">Select **Generate Difference File** to generate a difference file for the application from the previous sequenced version.</span></span>

4.  <span data-ttu-id="57ce0-118">Pour créer un package d’installation, sélectionnez **générer le package Microsoft Windows Installer (MSI)** .</span><span class="sxs-lookup"><span data-stu-id="57ce0-118">Select **Generate Microsoft Windows Installer (MSI) Package** to create an installer package.</span></span>

## <span data-ttu-id="57ce0-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57ce0-119">Related topics</span></span>


[<span data-ttu-id="57ce0-120">À propos de l'onglet Déploiement</span><span class="sxs-lookup"><span data-stu-id="57ce0-120">About the Deployment Tab</span></span>](about-the-deployment-tab.md)

[<span data-ttu-id="57ce0-121">Console Sequencer</span><span class="sxs-lookup"><span data-stu-id="57ce0-121">Sequencer Console</span></span>](sequencer-console.md)

 

 






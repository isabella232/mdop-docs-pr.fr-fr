---
title: Installation d'App-V5.0 Client pour le mode Magasin de contenu partagé
description: Installation d'App-V5.0 Client pour le mode Magasin de contenu partagé
author: dansimp
ms.assetid: 88f09e6f-19e7-48ea-965a-907052d1a02f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 704ea6c1e4b1ba4670a4e52d754b8e6e5a9fb8f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805442"
---
# <span data-ttu-id="1cd4f-103">Installation d'App-V5.0 Client pour le mode Magasin de contenu partagé</span><span class="sxs-lookup"><span data-stu-id="1cd4f-103">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>


<span data-ttu-id="1cd4f-104">Utilisez la procédure suivante pour installer le client Microsoft Application Virtualization (App-V) 5,0 de façon à ce qu’il utilise le mode SCS (App-5,0 V) Shared content Store.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 client so that it uses the App-V 5.0 Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="1cd4f-105">Assurez-vous que toutes les conditions préalables requises sont installées sur l’ordinateur sur lequel vous envisagez d’installer.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-105">You should ensure that all required prerequisites are installed on the computer you plan to install to.</span></span> <span data-ttu-id="1cd4f-106">Utilisez le lien suivant pour une [Configuration requise pour App-V 5,0](app-v-50-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="1cd4f-106">Use the following link for a [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

<span data-ttu-id="1cd4f-107">**Remarques**  Avant d’effectuer cette procédure, si nécessaire, désinstallez les versions existantes du client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-107">**Note** Before performing this procedure if necessary uninstall any existing version of the App-V 5.0 client.</span></span>

 

<span data-ttu-id="1cd4f-108">Pour plus d’informations sur le mode SCS, voir [magasin de contenus partagés dans Microsoft App-V 5,0-en coulisses](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .</span><span class="sxs-lookup"><span data-stu-id="1cd4f-108">For more information about SCS mode, see [Shared Content Store in Microsoft App-V 5.0 – Behind the Scenes](https://go.microsoft.com/fwlink/?LinkId=316879) (https://go.microsoft.com/fwlink/?LinkId=316879).</span></span>

**<span data-ttu-id="1cd4f-109">Installer et configurer le client App-V 5,0 pour le mode SCS</span><span class="sxs-lookup"><span data-stu-id="1cd4f-109">Install and configure the App-V 5.0 client for SCS mode</span></span>**

1.  <span data-ttu-id="1cd4f-110">Copiez les fichiers d’installation du client App-V 5,0 sur l’ordinateur sur lequel il est installé.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-110">Copy the App-V 5.0 client installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="1cd4f-111">Ouvrez une ligne de commande et à partir du répertoire où sont enregistrés les fichiers d’installation, tapez l’une des options suivantes, en fonction de la version du client que vous installez:</span><span class="sxs-lookup"><span data-stu-id="1cd4f-111">Open a command line and from the directory where the installation files are saved type one of the following options depending on the version of the client you are installing:</span></span>

    -   <span data-ttu-id="1cd4f-112">Pour installer la version RDS du type de client App-V 5,0: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-112">To install the RDS version of the App-V 5.0 client type: **appv\_client\_setup\_rds.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

    -   <span data-ttu-id="1cd4f-113">Pour installer la version standard du type de client App-V 5,0: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="1cd4f-113">To install the standard version of the App-V 5.0 client type: **appv\_client\_setup.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

        <span data-ttu-id="1cd4f-114">**Important**  Vous devez effectuer une installation silencieuse ou l’installation échouera.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-114">**Important** You must perform a silent installation or the installation will fail.</span></span>

         

2.  <span data-ttu-id="1cd4f-115">Une fois l’installation terminée, vous pouvez déployer des packages vers l’ordinateur exécutant le client et le contenu de tous les packages sera diffusé sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="1cd4f-115">After you have completed the installation you can deploy packages to the computer running the client and all package contents will be streamed across the network.</span></span>

    <span data-ttu-id="1cd4f-116">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="1cd4f-116">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="1cd4f-117">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="1cd4f-117">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="1cd4f-118">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="1cd4f-118">Got an App-V issue?</span></span>** <span data-ttu-id="1cd4f-119">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="1cd4f-119">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="1cd4f-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1cd4f-120">Related topics</span></span>


[<span data-ttu-id="1cd4f-121">Déploiement d'App-V5.0 Sequencer et Client</span><span class="sxs-lookup"><span data-stu-id="1cd4f-121">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 






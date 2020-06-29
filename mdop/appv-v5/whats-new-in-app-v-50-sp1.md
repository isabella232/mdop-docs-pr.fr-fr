---
title: Nouveautés dans App-V5.0 SP1
description: Nouveautés dans App-V5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804812"
---
# <span data-ttu-id="f63da-103">Nouveautés dans App-V5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="f63da-103">What's new in App-V 5.0 SP1</span></span>


<span data-ttu-id="f63da-104">Cette section s’utilise pour les utilisateurs qui connaissent déjà App-V et qui souhaitent savoir ce qui a changé dans App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="f63da-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 SP1.</span></span> <span data-ttu-id="f63da-105">Si vous n’avez pas encore l’habitude d’utiliser l’application-V, vous devez commencer par lire la [planification pour App-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="f63da-105">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="f63da-106">Modifications apportées aux fonctionnalités standard</span><span class="sxs-lookup"><span data-stu-id="f63da-106">Changes in Standard Functionality</span></span>


<span data-ttu-id="f63da-107">Les sections suivantes contiennent des informations sur les modifications apportées aux fonctionnalités standard pour App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="f63da-107">The following sections contain information about the changes in standard functionality for App-V 5.0 SP1.</span></span>

### <span data-ttu-id="f63da-108">Modifications apportées aux langues prises en charge</span><span class="sxs-lookup"><span data-stu-id="f63da-108">Changes to Supported Languages</span></span>

<span data-ttu-id="f63da-109">Pour plus d’informations, voir [à propos de App-V 5,0 SP1](about-app-v-50-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="f63da-109">For more information, see [About App-V 5.0 SP1](about-app-v-50-sp1.md).</span></span>

<span data-ttu-id="f63da-110">La liste suivante contient des informations supplémentaires sur les nouveaux modules linguistiques:</span><span class="sxs-lookup"><span data-stu-id="f63da-110">The following list contains more information about the new Language Packs:</span></span>

-   <span data-ttu-id="f63da-111">Les modules linguistiques App-V 5.0 SP1 sont intégrés au programme d’installation de **appv\_xxx\_setup.exe** pour tous les composants App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="f63da-111">The App-V 5.0SP1 language packs are bundled into the **appv\_xxx\_setup.exe** installer for all the App-V 5.0 Components.</span></span>

-   <span data-ttu-id="f63da-112">Lorsque vous exécutez le programme d’installation, le module linguistique le plus approprié est automatiquement installé en fonction des paramètres régionaux du système d’exploitation associé exécuté sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="f63da-112">When you run the installer it will automatically install the most appropriate language pack based on the locale of the associated operating system running on the target computer.</span></span>

-   <span data-ttu-id="f63da-113">Si des modules linguistiques supplémentaires sont requis, vous devez extraire ces modules linguistiques du programme d’installation en exécutant la commande suivante: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` .</span><span class="sxs-lookup"><span data-stu-id="f63da-113">If additional language packs are required, you must extract these language packs from the installer by running the following command: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”`.</span></span> <span data-ttu-id="f63da-114">Après l’exécution, le contenu du programme d’installation est extrait à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="f63da-114">After this has been run, the contents of the installer are extracted to the specified location.</span></span>

-   <span data-ttu-id="f63da-115">Vous devez installer le module linguistique souhaité en appliquant le fichier d’installation Windows du module linguistique approprié.</span><span class="sxs-lookup"><span data-stu-id="f63da-115">You must install the desired language pack by applying the appropriate Language pack Windows Installation file.</span></span> <span data-ttu-id="f63da-116">Par exemple, **appv\_hib\_LP\_jmmb\_x86.msi** ou **appv\_hib\_LP\_jmmb\_x64.msi**, où **Hib** fait référence au composant et **jmmb** fait référence aux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="f63da-116">For example, **appv\_hib\_LP\_jmmb\_x86.msi** or **appv\_hib\_LP\_jmmb\_x64.msi**, where **hib** refers to the component and **jmmb** refers to the locale.</span></span>

## <span data-ttu-id="f63da-117">Prise en charge améliorée de Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="f63da-117">Enhanced Support for Microsoft Office2010</span></span>


<span data-ttu-id="f63da-118">**Kit de séquençage Microsoft Office 2010 pour la virtualisation des applications 5,0** : permet aux utilisateurs d’avoir une interface cohérente à l’aide d’une version virtualisée de Microsoft Office 2010.</span><span class="sxs-lookup"><span data-stu-id="f63da-118">**Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** – helps provide users with a consistent experience using a virtualized version of Microsoft Office2010.</span></span> <span data-ttu-id="f63da-119">Le **Kit de séquençage Microsoft office 2010 pour application virtualization 5,0** est utilisé conjointement avec le **Kit de déploiement de Microsoft Office 2010 pour App-V** et fournit également le service de gestion des licences Microsoft Office 2010 requis.</span><span class="sxs-lookup"><span data-stu-id="f63da-119">The **Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** is used in conjunction with the **Microsoft Office 2010 Deployment Kit for App-V** and also provides the required Microsoft Office2010 licensing service.</span></span>






## <span data-ttu-id="f63da-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f63da-120">Related topics</span></span>


[<span data-ttu-id="f63da-121">À propos d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="f63da-121">About App-V 5.0</span></span>](about-app-v-50.md)

 

 






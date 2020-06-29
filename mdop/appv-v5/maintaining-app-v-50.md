---
title: Maintenance d'App-V5.0
description: Maintenance d'App-V5.0
author: dansimp
ms.assetid: 66851ec3-c674-493b-ad6d-db8fcbf1956c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3445bfe00ba7703a66fa3da2f9d7089990dd3854
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805112"
---
# <span data-ttu-id="3a568-103">Maintenance d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="3a568-103">Maintaining App-V 5.0</span></span>


<span data-ttu-id="3a568-104">Après avoir effectué toutes les opérations de planification nécessaires, puis le déploiement de App-V 5,0, vous pouvez utiliser les informations suivantes pour gérer l’infrastructure App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a568-104">After you have completed all the necessary planning, and then deployment of App-V 5.0, you can use the following information to maintain the App-V 5.0 infrastructure.</span></span>

## <a href="" id="move-the-app-v-5-0-server-"></a><span data-ttu-id="3a568-105">Déplacer le serveur App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3a568-105">Move the App-V 5.0 Server</span></span>


<span data-ttu-id="3a568-106">Le serveur App-V 5,0 se connecte à la base de données App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a568-106">The App-V 5.0 server connects to the App-V 5.0 database.</span></span> <span data-ttu-id="3a568-107">Par conséquent, vous pouvez installer le composant de gestion sur n’importe quel ordinateur du réseau, puis le connecter à la base de données App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a568-107">Therefore you can install the management component to any computer on the network and then connect it to the App-V 5.0 database.</span></span>

[<span data-ttu-id="3a568-108">Comment déplacer le serveur App-V vers un autre ordinateur</span><span class="sxs-lookup"><span data-stu-id="3a568-108">How to Move the App-V Server to Another Computer</span></span>](how-to-move-the-app-v-server-to-another-computer.md)

## <a href="" id="determine-if-an-app-v-5-0-application-is-running-virtualized-"></a><span data-ttu-id="3a568-109">Déterminer si une application application-V 5,0 est en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="3a568-109">Determine if an App-V 5.0 Application is Running Virtualized</span></span>


<span data-ttu-id="3a568-110">Les éditeurs de logiciels indépendants qui souhaitent déterminer si une application est en cours d’exécution avec App-V 5,0 ou une version ultérieure, doivent ouvrir un objet nommé appelé **AppVVirtual &lt; - &gt; PID** dans l’espace de noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="3a568-110">Independent software vendors (ISV) who want to determine if an application is running virtualized with App-V 5.0 or above, should open a named object called **AppVVirtual-&lt;PID&gt;** in the default namespace.</span></span> <span data-ttu-id="3a568-111">Par exemple, l’API Windows **GetCurrentProcessId ()** peut être utilisée pour obtenir l’ID du processus actuel, par exemple 4052, et si un objet d’événement nommé appelé **AppVVirtual-4052** peut être ouvert avec succès à l’aide de **OpenEvent ()** dans l’espace de noms par défaut pour l’accès en lecture, l’application est virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3a568-111">For example, Windows API **GetCurrentProcessId()** can be used to obtain the current process's ID, for example 4052, and then if a named Event object called **AppVVirtual-4052** can be successfully opened using **OpenEvent()** in the default namespace for read access, then the application is virtual.</span></span> <span data-ttu-id="3a568-112">En cas d’échec de l’appel de **OpenEvent ()** , l’application n’est pas virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3a568-112">If the **OpenEvent()** call fails, the application is not virtual.</span></span>

<span data-ttu-id="3a568-113">De plus, les éditeurs de logiciels indépendants qui souhaitent virtualiser ou ne pas virtualiser les appels sur des API spécifiques avec App-V 5,0 ou une version ultérieure peuvent utiliser les fonctions **VirtualizeCurrentThread ()** et **CurrentThreadIsVirtualized ()** implémentées dans le module AppEntSubsystems32.dll.</span><span class="sxs-lookup"><span data-stu-id="3a568-113">Additionally, ISV’s who want to explicitly virtualize or not virtualize calls on specific API’s with App-V 5.0 and above, can use the **VirtualizeCurrentThread()** and **CurrentThreadIsVirtualized()** functions implemented in the AppEntSubsystems32.dll module.</span></span> <span data-ttu-id="3a568-114">Celles-ci fournissent un moyen d’attirer l’œil sur un composant en aval qui ne doit pas être virtualisé.</span><span class="sxs-lookup"><span data-stu-id="3a568-114">These provide a way of hinting at a downstream component that the call should or should not be virtualized.</span></span>






## <span data-ttu-id="3a568-115">Autres ressources pour la maintenance de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3a568-115">Other resources for maintaining App-V 5.0</span></span>


[<span data-ttu-id="3a568-116">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="3a568-116">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 






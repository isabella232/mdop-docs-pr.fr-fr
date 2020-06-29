---
title: Détermination de l'état de chiffrement BitLocker des ordinateurs perdus
description: Détermination de l'état de chiffrement BitLocker des ordinateurs perdus
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810577"
---
# <span data-ttu-id="156c3-103">Détermination de l'état de chiffrement BitLocker des ordinateurs perdus</span><span class="sxs-lookup"><span data-stu-id="156c3-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="156c3-104">Utilisez cette procédure avec le site Web d’administration et de contrôle pour déterminer les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="156c3-104">Use this procedure with the Administration and Monitoring Website to determine the following:</span></span>

-   <span data-ttu-id="156c3-105">Le dernier état du chiffrement BitLocker connu des ordinateurs perdus ou volés</span><span class="sxs-lookup"><span data-stu-id="156c3-105">The last known BitLocker encryption status of lost or stolen computers</span></span>

-   <span data-ttu-id="156c3-106">Le chiffrement des volumes sur un ordinateur perdu ou volé</span><span class="sxs-lookup"><span data-stu-id="156c3-106">Whether the volumes on a lost or stolen computer were encrypted</span></span>

<span data-ttu-id="156c3-107">Pour effectuer cette tâche, vous devez accéder à la zone **rapports** du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="156c3-107">To complete this task, you need access to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="156c3-108">Pour pouvoir accéder à cette zone, vous devez avoir le rôle d’utilisateur de rapport MBAM.</span><span class="sxs-lookup"><span data-stu-id="156c3-108">To get access to this area, you must be assigned the MBAM Report Users role.</span></span> <span data-ttu-id="156c3-109">Il est possible que vous ayez attribué un nom différent aux rôles lorsque vous les avez créés.</span><span class="sxs-lookup"><span data-stu-id="156c3-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="156c3-110">Pour plus d’informations, reportez-vous [à planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="156c3-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="156c3-111">**Remarques**  La conformité de l’appareil est déterminée par les stratégies BitLocker déployées par votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="156c3-111">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="156c3-112">Il est possible que vous souhaitiez vérifier vos stratégies déployées avant d’essayer de déterminer l’état de chiffrement BitLocker d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="156c3-112">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

 

**<span data-ttu-id="156c3-113">Pour déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus</span><span class="sxs-lookup"><span data-stu-id="156c3-113">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="156c3-114">Ouvrez un navigateur Web, puis accédez au **site Web d’administration et de surveillance**.</span><span class="sxs-lookup"><span data-stu-id="156c3-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="156c3-115">Dans le volet gauche, sélectionnez **rapports** pour ouvrir la page rapports.</span><span class="sxs-lookup"><span data-stu-id="156c3-115">In the left pane, select **Reports** to open the Reports page.</span></span>

3.  <span data-ttu-id="156c3-116">Sélectionnez le **rapport de conformité**de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="156c3-116">Select the **Computer Compliance Report**.</span></span>

4.  <span data-ttu-id="156c3-117">Utilisez les champs de filtre dans le volet droit pour affiner les résultats de la recherche, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="156c3-117">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="156c3-118">Les résultats sont affichés sous votre requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="156c3-118">Results are shown under your search query.</span></span>

5.  <span data-ttu-id="156c3-119">Prenez l’action appropriée, déterminée par votre politique pour les appareils perdus.</span><span class="sxs-lookup"><span data-stu-id="156c3-119">Take the appropriate action, as determined by your policy for lost devices.</span></span>



## <span data-ttu-id="156c3-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="156c3-120">Related topics</span></span>


[<span data-ttu-id="156c3-121">Gestion de BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="156c3-121">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="156c3-122">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="156c3-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="156c3-123">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="156c3-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="156c3-124">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="156c3-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 






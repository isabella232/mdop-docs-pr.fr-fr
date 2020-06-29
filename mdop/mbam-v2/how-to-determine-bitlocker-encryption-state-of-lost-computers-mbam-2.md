---
title: Détermination de l'état de chiffrement BitLocker des ordinateurs perdus
description: Détermination de l'état de chiffrement BitLocker des ordinateurs perdus
author: dansimp
ms.assetid: dbd23b64-dff3-4913-9acd-affe67b9462e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9ea4afd6dd08f2040b9e2bd1e1a8998181d1e60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810661"
---
# <span data-ttu-id="69b0e-103">Détermination de l'état de chiffrement BitLocker des ordinateurs perdus</span><span class="sxs-lookup"><span data-stu-id="69b0e-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="69b0e-104">Vous pouvez utiliser l’analyse et la surveillance de BitLocker (MBAM) pour déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus ou volés.</span><span class="sxs-lookup"><span data-stu-id="69b0e-104">You can use Microsoft BitLocker Administration and Monitoring (MBAM) to determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span> <span data-ttu-id="69b0e-105">La procédure suivante vous explique comment déterminer si les volumes sur un ordinateur sont chiffrés en cas de perte ou de vol.</span><span class="sxs-lookup"><span data-stu-id="69b0e-105">The following procedure explains how to determine whether the volumes on a computer are encrypted if there is a loss or theft.</span></span>

**<span data-ttu-id="69b0e-106">Pour déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus</span><span class="sxs-lookup"><span data-stu-id="69b0e-106">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="69b0e-107">Ouvrez un navigateur Web, puis accédez au site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="69b0e-107">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

    <span data-ttu-id="69b0e-108">**Remarques**  Remarque: l’adresse par défaut du site Web d’administration et de surveillance est http://\* &lt; nomordinateur &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="69b0e-108">**Note** Note: The default address for the Administration and Monitoring website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="69b0e-109">L’utilisation du nom de serveur complet accélère les résultats de la navigation.</span><span class="sxs-lookup"><span data-stu-id="69b0e-109">Using the fully qualified server name will yield faster browsing results.</span></span>

     

2.  <span data-ttu-id="69b0e-110">Sélectionne le nœud de **rapport** dans le volet de navigation, puis sélectionne le **rapport de conformité**de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="69b0e-110">Selects the **Report** node from the navigation pane, and select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="69b0e-111">Utilisez les champs de filtre dans le volet droit pour affiner les résultats de la recherche, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="69b0e-111">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="69b0e-112">Les résultats sont affichés sous votre requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="69b0e-112">Results are shown below your search query.</span></span>

4.  <span data-ttu-id="69b0e-113">Prenez l’action appropriée, déterminée par votre politique pour les appareils perdus.</span><span class="sxs-lookup"><span data-stu-id="69b0e-113">Take the appropriate action, as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="69b0e-114">**Remarques**  La conformité de l’appareil est déterminée par les stratégies BitLocker déployées par votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="69b0e-114">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="69b0e-115">Il est possible que vous souhaitiez vérifier vos stratégies déployées avant d’essayer de déterminer l’état de chiffrement BitLocker d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="69b0e-115">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="69b0e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69b0e-116">Related topics</span></span>


[<span data-ttu-id="69b0e-117">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="69b0e-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 






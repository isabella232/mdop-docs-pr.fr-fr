---
title: Détermination de l'état de chiffrement BitLocker d'un ordinateur perdu
description: Détermination de l'état de chiffrement BitLocker d'un ordinateur perdu
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810469"
---
# <span data-ttu-id="098c7-103">Détermination de l'état de chiffrement BitLocker d'un ordinateur perdu</span><span class="sxs-lookup"><span data-stu-id="098c7-103">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>


<span data-ttu-id="098c7-104">Microsoft BitLocker Administration and Monitoring (MBAM) vous permet de déterminer le dernier état de chiffrement BitLocker connu pour les ordinateurs perdus ou volés.</span><span class="sxs-lookup"><span data-stu-id="098c7-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to determine the last known BitLocker encryption status of computers that are lost or stolen.</span></span> <span data-ttu-id="098c7-105">Utilisez la procédure suivante pour déterminer si les volumes ont été chiffrés sur des ordinateurs qui ne sont plus en votre possession.</span><span class="sxs-lookup"><span data-stu-id="098c7-105">Use the following procedure to determine whether the volumes have been encrypted on computers that are no longer in your possession.</span></span>

**<span data-ttu-id="098c7-106">Déterminer le dernier état de chiffrement BitLocker connu d’un ordinateur</span><span class="sxs-lookup"><span data-stu-id="098c7-106">Determine a Computer's Last Known BitLocker Encryption state</span></span>**

1.  <span data-ttu-id="098c7-107">Ouvrez le site Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="098c7-107">Open the MBAM website.</span></span>

    <span data-ttu-id="098c7-108">**Remarques**  L’adresse par défaut du site Web MBAM est http://\* &lt; nomordinateur &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="098c7-108">**Note** The default address for the MBAM website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="098c7-109">Utilisez le nom de serveur complet pour accélérer les résultats de la navigation.</span><span class="sxs-lookup"><span data-stu-id="098c7-109">Use the fully qualified server name for faster browsing results.</span></span>

     

2.  <span data-ttu-id="098c7-110">Sélectionnez le nœud de **rapport** dans le volet de navigation, puis sélectionnez le **rapport de conformité**de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="098c7-110">Select the **Report** node from the navigation pane, and then select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="098c7-111">Utilisez les champs de filtre dans le volet droit pour affiner les résultats de la recherche, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="098c7-111">Use the filter fields in the right-side pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="098c7-112">Les résultats s’affichent sous votre requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="098c7-112">Results will be shown below your search query.</span></span>

4.  <span data-ttu-id="098c7-113">Effectuez l’action appropriée en fonction de votre politique pour les appareils perdus.</span><span class="sxs-lookup"><span data-stu-id="098c7-113">Take the appropriate action as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="098c7-114">**Remarques**  La conformité de l’appareil est déterminée par les stratégies BitLocker déployées.</span><span class="sxs-lookup"><span data-stu-id="098c7-114">**Note** Device compliance is determined by the deployed BitLocker policies.</span></span> <span data-ttu-id="098c7-115">Vous devez vérifier ces stratégies déployées lorsque vous essayez de déterminer l’état de chiffrement BitLocker d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="098c7-115">You should verify these deployed policies when you are trying to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="098c7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="098c7-116">Related topics</span></span>


[<span data-ttu-id="098c7-117">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="098c7-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 






---
title: Surveillance des compteurs de performances pour les demandes de service web
description: Surveillance des compteurs de performances pour les demandes de service web
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810218"
---
# <span data-ttu-id="1ec1b-103">Surveillance des compteurs de performances pour les demandes de service web</span><span class="sxs-lookup"><span data-stu-id="1ec1b-103">Monitoring Web Service Request Performance Counters</span></span>


<span data-ttu-id="1ec1b-104">Le service d’administration et de surveillance de BitLocker Microsoft (MBAM) fournit des compteurs de performance qui enregistrent les performances des requêtes envoyées aux services Web suivants:</span><span class="sxs-lookup"><span data-stu-id="1ec1b-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides performance counters that record the performance of requests that are sent to the following web services:</span></span>

-   <span data-ttu-id="1ec1b-105">**StatusReportingService. svc** -service qui reçoit des demandes de statut de conformité</span><span class="sxs-lookup"><span data-stu-id="1ec1b-105">**StatusReportingService.svc** – service that receives requests for compliance status</span></span>

-   <span data-ttu-id="1ec1b-106">**CoreService. svc** -service qui reçoit des demandes de tentatives de récupération de clés</span><span class="sxs-lookup"><span data-stu-id="1ec1b-106">**CoreService.svc** – service that receives requests for key recovery attempts</span></span>

## <span data-ttu-id="1ec1b-107">Compteurs de performance fournis par MBAM</span><span class="sxs-lookup"><span data-stu-id="1ec1b-107">Performance counters that MBAM provides</span></span>


<span data-ttu-id="1ec1b-108">MBAM fournit les compteurs de performance suivants pour chacune des méthodes publiques qui sont implémentées par ses services Web StatusReportingService et CoreService:</span><span class="sxs-lookup"><span data-stu-id="1ec1b-108">MBAM provides the following performance counters for each of the public methods that is implemented by its StatusReportingService and CoreService web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ec1b-109">Type de compteur de performance</span><span class="sxs-lookup"><span data-stu-id="1ec1b-109">Type of performance counter</span></span></th>
<th align="left"><span data-ttu-id="1ec1b-110">Description</span><span class="sxs-lookup"><span data-stu-id="1ec1b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ec1b-111">Nombre total de demandes</span><span class="sxs-lookup"><span data-stu-id="1ec1b-111">Total number of requests</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ec1b-112">Fournit un nombre d’incréments commençant à zéro lors du démarrage ou du redémarrage du serveur.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-112">Provides an incrementing count that starts from zero when the server is started or restarted.</span></span></p>
<p><span data-ttu-id="1ec1b-113">Fournit une vue globale de l’activité du système.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-113">Provides an overall view of system activity.</span></span> <span data-ttu-id="1ec1b-114">Peuvent être surveillés par des outils automatisés pour garantir l’intégrité du serveur et vérifier que le compteur est incrémenté d’une période donnée.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-114">Can be monitored by automated tools to ensure the health of the server and to validate that the counter continually increments over a specified period of time.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ec1b-115">Demandes par seconde</span><span class="sxs-lookup"><span data-stu-id="1ec1b-115">Requests per second</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ec1b-116">Indique le débit actuel du serveur MBAM car il prend en charge la base de clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-116">Indicates the current throughput of the MBAM Server as it supports the MBAM client base.</span></span></p>
<p><span data-ttu-id="1ec1b-117">Permet aux administrateurs de sites d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="1ec1b-117">Enables site administrators to:</span></span></p>
<ul>
<li><p><span data-ttu-id="1ec1b-118">Calculez le nombre moyen de demandes par seconde, en fonction du nombre de clients MBAM et de la fréquence de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-118">Calculate the average number of requests per second, based on the number of MBAM Clients and their reporting frequency.</span></span></p></li>
<li><p><span data-ttu-id="1ec1b-119">Vérifiez que le nombre de demandes par seconde est corrélé de manière générale avec le nombre moyen de demandes par seconde calculée.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-119">Validate that the number of requests per second broadly correlates with the calculated average number of requests per second.</span></span> <span data-ttu-id="1ec1b-120">Une variance significative peut indiquer que le client MBAM n’est pas installé sur un pourcentage de la base du client ou qu’un objet de stratégie de groupe MBAM n’a pas été déployé correctement.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-120">A significant variance can indicate that the MBAM Client isn't installed on a percentage of the client base or that an MBAM Group Policy Object hasn't been successfully deployed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ec1b-121">Durée de la demande</span><span class="sxs-lookup"><span data-stu-id="1ec1b-121">Request duration</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ec1b-122">Enregistre la durée des demandes en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-122">Records the duration of requests in milliseconds.</span></span></p>
<p><span data-ttu-id="1ec1b-123">Même si ce compteur est mis à jour en fonction de la durée de chaque demande, les exemples de l’analyseur de performance Windows s’en trouvent périodiquement (en général, toutes les secondes), de sorte que vous pouvez voir la variabilité de la valeur.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-123">Although this counter is updated with the duration of each request, Windows Performance Monitor samples it only periodically (typically every second), so you might see some variability in the value.</span></span> <span data-ttu-id="1ec1b-124">Pour cette raison, envisagez d’utiliser la valeur moyenne affichée par l’analyseur de performances.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-124">For this reason, consider using the average value displayed by Performance Monitor.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1ec1b-125">Résultats et recommandations relatifs aux compteurs de performance</span><span class="sxs-lookup"><span data-stu-id="1ec1b-125">Performance counter results and recommendations</span></span>


<span data-ttu-id="1ec1b-126">Lorsque vous ajoutez de nouveaux clients MBAM à un serveur MBAM doté de capacités de secours, vous vous attendez à voir une augmentation du nombre de demandes par seconde.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-126">As you add new MBAM Clients to an MBAM Server with spare capacity, expect to see an increase in the number of requests per second.</span></span> <span data-ttu-id="1ec1b-127">Ce renforcement sera proportionnel au nombre de nouveaux ordinateurs client.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-127">This increase will be proportional to the number of new client computers.</span></span> <span data-ttu-id="1ec1b-128">La durée de requête moyenne reste relativement statique.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-128">The average request duration will remain relatively static.</span></span> <span data-ttu-id="1ec1b-129">Lorsque le serveur est proche de sa capacité maximale, les demandes par seconde commencent à se mettre en niveau, et la durée de requête moyenne commence à être plus longue.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-129">As the server nears its maximum capacity, the requests per second start to level out, and the average request duration starts to get longer.</span></span>

<span data-ttu-id="1ec1b-130">Si vos serveurs MBAM peuvent prendre en charge votre base de clients, envisagez de déployer MBAM par phases sur différentes collections d’ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-130">If you are concerned about whether your MBAM Servers can support your client base, consider deploying MBAM in phases across different collections of client computers.</span></span> <span data-ttu-id="1ec1b-131">Lorsque vous déployez MBAM sur chaque collection d’ordinateurs clients, nous vous conseillons de prendre des instantanés des compteurs de performance pour voir l’impact relatif du déploiement vers chaque nouvelle collection de clients.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-131">As you deploy MBAM to each collection of client computers, we recommend that you take snapshots of the performance counters to see the relative impact of deploying to each new client collection.</span></span> <span data-ttu-id="1ec1b-132">Si le nombre de demandes par seconde commence au niveau inférieur et que la durée de la requête moyenne augmente, envisagez d’améliorer l’infrastructure de votre serveur MBAM en effectuant l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="1ec1b-132">If the number of requests per second starts to level off and the average request duration increases, consider enhancing your MBAM Server infrastructure by doing one of the following:</span></span>

-   <span data-ttu-id="1ec1b-133">Déplacement de la base de données MBAM vers un cluster Microsoft SQL Server ou SQL Server dédié</span><span class="sxs-lookup"><span data-stu-id="1ec1b-133">Moving the MBAM database onto a dedicated Microsoft SQL Server or SQL Server cluster</span></span>

-   <span data-ttu-id="1ec1b-134">MBAM de l’équilibrage de charge sur plusieurs serveurs Web Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="1ec1b-134">Load-balancing MBAM across multiple Internet Information Services (IIS) web servers</span></span>

-   <span data-ttu-id="1ec1b-135">Déploiement de MBAM sur un matériel serveur plus puissant</span><span class="sxs-lookup"><span data-stu-id="1ec1b-135">Deploying MBAM on more powerful server hardware</span></span>

## <span data-ttu-id="1ec1b-136">Affichage des compteurs de performance</span><span class="sxs-lookup"><span data-stu-id="1ec1b-136">Viewing performance counters</span></span>


<span data-ttu-id="1ec1b-137">L’outil recommandé pour afficher les compteurs de performance MBAM est moniteur de performance Windows, qui est fourni avec Windows.</span><span class="sxs-lookup"><span data-stu-id="1ec1b-137">The recommended tool for viewing MBAM performance counters is Windows Performance Monitor, which comes with Windows.</span></span> <span data-ttu-id="1ec1b-138">Si vous utilisez Windows PowerShell, vous n’avez pas besoin d’activer les compteurs avant de les afficher, dans la mesure où ils sont automatiquement enregistrés par l’applet de cmdlet Windows PowerShell **Enable-WebApplication** .</span><span class="sxs-lookup"><span data-stu-id="1ec1b-138">If you are using Windows PowerShell, you don’t need to enable the counters before viewing them, as they are automatically registered by the Windows PowerShell **Enable-webapplication** cmdlet.</span></span>

<span data-ttu-id="1ec1b-139">Pour obtenir des instructions détaillées sur l’affichage des compteurs de performance, voir [comment afficher les compteurs de performances de MBAM](https://go.microsoft.com/fwlink/?LinkId=393457).</span><span class="sxs-lookup"><span data-stu-id="1ec1b-139">For detailed instructions on how to view performance counters, see [How to View MBAM Performance Counters](https://go.microsoft.com/fwlink/?LinkId=393457).</span></span>



## <span data-ttu-id="1ec1b-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ec1b-140">Related topics</span></span>


[<span data-ttu-id="1ec1b-141">Gestion de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="1ec1b-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)

 

 


## <span data-ttu-id="1ec1b-142">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="1ec1b-142">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1ec1b-143">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="1ec1b-143">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="1ec1b-144">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1ec1b-144">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



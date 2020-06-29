---
title: Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell
description: Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell
author: dansimp
ms.assetid: a7aaf553-0f83-4cd0-8df8-93a5f1ebe497
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c004b4900a9814a11cb2706659a2edb99de6cc1b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805466"
---
# <span data-ttu-id="60a3c-103">Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="60a3c-103">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>


<span data-ttu-id="60a3c-104">Utilisez la procédure suivante pour configurer l’application-V 5,0 pour la création de rapports.</span><span class="sxs-lookup"><span data-stu-id="60a3c-104">Use the following procedure to configure the App-V 5.0 for reporting.</span></span>

**<span data-ttu-id="60a3c-105">Pour configurer l’ordinateur exécutant le client App-V 5,0 pour la création de rapports</span><span class="sxs-lookup"><span data-stu-id="60a3c-105">To configure the computer running the App-V 5.0 client for reporting</span></span>**

1. <span data-ttu-id="60a3c-106">Installez le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="60a3c-106">Install the App-V 5.0 client.</span></span> <span data-ttu-id="60a3c-107">Pour plus d’informations sur l’installation du client [, voir comment déployer le client App-V](how-to-deploy-the-app-v-client-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="60a3c-107">For more information about installing the client see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md).</span></span>

2. <span data-ttu-id="60a3c-108">Après avoir installé le client App-V 5,0, utilisez **Set-AppvClientConfiguration** PowerShell pour configurer les paramètres de configuration de rapport appropriés:</span><span class="sxs-lookup"><span data-stu-id="60a3c-108">After you have installed the App-V 5.0 client, use the **Set-AppvClientConfiguration** PowerShell to configure appropriate Reporting Configuration settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="60a3c-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="60a3c-109">Setting</span></span></th>
   <th align="left"><span data-ttu-id="60a3c-110">Description</span><span class="sxs-lookup"><span data-stu-id="60a3c-110">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="60a3c-111">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="60a3c-111">ReportingEnabled</span></span></p></td>
   <td align="left"><p><span data-ttu-id="60a3c-112">Permet au client de renvoyer des informations vers un serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="60a3c-112">Enables the client to return information to a reporting server.</span></span> <span data-ttu-id="60a3c-113">Ce paramètre est requis pour que le client récupère les données de rapport sur le client.</span><span class="sxs-lookup"><span data-stu-id="60a3c-113">This setting is required for the client to collect the reporting data on the client.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="60a3c-114">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="60a3c-114">ReportingServerURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="60a3c-115">Spécifie l’emplacement sur le serveur de création de rapports où les informations client sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="60a3c-115">Specifies the location on the reporting server where client information is saved.</span></span> <span data-ttu-id="60a3c-116">Par exemple, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</span><span class="sxs-lookup"><span data-stu-id="60a3c-116">For example, http://&lt;reportingservername&gt;:&lt;reportingportnumber&gt;.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="60a3c-117">Remarque</span><span class="sxs-lookup"><span data-stu-id="60a3c-117">Note</span></span></strong><br/><p><span data-ttu-id="60a3c-118">Il s’agit du numéro de port attribué lors de la configuration du serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="60a3c-118">This is the port number that was assigned during the Reporting Server setup</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="60a3c-119">Heures de début de création de rapports</span><span class="sxs-lookup"><span data-stu-id="60a3c-119">Reporting Start Time</span></span></p></td>
   <td align="left"><p><span data-ttu-id="60a3c-120">Il est défini pour planifier le client pour envoyer automatiquement les données au serveur.</span><span class="sxs-lookup"><span data-stu-id="60a3c-120">This is set to schedule the client to automatically send the data to the server.</span></span> <span data-ttu-id="60a3c-121">Ce paramètre indique l’heure à laquelle les données de rapport doivent commencer à envoyer.</span><span class="sxs-lookup"><span data-stu-id="60a3c-121">This setting will indicate the hour at which the reporting data will start to send.</span></span> <span data-ttu-id="60a3c-122">Il est au format 24 heures et prend un numéro entre 0-23.</span><span class="sxs-lookup"><span data-stu-id="60a3c-122">It is in the 24 hour format and will take a number between 0-23.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="60a3c-123">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="60a3c-123">ReportingRandomDelay</span></span></p></td>
   <td align="left"><p><span data-ttu-id="60a3c-124">Spécifie le délai maximal (en minutes) pour les données à envoyer au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="60a3c-124">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="60a3c-125">Lorsque la tâche planifiée est lancée, le client génère un délai aléatoire compris entre 0 et ReportingRandomDelay et attend la durée spécifiée avant d’envoyer des données.</span><span class="sxs-lookup"><span data-stu-id="60a3c-125">When the scheduled task is started, the client generates a random delay between 0 and ReportingRandomDelay and will wait the specified duration before sending data.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="60a3c-126">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="60a3c-126">ReportingInterval</span></span></p></td>
   <td align="left"><p><span data-ttu-id="60a3c-127">Spécifie l’intervalle de réessayer que le client doit utiliser pour renvoyer les données au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="60a3c-127">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="60a3c-128">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="60a3c-128">ReportingDataCacheLimit</span></span></p></td>
   <td align="left"><p><span data-ttu-id="60a3c-129">Spécifie la taille maximale en mégaoctets (Mo) du cache XML pour le stockage des informations de rapport.</span><span class="sxs-lookup"><span data-stu-id="60a3c-129">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="60a3c-130">La taille s’applique au cache en mémoire.</span><span class="sxs-lookup"><span data-stu-id="60a3c-130">The size applies to the cache in memory.</span></span> <span data-ttu-id="60a3c-131">Lorsque la limite est atteinte, le fichier journal est restauré.</span><span class="sxs-lookup"><span data-stu-id="60a3c-131">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="60a3c-132">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="60a3c-132">ReportingDataBlockSize</span></span></p></td>
   <td align="left"><p><span data-ttu-id="60a3c-133">Spécifie la taille maximale en mégaoctets (Mo) du cache XML pour le stockage des informations de rapport.</span><span class="sxs-lookup"><span data-stu-id="60a3c-133">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="60a3c-134">La taille s’applique au cache en mémoire.</span><span class="sxs-lookup"><span data-stu-id="60a3c-134">The size applies to the cache in memory.</span></span> <span data-ttu-id="60a3c-135">Lorsque la limite est atteinte, le fichier journal est restauré.</span><span class="sxs-lookup"><span data-stu-id="60a3c-135">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="60a3c-136">Une fois les paramètres appropriés configurés, l’ordinateur exécutant le client App-V 5,0 collectera automatiquement les données et renverra les données au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="60a3c-136">After the appropriate settings have been configured, the computer running the App-V 5.0 client will automatically collect data and will send the data back to the reporting server.</span></span>

   <span data-ttu-id="60a3c-137">De plus, les administrateurs peuvent renvoyer les données manuellement en une méthode à la demande à l’aide de l’applet de requête PowerShell **Send-AppvClientReport** .</span><span class="sxs-lookup"><span data-stu-id="60a3c-137">Additionally, administrators can manually send the data back in an on-demand manner using the **Send-AppvClientReport** PowerShell cmdlet.</span></span>

   <span data-ttu-id="60a3c-138">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="60a3c-138">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="60a3c-139">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="60a3c-139">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="60a3c-140">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="60a3c-140">Got an App-V issue?</span></span>** <span data-ttu-id="60a3c-141">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="60a3c-141">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="60a3c-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60a3c-142">Related topics</span></span>


[<span data-ttu-id="60a3c-143">Administration d'App-V à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="60a3c-143">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)










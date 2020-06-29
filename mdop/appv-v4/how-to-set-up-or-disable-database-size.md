---
title: Procédure pour configurer ou désactiver la taille de base de données
description: Procédure pour configurer ou désactiver la taille de base de données
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806757"
---
# <span data-ttu-id="9d16c-103">Procédure pour configurer ou désactiver la taille de base de données</span><span class="sxs-lookup"><span data-stu-id="9d16c-103">How to Set Up or Disable Database Size</span></span>


<span data-ttu-id="9d16c-104">Vous pouvez utiliser les procédures suivantes dans la console de gestion du serveur d’applications pour spécifier la taille (en Mo) de l’utilisation du système de virtualisation des applications que vous voulez stocker dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="9d16c-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the size (in MB) of Application Virtualization System usage that you want to store in the database.</span></span>

<span data-ttu-id="9d16c-105">Lorsque la taille des données stockées atteint 95% (seuil maximal) de la limite spécifiée, le système supprime 10% des données d’utilisation en laissant 85% des données.</span><span class="sxs-lookup"><span data-stu-id="9d16c-105">When the size of the stored data reaches 95% (the high watermark) of the specified limit, the system will delete 10% of the usage data, leaving 85% of the data.</span></span> <span data-ttu-id="9d16c-106">Les données d’utilisation des packages et applications seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="9d16c-106">Package and application usage data will be deleted.</span></span> <span data-ttu-id="9d16c-107">Lorsque la taille de la base de données augmente et qu’elle approche du filigrane le plus élevé, un message d’avertissement est envoyé au journal SQL Server pour vous informer que cette limite a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="9d16c-107">When the database grows large enough and approaches the high watermark, a warning message is sent to the SQL Server log to inform you that this limit has been reached.</span></span> <span data-ttu-id="9d16c-108">Cet avertissement est nécessaire, car l’action de nettoyage peut affecter la sortie des rapports.</span><span class="sxs-lookup"><span data-stu-id="9d16c-108">This warning is necessary because the cleanup action can affect the output of the reports.</span></span> <span data-ttu-id="9d16c-109">Vous pouvez également décider si vous avez besoin d’augmenter la taille maximale de la base de données, de réduire le nombre de mois de données d’utilisation à conserver ou de désactiver le niveau de journalisation.</span><span class="sxs-lookup"><span data-stu-id="9d16c-109">It will also help you decide whether you need to increase the maximum database size, reduce the number of months of usage data to be kept, or turn down the logging level.</span></span>

<span data-ttu-id="9d16c-110">**Remarques**  Le **champ aucune limite de taille** et **conserver toutes les** options d’utilisation est fourni de sorte que vous puissiez désactiver les rapports d’utilisation et le nettoyage de la base de données.</span><span class="sxs-lookup"><span data-stu-id="9d16c-110">**Note** The **No Size Limit** and **Keep All Usage** options are provided so that you can disable usage reporting and database cleanup.</span></span> <span data-ttu-id="9d16c-111">La sélection de ces éléments entraîne le nettoyage du journal de transactions de la base de données.</span><span class="sxs-lookup"><span data-stu-id="9d16c-111">Selecting these items will clean up the database transaction log as well.</span></span> <span data-ttu-id="9d16c-112">(Toutes les transactions Microsoft SQL Server validées seront supprimées du journal de la base de données.)</span><span class="sxs-lookup"><span data-stu-id="9d16c-112">(All committed Microsoft SQL Server transactions will be removed from the database log.)</span></span>

 

**<span data-ttu-id="9d16c-113">Pour configurer la taille de la base de données</span><span class="sxs-lookup"><span data-stu-id="9d16c-113">To set up database size</span></span>**

1.  <span data-ttu-id="9d16c-114">Dans le volet gauche, cliquez avec le bouton droit sur le nœud système de virtualisation des applications, puis sélectionnez **Options système**.</span><span class="sxs-lookup"><span data-stu-id="9d16c-114">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="9d16c-115">Sélectionnez l’onglet **base de données** .</span><span class="sxs-lookup"><span data-stu-id="9d16c-115">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="9d16c-116">Activez la case d’option **taille maximale de la base de données (Mo)** ou **aucune taille** .</span><span class="sxs-lookup"><span data-stu-id="9d16c-116">Select the **Maximum Database Size (MB)** or **No Size Limit** radio button.</span></span>

4.  <span data-ttu-id="9d16c-117">Si vous choisissez de spécifier une taille de base de données, il est recommandé d’entrer un nombre compris entre 512 et 4096 Mo.</span><span class="sxs-lookup"><span data-stu-id="9d16c-117">If you choose to specify a database size, best practices recommend that you enter a number between 512 and 4096 MB.</span></span> <span data-ttu-id="9d16c-118">La taille par défaut est 1024 Mo et si vous avez besoin d’augmenter la taille de la base de données, la valeur maximale que vous pouvez entrer est 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="9d16c-118">The default size is 1024 MB and if you need to increase the database size, the maximum value you can enter is 2,147,483,647.</span></span> <span data-ttu-id="9d16c-119">Si vous **ne sélectionnez aucune limite de taille**, la base de données augmentera jusqu’à atteindre la limite de taille du disque.</span><span class="sxs-lookup"><span data-stu-id="9d16c-119">If you select **No Size Limit**, the database will grow until it reaches the disk size limit.</span></span>

5.  <span data-ttu-id="9d16c-120">Cliquez sur **appliquer** ou **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d16c-120">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="9d16c-121">Pour désactiver les limites de taille de base de données</span><span class="sxs-lookup"><span data-stu-id="9d16c-121">To disable database size limits</span></span>**

1.  <span data-ttu-id="9d16c-122">Dans le volet **étendue** , cliquez avec le bouton droit sur le nœud système de virtualisation des applications, puis sélectionnez **Options système**.</span><span class="sxs-lookup"><span data-stu-id="9d16c-122">Right-click the Application Virtualization System node in the **Scope** pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="9d16c-123">Sélectionnez l’onglet **base de données** .</span><span class="sxs-lookup"><span data-stu-id="9d16c-123">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="9d16c-124">Activez les cases d’option **aucune limite de taille** et **conserver toutes les utilisations** .</span><span class="sxs-lookup"><span data-stu-id="9d16c-124">Select the **No Size Limit** and **Keep All Usage** radio buttons.</span></span>

4.  <span data-ttu-id="9d16c-125">Cliquez sur **appliquer** ou **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d16c-125">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="9d16c-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d16c-126">Related topics</span></span>


[<span data-ttu-id="9d16c-127">Procédure pour personnaliser un système Application Virtualization dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="9d16c-127">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="9d16c-128">Procédure pour configurer ou désactiver la création de rapports d'utilisation</span><span class="sxs-lookup"><span data-stu-id="9d16c-128">How to Set Up or Disable Usage Reporting</span></span>](how-to-set-up-or-disable-usage-reporting.md)

 

 






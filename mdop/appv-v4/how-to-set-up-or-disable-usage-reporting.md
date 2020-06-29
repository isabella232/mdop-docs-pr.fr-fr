---
title: Procédure pour configurer ou désactiver la création de rapports d'utilisation
description: Procédure pour configurer ou désactiver la création de rapports d'utilisation
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806750"
---
# <span data-ttu-id="bcc60-103">Procédure pour configurer ou désactiver la création de rapports d'utilisation</span><span class="sxs-lookup"><span data-stu-id="bcc60-103">How to Set Up or Disable Usage Reporting</span></span>


<span data-ttu-id="bcc60-104">Vous pouvez utiliser les procédures suivantes dans la console de gestion du serveur d’applications pour spécifier la durée (en mois) des informations d’utilisation du système de virtualisation des applications que vous voulez stocker dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="bcc60-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the duration (in months) of Application Virtualization System usage information you want to store in the database.</span></span>

<span data-ttu-id="bcc60-105">**Remarques**  Pour stocker les informations d’utilisation, vous devez activer la case à cocher **journalisation des informations d’utilisation** sous l’onglet **pipeline du fournisseur** . Pour afficher cet onglet, cliquez avec le bouton droit sur la stratégie du fournisseur dans le volet de **résultats stratégies du fournisseur** , puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="bcc60-105">**Note** To store usage information, you must select the **Log Usage Information** check box on the **Provider Pipeline** tab. To display this tab, right-click the provider policy in the **Provider Policies Results** pane and select **Properties**.</span></span>

 

**<span data-ttu-id="bcc60-106">Pour configurer la création de rapports d’utilisation</span><span class="sxs-lookup"><span data-stu-id="bcc60-106">To set up usage reporting</span></span>**

1.  <span data-ttu-id="bcc60-107">Dans le volet gauche, cliquez avec le bouton droit sur le nœud système de virtualisation des applications, puis sélectionnez **Options système**.</span><span class="sxs-lookup"><span data-stu-id="bcc60-107">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="bcc60-108">Sélectionnez l’onglet **base de données** .</span><span class="sxs-lookup"><span data-stu-id="bcc60-108">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="bcc60-109">Sélectionnez la case **d’option conserver l’utilisation pour (mois)** ou **conserver tout l’utilisation** .</span><span class="sxs-lookup"><span data-stu-id="bcc60-109">Select the **Keep Usage For (Months)** or **Keep All Usage** radio button.</span></span>

4.  <span data-ttu-id="bcc60-110">Si vous choisissez de spécifier la durée d’utilisation en mois, entrez un nombre compris entre 1 et 120 (la valeur par défaut est 6 mois).</span><span class="sxs-lookup"><span data-stu-id="bcc60-110">If you choose to specify usage duration in months, enter a number from 1 to 120 (default value is 6 months).</span></span> <span data-ttu-id="bcc60-111">Si vous sélectionnez **conserver toute l’utilisation**, la base de données s’étire jusqu’à ce qu’elle atteigne la taille limite spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcc60-111">If you select **Keep All Usage**, the database will grow until it reaches the specified size limit.</span></span>

5.  <span data-ttu-id="bcc60-112">Cliquez sur **appliquer** ou **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcc60-112">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="bcc60-113">Pour désactiver la création de rapports d’utilisation</span><span class="sxs-lookup"><span data-stu-id="bcc60-113">To disable usage reporting</span></span>**

1.  <span data-ttu-id="bcc60-114">Cliquez sur le nœud **stratégies du fournisseur** .</span><span class="sxs-lookup"><span data-stu-id="bcc60-114">Click the **Provider Policies** node.</span></span>

2.  <span data-ttu-id="bcc60-115">Cliquez avec le bouton droit sur **stratégie du fournisseur** , puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="bcc60-115">Right-click **Provider Policy** and select **Properties**.</span></span>

3.  <span data-ttu-id="bcc60-116">Sélectionnez l’onglet **pipeline du fournisseur** .</span><span class="sxs-lookup"><span data-stu-id="bcc60-116">Select the **Provider Pipeline** tab.</span></span>

4.  <span data-ttu-id="bcc60-117">Décochez la case **journaliser les informations d’utilisation** .</span><span class="sxs-lookup"><span data-stu-id="bcc60-117">Clear the **Log Usage Information** check box.</span></span>

5.  <span data-ttu-id="bcc60-118">Cliquez sur **appliquer** ou **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcc60-118">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="bcc60-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bcc60-119">Related topics</span></span>


[<span data-ttu-id="bcc60-120">Procédure pour personnaliser un système Application Virtualization dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="bcc60-120">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="bcc60-121">Procédure pour configurer ou désactiver la taille de base de données</span><span class="sxs-lookup"><span data-stu-id="bcc60-121">How to Set Up or Disable Database Size</span></span>](how-to-set-up-or-disable-database-size.md)

 

 






---
title: Masquage de l'élément de chiffrement de lecteur BitLocker par défaut dans le Panneau de configuration
description: Masquage de l'élément de chiffrement de lecteur BitLocker par défaut dans le Panneau de configuration
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809750"
---
# <span data-ttu-id="5a41c-103">Masquage de l'élément de chiffrement de lecteur BitLocker par défaut dans le Panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="5a41c-103">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>


<span data-ttu-id="5a41c-104">Cette rubrique décrit comment masquer l’élément de panneau de configuration du **chiffrement de lecteurs BitLocker** , qui apparaît par défaut dans le panneau de configuration dans le cadre du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="5a41c-104">This topic describes how to hide the **BitLocker Drive Encryption** Control Panel item, which appears by default on Control Panel as part of the Windows operating system.</span></span>

<span data-ttu-id="5a41c-105">**Remarques**  Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) crée un élément de panneau de configuration personnalisé supplémentaire, appelé **options de chiffrement BitLocker**, qui permet aux utilisateurs finaux de gérer leur code confidentiel et leur mot de passe, d’activer BitLocker pour un lecteur et de vérifier le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="5a41c-105">**Note** Microsoft BitLocker Administration and Monitoring (MBAM) creates an additional, custom Control Panel item, called **BitLocker Encryption Options**, which enables end users to manage their PIN and password, turn on BitLocker for a drive, and check encryption.</span></span>

 

<span data-ttu-id="5a41c-106">Pour en savoir plus [, voir présentation des options de chiffrement de BitLocker et des éléments de chiffrement de lecteur BitLocker dans le panneau de configuration](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) :</span><span class="sxs-lookup"><span data-stu-id="5a41c-106">See [Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) to read about:</span></span>

-   <span data-ttu-id="5a41c-107">Différences entre le MBAM et les éléments du panneau de configuration par défaut</span><span class="sxs-lookup"><span data-stu-id="5a41c-107">Differences between the MBAM and the default Control Panel items</span></span>

-   <span data-ttu-id="5a41c-108">Menu contextuel **gérer BitLocker** qui s’affiche lorsque vous cliquez avec le bouton droit sur un lecteur dans l’Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="5a41c-108">**Manage BitLocker** shortcut menu that appears when you right-click a drive in Windows Explorer</span></span>

<span data-ttu-id="5a41c-109">**Important**  Ne modifiez pas les paramètres de stratégie de groupe du nœud **BitLocker Drive Encryption** .</span><span class="sxs-lookup"><span data-stu-id="5a41c-109">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node.</span></span> <span data-ttu-id="5a41c-110">Si tel est le cas, MBAM ne fonctionnera pas correctement.</span><span class="sxs-lookup"><span data-stu-id="5a41c-110">If you do, MBAM will not work correctly.</span></span> <span data-ttu-id="5a41c-111">Lorsque vous configurez les paramètres de stratégie de groupe dans le nœud **MDOP MBAM (gestion du BitLocker)** , MBAM configure automatiquement les paramètres de **chiffrement de lecteur BitLocker** pour vous.</span><span class="sxs-lookup"><span data-stu-id="5a41c-111">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="5a41c-112">Pour masquer l’élément de chiffrement de lecteur BitLocker par défaut dans le panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="5a41c-112">To hide the default BitLocker Drive Encryption item in Control Panel</span></span>**

1.  <span data-ttu-id="5a41c-113">Dans la console de gestion des stratégies de groupe (GPMC) ou dans la gestion avancée des stratégies de groupe, accédez au panneau de configuration modèles de **Configuration des utilisateurs** &gt; **Policies** &gt; **Administrative Templates** &gt; **Control Panel**.</span><span class="sxs-lookup"><span data-stu-id="5a41c-113">In the Group Policy Management Console (GPMC) or in Advanced Group Policy Management, browse to **User configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Control Panel**.</span></span>

2.  <span data-ttu-id="5a41c-114">Dans le volet **Détails** , double-cliquez sur **Masquer les éléments du panneau de configuration spécifiés**, puis cliquez sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="5a41c-114">In the **Details** pane, double-click **Hide specified Control Panel items**, and then click **Enabled**.</span></span>

3.  <span data-ttu-id="5a41c-115">Cliquez sur **Afficher**, puis sur **Ajouter**et tapez **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="5a41c-115">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span>



## <span data-ttu-id="5a41c-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a41c-116">Related topics</span></span>


[<span data-ttu-id="5a41c-117">Présentation des éléments Options de chiffrement BitLocker et Chiffrement de lecteur BitLocker du Panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="5a41c-117">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[<span data-ttu-id="5a41c-118">Déploiement d'objets de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5a41c-118">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)

 

## <span data-ttu-id="5a41c-119">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="5a41c-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5a41c-120">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="5a41c-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5a41c-121">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5a41c-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 






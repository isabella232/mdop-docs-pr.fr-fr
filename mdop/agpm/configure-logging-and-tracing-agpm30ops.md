---
title: Configurer la journalisation et suivi
description: Configurer la journalisation et suivi
author: dansimp
ms.assetid: 4f89552f-e949-48b0-9325-23746034eaa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6edcb643dd34a20a845cb3d44a0fe8b353a6291
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807725"
---
# <span data-ttu-id="f7c61-103">Configurer la journalisation et suivi</span><span class="sxs-lookup"><span data-stu-id="f7c61-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="f7c61-104">Vous pouvez configurer la journalisation et le suivi facultatifs à l’aide de modèles d’administration.</span><span class="sxs-lookup"><span data-stu-id="f7c61-104">You can centrally configure optional logging and tracing using Administrative templates.</span></span> <span data-ttu-id="f7c61-105">Cela pourrait s’avérer utile lors du diagnostic de problèmes liés à la gestion de stratégie de groupe avancée (AGPM).</span><span class="sxs-lookup"><span data-stu-id="f7c61-105">This may be helpful when diagnosing any problems related to Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="f7c61-106">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe (GPO) utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans AGPM est requis pour effectuer ces procédures.</span><span class="sxs-lookup"><span data-stu-id="f7c61-106">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account with the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="f7c61-107">Par ailleurs, un compte d’utilisateur ayant accès au serveur AGPM est requis pour lancer la journalisation sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="f7c61-107">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="f7c61-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f7c61-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f7c61-109">Pour configurer la journalisation et le suivi pour AGPM</span><span class="sxs-lookup"><span data-stu-id="f7c61-109">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="f7c61-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe pour lesquels vous souhaitez activer la journalisation et le suivi.</span><span class="sxs-lookup"><span data-stu-id="f7c61-110">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="f7c61-111">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="f7c61-111">(For more information, see [Editing a GPO](editing-a-gpo-agpm30ops.md).)</span></span>

2.  <span data-ttu-id="f7c61-112">Dans la fenêtre **éditeur de gestion des stratégies de groupe** , cliquez sur Configuration de l' **ordinateur**, **stratégies**, **modèles d’administration**, **composants Windows**et **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="f7c61-112">In the **Group Policy Management Editor** window, click **Computer Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="f7c61-113">Dans le volet Détails, double-cliquez sur **AGPM: configurer la journalisation**.</span><span class="sxs-lookup"><span data-stu-id="f7c61-113">In the details pane, double-click **AGPM: Configure logging**.</span></span>

4.  <span data-ttu-id="f7c61-114">Dans la fenêtre **Propriétés** , cliquez sur **activé**, puis configurez le niveau de détail à enregistrer dans les journaux.</span><span class="sxs-lookup"><span data-stu-id="f7c61-114">In the **Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

5.  <span data-ttu-id="f7c61-115">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7c61-115">Click **OK**.</span></span>

6.  <span data-ttu-id="f7c61-116">Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="f7c61-116">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="f7c61-117">Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm30ops.md). Après la mise à jour de la stratégie de groupe, vous devez redémarrer le service AGPM pour démarrer, modifier ou arrêter la journalisation sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="f7c61-117">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).) After Group Policy is updated, you must restart the AGPM Service to start, modify, or stop logging on the AGPM Server.</span></span> <span data-ttu-id="f7c61-118">Les administrateurs de stratégie de groupe doivent fermer et redémarrer le GPMC pour démarrer, modifier ou arrêter la journalisation sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f7c61-118">Group Policy administrators must close and restart the GPMC to start, modify, or stop logging on their computers.</span></span>

    <span data-ttu-id="f7c61-119">**Emplacement des fichiers de suivi**:</span><span class="sxs-lookup"><span data-stu-id="f7c61-119">**Trace file locations**:</span></span>

    -   <span data-ttu-id="f7c61-120">Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="f7c61-120">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="f7c61-121">Serveur:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="f7c61-121">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="f7c61-122">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="f7c61-122">Additional considerations</span></span>

-   <span data-ttu-id="f7c61-123">Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour configurer la journalisation et le suivi d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="f7c61-123">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="f7c61-124">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm30ops.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm30ops.md)</span><span class="sxs-lookup"><span data-stu-id="f7c61-124">See [Editing a GPO](editing-a-gpo-agpm30ops.md) and [Deploy a GPO](deploy-a-gpo-agpm30ops.md) for additional detail.</span></span>

### <span data-ttu-id="f7c61-125">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f7c61-125">Additional references</span></span>

-   [<span data-ttu-id="f7c61-126">Configuration de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="f7c61-126">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 






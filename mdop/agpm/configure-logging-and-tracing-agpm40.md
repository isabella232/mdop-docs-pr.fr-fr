---
title: Configurer la journalisation et suivi
description: Configurer la journalisation et suivi
author: dansimp
ms.assetid: 2418cb6a-7189-4080-8fe2-9c8d47dec62c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfc56d418ae83cbc5db24246bfac057305629df7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807718"
---
# <span data-ttu-id="d4390-103">Configurer la journalisation et suivi</span><span class="sxs-lookup"><span data-stu-id="d4390-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="d4390-104">Vous pouvez configurer la journalisation et le suivi facultatifs à l’aide de modèles d’administration.</span><span class="sxs-lookup"><span data-stu-id="d4390-104">You can centrally configure optional logging and tracing using Administrative templates.</span></span> <span data-ttu-id="d4390-105">Cela pourrait s’avérer utile lors du diagnostic de problèmes liés à la gestion de stratégie de groupe avancée (AGPM).</span><span class="sxs-lookup"><span data-stu-id="d4390-105">This may be helpful when diagnosing any problems related to Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="d4390-106">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe (GPO) utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans AGPM est requis pour effectuer ces procédures.</span><span class="sxs-lookup"><span data-stu-id="d4390-106">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account with the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="d4390-107">Par ailleurs, un compte d’utilisateur ayant accès au serveur AGPM est requis pour lancer la journalisation sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="d4390-107">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="d4390-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d4390-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d4390-109">Pour configurer la journalisation et le suivi pour AGPM</span><span class="sxs-lookup"><span data-stu-id="d4390-109">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="d4390-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe pour lesquels vous souhaitez activer la journalisation et le suivi.</span><span class="sxs-lookup"><span data-stu-id="d4390-110">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="d4390-111">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="d4390-111">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="d4390-112">Dans la fenêtre **éditeur de gestion des stratégies de groupe** , cliquez sur Configuration de l' **ordinateur**, **stratégies**, **modèles d’administration**, **composants Windows**et **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="d4390-112">In the **Group Policy Management Editor** window, click **Computer Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="d4390-113">Dans le volet Détails, double-cliquez sur **AGPM: configurer la journalisation**.</span><span class="sxs-lookup"><span data-stu-id="d4390-113">In the details pane, double-click **AGPM: Configure logging**.</span></span>

4.  <span data-ttu-id="d4390-114">Dans la fenêtre **Propriétés** , cliquez sur **activé**, puis configurez le niveau de détail à enregistrer dans les journaux.</span><span class="sxs-lookup"><span data-stu-id="d4390-114">In the **Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

5.  <span data-ttu-id="d4390-115">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4390-115">Click **OK**.</span></span>

6.  <span data-ttu-id="d4390-116">Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="d4390-116">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="d4390-117">Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md). Après la mise à jour de la stratégie de groupe, vous devez redémarrer le service AGPM pour démarrer, modifier ou arrêter la journalisation sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="d4390-117">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) After Group Policy is updated, you must restart the AGPM Service to start, modify, or stop logging on the AGPM Server.</span></span> <span data-ttu-id="d4390-118">Les administrateurs de stratégie de groupe doivent fermer et redémarrer le GPMC pour démarrer, modifier ou arrêter la journalisation sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d4390-118">Group Policy administrators must close and restart the GPMC to start, modify, or stop logging on their computers.</span></span>

    <span data-ttu-id="d4390-119">**Emplacement des fichiers de suivi**:</span><span class="sxs-lookup"><span data-stu-id="d4390-119">**Trace file locations**:</span></span>

    -   <span data-ttu-id="d4390-120">Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="d4390-120">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="d4390-121">Serveur:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="d4390-121">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="d4390-122">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="d4390-122">Additional considerations</span></span>

-   <span data-ttu-id="d4390-123">Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour configurer la journalisation et le suivi d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="d4390-123">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="d4390-124">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md)</span><span class="sxs-lookup"><span data-stu-id="d4390-124">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

### <span data-ttu-id="d4390-125">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="d4390-125">Additional references</span></span>

-   [<span data-ttu-id="d4390-126">Configuration de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="d4390-126">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 






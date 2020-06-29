---
title: Configurer la journalisation et suivi
description: Configurer la journalisation et suivi
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807721"
---
# <span data-ttu-id="0709f-103">Configurer la journalisation et suivi</span><span class="sxs-lookup"><span data-stu-id="0709f-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="0709f-104">Vous pouvez configurer la journalisation et le suivi facultatifs pour une gestion avancée des stratégies de groupe (AGPM) à l’aide de modèles d’administration.</span><span class="sxs-lookup"><span data-stu-id="0709f-104">You can centrally configure optional logging and tracing for Advanced Group Policy Management (AGPM) using Administrative templates.</span></span>

<span data-ttu-id="0709f-105">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer ces procédures.</span><span class="sxs-lookup"><span data-stu-id="0709f-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures.</span></span> <span data-ttu-id="0709f-106">Par ailleurs, un compte d’utilisateur ayant accès au serveur AGPM est requis pour lancer la journalisation sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="0709f-106">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="0709f-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0709f-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="0709f-108">Pour configurer la journalisation et le suivi pour AGPM</span><span class="sxs-lookup"><span data-stu-id="0709f-108">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="0709f-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe pour lesquels vous souhaitez activer la journalisation et le suivi.</span><span class="sxs-lookup"><span data-stu-id="0709f-109">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="0709f-110">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="0709f-110">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="0709f-111">Dans l' **éditeur d’objets de stratégie de groupe**, cliquez sur Configuration de l' **ordinateur**, **modèles d’administration**et **composants Windows**.</span><span class="sxs-lookup"><span data-stu-id="0709f-111">In the **Group Policy Object Editor**, click **Computer Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="0709f-112">Si **AGPM** ne figure pas dans la liste **composants Windows**:</span><span class="sxs-lookup"><span data-stu-id="0709f-112">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="0709f-113">Cliquez avec le bouton droit sur **modèles d’administration** et sélectionnez **Ajouter/supprimer des modèles**.</span><span class="sxs-lookup"><span data-stu-id="0709f-113">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="0709f-114">Cliquez **sur Ajouter**, sélectionnez **AGPM. admx** ou **AGPM. adm**, cliquez sur **ouvrir**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0709f-114">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="0709f-115">Sous **composants Windows**, double-cliquez sur **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="0709f-115">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="0709f-116">Dans le volet Détails, double-cliquez sur **journalisation d’AGPM**.</span><span class="sxs-lookup"><span data-stu-id="0709f-116">In the details pane, double-click **AGPM Logging**.</span></span>

6.  <span data-ttu-id="0709f-117">Dans la fenêtre **Propriétés de journalisation AGPM** , cliquez sur **activé**, puis configurez le niveau de détail à enregistrer dans les journaux.</span><span class="sxs-lookup"><span data-stu-id="0709f-117">In the **AGPM Logging Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

7.  <span data-ttu-id="0709f-118">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0709f-118">Click **OK**.</span></span>

8.  <span data-ttu-id="0709f-119">Fermez l' **éditeur d’objets de stratégie de groupe**.</span><span class="sxs-lookup"><span data-stu-id="0709f-119">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="0709f-120">Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md). Après la mise à jour de la stratégie de groupe, vous devez redémarrer le service AGPM pour commencer à vous connecter au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="0709f-120">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) After Group Policy is updated, you must restart the AGPM Service to begin logging on the AGPM Server.</span></span> <span data-ttu-id="0709f-121">Les administrateurs de stratégie de groupe doivent fermer et redémarrer la console GPMC pour commencer à se connecter sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0709f-121">Group Policy administrators must close and restart the GPMC to begin logging on their computers.</span></span>

    <span data-ttu-id="0709f-122">**Emplacement des fichiers de suivi**:</span><span class="sxs-lookup"><span data-stu-id="0709f-122">**Trace file locations**:</span></span>

    -   <span data-ttu-id="0709f-123">Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="0709f-123">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="0709f-124">Serveur:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="0709f-124">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="0709f-125">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="0709f-125">Additional considerations</span></span>

-   <span data-ttu-id="0709f-126">Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour configurer la journalisation et le suivi d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="0709f-126">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="0709f-127">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md)</span><span class="sxs-lookup"><span data-stu-id="0709f-127">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

### <span data-ttu-id="0709f-128">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0709f-128">Additional references</span></span>

-   [<span data-ttu-id="0709f-129">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="0709f-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 






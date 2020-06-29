---
title: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP2
description: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP2
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808286"
---
# <span data-ttu-id="58926-103">Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP2</span><span class="sxs-lookup"><span data-stu-id="58926-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>


<span data-ttu-id="58926-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="58926-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="58926-105">Lisez attentivement ces notes de publication avant d’installer Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="58926-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="58926-106">Ces notes de publication contiennent des informations nécessaires à l’installation d’AGPM 4.0 SP2 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="58926-106">These release notes contain information that is required to successfully install AGPM4.0 SP2 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="58926-107">S’il existe une différence entre ces notes de publication et toute autre documentation AGPM, envisagez la dernière modification faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="58926-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="58926-108">Ces notes de publication remplacent le contenu fourni avec ce produit.</span><span class="sxs-lookup"><span data-stu-id="58926-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="58926-109">Problèmes connus d’AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="58926-109">AGPM4.0 SP2 known issues</span></span>


<span data-ttu-id="58926-110">Cette section décrit les problèmes connus d’AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="58926-110">This section describes the known issues for AGPM 4.0 SP2.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="58926-111">L’outil «désinstaller» du panneau de configuration peut ne pas fonctionner lorsque vous tentez de modifier les paramètres du serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="58926-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="58926-112">L’outil du panneau de configuration que vous utilisez pour désinstaller ou modifier un programme risque de ne pas fonctionner lorsque vous tentez de modifier les paramètres du serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="58926-112">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="58926-113">**Solution de contournement:** Avant d’essayer de modifier les paramètres du serveur AGPM à l’aide du panneau de configuration, effectuez une copie du dossier d’archive AGPM.</span><span class="sxs-lookup"><span data-stu-id="58926-113">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="58926-114">Vous pouvez ensuite utiliser Setup.exe pour réinstaller le serveur AGPM et sélectionner les paramètres de configuration de votre choix.</span><span class="sxs-lookup"><span data-stu-id="58926-114">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="58926-115">Les rapports n’affichent pas les liens ajoutés à un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="58926-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="58926-116">Les paramètres d’AGPM et les rapports de différences n’affichent pas les liens ajoutés à un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="58926-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="58926-117">**Solution de contournement:** Pour afficher les liens dans les rapports, sélectionnez l’objet GPO dans la console de gestion des stratégies de groupe (GPMC), puis cliquez sur l’onglet **paramètres** dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="58926-117">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="58926-118">Les rapports n’affichent pas toutes les options de propriétés options de choix</span><span class="sxs-lookup"><span data-stu-id="58926-118">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="58926-119">Les paramètres d’AGPM et les rapports de différences n’affichent pas tous les paramètres qui ont été sélectionnés dans la fenêtre de **Propriétés options de choix** de l’éditeur d’objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="58926-119">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="58926-120">**Solution de contournement:** Utilisez la console GPMC pour afficher les paramètres de **Propriétés options de choix** sélectionnés dans les rapports.</span><span class="sxs-lookup"><span data-stu-id="58926-120">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="58926-121">Il est possible que les rapports n’affichent pas les onglets Afficher et masquer dans certains navigateurs</span><span class="sxs-lookup"><span data-stu-id="58926-121">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="58926-122">Les onglets **Afficher** et **Masquer** , situés dans la partie droite des rapports d’AGPM et des rapports de différences, risquent de ne pas apparaître lorsque vous affichez les rapports dans Google Chrome ou Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="58926-122">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="58926-123">**Solution de contournement:** Affichez les rapports à l’aide du navigateur Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="58926-123">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="58926-124">Les paramètres d’AGPM et les rapports de différences risquent d’afficher du contenu différent des rapports GPMC</span><span class="sxs-lookup"><span data-stu-id="58926-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="58926-125">Les rapports et les paramètres d’AGPM risquent de ne pas afficher le même contenu que les rapports dans la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="58926-125">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="58926-126">**Solution de contournement:** Utilisez la console GPMC pour afficher les rapports AGPM.</span><span class="sxs-lookup"><span data-stu-id="58926-126">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="58926-127">Le service AGPM ne démarre pas si le contrôleur de domaine est hors connexion</span><span class="sxs-lookup"><span data-stu-id="58926-127">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="58926-128">Lorsque le service AGPM est installé sur un contrôleur de domaine sur les systèmes d’exploitation Windows® 8 ou version ultérieure, le service ne démarre pas si le contrôleur de domaine est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="58926-128">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="58926-129">**Solution de contournement:** Démarrez manuellement le service AGPM une fois le contrôleur de domaine connecté.</span><span class="sxs-lookup"><span data-stu-id="58926-129">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="58926-130">La mise à niveau d’AGPM Server vers AGPM 4.0 SP2 est bloquée lors de la mise à niveau à partir d’AGPM 4.0 version plus HotFix1</span><span class="sxs-lookup"><span data-stu-id="58926-130">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="58926-131">Si vous essayez de mettre à niveau le serveur AGPM vers AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="58926-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="58926-132">SP2 après l’installation d’AGPM 4,0 Server, puis l’installation de la mise à jour d’AGPM nommée AGPM 4,0 signale les différences incorrectes dans le rapport HTML (Voir l’article de la base de connaissances [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), la mise à niveau échoue et ne peut pas être effectuée.</span><span class="sxs-lookup"><span data-stu-id="58926-132">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="58926-133">**Solution de contournement:** Désinstallez le serveur 4,0 AGPM, puis installez AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="58926-133">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="58926-134">Rapports ne pas afficher les liens d’unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="58926-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="58926-135">Si vous liez un objet de stratégie de groupe non contrôlé à une unité d’organisation, puis le contrôle à l’aide d’AGPM, les paramètres et les rapports d’AGPM n’affichent pas les liens d’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="58926-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="58926-136">**Solution de contournement:** Dans l’onglet **contrôlé** du nœud **modifier les paramètres** , cliquez avec le bouton droit sur l’objet de stratégie de groupe, cliquez sur **paramètres**, puis sur liens d’objets de **stratégie de groupe** pour afficher les liens d’organisation.</span><span class="sxs-lookup"><span data-stu-id="58926-136">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="58926-137">Vous pouvez également utiliser la console GPMC pour afficher les liens d’un objet de stratégie de groupe à partir de l’onglet **étendue** .</span><span class="sxs-lookup"><span data-stu-id="58926-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="58926-138">AGPM affiche une erreur si vous cliquez sur le bouton précédent dans la boîte de dialogue Modifier, réparer ou supprimer le client AGPM</span><span class="sxs-lookup"><span data-stu-id="58926-138">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="58926-139">Si vous naviguez jusqu’à **programmes et fonctionnalités** dans le panneau de configuration et sélectionnez gestion de la **stratégie de groupe Microsoft avancé-client**, AGPM affiche une erreur si vous cliquez sur **modifier** , puis cliquez sur le bouton **précédent** dans la boîte de dialogue **modifier, réparer ou supprimer le client AGPM** .</span><span class="sxs-lookup"><span data-stu-id="58926-139">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="58926-140">**Solution de contournement:** Cliquez sur **Annuler** pour supprimer l’erreur, puis redémarrez le processus.</span><span class="sxs-lookup"><span data-stu-id="58926-140">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="58926-141">Ne cliquez pas sur le bouton **précédent** lorsque vous cliquez sur **modifier** .</span><span class="sxs-lookup"><span data-stu-id="58926-141">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="58926-142">Le commentaire ne s’affiche pas dans la fenêtre historique lorsque l’approbateur déploie un objet de stratégie de groupe et entre un commentaire</span><span class="sxs-lookup"><span data-stu-id="58926-142">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="58926-143">Si un utilisateur qui dispose du rôle d’éditeur envoie une demande de déploiement d’un objet de stratégie de groupe et l’utilisateur qui a le rôle Approbateur déploie ensuite l’objet de stratégie de groupe et entre un commentaire, le commentaire ne peut pas s’afficher dans la fenêtre de l' **historique** .</span><span class="sxs-lookup"><span data-stu-id="58926-143">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="58926-144">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="58926-144">**Workaround:** None.</span></span>

## <span data-ttu-id="58926-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58926-145">Related topics</span></span>


[<span data-ttu-id="58926-146">Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="58926-146">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="58926-147">Nouveautés d'AGPM4.0SP2</span><span class="sxs-lookup"><span data-stu-id="58926-147">What's New in AGPM 4.0 SP2</span></span>](whats-new-in-agpm-40-sp2.md)

 

 






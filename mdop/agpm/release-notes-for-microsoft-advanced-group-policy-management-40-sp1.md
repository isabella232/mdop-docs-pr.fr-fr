---
title: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP1
description: Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP1
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807545"
---
# <span data-ttu-id="c9ead-103">Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP1</span><span class="sxs-lookup"><span data-stu-id="c9ead-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>


<span data-ttu-id="c9ead-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="c9ead-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="c9ead-105">Lisez attentivement ces notes de publication avant d’installer la gestion de la stratégie de groupe Microsoft avancée (AGPM) 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c9ead-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="c9ead-106">Ces notes de publication contiennent des informations nécessaires pour l’installation d’AGPM 4,0 SP1 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="c9ead-106">These release notes contain information that is required to successfully install AGPM 4.0 SP1 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="c9ead-107">S’il existe une différence entre ces notes de publication et une autre documentation AGPM, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="c9ead-107">If there is a difference between these release notes and other AGPM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="c9ead-108">Ces notes de publication remplacent le contenu fourni avec ce produit.</span><span class="sxs-lookup"><span data-stu-id="c9ead-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="c9ead-109">Problèmes connus d’AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c9ead-109">AGPM 4.0 SP1 known issues</span></span>


<span data-ttu-id="c9ead-110">Cette section contient des notes de publication pour AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c9ead-110">This section contains release notes for AGPM 4.0 SP1.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="c9ead-111">L’outil «désinstaller» du panneau de configuration peut ne pas fonctionner lorsque vous tentez de modifier les paramètres du serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="c9ead-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="c9ead-112">L’outil du panneau de configuration qui vous permet de désinstaller ou de modifier un programme risque de ne pas fonctionner lorsque vous tentez de modifier les paramètres du serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="c9ead-112">The tool in Control Panel that lets you uninstall or change a program may not work when you try to change AGPM server settings.</span></span>

<span data-ttu-id="c9ead-113">Solution de contournement: avant d’essayer de modifier les paramètres de serveur AGPM à l’aide du panneau de configuration, effectuez une copie du dossier d’archive AGPM.</span><span class="sxs-lookup"><span data-stu-id="c9ead-113">WORKAROUND: Before you try to change AGPM server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="c9ead-114">Vous pouvez ensuite utiliser Setup.exe pour réinstaller le serveur AGPM et sélectionner les paramètres de configuration de votre choix.</span><span class="sxs-lookup"><span data-stu-id="c9ead-114">You can then use Setup.exe to reinstall the AGPM server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="c9ead-115">Les rapports n’affichent pas les liens ajoutés à un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c9ead-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="c9ead-116">Les paramètres d’AGPM et les rapports de différences n’affichent pas les liens ajoutés à un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c9ead-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="c9ead-117">SOLUTION: pour afficher les liens dans les rapports, sélectionnez l’objet GPO dans la console de gestion des stratégies de groupe (GPMC), puis cliquez sur l’onglet **paramètres** dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="c9ead-117">WORKAROUND: To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and click the **Settings** tab in the right pane.</span></span>

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a><span data-ttu-id="c9ead-118">Les rapports n’affichent pas toutes les valeurs «propriétés des options choix»</span><span class="sxs-lookup"><span data-stu-id="c9ead-118">Reports do not display all “Choice Options Properties” settings</span></span>

<span data-ttu-id="c9ead-119">Les paramètres d’AGPM et les rapports de différences n’affichent pas tous les paramètres qui ont été sélectionnés dans la fenêtre de propriétés options de choix de l’éditeur d’objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c9ead-119">The AGPM settings and difference reports do not display all of the settings that were selected on the Choice Options Properties window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="c9ead-120">Solution de contournement: utilisez la console GPMC pour afficher les paramètres de propriétés options de choix sélectionnés dans les rapports.</span><span class="sxs-lookup"><span data-stu-id="c9ead-120">WORKAROUND: Use the GPMC to view the selected Choice Options Properties settings in the reports.</span></span>

### <span data-ttu-id="c9ead-121">Les rapports n’affichent pas les onglets Afficher et masquer dans certains navigateurs</span><span class="sxs-lookup"><span data-stu-id="c9ead-121">Reports do not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="c9ead-122">Les onglets Afficher et masquer qui s’affichent à droite des paramètres d’AGPM et des rapports de différences ne s’affichent pas lorsque vous affichez les rapports dans Google Chrome ou Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="c9ead-122">The Show and Hide tabs, shown on the right side of the AGPM settings and difference reports, are not displayed when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="c9ead-123">Solution de contournement: Affichez les rapports à l’aide d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c9ead-123">WORKAROUND: View the reports by using Internet Explorer.</span></span>

### <span data-ttu-id="c9ead-124">Les paramètres d’AGPM et les rapports de différences risquent d’afficher du contenu différent des rapports GPMC</span><span class="sxs-lookup"><span data-stu-id="c9ead-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="c9ead-125">Les paramètres et les différences d’AGPM risquent de ne pas afficher le même contenu que les rapports dans la console de gestion des stratégies de groupe (GPMC).</span><span class="sxs-lookup"><span data-stu-id="c9ead-125">The AGPM settings and difference reports may not show the same content as reports in the Group Policy Management Console (GPMC).</span></span>

<span data-ttu-id="c9ead-126">Solution de contournement: utilisez la console GPMC pour afficher les rapports AGPM.</span><span class="sxs-lookup"><span data-stu-id="c9ead-126">WORKAROUND: Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="c9ead-127">Le service AGPM ne démarre pas si le contrôleur de domaine n’est pas connecté</span><span class="sxs-lookup"><span data-stu-id="c9ead-127">AGPM Service does not start if the domain controller is not online</span></span>

<span data-ttu-id="c9ead-128">Lorsque le service AGPM est installé sur un contrôleur de domaine sous Windows 8, le service n’est pas démarré si le contrôleur de domaine n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="c9ead-128">When the AGPM Service is installed on a domain controller on Windows 8, the Service does not start if the domain controller is not online.</span></span>

<span data-ttu-id="c9ead-129">Solution de contournement: démarrez manuellement le service AGPM après que le contrôleur de domaine est en ligne.</span><span class="sxs-lookup"><span data-stu-id="c9ead-129">WORKAROUND: Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="c9ead-130">La mise à niveau d’AGPM Server vers AGPM 4,0 SP1 est bloquée lors de la mise à niveau à partir de la version d’AGPM 4,0 plus le correctif</span><span class="sxs-lookup"><span data-stu-id="c9ead-130">Upgrade of AGPM Server to AGPM 4.0 SP1 is blocked when you upgrade from the AGPM 4.0 release plus the hotfix</span></span>

<span data-ttu-id="c9ead-131">Si vous essayez de mettre à niveau le serveur AGPM vers AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="c9ead-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="c9ead-132">SP1 après l’installation d’AGPM 4,0, puis l’installation du correctif AGPM (Voir l’article de la base de connaissances [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), la mise à niveau échoue et ne peut pas être effectuée.</span><span class="sxs-lookup"><span data-stu-id="c9ead-132">SP1 after installing AGPM 4.0 and then installing the AGPM hotfix (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="c9ead-133">Solution de contournement: désinstallez le serveur AGPM 4,0, puis installez AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c9ead-133">WORKAROUND: Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP1.</span></span>

### <span data-ttu-id="c9ead-134">Rapports ne pas afficher les liens d’unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="c9ead-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="c9ead-135">Si vous liez un objet de stratégie de groupe non contrôlé à une unité d’organisation, puis le contrôle à l’aide d’AGPM, les paramètres et les rapports d’AGPM n’affichent pas les liens d’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="c9ead-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="c9ead-136">Solution de contournement: à partir de l’onglet **contrôlé** du nœud **modifier les paramètres** , cliquez avec le bouton droit sur l’objet de stratégie de groupe, cliquez sur **paramètres** , puis cliquez sur liens d’objets de **stratégie de groupe** pour afficher les liens d’organisation.</span><span class="sxs-lookup"><span data-stu-id="c9ead-136">WORKAROUND: From the **Controlled** tab of the **Change Settings** node, right-click the GPO and click **Settings** and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="c9ead-137">Vous pouvez également utiliser la console GPMC pour afficher les liens d’un objet de stratégie de groupe à partir de l’onglet **étendue** .</span><span class="sxs-lookup"><span data-stu-id="c9ead-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

## <span data-ttu-id="c9ead-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9ead-138">Related topics</span></span>


[<span data-ttu-id="c9ead-139">Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="c9ead-139">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="c9ead-140">Nouveautés d'AGPM4.0SP1</span><span class="sxs-lookup"><span data-stu-id="c9ead-140">What's New in AGPM 4.0 SP1</span></span>](whats-new-in-agpm-40-sp1.md)

 

 






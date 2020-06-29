---
title: Configuration de stratégies d'espace de travail MED-V
description: Configuration de stratégies d'espace de travail MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810806"
---
# <span data-ttu-id="5aa1d-103">Configuration de stratégies d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5aa1d-103">Configuring MED-V Workspace Policies</span></span>


<span data-ttu-id="5aa1d-104">Une stratégie d’espace de travail MED-V est un ensemble de paramètres configurables qui déterminent le mode d’exécution des applications et de l’environnement virtualisé sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-104">A MED-V workspace policy is a group of configurable settings that define how the virtualized environment and applications perform on the host machine.</span></span> <span data-ttu-id="5aa1d-105">Les rubriques de cette section décrivent tous les paramètres configurables de la stratégie d’espace de travail MED-V ainsi que leur influence sur l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-105">The topics in this section describe all the configurable settings in the MED-V workspace policy as well as how these settings influence the MED-V workspace.</span></span>

<span data-ttu-id="5aa1d-106">Les types d’espace de travail MED-V suivants sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="5aa1d-106">The following MED-V workspace types are available:</span></span>

-   <span data-ttu-id="5aa1d-107">**Permanent**: dans un espace de travail MED-v persistant, toutes les modifications et ajouts apportées par l’utilisateur à l’espace de travail MED-v sont enregistrés dans l’espace de travail MED-v entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-107">**Persistent**—In a persistent MED-V workspace, all changes and additions the user makes to the MED-V workspace are saved in the MED-V workspace between sessions.</span></span> <span data-ttu-id="5aa1d-108">Par ailleurs, un espace de travail MED-V permanent est généralement utilisé dans un environnement de domaine.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-108">Additionally, a persistent MED-V workspace is generally used in a domain environment.</span></span>

-   <span data-ttu-id="5aa1d-109">**Revertible**: dans un espace de travail Revertible med-v, à l’achèvement de chaque session (autrement dit, lorsque l’espace de travail MED-v est arrêté), l’espace de travail MED-v retrouve son état d’origine lors du déploiement.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-109">**Revertible**—In a revertible MED-V workspace, at the completion of each session (that is, when the MED-V workspace is stopped), the MED-V workspace reverts to its original state during deployment.</span></span> <span data-ttu-id="5aa1d-110">Aucune modification ou aucun complément n’est enregistré dans l’espace de travail MED-V entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-110">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span> <span data-ttu-id="5aa1d-111">Un espace de travail revertible MED-V ne peut pas être utilisé dans un environnement de domaine.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-111">A revertible MED-V workspace cannot be used in a domain environment.</span></span>

<span data-ttu-id="5aa1d-112">Il est important de décider du type d’espace de travail MED-V que vous créez avant de déployer l’espace de travail MED-V, car il n’est pas recommandé de reconfigurer le type d’espace de travail MED-V après le déploiement d’une stratégie sur les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-112">It is important to decide on the type of MED-V workspace you are creating before deploying the MED-V workspace, because it is not recommended to reconfigure the type of MED-V workspace after a policy has been deployed to users.</span></span>

<span data-ttu-id="5aa1d-113">**Remarques**  Lorsque vous configurez une stratégie, un symbole d’avertissement s’affiche en regard de champs obligatoires qui ne sont pas renseignés.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-113">**Note** When configuring a policy, a warning symbol appears next to mandatory fields that are not filled in.</span></span> <span data-ttu-id="5aa1d-114">Si un champ obligatoire n’est pas renseigné, le symbole s’affiche également dans l’onglet.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-114">If a mandatory field is not filled in, the symbol appears on the tab as well.</span></span>

 

## <span data-ttu-id="5aa1d-115">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5aa1d-115">In This Section</span></span>


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="5aa1d-116">Comment appliquer des paramètres généraux à un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5aa1d-116">How to Apply General Settings to a MED-V Workspace</span></span>](how-to-apply-general-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="5aa1d-117">Décrit les paramètres généraux d’un espace de travail MED-V et comment les appliquer à une stratégie.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-117">Describes the general settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="5aa1d-118">Comment appliquer des paramètres de machine virtuelle à un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5aa1d-118">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="5aa1d-119">Décrit les paramètres de la machine virtuelle pour un espace de travail MED-V et la façon de les appliquer à une stratégie.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-119">Describes the virtual machine settings for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[<span data-ttu-id="5aa1d-120">Comment configurer un utilisateur ou un groupe de domaine</span><span class="sxs-lookup"><span data-stu-id="5aa1d-120">How to Configure a Domain User or Group</span></span>](how-to-configure-a-domain-user-or-groupmedvv2.md)  
<span data-ttu-id="5aa1d-121">Décrit comment configurer les utilisateurs et les groupes du domaine.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-121">Describes how to configure domain users and groups.</span></span>

<a href="" id="how-to-configure-published-applications"></a>[<span data-ttu-id="5aa1d-122">Comment configurer des applications publiées</span><span class="sxs-lookup"><span data-stu-id="5aa1d-122">How to Configure Published Applications</span></span>](how-to-configure-published-applicationsmedvv2.md)  
<span data-ttu-id="5aa1d-123">Décrit les applications et les menus publiés et comment les appliquer à une stratégie.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-123">Describes published applications and menus, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[<span data-ttu-id="5aa1d-124">Comment configurer les paramètres Web pour un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5aa1d-124">How to Configure Web Settings for a MED-V Workspace</span></span>](how-to-configure-web-settings-for-a-med-v-workspace.md)  
<span data-ttu-id="5aa1d-125">Décrit les paramètres Web disponibles pour un espace de travail MED-V et la façon de les appliquer à une stratégie.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-125">Describes the Web settings available for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[<span data-ttu-id="5aa1d-126">Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5aa1d-126">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
<span data-ttu-id="5aa1d-127">Décrit la configuration de l’ordinateur virtuel pour un espace de travail MED-V et l’appliquer à une stratégie.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-127">Describes the virtual machine setup for a MED-V workspace, and how to apply it to a policy.</span></span>

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="5aa1d-128">Comment appliquer des paramètres réseau à un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5aa1d-128">How to Apply Network Settings to a MED-V Workspace</span></span>](how-to-apply-network-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="5aa1d-129">Décrit les paramètres réseau d’un espace de travail MED-V et la façon de les appliquer à une stratégie.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-129">Describes the network settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="5aa1d-130">Comment appliquer des paramètres de performances à un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5aa1d-130">How to Apply Performance Settings to a MED-V Workspace</span></span>](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="5aa1d-131">Décrit les paramètres de performances d’un espace de travail MED-V et la façon de les appliquer à une stratégie.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-131">Describes the performance settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-import-and-export-a-policy"></a>[<span data-ttu-id="5aa1d-132">Comment importer et exporter une stratégie</span><span class="sxs-lookup"><span data-stu-id="5aa1d-132">How to Import and Export a Policy</span></span>](how-to-import-and-export-a-policy.md)  
<span data-ttu-id="5aa1d-133">Décrit comment importer et exporter une stratégie.</span><span class="sxs-lookup"><span data-stu-id="5aa1d-133">Describes how to import and export a policy.</span></span>

 

 






---
title: Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0
description: Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810463"
---
# <span data-ttu-id="a3ea8-103">Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="a3ea8-103">How to Edit MBAM 1.0 GPO Settings</span></span>


<span data-ttu-id="a3ea8-104">Pour réussir le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM), vous devez d’abord déterminer les stratégies de groupe que vous utiliserez dans votre implémentation de l’administration et de la surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="a3ea8-105">Pour plus d’informations sur les différentes stratégies disponibles, voir [planification des exigences de la stratégie de groupe MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a3ea8-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="a3ea8-106">Après avoir déterminé les stratégies que vous allez utiliser, vous devez modifier un ou plusieurs objets de stratégie de groupe (GPO) incluant les paramètres de stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the MBAM policy settings.</span></span>

<span data-ttu-id="a3ea8-107">Les étapes suivantes expliquent comment configurer les paramètres de base d’un objet de stratégie de groupe (GPO) pour permettre à MBAM de gérer le chiffrement BitLocker pour les ordinateurs clients de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-107">The following steps describe how to configure the basic, recommended Group Policy object (GPO) settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="a3ea8-108">Pour modifier les paramètres de l’objet de stratégie de MBAM client</span><span class="sxs-lookup"><span data-stu-id="a3ea8-108">To edit the MBAM Client GPO settings</span></span>**

1.  <span data-ttu-id="a3ea8-109">Sur un ordinateur sur lequel le modèle de stratégie de groupe MBAM est installé, assurez-vous que les services MBAM sont activés.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="a3ea8-110">Utilisez la console de gestion des stratégies de groupe (GPMC. msc) ou le produit MDOP (Advanced Group Policy Management) pour les actions suivantes: sélectionnez **configuration**de l’ordinateur, sélectionnez **stratégies**, cliquez sur **modèles d’administration**, sélectionnez **composants Windows**, puis cliquez sur **MDOP MBAM (gestion BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-110">Use the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product for these actions: Select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="a3ea8-111">Modifiez les paramètres d’objets de stratégie de groupe requis pour activer les services clients MBAM sur des ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="a3ea8-112">Pour chaque stratégie figurant dans le tableau suivant, sélectionnez **groupe de stratégies**, cliquez sur la **stratégie**, puis configurez le **paramètre**.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**.</span></span>

    <span data-ttu-id="a3ea8-113">Groupe de stratégies</span><span class="sxs-lookup"><span data-stu-id="a3ea8-113">Policy Group</span></span>

    <span data-ttu-id="a3ea8-114">Stratégie</span><span class="sxs-lookup"><span data-stu-id="a3ea8-114">Policy</span></span>

    <span data-ttu-id="a3ea8-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a3ea8-115">Setting</span></span>

    <span data-ttu-id="a3ea8-116">Gestion des clients</span><span class="sxs-lookup"><span data-stu-id="a3ea8-116">Client Management</span></span>

    <span data-ttu-id="a3ea8-117">Configurer les services de MBAM</span><span class="sxs-lookup"><span data-stu-id="a3ea8-117">Configure MBAM Services</span></span>

    <span data-ttu-id="a3ea8-118">Activé.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-118">Enabled.</span></span> <span data-ttu-id="a3ea8-119">Définissez **MBAM point de terminaison du service matériel** et de récupération et **sélectionnez les informations de récupération BitLocker à stocker**.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-119">Set **MBAM Recovery and Hardware service endpoint** and **Select BitLocker recovery information to store**.</span></span>

    <span data-ttu-id="a3ea8-120">Définissez le **point de terminaison du service de conformité MBAM** et entrez la **fréquence du rapport d’État (minutes)**.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-120">Set **MBAM compliance service endpoint** and **Enter status report frequency in (minutes)**.</span></span>

    <span data-ttu-id="a3ea8-121">Autoriser la vérification de compatibilité matérielle</span><span class="sxs-lookup"><span data-stu-id="a3ea8-121">Allow hardware compatibility checking</span></span>

    <span data-ttu-id="a3ea8-122">Désactivé.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-122">Disabled.</span></span> <span data-ttu-id="a3ea8-123">Cette stratégie est activée par défaut, mais n’est pas nécessaire pour une implémentation de base MBAM.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-123">This policy is enabled by default, but is not needed for a basic MBAM implementation.</span></span>

    <span data-ttu-id="a3ea8-124">Lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a3ea8-124">Operating System Drive</span></span>

    <span data-ttu-id="a3ea8-125">Paramètres de chiffrement de lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a3ea8-125">Operating system drive encryption settings</span></span>

    <span data-ttu-id="a3ea8-126">Activé.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-126">Enabled.</span></span> <span data-ttu-id="a3ea8-127">Définissez **Sélectionner un protecteur pour le lecteur du système d’exploitation**.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-127">Set **Select protector for operating system drive**.</span></span> <span data-ttu-id="a3ea8-128">Cela est requis pour enregistrer les données du lecteur du système d’exploitation sur le serveur de récupération de clé MBAM.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-128">This is required to save operating system drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="a3ea8-129">Lecteur amovible</span><span class="sxs-lookup"><span data-stu-id="a3ea8-129">Removable Drive</span></span>

    <span data-ttu-id="a3ea8-130">Contrôler l’utilisation de BitLocker sur des lecteurs amovibles</span><span class="sxs-lookup"><span data-stu-id="a3ea8-130">Control Use of BitLocker on removable drives</span></span>

    <span data-ttu-id="a3ea8-131">Activé.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-131">Enabled.</span></span> <span data-ttu-id="a3ea8-132">Cela est requis Si MBAM enregistre les données du lecteur amovible sur le serveur de récupération de clés MBAM.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-132">This is required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="a3ea8-133">Lecteur fixe</span><span class="sxs-lookup"><span data-stu-id="a3ea8-133">Fixed Drive</span></span>

    <span data-ttu-id="a3ea8-134">Contrôler l’utilisation de BitLocker sur des disques fixes</span><span class="sxs-lookup"><span data-stu-id="a3ea8-134">Control Use of BitLocker on fixed drives</span></span>

    <span data-ttu-id="a3ea8-135">Activé.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-135">Enabled.</span></span> <span data-ttu-id="a3ea8-136">Cela est requis Si MBAM enregistre des données de disque fixe sur le serveur de récupération de clés MBAM.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-136">This is required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="a3ea8-137">Définissez **choisir la manière dont les lecteurs protégés par BitLocker peuvent être récupérés** et **autoriser l’agent de récupération de données**.</span><span class="sxs-lookup"><span data-stu-id="a3ea8-137">Set **Choose how BitLocker-protected drives can be recovered** and **Allow data recovery agent**.</span></span>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="a3ea8-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3ea8-138">Related topics</span></span>


[<span data-ttu-id="a3ea8-139">Déploiement d'objets de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="a3ea8-139">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)










---
title: Procédure de modification des paramètres d'objet de stratégie de groupe MBAM2.0
description: Procédure de modification des paramètres d'objet de stratégie de groupe MBAM2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810344"
---
# <span data-ttu-id="f1e2d-103">Procédure de modification des paramètres d'objet de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f1e2d-103">How to Edit MBAM 2.0 GPO Settings</span></span>


<span data-ttu-id="f1e2d-104">Pour réussir le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM), vous devez d’abord déterminer les stratégies de groupe que vous utiliserez dans votre implémentation de l’administration et de la surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="f1e2d-105">Pour plus d’informations sur les différentes stratégies disponibles, voir [planification des exigences de la stratégie de groupe MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="f1e2d-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="f1e2d-106">Après avoir déterminé les stratégies que vous allez utiliser, vous devez modifier un ou plusieurs objets de stratégie de groupe qui incluent les paramètres de stratégie pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the policy settings for MBAM.</span></span>

<span data-ttu-id="f1e2d-107">Vous pouvez utiliser les étapes suivantes pour configurer les paramètres de l’objet de stratégie de groupe de base et recommandés pour permettre à MBAM de gérer le chiffrement BitLocker pour les ordinateurs clients de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-107">You can use the following steps to configure the basic, recommended GPO settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="f1e2d-108">Pour modifier les paramètres de l’objet de stratégie de MBAM client</span><span class="sxs-lookup"><span data-stu-id="f1e2d-108">To Edit MBAM Client GPO Settings</span></span>**

1.  <span data-ttu-id="f1e2d-109">Sur un ordinateur sur lequel le modèle de stratégie de groupe MBAM est installé, assurez-vous que les services MBAM sont activés.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="f1e2d-110">À l’aide de la console de gestion des stratégies de groupe (GPMC. msc) ou du produit MDOP (Advanced Group Policy Management) sur un ordinateur sur lequel le modèle de stratégie de groupe MBAM est installé, sélectionnez **configuration**de l’ordinateur, cliquez sur **stratégies**, cliquez sur **modèles d’administration**, sélectionnez **composants Windows**, puis cliquez sur **MDOP MBAM (gestion BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-110">Using the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product on a computer with the MBAM Group Policy template installed, select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="f1e2d-111">Modifiez les paramètres d’objets de stratégie de groupe requis pour activer les services clients MBAM sur des ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="f1e2d-112">Pour chaque stratégie figurant dans le tableau suivant, sélectionnez **groupe de stratégies**, cliquez sur la **stratégie**, puis configurez le **paramètre**:</span><span class="sxs-lookup"><span data-stu-id="f1e2d-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="f1e2d-113">Groupe de stratégies</span><span class="sxs-lookup"><span data-stu-id="f1e2d-113">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="f1e2d-114">Stratégie</span><span class="sxs-lookup"><span data-stu-id="f1e2d-114">Policy</span></span></th>
    <th align="left"><span data-ttu-id="f1e2d-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f1e2d-115">Setting</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f1e2d-116">Gestion des clients</span><span class="sxs-lookup"><span data-stu-id="f1e2d-116">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f1e2d-117">Configurer les services de MBAM</span><span class="sxs-lookup"><span data-stu-id="f1e2d-117">Configure MBAM Services</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f1e2d-118">Activé.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-118">Enabled.</span></span> <span data-ttu-id="f1e2d-119">Définissez <strong> MBAM point de terminaison du service matériel et de récupération </strong> et <strong> sélectionnez les informations de récupération BitLocker à stocker </strong> .</span><span class="sxs-lookup"><span data-stu-id="f1e2d-119">Set <strong>MBAM Recovery and Hardware service endpoint</strong> and <strong>Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="f1e2d-120">Définissez le <strong> point de terminaison </strong> du service de conformité MBAM et entrez la fréquence du rapport d’État (minutes).</span><span class="sxs-lookup"><span data-stu-id="f1e2d-120">Set <strong>MBAM compliance service endpoint</strong> and Enter status report frequency in (minutes).</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f1e2d-121">Lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f1e2d-121">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f1e2d-122">Paramètres de chiffrement de lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f1e2d-122">Operating system drive encryption settings</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f1e2d-123">Activé.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-123">Enabled.</span></span> <span data-ttu-id="f1e2d-124">Définissez <strong> Sélectionner un protecteur pour le lecteur du système d’exploitation </strong> .</span><span class="sxs-lookup"><span data-stu-id="f1e2d-124">Set <strong>Select protector for operating system drive</strong>.</span></span> <span data-ttu-id="f1e2d-125">Requis pour enregistrer les données du lecteur du système d’exploitation sur le serveur de restauration MBAMKey.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-125">Required to save operating system drive data to the MBAMKey Recovery server.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f1e2d-126">Lecteur amovible</span><span class="sxs-lookup"><span data-stu-id="f1e2d-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f1e2d-127">Contrôler l’utilisation de BitLocker sur des lecteurs amovibles</span><span class="sxs-lookup"><span data-stu-id="f1e2d-127">Control Use of BitLocker on removable drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f1e2d-128">Activé.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-128">Enabled.</span></span> <span data-ttu-id="f1e2d-129">Obligatoire si MBAM enregistre les données du lecteur amovible sur le serveur de récupération de clés MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-129">Required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f1e2d-130">Lecteur fixe</span><span class="sxs-lookup"><span data-stu-id="f1e2d-130">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f1e2d-131">Contrôler l’utilisation de BitLocker sur des disques fixes</span><span class="sxs-lookup"><span data-stu-id="f1e2d-131">Control Use of BitLocker on fixed drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f1e2d-132">Activé.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-132">Enabled.</span></span> <span data-ttu-id="f1e2d-133">Obligatoire si MBAM enregistre des données de disque fixe sur le serveur de récupération de clés MBAM.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-133">Required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span></p>
    <p><span data-ttu-id="f1e2d-134">Définissez <strong> choisir la manière dont les lecteurs protégés par BitLocker peuvent être récupérés </strong> et <strong> autoriser l’agent de récupération de données </strong> .</span><span class="sxs-lookup"><span data-stu-id="f1e2d-134">Set <strong>Choose how BitLocker-protected drives can be recovered</strong> and <strong>Allow data recovery agent</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="f1e2d-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1e2d-135">Related topics</span></span>


[<span data-ttu-id="f1e2d-136">Déploiement d'objets de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f1e2d-136">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)










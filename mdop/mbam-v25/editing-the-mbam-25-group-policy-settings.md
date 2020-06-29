---
title: Modification des paramètres de stratégie de groupe MBAM2.5
description: Modification des paramètres de stratégie de groupe MBAM2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804345"
---
# <span data-ttu-id="07f1f-103">Modification des paramètres de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="07f1f-103">Editing the MBAM 2.5 Group Policy Settings</span></span>


<span data-ttu-id="07f1f-104">Pour réussir le déploiement de l’administration et de la surveillance de BitLocker Microsoft (MBAM), vous devez:</span><span class="sxs-lookup"><span data-stu-id="07f1f-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="07f1f-105">Tâche</span><span class="sxs-lookup"><span data-stu-id="07f1f-105">Task</span></span></th>
<th align="left"><span data-ttu-id="07f1f-106">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="07f1f-106">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07f1f-107">Copiez les modèles de stratégie de groupe MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="07f1f-107">Copy the MBAM 2.5 Group Policy Templates.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="07f1f-108">Copie des modèles de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="07f1f-108">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07f1f-109">Déterminez les objets de stratégie de groupe que vous voulez utiliser dans votre implémentation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="07f1f-109">Determine which Group Policy Objects (GPOs) you want to use in your MBAM implementation.</span></span> <span data-ttu-id="07f1f-110">En fonction des besoins de votre organisation, il se peut que vous deviez configurer des paramètres de stratégie de groupe supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="07f1f-110">Based on the needs of your organization, you might have to configure additional Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="07f1f-111">Planification de la stratégie de groupe MBAM 2,5 </a></span><span class="sxs-lookup"><span data-stu-id="07f1f-111">Planning for MBAM 2.5 Group Policy Requirements</a> – contains descriptions of the GPOs</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07f1f-112">Définissez les paramètres de stratégie de groupe pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="07f1f-112">Set the Group Policy settings for your organization.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="07f1f-113">**Important**  Ne modifiez pas les paramètres de stratégie de groupe du nœud **BitLocker Drive Encryption** , ou MBAM ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="07f1f-113">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="07f1f-114">Lorsque vous configurez les paramètres de stratégie de groupe dans le nœud **MDOP MBAM (gestion du BitLocker)** , MBAM configure automatiquement les paramètres de **chiffrement de lecteur BitLocker** pour vous.</span><span class="sxs-lookup"><span data-stu-id="07f1f-114">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="07f1f-115">Pour modifier les paramètres de stratégie de groupe du client MBAM</span><span class="sxs-lookup"><span data-stu-id="07f1f-115">To edit MBAM Client Group Policy settings</span></span>**

1.  <span data-ttu-id="07f1f-116">Sur un ordinateur sur lequel sont installés les modèles de stratégie de groupe de MBAM, assurez-vous que les services MBAM sont activés.</span><span class="sxs-lookup"><span data-stu-id="07f1f-116">On a computer that has the MBAM Group Policy Templates installed, make sure that MBAM Services are enabled.</span></span>

2.  <span data-ttu-id="07f1f-117">À l’aide de la console de gestion **des stratégies de** groupe (GPMC. msc) ou du produit de gestion de stratégie de groupe Microsoft avancée sur un ordinateur sur lequel sont installés &gt; **Policies** les modèles de &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="07f1f-117">Using the Group Policy Management Console (GPMC.msc) or the Microsoft Advanced Group Policy Management MDOP product on a computer with the MBAM Group Policy Templates installed, select **Computer configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="07f1f-118">Modifiez les paramètres de stratégie de groupe requis pour activer les services clients MBAM sur des ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="07f1f-118">Edit the Group Policy settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="07f1f-119">Pour chaque stratégie figurant dans le tableau suivant, sélectionnez **groupe de stratégies**, cliquez sur la **stratégie** souhaitée, puis configurez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="07f1f-119">For each policy in the following table, select **Policy Group**, click the **Policy** you want, and then configure the settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="07f1f-120">Groupe de stratégies</span><span class="sxs-lookup"><span data-stu-id="07f1f-120">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="07f1f-121">Stratégie</span><span class="sxs-lookup"><span data-stu-id="07f1f-121">Policy</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="07f1f-122">Gestion des clients</span><span class="sxs-lookup"><span data-stu-id="07f1f-122">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07f1f-123">Configurer les services de MBAM</span><span class="sxs-lookup"><span data-stu-id="07f1f-123">Configure MBAM Services</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="07f1f-124">Lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="07f1f-124">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07f1f-125">Paramètres de chiffrement de lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="07f1f-125">Operating system drive encryption settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="07f1f-126">Lecteur amovible</span><span class="sxs-lookup"><span data-stu-id="07f1f-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07f1f-127">Contrôler l’utilisation de BitLocker sur des lecteurs amovibles</span><span class="sxs-lookup"><span data-stu-id="07f1f-127">Control use of BitLocker on removable drives</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="07f1f-128">Lecteur fixe</span><span class="sxs-lookup"><span data-stu-id="07f1f-128">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="07f1f-129">Contrôler l’utilisation de BitLocker sur des disques fixes</span><span class="sxs-lookup"><span data-stu-id="07f1f-129">Control use of BitLocker on fixed drives</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="07f1f-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07f1f-130">Related topics</span></span>


[<span data-ttu-id="07f1f-131">Planification des exigences en matière de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="07f1f-131">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

[<span data-ttu-id="07f1f-132">Copie des modèles de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="07f1f-132">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

 
## <span data-ttu-id="07f1f-133">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="07f1f-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="07f1f-134">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="07f1f-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="07f1f-135">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="07f1f-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 






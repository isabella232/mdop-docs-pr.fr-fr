---
title: Gestion des exemptions de chiffrement BitLocker d'utilisateur
description: Gestion des exemptions de chiffrement BitLocker d'utilisateur
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804621"
---
# <span data-ttu-id="5ae76-103">Gestion des exemptions de chiffrement BitLocker d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="5ae76-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="5ae76-104">L’utilisation de Microsoft BitLocker administration et de la surveillance (MBAM) peut être utilisée pour gérer la protection de BitLocker en exemptant les utilisateurs qui n’ont pas besoin ou veulent que leurs lecteurs soient chiffrés.</span><span class="sxs-lookup"><span data-stu-id="5ae76-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="5ae76-105">Pour exempter les utilisateurs de la protection de BitLocker, une organisation doit d’abord créer une infrastructure pour prendre en charge ces exemptions.</span><span class="sxs-lookup"><span data-stu-id="5ae76-105">To exempt users from BitLocker protection, an organization must first create an infrastructure to support such exemptions.</span></span> <span data-ttu-id="5ae76-106">L’infrastructure de support technique peut inclure un numéro de téléphone de contact, une page Web ou une adresse postale pour demander une exemption.</span><span class="sxs-lookup"><span data-stu-id="5ae76-106">The supporting infrastructure might include a contact telephone number, webpage, or mailing address to request exemption.</span></span> <span data-ttu-id="5ae76-107">De plus, tous les utilisateurs exemptés devront être ajoutés à un groupe de sécurité pour une stratégie de groupe créée spécifiquement pour les utilisateurs exemptés.</span><span class="sxs-lookup"><span data-stu-id="5ae76-107">Also, any exempt user will have to be added to a security group for Group Policy created specifically for exempted users.</span></span> <span data-ttu-id="5ae76-108">Lorsque les membres de ce groupe de sécurité se connectent à un ordinateur, la stratégie de groupe d’utilisateurs indique que l’utilisateur est exempté de la protection BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ae76-108">When members of this security group log on to a computer, the user Group Policy shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="5ae76-109">La stratégie de l’utilisateur remplace la stratégie de l’ordinateur, et celle-ci reste exemptée du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ae76-109">The user policy overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="5ae76-110">**Remarques**  Si l’ordinateur est déjà protégé par BitLocker, la stratégie d’exemption d’utilisateur n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="5ae76-110">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="5ae76-111">Le tableau suivant indique la façon dont la protection de BitLocker est appliquée en fonction de la façon dont les exemptions sont définies.</span><span class="sxs-lookup"><span data-stu-id="5ae76-111">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ae76-112">État de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="5ae76-112">User Status</span></span></th>
<th align="left"><span data-ttu-id="5ae76-113">Ordinateur non exempté</span><span class="sxs-lookup"><span data-stu-id="5ae76-113">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="5ae76-114">Exonéré d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="5ae76-114">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5ae76-115">Utilisateur non exempté</span><span class="sxs-lookup"><span data-stu-id="5ae76-115">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ae76-116">La protection BitLocker est appliquée à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5ae76-116">BitLocker protection is enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ae76-117">La protection BitLocker n’est pas appliquée à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5ae76-117">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5ae76-118">Exonéré d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="5ae76-118">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ae76-119">La protection BitLocker n’est pas appliquée à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5ae76-119">BitLocker protection is not enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ae76-120">La protection BitLocker n’est pas appliquée à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5ae76-120">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="5ae76-121">Pour exempter un utilisateur d’un chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="5ae76-121">To exempt a user from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="5ae76-122">Créer un groupe de sécurité ActiveDirectoryDomainServices qui sera utilisé pour gérer les exemptions d’utilisateur à partir du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ae76-122">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption.</span></span>

2.  <span data-ttu-id="5ae76-123">Créer un paramètre d’objet de stratégie de groupe à l’aide du modèle de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ae76-123">Create a Group Policy Object setting by using the MBAM Group Policy template.</span></span> <span data-ttu-id="5ae76-124">Associez l’objet de stratégie de groupe au groupe Active Directory que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="5ae76-124">Associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="5ae76-125">Pour plus d’informations sur les paramètres de stratégie nécessaires et permettre aux utilisateurs de demander une exemption du chiffrement BitLocker, voir la section configurer une stratégie d’exemption d’utilisateur pour la [planification des spécifications de la stratégie de groupe MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5ae76-125">For more information about the necessary policy settings to enable users to request exemption from BitLocker encryption, see the Configure User Exemption Policy section in [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

3.  <span data-ttu-id="5ae76-126">Après avoir créé un groupe de sécurité pour les utilisateurs exemptés de BitLocker, ajoutez à ce groupe les noms des utilisateurs qui demandent une exemption.</span><span class="sxs-lookup"><span data-stu-id="5ae76-126">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting exemption.</span></span> <span data-ttu-id="5ae76-127">Lorsqu’un utilisateur ouvre une session sur un ordinateur contrôlé par BitLocker, le client MBAM vérifie le paramètre de stratégie d’exemption des utilisateurs et suspend la protection en fonction de la présence de l’utilisateur dans le groupe de sécurité d’exemption BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ae76-127">When a user logs on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="5ae76-128">**Remarques**  Les scénarios d’ordinateurs partagés nécessitent une prise en considération particulière concernant l’exemption des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5ae76-128">**Note** Shared computer scenarios require special consideration regarding user exemption.</span></span> <span data-ttu-id="5ae76-129">Si un utilisateur non exempté se connecte à un ordinateur partagé avec un utilisateur exempté, il est possible que l’ordinateur soit crypté.</span><span class="sxs-lookup"><span data-stu-id="5ae76-129">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="5ae76-130">Pour permettre aux utilisateurs de demander une exemption du chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="5ae76-130">To enable users to request exemption from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="5ae76-131">Après avoir configuré les stratégies d’exemption des utilisateurs en usingwith le modèle de stratégie MBAM, un utilisateur peut demander une exemption de protection BitLocker via le client MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ae76-131">After you have configured user-exemption policies by usingwith the MBAM Policy template, a user can request exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="5ae76-132">Lorsqu’un utilisateur ouvre une session sur un ordinateur marqué comme **compatible** dans la liste de compatibilité matérielle MBAM, le système présente à l’utilisateur une notification indiquant que l’ordinateur va être chiffré.</span><span class="sxs-lookup"><span data-stu-id="5ae76-132">When a user logs on to a computer that is marked as **Compatible** in the MBAM Hardware Compatibility list, the system presents the user with a notification that the computer is going to be encrypted.</span></span> <span data-ttu-id="5ae76-133">L’utilisateur peut sélectionner l' **exemption de demande** et différer le chiffrement en le sélectionnant **plus tard**, ou sélectionnez **Démarrer** pour accepter le chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ae76-133">The user can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="5ae76-134">**Remarques**  La sélection de l' **exemption de requête** différera la protection de BitLocker jusqu’à la durée maximale définie dans la stratégie d’exemption de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ae76-134">**Note** Selecting **Request Exemption** will postpone the BitLocker protection until the maximum time set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="5ae76-135">Lorsqu’un utilisateur sélectionne une **exemption de requête**, il est prévenu de contacter le groupe d’administration BitLocker de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="5ae76-135">When a user selects **Request Exemption**, the user is notified to contact the organization's BitLocker administration group.</span></span> <span data-ttu-id="5ae76-136">En fonction du mode de configuration de la stratégie d’exemption d’utilisateur, les utilisateurs disposent d’une ou plusieurs des méthodes de contact suivantes:</span><span class="sxs-lookup"><span data-stu-id="5ae76-136">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="5ae76-137">Numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="5ae76-137">Phone Number</span></span>

    -   <span data-ttu-id="5ae76-138">URL de la page Web</span><span class="sxs-lookup"><span data-stu-id="5ae76-138">Webpage URL</span></span>

    -   <span data-ttu-id="5ae76-139">Adresse postale</span><span class="sxs-lookup"><span data-stu-id="5ae76-139">Mailing Address</span></span>

    <span data-ttu-id="5ae76-140">Après l’envoi de la demande, l’administrateur MBAM peut décider s’il convient d’ajouter l’utilisateur au groupe Active Directory d’exemption BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ae76-140">After submittal of the request, the MBAM Administrator can decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="5ae76-141">**Remarques**  Lorsque la limite de temps de report de la stratégie d’exemption des utilisateurs a expiré, les utilisateurs ne voient pas l’option de demande d’exemption de la stratégie de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="5ae76-141">**Note** Once the postpone time limit from the User Exemption Policy has expired, users will not see the option to request exemption to the encryption policy.</span></span> <span data-ttu-id="5ae76-142">À ce stade, les utilisateurs doivent contacter l’administrateur MBAM directement pour pouvoir bénéficier d’une exemption de la protection de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ae76-142">At this point, users must contact the MBAM administrator directly in order to receive exemption from BitLocker Protection.</span></span>

     

## <span data-ttu-id="5ae76-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ae76-143">Related topics</span></span>


[<span data-ttu-id="5ae76-144">Administration des composants de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="5ae76-144">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 






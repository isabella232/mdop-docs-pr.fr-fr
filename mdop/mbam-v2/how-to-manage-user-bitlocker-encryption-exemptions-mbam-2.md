---
title: Gestion des exemptions de chiffrement BitLocker d'utilisateur
description: Gestion des exemptions de chiffrement BitLocker d'utilisateur
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810937"
---
# <span data-ttu-id="69c1d-103">Gestion des exemptions de chiffrement BitLocker d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="69c1d-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="69c1d-104">Le contrôle de la protection BitLocker par le biais de l’administration et de la surveillance de Microsoft BitLocker (MBAM) permet d’exempter les utilisateurs si des utilisateurs n’ont pas besoin ou veulent que leurs lecteurs soient chiffrés.</span><span class="sxs-lookup"><span data-stu-id="69c1d-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users if there are users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="69c1d-105">Pour exempter les utilisateurs de la protection de BitLocker, une organisation doit créer une infrastructure pour prendre en charge les utilisateurs exemptés, comme le fait de fournir à l’utilisateur un numéro de téléphone, une page Web ou une adresse de messagerie à utiliser pour demander une exemption.</span><span class="sxs-lookup"><span data-stu-id="69c1d-105">To exempt users from BitLocker protection, an organization will have to create an infrastructure to support exempted users, such as giving the user a contact telephone number, webpage, or mailing address to use to request an exemption.</span></span> <span data-ttu-id="69c1d-106">Par ailleurs, un utilisateur exempté doit être ajouté à un groupe de sécurité pour un objet de stratégie de groupe qui a été créé spécifiquement pour les utilisateurs exemptés.</span><span class="sxs-lookup"><span data-stu-id="69c1d-106">Also, an exempt user will have to be added to a security group for a Group Policy Object that was created specifically for exempted users.</span></span> <span data-ttu-id="69c1d-107">Lorsque les membres de ce groupe de sécurité se connectent à un ordinateur, le paramètre de stratégie de groupe de l’utilisateur indique que l’utilisateur est exempté de la protection de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="69c1d-107">When members of this security group log on to a computer, the user’s Group Policy setting shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="69c1d-108">Le paramètre de stratégie de groupe de l’utilisateur remplace la stratégie de l’ordinateur et l’ordinateur reste exempt du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="69c1d-108">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="69c1d-109">**Remarques**  Si l’ordinateur est déjà protégé par BitLocker, la stratégie d’exemption d’utilisateur n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="69c1d-109">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="69c1d-110">Le tableau suivant indique la façon dont la protection de BitLocker est appliquée en fonction de la façon dont les exemptions sont définies.</span><span class="sxs-lookup"><span data-stu-id="69c1d-110">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69c1d-111">État de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="69c1d-111">User Status</span></span></th>
<th align="left"><span data-ttu-id="69c1d-112">Ordinateur non exempté</span><span class="sxs-lookup"><span data-stu-id="69c1d-112">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="69c1d-113">Exonéré d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="69c1d-113">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="69c1d-114">Utilisateur non exempté</span><span class="sxs-lookup"><span data-stu-id="69c1d-114">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="69c1d-115">La protection BitLocker est appliquée sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="69c1d-115">BitLocker protection is enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="69c1d-116">La protection BitLocker n’est pas appliquée sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="69c1d-116">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="69c1d-117">Exonéré d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="69c1d-117">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="69c1d-118">La protection BitLocker n’est pas appliquée sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="69c1d-118">BitLocker protection is not enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="69c1d-119">La protection BitLocker n’est pas appliquée sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="69c1d-119">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="69c1d-120">Pour exempter un utilisateur d’un chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="69c1d-120">To exempt a user from BitLocker encryption</span></span>**

1.  <span data-ttu-id="69c1d-121">Créer un groupe de sécurité ActiveDirectoryDomainServices qui sera utilisé pour gérer les exemptions des utilisateurs des exigences de chiffrement de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="69c1d-121">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="69c1d-122">Créez un paramètre d’objet de stratégie de groupe à l’aide du modèle Microsoft BitLocker Administration and Monitoring Policy et associez-le au groupe Active Directory que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="69c1d-122">Create a Group Policy Object setting by using the Microsoft BitLocker Administration and Monitoring Group Policy template and associate it with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="69c1d-123">Les paramètres de stratégie permettant d’exempter les utilisateurs sont accessibles sous **UserConfiguration\\Administrative Templates\\Windows COMPONENTS\\MDOP MBAM (gestion de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="69c1d-123">The policy settings to exempt users can be found under **UserConfiguration\\Administrative Templates\\Windows Components\\MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="69c1d-124">Après avoir créé un groupe de sécurité pour les utilisateurs exemptés de BitLocker, ajoutez à ce groupe les noms des utilisateurs qui demandent une exemption.</span><span class="sxs-lookup"><span data-stu-id="69c1d-124">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting an exemption.</span></span> <span data-ttu-id="69c1d-125">Lorsque les utilisateurs se connectent à un ordinateur contrôlé par BitLocker, le client MBAM vérifie le paramètre de stratégie d’exemption des utilisateurs et suspend la protection en fonction de la présence de l’utilisateur dans le groupe de sécurité d’exemption BitLocker.</span><span class="sxs-lookup"><span data-stu-id="69c1d-125">When users log on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="69c1d-126">**Important**  Les scénarios d’ordinateurs partagés nécessitent une prise en considération particulière lors de l’utilisation d’exemptions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="69c1d-126">**Important** Shared computer scenarios require special consideration when using user exemptions.</span></span> <span data-ttu-id="69c1d-127">Si un utilisateur non exempté se connecte à un ordinateur partagé avec un utilisateur exempté, il est possible que l’ordinateur soit crypté.</span><span class="sxs-lookup"><span data-stu-id="69c1d-127">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="69c1d-128">Pour permettre aux utilisateurs de demander une exemption du chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="69c1d-128">To enable users to request an exemption from BitLocker encryption</span></span>**

1.  <span data-ttu-id="69c1d-129">Si vous avez configuré des stratégies d’exemption utilisateur à l’aide du modèle de stratégie MBAM, un utilisateur peut demander une exemption de protection BitLocker via le client MBAM.</span><span class="sxs-lookup"><span data-stu-id="69c1d-129">If you have configured user exemption policies by using the MBAM policy template, a user can request an exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="69c1d-130">Lorsque les utilisateurs se connectent à un ordinateur qui est tenu d’être chiffrés, ils reçoivent une notification indiquant que leur ordinateur va être chiffré.</span><span class="sxs-lookup"><span data-stu-id="69c1d-130">When users log on to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="69c1d-131">Ils peuvent sélectionner l' **exemption de demande** et différer le chiffrement en sélectionnant **plus tard**, ou sélectionnez **Démarrer** pour accepter le chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="69c1d-131">They can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="69c1d-132">**Remarques**  Le fait de sélectionner **dispense de requête** permet de différer la protection BitLocker jusqu’au délai maximal défini dans la stratégie d’exemption des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="69c1d-132">**Note** Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="69c1d-133">Si les utilisateurs sélectionnent une **exemption de demande**, ils reçoivent une notification leur indiquant de contacter le groupe d’administration BitLocker de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="69c1d-133">If users select **Request Exemption**, they receive a notification telling them to contact your organization’s BitLocker administration group.</span></span> <span data-ttu-id="69c1d-134">En fonction du mode de configuration de la stratégie d’exemption d’utilisateur, les utilisateurs disposent d’une ou plusieurs des méthodes de contact suivantes:</span><span class="sxs-lookup"><span data-stu-id="69c1d-134">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="69c1d-135">Numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="69c1d-135">Phone Number</span></span>

    -   <span data-ttu-id="69c1d-136">URL de la page Web</span><span class="sxs-lookup"><span data-stu-id="69c1d-136">Webpage URL</span></span>

    -   <span data-ttu-id="69c1d-137">Adresse postale</span><span class="sxs-lookup"><span data-stu-id="69c1d-137">Mailing Address</span></span>

    <span data-ttu-id="69c1d-138">Après la réception de la demande d’exemption, l’administrateur MBAM peut décider s’il convient d’ajouter l’utilisateur au groupe Active Directory d’exemption BitLocker.</span><span class="sxs-lookup"><span data-stu-id="69c1d-138">After the exemption request is received, the MBAM Administrator can take decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="69c1d-139">**Remarques**  Dès qu’un utilisateur envoie une demande d’exemption, l’agent MBAM signale que l’utilisateur est «exempt provisoire», puis attend un nombre de jours configuré avant de vérifier la compatibilité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="69c1d-139">**Note** Once a user submits an exemption request, the MBAM agent reports the user as “temporarily exempt” and then waits a configurable number of days before it checks the computer’s compliance again.</span></span> <span data-ttu-id="69c1d-140">Si l’administrateur MBAM rejette la demande d’exemption, l’option de demande d’exemption est désactivée, ce qui permet à l’utilisateur d’être à nouveau en mesure de demander l’exemption.</span><span class="sxs-lookup"><span data-stu-id="69c1d-140">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from being able to request the exemption again.</span></span>

     

## <span data-ttu-id="69c1d-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69c1d-141">Related topics</span></span>


[<span data-ttu-id="69c1d-142">Administration des composants de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="69c1d-142">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 






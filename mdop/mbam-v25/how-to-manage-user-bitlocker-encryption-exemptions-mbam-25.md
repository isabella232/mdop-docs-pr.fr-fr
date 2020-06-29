---
title: Gestion des exemptions de chiffrement BitLocker d'utilisateur
description: Gestion des exemptions de chiffrement BitLocker d'utilisateur
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811969"
---
# <span data-ttu-id="01ffa-103">Gestion des exemptions de chiffrement BitLocker d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="01ffa-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="01ffa-104">Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) vous permet d’exempter les utilisateurs des exigences relatives au chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="01ffa-105">Pour exempter les utilisateurs de la protection BitLocker, vous devez:</span><span class="sxs-lookup"><span data-stu-id="01ffa-105">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="01ffa-106">Tâche</span><span class="sxs-lookup"><span data-stu-id="01ffa-106">Task</span></span></th>
<th align="left"><span data-ttu-id="01ffa-107">Détails</span><span class="sxs-lookup"><span data-stu-id="01ffa-107">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01ffa-108">Créez une infrastructure pour prendre en charge les utilisateurs exemptés.</span><span class="sxs-lookup"><span data-stu-id="01ffa-108">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="01ffa-109">Dans le cas d’une telle infrastructure, il est possible de fournir aux utilisateurs un numéro de téléphone de contact, une page Web ou une adresse postale qu’ils peuvent utiliser pour demander une exemption.</span><span class="sxs-lookup"><span data-stu-id="01ffa-109">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01ffa-110">Ajoutez l’utilisateur exempté à un groupe de sécurité pour un objet de stratégie de groupe qui est configuré spécifiquement pour les utilisateurs exemptés.</span><span class="sxs-lookup"><span data-stu-id="01ffa-110">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="01ffa-111">Lorsque les membres de ce groupe de sécurité se connectent à un ordinateur, le paramètre de stratégie de groupe de l’utilisateur exempte l’utilisateur de la protection BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-111">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="01ffa-112">Le paramètre de stratégie de groupe de l’utilisateur remplace la stratégie de l’ordinateur et l’ordinateur reste exempt du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-112">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="01ffa-113">Remarque</span><span class="sxs-lookup"><span data-stu-id="01ffa-113">Note</span></span></strong><br/><p><span data-ttu-id="01ffa-114">MBAM ne prend pas en charge la stratégie de chiffrement si l’ordinateur est déjà protégé par BitLocker et qu’il est exempté.</span><span class="sxs-lookup"><span data-stu-id="01ffa-114">MBAM does not enact the encryption policy if the computer is already BitLocker-protected and the user is exempted.</span></span> <span data-ttu-id="01ffa-115">Toutefois, si un autre utilisateur qui n’est pas exempt de la stratégie de cryptage se connecte à l’ordinateur, le chiffrement aura lieu.</span><span class="sxs-lookup"><span data-stu-id="01ffa-115">However, if another user who is not exempt from the encryption policy signs in to the computer, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="01ffa-116">Les étapes suivantes décrivent ce qui se produit lorsque les utilisateurs finaux demandent une exemption du processus d’exemption du chiffrement de lecteur BitLocker par le biais du client MBAM ou du processus utilisé par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="01ffa-116">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="01ffa-117">Vous devez configurer des paramètres de stratégie de groupe MBAM pour autoriser les utilisateurs finaux à demander une exemption du chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-117">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="01ffa-118">Lorsque les utilisateurs finaux se connectent à un ordinateur requis pour être chiffrés, ils reçoivent une notification indiquant que leur ordinateur va être chiffré.</span><span class="sxs-lookup"><span data-stu-id="01ffa-118">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="01ffa-119">Ils peuvent sélectionner l' **exemption de demande** et différer le chiffrement en sélectionnant **différer**, ou ils peuvent sélectionner **commencer le chiffrement** pour accepter le chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-119">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="01ffa-120">Remarque</span><span class="sxs-lookup"><span data-stu-id="01ffa-120">Note</span></span>**  
    <span data-ttu-id="01ffa-121">Le fait de sélectionner **dispense de requête** permet de différer la protection BitLocker jusqu’au délai maximal défini dans la stratégie d’exemption des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="01ffa-121">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="01ffa-122">Si les utilisateurs finaux sélectionnent une **demande d’exemption**, ils reçoivent une notification leur demandant de contacter le groupe d’administration BitLocker de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="01ffa-122">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="01ffa-123">En fonction du mode de configuration de la **stratégie d’exemption d’utilisateur** , les utilisateurs disposent d’une ou plusieurs des méthodes de contact suivantes:</span><span class="sxs-lookup"><span data-stu-id="01ffa-123">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="01ffa-124">Numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="01ffa-124">Phone number</span></span>

    -   <span data-ttu-id="01ffa-125">URL de la page Web</span><span class="sxs-lookup"><span data-stu-id="01ffa-125">Webpage URL</span></span>

    -   <span data-ttu-id="01ffa-126">Adresse postale</span><span class="sxs-lookup"><span data-stu-id="01ffa-126">Mailing address</span></span>

3.  <span data-ttu-id="01ffa-127">Après la réception de la demande d’exemption, l’administrateur MBAM décide s’il doit ajouter l’utilisateur au groupe AD DS (Active Directory Domain Services) d’exemption BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-127">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="01ffa-128">Après l’envoi d’une demande d’exemption par un utilisateur final, le client MBAM signale que l’utilisateur est «exempté temporaire».</span><span class="sxs-lookup"><span data-stu-id="01ffa-128">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="01ffa-129">Le client attend alors un nombre de jours spécifié, qu’il doit configurer, avant de vérifier à nouveau la conformité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="01ffa-129">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="01ffa-130">Si l’administrateur MBAM rejette la demande d’exemption, l’option de demande d’exemption est désactivée, ce qui empêche l’utilisateur de demander de nouveau l’exemption.</span><span class="sxs-lookup"><span data-stu-id="01ffa-130">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

<span data-ttu-id="01ffa-131">Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) vous permet d’exempter les utilisateurs des exigences relatives au chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-131">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="01ffa-132">Pour exempter les utilisateurs de la protection BitLocker, vous devez:</span><span class="sxs-lookup"><span data-stu-id="01ffa-132">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="01ffa-133">Tâche</span><span class="sxs-lookup"><span data-stu-id="01ffa-133">Task</span></span></th>
<th align="left"><span data-ttu-id="01ffa-134">Détails</span><span class="sxs-lookup"><span data-stu-id="01ffa-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01ffa-135">Créez une infrastructure pour prendre en charge les utilisateurs exemptés.</span><span class="sxs-lookup"><span data-stu-id="01ffa-135">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="01ffa-136">Dans le cas d’une telle infrastructure, il est possible de fournir aux utilisateurs un numéro de téléphone de contact, une page Web ou une adresse postale qu’ils peuvent utiliser pour demander une exemption.</span><span class="sxs-lookup"><span data-stu-id="01ffa-136">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01ffa-137">Ajoutez l’utilisateur exempté à un groupe de sécurité pour un objet de stratégie de groupe qui est configuré spécifiquement pour les utilisateurs exemptés.</span><span class="sxs-lookup"><span data-stu-id="01ffa-137">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="01ffa-138">Lorsque les membres de ce groupe de sécurité se connectent à un ordinateur, le paramètre de stratégie de groupe de l’utilisateur exempte l’utilisateur de la protection BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-138">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="01ffa-139">Le paramètre de stratégie de groupe de l’utilisateur remplace la stratégie de l’ordinateur et l’ordinateur reste exempt du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-139">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="01ffa-140">Remarque</span><span class="sxs-lookup"><span data-stu-id="01ffa-140">Note</span></span></strong><br/><p><span data-ttu-id="01ffa-141">Si l’ordinateur est déjà protégé par BitLocker, la stratégie d’exemption d’utilisateur n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="01ffa-141">If the computer is already BitLocker-protected, the User Exemption Policy has no effect.</span></span> <span data-ttu-id="01ffa-142">De plus, si un autre utilisateur se connecte à un ordinateur qui n’est pas exempt de la stratégie de chiffrement, le chiffrement aura lieu.</span><span class="sxs-lookup"><span data-stu-id="01ffa-142">In addition, if another user signs in to a computer that is not exempt from the encryption policy, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="01ffa-143">Les étapes suivantes décrivent ce qui se produit lorsque les utilisateurs finaux demandent une exemption du processus d’exemption du chiffrement de lecteur BitLocker par le biais du client MBAM ou du processus utilisé par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="01ffa-143">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="01ffa-144">Vous devez configurer des paramètres de stratégie de groupe MBAM pour autoriser les utilisateurs finaux à demander une exemption du chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-144">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="01ffa-145">Lorsque les utilisateurs finaux se connectent à un ordinateur requis pour être chiffrés, ils reçoivent une notification indiquant que leur ordinateur va être chiffré.</span><span class="sxs-lookup"><span data-stu-id="01ffa-145">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="01ffa-146">Ils peuvent sélectionner l' **exemption de demande** et différer le chiffrement en sélectionnant **différer**, ou ils peuvent sélectionner **commencer le chiffrement** pour accepter le chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-146">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="01ffa-147">Remarque</span><span class="sxs-lookup"><span data-stu-id="01ffa-147">Note</span></span>**  
    <span data-ttu-id="01ffa-148">Le fait de sélectionner **dispense de requête** permet de différer la protection BitLocker jusqu’au délai maximal défini dans la stratégie d’exemption des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="01ffa-148">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="01ffa-149">Si les utilisateurs finaux sélectionnent une **demande d’exemption**, ils reçoivent une notification leur demandant de contacter le groupe d’administration BitLocker de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="01ffa-149">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="01ffa-150">En fonction du mode de configuration de la **stratégie d’exemption d’utilisateur** , les utilisateurs disposent d’une ou plusieurs des méthodes de contact suivantes:</span><span class="sxs-lookup"><span data-stu-id="01ffa-150">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="01ffa-151">Numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="01ffa-151">Phone number</span></span>

    -   <span data-ttu-id="01ffa-152">URL de la page Web</span><span class="sxs-lookup"><span data-stu-id="01ffa-152">Webpage URL</span></span>

    -   <span data-ttu-id="01ffa-153">Adresse postale</span><span class="sxs-lookup"><span data-stu-id="01ffa-153">Mailing address</span></span>

3.  <span data-ttu-id="01ffa-154">Après la réception de la demande d’exemption, l’administrateur MBAM décide s’il doit ajouter l’utilisateur au groupe AD DS (Active Directory Domain Services) d’exemption BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-154">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="01ffa-155">Après l’envoi d’une demande d’exemption par un utilisateur final, le client MBAM signale que l’utilisateur est «exempté temporaire».</span><span class="sxs-lookup"><span data-stu-id="01ffa-155">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="01ffa-156">Le client attend alors un nombre de jours spécifié, qu’il doit configurer, avant de vérifier à nouveau la conformité de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="01ffa-156">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="01ffa-157">Si l’administrateur MBAM rejette la demande d’exemption, l’option de demande d’exemption est désactivée, ce qui empêche l’utilisateur de demander de nouveau l’exemption.</span><span class="sxs-lookup"><span data-stu-id="01ffa-157">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

**<span data-ttu-id="01ffa-158">Pour exempter un utilisateur d’un chiffrement de lecteur BitLocker</span><span class="sxs-lookup"><span data-stu-id="01ffa-158">To exempt a user from BitLocker Drive Encryption</span></span>**

1.  <span data-ttu-id="01ffa-159">Créer un groupe de sécurité AD DS qui sera utilisé pour gérer les exemptions des utilisateurs des exigences de chiffrement de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-159">Create an AD DS security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="01ffa-160">Création d’un objet de stratégie de groupe à l’aide des modèles de stratégie de groupe Microsoft et administration de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-160">Create a Group Policy Object by using the Microsoft BitLocker Administration and Monitoring Group Policy Templates.</span></span>

3.  <span data-ttu-id="01ffa-161">Associez l’objet de stratégie de groupe au groupe AD DS que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="01ffa-161">Associate the Group Policy Object with the AD DS group that you created in the previous step.</span></span> <span data-ttu-id="01ffa-162">Les paramètres de stratégie permettant d’exempter les utilisateurs se trouvent dans l’emplacement suivant: **UserConfiguration** des &gt; **modèles d’administration** &gt; **composants** &gt; **MBAM MDOP (gestion de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="01ffa-162">The policy settings to exempt users are located at: **UserConfiguration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

4.  <span data-ttu-id="01ffa-163">Pour le groupe de sécurité que vous avez créé pour les utilisateurs exemptés de BitLocker, ajoutez le nom des utilisateurs demandant une exemption.</span><span class="sxs-lookup"><span data-stu-id="01ffa-163">To the security group you created for BitLocker exempted users, add the names of the users who are requesting an exemption.</span></span>

    <span data-ttu-id="01ffa-164">Lorsqu’un utilisateur se connecte à un ordinateur contrôlé par BitLocker, le client MBAM vérifie le paramètre de stratégie d’exemption de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="01ffa-164">When a user signs in to a computer controlled by BitLocker, the MBAM Client checks the User Exemption Policy setting.</span></span> <span data-ttu-id="01ffa-165">Si l’ordinateur est déjà crypté, la protection BitLocker n’est pas suspendue.</span><span class="sxs-lookup"><span data-stu-id="01ffa-165">If the computer is already encrypted, BitLocker protection is not suspended.</span></span> <span data-ttu-id="01ffa-166">Si l’ordinateur n’est pas chiffré, MBAM ne demande pas à l’utilisateur d’effectuer le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="01ffa-166">If the computer is not encrypted, MBAM does not prompt the user to encrypt.</span></span>

    **<span data-ttu-id="01ffa-167">Important</span><span class="sxs-lookup"><span data-stu-id="01ffa-167">Important</span></span>**  
    <span data-ttu-id="01ffa-168">Les scénarios d’ordinateurs partagés nécessitent une prise en considération particulière lors de l’utilisation d’exemptions d’utilisateur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="01ffa-168">Shared computer scenarios require special consideration when you are using BitLocker user exemptions.</span></span> <span data-ttu-id="01ffa-169">Si un utilisateur non exempté se connecte à un ordinateur partagé avec un utilisateur exempté, il est possible que l’ordinateur soit crypté.</span><span class="sxs-lookup"><span data-stu-id="01ffa-169">If a non-exempt user signs in to a computer that is shared with an exempt user, the computer may be encrypted.</span></span>




## <span data-ttu-id="01ffa-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01ffa-170">Related topics</span></span>


[<span data-ttu-id="01ffa-171">Administration des composants de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="01ffa-171">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="01ffa-172">Planification des exigences en matière de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="01ffa-172">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)




## <span data-ttu-id="01ffa-173">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="01ffa-173">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="01ffa-174">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="01ffa-174">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="01ffa-175">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="01ffa-175">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>





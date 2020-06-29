---
title: Planification des comptes et groupes MBAM2.5
description: Planification des comptes et groupes MBAM2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811375"
---
# <span data-ttu-id="557f7-103">Planification des comptes et groupes MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="557f7-103">Planning for MBAM 2.5 Groups and Accounts</span></span>


<span data-ttu-id="557f7-104">Cette rubrique répertorie les rôles et comptes que vous devez créer dans les services de domaine Active Directory (AD DS) pour fournir de la sécurité et des droits d’accès pour les bases de données, rapports et applications Web Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="557f7-104">This topic lists the roles and accounts that you must create in Active Directory Domain Services (AD DS) to provide security and access rights for the Microsoft BitLocker Administration and Monitoring (MBAM) databases, reports, and web applications.</span></span> <span data-ttu-id="557f7-105">Pour chaque rôle et compte, le champ correspondant dans l’Assistant Configuration de MBAM Server est fourni.</span><span class="sxs-lookup"><span data-stu-id="557f7-105">For each role and account, the corresponding field in the MBAM Server Configuration wizard is provided.</span></span> <span data-ttu-id="557f7-106">Pour obtenir la liste des cmdlets et paramètres Windows PowerShell qui correspondent à ces comptes, voir [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span><span class="sxs-lookup"><span data-stu-id="557f7-106">For a list of Windows PowerShell cmdlets and parameters that correspond to these accounts, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span></span>

**<span data-ttu-id="557f7-107">Remarque</span><span class="sxs-lookup"><span data-stu-id="557f7-107">Note</span></span>**  
<span data-ttu-id="557f7-108">MBAM ne prend pas en charge l’utilisation des comptes de service géré.</span><span class="sxs-lookup"><span data-stu-id="557f7-108">MBAM does not support the use of managed service accounts.</span></span>



## <span data-ttu-id="557f7-109">Comptes de base de données</span><span class="sxs-lookup"><span data-stu-id="557f7-109">Database accounts</span></span>


<span data-ttu-id="557f7-110">Créez les comptes suivants pour la base de données d’audit et de compatibilité et pour la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="557f7-110">Create the following accounts for the Compliance and Audit Database and the Recovery Database.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="557f7-111">Nom du compte et objet</span><span class="sxs-lookup"><span data-stu-id="557f7-111">Account name and purpose</span></span></th>
<th align="left"><span data-ttu-id="557f7-112">Type de compte</span><span class="sxs-lookup"><span data-stu-id="557f7-112">Account type</span></span></th>
<th align="left"><span data-ttu-id="557f7-113">Champ Assistant Configuration de MBAM Server qui correspond à ce compte</span><span class="sxs-lookup"><span data-stu-id="557f7-113">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="557f7-114">Description du champ de l’Assistant Configuration de MBAM Server qui correspond à ce compte.</span><span class="sxs-lookup"><span data-stu-id="557f7-114">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="557f7-115">Compatibilité et audit de la base de données et de la base de données de récupération utilisateur ou groupe en lecture/écriture pour les rapports</span><span class="sxs-lookup"><span data-stu-id="557f7-115">Compliance and Audit Database and Recovery Database read/write user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-116">Utilisateur ou groupe</span><span class="sxs-lookup"><span data-stu-id="557f7-116">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-117">Utilisateur ou groupe d’accès en lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="557f7-117">Read/write access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-118">Utilisateur ou groupe qui dispose d’un accès en lecture/écriture à la base de données de conformité et d’audit et à la base de données de récupération pour permettre aux applications Web d’accéder aux données et rapports dans ces bases de données.</span><span class="sxs-lookup"><span data-stu-id="557f7-118">Domain user or group that has read/write access to the Compliance and Audit Database and the Recovery Database to enable the web applications to access the data and reports in these databases.</span></span></p>
<p><span data-ttu-id="557f7-119">Si vous entrez un nom d’utilisateur dans ce champ, il doit être de la même valeur que la valeur dans le <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="557f7-119">If you enter a user name in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
<p><span data-ttu-id="557f7-120">Si vous entrez un nom de groupe dans ce champ, la valeur du <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> doit être membre du groupe que vous entrez dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="557f7-120">If you enter a group name in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="557f7-121">Conformité et audit de la base de données utilisateur ou groupe en lecture seule pour les rapports</span><span class="sxs-lookup"><span data-stu-id="557f7-121">Compliance and Audit Database read-only user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-122">Utilisateur ou groupe</span><span class="sxs-lookup"><span data-stu-id="557f7-122">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-123">Utilisateur ou groupe d’accès en lecture seule</span><span class="sxs-lookup"><span data-stu-id="557f7-123">Read-only access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-124">Nom de l’utilisateur ou du groupe qui dispose d’un accès en lecture seule à la base de données d’audit et de conformité pour permettre aux rapports d’accéder aux données de conformité et d’audit de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="557f7-124">Name of the user or group that will have read-only access to the Compliance and Audit Database to enable the reports to access the compliance and audit data in this database.</span></span></p>
<p><span data-ttu-id="557f7-125">Si vous entrez un nom d’utilisateur dans ce champ, il doit être le même que celui que vous avez spécifié dans le <strong> champ domaine de la base de données de conformité et d’audit </strong> de la <strong> page configurer des rapports </strong> .</span><span class="sxs-lookup"><span data-stu-id="557f7-125">If you enter a user name in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
<p><span data-ttu-id="557f7-126">Si vous entrez un nom de groupe dans ce champ, la valeur que vous spécifiez dans le <strong> champ domaine de la base de données de conformité et d’audit de </strong> la <strong> page configurer des rapports </strong> doit être membre du groupe que vous spécifiez dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="557f7-126">If you enter a group name in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="557f7-127">Comptes de création de rapports</span><span class="sxs-lookup"><span data-stu-id="557f7-127">Reporting accounts</span></span>


<span data-ttu-id="557f7-128">Créez les comptes suivants pour la fonction rapports.</span><span class="sxs-lookup"><span data-stu-id="557f7-128">Create the following accounts for the Reports feature.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="557f7-129">Nom/objectif du compte</span><span class="sxs-lookup"><span data-stu-id="557f7-129">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="557f7-130">Type de compte</span><span class="sxs-lookup"><span data-stu-id="557f7-130">Account type</span></span></th>
<th align="left"><span data-ttu-id="557f7-131">Champ Assistant Configuration de MBAM Server qui correspond à ce compte</span><span class="sxs-lookup"><span data-stu-id="557f7-131">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="557f7-132">Description du champ de l’Assistant Configuration de MBAM Server qui correspond à ce compte.</span><span class="sxs-lookup"><span data-stu-id="557f7-132">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="557f7-133">Rapport de groupe d’accès de domaine en lecture seule</span><span class="sxs-lookup"><span data-stu-id="557f7-133">Reports read-only domain access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-134">Groupe</span><span class="sxs-lookup"><span data-stu-id="557f7-134">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-135">Groupe de domaine de rôle de rapport</span><span class="sxs-lookup"><span data-stu-id="557f7-135">Reporting role domain group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-136">Spécifie le groupe d’utilisateurs de domaine qui dispose d’un accès en lecture seule aux rapports figurant sur le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="557f7-136">Specifies the domain user group that has read-only access to the reports in the Administration and Monitoring Website.</span></span> <span data-ttu-id="557f7-137">Le groupe que vous spécifiez doit être le même que celui que vous avez spécifié pour le paramètre rapport de groupe d’accès en lecture seule lorsque les applications Web sont activées.</span><span class="sxs-lookup"><span data-stu-id="557f7-137">The group you specify must be the same group you specified for the Reports Read Only Access Group parameter when the web apps are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="557f7-138">Compte d’utilisateur de base de données et de conformité</span><span class="sxs-lookup"><span data-stu-id="557f7-138">Compliance and Audit Database domain user account</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-139">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="557f7-139">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-140">Vérification de la conformité et de la base de données du compte de domaine</span><span class="sxs-lookup"><span data-stu-id="557f7-140">Compliance and Audit Database domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-141">Compte d’utilisateur de domaine et mot de passe que l’instance SQL Server Reporting Services locale utilise pour accéder à la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="557f7-141">Domain user account and password that the local SQL Server Reporting Services instance uses to access the Compliance and Audit Database.</span></span> <span data-ttu-id="557f7-142">Ce compte nécessite <strong> le droit d’ouverture de session par lot </strong> du serveur SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="557f7-142">This account requires <strong>Log On as Batch</strong> rights to the SQL Server Reporting Services server.</span></span></p>
<p><span data-ttu-id="557f7-143">Si la valeur que vous entrez dans le <strong> champ nom d’utilisateur ou de groupe d’accès en lecture seule </strong> de la <strong> page Configurer les bases de données </strong> est un nom d’utilisateur, vous devez entrer cette même valeur dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="557f7-143">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user name, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="557f7-144">Si la valeur que vous entrez dans le <strong> champ nom d’utilisateur ou de groupe d’accès en lecture seule </strong> de la <strong> page Configurer les bases de données </strong> est un nom de groupe, la valeur que vous entrez dans ce champ doit être membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="557f7-144">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group name, the value that you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="557f7-145">Configurez le mot de passe de ce compte pour qu’il n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="557f7-145">Configure the password for this account to never expire.</span></span> <span data-ttu-id="557f7-146">Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles pour le groupe utilisateurs de reports MBAM.</span><span class="sxs-lookup"><span data-stu-id="557f7-146">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a><span data-ttu-id="557f7-147">Site Web d’administration et de surveillance (support technique)</span><span class="sxs-lookup"><span data-stu-id="557f7-147">Administration and Monitoring Website (Help Desk) accounts</span></span>


<span data-ttu-id="557f7-148">Créez les comptes suivants pour le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="557f7-148">Create the following accounts for the Administration and Monitoring Website.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="557f7-149">Nom/objectif du compte</span><span class="sxs-lookup"><span data-stu-id="557f7-149">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="557f7-150">Type de compte</span><span class="sxs-lookup"><span data-stu-id="557f7-150">Account type</span></span></th>
<th align="left"><span data-ttu-id="557f7-151">Champ Assistant Configuration de MBAM Server qui correspond à ce compte</span><span class="sxs-lookup"><span data-stu-id="557f7-151">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="557f7-152">Description du champ de l’Assistant Configuration de MBAM Server qui correspond à ce compte.</span><span class="sxs-lookup"><span data-stu-id="557f7-152">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="557f7-153">Compte de domaine du pool d’applications de service Web</span><span class="sxs-lookup"><span data-stu-id="557f7-153">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-154">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="557f7-154">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-155">Compte de domaine du pool d’applications de service Web</span><span class="sxs-lookup"><span data-stu-id="557f7-155">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-156">Compte d’utilisateur de domaine devant être utilisé par le pool d’applications pour les applications Web.</span><span class="sxs-lookup"><span data-stu-id="557f7-156">Domain user account to be used by the application pool for the web applications.</span></span></p>
<p><span data-ttu-id="557f7-157">Si vous entrez un nom d’utilisateur dans le <strong> champ d’utilisateur ou de groupe de domaine d’accès en lecture/écriture </strong> sur la <strong> page configurer des bases de données </strong> , vous devez entrer cette même valeur dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="557f7-157">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="557f7-158">Si vous entrez un nom de groupe dans le <strong> champ User ou Group (lecture/écriture </strong> ) sur la <strong> page configure databases </strong> , la valeur que vous entrez dans ce champ doit être membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="557f7-158">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="557f7-159">Si vous ne spécifiez pas les informations d’identification, les informations d’identification spécifiées pour une application Web précédemment activée seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="557f7-159">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="557f7-160">Toutes les applications Web doivent utiliser les mêmes informations d’identification de pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="557f7-160">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="557f7-161">Si vous spécifiez des informations d’identification différentes pour différentes applications Web, la valeur la plus récemment spécifiée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="557f7-161">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="557f7-162">Important</span><span class="sxs-lookup"><span data-stu-id="557f7-162">Important</span></span></strong><br/><p><span data-ttu-id="557f7-163">Pour une sécurité améliorée, définissez le compte spécifié dans les informations d’identification pour disposer de droits d’utilisateur limités.</span><span class="sxs-lookup"><span data-stu-id="557f7-163">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="557f7-164">Groupe d’accès utilisateurs du support technique avancée MBAM</span><span class="sxs-lookup"><span data-stu-id="557f7-164">MBAM Advanced Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-165">Groupe</span><span class="sxs-lookup"><span data-stu-id="557f7-165">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-166">Utilisateurs du support technique avancée MBAM</span><span class="sxs-lookup"><span data-stu-id="557f7-166">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-167">Groupe d’utilisateurs de domaine dont les membres ont accès à toutes les zones de récupération du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="557f7-167">Domain user group whose members have access to all recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="557f7-168">Les utilisateurs disposant de ce rôle doivent entrer uniquement la clé de récupération, et non le domaine et le nom d’utilisateur de l’utilisateur final, pour aider les utilisateurs finaux à récupérer leurs lecteurs.</span><span class="sxs-lookup"><span data-stu-id="557f7-168">Users who have this role have to enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="557f7-169">Si un utilisateur est membre du groupe utilisateurs du support technique MBAM et du groupe utilisateurs du support technique avancée MBAM, les autorisations du groupe utilisateurs du support technique avancé MBAM remplacent les autorisations du groupe assistance technique MBAM.</span><span class="sxs-lookup"><span data-stu-id="557f7-169">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="557f7-170">Groupe d’accès utilisateurs du support MBAM</span><span class="sxs-lookup"><span data-stu-id="557f7-170">MBAM Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-171">Groupe</span><span class="sxs-lookup"><span data-stu-id="557f7-171">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-172">Utilisateurs du support technique MBAM</span><span class="sxs-lookup"><span data-stu-id="557f7-172">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-173">Groupe d’utilisateurs de domaine dont les membres ont accès aux zones gérer le module de plateforme sécurisée et de récupération des lecteurs du site Web d’administration et de contrôle MBAM.</span><span class="sxs-lookup"><span data-stu-id="557f7-173">Domain user group whose members have access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="557f7-174">Les personnes qui ont ce rôle doivent remplir tous les champs, y compris le nom de domaine et le nom du compte de l’utilisateur final, lorsqu’ils utilisent une option.</span><span class="sxs-lookup"><span data-stu-id="557f7-174">Individuals who have this role must fill-in all fields, including the end-user’s domain and account name, when they use either option.</span></span></p>
<p><span data-ttu-id="557f7-175">Si un utilisateur est membre du groupe utilisateurs du support technique MBAM et du groupe utilisateurs du support technique avancée MBAM, les autorisations du groupe utilisateurs du support technique avancé MBAM remplacent les autorisations du groupe assistance technique MBAM.</span><span class="sxs-lookup"><span data-stu-id="557f7-175">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="557f7-176">Groupe accéder aux utilisateurs du rapport MBAM</span><span class="sxs-lookup"><span data-stu-id="557f7-176">MBAM Report Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-177">Groupe</span><span class="sxs-lookup"><span data-stu-id="557f7-177">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-178">Utilisateurs de rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="557f7-178">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-179">Groupe d’utilisateurs de domaine dont les membres ont un accès en lecture seule aux rapports figurant dans la zone rapports du site Web Administration et analyse.</span><span class="sxs-lookup"><span data-stu-id="557f7-179">Domain user group whose members have read-only access to the reports in the Reports area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="557f7-180">Groupe d’utilisateurs de la migration des données MBAM</span><span class="sxs-lookup"><span data-stu-id="557f7-180">MBAM Data Migration User Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-181">Groupe</span><span class="sxs-lookup"><span data-stu-id="557f7-181">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-182">Utilisateurs de la migration des données MBAM</span><span class="sxs-lookup"><span data-stu-id="557f7-182">MBAM Data Migration Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="557f7-183">Groupe d’utilisateurs de domaine facultatif dont les membres ont l’autorisation d’écrire des données dans MBAM à l’aide du service de récupération et de matériel de MBAM exécuté sur le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="557f7-183">Optional domain user group whose members have permissions to write data to MBAM by using the MBAM Recovery and Hardware Service running on the MBAM server.</span></span> <span data-ttu-id="557f7-184">Ce compte est généralement utilisé avec les applets de contrôle Write-MBAM \* pour écrire des données de récupération et de TPM à partir d’Active Directory dans la base de données MBAM.</span><span class="sxs-lookup"><span data-stu-id="557f7-184">This account is generally used with the Write-Mbam\* cmdlets to write recovery and TPM data from Active Directory into the MBAM database.</span></span></p>
<p><span data-ttu-id="557f7-185">Pour plus d’informations, consultez <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considérations relatives à la sécurité de MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="557f7-185">For more information, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="557f7-186">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="557f7-186">Related topics</span></span>


[<span data-ttu-id="557f7-187">Préparation de votre environnement pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="557f7-187">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="557f7-188">Conditions préalables au déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="557f7-188">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)



## <span data-ttu-id="557f7-189">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="557f7-189">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="557f7-190">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="557f7-190">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="557f7-191">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="557f7-191">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 






---
title: Considérations relatives à la sécurité pour MBAM2.0
description: Considérations relatives à la sécurité pour MBAM2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810241"
---
# <span data-ttu-id="03566-103">Considérations relatives à la sécurité pour MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="03566-103">MBAM 2.0 Security Considerations</span></span>


<span data-ttu-id="03566-104">Cette rubrique fournit une vue d’ensemble sur les comptes et les groupes, les fichiers journaux et les autres considérations relatives à la sécurité relatives à l’administration et à la surveillance de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="03566-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="03566-105">Pour plus d’informations, suivez les liens fournis dans cet article.</span><span class="sxs-lookup"><span data-stu-id="03566-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="03566-106">Considérations générales en matière de sécurité</span><span class="sxs-lookup"><span data-stu-id="03566-106">General Security Considerations</span></span>


**<span data-ttu-id="03566-107">Comprenez les risques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="03566-107">Understand the security risks.</span></span>** <span data-ttu-id="03566-108">Le risque le plus sérieux découlant de l’administration et de la surveillance de BitLocker est que ses fonctionnalités peuvent être piratées par un utilisateur non autorisé qui peut ensuite reconfigurer le chiffrement BitLocker et obtenir les données de clé de chiffrement BitLocker sur les clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-108">The most serious risk from Microsoft BitLocker Administration and Monitoring is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="03566-109">Toutefois, en raison d’une attaque par déni de service, la perte de fonctionnalité MBAM n’a pas d’impact négatif, contrairement à la messagerie électronique, aux communications réseau, au faible potentiel et à l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="03566-109">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, e-mail, network communications, light, and power.</span></span>

<span data-ttu-id="03566-110">**Sécurisez vos ordinateurs de façon sécurisée**.</span><span class="sxs-lookup"><span data-stu-id="03566-110">**Physically secure your computers**.</span></span> <span data-ttu-id="03566-111">Il n’y a aucune sécurité sans sécurité physique.</span><span class="sxs-lookup"><span data-stu-id="03566-111">There is no security without physical security.</span></span> <span data-ttu-id="03566-112">Un attaquant qui obtient l’accès physique à un serveur MBAM peut peut-être l’utiliser pour attaquer la base de clients tout entière.</span><span class="sxs-lookup"><span data-stu-id="03566-112">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="03566-113">Toutes les attaques physiques potentielles doivent être considérées comme présentant un risque élevé et atténuées de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="03566-113">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="03566-114">Les serveurs MBAM doivent être stockés dans une salle serveur sécurisée avec un accès contrôlé.</span><span class="sxs-lookup"><span data-stu-id="03566-114">MBAM servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="03566-115">Sécurisez ces ordinateurs lorsque les administrateurs ne sont pas présents physiquement en faisant en sorte que le système d’exploitation verrouille l’ordinateur ou à l’aide d’un économiseur d’écran sécurisé.</span><span class="sxs-lookup"><span data-stu-id="03566-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="03566-116">**Appliquez les mises à jour de sécurité les plus récentes à tous les ordinateurs**.</span><span class="sxs-lookup"><span data-stu-id="03566-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="03566-117">Restez informé des nouvelles mises à jour de systèmes d’exploitation, de Microsoft SQL Server et de MBAM en vous abonnant au service de notification de sécurité ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="03566-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

<span data-ttu-id="03566-118">**Utiliser des mots de passe forts ou des expressions de passe**.</span><span class="sxs-lookup"><span data-stu-id="03566-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="03566-119">Utilisez toujours des mots de passe forts avec au moins 15 caractères pour tous les comptes d’administrateur MBAM et MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="03566-120">N’utilisez jamais de mots de passe vides.</span><span class="sxs-lookup"><span data-stu-id="03566-120">Never use blank passwords.</span></span> <span data-ttu-id="03566-121">Pour plus d’informations sur les concepts de mot de passe, consultez le livre blanc «mots de passe et stratégies de compte» sur TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="03566-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/?LinkId=30009>).</span></span>

## <span data-ttu-id="03566-122">Comptes et groupes dans MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="03566-123">La meilleure pratique pour gérer les comptes d’utilisateur consiste à créer des groupes globaux de domaine et à y ajouter des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="03566-123">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="03566-124">Ajoutez ensuite les comptes globaux Domain aux groupes locaux MBAM nécessaires sur les serveurs MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="03566-125">Groupes ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="03566-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="03566-126">Aucun groupe Active Directory n’est créé automatiquement lors du processus de configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-126">No Active Directory groups are created automatically during the MBAM setup process.</span></span> <span data-ttu-id="03566-127">Néanmoins, il est recommandé de créer les groupes globaux ActiveDirectoryDomainServices suivants pour gérer les opérations MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-127">However, it is recommended that you create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="03566-128">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="03566-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="03566-129">Détails</span><span class="sxs-lookup"><span data-stu-id="03566-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03566-130">Utilisateurs du support technique avancée MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-131">Créez ce groupe pour gérer les membres du groupe local du support technique MBAM avancée créé lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03566-132">Accès aux BD d’audit de conformité MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-133">Créer ce groupe pour gérer les membres du groupe local d’audit de compatibilité MBAM qui a été créé lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03566-134">Utilisateurs du support technique MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-134">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-135">Créez ce groupe pour gérer les membres du groupe local du support technique MBAM créés lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-135">Create this group to manage members of the MBAM Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03566-136">MBAM de récupération et de BDD matériel</span><span class="sxs-lookup"><span data-stu-id="03566-136">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-137">Créez ce groupe pour gérer les membres du groupe local de restauration MBAM et de la base de ressources matérielle pour l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-137">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03566-138">Utilisateurs de rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-138">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-139">Créez ce groupe pour gérer les membres du groupe d’utilisateurs de rapports MBAM créés lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-139">Create this group to manage members of the MBAM Report Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03566-140">Administrateurs système MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-140">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-141">Créez ce groupe pour gérer les membres du groupe local Administrateurs de systèmes MBAM créés lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-141">Create this group to manage members of the MBAM System Administrators local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03566-142">Exemptions de chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="03566-142">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-143">Créez ce groupe pour gérer les comptes d’utilisateurs qui doivent être exemptés du chiffrement BitLocker en commençant sur les ordinateurs sur lesquels ils se connectent.</span><span class="sxs-lookup"><span data-stu-id="03566-143">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> <span data-ttu-id="03566-144">Groupes locaux du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-144">MBAM Server Local Groups</span></span>

<span data-ttu-id="03566-145">Le programme d’installation d’MBAM crée des groupes locaux pour prendre en charge les opérations MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-145">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="03566-146">Vous devez ajouter les groupes globaux ActiveDirectoryDomainServices aux groupes locaux MBAM appropriés pour configurer les autorisations de sécurité et d’accès aux données MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-146">You should add the ActiveDirectoryDomainServices global groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="03566-147">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="03566-147">Group Name</span></span></th>
<th align="left"><span data-ttu-id="03566-148">Détails</span><span class="sxs-lookup"><span data-stu-id="03566-148">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03566-149">Utilisateurs du support technique avancée MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-149">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-150">Les membres de ce groupe ont un accès accru aux fonctionnalités du support technique de MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-150">Members of this group have increased access to the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03566-151">Accès aux BD d’audit de conformité MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-151">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-152">Contient les ordinateurs qui ont accès à la base de données de compatibilité et d’audit MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-152">Contains the machines that have access to the MBAM Compliance and Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03566-153">Utilisateurs du support technique MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-153">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-154">Les membres de ce groupe ont accès à certaines des fonctionnalités du support technique de MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-154">Members of this group have access to some of the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03566-155">MBAM de récupération et de BDD matériel</span><span class="sxs-lookup"><span data-stu-id="03566-155">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-156">Contient les ordinateurs qui ont accès à la base de données de récupération MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-156">Contains the machines that have access to the MBAM Recovery Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03566-157">Utilisateurs de rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-157">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-158">Les membres de ce groupe ont accès aux rapports de conformité et d’audit de MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-158">Members of this group have access to the Compliance and Audit reports from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03566-159">Administrateurs système MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-159">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="03566-160">Les membres de ce groupe ont accès à toutes les fonctionnalités de MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-160">Members of this group have access to all MBAM features.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="03566-161">Compte de service des rapports SSRS</span><span class="sxs-lookup"><span data-stu-id="03566-161">SSRS Reports Service Account</span></span>

<span data-ttu-id="03566-162">Le compte de service des rapports SSRS fournit le contexte de sécurité permettant d’exécuter les rapports MBAM disponibles via SSRS.</span><span class="sxs-lookup"><span data-stu-id="03566-162">The SSRS Reports service account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="03566-163">Il est configuré lors de la configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-163">It is configured during MBAM Setup.</span></span>

<span data-ttu-id="03566-164">Lorsque vous configurez le compte de service des rapports SSRS, spécifiez un compte d’utilisateur de domaine et configurez le mot de passe pour qu’il n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="03566-164">When you configure the SSRS Reports service account, specify a domain user account, and configure the password to never expire.</span></span>

<span data-ttu-id="03566-165">**Remarques**  Si vous modifiez le nom du compte de service après avoir déployé MBAM, vous devez reconfigurer la source de données de création de rapports pour utiliser les informations d’identification du compte de service.</span><span class="sxs-lookup"><span data-stu-id="03566-165">**Note** If you change the name of the service account after you deploy MBAM, you must reconfigure the reporting data source to use the new service account credentials.</span></span> <span data-ttu-id="03566-166">Dans le cas contraire, vous ne pourrez pas accéder au portail du support technique.</span><span class="sxs-lookup"><span data-stu-id="03566-166">Otherwise, you will not be able to access the Help Desk Portal.</span></span>

 

## <a href="" id="---------mbam-log-files"></a> <span data-ttu-id="03566-167">Fichiers journaux de MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-167">MBAM Log Files</span></span>


<span data-ttu-id="03566-168">Les fichiers journaux d’installation de MBAM suivants sont créés dans le dossier% Temp% de l’installation de l’utilisateur lors de l’installation d’MBAM:</span><span class="sxs-lookup"><span data-stu-id="03566-168">The following MBAM Setup log files are created in the installing user’s %temp% folder during MBAM Setup:</span></span>

**<span data-ttu-id="03566-169">Fichiers journaux de configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="03566-169">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="03566-170">Fichiers MSI de <em> &lt; cinq caractères aléatoires &gt; </em></span><span class="sxs-lookup"><span data-stu-id="03566-170">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="03566-171">Enregistre les actions effectuées lors de l’installation d’MBAM et de la fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="03566-171">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="03566-172">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="03566-172">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="03566-173">Consigne les actions effectuées pour créer la configuration de la base de données d’audit et de conformité MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-173">Logs actions taken to create the MBAM Compliance and Audit Database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="03566-174">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="03566-174">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="03566-175">Consigne les actions entreprises pour créer la base de données de récupération de MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-175">Logs actions taken to create the MBAM Recovery Database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="03566-176">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="03566-176">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="03566-177">Consigne les actions effectuées pour créer les connexions SQL Server sur la base de données de conformité et d’audit MBAM et autoriser le service Web d’assistance technique pour les rapports.</span><span class="sxs-lookup"><span data-stu-id="03566-177">Logs actions taken to create the SQL Server logins on the MBAM Compliance and Audit database and authorize the HelpDesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="03566-178">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="03566-178">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="03566-179">Consigne les actions d’autorisation d’accès aux services Web dans la base de données pour la récupération de clés et de création de connexion dans la base de données de récupération MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-179">Logs actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery Database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="03566-180">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="03566-180">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="03566-181">Consigne les actions entreprises pour autoriser les services Web à MBAM la conformité et l’audit de la base de données pour la création de rapports de conformité.</span><span class="sxs-lookup"><span data-stu-id="03566-181">Logs actions taken to authorize web services to MBAM Compliance and Audit Database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="03566-182">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="03566-182">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="03566-183">Consigne les actions entreprises pour autoriser les services Web dans la base de données de récupération MBAM pour la récupération de clé.</span><span class="sxs-lookup"><span data-stu-id="03566-183">Logs actions taken to authorize web services to the MBAM Recovery database for key recovery.</span></span>

<span data-ttu-id="03566-184">**Remarques**  Pour obtenir d’autres fichiers journaux d’installation d’MBAM, vous devez installer MBAM à l’aide du package msiexec et de &lt; l' &gt; option/l emplacement.</span><span class="sxs-lookup"><span data-stu-id="03566-184">**Note** In order to obtain additional MBAM Setup log files, you have to install MBAM by using the msiexec package and the /L &lt;location&gt; option.</span></span> <span data-ttu-id="03566-185">Les fichiers journaux sont créés à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="03566-185">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="03566-186">Fichiers journaux d’installation du client MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-186">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="03566-187">Fichiers MSI de <em> &lt; cinq caractères aléatoires &gt; </em></span><span class="sxs-lookup"><span data-stu-id="03566-187">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="03566-188">Enregistre les actions effectuées lors de l’installation du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-188">Logs the actions taken during MBAM Client installation.</span></span>

## <a href="" id="---------mbam-database-tde-considerations"></a> <span data-ttu-id="03566-189">Remarques sur les TDE de base de données MBAM</span><span class="sxs-lookup"><span data-stu-id="03566-189">MBAM Database TDE Considerations</span></span>


<span data-ttu-id="03566-190">La fonction de chiffrement de données (TDE) qui est disponible dans SQL Server est une installation facultative pour les instances de base de données qui hébergent les fonctionnalités de base de données MBAM.</span><span class="sxs-lookup"><span data-stu-id="03566-190">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="03566-191">Avec TDE, vous pouvez effectuer un chiffrement complet en temps réel au niveau de la base de données.</span><span class="sxs-lookup"><span data-stu-id="03566-191">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="03566-192">TDE est le choix le plus optimal pour le chiffrement en bloc pour répondre aux exigences de conformité aux réglementations ou à la sécurité des données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="03566-192">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="03566-193">TDE fonctionne au niveau fichier, qui est semblable à deux fonctionnalités Windows: le système de fichiers de chiffrement (EFS) et le chiffrement de lecteur BitLocker, qui chiffrent également les données sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="03566-193">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="03566-194">TDE ne remplace pas le chiffrement au niveau de la cellule, EFS ou BitLocker.</span><span class="sxs-lookup"><span data-stu-id="03566-194">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="03566-195">Lorsque TDE est activé sur une base de données, toutes les sauvegardes sont chiffrées.</span><span class="sxs-lookup"><span data-stu-id="03566-195">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="03566-196">Par conséquent, il est nécessaire de veiller à ce que le certificat utilisé pour protéger la clé de chiffrement de la base de données soit sauvegardé et entretenu par la sauvegarde de la base de données.</span><span class="sxs-lookup"><span data-stu-id="03566-196">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="03566-197">En cas de perte de ce (ou ces certificats), les données ne seront pas lisibles.</span><span class="sxs-lookup"><span data-stu-id="03566-197">If this certificate (or certificates) is lost, the data will be unreadable.</span></span> <span data-ttu-id="03566-198">Sauvegardez le certificat en même temps que la base de données.</span><span class="sxs-lookup"><span data-stu-id="03566-198">Back up the certificate along with the database.</span></span> <span data-ttu-id="03566-199">Chaque sauvegarde de certificat doit comporter deux fichiers.</span><span class="sxs-lookup"><span data-stu-id="03566-199">Each certificate backup should have two files.</span></span> <span data-ttu-id="03566-200">Ces deux fichiers doivent être archivés (idéalement dans le fichier de sauvegarde de la base de données).</span><span class="sxs-lookup"><span data-stu-id="03566-200">Both of these files should be archived (ideally separately from the database backup file for security).</span></span> <span data-ttu-id="03566-201">Vous pouvez également envisager d’utiliser la fonctionnalité de gestion des clés extensible (EKM) (voir gestion de clés extensible) pour stocker et gérer les clés utilisées pour TDE.</span><span class="sxs-lookup"><span data-stu-id="03566-201">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys used for TDE.</span></span>

<span data-ttu-id="03566-202">Pour obtenir un exemple de la façon d’activer TDE pour les instances de base de données MBAM, voir [évaluation d’MBAM 2,0](evaluating-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="03566-202">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 2.0](evaluating-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="03566-203">Pour plus d’informations sur TDE dans SQLServer 2008, voir [chiffrement SQL Server]( https://go.microsoft.com/fwlink/?LinkId=299883).</span><span class="sxs-lookup"><span data-stu-id="03566-203">For more information about TDE in SQLServer 2008, see [SQL Server Encryption]( https://go.microsoft.com/fwlink/?LinkId=299883).</span></span>

## <span data-ttu-id="03566-204">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03566-204">Related topics</span></span>


[<span data-ttu-id="03566-205">Sécurité et confidentialité de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="03566-205">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)

 

 






---
title: Considérations relatives à la sécurité pour MBAM1.0
description: Considérations relatives à la sécurité pour MBAM1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811609"
---
# <span data-ttu-id="b2ca1-103">Considérations relatives à la sécurité pour MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="b2ca1-103">Security Considerations for MBAM 1.0</span></span>


<span data-ttu-id="b2ca1-104">Cette rubrique fournit une vue d’ensemble des comptes et des groupes, des fichiers journaux et d’autres considérations relatives à la sécurité relatives à l’administration et à la surveillance de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="b2ca1-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="b2ca1-105">Pour plus d’informations, suivez les liens de cet article.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-105">For more information, follow the links in this article.</span></span>

## <span data-ttu-id="b2ca1-106">Considérations générales en matière de sécurité</span><span class="sxs-lookup"><span data-stu-id="b2ca1-106">General security considerations</span></span>


**<span data-ttu-id="b2ca1-107">Comprenez les risques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-107">Understand the security risks.</span></span>** <span data-ttu-id="b2ca1-108">Le risque le plus sérieux pour MBAM est qu’il peut être détourné par un utilisateur non autorisé qui peut ensuite reconfigurer le chiffrement BitLocker et obtenir les données de clé de chiffrement BitLocker sur les clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-108">The most serious risk to MBAM is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="b2ca1-109">Toutefois, la perte de fonctionnalités MBAM pendant une courte période à cause d’une attaque par déni de service n’a pas d’impact négatif.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-109">However, the loss of MBAM functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="b2ca1-110">**Sécurisez vos ordinateurs de façon sécurisée**.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-110">**Physically secure your computers**.</span></span> <span data-ttu-id="b2ca1-111">La sécurité est incomplète sans sécurité physique.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-111">Security is incomplete without physical security.</span></span> <span data-ttu-id="b2ca1-112">Toute personne disposant d’un accès physique à un serveur MBAM risque d’attaquer la base de clients entière.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-112">Anyone with physical access to an MBAM Server could potentially attack the entire client base.</span></span> <span data-ttu-id="b2ca1-113">Tout risque d’attaques physiques potentielles doit être considéré comme présentant un risque élevé et atténué de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-113">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="b2ca1-114">Les serveurs MBAM doivent être stockés dans une salle serveur sécurisée avec un accès contrôlé.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-114">MBAM servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="b2ca1-115">Sécurisez ces ordinateurs lorsque les administrateurs ne sont pas présents physiquement en faisant en sorte que le système d’exploitation verrouille l’ordinateur ou à l’aide d’un économiseur d’écran sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="b2ca1-116">**Appliquez les mises à jour de sécurité les plus récentes à tous les ordinateurs**.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="b2ca1-117">Restez informé des nouvelles mises à jour de systèmes d’exploitation, de Microsoft SQL Server et de MBAM en vous abonnant au service de notification de sécurité ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="b2ca1-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="b2ca1-118">**Utiliser des mots de passe forts ou des expressions de passe**.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="b2ca1-119">Utilisez toujours des mots de passe forts avec au moins 15 caractères pour tous les comptes d’administrateur MBAM et MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="b2ca1-120">N’utilisez jamais de mots de passe vides.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-120">Never use blank passwords.</span></span> <span data-ttu-id="b2ca1-121">Pour plus d’informations sur les concepts de mot de passe, consultez le livre blanc «mots de passe et stratégies de compte» sur TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="b2ca1-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="b2ca1-122">Comptes et groupes dans MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="b2ca1-123">Pour la gestion des comptes d’utilisateur, il est recommandé de créer des groupes globaux de domaine et d’y ajouter des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-123">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="b2ca1-124">Ajoutez ensuite les comptes globaux Domain aux groupes locaux MBAM nécessaires sur les serveurs MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="b2ca1-125">Groupes ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="b2ca1-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="b2ca1-126">Aucun groupe n’est créé automatiquement lors de la configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-126">No groups are created automatically during MBAM Setup.</span></span> <span data-ttu-id="b2ca1-127">Toutefois, vous devez créer les groupes globaux ActiveDirectoryDomainServices suivants pour gérer les opérations MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-127">However, you should create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b2ca1-128">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="b2ca1-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="b2ca1-129">Détails</span><span class="sxs-lookup"><span data-stu-id="b2ca1-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2ca1-130">Utilisateurs du support technique avancée MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-131">Créez ce groupe pour gérer les membres du groupe local de l’assistance technique avancée MBAM créé lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2ca1-132">Accès aux BD d’audit de conformité MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-133">Créez ce groupe pour gérer les membres du groupe local d’audit de compatibilité MBAM qui a été créé lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2ca1-134">Utilisateurs de matériel MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-134">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-135">Créez ce groupe pour gérer les membres du groupe local utilisateurs de matériel MBAM qui a été créé lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-135">Create this group to manage members of the MBAM Hardware Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2ca1-136">Utilisateurs du support technique MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-136">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-137">Créez ce groupe pour gérer les membres du groupe local du support technique MBAM créé lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-137">Create this group to manage members of the MBAM Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2ca1-138">MBAM de récupération et de BDD matériel</span><span class="sxs-lookup"><span data-stu-id="b2ca1-138">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-139">Créez ce groupe pour gérer les membres du groupe local de récupération MBAM et de la base de ressources matérielle pour la configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-139">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2ca1-140">Utilisateurs de rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-140">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-141">Créez ce groupe pour gérer les membres du groupe local utilisateurs de rapports MBAM créés lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-141">Create this group to manage members of the MBAM Report Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2ca1-142">Administrateurs système MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-142">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-143">Créez ce groupe pour gérer les membres du groupe local Administrateurs de systèmes MBAM qui a été créé lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-143">Create this group to manage members of the MBAM System Administrators local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2ca1-144">Exemptions de chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="b2ca1-144">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-145">Créez ce groupe pour gérer les comptes d’utilisateurs qui doivent être exemptés du chiffrement BitLocker en commençant sur les ordinateurs sur lesquels ils se connectent.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-145">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b2ca1-146">Groupes locaux du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-146">MBAM Server Local Groups</span></span>

<span data-ttu-id="b2ca1-147">Le programme d’installation d’MBAM crée des groupes locaux pour prendre en charge les opérations MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-147">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="b2ca1-148">Vous devez ajouter les groupes globaux ActiveDirectoryDomainServices aux groupes locaux MBAM appropriés pour configurer les autorisations de sécurité et d’accès aux données MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-148">You should add the ActiveDirectoryDomainServices Global Groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b2ca1-149">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="b2ca1-149">Group Name</span></span></th>
<th align="left"><span data-ttu-id="b2ca1-150">Détails</span><span class="sxs-lookup"><span data-stu-id="b2ca1-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2ca1-151">Utilisateurs du support technique avancée MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-151">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-152">Les membres de ce groupe ont étendu l’accès aux fonctionnalités de support technique de Microsoft BitLocker administration et de la surveillance.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-152">Members of this group have expanded access to the Helpdesk features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2ca1-153">Accès aux BD d’audit de conformité MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-153">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-154">Ce groupe contient les ordinateurs qui ont accès à la base de données d’audit de conformité MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-154">This group contains the machines that have access to the MBAM Compliance Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2ca1-155">Utilisateurs de matériel MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-155">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-156">Les membres de ce groupe ont accès à certaines des fonctionnalités de fonctionnalité matérielle de l’administration et de la surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-156">Members of this group have access to some of the Hardware Capability features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2ca1-157">Utilisateurs du support technique MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-157">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-158">Les membres de ce groupe ont accès à certaines des fonctionnalités de support technique de Microsoft BitLocker administration et de la surveillance.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-158">Members of this group have access to some of the Helpdesk features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2ca1-159">MBAM de récupération et de BDD matériel</span><span class="sxs-lookup"><span data-stu-id="b2ca1-159">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-160">Ce groupe contient les ordinateurs qui ont accès à la base de données MBAM et de récupération de la base de données matérielle.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-160">This group contains the computers that have access to the MBAM Recovery and Hardware Database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2ca1-161">Utilisateurs de rapports MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-161">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-162">Les membres de ce groupe ont accès aux rapports de conformité et d’audit de Microsoft BitLocker administration et de la surveillance.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-162">Members of this group have access to the Compliance and Audit reports from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2ca1-163">Administrateurs système MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-163">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2ca1-164">Les membres de ce groupe ont accès à toutes les fonctionnalités d’administration et de surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-164">Members of this group have access to all the features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b2ca1-165">Compte d’accès aux rapports SSRS</span><span class="sxs-lookup"><span data-stu-id="b2ca1-165">SSRS Reports Access Account</span></span>

<span data-ttu-id="b2ca1-166">Le compte de service des rapports SQL Server Reporting Services (SSRS) fournit le contexte de sécurité permettant d’exécuter les rapports MBAM disponibles via SSRS.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-166">The SQL Server Reporting Services (SSRS) Reports Service Account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="b2ca1-167">Ce compte est configuré dans le cadre de la configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-167">This account is configured during MBAM Setup.</span></span>

## <span data-ttu-id="b2ca1-168">Fichiers journaux de MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-168">MBAM Log Files</span></span>


<span data-ttu-id="b2ca1-169">Lors de l’installation d’MBAM, les fichiers journaux d’installation de MBAM suivants sont créés dans le dossier% Temp% de l’utilisateur qui installe le</span><span class="sxs-lookup"><span data-stu-id="b2ca1-169">During MBAM Setup, the following MBAM Setup log files are created in the %temp% folder of the user who installs the</span></span>

**<span data-ttu-id="b2ca1-170">Fichiers journaux de configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="b2ca1-170">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="b2ca1-171">Fichiers MSI de <em> &lt; cinq caractères aléatoires &gt; </em></span><span class="sxs-lookup"><span data-stu-id="b2ca1-171">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="b2ca1-172">Enregistre les actions effectuées lors de l’installation d’MBAM et de la fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-172">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="b2ca1-173">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="b2ca1-173">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="b2ca1-174">Consigne les actions effectuées pour créer la configuration de la base de données d’état de conformité MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-174">Logs the actions taken to create the MBAM Compliance Status database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="b2ca1-175">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="b2ca1-175">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="b2ca1-176">Consigne les actions entreprises pour créer la base de données de récupération et de MBAM de données matérielle.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-176">Logs the actions taken to create the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="b2ca1-177">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="b2ca1-177">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="b2ca1-178">Consigne les actions effectuées pour créer les connexions SQL Server sur la base de données d’état de conformité d’MBAM et autoriser le service Web d’assistance technique pour les rapports.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-178">Logs the actions taken to create the SQL Server logins on the MBAM Compliance Status database and authorize helpdesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="b2ca1-179">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="b2ca1-179">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="b2ca1-180">Consigne les actions entreprises pour autoriser les services Web dans la base de données pour la récupération de clés et créer des connexions sur la base de données de récupération et de matériel MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-180">Logs the actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="b2ca1-181">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="b2ca1-181">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="b2ca1-182">Consigne les actions entreprises pour autoriser les services Web à MBAM la base de données d’état de conformité pour le rapport de conformité.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-182">Logs the actions taken to authorize web services to MBAM Compliance Status database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="b2ca1-183">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="b2ca1-183">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="b2ca1-184">Consigne les actions entreprises pour autoriser les services Web à MBAM la restauration de la clé matérielle et de la base de données matérielle.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-184">Logs the actions taken to authorize web services to MBAM Recovery and Hardware database for key recovery.</span></span>

<span data-ttu-id="b2ca1-185">**Remarques**  Pour obtenir d’autres fichiers journaux d’installation d’MBAM, vous devez installer l’administration et la surveillance de BitLocker en utilisant le package **msiexec** et l’option **/l** &lt; emplacement &gt; .</span><span class="sxs-lookup"><span data-stu-id="b2ca1-185">**Note** In order to obtain additional MBAM Setup log files, you must install Microsoft BitLocker Administration and Monitoring by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="b2ca1-186">Les fichiers journaux sont créés à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-186">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="b2ca1-187">Fichiers journaux d’installation du client MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-187">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="b2ca1-188">Fichiers MSI de <em> &lt; cinq caractères aléatoires &gt; </em></span><span class="sxs-lookup"><span data-stu-id="b2ca1-188">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="b2ca1-189">Enregistre les actions effectuées lors de l’installation du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-189">Logs the actions taken during MBAM Client installation.</span></span>

## <span data-ttu-id="b2ca1-190">Remarques sur les TDE de base de données MBAM</span><span class="sxs-lookup"><span data-stu-id="b2ca1-190">MBAM Database TDE considerations</span></span>


<span data-ttu-id="b2ca1-191">La fonctionnalité de chiffrement de données transparente (TDE) disponible dans SQL Server 2008 est une condition requise d’installation requise pour les instances de base de données qui hébergent les fonctionnalités de base de données MBAM.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-191">The Transparent Data Encryption (TDE) feature available in SQL Server 2008 is a required installation prerequisite for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="b2ca1-192">Avec TDE, vous pouvez effectuer un chiffrement complet en temps réel au niveau de la base de données.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-192">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="b2ca1-193">TDE est un choix idéal pour le chiffrement en bloc pour répondre aux exigences réglementaires ou à la sécurité des données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-193">TDE is a well-suited choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="b2ca1-194">TDE fonctionne au niveau fichier, qui est semblable à deux fonctionnalités Windows: le système de fichiers de chiffrement (EFS) et le chiffrement de lecteur BitLocker, qui chiffrent également les données sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-194">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="b2ca1-195">TDE ne remplace pas le chiffrement au niveau de la cellule, EFS ou BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-195">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="b2ca1-196">Lorsque TDE est activé sur une base de données, toutes les sauvegardes sont chiffrées.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-196">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="b2ca1-197">Par conséquent, il est nécessaire de veiller à ce que le certificat utilisé pour protéger la clé de chiffrement de la base de données (DEK) soit sauvegardé et entretenu par la sauvegarde de la base de données.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-197">Thus, special care must be taken to ensure that the certificate that was used to protect the Database Encryption Key (DEK) is backed up and maintained with the database backup.</span></span> <span data-ttu-id="b2ca1-198">Sans certificat, les données ne seront pas lisibles.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-198">Without a certificate, the data will be unreadable.</span></span> <span data-ttu-id="b2ca1-199">Sauvegardez le certificat en même temps que la base de données.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-199">Back up the certificate along with the database.</span></span> <span data-ttu-id="b2ca1-200">Chaque sauvegarde de certificat doit comporter deux fichiers. ces deux fichiers doivent être archivés. Il est préférable de les archiver indépendamment du fichier de sauvegarde de base de données à des fins de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b2ca1-200">Each certificate backup should have two files; both of these files should be archived .It is best to archive them separately from the database backup file for security.</span></span>

<span data-ttu-id="b2ca1-201">Pour obtenir un exemple de la façon d’activer TDE pour les instances de base de données MBAM, voir [évaluation d’MBAM 1,0](evaluating-mbam-10.md).</span><span class="sxs-lookup"><span data-stu-id="b2ca1-201">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 1.0](evaluating-mbam-10.md).</span></span>

<span data-ttu-id="b2ca1-202">Pour plus d’informations sur TDE dans SQLServer 2008, voir [chiffrement de base de données dans SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span><span class="sxs-lookup"><span data-stu-id="b2ca1-202">For more information about TDE in SQLServer 2008, see [Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span></span>

## <span data-ttu-id="b2ca1-203">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2ca1-203">Related topics</span></span>


[<span data-ttu-id="b2ca1-204">Sécurité et confidentialité de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="b2ca1-204">Security and Privacy for MBAM 1.0</span></span>](security-and-privacy-for-mbam-10.md)

 

 






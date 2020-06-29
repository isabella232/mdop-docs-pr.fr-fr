---
title: Considérations sur la sécurité d'App-V5.0
description: Considérations sur la sécurité d'App-V5.0
author: dansimp
ms.assetid: 1e7292a0-7972-4b4f-85a9-eaf33f6c563a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fcd740345be7f532502b8996d8d2b1f4437ed6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806006"
---
# <span data-ttu-id="c4c46-103">Considérations sur la sécurité d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="c4c46-103">App-V 5.0 Security Considerations</span></span>


<span data-ttu-id="c4c46-104">Cette rubrique fournit une vue d’ensemble des comptes et des groupes, des fichiers journaux et d’autres considérations relatives à la sécurité pour App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for App-V 5.0.</span></span>

**<span data-ttu-id="c4c46-105">Important</span><span class="sxs-lookup"><span data-stu-id="c4c46-105">Important</span></span>**  
<span data-ttu-id="c4c46-106">App-V 5,0 n’est pas un produit de sécurité et ne fournit aucune garantie pour un environnement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="c4c46-106">App-V 5.0 is not a security product and does not provide any guarantees for a secure environment.</span></span>



## <span data-ttu-id="c4c46-107">La fonctionnalité PackageStoreAccessControl (PSAC) est déconseillée</span><span class="sxs-lookup"><span data-stu-id="c4c46-107">PackageStoreAccessControl (PSAC) feature has been deprecated</span></span>


<span data-ttu-id="c4c46-108">À compter de juin, 2014, PackageStoreAccessControl (PSAC), incluse dans Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2), a été déconseillée dans les environnements à utilisateurs unique et à plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c4c46-108">Effective as of June, 2014, the PackageStoreAccessControl (PSAC) feature that was introduced in Microsoft Application Virtualization (App-V) 5.0 Service Pack 2 (SP2) has been deprecated in both single-user and multi-user environments.</span></span>

## <span data-ttu-id="c4c46-109">Considérations générales en matière de sécurité</span><span class="sxs-lookup"><span data-stu-id="c4c46-109">General security considerations</span></span>


**<span data-ttu-id="c4c46-110">Comprenez les risques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c4c46-110">Understand the security risks.</span></span>** <span data-ttu-id="c4c46-111">Le risque le plus sérieux pour App-V 5,0 est qu’il peut être détourné par un utilisateur non autorisé qui peut ensuite reconfigurer des données clés sur des clients App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-111">The most serious risk to App-V 5.0 is that its functionality could be hijacked by an unauthorized user who could then reconfigure key data on App-V 5.0 clients.</span></span> <span data-ttu-id="c4c46-112">La perte de fonctionnalité de l’application 5,0 App-V pour une courte période à cause d’une attaque par déni de service n’a généralement pas d’impact sur la catastrophe.</span><span class="sxs-lookup"><span data-stu-id="c4c46-112">The loss of App-V 5.0 functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="c4c46-113">**Sécurisez vos ordinateurs de façon sécurisée**.</span><span class="sxs-lookup"><span data-stu-id="c4c46-113">**Physically secure your computers**.</span></span> <span data-ttu-id="c4c46-114">La sécurité est incomplète sans sécurité physique.</span><span class="sxs-lookup"><span data-stu-id="c4c46-114">Security is incomplete without physical security.</span></span> <span data-ttu-id="c4c46-115">Toute personne disposant d’un accès physique à un serveur App-V 5,0 peut éventuellement attaquer la base de clients entière.</span><span class="sxs-lookup"><span data-stu-id="c4c46-115">Anyone with physical access to an App-V 5.0 server could potentially attack the entire client base.</span></span> <span data-ttu-id="c4c46-116">Tout risque d’attaques physiques potentielles doit être considéré comme présentant un risque élevé et atténué de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="c4c46-116">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="c4c46-117">Les serveurs App-V 5,0 doivent être stockés dans une salle serveur sécurisée avec accès contrôlé.</span><span class="sxs-lookup"><span data-stu-id="c4c46-117">App-V 5.0 servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="c4c46-118">Sécurisez ces ordinateurs lorsque les administrateurs ne sont pas présents physiquement en faisant en sorte que le système d’exploitation verrouille l’ordinateur ou à l’aide d’un économiseur d’écran sécurisé.</span><span class="sxs-lookup"><span data-stu-id="c4c46-118">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="c4c46-119">**Appliquez les mises à jour de sécurité les plus récentes à tous les ordinateurs**.</span><span class="sxs-lookup"><span data-stu-id="c4c46-119">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="c4c46-120">Pour vous tenir informé des dernières mises à jour pour les systèmes d’exploitation, Microsoft SQL Server et App-V 5,0, abonnez-vous au service de notification de sécurité ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="c4c46-120">To stay informed about the latest updates for operating systems, Microsoft SQL Server, and App-V 5.0, subscribe to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="c4c46-121">**Utiliser des mots de passe forts ou des expressions de passe**.</span><span class="sxs-lookup"><span data-stu-id="c4c46-121">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="c4c46-122">Utilisez toujours des mots de passe forts avec au moins 15 caractères pour tous les comptes d’administrateur App-V 5,0 et App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-122">Always use strong passwords with 15 or more characters for all App-V 5.0 and App-V 5.0 administrator accounts.</span></span> <span data-ttu-id="c4c46-123">N’utilisez jamais de mots de passe vides.</span><span class="sxs-lookup"><span data-stu-id="c4c46-123">Never use blank passwords.</span></span> <span data-ttu-id="c4c46-124">Pour plus d’informations sur les concepts de mot de passe, consultez le livre blanc «mots de passe et stratégies de compte» sur TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="c4c46-124">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="c4c46-125">Comptes et groupes dans App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c4c46-125">Accounts and groups in App-V 5.0</span></span>


<span data-ttu-id="c4c46-126">Pour la gestion des comptes d’utilisateur, il est recommandé de créer des groupes globaux de domaine et d’y ajouter des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c4c46-126">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="c4c46-127">Ensuite, ajoutez les comptes globaux Domain aux groupes locaux App-V 5,0 nécessaires sur les serveurs App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-127">Then, add the domain global accounts to the necessary App-V 5.0 local groups on the App-V 5.0 servers.</span></span>

**<span data-ttu-id="c4c46-128">Remarque</span><span class="sxs-lookup"><span data-stu-id="c4c46-128">Note</span></span>**  
<span data-ttu-id="c4c46-129">Les comptes d’ordinateur client App-V qui doivent se connecter au serveur de publication doivent faire partie du groupe local **utilisateurs** du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="c4c46-129">App-V client computer accounts that need to connect to the publishing server must be part of the publishing server’s **Users** local group.</span></span> <span data-ttu-id="c4c46-130">Par défaut, tous les ordinateurs du domaine font partie du groupe **utilisateurs autorisés** , qui fait partie du groupe local **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="c4c46-130">By default, all computers in the domain are part of the **Authorized Users** group, which is part of the **Users** local group.</span></span>



### <a href="" id="-------------app-v-5-0-server-security"></a> <span data-ttu-id="c4c46-131">Sécurité du serveur App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c4c46-131">App-V 5.0 server security</span></span>

<span data-ttu-id="c4c46-132">Aucun groupe n’est créé automatiquement lors de la configuration de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-132">No groups are created automatically during App-V 5.0 Setup.</span></span> <span data-ttu-id="c4c46-133">Il est recommandé de créer les groupes globaux services de domaine Active Directory suivants pour gérer les opérations du serveur App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-133">You should create the following Active Directory Domain Services global groups to manage App-V 5.0 server operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c4c46-134">Nom du groupe</span><span class="sxs-lookup"><span data-stu-id="c4c46-134">Group name</span></span></th>
<th align="left"><span data-ttu-id="c4c46-135">Détails</span><span class="sxs-lookup"><span data-stu-id="c4c46-135">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c46-136">Groupe d’administration de l’application-V</span><span class="sxs-lookup"><span data-stu-id="c4c46-136">App-V Management Admin group</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c46-137">Utilisé pour gérer le serveur de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-137">Used to manage the App-V 5.0 management server.</span></span> <span data-ttu-id="c4c46-138">Ce groupe est créé pendant l’installation de l’application-V 5,0 Management Server.</span><span class="sxs-lookup"><span data-stu-id="c4c46-138">This group is created during the App-V 5.0 Management Server installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c4c46-139">Important</span><span class="sxs-lookup"><span data-stu-id="c4c46-139">Important</span></span></strong><br/><p><span data-ttu-id="c4c46-140">Il n’existe aucune méthode de création du groupe à l’aide de la console de gestion une fois l’installation terminée.</span><span class="sxs-lookup"><span data-stu-id="c4c46-140">There is no method to create the group using the management console after you have completed the installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4c46-141">Lecture/écriture de base de données pour le compte de service de gestion</span><span class="sxs-lookup"><span data-stu-id="c4c46-141">Database read/write for Management Service account</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c46-142">Fournit un accès en lecture/écriture à la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="c4c46-142">Provides read/write access to the management database.</span></span> <span data-ttu-id="c4c46-143">Ce compte doit être créé lors de l’installation de la base de données de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-143">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c46-144">Compte d’administrateur d’installation du service d’application-V</span><span class="sxs-lookup"><span data-stu-id="c4c46-144">App-V Management Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c4c46-145">Remarque</span><span class="sxs-lookup"><span data-stu-id="c4c46-145">Note</span></span></strong><br/><p><span data-ttu-id="c4c46-146">Ceci est requis uniquement si la base de données de gestion est installée séparément du service.</span><span class="sxs-lookup"><span data-stu-id="c4c46-146">This is only required if management database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c4c46-147">Fournit un accès public à la table de version de schéma dans la base de données de gestion.</span><span class="sxs-lookup"><span data-stu-id="c4c46-147">Provides public access to schema-version table in management database.</span></span> <span data-ttu-id="c4c46-148">Ce compte doit être créé lors de l’installation de la base de données de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-148">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4c46-149">Compte d’administrateur d’installation du service de création de rapports App-V</span><span class="sxs-lookup"><span data-stu-id="c4c46-149">App-V Reporting Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c4c46-150">Remarque</span><span class="sxs-lookup"><span data-stu-id="c4c46-150">Note</span></span></strong><br/><p><span data-ttu-id="c4c46-151">Ceci est requis uniquement si la base de données de création de rapports est installée séparément du service.</span><span class="sxs-lookup"><span data-stu-id="c4c46-151">This is only required if reporting database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c4c46-152">Accès public à la table Schema-Version dans la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="c4c46-152">Public access to schema-version table in reporting database.</span></span> <span data-ttu-id="c4c46-153">Ce compte doit être créé lors de l’installation de la base de données de création de rapports App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c4c46-153">This account should be created during the App-V 5.0 reporting database installation.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="c4c46-154">Prenez en compte les informations supplémentaires suivantes:</span><span class="sxs-lookup"><span data-stu-id="c4c46-154">Consider the following additional information:</span></span>

-   <span data-ttu-id="c4c46-155">Accès aux partages du package: s’il existe un partage sur le même ordinateur que le serveur de gestion, le service **réseau** doit avoir accès en lecture au partage.</span><span class="sxs-lookup"><span data-stu-id="c4c46-155">Access to the package shares - If a share exists on the same computer as the management Server, the **Network** service requires read access to the share.</span></span> <span data-ttu-id="c4c46-156">Par ailleurs, chaque ordinateur client App-V doit avoir accès en lecture au partage de package.</span><span class="sxs-lookup"><span data-stu-id="c4c46-156">In addition, each App-V client computer must have read access to the package share.</span></span>

    **<span data-ttu-id="c4c46-157">Remarque</span><span class="sxs-lookup"><span data-stu-id="c4c46-157">Note</span></span>**  
    <span data-ttu-id="c4c46-158">Dans les versions précédentes de App-V, le partage de package était appelé partage de contenu.</span><span class="sxs-lookup"><span data-stu-id="c4c46-158">In previous versions of App-V, package share was referred to as content share.</span></span>



-   <span data-ttu-id="c4c46-159">Inscription des serveurs de publication auprès du serveur de gestion: un serveur de publication doit être enregistré auprès du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="c4c46-159">Registering publishing servers with Management Server - A publishing server must be registered with the Management server.</span></span> <span data-ttu-id="c4c46-160">Par exemple, il doit être ajouté à la base de données, de sorte que les comptes d’ordinateur du serveur de publication puissent appeler l’API du service de gestion.</span><span class="sxs-lookup"><span data-stu-id="c4c46-160">For example, it must be added to the database, so that the Publishing server machine accounts are able to call into the Management service API.</span></span>

### <a href="" id="-------------app-v-5-0-package-security"></a> <span data-ttu-id="c4c46-161">Sécurité du package App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c4c46-161">App-V 5.0 package security</span></span>

<span data-ttu-id="c4c46-162">Vous trouverez ci-après des informations sur la façon de garantir la sécurité des packages virtualisés.</span><span class="sxs-lookup"><span data-stu-id="c4c46-162">The following will help you plan how to ensure that virtualized packages are secure.</span></span>

-   <span data-ttu-id="c4c46-163">Si un programme d’installation d’application applique une liste de contrôle d’accès (ACL) à un fichier ou un répertoire, il n’est pas conservé dans le package.</span><span class="sxs-lookup"><span data-stu-id="c4c46-163">If an application installer applies an access control list (ACL) to a file or directory, then that ACL is not persisted in the package.</span></span> <span data-ttu-id="c4c46-164">Lorsque le package est déployé, si le fichier ou le répertoire est modifié par un utilisateur, il héritera de l’ACL dans le **% UserProfile%** ou héritera de la liste de contrôle d’accès de l’annuaire de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="c4c46-164">When the package is deployed, if the file or directory is modified by a user it will either inherit the ACL in the **%userprofile%** or inherit the ACL of the target computer’s directory.</span></span> <span data-ttu-id="c4c46-165">Le premier cas se produit si le fichier ou le répertoire n’existe pas dans l’emplacement du système de fichiers virtuel; ce dernier cas se produit si le fichier ou répertoire existe dans l’emplacement du système de fichiers virtuel, par exemple **% windir%**.</span><span class="sxs-lookup"><span data-stu-id="c4c46-165">The former case occurs if the file or directory does not exist in a virtual file system location; the latter case occurs if the file or directory exists in a virtual file system location, for example **%windir%**.</span></span>

## <a href="" id="---------app-v-5-0-log-files"></a> <span data-ttu-id="c4c46-166">Fichiers journaux App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c4c46-166">App-V 5.0 log files</span></span>


<span data-ttu-id="c4c46-167">Lors de l’installation d’App-V 5,0, les fichiers journaux d’installation sont créés dans le dossier **% temp%** de l’utilisateur qui a installé l’application.</span><span class="sxs-lookup"><span data-stu-id="c4c46-167">During App-V 5.0 Setup, setup log files are created in the **%temp%** folder of the installing user.</span></span>

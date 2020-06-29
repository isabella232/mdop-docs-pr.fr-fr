---
title: Déléguer l'accès à l'environnement de production
description: Déléguer l'accès à l'environnement de production
author: dansimp
ms.assetid: 4c670581-8c47-41ea-80eb-02846ff1ec1f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a3920a8ba5835cbbcb8a74f0af4e3ca1e1c5f43f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807622"
---
# <span data-ttu-id="56d27-103">Déléguer l'accès à l'environnement de production</span><span class="sxs-lookup"><span data-stu-id="56d27-103">Delegate Access to the Production Environment</span></span>


<span data-ttu-id="56d27-104">Dans Advanced Group Policy Management (AGPM), vous pouvez modifier l’accès aux objets de stratégie de groupe dans l’environnement de production du domaine, en remplaçant les autorisations existantes sur ces objets.</span><span class="sxs-lookup"><span data-stu-id="56d27-104">In Advanced Group Policy Management (AGPM), you can change access to Group Policy Objects (GPOs) in the production environment of the domain, replacing any existing permissions on those GPOs.</span></span> <span data-ttu-id="56d27-105">Vous pouvez configurer des autorisations au niveau du domaine pour autoriser ou empêcher les utilisateurs de modifier, de supprimer ou de modifier la sécurité des objets de stratégie de groupe dans l’environnement de production quand ils n’utilisent pas le dossier de **contrôle de modification** dans la console de gestion des stratégies de groupe (GPMC).</span><span class="sxs-lookup"><span data-stu-id="56d27-105">You can configure permissions at the domain level to either allow or prevent users from editing, deleting, or modifying the security of GPOs in the production environment when they are not using the **Change Control** folder in the Group Policy Management Console (GPMC).</span></span>

**<span data-ttu-id="56d27-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="56d27-106">Note</span></span>**  
-   <span data-ttu-id="56d27-107">La modification de la façon dont l’accès à l’environnement de production est délégué n’a pas d’incidence sur la possibilité de lier les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="56d27-107">Changing how access to the production environment is delegated does not affect users' ability to link GPOs.</span></span>

-   <span data-ttu-id="56d27-108">Lorsque des objets de stratégie de groupe sont contrôlés ou déployés, l’accès pour tous les autres comptes, à l’exception de ceux portant les autorisations **lecture** et **appliquer** est supprimé</span><span class="sxs-lookup"><span data-stu-id="56d27-108">When GPOs are controlled or deployed, access for any other accounts except those with **Read** and **Apply** permissions is removed.</span></span>

 

<span data-ttu-id="56d27-109">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="56d27-109">A user account that has either the role of AGPM Administrator (Full Control) or the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="56d27-110">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="56d27-110">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="56d27-111">Pour modifier l’accès aux objets de stratégie de groupe dans l’environnement de production du domaine</span><span class="sxs-lookup"><span data-stu-id="56d27-111">To change access to GPOs in the production environment of the domain</span></span>**

1.  <span data-ttu-id="56d27-112">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="56d27-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="56d27-113">Cliquez sur l’onglet **délégation de production** .</span><span class="sxs-lookup"><span data-stu-id="56d27-113">Click the **Production Delegation** tab.</span></span>

3.  <span data-ttu-id="56d27-114">Pour ajouter des autorisations pour un utilisateur ou un groupe qui n’ont pas accès à l’environnement de production, ou pour remplacer les autorisations d’un utilisateur ou d’un groupe qui a accès:</span><span class="sxs-lookup"><span data-stu-id="56d27-114">To add permissions for a user or group that does not have access to the production environment, or to replace the permissions for a user or group that does have access:</span></span>

    1.  <span data-ttu-id="56d27-115">Cliquez sur **Ajouter**, sélectionnez un utilisateur ou un groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="56d27-115">Click **Add**, select a user or group, and then click **OK**.</span></span>

    2.  <span data-ttu-id="56d27-116">Sélectionnez les autorisations à déléguer à un utilisateur ou à un groupe pour l’environnement de production, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="56d27-116">Select permissions to delegate to that user or group for the production environment, and then click **OK**.</span></span>

4.  <span data-ttu-id="56d27-117">Pour supprimer toutes les autorisations de l’environnement de production pour un utilisateur ou un groupe, sélectionnez l’utilisateur ou le groupe, cliquez sur **supprimer**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="56d27-117">To remove all permissions to the production environment for a user or group, select the user or group, click **Remove**, and then click **OK**.</span></span>

### <span data-ttu-id="56d27-118">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="56d27-118">Additional considerations</span></span>

-   <span data-ttu-id="56d27-119">Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="56d27-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="56d27-120">Plus précisément, vous devez disposer des autorisations de modification de la **sécurité** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="56d27-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="56d27-121">Les autorisations pour le compte de service AGPM ne peuvent pas être modifiées sous l’onglet **délégation de production** .</span><span class="sxs-lookup"><span data-stu-id="56d27-121">Permissions for the AGPM Service Account cannot be changed on the **Production Delegation** tab.</span></span>

-   <span data-ttu-id="56d27-122">Par défaut, les comptes suivants possèdent des autorisations pour les objets de stratégie de groupe dans l’environnement de production:</span><span class="sxs-lookup"><span data-stu-id="56d27-122">By default, the following accounts have permissions for GPOs in the production environment:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="56d27-123">Compte</span><span class="sxs-lookup"><span data-stu-id="56d27-123">Account</span></span></th>
    <th align="left"><span data-ttu-id="56d27-124">Autorisations par défaut pour les objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="56d27-124">Default Permissions for GPOs</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="56d27-125">&lt;Compte de service AGPM&gt;</span><span class="sxs-lookup"><span data-stu-id="56d27-125">&lt;AGPM Service Account&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="56d27-126">Modifier les paramètres, supprimer ou modifier la sécurité</span><span class="sxs-lookup"><span data-stu-id="56d27-126">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="56d27-127">Utilisateurs authentifiés</span><span class="sxs-lookup"><span data-stu-id="56d27-127">Authenticated Users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="56d27-128">Lire, appliquer</span><span class="sxs-lookup"><span data-stu-id="56d27-128">Read, Apply</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="56d27-129">Administrateurs de domaine</span><span class="sxs-lookup"><span data-stu-id="56d27-129">Domain Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="56d27-130">Modifier les paramètres, supprimer ou modifier la sécurité</span><span class="sxs-lookup"><span data-stu-id="56d27-130">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="56d27-131">Administrateurs d’entreprise</span><span class="sxs-lookup"><span data-stu-id="56d27-131">Enterprise Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="56d27-132">Modifier les paramètres, supprimer ou modifier la sécurité</span><span class="sxs-lookup"><span data-stu-id="56d27-132">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="56d27-133">Contrôleurs de domaine d’entreprise</span><span class="sxs-lookup"><span data-stu-id="56d27-133">Enterprise Domain Controllers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="56d27-134">Read</span><span class="sxs-lookup"><span data-stu-id="56d27-134">Read</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="56d27-135">Système</span><span class="sxs-lookup"><span data-stu-id="56d27-135">System</span></span></p></td>
    <td align="left"><p><span data-ttu-id="56d27-136">Modifier les paramètres, supprimer ou modifier la sécurité</span><span class="sxs-lookup"><span data-stu-id="56d27-136">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="56d27-137">L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte, soit n’est pas utilisé pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="56d27-137">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="56d27-138">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="56d27-138">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="56d27-139">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="56d27-139">Additional references</span></span>

-   [<span data-ttu-id="56d27-140">Configuration de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="56d27-140">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 






---
title: Déléguer l'accès à un objet de stratégie de groupe individuel
description: Déléguer l'accès à un objet de stratégie de groupe individuel
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807625"
---
# <span data-ttu-id="4eccc-103">Déléguer l'accès à un objet de stratégie de groupe individuel</span><span class="sxs-lookup"><span data-stu-id="4eccc-103">Delegate Access to an Individual GPO</span></span>


<span data-ttu-id="4eccc-104">En tant qu’administrateur d’AGPM (contrôle total), vous pouvez déléguer la gestion d’un objet de stratégie de groupe contrôlé (GPO), de sorte que les groupes et les éditeurs sélectionnés puissent le modifier, les réviseurs peuvent le réviser et les approbateurs peuvent l’approuver.</span><span class="sxs-lookup"><span data-stu-id="4eccc-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy object (GPO), so selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="4eccc-105">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe ou un compte d’utilisateur disposant des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="4eccc-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="4eccc-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4eccc-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="4eccc-107">Pour déléguer la gestion d’un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="4eccc-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="4eccc-108">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4eccc-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="4eccc-109">Dans l’onglet **Sommaire** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés, puis cliquez sur l’objet de stratégie de groupe à déléguer.</span><span class="sxs-lookup"><span data-stu-id="4eccc-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="4eccc-110">Cliquez sur le bouton **Ajouter** , sélectionnez les utilisateurs ou les groupes auxquels vous avez accès autorisé, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4eccc-110">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="4eccc-111">Pour personnaliser les autorisations pour chaque utilisateur ou groupe, cliquez sur le bouton **avancé** sous l’onglet **Sommaire** et activez les cases à cocher autorisations de rôle pour autoriser ou refuser.</span><span class="sxs-lookup"><span data-stu-id="4eccc-111">To customize the permissions for each user or group, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="4eccc-112">(Pour un contrôle plus détaillé, cliquez sur **Options avancées** dans la boîte de dialogue **autorisations** .)</span><span class="sxs-lookup"><span data-stu-id="4eccc-112">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="4eccc-113">Cliquez sur **appliquer**, puis sur **OK** dans la boîte de dialogue **autorisations** .</span><span class="sxs-lookup"><span data-stu-id="4eccc-113">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="4eccc-114">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="4eccc-114">Additional considerations</span></span>

-   <span data-ttu-id="4eccc-115">Par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="4eccc-115">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="4eccc-116">Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine et modifier les autorisations de **sécurité** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4eccc-116">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="4eccc-117">Pour déléguer l’accès en lecture aux administrateurs de stratégie de groupe qui utilisent AGPM, vous devez leur attribuer le contenu de la **liste** et les autorisations de **paramètres de lecture** .</span><span class="sxs-lookup"><span data-stu-id="4eccc-117">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="4eccc-118">Cela leur permet d’afficher des objets de stratégie de groupe dans l’onglet **contenu** d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="4eccc-118">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="4eccc-119">Définissez l’autorisation à appliquer à **cet objet et aux objets imbriqués**.</span><span class="sxs-lookup"><span data-stu-id="4eccc-119">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="4eccc-120">D’autres autorisations doivent être déléguées explicitement.</span><span class="sxs-lookup"><span data-stu-id="4eccc-120">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="4eccc-121">Les éditeurs doivent disposer d’une autorisation de **lecture** pour la copie déployée d’un objet de stratégie de groupe pour tirer pleinement parti de l’installation de logiciels de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4eccc-121">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="4eccc-122">L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte afin qu’elle ne soit pas utilisée pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4eccc-122">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="4eccc-123">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="4eccc-123">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="4eccc-124">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4eccc-124">Additional references</span></span>

-   [<span data-ttu-id="4eccc-125">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="4eccc-125">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 






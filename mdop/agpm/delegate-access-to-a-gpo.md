---
title: Déléguer l'accès à un objet de stratégie de groupe
description: Déléguer l'accès à un objet de stratégie de groupe
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807645"
---
# <span data-ttu-id="d64d6-103">Déléguer l'accès à un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d64d6-103">Delegate Access to a GPO</span></span>


<span data-ttu-id="d64d6-104">Un approbateur peut déléguer la gestion d’un objet de stratégie de groupe contrôlé (GPO) qui a été **créé par cet approbateur**.</span><span class="sxs-lookup"><span data-stu-id="d64d6-104">An Approver can delegate the management of a controlled Group Policy object (GPO) that was **created by that Approver**.</span></span> <span data-ttu-id="d64d6-105">À l’instar d’un administrateur AGPM (contrôle total), l’approbateur peut déléguer l’accès à un tel objet de stratégie de groupe, de sorte que les éditeurs sélectionnés puissent le modifier, les réviseurs pourront le consulter et permettre à d’autres approbateurs de l’approuver.</span><span class="sxs-lookup"><span data-stu-id="d64d6-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO, so selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="d64d6-106">Par défaut, un approbateur ne peut pas déléguer l’accès aux objets de stratégie de groupe créés par un autre administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d64d6-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="d64d6-107">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe ou un compte d’utilisateur disposant des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="d64d6-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="d64d6-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d64d6-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d64d6-109">Pour déléguer la gestion d’un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="d64d6-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="d64d6-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d64d6-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d64d6-111">Dans l’onglet **Sommaire** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés, puis cliquez sur l’objet de stratégie de groupe à déléguer.</span><span class="sxs-lookup"><span data-stu-id="d64d6-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="d64d6-112">Cliquez sur le bouton **Ajouter** , sélectionnez les utilisateurs ou les groupes auxquels vous avez accès autorisé, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d64d6-112">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="d64d6-113">Pour personnaliser les autorisations pour chacun d’eux, cliquez sur le bouton **avancé** sous l’onglet **Sommaire** et activez la case à cocher autorisations de rôle à autoriser ou à refuser.</span><span class="sxs-lookup"><span data-stu-id="d64d6-113">To customize the permissions for each, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="d64d6-114">(Pour un contrôle plus détaillé, cliquez sur **Options avancées** dans la boîte de dialogue **autorisations** .)</span><span class="sxs-lookup"><span data-stu-id="d64d6-114">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="d64d6-115">Cliquez sur **appliquer**, puis sur **OK** dans la boîte de dialogue **autorisations** .</span><span class="sxs-lookup"><span data-stu-id="d64d6-115">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="d64d6-116">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="d64d6-116">Additional considerations</span></span>

-   <span data-ttu-id="d64d6-117">Par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="d64d6-117">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="d64d6-118">Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine et modifier les autorisations de **sécurité** pour l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d64d6-118">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

### <span data-ttu-id="d64d6-119">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="d64d6-119">Additional references</span></span>

-   [<span data-ttu-id="d64d6-120">Création, contrôle ou importation d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d64d6-120">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 






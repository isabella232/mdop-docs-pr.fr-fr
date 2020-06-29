---
title: Importer un objet de stratégie de groupe de production
description: Importer un objet de stratégie de groupe de production
author: dansimp
ms.assetid: 35c2a682-ece8-4577-a083-7e3e9facfd13
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3d739a46d5ca078ec9d218c1cc1e5bd258c55601
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808417"
---
# <span data-ttu-id="6b297-103">Importer un objet de stratégie de groupe de production</span><span class="sxs-lookup"><span data-stu-id="6b297-103">Import a GPO from Production</span></span>


<span data-ttu-id="6b297-104">Si des modifications sont apportées à un objet de stratégie de groupe contrôlé (GPO) en dehors de la gestion de la stratégie de groupe avancée (AGPM), vous pouvez importer une copie de l’objet de stratégie de groupe à partir de l’environnement de production et l’enregistrer dans l’Archive pour amener l’archive et l’environnement de production à un état cohérent.</span><span class="sxs-lookup"><span data-stu-id="6b297-104">If changes are made to a controlled Group Policy Object (GPO) outside of Advanced Group Policy Management (AGPM), you can import a copy of the GPO from the production environment and save it to the archive to bring the archive and the production environment to a consistent state.</span></span> <span data-ttu-id="6b297-105">(Pour importer un objet de stratégie de groupe non contrôlé, contrôlez l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="6b297-105">(To import an uncontrolled GPO, control the GPO.</span></span> <span data-ttu-id="6b297-106">Voir [demander le contrôle d’un objet de stratégie de groupe non contrôlé](request-control-of-an-uncontrolled-gpo-agpm30ops.md).)</span><span class="sxs-lookup"><span data-stu-id="6b297-106">See [Request Control of an Uncontrolled GPO](request-control-of-an-uncontrolled-gpo-agpm30ops.md).)</span></span>

<span data-ttu-id="6b297-107">Un compte d’utilisateur ayant le rôle d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires inAGPM est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6b297-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions inAGPM is required to complete this procedure.</span></span> <span data-ttu-id="6b297-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="6b297-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="6b297-109">Pour importer un objet de stratégie de groupe à partir de l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="6b297-109">To import a GPO from the production environment</span></span>**

1.  <span data-ttu-id="6b297-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="6b297-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="6b297-111">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="6b297-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="6b297-112">Cliquez avec le bouton droit sur l’objet de stratégie de groupe, puis cliquez sur **Importer à partir de la production**.</span><span class="sxs-lookup"><span data-stu-id="6b297-112">Right-click the GPO, and then click **Import from Production**.</span></span>

4.  <span data-ttu-id="6b297-113">Tapez un commentaire pour la piste d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b297-113">Type a comment for the audit trail of the GPO, and then click **OK**.</span></span>

### <span data-ttu-id="6b297-114">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="6b297-114">Additional considerations</span></span>

-   <span data-ttu-id="6b297-115">Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6b297-115">By default, you must be an Editor, Approver, or AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="6b297-116">Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres**, déployer l’objet de stratégie de **groupe**ou **supprimer** des autorisations d’objet GPO pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="6b297-116">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="6b297-117">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6b297-117">Additional references</span></span>

-   [<span data-ttu-id="6b297-118">Création, contrôle ou importation d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="6b297-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 






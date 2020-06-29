---
title: Créer un modèle
description: Créer un modèle
author: dansimp
ms.assetid: 8208f14a-5c18-43a7-8564-118230398cca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f6713cd0fadb651e1de028bbcf2ae3ec1dd067c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808565"
---
# <span data-ttu-id="640f1-103">Créer un modèle</span><span class="sxs-lookup"><span data-stu-id="640f1-103">Create a Template</span></span>


<span data-ttu-id="640f1-104">La création d’un modèle vous permet d’enregistrer tous les paramètres d’une version particulière d’un objet de stratégie de groupe à utiliser comme point de départ pour la création de nouveaux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="640f1-104">Creating a template enables you to save all of the settings of a particular version of a Group Policy Object (GPO) to use as a starting point for creating new GPOs.</span></span>

<span data-ttu-id="640f1-105">**Remarques**  Un modèle est une version statique non modifiable d’un objet de stratégie de groupe à utiliser comme point de départ pour créer de nouveaux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="640f1-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="640f1-106">Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="640f1-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="640f1-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="640f1-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="640f1-108">Pour créer un modèle sur la base d’un objet de stratégie de groupe existant</span><span class="sxs-lookup"><span data-stu-id="640f1-108">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="640f1-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="640f1-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="640f1-110">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** ou non **contrôlé** pour afficher les objets de stratégie de groupe disponibles.</span><span class="sxs-lookup"><span data-stu-id="640f1-110">On the **Contents** tab in the details pane, click the **Controlled** or **Uncontrolled** tab to display available GPOs.</span></span>

3.  <span data-ttu-id="640f1-111">Cliquez avec le bouton droit sur l’objet GPO à partir duquel vous souhaitez créer un modèle, puis cliquez sur **Enregistrer comme modèle**.</span><span class="sxs-lookup"><span data-stu-id="640f1-111">Right-click the GPO from which you want to create a template, and then click **Save as Template**.</span></span>

4.  <span data-ttu-id="640f1-112">Tapez un nom pour le modèle et un commentaire, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="640f1-112">Type a name for the template and a comment, and then click **OK**.</span></span>

5.  <span data-ttu-id="640f1-113">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="640f1-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="640f1-114">Le nouveau modèle s’affiche sous l’onglet **modèles** .</span><span class="sxs-lookup"><span data-stu-id="640f1-114">The new template appears on the **Templates** tab.</span></span>

### <span data-ttu-id="640f1-115">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="640f1-115">Additional considerations</span></span>

-   <span data-ttu-id="640f1-116">Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="640f1-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="640f1-117">Plus précisément, vous devez disposer du **contenu de liste** et créer des autorisations de **modèle** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="640f1-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="640f1-118">Le changement de nom ou la suppression d’un modèle n’a pas d’incidence sur les objets de stratégie de groupe créés à partir du modèle</span><span class="sxs-lookup"><span data-stu-id="640f1-118">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="640f1-119">Étant donné qu’il ne peut pas être modifié, un modèle n’a pas d’historique.</span><span class="sxs-lookup"><span data-stu-id="640f1-119">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="640f1-120">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="640f1-120">Additional references</span></span>

-   [<span data-ttu-id="640f1-121">Création d'un modèle et définition d'un modèle par défaut</span><span class="sxs-lookup"><span data-stu-id="640f1-121">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm30ops.md)

-   [<span data-ttu-id="640f1-122">Demander la création d'un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="640f1-122">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo-agpm30ops.md)

 

 






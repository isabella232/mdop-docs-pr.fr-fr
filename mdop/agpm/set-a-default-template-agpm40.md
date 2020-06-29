---
title: Définir un modèle par défaut
description: Définir un modèle par défaut
author: dansimp
ms.assetid: 07208b6b-cb3a-4f6c-9c84-36d4dc1486d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51a13c2c57e38adca883a6eb962d8c5eae4316db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808225"
---
# <span data-ttu-id="f085d-103">Définir un modèle par défaut</span><span class="sxs-lookup"><span data-stu-id="f085d-103">Set a Default Template</span></span>


<span data-ttu-id="f085d-104">En tant qu’éditeur, vous pouvez spécifier lequel des modèles disponibles sera le modèle par défaut suggéré par tous les administrateurs de stratégie de groupe pour créer des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f085d-104">As an Editor, you can specify which of the available templates will be the default template suggested for all Group Policy administrators creating new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="f085d-105">**Remarques**  Un modèle est une version statique non modifiable d’un objet de stratégie de groupe à utiliser comme point de départ pour créer de nouveaux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f085d-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="f085d-106">Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f085d-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="f085d-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f085d-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f085d-108">Pour définir le modèle par défaut à utiliser lors de la création de nouveaux objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="f085d-108">To set the default template for use when creating new GPOs</span></span>**

1.  <span data-ttu-id="f085d-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f085d-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f085d-110">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **modèles** pour afficher les modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="f085d-110">On the **Contents** tab in the details pane, click the **Templates** tab to display available templates.</span></span>

3.  <span data-ttu-id="f085d-111">Cliquez avec le bouton droit sur le modèle que vous voulez définir par défaut, puis cliquez sur **définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="f085d-111">Right-click the template that you want to set as the default, and then click **Set as Default**.</span></span>

4.  <span data-ttu-id="f085d-112">Cliquez sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="f085d-112">Click **Yes** to confirm.</span></span>

5.  <span data-ttu-id="f085d-113">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f085d-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f085d-114">Le modèle par défaut comporte une icône bleue et l’État est identifié comme **modèle (par défaut)** sous l’onglet **modèles** .</span><span class="sxs-lookup"><span data-stu-id="f085d-114">The default template has a blue icon and the state is identified as **Template (default)** on the **Templates** tab.</span></span>

### <span data-ttu-id="f085d-115">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="f085d-115">Additional considerations</span></span>

-   <span data-ttu-id="f085d-116">Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f085d-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="f085d-117">Plus précisément, vous devez disposer du **contenu de liste** et créer des autorisations de **modèle** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="f085d-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="f085d-118">Après avoir défini un modèle comme modèle par défaut, ce modèle sera le premier sélectionné dans la boîte de dialogue **nouvel objet GPO contrôlé** lors de la création de nouveaux objets de stratégie de groupe par les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f085d-118">After you set a template as the default, that template will be the one initially selected in the **New Controlled GPO** dialog box when Group Policy administrators create new GPOs.</span></span> <span data-ttu-id="f085d-119">Toutefois, ils pourront sélectionner un autre modèle d’objet de stratégie de groupe, y compris un \*\* &lt; objet de stratégie de groupe &gt; vide\*\*, qui n’inclut pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f085d-119">However, they will have the option to select any other GPO template, including **&lt;Empty GPO&gt;**, which does not include any settings.</span></span>

-   <span data-ttu-id="f085d-120">Le changement de nom ou la suppression d’un modèle n’a pas d’incidence sur les objets de stratégie de groupe créés à partir du modèle</span><span class="sxs-lookup"><span data-stu-id="f085d-120">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="f085d-121">Étant donné qu’il ne peut pas être modifié, un modèle n’a pas d’historique.</span><span class="sxs-lookup"><span data-stu-id="f085d-121">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="f085d-122">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f085d-122">Additional references</span></span>

-   [<span data-ttu-id="f085d-123">Création d'un modèle et définition d'un modèle par défaut</span><span class="sxs-lookup"><span data-stu-id="f085d-123">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="f085d-124">Demander la création d'un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="f085d-124">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 






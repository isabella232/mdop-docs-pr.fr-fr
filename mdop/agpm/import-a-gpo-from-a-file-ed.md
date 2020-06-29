---
title: Importer un objet de stratégie de groupe à partir d'un fichier
description: Importer un objet de stratégie de groupe à partir d'un fichier
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808421"
---
# <span data-ttu-id="2e2e1-103">Importer un objet de stratégie de groupe à partir d'un fichier</span><span class="sxs-lookup"><span data-stu-id="2e2e1-103">Import a GPO from a File</span></span>


<span data-ttu-id="2e2e1-104">Dans Advanced Group Policy Management (AGPM), si vous avez exporté un objet de stratégie de groupe (GPO) vers un fichier CAB, vous pouvez importer les paramètres de stratégie de cet objet GPO dans un objet de stratégie de groupe existant d’un domaine d’une autre forêt.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-104">In Advanced Group Policy Management (AGPM), if you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="2e2e1-105">L’importation des paramètres de stratégie dans un objet de stratégie de groupe existant remplace tous les paramètres de stratégie de cet objet.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-105">Importing policy settings into an existing GPO replaces all policy settings within that GPO.</span></span> <span data-ttu-id="2e2e1-106">Pour plus d’informations sur l’exportation des paramètres d’objet de stratégie de groupe dans un fichier CAB, voir [exporter un objet de stratégie de groupe dans un fichier](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-106">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="2e2e1-107">Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-107">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="2e2e1-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-108">Review the details in "Additional considerations" in this topic.</span></span>

## <a href="" id="bkmk-existing"></a>


**<span data-ttu-id="2e2e1-109">Pour importer les paramètres de stratégie dans un objet de stratégie de groupe existant</span><span class="sxs-lookup"><span data-stu-id="2e2e1-109">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="2e2e1-110">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans le domaine dans lequel vous voulez importer les paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-110">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="2e2e1-111">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="2e2e1-112">Consultez l’objet GPO de destination sur lequel vous souhaitez importer les paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-112">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="2e2e1-113">Cliquez avec le bouton droit sur l’objet GPO de destination, pointez sur **Importer à partir de**, puis cliquez sur **fichier**.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-113">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="2e2e1-114">Suivez les instructions de l' **Assistant importation de paramètres** pour sélectionner une sauvegarde d’objet de stratégie de groupe, importez les paramètres de la stratégie de votre choix pour remplacer celles de l’objet GPO de destination et entrez un commentaire pour la piste d’audit de l’objet GPO de destination.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-114">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="2e2e1-115">Par défaut, l’objet GPO de destination est réintégré lorsque l’Assistant est terminé.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-115">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="2e2e1-116">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="2e2e1-116">Additional considerations</span></span>

-   <span data-ttu-id="2e2e1-117">Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-117">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="2e2e1-118">En particulier, vous devez disposer d’un **contenu de liste**, **modifier des paramètres**et importer des autorisations d’objets de **stratégie de groupe** pour le domaine, et l’objet de stratégie de groupe doit être extrait par vous.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-118">Specifically, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span>

-   <span data-ttu-id="2e2e1-119">Même si un éditeur ne peut pas importer les paramètres de stratégie dans un nouvel objet GPO lors de sa création, un éditeur peut demander la création d’un nouvel objet de stratégie de groupe, puis importer les paramètres de stratégie dans ce dernier après sa création.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-119">Although an Editor cannot import policy settings into a new GPO during its creation, an Editor can request the creation of a new GPO and then import policy settings into it after it is created.</span></span>

### <span data-ttu-id="2e2e1-120">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2e2e1-120">Additional references</span></span>

-   [<span data-ttu-id="2e2e1-121">Utilisation d'un environnement de test</span><span class="sxs-lookup"><span data-stu-id="2e2e1-121">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 






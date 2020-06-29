---
title: Importer un objet de stratégie de groupe à partir d'un fichier
description: Importer un objet de stratégie de groupe à partir d'un fichier
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808433"
---
# <span data-ttu-id="f03aa-103">Importer un objet de stratégie de groupe à partir d'un fichier</span><span class="sxs-lookup"><span data-stu-id="f03aa-103">Import a GPO from a File</span></span>


<span data-ttu-id="f03aa-104">Dans Advanced Group Policy Management (AGPM), si vous êtes un administrateur AGPM (contrôle total) et si vous avez exporté un objet de stratégie de groupe (GPO) vers un fichier CAB, vous pouvez importer les paramètres de stratégie de cet objet GPO dans un nouvel objet de stratégie de groupe ou un objet de stratégie de groupe existant dans un domaine d’une autre forêt.</span><span class="sxs-lookup"><span data-stu-id="f03aa-104">In Advanced Group Policy Management (AGPM), if you are an AGPM Administrator (Full Control) and you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into a new GPO or an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="f03aa-105">Pour plus d’informations sur l’exportation des paramètres d’objet de stratégie de groupe dans un fichier CAB, voir [exporter un objet de stratégie de groupe dans un fichier](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="f03aa-105">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="f03aa-106">Un compte d’utilisateur ayant le rôle d’administrateur AGPM ou les autorisations nécessaires dans AGPM est requis pour importer les paramètres de stratégie dans un nouvel objet de stratégie de groupe contrôlé.</span><span class="sxs-lookup"><span data-stu-id="f03aa-106">A user account with the AGPM Administrator role or the necessary permissions in AGPM is required to import policy settings into a new controlled GPO.</span></span> <span data-ttu-id="f03aa-107">Un compte d’utilisateur possédant le rôle d’administrateur de l’éditeur ou d’AGPM ou les autorisations nécessaires dans AGPM est requis pour importer les paramètres de stratégie dans un objet de stratégie de groupe existant.</span><span class="sxs-lookup"><span data-stu-id="f03aa-107">A user account with the Editor or AGPM Administrator role or necessary permissions in AGPM is required to import policy settings into an existing GPO.</span></span> <span data-ttu-id="f03aa-108">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f03aa-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="f03aa-109">Importation des paramètres de stratégie à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="f03aa-109">Importing policy settings from a file</span></span>


<span data-ttu-id="f03aa-110">Lorsque vous importez des paramètres de stratégie à partir d’un fichier, vous pouvez les importer dans un nouvel objet de stratégie de groupe ou un objet de stratégie de groupe existant.</span><span class="sxs-lookup"><span data-stu-id="f03aa-110">When you import policy settings from a file, you can import them into a new GPO or an existing GPO.</span></span> <span data-ttu-id="f03aa-111">Toutefois, si vous importez des paramètres de stratégie dans un objet de stratégie de groupe existant, tous les paramètres de stratégie qu’il contient sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="f03aa-111">However, if you import policy settings into an existing GPO, all policy settings within it are replaced.</span></span>

-   [<span data-ttu-id="f03aa-112">Importer les paramètres de stratégie dans un nouvel objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="f03aa-112">Import policy settings into a new controlled GPO</span></span>](#bkmk-new)

-   [<span data-ttu-id="f03aa-113">Importer les paramètres de stratégie dans un objet de stratégie de groupe existant</span><span class="sxs-lookup"><span data-stu-id="f03aa-113">Import policy settings into an existing GPO</span></span>](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**<span data-ttu-id="f03aa-114">Pour importer les paramètres de stratégie dans un nouvel objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="f03aa-114">To import policy settings into a new controlled GPO</span></span>**

1.  <span data-ttu-id="f03aa-115">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans le domaine dans lequel vous voulez importer les paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="f03aa-115">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="f03aa-116">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="f03aa-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="f03aa-117">Créer un objet de stratégie de groupe contrôlé.</span><span class="sxs-lookup"><span data-stu-id="f03aa-117">Create a new controlled GPO.</span></span> <span data-ttu-id="f03aa-118">Dans la boîte de dialogue **nouvel objet GPO contrôlé** , cliquez sur **Importer** , puis sur **Assistant lancement**.</span><span class="sxs-lookup"><span data-stu-id="f03aa-118">In the **New Controlled GPO** dialog box, click **Import** and then click **Launch Wizard**.</span></span> <span data-ttu-id="f03aa-119">Pour plus d’informations sur la création d’un objet de stratégie de groupe, voir [créer un objet de stratégie de groupe contrôlé](create-a-new-controlled-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="f03aa-119">For more information about how to create a GPO, see [Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md).</span></span>

4.  <span data-ttu-id="f03aa-120">Suivez les instructions de l' **Assistant importation de paramètres** pour sélectionner une sauvegarde de l’objet de stratégie de groupe, importer les paramètres de stratégie de celle-ci pour le nouvel objet de stratégie de groupe et entrer un commentaire pour la trace d’audit du nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="f03aa-120">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import policy settings from it for the new GPO, and enter a comment for the audit trail of the new GPO.</span></span>

### <a href="" id="bkmk-existing"></a>

**<span data-ttu-id="f03aa-121">Pour importer les paramètres de stratégie dans un objet de stratégie de groupe existant</span><span class="sxs-lookup"><span data-stu-id="f03aa-121">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="f03aa-122">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans le domaine dans lequel vous voulez importer les paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="f03aa-122">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="f03aa-123">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="f03aa-123">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="f03aa-124">Consultez l’objet GPO de destination sur lequel vous souhaitez importer les paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="f03aa-124">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="f03aa-125">Cliquez avec le bouton droit sur l’objet GPO de destination, pointez sur **Importer à partir de**, puis cliquez sur **fichier**.</span><span class="sxs-lookup"><span data-stu-id="f03aa-125">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="f03aa-126">Suivez les instructions de l' **Assistant importation de paramètres** pour sélectionner une sauvegarde d’objet de stratégie de groupe, importez les paramètres de la stratégie de votre choix pour remplacer celles de l’objet GPO de destination et entrez un commentaire pour la piste d’audit de l’objet GPO de destination.</span><span class="sxs-lookup"><span data-stu-id="f03aa-126">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="f03aa-127">Par défaut, l’objet GPO de destination est réintégré lorsque l’Assistant est terminé.</span><span class="sxs-lookup"><span data-stu-id="f03aa-127">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="f03aa-128">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="f03aa-128">Additional considerations</span></span>

-   <span data-ttu-id="f03aa-129">Pour importer les paramètres de stratégie dans un nouvel objet de stratégie de groupe, vous devez disposer d’un **contenu de liste**, d’importer un **objet de stratégie**de groupe et de créer des autorisations d' **objet GPO** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="f03aa-129">To import policy settings to a new controlled GPO, you must have **List Contents**, **Import GPO**, and **Create GPO** permissions for the domain.</span></span> <span data-ttu-id="f03aa-130">Par défaut, vous devez être administrateur d’AGPM pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f03aa-130">By default, you must be an AGPM Administrator to perform this procedure.</span></span>

-   <span data-ttu-id="f03aa-131">Pour importer les paramètres de stratégie d’un objet de stratégie de groupe existant, vous devez disposer d’un **contenu de liste**, **modifier des paramètres**et importer des autorisations d' **objets** de stratégie de groupe pour le domaine et l’objet de stratégie de groupe doit être extrait par vous.</span><span class="sxs-lookup"><span data-stu-id="f03aa-131">To import policy settings to an existing GPO, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span> <span data-ttu-id="f03aa-132">Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f03aa-132">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span>

### <span data-ttu-id="f03aa-133">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f03aa-133">Additional references</span></span>

-   [<span data-ttu-id="f03aa-134">Gestion de l'archivage</span><span class="sxs-lookup"><span data-stu-id="f03aa-134">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 






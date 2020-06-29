---
title: Exporter un objet de stratégie de groupe dans un fichier
description: Exporter un objet de stratégie de groupe dans un fichier
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808473"
---
# <span data-ttu-id="34145-103">Exporter un objet de stratégie de groupe dans un fichier</span><span class="sxs-lookup"><span data-stu-id="34145-103">Export a GPO to a File</span></span>


<span data-ttu-id="34145-104">Vous pouvez exporter un objet de stratégie de groupe contrôlé (GPO) vers un fichier CAB de sorte que vous puissiez le copier dans un domaine d’une autre forêt et importer l’objet GPO dans Advanced Group Policy Management (AGPM) dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="34145-104">You can export a controlled Group Policy Object (GPO) to a CAB file so that you can copy it to a domain in another forest and import the GPO into Advanced Group Policy Management (AGPM) in that domain.</span></span> <span data-ttu-id="34145-105">Pour plus d’informations sur l’importation des paramètres de l’objet de stratégie de groupe dans un objet GPO nouveau ou existant, voir [Importer un objet GPO à partir d’un fichier](import-a-gpo-from-a-file-ed.md).</span><span class="sxs-lookup"><span data-stu-id="34145-105">For information about how to import GPO settings into a new or existing GPO, see [Import a GPO from a File](import-a-gpo-from-a-file-ed.md).</span></span>

<span data-ttu-id="34145-106">Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="34145-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="34145-107">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="34145-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="34145-108">Pour exporter un objet de stratégie de groupe dans un fichier</span><span class="sxs-lookup"><span data-stu-id="34145-108">To export a GPO to a file</span></span>**

1.  <span data-ttu-id="34145-109">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="34145-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="34145-110">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="34145-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="34145-111">Cliquez avec le bouton droit sur l’objet de stratégie de groupe, puis cliquez sur **Exporter vers**.</span><span class="sxs-lookup"><span data-stu-id="34145-111">Right-click the GPO, and then click **Export to**.</span></span>

4.  <span data-ttu-id="34145-112">Entrez un nom de fichier pour le fichier dans lequel vous voulez exporter l’objet de stratégie de groupe, puis cliquez sur **Exporter**.</span><span class="sxs-lookup"><span data-stu-id="34145-112">Enter a file name for the file to which you want to export the GPO, and then click **Export**.</span></span> <span data-ttu-id="34145-113">Si le fichier n’existe pas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="34145-113">If the file does not exist, it is created.</span></span> <span data-ttu-id="34145-114">S’il existe déjà, il est remplacé.</span><span class="sxs-lookup"><span data-stu-id="34145-114">If it already exists, it is replaced.</span></span>

### <span data-ttu-id="34145-115">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="34145-115">Additional considerations</span></span>

-   <span data-ttu-id="34145-116">Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="34145-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="34145-117">Plus précisément, vous devez disposer d’autorisations de **liste**, de **paramètres de lecture**et d' **exportation d’objets** de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="34145-117">Specifically, you must have **List Contents**, **Read Settings**, and **Export GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="34145-118">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="34145-118">Additional references</span></span>

-   [<span data-ttu-id="34145-119">Utilisation d'un environnement de test</span><span class="sxs-lookup"><span data-stu-id="34145-119">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 






---
title: Utiliser un environnement de test
description: Utiliser un environnement de test
author: dansimp
ms.assetid: 86295084-b39e-4040-bb3f-15c3c1e99b1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1264d9fe6f922a7e61bcd069581c7bd5e39b7787
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807426"
---
# <span data-ttu-id="7bb34-103">Utiliser un environnement de test</span><span class="sxs-lookup"><span data-stu-id="7bb34-103">Use a Test Environment</span></span>


<span data-ttu-id="7bb34-104">Si vous utilisez une unité d’organisation de test (UO) pour tester les objets de stratégie de groupe avant le déploiement dans l’environnement de production, vous devez disposer des autorisations nécessaires pour accéder à l’unité d’organisation test.</span><span class="sxs-lookup"><span data-stu-id="7bb34-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="7bb34-105">L’utilisation d’une UO de test est facultative.</span><span class="sxs-lookup"><span data-stu-id="7bb34-105">The use of a test OU is optional.</span></span>

**<span data-ttu-id="7bb34-106">Pour utiliser une UO de test</span><span class="sxs-lookup"><span data-stu-id="7bb34-106">To use a test OU</span></span>**

1.  <span data-ttu-id="7bb34-107">Dans la console de gestion des stratégies de groupe, dans la **console de gestion des stratégies de groupe**, cliquez sur objets de **stratégie de groupe** dans la forêt et le domaine dans lequel vous gérez les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7bb34-107">While you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="7bb34-108">Cliquez sur la copie extraite de l’objet de stratégie de groupe à tester.</span><span class="sxs-lookup"><span data-stu-id="7bb34-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="7bb34-109">Le nom est précédé de **\ [extrait.]**.</span><span class="sxs-lookup"><span data-stu-id="7bb34-109">The name will be preceded with **\[Checked Out\]**.</span></span> <span data-ttu-id="7bb34-110">(S’il n’apparaît pas dans la liste, cliquez sur **action**, puis sur **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="7bb34-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="7bb34-111">Triez les noms par ordre alphabétique, et les objets de stratégie de groupe **\ [extraits]** apparaissent généralement en haut de la liste.)</span><span class="sxs-lookup"><span data-stu-id="7bb34-111">Sort the names alphabetically, and **\[Checked Out\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="7bb34-112">Faites glisser et déplacez l’objet GPO vers l’unité d’organisation test.</span><span class="sxs-lookup"><span data-stu-id="7bb34-112">Drag and drop the GPO to the test OU.</span></span>

4.  <span data-ttu-id="7bb34-113">Cliquez sur **OK** dans la boîte de dialogue qui vous demande si vous souhaitez créer un lien vers l’objet GPO dans l’unité d’organisation de test.</span><span class="sxs-lookup"><span data-stu-id="7bb34-113">Click **OK** in the dialog box asking whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="7bb34-114">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="7bb34-114">Additional considerations</span></span>

-   <span data-ttu-id="7bb34-115">Une fois le test terminé, l’archivage de l’objet de stratégie de groupe supprime automatiquement le lien vers la copie extraite de l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="7bb34-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="7bb34-116">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="7bb34-116">Additional references</span></span>

-   [<span data-ttu-id="7bb34-117">Modification d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7bb34-117">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

 

 






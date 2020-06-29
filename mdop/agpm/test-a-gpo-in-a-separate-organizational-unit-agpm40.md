---
title: Tester un objet de stratégie de groupe dans une unité d'organisation distincte
description: Tester un objet de stratégie de groupe dans une unité d'organisation distincte
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807434"
---
# <span data-ttu-id="54e93-103">Tester un objet de stratégie de groupe dans une unité d'organisation distincte</span><span class="sxs-lookup"><span data-stu-id="54e93-103">Test a GPO in a Separate Organizational Unit</span></span>


<span data-ttu-id="54e93-104">Si vous utilisez une unité d’organisation de test (UO) pour tester les objets de stratégie de groupe au sein d’un même domaine avant de procéder au déploiement vers l’environnement de production, vous devez disposer des autorisations nécessaires pour accéder à l’unité d’organisation de test.</span><span class="sxs-lookup"><span data-stu-id="54e93-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) within the same domain before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="54e93-105">L’utilisation d’une UO de test est facultative.</span><span class="sxs-lookup"><span data-stu-id="54e93-105">Using a test OU is optional.</span></span>

**<span data-ttu-id="54e93-106">Pour utiliser une UO de test</span><span class="sxs-lookup"><span data-stu-id="54e93-106">To use a test OU</span></span>**

1.  <span data-ttu-id="54e93-107">Même si l’objet de stratégie de groupe est extrait pour modification, dans la **console de gestion des stratégies de groupe**, cliquez sur objets de stratégie de **groupe** dans la forêt et dans le domaine dans lequel vous gérez les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="54e93-107">Although you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="54e93-108">Cliquez sur la copie extraite de l’objet de stratégie de groupe à tester.</span><span class="sxs-lookup"><span data-stu-id="54e93-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="54e93-109">Le nom est précédé de **\ [AGPM \]**.</span><span class="sxs-lookup"><span data-stu-id="54e93-109">The name will be preceded by **\[AGPM\]**.</span></span> <span data-ttu-id="54e93-110">(S’il n’apparaît pas dans la liste, cliquez sur **action**, puis sur **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="54e93-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="54e93-111">Triez les noms par ordre alphabétique, et les objets de stratégie de groupe **\ [AGPM \]** apparaissent généralement en haut de la liste.)</span><span class="sxs-lookup"><span data-stu-id="54e93-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="54e93-112">Faites glisser l’objet GPO vers l’unité d’organisation test.</span><span class="sxs-lookup"><span data-stu-id="54e93-112">Drag the GPO to the test OU.</span></span>

4.  <span data-ttu-id="54e93-113">Cliquez sur **OK** dans la boîte de dialogue qui vous demande si vous souhaitez créer un lien vers l’objet de stratégie de groupe dans l’unité d’organisation test.</span><span class="sxs-lookup"><span data-stu-id="54e93-113">Click **OK** in the dialog box that asks whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="54e93-114">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="54e93-114">Additional considerations</span></span>

-   <span data-ttu-id="54e93-115">Une fois le test terminé, l’archivage de l’objet de stratégie de groupe supprime automatiquement le lien vers la copie extraite de l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="54e93-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="54e93-116">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="54e93-116">Additional references</span></span>

-   [<span data-ttu-id="54e93-117">Utilisation d'un environnement de test</span><span class="sxs-lookup"><span data-stu-id="54e93-117">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 






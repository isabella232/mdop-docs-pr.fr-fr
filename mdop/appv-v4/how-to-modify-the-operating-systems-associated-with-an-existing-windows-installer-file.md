---
title: Procédure pour modifier les systèmes d'exploitation associés à un fichier Windows Installer existant
description: Procédure pour modifier les systèmes d'exploitation associés à un fichier Windows Installer existant
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806913"
---
# <span data-ttu-id="2f45b-103">Procédure pour modifier les systèmes d'exploitation associés à un fichier Windows Installer existant</span><span class="sxs-lookup"><span data-stu-id="2f45b-103">How to Modify the Operating Systems Associated With an Existing Windows Installer File</span></span>


<span data-ttu-id="2f45b-104">Utilisez la procédure suivante pour modifier les versions de système d’exploitation associées à un fichier Windows Installer (**MSI**) existant qui a été créé à l’aide du Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="2f45b-104">Use the following procedure to modify the operating system versions associated with an existing Windows Installer (**MSI**) file that was created by using the App-V Sequencer.</span></span>

**<span data-ttu-id="2f45b-105">Pour modifier les systèmes d’exploitation d’un fichier Windows Installer existant</span><span class="sxs-lookup"><span data-stu-id="2f45b-105">To modify the operating systems of an existing Windows Installer file</span></span>**

1.  <span data-ttu-id="2f45b-106">Installez le Sequencer App-V sur un ordinateur de votre environnement sur lequel seul le système d’exploitation est installé.</span><span class="sxs-lookup"><span data-stu-id="2f45b-106">Install the App-V Sequencer on a computer in your environment that has only the operating system installed.</span></span> <span data-ttu-id="2f45b-107">Vous pouvez également installer le Sequencer sur un ordinateur exécutant un environnement virtuel (par exemple, Microsoft Virtual PC).</span><span class="sxs-lookup"><span data-stu-id="2f45b-107">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="2f45b-108">Cette méthode est utile, car il est plus facile de conserver un environnement de séquençage net que vous pouvez réutiliser avec une configuration supplémentaire minimum.</span><span class="sxs-lookup"><span data-stu-id="2f45b-108">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span> <span data-ttu-id="2f45b-109">Pour plus d’informations sur l’installation de Sequencer App-V, voir [Comment installer le Sequencer](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="2f45b-109">For more information about installing the App-V Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

2.  <span data-ttu-id="2f45b-110">Copiez l’intégralité du package d’application virtuel contenant le fichier Windows Installer que vous voulez modifier sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2f45b-110">Copy the entire virtual application package that contains the Windows Installer file you want to modify to the computer running the Sequencer.</span></span>

3.  <span data-ttu-id="2f45b-111">Pour modifier le fichier du programme d’installation Windows, ouvrez la console de Sequencer, sélectionnez **package**  /  **Open**, puis naviguez jusqu’à l’emplacement dans lequel le package d’application virtuel associé au fichier d’installation Windows est enregistré.</span><span class="sxs-lookup"><span data-stu-id="2f45b-111">To modify the Windows Installer file, open the Sequencer console, select **Package** / **Open**, and then browse to the location where the virtual application package associated with the Windows Installer file is saved.</span></span>

4.  <span data-ttu-id="2f45b-112">Pour ajouter ou supprimer des systèmes d’exploitation, sélectionnez l’onglet **déploiement** dans la console de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2f45b-112">To add or remove operating systems, select the **Deployment** tab in the Sequencer console.</span></span> <span data-ttu-id="2f45b-113">Pour spécifier d’autres systèmes d’exploitation qui seront associés au fichier du programme d’installation Windows, sélectionnez le système d’exploitation de votre choix, puis cliquez sur la flèche qui pointe vers le contrôle de liste du système d’exploitation **sélectionné** .</span><span class="sxs-lookup"><span data-stu-id="2f45b-113">To specify additional operating systems that will be associated with the Windows Installer file, select the desired operating system, and then click the arrow that points to the **Selected** operating system list control.</span></span>

    <span data-ttu-id="2f45b-114">Pour supprimer une association de système d’exploitation, sélectionnez le système d’exploitation que vous voulez supprimer, puis cliquez sur la flèche qui pointe vers le contrôle de liste de systèmes d’exploitation **disponibles** .</span><span class="sxs-lookup"><span data-stu-id="2f45b-114">To remove an operating system association, select the operating system you want to remove, and then click the arrow that points to the **Available** operating system list control.</span></span>

5.  <span data-ttu-id="2f45b-115">Pour créer un nouveau programme d’installation Windows qui sera associé au package d’application virtuelle, sélectionnez **générer le package Microsoft Windows Installer (MSI)**.</span><span class="sxs-lookup"><span data-stu-id="2f45b-115">To create a new Windows Installer that will be associated with the virtual application package, select **Generate Microsoft Windows Installer (MSI) Package**.</span></span> <span data-ttu-id="2f45b-116">Vous pouvez également sélectionner **Outils**  /  **créer**un fichier msi.</span><span class="sxs-lookup"><span data-stu-id="2f45b-116">Alternatively, you can select **Tools** / **Create MSI**.</span></span>

    <span data-ttu-id="2f45b-117">**Remarques**  Si vous sélectionnez **Outils** / **création de MSI** pour créer un nouveau fichier Windows Installer, vous pouvez ignorer l' **étape 6** de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2f45b-117">**Note** If you select **Tools** / **Create MSI** to create a new Windows Installer file, you can skip **Step 6** of this procedure.</span></span>

     

6.  <span data-ttu-id="2f45b-118">Pour enregistrer le package d’application virtuelle, sélectionnez Enregistrer le **package**  /  **Save**.</span><span class="sxs-lookup"><span data-stu-id="2f45b-118">To save the virtual application package, select **Package** / **Save**.</span></span>

## <span data-ttu-id="2f45b-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f45b-119">Related topics</span></span>


[<span data-ttu-id="2f45b-120">Tâches pour Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2f45b-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 






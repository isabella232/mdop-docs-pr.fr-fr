---
title: À propos des phases de séquencement
description: À propos des phases de séquencement
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808133"
---
# <span data-ttu-id="8712f-103">À propos des phases de séquencement</span><span class="sxs-lookup"><span data-stu-id="8712f-103">About Sequencing Phases</span></span>


<span data-ttu-id="8712f-104">Le séquençage est le processus par lequel vous créez un package d’application séquencé en utilisant le Sequencer Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="8712f-104">Sequencing is the process by which you create a sequenced application package by using the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="8712f-105">Lors du séquençage, le Sequencer analyse et enregistre tous les processus d’installation et de configuration pour une application et crée les fichiers suivants: ICO, OSD, SFT et SPRJ.</span><span class="sxs-lookup"><span data-stu-id="8712f-105">During sequencing, the Sequencer monitors and records all installation and setup processes for an application and creates the following files: ICO, OSD, SFT, and SPRJ.</span></span> <span data-ttu-id="8712f-106">Ces fichiers contiennent toutes les informations nécessaires sur une application et permettent à cette application de s’exécuter dans un environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="8712f-106">These files contain all the necessary information about an application, and they allow that application to run in a virtual environment.</span></span>

<span data-ttu-id="8712f-107">Les quatre phases pour séquençager une application et la création d’un package d’application virtuelle sont l’installation, le lancement, la personnalisation et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8712f-107">The four phases to sequencing an application and creating a virtual application package are installation, launch, customization, and save.</span></span> <span data-ttu-id="8712f-108">La liste suivante fournit des informations sur chacune des phases:</span><span class="sxs-lookup"><span data-stu-id="8712f-108">The following list provides information about each of the phases:</span></span>

1.  <span data-ttu-id="8712f-109">**Phase d’installation**: vous spécifiez le nom du package et un commentaire associé facultatif qui sera associé au package.</span><span class="sxs-lookup"><span data-stu-id="8712f-109">**Installation phase**—During the installation phase, you specify the package name and an optional associated comment that will be associated with the package.</span></span> <span data-ttu-id="8712f-110">Vous pouvez également configurer des options de surveillance avancées au cours de cette phase.</span><span class="sxs-lookup"><span data-stu-id="8712f-110">You can also configure advanced monitoring options during this phase.</span></span> <span data-ttu-id="8712f-111">Les options de surveillance avancée incluent la spécification de la taille du bloc et l’installation des mises à jour automatiques lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="8712f-111">Advanced monitoring options include specifying the block size and whether you will install automatic updates during monitoring.</span></span> <span data-ttu-id="8712f-112">Le Sequencer enregistre toutes les informations et configurations nécessaires nécessaires pour créer un package d’application virtuelle et les paramètres de fichier et de Registre associés.</span><span class="sxs-lookup"><span data-stu-id="8712f-112">The sequencer records all necessary information and configurations required to create a virtual application package and the associated file and registry settings.</span></span>

    <span data-ttu-id="8712f-113">**Important**  Pour afficher les options avancées, sélectionnez **afficher les options de surveillance avancée** dans la page informations sur le **package** .</span><span class="sxs-lookup"><span data-stu-id="8712f-113">**Important** To view the advanced options select **Show Advanced Monitoring Options** on the **Package Information** page.</span></span>

     

2.  <span data-ttu-id="8712f-114">**Phase de lancement**: lors de la phase de lancement, vous pouvez spécifier les associations de fichiers et les descripteurs de sécurité nécessaires qui doivent être configurés avec le package.</span><span class="sxs-lookup"><span data-stu-id="8712f-114">**Launch phase**—During the launch phase, you can specify any required file associations and security descriptors that should be configured with the package.</span></span> <span data-ttu-id="8712f-115">Vous devriez ouvrir l’application autant de fois que nécessaire pour garantir la stabilité et la fonctionnalité de l’application.</span><span class="sxs-lookup"><span data-stu-id="8712f-115">You should open the application as many times as necessary to ensure application functionality and stability.</span></span>

3.  <span data-ttu-id="8712f-116">**Phase de personnalisation**-lors de la phase de personnalisation, vous pouvez configurer votre package à l’aide des fichiers. OSD associés.</span><span class="sxs-lookup"><span data-stu-id="8712f-116">**Customization phase**—During the customization phase, you can configure your package by using the associated .osd files.</span></span> <span data-ttu-id="8712f-117">Vous pouvez spécifier si tous les scripts associés doivent s’exécuter à l’intérieur ou à l’extérieur de l’environnement virtuel, spécifier d’autres actions qui doivent être exécutées, spécifier la façon dont les scripts associés sont exécutés (de manière synchrone ou asynchrone) et spécifier d’autres scripts qui doivent être exécutés dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8712f-117">You can specify whether any associated scripts should run inside or outside of the virtual environment, specify additional actions that should be performed, specify how associated scripts run (synchronously or asynchronously), and specify any additional scripts that should be run under the user context.</span></span>

4.  <span data-ttu-id="8712f-118">**Phase de sauvegarde**: lors de la phase de sauvegarde, tous les fichiers requis pour le package d’application virtuelle sont créés.</span><span class="sxs-lookup"><span data-stu-id="8712f-118">**Save phase**—During the save phase, all required files for the virtual application package are created.</span></span> <span data-ttu-id="8712f-119">Les fichiers créés sont. sprj,. SFT,. OSD,. ico,. xml et le fichier Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="8712f-119">The files created are .sprj, .sft, .osd, .ico, .xml manifest, and the Windows installer (.msi) file.</span></span>

## <span data-ttu-id="8712f-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8712f-120">Related topics</span></span>


[<span data-ttu-id="8712f-121">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8712f-121">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 






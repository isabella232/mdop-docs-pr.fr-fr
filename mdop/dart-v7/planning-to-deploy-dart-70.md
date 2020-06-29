---
title: Planification du déploiement de DaRT7.0
description: Planification du déploiement de DaRT7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808682"
---
# <span data-ttu-id="00516-103">Planification du déploiement de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="00516-103">Planning to Deploy DaRT 7.0</span></span>


<span data-ttu-id="00516-104">Il existe un certain nombre de configurations et de configurations de déploiement différentes que vous devez prendre en compte avant de créer le plan de déploiement.</span><span class="sxs-lookup"><span data-stu-id="00516-104">There are a number of different deployment configurations and prerequisites that you must consider before you create your deployment plan.</span></span> <span data-ttu-id="00516-105">Cette section contient des informations qui vous aideront à collecter les informations nécessaires pour formuler un plan de déploiement qui répond le mieux à vos besoins professionnels.</span><span class="sxs-lookup"><span data-stu-id="00516-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

<span data-ttu-id="00516-106">Prenez en compte les points suivants lorsque vous planifiez l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 7:</span><span class="sxs-lookup"><span data-stu-id="00516-106">Consider the following when you plan your Microsoft Diagnostics and Recovery Toolset (DaRT)7 installation:</span></span>

-   <span data-ttu-id="00516-107">Lors de l’installation de DaRT, vous pouvez installer toutes les fonctionnalités sur un ordinateur d’administration informatique sur lequel vous exécuterez toutes les tâches associées à l’exécution de DaRT.</span><span class="sxs-lookup"><span data-stu-id="00516-107">When you install DaRT, you can either install all functionality on an IT administrator computer where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="00516-108">Ou vous pouvez installer uniquement la fonctionnalité DaRT qui crée l’image de récupération sur l’ordinateur de l’administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="00516-108">Or you can install only the DaRT functionality that creates the recovery image on the IT administrator computer.</span></span> <span data-ttu-id="00516-109">Ensuite, installez la fonctionnalité utilisée pour exécuter DaRT, telle que la **visionneuse de connexion à distance** et l' **analyseur d’incident**de DART, sur un ordinateur d’agent de support technique.</span><span class="sxs-lookup"><span data-stu-id="00516-109">Then, install the functionality used to run DaRT, such as the **DaRT Remote Connection Viewer** and **Crash Analyzer**, on a helpdesk agent computer.</span></span>

-   <span data-ttu-id="00516-110">Pour pouvoir exécuter DaRT à distance, assurez-vous que l’ordinateur de l’agent de support technique et tous les ordinateurs qui peuvent résoudre les problèmes distants se trouvent sur le même réseau.</span><span class="sxs-lookup"><span data-stu-id="00516-110">To be able to run DaRT remotely, make sure that the helpdesk agent computer and all computers that you might be troubleshooting remotely are on the same network.</span></span>

-   <span data-ttu-id="00516-111">Avant de déployer le DaRT en production, vous pouvez commencer par créer un environnement de laboratoire pour le test.</span><span class="sxs-lookup"><span data-stu-id="00516-111">Before you roll out DaRT into production, you can first build a lab environment for testing.</span></span> <span data-ttu-id="00516-112">Un atelier de test doit inclure un minimum de deux ordinateurs, un pour agir en tant qu’administrateur informatique/agent du support technique et un pour agir en tant qu’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="00516-112">A test lab should include a minimum of two computers, one to act as the IT administrator/helpdesk agent computer and one to act as an end-user computer.</span></span> <span data-ttu-id="00516-113">Vous pouvez ou utiliser trois ordinateurs dans votre laboratoire si vous voulez séparer les responsabilités de l’administrateur informatique de celles de l’agent de support technique.</span><span class="sxs-lookup"><span data-stu-id="00516-113">Or, you can use three computers in your lab if you want to separate the IT administrator responsibilities from those of the helpdesk agent.</span></span>

## <span data-ttu-id="00516-114">Examiner les configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="00516-114">Review the supported configurations</span></span>


<span data-ttu-id="00516-115">Prenez connaissance des informations sur les configurations prises en charge de Microsoft Diagnostics and Recovery Tools (DaRT) 7 prises en charge pour vérifier que les ordinateurs que vous avez sélectionnés pour l’installation d’un client ou d’une fonctionnalité répondent à la configuration minimale requise en matière de matériel et de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="00516-115">You should review the Microsoft Diagnostics and Recovery Toolset (DaRT)7 Supported Configurations information to confirm that the computers you have selected for client or feature installation meet the minimum hardware and operating system requirements.</span></span>

[<span data-ttu-id="00516-116">Configurations prises en charge par DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="00516-116">DaRT 7.0 Supported Configurations</span></span>](dart-70-supported-configurations-dart-7.md)

## <span data-ttu-id="00516-117">Plan de création de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="00516-117">Plan for creating the DaRT recovery image</span></span>


<span data-ttu-id="00516-118">Lorsque vous créez l’image de récupération DaRT, vous devez choisir les outils à inclure dans l’image.</span><span class="sxs-lookup"><span data-stu-id="00516-118">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="00516-119">Lorsque vous prenez cette décision, rappelez-vous que les utilisateurs finaux peuvent avoir accès occasionnellement aux différents outils DaRT.</span><span class="sxs-lookup"><span data-stu-id="00516-119">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="00516-120">Lorsque vous créez l’image de récupération, vous devez également indiquer si vous souhaitez inclure d’autres pilotes ou fichiers.</span><span class="sxs-lookup"><span data-stu-id="00516-120">When you create the recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="00516-121">Déterminez les emplacements des pilotes ou fichiers supplémentaires que vous voulez inclure dans l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="00516-121">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="00516-122">Prenez en compte les conditions préalables et d’autres recommandations en matière de planification pour la création de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="00516-122">You should be aware of the prerequisites and other additional planning recommendations for creating the DaRT recovery image.</span></span>

[<span data-ttu-id="00516-123">Planification pour créer l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="00516-123">Planning to Create the DaRT 7.0 Recovery Image</span></span>](planning-to-create-the-dart-70-recovery-image.md)

## <span data-ttu-id="00516-124">Planifier l’enregistrement et le déploiement de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="00516-124">Plan for saving and deploying the DaRT recovery image</span></span>


<span data-ttu-id="00516-125">Plusieurs méthodes peuvent être utilisées pour enregistrer et déployer l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="00516-125">Several methods can be used to save and deploy the DaRT recovery image.</span></span> <span data-ttu-id="00516-126">Lorsque vous déterminez la méthode à utiliser, examinez les avantages et inconvénients de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="00516-126">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="00516-127">Par ailleurs, réfléchissez à la façon dont vous souhaitez utiliser DaRT au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="00516-127">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="00516-128">**Remarques**  Vous souhaiterez peut-être utiliser plusieurs méthodes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="00516-128">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="00516-129">Par exemple, vous pouvez démarrer dans DaRT à partir d’une partition distante dans la plupart des cas, et disposer d’un lecteur flash USB dans le cas où l’ordinateur de l’utilisateur final ne peut pas se connecter au réseau.</span><span class="sxs-lookup"><span data-stu-id="00516-129">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

[<span data-ttu-id="00516-130">Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="00516-130">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## <span data-ttu-id="00516-131">Autres ressources pour planifier le déploiement de DaRT</span><span class="sxs-lookup"><span data-stu-id="00516-131">Other resources for Planning to Deploy DaRT</span></span>


[<span data-ttu-id="00516-132">Planification de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="00516-132">Planning for DaRT 7.0</span></span>](planning-for-dart-70-new-ia.md)

 

 






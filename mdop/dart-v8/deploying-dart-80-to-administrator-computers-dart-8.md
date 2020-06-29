---
title: Déploiement de DaRT8.0 sur les ordinateurs des administrateurs
description: Déploiement de DaRT8.0 sur les ordinateurs des administrateurs
author: dansimp
ms.assetid: f918ead8-742e-464a-8bf6-1fcedde66cae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0ab001f612f2257ecbd77c39319cc99c17d36197
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810367"
---
# <span data-ttu-id="21625-103">Déploiement de DaRT8.0 sur les ordinateurs des administrateurs</span><span class="sxs-lookup"><span data-stu-id="21625-103">Deploying DaRT 8.0 to Administrator Computers</span></span>


<span data-ttu-id="21625-104">Avant de commencer le déploiement de Microsoft Diagnostics and Recovery Tools (DaRT) 8,0, consultez la configuration requise pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="21625-104">Before you begin the deployment of Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, review the requirements for your environment.</span></span> <span data-ttu-id="21625-105">Cela inclut la configuration matérielle requise pour l’installation de DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="21625-105">This includes the hardware requirements for installing DaRT 8.0.</span></span> <span data-ttu-id="21625-106">Pour plus d’informations sur la configuration matérielle et logicielle requise pour DaRT, voir [Configurations prises en charge par dart 8,0](dart-80-supported-configurations-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="21625-106">For more information about DaRT hardware and software requirements, see [DaRT 8.0 Supported Configurations](dart-80-supported-configurations-dart-8.md).</span></span>

<span data-ttu-id="21625-107">Les rubriques de cette section peuvent être utilisées pour vous aider à déployer DaRT dans votre entreprise en fonction de votre environnement et de votre stratégie de déploiement.</span><span class="sxs-lookup"><span data-stu-id="21625-107">The topics in this section can be used to help you deploy DaRT in your enterprise based on your environment and deployment strategy.</span></span>

## <span data-ttu-id="21625-108">Déploiement de DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="21625-108">Deploy DaRT 8.0</span></span>


<span data-ttu-id="21625-109">Vous pouvez utiliser le fichier d’installation Windows pour DaRT pour installer DaRT sur un ordinateur que vous utiliserez pour la première création de l’image de récupération DaRT, puis résoudre les problèmes liés aux ordinateurs des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="21625-109">You can use the Windows Installer file for DaRT to install DaRT on a computer that you will use to first create the DaRT recovery image and then troubleshoot and fix end-user computers.</span></span> <span data-ttu-id="21625-110">Souvent, au sein d’une organisation, vous pouvez installer uniquement sur l’ordinateur d’administration la fonctionnalité DaRT dont vous avez besoin pour créer une image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="21625-110">Frequently, across an organization, you might install on the administrator computer only the DaRT functionality that you need to create a DaRT recovery image.</span></span> <span data-ttu-id="21625-111">Sur l’ordinateur de l’administrateur du support technique, vous pouvez ensuite installer uniquement la fonctionnalité DaRT dont vous avez besoin pour résoudre un problème d’ordinateur, tel que la visionneuse de connexion à distance DaRT et l’analyseur d’incident.</span><span class="sxs-lookup"><span data-stu-id="21625-111">Then, on a help desk administrator’s computer, you might install only the DaRT functionality that you must have to troubleshoot a problem computer, such as the DaRT Remote Connection Viewer and the Crash Analyzer.</span></span>

<span data-ttu-id="21625-112">Outre le fonctionnement manuel du fichier d’installation Windows pour l’installation de DaRT, vous pouvez également installer DaRT à l’invite de commandes pour prendre en charge des systèmes de déploiement de logiciels d’entreprise tels que SystemCenterConfigurationManager2012.</span><span class="sxs-lookup"><span data-stu-id="21625-112">In addition to manually running the Windows Installer file to install DaRT, you can also install DaRT at the command prompt to support enterprise software deployment systems such as SystemCenterConfigurationManager2012.</span></span>

[<span data-ttu-id="21625-113">Procédure de déploiement de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="21625-113">How to Deploy DaRT 8.0</span></span>](how-to-deploy-dart-80-dart-8.md)

## <span data-ttu-id="21625-114">Modification, réparation ou suppression du DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="21625-114">Change, repair, or remove DaRT 8.0</span></span>


<span data-ttu-id="21625-115">Vous pouvez modifier, réparer ou supprimer l’installation de DaRT en double-cliquant sur le fichier d’installation de DaRT, puis en cliquant sur le bouton correspondant à l’action que vous souhaitez exécuter ou par le biais du panneau de configuration Windows.</span><span class="sxs-lookup"><span data-stu-id="21625-115">You can change, repair, or remove the DaRT installation by double-clicking the DaRT installation file and then clicking the button that corresponds to the action that you want to perform or through the Windows Control Panel.</span></span>

[<span data-ttu-id="21625-116">Procédure pour modifier, réparer ou supprimer DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="21625-116">How to Change, Repair, or Remove DaRT 8.0</span></span>](how-to-change-repair-or-remove-dart-80-dart-8.md)

## <span data-ttu-id="21625-117">Obtention de la 8,0 DaRT</span><span class="sxs-lookup"><span data-stu-id="21625-117">How to get DaRT 8.0</span></span>


<span data-ttu-id="21625-118">Pour obtenir le logiciel DaRT, reportez-vous à la rubrique [obtention de MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="21625-118">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="21625-119">Autres ressources pour le déploiement de la 8,0 DaRT sur des ordinateurs d’administration</span><span class="sxs-lookup"><span data-stu-id="21625-119">Other resources for deploying the DaRT 8.0 to administrator computers</span></span>


[<span data-ttu-id="21625-120">Déploiement de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="21625-120">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 






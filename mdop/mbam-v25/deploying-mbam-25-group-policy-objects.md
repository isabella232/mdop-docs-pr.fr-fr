---
title: Déploiement d'objets de stratégie de groupe MBAM2.5
description: Déploiement d'objets de stratégie de groupe MBAM2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810524"
---
# <span data-ttu-id="8d4ff-103">Déploiement d'objets de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8d4ff-103">Deploying MBAM 2.5 Group Policy Objects</span></span>


<span data-ttu-id="8d4ff-104">Pour déployer MBAM, vous devez définir les paramètres de stratégie de groupe définissant les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8d4ff-104">To deploy MBAM, you have to set Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="8d4ff-105">Pour effectuer cette tâche, vous devez copier les modèles de stratégie de groupe MBAM sur un serveur ou une station de travail capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou la gestion avancée des stratégies de groupe (AGPM), puis de modifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="8d4ff-105">To complete this task, you must copy the MBAM Group Policy Templates to a server or workstation that are capable of running Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM), and then edit the settings.</span></span>

<span data-ttu-id="8d4ff-106">**Important**  Ne modifiez pas les paramètres de stratégie de groupe du nœud **BitLocker Drive Encryption** , ou MBAM ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="8d4ff-106">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="8d4ff-107">Lorsque vous configurez les paramètres de stratégie de groupe dans le nœud **MDOP MBAM (gestion du BitLocker)** , MBAM configure automatiquement les paramètres de **chiffrement de lecteur BitLocker** pour vous.</span><span class="sxs-lookup"><span data-stu-id="8d4ff-107">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

## <span data-ttu-id="8d4ff-108">Copie des modèles de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8d4ff-108">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="8d4ff-109">Avant d’installer le client MBAM, vous devez copier des objets de stratégie de groupe spécifiques MBAM (GPO) sur la station de travail de gestion.</span><span class="sxs-lookup"><span data-stu-id="8d4ff-109">Before you install the MBAM Client, you must copy MBAM-specific Group Policy Objects (GPOs) to the Management Workstation.</span></span> <span data-ttu-id="8d4ff-110">Ces objets de stratégie de groupe définissent des paramètres d’implémentation MBAM pour le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8d4ff-110">These GPOs define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="8d4ff-111">Vous pouvez copier les modèles de stratégie de groupe sur n’importe quel serveur ou station de travail, qui est un ordinateur client ou un serveur Windows pris en charge, et qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="8d4ff-111">You can copy the Group Policy templates to any server or workstation that is a supported Windows server or client computer and that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="8d4ff-112">Copie des modèles de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8d4ff-112">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

## <span data-ttu-id="8d4ff-113">Modification des paramètres de l’objet de stratégie de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="8d4ff-113">Editing MBAM 2.0 GPO settings</span></span>


<span data-ttu-id="8d4ff-114">Après avoir créé les objets de stratégie de groupe nécessaires, vous devez déployer les paramètres de stratégie de groupe MBAM sur les ordinateurs clients de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8d4ff-114">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span> <span data-ttu-id="8d4ff-115">Pour afficher et créer des objets de stratégie de groupe, vous devez avoir installé la console de gestion des stratégies de groupe (GPMC) ou la gestion de la stratégie de groupe avancée.</span><span class="sxs-lookup"><span data-stu-id="8d4ff-115">To view and create GPOs, you must have Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) installed.</span></span>

[<span data-ttu-id="8d4ff-116">Modification des paramètres de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8d4ff-116">Editing the MBAM 2.5 Group Policy Settings</span></span>](editing-the-mbam-25-group-policy-settings.md)

## <span data-ttu-id="8d4ff-117">Affichage ou masquage du panneau de configuration MBAM du panneau de configuration Windows</span><span class="sxs-lookup"><span data-stu-id="8d4ff-117">Showing or hiding the MBAM Control Panel in Windows Control Panel</span></span>


<span data-ttu-id="8d4ff-118">Dans la mesure où MBAM propose un panneau de configuration MBAM personnalisé qui peut remplacer le panneau de configuration Windows BitLocker par défaut, vous pouvez également choisir d’afficher ou de masquer le panneau de configuration BitLocker par défaut auprès des utilisateurs finaux à l’aide de paramètres de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8d4ff-118">Since MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to show or hide the default BitLocker Control Panel from end users by using Group Policy settings.</span></span>

[<span data-ttu-id="8d4ff-119">Masquage de l'élément de chiffrement de lecteur BitLocker par défaut dans le Panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="8d4ff-119">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## <span data-ttu-id="8d4ff-120">Autres ressources pour le déploiement d’objets de stratégie de groupe MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="8d4ff-120">Other Resources for deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="8d4ff-121">Déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8d4ff-121">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

## <span data-ttu-id="8d4ff-122">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="8d4ff-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8d4ff-123">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="8d4ff-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8d4ff-124">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8d4ff-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 






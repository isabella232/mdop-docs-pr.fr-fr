---
title: Déploiement d'objets de stratégie de groupe MBAM1.0
description: Déploiement d'objets de stratégie de groupe MBAM1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808622"
---
# <span data-ttu-id="5a8be-103">Déploiement d'objets de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="5a8be-103">Deploying MBAM 1.0 Group Policy Objects</span></span>


<span data-ttu-id="5a8be-104">Pour réussir le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM), vous devez d’abord déterminer les stratégies de groupe que vous utiliserez dans votre implémentation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a8be-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of MBAM.</span></span> <span data-ttu-id="5a8be-105">Pour plus d’informations sur les différentes stratégies disponibles, voir [planification des exigences de la stratégie de groupe MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5a8be-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="5a8be-106">Une fois que vous avez déterminé les stratégies que vous allez utiliser, vous devez utiliser le modèle de stratégie de groupe MBAM 1,0 pour créer et déployer un ou plusieurs objets de stratégie de groupe (GPO) incluant les paramètres de stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a8be-106">When you have determined the policies that you are going to use, you must use the MBAM 1.0 Group Policy template to create and deploy one or more Group Policy objects (GPO) that include the MBAM policy settings.</span></span>

## <span data-ttu-id="5a8be-107">Installer le modèle de stratégie de groupe MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5a8be-107">Install the MBAM 1.0 Group Policy template</span></span>


<span data-ttu-id="5a8be-108">Outre la fourniture de fonctionnalités relatives au serveur de MBAM, l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="5a8be-108">In addition to providing server-related features of MBAM, the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="5a8be-109">Vous pouvez installer ce modèle sur n’importe quel ordinateur qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="5a8be-109">You can install this template on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="5a8be-110">Installation du modèle de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="5a8be-110">How to Install the MBAM 1.0 Group Policy Template</span></span>](how-to-install-the-mbam-10-group-policy-template.md)

## <span data-ttu-id="5a8be-111">Déploiement des paramètres de stratégie de groupe de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5a8be-111">Deploy MBAM 1.0 Group Policy settings</span></span>


<span data-ttu-id="5a8be-112">Après avoir créé les objets de stratégie de groupe nécessaires, vous devez déployer les paramètres de stratégie de groupe MBAM sur les ordinateurs clients de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5a8be-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="5a8be-113">Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="5a8be-113">How to Edit MBAM 1.0 GPO Settings</span></span>](how-to-edit-mbam-10-gpo-settings.md)

## <span data-ttu-id="5a8be-114">Afficher l’MBAM panneau de configuration dans Windows</span><span class="sxs-lookup"><span data-stu-id="5a8be-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="5a8be-115">Comme MBAM propose un panneau de configuration MBAM personnalisé qui peut remplacer le panneau de configuration Windows BitLocker par défaut, vous pouvez également choisir de masquer le panneau de configuration BitLocker par défaut aux utilisateurs finaux à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5a8be-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="5a8be-116">Masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows</span><span class="sxs-lookup"><span data-stu-id="5a8be-116">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## <span data-ttu-id="5a8be-117">Autres ressources pour le déploiement d’objets de stratégie de groupe MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5a8be-117">Other resources for deploying MBAM 1.0 Group Policy Objects</span></span>


[<span data-ttu-id="5a8be-118">Déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="5a8be-118">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 






---
title: Déploiement d'objets de stratégie de groupe MBAM2.0
description: Déploiement d'objets de stratégie de groupe MBAM2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809989"
---
# <span data-ttu-id="03eac-103">Déploiement d'objets de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="03eac-103">Deploying MBAM 2.0 Group Policy Objects</span></span>


<span data-ttu-id="03eac-104">Pour réussir le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM), vous devez d’abord déterminer les stratégies de groupe que vous utiliserez dans votre implémentation de l’administration et de la surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="03eac-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="03eac-105">Pour plus d’informations sur les différentes stratégies disponibles, voir [planification des exigences de la stratégie de groupe MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="03eac-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="03eac-106">Lorsque vous déterminez les stratégies que vous allez utiliser, vous devez créer et déployer un ou plusieurs objets de stratégie de groupe qui incluent les paramètres de stratégie pour MBAM à l’aide du modèle de stratégie de groupe MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="03eac-106">When you have determined the policies that you are going to use, you then must create and deploy one or more Group Policy Objects (GPO) that include the policy settings for MBAM by using the MBAM 2.0 Group Policy template.</span></span>

## <span data-ttu-id="03eac-107">Installer le modèle de stratégie de groupe MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="03eac-107">Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="03eac-108">Outre les fonctionnalités d’administration et de surveillance de Microsoft BitLocker associées au serveur, l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="03eac-108">In addition to the server-related Microsoft BitLocker Administration and Monitoring features, the server setup application includes a MBAM Group Policy template.</span></span> <span data-ttu-id="03eac-109">Ce modèle peut être installé sur n’importe quel ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="03eac-109">This template can be installed on any computer able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="03eac-110">Installation du modèle de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="03eac-110">How to Install the MBAM 2.0 Group Policy Template</span></span>](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## <span data-ttu-id="03eac-111">Déploiement des paramètres de stratégie de groupe de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="03eac-111">Deploy MBAM 2.0 Group Policy Settings</span></span>


<span data-ttu-id="03eac-112">Après avoir créé les objets de stratégie de groupe nécessaires, vous devez déployer les paramètres de stratégie de groupe MBAM sur les ordinateurs clients de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="03eac-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="03eac-113">Procédure de modification des paramètres d'objet de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="03eac-113">How to Edit MBAM 2.0 GPO Settings</span></span>](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## <span data-ttu-id="03eac-114">Afficher l’MBAM panneau de configuration dans Windows</span><span class="sxs-lookup"><span data-stu-id="03eac-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="03eac-115">Comme MBAM propose un panneau de configuration MBAM personnalisé qui peut remplacer le panneau de configuration Windows BitLocker par défaut, vous pouvez également choisir de masquer le panneau de configuration BitLocker par défaut aux utilisateurs finaux à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="03eac-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="03eac-116">Comment masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows</span><span class="sxs-lookup"><span data-stu-id="03eac-116">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## <span data-ttu-id="03eac-117">Autres ressources pour le déploiement d’objets de stratégie de groupe MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="03eac-117">Other Resources for Deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="03eac-118">Déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="03eac-118">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 






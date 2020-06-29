---
title: Installation du modèle de stratégie de groupe MBAM2.0
description: Installation du modèle de stratégie de groupe MBAM2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811645"
---
# <span data-ttu-id="27816-103">Installation du modèle de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="27816-103">How to Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="27816-104">Outre les fonctionnalités d’administration et de surveillance de l’application Microsoft BitLocker associées au serveur, l’application de configuration du serveur inclut un modèle de stratégie de groupe d’administration et de surveillance de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="27816-104">In addition to the server-related Microsoft BitLocker Administration and Monitoring (MBAM) features, the server setup application includes an Microsoft BitLocker Administration and Monitoring Group Policy template.</span></span> <span data-ttu-id="27816-105">Ce modèle peut être installé sur n’importe quel ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou la gestion avancée des stratégies de groupe (AGPM).</span><span class="sxs-lookup"><span data-stu-id="27816-105">This template can be installed on any computer capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="27816-106">Les étapes suivantes expliquent comment installer le modèle de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="27816-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="27816-107">**Remarques**  Vérifiez que vous utilisez la configuration de 32 bits sur les serveurs 32 bits et la configuration 64 bits sur les serveurs 64.</span><span class="sxs-lookup"><span data-stu-id="27816-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="27816-108">Pour installer le modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="27816-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="27816-109">Sur le serveur sur lequel vous souhaitez installer MBAM, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="27816-109">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="27816-110">Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="27816-110">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="27816-111">Lisez et acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="27816-111">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="27816-112">Par défaut, toutes les fonctionnalités d’administration et de contrôle Microsoft BitLocker sont sélectionnées pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="27816-112">By default, all Microsoft BitLocker Administration and Monitoring features are selected for installation.</span></span> <span data-ttu-id="27816-113">Désactivez toutes les options de fonctionnalité sauf pour le **modèle de stratégie**, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="27816-113">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="27816-114">**Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes.</span><span class="sxs-lookup"><span data-stu-id="27816-114">**Note** The installation wizard checks the prerequisites for your installation and displays prerequisites that are missing.</span></span> <span data-ttu-id="27816-115">Si toutes les conditions préalables sont remplies, l’installation continue.</span><span class="sxs-lookup"><span data-stu-id="27816-115">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="27816-116">Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="27816-116">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="27816-117">Une fois que toutes les conditions préalables sont remplies, l’installation reprend.</span><span class="sxs-lookup"><span data-stu-id="27816-117">Once all prerequisites are met, the installation will resume.</span></span>

     

5.  <span data-ttu-id="27816-118">Pour obtenir des instructions détaillées sur la manière d’installer les modèles, voir [Comment télécharger et déployer des modèles de stratégie de groupe MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="27816-118">For specific steps about how and where to install the templates, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

6.  <span data-ttu-id="27816-119">Lorsque l’Assistant Configuration de l’administration et de la surveillance de Microsoft BitLocker affiche les pages d’installation pour les fonctionnalités sélectionnées, cliquez sur **Terminer** pour fermer MBAM.</span><span class="sxs-lookup"><span data-stu-id="27816-119">After the Microsoft BitLocker Administration and Monitoring Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="27816-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27816-120">Related topics</span></span>


[<span data-ttu-id="27816-121">Déploiement d'objets de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="27816-121">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 






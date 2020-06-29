---
title: Installation du modèle de stratégie de groupe MBAM1.0
description: Installation du modèle de stratégie de groupe MBAM1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811094"
---
# <span data-ttu-id="b72b9-103">Installation du modèle de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="b72b9-103">How to Install the MBAM 1.0 Group Policy Template</span></span>


<span data-ttu-id="b72b9-104">Outre les fonctionnalités liées au serveur de l’administration et de la surveillance de BitLocker Microsoft (MBAM), l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="b72b9-104">In addition to the server-related features of Microsoft BitLocker Administration and Monitoring (MBAM), the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="b72b9-105">Vous pouvez installer ce modèle sur n’importe quel ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="b72b9-105">You can install this template on any computer that is capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="b72b9-106">Les étapes suivantes expliquent comment installer le modèle de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="b72b9-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="b72b9-107">**Remarques**  Vérifiez que vous utilisez la configuration de 32 bits sur les serveurs 32 bits et la configuration 64 bits sur les serveurs 64.</span><span class="sxs-lookup"><span data-stu-id="b72b9-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="b72b9-108">Pour installer le modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="b72b9-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="b72b9-109">Démarrez l’Assistant Installation de MBAM; dans la page Bienvenue, cliquez sur **installer** .</span><span class="sxs-lookup"><span data-stu-id="b72b9-109">Start the MBAM installation wizard; then, click **Install** on the Welcome page.</span></span>

2.  <span data-ttu-id="b72b9-110">Lisez et acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="b72b9-110">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="b72b9-111">Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="b72b9-111">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="b72b9-112">Désactivez toutes les options de fonctionnalité sauf pour le **modèle de stratégie**, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="b72b9-112">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="b72b9-113">**Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes.</span><span class="sxs-lookup"><span data-stu-id="b72b9-113">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="b72b9-114">Si toutes les conditions préalables sont remplies, l’installation continue.</span><span class="sxs-lookup"><span data-stu-id="b72b9-114">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="b72b9-115">Si un prérequis manquant est détecté, vous devez résoudre le prérequis manquant, puis cliquez **à nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="b72b9-115">If a missing prerequisite is detected, you must resolve the missing prerequisite and then click **Check prerequisites again**.</span></span> <span data-ttu-id="b72b9-116">Une fois que toutes les conditions préalables sont remplies, l’installation reprend.</span><span class="sxs-lookup"><span data-stu-id="b72b9-116">Once all prerequisites are met, the installation will resume.</span></span>

     

4.  <span data-ttu-id="b72b9-117">À l’issue de l’Assistant Installation de MBAM, cliquez sur **Terminer** pour fermer MBAM de configuration des fonctionnalités sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="b72b9-117">After the MBAM Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="b72b9-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b72b9-118">Related topics</span></span>


[<span data-ttu-id="b72b9-119">Déploiement d'objets de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="b72b9-119">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 






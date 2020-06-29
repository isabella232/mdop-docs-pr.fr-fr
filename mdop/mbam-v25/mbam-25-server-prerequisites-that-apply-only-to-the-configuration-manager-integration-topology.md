---
title: Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager
description: Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804321"
---
# <span data-ttu-id="9b3ea-103">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9b3ea-103">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="9b3ea-104">Si vous installez la fonctionnalité d’administration et de surveillance de BitLocker (MBAM) 2,5 à l’aide de la fonctionnalité d’intégration de System Center Configuration Manager, vous devez remplir les conditions préalables décrites dans cette rubrique, en plus de celles dans [MBAM 2,5 Server Prerequisites pour les topologies d’intégration autonome et Configuration Manager](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="9b3ea-104">If you are installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 by using the System Center Configuration Manager Integration feature, you must complete the prerequisites described in this topic, in addition to those in [MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span></span> <span data-ttu-id="9b3ea-105">Vous devez également créer ou modifier des fichiers. mof nécessaires pour la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9b3ea-105">You must also create or modify .mof files that are needed for the Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="9b3ea-106">Conditions préalables pour le composant Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9b3ea-106">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="9b3ea-107">Si vous configurez MBAM avec la topologie d’intégration System Center Configuration Manager, vous devez effectuer les conditions préalables supplémentaires requises pour Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9b3ea-107">If you are configuring MBAM with the System Center Configuration Manager Integration topology, you must complete additional prerequisites that are required for Configuration Manager.</span></span>

[<span data-ttu-id="9b3ea-108">Conditions préalables pour le composant Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9b3ea-108">Prerequisites for the Configuration Manager Integration Feature</span></span>](prerequisites-for-the-configuration-manager-integration-feature.md)

## <span data-ttu-id="9b3ea-109">Modifier le fichier Configuration. mof</span><span class="sxs-lookup"><span data-stu-id="9b3ea-109">Edit the Configuration.mof file</span></span>


<span data-ttu-id="9b3ea-110">Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez modifier le fichier Configuration. mof pour SystemCenter2012 ConfigurationManager et Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="9b3ea-110">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager Reports, you have to edit the Configuration.mof file for SystemCenter2012 ConfigurationManager and Microsoft System Center Configuration Manager 2007.</span></span>

[<span data-ttu-id="9b3ea-111">Modifier le fichier Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="9b3ea-111">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="9b3ea-112">Créer ou modifier le fichier SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="9b3ea-112">Create or edit the Sms\_def.mof file</span></span>


<span data-ttu-id="9b3ea-113">Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker dans les rapports du gestionnaire de configuration MBAM, vous devez créer ou modifier le fichier SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="9b3ea-113">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager Reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="9b3ea-114">Si vous utilisez SystemCenter2012 ConfigurationManager, vous devez créer le fichier.</span><span class="sxs-lookup"><span data-stu-id="9b3ea-114">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="9b3ea-115">Dans Configuration Manager 2007, le fichier existe déjà, vous devez donc modifier le fichier existant, mais pas le remplacer.</span><span class="sxs-lookup"><span data-stu-id="9b3ea-115">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span>

[<span data-ttu-id="9b3ea-116">Créer ou modifier le fichier SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="9b3ea-116">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file-mbam-25.md)


## <span data-ttu-id="9b3ea-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b3ea-117">Related topics</span></span>


[<span data-ttu-id="9b3ea-118">Préparation de votre environnement pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="9b3ea-118">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="9b3ea-119">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="9b3ea-119">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="9b3ea-120">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="9b3ea-120">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="9b3ea-121">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="9b3ea-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9b3ea-122">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="9b3ea-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="9b3ea-123">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="9b3ea-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>





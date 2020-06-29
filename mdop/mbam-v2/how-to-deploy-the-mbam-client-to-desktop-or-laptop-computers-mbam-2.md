---
title: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
description: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804656"
---
# <span data-ttu-id="b7ca0-103">Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables</span><span class="sxs-lookup"><span data-stu-id="b7ca0-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="b7ca0-104">Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b7ca0-104">The Microsoft BitLocker Administration and Monitoring (MBAM) client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="b7ca0-105">Le client BitLocker peut être intégré à une organisation en déployant le client par le biais d’un système de distribution de logiciels électronique, tel que les services de domaine Active Directory ou MicrosoftSystemCenterConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="b7ca0-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfigurationManager.</span></span>

<span data-ttu-id="b7ca0-106">**Remarques**  Pour vérifier la configuration système requise pour le client d’administration et de surveillance de BitLocker, voir [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="b7ca0-106">**Note** To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

 

**<span data-ttu-id="b7ca0-107">Pour déployer le client MBAM sur un ordinateur portable ou de bureau</span><span class="sxs-lookup"><span data-stu-id="b7ca0-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="b7ca0-108">Recherchez les fichiers d’installation du client MBAM fournis avec le logiciel MBAM.</span><span class="sxs-lookup"><span data-stu-id="b7ca0-108">Locate the MBAM client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="b7ca0-109">Utilisez les services de domaine Active Directory ou un outil de déploiement de logiciels d’entreprise tel que MicrosoftSystemCenterConfigurationManager pour déployer le package Windows Installer sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="b7ca0-109">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfigurationManager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="b7ca0-110">Pour exécuter le fichier d’installation du client MBAM, vous pouvez configurer les paramètres de distribution ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b7ca0-110">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="b7ca0-111">Après l’installation, le client MBAM applique les paramètres de stratégie de groupe qui sont reçus par un contrôleur de domaine pour commencer à effectuer le chiffrement et les fonctions de gestion de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b7ca0-111">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="b7ca0-112">Pour plus d’informations sur les paramètres de stratégie de groupe de MBAM, reportez-vous [à la planification des exigences de stratégie de groupe MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="b7ca0-112">For more information about MBAM group policy settings, see [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span></span>

    <span data-ttu-id="b7ca0-113">**Important**  Le client MBAM ne démarrera pas les actions de chiffrement BitLocker si une connexion de protocole de bureau à distance est active.</span><span class="sxs-lookup"><span data-stu-id="b7ca0-113">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="b7ca0-114">Toutes les connexions de console distante doivent être fermées avant le début du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b7ca0-114">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="b7ca0-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7ca0-115">Related topics</span></span>


[<span data-ttu-id="b7ca0-116">Déploiement du client MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="b7ca0-116">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 






---
title: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
description: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810578"
---
# <span data-ttu-id="8a4bc-103">Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables</span><span class="sxs-lookup"><span data-stu-id="8a4bc-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="8a4bc-104">Cette rubrique explique comment déployer le client MBAM sur les ordinateurs des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="8a4bc-104">This topic explains how to deploy the MBAM Client to end users’ computers.</span></span> <span data-ttu-id="8a4bc-105">Vous pouvez déployer le client MBAM par le biais d’un système de distribution de logiciels électronique, tel que Active Directory Domain Services ou MicrosoftSystemCenterConfiguration Manager.</span><span class="sxs-lookup"><span data-stu-id="8a4bc-105">You can deploy the MBAM Client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfiguration Manager.</span></span>

<span data-ttu-id="8a4bc-106">Pour déployer le client MBAM dans le cadre d’un déploiement Windows, voir [Comment activer BitLocker en utilisant MBAM dans le cadre d’un déploiement Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="8a4bc-106">To deploy the MBAM Client as part of a Windows deployment, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span></span>

<span data-ttu-id="8a4bc-107">Avant de démarrer le déploiement du client MBAM, passez [en revue les configurations MBAM 2,5 prises en charge](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="8a4bc-107">Before you start the MBAM Client deployment, review the [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="8a4bc-108">Pour déployer le client MBAM sur un ordinateur portable ou de bureau</span><span class="sxs-lookup"><span data-stu-id="8a4bc-108">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="8a4bc-109">Recherchez les fichiers d’installation du client MBAM fournis avec le logiciel MBAM.</span><span class="sxs-lookup"><span data-stu-id="8a4bc-109">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="8a4bc-110">Utilisez les services de domaine Active Directory ou un outil de déploiement de logiciels d’entreprise tel que MicrosoftSystemCenterConfiguration Manager pour déployer le package Windows Installer sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="8a4bc-110">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfiguration Manager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="8a4bc-111">Pour exécuter le fichier d’installation du client MBAM, vous pouvez configurer les paramètres de distribution ou les paramètres de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8a4bc-111">Configure the distribution settings or Group Policy settings to run the MBAM Client installation file.</span></span>

    <span data-ttu-id="8a4bc-112">Après l’installation, le client MBAM applique les paramètres de stratégie de groupe qui sont reçus d’un contrôleur de domaine pour commencer le chiffrement et les fonctions de gestion du lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8a4bc-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker Drive Encryption and management functions.</span></span>

    <span data-ttu-id="8a4bc-113">**Important**  Le client MBAM ne démarre pas les actions de chiffrement de lecteur BitLocker si une connexion de protocole de bureau à distance est active.</span><span class="sxs-lookup"><span data-stu-id="8a4bc-113">**Important** The MBAM Client does not start BitLocker Drive Encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="8a4bc-114">Toutes les connexions de console distante doivent être fermées et un utilisateur doit être connecté à une session de console physique avant le début du chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8a4bc-114">All remote console connections must be closed and a user must be logged on to a physical console session before BitLocker Drive Encryption begins.</span></span>

     


## <span data-ttu-id="8a4bc-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a4bc-115">Related topics</span></span>
[<span data-ttu-id="8a4bc-116">Déploiement du client MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8a4bc-116">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="8a4bc-117">Planification du déploiement de clients MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8a4bc-117">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

 

## <span data-ttu-id="8a4bc-118">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="8a4bc-118">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8a4bc-119">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="8a4bc-119">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8a4bc-120">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8a4bc-120">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 






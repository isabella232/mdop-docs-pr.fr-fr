---
title: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
description: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811219"
---
# <span data-ttu-id="d26d7-103">Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables</span><span class="sxs-lookup"><span data-stu-id="d26d7-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="d26d7-104">Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d26d7-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="d26d7-105">Le client MBAM peut être intégré à une organisation en déployant le client par le biais d’outils, tels que les services de domaine Active Directory (AD FS) ou un outil de déploiement de logiciels d’entreprise tel que MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="d26d7-105">The MBAM Client can be integrated into an organization by deploying the client through tools, such as Active Directory Domain Services or an enterprise software deployment tool such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

<span data-ttu-id="d26d7-106">**Remarques**  Pour vérifier la configuration système requise pour le client MBAM, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="d26d7-106">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

**<span data-ttu-id="d26d7-107">Pour déployer le client MBAM sur un ordinateur portable ou de bureau</span><span class="sxs-lookup"><span data-stu-id="d26d7-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="d26d7-108">Recherchez les fichiers d’installation du client MBAM fournis avec le logiciel MBAM.</span><span class="sxs-lookup"><span data-stu-id="d26d7-108">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="d26d7-109">Déployez le package Windows Installer sur les ordinateurs cibles à l’aide des services de domaine Active Directory ou d’un outil déploiement de logiciels d’entreprise, tels que les ConfigurationManagers MicrosoftSystemCenter2012.</span><span class="sxs-lookup"><span data-stu-id="d26d7-109">Deploy the Windows Installer package to target computers by using Active Directory Domain Services or an enterprise software deployment tool, such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

    <span data-ttu-id="d26d7-110">**Remarques**  Vous ne devez pas utiliser de stratégie de groupe pour déployer le package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d26d7-110">**Note** You should not use Group Policy to deploy the Windows Installer package.</span></span>

     

3.  <span data-ttu-id="d26d7-111">Pour exécuter le fichier d’installation du client MBAM, vous pouvez configurer les paramètres de distribution ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d26d7-111">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="d26d7-112">Après l’installation, le client MBAM applique les paramètres de stratégie de groupe qui sont reçus par un contrôleur de domaine pour commencer à effectuer le chiffrement et les fonctions de gestion de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d26d7-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="d26d7-113">Pour plus d’informations sur les paramètres de stratégie de groupe de MBAM, reportez-vous [à la planification des exigences de stratégie de groupe MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d26d7-113">For more information about MBAM Group Policy settings, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

    <span data-ttu-id="d26d7-114">**Important**  Le client MBAM ne démarrera pas les actions de chiffrement BitLocker si une connexion de protocole de bureau à distance est active.</span><span class="sxs-lookup"><span data-stu-id="d26d7-114">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="d26d7-115">Toutes les connexions de console distante doivent être fermées avant le début du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d26d7-115">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="d26d7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d26d7-116">Related topics</span></span>


[<span data-ttu-id="d26d7-117">Déploiement du client MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="d26d7-117">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 






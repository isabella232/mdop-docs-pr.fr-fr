---
title: Déploiement de MBAM avec Configuration Manager
description: Déploiement de MBAM avec Configuration Manager
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809965"
---
# <span data-ttu-id="9a8d2-103">Déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9a8d2-103">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="9a8d2-104">Les procédures suivantes décrivent le déploiement de l’administration et de la surveillance de l’utilisation de BitLocker (MBAM) Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012 (en anglais) par utilisantle configuration recommandée, décrite dans la rubrique [mise en route de MBAM avec Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="9a8d2-104">The following procedures describe how to deploy Microsoft BitLocker Administration and Monitoring (MBAM) with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager by usingthe recommended configuration, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="9a8d2-105">La configuration recommandée consiste à installer les fonctionnalités d’administration et de surveillance sur un ou plusieurs serveurs d’administration et de surveillance Microsoft BitLocker, et à installer Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012 sur un serveur distinct.</span><span class="sxs-lookup"><span data-stu-id="9a8d2-105">The recommended configuration is to install the Administration and Monitoring features on one or more Microsoft BitLocker Administration and Monitoring servers, and install Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager on a separate server.</span></span>

<span data-ttu-id="9a8d2-106">Avant de commencer l’installation, assurez-vous que vous remplissez les conditions préalables et la configuration matérielle et logicielle requise pour l’installation d’MBAM avec Configuration Manager en passant en revue la [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="9a8d2-106">Before you start the installation, ensure that you have met the prerequisites and hardware and software requirements for installing MBAM with Configuration Manager by reviewing [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="9a8d2-107">Si vous devez réinstaller MBAM avec la topologie Configuration Manager, vous devez d’abord supprimer certains objets de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9a8d2-107">If you ever have to reinstall MBAM with the Configuration Manager topology, you will need to remove certain Configuration Manager objects first.</span></span> <span data-ttu-id="9a8d2-108">Pour plus d’informations, consultez l’article de la [base de connaissances](https://go.microsoft.com/fwlink/?LinkId=286306) .</span><span class="sxs-lookup"><span data-stu-id="9a8d2-108">Read the [Knowledge Base article](https://go.microsoft.com/fwlink/?LinkId=286306) for more information.</span></span>

<span data-ttu-id="9a8d2-109">Les étapes permettant d’installer MBAM avec Configuration Manager sont regroupées dans les catégories suivantes.</span><span class="sxs-lookup"><span data-stu-id="9a8d2-109">The steps to install MBAM with Configuration Manager are grouped into the following categories.</span></span> <span data-ttu-id="9a8d2-110">Suivez les étapes de chaque catégorie pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="9a8d2-110">Complete the steps for each category to complete the installation.</span></span>

## <span data-ttu-id="9a8d2-111">Création ou modification des fichiers mof</span><span class="sxs-lookup"><span data-stu-id="9a8d2-111">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="9a8d2-112">Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez modifier le fichier **Configuration. mof** , puis modifier ou créer le fichier Sms \ _def. mof, en fonction de la version de Configuration Manager que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="9a8d2-112">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the **Configuration.mof** file, and either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

[<span data-ttu-id="9a8d2-113">Création ou modification des fichiers mof</span><span class="sxs-lookup"><span data-stu-id="9a8d2-113">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

## <span data-ttu-id="9a8d2-114">Installation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9a8d2-114">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="9a8d2-115">Cette section présente les étapes à suivre pour installer les éléments suivants: MBAM sur le serveur Configuration Manager; les bases de données de récupération et d’audit sur le serveur de base de données; ainsi que les fonctionnalités d’administration et de surveillance du serveur sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="9a8d2-115">This section provides steps about how to install the following: MBAM on the Configuration Manager Server; the Recovery and Audit Databases on the Database Server; and the Administration and Monitoring Server features on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="9a8d2-116">Installation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9a8d2-116">How to Install MBAM with Configuration Manager</span></span>](how-to-install-mbam-with-configuration-manager.md)

## <span data-ttu-id="9a8d2-117">Valider l’installation de la fonctionnalité MBAM Server sur le serveur Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9a8d2-117">How to Validate the MBAM Server Feature Installation on the Configuration Manager Server</span></span>


<span data-ttu-id="9a8d2-118">Lorsque l’installation de l’administration et du suivi de BitLocker est terminée, vérifiez que l’installation a correctement configuré toutes les fonctionnalités MBAM nécessaires pour le serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9a8d2-118">When the Microsoft BitLocker Administration and Monitoring installation is complete, validate that the installation has successfully set up all the necessary MBAM features required for the Configuration Manager Server.</span></span>

[<span data-ttu-id="9a8d2-119">Validation de l'installation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9a8d2-119">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## <span data-ttu-id="9a8d2-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a8d2-120">Related topics</span></span>


[<span data-ttu-id="9a8d2-121">Utilisation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9a8d2-121">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 






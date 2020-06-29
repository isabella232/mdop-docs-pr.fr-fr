---
title: Installation de MBAM Language Update sur des serveurs distribués
description: Installation de MBAM Language Update sur des serveurs distribués
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811310"
---
# <span data-ttu-id="f4261-103">Installation de MBAM Language Update sur des serveurs distribués</span><span class="sxs-lookup"><span data-stu-id="f4261-103">How to Install the MBAM Language Update on Distributed Servers</span></span>


<span data-ttu-id="f4261-104">L’administration et l’analyse de BitLocker Microsoft (MBAM) incluent quatre rôles de serveur qui peuvent être exécutés sur un ou plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="f4261-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="f4261-105">Toutefois, seules deux fonctionnalités du serveur MBAM requièrent la mise à jour pour la prise en charge de l’installation de la version de MBAM 1,0 Language et du modèle de stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4261-105">However, only two MBAM Server features require the update to support the installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="f4261-106">Dans les configurations avec les fonctionnalités de MBAM Server installées sur plusieurs ordinateurs, seules les fonctionnalités serveur suivantes doivent être mises à jour:</span><span class="sxs-lookup"><span data-stu-id="f4261-106">In configurations with the MBAM Server features installed on multiple computers, only the following server features need to be updated:</span></span>

-   <span data-ttu-id="f4261-107">Rapports de conformité et d’audit de MBAM</span><span class="sxs-lookup"><span data-stu-id="f4261-107">The MBAM Compliance and Audit Reports</span></span>

-   <span data-ttu-id="f4261-108">Serveur d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="f4261-108">The MBAM Administration and Monitoring Server</span></span>

<span data-ttu-id="f4261-109">**Important**  Les fonctionnalités du serveur MBAM doivent être mises à jour dans cet ordre: les rapports de conformité et d’audit d’abord, puis le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="f4261-109">**Important** The MBAM server features must be updated in this order: Compliance and Audit Reports first, and then the Administration and Monitoring Server.</span></span> <span data-ttu-id="f4261-110">Les modèles de stratégie de groupe MBAM peuvent être mis à jour à tout moment sans vous soucier de la séquence.</span><span class="sxs-lookup"><span data-stu-id="f4261-110">The MBAM Group Policy templates can be updated at any time without concern for sequence.</span></span>

 

**<span data-ttu-id="f4261-111">Pour installer la mise à jour de langue MBAM sur la fonctionnalité serveur de rapport d’audit et de conformité MBAM</span><span class="sxs-lookup"><span data-stu-id="f4261-111">To install the MBAM Language Update on the MBAM Compliance and Audit Report Server feature</span></span>**

1.  <span data-ttu-id="f4261-112">Sur l’ordinateur exécutant la fonctionnalité de compatibilité et d’audit de MBAM, recherchez et exécutez l’Assistant Configuration de la mise à jour de MBAM (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="f4261-112">On the computer running the MBAM Compliance and Audit Report feature, locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span>

2.  <span data-ttu-id="f4261-113">Terminez l’Assistant pour les rapports de conformité et d’audit, puis fermez l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="f4261-113">Complete the wizard for the Compliance and Audit Reports and then close the wizard.</span></span>

**<span data-ttu-id="f4261-114">Pour installer la mise à jour de la langue MBAM sur la fonctionnalité serveur d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="f4261-114">To install the MBAM Language Update on the MBAM Administration and Monitoring Server feature</span></span>**

1.  <span data-ttu-id="f4261-115">Sur l’ordinateur qui exécute la fonctionnalité d’administration et de surveillance de MBAM, ouvrez la console de gestion des services Internet (IIS), accédez à **sites**, puis arrêtez le site Web d’administration et de contrôle Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f4261-115">On the computer that is running the MBAM Administration and Monitoring feature, open the Internet Information Services (IIS) management console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="f4261-116">Choisissez de modifier les liaisons pour le site Web MBAM, puis modifiez les liaisons du site.</span><span class="sxs-lookup"><span data-stu-id="f4261-116">Choose to edit the bindings for the MBAM website, and then modify the bindings of the site.</span></span> <span data-ttu-id="f4261-117">Par exemple, changez le port de 443 vers 9443.</span><span class="sxs-lookup"><span data-stu-id="f4261-117">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="f4261-118">Recherchez et exécutez l’Assistant Configuration de la mise à jour des langues de MBAM (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="f4261-118">Locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span> <span data-ttu-id="f4261-119">Suivez la procédure de l’Assistant pour la fonctionnalité d’administration et de surveillance du serveur, puis fermez l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="f4261-119">Complete the wizard for the Administration and Monitoring Server feature and then close the wizard.</span></span>

4.  <span data-ttu-id="f4261-120">Après avoir effectué la mise à niveau de la base de données du serveur, ouvrez la console de gestion IIS et passez en revue les liaisons du site Web d’administration et de contrôle Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f4261-120">After you upgrade the server database, open IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="f4261-121">Supprimez l’ancienne liaison et assurez-vous que la liaison restante dispose du nom d’hôte, du certificat et du numéro de port appropriés pour la configuration d’entreprise MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4261-121">Delete the old binding and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="f4261-122">Redémarrez le site Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4261-122">Restart the MBAM web site.</span></span>

7.  <span data-ttu-id="f4261-123">Testez la fonctionnalité du site Web MBAM:</span><span class="sxs-lookup"><span data-stu-id="f4261-123">Test the MBAM web site functionality:</span></span>

    -   <span data-ttu-id="f4261-124">Ouvrez l’interface Web MBAM et assurez-vous que vous pouvez obtenir une clé de récupération pour un client.</span><span class="sxs-lookup"><span data-stu-id="f4261-124">Open the MBAM web interface and ensure that you can obtain a recovery key for a client.</span></span>

    -   <span data-ttu-id="f4261-125">Mettre en place un chiffrement d’un ordinateur client nouveau ou déchiffré manuellement.</span><span class="sxs-lookup"><span data-stu-id="f4261-125">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="f4261-126">**Remarques**  Le client MBAM s’ouvre uniquement s’il peut communiquer avec la base de données de récupération et de matériel.</span><span class="sxs-lookup"><span data-stu-id="f4261-126">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="f4261-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4261-127">Related topics</span></span>


[<span data-ttu-id="f4261-128">Déploiement de MBAM1.0 Language Release Update</span><span class="sxs-lookup"><span data-stu-id="f4261-128">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 






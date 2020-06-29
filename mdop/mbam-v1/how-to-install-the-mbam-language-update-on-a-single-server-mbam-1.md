---
title: Installation de MBAM Language Update sur un serveur unique
description: Installation de MBAM Language Update sur un serveur unique
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810745"
---
# <span data-ttu-id="74be6-103">Installation de MBAM Language Update sur un serveur unique</span><span class="sxs-lookup"><span data-stu-id="74be6-103">How to Install the MBAM Language Update on a Single Server</span></span>


<span data-ttu-id="74be6-104">L’administration et l’analyse de BitLocker Microsoft (MBAM) incluent quatre rôles de serveur qui peuvent être exécutés sur un ou plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="74be6-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="74be6-105">Toutefois, seules deux fonctionnalités du serveur MBAM requièrent la mise à jour pour la prise en charge de l’installation de la version MBAM 1,0 et du modèle de stratégie MBAM.</span><span class="sxs-lookup"><span data-stu-id="74be6-105">However, only two MBAM Server features require the update to support installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="74be6-106">Pour mettre à jour les trois fonctionnalités MBAM requises devant être installées sur un ordinateur, suivez la procédure décrite dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="74be6-106">To update all three of the required MBAM features to be installed on one computer, perform the steps described in this topic.</span></span>

**<span data-ttu-id="74be6-107">Pour installer la mise à jour de langue MBAM sur un serveur unique</span><span class="sxs-lookup"><span data-stu-id="74be6-107">To install the MBAM language update on a single server</span></span>**

1.  <span data-ttu-id="74be6-108">Ouvrez la console de gestion d’Internet Information Services (IIS), accédez à **sites**, puis arrêtez le site Web d’administration et de contrôle Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="74be6-108">Open the Internet Information Services (IIS) Management Console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="74be6-109">Modifiez les liaisons pour le site Web MBAM, puis modifiez temporairement les liaisons du site.</span><span class="sxs-lookup"><span data-stu-id="74be6-109">Edit the bindings for the MBAM website, and then temporarily modify the bindings of the site.</span></span> <span data-ttu-id="74be6-110">Par exemple, changez le port de 443 vers 9443.</span><span class="sxs-lookup"><span data-stu-id="74be6-110">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="74be6-111">Recherchez et exécutez l’Assistant Configuration de MBAM (MBAMsetup.exe), puis sélectionnez les trois fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="74be6-111">Locate and run the MBAM setup wizard (MBAMsetup.exe) and select the following three features:</span></span>

    1.  <span data-ttu-id="74be6-112">Rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="74be6-112">Compliance and Audit Reports</span></span>

    2.  <span data-ttu-id="74be6-113">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="74be6-113">Administration and Monitoring Server</span></span>

    3.  <span data-ttu-id="74be6-114">Modèles de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="74be6-114">Group Policy Templates</span></span>

    <span data-ttu-id="74be6-115">**Important**  Les fonctionnalités du serveur MBAM doivent être mises à jour dans l’ordre suivant: les rapports de conformité et d’audit d’abord, puis sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="74be6-115">**Important** The MBAM server features must be updated in the following order: Compliance and Audit Reports first, then Administration and Monitoring Server.</span></span> <span data-ttu-id="74be6-116">Les modèles de stratégie de groupe peuvent être mis à jour à tout moment sans vous soucier de la séquence.</span><span class="sxs-lookup"><span data-stu-id="74be6-116">The Group Policy templates can be updated at any time without concern for sequence.</span></span>

     

4.  <span data-ttu-id="74be6-117">Après avoir effectué la mise à niveau de la base de données du serveur, ouvrez la console de gestion IIS et passez en revue les liaisons du site Web d’administration et de contrôle Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="74be6-117">After you upgrade the server database, open the IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="74be6-118">Supprimez l’une des liaisons et assurez-vous que la liaison restante dispose du nom d’hôte, du certificat et du numéro de port appropriés pour la configuration d’entreprise MBAM.</span><span class="sxs-lookup"><span data-stu-id="74be6-118">Delete one of the bindings and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="74be6-119">Redémarrez le site Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="74be6-119">Restart the MBAM website.</span></span>

7.  <span data-ttu-id="74be6-120">Testez la fonctionnalité de site Web MBAM:</span><span class="sxs-lookup"><span data-stu-id="74be6-120">Test the MBAM website functionality:</span></span>

    -   <span data-ttu-id="74be6-121">Ouvrez l’interface Web MBAM et assurez-vous que vous pouvez récupérer une clé de récupération pour un client.</span><span class="sxs-lookup"><span data-stu-id="74be6-121">Open the MBAM web interface and ensure you can fetch a recovery key for a client.</span></span>

    -   <span data-ttu-id="74be6-122">Mettre en place un chiffrement d’un ordinateur client nouveau ou déchiffré manuellement.</span><span class="sxs-lookup"><span data-stu-id="74be6-122">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="74be6-123">**Remarques**  Le client MBAM s’ouvre uniquement s’il peut communiquer avec la base de données de récupération et de matériel.</span><span class="sxs-lookup"><span data-stu-id="74be6-123">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="74be6-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74be6-124">Related topics</span></span>


[<span data-ttu-id="74be6-125">Déploiement de MBAM1.0 Language Release Update</span><span class="sxs-lookup"><span data-stu-id="74be6-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 






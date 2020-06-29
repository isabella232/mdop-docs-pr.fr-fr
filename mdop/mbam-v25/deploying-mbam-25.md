---
title: Déploiement de MBAM2.5
description: Déploiement de MBAM2.5
author: dansimp
ms.assetid: 45403607-1f4d-42fe-8413-0d4da01808a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0cfa0a190530186211cd96884b2e32e9c65881f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811663"
---
# <span data-ttu-id="f87b9-103">Déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-103">Deploying MBAM 2.5</span></span>


<span data-ttu-id="f87b9-104">Utilisez les informations ci-dessous pour identifier les procédures à suivre afin de déployer et de configurer les fonctionnalités de serveur d’administration et de surveillance de Microsoft BitLocker (MBAM 2,5) pour effectuer une mise à niveau vers MBAM 2,5 de versions précédentes ou pour supprimer les fonctionnalités du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="f87b9-104">Use this information to identify the procedures you can follow to deploy and configure Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features to upgrade to MBAM 2.5 from previous versions, or to remove MBAM Server features.</span></span>

## <span data-ttu-id="f87b9-105">Informations de déploiement</span><span class="sxs-lookup"><span data-stu-id="f87b9-105">Deployment information</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f87b9-106">Description du sujet</span><span class="sxs-lookup"><span data-stu-id="f87b9-106">Topic description</span></span></th>
<th align="left"><span data-ttu-id="f87b9-107">Liens vers des rubriques</span><span class="sxs-lookup"><span data-stu-id="f87b9-107">Links to topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="f87b9-108">Options de topologie de déploiement.</span><span class="sxs-lookup"><span data-stu-id="f87b9-108">Deployment topology options.</span></span></p></li>
<li><p><span data-ttu-id="f87b9-109">Comment installer le logiciel serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="f87b9-109">How to install the MBAM Server software.</span></span></p></li>
<li><p><span data-ttu-id="f87b9-110">Comment configurer les fonctionnalités du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="f87b9-110">How to configure the MBAM Server features.</span></span></p></li>
</ul></td>
<td align="left"><p><a href="deploying-the-mbam-25-server-infrastructure.md" data-raw-source="[Deploying the MBAM 2.5 Server Infrastructure](deploying-the-mbam-25-server-infrastructure.md)"><span data-ttu-id="f87b9-111">Déploiement de l'infrastructure de serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-111">Deploying the MBAM 2.5 Server Infrastructure</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f87b9-112">Le téléchargement et le déploiement des modèles de stratégie de groupe MBAM requis pour gérer les clients MBAM et les stratégies de chiffrement BitLocker au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f87b9-112">How to download and deploy the MBAM Group Policy Templates, which are required to manage MBAM Clients and BitLocker encryption policies in the enterprise.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-25-group-policy-objects.md" data-raw-source="[Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md)"><span data-ttu-id="f87b9-113">Déploiement d'objets de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-113">Deploying MBAM 2.5 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f87b9-114">Comment utiliser les fichiers du programme d’installation du client MBAM pour déployer le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="f87b9-114">How to use the MBAM Client Windows Installer files to deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)"><span data-ttu-id="f87b9-115">Déploiement du client MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-115">Deploying the MBAM 2.5 Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f87b9-116">Liste de vérification qui peut vous aider à déployer les fonctionnalités du serveur MBAM et le client MBAM.</span><span class="sxs-lookup"><span data-stu-id="f87b9-116">Checklist that can assist you in deploying the MBAM Server features and MBAM Client.</span></span></p></td>
<td align="left"><p><a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"><span data-ttu-id="f87b9-117">Liste de contrôle du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-117">MBAM 2.5 Deployment Checklist</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f87b9-118">Comment mettre à niveau MBAM à partir de versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="f87b9-118">How to upgrade MBAM from previous versions.</span></span></p></td>
<td align="left"><p><a href="upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md" data-raw-source="[Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)"><span data-ttu-id="f87b9-119">Mise à niveau vers MBAM2.5 ou MBAM2.5 SP1 àpartir de versions antérieures</span><span class="sxs-lookup"><span data-stu-id="f87b9-119">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f87b9-120">Comment supprimer les fonctionnalités ou logiciels du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="f87b9-120">How to remove MBAM Server features or software.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="f87b9-121">Suppression du logiciel ou des composants serveur de MBAM</span><span class="sxs-lookup"><span data-stu-id="f87b9-121">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f87b9-122">Autres ressources pour le déploiement d’MBAM</span><span class="sxs-lookup"><span data-stu-id="f87b9-122">Other resources for deploying MBAM</span></span>


[<span data-ttu-id="f87b9-123">Microsoft BitLocker Administration and Monitoring2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-123">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="f87b9-124">Prise en main de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-124">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="f87b9-125">Planification de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-125">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

[<span data-ttu-id="f87b9-126">Opérations de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-126">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

[<span data-ttu-id="f87b9-127">Résolution des problèmes MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-127">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)

[<span data-ttu-id="f87b9-128">Document de référence technique pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="f87b9-128">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="f87b9-129">Déploiement de MBAM2.5 dans une configuration autonome</span><span class="sxs-lookup"><span data-stu-id="f87b9-129">Deploying MBAM 2.5 in a stand-alone configuration</span></span>](https://support.microsoft.com/kb/3046555)

## <span data-ttu-id="f87b9-130">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="f87b9-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f87b9-131">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="f87b9-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f87b9-132">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f87b9-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 






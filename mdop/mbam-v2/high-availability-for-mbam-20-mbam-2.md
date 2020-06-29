---
title: Haute disponibilité de MBAM2.0
description: Haute disponibilité de MBAM2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810728"
---
# <span data-ttu-id="009c4-103">Haute disponibilité de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="009c4-103">High Availability for MBAM 2.0</span></span>


<span data-ttu-id="009c4-104">Cette rubrique fournit des informations de base sur une installation hautement disponible de Microsoft BitLocker administration et analyse (MBAM).</span><span class="sxs-lookup"><span data-stu-id="009c4-104">This topic provides basic information about a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="009c4-105">Les scénarios de haute disponibilité ne sont pas entièrement pris en charge dans cette version de MBAM, ce qui signifie qu’ils ne sont pas décrits ici.</span><span class="sxs-lookup"><span data-stu-id="009c4-105">High-availability scenarios are not fully supported in this version of MBAM, so they are not described here.</span></span> <span data-ttu-id="009c4-106">Nous vous conseillons de rechercher des blogs et des forums connexes dans lesquels les utilisateurs décrivent la façon dont ils ont correctement configuré la haute disponibilité pour MBAM dans leur environnement.</span><span class="sxs-lookup"><span data-stu-id="009c4-106">It is recommended that you search related blogs and forums, where users describe how they have successfully configured high availability for MBAM in their environments.</span></span>

## <span data-ttu-id="009c4-107">Scénarios de haute disponibilité pour MBAM</span><span class="sxs-lookup"><span data-stu-id="009c4-107">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="009c4-108">L’administration et la surveillance de Microsoft BitLocker sont conçues pour être tolérantes aux pannes.</span><span class="sxs-lookup"><span data-stu-id="009c4-108">Microsoft BitLocker Administration and Monitoring is designed to be fault-tolerant.</span></span> <span data-ttu-id="009c4-109">Si un serveur devient indisponible, l’utilisateur ne doit pas être touché de façon négative.</span><span class="sxs-lookup"><span data-stu-id="009c4-109">If a server becomes unavailable, users should not be negatively affected.</span></span> <span data-ttu-id="009c4-110">Par exemple, si l’agent MBAM ne peut pas se connecter au serveur Web MBAM, les utilisateurs ne doivent pas être invités à effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="009c4-110">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="009c4-111">Lorsque vous planifiez votre installation de MBAM, prenez en compte les éléments suivants qui peuvent affecter la disponibilité du service MBAM:</span><span class="sxs-lookup"><span data-stu-id="009c4-111">When you plan your MBAM installation, consider the following items, which can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="009c4-112">Le chiffrement du lecteur et le mot de passe de récupération: si un mot de passe de récupération ne peut pas être de confiance, le chiffrement ne démarre pas sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="009c4-112">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption does not start on the client computer.</span></span>

-   <span data-ttu-id="009c4-113">Chargement des données d’état de conformité: si le serveur qui héberge le service de rapport d’état de conformité n’est pas disponible, les données de conformité ne restent pas actuelles.</span><span class="sxs-lookup"><span data-stu-id="009c4-113">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data does not remain current.</span></span>

-   <span data-ttu-id="009c4-114">Accès à la clé de récupération du support technique: si le support technique ne peut pas accéder aux informations de la base de données MBAM, l’assistance technique ne peut pas fournir de clés de récupération aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="009c4-114">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, the Help Desk cannot provide recovery keys to users.</span></span>

-   <span data-ttu-id="009c4-115">Disponibilité des rapports: si le serveur qui héberge les rapports de compatibilité et d’audit n’est pas disponible, les rapports ne seront pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="009c4-115">Availability of reports –If the server that hosts the Compliance and Audit Reports is not available, reports will not be available.</span></span>

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a><span data-ttu-id="009c4-116">Comment la sauvegarde MBAM utilise le service de cliché instantané de volume (VSS)</span><span class="sxs-lookup"><span data-stu-id="009c4-116">How the MBAM Backup Uses the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="009c4-117">MBAM 2.0 fournit un writer de service de cliché instantané de volume (VSS) appelé Microsoft BitLocker Management and Management Writer, qui facilite la sauvegarde de la base de données d’audit et de conformité et de la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="009c4-117">MBAM2.0 provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer, which facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="009c4-118">Le programme d’installation de MBAM Server Windows enregistre MBAM VSS Writer.</span><span class="sxs-lookup"><span data-stu-id="009c4-118">The MBAM Server Windows Installer registers the MBAM VSS Writer.</span></span> <span data-ttu-id="009c4-119">Tout échec de l’inscription du writer VSS entraîne la restauration de l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="009c4-119">Any failure during the VSS writer registration causes the MBAM Server installation to roll back.</span></span> <span data-ttu-id="009c4-120">Dans le cas où la base de données d’audit et de conformité, ainsi que la base de données de récupération, sont installées sur différents serveurs, une instance distincte de MBAM VSS Writer est inscrite sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="009c4-120">In a topology where the Compliance and Audit Database and the Recovery Database are installed on different servers, a separate instance of MBAM VSS Writer is registered on each server.</span></span> <span data-ttu-id="009c4-121">Le scripteur VSS MBAM dépend du writer SQL Server VSS.</span><span class="sxs-lookup"><span data-stu-id="009c4-121">The MBAM VSS Writer is dependent on the SQL Server VSS Writer.</span></span> <span data-ttu-id="009c4-122">Le writer SQL Server VSS est inscrit dans le cadre de l’installation de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="009c4-122">The SQL Server VSS Writer is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="009c4-123">Toute technologie de sauvegarde qui utilise des Writers VSS pour effectuer une sauvegarde peut découvrir le scripteur VSS MBAM.</span><span class="sxs-lookup"><span data-stu-id="009c4-123">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS Writer.</span></span>

## <span data-ttu-id="009c4-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="009c4-124">Related topics</span></span>


[<span data-ttu-id="009c4-125">Gestion de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="009c4-125">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)

 

 






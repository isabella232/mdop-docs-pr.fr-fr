---
title: Haute disponibilité de MBAM1.0
description: Haute disponibilité de MBAM1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811111"
---
# <span data-ttu-id="5a5e2-103">Haute disponibilité de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="5a5e2-103">High Availability for MBAM 1.0</span></span>


<span data-ttu-id="5a5e2-104">Cette rubrique décrit comment configurer une installation hautement disponible de Microsoft BitLocker administration et de la surveillance (MBAM).</span><span class="sxs-lookup"><span data-stu-id="5a5e2-104">This topic describes how to configure a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

## <span data-ttu-id="5a5e2-105">Scénarios de haute disponibilité pour MBAM</span><span class="sxs-lookup"><span data-stu-id="5a5e2-105">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="5a5e2-106">La surveillance et l’administration de BitLocker Microsoft (MBAM) sont conçues pour être tolérantes aux pannes.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-106">Microsoft BitLocker Administration and Monitoring (MBAM) is designed to be fault-tolerant.</span></span> <span data-ttu-id="5a5e2-107">Si un serveur devient indisponible, les utilisateurs ne doivent pas être touchés par le négatif.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-107">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="5a5e2-108">Par exemple, si l’agent MBAM ne peut pas se connecter au serveur Web MBAM, les utilisateurs ne doivent pas être invités à effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-108">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="5a5e2-109">Lorsque vous planifiez votre installation de MBAM, prenez en compte les problèmes suivants qui peuvent affecter la disponibilité du service MBAM:</span><span class="sxs-lookup"><span data-stu-id="5a5e2-109">When you plan your MBAM installation, consider the following concerns that can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="5a5e2-110">Chiffrement du lecteur et mot de passe de récupération: si un mot de passe de récupération ne peut pas être de confiance, le chiffrement ne démarrera pas sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-110">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption will not start on the client computer.</span></span>

-   <span data-ttu-id="5a5e2-111">Chargement des données d’état de conformité: si le serveur qui héberge le service de rapport d’état de conformité n’est pas disponible, les données de conformité ne seront pas conservées.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-111">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data will not remain current.</span></span>

-   <span data-ttu-id="5a5e2-112">Accès à la clé de récupération du support technique: si l’assistance ne peut pas accéder aux informations de la base de données MBAM, ils ne seront pas en mesure de fournir des clés de récupération aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-112">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, they will be unable to provide recovery keys to users.</span></span>

-   <span data-ttu-id="5a5e2-113">Disponibilité des rapports: les rapports ne seront pas disponibles si le serveur qui héberge les rapports de compatibilité et d’audit n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-113">Availability of reports – Reports will not be available if the server that hosts the Compliance and Audit Reports is not available.</span></span>

<span data-ttu-id="5a5e2-114">Le principal souci de la haute disponibilité MBAM est la disponibilité de la récupération de clé BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-114">The main concern for MBAM high availability is BitLocker key recovery availability.</span></span> <span data-ttu-id="5a5e2-115">Si le support technique ne peut pas fournir de clés de récupération, les utilisateurs qui sont verrouillés ne peuvent pas déverrouiller leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-115">If the help desk cannot provide recovery keys, users who are locked out cannot unlock their computers.</span></span> <span data-ttu-id="5a5e2-116">Pour éviter ce problème, envisagez d’implémenter des serveurs et bases de données Web redondants pour garantir une disponibilité élevée.</span><span class="sxs-lookup"><span data-stu-id="5a5e2-116">To avoid this problem, consider implementing redundant web servers and databases to ensure high availability.</span></span>

<span data-ttu-id="5a5e2-117">Pour plus d’informations sur l’évolutivité et la disponibilité de MBAM, voir le [livre blanc](https://go.microsoft.com/fwlink/p/?LinkId=229025) sur l’évolutivité d’MBAM ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .</span><span class="sxs-lookup"><span data-stu-id="5a5e2-117">For more information about MBAM scalability and high availability, see the [MBAM Scalability White Paper](https://go.microsoft.com/fwlink/p/?LinkId=229025) (https://go.microsoft.com/fwlink/p/?LinkId=229025).</span></span>

<span data-ttu-id="5a5e2-118">Pour obtenir des instructions générales sur la haute disponibilité de Microsoft SQL Server, voir [haute disponibilité](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .</span><span class="sxs-lookup"><span data-stu-id="5a5e2-118">For general guidance on high availability for Microsoft SQL Server, see [High Availability](https://go.microsoft.com/fwlink/p/?LinkId=221504) (https://go.microsoft.com/fwlink/p/?LinkId=221504).</span></span>

<span data-ttu-id="5a5e2-119">Pour obtenir des instructions générales sur la disponibilité et l’extensibilité pour les serveurs Web, voir [disponibilité et extensibilité](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .</span><span class="sxs-lookup"><span data-stu-id="5a5e2-119">For general guidance on availability and scalability for web servers, see [Availability and Scalability](https://go.microsoft.com/fwlink/p/?LinkId=221503) (https://go.microsoft.com/fwlink/p/?LinkId=221503).</span></span>

## <span data-ttu-id="5a5e2-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a5e2-120">Related topics</span></span>


[<span data-ttu-id="5a5e2-121">Gestion de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="5a5e2-121">Maintaining MBAM 1.0</span></span>](maintaining-mbam-10.md)

 

 






---
title: Gestion de MBAM1.0
description: Gestion de MBAM1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811357"
---
# <span data-ttu-id="0bce5-103">Gestion de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="0bce5-103">Maintaining MBAM 1.0</span></span>


<span data-ttu-id="0bce5-104">Après avoir effectué toutes les opérations de planification nécessaires, puis déployé le programme d’administration et de surveillance de BitLocker (MBAM), vous pouvez configurer MBAM pour qu’il s’exécute de manière très disponible lors de son utilisation pour gérer les opérations de chiffrement d’entreprise BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0bce5-104">After you complete all the necessary planning and then deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure MBAM to run in a highly available fashion while using it to manage enterprise BitLocker encryption operations.</span></span> <span data-ttu-id="0bce5-105">Les informations contenues dans cette section décrivent les options de haute disponibilité pour MBAM, ainsi que le déplacement des fonctionnalités de MBAM Server si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0bce5-105">The information in this section describes high availability options for MBAM, as well as how to move MBAM Server features if necessary.</span></span>

## <span data-ttu-id="0bce5-106">Pack d’administration MBAM</span><span class="sxs-lookup"><span data-stu-id="0bce5-106">MBAM Management Pack</span></span>


<span data-ttu-id="0bce5-107">Le pack d’administration MicrosoftSystemCenterOperationsManager pour MBAM est disponible en téléchargement dans le centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0bce5-107">The MicrosoftSystemCenterOperationsManager Management Pack for MBAM is available for download from the Microsoft Download Center.</span></span>

<span data-ttu-id="0bce5-108">Ce pack d’administration surveille les interactions critiques dans l’infrastructure côté serveur, telles que les connexions entre les services Web et les bases de données et les appels opérationnels entre les sites Web et leur service Web de support technique.</span><span class="sxs-lookup"><span data-stu-id="0bce5-108">This management pack monitors the critical interactions in the server-side infrastructure, such as the connections between the web services and databases and the operational calls between websites and their supportive web service.</span></span> <span data-ttu-id="0bce5-109">Il télécharge également les demandes entre les clients de bureau et leurs points de terminaison de service Web de réception correspondants.</span><span class="sxs-lookup"><span data-stu-id="0bce5-109">It also uploads the requests between desktop clients and their respective receiving web service endpoints.</span></span>

[<span data-ttu-id="0bce5-110">Pack d’administration et de surveillance Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="0bce5-110">Microsoft BitLocker Administration And Monitoring Management Pack</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## <span data-ttu-id="0bce5-111">Garantir une disponibilité élevée pour MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="0bce5-111">Ensure high availability for MBAM 1.0</span></span>


<span data-ttu-id="0bce5-112">MBAM est conçu pour être tolérant aux pannes.</span><span class="sxs-lookup"><span data-stu-id="0bce5-112">MBAM is designed to be fault-tolerant.</span></span> <span data-ttu-id="0bce5-113">Si un serveur devient indisponible, les utilisateurs ne doivent pas être touchés par le négatif.</span><span class="sxs-lookup"><span data-stu-id="0bce5-113">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="0bce5-114">Les informations contenues dans cette section peuvent être utilisées pour configurer une installation MBAM très disponible.</span><span class="sxs-lookup"><span data-stu-id="0bce5-114">The information in this section can be used to configure a highly available MBAM installation.</span></span>

[<span data-ttu-id="0bce5-115">Haute disponibilité de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="0bce5-115">High Availability for MBAM 1.0</span></span>](high-availability-for-mbam-10.md)

## <span data-ttu-id="0bce5-116">Déplacer les fonctionnalités de MBAM 1,0 vers un autre serveur</span><span class="sxs-lookup"><span data-stu-id="0bce5-116">Move MBAM 1.0 features to another server</span></span>


<span data-ttu-id="0bce5-117">Lorsque vous avez besoin de déplacer une fonctionnalité de MBAM Server d’un ordinateur serveur vers un autre, il existe un ordre spécifique et des étapes requises à suivre pour éviter la perte de productivité et de données.</span><span class="sxs-lookup"><span data-stu-id="0bce5-117">When you need to move an MBAM Server feature from one server computer to another, there is a specific order and required steps that you should follow to avoid loss of productivity or data.</span></span> <span data-ttu-id="0bce5-118">Cette section décrit les étapes à suivre pour déplacer une ou plusieurs fonctionnalités de MBAM Server vers un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0bce5-118">This section describes the steps that you should take to move one or more MBAM Server features to a different computer.</span></span>

[<span data-ttu-id="0bce5-119">Déplacement de composants MBAM1.0 vers un autre ordinateur</span><span class="sxs-lookup"><span data-stu-id="0bce5-119">How to Move MBAM 1.0 Features to Another Computer</span></span>](how-to-move-mbam-10-features-to-another-computer.md)

## <span data-ttu-id="0bce5-120">Autres ressources pour la mise à jour de MBAM</span><span class="sxs-lookup"><span data-stu-id="0bce5-120">Other resources for maintaining MBAM</span></span>


[<span data-ttu-id="0bce5-121">Opérations de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="0bce5-121">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 






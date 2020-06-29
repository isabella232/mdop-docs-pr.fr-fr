---
title: Identifier le nombre d'instances MED-V
description: Identifier le nombre d'instances MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810446"
---
# <span data-ttu-id="5be43-103">Identifier le nombre d'instances MED-V</span><span class="sxs-lookup"><span data-stu-id="5be43-103">Identify the Number of MED-V Instances</span></span>


<span data-ttu-id="5be43-104">Vous devez déterminer le nombre d’instances de MED-V et définir l’étendue de chaque instance pour pouvoir concevoir l’infrastructure du serveur.</span><span class="sxs-lookup"><span data-stu-id="5be43-104">You need to determine the number of MED-V instances, as well as define the scope for each instance so that you can design the server infrastructure.</span></span> <span data-ttu-id="5be43-105">Une instance MED-V inclut les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="5be43-105">A MED-V instance includes the following:</span></span>

-   <span data-ttu-id="5be43-106">Serveur MED-V et espaces de travail MED-V stockés sur le serveur, y compris les autorisations Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5be43-106">The MED-V server and the MED-V workspaces stored on the server, including Active Directory permissions.</span></span>

-   <span data-ttu-id="5be43-107">Une base de données SQL Server qui stocke des événements client.</span><span class="sxs-lookup"><span data-stu-id="5be43-107">A SQL Server database that stores client events.</span></span> <span data-ttu-id="5be43-108">Il est possible que la base de données soit partagée par plusieurs instances MED-V.</span><span class="sxs-lookup"><span data-stu-id="5be43-108">The database may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="5be43-109">Référentiel d’image pour les images MED-V compactées.</span><span class="sxs-lookup"><span data-stu-id="5be43-109">The image repository for the packed MED-V images.</span></span> <span data-ttu-id="5be43-110">Le référentiel est susceptible d’être partagé par plusieurs instances MED-V.</span><span class="sxs-lookup"><span data-stu-id="5be43-110">The repository may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="5be43-111">La console de gestion utilisée pour créer et empaqueter des images, et créer des espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="5be43-111">The management console used to create and pack images and to create MED-V workspaces.</span></span> <span data-ttu-id="5be43-112">La console ne peut pas être utilisée simultanément par plusieurs instances MED-V, mais elle peut être déconnectée d’un serveur MED-V, puis connectée à un serveur MED-V différent.</span><span class="sxs-lookup"><span data-stu-id="5be43-112">The console cannot be used simultaneously by multiple MED-V instances, but it can be disconnected from one MED-V server and then connected to a different MED-V server.</span></span>

-   <span data-ttu-id="5be43-113">Les clients MED-V qui reçoivent des espaces de travail MED-V et qui peuvent les utiliser à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="5be43-113">MED-V clients that receive MED-V workspaces, and authorization to use them, from the server.</span></span>

<span data-ttu-id="5be43-114">Les instances MED-V distinctes ne peuvent pas être intégrées ou partager des espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="5be43-114">Separate MED-V instances cannot be integrated or share MED-V workspaces.</span></span> <span data-ttu-id="5be43-115">Par conséquent, chaque instance supplémentaire décentralise la gestion de la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="5be43-115">Therefore, each additional instance decentralizes the virtualization management.</span></span>

## <span data-ttu-id="5be43-116">Déterminer le nombre d’instances MED-V requises</span><span class="sxs-lookup"><span data-stu-id="5be43-116">Determine the Number of MED-V Instances Required</span></span>


<span data-ttu-id="5be43-117">Commencez par supposer que vous utilisez une instance MED-V.</span><span class="sxs-lookup"><span data-stu-id="5be43-117">Start by assuming you are using one MED-V instance.</span></span> <span data-ttu-id="5be43-118">Prenez en compte les conditions suivantes et ajoutez des instances supplémentaires pour chaque condition qui s’appliquent à votre infrastructure.</span><span class="sxs-lookup"><span data-stu-id="5be43-118">Then, consider the following conditions, and add additional instances for each condition that applies to your infrastructure.</span></span>

-   <span data-ttu-id="5be43-119">Nombre d’utilisateurs pris en charge: chaque instance MED-V peut prendre en charge jusqu’à 5 000 de clients actifs simultanément.</span><span class="sxs-lookup"><span data-stu-id="5be43-119">Number of supported users—Each MED-V instance can support up to 5,000 concurrently active clients.</span></span> <span data-ttu-id="5be43-120">L’activation simultanée signifie que le client est en ligne avec le serveur MED-V et qu’il envoie des sondages au serveur pour les mises à jour de stratégie et d’image, ainsi que les événements.</span><span class="sxs-lookup"><span data-stu-id="5be43-120">Concurrently active means the client is online with the MED-V server and sending polls to the server for policy and image updates, as well as events.</span></span> <span data-ttu-id="5be43-121">Si votre infrastructure inclura plus de 5 000 utilisateurs actifs, ajoutez une instance pour chaque utilisateur 5 000.</span><span class="sxs-lookup"><span data-stu-id="5be43-121">If your infrastructure will include more than 5,000 active users, add one instance for every 5,000 users.</span></span>

-   <span data-ttu-id="5be43-122">Utilisateurs des domaines non approuvés: MED-V Server associe les autorisations d’espace de travail MED-V aux utilisateurs et/ou groupes Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5be43-122">Users in untrusted domains—The MED-V server associates MED-V workspace permissions with Active Directory users and/or groups.</span></span> <span data-ttu-id="5be43-123">Cela nécessite que les utilisateurs MED-V existent dans la limite de confiance du serveur MED-V.</span><span class="sxs-lookup"><span data-stu-id="5be43-123">This requires MED-V users to exist within the trust boundary of the MED-V server.</span></span> <span data-ttu-id="5be43-124">Ajoutez une instance MED-V pour chaque groupe d’utilisateurs MED-V figurant dans un domaine distinct et non fiable.</span><span class="sxs-lookup"><span data-stu-id="5be43-124">Add one MED-V instance for each group of MED-V users that is in a separate, untrusted domain.</span></span>

-   <span data-ttu-id="5be43-125">Clients dans les réseaux isolés: Déterminez si des clients résident dans des réseaux isolés et nécessitent par conséquent une instance MED-V distincte.</span><span class="sxs-lookup"><span data-stu-id="5be43-125">Clients in isolated networks—Determine whether any clients reside in networks that are isolated and therefore require a separate MED-V instance.</span></span> <span data-ttu-id="5be43-126">Par exemple, les organisations isolent souvent les réseaux de laboratoire des réseaux de production.</span><span class="sxs-lookup"><span data-stu-id="5be43-126">For example, organizations often isolate lab networks from production networks.</span></span> <span data-ttu-id="5be43-127">Ajoutez une instance MED-V pour chaque réseau isolé qui contient des clients MED-V.</span><span class="sxs-lookup"><span data-stu-id="5be43-127">Add a MED-V instance for each isolated network that will contain MED-V clients.</span></span>

-   <span data-ttu-id="5be43-128">Exigences organisationnelles: l’organisation risque de nécessiter la gestion d’un groupe de clients par une instance MED-V distincte pour des raisons de sécurité, par exemple lorsque des applications sensibles sont transmises uniquement à un ensemble restreint d’utilisateurs au sein d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="5be43-128">Organizational requirements—The organization may require that a group of clients be managed by a separate MED-V instance for security reasons, such as when sensitive applications are delivered only to a restricted set of users within a domain.</span></span> <span data-ttu-id="5be43-129">Par exemple, le service Payroll risque de refuser aux utilisateurs d’autres services l’accès à l’instance MED-V qui stocke une stratégie de traitement de la paie.</span><span class="sxs-lookup"><span data-stu-id="5be43-129">For example, the payroll department may deny users from other departments access to the MED-V instance that stores policy for payroll processing.</span></span> <span data-ttu-id="5be43-130">De plus, si l’organisation utilise un modèle de gestion distribuée, une instance MED-V séparée est susceptible d’être requise pour chaque groupe d’entreprise disposant de clients MED-V pour permettre au groupe de gérer son propre environnement virtualisé.</span><span class="sxs-lookup"><span data-stu-id="5be43-130">Additionally, if the organization uses a distributed management model, a separate MED-V instance may be required for each business group having MED-V clients in order to enable the group to manage its own virtualized environment.</span></span> <span data-ttu-id="5be43-131">Ajoutez une instance MED-V pour chaque exigence d’organisation distincte.</span><span class="sxs-lookup"><span data-stu-id="5be43-131">Add one MED-V instance for each separate organizational requirement.</span></span>

-   <span data-ttu-id="5be43-132">Considérations juridiques: les problèmes liés à la sécurité nationale ou à la confidentialité et à la législation fiduciaire peuvent nécessiter une séparation de certaines données ou empêcher d’autres données de traverser les frontières nationales.</span><span class="sxs-lookup"><span data-stu-id="5be43-132">Legal considerations—National security or privacy issues and fiduciary laws could require the separation of certain data or prevent other data from crossing national borders.</span></span> <span data-ttu-id="5be43-133">Le cas échéant, ajoutez d’autres instances MED-V pour répondre à ce besoin.</span><span class="sxs-lookup"><span data-stu-id="5be43-133">If necessary, add additional MED-V instances to address this need.</span></span>

<span data-ttu-id="5be43-134">Après avoir déterminé le nombre d’instances MED-V requises pour votre infrastructure, ainsi que le raisonnement pour chacun d’eux, donnez un nom à chaque instance.</span><span class="sxs-lookup"><span data-stu-id="5be43-134">After you determine the number of MED-V instances required for your infrastructure, as well as the reasoning for each one, provide a name for each instance.</span></span>

 

 






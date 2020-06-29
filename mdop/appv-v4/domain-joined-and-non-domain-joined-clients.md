---
title: Clients joints au domaine et non joints au domaine
description: Clients joints au domaine et non joints au domaine
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808873"
---
# <span data-ttu-id="bf823-103">Clients joints au domaine et non joints au domaine</span><span class="sxs-lookup"><span data-stu-id="bf823-103">Domain-Joined and Non-Domain-Joined Clients</span></span>


<span data-ttu-id="bf823-104">Le client de bureau App-V peut être configuré pour autoriser la connexion à un réseau, qu’il s’agisse d’un domaine ou d’un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="bf823-104">The App-V Desktop Client can be configured to allow connection to a network regardless of whether the client is domain joined or non-domain joined.</span></span>

## <span data-ttu-id="bf823-105">Clients liés à un domaine</span><span class="sxs-lookup"><span data-stu-id="bf823-105">Domain-Joined Clients</span></span>


<span data-ttu-id="bf823-106">Les clients appartenant à un domaine, mais en dehors du réseau interne, peuvent communiquer avec l’infrastructure App-V via une connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="bf823-106">Clients that are domain joined, but outside the internal network, can communicate with the App-V infrastructure by using a VPN connection.</span></span> <span data-ttu-id="bf823-107">Lorsque vous souhaitez offrir aux utilisateurs la possibilité de quitter le réseau interne tout en continuant à communiquer dans une infrastructure App-V, votre environnement nécessite une configuration très légère.</span><span class="sxs-lookup"><span data-stu-id="bf823-107">When you want to provide users the ability to leave the internal network but still communicate in an App-V infrastructure, your environment requires very little setup.</span></span> <span data-ttu-id="bf823-108">Dans la mesure où les utilisateurs font déjà partie du domaine, il vous suffit de vérifier que les informations d’identification mises en cache sont prises en charge sur le client.</span><span class="sxs-lookup"><span data-stu-id="bf823-108">Because the users are already part of the domain, you simply need to ensure that Cached Credentials are supported on the client.</span></span> <span data-ttu-id="bf823-109">Il s’agit de la configuration par défaut, et les modifications apportées à ce paramètre peuvent être effectuées à partir de stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="bf823-109">This is the default configuration, and any changes to this setting can be accomplished from Group Policies.</span></span>

<span data-ttu-id="bf823-110">Comme indiqué dans le guide des pratiques recommandées pour l’application-V, l’utilisateur tente d’envoyer son ticket utilisateur à l’infrastructure App-V pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="bf823-110">As mentioned in the App-V Security Best Practices Guide, the user will attempt to send their user ticket to the App-V infrastructure for authentication.</span></span> <span data-ttu-id="bf823-111">Si le ticket est arrivé à expiration, il revient à utiliser NTLM et aux informations d’identification mises en cache sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bf823-111">If the ticket is expired, it will revert to using NTLM and the cached credentials on the computer.</span></span> <span data-ttu-id="bf823-112">Pour autoriser l’itinérance, les administrateurs doivent s’assurer que le serveur de publication qui est consulté en interne est disponible au même nom de manière externe pour que les noms soient résolus correctement.</span><span class="sxs-lookup"><span data-stu-id="bf823-112">To allow roaming, administrators must ensure that the publishing server being accessed internally is available at the same name externally for the names to resolve properly.</span></span>

## <span data-ttu-id="bf823-113">Clients non liés à un domaine</span><span class="sxs-lookup"><span data-stu-id="bf823-113">Non-Domain-Joined Clients</span></span>


<span data-ttu-id="bf823-114">Les clients qui ne sont pas connectés au domaine et qui doivent communiquer dans l’infrastructure App-V doivent être configurés pour s’assurer que l’authentification auprès de l’infrastructure App-V est réussie.</span><span class="sxs-lookup"><span data-stu-id="bf823-114">Clients that are non-domain joined but need to communicate in the App-V infrastructure must be configured to ensure that authentication to the App-V infrastructure is successful.</span></span> <span data-ttu-id="bf823-115">Le client de bureau App-V n’autorise pas le processus de mise à jour de la publication, de sorte que le client doit être configuré pour présenter les informations d’identification appropriées au serveur de gestion de l’application-V.</span><span class="sxs-lookup"><span data-stu-id="bf823-115">The App-V Desktop Client does not permit prompting for the publishing refresh process, so the client must be configured to present the proper credentials to the App-V Management Server.</span></span>

<span data-ttu-id="bf823-116">Le serveur de publication qui est configuré pour l’actualisation de la publication à partir du client autre qu’un domaine joint, exige que le nom externe auquel les clients accèdent soit configuré en tant que nom commun ou autre nom (SAN) sur le certificat du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="bf823-116">The publishing server, which is configured for publishing refresh from the non-domain joined client, requires that the external name that clients access is configured as the common name or a subject alternate name (SAN) on the publishing server’s certificate.</span></span>

## <span data-ttu-id="bf823-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf823-117">Related topics</span></span>


[<span data-ttu-id="bf823-118">Comment affecter les informations d’identification appropriées pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf823-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

[<span data-ttu-id="bf823-119">Comment affecter les informations d’identification appropriées pour Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf823-119">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 






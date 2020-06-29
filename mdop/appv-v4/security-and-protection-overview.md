---
title: Vue d'ensemble de la sécurité et de la protection
description: Vue d'ensemble de la sécurité et de la protection
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806394"
---
# <span data-ttu-id="ffb76-103">Vue d'ensemble de la sécurité et de la protection</span><span class="sxs-lookup"><span data-stu-id="ffb76-103">Security and Protection Overview</span></span>


<span data-ttu-id="ffb76-104">Microsoft Application Virtualization 4.5 fournit les fonctionnalités de sécurité améliorées suivantes pour vous aider à planifier et à implémenter une stratégie de déploiement plus sécurisée:</span><span class="sxs-lookup"><span data-stu-id="ffb76-104">Microsoft Application Virtualization4.5 provides the following enhanced security features to help you plan and implement a more secure deployment strategy:</span></span>

-   <span data-ttu-id="ffb76-105">La virtualisation des applications prend désormais en charge le protocole TLS (Transport Layer Security) à l’aide de certificats X. 509 v3.</span><span class="sxs-lookup"><span data-stu-id="ffb76-105">Application Virtualization now supports Transport Layer Security (TLS) using X.509 V3 certificates.</span></span> <span data-ttu-id="ffb76-106">Dans la mesure où un certificat de serveur a été configuré pour la gestion des applications planifiées ou le serveur de diffusion en continu, l’installation sera sécurisée par défaut en utilisant le protocole RTSP sur le port 322.</span><span class="sxs-lookup"><span data-stu-id="ffb76-106">Provided that a server certificate has been provisioned to the planned Application Virtualization Management or Streaming Server, the installation will default to secure, using the RTSPS protocol over port 322.</span></span> <span data-ttu-id="ffb76-107">L’utilisation de RTSPs vous permet de garantir que les communications entre les serveurs de virtualisation des applications et les clients de virtualisation d’application sont signées et chiffrées.</span><span class="sxs-lookup"><span data-stu-id="ffb76-107">Using RTSPS ensures that communication between the Application Virtualization Servers and the Application Virtualization Clients is signed and encrypted.</span></span> <span data-ttu-id="ffb76-108">Si aucun certificat n’est attribué au serveur lors de l’installation du serveur de virtualisation des applications, la communication sera définie sur RTSP sur le port 554.</span><span class="sxs-lookup"><span data-stu-id="ffb76-108">If no certificate is assigned to the server during the Application Virtualization Server installation, the communication will be set to RTSP over port 554.</span></span>

    **<span data-ttu-id="ffb76-109">Note de sécurité:</span><span class="sxs-lookup"><span data-stu-id="ffb76-109">Security Note:</span></span>**

    <span data-ttu-id="ffb76-110">Pour garantir la sécurité de l’installation du serveur, vous devez vous assurer que les ports RTSP sont désactivés, même si tous les packages sont configurés pour utiliser les RTSP.</span><span class="sxs-lookup"><span data-stu-id="ffb76-110">To help provide a secure setup of the server, you must make sure that RTSP ports are disabled even if you have all packages configured to use RTSPS.</span></span>

    <span data-ttu-id="ffb76-111">Si vous ajoutez des certificats de sécurité au serveur après l’installation du serveur, il est possible que le serveur ne détecte pas les certificats.</span><span class="sxs-lookup"><span data-stu-id="ffb76-111">If you add security certificates to the server after installing the server, the server might not detect the certificates.</span></span> <span data-ttu-id="ffb76-112">Pour garantir la détection des certificats de sécurité, redémarrez le serveur une fois que vous avez ajouté les certificats.</span><span class="sxs-lookup"><span data-stu-id="ffb76-112">To help ensure security certificate detection, restart the server after adding the certificates.</span></span>

-   <span data-ttu-id="ffb76-113">Le client doit être configuré pour utiliser le même protocole et port que le serveur, mais il ne sera pas en mesure de communiquer avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="ffb76-113">The client must be configured to use the same protocol and port as the server, or it will not be able to communicate with the server.</span></span> <span data-ttu-id="ffb76-114">Le client doit également approuver l’émetteur du certificat et est fourni avec plusieurs des fournisseurs principaux dans son magasin de racines de confiance.</span><span class="sxs-lookup"><span data-stu-id="ffb76-114">The client must also trust the issuer of the certificate and ships with several of the primary providers in its Trusted Root Store.</span></span> <span data-ttu-id="ffb76-115">Vous pouvez utiliser des certificats auto-signés, mais vous devrez mettre à jour les clients.</span><span class="sxs-lookup"><span data-stu-id="ffb76-115">You can use self-signed certificates, but you will need to update the clients.</span></span>

-   <span data-ttu-id="ffb76-116">Lorsque vous configurez des serveurs IIS pour utiliser le protocole HTTPs pour la diffusion en continu, vous devez configurer SSL (Secure Sockets Layer) sur le serveur IIS et approvisionner le certificat du serveur.</span><span class="sxs-lookup"><span data-stu-id="ffb76-116">When configuring IIS servers to use the HTTPS protocol for streaming, you will need to set up Secure Sockets Layer (SSL) on the IIS server and provision the certificate for the server.</span></span> <span data-ttu-id="ffb76-117">Les clients devront également être configurés de manière à approuver l’autorité de certification racine qui a émis le certificat de serveur.</span><span class="sxs-lookup"><span data-stu-id="ffb76-117">The clients will also need to be configured to trust the root certification authority that issued the server certificate.</span></span>

-   <span data-ttu-id="ffb76-118">L’authentification Kerberos a été ajoutée à la virtualisation d’application Microsoft comme mécanisme d’authentification par défaut.</span><span class="sxs-lookup"><span data-stu-id="ffb76-118">Kerberos authentication has been added to Microsoft Application Virtualization as the default authentication mechanism.</span></span> <span data-ttu-id="ffb76-119">Les versions antérieures étaient réutilisables avec NTLM v2 pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="ffb76-119">Earlier versions relied upon NTLM V2 for authentication.</span></span> <span data-ttu-id="ffb76-120">L’authentification Kerberos renforce la sécurité de la communication entre le client et le serveur de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="ffb76-120">Using Kerberos Authentication strengthens the security of the communication between the client and the Application Virtualization server.</span></span> <span data-ttu-id="ffb76-121">Lors de l’initialisation d’une connexion à partir du client, le serveur de virtualisation des applications vérifie le ticket de session avec le centre de distribution principal.</span><span class="sxs-lookup"><span data-stu-id="ffb76-121">When a connection has been initiated from the client, the Application Virtualization Server verifies the session ticket with the Key Distribution Center (KDC).</span></span>

-   <span data-ttu-id="ffb76-122">En raison de la prise en charge de l’utilisation des certificats de serveur et de l’utilisation des protocoles RTSP ou HTTPs, vous pouvez désormais prendre en charge des clients en dehors du réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ffb76-122">Because of the support for using server certificates and using the RTSPS or HTTPS protocols, you can now support clients outside of the corporate network.</span></span> <span data-ttu-id="ffb76-123">Cela peut vous aider à éviter que les utilisateurs mobiles aient configuré une connexion sécurisée au réseau d’entreprise (VPN, RAS, etc.) avant de lancer des applications de virtualisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="ffb76-123">This can help eliminate the need for mobile users to set up a secure connection to the corporate network (VPN, RAS, and so on) prior to launching Application Virtualization provisioned applications.</span></span>

<span data-ttu-id="ffb76-124">Voici d’autres considérations importantes en matière de sécurité à prendre en compte:</span><span class="sxs-lookup"><span data-stu-id="ffb76-124">Other important security considerations to consider include the following:</span></span>

-   <span data-ttu-id="ffb76-125">Veillez à toujours mettre à jour et à protéger les serveurs.</span><span class="sxs-lookup"><span data-stu-id="ffb76-125">Always keep servers fully updated and protected.</span></span>

-   <span data-ttu-id="ffb76-126">Pour ajouter un certificat afin d’offrir des communications plus sûres au serveur de gestion des applications, les critères suivants doivent être satisfaits:</span><span class="sxs-lookup"><span data-stu-id="ffb76-126">To add a certificate to enable more secure communications to the Application Virtualization Management Server, the following criteria must be met:</span></span>

    -   <span data-ttu-id="ffb76-127">L’utilisateur qui va ajouter le certificat doit être administrateur sur le serveur sur lequel se trouve le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="ffb76-127">The user who will be adding the certificate must be an administrator on the server where the certificate store is located.</span></span>

    -   <span data-ttu-id="ffb76-128">Le service serveur doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="ffb76-128">The server service must be started.</span></span>

    -   <span data-ttu-id="ffb76-129">Le port 139 du serveur de gestion doit être ouvert au service Web server’sIP.</span><span class="sxs-lookup"><span data-stu-id="ffb76-129">Port 139 on the Management Server must be open to the Web Service server’sIP.</span></span>

-   <span data-ttu-id="ffb76-130">Utilisez les listes de contrôle d’accès (ACL) pour vous assurer que les packages d’application et tous les fichiers de package sont protégés et ne peuvent pas être falsifiés.</span><span class="sxs-lookup"><span data-stu-id="ffb76-130">Use access control lists (ACLs) to ensure that the application packages and all package files are protected and cannot be tampered.</span></span> <span data-ttu-id="ffb76-131">Les listes de Contrã’le d’accès restreignent l’accès à l’emplacement ou au dossier où vous stockez les packages, autorisant uniquement l’accès à certains comptes.</span><span class="sxs-lookup"><span data-stu-id="ffb76-131">ACLs restrict access to the location or folder where you store the packages, allowing access only to certain accounts.</span></span>

-   <span data-ttu-id="ffb76-132">Vérifiez que le canal entre le serveur de gestion de la virtualisation des applications et la base de données est sécurisé (par exemple, en utilisant IPsec).</span><span class="sxs-lookup"><span data-stu-id="ffb76-132">Make sure that the channel between the Application Virtualization Management Server and the database is secured—for example, by using IPsec.</span></span>

-   <span data-ttu-id="ffb76-133">Si les packages sont stockés sur un réseau SAN ou NAS, assurez-vous que la connexion entre le périphérique de stockage central et les serveurs de virtualisation des applications est assurée.</span><span class="sxs-lookup"><span data-stu-id="ffb76-133">If packages are stored on a SAN or NAS, ensure the connection between the central storage device and the Application Virtualization Servers is protected.</span></span>

-   <span data-ttu-id="ffb76-134">Tous les canaux de communication vers le client doivent être protégés (y compris les connexions au serveur de publication, le serveur de virtualisation des applications, ainsi que le chemin d’accès aux fichiers OSD et ICO) en utilisant un protocole tel que HTTPs ou IPsec.</span><span class="sxs-lookup"><span data-stu-id="ffb76-134">All communication channels to the client should be protected—including connections to the publishing server, the Application Virtualization Server, and the path to the OSD and ICO files—by using a protocol such as HTTPS or IPsec.</span></span> 

-   <span data-ttu-id="ffb76-135">Les autorisations client doivent être configurées pour vous assurer que les packages ne peuvent pas être falsifiés par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ffb76-135">Client permissions should be configured to help ensure that packages cannot be tampered with by users.</span></span> <span data-ttu-id="ffb76-136">Il est particulièrement important que vous ne soyez pas autorisé à autoriser les utilisateurs à ajouter ou à mettre à jour des packages sur des systèmes, tels que des serveurs d’hôte de session Bureau à distance (RDSession) partagés avec plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ffb76-136">It is especially important that you do not grant users permission to add or update packages on systems, such as Remote Desktop Session Host (RDSession Host) servers, that are shared with multiple users.</span></span>

-   <span data-ttu-id="ffb76-137">L’authentification Kerberos doit être autorisée sur les environnements de domaine ou de forêt pour que la console de gestion du serveur fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="ffb76-137">Kerberos authentication must be permitted across domain or forest environments for the Server Management Console to work correctly.</span></span>

-   <span data-ttu-id="ffb76-138">Cette version du logiciel n’est pas prise en charge par l’hébergement d’un serveur RTSP utilisant Kerberos et d’un serveur IIS Microsoft NTLM uniquement sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ffb76-138">This release of the software does not support hosting a Kerberos-based RTSP server and a Microsoft NTLM-only-based IIS server on the same computer.</span></span> <span data-ttu-id="ffb76-139">Pour héberger un serveur RTSP et un serveur IIS sur le même ordinateur, supprimez le SPN du serveur IIS et utilisez l’authentification NTLM.</span><span class="sxs-lookup"><span data-stu-id="ffb76-139">To host an RTSP server and an IIS server on the same computer, remove the SPN from the IIS server and use NTLM authentication.</span></span>

## <span data-ttu-id="ffb76-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffb76-140">Related topics</span></span>


[<span data-ttu-id="ffb76-141">Planification du déploiement du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ffb76-141">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 






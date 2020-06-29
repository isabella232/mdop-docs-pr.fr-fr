---
title: Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server
description: Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809030"
---
# <span data-ttu-id="33410-103">Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server</span><span class="sxs-lookup"><span data-stu-id="33410-103">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>


<span data-ttu-id="33410-104">Après avoir terminé le processus de mise en service des certificats et modifié les autorisations de clé privée pour prendre en charge l’installation de l’application-V, vous pouvez lancer le programme d’installation du serveur de gestion ou du serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="33410-104">After you complete the certificate provisioning process and change the private key permissions to support the App-V installation, you can launch the setup of the Management Server or the Streaming Server.</span></span> <span data-ttu-id="33410-105">Lors de l’installation, si un certificat est configuré avant d’exécuter le programme d’installation, l’Assistant affiche le certificat dans l’écran **mode de sécurité** de la connexion et, par défaut, la case à cocher **utiliser la sécurité améliorée** est activée.</span><span class="sxs-lookup"><span data-stu-id="33410-105">During setup, if a certificate is provisioned before running the setup program, the wizard displays the certificate in the **Connection Security Mode** screen and, by default, the **Use enhanced security** check box is selected.</span></span>

<span data-ttu-id="33410-106">**Remarques**  Sélectionnez le certificat configuré pour App-V s’il existe plusieurs certificats approvisionnés pour ce serveur.</span><span class="sxs-lookup"><span data-stu-id="33410-106">**Note** Select the certificate that was configured for App-V if there is more than one certificate provisioned for this server.</span></span>

 

<span data-ttu-id="33410-107">**Important**  Lors de la mise à niveau de la version 4,2 vers la version 4,5, le programme d’installation propose une option d’utilisation de la **sécurité améliorée**. Toutefois, la sélection de cette option ne désactive pas la diffusion en continu sur RTSP.</span><span class="sxs-lookup"><span data-stu-id="33410-107">**Important** When upgrading from version 4.2 to version 4.5, the setup has an option for **Use enhanced security**; however, selecting this option will not disable streaming over RTSP.</span></span> <span data-ttu-id="33410-108">Vous devez utiliser la console de gestion pour désactiver RTSP après l’installation.</span><span class="sxs-lookup"><span data-stu-id="33410-108">You must use the Management Console to disable RTSP after installation.</span></span>

 

<span data-ttu-id="33410-109">Sélectionnez le port TCP utilisé par le service pour les communications client.</span><span class="sxs-lookup"><span data-stu-id="33410-109">Select the TCP port that the service will use for client communications.</span></span> <span data-ttu-id="33410-110">Le port par défaut est TCP 322; Toutefois, vous pouvez remplacer le port par un port personnalisé pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="33410-110">The default port is TCP 322; however, you can change the port to a custom port for your environment.</span></span>

<span data-ttu-id="33410-111">Les étapes restantes de l’Assistant sont identiques à celles de déploiement d’une application ou d’un serveur de diffusion en continu sans utilisation de la fonctionnalité de **sécurité améliorée** .</span><span class="sxs-lookup"><span data-stu-id="33410-111">The remaining steps of the wizard are the same as if you were deploying an App-V Management or Streaming Server without using the **Enhanced security** feature.</span></span>

## <span data-ttu-id="33410-112">Configuration de certificats pour les environnements NLB</span><span class="sxs-lookup"><span data-stu-id="33410-112">Configuring Certificates for NLB Environments</span></span>


<span data-ttu-id="33410-113">Pour prendre en charge des entreprises de grande taille, le serveur de gestion est souvent placé dans un cluster d’équilibrage de charge réseau (NLB) pour prendre en charge un grand nombre de connexions.</span><span class="sxs-lookup"><span data-stu-id="33410-113">To support large enterprises, often the Management Server is placed into a Network Load Balancing (NLB) cluster to support the large number of connections.</span></span> <span data-ttu-id="33410-114">Cela nécessite au moins deux serveurs d’administration qui semblent être un serveur de gestion unique.</span><span class="sxs-lookup"><span data-stu-id="33410-114">This requires at least two Management Servers that appear to be a single Management Server.</span></span> <span data-ttu-id="33410-115">Lorsque votre environnement utilise un cluster NLB avec plusieurs serveurs de gestion, vous avez besoin d’une configuration avancée du certificat utilisé pour le cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="33410-115">When your environment uses an NLB cluster with several Management Servers, you need an advanced configuration of the certificate used for the NLB cluster.</span></span>

<span data-ttu-id="33410-116">Le certificat App-V est soumis à une autorité de certification qui est configurée sur un ordinateur exécutant Windows Server2003.</span><span class="sxs-lookup"><span data-stu-id="33410-116">The App-V certificate is submitted to a certification authority (CA) that is configured on a computer running Windows Server2003.</span></span> <span data-ttu-id="33410-117">Le SAN vous permet de vous connecter à un nom d’hôte de cluster de votre serveur de gestion NLB en utilisant un nom DNS (Domain Name System) qui peut différer du nom de l’ordinateur réel, car il peut y avoir jusqu’à 32 serveurs qui comprennent le cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="33410-117">The SAN lets you connect to a specific Management Server NLB cluster host name by using a Domain Name System (DNS) name that might differ from the actual computer names, because there can be up to 32 servers that comprise the NLB cluster.</span></span>

<span data-ttu-id="33410-118">Cette configuration est nécessaire uniquement lors de l’utilisation d’un cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="33410-118">This configuration is necessary only when using an NLB cluster.</span></span> <span data-ttu-id="33410-119">Lorsque le client se connecte au serveur, il se connecte à l’aide du nom de domaine complet (FQDN) du cluster NLB et non du nom de domaine complet d’un serveur individuel.</span><span class="sxs-lookup"><span data-stu-id="33410-119">When the client connects to the server, it will connect using the fully qualified domain name (FQDN) of the NLB cluster and not the FQDN of an individual server.</span></span> <span data-ttu-id="33410-120">Si vous n’ajoutez pas la propriété SAN avec le nom de domaine complet (FQDN) des nœuds serveur dans le groupe, toutes les connexions client ne correspondent pas, car le nom commun du certificat ne correspond pas au nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="33410-120">If you do not add the SAN property with the FQDN of the server nodes in the cluster, all client connections are refused because the common name of the certificate won’t match the server name.</span></span>

<span data-ttu-id="33410-121">Pour plus d’informations sur la configuration des certificats avec l’attribut SAN, voir <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="33410-121">For more detailed information about configuring certificates with the SAN attribute, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

## <span data-ttu-id="33410-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33410-122">Related topics</span></span>


[<span data-ttu-id="33410-123">Configuration de certificats pour prendre en charge la diffusion en continu sécurisée</span><span class="sxs-lookup"><span data-stu-id="33410-123">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

[<span data-ttu-id="33410-124">Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server</span><span class="sxs-lookup"><span data-stu-id="33410-124">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 






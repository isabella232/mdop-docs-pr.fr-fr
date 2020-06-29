---
title: Installation d'App-V Management Server ou Streaming Server en toute sécurité
description: Installation d'App-V Management Server ou Streaming Server en toute sécurité
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806662"
---
# <span data-ttu-id="3bf84-103">Installation d'App-V Management Server ou Streaming Server en toute sécurité</span><span class="sxs-lookup"><span data-stu-id="3bf84-103">Installing App-V Management Server or Streaming Server Securely</span></span>


<span data-ttu-id="3bf84-104">Les rubriques de cette section fournissent des informations sur l’installation d’une version de sécurité améliorée du serveur d’administration d’applications-V ou du serveur de streaming d’applications-V.</span><span class="sxs-lookup"><span data-stu-id="3bf84-104">The topics in this section provide information for installing an enhanced security version of the App-V Management Server or the App-V Streaming Server.</span></span>

<span data-ttu-id="3bf84-105">**Remarques**  Pour utiliser la sécurité améliorée (par exemple, Transport Layer Security ou TLS), l’installation ou la configuration d’une gestion d’application-V ou d’un serveur de diffusion en continu nécessite le mise en service d’un certificat X. 509 v3 sur le serveur App-V.</span><span class="sxs-lookup"><span data-stu-id="3bf84-105">**Note** Installing or configuring an App-V Management or Streaming Server to use enhanced security (for example, Transport Layer Security, or TLS) requires that an X.509 V3 certificate has been provisioned to the App-V server.</span></span>

 

<span data-ttu-id="3bf84-106">Lorsque vous préparez l’installation ou la configuration d’une gestion sécurisée ou d’un serveur de diffusion en continu, prenez en compte les exigences techniques suivantes:</span><span class="sxs-lookup"><span data-stu-id="3bf84-106">When you prepare to install or configure a secure Management or Streaming Server, consider the following technical requirements:</span></span>

-   <span data-ttu-id="3bf84-107">Le certificat doit être valide.</span><span class="sxs-lookup"><span data-stu-id="3bf84-107">The certificate must be valid.</span></span> <span data-ttu-id="3bf84-108">Si le certificat n’est pas valide, le client arrête la connexion.</span><span class="sxs-lookup"><span data-stu-id="3bf84-108">If the certificate is not valid, the client ends the connection.</span></span>

-   <span data-ttu-id="3bf84-109">Le certificat doit contenir l' *utilisation améliorée* de l’utilisation de la clé (EKU), authentification serveur (OID 1.3.6.1.5.5.7.3.1).</span><span class="sxs-lookup"><span data-stu-id="3bf84-109">The certificate must contain the correct *Enhanced Key Usage* (EKU)—Server Authentication (OID 1.3.6.1.5.5.7.3.1).</span></span> <span data-ttu-id="3bf84-110">Si ce n’est pas le cas, le client arrête la connexion.</span><span class="sxs-lookup"><span data-stu-id="3bf84-110">If the certificate does not contain this EKU, the client ends the connection.</span></span>

-   <span data-ttu-id="3bf84-111">Le nom de domaine complet (FQDN) du certificat doit correspondre au serveur sur lequel il est installé.</span><span class="sxs-lookup"><span data-stu-id="3bf84-111">The certificate fully qualified domain name (FQDN) must match the server on which it is installed.</span></span> <span data-ttu-id="3bf84-112">Par exemple, si le client appelle `RTSPS://Myserver.mycompany.com/content/MyApp.sft` et que le certificat **émis pour** le champ est défini sur `Server1.mycompany.com` , le client ne se connecte pas au serveur et la session se termine.</span><span class="sxs-lookup"><span data-stu-id="3bf84-112">For example, if the client is calling `RTSPS://Myserver.mycompany.com/content/MyApp.sft` and the certificate **Issued To** field is set to `Server1.mycompany.com`, the client will not connect to the server and the session ends.</span></span> <span data-ttu-id="3bf84-113">L’erreur est signalée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3bf84-113">The failure is reported to the user.</span></span>

    <span data-ttu-id="3bf84-114">**Remarques**  Si vous utilisez App-V dans un cluster d’équilibrage de charge réseau, vous devez configurer le certificat avec d’autres noms de sujet (San) pour prendre en charge les RTSP.</span><span class="sxs-lookup"><span data-stu-id="3bf84-114">**Note** If you are using App-V in a Network Load Balancing cluster, you must configure the certificate with Subject Alternate Names (SANs) to support RTSPS.</span></span> <span data-ttu-id="3bf84-115">Pour plus d’informations sur la configuration de l’autorité de certification et la création de certificats avec des réseaux SAN, voir <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="3bf84-115">For information about configuring the certification authority (CA) and creating certificates with SANs, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

     

-   <span data-ttu-id="3bf84-116">Le client et le serveur doivent faire confiance à l’autorité de certification racine; l’autorité de certification émettant le certificat au serveur App-V doit être approuvée par le client se connectant au serveur.</span><span class="sxs-lookup"><span data-stu-id="3bf84-116">The client and the server need to trust the root CA—The CA issuing the certificate to the App-V server must by trusted by the client connecting to the server.</span></span> <span data-ttu-id="3bf84-117">Si ce n’est pas le cas, le client arrête la connexion.</span><span class="sxs-lookup"><span data-stu-id="3bf84-117">If not, the client ends the connection.</span></span>

-   <span data-ttu-id="3bf84-118">La clé privée du certificat doit être modifiée pour permettre au compte de service App-V d’accéder au certificat.</span><span class="sxs-lookup"><span data-stu-id="3bf84-118">The certificate’s private key must have permissions changed to allow the App-V Service account to access the certificate.</span></span> <span data-ttu-id="3bf84-119">Par défaut, l’application-V utilise le compte de service réseau, et par défaut, le compte de service réseau n’a pas l’autorisation d’accéder à la clé privée, ce qui empêchera les connexions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="3bf84-119">By default, App-V uses the Network Service account, and by default, the Network Service account does not have permission to access the private key, which will prevent secure connections.</span></span>

## <span data-ttu-id="3bf84-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3bf84-120">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[<span data-ttu-id="3bf84-121">Configuration de certificats pour prendre en charge la diffusion en continu sécurisée</span><span class="sxs-lookup"><span data-stu-id="3bf84-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)  
<span data-ttu-id="3bf84-122">Fournit des informations sur l’obtention, la configuration et l’installation de certificats pour la prise en charge de la diffusion en continu sécurisée.</span><span class="sxs-lookup"><span data-stu-id="3bf84-122">Provides information about obtaining, configuring, and installing certificates to support secure streaming.</span></span>

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[<span data-ttu-id="3bf84-123">Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server</span><span class="sxs-lookup"><span data-stu-id="3bf84-123">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
<span data-ttu-id="3bf84-124">Fournit des procédures que vous pouvez utiliser pour modifier des clés dans Windows Server2003 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3bf84-124">Provides procedures you can use to modify keys in Windows Server2003 and Windows Server2008.</span></span>

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[<span data-ttu-id="3bf84-125">Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server</span><span class="sxs-lookup"><span data-stu-id="3bf84-125">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
<span data-ttu-id="3bf84-126">Fournit des informations sur la configuration des certificats pour la gestion des applications ou des serveurs de diffusion en continu, y compris des informations sur la configuration des certificats pour les environnements d’équilibrage de charge réseau.</span><span class="sxs-lookup"><span data-stu-id="3bf84-126">Provides information about configuring certificates for the App-V Management or Streaming Servers, including information about configuring certificates for Network Load Balancing environments.</span></span>

 

 






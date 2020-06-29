---
title: Configuration de certificats pour prendre en charge la diffusion en continu sécurisée
description: Configuration de certificats pour prendre en charge la diffusion en continu sécurisée
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809029"
---
# <span data-ttu-id="290ce-103">Configuration de certificats pour prendre en charge la diffusion en continu sécurisée</span><span class="sxs-lookup"><span data-stu-id="290ce-103">Configuring Certificates to Support Secure Streaming</span></span>


<span data-ttu-id="290ce-104">Par défaut, le service App-V s’exécute sous le compte service réseau.</span><span class="sxs-lookup"><span data-stu-id="290ce-104">By default, the App-V service runs under the Network Service account.</span></span> <span data-ttu-id="290ce-105">Toutefois, vous pouvez créer un compte de service dans les services de domaine Active Directory et remplacer le compte de service réseau par le compte de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="290ce-105">However, you can create a service account in Active Directory Domain Services and replace the Network Service account with the Active Directory Domain account.</span></span>

<span data-ttu-id="290ce-106">Le contexte de sécurité en vertu duquel le service s’exécute est important pour la configuration des communications sécurisées améliorées.</span><span class="sxs-lookup"><span data-stu-id="290ce-106">The security context under which the service runs is important for configuring enhanced secure communications.</span></span> <span data-ttu-id="290ce-107">Ce contexte de sécurité doit disposer d’autorisations de lecture pour la clé privée du certificat.</span><span class="sxs-lookup"><span data-stu-id="290ce-107">This security context must have read permissions for the certificate private key.</span></span> <span data-ttu-id="290ce-108">Lorsqu’une *demande de signature de certificat* (CSR) PKCS \ #10 est générée pour le serveur App-V, *il est appelé* et une clé privée est générée.</span><span class="sxs-lookup"><span data-stu-id="290ce-108">When a PKCS\#10 *Certificate Signing Request* (CSR) is generated for the App-V server, the Windows *Cryptographic Service Provider* is called and a private key is generated.</span></span> <span data-ttu-id="290ce-109">La clé privée est sécurisée, avec les autorisations accordées uniquement aux comptes système et administrateur.</span><span class="sxs-lookup"><span data-stu-id="290ce-109">The private key is secured with permissions given to the System and Administrator accounts only.</span></span>

<span data-ttu-id="290ce-110">Vous devez modifier les listes de contrôle d’accès (ACL) sur la clé privée pour autoriser la gestion de l’application-V ou du serveur de diffusion en continu à utiliser la clé privée pour une communication sécurisée TLS correcte.</span><span class="sxs-lookup"><span data-stu-id="290ce-110">You must modify the access control lists (ACLs) on the private key to let the App-V Management or Streaming Server access the private key required for successful TLS secured communication.</span></span>

## <span data-ttu-id="290ce-111">Obtention et installation d’un certificat</span><span class="sxs-lookup"><span data-stu-id="290ce-111">Obtaining and Installing a Certificate</span></span>


<span data-ttu-id="290ce-112">Les scénarios d’obtention et d’installation d’un certificat pour App-V sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="290ce-112">The scenarios for obtaining and installing a certificate for App-V are as follows:</span></span>

-   <span data-ttu-id="290ce-113">Infrastructure à clé publique (PKI) interne.</span><span class="sxs-lookup"><span data-stu-id="290ce-113">Internal public key infrastructure (PKI).</span></span>

-   <span data-ttu-id="290ce-114">Certificat tiers délivrant une autorité de certification (CA).</span><span class="sxs-lookup"><span data-stu-id="290ce-114">Third-party certificate issuing certification authority (CA).</span></span>

    <span data-ttu-id="290ce-115">**Remarques**  Si vous avez besoin d’obtenir un certificat auprès d’une autorité de certification tierce, suivez la documentation disponible sur le site Web de cette autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="290ce-115">**Note** If you need to obtain a certificate from a third-party CA, follow the documentation available on that CA’s Web site.</span></span>

     

<span data-ttu-id="290ce-116">Si une infrastructure PKI a été déployée, contactez les administrateurs d’infrastructure à clé publique pour obtenir un certificat conforme aux exigences décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="290ce-116">If a PKI infrastructure has been deployed, consult with the PKI administrators to acquire a certificate that complies with the requirements described in this topic.</span></span> <span data-ttu-id="290ce-117">Si aucune infrastructure PKI n’est disponible, utilisez une autorité de certification tierce pour obtenir un certificat valide.</span><span class="sxs-lookup"><span data-stu-id="290ce-117">If a PKI infrastructure is not available, use a third-party CA to obtain a valid certificate.</span></span>

<span data-ttu-id="290ce-118">Pour obtenir des instructions détaillées sur l’obtention et l’installation d’un certificat, voir <https://go.microsoft.com/fwlink/?LinkId=151969> .</span><span class="sxs-lookup"><span data-stu-id="290ce-118">For step-by-step guidance for obtaining and installing a certificate, see <https://go.microsoft.com/fwlink/?LinkId=151969>.</span></span>

## <span data-ttu-id="290ce-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="290ce-119">Related topics</span></span>


<span data-ttu-id="290ce-120">Configuration de certificats pour la prise en charge de la diffusion en continu sécurisé de [la modification des autorisations de clé privée pour le serveur de gestion ou le serveur de diffusion](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span><span class="sxs-lookup"><span data-stu-id="290ce-120">Configuring Certificates to Support Secure Streaming [How to Modify Private Key Permissions to Support Management Server or Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span></span>

 

 






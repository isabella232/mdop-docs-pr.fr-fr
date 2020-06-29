---
title: Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server
description: Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806942"
---
# <span data-ttu-id="8c662-103">Procédure de modification des autorisations de clé privée pour la prise en charge de Management Server ou Streaming Server</span><span class="sxs-lookup"><span data-stu-id="8c662-103">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>


<span data-ttu-id="8c662-104">Pour prendre en charge une installation App-V plus sécurisée, vous pouvez utiliser les procédures suivantes pour modifier les clés privées dans Windows Server2003 ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8c662-104">To support a more secure App-V installation, you can use the following procedures to modify private keys in either Windows Server2003 or Windows Server2008.</span></span> <span data-ttu-id="8c662-105">Pour modifier les autorisations de la clé privée, vous pouvez utiliser l’outil Kit de ressources Windows Server2003 `WinHttpCertCfg.exe` .</span><span class="sxs-lookup"><span data-stu-id="8c662-105">To modify the permissions of the private key, you can use the Windows Server2003 Resource Kit tool `WinHttpCertCfg.exe`.</span></span>

<span data-ttu-id="8c662-106">Pour Windows Server 2003, la procédure exige qu’un certificat qui répond aux conditions préalables répertoriées dans ce document soit installé sur l’ordinateur ou sur les ordinateurs sur lesquels vous installez la gestion de l’application-V ou du serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="8c662-106">For Windows Server2003, the procedure requires that a certificate that meets the prerequisites listed in this document is installed on the computer or computers on which you will install the App-V Management or Streaming Server.</span></span> <span data-ttu-id="8c662-107">Des informations supplémentaires sur l’utilisation de l' `WinHttpCertCfg.exe` outil sont disponibles à l’adresse <https://go.microsoft.com/fwlink/?LinkId=151981> .</span><span class="sxs-lookup"><span data-stu-id="8c662-107">Additional information about using the `WinHttpCertCfg.exe` tool is available at <https://go.microsoft.com/fwlink/?LinkId=151981>.</span></span>

<span data-ttu-id="8c662-108">Dans Windows Server 2008, le processus de modification des ACL sur la clé privée est beaucoup plus simple.</span><span class="sxs-lookup"><span data-stu-id="8c662-108">In Windows Server2008, the process of changing the ACLs on the private key is much simpler.</span></span> <span data-ttu-id="8c662-109">L’interface utilisateur du certificat peut être utilisée pour gérer les autorisations de clés privées.</span><span class="sxs-lookup"><span data-stu-id="8c662-109">The certificate’s user interface can be used to manage private key permissions.</span></span>

<span data-ttu-id="8c662-110">**Remarques**  Le contexte de sécurité par défaut est service réseau. Toutefois, un compte de domaine peut être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="8c662-110">**Note** The default security context is Network Service; however, a domain account can be used instead.</span></span>

 

**<span data-ttu-id="8c662-111">Pour gérer les clés privées dans Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="8c662-111">To manage private keys in Windows Server2003</span></span>**

1.  <span data-ttu-id="8c662-112">Sur l’ordinateur qui deviendra la gestion de l’App-V ou du serveur de diffusion en continu, tapez la commande suivante dans une invite de commandes pour répertorier les autorisations actuelles affectées à un certificat spécifique:</span><span class="sxs-lookup"><span data-stu-id="8c662-112">On the computer that will become the App-V Management or Streaming Server, type the following command in a command prompt to list the current permissions assigned to a specific certificate:</span></span>

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  <span data-ttu-id="8c662-113">Le cas échéant, modifiez les autorisations du certificat afin d’offrir un accès en lecture au contexte de sécurité qui sera utilisé pour la gestion ou le service de diffusion en continu:</span><span class="sxs-lookup"><span data-stu-id="8c662-113">If necessary, modify the permissions of the certificate to provide read access to the security context that will be used for Management or Streaming Service:</span></span>

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  <span data-ttu-id="8c662-114">Vérifiez que le contexte de sécurité a été correctement ajouté en indiquant les autorisations sur le certificat:</span><span class="sxs-lookup"><span data-stu-id="8c662-114">Verify that the security context was properly added by listing the permissions on the certificate:</span></span>

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**<span data-ttu-id="8c662-115">Pour gérer les clés privées dans Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c662-115">To manage private keys in Windows Server2008</span></span>**

1.  <span data-ttu-id="8c662-116">Créez une console MMC en utilisant le composant logiciel enfichable *certificats* qui cible le magasin de certificats de l' *ordinateur local* .</span><span class="sxs-lookup"><span data-stu-id="8c662-116">Create a Microsoft Management Console (MMC) with the *Certificates* snap-in that targets the *Local Machine* certificate store.</span></span>

2.  <span data-ttu-id="8c662-117">Développez la console MMC et sélectionnez **gérer les clés privées**.</span><span class="sxs-lookup"><span data-stu-id="8c662-117">Expand the MMC and select **Manage Private Keys**.</span></span>

3.  <span data-ttu-id="8c662-118">Dans l’onglet **sécurité** , ajoutez le compte **service réseau** avec accès **en lecture** .</span><span class="sxs-lookup"><span data-stu-id="8c662-118">On the **Security** tab, add the **Network Service** account with **Read** access.</span></span>

## <span data-ttu-id="8c662-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c662-119">Related topics</span></span>


[<span data-ttu-id="8c662-120">Configuration de certificats pour prendre en charge App-V Management Server ou Streaming Server</span><span class="sxs-lookup"><span data-stu-id="8c662-120">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[<span data-ttu-id="8c662-121">Configuration de certificats pour prendre en charge la diffusion en continu sécurisée</span><span class="sxs-lookup"><span data-stu-id="8c662-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

 

 






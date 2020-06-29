---
title: Configuration de certificats pour prendre en charge le service de gestion Web App-V
description: Configuration de certificats pour prendre en charge le service de gestion Web App-V
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809024"
---
# <span data-ttu-id="246bd-103">Configuration de certificats pour prendre en charge le service de gestion Web App-V</span><span class="sxs-lookup"><span data-stu-id="246bd-103">Configuring Certificates to Support the App-V Web Management Service</span></span>


<span data-ttu-id="246bd-104">Le service de gestion de site Web de l’application doit être configuré pour prendre en charge les connexions SSL pour sécuriser la communication.</span><span class="sxs-lookup"><span data-stu-id="246bd-104">The App-V Web Management Service must be configured to support SSL-based connections to help secure the communication.</span></span> <span data-ttu-id="246bd-105">Ce processus exige que le serveur Web ou l’ordinateur sur lequel le service de gestion est installé dispose d’un certificat délivré au service ou à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="246bd-105">This process requires that the Web server or computer on which the Management Service is installed has a certificate issued to the service or computer.</span></span>

<span data-ttu-id="246bd-106">Les scénarios suivants montrent comment obtenir un certificat à cette fin:</span><span class="sxs-lookup"><span data-stu-id="246bd-106">The following scenarios illustrate how to obtain a certificate for this purpose:</span></span>

1.  <span data-ttu-id="246bd-107">L’infrastructure de l’entreprise possède déjà une infrastructure à clé publique (PKI) qui publie automatiquement des certificats sur les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="246bd-107">The company infrastructure already has a public key infrastructure (PKI) in place that automatically issues certificates to computers.</span></span>

2.  <span data-ttu-id="246bd-108">L’infrastructure de l’entreprise possède déjà une infrastructure PKI, même si elle n’émet pas automatiquement de certificats pour les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="246bd-108">The company infrastructure already has a PKI in place, although it does not automatically issue certificates to computers.</span></span>

3.  <span data-ttu-id="246bd-109">Aucune PKI n’est en place pour l’infrastructure de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="246bd-109">The company infrastructure has no PKI in place.</span></span>

<span data-ttu-id="246bd-110">Dans chacun des scénarios ci-dessus, la méthode d’obtention d’un certificat est différente, mais le résultat final est le même.</span><span class="sxs-lookup"><span data-stu-id="246bd-110">In each of the preceding scenarios, the method for obtaining a certificate is different, but the end result is the same.</span></span> <span data-ttu-id="246bd-111">L’administrateur doit attribuer un certificat au site Web IIS par défaut et configurer le service de gestion des applications Web App-V pour exiger des communications sécurisées.</span><span class="sxs-lookup"><span data-stu-id="246bd-111">The administrator must assign a certificate to the IIS Default Web Site and configure the App-V Web Management Service to require secure communications.</span></span>

<span data-ttu-id="246bd-112">**Important**  Le nom du certificat doit correspondre au nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="246bd-112">**Important** The name of the certificate must match the name of the server.</span></span> <span data-ttu-id="246bd-113">Il est recommandé d’utiliser des noms de domaine complets (FQDN) pour le nom usuel du certificat.</span><span class="sxs-lookup"><span data-stu-id="246bd-113">It is a best practice to use fully qualified domain names (FQDNs) for the common name of the certificate.</span></span>

 

<span data-ttu-id="246bd-114">App-V peut utiliser les serveurs IIS pour prendre en charge différentes configurations d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="246bd-114">App-V can use IIS servers to support different infrastructure configurations.</span></span> <span data-ttu-id="246bd-115">Pour plus d’informations sur la configuration des serveurs IIS pour la prise en charge des HTTPs, voir <https://go.microsoft.com/fwlink/?LinkId=151972> .</span><span class="sxs-lookup"><span data-stu-id="246bd-115">For more information about configuring IIS servers to support HTTPS, see <https://go.microsoft.com/fwlink/?LinkId=151972>.</span></span>

## <span data-ttu-id="246bd-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="246bd-116">Related topics</span></span>


[<span data-ttu-id="246bd-117">Comment installer et configurer App-V Management Console pour un environnement plus sécurisé</span><span class="sxs-lookup"><span data-stu-id="246bd-117">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 






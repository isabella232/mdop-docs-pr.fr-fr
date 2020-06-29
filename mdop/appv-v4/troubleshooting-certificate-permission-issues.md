---
title: Résolution des problèmes d'autorisation de certificat
description: Résolution des problèmes d'autorisation de certificat
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806214"
---
# <span data-ttu-id="10850-103">Résolution des problèmes d'autorisation de certificat</span><span class="sxs-lookup"><span data-stu-id="10850-103">Troubleshooting Certificate Permission Issues</span></span>


<span data-ttu-id="10850-104">Après l’installation de App-V 4.5, si la clé privée n’a pas été configurée à l’aide de la liste de contrôle d’accès correcte pour le service réseau, un événement est consigné dans le journal des événements Windows et une entrée est placée dans le `Sft-server.log` fichier.</span><span class="sxs-lookup"><span data-stu-id="10850-104">After the installation of App-V4.5, if the private key has not been configured with the proper ACL for the Network Service, an event is logged in the NT Event Log and an entry is placed in the `Sft-server.log` file.</span></span>

## <span data-ttu-id="10850-105">Messages d’erreur</span><span class="sxs-lookup"><span data-stu-id="10850-105">Error Messages</span></span>


### <span data-ttu-id="10850-106">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="10850-106">Windows Server2003</span></span>

<span data-ttu-id="10850-107">ID d’événement 36870: une erreur irrécupérable s’est produite lors d’une tentative d’accès à la clé privée d’informations d’identification du serveur SSL.</span><span class="sxs-lookup"><span data-stu-id="10850-107">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="10850-108">Le code d’erreur renvoyé par le module cryptographique est 0x80090016.</span><span class="sxs-lookup"><span data-stu-id="10850-108">The error code returned from the cryptographic module is 0x80090016.</span></span>

### <span data-ttu-id="10850-109">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10850-109">Windows Server2008</span></span>

<span data-ttu-id="10850-110">ID d’événement 36870: une erreur irrécupérable s’est produite lors d’une tentative d’accès à la clé privée d’informations d’identification du serveur SSL.</span><span class="sxs-lookup"><span data-stu-id="10850-110">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="10850-111">Le code d’erreur renvoyé par le module cryptographique est 0x8009030d.</span><span class="sxs-lookup"><span data-stu-id="10850-111">The error code returned from the cryptographic module is 0x8009030d.</span></span>

## <span data-ttu-id="10850-112">SFT-Server. log</span><span class="sxs-lookup"><span data-stu-id="10850-112">Sft-server.log</span></span>


<span data-ttu-id="10850-113">Le message d’erreur suivant est placé dans le `sft-server.log` fichier situé dans le `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` répertoire:</span><span class="sxs-lookup"><span data-stu-id="10850-113">The following error is placed in the `sft-server.log` file located in the `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` directory:</span></span>

<span data-ttu-id="10850-114">Le certificat n’a pas pu être chargé.</span><span class="sxs-lookup"><span data-stu-id="10850-114">Certificate could not be loaded.</span></span> <span data-ttu-id="10850-115">Code d’erreur \ [-2146893043 \].</span><span class="sxs-lookup"><span data-stu-id="10850-115">Error code \[-2146893043\].</span></span> <span data-ttu-id="10850-116">Assurez-vous que le compte de service réseau dispose de l’accès approprié au certificat et au fichier de clé privée correspondant.</span><span class="sxs-lookup"><span data-stu-id="10850-116">Make sure that the Network Service account has proper access to the certificate and its corresponding private key file.</span></span>

 

 






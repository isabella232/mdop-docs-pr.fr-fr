---
title: Configuration de Management ou Streaming Server pour sécuriser les communications post-installation
description: Configuration de Management ou Streaming Server pour sécuriser les communications post-installation
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809018"
---
# <span data-ttu-id="38853-103">Configuration de Management ou Streaming Server pour sécuriser les communications post-installation</span><span class="sxs-lookup"><span data-stu-id="38853-103">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>


<span data-ttu-id="38853-104">Si le certificat approprié n’a pas été approvisionné avant l’installation du serveur de gestion des applications-V ou du serveur de streaming d’applications-V, l’application-V peut être configurée pour une sécurité renforcée après l’installation initiale.</span><span class="sxs-lookup"><span data-stu-id="38853-104">If the proper certificate was not provisioned before the installation of the App-V Management Server or the App-V Streaming Server, App-V can be configured for enhanced security after the initial installation.</span></span> <span data-ttu-id="38853-105">Vous pouvez configurer le serveur de gestion de l’application-V par le biais de la console de gestion App-V.</span><span class="sxs-lookup"><span data-stu-id="38853-105">You can configure the App-V Management Server through the App-V Management Console.</span></span> <span data-ttu-id="38853-106">Toutefois, le serveur de streaming App-V est géré par le biais du Registre.</span><span class="sxs-lookup"><span data-stu-id="38853-106">However, the App-V Streaming Server is managed through the registry.</span></span> <span data-ttu-id="38853-107">Dans les deux cas, le certificat doit inclure l' *utilisation de la clé étendue* (EKU) appropriée pour l’authentification du serveur et le service réseau doit avoir accès en lecture à la clé privée.</span><span class="sxs-lookup"><span data-stu-id="38853-107">In either case, the certificate must include the proper *extended key usage* (EKU) for Server authentication and the Network Service must have read access to the private key.</span></span>

## <span data-ttu-id="38853-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="38853-108">In This Section</span></span>


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[<span data-ttu-id="38853-109">Procédure pour configurer la sécurité post-installation de Management Server</span><span class="sxs-lookup"><span data-stu-id="38853-109">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)  
<span data-ttu-id="38853-110">Fournit une procédure qui peut être effectuée après l’installation, à l’aide de la console de gestion des applications pour ajouter le certificat et configurer le serveur de gestion App-V pour une sécurité renforcée.</span><span class="sxs-lookup"><span data-stu-id="38853-110">Provides a procedure that can be performed post-installation, using the App-V Management Console, to add the certificate and configure the App-V Management Server for enhanced security.</span></span>

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[<span data-ttu-id="38853-111">Procédure pour configurer la sécurité post-installation de Streaming Server</span><span class="sxs-lookup"><span data-stu-id="38853-111">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)  
<span data-ttu-id="38853-112">Fournit une procédure qui peut être effectuée après l’installation, ajouter le certificat et configurer le serveur de streaming App-V pour renforcer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="38853-112">Provides a procedure that can be performed post-installation, to add the certificate and configure the App-V Streaming Server for enhanced security.</span></span>

<a href="" id="troubleshooting-certificate-permission-issues"></a>[<span data-ttu-id="38853-113">Résolution des problèmes d'autorisation de certificat</span><span class="sxs-lookup"><span data-stu-id="38853-113">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)  
<span data-ttu-id="38853-114">Fournit des conseils de dépannage pour le moment où la clé privée n’a pas été configurée à l’aide de la liste de contrôle d’accès appropriée pour le service réseau.</span><span class="sxs-lookup"><span data-stu-id="38853-114">Provides troubleshooting guidance for when the private key has not been configured with the proper ACL for the Network Service.</span></span>

 

 






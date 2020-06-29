---
title: Configuration d'App-V pour l'administration sécurisée
description: Configuration d'App-V pour l'administration sécurisée
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809035"
---
# <span data-ttu-id="15a5b-103">Configuration d'App-V pour l'administration sécurisée</span><span class="sxs-lookup"><span data-stu-id="15a5b-103">Configuring App-V for Secure Administration</span></span>


<span data-ttu-id="15a5b-104">Dans un environnement où les opérations d’administration sécurisées sont importantes, App-V autorise une communication sécurisée entre le service de gestion des applications Web de l’application et la console de gestion de l’application-V.</span><span class="sxs-lookup"><span data-stu-id="15a5b-104">In an environment where securing administrative operations is important, App-V allows for secure communication between the App-V Web Management Service and the App-V Management Console.</span></span> <span data-ttu-id="15a5b-105">Étant donné que le service de gestion est une application basée sur le Web, il est nécessaire de sécuriser l’application serveur de gestion des applications sur le serveur Web qui héberge le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="15a5b-105">Because the Management Service is a Web-based application, it requires securing the App-V Management Server application on the Web server that hosts the Management Service.</span></span> <span data-ttu-id="15a5b-106">Comme le montre l’illustration suivante, ce processus inclut l’utilisation de HTTPs pour la communication et la configuration du serveur IIS pour autoriser uniquement l’authentification intégrée à Windows.</span><span class="sxs-lookup"><span data-stu-id="15a5b-106">As shown in the following illustration, this process includes using HTTPS for communication and configuring the IIS server to allow only Windows Integrated Authentication.</span></span>

![configuration du réseau de service Web de l’application v](images/appvmgmtwebservice.gif)

<span data-ttu-id="15a5b-108">Le service de gestion des applications Web App-V est installé en tant qu’application Web sur IIS.</span><span class="sxs-lookup"><span data-stu-id="15a5b-108">The App-V Web Management Service is installed as a Web-based application on IIS.</span></span> <span data-ttu-id="15a5b-109">Pour que le service de gestion des sites Web prenne en charge les connexions sécurisées (SSL) entre la console de gestion des applications et le service de gestion des sites Web, vous devez configurer le serveur IIS sur lequel le service de gestion des sites Web est installé et configurer la console de gestion des applications V.</span><span class="sxs-lookup"><span data-stu-id="15a5b-109">For the Web Management Service to support secure (SSL) connections between the App-V Management Console and the Web Management Service, you will need to configure the IIS server where the Web Management Service is installed and configure the App-V Management Console.</span></span>

## <span data-ttu-id="15a5b-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="15a5b-110">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[<span data-ttu-id="15a5b-111">Configuration de certificats pour prendre en charge le service de gestion Web App-V</span><span class="sxs-lookup"><span data-stu-id="15a5b-111">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)  
<span data-ttu-id="15a5b-112">Fournit des informations utiles sur la configuration des certificats pour la prise en charge des connexions SSL, pour vous aider à sécuriser la communication pour le service de gestion des applications Web App-V.</span><span class="sxs-lookup"><span data-stu-id="15a5b-112">Provides helpful information about configuring certificates to support SSL-based connections, to help secure communication for the App-V Web Management Service.</span></span>

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[<span data-ttu-id="15a5b-113">Comment installer et configurer App-V Management Console pour un environnement plus sécurisé</span><span class="sxs-lookup"><span data-stu-id="15a5b-113">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
<span data-ttu-id="15a5b-114">Fournit une procédure pas à pas de connexion à un service de gestion des applications Web App-V via une connexion sécurisée.</span><span class="sxs-lookup"><span data-stu-id="15a5b-114">Provides a step-by-step procedure for connecting to an App-V Web Management Service by using a secure connection.</span></span>

 

 






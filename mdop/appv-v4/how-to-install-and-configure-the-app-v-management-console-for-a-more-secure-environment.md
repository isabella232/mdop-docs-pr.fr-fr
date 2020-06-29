---
title: Comment installer et configurer App-V Management Console pour un environnement plus sécurisé
description: Comment installer et configurer App-V Management Console pour un environnement plus sécurisé
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807081"
---
# <span data-ttu-id="dc29e-103">Comment installer et configurer App-V Management Console pour un environnement plus sécurisé</span><span class="sxs-lookup"><span data-stu-id="dc29e-103">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>


<span data-ttu-id="dc29e-104">L’installation par défaut de la console de gestion App-V prend en charge les communications sécurisées.</span><span class="sxs-lookup"><span data-stu-id="dc29e-104">The default installation of the App-V Management Console includes support for secure communications.</span></span> <span data-ttu-id="dc29e-105">Chaque console de gestion est configurée sur une base par connexion lorsque la console est démarrée pour la première fois ou lors d’une connexion à un service de gestion des applications Web supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="dc29e-105">Each Management Console is configured on a per-connection basis when the console is started for the first time or when connecting to an additional App-V Web Management Service.</span></span> <span data-ttu-id="dc29e-106">La configuration par défaut utilise SSL via le port TCP 443.</span><span class="sxs-lookup"><span data-stu-id="dc29e-106">The default configuration uses SSL over TCP port 443.</span></span> <span data-ttu-id="dc29e-107">Vous pouvez modifier le numéro de port si le numéro de port a été modifié sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="dc29e-107">You can change the port number if the port number was modified on the server.</span></span> <span data-ttu-id="dc29e-108">Vous pouvez utiliser la procédure suivante pour vous connecter à un service de gestion des applications Web App-V via une connexion sécurisée.</span><span class="sxs-lookup"><span data-stu-id="dc29e-108">You can use the following procedure to connect to an App-V Web Management Service by using a secure connection.</span></span>

**<span data-ttu-id="dc29e-109">Se connecter à un service de gestion d’application-V à l’aide d’une connexion SSL</span><span class="sxs-lookup"><span data-stu-id="dc29e-109">How to Connect to an App-V Management Service by Using an SSL Connection</span></span>**

1.  <span data-ttu-id="dc29e-110">Démarrez la console de gestion Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="dc29e-110">Start the Application Virtualization Management Console.</span></span>

2.  <span data-ttu-id="dc29e-111">Cliquez sur **configurer la connexion** dans le volet actions de la console.</span><span class="sxs-lookup"><span data-stu-id="dc29e-111">Click **Configure Connection** in the actions pane of the console.</span></span>

3.  <span data-ttu-id="dc29e-112">Entrez le **nom d’hôte du service Web**, puis vérifiez que l’option **utiliser une connexion sécurisée** est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="dc29e-112">Type the **Web Service Host Name**, and ensure that **Use Secure Connection** is selected.</span></span>

    <span data-ttu-id="dc29e-113">**Important**  Le nom fourni dans le nom d’hôte du service Web doit correspondre au nom usuel du certificat ou la connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="dc29e-113">**Important** The name provided in the Web Service Host Name must match the common name on the certificate, or the connection will fail.</span></span>

     

4.  <span data-ttu-id="dc29e-114">Sélectionnez les informations d’identification appropriées, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc29e-114">Select the appropriate login credentials, and click **OK**.</span></span>

## <span data-ttu-id="dc29e-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc29e-115">Related topics</span></span>


[<span data-ttu-id="dc29e-116">Configuration de certificats pour prendre en charge le service de gestion Web App-V</span><span class="sxs-lookup"><span data-stu-id="dc29e-116">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 






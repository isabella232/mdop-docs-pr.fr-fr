---
title: Procédure pour configurer le client en mode de fonctionnement hors connexion
description: Procédure pour configurer le client en mode de fonctionnement hors connexion
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807258"
---
# <span data-ttu-id="92d62-103">Procédure pour configurer le client en mode de fonctionnement hors connexion</span><span class="sxs-lookup"><span data-stu-id="92d62-103">How to Configure the Client for Disconnected Operation Mode</span></span>


<span data-ttu-id="92d62-104">Le mode de fonctionnement déconnecté permet au client de bureau App-V (App-V) ou au client de virtualisation des applications (App-V) d’exécuter des applications qui sont stockées dans le cache du système de fichiers du client lorsque le client ne peut pas se connecter au serveur de gestion App-V.</span><span class="sxs-lookup"><span data-stu-id="92d62-104">The disconnected operation mode enables the Application Virtualization (App-V) Desktop Client or the Application Virtualization (App-V) Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client cannot connect to the App-V Management Server.</span></span>

<span data-ttu-id="92d62-105">**Important**  Dans une grande organisation où de multiples serveurs de session Bureau à distance (hôtes de session de bureau à distance) sont liés dans une batterie de serveurs pour prendre en charge de nombreux utilisateurs, le recours à un serveur d’administration d’application unique pour la prise en charge de la batterie représente un point de défaillance unique.</span><span class="sxs-lookup"><span data-stu-id="92d62-105">**Important** In a large organization where multiple Remote Desktop Session Host (RD°Session Host) servers (formerly Terminal Servers) are linked in a farm to support many users, using a single App-V Management Server to support the farm represents a single point of failure.</span></span> <span data-ttu-id="92d62-106">Pour garantir une haute disponibilité à la prise en charge de la batterie d’hébergement RDSession, envisagez de lier deux ou plusieurs serveurs d’administration d’applications-V pour utiliser la même base de données.</span><span class="sxs-lookup"><span data-stu-id="92d62-106">To provide high availability to support the RDSession Host farm, consider linking two or more App-V Management Servers to use the same database.</span></span>

 

**<span data-ttu-id="92d62-107">Pour activer le mode de fonctionnement déconnecté</span><span class="sxs-lookup"><span data-stu-id="92d62-107">To enable disconnected operation mode</span></span>**

-   <span data-ttu-id="92d62-108">Définissez la valeur de clé de Registre suivante sur 1 pour activer le mode de fonctionnement hors connexion:</span><span class="sxs-lookup"><span data-stu-id="92d62-108">Set the following registry key value equal to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="92d62-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="92d62-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

**<span data-ttu-id="92d62-110">Pour définir un délai d’utilisation du mode de fonctionnement déconnecté</span><span class="sxs-lookup"><span data-stu-id="92d62-110">To set a time limit on disconnected operation mode use</span></span>**

1.  <span data-ttu-id="92d62-111">Attribuez la valeur 1 à la clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="92d62-111">Set the following registry key value to 1:</span></span>

    <span data-ttu-id="92d62-112">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="92d62-112">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

2.  <span data-ttu-id="92d62-113">Définissez la valeur de clé de Registre suivante sur le nombre de minutes pendant lequel vous voulez limiter le mode de fonctionnement déconnecté.</span><span class="sxs-lookup"><span data-stu-id="92d62-113">Set the following registry key value to the number of minutes you want to limit disconnected operation mode.</span></span> <span data-ttu-id="92d62-114">La plage de valeurs valide est 1 – 999999.</span><span class="sxs-lookup"><span data-stu-id="92d62-114">The valid range of values is 1–999999.</span></span> <span data-ttu-id="92d62-115">La valeur par défaut est 90 jours ou 129 600 minutes.</span><span class="sxs-lookup"><span data-stu-id="92d62-115">The default value is 90 days or 129,600 minutes.</span></span>

    <span data-ttu-id="92d62-116">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="92d62-116">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span></span>

**<span data-ttu-id="92d62-117">Pour configurer le client pour les services Bureau à distance pour le mode de fonctionnement déconnecté</span><span class="sxs-lookup"><span data-stu-id="92d62-117">To configure the Client for Remote Desktop Services for disconnected operation mode</span></span>**

1.  <span data-ttu-id="92d62-118">Définissez la valeur de clé de Registre suivante sur 1 pour activer le mode de fonctionnement hors connexion:</span><span class="sxs-lookup"><span data-stu-id="92d62-118">Set the following registry key value to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="92d62-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="92d62-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

2.  <span data-ttu-id="92d62-120">Définissez la valeur de clé de Registre suivante sur 0 (zéro) pour autoriser l’utilisation illimitée du mode de fonctionnement hors connexion:</span><span class="sxs-lookup"><span data-stu-id="92d62-120">Set the following registry key value to 0 (zero) to allow unlimited use of disconnected operation mode:</span></span>

    <span data-ttu-id="92d62-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="92d62-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

3.  <span data-ttu-id="92d62-122">Assurez-vous que tous les packages sont préchargés dans le cache pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="92d62-122">Ensure that all packages are preloaded into the cache to improve performance.</span></span>

## <span data-ttu-id="92d62-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92d62-123">Related topics</span></span>


[<span data-ttu-id="92d62-124">Mode de fonctionnement déconnecté</span><span class="sxs-lookup"><span data-stu-id="92d62-124">Disconnected Operation Mode</span></span>](disconnected-operation-mode.md)

[<span data-ttu-id="92d62-125">Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="92d62-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 






---
title: Mode de fonctionnement déconnecté
description: Mode de fonctionnement déconnecté
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808867"
---
# <span data-ttu-id="60b2f-103">Mode de fonctionnement déconnecté</span><span class="sxs-lookup"><span data-stu-id="60b2f-103">Disconnected Operation Mode</span></span>


<span data-ttu-id="60b2f-104">Les paramètres du mode de l’opération déconnectée, accessibles en cliquant avec le bouton droit sur le nœud de virtualisation de l' **application** , en sélectionnant **Propriétés**, puis en cliquant sur l’onglet **connectivité** , permettent au client de bureau virtuel d’applications ou au client pour les services Bureau à distance (anciennement services Terminal Server) d’exécuter des applications qui sont stockées dans le cache du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="60b2f-104">The disconnected operation mode settings—accessible by right-clicking the **Application Virtualization** node, selecting **Properties**, and clicking the **Connectivity** tab—enables the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client is unable to connect to the Application Virtualization Management Server.</span></span>

<span data-ttu-id="60b2f-105">Les raisons pour lesquelles il est impossible de se connecter au serveur sont les suivantes: échec du serveur, interruption du réseau ou déconnexion du réseau.</span><span class="sxs-lookup"><span data-stu-id="60b2f-105">Reasons for failure to connect to the server include server failure, network outage, or disconnection from the network.</span></span> <span data-ttu-id="60b2f-106">En cas d’échec, le client bascule automatiquement vers l’opération déconnectée.</span><span class="sxs-lookup"><span data-stu-id="60b2f-106">If any failure occurs, the client will automatically switch to disconnected operation.</span></span> <span data-ttu-id="60b2f-107">Après sa déconnexion, si le client a besoin de données supplémentaires du serveur pour continuer à exécuter une application ou si le délai d’expiration de l’opération déconnectée expire, le client tente de se reconnecter au serveur.</span><span class="sxs-lookup"><span data-stu-id="60b2f-107">After it is disconnected, if the client needs additional data from the server to continue to run an application or if the disconnected operation time-out expires, the client will attempt to reconnect to the server.</span></span> <span data-ttu-id="60b2f-108">Si cette tentative de connexion échoue, l’application est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="60b2f-108">If this connection attempt fails, the application will be shut down.</span></span>

<span data-ttu-id="60b2f-109">Par défaut, l’opération hors connexion est activée et le délai d’expiration est de 90 jours.</span><span class="sxs-lookup"><span data-stu-id="60b2f-109">By default, disconnected operation is enabled and the time-out is set to 90 days.</span></span> <span data-ttu-id="60b2f-110">La valeur du délai d’expiration est spécifiée en tant que nombre de jours pendant lequel vous voulez limiter le mode de fonctionnement déconnecté et vous pouvez entrer une valeur comprise entre 1 et 999.</span><span class="sxs-lookup"><span data-stu-id="60b2f-110">The time-out value is specified as the number of days you want to limit disconnected operation mode, and you can enter a value from 1–999.</span></span>

## <span data-ttu-id="60b2f-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60b2f-111">Related topics</span></span>


[<span data-ttu-id="60b2f-112">Procédure pour désactiver ou modifier des paramètres de mode de fonctionnement déconnecté</span><span class="sxs-lookup"><span data-stu-id="60b2f-112">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 






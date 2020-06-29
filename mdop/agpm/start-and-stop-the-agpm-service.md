---
title: Démarrer et arrêter le service AGPM
description: Démarrer et arrêter le service AGPM
author: dansimp
ms.assetid: 769aa0ce-224a-446f-9958-9518af4ad159
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 33e797182d49157da0fe8f36dce17b4b35cdd623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807461"
---
# <span data-ttu-id="40c5a-103">Démarrer et arrêter le service AGPM</span><span class="sxs-lookup"><span data-stu-id="40c5a-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="40c5a-104">Le service AGPM est un service Windows agissant en tant que proxy de sécurité, gérant l’accès client aux objets de stratégie de groupe (GPO) dans l’environnement d’archivage et de production.</span><span class="sxs-lookup"><span data-stu-id="40c5a-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="40c5a-105">**Important**  L’arrêt ou la désactivation du service AGPM empêche les clients d’AGPM d’exécuter des opérations (par exemple, les listes ou les modifications d’objets de stratégie de groupe) par le biais du serveur.</span><span class="sxs-lookup"><span data-stu-id="40c5a-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="40c5a-106">Un compte d’utilisateur ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le service AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="40c5a-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="40c5a-107">Pour démarrer ou arrêter le service AGPM</span><span class="sxs-lookup"><span data-stu-id="40c5a-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="40c5a-108">Sur l’ordinateur sur lequel Microsoft Advanced Group Policy Management-Server (et par conséquent le service AGPM) est installé, cliquez sur **Démarrer**, sur **panneau de configuration**, sur **Outils d’administration**, puis sur **services**.</span><span class="sxs-lookup"><span data-stu-id="40c5a-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="40c5a-109">Dans la liste des services, cliquez avec le bouton droit sur **service AGPM** et sélectionnez **Démarrer**, **redémarrer**ou **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="40c5a-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="40c5a-110">**Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="40c5a-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="40c5a-111">Cela peut empêcher le démarrage du service AGPM.</span><span class="sxs-lookup"><span data-stu-id="40c5a-111">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="40c5a-112">Pour modifier les paramètres du service, voir [gestion du service AGPM](managing-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="40c5a-112">To modify settings for the service, see [Managing the AGPM Service](managing-the-agpm-service.md).</span></span>

     

### <span data-ttu-id="40c5a-113">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="40c5a-113">Additional references</span></span>

-   [<span data-ttu-id="40c5a-114">Gestion du service AGPM</span><span class="sxs-lookup"><span data-stu-id="40c5a-114">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 






---
title: Démarrer et arrêter le service AGPM
description: Démarrer et arrêter le service AGPM
author: dansimp
ms.assetid: dcc9566c-c515-4fbe-b7f5-8ac030141307
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c254cc122c43262ff5ec4cb0bf5a5ab2c77fac3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808214"
---
# <span data-ttu-id="f7037-103">Démarrer et arrêter le service AGPM</span><span class="sxs-lookup"><span data-stu-id="f7037-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="f7037-104">Le service AGPM est un service Windows agissant en tant que proxy de sécurité, gérant l’accès client aux objets de stratégie de groupe (GPO) dans l’environnement d’archivage et de production.</span><span class="sxs-lookup"><span data-stu-id="f7037-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="f7037-105">**Important**  L’arrêt ou la désactivation du service AGPM empêche les clients d’AGPM d’exécuter des opérations (par exemple, les listes ou les modifications d’objets de stratégie de groupe) par le biais du serveur.</span><span class="sxs-lookup"><span data-stu-id="f7037-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM Clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="f7037-106">Un compte d’utilisateur ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le service AGPM) est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f7037-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="f7037-107">Pour démarrer ou arrêter le service AGPM</span><span class="sxs-lookup"><span data-stu-id="f7037-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="f7037-108">Sur l’ordinateur sur lequel Microsoft Advanced Group Policy Management-Server (et par conséquent le service AGPM) est installé, cliquez sur **Démarrer**, sur **panneau de configuration**, sur **Outils d’administration**, puis sur **services**.</span><span class="sxs-lookup"><span data-stu-id="f7037-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="f7037-109">Dans la liste des services, cliquez avec le bouton droit sur **service AGPM** et sélectionnez **Démarrer**, **redémarrer**ou **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="f7037-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="f7037-110">**Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f7037-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="f7037-111">Cela peut empêcher le démarrage du service AGPM.</span><span class="sxs-lookup"><span data-stu-id="f7037-111">Doing so can prevent the AGPM Service from starting.</span></span>

     

### <span data-ttu-id="f7037-112">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f7037-112">Additional references</span></span>

-   [<span data-ttu-id="f7037-113">Gestion du service AGPM</span><span class="sxs-lookup"><span data-stu-id="f7037-113">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm40.md)

 

 






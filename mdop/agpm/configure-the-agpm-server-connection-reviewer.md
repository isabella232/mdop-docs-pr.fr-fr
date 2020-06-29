---
title: Configurer la connexion au serveur AGPM
description: Configurer la connexion au serveur AGPM
author: dansimp
ms.assetid: 74e8f348-a8ed-4d69-a8e0-9c974aaeca2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83a2437ee8c2fe562141ff167cb85c6a06b7cefe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807698"
---
# <span data-ttu-id="5dfc0-103">Configurer la connexion au serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="5dfc0-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="5dfc0-104">Pour vous assurer que vous êtes connecté à l’archive centrale appropriée, vérifiez la configuration de la connexion au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="5dfc0-104">To ensure that you are connected to the correct central archive, review the configuration of the AGPM Server connection.</span></span> <span data-ttu-id="5dfc0-105">Si un administrateur AGPM (contrôle total) n’a pas configuré la connexion de serveur AGPM pour vous, vous devez le configurer manuellement.</span><span class="sxs-lookup"><span data-stu-id="5dfc0-105">If an AGPM Administrator (Full Control) has not configured the AGPM Server connection for you, then you must manually configure it.</span></span>

**<span data-ttu-id="5dfc0-106">Pour sélectionner un serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="5dfc0-106">To select an AGPM Server</span></span>**

1.  <span data-ttu-id="5dfc0-107">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5dfc0-107">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5dfc0-108">Dans le volet Détails, cliquez sur l’onglet **serveur AGPM** :</span><span class="sxs-lookup"><span data-stu-id="5dfc0-108">In the details pane, click the **AGPM Server** tab:</span></span>

    -   <span data-ttu-id="5dfc0-109">Si les options sous l’onglet **serveur AGPM** ne sont pas disponibles, cela a été configuré de manière centralisée par un administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="5dfc0-109">If the options on the **AGPM Server** tab are unavailable, they have been centrally configured by an AGPM Administrator.</span></span>

    -   <span data-ttu-id="5dfc0-110">Si les options sous l’onglet **serveur AGPM** sont disponibles, tapez le nom complet de l’ordinateur pour le serveur AGPM (par exemple, Server.contoso.com) et le port sur lequel le service AGPM écoute (par défaut, le port 4600).</span><span class="sxs-lookup"><span data-stu-id="5dfc0-110">If the options on the **AGPM Server** tab are available, type the fully-qualified computer name for the AGPM Server (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span> <span data-ttu-id="5dfc0-111">Cliquez sur **appliquer**, puis sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="5dfc0-111">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="5dfc0-112">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="5dfc0-112">Additional considerations</span></span>

-   <span data-ttu-id="5dfc0-113">Les serveurs AGPM sélectionnés déterminent les objets de stratégie de groupe qui s’affichent dans l’onglet **Sommaire** et à quel emplacement les paramètres de l’onglet **délégation de domaine** sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="5dfc0-113">The AGPM Servers selected determine which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="5dfc0-114">S’ils ne sont pas gérés de manière centralisée par le biais du modèle d’administration, chaque administrateur de stratégie de groupe doit configurer ce paramètre pour qu’il pointe vers le serveur AGPM du domaine.</span><span class="sxs-lookup"><span data-stu-id="5dfc0-114">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

### <span data-ttu-id="5dfc0-115">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="5dfc0-115">Additional references</span></span>

-   [<span data-ttu-id="5dfc0-116">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="5dfc0-116">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="5dfc0-117">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="5dfc0-117">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="5dfc0-118">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="5dfc0-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 






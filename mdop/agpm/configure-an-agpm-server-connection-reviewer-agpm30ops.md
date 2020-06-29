---
title: Configurer une connexion au serveur AGPM
description: Configurer une connexion au serveur AGPM
author: dansimp
ms.assetid: ae78dc74-111d-4509-b0a6-e8b8b451c22a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 50968d8b1b1eb5d464c6dbdb251354a9dc691d62
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807734"
---
# <span data-ttu-id="09e8f-103">Configurer une connexion au serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="09e8f-103">Configure an AGPM Server Connection</span></span>


<span data-ttu-id="09e8f-104">Pour vous assurer que vous êtes connecté à l’archive centrale appropriée, vérifiez la configuration de la connexion au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="09e8f-104">To ensure that you are connected to the correct central archive, review the configuration of the AGPM Server connection.</span></span> <span data-ttu-id="09e8f-105">Si un administrateur AGPM (contrôle total) n’a pas configuré de connexion de serveur AGPM pour vous, vous devez le configurer manuellement.</span><span class="sxs-lookup"><span data-stu-id="09e8f-105">If an AGPM Administrator (Full Control) has not configured an AGPM Server connection for you, then you must manually configure it.</span></span>

**<span data-ttu-id="09e8f-106">Pour sélectionner un serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="09e8f-106">To select an AGPM Server</span></span>**

1.  <span data-ttu-id="09e8f-107">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="09e8f-107">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="09e8f-108">Dans le volet Détails, cliquez sur l’onglet **serveur AGPM** :</span><span class="sxs-lookup"><span data-stu-id="09e8f-108">In the details pane, click the **AGPM Server** tab:</span></span>

    -   <span data-ttu-id="09e8f-109">Si les options sous l’onglet **serveur AGPM** ne sont pas disponibles, cela a été configuré de manière centralisée par un administrateur AGPM.</span><span class="sxs-lookup"><span data-stu-id="09e8f-109">If the options on the **AGPM Server** tab are unavailable, they have been centrally configured by an AGPM Administrator.</span></span>

    -   <span data-ttu-id="09e8f-110">Si les options sous l’onglet **serveur AGPM** sont disponibles, tapez le nom complet de l’ordinateur pour le serveur AGPM (par exemple, Server.contoso.com) et le port sur lequel le service AGPM écoute (par défaut, le port 4600).</span><span class="sxs-lookup"><span data-stu-id="09e8f-110">If the options on the **AGPM Server** tab are available, type the fully-qualified computer name for the AGPM Server (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span> <span data-ttu-id="09e8f-111">Cliquez sur **appliquer**, puis sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="09e8f-111">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="09e8f-112">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="09e8f-112">Additional considerations</span></span>

-   <span data-ttu-id="09e8f-113">Les serveurs AGPM sélectionnés déterminent les objets de stratégie de groupe qui s’affichent dans l’onglet **Sommaire** et à quel emplacement les paramètres de l’onglet **délégation de domaine** sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="09e8f-113">The AGPM Servers selected determine which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="09e8f-114">S’ils ne sont pas gérés de manière centralisée par le biais du modèle d’administration, chaque administrateur de stratégie de groupe doit configurer ce paramètre pour qu’il pointe vers le serveur AGPM du domaine.</span><span class="sxs-lookup"><span data-stu-id="09e8f-114">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

### <span data-ttu-id="09e8f-115">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="09e8f-115">Additional references</span></span>

-   [<span data-ttu-id="09e8f-116">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="09e8f-116">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="09e8f-117">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="09e8f-117">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="09e8f-118">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="09e8f-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 






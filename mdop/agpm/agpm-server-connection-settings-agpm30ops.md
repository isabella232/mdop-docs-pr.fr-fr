---
title: Paramètres de connexion du serveur AGPM
description: Paramètres de connexion du serveur AGPM
author: dansimp
ms.assetid: 5f03e397-b868-4c49-9cbf-a5f5d0ddcc39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ee1e67eb2c565bcf833314d82cdf611e2caa85
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804639"
---
# <span data-ttu-id="35704-103">Paramètres de connexion du serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="35704-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="35704-104">Vous pouvez utiliser les paramètres de modèle d’administration pour la gestion avancée de la stratégie de groupe pour configurer de manière centralisée les connexions serveur AGPM pour les administrateurs de stratégie de groupe pour lesquels un objet de stratégie de groupe avec ces paramètres est appliqué.</span><span class="sxs-lookup"><span data-stu-id="35704-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="35704-105">Les paramètres suivants sont disponibles sous User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM lors de la modification d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="35704-105">The following settings are available under User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="35704-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="35704-106">Setting</span></span></th>
<th align="left"><span data-ttu-id="35704-107">Effet</span><span class="sxs-lookup"><span data-stu-id="35704-107">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="35704-108">AGPM: spécifier le serveur AGPM par défaut (tous les domaines)</span><span class="sxs-lookup"><span data-stu-id="35704-108">AGPM: Specify default AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="35704-109">Ce paramètre de stratégie vous permet de spécifier un serveur AGPM par défaut pour tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="35704-109">This policy setting allows you to specify a default AGPM Server for all domains.</span></span> <span data-ttu-id="35704-110">Ce paramètre est utilisé uniquement par les clients AGPM et limite les administrateurs de stratégie de groupe à la connexion à une autre archive.</span><span class="sxs-lookup"><span data-stu-id="35704-110">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to another archive.</span></span> <span data-ttu-id="35704-111">Vous pouvez remplacer cette valeur par défaut pour des domaines individuels à l’aide du <strong> paramètre AGPM: spécifier les serveurs AGPM </strong> .</span><span class="sxs-lookup"><span data-stu-id="35704-111">You can override this default for individual domains using the <strong>AGPM: Specify AGPM Servers</strong> setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="35704-112">AGPM: spécifier les serveurs AGPM</span><span class="sxs-lookup"><span data-stu-id="35704-112">AGPM: Specify AGPM Servers</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="35704-113">Ce paramètre de stratégie vous permet de spécifier les serveurs AGPM pour des domaines individuels.</span><span class="sxs-lookup"><span data-stu-id="35704-113">This policy setting allows you to specify the AGPM Servers for individual domains.</span></span> <span data-ttu-id="35704-114">Ce paramètre est utilisé uniquement par les clients AGPM et limite les administrateurs de stratégie de groupe à la connexion à une autre Archive pour le domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="35704-114">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to a different archive for the specified domain.</span></span> <span data-ttu-id="35704-115">Pour spécifier un serveur AGPM par défaut, utilisez le <strong> paramètre AGPM: spécifiez le serveur AGPM par défaut (tous les domaines), </strong> puis utilisez ce paramètre de stratégie pour remplacer la valeur par défaut pour chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="35704-115">To specify a default AGPM Server, use the <strong>AGPM: Specify default AGPM Server (all domains)</strong> setting and use this policy setting to override the default on a per domain basis.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="35704-116">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="35704-116">Additional references</span></span>

-   [<span data-ttu-id="35704-117">Dossier Modèles d'administration</span><span class="sxs-lookup"><span data-stu-id="35704-117">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm30ops.md)

-   [<span data-ttu-id="35704-118">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="35704-118">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

 

 






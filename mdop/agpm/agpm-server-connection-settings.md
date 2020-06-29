---
title: Paramètres de connexion du serveur AGPM
description: Paramètres de connexion du serveur AGPM
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804663"
---
# <span data-ttu-id="6019c-103">Paramètres de connexion du serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="6019c-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="6019c-104">Vous pouvez utiliser les paramètres de modèle d’administration pour la gestion avancée de la stratégie de groupe pour configurer de manière centralisée les connexions serveur AGPM pour les administrateurs de stratégie de groupe pour lesquels un objet de stratégie de groupe avec ces paramètres est appliqué.</span><span class="sxs-lookup"><span data-stu-id="6019c-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="6019c-105">Les paramètres suivants sont disponibles sous User Configuration\\Administrative Templates\\Windows Components\\AGPM lors de la modification d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="6019c-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span> <span data-ttu-id="6019c-106">Si ce chemin d’accès n’est pas visible, cliquez avec le bouton droit sur **modèles d’administration**, puis ajoutez le modèle AGPM. admx ou AGPM. adm.</span><span class="sxs-lookup"><span data-stu-id="6019c-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6019c-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6019c-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="6019c-108">Effet</span><span class="sxs-lookup"><span data-stu-id="6019c-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6019c-109">Serveur AGPM (tous les domaines)</span><span class="sxs-lookup"><span data-stu-id="6019c-109">AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6019c-110">Si cette option est activée, vous configurez de manière centralisée une connexion de serveur AGPM pour une utilisation par tous les domaines et désactive les paramètres sous l' <strong> onglet serveur AGPM </strong> pour les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="6019c-110">If enabled, this setting centrally configures one AGPM Server connection for use by all domains and disables the settings on the <strong>AGPM Server</strong> tab for Group Policy administrators.</span></span> <span data-ttu-id="6019c-111">Pour plusieurs serveurs AGPM, configurez ce paramètre avec un serveur par défaut, puis configurez le <strong> paramètre serveur AGPM </strong> dans le modèle d’administration pour remplacer ce serveur par d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="6019c-111">For multiple AGPM Servers, configure this setting with a default server and then configure the <strong>AGPM Server</strong> setting in the Administrative template to override this server for other domains.</span></span></p>
<p><span data-ttu-id="6019c-112">Si elle est désactivée ou n’est pas configurée, les administrateurs de stratégie de groupe doivent sélectionner le serveur AGPM à afficher pour chaque domaine sous l' <strong> onglet serveur AGPM </strong> dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="6019c-112">If disabled or not configured, each Group Policy administrator must select the AGPM Server to display for each domain on the <strong>AGPM Server</strong> tab in AGPM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6019c-113">Serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="6019c-113">AGPM Server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6019c-114">Si ce paramètre est activé, il configure de manière centralisée plusieurs serveurs AGPM spécifiques au domaine, <strong> en remplaçant le paramètre serveur AGPM (tous les domaines) </strong> dans le modèle d’administration.</span><span class="sxs-lookup"><span data-stu-id="6019c-114">If enabled, this setting centrally configures multiple domain-specific AGPM Servers, overriding the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span> <span data-ttu-id="6019c-115">Si votre environnement nécessite uniquement un serveur AGPM unique, utilisez uniquement le <strong> paramètre serveur AGPM (tous les domaines) du </strong> modèle d’administration.</span><span class="sxs-lookup"><span data-stu-id="6019c-115">If your environment requires only a single AGPM Server, use only the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span></p>
<p><span data-ttu-id="6019c-116">Si ce paramètre est désactivé ou n’est pas configuré, le <strong> paramètre serveur AGPM (tous les domaines) du </strong> modèle d’administration configure la connexion au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="6019c-116">If disabled or not configured, the <strong>AGPM Server (all domains)</strong> setting in the Administrative template configures the AGPM Server connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6019c-117">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6019c-117">Additional references</span></span>

-   [<span data-ttu-id="6019c-118">Paramètres de modèles d'administration</span><span class="sxs-lookup"><span data-stu-id="6019c-118">Administrative Template Settings</span></span>](administrative-template-settings.md)

-   [<span data-ttu-id="6019c-119">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="6019c-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





